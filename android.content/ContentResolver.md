# ContentResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContentResolver

Kotlin| [Java](https://developer.android.com/reference/android/content/ContentResolver "View this page in Java") 

```
abstract class ContentResolver
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.content.ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver#) |

| Known Direct Subclasses [MockContentResolver](https://developer.android.com/reference/kotlin/android/test/mock/MockContentResolver.html#) |-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MockContentResolver](https://developer.android.com/reference/kotlin/android/test/mock/MockContentResolver.html#) | An extension of [android.content.ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver#) that is designed for testing. | |

This class provides applications access to the content model.
|
| ### Developer Guides
|
| For more information about using a ContentResolver with content providers, read the [Content Providers](https://developer.android.com/guide/topics/providers/content-providers.html) developer guide.

<br />

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [MimeTypeInfo](https://developer.android.com/reference/kotlin/android/content/ContentResolver.MimeTypeInfo) Detailed description of a specific MIME type, including an icon and label that describe the type. |

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ANY_CURSOR_ITEM_TYPE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#ANY_CURSOR_ITEM_TYPE:kotlin.String) This is the Android platform's generic MIME type to match any MIME type of the form " [CURSOR_ITEM_BASE_TYPE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#CURSOR_ITEM_BASE_TYPE:kotlin.String)/`SUB_TYPE`". |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CURSOR_DIR_BASE_TYPE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#CURSOR_DIR_BASE_TYPE:kotlin.String) This is the Android platform's base MIME type for a content: URI containing a Cursor of zero or more items. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CURSOR_ITEM_BASE_TYPE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#CURSOR_ITEM_BASE_TYPE:kotlin.String) This is the Android platform's base MIME type for a content: URI containing a Cursor of a single item. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_HONORED_ARGS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#EXTRA_HONORED_ARGS:kotlin.String) Allows provider to report back to client which query keys are honored in a Cursor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_REFRESH_SUPPORTED](https://developer.android.com/reference/kotlin/android/content/ContentResolver#EXTRA_REFRESH_SUPPORTED:kotlin.String) An extra boolean describing whether a particular provider supports refresh or not. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_SIZE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#EXTRA_SIZE:kotlin.String) An extra [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#) describing the optimal size for a requested image resource, in pixels. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_TOTAL_COUNT](https://developer.android.com/reference/kotlin/android/content/ContentResolver#EXTRA_TOTAL_COUNT:kotlin.String) Added to [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) extras [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) to indicate total row count of recordset when paging is supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NOTIFY_DELETE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#NOTIFY_DELETE:kotlin.Int) Flag for [notifyChange(android.net.Uri,android.database.ContentObserver,int)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(android.net.Uri,%20android.database.ContentObserver,%20kotlin.Int)): typically set by a [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) to indicate that this notification is the result of a android. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NOTIFY_INSERT](https://developer.android.com/reference/kotlin/android/content/ContentResolver#NOTIFY_INSERT:kotlin.Int) Flag for [notifyChange(android.net.Uri,android.database.ContentObserver,int)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(android.net.Uri,%20android.database.ContentObserver,%20kotlin.Int)): typically set by a [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) to indicate that this notification is the result of an android. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NOTIFY_SKIP_NOTIFY_FOR_DESCENDANTS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#NOTIFY_SKIP_NOTIFY_FOR_DESCENDANTS:kotlin.Int) Flag for [notifyChange(android.net.Uri,android.database.ContentObserver,int)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(android.net.Uri,%20android.database.ContentObserver,%20kotlin.Int)): if set, this notification will be skipped if it is being delivered to the root URI of a ContentObserver that is using "notify for descendants. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NOTIFY_SYNC_TO_NETWORK](https://developer.android.com/reference/kotlin/android/content/ContentResolver#NOTIFY_SYNC_TO_NETWORK:kotlin.Int) Flag for [notifyChange(android.net.Uri,android.database.ContentObserver,int)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(android.net.Uri,%20android.database.ContentObserver,%20kotlin.Int)): attempt to sync the change to the network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NOTIFY_UPDATE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#NOTIFY_UPDATE:kotlin.Int) Flag for [notifyChange(android.net.Uri,android.database.ContentObserver,int)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(android.net.Uri,%20android.database.ContentObserver,%20kotlin.Int)): typically set by a [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) to indicate that this notification is the result of an android. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [QUERY_ARG_GROUP_COLUMNS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_GROUP_COLUMNS:kotlin.String) Specifies the list of columns (stored as a`String[]`) against which to group results. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [QUERY_ARG_LIMIT](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_LIMIT:kotlin.String) Specifies the max number of rows to include in a Cursor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [QUERY_ARG_OFFSET](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_OFFSET:kotlin.String) Specifies the offset row index within a Cursor. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [QUERY_ARG_SORT_COLLATION](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_COLLATION:kotlin.String) Allows client to specify a hint to the provider declaring which collation to use when sorting values. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [QUERY_ARG_SORT_COLUMNS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_COLUMNS:kotlin.String) Specifies the list of columns (stored as a`String[]`) against which to sort results. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [QUERY_ARG_SORT_DIRECTION](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_DIRECTION:kotlin.String) Specifies desired sort order. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [QUERY_ARG_SORT_LOCALE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_LOCALE:kotlin.String) Allows client to specify a hint to the provider declaring which locale to use when sorting values. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [QUERY_ARG_SQL_GROUP_BY](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SQL_GROUP_BY:kotlin.String) Key for an SQL style`GROUP BY`string that may be present in the query Bundle argument passed to[ContentProvider.query(Uri, String[], Bundle, CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [QUERY_ARG_SQL_HAVING](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SQL_HAVING:kotlin.String) Key for an SQL style`HAVING`string that may be present in the query Bundle argument passed to[ContentProvider.query(Uri, String[], Bundle, CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [QUERY_ARG_SQL_LIMIT](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SQL_LIMIT:kotlin.String) Key for an SQL style`LIMIT`string that may be present in the query Bundle argument passed to[ContentProvider.query(Uri, String[], Bundle, CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [QUERY_ARG_SQL_SELECTION](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SQL_SELECTION:kotlin.String) Key for an SQL style selection string that may be present in the query Bundle argument passed to[ContentProvider.query(Uri, String[], Bundle, CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal))when called by a legacy client. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [QUERY_ARG_SQL_SELECTION_ARGS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SQL_SELECTION_ARGS:kotlin.String) Key for SQL selection string arguments list. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [QUERY_ARG_SQL_SORT_ORDER](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SQL_SORT_ORDER:kotlin.String) Key for an SQL style sort string that may be present in the query Bundle argument passed to[ContentProvider.query(Uri, String[], Bundle, CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal))when called by a legacy client. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUERY_SORT_DIRECTION_ASCENDING](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_SORT_DIRECTION_ASCENDING:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUERY_SORT_DIRECTION_DESCENDING](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_SORT_DIRECTION_DESCENDING:kotlin.Int) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SCHEME_ANDROID_RESOURCE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SCHEME_ANDROID_RESOURCE:kotlin.String) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SCHEME_CONTENT](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SCHEME_CONTENT:kotlin.String) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SCHEME_FILE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SCHEME_FILE:kotlin.String) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_EXTRAS_ACCOUNT](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_ACCOUNT:kotlin.String) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_EXTRAS_DISCARD_LOCAL_DELETIONS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_DISCARD_LOCAL_DELETIONS:kotlin.String) Indicates that the sync adapter should not proceed with the delete operations, if it determines that there are too many. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_EXTRAS_DO_NOT_RETRY](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_DO_NOT_RETRY:kotlin.String) If this extra is set to true then the request will not be retried if it fails. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_EXTRAS_EXPEDITED](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_EXPEDITED:kotlin.String) If this extra is set to true, the sync request will be scheduled at the front of the sync request queue, but it is still subject to JobScheduler quota and throttling due to App Standby buckets. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_EXTRAS_FORCE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_FORCE:kotlin.String) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_EXTRAS_IGNORE_BACKOFF](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_IGNORE_BACKOFF:kotlin.String) If this extra is set to true then any backoffs for the initial attempt (e.g. due to retries) are ignored by the sync scheduler. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_EXTRAS_IGNORE_SETTINGS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_IGNORE_SETTINGS:kotlin.String) If this extra is set to true then the sync settings (like getSyncAutomatically()) are ignored by the sync scheduler. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_EXTRAS_INITIALIZE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_INITIALIZE:kotlin.String) Set by the SyncManager to request that the SyncAdapter initialize itself for the given account/authority pair. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_EXTRAS_MANUAL](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_MANUAL:kotlin.String) Setting this extra is the equivalent of setting both [SYNC_EXTRAS_IGNORE_SETTINGS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_IGNORE_SETTINGS:kotlin.String) and [SYNC_EXTRAS_IGNORE_BACKOFF](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_IGNORE_BACKOFF:kotlin.String) |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_EXTRAS_OVERRIDE_TOO_MANY_DELETIONS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_OVERRIDE_TOO_MANY_DELETIONS:kotlin.String) Indicates that the sync adapter should proceed with the delete operations, even if it determines that there are too many. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_EXTRAS_REQUIRE_CHARGING](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_REQUIRE_CHARGING:kotlin.String) If this extra is set to true, the sync request will be scheduled only when the device is plugged in. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_EXTRAS_SCHEDULE_AS_EXPEDITED_JOB](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_SCHEDULE_AS_EXPEDITED_JOB:kotlin.String) Run this sync operation as an "expedited job" (see [android.app.job.JobInfo.Builder#setExpedited(boolean)](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder.html#setExpedited(kotlin.Boolean))). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC_EXTRAS_UPLOAD](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_UPLOAD:kotlin.String) Indicates that this sync is intended to only upload local changes to the server. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SYNC_OBSERVER_TYPE_ACTIVE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_OBSERVER_TYPE_ACTIVE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SYNC_OBSERVER_TYPE_PENDING](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_OBSERVER_TYPE_PENDING:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SYNC_OBSERVER_TYPE_SETTINGS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_OBSERVER_TYPE_SETTINGS:kotlin.Int) <br /> |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver#ContentResolver(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context)?`)` Note: passing a`null`context here could lead to unexpected behavior in certain ContentResolver APIs so it is highly recommended to pass a non-null context here. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ContentProviderClient](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient)? | [acquireContentProviderClient](https://developer.android.com/reference/kotlin/android/content/ContentResolver#acquireContentProviderClient(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` Returns a [ContentProviderClient](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient) that is associated with the [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) that services the content at uri, starting the provider if necessary. |
| [ContentProviderClient](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient)? | [acquireContentProviderClient](https://developer.android.com/reference/kotlin/android/content/ContentResolver#acquireContentProviderClient(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns a [ContentProviderClient](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient) that is associated with the [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) with the authority of name, starting the provider if necessary. |
| [ContentProviderClient](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient)? | [acquireUnstableContentProviderClient](https://developer.android.com/reference/kotlin/android/content/ContentResolver#acquireUnstableContentProviderClient(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` Like [acquireContentProviderClient(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#acquireContentProviderClient(android.net.Uri)), but for use when you do not trust the stability of the target content provider. |
| [ContentProviderClient](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient)? | [acquireUnstableContentProviderClient](https://developer.android.com/reference/kotlin/android/content/ContentResolver#acquireUnstableContentProviderClient(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Like [acquireContentProviderClient(java.lang.String)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#acquireContentProviderClient(kotlin.String)), but for use when you do not trust the stability of the target content provider. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addPeriodicSync](https://developer.android.com/reference/kotlin/android/content/ContentResolver#addPeriodicSync(android.accounts.Account,%20kotlin.String,%20android.os.Bundle,%20kotlin.Long))`(`account:` ` [Account](https://developer.android.com/reference/kotlin/android/accounts/Account.html#)!`, `authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`, `pollFrequency:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Specifies that a sync should be requested with the specified the account, authority, and extras at the given frequency. |
| openstatic [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [addStatusChangeListener](https://developer.android.com/reference/kotlin/android/content/ContentResolver#addStatusChangeListener(kotlin.Int,%20android.content.SyncStatusObserver))`(`mask:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `callback:` ` [SyncStatusObserver](https://developer.android.com/reference/kotlin/android/content/SyncStatusObserver)!`)` Request notifications when the different aspects of the SyncManager change. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult)!\> | [applyBatch](https://developer.android.com/reference/kotlin/android/content/ContentResolver#applyBatch(kotlin.String,%20java.util.ArrayList))`(`authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `operations:` ` [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)< [ContentProviderOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation)!>`)` Applies each of the [ContentProviderOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation) objects and returns an array of their results. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bulkInsert](https://developer.android.com/reference/kotlin/android/content/ContentResolver#bulkInsert(android.net.Uri,%20kotlin.Array))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `values:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)!>`)` Inserts multiple rows into a table at the given URL. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | [call](https://developer.android.com/reference/kotlin/android/content/ContentResolver#call(android.net.Uri,%20kotlin.String,%20kotlin.String,%20android.os.Bundle))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `method:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `arg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` Call a provider-defined method. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | [call](https://developer.android.com/reference/kotlin/android/content/ContentResolver#call(kotlin.String,%20kotlin.String,%20kotlin.String,%20android.os.Bundle))`(`authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `method:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `arg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancelSync](https://developer.android.com/reference/kotlin/android/content/ContentResolver#cancelSync(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`)` Cancel any active or pending syncs that match the Uri. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancelSync](https://developer.android.com/reference/kotlin/android/content/ContentResolver#cancelSync(android.accounts.Account,%20kotlin.String))`(`account:` ` [Account](https://developer.android.com/reference/kotlin/android/accounts/Account.html#)!`, `authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Cancel any active or pending syncs that match account and authority. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancelSync](https://developer.android.com/reference/kotlin/android/content/ContentResolver#cancelSync(android.content.SyncRequest))`(`request:` ` [SyncRequest](https://developer.android.com/reference/kotlin/android/content/SyncRequest)!`)` Remove the specified sync. |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [canonicalize](https://developer.android.com/reference/kotlin/android/content/ContentResolver#canonicalize(android.net.Uri))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` Transform the given url to a canonical representation of its referenced resource, which can be used across devices, persisted, backed up and restored, etc. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [delete](https://developer.android.com/reference/kotlin/android/content/ContentResolver#delete(android.net.Uri,%20android.os.Bundle))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` Deletes row(s) specified by a content URI. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [delete](https://developer.android.com/reference/kotlin/android/content/ContentResolver#delete(android.net.Uri,%20kotlin.String,%20kotlin.Array))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `where:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` Deletes row(s) specified by a content URI. |
| openstatic [SyncInfo](https://developer.android.com/reference/kotlin/android/content/SyncInfo)! | [getCurrentSync](https://developer.android.com/reference/kotlin/android/content/ContentResolver#getCurrentSync())`()` If a sync is active returns the information about it, otherwise returns null. |
| openstatic [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SyncInfo](https://developer.android.com/reference/kotlin/android/content/SyncInfo)!\>! | [getCurrentSyncs](https://developer.android.com/reference/kotlin/android/content/ContentResolver#getCurrentSyncs())`()` Returns a list with information about all the active syncs. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIsSyncable](https://developer.android.com/reference/kotlin/android/content/ContentResolver#getIsSyncable(android.accounts.Account,%20kotlin.String))`(`account:` ` [Account](https://developer.android.com/reference/kotlin/android/accounts/Account.html#)!`, `authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Check if this account/provider is syncable. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getMasterSyncAutomatically](https://developer.android.com/reference/kotlin/android/content/ContentResolver#getMasterSyncAutomatically())`()` Gets the global auto-sync setting that applies to all the providers and accounts. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [UriPermission](https://developer.android.com/reference/kotlin/android/content/UriPermission)!\> | [getOutgoingPersistedUriPermissions](https://developer.android.com/reference/kotlin/android/content/ContentResolver#getOutgoingPersistedUriPermissions())`()` Return list of all persisted URI permission grants that are hosted by the calling app. |
| openstatic [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PeriodicSync](https://developer.android.com/reference/kotlin/android/content/PeriodicSync)!\>! | [getPeriodicSyncs](https://developer.android.com/reference/kotlin/android/content/ContentResolver#getPeriodicSyncs(android.accounts.Account,%20kotlin.String))`(`account:` ` [Account](https://developer.android.com/reference/kotlin/android/accounts/Account.html#)!`, `authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get the list of information about the periodic syncs for the given account and authority. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [UriPermission](https://developer.android.com/reference/kotlin/android/content/UriPermission)!\> | [getPersistedUriPermissions](https://developer.android.com/reference/kotlin/android/content/ContentResolver#getPersistedUriPermissions())`()` Return list of all URI permission grants that have been persisted by the calling app. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | [getStreamTypes](https://developer.android.com/reference/kotlin/android/content/ContentResolver#getStreamTypes(android.net.Uri,%20kotlin.String))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mimeTypeFilter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Query for the possible MIME types for the representations the given content URL can be returned when opened as as stream with #openTypedAssetFileDescriptor. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [SyncAdapterType](https://developer.android.com/reference/kotlin/android/content/SyncAdapterType)!\>! | [getSyncAdapterTypes](https://developer.android.com/reference/kotlin/android/content/ContentResolver#getSyncAdapterTypes())`()` Get information about the SyncAdapters that are known to the system. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getSyncAutomatically](https://developer.android.com/reference/kotlin/android/content/ContentResolver#getSyncAutomatically(android.accounts.Account,%20kotlin.String))`(`account:` ` [Account](https://developer.android.com/reference/kotlin/android/accounts/Account.html#)!`, `authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Check if the provider should be synced when a network tickle is received |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getType](https://developer.android.com/reference/kotlin/android/content/ContentResolver#getType(android.net.Uri))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` Return the MIME type of the given content URL. |
| [ContentResolver.MimeTypeInfo](https://developer.android.com/reference/kotlin/android/content/ContentResolver.MimeTypeInfo) | [getTypeInfo](https://developer.android.com/reference/kotlin/android/content/ContentResolver#getTypeInfo(kotlin.String))`(`mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Return a detailed description of the given MIME type, including an icon and label that describe the type. |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [insert](https://developer.android.com/reference/kotlin/android/content/ContentResolver#insert(android.net.Uri,%20android.content.ContentValues))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `values:` ` [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)?`)` Inserts a row into a table at the given URL. |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [insert](https://developer.android.com/reference/kotlin/android/content/ContentResolver#insert(android.net.Uri,%20android.content.ContentValues,%20android.os.Bundle))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `values:` ` [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)?`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` Inserts a row into a table at the given URL. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSyncActive](https://developer.android.com/reference/kotlin/android/content/ContentResolver#isSyncActive(android.accounts.Account,%20kotlin.String))`(`account:` ` [Account](https://developer.android.com/reference/kotlin/android/accounts/Account.html#)!`, `authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns true if there is currently a sync operation for the given account or authority actively being processed. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSyncPending](https://developer.android.com/reference/kotlin/android/content/ContentResolver#isSyncPending(android.accounts.Account,%20kotlin.String))`(`account:` ` [Account](https://developer.android.com/reference/kotlin/android/accounts/Account.html#)!`, `authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Return true if the pending status is true of any matching authorities. |
| open [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#) | [loadThumbnail](https://developer.android.com/reference/kotlin/android/content/ContentResolver#loadThumbnail(android.net.Uri,%20android.util.Size,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `size:` ` [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#)`, `signal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` Convenience method that efficiently loads a visual thumbnail for the given [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyChange](https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(android.net.Uri,%20android.database.ContentObserver))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `observer:` ` [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#)?`)` Notify registered observers that a row was updated and attempt to sync changes to the network. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyChange](https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(android.net.Uri,%20android.database.ContentObserver,%20kotlin.Boolean))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `observer:` ` [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#)?`, `syncToNetwork:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Notify registered observers that a row was updated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyChange](https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(android.net.Uri,%20android.database.ContentObserver,%20kotlin.Int))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `observer:` ` [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#)?`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Notify registered observers that a row was updated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyChange](https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(kotlin.collections.MutableCollection,%20android.database.ContentObserver,%20kotlin.Int))`(`uris:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!>`, `observer:` ` [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#)?`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Notify registered observers that several rows have been updated. |
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | [openAssetFile](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openAssetFile(android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `signal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` <br /> |
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | [openAssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openAssetFileDescriptor(android.net.Uri,%20kotlin.String))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Open a raw file descriptor to access data under a URI. |
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | [openAssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openAssetFileDescriptor(android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` Open a raw file descriptor to access data under a URI. |
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)? | [openFile](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openFile(android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `signal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` <br /> |
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)? | [openFileDescriptor](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openFileDescriptor(android.net.Uri,%20kotlin.String))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Open a raw file descriptor to access data under a URI. |
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)? | [openFileDescriptor](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openFileDescriptor(android.net.Uri,%20kotlin.String,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` Open a raw file descriptor to access data under a URI. |
| [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)? | [openInputStream](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openInputStream(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` Open a stream on to the content associated with a content URI. |
| [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)? | [openOutputStream](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openOutputStream(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` Synonym for [openOutputStream(uri, "w")](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openOutputStream(android.net.Uri,%20kotlin.String)). |
| [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)? | [openOutputStream](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openOutputStream(android.net.Uri,%20kotlin.String))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Open a stream on to the content associated with a content URI. |
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | [openTypedAssetFile](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openTypedAssetFile(android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mimeTypeFilter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `opts:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `signal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` <br /> |
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | [openTypedAssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openTypedAssetFileDescriptor(android.net.Uri,%20kotlin.String,%20android.os.Bundle))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `opts:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` Open a raw file descriptor to access (potentially type transformed) data from a "content:" URI. |
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | [openTypedAssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openTypedAssetFileDescriptor(android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `opts:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` Open a raw file descriptor to access (potentially type transformed) data from a "content:" URI. |
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | [query](https://developer.android.com/reference/kotlin/android/content/ContentResolver#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `projection:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `queryArgs:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` Query the given URI, returning a [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) over the result set with support for cancellation. |
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | [query](https://developer.android.com/reference/kotlin/android/content/ContentResolver#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `projection:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `sortOrder:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Query the given URI, returning a [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) over the result set. |
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | [query](https://developer.android.com/reference/kotlin/android/content/ContentResolver#query(android.net.Uri,%20kotlin.Array,%20kotlin.String,%20kotlin.Array,%20kotlin.String,%20android.os.CancellationSignal))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `projection:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `selection:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`, `sortOrder:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` Query the given URI, returning a [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) over the result set with optional support for cancellation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [refresh](https://developer.android.com/reference/kotlin/android/content/ContentResolver#refresh(android.net.Uri,%20android.os.Bundle,%20android.os.CancellationSignal))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`)` This allows clients to request an explicit refresh of content identified by`uri`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerContentObserver](https://developer.android.com/reference/kotlin/android/content/ContentResolver#registerContentObserver(android.net.Uri,%20kotlin.Boolean,%20android.database.ContentObserver))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `notifyForDescendants:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `observer:` ` [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#)`)` Register an observer class that gets callbacks when data identified by a given content URI changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releasePersistableUriPermission](https://developer.android.com/reference/kotlin/android/content/ContentResolver#releasePersistableUriPermission(android.net.Uri,%20kotlin.Int))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `modeFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Relinquish a persisted URI permission grant. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removePeriodicSync](https://developer.android.com/reference/kotlin/android/content/ContentResolver#removePeriodicSync(android.accounts.Account,%20kotlin.String,%20android.os.Bundle))`(`account:` ` [Account](https://developer.android.com/reference/kotlin/android/accounts/Account.html#)!`, `authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Remove a periodic sync. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeStatusChangeListener](https://developer.android.com/reference/kotlin/android/content/ContentResolver#removeStatusChangeListener(kotlin.Any))`(`handle:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Remove a previously registered status change listener. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestSync](https://developer.android.com/reference/kotlin/android/content/ContentResolver#requestSync(android.accounts.Account,%20kotlin.String,%20android.os.Bundle))`(`account:` ` [Account](https://developer.android.com/reference/kotlin/android/accounts/Account.html#)!`, `authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Start an asynchronous sync operation. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestSync](https://developer.android.com/reference/kotlin/android/content/ContentResolver#requestSync(android.content.SyncRequest))`(`request:` ` [SyncRequest](https://developer.android.com/reference/kotlin/android/content/SyncRequest)!`)` Register a sync with the SyncManager. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIsSyncable](https://developer.android.com/reference/kotlin/android/content/ContentResolver#setIsSyncable(android.accounts.Account,%20kotlin.String,%20kotlin.Int))`(`account:` ` [Account](https://developer.android.com/reference/kotlin/android/accounts/Account.html#)!`, `authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `syncable:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set whether this account/provider is syncable. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMasterSyncAutomatically](https://developer.android.com/reference/kotlin/android/content/ContentResolver#setMasterSyncAutomatically(kotlin.Boolean))`(`sync:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the global auto-sync setting that applies to all the providers and accounts. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSyncAutomatically](https://developer.android.com/reference/kotlin/android/content/ContentResolver#setSyncAutomatically(android.accounts.Account,%20kotlin.String,%20kotlin.Boolean))`(`account:` ` [Account](https://developer.android.com/reference/kotlin/android/accounts/Account.html#)!`, `authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sync:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set whether or not the provider is synced when it receives a network tickle. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startSync](https://developer.android.com/reference/kotlin/android/content/ContentResolver#startSync(android.net.Uri,%20android.os.Bundle))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Start an asynchronous sync operation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [takePersistableUriPermission](https://developer.android.com/reference/kotlin/android/content/ContentResolver#takePersistableUriPermission(android.net.Uri,%20kotlin.Int))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `modeFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Take a persistable URI permission grant that has been offered. |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [uncanonicalize](https://developer.android.com/reference/kotlin/android/content/ContentResolver#uncanonicalize(android.net.Uri))`(`url:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` Given a canonical Uri previously generated by [canonicalize](https://developer.android.com/reference/kotlin/android/content/ContentResolver#canonicalize(android.net.Uri)), convert it to its local non-canonical form. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterContentObserver](https://developer.android.com/reference/kotlin/android/content/ContentResolver#unregisterContentObserver(android.database.ContentObserver))`(`observer:` ` [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#)`)` Unregisters a change observer. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [update](https://developer.android.com/reference/kotlin/android/content/ContentResolver#update(android.net.Uri,%20android.content.ContentValues,%20android.os.Bundle))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `values:` ` [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)?`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` Update row(s) in a content URI. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [update](https://developer.android.com/reference/kotlin/android/content/ContentResolver#update(android.net.Uri,%20android.content.ContentValues,%20kotlin.String,%20kotlin.Array))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `values:` ` [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)?`, `where:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `selectionArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` Update row(s) in a content URI. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [validateSyncExtrasBundle](https://developer.android.com/reference/kotlin/android/content/ContentResolver#validateSyncExtrasBundle(android.os.Bundle))`(`extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Check that only values of the following types are in the Bundle: - Integer - Long - Boolean - Float - Double - String - Account - null <br /> |
| openstatic [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver#) | [wrap](https://developer.android.com/reference/kotlin/android/content/ContentResolver#wrap(android.content.ContentProvider))`(`wrapped:` ` [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider)`)` Create a [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver#) instance that redirects all its methods to the given [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider). |
| openstatic [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver#) | [wrap](https://developer.android.com/reference/kotlin/android/content/ContentResolver#wrap(android.content.ContentProviderClient))`(`wrapped:` ` [ContentProviderClient](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient)`)` Create a [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver#) instance that redirects all its methods to the given [ContentProviderClient](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient). |

## Constants

### ANY_CURSOR_ITEM_TYPE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ANY_CURSOR_ITEM_TYPE: String
```

This is the Android platform's generic MIME type to match any MIME type of the form " [CURSOR_ITEM_BASE_TYPE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#CURSOR_ITEM_BASE_TYPE:kotlin.String)/`SUB_TYPE`".`SUB_TYPE`is the sub-type of the application-dependent content, e.g., "audio", "video", "playlist". 

 Value: "vnd.android.cursor.item/*"

### CURSOR_DIR_BASE_TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CURSOR_DIR_BASE_TYPE: String
```

This is the Android platform's base MIME type for a content: URI containing a Cursor of zero or more items. Applications should use this as the base type along with their own sub-type of their content: URIs that represent a directory of items. For example, hypothetical IMAP email client may have a URI`content://com.company.provider.imap/inbox`for all of the messages in its inbox, whose MIME type would be reported as`CURSOR_DIR_BASE_TYPE + "/vnd.company.imap-msg"`

Note how the base MIME type varies between this and [CURSOR_ITEM_BASE_TYPE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#CURSOR_ITEM_BASE_TYPE:kotlin.String) depending on whether there is one single item or multiple items in the data set, while the sub-type remains the same because in either case the data structure contained in the cursor is the same. 

 Value: "vnd.android.cursor.dir"

### CURSOR_ITEM_BASE_TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CURSOR_ITEM_BASE_TYPE: String
```

This is the Android platform's base MIME type for a content: URI containing a Cursor of a single item. Applications should use this as the base type along with their own sub-type of their content: URIs that represent a particular item. For example, hypothetical IMAP email client may have a URI`content://com.company.provider.imap/inbox/1`for a particular message in the inbox, whose MIME type would be reported as`CURSOR_ITEM_BASE_TYPE + "/vnd.company.imap-msg"`

Compare with [CURSOR_DIR_BASE_TYPE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#CURSOR_DIR_BASE_TYPE:kotlin.String). 

 Value: "vnd.android.cursor.item"

### EXTRA_HONORED_ARGS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_HONORED_ARGS: String
```

Allows provider to report back to client which query keys are honored in a Cursor.

Key identifying a`String[]`containing all QUERY_ARG_SORT\* arguments honored by the provider. Include this in [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) extras [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) when any QUERY_ARG_SORT\* value was honored during the preparation of the results [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#).

If present, ALL honored arguments are enumerated in this extra's payload. 

 Value: "android.content.extra.HONORED_ARGS"

**See Also**

- [#QUERY_ARG_SORT_COLUMNS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_COLUMNS:kotlin.String)
- [#QUERY_ARG_SORT_DIRECTION](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_DIRECTION:kotlin.String)
- [#QUERY_ARG_SORT_COLLATION](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_COLLATION:kotlin.String)
- [#QUERY_ARG_SORT_LOCALE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_LOCALE:kotlin.String)
- [#QUERY_ARG_GROUP_COLUMNS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_GROUP_COLUMNS:kotlin.String) 

### EXTRA_REFRESH_SUPPORTED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_REFRESH_SUPPORTED: String
```

An extra boolean describing whether a particular provider supports refresh or not. If a provider supports refresh, it should include this key in its returned Cursor as part of its query call. 

 Value: "android.content.extra.REFRESH_SUPPORTED"

### EXTRA_SIZE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_SIZE: String
```

An extra [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#) describing the optimal size for a requested image resource, in pixels. If a provider has multiple sizes of the image, it should return the image closest to this size. 

 Value: "android.content.extra.SIZE"

**See Also**

- [#openTypedAssetFileDescriptor(Uri, String, Bundle)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openTypedAssetFileDescriptor(android.net.Uri,%20kotlin.String,%20android.os.Bundle))
- [#openTypedAssetFileDescriptor(Uri, String, Bundle,
* CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openTypedAssetFileDescriptor(android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.os.CancellationSignal)) 

### EXTRA_TOTAL_COUNT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_TOTAL_COUNT: String
```

Added to [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) extras [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) to indicate total row count of recordset when paging is supported. Providers must include this when implementing paging support.

A provider may return -1 that row count of the recordset is unknown.

Providers having returned -1 in a previous query are recommended to send content change notification once (if) full recordset size becomes known. 

 Value: "android.content.extra.TOTAL_COUNT"

### NOTIFY_DELETE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NOTIFY_DELETE: Int
```

Flag for [notifyChange(android.net.Uri,android.database.ContentObserver,int)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(android.net.Uri,%20android.database.ContentObserver,%20kotlin.Int)): typically set by a [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) to indicate that this notification is the result of a android.content.ContentProvider#delete call.

Sending these detailed flags are optional, but providers are strongly recommended to send them. 

 Value: 16

### NOTIFY_INSERT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NOTIFY_INSERT: Int
```

Flag for [notifyChange(android.net.Uri,android.database.ContentObserver,int)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(android.net.Uri,%20android.database.ContentObserver,%20kotlin.Int)): typically set by a [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) to indicate that this notification is the result of an android.content.ContentProvider#insert call.

Sending these detailed flags are optional, but providers are strongly recommended to send them. 

 Value: 4

### NOTIFY_SKIP_NOTIFY_FOR_DESCENDANTS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NOTIFY_SKIP_NOTIFY_FOR_DESCENDANTS: Int
```

Flag for [notifyChange(android.net.Uri,android.database.ContentObserver,int)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(android.net.Uri,%20android.database.ContentObserver,%20kotlin.Int)): if set, this notification will be skipped if it is being delivered to the root URI of a ContentObserver that is using "notify for descendants." The purpose of this is to allow the provide to send a general notification of "something under X" changed that observers of that specific URI can receive, while also sending a specific URI under X. It would use this flag when sending the former, so that observers of "X and descendants" only see the latter. 

 Value: 2

### NOTIFY_SYNC_TO_NETWORK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NOTIFY_SYNC_TO_NETWORK: Int
```

Flag for [notifyChange(android.net.Uri,android.database.ContentObserver,int)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(android.net.Uri,%20android.database.ContentObserver,%20kotlin.Int)): attempt to sync the change to the network. 

 Value: 1

### NOTIFY_UPDATE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NOTIFY_UPDATE: Int
```

Flag for [notifyChange(android.net.Uri,android.database.ContentObserver,int)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(android.net.Uri,%20android.database.ContentObserver,%20kotlin.Int)): typically set by a [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) to indicate that this notification is the result of an android.content.ContentProvider#update call.

Sending these detailed flags are optional, but providers are strongly recommended to send them. 

 Value: 8

### QUERY_ARG_GROUP_COLUMNS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUERY_ARG_GROUP_COLUMNS: String
```

Specifies the list of columns (stored as a`String[]`) against which to group results. When column values are identical, multiple records are collapsed together into a single record.

Columns present in this list must also be included in the projection supplied to[ContentResolver.query(Uri, String[], Bundle, CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)).

Apps targeting [android.os.Build.VERSION_CODES#R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or higher:
- [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) implementations: When preparing data in[ContentProvider.query(Uri, String[], Bundle, CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)), if group columns is reflected in the returned Cursor, it is strongly recommended that [QUERY_ARG_SORT_COLUMNS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_COLUMNS:kotlin.String) then be included in the array of honored arguments reflected in [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) extras [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) under [EXTRA_HONORED_ARGS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#EXTRA_HONORED_ARGS:kotlin.String).
- When querying a provider, where no QUERY_ARG_SQL\* otherwise exists in the arguments [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#), the Content framework will attempt to synthesize an QUERY_ARG_SQL\* argument using the corresponding QUERY_ARG_SORT\* values. 

 Value: "android:query-arg-group-columns"

### QUERY_ARG_LIMIT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUERY_ARG_LIMIT: String
```

Specifies the max number of rows to include in a Cursor. 

 Value: "android:query-arg-limit"

### QUERY_ARG_OFFSET

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUERY_ARG_OFFSET: String
```

Specifies the offset row index within a Cursor. 

 Value: "android:query-arg-offset"

### QUERY_ARG_SORT_COLLATION

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUERY_ARG_SORT_COLLATION: String
```

Allows client to specify a hint to the provider declaring which collation to use when sorting values.

Providers may support custom collators. When specifying a custom collator the value is determined by the Provider.

[ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) implementations: When preparing data in[ContentProvider.query(Uri, String[], Bundle, CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)), if sort collation is reflected in the returned Cursor, it is strongly recommended that [QUERY_ARG_SORT_COLLATION](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_COLLATION:kotlin.String) then be included in the array of honored arguments reflected in [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) extras [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) under [EXTRA_HONORED_ARGS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#EXTRA_HONORED_ARGS:kotlin.String).

When querying a provider, where no QUERY_ARG_SQL\* otherwise exists in the arguments [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#), the Content framework will attempt to synthesize a QUERY_ARG_SQL\* argument using the corresponding QUERY_ARG_SORT\* values. 

 Value: "android:query-arg-sort-collation"

**See Also**

- [java.text.Collator#PRIMARY](https://developer.android.com/reference/kotlin/java/text/Collator.html#PRIMARY:kotlin.Int)
- [java.text.Collator#SECONDARY](https://developer.android.com/reference/kotlin/java/text/Collator.html#SECONDARY:kotlin.Int)
- [java.text.Collator#TERTIARY](https://developer.android.com/reference/kotlin/java/text/Collator.html#TERTIARY:kotlin.Int)
- [java.text.Collator#IDENTICAL](https://developer.android.com/reference/kotlin/java/text/Collator.html#IDENTICAL:kotlin.Int) 

### QUERY_ARG_SORT_COLUMNS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUERY_ARG_SORT_COLUMNS: String
```

Specifies the list of columns (stored as a`String[]`) against which to sort results. When first column values are identical, records are then sorted based on second column values, and so on.

Columns present in this list must also be included in the projection supplied to[ContentResolver.query(Uri, String[], Bundle, CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)).

Apps targeting [android.os.Build.VERSION_CODES#O](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int) or higher:
- [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) implementations: When preparing data in[ContentProvider.query(Uri, String[], Bundle, CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)), if sort columns is reflected in the returned Cursor, it is strongly recommended that [QUERY_ARG_SORT_COLUMNS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_COLUMNS:kotlin.String) then be included in the array of honored arguments reflected in [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) extras [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) under [EXTRA_HONORED_ARGS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#EXTRA_HONORED_ARGS:kotlin.String).
- When querying a provider, where no QUERY_ARG_SQL\* otherwise exists in the arguments [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#), the Content framework will attempt to synthesize a QUERY_ARG_SQL\* argument using the corresponding QUERY_ARG_SORT\* values. 

 Value: "android:query-arg-sort-columns"

### QUERY_ARG_SORT_DIRECTION

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUERY_ARG_SORT_DIRECTION: String
```

Specifies desired sort order. When unspecified a provider may provide a default sort direction, or choose to return unsorted results.

Apps targeting [android.os.Build.VERSION_CODES#O](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int) or higher:
- [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) implementations: When preparing data in[ContentProvider.query(Uri, String[], Bundle, CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)), if sort direction is reflected in the returned Cursor, it is strongly recommended that [QUERY_ARG_SORT_DIRECTION](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_DIRECTION:kotlin.String) then be included in the array of honored arguments reflected in [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) extras [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) under [EXTRA_HONORED_ARGS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#EXTRA_HONORED_ARGS:kotlin.String).
- When querying a provider, where no QUERY_ARG_SQL\* otherwise exists in the arguments [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#), the Content framework will attempt to synthesize a QUERY_ARG_SQL\* argument using the corresponding QUERY_ARG_SORT\* values. 

 Value: "android:query-arg-sort-direction"

**See Also**

- [#QUERY_SORT_DIRECTION_ASCENDING](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_SORT_DIRECTION_ASCENDING:kotlin.Int)
- [#QUERY_SORT_DIRECTION_DESCENDING](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_SORT_DIRECTION_DESCENDING:kotlin.Int)

### QUERY_ARG_SORT_LOCALE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUERY_ARG_SORT_LOCALE: String
```

Allows client to specify a hint to the provider declaring which locale to use when sorting values.

The value is defined as a RFC 3066 locale ID followed by an optional keyword list, which is the locale format used to configure ICU through classes like [android.icu.util.ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#). This supports requesting advanced sorting options, such as`de@collation=phonebook`,`zh@collation=pinyin`, etc.

[ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) implementations: When preparing data in[ContentProvider.query(Uri, String[], Bundle, CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)), if sort locale is reflected in the returned Cursor, it is strongly recommended that [QUERY_ARG_SORT_LOCALE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_LOCALE:kotlin.String) then be included in the array of honored arguments reflected in [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) extras [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) under [EXTRA_HONORED_ARGS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#EXTRA_HONORED_ARGS:kotlin.String). 

 Value: "android:query-arg-sort-locale"

**See Also**

- [java.util.Locale#Locale(String)](https://developer.android.com/reference/kotlin/java/util/Locale.html#Locale(kotlin.String))
- [android.icu.util.ULocale#ULocale(String)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#ULocale(kotlin.String)) 

### QUERY_ARG_SQL_GROUP_BY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUERY_ARG_SQL_GROUP_BY: String
```

Key for an SQL style`GROUP BY`string that may be present in the query Bundle argument passed to[ContentProvider.query(Uri, String[], Bundle, CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)).

**Apps targeting [android.os.Build.VERSION_CODES#O](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int) or higher are strongly encourage to use structured query arguments in lieu of opaque SQL query clauses.** 

 Value: "android:query-arg-sql-group-by"

**See Also**

- [#QUERY_ARG_GROUP_COLUMNS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_GROUP_COLUMNS:kotlin.String) 

### QUERY_ARG_SQL_HAVING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUERY_ARG_SQL_HAVING: String
```

Key for an SQL style`HAVING`string that may be present in the query Bundle argument passed to[ContentProvider.query(Uri, String[], Bundle, CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)).

**Apps targeting [android.os.Build.VERSION_CODES#O](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int) or higher are strongly encourage to use structured query arguments in lieu of opaque SQL query clauses.** 

 Value: "android:query-arg-sql-having"

### QUERY_ARG_SQL_LIMIT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUERY_ARG_SQL_LIMIT: String
```

Key for an SQL style`LIMIT`string that may be present in the query Bundle argument passed to[ContentProvider.query(Uri, String[], Bundle, CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal)).

**Apps targeting [android.os.Build.VERSION_CODES#O](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int) or higher are strongly encourage to use structured query arguments in lieu of opaque SQL query clauses.** 

 Value: "android:query-arg-sql-limit"

**See Also**

- [#QUERY_ARG_LIMIT](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_LIMIT:kotlin.String)
- [#QUERY_ARG_OFFSET](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_OFFSET:kotlin.String) 

### QUERY_ARG_SQL_SELECTION

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUERY_ARG_SQL_SELECTION: String
```

Key for an SQL style selection string that may be present in the query Bundle argument passed to[ContentProvider.query(Uri, String[], Bundle, CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal))when called by a legacy client.

Clients should never include user supplied values directly in the selection string, as this presents an avenue for SQL injection attacks. In lieu of this, a client should use standard placeholder notation to represent values in a selection string, then supply a corresponding value in {@value #QUERY_ARG_SQL_SELECTION_ARGS}.

**Apps targeting [android.os.Build.VERSION_CODES#O](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int) or higher are strongly encourage to use structured query arguments in lieu of opaque SQL query clauses.** 

 Value: "android:query-arg-sql-selection"

**See Also**

- [#QUERY_ARG_SORT_COLUMNS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_COLUMNS:kotlin.String)
- [#QUERY_ARG_SORT_DIRECTION](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_DIRECTION:kotlin.String)
- [#QUERY_ARG_SORT_COLLATION](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_COLLATION:kotlin.String)
- [#QUERY_ARG_SORT_LOCALE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_LOCALE:kotlin.String) 

### QUERY_ARG_SQL_SELECTION_ARGS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUERY_ARG_SQL_SELECTION_ARGS: String
```

Key for SQL selection string arguments list.

Clients should never include user supplied values directly in the selection string, as this presents an avenue for SQL injection attacks. In lieu of this, a client should use standard placeholder notation to represent values in a selection string, then supply a corresponding value in {@value #QUERY_ARG_SQL_SELECTION_ARGS}.

**Apps targeting [android.os.Build.VERSION_CODES#O](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int) or higher are strongly encourage to use structured query arguments in lieu of opaque SQL query clauses.** 

 Value: "android:query-arg-sql-selection-args"

**See Also**

- [#QUERY_ARG_SORT_COLUMNS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_COLUMNS:kotlin.String)
- [#QUERY_ARG_SORT_DIRECTION](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_DIRECTION:kotlin.String)
- [#QUERY_ARG_SORT_COLLATION](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_COLLATION:kotlin.String)
- [#QUERY_ARG_SORT_LOCALE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_LOCALE:kotlin.String) 

### QUERY_ARG_SQL_SORT_ORDER

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUERY_ARG_SQL_SORT_ORDER: String
```

Key for an SQL style sort string that may be present in the query Bundle argument passed to[ContentProvider.query(Uri, String[], Bundle, CancellationSignal)](https://developer.android.com/reference/kotlin/android/content/ContentProvider#query(android.net.Uri,%20kotlin.Array,%20android.os.Bundle,%20android.os.CancellationSignal))when called by a legacy client.

**Apps targeting [android.os.Build.VERSION_CODES#O](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int) or higher are strongly encourage to use structured query arguments in lieu of opaque SQL query clauses.** 

 Value: "android:query-arg-sql-sort-order"

**See Also**

- [#QUERY_ARG_SORT_COLUMNS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_COLUMNS:kotlin.String)
- [#QUERY_ARG_SORT_DIRECTION](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_DIRECTION:kotlin.String)
- [#QUERY_ARG_SORT_COLLATION](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_COLLATION:kotlin.String)
- [#QUERY_ARG_SORT_LOCALE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_LOCALE:kotlin.String) 

### QUERY_SORT_DIRECTION_ASCENDING

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUERY_SORT_DIRECTION_ASCENDING: Int
```  

 Value: 0

### QUERY_SORT_DIRECTION_DESCENDING

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUERY_SORT_DIRECTION_DESCENDING: Int
```  

 Value: 1

### SCHEME_ANDROID_RESOURCE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCHEME_ANDROID_RESOURCE: String
```  

 Value: "android.resource"

### SCHEME_CONTENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCHEME_CONTENT: String
```  

 Value: "content"

### SCHEME_FILE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCHEME_FILE: String
```  

 Value: "file"

### SYNC_EXTRAS_ACCOUNT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_EXTRAS_ACCOUNT: String
```

**Deprecated:** *instead use [requestSync(android.accounts.Account,java.lang.String,android.os.Bundle)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#requestSync(android.accounts.Account,%20kotlin.String,%20android.os.Bundle))* 

 Value: "account"

### SYNC_EXTRAS_DISCARD_LOCAL_DELETIONS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_EXTRAS_DISCARD_LOCAL_DELETIONS: String
```

Indicates that the sync adapter should not proceed with the delete operations, if it determines that there are too many. See [SyncResult.tooManyDeletions](https://developer.android.com/reference/kotlin/android/content/SyncResult#tooManyDeletions:kotlin.Boolean) 

 Value: "discard_deletions"

### SYNC_EXTRAS_DO_NOT_RETRY

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_EXTRAS_DO_NOT_RETRY: String
```

If this extra is set to true then the request will not be retried if it fails. 

 Value: "do_not_retry"

### SYNC_EXTRAS_EXPEDITED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_EXTRAS_EXPEDITED: String
```

If this extra is set to true, the sync request will be scheduled at the front of the sync request queue, but it is still subject to JobScheduler quota and throttling due to App Standby buckets.

This is different from [SYNC_EXTRAS_SCHEDULE_AS_EXPEDITED_JOB](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_SCHEDULE_AS_EXPEDITED_JOB:kotlin.String). 

 Value: "expedited"

### SYNC_EXTRAS_FORCE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_EXTRAS_FORCE: String
```

**Deprecated:** *instead use [SYNC_EXTRAS_MANUAL](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_MANUAL:kotlin.String)* 

 Value: "force"

### SYNC_EXTRAS_IGNORE_BACKOFF

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_EXTRAS_IGNORE_BACKOFF: String
```

If this extra is set to true then any backoffs for the initial attempt (e.g. due to retries) are ignored by the sync scheduler. If this request fails and gets rescheduled then the retries will still honor the backoff. 

 Value: "ignore_backoff"

### SYNC_EXTRAS_IGNORE_SETTINGS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_EXTRAS_IGNORE_SETTINGS: String
```

If this extra is set to true then the sync settings (like getSyncAutomatically()) are ignored by the sync scheduler. 

 Value: "ignore_settings"

### SYNC_EXTRAS_INITIALIZE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_EXTRAS_INITIALIZE: String
```

Set by the SyncManager to request that the SyncAdapter initialize itself for the given account/authority pair. One required initialization step is to ensure that [setIsSyncable(android.accounts.Account,java.lang.String,int)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#setIsSyncable(android.accounts.Account,%20kotlin.String,%20kotlin.Int))has been called with a \>= 0 value. When this flag is set the SyncAdapter does not need to do a full sync, though it is allowed to do so. 

 Value: "initialize"

### SYNC_EXTRAS_MANUAL

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_EXTRAS_MANUAL: String
```

Setting this extra is the equivalent of setting both [SYNC_EXTRAS_IGNORE_SETTINGS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_IGNORE_SETTINGS:kotlin.String) and [SYNC_EXTRAS_IGNORE_BACKOFF](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_IGNORE_BACKOFF:kotlin.String) 

 Value: "force"

### SYNC_EXTRAS_OVERRIDE_TOO_MANY_DELETIONS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_EXTRAS_OVERRIDE_TOO_MANY_DELETIONS: String
```

Indicates that the sync adapter should proceed with the delete operations, even if it determines that there are too many. See [SyncResult.tooManyDeletions](https://developer.android.com/reference/kotlin/android/content/SyncResult#tooManyDeletions:kotlin.Boolean) 

 Value: "deletions_override"

### SYNC_EXTRAS_REQUIRE_CHARGING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_EXTRAS_REQUIRE_CHARGING: String
```

If this extra is set to true, the sync request will be scheduled only when the device is plugged in. This is equivalent to calling setRequiresCharging(true) on [SyncRequest](https://developer.android.com/reference/kotlin/android/content/SyncRequest). 

 Value: "require_charging"

### SYNC_EXTRAS_SCHEDULE_AS_EXPEDITED_JOB

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_EXTRAS_SCHEDULE_AS_EXPEDITED_JOB: String
```

Run this sync operation as an "expedited job" (see [android.app.job.JobInfo.Builder#setExpedited(boolean)](https://developer.android.com/reference/kotlin/android/app/job/JobInfo.Builder.html#setExpedited(kotlin.Boolean))). Normally (if this flag isn't specified), sync operations are executed as regular [android.app.job.JobService](https://developer.android.com/reference/kotlin/android/app/job/JobService.html#) jobs.

Because Expedited Jobs have various restrictions compared to regular jobs, this flag cannot be combined with certain other flags, otherwise an`IllegalArgumentException`will be thrown. Notably, because Expedited Jobs do not support various constraints, the following restriction apply:

- Can't be used with [SYNC_EXTRAS_REQUIRE_CHARGING](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_REQUIRE_CHARGING:kotlin.String)
- Can't be used with [SYNC_EXTRAS_EXPEDITED](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_EXPEDITED:kotlin.String)
- Can't be used on periodic syncs.
- When an expedited-job-sync fails and a retry is scheduled, the retried sync will be scheduled as a regular job unless [SYNC_EXTRAS_IGNORE_BACKOFF](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_IGNORE_BACKOFF:kotlin.String) is set.

This is different from [SYNC_EXTRAS_EXPEDITED](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_EXPEDITED:kotlin.String). 

 Value: "schedule_as_expedited_job"

### SYNC_EXTRAS_UPLOAD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_EXTRAS_UPLOAD: String
```

Indicates that this sync is intended to only upload local changes to the server. For example, this will be set to true if the sync is initiated by a call to [ContentResolver.notifyChange(android.net.Uri, android.database.ContentObserver, boolean)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(android.net.Uri,%20android.database.ContentObserver,%20kotlin.Boolean)) 

 Value: "upload"

### SYNC_OBSERVER_TYPE_ACTIVE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_OBSERVER_TYPE_ACTIVE: Int
```  

 Value: 4

### SYNC_OBSERVER_TYPE_PENDING

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_OBSERVER_TYPE_PENDING: Int
```  

 Value: 2

### SYNC_OBSERVER_TYPE_SETTINGS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC_OBSERVER_TYPE_SETTINGS: Int
```  

 Value: 1

## Public constructors

### ContentResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ContentResolver(context: Context?)
```

Note: passing a`null`context here could lead to unexpected behavior in certain ContentResolver APIs so it is highly recommended to pass a non-null context here.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context)?:This value may be`null`. |

## Public methods

### acquireContentProviderClient

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun acquireContentProviderClient(uri: Uri): ContentProviderClient?
```

Returns a [ContentProviderClient](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient) that is associated with the [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) that services the content at uri, starting the provider if necessary. Returns null if there is no provider associated wih the uri. The caller must indicate that they are done with the provider by calling [ContentProviderClient.release](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#release())which will allow the system to release the provider if it determines that there is no other reason for keeping it active.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):specifies which provider should be acquired This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ContentProviderClient](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient)? | a [ContentProviderClient](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient) that is associated with the [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) that services the content at uri or null if there isn't one. |

### acquireContentProviderClient

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun acquireContentProviderClient(name: String): ContentProviderClient?
```

Returns a [ContentProviderClient](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient) that is associated with the [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) with the authority of name, starting the provider if necessary. Returns null if there is no provider associated wih the uri. The caller must indicate that they are done with the provider by calling [ContentProviderClient.release](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient#release())which will allow the system to release the provider if it determines that there is no other reason for keeping it active.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):specifies which provider should be acquired This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ContentProviderClient](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient)? | a [ContentProviderClient](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient) that is associated with the [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) with the authority of name or null if there isn't one. |

### acquireUnstableContentProviderClient

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun acquireUnstableContentProviderClient(uri: Uri): ContentProviderClient?
```

Like [acquireContentProviderClient(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#acquireContentProviderClient(android.net.Uri)), but for use when you do not trust the stability of the target content provider. This turns off the mechanism in the platform clean up processes that are dependent on a content provider if that content provider's process goes away. Normally you can safely assume that once you have acquired a provider, you can freely use it as needed and it won't disappear, even if your process is in the background. If using this method, you need to take care to deal with any failures when communicating with the provider, and be sure to close it so that it can be re-opened later. In particular, catching a [android.os.DeadObjectException](https://developer.android.com/reference/kotlin/android/os/DeadObjectException.html#) from the calls there will let you know that the content provider has gone away; at that point the current ContentProviderClient object is invalid, and you should release it. You can acquire a new one if you would like to try to restart the provider and perform new operations on it.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|--------------------------|
| [ContentProviderClient](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient)? | This value may be`null`. |

### acquireUnstableContentProviderClient

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun acquireUnstableContentProviderClient(name: String): ContentProviderClient?
```

Like [acquireContentProviderClient(java.lang.String)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#acquireContentProviderClient(kotlin.String)), but for use when you do not trust the stability of the target content provider. This turns off the mechanism in the platform clean up processes that are dependent on a content provider if that content provider's process goes away. Normally you can safely assume that once you have acquired a provider, you can freely use it as needed and it won't disappear, even if your process is in the background. If using this method, you need to take care to deal with any failures when communicating with the provider, and be sure to close it so that it can be re-opened later. In particular, catching a [android.os.DeadObjectException](https://developer.android.com/reference/kotlin/android/os/DeadObjectException.html#) from the calls there will let you know that the content provider has gone away; at that point the current ContentProviderClient object is invalid, and you should release it. You can acquire a new one if you would like to try to restart the provider and perform new operations on it.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|--------------------------|
| [ContentProviderClient](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient)? | This value may be`null`. |

### addPeriodicSync

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun addPeriodicSync(
    account: Account!, 
    authority: String!, 
    extras: Bundle!, 
    pollFrequency: Long
): Unit
```

Specifies that a sync should be requested with the specified the account, authority, and extras at the given frequency. If there is already another periodic sync scheduled with the account, authority and extras then a new periodic sync won't be added, instead the frequency of the previous one will be updated.

These periodic syncs honor the "syncAutomatically" and "masterSyncAutomatically" settings. Although these sync are scheduled at the specified frequency, it may take longer for it to actually be started if other syncs are ahead of it in the sync operation queue. This means that the actual start time may drift.

Periodic syncs are not allowed to have any of [SYNC_EXTRAS_DO_NOT_RETRY](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_DO_NOT_RETRY:kotlin.String), [SYNC_EXTRAS_IGNORE_BACKOFF](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_IGNORE_BACKOFF:kotlin.String), [SYNC_EXTRAS_IGNORE_SETTINGS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_IGNORE_SETTINGS:kotlin.String), [SYNC_EXTRAS_INITIALIZE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_INITIALIZE:kotlin.String), [SYNC_EXTRAS_FORCE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_FORCE:kotlin.String), [SYNC_EXTRAS_EXPEDITED](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_EXPEDITED:kotlin.String), [SYNC_EXTRAS_MANUAL](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_MANUAL:kotlin.String), [SYNC_EXTRAS_SCHEDULE_AS_EXPEDITED_JOB](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_SCHEDULE_AS_EXPEDITED_JOB:kotlin.String) set to true. If any are supplied then an [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) will be thrown.

This method requires the caller to hold the permission [android.Manifest.permission#WRITE_SYNC_SETTINGS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_SYNC_SETTINGS:kotlin.String).

The bundle for a periodic sync can be queried by applications with the correct permissions using [ContentResolver.getPeriodicSyncs(Account account, String provider)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#getPeriodicSyncs(android.accounts.Account,%20kotlin.String)), so no sensitive data should be transferred here.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account.html#)!:the account to specify in the sync |
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the provider to specify in the sync request |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:extra parameters to go along with the sync request |
| `pollFrequency` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):how frequently the sync should be performed, in seconds. On Android API level 24 and above, a minimum interval of 15 minutes is enforced. On previous versions, the minimum interval is 1 hour. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if an illegal extra was set or if any of the parameters are null. |

### addStatusChangeListener

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun addStatusChangeListener(
    mask: Int, 
    callback: SyncStatusObserver!
): Any!
```

Request notifications when the different aspects of the SyncManager change. The different items that can be requested are:

- [SYNC_OBSERVER_TYPE_PENDING](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_OBSERVER_TYPE_PENDING:kotlin.Int)
- [SYNC_OBSERVER_TYPE_ACTIVE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_OBSERVER_TYPE_ACTIVE:kotlin.Int)
- [SYNC_OBSERVER_TYPE_SETTINGS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_OBSERVER_TYPE_SETTINGS:kotlin.Int)

The caller can set one or more of the status types in the mask for any given listener registration.

<br />

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the status change types that will cause the callback to be invoked |
| `callback` | [SyncStatusObserver](https://developer.android.com/reference/kotlin/android/content/SyncStatusObserver)!:observer to be invoked when the status changes |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | a handle that can be used to remove the listener at a later time |

### applyBatch

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyBatch(
    authority: String, 
    operations: ArrayList<ContentProviderOperation!>
): Array<ContentProviderResult!>
```

Applies each of the [ContentProviderOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation) objects and returns an array of their results. Passes through OperationApplicationException, which may be thrown by the call to [ContentProviderOperation.apply](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#apply(android.content.ContentProvider,%20kotlin.Array,%20kotlin.Int)). If all the applications succeed then a [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult) array with the same number of elements as the operations will be returned. It is implementation-specific how many, if any, operations will have been successfully applied if a call to apply results in a [OperationApplicationException](https://developer.android.com/reference/kotlin/android/content/OperationApplicationException).

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the authority of the ContentProvider to which this batch should be applied This value cannot be`null`. |
| `operations` | [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [ContentProviderOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation)!\>:the operations to apply This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ContentProviderResult](https://developer.android.com/reference/kotlin/android/content/ContentProviderResult)!> | the results of the applications This value cannot be`null`. |

| Exceptions ||
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.content.OperationApplicationException` | thrown if an application fails. See [ContentProviderOperation.apply](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation#apply(android.content.ContentProvider,%20kotlin.Array,%20kotlin.Int))for more information. |
| `android.os.RemoteException` | thrown if a RemoteException is encountered while attempting to communicate with a remote provider. |

### bulkInsert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun bulkInsert(
    url: Uri, 
    values: Array<ContentValues!>
): Int
```

Inserts multiple rows into a table at the given URL. This function make no guarantees about the atomicity of the insertions.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URL of the table to insert into. This value cannot be`null`. |
| `values` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)!\>:The initial values for the newly inserted rows. The key is the column name for the field. Passing null will create an empty row. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of newly created rows. |

### call

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun call(
    uri: Uri, 
    method: String, 
    arg: String?, 
    extras: Bundle?
): Bundle?
```

Call a provider-defined method. This can be used to implement read or write interfaces which are cheaper than using a Cursor and/or do not fit into the traditional table model.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `method` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):provider-defined method name to call. Opaque to framework, but must be non-null. |
| `arg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:provider-defined String argument. May be null. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:provider-defined Bundle argument. May be null. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | a result Bundle, possibly null. Will be null if the ContentProvider does not implement call. |

| Exceptions ||
|--------------------------------------|--------------------------|
| `java.lang.NullPointerException` | if uri or method is null |
| `java.lang.IllegalArgumentException` | if uri is not known |

### call

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun call(
    authority: String, 
    method: String, 
    arg: String?, 
    extras: Bundle?
): Bundle?
```

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------|
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `method` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `arg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | This value may be`null`. |

### cancelSync

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun cancelSync(uri: Uri!): Unit
```

**Deprecated:** *instead use [cancelSync(android.accounts.Account,java.lang.String)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#cancelSync(android.accounts.Account,%20kotlin.String))*

Cancel any active or pending syncs that match the Uri. If the uri is null then all syncs will be canceled.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:the uri of the provider to sync or null to sync all providers. |

### cancelSync

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun cancelSync(
    account: Account!, 
    authority: String!
): Unit
```

Cancel any active or pending syncs that match account and authority. The account and authority can each independently be set to null, which means that syncs with any account or authority, respectively, will match.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account.html#)!:filters the syncs that match by this account |
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:filters the syncs that match by this authority |

### cancelSync

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun cancelSync(request: SyncRequest!): Unit
```

Remove the specified sync. This will cancel any pending or active syncs. If the request is for a periodic sync, this call will remove any future occurrences.

If a periodic sync is specified, the caller must hold the permission [android.Manifest.permission#WRITE_SYNC_SETTINGS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_SYNC_SETTINGS:kotlin.String).
It is possible to cancel a sync using a SyncRequest object that is not the same object with which you requested the sync. Do so by building a SyncRequest with the same adapter, frequency,**and** extras bundle.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [SyncRequest](https://developer.android.com/reference/kotlin/android/content/SyncRequest)!:SyncRequest object containing information about sync to cancel. |

### canonicalize

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun canonicalize(url: Uri): Uri?
```

Transform the given url to a canonical representation of its referenced resource, which can be used across devices, persisted, backed up and restored, etc. The returned Uri is still a fully capable Uri for use with its content provider, allowing you to do all of the same content provider operations as with the original Uri -- #query, [openInputStream(android.net.Uri)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openInputStream(android.net.Uri)), etc. The only difference in behavior between the original and new Uris is that the content provider may need to do some additional work at each call using it to resolve it to the correct resource, especially if the canonical Uri has been moved to a different environment.

If you are moving a canonical Uri between environments, you should perform another call to [canonicalize](https://developer.android.com/reference/kotlin/android/content/ContentResolver#canonicalize(android.net.Uri))with that original Uri to re-canonicalize it for the current environment. Alternatively, you may want to use [uncanonicalize](https://developer.android.com/reference/kotlin/android/content/ContentResolver#uncanonicalize(android.net.Uri))to transform it to a non-canonical Uri that works only in the current environment but potentially more efficiently than the canonical representation.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) that is to be transformed to a canonical representation. Like all resolver calls, the input can be either a non-canonical or canonical Uri. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | Returns the official canonical representation of url, or null if the content provider does not support a canonical representation of the given Uri. Many providers may not support canonicalization of some or all of their Uris. |

**See Also**

- [#uncanonicalize](https://developer.android.com/reference/kotlin/android/content/ContentResolver#uncanonicalize(android.net.Uri)) 

### delete

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun delete(
    url: Uri, 
    extras: Bundle?
): Int
```

Deletes row(s) specified by a content URI. If the content provider supports transactions, the deletion will be atomic.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URL of the row to delete. This value cannot be`null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:A Bundle containing additional information necessary for the operation. Arguments may include SQL style arguments, such as [ContentResolver.QUERY_ARG_SQL_LIMIT](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SQL_LIMIT:kotlin.String), but note that the documentation for each individual provider will indicate which arguments they support. This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of rows deleted. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the provider doesn't support one of the requested Bundle arguments. |

### delete

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun delete(
    url: Uri, 
    where: String?, 
    selectionArgs: Array<String!>?
): Int
```

Deletes row(s) specified by a content URI. If the content provider supports transactions, the deletion will be atomic.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URL of the row to delete. This value cannot be`null`. |
| `where` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:A filter to apply to rows before deleting, formatted as an SQL WHERE clause (excluding the WHERE itself). This value may be`null`. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of rows deleted. |

### getCurrentSync

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getCurrentSync(): SyncInfo!
```

**Deprecated:** *Since multiple concurrent syncs are now supported you should use [getCurrentSyncs()](https://developer.android.com/reference/kotlin/android/content/ContentResolver#getCurrentSyncs())to get the accurate list of current syncs. This method returns the first item from the list of current syncs or null if there are none.*

If a sync is active returns the information about it, otherwise returns null.

This method requires the caller to hold the permission [android.Manifest.permission#READ_SYNC_STATS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_SYNC_STATS:kotlin.String).

<br />

| Return ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [SyncInfo](https://developer.android.com/reference/kotlin/android/content/SyncInfo)! | the SyncInfo for the currently active sync or null if one is not active. |

### getCurrentSyncs

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getCurrentSyncs(): MutableList<SyncInfo!>!
```

Returns a list with information about all the active syncs. This list will be empty if there are no active syncs.

This method requires the caller to hold the permission [android.Manifest.permission#READ_SYNC_STATS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_SYNC_STATS:kotlin.String).

<br />

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [SyncInfo](https://developer.android.com/reference/kotlin/android/content/SyncInfo)!>! | a List of SyncInfo objects for the currently active syncs. |

### getIsSyncable

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getIsSyncable(
    account: Account!, 
    authority: String!
): Int
```

Check if this account/provider is syncable.

This method requires the caller to hold the permission [android.Manifest.permission#READ_SYNC_SETTINGS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_SYNC_SETTINGS:kotlin.String).

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | \>0 if it is syncable, 0 if not, and \<0 if the state isn't known yet. |

### getMasterSyncAutomatically

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getMasterSyncAutomatically(): Boolean
```

Gets the global auto-sync setting that applies to all the providers and accounts. If this is false then the per-provider auto-sync setting is ignored.

This method requires the caller to hold the permission [android.Manifest.permission#READ_SYNC_SETTINGS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_SYNC_SETTINGS:kotlin.String).

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the global auto-sync setting that applies to all the providers and accounts |

### getOutgoingPersistedUriPermissions

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOutgoingPersistedUriPermissions(): MutableList<UriPermission!>
```

Return list of all persisted URI permission grants that are hosted by the calling app. That is, the returned permissions have been granted*from* the calling app. Only grants taken with [takePersistableUriPermission(android.net.Uri,int)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#takePersistableUriPermission(android.net.Uri,%20kotlin.Int))are returned.

Note: Some of the returned URIs may not be usable until after the user is unlocked.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [UriPermission](https://developer.android.com/reference/kotlin/android/content/UriPermission)!> | This value cannot be`null`. |

### getPeriodicSyncs

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getPeriodicSyncs(
    account: Account!, 
    authority: String!
): MutableList<PeriodicSync!>!
```

Get the list of information about the periodic syncs for the given account and authority.

This method requires the caller to hold the permission [android.Manifest.permission#READ_SYNC_SETTINGS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_SYNC_SETTINGS:kotlin.String).

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account.html#)!:the account whose periodic syncs we are querying |
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the provider whose periodic syncs we are querying |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PeriodicSync](https://developer.android.com/reference/kotlin/android/content/PeriodicSync)!>! | a list of PeriodicSync objects. This list may be empty but will never be null. |

### getPersistedUriPermissions

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPersistedUriPermissions(): MutableList<UriPermission!>
```

Return list of all URI permission grants that have been persisted by the calling app. That is, the returned permissions have been granted*to* the calling app. Only persistable grants taken with [takePersistableUriPermission(android.net.Uri,int)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#takePersistableUriPermission(android.net.Uri,%20kotlin.Int))are returned.

Note: Some of the returned URIs may not be usable until after the user is unlocked.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [UriPermission](https://developer.android.com/reference/kotlin/android/content/UriPermission)!> | This value cannot be`null`. |

**See Also**

- [#takePersistableUriPermission(Uri, int)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#takePersistableUriPermission(android.net.Uri,%20kotlin.Int))
- [#releasePersistableUriPermission(Uri, int)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#releasePersistableUriPermission(android.net.Uri,%20kotlin.Int)) 

### getStreamTypes

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStreamTypes(
    url: Uri, 
    mimeTypeFilter: String
): Array<String!>?
```

Query for the possible MIME types for the representations the given content URL can be returned when opened as as stream with #openTypedAssetFileDescriptor. Note that the types here are not necessarily a superset of the type returned by [getType](https://developer.android.com/reference/kotlin/android/content/ContentResolver#getType(android.net.Uri))-- many content providers cannot return a raw stream for the structured data that they contain.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):A Uri identifying content (either a list or specific type), using the content:// scheme. This value cannot be`null`. |
| `mimeTypeFilter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The desired MIME type. This may be a pattern, such as \*/\*, to query for all available MIME types that match the pattern. This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>? | Returns an array of MIME type strings for all available data streams that match the given mimeTypeFilter. If there are none, null is returned. |

### getSyncAdapterTypes

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getSyncAdapterTypes(): Array<SyncAdapterType!>!
```

Get information about the SyncAdapters that are known to the system.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [SyncAdapterType](https://developer.android.com/reference/kotlin/android/content/SyncAdapterType)!>! | an array of SyncAdapters that have registered with the system |

### getSyncAutomatically

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getSyncAutomatically(
    account: Account!, 
    authority: String!
): Boolean
```

Check if the provider should be synced when a network tickle is received

This method requires the caller to hold the permission [android.Manifest.permission#READ_SYNC_SETTINGS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_SYNC_SETTINGS:kotlin.String).

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account.html#)!:the account whose setting we are querying |
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the provider whose setting we are querying |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the provider should be synced when a network tickle is received |

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(url: Uri): String?
```

Return the MIME type of the given content URL.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):A Uri identifying content (either a list or specific type), using the content:// scheme. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | A MIME type for the content, or null if the URL is invalid or the type is unknown |

### getTypeInfo

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTypeInfo(mimeType: String): ContentResolver.MimeTypeInfo
```

Return a detailed description of the given MIME type, including an icon and label that describe the type.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):Valid, concrete MIME type. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ContentResolver.MimeTypeInfo](https://developer.android.com/reference/kotlin/android/content/ContentResolver.MimeTypeInfo) | This value cannot be`null`. |

### insert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun insert(
    url: Uri, 
    values: ContentValues?
): Uri?
```

Inserts a row into a table at the given URL. If the content provider supports transactions the insertion will be atomic.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URL of the table to insert into. This value cannot be`null`. |
| `values` | [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)?:The initial values for the newly inserted row. The key is the column name for the field. Passing an empty ContentValues will create an empty row. This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | the URL of the newly created row. May return`null`if the underlying content provider returns`null`, or if it crashes. |

### insert

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun insert(
    url: Uri, 
    values: ContentValues?, 
    extras: Bundle?
): Uri?
```

Inserts a row into a table at the given URL. If the content provider supports transactions the insertion will be atomic.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URL of the table to insert into. This value cannot be`null`. |
| `values` | [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)?:The initial values for the newly inserted row. The key is the column name for the field. Passing an empty ContentValues will create an empty row. This value may be`null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:A Bundle containing additional information necessary for the operation. Arguments may include SQL style arguments, such as [ContentResolver.QUERY_ARG_SQL_LIMIT](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SQL_LIMIT:kotlin.String), but note that the documentation for each individual provider will indicate which arguments they support. This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | the URL of the newly created row. May return`null`if the underlying content provider returns`null`, or if it crashes. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the provider doesn't support one of the requested Bundle arguments. |

### isSyncActive

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isSyncActive(
    account: Account!, 
    authority: String!
): Boolean
```

Returns true if there is currently a sync operation for the given account or authority actively being processed.

This method requires the caller to hold the permission [android.Manifest.permission#READ_SYNC_STATS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_SYNC_STATS:kotlin.String).

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account.html#)!:the account whose setting we are querying |
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the provider whose behavior is being queried |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if a sync is active for the given account or authority. |

### isSyncPending

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isSyncPending(
    account: Account!, 
    authority: String!
): Boolean
```

Return true if the pending status is true of any matching authorities.

This method requires the caller to hold the permission [android.Manifest.permission#READ_SYNC_STATS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_SYNC_STATS:kotlin.String).

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account.html#)!:the account whose setting we are querying |
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the provider whose behavior is being queried |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if there is a pending sync with the matching account and authority |

### loadThumbnail

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun loadThumbnail(
    uri: Uri, 
    size: Size, 
    signal: CancellationSignal?
): Bitmap
```

Convenience method that efficiently loads a visual thumbnail for the given [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#). Internally calls android.content.ContentProvider#openTypedAssetFile on the remote provider, but also defensively resizes any returned content to match the requested target size.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The item that should be visualized as a thumbnail. This value cannot be`null`. |
| `size` | [Size](https://developer.android.com/reference/kotlin/android/util/Size.html#):The target area on the screen where this thumbnail will be shown. This is passed to the provider as [EXTRA_SIZE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#EXTRA_SIZE:kotlin.String) to help it avoid downloading or generating heavy resources. This value cannot be`null`. |
| `signal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:A signal to cancel the operation in progress. This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#) | Valid [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#) which is a visual thumbnail. This value cannot be`null`. |

| Exceptions ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | If any trouble was encountered while generating or loading the thumbnail, or if [CancellationSignal.cancel()](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#cancel())was invoked. |

### notifyChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun notifyChange(
    uri: Uri, 
    observer: ContentObserver?
): Unit
```

Notify registered observers that a row was updated and attempt to sync changes to the network.

To observe events sent through this call, use [registerContentObserver(android.net.Uri,boolean,android.database.ContentObserver)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#registerContentObserver(android.net.Uri,%20kotlin.Boolean,%20android.database.ContentObserver)).

Starting in [android.os.Build.VERSION_CODES#O](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int), all content notifications must be backed by a valid [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider).

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The uri of the content that was changed. This value cannot be`null`. |
| `observer` | [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#)?:The observer that originated the change, may be`null. The observer that originated the change will only receive the notification if it has requested to receive self-change notifications by implementing ` [ContentObserver.deliverSelfNotifications()](https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#deliverSelfNotifications())` to return true.` |

### notifyChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun notifyChange(
    uri: Uri, 
    observer: ContentObserver?, 
    syncToNetwork: Boolean
): Unit
```

**Deprecated:** *callers should consider migrating to [notifyChange(android.net.Uri,android.database.ContentObserver,int)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(android.net.Uri,%20android.database.ContentObserver,%20kotlin.Int)), as it offers support for many more options than just [NOTIFY_SYNC_TO_NETWORK](https://developer.android.com/reference/kotlin/android/content/ContentResolver#NOTIFY_SYNC_TO_NETWORK:kotlin.Int).*

Notify registered observers that a row was updated.

To observe events sent through this call, use [registerContentObserver(android.net.Uri,boolean,android.database.ContentObserver)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#registerContentObserver(android.net.Uri,%20kotlin.Boolean,%20android.database.ContentObserver)).

If syncToNetwork is true, this will attempt to schedule a local sync using the sync adapter that's registered for the authority of the provided uri. No account will be passed to the sync adapter, so all matching accounts will be synchronized.

Starting in [android.os.Build.VERSION_CODES#O](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int), all content notifications must be backed by a valid [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider).

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The uri of the content that was changed. This value cannot be`null`. |
| `observer` | [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#)?:The observer that originated the change, may be`null. The observer that originated the change will only receive the notification if it has requested to receive self-change notifications by implementing ` [ContentObserver.deliverSelfNotifications()](https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#deliverSelfNotifications())` to return true.` |
| `syncToNetwork` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true, same as [NOTIFY_SYNC_TO_NETWORK](https://developer.android.com/reference/kotlin/android/content/ContentResolver#NOTIFY_SYNC_TO_NETWORK:kotlin.Int). |

**See Also**

- [#requestSync(android.accounts.Account, String, android.os.Bundle)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#requestSync(android.accounts.Account,%20kotlin.String,%20android.os.Bundle)) 

### notifyChange

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun notifyChange(
    uri: Uri, 
    observer: ContentObserver?, 
    flags: Int
): Unit
```

Notify registered observers that a row was updated.

To observe events sent through this call, use [registerContentObserver(android.net.Uri,boolean,android.database.ContentObserver)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#registerContentObserver(android.net.Uri,%20kotlin.Boolean,%20android.database.ContentObserver)).

If [NOTIFY_SYNC_TO_NETWORK](https://developer.android.com/reference/kotlin/android/content/ContentResolver#NOTIFY_SYNC_TO_NETWORK:kotlin.Int) is set, this will attempt to schedule a local sync using the sync adapter that's registered for the authority of the provided uri. No account will be passed to the sync adapter, so all matching accounts will be synchronized.

Starting in [android.os.Build.VERSION_CODES#O](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int), all content notifications must be backed by a valid [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The uri of the content that was changed. This value cannot be`null`. |
| `observer` | [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#)?:The observer that originated the change, may be`null. The observer that originated the change will only receive the notification if it has requested to receive self-change notifications by implementing ` [ContentObserver.deliverSelfNotifications()](https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#deliverSelfNotifications())` to return true.` |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags: [NOTIFY_SYNC_TO_NETWORK](https://developer.android.com/reference/kotlin/android/content/ContentResolver#NOTIFY_SYNC_TO_NETWORK:kotlin.Int). Value is either`0`or a combination of [android.content.ContentResolver#NOTIFY_SYNC_TO_NETWORK](https://developer.android.com/reference/kotlin/android/content/ContentResolver#NOTIFY_SYNC_TO_NETWORK:kotlin.Int), [android.content.ContentResolver#NOTIFY_SKIP_NOTIFY_FOR_DESCENDANTS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#NOTIFY_SKIP_NOTIFY_FOR_DESCENDANTS:kotlin.Int), [android.content.ContentResolver#NOTIFY_INSERT](https://developer.android.com/reference/kotlin/android/content/ContentResolver#NOTIFY_INSERT:kotlin.Int), [android.content.ContentResolver#NOTIFY_UPDATE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#NOTIFY_UPDATE:kotlin.Int), and [android.content.ContentResolver#NOTIFY_DELETE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#NOTIFY_DELETE:kotlin.Int) |

**See Also**

- [#requestSync(android.accounts.Account, String, android.os.Bundle)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#requestSync(android.accounts.Account,%20kotlin.String,%20android.os.Bundle)) 

### notifyChange

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun notifyChange(
    uris: MutableCollection<Uri!>, 
    observer: ContentObserver?, 
    flags: Int
): Unit
```

Notify registered observers that several rows have been updated.

To observe events sent through this call, use [registerContentObserver(android.net.Uri,boolean,android.database.ContentObserver)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#registerContentObserver(android.net.Uri,%20kotlin.Boolean,%20android.database.ContentObserver)).

If [NOTIFY_SYNC_TO_NETWORK](https://developer.android.com/reference/kotlin/android/content/ContentResolver#NOTIFY_SYNC_TO_NETWORK:kotlin.Int) is set, this will attempt to schedule a local sync using the sync adapter that's registered for the authority of the provided uri. No account will be passed to the sync adapter, so all matching accounts will be synchronized.

Starting in [android.os.Build.VERSION_CODES#O](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int), all content notifications must be backed by a valid [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uris` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>:The uris of the content that was changed. This value cannot be`null`. |
| `observer` | [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#)?:The observer that originated the change, may be`null. The observer that originated the change will only receive the notification if it has requested to receive self-change notifications by implementing ` [ContentObserver.deliverSelfNotifications()](https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#deliverSelfNotifications())` to return true.` |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Flags such as [NOTIFY_SYNC_TO_NETWORK](https://developer.android.com/reference/kotlin/android/content/ContentResolver#NOTIFY_SYNC_TO_NETWORK:kotlin.Int) or [NOTIFY_SKIP_NOTIFY_FOR_DESCENDANTS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#NOTIFY_SKIP_NOTIFY_FOR_DESCENDANTS:kotlin.Int). Value is either`0`or a combination of [android.content.ContentResolver#NOTIFY_SYNC_TO_NETWORK](https://developer.android.com/reference/kotlin/android/content/ContentResolver#NOTIFY_SYNC_TO_NETWORK:kotlin.Int), [android.content.ContentResolver#NOTIFY_SKIP_NOTIFY_FOR_DESCENDANTS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#NOTIFY_SKIP_NOTIFY_FOR_DESCENDANTS:kotlin.Int), [android.content.ContentResolver#NOTIFY_INSERT](https://developer.android.com/reference/kotlin/android/content/ContentResolver#NOTIFY_INSERT:kotlin.Int), [android.content.ContentResolver#NOTIFY_UPDATE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#NOTIFY_UPDATE:kotlin.Int), and [android.content.ContentResolver#NOTIFY_DELETE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#NOTIFY_DELETE:kotlin.Int) |

### openAssetFile

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openAssetFile(
    uri: Uri, 
    mode: String, 
    signal: CancellationSignal?
): AssetFileDescriptor?
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `signal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|--------------------------|
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | This value may be`null`. |

### openAssetFileDescriptor

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openAssetFileDescriptor(
    uri: Uri, 
    mode: String
): AssetFileDescriptor?
```

Open a raw file descriptor to access data under a URI. This interacts with the underlying android.content.ContentProvider#openAssetFile method of the provider associated with the given URI, to retrieve any file stored there.

##### Accepts the following URI schemes:

- content ([SCHEME_CONTENT](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SCHEME_CONTENT:kotlin.String))
- android.resource ([SCHEME_ANDROID_RESOURCE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SCHEME_ANDROID_RESOURCE:kotlin.String))
- file ([SCHEME_FILE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SCHEME_FILE:kotlin.String))

##### The android.resource ([SCHEME_ANDROID_RESOURCE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SCHEME_ANDROID_RESOURCE:kotlin.String)) Scheme

<br />

A Uri object can be used to reference a resource in an APK file. The Uri should be one of the following formats:

- `android.resource://package_name/id_number` 
 `package_name`is your package name as listed in your AndroidManifest.xml. For example`com.example.myapp` 
 `id_number`is the int form of the ID. 
 The easiest way to construct this form is 

  ```kotlin
  Uri uri = Uri.parse("android.resource://com.example.myapp/" + R.raw.my_resource");
  ```
- `android.resource://package_name/type/name` 
 `package_name`is your package name as listed in your AndroidManifest.xml. For example`com.example.myapp` 
 `type`is the string form of the resource type. For example,`raw`or`drawable`.`name`is the string form of the resource name. That is, whatever the file name was in your res directory, without the type extension. The easiest way to construct this form is 

  ```kotlin
  Uri uri = Uri.parse("android.resource://com.example.myapp/raw/my_resource");
  ```

Note that if this function is called for read-only input (mode is "r") on a content: URI, it will instead call #openTypedAssetFileDescriptor for you with a MIME type of "\*/\*". This allows such callers to benefit from any built-in data conversion that a provider implements.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The desired URI to open. This value cannot be`null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The string representation of the file mode. Can be "r", "w", "wt", "wa", "rw" or "rwt". Please note the exact implementation of these may differ for each Provider implementation - for example, "w" may or may not truncate. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | Returns a new ParcelFileDescriptor pointing to the file or`null`if the provider recently crashed. You own this descriptor and are responsible for closing it when done. |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | Throws FileNotFoundException of no file exists under the URI or the mode is invalid. |

### openAssetFileDescriptor

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openAssetFileDescriptor(
    uri: Uri, 
    mode: String, 
    cancellationSignal: CancellationSignal?
): AssetFileDescriptor?
```

Open a raw file descriptor to access data under a URI. This interacts with the underlying android.content.ContentProvider#openAssetFile method of the provider associated with the given URI, to retrieve any file stored there.

##### Accepts the following URI schemes:

- content ([SCHEME_CONTENT](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SCHEME_CONTENT:kotlin.String))
- android.resource ([SCHEME_ANDROID_RESOURCE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SCHEME_ANDROID_RESOURCE:kotlin.String))
- file ([SCHEME_FILE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SCHEME_FILE:kotlin.String))

##### The android.resource ([SCHEME_ANDROID_RESOURCE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SCHEME_ANDROID_RESOURCE:kotlin.String)) Scheme

<br />

A Uri object can be used to reference a resource in an APK file. The Uri should be one of the following formats:

- `android.resource://package_name/id_number` 
 `package_name`is your package name as listed in your AndroidManifest.xml. For example`com.example.myapp` 
 `id_number`is the int form of the ID. 
 The easiest way to construct this form is 

  ```kotlin
  Uri uri = Uri.parse("android.resource://com.example.myapp/" + R.raw.my_resource");
  ```
- `android.resource://package_name/type/name` 
 `package_name`is your package name as listed in your AndroidManifest.xml. For example`com.example.myapp` 
 `type`is the string form of the resource type. For example,`raw`or`drawable`.`name`is the string form of the resource name. That is, whatever the file name was in your res directory, without the type extension. The easiest way to construct this form is 

  ```kotlin
  Uri uri = Uri.parse("android.resource://com.example.myapp/raw/my_resource");
  ```

Note that if this function is called for read-only input (mode is "r") on a content: URI, it will instead call #openTypedAssetFileDescriptor for you with a MIME type of "\*/\*". This allows such callers to benefit from any built-in data conversion that a provider implements.

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The desired URI to open. This value cannot be`null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The string representation of the file mode. Can be "r", "w", "wt", "wa", "rw" or "rwt". Please note "w" is write only and "wt" is write and truncate. See [ParcelFileDescriptor.parseMode](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#parseMode(kotlin.String))for more details. This value cannot be`null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:A signal to cancel the operation in progress, or null if none. If the operation is canceled, then [OperationCanceledException](https://developer.android.com/reference/kotlin/android/os/OperationCanceledException.html#) will be thrown. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | Returns a new ParcelFileDescriptor pointing to the file or`null`if the provider recently crashed. You own this descriptor and are responsible for closing it when done. |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | Throws FileNotFoundException of no file exists under the URI or the mode is invalid. |

### openFile

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openFile(
    uri: Uri, 
    mode: String, 
    signal: CancellationSignal?
): ParcelFileDescriptor?
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `signal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:This value may be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------------------|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)? | This value may be`null`. |

### openFileDescriptor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openFileDescriptor(
    uri: Uri, 
    mode: String
): ParcelFileDescriptor?
```

Open a raw file descriptor to access data under a URI. This is like [openAssetFileDescriptor(android.net.Uri,java.lang.String)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openAssetFileDescriptor(android.net.Uri,%20kotlin.String)), but uses the underlying android.content.ContentProvider#openFile ContentProvider.openFile()} method, so will*not* work with providers that return sub-sections of files. If at all possible, you should use [openAssetFileDescriptor(android.net.Uri,java.lang.String)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openAssetFileDescriptor(android.net.Uri,%20kotlin.String)). You will receive a FileNotFoundException exception if the provider returns a sub-section of a file.

##### Accepts the following URI schemes:

- content ([SCHEME_CONTENT](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SCHEME_CONTENT:kotlin.String))
- file ([SCHEME_FILE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SCHEME_FILE:kotlin.String))

<br />

See [openAssetFileDescriptor(android.net.Uri,java.lang.String)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openAssetFileDescriptor(android.net.Uri,%20kotlin.String))for more information on these schemes.

If opening with the exclusive "r" or "w" modes, the returned ParcelFileDescriptor could be a pipe or socket pair to enable streaming of data. Opening with the "rw" mode implies a file on disk that supports seeking. If possible, always use an exclusive mode to give the underlying [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) the most flexibility.

If you are writing a file, and need to communicate an error to the provider, use [ParcelFileDescriptor.closeWithError(String)](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#closeWithError(kotlin.String)).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The desired URI to open. This value cannot be`null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The string representation of the file mode. Can be "r", "w", "wt", "wa", "rw" or "rwt". Please note the exact implementation of these may differ for each Provider implementation - for example, "w" may or may not truncate. This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)? | Returns a new ParcelFileDescriptor pointing to the file or`null`if the provider recently crashed. You own this descriptor and are responsible for closing it when done. |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | Throws FileNotFoundException if no file exists under the URI or the mode is invalid. |

**See Also**

- [#openAssetFileDescriptor(Uri, String)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openAssetFileDescriptor(android.net.Uri,%20kotlin.String)) 

### openFileDescriptor

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openFileDescriptor(
    uri: Uri, 
    mode: String, 
    cancellationSignal: CancellationSignal?
): ParcelFileDescriptor?
```

Open a raw file descriptor to access data under a URI. This is like [openAssetFileDescriptor(android.net.Uri,java.lang.String)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openAssetFileDescriptor(android.net.Uri,%20kotlin.String)), but uses the underlying android.content.ContentProvider#openFile ContentProvider.openFile()} method, so will*not* work with providers that return sub-sections of files. If at all possible, you should use [openAssetFileDescriptor(android.net.Uri,java.lang.String)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openAssetFileDescriptor(android.net.Uri,%20kotlin.String)). You will receive a FileNotFoundException exception if the provider returns a sub-section of a file.

##### Accepts the following URI schemes:

- content ([SCHEME_CONTENT](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SCHEME_CONTENT:kotlin.String))
- file ([SCHEME_FILE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SCHEME_FILE:kotlin.String))

<br />

See [openAssetFileDescriptor(android.net.Uri,java.lang.String)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openAssetFileDescriptor(android.net.Uri,%20kotlin.String))for more information on these schemes.

If opening with the exclusive "r" or "w" modes, the returned ParcelFileDescriptor could be a pipe or socket pair to enable streaming of data. Opening with the "rw" mode implies a file on disk that supports seeking. If possible, always use an exclusive mode to give the underlying [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) the most flexibility.

If you are writing a file, and need to communicate an error to the provider, use [ParcelFileDescriptor.closeWithError(String)](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#closeWithError(kotlin.String)).

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The desired URI to open. This value cannot be`null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The string representation of the file mode. Can be "r", "w", "wt", "wa", "rw" or "rwt". Please note the exact implementation of these may differ for each Provider implementation - for example, "w" may or may not truncate. This value cannot be`null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:A signal to cancel the operation in progress, or null if none. If the operation is canceled, then [OperationCanceledException](https://developer.android.com/reference/kotlin/android/os/OperationCanceledException.html#) will be thrown. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)? | Returns a new ParcelFileDescriptor pointing to the file or`null`if the provider recently crashed. You own this descriptor and are responsible for closing it when done. |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | Throws FileNotFoundException if no file exists under the URI or the mode is invalid. |

**See Also**

- [#openAssetFileDescriptor(Uri, String)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openAssetFileDescriptor(android.net.Uri,%20kotlin.String)) 

### openInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openInputStream(uri: Uri): InputStream?
```

Open a stream on to the content associated with a content URI. If there is no data associated with the URI, FileNotFoundException is thrown.

##### Accepts the following URI schemes:

- content ([SCHEME_CONTENT](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SCHEME_CONTENT:kotlin.String))
- android.resource ([SCHEME_ANDROID_RESOURCE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SCHEME_ANDROID_RESOURCE:kotlin.String))
- file ([SCHEME_FILE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SCHEME_FILE:kotlin.String))

<br />

See [openAssetFileDescriptor(android.net.Uri,java.lang.String)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openAssetFileDescriptor(android.net.Uri,%20kotlin.String))for more information on these schemes.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The desired URI. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)? | InputStream or`null`if the provider recently crashed. |

| Exceptions ||
|---------------------------------|------------------------------------------|
| `java.io.FileNotFoundException` | if the provided URI could not be opened. |

**See Also**

- [#openAssetFileDescriptor(Uri, String)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openAssetFileDescriptor(android.net.Uri,%20kotlin.String)) 

### openOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openOutputStream(uri: Uri): OutputStream?
```

Synonym for [openOutputStream(uri, "w")](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openOutputStream(android.net.Uri,%20kotlin.String)). Please note the implementation of "w" is up to each Provider implementation and it may or may not truncate.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The desired URI. This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)? | an OutputStream or`null`if the provider recently crashed. |

| Exceptions ||
|---------------------------------|------------------------------------------|
| `java.io.FileNotFoundException` | if the provided URI could not be opened. |

### openOutputStream

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openOutputStream(
    uri: Uri, 
    mode: String
): OutputStream?
```

Open a stream on to the content associated with a content URI. If there is no data associated with the URI, FileNotFoundException is thrown.

##### Accepts the following URI schemes:

- content ([SCHEME_CONTENT](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SCHEME_CONTENT:kotlin.String))
- file ([SCHEME_FILE](https://developer.android.com/reference/kotlin/android/content/ContentResolver#SCHEME_FILE:kotlin.String))

<br />

See [openAssetFileDescriptor(android.net.Uri,java.lang.String)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openAssetFileDescriptor(android.net.Uri,%20kotlin.String))for more information on these schemes.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The desired URI. This value cannot be`null`. |
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The string representation of the file mode. Can be "r", "w", "wt", "wa", "rw" or "rwt". Please note the exact implementation of these may differ for each Provider implementation - for example, "w" may or may not truncate. This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)? | an OutputStream or`null`if the provider recently crashed. |

| Exceptions ||
|---------------------------------|------------------------------------------|
| `java.io.FileNotFoundException` | if the provided URI could not be opened. |

**See Also**

- [#openAssetFileDescriptor(Uri, String)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#openAssetFileDescriptor(android.net.Uri,%20kotlin.String)) 

### openTypedAssetFile

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openTypedAssetFile(
    uri: Uri, 
    mimeTypeFilter: String, 
    opts: Bundle?, 
    signal: CancellationSignal?
): AssetFileDescriptor?
```

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |
| `mimeTypeFilter` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `opts` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:This value may be`null`. |
| `signal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|--------------------------|
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | This value may be`null`. |

### openTypedAssetFileDescriptor

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openTypedAssetFileDescriptor(
    uri: Uri, 
    mimeType: String, 
    opts: Bundle?
): AssetFileDescriptor?
```

Open a raw file descriptor to access (potentially type transformed) data from a "content:" URI. This interacts with the underlying android.content.ContentProvider#openTypedAssetFile method of the provider associated with the given URI, to retrieve retrieve any appropriate data stream for the data stored there.

Unlike #openAssetFileDescriptor, this function only works with "content:" URIs, because content providers are the only facility with an associated MIME type to ensure that the returned data stream is of the desired type.

All text/\* streams are encoded in UTF-8.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The desired URI to open. This value cannot be`null`. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The desired MIME type of the returned data. This can be a pattern such as \*/\*, which will allow the content provider to select a type, though there is no way for you to determine what type it is returning. This value cannot be`null`. |
| `opts` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:Additional provider-dependent options. This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | Returns a new ParcelFileDescriptor from which you can read the data stream from the provider or`null`if the provider recently crashed. Note that this may be a pipe, meaning you can't seek in it. The only seek you should do is if the AssetFileDescriptor contains an offset, to move to that offset before reading. You own this descriptor and are responsible for closing it when done. |

| Exceptions ||
|---------------------------------|-----------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | Throws FileNotFoundException of no data of the desired type exists under the URI. |

### openTypedAssetFileDescriptor

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openTypedAssetFileDescriptor(
    uri: Uri, 
    mimeType: String, 
    opts: Bundle?, 
    cancellationSignal: CancellationSignal?
): AssetFileDescriptor?
```

Open a raw file descriptor to access (potentially type transformed) data from a "content:" URI. This interacts with the underlying android.content.ContentProvider#openTypedAssetFile method of the provider associated with the given URI, to retrieve any appropriate data stream for the data stored there.

Unlike #openAssetFileDescriptor, this function only works with "content:" URIs, because content providers are the only facility with an associated MIME type to ensure that the returned data stream is of the desired type.

All text/\* streams are encoded in UTF-8.

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The desired URI to open. This value cannot be`null`. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The desired MIME type of the returned data. This can be a pattern such as \*/\*, which will allow the content provider to select a type, though there is no way for you to determine what type it is returning. This value cannot be`null`. |
| `opts` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:Additional provider-dependent options. This value may be`null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:A signal to cancel the operation in progress, or null if none. If the operation is canceled, then [OperationCanceledException](https://developer.android.com/reference/kotlin/android/os/OperationCanceledException.html#) will be thrown. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor)? | Returns a new ParcelFileDescriptor from which you can read the data stream from the provider or`null`if the provider recently crashed. Note that this may be a pipe, meaning you can't seek in it. The only seek you should do is if the AssetFileDescriptor contains an offset, to move to that offset before reading. You own this descriptor and are responsible for closing it when done. |

| Exceptions ||
|---------------------------------|-----------------------------------------------------------------------------------|
| `java.io.FileNotFoundException` | Throws FileNotFoundException of no data of the desired type exists under the URI. |

### query

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun query(
    uri: Uri, 
    projection: Array<String!>?, 
    queryArgs: Bundle?, 
    cancellationSignal: CancellationSignal?
): Cursor?
```

Query the given URI, returning a [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) over the result set with support for cancellation.

For best performance, the caller should follow these guidelines:
- Provide an explicit projection, to prevent reading data from storage that aren't going to be used. Provider must identify which QUERY_ARG_SORT\* arguments were honored during the preparation of the result set by including the respective argument keys in the [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) extras [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#). See [EXTRA_HONORED_ARGS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#EXTRA_HONORED_ARGS:kotlin.String) for details.

| Parameters ||
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URI, using the content:// scheme, for the content to retrieve. This value cannot be`null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:A list of which columns to return. Passing null will return all columns, which is inefficient. |
| `queryArgs` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:A Bundle containing additional information necessary for the operation. Arguments may include SQL style arguments, such as [ContentResolver.QUERY_ARG_SQL_LIMIT](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SQL_LIMIT:kotlin.String), but note that the documentation for each individual provider will indicate which arguments they support. This value may be`null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:A signal to cancel the operation in progress, or null if none. If the operation is canceled, then [OperationCanceledException](https://developer.android.com/reference/kotlin/android/os/OperationCanceledException.html#) will be thrown when the query is executed. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | A Cursor object, which is positioned before the first entry. May return`null`if the underlying content provider returns`null`, or if it crashes. |

**See Also**

- [#QUERY_ARG_SORT_COLUMNS](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_COLUMNS:kotlin.String)
- [#QUERY_ARG_SORT_DIRECTION](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_DIRECTION:kotlin.String)
- [#QUERY_ARG_SORT_COLLATION](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SORT_COLLATION:kotlin.String)
- [android.database.Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)

### query

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun query(
    uri: Uri, 
    projection: Array<String!>?, 
    selection: String?, 
    selectionArgs: Array<String!>?, 
    sortOrder: String?
): Cursor?
```

Query the given URI, returning a [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) over the result set.

For best performance, the caller should follow these guidelines:

- Provide an explicit projection, to prevent reading data from storage that aren't going to be used.
- Use question mark parameter markers such as 'phone=?' instead of explicit values in the`selection`parameter, so that queries that differ only by those values will be recognized as the same for caching purposes.

<br />

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URI, using the content:// scheme, for the content to retrieve. This value cannot be`null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:A list of which columns to return. Passing null will return all columns, which is inefficient. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:A filter declaring which rows to return, formatted as an SQL WHERE clause (excluding the WHERE itself). Passing null will return all rows for the given URI. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:You may include ?s in selection, which will be replaced by the values from selectionArgs, in the order that they appear in the selection. The values will be bound as Strings. This value may be`null`. |
| `sortOrder` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:How to order the rows, formatted as an SQL ORDER BY clause (excluding the ORDER BY itself). Passing null will use the default sort order, which may be unordered. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | A Cursor object, which is positioned before the first entry. May return`null`if the underlying content provider returns`null`, or if it crashes. |

**See Also**

- [android.database.Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) 

### query

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun query(
    uri: Uri, 
    projection: Array<String!>?, 
    selection: String?, 
    selectionArgs: Array<String!>?, 
    sortOrder: String?, 
    cancellationSignal: CancellationSignal?
): Cursor?
```

Query the given URI, returning a [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) over the result set with optional support for cancellation.

For best performance, the caller should follow these guidelines:

- Provide an explicit projection, to prevent reading data from storage that aren't going to be used.
- Use question mark parameter markers such as 'phone=?' instead of explicit values in the`selection`parameter, so that queries that differ only by those values will be recognized as the same for caching purposes.

<br />

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URI, using the content:// scheme, for the content to retrieve. This value cannot be`null`. |
| `projection` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:A list of which columns to return. Passing null will return all columns, which is inefficient. |
| `selection` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:A filter declaring which rows to return, formatted as an SQL WHERE clause (excluding the WHERE itself). Passing null will return all rows for the given URI. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:You may include ?s in selection, which will be replaced by the values from selectionArgs, in the order that they appear in the selection. The values will be bound as Strings. This value may be`null`. |
| `sortOrder` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:How to order the rows, formatted as an SQL ORDER BY clause (excluding the ORDER BY itself). Passing null will use the default sort order, which may be unordered. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:A signal to cancel the operation in progress, or null if none. If the operation is canceled, then [OperationCanceledException](https://developer.android.com/reference/kotlin/android/os/OperationCanceledException.html#) will be thrown when the query is executed. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)? | A Cursor object, which is positioned before the first entry. May return`null`if the underlying content provider returns`null`, or if it crashes. |

**See Also**

- [android.database.Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) 

### refresh

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun refresh(
    url: Uri, 
    extras: Bundle?, 
    cancellationSignal: CancellationSignal?
): Boolean
```

This allows clients to request an explicit refresh of content identified by`uri`.

Client code should only invoke this method when there is a strong indication (such as a user initiated pull to refresh gesture) that the content is stale.

<br />

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The Uri identifying the data to refresh. This value cannot be`null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:Additional options from the client. The definitions of these are specific to the content provider being called. This value may be`null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:A signal to cancel the operation in progress, or`null`if none. For example, if you called refresh on a particular uri, you should call [CancellationSignal.throwIfCanceled()](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#throwIfCanceled())to check whether the client has canceled the refresh request. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the provider actually tried refreshing. |

### registerContentObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerContentObserver(
    uri: Uri, 
    notifyForDescendants: Boolean, 
    observer: ContentObserver
): Unit
```

Register an observer class that gets callbacks when data identified by a given content URI changes.

Starting in [android.os.Build.VERSION_CODES#O](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int), all content notifications must be backed by a valid [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider).

| Parameters ||
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URI to watch for changes. This can be a specific row URI, or a base URI for a whole class of content. This value cannot be`null`. |
| `notifyForDescendants` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):When false, the observer will be notified whenever a change occurs to the exact URI specified by`uri`or to one of the URI's ancestors in the path hierarchy. When true, the observer will also be notified whenever a change occurs to the URI's descendants in the path hierarchy. |
| `observer` | [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#):The object that receives callbacks when changes occur. This value cannot be`null`. |

**See Also**

- [#unregisterContentObserver](https://developer.android.com/reference/kotlin/android/content/ContentResolver#unregisterContentObserver(android.database.ContentObserver)) 

### releasePersistableUriPermission

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun releasePersistableUriPermission(
    uri: Uri, 
    modeFlags: Int
): Unit
```

Relinquish a persisted URI permission grant. The URI must have been previously made persistent with [takePersistableUriPermission(android.net.Uri,int)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#takePersistableUriPermission(android.net.Uri,%20kotlin.Int)). Any non-persistent grants to the calling package will remain intact.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |
| `modeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or a combination of [android.content.Intent#FLAG_GRANT_READ_URI_PERMISSION](https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int), and [android.content.Intent#FLAG_GRANT_WRITE_URI_PERMISSION](https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int) |

**See Also**

- <https://developer.android.com/reference/kotlin/android/content/ContentResolver#getPersistedUriPermissions()> 

### removePeriodicSync

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun removePeriodicSync(
    account: Account!, 
    authority: String!, 
    extras: Bundle!
): Unit
```

Remove a periodic sync. Has no affect if account, authority and extras don't match an existing periodic sync.

This method requires the caller to hold the permission [android.Manifest.permission#WRITE_SYNC_SETTINGS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_SYNC_SETTINGS:kotlin.String).

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account.html#)!:the account of the periodic sync to remove |
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the provider of the periodic sync to remove |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:the extras of the periodic sync to remove |

### removeStatusChangeListener

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun removeStatusChangeListener(handle: Any!): Unit
```

Remove a previously registered status change listener.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `handle` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the handle that was returned by [addStatusChangeListener](https://developer.android.com/reference/kotlin/android/content/ContentResolver#addStatusChangeListener(kotlin.Int,%20android.content.SyncStatusObserver)) |

### requestSync

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun requestSync(
    account: Account!, 
    authority: String!, 
    extras: Bundle!
): Unit
```

Start an asynchronous sync operation. If you want to monitor the progress of the sync you may register a SyncObserver. Only values of the following types may be used in the extras bundle:

- Integer
- Long
- Boolean
- Float
- Double
- String
- Account
- null

<br />

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account.html#)!:which account should be synced |
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:which authority should be synced |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:any extras to pass to the SyncAdapter. |

### requestSync

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun requestSync(request: SyncRequest!): Unit
```

Register a sync with the SyncManager. These requests are built using the [SyncRequest.Builder](https://developer.android.com/reference/kotlin/android/content/SyncRequest.Builder). 

### setIsSyncable

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setIsSyncable(
    account: Account!, 
    authority: String!, 
    syncable: Int
): Unit
```

Set whether this account/provider is syncable.

This method requires the caller to hold the permission [android.Manifest.permission#WRITE_SYNC_SETTINGS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_SYNC_SETTINGS:kotlin.String).

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `syncable` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):\>0 denotes syncable, 0 means not syncable, \<0 means unknown |

### setMasterSyncAutomatically

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setMasterSyncAutomatically(sync: Boolean): Unit
```

Sets the global auto-sync setting that applies to all the providers and accounts. If this is false then the per-provider auto-sync setting is ignored.

This method requires the caller to hold the permission [android.Manifest.permission#WRITE_SYNC_SETTINGS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_SYNC_SETTINGS:kotlin.String).

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sync` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the global auto-sync setting that applies to all the providers and accounts |

### setSyncAutomatically

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setSyncAutomatically(
    account: Account!, 
    authority: String!, 
    sync: Boolean
): Unit
```

Set whether or not the provider is synced when it receives a network tickle.

This method requires the caller to hold the permission [android.Manifest.permission#WRITE_SYNC_SETTINGS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_SYNC_SETTINGS:kotlin.String).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `account` | [Account](https://developer.android.com/reference/kotlin/android/accounts/Account.html#)!:the account whose setting we are querying |
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the provider whose behavior is being controlled |
| `sync` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the provider should be synced when tickles are received for it |

### startSync

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startSync(
    uri: Uri!, 
    extras: Bundle!
): Unit
```

**Deprecated:** *instead use [requestSync(android.accounts.Account,java.lang.String,android.os.Bundle)](https://developer.android.com/reference/kotlin/android/content/ContentResolver#requestSync(android.accounts.Account,%20kotlin.String,%20android.os.Bundle))*

Start an asynchronous sync operation. If you want to monitor the progress of the sync you may register a SyncObserver. Only values of the following types may be used in the extras bundle:

- Integer
- Long
- Boolean
- Float
- Double
- String
- Account
- null

<br />

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:the uri of the provider to sync or null to sync all providers. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:any extras to pass to the SyncAdapter. |

### takePersistableUriPermission

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun takePersistableUriPermission(
    uri: Uri, 
    modeFlags: Int
): Unit
```

Take a persistable URI permission grant that has been offered. Once taken, the permission grant will be remembered across device reboots. Only URI permissions granted with [Intent.FLAG_GRANT_PERSISTABLE_URI_PERMISSION](https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_PERSISTABLE_URI_PERMISSION:kotlin.Int) can be persisted. If the grant has already been persisted, taking it again will touch [UriPermission.getPersistedTime()](https://developer.android.com/reference/kotlin/android/content/UriPermission#getPersistedTime()).

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |
| `modeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or a combination of [android.content.Intent#FLAG_GRANT_READ_URI_PERMISSION](https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int), and [android.content.Intent#FLAG_GRANT_WRITE_URI_PERMISSION](https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int) |

**See Also**

- <https://developer.android.com/reference/kotlin/android/content/ContentResolver#getPersistedUriPermissions()> 

### uncanonicalize

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun uncanonicalize(url: Uri): Uri?
```

Given a canonical Uri previously generated by [canonicalize](https://developer.android.com/reference/kotlin/android/content/ContentResolver#canonicalize(android.net.Uri)), convert it to its local non-canonical form. This can be useful in some cases where you know that you will only be using the Uri in the current environment and want to avoid any possible overhead when using it with the content provider or want to verify that the referenced data exists at all in the new environment.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The canonical [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) that is to be convered back to its non-canonical form. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | Returns the non-canonical representation of url. This will return null if data identified by the canonical Uri can not be found in the current environment; callers must always check for null and deal with that by appropriately falling back to an alternative. |

**See Also**

- [#canonicalize](https://developer.android.com/reference/kotlin/android/content/ContentResolver#canonicalize(android.net.Uri)) 

### unregisterContentObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterContentObserver(observer: ContentObserver): Unit
```

Unregisters a change observer.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `observer` | [ContentObserver](https://developer.android.com/reference/kotlin/android/database/ContentObserver.html#):The previously registered observer that is no longer needed. This value cannot be`null`. |

**See Also**

- [#registerContentObserver](https://developer.android.com/reference/kotlin/android/content/ContentResolver#registerContentObserver(android.net.Uri,%20kotlin.Boolean,%20android.database.ContentObserver)) 

### update

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun update(
    uri: Uri, 
    values: ContentValues?, 
    extras: Bundle?
): Int
```

Update row(s) in a content URI. If the content provider supports transactions the update will be atomic.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URI to modify. This value cannot be`null`. |
| `values` | [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)?:The new field values. The key is the column name for the field. A null value will remove an existing field value. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:A Bundle containing additional information necessary for the operation. Arguments may include SQL style arguments, such as [ContentResolver.QUERY_ARG_SQL_LIMIT](https://developer.android.com/reference/kotlin/android/content/ContentResolver#QUERY_ARG_SQL_LIMIT:kotlin.String), but note that the documentation for each individual provider will indicate which arguments they support. This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of rows updated. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if uri or values are null |
| `java.lang.IllegalArgumentException` | if the provider doesn't support one of the requested Bundle arguments. |

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun update(
    uri: Uri, 
    values: ContentValues?, 
    where: String?, 
    selectionArgs: Array<String!>?
): Int
```

Update row(s) in a content URI. If the content provider supports transactions the update will be atomic.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URI to modify. This value cannot be`null`. |
| `values` | [ContentValues](https://developer.android.com/reference/kotlin/android/content/ContentValues)?:The new field values. The key is the column name for the field. A null value will remove an existing field value. |
| `where` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:A filter to apply to rows before updating, formatted as an SQL WHERE clause (excluding the WHERE itself). This value may be`null`. |
| `selectionArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of rows updated. |

| Exceptions ||
|----------------------------------|---------------------------|
| `java.lang.NullPointerException` | if uri or values are null |

### validateSyncExtrasBundle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun validateSyncExtrasBundle(extras: Bundle!): Unit
```

Check that only values of the following types are in the Bundle:

- Integer
- Long
- Boolean
- Float
- Double
- String
- Account
- null

<br />

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------|
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:the Bundle to check |

### wrap

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun wrap(wrapped: ContentProvider): ContentResolver
```

Create a [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver#) instance that redirects all its methods to the given [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider).

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------|
| `wrapped` | [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider):This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------|-----------------------------|
| [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver#) | This value cannot be`null`. |

### wrap

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun wrap(wrapped: ContentProviderClient): ContentResolver
```

Create a [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver#) instance that redirects all its methods to the given [ContentProviderClient](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient).

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `wrapped` | [ContentProviderClient](https://developer.android.com/reference/kotlin/android/content/ContentProviderClient):This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------|-----------------------------|
| [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver#) | This value cannot be`null`. |
