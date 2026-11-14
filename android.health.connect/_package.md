# android.health.connect

## Interfaces

| [TimeRangeFilter](TimeRangeFilter.md) | A Base class to represent a request for time range for read and delete requests. |
| --- | --- |

## Classes

| [AggregateRecordsGroupedByDurationResponse](AggregateRecordsGroupedByDurationResponse.md) | Class to represent the response from aggregateGroupByDuration |
| --- | --- |
| [AggregateRecordsGroupedByPeriodResponse](AggregateRecordsGroupedByPeriodResponse.md) | Class to represent the response from aggregateGroupByPeriod |
| [AggregateRecordsRequest](AggregateRecordsRequest.md) | A class to create requests for aggregate |
| [AggregateRecordsResponse](AggregateRecordsResponse.md) | A class representing response for aggregate |
| --- | --- |
| [CreateMedicalDataSourceRequest](CreateMedicalDataSourceRequest.md) | A create request for createMedicalDataSource. |
| [DeleteMedicalResourcesRequest](DeleteMedicalResourcesRequest.md) | A delete request for android. |
| [DeviceDataSource](DeviceDataSource.md) | Represents a device that acts as a source of health and fitness data. |
| --- | --- |
| [DeviceDataSourceCapabilities](../android/health/connect/DeviceDataSourceCapabilities.md) | Represents the set of record types a device data source can provide. |
| [DeviceDataTypeSource](../android/health/connect/DeviceDataTypeSource.md) | A data type provided by a device. |
| [GetDeviceDataSourcesResponse](../android/health/connect/GetDeviceDataSourcesResponse.md) | Response containing the list of DeviceDataSource. |
| --- | --- |
| [GetMedicalDataSourcesRequest](GetMedicalDataSourcesRequest.md) | A create request for android. |
| [HealthConnectManager](HealthConnectManager.md) | This class provides APIs to interact with the centralized HealthConnect storage maintained by the system. |
| [HealthPermissions](HealthPermissions.md) | Permissions for accessing the HealthConnect APIs. |
| --- | --- |
| [InsertRecordsResponse](InsertRecordsResponse.md) | Response for insertRecords. |
| [LocalTimeRangeFilter](LocalTimeRangeFilter.md) | Specification of local time range for health connect requests. |
| [MatchmakingRequest](MatchmakingRequest.md) | Represents a request to determine if there are matching data sources for a given set of record types. |
| --- | --- |
| [MatchmakingResponse](../android/health/connect/MatchmakingResponse.md) | A response for isMatchmakingPossible. |
| [MedicalResourceId](MedicalResourceId.md) | A class to represent a unique identifier of a medical resource. |
| [ReadMedicalResourcesInitialRequest](ReadMedicalResourcesInitialRequest.md) | An initial read request with specified filters for android. |
| --- | --- |
| [ReadMedicalResourcesPageRequest](ReadMedicalResourcesPageRequest.md) | A page read request with specified `pageToken` for android. |
| [ReadMedicalResourcesRequest](ReadMedicalResourcesRequest.md) | A base class to represent a read request for android. |
| [ReadMedicalResourcesResponse](ReadMedicalResourcesResponse.md) | A read response for android. |
| --- | --- |
| [ReadRecordsRequest](ReadRecordsRequest.md) | A Base class to represent a request for readRecords |
| [ReadRecordsRequestUsingFilters](ReadRecordsRequestUsingFilters.md) | Class to represent a request based on time range and data origin filters for readRecords |
| [ReadRecordsRequestUsingIds](ReadRecordsRequestUsingIds.md) | A request class to represent request based on RecordIdFilter for readRecords |
| --- | --- |
| [ReadRecordsResponse](ReadRecordsResponse.md) | Response containing list of Records for readRecords. |
| [RecordIdFilter](RecordIdFilter.md) | A class to represent filtering based on record ID or client ID. |
| [TimeInstantRangeFilter](TimeInstantRangeFilter.md) | Specification of time range for read and delete requests. |
| --- | --- |
| [UpsertMedicalResourceRequest](UpsertMedicalResourceRequest.md) | An upsert request for upsertMedicalResources. |

## Exceptions

| [HealthConnectException](HealthConnectException.md) | Class representing health connect exceptions. |
| --- | --- |
