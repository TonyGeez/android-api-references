# android.health.connect

## Interfaces

| [TimeRangeFilter](https://developer.android.com/reference/kotlin/android/health/connect/TimeRangeFilter) | A Base class to represent a request for time range for read and delete requests. |
| --- | --- |

## Classes

| [AggregateRecordsGroupedByDurationResponse](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsGroupedByDurationResponse) | Class to represent the response from `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#aggregateGroupByDuration(android.health.connect.AggregateRecordsRequest,%20java.time.Duration,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` |
| --- | --- |
| [AggregateRecordsGroupedByPeriodResponse](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsGroupedByPeriodResponse) | Class to represent the response from `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#aggregateGroupByPeriod(android.health.connect.AggregateRecordsRequest,%20java.time.Period,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` |
| [AggregateRecordsRequest](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsRequest) | A class to create requests for `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#aggregate(android.health.connect.AggregateRecordsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` |
| [AggregateRecordsResponse](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsResponse) | A class representing response for `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#aggregate(android.health.connect.AggregateRecordsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` |
| --- | --- |
| [CreateMedicalDataSourceRequest](https://developer.android.com/reference/kotlin/android/health/connect/CreateMedicalDataSourceRequest) | A create request for `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#createMedicalDataSource(android.health.connect.CreateMedicalDataSourceRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |
| [DeleteMedicalResourcesRequest](https://developer.android.com/reference/kotlin/android/health/connect/DeleteMedicalResourcesRequest) | A delete request for android. |
| [DeviceDataSource](https://developer.android.com/reference/kotlin/android/health/connect/DeviceDataSource) | Represents a device that acts as a source of health and fitness data. |
| --- | --- |
| [DeviceDataSourceCapabilities](https://developer.android.com/reference/kotlin/android/health/connect/DeviceDataSourceCapabilities) | Represents the set of record types a device data source can provide. |
| [DeviceDataTypeSource](https://developer.android.com/reference/kotlin/android/health/connect/DeviceDataTypeSource) | A data type provided by a device. |
| [GetDeviceDataSourcesResponse](https://developer.android.com/reference/kotlin/android/health/connect/GetDeviceDataSourcesResponse) | Response containing the list of `https://developer.android.com/reference/kotlin/android/health/connect/DeviceDataSource`. |
| --- | --- |
| [GetMedicalDataSourcesRequest](https://developer.android.com/reference/kotlin/android/health/connect/GetMedicalDataSourcesRequest) | A create request for android. |
| [HealthConnectManager](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager) | This class provides APIs to interact with the centralized HealthConnect storage maintained by the system. |
| [HealthPermissions](https://developer.android.com/reference/kotlin/android/health/connect/HealthPermissions) | Permissions for accessing the HealthConnect APIs. |
| --- | --- |
| [InsertRecordsResponse](https://developer.android.com/reference/kotlin/android/health/connect/InsertRecordsResponse) | Response for `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#insertRecords(kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |
| [LocalTimeRangeFilter](https://developer.android.com/reference/kotlin/android/health/connect/LocalTimeRangeFilter) | Specification of local time range for health connect requests. |
| [MatchmakingRequest](https://developer.android.com/reference/kotlin/android/health/connect/MatchmakingRequest) | Represents a request to determine if there are matching data sources for a given set of record types. |
| --- | --- |
| [MatchmakingResponse](https://developer.android.com/reference/kotlin/android/health/connect/MatchmakingResponse) | A response for `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#isMatchmakingPossible(android.health.connect.MatchmakingRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |
| [MedicalResourceId](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId) | A class to represent a unique identifier of a medical resource. |
| [ReadMedicalResourcesInitialRequest](https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesInitialRequest) | An initial read request with specified filters for android. |
| --- | --- |
| [ReadMedicalResourcesPageRequest](https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesPageRequest) | A page read request with specified `pageToken` for android. |
| [ReadMedicalResourcesRequest](https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesRequest) | A base class to represent a read request for android. |
| [ReadMedicalResourcesResponse](https://developer.android.com/reference/kotlin/android/health/connect/ReadMedicalResourcesResponse) | A read response for android. |
| --- | --- |
| [ReadRecordsRequest](https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequest) | A Base class to represent a request for `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#readRecords(android.health.connect.ReadRecordsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` |
| [ReadRecordsRequestUsingFilters](https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequestUsingFilters) | Class to represent a request based on time range and data origin filters for `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#readRecords(android.health.connect.ReadRecordsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` |
| [ReadRecordsRequestUsingIds](https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequestUsingIds) | A request class to represent request based on `https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter` for `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#readRecords(android.health.connect.ReadRecordsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` |
| --- | --- |
| [ReadRecordsResponse](https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsResponse) | Response containing list of Records for `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#readRecords(android.health.connect.ReadRecordsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |
| [RecordIdFilter](https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter) | A class to represent filtering based on record ID or client ID. |
| [TimeInstantRangeFilter](https://developer.android.com/reference/kotlin/android/health/connect/TimeInstantRangeFilter) | Specification of time range for read and delete requests. |
| --- | --- |
| [UpsertMedicalResourceRequest](https://developer.android.com/reference/kotlin/android/health/connect/UpsertMedicalResourceRequest) | An upsert request for `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#upsertMedicalResources(kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |

## Exceptions

| [HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException) | Class representing health connect exceptions. |
| --- | --- |
