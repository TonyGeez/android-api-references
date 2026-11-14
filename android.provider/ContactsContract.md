Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContactsContract

Kotlin | [Java](ContactsContract.md)
| --- | --- |

```
class ContactsContract
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.provider.ContactsContract](ContactsContract.md) |

The contract between the contacts provider and applications. Contains definitions for the supported URIs and columns. These APIs supersede `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts`.

### Overview

ContactsContract defines an extensible database of contact-related information. Contact information is stored in a three-tier data model:

- A row in the `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data` table can store any kind of personal data, such as a phone number or email addresses. The set of data kinds that can be stored in this table is open-ended. There is a predefined set of common kinds, but any application can add its own data kinds.
- A row in the `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts` table represents a set of data describing a person and associated with a single account (for example, one of the user's Gmail accounts).
- A row in the `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts` table represents an aggregate of one or more RawContacts presumably describing the same person. When data in or associated with the RawContacts table is changed, the affected aggregate contacts are updated as necessary.

Other tables include:

- `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Groups`, which contains information about raw contact groups such as Gmail contact groups. The current API does not support the notion of groups spanning multiple accounts.
- `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusUpdates`, which contains social status updates including IM availability.
- `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.AggregationExceptions`, which is used for manual aggregation and disaggregation of raw contacts
- `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Settings`, which contains visibility and sync settings for accounts and groups.
- `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.SyncState`, which contains free-form data maintained on behalf of sync adapters
- `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneLookup`, which is used for quick caller-ID lookup

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.AggregationExceptions` Constants for the contact aggregation exceptions table, which contains aggregation rules overriding those used by automatic aggregation. |
| abstract | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.BaseSyncColumns` Generic columns for use by sync adapters. |
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds` Container for definitions of common data types stored in the `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data` table. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactNameColumns` Contact name and contact name metadata columns in the RawContacts table. |
| abstract | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactOptionsColumns` Columns of `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts` that track the user's preferences for, or interactions with, the contact. |
| abstract | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactStatusColumns` <br /> |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts` Constants for the contacts table, which contains a record per aggregate of raw contacts representing the same person. |
| abstract | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactsColumns` Columns of `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts` that refer to intrinsic properties of the contact, as opposed to the user-specified options found in `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ContactOptionsColumns`. |
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data` Constants for the data table, which contains data points tied to a raw contact. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns` Columns in the Data table. |
| abstract | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumnsWithJoins` Combines all columns returned by `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data` table queries. |
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataUsageFeedback` API allowing applications to send usage information for each `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data` row to the Contacts Provider. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataUsageStatColumns` Columns in the Data_Usage_Stat table |
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DeletedContacts` Constants for the deleted contact table. |
| abstract | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DeletedContactsColumns` <br /> |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Directory` A Directory represents a contacts corpus, e. |
| abstract | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DisplayNameSources` Types of data used to produce the display name for a contact. |
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DisplayPhoto` Helper class for accessing full-size photos by photo file ID. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.FullNameStyle` Constants for various styles of combining given name, family name etc into a full name. |
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Groups` Constants for the groups table. |
| abstract | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.GroupsColumns` <br /> |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Intents` Contains helper classes used to create or manage `https://developer.android.com/reference/kotlin/android/content/Intent.html#` that involve contacts. |
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneLookup` A table that represents the result of looking up a phone number, for example for caller ID. |
| abstract | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneLookupColumns` <br /> |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneticNameStyle` Constants for various styles of capturing the pronunciation of a person's name. |
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PinnedPositions` Contact-specific information about whether or not a contact has been pinned by the user at a particular position within the system contact application's user interface. |
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Presence` <br /> |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PresenceColumns` Additional data mixed in with `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns` to link back to specific `https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String` entries. |
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Profile` Constants for the user's profile data, which is represented as a single contact on the device that represents the user. |
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ProfileSyncState` A table provided for sync adapters to use for storing private sync state data for the user's personal profile. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.ProviderStatus` API for inquiring about the general status of the provider. |
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.QuickContact` Helper methods to display QuickContact dialogs that display all the information belonging to a specific `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts` entry. |
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts` Constants for the raw contacts table, which contains one row of contact information for each person in each synced account. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContactsColumns` <br /> |
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContactsEntity` Constants for the raw contacts entities table, which can be thought of as an outer join of the raw_contacts table with the data table. |
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.SearchSnippets` Additional column returned by `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts#CONTENT_FILTER_URI:android.net.Uri` explaining why the filter matched the contact. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Settings` Contacts-specific settings for various `https://developer.android.com/reference/kotlin/android/accounts/Account.html#`'s. |
| abstract | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.SettingsColumns` <br /> |
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.SimAccount` A parcelable class encapsulating account data for contacts that originate from a SIM card. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.SimContacts` Class containing utility methods around determine what accounts in the ContactsProvider are related to the SIM cards in the device. |
| abstract | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns` Social status update columns. |
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusUpdates` A status update is linked to a `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data` row and captures the user's latest status update via the corresponding source, e. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.SyncColumns` Columns that appear when each row of a table belongs to a specific account, including sync information that an account may need. |
| | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.SyncState` A table provided for sync adapters to use for storing private sync state data for contacts. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract#AUTHORITY:kotlin.String` The authority for the contacts provider |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract#CALLER_IS_SYNCADAPTER:kotlin.String` An optional URI parameter for insert, update, or delete queries that allows the caller to specify that it is a sync adapter. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract#DEFERRED_SNIPPETING:kotlin.String` A key to a boolean in the "extras" bundle of the cursor. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract#DEFERRED_SNIPPETING_QUERY:kotlin.String` Key to retrieve the original deferred snippeting from the cursor on the client side. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract#DIRECTORY_PARAM_KEY:kotlin.String` Query parameter that should be used by the client to access a specific `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Directory`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract#LIMIT_PARAM_KEY:kotlin.String` A query parameter that limits the number of results returned for supported URIs. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract#PRIMARY_ACCOUNT_NAME:kotlin.String` A query parameter specifing a primary account. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract#PRIMARY_ACCOUNT_TYPE:kotlin.String` A query parameter specifing a primary account. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract#REMOVE_DUPLICATE_ENTRIES:kotlin.String` A boolean parameter for `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone#CONTENT_URI:android.net.Uri`, `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Email#CONTENT_URI:android.net.Uri`, and `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.StructuredPostal#CONTENT_URI:android.net.Uri`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract#STREQUENT_PHONE_ONLY:kotlin.String` A boolean parameter for `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts#CONTENT_STREQUENT_URI:android.net.Uri` and `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts#CONTENT_STREQUENT_FILTER_URI:android.net.Uri`, which requires the ContactsProvider to return only phone-related results. |

| Public constructors ||
|---|---|
| ContactsContract <br /> |

| Public methods ||
|---|---|
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isProfileId This method can be used to identify whether the given ID is associated with profile data. |

| Properties ||
|---|---|
| static [Uri](../android.net/Uri.md)! | `https://developer.android.com/reference/kotlin/android/provider/ContactsContract#AUTHORITY_URI:android.net.Uri` A content:// style uri to the authority for the contacts provider |

## Constants

### AUTHORITY

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTHORITY: String
```

The authority for the contacts provider

 Value: "com.android.contacts"

### CALLER_IS_SYNCADAPTER

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CALLER_IS_SYNCADAPTER: String
```

An optional URI parameter for insert, update, or delete queries that allows the caller to specify that it is a sync adapter. The default value is false. If true `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.SyncColumns#DIRTY:kotlin.String` is not automatically set and the "syncToNetwork" parameter is set to false when calling notifyChange. This prevents an unnecessary extra synchronization, see the discussion of the delete operation in `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts`.

 Value: "caller_is_syncadapter"

### DEFERRED_SNIPPETING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEFERRED_SNIPPETING: String
```

A key to a boolean in the "extras" bundle of the cursor. The boolean indicates that the provider did not create a snippet and that the client asking for the snippet should do it (true means the snippeting was deferred to the client).

 Value: "deferred_snippeting"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.SearchSnippets`

### DEFERRED_SNIPPETING_QUERY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEFERRED_SNIPPETING_QUERY: String
```

Key to retrieve the original deferred snippeting from the cursor on the client side.

 Value: "deferred_snippeting_query"

**See Also**

- `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.SearchSnippets`
- `https://developer.android.com/reference/kotlin/android/provider/ContactsContract#DEFERRED_SNIPPETING:kotlin.String`

### DIRECTORY_PARAM_KEY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTORY_PARAM_KEY: String
```

Query parameter that should be used by the client to access a specific `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Directory`. The parameter value should be the _ID of the corresponding directory, e.g. `content://com.android.contacts/data/emails/filter/acme?directory=3`

 Value: "directory"

### LIMIT_PARAM_KEY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LIMIT_PARAM_KEY: String
```

A query parameter that limits the number of results returned for supported URIs. The parameter value should be an integer.

This parameter is not supported by all URIs. Supported URIs include, but not limited to, `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts#CONTENT_URI:android.net.Uri`, `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts#CONTENT_URI:android.net.Uri`, `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data#CONTENT_URI:android.net.Uri`, `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone#CONTENT_URI:android.net.Uri`, `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Callable#CONTENT_URI:android.net.Uri`, `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Email#CONTENT_URI:android.net.Uri`, `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Contactables#CONTENT_URI:android.net.Uri`,

In order to limit the number of rows returned by a non-supported URI, you can implement a `https://developer.android.com/reference/kotlin/android/database/CursorWrapper.html#` and override the getCount methods.

 Value: "limit"

### PRIMARY_ACCOUNT_NAME

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRIMARY_ACCOUNT_NAME: String
```

A query parameter specifing a primary account. This parameter should be used with `https://developer.android.com/reference/kotlin/android/provider/ContactsContract#PRIMARY_ACCOUNT_TYPE:kotlin.String`. The contacts provider handling a query may rely on this information to optimize its query results. For example, in an email composition screen, its implementation can specify an account when obtaining possible recipients, letting the provider know which account is selected during the composition. The provider may use the "primary account" information to optimize the search result.

 Value: "name_for_primary_account"

### PRIMARY_ACCOUNT_TYPE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRIMARY_ACCOUNT_TYPE: String
```

A query parameter specifing a primary account. This parameter should be used with `https://developer.android.com/reference/kotlin/android/provider/ContactsContract#PRIMARY_ACCOUNT_NAME:kotlin.String`. See the doc in `https://developer.android.com/reference/kotlin/android/provider/ContactsContract#PRIMARY_ACCOUNT_NAME:kotlin.String`.

 Value: "type_for_primary_account"

### REMOVE_DUPLICATE_ENTRIES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REMOVE_DUPLICATE_ENTRIES: String
```

A boolean parameter for `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone#CONTENT_URI:android.net.Uri`, `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Email#CONTENT_URI:android.net.Uri`, and `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.StructuredPostal#CONTENT_URI:android.net.Uri`. This enables a content provider to remove duplicate entries in results.

 Value: "remove_duplicate_entries"

### STREQUENT_PHONE_ONLY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STREQUENT_PHONE_ONLY: String
```

A boolean parameter for `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts#CONTENT_STREQUENT_URI:android.net.Uri` and `https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts#CONTENT_STREQUENT_FILTER_URI:android.net.Uri`, which requires the ContactsProvider to return only phone-related results.

 Value: "strequent_phone_only"

## Public constructors

### ContactsContract

```
ContactsContract()
```

## Public methods

### isProfileId

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isProfileId(id: Long): Boolean
```

This method can be used to identify whether the given ID is associated with profile data. It does not necessarily indicate that the ID is tied to valid data, merely that accessing data using this ID will result in profile access checks and will only return data from the profile.

| Parameters ||
|---|---|
| `id` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The ID to check. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the ID is associated with profile data. |

## Properties

### AUTHORITY_URI

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUTHORITY_URI: Uri!
```

A content:// style uri to the authority for the contacts provider
