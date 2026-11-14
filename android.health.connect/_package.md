# android.health.connect

## Interfaces

| [TimeRangeFilter](TimeRangeFilter.md) | A Base class to represent a request for time range for read and delete requests. |
| --- | --- |

## Classes

| [AggregateRecordsGroupedByDurationResponse](AggregateRecordsGroupedByDurationResponse.md) | Class to represent the response from `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#aggregateGroupByDuration(android.health.connect.AggregateRecordsRequest,%20java.time.Duration,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` |
| --- | --- |
| [AggregateRecordsGroupedByPeriodResponse](AggregateRecordsGroupedByPeriodResponse.md) | Class to represent the response from `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#aggregateGroupByPeriod(android.health.connect.AggregateRecordsRequest,%20java.time.Period,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` |
| [AggregateRecordsRequest](AggregateRecordsRequest.md) | A class to create requests for `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#aggregate(android.health.connect.AggregateRecordsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` |
| [AggregateRecordsResponse](AggregateRecordsResponse.md) | A class representing response for `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#aggregate(android.health.connect.AggregateRecordsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` |
| --- | --- |
| [CreateMedicalDataSourceRequest](CreateMedicalDataSourceRequest.md) | A create request for `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#createMedicalDataSource(android.health.connect.CreateMedicalDataSourceRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |
| [DeleteMedicalResourcesRequest](DeleteMedicalResourcesRequest.md) | A delete request for android. |
| [DeviceDataSource](DeviceDataSource.md) | Represents a device that acts as a source of health and fitness data. |
| --- | --- |
| [DeviceDataSourceCapabilities](../android/health/connect/DeviceDataSourceCapabilities.md) | Represents the set of record types a device data source can provide. |
| [DeviceDataTypeSource](../android/health/connect/DeviceDataTypeSource.md) | A data type provided by a device. |
| [GetDeviceDataSourcesResponse](../android/health/connect/GetDeviceDataSourcesResponse.md) | Response containing the list of `https://developer.android.com/reference/kotlin/android/health/connect/DeviceDataSource`. |
| --- | --- |
| [GetMedicalDataSourcesRequest](GetMedicalDataSourcesRequest.md) | A create request for android. |
| [HealthConnectManager](HealthConnectManager.md) | This class provides APIs to interact with the centralized HealthConnect storage maintained by the system. |
| [HealthPermissions](HealthPermissions.md) | Permissions for accessing the HealthConnect APIs. |
| --- | --- |
| [InsertRecordsResponse](InsertRecordsResponse.md) | Response for `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#insertRecords(kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |
| [LocalTimeRangeFilter](LocalTimeRangeFilter.md) | Specification of local time range for health connect requests. |
| [MatchmakingRequest](MatchmakingRequest.md) | Represents a request to determine if there are matching data sources for a given set of record types. |
| --- | --- |
| [MatchmakingResponse](../android/health/connect/MatchmakingResponse.md) | A response for `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#isMatchmakingPossible(android.health.connect.MatchmakingRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |
| [MedicalResourceId](MedicalResourceId.md) | A class to represent a unique identifier of a medical resource. |
| [ReadMedicalResourcesInitialRequest](ReadMedicalResourcesInitialRequest.md) | An initial read request with specified filters for android. |
| --- | --- |
| [ReadMedicalResourcesPageRequest](ReadMedicalResourcesPageRequest.md) | A page read request with specified `pageToken` for android. |
| [ReadMedicalResourcesRequest](ReadMedicalResourcesRequest.md) | A base class to represent a read request for android. |
| [ReadMedicalResourcesResponse](ReadMedicalResourcesResponse.md) | A read response for android. |
| --- | --- |
| [ReadRecordsRequest](ReadRecordsRequest.md) | A Base class to represent a request for `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#readRecords(android.health.connect.ReadRecordsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` |
| [ReadRecordsRequestUsingFilters](ReadRecordsRequestUsingFilters.md) | Class to represent a request based on time range and data origin filters for `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#readRecords(android.health.connect.ReadRecordsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` |
| [ReadRecordsRequestUsingIds](ReadRecordsRequestUsingIds.md) | A request class to represent request based on `https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter` for `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#readRecords(android.health.connect.ReadRecordsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` |
| --- | --- |
| [ReadRecordsResponse](ReadRecordsResponse.md) | Response containing list of Records for `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#readRecords(android.health.connect.ReadRecordsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |
| [RecordIdFilter](RecordIdFilter.md) | A class to represent filtering based on record ID or client ID. |
| [TimeInstantRangeFilter](TimeInstantRangeFilter.md) | Specification of time range for read and delete requests. |
| --- | --- |
| [UpsertMedicalResourceRequest](UpsertMedicalResourceRequest.md) | An upsert request for `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#upsertMedicalResources(kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |

## Exceptions

| [HealthConnectException](HealthConnectException.md) | Class representing health connect exceptions. |
| --- | --- |
