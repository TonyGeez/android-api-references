Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PeopleContract

```
class PeopleContract
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.provider.PeopleContract](PeopleContract.md) |

Defines the contract between client applications, People Directory applications (such as VoIP and messaging services), and the system's People Provider.

The People Provider acts as a central aggregator and caching repository for person and group identities across installed applications known as "People Directories". This contract establishes standard procedures for two primary developer audiences:

- **People Directory applications (VoIP and Messaging Applications):** Applications that supply contact definitions to the system by declaring a `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` registered with the manifest property `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Directory#DIRECTORY_PROPERTY:kotlin.String`. People Directory applications notify the system of data changes via notifyChange and handle interaction requests via `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Intents#ACTION_START_PEOPLE_INTERACTION:kotlin.String`.
- **Client applications (Queriers):** Applications (such as dialers, contacts apps, or system UI) that query available directories, retrieve aggregated person and group records, observe data changes, and request secure interaction intents (such as messaging, audio calling, or video calling).

### Overview

The interaction between People Directories, the People Provider, and client applications follows a standard lifecycle:

1. **Query:** A client application queries the People Provider with `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Persons#CONTENT_URI:android.net.Uri` or `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Groups#CONTENT_URI:android.net.Uri` for person or group records.
2. **Database lookup and fetch:** The People Provider immediately returns any records from the local database. If target records from a specific People Directory are missing or expired, the People Provider triggers debounced, scheduled background maintenance jobs to fetch data from the registered People Directory. Note that these scheduled jobs may not run immediately.
3. **Backfill and notify:** The People Provider stores the returned records in its local database and alerts the client application via a `https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#` on the notification URI (see `https://developer.android.com/reference/kotlin/android/provider/PeopleContract#EXTRA_NOTIFICATION_URI:kotlin.String`). The client application then re-queries to retrieve the updated records from the local database.
4. **Interaction:** To start an interaction (such as messaging, audio calling, or video calling), the client application requests a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` from the People Provider (see createPeopleInteractionRequest), which routes the request securely to the target People Directory application's interaction Activity.

### Implementing a People Directory

For applications wishing to integrate as a People Directory and surface their user network in system calling and messaging flows, follow these implementation requirements:

1. **Manifest Declaration:** Declare an exported `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#` in your package manifest. Within the provider declaration, include a `<property>` tag for `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Directory#DIRECTORY_PROPERTY:kotlin.String` set to `true` so the system discovers your service during app scanning:

   ```kotlin
   <code>&lt;provider android:name=".MyPeopleDirectoryProvider"
               android:authorities="com.example.app.people"
               android:exported="true"&gt;
         &lt;property android:name="android.content.PeopleDirectory" android:value="true" /&gt;
     &lt;/provider&gt;
     </code>
   ```
 You could also use `android:readPermission="android.permission.BIND_DIRECTORY_SEARCH"` to restrict access to the directory to the system only.

 **Note:** An application may register at most one People Directory. Packages declaring multiple directory providers are ignored by the system.
2. **Fulfilling Queries:** When the system queries your provider, it invokes query against paths matching `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Persons#CONTENT_URI:android.net.Uri` or `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Groups#CONTENT_URI:android.net.Uri` under your authority. The query bundle contains `https://developer.android.com/reference/kotlin/android/provider/PeopleContract#QUERY_ARG_QUERIES:kotlin.String`, a list of sub-query argument bundles specifying the matching criteria (for example, phone numbers, email addresses, or lookup keys via `https://developer.android.com/reference/kotlin/android/provider/PeopleContract#QUERY_ARG_SELECTION_TYPE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/provider/PeopleContract#QUERY_ARG_SELECTION_VALUE:kotlin.String`). Your provider must match these criteria against its app database and return a `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` populating standard columns:
 - For `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Persons#CONTENT_URI:android.net.Uri`, return: `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Persons#LOOKUP_KEY:kotlin.String` (required, stable opaque key), `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Persons#DISPLAY_NAME:kotlin.String`, `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Persons#PHOTO_URI:kotlin.String`, `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Persons#CAPABILITY:kotlin.String` (bitmask of `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Capability` flags), as well as `https://developer.android.com/reference/kotlin/android/provider/PeopleContract#QUERY_ARG_SELECTION_TYPE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/provider/PeopleContract#QUERY_ARG_SELECTION_VALUE:kotlin.String` corresponding to the matched query request.
 - For `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Groups#CONTENT_URI:android.net.Uri`, return: `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Groups#LOOKUP_KEY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Groups#DISPLAY_NAME:kotlin.String`, along with `https://developer.android.com/reference/kotlin/android/provider/PeopleContract#QUERY_ARG_SELECTION_TYPE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/provider/PeopleContract#QUERY_ARG_SELECTION_VALUE:kotlin.String`.
3. **Change Notifications:** Call notifyChange whenever a person or group record is added, modified, or removed in your service so the provider can update its local database. Call requestRefresh after large-scale state changes (such as completing an account sync or user log-outs).
4. **Handling User Interactions:** Declare an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` in your manifest with an intent filter matching `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Intents#ACTION_START_PEOPLE_INTERACTION:kotlin.String`. This Activity must declare `android:exported="true"` in the manifest to allow the People Provider to discover and launch it. It is highly recommended to protect this Activity with `android:readPermission="android.permission.BIND_DIRECTORY_SEARCH"` to restrict the creation of the Activity's `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` to the system only, so that it shares the same restriction as queries to the People Directory.

 When launched by a client's `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#`, read `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Intents#EXTRA_PEOPLE_INTERACTION_TYPE:kotlin.String` (such as voice call, video call, or message) and `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Intents#EXTRA_PEOPLE_QUERY_ARGS:kotlin.String` from the intent. To extract the target record from the query arguments bundle, retrieve the query list via `bundle.getParcelableArrayList(QUERY_ARG_QUERIES, Bundle.class)` and inspect `https://developer.android.com/reference/kotlin/android/provider/PeopleContract#QUERY_ARG_SELECTION_TYPE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/provider/PeopleContract#QUERY_ARG_SELECTION_VALUE:kotlin.String` to route the user directly into the communication session.

### Query and notification

Unlike traditional content providers that accept SQL-style selection strings, the People Provider provides a unified, read-only query interface. Clients **must** perform queries using query, passing structured query arguments (constructed via `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Persons.Query.Builder` or `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Groups.Query.Builder`) in the query `https://developer.android.com/reference/kotlin/android/os/Bundle.html#`. Traditional selection-string query overloads (i.e. those using selection and selectionArgs instead of the query Bundle), as well as modification operations (`insert`, `update`, and `delete`), are unsupported and will throw an `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

**Background maintenance mechanism:** When a client performs a query, the People Provider returns records from its local database immediately. If the requested data is missing or expired, the provider enqueues debounced, scheduled maintenance jobs to backfill data from the target People Directory into the local database. These scheduled jobs may not run immediately; for example, global directory syncs and heavy targeted refreshes may be deferred to run when the device is idle and charging. Because initial query results may be empty or incomplete prior to maintenance job completion, client applications may register a `https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#` on the URI returned in the cursor's extras under `https://developer.android.com/reference/kotlin/android/provider/PeopleContract#EXTRA_NOTIFICATION_URI:kotlin.String` (or on `https://developer.android.com/reference/kotlin/android/provider/PeopleContract#CONTENT_NOTIFICATION_URI:android.net.Uri`). When the local database is updated, the observer is notified, allowing the client to re-query and display the updated records.

### Permissions

Reading data from the People Provider requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_CONTACTS:kotlin.String` permission.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Capability` Bitmask flags indicating the types of communication reached or supported by a user identity in a People Directory. |
| | `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Directory` Constants and utilities for registering and discovering People Directories. |
| | `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Groups` Constants, URI definitions, and query utilities for group records aggregated from People Directories. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Intents` Standard intent actions, extras, and interaction constants used to bridge client applications with communication flows in People Directory applications. |
| | `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Persons` Constants, URI definitions, and query utilities for person identity records aggregated from People Directories. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/PeopleContract#AUTHORITY:kotlin.String` The authority for the People Provider. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/PeopleContract#EXTRA_NOTIFICATION_URI:kotlin.String` Key for an extra in the `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` containing a query-specific notification URI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/PeopleContract#QUERY_ARG_PACKAGE:kotlin.String` Query argument key specifying the package name of the target People Directory for a sub-query. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/PeopleContract#QUERY_ARG_QUERIES:kotlin.String` Query argument key used to pass a structured list of query requests to the People Provider. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/PeopleContract#QUERY_ARG_SELECTION_TYPE:kotlin.String` Query argument key specifying the selection criterion type (for example, `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Persons.Query#SELECTION_TYPE_PHONE:kotlin.String` for phone number, `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Persons.Query#SELECTION_TYPE_EMAIL:kotlin.String` for email address, etc. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/PeopleContract#QUERY_ARG_SELECTION_VALUE:kotlin.String` Query argument key specifying the array of values to match against for a given `https://developer.android.com/reference/kotlin/android/provider/PeopleContract#QUERY_ARG_SELECTION_TYPE:kotlin.String`. |
| --- | --- |

| Public methods ||
|---|---|
| static [PendingIntent](../android.app/PendingIntent.md)? | createPeopleInteractionRequest Creates a that allows a client application to initiate an interactive communication session (such as messaging, audio calling, or video calling) with a person or group in a target People Directory application. |

| Properties ||
|---|---|
| static [Uri](../android.net/Uri.md) | `https://developer.android.com/reference/kotlin/android/provider/PeopleContract#AUTHORITY_URI:android.net.Uri` A content:// style URI to the authority for the People Provider. |
| static [Uri](../android.net/Uri.md) | `https://developer.android.com/reference/kotlin/android/provider/PeopleContract#CONTENT_NOTIFICATION_URI:android.net.Uri` A content:// style URI for receiving general change notifications from the People Provider. |

## Constants

### AUTHORITY

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTHORITY: String
```

The authority for the People Provider.

 Value: "com.android.people"

### EXTRA_NOTIFICATION_URI

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NOTIFICATION_URI: String
```

Key for an extra in the `https://developer.android.com/reference/kotlin/android/database/Cursor.html#` `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` containing a query-specific notification URI.

This URI is generated by the People Provider and is unique to each query.

**For client applications:** Clients can extract this URI when a cursor is returned from a query and register a `https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#` via registerContentObserver to stay updated on data changes. Because initial queries may return partial or empty results while background maintenance jobs run, observing this URI allows the client to be notified when the local database is updated so that it can re-query and update the UI.

**For People Directory applications:** People Directory implementations do not use this key.

 Value: "android.provider.extra.NOTIFICATION_URI"

### QUERY_ARG_PACKAGE

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUERY_ARG_PACKAGE: String
```

Query argument key specifying the package name of the target People Directory for a sub-query.

 Value: "android:query-arg-package"

### QUERY_ARG_QUERIES

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUERY_ARG_QUERIES: String
```

Query argument key used to pass a structured list of query requests to the People Provider.

The value must be an `https://developer.android.com/reference/kotlin/java/util/ArrayList.html#` of `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` objects, where each bundle represents selection criteria targeting a specific directory package.

**For client applications:** Rather than constructing these bundles manually, clients should use `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Persons.Query.Builder` or `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Groups.Query.Builder` to create the query bundle.

**For People Directory applications:** When the People Provider dispatches query requests to a People Directory application, it passes query argument bundles containing this key so the application can inspect and fulfill the requested criteria.

 Value: "android:query-arg-queries"

### QUERY_ARG_SELECTION_TYPE

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUERY_ARG_SELECTION_TYPE: String
```

Query argument key specifying the selection criterion type (for example, `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Persons.Query#SELECTION_TYPE_PHONE:kotlin.String` for phone number, `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Persons.Query#SELECTION_TYPE_EMAIL:kotlin.String` for email address, etc.).

In query argument bundles, this key maps to a string specifying which attribute to search in the directory (e.g., phone numbers or email addresses).

In query cursors returned by a People Directory, this must be included as a `TEXT` column containing the selection criterion type string that caused that record to match.

 Value: "android:query-arg-selection-type"

### QUERY_ARG_SELECTION_VALUE

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUERY_ARG_SELECTION_VALUE: String
```

Query argument key specifying the array of values to match against for a given `https://developer.android.com/reference/kotlin/android/provider/PeopleContract#QUERY_ARG_SELECTION_TYPE:kotlin.String`.

In query argument bundles, this key maps to an array of strings (`String[]`) containing the target criteria to search for in the directory (e.g., a list of phone numbers).

In query cursors returned by a People Directory, this must be included as a `TEXT` column containing the single matching string (e.g., the specific phone number) that matched the record.

 Value: "android:query-arg-selection-value"

## Public methods

### createPeopleInteractionRequest

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createPeopleInteractionRequest(
    resolver: ContentResolver, 
    interactionType: String, 
    queryArgs: Bundle
): PendingIntent?
```

Creates a that allows a client application to initiate an interactive communication session (such as messaging, audio calling, or video calling) with a person or group in a target People Directory application.

**For client applications:** Clients invoke this method with the desired interaction type and a `queryArgs` bundle identifying the target person or group. The `queryArgs` bundle must be constructed using `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Persons.Query.Builder` and contain exactly one target sub-query targeting a single People Directory application. Clients can identify targets using:

- addLookupQuery: To target a specific person by their lookup key.
- addPhoneQuery: To target a person by phone number.
- addEmailQuery: To target a person by email address.
- addGroupQuery: To target a communication session with a group by group lookup key.

The returned `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` is minted under the People Provider's identity, enabling secure initiation of communication flows.

**For People Directory applications:** People Directory applications do not call this method. To support interaction requests, People Directory applications must declare an Activity in their manifest capable of handling `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Intents#ACTION_START_PEOPLE_INTERACTION:kotlin.String`. When the generated `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` is launched by a client, the People Directory application receives an Intent containing `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Intents#EXTRA_PEOPLE_INTERACTION_TYPE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Intents#EXTRA_PEOPLE_QUERY_ARGS:kotlin.String`. Based upon the `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Intents#EXTRA_PEOPLE_INTERACTION_TYPE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Intents#EXTRA_PEOPLE_QUERY_ARGS:kotlin.String`, People Directory applications should inspect the selection type and values to start the desired communication session for the matching person or group.

| Parameters ||
|---|---|
| `resolver` | [ContentResolver](../android.content/ContentResolver.md): The `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#` used to interact with the People Provider. This value cannot be `null`. |
| `interactionType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The desired type of communication, which must be one of the `PEOPLE_INTERACTION_TYPE_*` constants defined in `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Intents`. This value cannot be `null`. |
| `queryArgs` | [Bundle](../android.os/Bundle.md): A query arguments `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` identifying the target person or group. This bundle must contain exactly one target sub-query generated using `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Persons.Query.Builder` (e.g. via addLookupQuery, addPhoneQuery, addEmailQuery, or addGroupQuery). This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#?` | A `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` configured to launch the interaction Activity in the target directory application, or `null` if the request could not be processed. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `queryArgs` is malformed, does not contain exactly one target sub-query, or specifies a target package that is not recognized as a registered People Directory or does not handle `https://developer.android.com/reference/kotlin/android/provider/PeopleContract.Intents#ACTION_START_PEOPLE_INTERACTION:kotlin.String`. |
| `java.lang.NullPointerException` | if any argument is null. |

## Properties

### AUTHORITY_URI

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTHORITY_URI: Uri
```

A content:// style URI to the authority for the People Provider.

### CONTENT_NOTIFICATION_URI

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTENT_NOTIFICATION_URI: Uri
```

A content:// style URI for receiving general change notifications from the People Provider.

**For client applications:** Clients can register a `https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#` on this URI to be notified when directory data, person records, or group records change across any directory. This observer will trigger when the local database changes due to maintenance jobs or when People Directory applications report updates.

**For People Directory applications:** People Directory applications trigger notifications on this URI indirectly by invoking notifyChange whenever their backing user records are modified.

Note: People Directory applications should not invoke notifyChange on this URI directly. Doing so will not update the People Provider local database or propagate changes to client applications.
