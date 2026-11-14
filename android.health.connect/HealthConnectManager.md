Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# HealthConnectManager

```
open class HealthConnectManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.HealthConnectManager](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#) |

This class provides APIs to interact with the centralized HealthConnect storage maintained by the system.

HealthConnect is an offline, on-device storage that unifies data from multiple devices and apps into an ecosystem featuring.

- APIs to insert data of various types into the system.

The basic unit of data in HealthConnect is represented as a `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` object, which is the base class for all the other data types such as `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/StepsRecord`.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#ACTION_MANAGE_HEALTH_PERMISSIONS:kotlin.String` Activity action: Launch UI to manage (e.g. grant/revoke) health permissions. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#ACTION_REQUEST_EXERCISE_ROUTE:kotlin.String` Activity action: Launch UI to share the route associated with an exercise session. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#ACTION_SHOW_ONBOARDING:kotlin.String` Activity action: Launch activity exported by client application that handles onboarding to Health Connect. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#CATEGORY_HEALTH_PERMISSIONS:kotlin.String` Used in conjunction with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_VIEW_PERMISSION_USAGE:kotlin.String` to launch UI to show an app's health permission rationale/data policy. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#EXTRA_EXERCISE_ROUTE:kotlin.String` An exercise route requested via `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#ACTION_REQUEST_EXERCISE_ROUTE:kotlin.String`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#EXTRA_SESSION_ID:kotlin.String` A string ID of a session to be used with `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#ACTION_REQUEST_EXERCISE_ROUTE:kotlin.String`. |
| --- | --- |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#aggregate(android.health.connect.AggregateRecordsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsRequest<T>, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsResponse<T>!, https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException!>)` Get aggregations corresponding to `request`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#aggregateGroupByDuration(android.health.connect.AggregateRecordsRequest,%20java.time.Duration,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsRequest<T>, duration: https://developer.android.com/reference/kotlin/java/time/Duration.html#, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsGroupedByDurationResponse<T>!>!, https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException!>)` Get aggregations corresponding to `request`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#aggregateGroupByPeriod(android.health.connect.AggregateRecordsRequest,%20java.time.Period,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsRequest<T>, period: https://developer.android.com/reference/kotlin/java/time/Period.html#, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsGroupedByPeriodResponse<T>!>!, https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException!>)` Get aggregations corresponding to `request`. |
| --- | --- |
| open [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#createMatchmakingIntent(android.health.connect.MatchmakingRequest)(request: https://developer.android.com/reference/kotlin/android/health/connect/MatchmakingRequest)` Creates an `https://developer.android.com/reference/kotlin/android/content/Intent.html#` to launch a Health Connect flow where users can: - **Discover compatible data sources:** See other installed data sources that have not yet granted permissions to write some of the `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` classes the calling app can read. - **Grant missing permissions:** Easily grant these discovered data sources the necessary write permissions for health data record types that haven't been granted yet. Only `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` types the calling package is permitted to read are being considered. This flow helps users connect new data sources to Health Connect, by matching record types readable by the calling package to appropriate writing data sources. <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#createMedicalDataSource(android.health.connect.CreateMedicalDataSourceRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/health/connect/CreateMedicalDataSourceRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource!, https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException!>)` Creates a `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource` in HealthConnect based on the `https://developer.android.com/reference/kotlin/android/health/connect/CreateMedicalDataSourceRequest` request values. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#deleteMedicalDataSourceWithData(kotlin.String,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!, https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException!>)` Deletes a `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource` and all data linked to it. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#deleteMedicalResources(android.health.connect.DeleteMedicalResourcesRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/health/connect/DeleteMedicalResourcesRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!, https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException!>)` Deletes `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource`s based on given filters in `https://developer.android.com/reference/kotlin/android/health/connect/DeleteMedicalResourcesRequest` |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#deleteMedicalResources(kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(ids: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId!>, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!, https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException!>)` Deletes a list of `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource`s by the provided list of `https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId`s. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#deleteRecords(java.lang.Class,%20android.health.connect.TimeRangeFilter,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(recordType: https://developer.android.com/reference/kotlin/java/lang/Class.html#<out https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record!>, timeRangeFilter: https://developer.android.com/reference/kotlin/android/health/connect/TimeRangeFilter, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!, https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException!>)` Deletes records based on the `https://developer.android.com/reference/kotlin/android/health/connect/TimeRangeFilter`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#deleteRecords(kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(recordIds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter!>, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!, https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException!>)` Deletes records based on `https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#getChangeLogToken(android.health.connect.changelog.ChangeLogTokenRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogTokenRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogTokenResponse!, https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException!>)` Get token for {HealthConnectManager#getChangeLogs}. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#getChangeLogs(android.health.connect.changelog.ChangeLogsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(changeLogsRequest: https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogsRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogsResponse!, https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException!>)` Get change logs post the time when `token` was generated. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#getCurrentDeviceDataSource(java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/health/connect/DeviceDataSource!, https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException!>)` Retrieves the `https://developer.android.com/reference/kotlin/android/health/connect/DeviceDataSource` for the current device. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#getDeviceDataSourceCapabilities(java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/health/connect/DeviceDataSourceCapabilities!, https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException!>)` Returns a set of record type classes that device data sources are capable of providing. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#getDeviceDataSources(java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/health/connect/GetDeviceDataSourcesResponse!, https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException!>)` Retrieves the list of all `https://developer.android.com/reference/kotlin/android/health/connect/DeviceDataSource`s. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#getMedicalDataSources(android.health.connect.GetMedicalDataSourcesRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/health/connect/GetMedicalDataSourcesRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource!>!, https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException!>)` Returns the requested `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource`s. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#getMedicalDataSources(kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(ids: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource!>!, https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException!>)` Returns `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource`s for the provided list of IDs. |
| open static [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<out [Record](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record)!\>!\> | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#getPermissionSensitiveDeviceDataSourceCapabilities()()` Returns the set of data types which are excluded from the output of #getDeviceDataSourceCapabilities unless the caller holds the read permission for those data types. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#insertRecords(kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(records: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record!>, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/health/connect/InsertRecordsResponse!, https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException!>)` Inserts `records` into the HealthConnect database. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#isMatchmakingPossible(android.health.connect.MatchmakingRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/health/connect/MatchmakingRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/health/connect/MatchmakingResponse!, https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException!>)` Checks if launching the intent returned by `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#createMatchmakingIntent(android.health.connect.MatchmakingRequest)` with the same arguments will result in showing at least one matching data source. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#readMedicalResources(android.health.connect.ReadMedicalResourcesRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesRequest, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesResponse!, https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException!>)` Reads `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource`s based on `https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesInitialRequest` or `https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesPageRequest`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#readMedicalResources(kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(ids: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId!>, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource!>!, https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException!>)` Reads `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource`s based on a list of `https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId`s. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#readRecords(android.health.connect.ReadRecordsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequest<T>, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsResponse<T>!, https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException!>)` API to read records based on `https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequestUsingFilters` or `https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequestUsingIds` |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#updateRecords(kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(records: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record!>, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!, https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException!>)` Updates `records` into the HealthConnect database. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#upsertMedicalResources(kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(requests: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/health/connect/UpsertMedicalResourceRequest!>, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource!>!, https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException!>)` Inserts or updates a list of `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource`s into the HealthConnect database using `https://developer.android.com/reference/kotlin/android/health/connect/UpsertMedicalResourceRequest`. |

## Constants

### ACTION_MANAGE_HEALTH_PERMISSIONS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val ACTION_MANAGE_HEALTH_PERMISSIONS: String
```

Activity action: Launch UI to manage (e.g. grant/revoke) health permissions.

Shows a list of apps which request at least one permission of the Health permission group.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_PACKAGE_NAME:kotlin.String` string extra with the name of the app requesting the action. Optional: Adding package name extras launches a UI to manager (e.g. grant/revoke) for this app.

 Value: "android.health.connect.action.MANAGE_HEALTH_PERMISSIONS"

### ACTION_REQUEST_EXERCISE_ROUTE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val ACTION_REQUEST_EXERCISE_ROUTE: String
```

Activity action: Launch UI to share the route associated with an exercise session.

Input: caller must provide \`String\` extra EXTRA_SESSION_ID

Result will be delivered via \[Activity.onActivityResult\] with \`ExerciseRoute\` EXTRA_EXERCISE_ROUTE.

 Value: "android.health.connect.action.REQUEST_EXERCISE_ROUTE"

### ACTION_SHOW_ONBOARDING

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 19](https://developer.android.com/sdkExtensions)

```
static val ACTION_SHOW_ONBOARDING: String
```

Activity action: Launch activity exported by client application that handles onboarding to Health Connect.

Health Connect will invoke this intent whenever the user attempts to connect an app that has exported an activity that responds to this intent. The launched activity is responsible for making permission requests and any other prerequisites for connecting to Health Connect.

Applications exporting an activity that is launched by this intent must also guard it with `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#START_ONBOARDING:kotlin.String` so that only the system can launch it.

 Value: "android.health.connect.action.SHOW_ONBOARDING"

### CATEGORY_HEALTH_PERMISSIONS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val CATEGORY_HEALTH_PERMISSIONS: String
```

Used in conjunction with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_VIEW_PERMISSION_USAGE:kotlin.String` to launch UI to show an app's health permission rationale/data policy.

**Note:** Used by apps to define an intent filter in conjunction with `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_VIEW_PERMISSION_USAGE:kotlin.String` that the HC UI can link out to.

 Value: "android.intent.category.HEALTH_PERMISSIONS"

### EXTRA_EXERCISE_ROUTE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val EXTRA_EXERCISE_ROUTE: String
```

An exercise route requested via `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#ACTION_REQUEST_EXERCISE_ROUTE:kotlin.String`.

This is returned for a successful request to access a route associated with an exercise session.

 Value: "android.health.connect.extra.EXERCISE_ROUTE"

### EXTRA_SESSION_ID

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val EXTRA_SESSION_ID: String
```

A string ID of a session to be used with `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#ACTION_REQUEST_EXERCISE_ROUTE:kotlin.String`.

This is used to specify route of which exercise session we want to request.

 Value: "android.health.connect.extra.SESSION_ID"

## Public methods

### aggregate

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
open fun <T : Any!> aggregate(
    request: AggregateRecordsRequest<T>, 
    executor: Executor, 
    callback: OutcomeReceiver<AggregateRecordsResponse<T>!, HealthConnectException!>
): Unit
```

Get aggregations corresponding to `request`.

| Parameters ||
|---|---|
| `<T>` | Result type of the aggregation. Note: This type is embedded in the `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType` as `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType` are typed in nature. Only `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType`s that are of same type T can be queried together |
| `request` | [AggregateRecordsRequest](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsRequest)\<T\>: request for different aggregation. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| --- | --- |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [AggregateRecordsResponse](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsResponse)\<T\>!, [HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException)!\>: Callback to receive result of performing this operation. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsResponse#get(android.health.connect.datatypes.AggregationType)`

### aggregateGroupByDuration

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
open fun <T : Any!> aggregateGroupByDuration(
    request: AggregateRecordsRequest<T>, 
    duration: Duration, 
    executor: Executor, 
    callback: OutcomeReceiver<MutableList<AggregateRecordsGroupedByDurationResponse<T>!>!, HealthConnectException!>
): Unit
```

Get aggregations corresponding to `request`. Use this API if results are to be grouped by concrete intervals of time, for example 5 Hrs, 10 Hrs etc.

| Parameters ||
|---|---|
| `<T>` | Result type of the aggregation. Note: This type is embedded in the `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType` as `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType` are typed in nature. Only `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType`s that are of same type T can be queried together |
| `request` | [AggregateRecordsRequest](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsRequest)\<T\>: request for different aggregation. This value cannot be `null`. |
| `duration` | [Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#): Duration on which to group by results. This value cannot be `null`. |
| --- | --- |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AggregateRecordsGroupedByDurationResponse](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsGroupedByDurationResponse)\<T\>!\>!, [HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException)!\>: Callback to receive result of performing this operation. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#aggregateGroupByPeriod(android.health.connect.AggregateRecordsRequest,%20java.time.Period,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`

### aggregateGroupByPeriod

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
open fun <T : Any!> aggregateGroupByPeriod(
    request: AggregateRecordsRequest<T>, 
    period: Period, 
    executor: Executor, 
    callback: OutcomeReceiver<MutableList<AggregateRecordsGroupedByPeriodResponse<T>!>!, HealthConnectException!>
): Unit
```

Get aggregations corresponding to `request`. Use this API if results are to be grouped by number of days. This API handles changes in `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` when computing the data on a per-day basis.

| Parameters ||
|---|---|
| `<T>` | Result type of the aggregation. Note: This type is embedded in the `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType` as `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType` are typed in nature. Only `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType`s that are of same type T can be queried together |
| `request` | [AggregateRecordsRequest](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsRequest)\<T\>: Request for different aggregation. This value cannot be `null`. |
| `period` | [Period](https://developer.android.com/reference/kotlin/java/time/Period.html#): Period on which to group by results. This value cannot be `null`. |
| --- | --- |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AggregateRecordsGroupedByPeriodResponse](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsGroupedByPeriodResponse)\<T\>!\>!, [HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException)!\>: Callback to receive result of performing this operation. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsGroupedByPeriodResponse#get(android.health.connect.datatypes.AggregationType)`
- `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#aggregateGroupByDuration(android.health.connect.AggregateRecordsRequest,%20java.time.Duration,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`

### createMatchmakingIntent

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
open fun createMatchmakingIntent(request: MatchmakingRequest): Intent
```

Creates an `https://developer.android.com/reference/kotlin/android/content/Intent.html#` to launch a Health Connect flow where users can:

- **Discover compatible data sources:** See other installed data sources that have not yet granted permissions to write some of the `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` classes the calling app can read.
- **Grant missing permissions:** Easily grant these discovered data sources the necessary write permissions for health data record types that haven't been granted yet. Only `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` types the calling package is permitted to read are being considered.

This flow helps users connect new data sources to Health Connect, by matching record types readable by the calling package to appropriate writing data sources.

<br />

**How to launch this Intent** This intent must be launched using the androidx.activity.result.ActivityResultLauncher with an appropriate contract (e.g., androidx.activity.result.contract.ActivityResultContracts.StartActivityForResult), or the `https://developer.android.com/reference/kotlin/android/app/Activity.html#startActivityForResult(android.content.Intent,%20kotlin.Int)` API. It is not designed to be used with a android.app.Activity#startActivity(android.content.Intent) call. The launched activity may return a result code (e.g., `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int`) indicating the user's interaction with the flow:

- `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int`: The user has successfully granted permissions to at least one application.
- `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int`: The user has canceled the flow, either by closing the activity or by not granting any permissions. `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int` can also occur if the intent was launched in a discouraged way when no matching apps are available. This can be avoided by ensuring `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#isMatchmakingPossible(android.health.connect.MatchmakingRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` returns `true` before launching the intent.

The launched flow will only show packages that have declared, but not yet been granted write permissions (that have not been denied by the user twice) for at least one of the relevant `recordTypes`, and for the relevant included/excluded data sources:

- **If `recordTypes` is not empty:** The launched screen will focus on data sources capable of writing data for at least one of the specified health `recordTypes`. The user can then grant write permissions to these discovered data sources specifically for these types. Record types the calling app does not have permission to read are considered ignored.
- **If `recordTypes` is empty:** The system first determines all health data record types for which the calling package has already been granted read permission. The launched flow will then display data sources capable of writing any of these record types, where the user can grant write permissions for these types.
- **If `includedDataSources` is not empty:** Only data sources whose package names are present in this set are considered for matchmaking. If a data source is an app, the calling app must have visibility of the package name (e.g. declared in the manifest inside `<queries>`). If a data source is a device, the calling app does not need to declare it in the manifest, but should identify available devices via `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#getDeviceDataSources(java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`.
- **If `excludedDataSources` is not empty:** Data sources whose package names are present in this set are excluded from matchmaking. As with inclusion, app data sources must be visible to the calling app, while device data sources do not require manifest declaration.
- **If both are empty:** All compatible data sources are considered.

Note: `includedDataSources` and `excludedDataSources` cannot both be non-empty at the same time.

| Parameters ||
|---|---|
| `request` | [MatchmakingRequest](https://developer.android.com/reference/kotlin/android/health/connect/MatchmakingRequest): A `https://developer.android.com/reference/kotlin/android/health/connect/MatchmakingRequest` that contains: - A non-null set of `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` classes. If non-empty, the flow focuses on these specific types. If empty, the flow focuses on types for which the calling package has permission to read. - A non-null set of `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/DataOrigin` to include in matchmaking. If non-empty, only specified data origins are considered. App data origins must be visible to the calling app (declared in `<queries>`). Device data origins (from `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#getDeviceDataSources(java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`) do not require manifest declaration. - A non-null set of `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/DataOrigin` to exclude from matchmaking. If non-empty, specified data origins are EXCLUDED. App data origins must be visible to the calling app. Device data origins do not require manifest declaration. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Intent.html#` | An `https://developer.android.com/reference/kotlin/android/content/Intent.html#` configured to show the flow for discovering and managing write permissions for matching data origins. This intent must be launched using `https://developer.android.com/reference/kotlin/android/app/Activity.html#startActivityForResult(android.content.Intent,%20kotlin.Int)`. This value cannot be `null`. |

**See Also**

### createMedicalDataSource

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
open fun createMedicalDataSource(
    request: CreateMedicalDataSourceRequest, 
    executor: Executor, 
    callback: OutcomeReceiver<MedicalDataSource!, HealthConnectException!>
): Unit
```

Creates a `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource` in HealthConnect based on the `https://developer.android.com/reference/kotlin/android/health/connect/CreateMedicalDataSourceRequest` request values.

Medical data is represented using the [Fast Healthcare Interoperability Resources (FHIR)](https://hl7.org/fhir/) standard.

A `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource` needs to be created before any `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource`s for that source can be inserted. Separate `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource`s should be created for medical records coming from different sources (e.g. different FHIR endpoints, different healthcare systems), unless the data has been reconciled and all records have a unique combination of resource type and resource id.

The `https://developer.android.com/reference/kotlin/android/health/connect/CreateMedicalDataSourceRequest.Builder#setDisplayName(kotlin.String)` must be unique per app, and `https://developer.android.com/reference/kotlin/android/health/connect/CreateMedicalDataSourceRequest.Builder#setFhirVersion(android.health.connect.datatypes.FhirVersion)` FHIR version} must be a version supported by Health Connect, as documented on the `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirVersion`. See `https://developer.android.com/reference/kotlin/android/health/connect/CreateMedicalDataSourceRequest.Builder#setFhirBaseUri(android.net.Uri)` for more details on the FHIR base URI. 
Requires `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_MEDICAL_DATA:kotlin.String`

| Parameters ||
|---|---|
| `request` | [CreateMedicalDataSourceRequest](https://developer.android.com/reference/kotlin/android/health/connect/CreateMedicalDataSourceRequest): Creation request. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [MedicalDataSource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource)!, [HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException)!\>: Callback to receive result of performing this operation. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `request` contains a FHIR base URI or display name exceeding the character limits, or an unsupported FHIR version. |

### deleteMedicalDataSourceWithData

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
open fun deleteMedicalDataSourceWithData(
    id: String, 
    executor: Executor, 
    callback: OutcomeReceiver<Void!, HealthConnectException!>
): Unit
```

Deletes a `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource` and all data linked to it.

If the provided data source `id` is either invalid, or does not exist, or owned by another apps, the caller will receive an exception with code `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException#ERROR_INVALID_ARGUMENT:kotlin.Int` via `callback.onError()`.

Regarding permissions:

- Only apps with the system permission can delete data written by apps other than themselves.
- Deletes are permitted in the foreground or background.

. 
Requires `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_MEDICAL_DATA:kotlin.String` or android.health.connect.HealthPermissions.MANAGE_HEALTH_DATA_PERMISSION

| Parameters ||
|---|---|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The id of the data source to delete. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!, [HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException)!\>: Callback to receive result of performing this operation. This value cannot be `null`. |
| --- | --- |

### deleteMedicalResources

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
open fun deleteMedicalResources(
    request: DeleteMedicalResourcesRequest, 
    executor: Executor, 
    callback: OutcomeReceiver<Void!, HealthConnectException!>
): Unit
```

Deletes `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource`s based on given filters in `https://developer.android.com/reference/kotlin/android/health/connect/DeleteMedicalResourcesRequest`

Regarding permissions:

- Only apps with the system permission can delete data written by apps other than themselves.
- Deletes are permitted in the foreground or background.

. 
Requires `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_MEDICAL_DATA:kotlin.String` or android.health.connect.HealthPermissions.MANAGE_HEALTH_DATA_PERMISSION

| Parameters ||
|---|---|
| `request` | [DeleteMedicalResourcesRequest](https://developer.android.com/reference/kotlin/android/health/connect/DeleteMedicalResourcesRequest): The delete request. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!, [HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException)!\>: Callback to receive result of performing this operation. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `request` contains unsupported medical resource types or invalid `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource` IDs. |

### deleteMedicalResources

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
open fun deleteMedicalResources(
    ids: MutableList<MedicalResourceId!>, 
    executor: Executor, 
    callback: OutcomeReceiver<Void!, HealthConnectException!>
): Unit
```

Deletes a list of `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource`s by the provided list of `https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId`s.

- If any ID in `ids` is invalid, the API will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`, and nothing will be deleted.
- If any ID in `ids` does not exist, that ID will be ignored, while deletion on other IDs will be performed.

<br />

Regarding permissions:

- Only apps with the system permission can delete data written by apps other than themselves.
- Deletes are permitted in the foreground or background.

. 
Requires `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_MEDICAL_DATA:kotlin.String` or android.health.connect.HealthPermissions.MANAGE_HEALTH_DATA_PERMISSION

| Parameters ||
|---|---|
| `ids` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MedicalResourceId](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId)!\>: The ids to delete. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!, [HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException)!\>: Callback to receive result of performing this operation. This value cannot be `null`. |
| --- | --- |

### deleteRecords

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
open fun deleteRecords(
    recordType: Class<out Record!>, 
    timeRangeFilter: TimeRangeFilter, 
    executor: Executor, 
    callback: OutcomeReceiver<Void!, HealthConnectException!>
): Unit
```

Deletes records based on the `https://developer.android.com/reference/kotlin/android/health/connect/TimeRangeFilter`.

Deletions are performed in a transaction i.e. either all will be deleted or none

| Parameters ||
|---|---|
| `recordType` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<out [Record](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record)!\>: recordType to perform delete operation on. This value cannot be `null`. |
| `timeRangeFilter` | [TimeRangeFilter](https://developer.android.com/reference/kotlin/android/health/connect/TimeRangeFilter): time filter based on which to delete the records. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. |
| --- | --- |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!, [HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException)!\>: Callback to receive result of performing this operation. This value cannot be `null`. |

### deleteRecords

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
open fun deleteRecords(
    recordIds: MutableList<RecordIdFilter!>, 
    executor: Executor, 
    callback: OutcomeReceiver<Void!, HealthConnectException!>
): Unit
```

Deletes records based on `https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter`.

Deletions are performed in a transaction i.e. either all will be deleted or none

| Parameters ||
|---|---|
| `recordIds` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RecordIdFilter](https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter)!\>: recordIds on which to perform delete operation. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!, [HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException)!\>: Callback to receive result of performing this operation. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `recordIds is empty` |

### getChangeLogToken

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
open fun getChangeLogToken(
    request: ChangeLogTokenRequest, 
    executor: Executor, 
    callback: OutcomeReceiver<ChangeLogTokenResponse!, HealthConnectException!>
): Unit
```

Get token for {HealthConnectManager#getChangeLogs}. Changelogs requested corresponding to this token will be post the time this token was generated by the system all items that match the given filters.

If the app doesn't have the necessary permissions to read data of any type requested here, the request will throw an exception.

Tokens from this request are to be passed to {HealthConnectManager#getChangeLogs}

| Parameters ||
|---|---|
| `request` | [ChangeLogTokenRequest](https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogTokenRequest): A request to get changelog token. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [ChangeLogTokenResponse](https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogTokenResponse)!, [HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException)!\>: Callback to receive result of performing this operation. This value cannot be `null`. |
| --- | --- |

### getChangeLogs

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
open fun getChangeLogs(
    changeLogsRequest: ChangeLogsRequest, 
    executor: Executor, 
    callback: OutcomeReceiver<ChangeLogsResponse!, HealthConnectException!>
): Unit
```

Get change logs post the time when `token` was generated.

| Parameters ||
|---|---|
| `changeLogsRequest` | [ChangeLogsRequest](https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogsRequest): The token from `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#getChangeLogToken(android.health.connect.changelog.ChangeLogTokenRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [ChangeLogsResponse](https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogsResponse)!, [HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException)!\>: Callback to receive result of performing this operation. This value cannot be `null`. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#getChangeLogToken(android.health.connect.changelog.ChangeLogTokenRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`

### getCurrentDeviceDataSource

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 22](https://developer.android.com/sdkExtensions)

```
open fun getCurrentDeviceDataSource(
    executor: Executor, 
    callback: OutcomeReceiver<DeviceDataSource!, HealthConnectException!>
): Unit
```

Retrieves the `https://developer.android.com/reference/kotlin/android/health/connect/DeviceDataSource` for the current device.

The caller must hold at least one Health Connect read permission in order to call this method.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [DeviceDataSource](https://developer.android.com/reference/kotlin/android/health/connect/DeviceDataSource)!, [HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException)!\>: Callback to receive result of performing this operation. This value cannot be `null`. |

### getDeviceDataSourceCapabilities

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 22](https://developer.android.com/sdkExtensions)

```
open fun getDeviceDataSourceCapabilities(
    executor: Executor, 
    callback: OutcomeReceiver<DeviceDataSourceCapabilities!, HealthConnectException!>
): Unit
```

Returns a set of record type classes that device data sources are capable of providing.

Use this method to avoid making unnecessary permission requests when reading device data in case the data type is not provided by any device data sources.

This will filter out any permission sensitive data types the caller does not hold read permissions for. Data types belonging to `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#getPermissionSensitiveDeviceDataSourceCapabilities()` are excluded from the response unless the caller holds read permissions for those data types.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [DeviceDataSourceCapabilities](https://developer.android.com/reference/kotlin/android/health/connect/DeviceDataSourceCapabilities)!, [HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException)!\>: Callback to receive result of performing this operation. This value cannot be `null`. |

### getDeviceDataSources

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 22](https://developer.android.com/sdkExtensions)

```
open fun getDeviceDataSources(
    executor: Executor, 
    callback: OutcomeReceiver<GetDeviceDataSourcesResponse!, HealthConnectException!>
): Unit
```

Retrieves the list of all `https://developer.android.com/reference/kotlin/android/health/connect/DeviceDataSource`s.

The returned list includes all devices that have been advertised by device data providers, filtered based on the caller's permissions. A device is included if the caller holds the READ permission for at least one of the data types supported by the device. Other data types supported by the device that the caller does not have permission for will nonetheless be included.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [GetDeviceDataSourcesResponse](https://developer.android.com/reference/kotlin/android/health/connect/GetDeviceDataSourcesResponse)!, [HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException)!\>: Callback to receive result of performing this operation. This value cannot be `null`. |

### getMedicalDataSources

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
open fun getMedicalDataSources(
    request: GetMedicalDataSourcesRequest, 
    executor: Executor, 
    callback: OutcomeReceiver<MutableList<MedicalDataSource!>!, HealthConnectException!>
): Unit
```

Returns the requested `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource`s.

Number of data sources returned by this API will depend based on below factors:

- If an empty `https://developer.android.com/reference/kotlin/android/health/connect/GetMedicalDataSourcesRequest#getPackageNames()` is passed, all permitted data sources from all apps will be returned. See below.
- If any package name in the `https://developer.android.com/reference/kotlin/android/health/connect/GetMedicalDataSourcesRequest#getPackageNames()` is invalid, the API will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.
- If a non-empty `https://developer.android.com/reference/kotlin/android/health/connect/GetMedicalDataSourcesRequest#getPackageNames()` is specified in the request, then only the permitted data sources created by those packages will be returned. See below.

There is no specific read permission for getting data sources. Instead permission to read data sources is based on whether the caller has permission to read the data currently linked to that data source. Being permitted to get data sources is dependent on the following logic, in priority order, earlier statements take precedence.

1. A caller with the system permission can get any data source in the foreground or background.
2. A caller without any read or write permissions for health data will not be able to get any medical data sources and receive an exception with code `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException#ERROR_SECURITY:kotlin.Int` via `callback.onError()`, even for data sources the caller has created.
3. Callers can get data sources they have created, whether this method is called in the foreground or background. Note this only applies if the caller has at least one read or write permission for health data.
4. For any given data source, a caller can get that data source in the foreground if the caller has permission to read any of the data linked to that data source. For clarity, the does not allow it to get an empty data source.
5. For any given data source, a caller can get that data source in the background if it has both permission to read any of the data linked to that data source, and `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_HEALTH_DATA_IN_BACKGROUND:kotlin.String`.
6. In all other cases the caller is not permitted to get the given data source and it will not be returned.

| Parameters ||
|---|---|
| `request` | [GetMedicalDataSourcesRequest](https://developer.android.com/reference/kotlin/android/health/connect/GetMedicalDataSourcesRequest): the request for which data sources to return. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MedicalDataSource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource)!\>!, [HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException)!\>: Callback to receive result of performing this operation. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `request` contains invalid package names. |

### getMedicalDataSources

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
open fun getMedicalDataSources(
    ids: MutableList<String!>, 
    executor: Executor, 
    callback: OutcomeReceiver<MutableList<MedicalDataSource!>!, HealthConnectException!>
): Unit
```

Returns `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource`s for the provided list of IDs.

The number and order of medical data sources returned by this API is not guaranteed. The number will depend on the factors below:

- If an empty list of `ids` is provided, an empty list will be returned.
- If any ID in `ids` is invalid, the caller will receive an exception with code `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException#ERROR_INVALID_ARGUMENT:kotlin.Int` via `callback.onError()`.
- If any ID in `ids` does not exist, no data source will be returned for that ID.
- Callers will only get data sources they are permitted to get. See below.

There is no specific read permission for getting data sources. Instead, permission to read data sources is based on whether the caller has permission to read the data currently linked to that data source. Being permitted to get data sources is dependent on the following logic, in priority order, earlier statements take precedence.

1. A caller with the system permission can get any data source in the foreground or background.
2. A caller without any read or write permissions for health data will not be able to get any medical data sources and receive an exception with code `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException#ERROR_SECURITY:kotlin.Int` via `callback.onError()`, even for data sources the caller has created.
3. Callers can get data sources they have created, whether this method is called in the foreground or background. Note this only applies if the caller has at least one read or write permission for health data.
4. For any given data source, a caller can get that data source in the foreground if the caller has permission to read any of the data linked to that data source. For clarity, the does not allow it to get an empty data source.
5. For any given data source, a caller can get that data source in the background if it has both permission to read any of the data linked to that data source, and `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_HEALTH_DATA_IN_BACKGROUND:kotlin.String`.
6. In all other cases the caller is not permitted to get the given data source and it will not be returned.

| Parameters ||
|---|---|
| `ids` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: Identifiers for data sources to get. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MedicalDataSource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource)!\>!, [HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException)!\>: Callback to receive result of performing this operation. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the size of `ids` is more than 5000. |

### getPermissionSensitiveDeviceDataSourceCapabilities

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 22](https://developer.android.com/sdkExtensions)

```
open static fun getPermissionSensitiveDeviceDataSourceCapabilities(): MutableSet<Class<out Record!>!>
```

Returns the set of data types which are excluded from the output of #getDeviceDataSourceCapabilities unless the caller holds the read permission for those data types.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/java/lang/Class.html#<out https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record!>!>` | This value cannot be `null`. |

### insertRecords

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
open fun insertRecords(
    records: MutableList<Record!>, 
    executor: Executor, 
    callback: OutcomeReceiver<InsertRecordsResponse!, HealthConnectException!>
): Unit
```

Inserts `records` into the HealthConnect database. The records returned in `https://developer.android.com/reference/kotlin/android/health/connect/InsertRecordsResponse` contains the unique IDs of the input records. The values are in same order as `records`. In case of an error or a permission failure the HealthConnect service, `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#onError(android.os.OutcomeReceiver.E)` will be invoked with a `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException`.

| Parameters ||
|---|---|
| `records` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Record](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record)!\>: list of records to be inserted. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [InsertRecordsResponse](https://developer.android.com/reference/kotlin/android/health/connect/InsertRecordsResponse)!, [HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException)!\>: Callback to receive result of performing this operation. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.RuntimeException` | for internal errors |

### isMatchmakingPossible

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
open fun isMatchmakingPossible(
    request: MatchmakingRequest, 
    executor: Executor, 
    callback: OutcomeReceiver<MatchmakingResponse!, HealthConnectException!>
): Unit
```

Checks if launching the intent returned by `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#createMatchmakingIntent(android.health.connect.MatchmakingRequest)` with the same arguments will result in showing at least one matching data source.

- Returns `true` if the flow launched by the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` from `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#createMatchmakingIntent(android.health.connect.MatchmakingRequest)` would display at least one matching data source, allowing the user to take action.
- Returns `false` if the launched flow would immediately return `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int` because there are no relevant data sources to show.

<br />

| Parameters ||
|---|---|
| `request` | [MatchmakingRequest](https://developer.android.com/reference/kotlin/android/health/connect/MatchmakingRequest): A non-null `https://developer.android.com/reference/kotlin/android/health/connect/MatchmakingRequest` that contains a set of `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` classes. See description at `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#createMatchmakingIntent(android.health.connect.MatchmakingRequest)`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): A non-null `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` on which the `callback` will be invoked. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [MatchmakingResponse](https://developer.android.com/reference/kotlin/android/health/connect/MatchmakingResponse)!, [HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException)!\>: A non-null `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#` to receive the result. The `onResult` method will be called with a boolean indicating if there are matching writing data sources to show. The `onError` method will be called if an error occurs. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#createMatchmakingIntent(android.health.connect.MatchmakingRequest)`

### readMedicalResources

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
open fun readMedicalResources(
    request: ReadMedicalResourcesRequest, 
    executor: Executor, 
    callback: OutcomeReceiver<ReadMedicalResourcesResponse!, HealthConnectException!>
): Unit
```

Reads `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource`s based on `https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesInitialRequest` or `https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesPageRequest`.

Being permitted to read medical resources is dependent on the following logic, in priority order, earlier statements take precedence.

1. A caller with the system permission can get any medical resources in the foreground or background.
2. A caller without any read or write permissions for health data will not be able to get any medical resources and receive an exception with code `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException#ERROR_SECURITY:kotlin.Int` via `callback.onError()`, even for medical resources the caller has created.
3. Callers can get medical resources they have created, whether this method is called in the foreground or background. Note this only applies if the caller has at least one read or write permission for health data.
4. For any given medical resource, a caller can get that medical resource in the foreground if the caller has the corresponding read permission, or in the background if it also has `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_HEALTH_DATA_IN_BACKGROUND:kotlin.String`.
5. In all other cases the caller is not permitted to get the given medical resource and it will not be returned.

| Parameters ||
|---|---|
| `request` | [ReadMedicalResourcesRequest](https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesRequest): The read request `https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesInitialRequest` or `https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesPageRequest`. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [ReadMedicalResourcesResponse](https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesResponse)!, [HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException)!\>: Callback to receive result of performing this operation. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `request` has set page size to be less than 1 or more than 5000; or if contains unsupported medical resource type or invalid `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource` IDs when using `https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesInitialRequest`. |

### readMedicalResources

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
open fun readMedicalResources(
    ids: MutableList<MedicalResourceId!>, 
    executor: Executor, 
    callback: OutcomeReceiver<MutableList<MedicalResource!>!, HealthConnectException!>
): Unit
```

Reads `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource`s based on a list of `https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId`s.

The number and order of medical resources returned by this API is not guaranteed. The number will depend on the factors below:

- If an empty list of `ids` is provided, an empty list will be returned.
- If the size of `ids` is more than 5000, the API will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.
- If any ID in `ids` is invalid, the API will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`.
- If any ID in `ids` does not exist, no medical resource will be returned for that ID.
- Callers will only get medical resources they are permitted to get. See below.

Being permitted to read medical resources is dependent on the following logic, in priority order, earlier statements take precedence.

1. A caller with the system permission can get any medical resources in the foreground or background.
2. A caller without any read or write permissions for health data will not be able to get any medical resources and receive an exception with code `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException#ERROR_SECURITY:kotlin.Int` via `callback.onError()`, even for medical resources the caller has created.
3. Callers can get medical resources they have created, whether this method is called in the foreground or background. Note this only applies if the caller has at least one read or write permission for health data.
4. For any given medical resource, a caller can get that medical resource in the foreground if the caller has the corresponding read permission, or in the background if it also has `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#READ_HEALTH_DATA_IN_BACKGROUND:kotlin.String`.
5. In all other cases the caller is not permitted to get the given medical resource and it will not be returned.

Each returned `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource` has passed the Health Connect FHIR validation checks at write time, but is not guaranteed to meet all requirements of the [Fast Healthcare Interoperability Resources (FHIR) spec](https://hl7.org/fhir/resourcelist.html). If required, clients should perform their own checks on the data.

| Parameters ||
|---|---|
| `ids` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MedicalResourceId](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId)!\>: Identifiers on which to perform read operation. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MedicalResource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource)!\>!, [HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException)!\>: Callback to receive result of performing this operation. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the size of `ids` is more than 5000 or if any id is invalid. |

### readRecords

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
open fun <T : Record!> readRecords(
    request: ReadRecordsRequest<T>, 
    executor: Executor, 
    callback: OutcomeReceiver<ReadRecordsResponse<T>!, HealthConnectException!>
): Unit
```

API to read records based on `https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequestUsingFilters` or `https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequestUsingIds`

Number of records returned by this API will depend based on below factors:

When an app with read permission allowed calls the API from background then it will be able to read only its own inserted records and will not get records inserted by other apps. This may be less than the total records present for the record type.

When an app with read permission allowed calls the API from foreground then it will be able to read all records for the record type.

App with only write permission but no read permission allowed will be able to read only its own inserted records both when in foreground or background.

An app without both read and write permissions will not be able to read any record and the API will throw Security Exception.

| Parameters ||
|---|---|
| `request` | [ReadRecordsRequest](https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequest)\<T\>: Read request based on `https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequestUsingFilters` or `https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequestUsingIds` This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [ReadRecordsResponse](https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsResponse)\<T\>!, [HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException)!\>: Callback to receive result of performing this operation. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if request page size set is more than 5000 in `https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequestUsingFilters` |
| `java.lang.SecurityException` | if app without read or write permission tries to read. |

### updateRecords

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
open fun updateRecords(
    records: MutableList<Record!>, 
    executor: Executor, 
    callback: OutcomeReceiver<Void!, HealthConnectException!>
): Unit
```

Updates `records` into the HealthConnect database. In case of an error or a permission failure the HealthConnect service, `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#onError(android.os.OutcomeReceiver.E)` will be invoked with a `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException`.

In case the input record to be updated does not exist in the database or the caller is not the owner of the record then `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException#ERROR_INVALID_ARGUMENT:kotlin.Int` will be thrown.

| Parameters ||
|---|---|
| `records` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Record](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record)!\>: list of records to be updated. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!, [HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException)!\>: Callback to receive result of performing this operation. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if at least one of the records is missing both ClientRecordID and UUID. |

### upsertMedicalResources

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
open fun upsertMedicalResources(
    requests: MutableList<UpsertMedicalResourceRequest!>, 
    executor: Executor, 
    callback: OutcomeReceiver<MutableList<MedicalResource!>!, HealthConnectException!>
): Unit
```

Inserts or updates a list of `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource`s into the HealthConnect database using `https://developer.android.com/reference/kotlin/android/health/connect/UpsertMedicalResourceRequest`.

For each `https://developer.android.com/reference/kotlin/android/health/connect/UpsertMedicalResourceRequest`, one `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource` will be returned. The returned list of `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource`s will be in the same order as the `requests`.

Note that a `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource` needs to be created using `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#createMedicalDataSource(android.health.connect.CreateMedicalDataSourceRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` before any `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource`s can be upserted for this source.

Medical data is represented using the [Fast Healthcare Interoperability Resources (FHIR)](https://hl7.org/fhir/) standard. The FHIR resource provided in `https://developer.android.com/reference/kotlin/android/health/connect/UpsertMedicalResourceRequest#getData()` is expected to be valid FHIR in JSON representation for the specified `https://developer.android.com/reference/kotlin/android/health/connect/UpsertMedicalResourceRequest#getFhirVersion()` according to the [FHIR spec](https://hl7.org/fhir/resourcelist.html). Structural validation checks such as resource structure, field types and presence of required fields are performed, but these checks may not cover all FHIR spec requirements and may change in future versions.

Data written to Health Connect should be for a single individual only. However, the API allows for multiple Patient resources to be written to account for the possibility of multiple Patient resources being present in one individual's medical record.

Each `https://developer.android.com/reference/kotlin/android/health/connect/UpsertMedicalResourceRequest` also has to meet the following requirements.

- The FHIR resource contains an "id" and "resourceType" field.
- The FHIR resource type is in our accepted list of resource types. See `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirResource` for the accepted types.
- The FHIR resource does not contain any "contained" resources.
- The resource can be mapped to one of the READ_MEDICAL_DATA_ `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions` categories.
- The `https://developer.android.com/reference/kotlin/android/health/connect/UpsertMedicalResourceRequest#getDataSourceId()` is valid.
- The `https://developer.android.com/reference/kotlin/android/health/connect/UpsertMedicalResourceRequest#getFhirVersion()` matches the `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FhirVersion` of the `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource`.

If any request contains invalid `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource` IDs, the API will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`, and none of the `requests` will be upserted into the HealthConnect database.

If any request is deemed invalid for any other reasons, the caller will receive an exception with code `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException#ERROR_INVALID_ARGUMENT:kotlin.Int` via `callback.onError()`, and none of the `requests` will be upserted into the HealthConnect database.

If data for any `https://developer.android.com/reference/kotlin/android/health/connect/UpsertMedicalResourceRequest` fails to be upserted, then no data from any `requests` will be upserted into the database.

The uniqueness of each request is calculated comparing the combination of `https://developer.android.com/reference/kotlin/android/health/connect/UpsertMedicalResourceRequest#getDataSourceId()`, FHIR resource type and FHIR resource ID extracted from the provided `https://developer.android.com/reference/kotlin/android/health/connect/UpsertMedicalResourceRequest#getData()`. If the above combination does not match with an existing one in Health Connect, then a new `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource` is inserted, otherwise the existing one is updated. 
Requires `https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions#WRITE_MEDICAL_DATA:kotlin.String`

| Parameters ||
|---|---|
| `requests` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [UpsertMedicalResourceRequest](https://developer.android.com/reference/kotlin/android/health/connect/UpsertMedicalResourceRequest)!\>: List of upsert requests. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): Executor on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MedicalResource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource)!\>!, [HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException)!\>: Callback to receive result of performing this operation. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if any `requests` contains invalid `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalDataSource` IDs. |
