# android.credentials

# android.credentials

Kotlin| [Java](_package.md)
| --- | --- |

## Classes

| [ClearCredentialStateRequest](ClearCredentialStateRequest.md) | A request class for clearing a user's credential state from the credential providers. |
| --- | --- |
| [CreateCredentialRequest](CreateCredentialRequest.md) | A request to register a specific type of user credential, potentially launching UI flows to collect user consent and any other operation needed. |
| [CreateCredentialResponse](CreateCredentialResponse.md) | A response object that encapsulates the result of a successful credential creation execution. |
| [Credential](Credential.md) | Represents a user credential that can be used to authenticate to your app. |
| --- | --- |
| [CredentialDescription](CredentialDescription.md) | Represents the type and contained data fields of a [Credential](Credential.md). |
| [CredentialManager](CredentialManager.md) | Manages user authentication flows. |
| [CredentialOption](CredentialOption.md) | Information about a specific type of credential to be requested during a android. |
| --- | --- |
| [GetCredentialRequest](GetCredentialRequest.md) | A request to retrieve the user credential, potentially launching UI flows to let the user pick from different credential sources. |
| [GetCredentialResponse](GetCredentialResponse.md) | A response object that encapsulates the credential successfully retrieved from the user. |
| [PrepareGetCredentialResponse](PrepareGetCredentialResponse.md) | A response object that prefetches user app credentials and provides metadata about them. |
| --- | --- |
| [RegisterCredentialDescriptionRequest](RegisterCredentialDescriptionRequest.md) | A request to register a [ComponentName](../android.content/ComponentName.md) that contains an actively provisioned [Credential](Credential.md) represented by a [CredentialDescription](CredentialDescription.md). |
| [UnregisterCredentialDescriptionRequest](UnregisterCredentialDescriptionRequest.md) | A request to unregister a [ComponentName](../android.content/ComponentName.md) that contains an actively provisioned [Credential](Credential.md) represented by a [CredentialDescription](CredentialDescription.md). |

## Exceptions

| [ClearCredentialStateException](ClearCredentialStateException.md) | Represents an error encountered during the [CredentialManager.clearCredentialState(ClearCredentialStateRequest,](CredentialManager.md))operation. |
| --- | --- |
| [CreateCredentialException](CreateCredentialException.md) | Represents an error encountered during the [CredentialManager.createCredential(Context, CreateCredentialRequest,](CredentialManager.md))operation. |
| [GetCredentialException](GetCredentialException.md) | Represents an error encountered during the [CredentialManager.getCredential(Context, GetCredentialRequest,](CredentialManager.md))operation. |
