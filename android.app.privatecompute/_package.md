# android.app.privatecompute

## Classes

| [AssistantQueryRequest](../android/app/privatecompute/AssistantQueryRequest.md) | Request object specifically for Assistant Query Egress operations. |
| --- | --- |
| [AssistantQueryResponse](../android/app/privatecompute/AssistantQueryResponse.md) | Specialized response for Assistant Query use-cases. |
| [DataMigrationToPccService](../android/app/privatecompute/DataMigrationToPccService.md) | Base class for a service that handles data migration to the Private Compute Core (PCC) storage of an application. |
| [EgressReceiverService](../android/app/privatecompute/EgressReceiverService.md) | Base Service to be implemented by the partner agent proxy process to receive egress queries from a client running inside the Private Compute Core (PCC) sandbox. |
| --- | --- |
| [EgressRequest](../android/app/privatecompute/EgressRequest.md) | Abstract base request class for PccSandboxManager. |
| [EgressResponse](../android/app/privatecompute/EgressResponse.md) | Abstract base response class for PccSandboxManager. |
| [MigrationRequestResult](../android/app/privatecompute/MigrationRequestResult.md) | Result of a migration request initiated by a PCC component. |
| --- | --- |
| [PccClient](../android/app/privatecompute/PccClient.md) | Provides a connection to a PCC service. |
| [PccSandboxManager](../android/app/privatecompute/PccSandboxManager.md) | Manager for interacting with the Private Compute Core (PCC) sandbox. |
| [PccService](../android/app/privatecompute/PccService.md) | Abstract base class for a PCC service that receives data from other components. |
| --- | --- |

## Exceptions

| [MigrationException](../android/app/privatecompute/MigrationException.md) | Exception thrown when a migration request fails. |
| --- | --- |
| [PccEgressException](../android/app/privatecompute/PccEgressException.md) | Exception thrown when an egress request fails inside the PCC sandbox. |
