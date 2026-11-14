# android.app.privatecompute

## Classes

| [AssistantQueryRequest](https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryRequest) | Request object specifically for Assistant Query Egress operations. |
| [AssistantQueryResponse](https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryResponse) | Specialized response for Assistant Query use-cases. |
| [DataMigrationToPccService](https://developer.android.com/reference/kotlin/android/app/privatecompute/DataMigrationToPccService) | Base class for a service that handles data migration to the Private Compute Core (PCC) storage of an application. |
| [EgressReceiverService](https://developer.android.com/reference/kotlin/android/app/privatecompute/EgressReceiverService) | Base Service to be implemented by the partner agent proxy process to receive egress queries from a client running inside the Private Compute Core (PCC) sandbox. |
| [EgressRequest](https://developer.android.com/reference/kotlin/android/app/privatecompute/EgressRequest) | Abstract base request class for PccSandboxManager. |
| [EgressResponse](https://developer.android.com/reference/kotlin/android/app/privatecompute/EgressResponse) | Abstract base response class for PccSandboxManager. |
| [MigrationRequestResult](https://developer.android.com/reference/kotlin/android/app/privatecompute/MigrationRequestResult) | Result of a migration request initiated by a PCC component. |
| [PccClient](https://developer.android.com/reference/kotlin/android/app/privatecompute/PccClient) | Provides a connection to a PCC service. |
| [PccSandboxManager](https://developer.android.com/reference/kotlin/android/app/privatecompute/PccSandboxManager) | Manager for interacting with the Private Compute Core (PCC) sandbox. |
| [PccService](https://developer.android.com/reference/kotlin/android/app/privatecompute/PccService) | Abstract base class for a PCC service that receives data from other components. |

## Exceptions

| [MigrationException](https://developer.android.com/reference/kotlin/android/app/privatecompute/MigrationException) | Exception thrown when a migration request fails. |
| [PccEgressException](https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException) | Exception thrown when an egress request fails inside the PCC sandbox. |
