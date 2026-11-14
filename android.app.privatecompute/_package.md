# android.app.privatecompute

## Classes

| [AssistantQueryRequest](AssistantQueryRequest.md) | Request object specifically for Assistant Query Egress operations. |
| --- | --- |
| [AssistantQueryResponse](AssistantQueryResponse.md) | Specialized response for Assistant Query use-cases. |
| [DataMigrationToPccService](DataMigrationToPccService.md) | Base class for a service that handles data migration to the Private Compute Core (PCC) storage of an application. |
| [EgressReceiverService](EgressReceiverService.md) | Base Service to be implemented by the partner agent proxy process to receive egress queries from a client running inside the Private Compute Core (PCC) sandbox. |
| --- | --- |
| [EgressRequest](EgressRequest.md) | Abstract base request class for PccSandboxManager. |
| [EgressResponse](EgressResponse.md) | Abstract base response class for PccSandboxManager. |
| [MigrationRequestResult](MigrationRequestResult.md) | Result of a migration request initiated by a PCC component. |
| --- | --- |
| [PccClient](../android/app/privatecompute/PccClient.md) | Provides a connection to a PCC service. |
| [PccSandboxManager](PccSandboxManager.md) | Manager for interacting with the Private Compute Core (PCC) sandbox. |
| [PccService](PccService.md) | Abstract base class for a PCC service that receives data from other components. |
| --- | --- |

## Exceptions

| [MigrationException](MigrationException.md) | Exception thrown when a migration request fails. |
| --- | --- |
| [PccEgressException](PccEgressException.md) | Exception thrown when an egress request fails inside the PCC sandbox. |
