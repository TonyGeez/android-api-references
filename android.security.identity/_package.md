# android.security.identity

## Interfaces

| [Entries](../android/security/identity/CredentialDataResult.Entries.md) | A class for representing data elements returned. |
| --- | --- |

## Classes

| [AccessControlProfile](AccessControlProfile.md) | A class used to specify access controls. |
| --- | --- |
| [AccessControlProfileId](AccessControlProfileId.md) | A class used to wrap an access control profile identifiers. |
| [AuthenticationKeyMetadata](AuthenticationKeyMetadata.md) | Data about authentication keys. |
| [CredentialDataRequest](CredentialDataRequest.md) | An object representing a request for credential data. |
| --- | --- |
| [CredentialDataResult](CredentialDataResult.md) | An object that contains the result of retrieving data from a credential. |
| [IdentityCredential](IdentityCredential.md) | Class used to read data from a previously provisioned credential. |
| [IdentityCredentialStore](IdentityCredentialStore.md) | An interface to a secure store for user identity documents. |
| --- | --- |
| [PersonalizationData](PersonalizationData.md) | An object that holds personalization data. |
| [PresentationSession](PresentationSession.md) | Class for presenting multiple documents to a remote verifier. |
| [ResultData](ResultData.md) | An object that contains the result of retrieving data from a credential. |
| --- | --- |
| [WritableIdentityCredential](WritableIdentityCredential.md) | Class used to personalize a new identity credential. |

## Exceptions

| [AlreadyPersonalizedException](AlreadyPersonalizedException.md) | Thrown if trying to create a credential which already exists. |
| --- | --- |
| [CipherSuiteNotSupportedException](CipherSuiteNotSupportedException.md) | Thrown if trying to use a cipher suite which isn't supported. |
| [DocTypeNotSupportedException](DocTypeNotSupportedException.md) | Thrown if trying to create a credential with an unsupported document type. |
| [EphemeralPublicKeyNotFoundException](EphemeralPublicKeyNotFoundException.md) | Thrown if the ephemeral public key was not found in the session transcript passed to `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredential#getEntries(kotlin.ByteArray,%20kotlin.collections.MutableMap,%20kotlin.ByteArray,%20kotlin.ByteArray)`. |
| --- | --- |
| [IdentityCredentialException](IdentityCredentialException.md) | Base class for all Identity Credential exceptions. |
| [InvalidReaderSignatureException](InvalidReaderSignatureException.md) | Thrown if the reader signature is invalid, or it doesn't contain a certificate chain, or if the signature failed to validate. |
| [InvalidRequestMessageException](InvalidRequestMessageException.md) | Thrown if message with the request doesn't satisfy the requirements documented in `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredential#getEntries(kotlin.ByteArray,%20kotlin.collections.MutableMap,%20kotlin.ByteArray,%20kotlin.ByteArray)`. |
| --- | --- |
| [MessageDecryptionException](MessageDecryptionException.md) | Thrown when failing to decrypt a message from the reader device. |
| [NoAuthenticationKeyAvailableException](NoAuthenticationKeyAvailableException.md) | Thrown if no dynamic authentication keys are available. |
| [SessionTranscriptMismatchException](SessionTranscriptMismatchException.md) | Thrown when trying use multiple different session transcripts in the same presentation session. |
| --- | --- |
| [UnknownAuthenticationKeyException](UnknownAuthenticationKeyException.md) | Thrown if trying to certify an unknown dynamic authentication key. |
