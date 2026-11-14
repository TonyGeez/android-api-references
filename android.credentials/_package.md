# android.credentials

# android.credentials

Kotlin| [Java](https://developer.android.com/reference/android/credentials/package-summary "View this page in Java")
| --- | --- |

## Classes

| [ClearCredentialStateRequest](https://developer.android.com/reference/kotlin/android/credentials/ClearCredentialStateRequest) | A request class for clearing a user's credential state from the credential providers. |
| --- | --- |
| [CreateCredentialRequest](https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialRequest) | A request to register a specific type of user credential, potentially launching UI flows to collect user consent and any other operation needed. |
| [CreateCredentialResponse](https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialResponse) | A response object that encapsulates the result of a successful credential creation execution. |
| [Credential](https://developer.android.com/reference/kotlin/android/credentials/Credential) | Represents a user credential that can be used to authenticate to your app. |
| --- | --- |
| [CredentialDescription](https://developer.android.com/reference/kotlin/android/credentials/CredentialDescription) | Represents the type and contained data fields of a [Credential](https://developer.android.com/reference/kotlin/android/credentials/Credential). |
| [CredentialManager](https://developer.android.com/reference/kotlin/android/credentials/CredentialManager) | Manages user authentication flows. |
| [CredentialOption](https://developer.android.com/reference/kotlin/android/credentials/CredentialOption) | Information about a specific type of credential to be requested during a android. |
| --- | --- |
| [GetCredentialRequest](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialRequest) | A request to retrieve the user credential, potentially launching UI flows to let the user pick from different credential sources. |
| [GetCredentialResponse](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialResponse) | A response object that encapsulates the credential successfully retrieved from the user. |
| [PrepareGetCredentialResponse](https://developer.android.com/reference/kotlin/android/credentials/PrepareGetCredentialResponse) | A response object that prefetches user app credentials and provides metadata about them. |
| --- | --- |
| [RegisterCredentialDescriptionRequest](https://developer.android.com/reference/kotlin/android/credentials/RegisterCredentialDescriptionRequest) | A request to register a [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#) that contains an actively provisioned [Credential](https://developer.android.com/reference/kotlin/android/credentials/Credential) represented by a [CredentialDescription](https://developer.android.com/reference/kotlin/android/credentials/CredentialDescription). |
| [UnregisterCredentialDescriptionRequest](https://developer.android.com/reference/kotlin/android/credentials/UnregisterCredentialDescriptionRequest) | A request to unregister a [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#) that contains an actively provisioned [Credential](https://developer.android.com/reference/kotlin/android/credentials/Credential) represented by a [CredentialDescription](https://developer.android.com/reference/kotlin/android/credentials/CredentialDescription). |

## Exceptions

| [ClearCredentialStateException](https://developer.android.com/reference/kotlin/android/credentials/ClearCredentialStateException) | Represents an error encountered during the [CredentialManager.clearCredentialState(ClearCredentialStateRequest,](https://developer.android.com/reference/kotlin/android/credentials/CredentialManager#clearCredentialState(android.credentials.ClearCredentialStateRequest,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))operation. |
| --- | --- |
| [CreateCredentialException](https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialException) | Represents an error encountered during the [CredentialManager.createCredential(Context, CreateCredentialRequest,](https://developer.android.com/reference/kotlin/android/credentials/CredentialManager#createCredential(android.content.Context,%20android.credentials.CreateCredentialRequest,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))operation. |
| [GetCredentialException](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException) | Represents an error encountered during the [CredentialManager.getCredential(Context, GetCredentialRequest,](https://developer.android.com/reference/kotlin/android/credentials/CredentialManager#getCredential(android.content.Context,%20android.credentials.GetCredentialRequest,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))operation. |
