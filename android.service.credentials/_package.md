# android.service.credentials

# android.service.credentials

Kotlin| [Java](_package.md)
| --- | --- |

## Classes

| [Action](Action.md) | An action defined by the provider that intents into the provider's app for specific user actions. |
| --- | --- |
| [BeginCreateCredentialRequest](BeginCreateCredentialRequest.md) | Request for beginning a create credential request. |
| [BeginCreateCredentialResponse](BeginCreateCredentialResponse.md) | Response to a [BeginCreateCredentialRequest](BeginCreateCredentialRequest.md). |
| [BeginGetCredentialOption](BeginGetCredentialOption.md) | A specific type of credential request to be sent to the provider during the query phase of a get flow. |
| --- | --- |
| [BeginGetCredentialRequest](BeginGetCredentialRequest.md) | Query stage request for getting user's credentials from a given credential provider. |
| [BeginGetCredentialResponse](BeginGetCredentialResponse.md) | Response from a credential provider, containing credential entries and other associated data to be shown on the account selector UI. |
| [CallingAppInfo](CallingAppInfo.md) | Information pertaining to the calling application, including the package name and a list of app signatures. |
| --- | --- |
| [ClearCredentialStateRequest](ClearCredentialStateRequest.md) | A request class for clearing a user's credential state. |
| [CreateCredentialRequest](CreateCredentialRequest.md) | Request for creating a credential. |
| [CreateEntry](CreateEntry.md) | An entry to be shown on the UI. |
| --- | --- |
| [CredentialEntry](CredentialEntry.md) | A credential entry that is to be displayed on the account selector that is presented to the user. |
| [CredentialProviderService](CredentialProviderService.md) | Service to be extended by credential providers, in order to return user credentials to the framework. |
| [GetCredentialRequest](GetCredentialRequest.md) | Request for getting user's credential from a given credential provider. |
| --- | --- |
| [RemoteEntry](RemoteEntry.md) | An entry to be shown on the UI. |
