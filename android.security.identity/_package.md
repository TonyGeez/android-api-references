# android.security.identity

## Interfaces

| [Entries](https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult.Entries) | A class for representing data elements returned. |

## Classes

| [AccessControlProfile](https://developer.android.com/reference/kotlin/android/security/identity/AccessControlProfile) | A class used to specify access controls. |
| [AccessControlProfileId](https://developer.android.com/reference/kotlin/android/security/identity/AccessControlProfileId) | A class used to wrap an access control profile identifiers. |
| [AuthenticationKeyMetadata](https://developer.android.com/reference/kotlin/android/security/identity/AuthenticationKeyMetadata) | Data about authentication keys. |
| [CredentialDataRequest](https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataRequest) | An object representing a request for credential data. |
| [CredentialDataResult](https://developer.android.com/reference/kotlin/android/security/identity/CredentialDataResult) | An object that contains the result of retrieving data from a credential. |
| [IdentityCredential](https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredential) | Class used to read data from a previously provisioned credential. |
| [IdentityCredentialStore](https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialStore) | An interface to a secure store for user identity documents. |
| [PersonalizationData](https://developer.android.com/reference/kotlin/android/security/identity/PersonalizationData) | An object that holds personalization data. |
| [PresentationSession](https://developer.android.com/reference/kotlin/android/security/identity/PresentationSession) | Class for presenting multiple documents to a remote verifier. |
| [ResultData](https://developer.android.com/reference/kotlin/android/security/identity/ResultData) | An object that contains the result of retrieving data from a credential. |
| [WritableIdentityCredential](https://developer.android.com/reference/kotlin/android/security/identity/WritableIdentityCredential) | Class used to personalize a new identity credential. |

## Exceptions

| [AlreadyPersonalizedException](https://developer.android.com/reference/kotlin/android/security/identity/AlreadyPersonalizedException) | Thrown if trying to create a credential which already exists. |
| [CipherSuiteNotSupportedException](https://developer.android.com/reference/kotlin/android/security/identity/CipherSuiteNotSupportedException) | Thrown if trying to use a cipher suite which isn't supported. |
| [DocTypeNotSupportedException](https://developer.android.com/reference/kotlin/android/security/identity/DocTypeNotSupportedException) | Thrown if trying to create a credential with an unsupported document type. |
| [EphemeralPublicKeyNotFoundException](https://developer.android.com/reference/kotlin/android/security/identity/EphemeralPublicKeyNotFoundException) | Thrown if the ephemeral public key was not found in the session transcript passed to `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredential#getEntries(kotlin.ByteArray,%20kotlin.collections.MutableMap,%20kotlin.ByteArray,%20kotlin.ByteArray)`. |
| [IdentityCredentialException](https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialException) | Base class for all Identity Credential exceptions. |
| [InvalidReaderSignatureException](https://developer.android.com/reference/kotlin/android/security/identity/InvalidReaderSignatureException) | Thrown if the reader signature is invalid, or it doesn't contain a certificate chain, or if the signature failed to validate. |
| [InvalidRequestMessageException](https://developer.android.com/reference/kotlin/android/security/identity/InvalidRequestMessageException) | Thrown if message with the request doesn't satisfy the requirements documented in `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredential#getEntries(kotlin.ByteArray,%20kotlin.collections.MutableMap,%20kotlin.ByteArray,%20kotlin.ByteArray)`. |
| [MessageDecryptionException](https://developer.android.com/reference/kotlin/android/security/identity/MessageDecryptionException) | Thrown when failing to decrypt a message from the reader device. |
| [NoAuthenticationKeyAvailableException](https://developer.android.com/reference/kotlin/android/security/identity/NoAuthenticationKeyAvailableException) | Thrown if no dynamic authentication keys are available. |
| [SessionTranscriptMismatchException](https://developer.android.com/reference/kotlin/android/security/identity/SessionTranscriptMismatchException) | Thrown when trying use multiple different session transcripts in the same presentation session. |
| [UnknownAuthenticationKeyException](https://developer.android.com/reference/kotlin/android/security/identity/UnknownAuthenticationKeyException) | Thrown if trying to certify an unknown dynamic authentication key. |
