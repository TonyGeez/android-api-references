# android.security.identity

## Interfaces

| [Entries](../android/security/identity/CredentialDataResult.Entries.md) | A class for representing data elements returned. |
| --- | --- |

## Classes

| [AccessControlProfile](../android/security/identity/AccessControlProfile.md) | A class used to specify access controls. |
| --- | --- |
| [AccessControlProfileId](../android/security/identity/AccessControlProfileId.md) | A class used to wrap an access control profile identifiers. |
| [AuthenticationKeyMetadata](../android/security/identity/AuthenticationKeyMetadata.md) | Data about authentication keys. |
| [CredentialDataRequest](../android/security/identity/CredentialDataRequest.md) | An object representing a request for credential data. |
| --- | --- |
| [CredentialDataResult](../android/security/identity/CredentialDataResult.md) | An object that contains the result of retrieving data from a credential. |
| [IdentityCredential](../android/security/identity/IdentityCredential.md) | Class used to read data from a previously provisioned credential. |
| [IdentityCredentialStore](../android/security/identity/IdentityCredentialStore.md) | An interface to a secure store for user identity documents. |
| --- | --- |
| [PersonalizationData](../android/security/identity/PersonalizationData.md) | An object that holds personalization data. |
| [PresentationSession](../android/security/identity/PresentationSession.md) | Class for presenting multiple documents to a remote verifier. |
| [ResultData](../android/security/identity/ResultData.md) | An object that contains the result of retrieving data from a credential. |
| --- | --- |
| [WritableIdentityCredential](../android/security/identity/WritableIdentityCredential.md) | Class used to personalize a new identity credential. |

## Exceptions

| [AlreadyPersonalizedException](../android/security/identity/AlreadyPersonalizedException.md) | Thrown if trying to create a credential which already exists. |
| --- | --- |
| [CipherSuiteNotSupportedException](../android/security/identity/CipherSuiteNotSupportedException.md) | Thrown if trying to use a cipher suite which isn't supported. |
| [DocTypeNotSupportedException](../android/security/identity/DocTypeNotSupportedException.md) | Thrown if trying to create a credential with an unsupported document type. |
| [EphemeralPublicKeyNotFoundException](../android/security/identity/EphemeralPublicKeyNotFoundException.md) | Thrown if the ephemeral public key was not found in the session transcript passed to `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredential#getEntries(kotlin.ByteArray,%20kotlin.collections.MutableMap,%20kotlin.ByteArray,%20kotlin.ByteArray)`. |
| --- | --- |
| [IdentityCredentialException](../android/security/identity/IdentityCredentialException.md) | Base class for all Identity Credential exceptions. |
| [InvalidReaderSignatureException](../android/security/identity/InvalidReaderSignatureException.md) | Thrown if the reader signature is invalid, or it doesn't contain a certificate chain, or if the signature failed to validate. |
| [InvalidRequestMessageException](../android/security/identity/InvalidRequestMessageException.md) | Thrown if message with the request doesn't satisfy the requirements documented in `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredential#getEntries(kotlin.ByteArray,%20kotlin.collections.MutableMap,%20kotlin.ByteArray,%20kotlin.ByteArray)`. |
| --- | --- |
| [MessageDecryptionException](../android/security/identity/MessageDecryptionException.md) | Thrown when failing to decrypt a message from the reader device. |
| [NoAuthenticationKeyAvailableException](../android/security/identity/NoAuthenticationKeyAvailableException.md) | Thrown if no dynamic authentication keys are available. |
| [SessionTranscriptMismatchException](../android/security/identity/SessionTranscriptMismatchException.md) | Thrown when trying use multiple different session transcripts in the same presentation session. |
| --- | --- |
| [UnknownAuthenticationKeyException](../android/security/identity/UnknownAuthenticationKeyException.md) | Thrown if trying to certify an unknown dynamic authentication key. |
