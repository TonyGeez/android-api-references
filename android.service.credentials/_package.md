# android.service.credentials

# android.service.credentials

Kotlin| [Java](../android/service/credentials/_package.md)
| --- | --- |

## Classes

| [Action](../android/service/credentials/Action.md) | An action defined by the provider that intents into the provider's app for specific user actions. |
| --- | --- |
| [BeginCreateCredentialRequest](../android/service/credentials/BeginCreateCredentialRequest.md) | Request for beginning a create credential request. |
| [BeginCreateCredentialResponse](../android/service/credentials/BeginCreateCredentialResponse.md) | Response to a [BeginCreateCredentialRequest](../android/service/credentials/BeginCreateCredentialRequest.md). |
| [BeginGetCredentialOption](../android/service/credentials/BeginGetCredentialOption.md) | A specific type of credential request to be sent to the provider during the query phase of a get flow. |
| --- | --- |
| [BeginGetCredentialRequest](../android/service/credentials/BeginGetCredentialRequest.md) | Query stage request for getting user's credentials from a given credential provider. |
| [BeginGetCredentialResponse](../android/service/credentials/BeginGetCredentialResponse.md) | Response from a credential provider, containing credential entries and other associated data to be shown on the account selector UI. |
| [CallingAppInfo](../android/service/credentials/CallingAppInfo.md) | Information pertaining to the calling application, including the package name and a list of app signatures. |
| --- | --- |
| [ClearCredentialStateRequest](../android/service/credentials/ClearCredentialStateRequest.md) | A request class for clearing a user's credential state. |
| [CreateCredentialRequest](../android/service/credentials/CreateCredentialRequest.md) | Request for creating a credential. |
| [CreateEntry](../android/service/credentials/CreateEntry.md) | An entry to be shown on the UI. |
| --- | --- |
| [CredentialEntry](../android/service/credentials/CredentialEntry.md) | A credential entry that is to be displayed on the account selector that is presented to the user. |
| [CredentialProviderService](../android/service/credentials/CredentialProviderService.md) | Service to be extended by credential providers, in order to return user credentials to the framework. |
| [GetCredentialRequest](../android/service/credentials/GetCredentialRequest.md) | Request for getting user's credential from a given credential provider. |
| --- | --- |
| [RemoteEntry](../android/service/credentials/RemoteEntry.md) | An entry to be shown on the UI. |
