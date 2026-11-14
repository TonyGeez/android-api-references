Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Exception

```
open class Exception : Throwable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception#) |

Known Direct Subclasses [AccountsException](https://developer.android.com/reference/kotlin/android/accounts/AccountsException.html#), [AclNotFoundException](https://developer.android.com/reference/kotlin/java/security/acl/AclNotFoundException.html#), [AdServicesException](https://developer.android.com/reference/kotlin/android/adservices/exceptions/AdServicesException.html#), [AndroidException](https://developer.android.com/reference/kotlin/android/util/AndroidException.html#), [AppFunctionException](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException.html#), [AppInteractionException](https://developer.android.com/reference/kotlin/android/app/AppInteractionException.html#), [AppSearchException](https://developer.android.com/reference/kotlin/android/app/appsearch/exceptions/AppSearchException.html#), [BackingStoreException](https://developer.android.com/reference/kotlin/java/util/prefs/BackingStoreException.html#), [BrokenBarrierException](https://developer.android.com/reference/kotlin/java/util/concurrent/BrokenBarrierException.html#), [CertificateException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateException.html#), [ClearCredentialStateException](https://developer.android.com/reference/kotlin/android/credentials/ClearCredentialStateException.html#), [CloneNotSupportedException](https://developer.android.com/reference/kotlin/java/lang/CloneNotSupportedException), and 55 others. [AccountsException](https://developer.android.com/reference/kotlin/android/accounts/AccountsException.html#) <br />

[AclNotFoundException](https://developer.android.com/reference/kotlin/java/security/acl/AclNotFoundException.html#) This is an exception that is thrown whenever a reference is made to a non-existent ACL (Access Control List).
[AdServicesException](https://developer.android.com/reference/kotlin/android/adservices/exceptions/AdServicesException.html#) Exception thrown by AdServices.
[AndroidException](https://developer.android.com/reference/kotlin/android/util/AndroidException.html#) Base class for all checked exceptions thrown by the Android frameworks.
[AppFunctionException](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException.html#) App function related error.
[AppInteractionException](https://developer.android.com/reference/kotlin/android/app/AppInteractionException.html#) Exception thrown when an app interaction operation fails.
[AppSearchException](https://developer.android.com/reference/kotlin/android/app/appsearch/exceptions/AppSearchException.html#) An exception thrown by `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession.html#` or a subcomponent.
[BackingStoreException](https://developer.android.com/reference/kotlin/java/util/prefs/BackingStoreException.html#) Thrown to indicate that a preferences operation could not complete because of a failure in the backing store, or a failure to contact the backing store.
[BrokenBarrierException](https://developer.android.com/reference/kotlin/java/util/concurrent/BrokenBarrierException.html#) Exception thrown when a thread tries to wait upon a barrier that is in a broken state, or which enters the broken state while the thread is waiting.
[CertificateException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateException.html#) This exception indicates one of a variety of certificate problems.
[ClearCredentialStateException](https://developer.android.com/reference/kotlin/android/credentials/ClearCredentialStateException.html#) Represents an error encountered during the `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#clearCredentialState(android.credentials.ClearCredentialStateRequest,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` operation.
[CloneNotSupportedException](https://developer.android.com/reference/kotlin/java/lang/CloneNotSupportedException) Thrown to indicate that the `clone` method in class `Object` has been called to clone an object, but that the object's class does not implement the `Cloneable` interface.
[ConfirmationAlreadyPresentingException](https://developer.android.com/reference/kotlin/android/security/ConfirmationAlreadyPresentingException.html#) This exception is thrown when presenting a prompt fails because another prompt is already being presented.
[ConfirmationNotAvailableException](https://developer.android.com/reference/kotlin/android/security/ConfirmationNotAvailableException.html#) This exception is thrown when presenting a prompt fails because the environment lacks facilities for showing confirmations.
[CreateCredentialException](https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialException.html#) Represents an error encountered during the `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#createCredential(android.content.Context,%20android.credentials.CreateCredentialRequest,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` operation.
[CrossDeviceAuthenticationException](https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/CrossDeviceAuthenticationException.html#) Exception thrown when cross-device authentication fails.
[DataFormatException](https://developer.android.com/reference/kotlin/java/util/zip/DataFormatException.html#) Signals that a data format error has occurred.
[DatatypeConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/datatype/DatatypeConfigurationException.html#) Indicates a serious configuration error.
[DestroyFailedException](https://developer.android.com/reference/kotlin/javax/security/auth/DestroyFailedException.html#) Signals that a `destroy` operation failed.
[DnsResolver.DnsException](https://developer.android.com/reference/kotlin/android/net/DnsResolver.DnsException.html#) Class to represent DNS error
[ErrnoException](https://developer.android.com/reference/kotlin/android/system/ErrnoException.html#) A checked exception thrown when `https://developer.android.com/reference/kotlin/android/system/Os.html#` methods fail.
[ExecutionException](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutionException.html#) Exception thrown when attempting to retrieve the result of a task that aborted by throwing an exception.
[FormatException](https://developer.android.com/reference/kotlin/android/nfc/FormatException.html#) <br />

[GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException.html#) The `GeneralSecurityException` class is a generic security exception class that provides type safety for all the security-related exception classes that extend from it.
[GetCredentialException](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException.html#) Represents an error encountered during the `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#getCredential(android.content.Context,%20android.credentials.GetCredentialRequest,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` operation.
[IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) Signals that an I/O exception of some sort has occurred.
[IdentityCredentialException](https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredentialException.html#) Base class for all Identity Credential exceptions.
[IkeException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeException.html#) IkeException represents a generic exception that includes internal and protocol exceptions.
[ImsException](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsException.html#) This class defines an IMS-related exception that has been thrown while interacting with a device or carrier provided ImsService implementation.
[InterruptedException](https://developer.android.com/reference/kotlin/java/lang/InterruptedException) Thrown when a thread is waiting, sleeping, or otherwise occupied, and the thread is interrupted, either before or during the activity.
[InvalidPreferencesFormatException](https://developer.android.com/reference/kotlin/java/util/prefs/InvalidPreferencesFormatException.html#) Thrown to indicate that an operation could not complete because the input did not conform to the appropriate XML document type for a collection of preferences, as per the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences.html#` specification.
[IsolatedServiceException](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedServiceException.html#) A class that an `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService.html#` can use to signal a failure in handling a request and return an error to be logged and aggregated.
[JSONException](https://developer.android.com/reference/kotlin/org/json/JSONException.html#) Thrown to indicate a problem with the JSON API.
[KeyChainException](https://developer.android.com/reference/kotlin/android/security/KeyChainException.html#) Thrown on problems accessing the `https://developer.android.com/reference/kotlin/android/security/KeyChain.html#`.
[KeyStoreException](https://developer.android.com/reference/kotlin/android/security/KeyStoreException.html#) Exception containing information about the failure at the Keystore / KeyMint layer while generating or using a key.
[LambdaConversionException](https://developer.android.com/reference/kotlin/java/lang/invoke/LambdaConversionException) LambdaConversionException
[LastOwnerException](https://developer.android.com/reference/kotlin/java/security/acl/LastOwnerException.html#) This is an exception that is thrown whenever an attempt is made to delete the last owner of an Access Control List.
[LoadSdkException](https://developer.android.com/reference/kotlin/android/app/sdksandbox/LoadSdkException.html#) Exception thrown by `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager.html#loadSdk(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`
[MediaCasException](https://developer.android.com/reference/kotlin/android/media/MediaCasException.html#) Base class for MediaCas exceptions
[MediaCryptoException](https://developer.android.com/reference/kotlin/android/media/MediaCryptoException.html#) Exception thrown if MediaCrypto object could not be instantiated or if unable to perform an operation on the MediaCrypto object.
[MediaDrmException](https://developer.android.com/reference/kotlin/android/media/MediaDrmException.html#) Base class for MediaDrm exceptions
[MigrationException](https://developer.android.com/reference/kotlin/android/app/privatecompute/MigrationException.html#) Exception thrown when a migration request fails.
[NotOwnerException](https://developer.android.com/reference/kotlin/java/security/acl/NotOwnerException.html#) This is an exception that is thrown whenever the modification of an object (such as an Access Control List) is only allowed to be done by an owner of the object, but the Principal attempting the modification is not an owner.
[OnDevicePersonalizationException](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException.html#) Exception thrown by OnDevicePersonalization APIs.
[OperationApplicationException](https://developer.android.com/reference/kotlin/android/content/OperationApplicationException.html#) Thrown when an application of a `https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.html#` fails due the specified constraints.
[ParseException](https://developer.android.com/reference/kotlin/java/text/ParseException.html#) Signals that an error has been reached unexpectedly while parsing.
[ParserConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/parsers/ParserConfigurationException.html#) Indicates a serious configuration error.
[PccEgressException](https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException.html#) Exception thrown when an egress request fails inside the PCC sandbox.
[PrivilegedActionException](https://developer.android.com/reference/kotlin/java/security/PrivilegedActionException.html#) Legacy security code; do not use.
[ReflectiveOperationException](https://developer.android.com/reference/kotlin/java/lang/ReflectiveOperationException) Common superclass of exceptions thrown by reflective operations in core reflection.
[RequestSurfacePackageException](https://developer.android.com/reference/kotlin/android/app/sdksandbox/RequestSurfacePackageException.html#) Exception thrown by `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager.html#requestSurfacePackage(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`
[RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException) `RuntimeException` is the superclass of those exceptions that can be thrown during the normal operation of the Java Virtual Machine.
[SAXException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException.html#) Encapsulate a general SAX error or warning.
[SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException.html#) An exception that provides information on a database access error or other errors.
[SigningInfoException](https://developer.android.com/reference/kotlin/android/content/pm/SigningInfoException.html#) Indicates an error when verifying the [app signing](https://source.android.com/docs/security/features/apksigning) information.
[SipException](https://developer.android.com/reference/kotlin/android/net/sip/SipException.html#) Indicates a general SIP-related exception.
[StringConcatException](https://developer.android.com/reference/kotlin/java/lang/invoke/StringConcatException) StringConcatException is thrown by `https://developer.android.com/reference/kotlin/java/lang/Exception#` when linkage invariants are violated.
[SurfaceTexture.OutOfResourcesException](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.OutOfResourcesException.html#) Exception thrown when a SurfaceTexture couldn't be created or resized.
[TelephonyManager.CallComposerException](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.CallComposerException.html#) Exception that may be supplied to the callback in #uploadCallComposerPicture if something goes awry.
[TelephonyManager.NetworkSlicingException](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.NetworkSlicingException.html#) Exception that may be supplied to the callback in `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#getNetworkSlicingConfiguration(java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` if something goes awry.
[TimeoutException](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeoutException.html#) Exception thrown when a blocking operation times out.
[TooManyListenersException](https://developer.android.com/reference/kotlin/java/util/TooManyListenersException.html#) The `TooManyListenersException ` Exception is used as part of the Java Event model to annotate and implement a unicast special case of a multicast Event Source.
[TransformerException](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException.html#) This class specifies an exceptional condition that occurred during the transformation process.
[URISyntaxException](https://developer.android.com/reference/kotlin/java/net/URISyntaxException.html#) Checked exception thrown to indicate that a string could not be parsed as a URI reference.
[UnsupportedCallbackException](https://developer.android.com/reference/kotlin/javax/security/auth/callback/UnsupportedCallbackException.html#) Signals that a `CallbackHandler` does not recognize a particular `Callback`.
[XPathException](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathException.html#) `XPathException` represents a generic XPath exception.
[XmlPullParserException](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserException.html#) This exception is thrown to signal XML Pull Parser related faults.
Known Indirect Subclasses [AEADBadTagException](https://developer.android.com/reference/kotlin/javax/crypto/AEADBadTagException.html#), [AcceptPendingException](https://developer.android.com/reference/kotlin/java/nio/channels/AcceptPendingException.html#), [AccessControlException](https://developer.android.com/reference/kotlin/java/security/AccessControlException.html#), [AccessDeniedException](https://developer.android.com/reference/kotlin/java/nio/file/AccessDeniedException.html#), [AconfigStorageReadException](https://developer.android.com/reference/kotlin/android/os/flagging/AconfigStorageReadException.html#), [ActivityNotFoundException](https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException.html#), [AlreadyBoundException](https://developer.android.com/reference/kotlin/java/nio/channels/AlreadyBoundException.html#), [AlreadyConnectedException](https://developer.android.com/reference/kotlin/java/nio/channels/AlreadyConnectedException.html#), [AlreadyPersonalizedException](https://developer.android.com/reference/kotlin/android/security/identity/AlreadyPersonalizedException.html#), [AndroidRuntimeException](https://developer.android.com/reference/kotlin/android/util/AndroidRuntimeException.html#), [AnnotationTypeMismatchException](https://developer.android.com/reference/kotlin/java/lang/annotation/AnnotationTypeMismatchException), [AppInteractionDeniedException](https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException.html#), and 354 others. [AEADBadTagException](https://developer.android.com/reference/kotlin/javax/crypto/AEADBadTagException.html#) This exception is thrown when a `https://developer.android.com/reference/kotlin/javax/crypto/Cipher.html#` operating in an AEAD mode (such as GCM/CCM) is unable to verify the supplied authentication tag.
[AcceptPendingException](https://developer.android.com/reference/kotlin/java/nio/channels/AcceptPendingException.html#) Unchecked exception thrown when an attempt is made to initiate an accept operation on a channel and a previous accept operation has not completed.
[AccessControlException](https://developer.android.com/reference/kotlin/java/security/AccessControlException.html#) This exception is thrown by the AccessController to indicate that a requested access (to a critical system resource such as the file system or the network) is denied.
[AccessDeniedException](https://developer.android.com/reference/kotlin/java/nio/file/AccessDeniedException.html#) Checked exception thrown when a file system operation is denied, typically due to a file permission or other access check.
[AconfigStorageReadException](https://developer.android.com/reference/kotlin/android/os/flagging/AconfigStorageReadException.html#) Exception thrown when an error occurs while reading from Aconfig Storage.
[ActivityNotFoundException](https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException.html#) This exception is thrown when a call to android.
[AlreadyBoundException](https://developer.android.com/reference/kotlin/java/nio/channels/AlreadyBoundException.html#) Unchecked exception thrown when an attempt is made to bind the socket a network oriented channel that is already bound.
[AlreadyConnectedException](https://developer.android.com/reference/kotlin/java/nio/channels/AlreadyConnectedException.html#) Unchecked exception thrown when an attempt is made to connect a `https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel.html#` that is already connected.
[AlreadyPersonalizedException](https://developer.android.com/reference/kotlin/android/security/identity/AlreadyPersonalizedException.html#) Thrown if trying to create a credential which already exists.
[AndroidRuntimeException](https://developer.android.com/reference/kotlin/android/util/AndroidRuntimeException.html#) Base class for all unchecked exceptions thrown by the Android frameworks.
[AnnotationTypeMismatchException](https://developer.android.com/reference/kotlin/java/lang/annotation/AnnotationTypeMismatchException) Thrown to indicate that a program has attempted to access an element of an annotation whose type has changed after the annotation was compiled (or serialized).
[AppInteractionDeniedException](https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException.html#) Exception thrown when an app interaction is denied.
[ArithmeticException](https://developer.android.com/reference/kotlin/java/lang/ArithmeticException) Thrown when an exceptional arithmetic condition has occurred.
[ArrayIndexOutOfBoundsException](https://developer.android.com/reference/kotlin/java/lang/ArrayIndexOutOfBoundsException) Thrown to indicate that an array has been accessed with an illegal index.
[ArrayStoreException](https://developer.android.com/reference/kotlin/java/lang/ArrayStoreException) Thrown to indicate that an attempt has been made to store the wrong type of object into an array of objects.
[AsynchronousCloseException](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousCloseException.html#) Checked exception received by a thread when another thread closes the channel or the part of the channel upon which it is blocked in an I/O operation.
[AtomicMoveNotSupportedException](https://developer.android.com/reference/kotlin/java/nio/file/AtomicMoveNotSupportedException.html#) Checked exception thrown when a file cannot be moved as an atomic file system operation.
[AuthenticationRequiredException](https://developer.android.com/reference/kotlin/android/app/AuthenticationRequiredException.html#) Specialization of `https://developer.android.com/reference/kotlin/java/lang/SecurityException` that is thrown when authentication is needed from the end user before viewing the content.
[AuthenticatorException](https://developer.android.com/reference/kotlin/android/accounts/AuthenticatorException.html#) <br />

[BackendBusyException](https://developer.android.com/reference/kotlin/android/security/keystore/BackendBusyException.html#) Indicates a transient error that prevented a key operation from being created.
[BackgroundServiceStartNotAllowedException](https://developer.android.com/reference/kotlin/android/app/BackgroundServiceStartNotAllowedException.html#) Exception thrown when an app tries to start a background `https://developer.android.com/reference/kotlin/android/app/Service.html#` when it's not allowed to do so.
[BadPaddingException](https://developer.android.com/reference/kotlin/javax/crypto/BadPaddingException.html#) This exception is thrown when a particular padding mechanism is expected for the input data but the data is not padded properly.
[BadParcelableException](https://developer.android.com/reference/kotlin/android/os/BadParcelableException.html#) Exception thrown when a `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` is malformed or otherwise invalid.
[Base64DataException](https://developer.android.com/reference/kotlin/android/util/Base64DataException.html#) This exception is thrown by `https://developer.android.com/reference/kotlin/android/util/Base64InputStream.html#` or `https://developer.android.com/reference/kotlin/android/util/Base64OutputStream.html#` when an error is detected in the data being decoded.
[BatchUpdateException](https://developer.android.com/reference/kotlin/java/sql/BatchUpdateException.html#) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` thrown when an error occurs during a batch update operation.
[BindException](https://developer.android.com/reference/kotlin/java/net/BindException.html#) Signals that an error occurred while attempting to bind a socket to a local address and port.
[BluetoothSocketException](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketException.html#) Thrown when an error occurs during a Bluetooth Socket related exception.
[BufferOverflowException](https://developer.android.com/reference/kotlin/java/nio/BufferOverflowException.html#) Unchecked exception thrown when a relative *put* operation reaches the target buffer's limit.
[BufferUnderflowException](https://developer.android.com/reference/kotlin/java/nio/BufferUnderflowException.html#) Unchecked exception thrown when a relative *get* operation reaches the source buffer's limit.
[CRLException](https://developer.android.com/reference/kotlin/java/security/cert/CRLException.html#) CRL (Certificate Revocation List) Exception.
[CallEndpointException](https://developer.android.com/reference/kotlin/android/telecom/CallEndpointException.html#) This class represents a set of exceptions that can occur when requesting a `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint.html#` change.
[CallException](https://developer.android.com/reference/kotlin/android/telecom/CallException.html#) This class defines exceptions that can be thrown when using Telecom APIs with `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#`s.
[CallbackException](https://developer.android.com/reference/kotlin/android/net/http/CallbackException.html#) Exception passed to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback.html#onFailed(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)` when `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback.html#` or `https://developer.android.com/reference/kotlin/android/net/http/UploadDataProvider.html#` method throws an exception.
[CameraAccessException](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException.html#) `CameraAccessException` is thrown if a camera device could not be queried or opened by the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.html#`, or if the connection to an opened `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#` is no longer valid.
[CancellationException](https://developer.android.com/reference/kotlin/java/util/concurrent/CancellationException.html#) Exception indicating that the result of a value-producing task, such as a `https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask.html#`, cannot be retrieved because the task was cancelled.
[CancelledKeyException](https://developer.android.com/reference/kotlin/java/nio/channels/CancelledKeyException.html#) Unchecked exception thrown when an attempt is made to use a selection key that is no longer valid.
[CertPathBuilderException](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilderException.html#) An exception indicating one of a variety of problems encountered when building a certification path with a `CertPathBuilder`.
[CertPathValidatorException](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException.html#) An exception indicating one of a variety of problems encountered when validating a certification path.
[CertStoreException](https://developer.android.com/reference/kotlin/java/security/cert/CertStoreException.html#) An exception indicating one of a variety of problems retrieving certificates and CRLs from a `CertStore`.
[CertificateEncodingException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateEncodingException.html#) Certificate Encoding Exception.
[CertificateEncodingException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateEncodingException.html#) Certificate Encoding Exception.
[CertificateException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateException.html#) This exception indicates one of a variety of certificate problems.
[CertificateExpiredException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateExpiredException.html#) Certificate Expired Exception.
[CertificateExpiredException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateExpiredException.html#) Certificate Expired Exception.
[CertificateNotYetValidException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateNotYetValidException.html#) Certificate is not yet valid exception.
[CertificateNotYetValidException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateNotYetValidException.html#) Certificate is not yet valid exception.
[CertificateParsingException](https://developer.android.com/reference/kotlin/javax/security/cert/CertificateParsingException.html#) Certificate Parsing Exception.
[CertificateParsingException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateParsingException.html#) Certificate Parsing Exception.
[CertificateRevokedException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateRevokedException.html#) An exception that indicates an X.
[CharConversionException](https://developer.android.com/reference/kotlin/java/io/CharConversionException.html#) Base class for character conversion exceptions.
[CharacterCodingException](https://developer.android.com/reference/kotlin/java/nio/charset/CharacterCodingException.html#) Checked exception thrown when a character encoding or decoding error occurs.
[CipherSuiteNotSupportedException](https://developer.android.com/reference/kotlin/android/security/identity/CipherSuiteNotSupportedException.html#) Thrown if trying to use a cipher suite which isn't supported.
[ClassCastException](https://developer.android.com/reference/kotlin/java/lang/ClassCastException) Thrown to indicate that the code has attempted to cast an object to a subclass of which it is not an instance.
[ClassNotFoundException](https://developer.android.com/reference/kotlin/java/lang/ClassNotFoundException) Thrown when an application tries to load in a class through its string name using:

- The `forName` method in class `Class`.
- The `findSystemClass` method in class `ClassLoader` .
- The `loadClass` method in class `ClassLoader`.

<br />

[ClosedByInterruptException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedByInterruptException.html#) Checked exception received by a thread when another thread interrupts it while it is blocked in an I/O operation upon a channel.
[ClosedChannelException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedChannelException.html#) Checked exception thrown when an attempt is made to invoke or complete an I/O operation upon channel that is closed, or at least closed to that operation.
[ClosedDirectoryStreamException](https://developer.android.com/reference/kotlin/java/nio/file/ClosedDirectoryStreamException.html#) Unchecked exception thrown when an attempt is made to invoke an operation on a directory stream that is closed.
[ClosedFileSystemException](https://developer.android.com/reference/kotlin/java/nio/file/ClosedFileSystemException.html#) Unchecked exception thrown when an attempt is made to invoke an operation on a file and the file system is closed.
[ClosedSelectorException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedSelectorException.html#) Unchecked exception thrown when an attempt is made to invoke an I/O operation upon a closed selector.
[ClosedWatchServiceException](https://developer.android.com/reference/kotlin/java/nio/file/ClosedWatchServiceException.html#) Unchecked exception thrown when an attempt is made to invoke an operation on a watch service that is closed.
[CompanionException](https://developer.android.com/reference/kotlin/android/companion/CompanionException.html#) `CompanionException` can be thrown during the companion system data transfer process.
[CompletionException](https://developer.android.com/reference/kotlin/java/util/concurrent/CompletionException.html#) Exception thrown when an error or other exception is encountered in the course of completing a result or task.
[ConcurrentModificationException](https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException.html#) This exception may be thrown by methods that have detected concurrent modification of an object when such modification is not permissible.
[ConnectException](https://developer.android.com/reference/kotlin/java/net/ConnectException.html#) Signals that an error occurred while attempting to connect a socket to a remote address and port.
[ConnectTimeoutException](https://developer.android.com/reference/kotlin/org/apache/http/conn/ConnectTimeoutException.html#) A timeout while connecting to an HTTP server or waiting for an available connection from an HttpConnectionManager.
[ConnectionPendingException](https://developer.android.com/reference/kotlin/java/nio/channels/ConnectionPendingException.html#) Unchecked exception thrown when an attempt is made to connect a `https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel.html#` for which a non-blocking connection operation is already in progress.
[CursorIndexOutOfBoundsException](https://developer.android.com/reference/kotlin/android/database/CursorIndexOutOfBoundsException.html#) An exception indicating that a cursor is out of bounds.
[CursorWindowAllocationException](https://developer.android.com/reference/kotlin/android/database/CursorWindowAllocationException.html#) This exception is thrown when a CursorWindow couldn't be allocated, most probably due to memory not being available.
[DOMException](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMException.html#) DOM operations only raise exceptions in "exceptional" circumstances, i.
[DataTruncation](https://developer.android.com/reference/kotlin/java/sql/DataTruncation.html#) An exception thrown as a `DataTruncation` exception (on writes) or reported as a `DataTruncation` warning (on reads) when a data values is unexpectedly truncated for reasons other than its having execeeded `MaxFieldSize`.
[DateTimeException](https://developer.android.com/reference/kotlin/java/time/DateTimeException.html#) Exception used to indicate a problem while calculating a date-time.
[DateTimeParseException](https://developer.android.com/reference/kotlin/java/time/format/DateTimeParseException.html#) An exception thrown when an error occurs during parsing.
[DeadObjectException](https://developer.android.com/reference/kotlin/android/os/DeadObjectException.html#) The object you are calling has died, because its hosting process no longer exists, or there has been a low-level binder error.
[DeadSystemException](https://developer.android.com/reference/kotlin/android/os/DeadSystemException.html#) The core Android system has died and is going through a runtime restart.
[DeniedByServerException](https://developer.android.com/reference/kotlin/android/media/DeniedByServerException.html#) Exception thrown when the provisioning server or key server denies a certficate or license for a device.
[DeviceNotAssociatedException](https://developer.android.com/reference/kotlin/android/companion/DeviceNotAssociatedException.html#) An exception for a case when a given device was not android.
[DigestException](https://developer.android.com/reference/kotlin/java/security/DigestException.html#) This is the generic Message Digest exception.
[DirectoryIteratorException](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryIteratorException.html#) Runtime exception thrown if an I/O error is encountered when iterating over the entries in a directory.
[DirectoryNotEmptyException](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryNotEmptyException.html#) Checked exception thrown when a file system operation fails because a directory is not empty.
[DocTypeNotSupportedException](https://developer.android.com/reference/kotlin/android/security/identity/DocTypeNotSupportedException.html#) Thrown if trying to create a credential with an unsupported document type.
[DuplicateFormatFlagsException](https://developer.android.com/reference/kotlin/java/util/DuplicateFormatFlagsException.html#) Unchecked exception thrown when duplicate flags are provided in the format specifier.
[EOFException](https://developer.android.com/reference/kotlin/java/io/EOFException.html#) Signals that an end of file or end of stream has been reached unexpectedly during input.
[EchConfigMismatchException](https://developer.android.com/reference/kotlin/android/net/ssl/EchConfigMismatchException.html#) Exception thrown when the provided ECH (Encrypted Client Hello) config does not match the server.
[EmptyStackException](https://developer.android.com/reference/kotlin/java/util/EmptyStackException.html#) Thrown by methods in the `Stack` class to indicate that the stack is empty.
[EnumConstantNotPresentException](https://developer.android.com/reference/kotlin/java/lang/EnumConstantNotPresentException) Thrown when an application tries to access an enum constant by name and the enum type contains no constant with the specified name.
[EphemeralPublicKeyNotFoundException](https://developer.android.com/reference/kotlin/android/security/identity/EphemeralPublicKeyNotFoundException.html#) Thrown if the ephemeral public key was not found in the session transcript passed to `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredential.html#getEntries(kotlin.ByteArray,%20kotlin.collections.MutableMap,%20kotlin.ByteArray,%20kotlin.ByteArray)`.
[ExemptionMechanismException](https://developer.android.com/reference/kotlin/javax/crypto/ExemptionMechanismException.html#) This is the generic ExemptionMechanism exception.
[FileAlreadyExistsException](https://developer.android.com/reference/kotlin/java/nio/file/FileAlreadyExistsException.html#) Checked exception thrown when an attempt is made to create a file or directory and a file of that name already exists.
[FileLockInterruptionException](https://developer.android.com/reference/kotlin/java/nio/channels/FileLockInterruptionException.html#) Checked exception received by a thread when another thread interrupts it while it is waiting to acquire a file lock.
[FileNotFoundException](https://developer.android.com/reference/kotlin/java/io/FileNotFoundException.html#) Signals that an attempt to open the file denoted by a specified pathname has failed.
[FileSystemAlreadyExistsException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemAlreadyExistsException.html#) Runtime exception thrown when an attempt is made to create a file system that already exists.
[FileSystemException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException.html#) Thrown when a file system operation fails on one or two files.
[FileSystemLoopException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemLoopException.html#) Checked exception thrown when a file system loop, or cycle, is encountered.
[FileSystemNotFoundException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemNotFoundException.html#) Runtime exception thrown when a file system cannot be found.
[FileUriExposedException](https://developer.android.com/reference/kotlin/android/os/FileUriExposedException.html#) The exception that may be thrown when an application exposes a `file://` `https://developer.android.com/reference/kotlin/android/net/Uri.html#` to another app.
[ForegroundServiceStartNotAllowedException](https://developer.android.com/reference/kotlin/android/app/ForegroundServiceStartNotAllowedException.html#) Exception thrown when an app tries to start a foreground `https://developer.android.com/reference/kotlin/android/app/Service.html#` when it's not allowed to do so.
[ForegroundServiceTypeException](https://developer.android.com/reference/kotlin/android/app/ForegroundServiceTypeException.html#) Base exception thrown when an app tries to start a foreground `https://developer.android.com/reference/kotlin/android/app/Service.html#` without a valid type.
[FormatFlagsConversionMismatchException](https://developer.android.com/reference/kotlin/java/util/FormatFlagsConversionMismatchException.html#) Unchecked exception thrown when a conversion and flag are incompatible.
[FormatterClosedException](https://developer.android.com/reference/kotlin/java/util/FormatterClosedException.html#) Unchecked exception thrown when the formatter has been closed.
[Fragment.InstantiationException](https://developer.android.com/reference/kotlin/android/app/Fragment.InstantiationException.html#) Thrown by `https://developer.android.com/reference/kotlin/android/app/Fragment.html#instantiate(android.content.Context,%20kotlin.String,%20android.os.Bundle)` when there is an instantiation failure.
[GLException](https://developer.android.com/reference/kotlin/android/opengl/GLException.html#) An exception class for OpenGL errors.
[HealthConnectException](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectException.html#) Class representing health connect exceptions.
[HttpException](https://developer.android.com/reference/kotlin/android/net/http/HttpException.html#) Base exception passed to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback.html#onFailed(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)`.
[HttpRetryException](https://developer.android.com/reference/kotlin/java/net/HttpRetryException.html#) Thrown to indicate that a HTTP request needs to be retried but cannot be retried automatically, due to streaming mode being enabled.
[ICUUncheckedIOException](https://developer.android.com/reference/kotlin/android/icu/util/ICUUncheckedIOException.html#) Unchecked version of `https://developer.android.com/reference/kotlin/java/io/IOException.html#`.
[IkeIOException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeIOException.html#) Wrapper for I/O exceptions encountered during IKE operations.
[IkeInternalException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeInternalException.html#) IkeInternalException encapsulates all local implementation or resource related exceptions.
[IkeNetworkLostException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeNetworkLostException.html#) IkeNetworkLostException is returned to the caller via `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback.html#onError(android.net.ipsec.ike.exceptions.IkeException)` if the underlying Network for the `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession.html#` was lost with no alternatives.
[IkeNonProtocolException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeNonProtocolException.html#) IkeNonProtocolException encapsulates all implementation-specific non-protocol IKE errors.
[IkeProtocolException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeProtocolException.html#) IkeProtocolException is an abstract class that represents the common information for all IKE protocol errors.
[IkeTimeoutException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeTimeoutException.html#) This exception is thrown when there is an IKE retransmission timeout.
[IllegalAccessException](https://developer.android.com/reference/kotlin/java/lang/IllegalAccessException) An IllegalAccessException is thrown when an application tries to reflectively create an instance (other than an array), set or get a field, or invoke a method, but the currently executing method does not have access to the definition of the specified class, field, method or constructor.
[IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException) Thrown to indicate that a method has been passed an illegal or inappropriate argument.
[IllegalBlockSizeException](https://developer.android.com/reference/kotlin/javax/crypto/IllegalBlockSizeException.html#) This exception is thrown when the length of data provided to a block cipher is incorrect, i.
[IllegalBlockingModeException](https://developer.android.com/reference/kotlin/java/nio/channels/IllegalBlockingModeException.html#) Unchecked exception thrown when a blocking-mode-specific operation is invoked upon a channel in the incorrect blocking mode.
[IllegalCallerException](https://developer.android.com/reference/kotlin/java/lang/IllegalCallerException) Thrown to indicate that a method has been called by an inappropriate caller.
[IllegalChannelGroupException](https://developer.android.com/reference/kotlin/java/nio/channels/IllegalChannelGroupException.html#) Unchecked exception thrown when an attempt is made to open a channel in a group that was not created by the same provider.
[IllegalCharsetNameException](https://developer.android.com/reference/kotlin/java/nio/charset/IllegalCharsetNameException.html#) Unchecked exception thrown when a string that is not a [legal charset name](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#names) is used as such.
[IllegalFormatCodePointException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatCodePointException.html#) Unchecked exception thrown when a character with an invalid Unicode code point as defined by `https://developer.android.com/reference/kotlin/java/lang/Character#isValidCodePoint(kotlin.Int)` is passed to the `https://developer.android.com/reference/kotlin/java/util/Formatter.html#`.
[IllegalFormatConversionException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatConversionException.html#) Unchecked exception thrown when the argument corresponding to the format specifier is of an incompatible type.
[IllegalFormatException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatException.html#) Unchecked exception thrown when a format string contains an illegal syntax or a format specifier that is incompatible with the given arguments.
[IllegalFormatFlagsException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatFlagsException.html#) Unchecked exception thrown when an illegal combination flags is given.
[IllegalFormatPrecisionException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatPrecisionException.html#) Unchecked exception thrown when the precision is a negative value other than `-1`, the conversion does not support a precision, or the value is otherwise unsupported.
[IllegalFormatWidthException](https://developer.android.com/reference/kotlin/java/util/IllegalFormatWidthException.html#) Unchecked exception thrown when the format width is a negative value other than `-1` or is otherwise unsupported.
[IllegalMonitorStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalMonitorStateException) Thrown to indicate that a thread has attempted to wait on an object's monitor or to notify other threads waiting on an object's monitor without owning the specified monitor.
[IllegalSelectorException](https://developer.android.com/reference/kotlin/java/nio/channels/IllegalSelectorException.html#) Unchecked exception thrown when an attempt is made to register a channel with a selector that was not created by the provider that created the channel.
[IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException) Signals that a method has been invoked at an illegal or inappropriate time.
[IllegalThreadStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalThreadStateException) Thrown to indicate that a thread is not in an appropriate state for the requested operation.
[IllformedLocaleException](https://developer.android.com/reference/kotlin/java/util/IllformedLocaleException.html#) Thrown by methods in `https://developer.android.com/reference/kotlin/java/util/Locale.html#` and `https://developer.android.com/reference/kotlin/java/util/Locale.Builder.html#` to indicate that an argument is not a well-formed BCP 47 tag.
[IllformedLocaleException](https://developer.android.com/reference/kotlin/android/icu/util/IllformedLocaleException.html#) Thrown by methods in `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#` and `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Builder.html#` to indicate that an argument is not a well-formed BCP 47 tag.
[ImageDecoder.DecodeException](https://developer.android.com/reference/kotlin/android/graphics/ImageDecoder.DecodeException.html#) Information about an interrupted decode.
[IncompleteAnnotationException](https://developer.android.com/reference/kotlin/java/lang/annotation/IncompleteAnnotationException) Thrown to indicate that a program has attempted to access an element of an annotation interface that was added to the annotation interface definition after the annotation was compiled (or serialized).
[IndexOutOfBoundsException](https://developer.android.com/reference/kotlin/java/lang/IndexOutOfBoundsException) Thrown to indicate that an index of some sort (such as to an array, to a string, or to a vector) is out of range.
[InfeasibleActivityOptionsException](https://developer.android.com/reference/kotlin/android/app/InfeasibleActivityOptionsException.html#) This exception is thrown when a call to android.
[InflateException](https://developer.android.com/reference/kotlin/android/view/InflateException.html#) This exception is thrown by an inflater on error conditions.
[InlineExecutionProhibitedException](https://developer.android.com/reference/kotlin/android/net/http/InlineExecutionProhibitedException.html#) Thrown when an executor runs a submitted runnable inline in `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#execute(java.lang.Runnable)` and `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder.html#setDirectExecutorAllowed(kotlin.Boolean)` was not called.
[InputMismatchException](https://developer.android.com/reference/kotlin/java/util/InputMismatchException.html#) Thrown by a `Scanner` to indicate that the token retrieved does not match the pattern for the expected type, or that the token is out of range for the expected type.
[InspectionCompanion.UninitializedPropertyMapException](https://developer.android.com/reference/kotlin/android/view/inspector/InspectionCompanion.UninitializedPropertyMapException.html#) Thrown by `https://developer.android.com/reference/kotlin/android/view/inspector/InspectionCompanion.html#readProperties(android.view.inspector.InspectionCompanion.T,%20android.view.inspector.PropertyReader)` if called before `https://developer.android.com/reference/kotlin/android/view/inspector/InspectionCompanion.html#mapProperties(android.view.inspector.PropertyMapper)`.
[InstantiationException](https://developer.android.com/reference/kotlin/java/lang/InstantiationException) Thrown when an application tries to create an instance of a class using the `newInstance` method in class `Class`, but the specified class object cannot be instantiated.
[IntentFilter.MalformedMimeTypeException](https://developer.android.com/reference/kotlin/android/content/IntentFilter.MalformedMimeTypeException.html#) This exception is thrown when a given MIME type does not have a valid syntax.
[IntentSender.SendIntentException](https://developer.android.com/reference/kotlin/android/content/IntentSender.SendIntentException.html#) Exception thrown when trying to send through a PendingIntent that has been canceled or is otherwise no longer able to execute the request.
[InterruptedByTimeoutException](https://developer.android.com/reference/kotlin/java/nio/channels/InterruptedByTimeoutException.html#) Checked exception received by a thread when a timeout elapses before an asynchronous operation completes.
[InterruptedIOException](https://developer.android.com/reference/kotlin/java/io/InterruptedIOException.html#) Signals that an I/O operation has been interrupted.
[InvalidAlgorithmParameterException](https://developer.android.com/reference/kotlin/java/security/InvalidAlgorithmParameterException.html#) This is the exception for invalid or inappropriate algorithm parameters.
[InvalidClassException](https://developer.android.com/reference/kotlin/java/io/InvalidClassException.html#) Thrown when the Serialization runtime detects one of the following problems with a Class.
[InvalidEchDataException](https://developer.android.com/reference/kotlin/android/net/ssl/InvalidEchDataException.html#) Exception thrown when the ECH (Encrypted Client Hello) data is empty or invalid.
[InvalidForegroundServiceTypeException](https://developer.android.com/reference/kotlin/android/app/InvalidForegroundServiceTypeException.html#) Exception thrown when an app tries to start a foreground `https://developer.android.com/reference/kotlin/android/app/Service.html#` with an invalid type.
[InvalidKeException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/InvalidKeException.html#) This exception is thrown when the remote server expected a different Diffie-Hellman group.
[InvalidKeyException](https://developer.android.com/reference/kotlin/java/security/InvalidKeyException.html#) This is the exception for invalid Keys (invalid encoding, wrong length, uninitialized, etc).
[InvalidKeySpecException](https://developer.android.com/reference/kotlin/java/security/spec/InvalidKeySpecException.html#) This is the exception for invalid key specifications.
[InvalidMajorVersionException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/InvalidMajorVersionException.html#) This exception is thrown when major version of an inbound message is higher than 2.
[InvalidMarkException](https://developer.android.com/reference/kotlin/java/nio/InvalidMarkException.html#) Unchecked exception thrown when an attempt is made to reset a buffer when its mark is not defined.
[InvalidObjectException](https://developer.android.com/reference/kotlin/java/io/InvalidObjectException.html#) Indicates that one or more deserialized objects failed validation tests.
[InvalidParameterException](https://developer.android.com/reference/kotlin/java/security/InvalidParameterException.html#) This exception, designed for use by the JCA/JCE engine classes, is thrown when an invalid parameter is passed to a method.
[InvalidParameterSpecException](https://developer.android.com/reference/kotlin/java/security/spec/InvalidParameterSpecException.html#) This is the exception for invalid parameter specifications.
[InvalidPathException](https://developer.android.com/reference/kotlin/java/nio/file/InvalidPathException.html#) Unchecked exception thrown when path string cannot be converted into a `https://developer.android.com/reference/kotlin/java/nio/file/Path.html#` because the path string contains invalid characters, or the path string is invalid for other file system specific reasons.
[InvalidPropertiesFormatException](https://developer.android.com/reference/kotlin/java/util/InvalidPropertiesFormatException.html#) Thrown to indicate that an operation could not complete because the input did not conform to the appropriate XML document type for a collection of properties, as per the `https://developer.android.com/reference/kotlin/java/util/Properties.html#` specification.
[InvalidReaderSignatureException](https://developer.android.com/reference/kotlin/android/security/identity/InvalidReaderSignatureException.html#) Thrown if the reader signature is invalid, or it doesn't contain a certificate chain, or if the signature failed to validate.
[InvalidRequestMessageException](https://developer.android.com/reference/kotlin/android/security/identity/InvalidRequestMessageException.html#) Thrown if message with the request doesn't satisfy the requirements documented in `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredential.html#getEntries(kotlin.ByteArray,%20kotlin.collections.MutableMap,%20kotlin.ByteArray,%20kotlin.ByteArray)`.
[InvalidSelectorsException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/InvalidSelectorsException.html#) This exception is thrown if the remote server received an IPsec packet with mismatched selectors.
[InvocationTargetException](https://developer.android.com/reference/kotlin/java/lang/reflect/InvocationTargetException) InvocationTargetException is a checked exception that wraps an exception thrown by an invoked method or constructor.
[IpSecManager.ResourceUnavailableException](https://developer.android.com/reference/kotlin/android/net/IpSecManager.ResourceUnavailableException.html#) Thrown to indicate that an IPsec resource is unavailable.
[IpSecManager.SpiUnavailableException](https://developer.android.com/reference/kotlin/android/net/IpSecManager.SpiUnavailableException.html#) Thrown to indicate that a requested SPI is in use.
[JarException](https://developer.android.com/reference/kotlin/java/util/jar/JarException.html#) Signals that an error of some sort has occurred while reading from or writing to a JAR file.
[KeyCharacterMap.UnavailableException](https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap.UnavailableException.html#) Thrown by `https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap.html#load(kotlin.Int)` when a key character map could not be loaded.
[KeyException](https://developer.android.com/reference/kotlin/java/security/KeyException.html#) This is the basic key exception.
[KeyExpiredException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyExpiredException.html#) Indicates that a cryptographic operation failed because the employed key's validity end date is in the past.
[KeyManagementException](https://developer.android.com/reference/kotlin/java/security/KeyManagementException.html#) This is the general key management exception for all operations dealing with key management.
[KeyNotYetValidException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyNotYetValidException.html#) Indicates that a cryptographic operation failed because the employed key's validity start date is in the future.
[KeyPermanentlyInvalidatedException](https://developer.android.com/reference/kotlin/android/security/keystore/KeyPermanentlyInvalidatedException.html#) Indicates that the key can no longer be used because it has been permanently invalidated.
[KeyStoreException](https://developer.android.com/reference/kotlin/java/security/KeyStoreException.html#) This is the generic KeyStore exception.
[LSException](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSException.html#) Parser or write operations may throw an `LSException` if the processing is stopped.
[LimitExceededException](https://developer.android.com/reference/kotlin/android/os/LimitExceededException.html#) Indicates that the app has exceeded a limit set by the System.
[LoginException](https://developer.android.com/reference/kotlin/javax/security/auth/login/LoginException.html#) This is the basic login exception.
[MalformedInputException](https://developer.android.com/reference/kotlin/java/nio/charset/MalformedInputException.html#) Checked exception thrown when an input byte sequence is not legal for given charset, or an input character sequence is not a legal sixteen-bit Unicode sequence.
[MalformedJsonException](https://developer.android.com/reference/kotlin/android/util/MalformedJsonException.html#) Thrown when a reader encounters malformed JSON.
[MalformedParameterizedTypeException](https://developer.android.com/reference/kotlin/java/lang/reflect/MalformedParameterizedTypeException) Thrown when a semantically malformed parameterized type is encountered by a reflective method that needs to instantiate it.
[MalformedParametersException](https://developer.android.com/reference/kotlin/java/lang/reflect/MalformedParametersException) Thrown when `https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#getParameters()` attempts to read method parameters from a class file and determines that one or more parameters are malformed.
[MalformedURLException](https://developer.android.com/reference/kotlin/java/net/MalformedURLException.html#) Thrown to indicate that a malformed URL has occurred.
[MatchException](https://developer.android.com/reference/kotlin/java/lang/MatchException) Thrown to indicate an unexpected failure in pattern matching.
[MediaCasException.DeniedByServerException](https://developer.android.com/reference/kotlin/android/media/MediaCasException.DeniedByServerException.html#) Exception thrown when the provisioning server or key server denies a license for a device.
[MediaCasException.InsufficientResourceException](https://developer.android.com/reference/kotlin/android/media/MediaCasException.InsufficientResourceException.html#) Exception thrown when an operation on a MediaCas object is attempted and hardware resources are not sufficient to allocate, due to client's lower priority.
[MediaCasException.NotProvisionedException](https://developer.android.com/reference/kotlin/android/media/MediaCasException.NotProvisionedException.html#) Exception thrown when an operation on a MediaCas object is attempted before it's provisioned successfully.
[MediaCasException.ResourceBusyException](https://developer.android.com/reference/kotlin/android/media/MediaCasException.ResourceBusyException.html#) Exception thrown when an operation on a MediaCas object is attempted and hardware resources are not available, due to being in use.
[MediaCasException.UnsupportedCasException](https://developer.android.com/reference/kotlin/android/media/MediaCasException.UnsupportedCasException.html#) Exception thrown when an attempt is made to construct a MediaCas object using a CA_system_id that is not supported by the device
[MediaCasStateException](https://developer.android.com/reference/kotlin/android/media/MediaCasStateException.html#) Base class for MediaCas runtime exceptions
[MediaCodec.CodecException](https://developer.android.com/reference/kotlin/android/media/MediaCodec.CodecException.html#) Thrown when an internal codec error occurs.
[MediaCodec.CryptoException](https://developer.android.com/reference/kotlin/android/media/MediaCodec.CryptoException.html#) Thrown when a crypto error occurs while queueing a secure input buffer.
[MediaCodec.IncompatibleWithBlockModelException](https://developer.android.com/reference/kotlin/android/media/MediaCodec.IncompatibleWithBlockModelException.html#) Thrown when the codec is configured for block model and an incompatible API is called.
[MediaCodec.InvalidBufferFlagsException](https://developer.android.com/reference/kotlin/android/media/MediaCodec.InvalidBufferFlagsException.html#) Thrown when a buffer is marked with an invalid combination of flags (e.g. both
[MediaDrm.MediaDrmStateException](https://developer.android.com/reference/kotlin/android/media/MediaDrm.MediaDrmStateException.html#) Thrown when a general failure occurs during a MediaDrm operation.
[MediaDrm.SessionException](https://developer.android.com/reference/kotlin/android/media/MediaDrm.SessionException.html#) `https://developer.android.com/reference/kotlin/android/media/MediaDrm.SessionException.html#` is a misnomer because it may occur in methods **without** a session context.
[MediaDrmResetException](https://developer.android.com/reference/kotlin/android/media/MediaDrmResetException.html#) This exception is thrown when the MediaDrm instance has become unusable due to a restart of the mediaserver process.
[MediaParser.ParsingException](https://developer.android.com/reference/kotlin/android/media/MediaParser.ParsingException.html#) Thrown when an error occurs while parsing a media stream.
[MediaParser.UnrecognizedInputFormatException](https://developer.android.com/reference/kotlin/android/media/MediaParser.UnrecognizedInputFormatException.html#) Thrown if all parser implementations provided to `https://developer.android.com/reference/kotlin/android/media/MediaParser.html#create(android.media.MediaParser.OutputConsumer,%20kotlin.String)` failed to sniff the input content.
[MediaPlayer.NoDrmSchemeException](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.NoDrmSchemeException.html#) Thrown when a DRM method is called before preparing a DRM scheme through prepareDrm().
[MediaPlayer.ProvisioningNetworkErrorException](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.ProvisioningNetworkErrorException.html#) Thrown when the device requires DRM provisioning but the provisioning attempt has failed due to a network error (Internet reachability, timeout, etc.).
[MediaPlayer.ProvisioningServerErrorException](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.ProvisioningServerErrorException.html#) Thrown when the device requires DRM provisioning but the provisioning attempt has failed due to the provisioning server denying the request.
[MessageDecryptionException](https://developer.android.com/reference/kotlin/android/security/identity/MessageDecryptionException.html#) Thrown when failing to decrypt a message from the reader device.
[MissingForegroundServiceTypeException](https://developer.android.com/reference/kotlin/android/app/MissingForegroundServiceTypeException.html#) Exception thrown when an app tries to start a foreground `https://developer.android.com/reference/kotlin/android/app/Service.html#` without a type.
[MissingFormatArgumentException](https://developer.android.com/reference/kotlin/java/util/MissingFormatArgumentException.html#) Unchecked exception thrown when there is a format specifier which does not have a corresponding argument or if an argument index refers to an argument that does not exist.
[MissingFormatWidthException](https://developer.android.com/reference/kotlin/java/util/MissingFormatWidthException.html#) Unchecked exception thrown when the format width is required.
[MissingResourceException](https://developer.android.com/reference/kotlin/java/util/MissingResourceException.html#) Signals that a resource is missing.
[NegativeArraySizeException](https://developer.android.com/reference/kotlin/java/lang/NegativeArraySizeException) Thrown if an application tries to create an array with negative size.
[NetworkErrorException](https://developer.android.com/reference/kotlin/android/accounts/NetworkErrorException.html#) <br />

[NetworkException](https://developer.android.com/reference/kotlin/android/net/http/NetworkException.html#) Exception passed to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback.html#onFailed(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)` when the HTTP stack fails to process a network request.
[NetworkOnMainThreadException](https://developer.android.com/reference/kotlin/android/os/NetworkOnMainThreadException.html#) The exception that is thrown when an application attempts to perform a networking operation on its main thread.
[NoAuthenticationKeyAvailableException](https://developer.android.com/reference/kotlin/android/security/identity/NoAuthenticationKeyAvailableException.html#) Thrown if no dynamic authentication keys are available.
[NoConnectionPendingException](https://developer.android.com/reference/kotlin/java/nio/channels/NoConnectionPendingException.html#) Unchecked exception thrown when the `https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel.html#finishConnect()` method of a `https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel.html#` is invoked without first successfully invoking its `https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel.html#connect(java.net.SocketAddress)` method.
[NoRouteToHostException](https://developer.android.com/reference/kotlin/java/net/NoRouteToHostException.html#) Signals that an error occurred while attempting to connect a socket to a remote address and port.
[NoSuchAlgorithmException](https://developer.android.com/reference/kotlin/java/security/NoSuchAlgorithmException.html#) This exception is thrown when a particular cryptographic algorithm is requested but is not available in the environment.
[NoSuchElementException](https://developer.android.com/reference/kotlin/java/util/NoSuchElementException.html#) Thrown by various accessor methods to indicate that the element being requested does not exist.
[NoSuchFieldException](https://developer.android.com/reference/kotlin/java/lang/NoSuchFieldException) Signals that the class doesn't have a field of a specified name.
[NoSuchFileException](https://developer.android.com/reference/kotlin/java/nio/file/NoSuchFileException.html#) Checked exception thrown when an attempt is made to access a file that does not exist.
[NoSuchMethodException](https://developer.android.com/reference/kotlin/java/lang/NoSuchMethodException) Thrown when a particular method cannot be found.
[NoSuchPaddingException](https://developer.android.com/reference/kotlin/javax/crypto/NoSuchPaddingException.html#) This exception is thrown when a particular padding mechanism is requested but is not available in the environment.
[NoSuchPropertyException](https://developer.android.com/reference/kotlin/android/util/NoSuchPropertyException.html#) Thrown when code requests a `https://developer.android.com/reference/kotlin/android/util/Property.html#` on a class that does not expose the appropriate method or field.
[NoSuchProviderException](https://developer.android.com/reference/kotlin/java/security/NoSuchProviderException.html#) This exception is thrown when a particular security provider is requested but is not available in the environment.
[NonReadableChannelException](https://developer.android.com/reference/kotlin/java/nio/channels/NonReadableChannelException.html#) Unchecked exception thrown when an attempt is made to read from a channel that was not originally opened for reading.
[NonWritableChannelException](https://developer.android.com/reference/kotlin/java/nio/channels/NonWritableChannelException.html#) Unchecked exception thrown when an attempt is made to write to a channel that was not originally opened for writing.
[NotActiveException](https://developer.android.com/reference/kotlin/java/io/NotActiveException.html#) Thrown when serialization or deserialization is not active.
[NotDirectoryException](https://developer.android.com/reference/kotlin/java/nio/file/NotDirectoryException.html#) Checked exception thrown when a file system operation, intended for a directory, fails because the file is not a directory.
[NotLinkException](https://developer.android.com/reference/kotlin/java/nio/file/NotLinkException.html#) Checked exception thrown when a file system operation fails because a file is not a symbolic link.
[NotProvisionedException](https://developer.android.com/reference/kotlin/android/media/NotProvisionedException.html#) Exception thrown when an operation on a MediaDrm object is attempted and the device does not have a certificate.
[NotSerializableException](https://developer.android.com/reference/kotlin/java/io/NotSerializableException.html#) Thrown when an instance is required to have a Serializable interface.
[NotYetBoundException](https://developer.android.com/reference/kotlin/java/nio/channels/NotYetBoundException.html#) Unchecked exception thrown when an attempt is made to invoke an I/O operation upon a server socket channel that is not yet bound.
[NotYetConnectedException](https://developer.android.com/reference/kotlin/java/nio/channels/NotYetConnectedException.html#) Unchecked exception thrown when an attempt is made to invoke an I/O operation upon a socket channel that is not yet connected.
[NullPointerException](https://developer.android.com/reference/kotlin/java/lang/NullPointerException) Thrown when an application attempts to use `null` in a case where an object is required.
[NumberFormatException](https://developer.android.com/reference/kotlin/java/lang/NumberFormatException) Thrown to indicate that the application has attempted to convert a string to one of the numeric types, but that the string does not have the appropriate format.
[ObjectStreamException](https://developer.android.com/reference/kotlin/java/io/ObjectStreamException.html#) Superclass of all exceptions specific to Object Stream classes.
[OperationCanceledException](https://developer.android.com/reference/kotlin/android/os/OperationCanceledException.html#) An exception type that is thrown when an operation in progress is canceled.
[OperationCanceledException](https://developer.android.com/reference/kotlin/android/accounts/OperationCanceledException.html#) <br />

[OptionalDataException](https://developer.android.com/reference/kotlin/java/io/OptionalDataException.html#) Exception indicating the failure of an object read operation due to unread primitive data, or the end of data belonging to a serialized object in the stream.
[OverlappingFileLockException](https://developer.android.com/reference/kotlin/java/nio/channels/OverlappingFileLockException.html#) Unchecked exception thrown when an attempt is made to acquire a lock on a region of a file that overlaps a region already locked by the same Java virtual machine, or when another thread is already waiting to lock an overlapping region of the same file.
[PackageManager.NameNotFoundException](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.NameNotFoundException.html#) This exception is thrown when a given package, application, or component name cannot be found.
[ParcelFileDescriptor.FileDescriptorDetachedException](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.FileDescriptorDetachedException.html#) Exception that indicates that the file descriptor was detached.
[ParcelFormatException](https://developer.android.com/reference/kotlin/android/os/ParcelFormatException.html#) The contents of a Parcel (usually during unmarshalling) does not contain the expected data.
[ParseException](https://developer.android.com/reference/kotlin/android/net/ParseException.html#) Thrown when parsing failed.
[PatternSyntaxException](https://developer.android.com/reference/kotlin/java/util/regex/PatternSyntaxException.html#) Unchecked exception thrown to indicate a syntax error in a regular-expression pattern.
[PendingIntent.CanceledException](https://developer.android.com/reference/kotlin/android/app/PendingIntent.CanceledException.html#) Exception thrown when trying to send through a PendingIntent that has been canceled or is otherwise no longer able to execute the request.
[PortUnreachableException](https://developer.android.com/reference/kotlin/java/net/PortUnreachableException.html#) Signals that an ICMP Port Unreachable message has been received on a connected datagram.
[PropertyMapper.PropertyConflictException](https://developer.android.com/reference/kotlin/android/view/inspector/PropertyMapper.PropertyConflictException.html#) Thrown from a map method if a property name is already mapped as different type.
[PropertyReader.PropertyTypeMismatchException](https://developer.android.com/reference/kotlin/android/view/inspector/PropertyReader.PropertyTypeMismatchException.html#) Thrown if a client calls a typed read method for a property of a different type.
[ProtocolException](https://developer.android.com/reference/kotlin/java/net/ProtocolException.html#) Thrown to indicate that there is an error in the underlying protocol, such as a TCP error.
[ProviderException](https://developer.android.com/reference/kotlin/java/security/ProviderException.html#) A runtime exception for Provider exceptions (such as misconfiguration errors or unrecoverable internal errors), which may be subclassed by Providers to throw specialized, provider-specific runtime errors.
[ProviderMismatchException](https://developer.android.com/reference/kotlin/java/nio/file/ProviderMismatchException.html#) Unchecked exception thrown when an attempt is made to invoke a method on an object created by one file system provider with a parameter created by a different file system provider.
[ProviderNotFoundException](https://developer.android.com/reference/kotlin/java/nio/file/ProviderNotFoundException.html#) Runtime exception thrown when a provider of the required type cannot be found.
[QueryLocationException](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException.html#) This class represents a set of exceptions that can occur when requesting a `https://developer.android.com/reference/kotlin/android/telecom/Connection.html#queryLocationForEmergency(kotlin.Long,%20kotlin.String,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`
[QuicException](https://developer.android.com/reference/kotlin/android/net/http/QuicException.html#) Subclass of `https://developer.android.com/reference/kotlin/android/net/http/NetworkException.html#` which contains a detailed [QUIC](https://www.chromium.org/quic) error code from [QuicErrorCode](https://cs.chromium.org/search/?q=symbol:%5CbQuicErrorCode%5Cb).
[RSDriverException](https://developer.android.com/reference/kotlin/android/renderscript/RSDriverException.html#) Base class for all exceptions thrown by the Android RenderScript
[RSIllegalArgumentException](https://developer.android.com/reference/kotlin/android/renderscript/RSIllegalArgumentException.html#) Base class for all exceptions thrown by the Android RenderScript
[RSInvalidStateException](https://developer.android.com/reference/kotlin/android/renderscript/RSInvalidStateException.html#) Base class for all exceptions thrown by the Android RenderScript
[RSRuntimeException](https://developer.android.com/reference/kotlin/android/renderscript/RSRuntimeException.html#) Base class for all exceptions thrown by the Android RenderScript
[ReadOnlyBufferException](https://developer.android.com/reference/kotlin/java/nio/ReadOnlyBufferException.html#) Unchecked exception thrown when a content-mutation method such as put or compact is invoked upon a read-only buffer.
[ReadOnlyFileSystemException](https://developer.android.com/reference/kotlin/java/nio/file/ReadOnlyFileSystemException.html#) Unchecked exception thrown when an attempt is made to update an object associated with a `https://developer.android.com/reference/kotlin/java/nio/file/FileSystem.html#isReadOnly()` `FileSystem`.
[ReadPendingException](https://developer.android.com/reference/kotlin/java/nio/channels/ReadPendingException.html#) Unchecked exception thrown when an attempt is made to read from an asynchronous socket channel and a previous read has not completed.
[ReceiverCallNotAllowedException](https://developer.android.com/reference/kotlin/android/content/ReceiverCallNotAllowedException.html#) This exception is thrown from android.
[RecoverableSecurityException](https://developer.android.com/reference/kotlin/android/app/RecoverableSecurityException.html#) Specialization of `https://developer.android.com/reference/kotlin/java/lang/SecurityException` that contains additional information about how to involve the end user to recover from the exception.
[RejectedExecutionException](https://developer.android.com/reference/kotlin/java/util/concurrent/RejectedExecutionException.html#) Exception thrown by an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` when a task cannot be accepted for execution.
[RemoteException](https://developer.android.com/reference/kotlin/android/os/RemoteException.html#) Parent exception for all Binder remote-invocation errors Note: not all exceptions from binder services will be subclasses of this.
[RemoteViews.ActionException](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.ActionException.html#) Exception to send when something goes wrong executing an action
[ResourceBusyException](https://developer.android.com/reference/kotlin/android/media/ResourceBusyException.html#) Exception thrown when an operation on a MediaDrm object is attempted and hardware resources are not available, due to being in use.
[Resources.NotFoundException](https://developer.android.com/reference/kotlin/android/content/res/Resources.NotFoundException.html#) This exception is thrown by the resource APIs when a requested resource can not be found.
[SAXNotRecognizedException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXNotRecognizedException.html#) Exception class for an unrecognized identifier.
[SAXNotSupportedException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXNotSupportedException.html#) Exception class for an unsupported operation.
[SAXParseException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXParseException.html#) Encapsulate an XML parse error or warning.
[SQLClientInfoException](https://developer.android.com/reference/kotlin/java/sql/SQLClientInfoException.html#) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` is thrown when one or more client info properties could not be set on a `Connection`.
[SQLDataException](https://developer.android.com/reference/kotlin/java/sql/SQLDataException.html#) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` thrown when the SQLState class value is '*22*', or under vendor-specified conditions.
[SQLException](https://developer.android.com/reference/kotlin/android/database/SQLException.html#) An exception that indicates there was an error with SQL parsing or execution.
[SQLFeatureNotSupportedException](https://developer.android.com/reference/kotlin/java/sql/SQLFeatureNotSupportedException.html#) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` thrown when the SQLState class value is '*0A*' ( the value is 'zero' A).
[SQLIntegrityConstraintViolationException](https://developer.android.com/reference/kotlin/java/sql/SQLIntegrityConstraintViolationException.html#) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` thrown when the SQLState class value is '*23*', or under vendor-specified conditions.
[SQLInvalidAuthorizationSpecException](https://developer.android.com/reference/kotlin/java/sql/SQLInvalidAuthorizationSpecException.html#) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` thrown when the SQLState class value is '*28*', or under vendor-specified conditions.
[SQLNonTransientConnectionException](https://developer.android.com/reference/kotlin/java/sql/SQLNonTransientConnectionException.html#) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` thrown for the SQLState class value '*08*', or under vendor-specified conditions.
[SQLNonTransientException](https://developer.android.com/reference/kotlin/java/sql/SQLNonTransientException.html#) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` thrown when an instance where a retry of the same operation would fail unless the cause of the `SQLException` is corrected.
[SQLRecoverableException](https://developer.android.com/reference/kotlin/java/sql/SQLRecoverableException.html#) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` thrown in situations where a previously failed operation might be able to succeed if the application performs some recovery steps and retries the entire transaction or in the case of a distributed transaction, the transaction branch.
[SQLSyntaxErrorException](https://developer.android.com/reference/kotlin/java/sql/SQLSyntaxErrorException.html#) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` thrown when the SQLState class value is '*42*', or under vendor-specified conditions.
[SQLTimeoutException](https://developer.android.com/reference/kotlin/java/sql/SQLTimeoutException.html#) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` thrown when the timeout specified by `Statement` has expired.
[SQLTransactionRollbackException](https://developer.android.com/reference/kotlin/java/sql/SQLTransactionRollbackException.html#) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` thrown when the SQLState class value is '*40*', or under vendor-specified conditions.
[SQLTransientConnectionException](https://developer.android.com/reference/kotlin/java/sql/SQLTransientConnectionException.html#) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` for the SQLState class value '*08*', or under vendor-specified conditions.
[SQLTransientException](https://developer.android.com/reference/kotlin/java/sql/SQLTransientException.html#) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` is thrown in situations where a previoulsy failed operation might be able to succeed when the operation is retried without any intervention by application-level functionality.
[SQLWarning](https://developer.android.com/reference/kotlin/java/sql/SQLWarning.html#) An exception that provides information on database access warnings.
[SQLiteAbortException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteAbortException.html#) An exception that indicates that the SQLite program was aborted.
[SQLiteAccessPermException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteAccessPermException.html#) This exception class is used when sqlite can't access the database file due to lack of permissions on the file.
[SQLiteBindOrColumnIndexOutOfRangeException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteBindOrColumnIndexOutOfRangeException.html#) Thrown if the bind or column parameter index is out of range.
[SQLiteBlobTooBigException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteBlobTooBigException.html#) <br />

[SQLiteCantOpenDatabaseException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteCantOpenDatabaseException.html#) <br />

[SQLiteConstraintException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteConstraintException.html#) An exception that indicates that an integrity constraint was violated.
[SQLiteDatabaseCorruptException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabaseCorruptException.html#) An exception that indicates that the SQLite database file is corrupt.
[SQLiteDatabaseLockedException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabaseLockedException.html#) Thrown if the database engine was unable to acquire the database locks it needs to do its job.
[SQLiteDatatypeMismatchException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatatypeMismatchException.html#) <br />

[SQLiteDiskIOException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDiskIOException.html#) Indicates that an IO error occurred while accessing the SQLite database file.
[SQLiteDoneException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDoneException.html#) An exception that indicates that the SQLite program is done.
[SQLiteException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteException.html#) A SQLite exception that indicates there was an error with SQL parsing or execution.
[SQLiteFullException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteFullException.html#) An exception that indicates that the SQLite database is full.
[SQLiteMisuseException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteMisuseException.html#) This error can occur if the application creates a SQLiteStatement object and allows multiple threads in the application use it at the same time.
[SQLiteOutOfMemoryException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteOutOfMemoryException.html#) <br />

[SQLiteReadOnlyDatabaseException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteReadOnlyDatabaseException.html#) <br />

[SQLiteTableLockedException](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteTableLockedException.html#) <br />

[SSLException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLException.html#) Indicates some kind of error detected by an SSL subsystem.
[SSLHandshakeException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLHandshakeException.html#) Indicates that the client and server could not negotiate the desired level of security.
[SSLKeyException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLKeyException.html#) Reports a bad SSL key.
[SSLPeerUnverifiedException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLPeerUnverifiedException.html#) Indicates that the peer's identity has not been verified.
[SSLProtocolException](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLProtocolException.html#) Reports an error in the operation of the SSL protocol.
[SecureKeyImportUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/SecureKeyImportUnavailableException.html#) Indicates that the Keystore does not support securely importing wrapped keys.
[SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException) Thrown by the security manager to indicate a security violation.
[ServiceStartNotAllowedException](https://developer.android.com/reference/kotlin/android/app/ServiceStartNotAllowedException.html#) Exception thrown when an app tries to start a `https://developer.android.com/reference/kotlin/android/app/Service.html#` when it's not allowed to do so.
[SessionTranscriptMismatchException](https://developer.android.com/reference/kotlin/android/security/identity/SessionTranscriptMismatchException.html#) Thrown when trying use multiple different session transcripts in the same presentation session.
[Settings.SettingNotFoundException](https://developer.android.com/reference/kotlin/android/provider/Settings.SettingNotFoundException.html#) <br />

[ShortBufferException](https://developer.android.com/reference/kotlin/javax/crypto/ShortBufferException.html#) This exception is thrown when an output buffer provided by the user is too short to hold the operation result.
[ShutdownChannelGroupException](https://developer.android.com/reference/kotlin/java/nio/channels/ShutdownChannelGroupException.html#) Unchecked exception thrown when an attempt is made to construct a channel in a group that is shutdown or the completion handler for an I/O operation cannot be invoked because the channel group has terminated.
[SignatureException](https://developer.android.com/reference/kotlin/java/security/SignatureException.html#) This is the generic Signature exception.
[SkeletonSyntaxException](https://developer.android.com/reference/kotlin/android/icu/number/SkeletonSyntaxException.html#) Exception used for illegal number skeleton strings.
[SocketException](https://developer.android.com/reference/kotlin/java/net/SocketException.html#) Thrown to indicate that there is an error creating or accessing a Socket.
[SocketTimeoutException](https://developer.android.com/reference/kotlin/java/net/SocketTimeoutException.html#) Signals that a timeout has occurred on a socket read or accept.
[StaleDataException](https://developer.android.com/reference/kotlin/android/database/StaleDataException.html#) This exception is thrown when a Cursor contains stale data and must be requeried before being used again.
[StartForegroundCalledOnStoppedServiceException](https://developer.android.com/reference/kotlin/android/app/StartForegroundCalledOnStoppedServiceException.html#) Exception thrown when android.
[StreamCorruptedException](https://developer.android.com/reference/kotlin/java/io/StreamCorruptedException.html#) Thrown when control information that was read from an object stream violates internal consistency checks.
[StringIndexOutOfBoundsException](https://developer.android.com/reference/kotlin/java/lang/StringIndexOutOfBoundsException) Thrown by `String` methods to indicate that an index is either negative or greater than the size of the string.
[StringPrepParseException](https://developer.android.com/reference/kotlin/android/icu/text/StringPrepParseException.html#) Exception that signals an error has occurred while parsing the input to StringPrep or IDNA.
[StrongBoxUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/StrongBoxUnavailableException.html#) Indicates that an operation could not be performed because the requested security hardware is not available.
[Surface.OutOfResourcesException](https://developer.android.com/reference/kotlin/android/view/Surface.OutOfResourcesException.html#) Exception thrown when a Canvas couldn't be locked with `https://developer.android.com/reference/kotlin/android/view/Surface.html#lockCanvas(android.graphics.Rect)`, or when a SurfaceTexture could not successfully be allocated.
[SurfaceHolder.BadSurfaceTypeException](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.BadSurfaceTypeException.html#) Exception that is thrown from #lockCanvas when called on a Surface whose type is SURFACE_TYPE_PUSH_BUFFERS.
[SyncFailedException](https://developer.android.com/reference/kotlin/java/io/SyncFailedException.html#) Signals that a sync operation has failed.
[SystemUpdatePolicy.ValidationFailedException](https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy.ValidationFailedException.html#) An exception class that represents various validation errors thrown from `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy.html#setFreezePeriods(kotlin.collections.MutableList)` and `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#setSystemUpdatePolicy(android.content.ComponentName,%20android.app.admin.SystemUpdatePolicy)`
[TagLostException](https://developer.android.com/reference/kotlin/android/nfc/TagLostException.html#) <br />

[TelephonyManager.ModemErrorException](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.ModemErrorException.html#) Exception that is supplied to the callback in `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#getNetworkSlicingConfiguration(java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` if the modem returned a failure.
[TelephonyManager.TimeoutException](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.TimeoutException.html#) Exception that is supplied to the callback in `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#getNetworkSlicingConfiguration(java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` if the system timed out waiting for a response from the Radio.
[TimeFormatException](https://developer.android.com/reference/kotlin/android/util/TimeFormatException.html#) <br />

[TransactionTooLargeException](https://developer.android.com/reference/kotlin/android/os/TransactionTooLargeException.html#) The Binder transaction failed because it was too large.
[TransformerConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerConfigurationException.html#) Indicates a serious configuration error.
[TypeNotPresentException](https://developer.android.com/reference/kotlin/java/lang/TypeNotPresentException) Thrown when an application tries to access a type using a string representing the type's name, but no definition for the type with the specified name can be found.
[UTFDataFormatException](https://developer.android.com/reference/kotlin/java/io/UTFDataFormatException.html#) Signals that a malformed string in [modified UTF-8](https://developer.android.com/reference/kotlin/java/io/DataInput.html#modified-utf-8) format has been read in a data input stream or by any class that implements the data input interface.
[UncheckedIOException](https://developer.android.com/reference/kotlin/java/io/UncheckedIOException.html#) Wraps an `https://developer.android.com/reference/kotlin/java/io/IOException.html#` with an unchecked exception.
[UndeclaredThrowableException](https://developer.android.com/reference/kotlin/java/lang/reflect/UndeclaredThrowableException) Thrown by a method invocation on a proxy instance if its invocation handler's `https://developer.android.com/reference/kotlin/java/lang/reflect/InvocationHandler#invoke(kotlin.Any,%20java.lang.reflect.Method,%20kotlin.Array)` method throws a checked exception (a `Throwable` that is not assignable to `RuntimeException` or `Error`) that is not assignable to any of the exception types declared in the `throws` clause of the method that was invoked on the proxy instance and dispatched to the invocation handler.
[UnknownAuthenticationKeyException](https://developer.android.com/reference/kotlin/android/security/identity/UnknownAuthenticationKeyException.html#) Thrown if trying to certify an unknown dynamic authentication key.
[UnknownFormatConversionException](https://developer.android.com/reference/kotlin/java/util/UnknownFormatConversionException.html#) Unchecked exception thrown when an unknown conversion is given.
[UnknownFormatFlagsException](https://developer.android.com/reference/kotlin/java/util/UnknownFormatFlagsException.html#) Unchecked exception thrown when an unknown flag is given.
[UnknownHostException](https://developer.android.com/reference/kotlin/java/net/UnknownHostException.html#) Thrown to indicate that the IP address of a host could not be determined.
[UnknownServiceException](https://developer.android.com/reference/kotlin/java/net/UnknownServiceException.html#) Thrown to indicate that an unknown service exception has occurred.
[UnmappableCharacterException](https://developer.android.com/reference/kotlin/java/nio/charset/UnmappableCharacterException.html#) Checked exception thrown when an input character (or byte) sequence is valid but cannot be mapped to an output byte (or character) sequence.
[UnrecoverableEntryException](https://developer.android.com/reference/kotlin/java/security/UnrecoverableEntryException.html#) This exception is thrown if an entry in the keystore cannot be recovered.
[UnrecoverableKeyException](https://developer.android.com/reference/kotlin/java/security/UnrecoverableKeyException.html#) This exception is thrown if a key in the keystore cannot be recovered.
[UnresolvedAddressException](https://developer.android.com/reference/kotlin/java/nio/channels/UnresolvedAddressException.html#) Unchecked exception thrown when an attempt is made to invoke a network operation upon an unresolved socket address.
[UnsafeStateException](https://developer.android.com/reference/kotlin/android/app/admin/UnsafeStateException.html#) Exception thrown when a `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#` operation failed because it was not safe to be executed at that moment.
[UnsupportedAddressTypeException](https://developer.android.com/reference/kotlin/java/nio/channels/UnsupportedAddressTypeException.html#) Unchecked exception thrown when an attempt is made to bind or connect to a socket address of a type that is not supported.
[UnsupportedCharsetException](https://developer.android.com/reference/kotlin/java/nio/charset/UnsupportedCharsetException.html#) Unchecked exception thrown when no support is available for a requested charset.
[UnsupportedEncodingException](https://developer.android.com/reference/kotlin/java/io/UnsupportedEncodingException.html#) The Character Encoding is not supported.
[UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException) Thrown to indicate that the requested operation is not supported.
[UnsupportedSchemeException](https://developer.android.com/reference/kotlin/android/media/UnsupportedSchemeException.html#) Exception thrown when an attempt is made to construct a MediaDrm object using a crypto scheme UUID that is not supported by the device
[UnsupportedTemporalTypeException](https://developer.android.com/reference/kotlin/java/time/temporal/UnsupportedTemporalTypeException.html#) UnsupportedTemporalTypeException indicates that a ChronoField or ChronoUnit is not supported for a Temporal class.
[UserManager.UserOperationException](https://developer.android.com/reference/kotlin/android/os/UserManager.UserOperationException.html#) Thrown to indicate user operation failed.
[UserNotAuthenticatedException](https://developer.android.com/reference/kotlin/android/security/keystore/UserNotAuthenticatedException.html#) Indicates that a cryptographic operation could not be performed because the user has not been authenticated recently enough.
[UserPresenceUnavailableException](https://developer.android.com/reference/kotlin/android/security/keystore/UserPresenceUnavailableException.html#) Indicates the condition that a proof of user-presence was requested but this proof was not presented.
[UserPrincipalNotFoundException](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipalNotFoundException.html#) Checked exception thrown when a lookup of `https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipal.html#` fails because the principal does not exist.
[VibrationEffect.VibrationParseException](https://developer.android.com/reference/kotlin/android/os/VibrationEffect.VibrationParseException.html#) Exception thrown when parsing a vibration XML fails due to invalid format or values.
[WindowManager.BadTokenException](https://developer.android.com/reference/kotlin/android/view/WindowManager.BadTokenException.html#) Exception that is thrown when trying to add view whose `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#` `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#token:android.os.IBinder` is invalid.
[WindowManager.InvalidDisplayException](https://developer.android.com/reference/kotlin/android/view/WindowManager.InvalidDisplayException.html#) Exception that is thrown when calling `https://developer.android.com/reference/kotlin/android/view/ViewManager.html#addView(android.view.View,%20android.view.ViewGroup.LayoutParams)` to a secondary display that cannot be found.
[WriteAbortedException](https://developer.android.com/reference/kotlin/java/io/WriteAbortedException.html#) Signals that one of the ObjectStreamExceptions was thrown during a write operation.
[WritePendingException](https://developer.android.com/reference/kotlin/java/nio/channels/WritePendingException.html#) Unchecked exception thrown when an attempt is made to write to an asynchronous socket channel and a previous write has not completed.
[WrongMethodTypeException](https://developer.android.com/reference/kotlin/java/lang/invoke/WrongMethodTypeException) Thrown to indicate that code has attempted to call a method handle via the wrong method type.
[WrongThreadException](https://developer.android.com/reference/kotlin/java/lang/WrongThreadException) Thrown to indicate that a method has been called on the wrong thread.
[XPathExpressionException](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathExpressionException.html#) `XPathExpressionException` represents an error in an XPath expression.
[XPathFactoryConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFactoryConfigurationException.html#) `XPathFactoryConfigurationException` represents a configuration error in a `XPathFactory` environment.
[XPathFunctionException](https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathFunctionException.html#) `XPathFunctionException` represents an error with an XPath function.
[ZipException](https://developer.android.com/reference/kotlin/java/util/zip/ZipException.html#) Signals that a Zip exception of some sort has occurred.
[ZoneRulesException](https://developer.android.com/reference/kotlin/java/time/zone/ZoneRulesException.html#) Thrown to indicate a problem with time-zone configuration.

The class `Exception` and its subclasses are a form of `Throwable` that indicates conditions that a reasonable application might want to catch.

The class `Exception` and any subclasses that are not also subclasses of `https://developer.android.com/reference/kotlin/java/lang/RuntimeException` are *checked exceptions* . Checked exceptions need to be declared in a method or constructor's `throws` clause if they can be thrown by the execution of the method or constructor and propagate outside the method or constructor boundary.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Exception#Exception()()` Constructs a new exception with `null` as its detail message. |
| `https://developer.android.com/reference/kotlin/java/lang/Exception#Exception(kotlin.String)(message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Constructs a new exception with the specified detail message. |
| `https://developer.android.com/reference/kotlin/java/lang/Exception#Exception(kotlin.String,%20kotlin.Throwable)(message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, cause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!)` Constructs a new exception with the specified detail message and cause. |
| `https://developer.android.com/reference/kotlin/java/lang/Exception#Exception(kotlin.Throwable)(cause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!)` Constructs a new exception with the specified cause and a detail message of `(cause==null ? null : cause.toString())` (which typically contains the class and detail message of `cause`). |

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Exception#Exception(kotlin.String,%20kotlin.Throwable,%20kotlin.Boolean,%20kotlin.Boolean)(message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, cause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!, enableSuppression: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, writableStackTrace: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Constructs a new exception with the specified detail message, cause, suppression enabled or disabled, and writable stack trace enabled or disabled. |

## Public constructors

### Exception

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Exception()
```

Constructs a new exception with `null` as its detail message. The cause is not initialized, and may subsequently be initialized by a call to `https://developer.android.com/reference/kotlin/java/lang/Throwable#initCause(kotlin.Throwable)`.

### Exception

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Exception(message: String!)
```

Constructs a new exception with the specified detail message. The cause is not initialized, and may subsequently be initialized by a call to `https://developer.android.com/reference/kotlin/java/lang/Throwable#initCause(kotlin.Throwable)`.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message. The detail message is saved for later retrieval by the `https://developer.android.com/reference/kotlin/java/lang/Throwable#getMessage()` method. |

### Exception

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Exception(
    message: String!, 
    cause: Throwable!)
```

Constructs a new exception with the specified detail message and cause.

Note that the detail message associated with `cause` is *not* automatically incorporated in this exception's detail message.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message (which is saved for later retrieval by the `https://developer.android.com/reference/kotlin/java/lang/Throwable#getMessage()` method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause (which is saved for later retrieval by the `https://developer.android.com/reference/kotlin/java/lang/Throwable#getCause()` method). (A `null` value is permitted, and indicates that the cause is nonexistent or unknown.) |

### Exception

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Exception(cause: Throwable!)
```

Constructs a new exception with the specified cause and a detail message of `(cause==null ? null : cause.toString())` (which typically contains the class and detail message of `cause`). This constructor is useful for exceptions that are little more than wrappers for other throwables (for example, `https://developer.android.com/reference/kotlin/java/security/PrivilegedActionException.html#`).

| Parameters ||
|---|---|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause (which is saved for later retrieval by the `https://developer.android.com/reference/kotlin/java/lang/Throwable#getCause()` method). (A `null` value is permitted, and indicates that the cause is nonexistent or unknown.) |

## Protected constructors

### Exception

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected Exception(
    message: String!, 
    cause: Throwable!, 
    enableSuppression: Boolean, 
    writableStackTrace: Boolean)
```

Constructs a new exception with the specified detail message, cause, suppression enabled or disabled, and writable stack trace enabled or disabled.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause. (A `null` value is permitted, and indicates that the cause is nonexistent or unknown.) |
| `enableSuppression` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether or not suppression is enabled or disabled |
| `writableStackTrace` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether or not the stack trace should be writable |
