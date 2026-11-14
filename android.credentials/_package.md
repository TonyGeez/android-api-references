# android.credentials

# android.credentials

Kotlin| [Java](../android/credentials/_package.md)
| --- | --- |

## Classes

| [ClearCredentialStateRequest](../android/credentials/ClearCredentialStateRequest.md) | A request class for clearing a user's credential state from the credential providers. |
| --- | --- |
| [CreateCredentialRequest](../android/credentials/CreateCredentialRequest.md) | A request to register a specific type of user credential, potentially launching UI flows to collect user consent and any other operation needed. |
| [CreateCredentialResponse](../android/credentials/CreateCredentialResponse.md) | A response object that encapsulates the result of a successful credential creation execution. |
| [Credential](../android/credentials/Credential.md) | Represents a user credential that can be used to authenticate to your app. |
| --- | --- |
| [CredentialDescription](../android/credentials/CredentialDescription.md) | Represents the type and contained data fields of a [Credential](../android/credentials/Credential.md). |
| [CredentialManager](../android/credentials/CredentialManager.md) | Manages user authentication flows. |
| [CredentialOption](../android/credentials/CredentialOption.md) | Information about a specific type of credential to be requested during a android. |
| --- | --- |
| [GetCredentialRequest](../android/credentials/GetCredentialRequest.md) | A request to retrieve the user credential, potentially launching UI flows to let the user pick from different credential sources. |
| [GetCredentialResponse](../android/credentials/GetCredentialResponse.md) | A response object that encapsulates the credential successfully retrieved from the user. |
| [PrepareGetCredentialResponse](../android/credentials/PrepareGetCredentialResponse.md) | A response object that prefetches user app credentials and provides metadata about them. |
| --- | --- |
| [RegisterCredentialDescriptionRequest](../android/credentials/RegisterCredentialDescriptionRequest.md) | A request to register a [ComponentName](../android/content/ComponentName.md) that contains an actively provisioned [Credential](../android/credentials/Credential.md) represented by a [CredentialDescription](../android/credentials/CredentialDescription.md). |
| [UnregisterCredentialDescriptionRequest](../android/credentials/UnregisterCredentialDescriptionRequest.md) | A request to unregister a [ComponentName](../android/content/ComponentName.md) that contains an actively provisioned [Credential](../android/credentials/Credential.md) represented by a [CredentialDescription](../android/credentials/CredentialDescription.md). |

## Exceptions

| [ClearCredentialStateException](../android/credentials/ClearCredentialStateException.md) | Represents an error encountered during the [CredentialManager.clearCredentialState(ClearCredentialStateRequest,](../android/credentials/CredentialManager.md))operation. |
| --- | --- |
| [CreateCredentialException](../android/credentials/CreateCredentialException.md) | Represents an error encountered during the [CredentialManager.createCredential(Context, CreateCredentialRequest,](../android/credentials/CredentialManager.md))operation. |
| [GetCredentialException](../android/credentials/GetCredentialException.md) | Represents an error encountered during the [CredentialManager.getCredential(Context, GetCredentialRequest,](../android/credentials/CredentialManager.md))operation. |
