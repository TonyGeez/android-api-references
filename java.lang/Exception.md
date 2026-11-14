Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Exception

```
open class Exception : Throwable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |

Known Direct Subclasses [AccountsException](../android/accounts/AccountsException.md), [AclNotFoundException](../java/security/acl/AclNotFoundException.md), [AdServicesException](../android/adservices/exceptions/AdServicesException.md), [AndroidException](../android/util/AndroidException.md), [AppFunctionException](../android/app/appfunctions/AppFunctionException.md), [AppInteractionException](../android/app/AppInteractionException.md), [AppSearchException](../android/app/appsearch/exceptions/AppSearchException.md), [BackingStoreException](../java/util/prefs/BackingStoreException.md), [BrokenBarrierException](../java/util/concurrent/BrokenBarrierException.md), [CertificateException](../javax/security/cert/CertificateException.md), [ClearCredentialStateException](../android/credentials/ClearCredentialStateException.md), [CloneNotSupportedException](../java/lang/CloneNotSupportedException.md), and 55 others. [AccountsException](../android/accounts/AccountsException.md) <br />

[AclNotFoundException](../java/security/acl/AclNotFoundException.md) This is an exception that is thrown whenever a reference is made to a non-existent ACL (Access Control List).
[AdServicesException](../android/adservices/exceptions/AdServicesException.md) Exception thrown by AdServices.
[AndroidException](../android/util/AndroidException.md) Base class for all checked exceptions thrown by the Android frameworks.
[AppFunctionException](../android/app/appfunctions/AppFunctionException.md) App function related error.
[AppInteractionException](../android/app/AppInteractionException.md) Exception thrown when an app interaction operation fails.
[AppSearchException](../android/app/appsearch/exceptions/AppSearchException.md) An exception thrown by `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession.html#` or a subcomponent.
[BackingStoreException](../java/util/prefs/BackingStoreException.md) Thrown to indicate that a preferences operation could not complete because of a failure in the backing store, or a failure to contact the backing store.
[BrokenBarrierException](../java/util/concurrent/BrokenBarrierException.md) Exception thrown when a thread tries to wait upon a barrier that is in a broken state, or which enters the broken state while the thread is waiting.
[CertificateException](../javax/security/cert/CertificateException.md) This exception indicates one of a variety of certificate problems.
[ClearCredentialStateException](../android/credentials/ClearCredentialStateException.md) Represents an error encountered during the `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#clearCredentialState(android.credentials.ClearCredentialStateRequest,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` operation.
[CloneNotSupportedException](../java/lang/CloneNotSupportedException.md) Thrown to indicate that the `clone` method in class `Object` has been called to clone an object, but that the object's class does not implement the `Cloneable` interface.
[ConfirmationAlreadyPresentingException](../android/security/ConfirmationAlreadyPresentingException.md) This exception is thrown when presenting a prompt fails because another prompt is already being presented.
[ConfirmationNotAvailableException](../android/security/ConfirmationNotAvailableException.md) This exception is thrown when presenting a prompt fails because the environment lacks facilities for showing confirmations.
[CreateCredentialException](../android/credentials/CreateCredentialException.md) Represents an error encountered during the `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#createCredential(android.content.Context,%20android.credentials.CreateCredentialRequest,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` operation.
[CrossDeviceAuthenticationException](../android/security/authenticationpolicy/CrossDeviceAuthenticationException.md) Exception thrown when cross-device authentication fails.
[DataFormatException](../java/util/zip/DataFormatException.md) Signals that a data format error has occurred.
[DatatypeConfigurationException](../javax/xml/datatype/DatatypeConfigurationException.md) Indicates a serious configuration error.
[DestroyFailedException](../javax/security/auth/DestroyFailedException.md) Signals that a `destroy` operation failed.
[DnsResolver.DnsException](../android/net/DnsResolver.DnsException.md) Class to represent DNS error
[ErrnoException](../android/system/ErrnoException.md) A checked exception thrown when `https://developer.android.com/reference/kotlin/android/system/Os.html#` methods fail.
[ExecutionException](../java/util/concurrent/ExecutionException.md) Exception thrown when attempting to retrieve the result of a task that aborted by throwing an exception.
[FormatException](../android/nfc/FormatException.md) <br />

[GeneralSecurityException](../java/security/GeneralSecurityException.md) The `GeneralSecurityException` class is a generic security exception class that provides type safety for all the security-related exception classes that extend from it.
[GetCredentialException](../android/credentials/GetCredentialException.md) Represents an error encountered during the `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#getCredential(android.content.Context,%20android.credentials.GetCredentialRequest,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` operation.
[IOException](../java/io/IOException.md) Signals that an I/O exception of some sort has occurred.
[IdentityCredentialException](../android/security/identity/IdentityCredentialException.md) Base class for all Identity Credential exceptions.
[IkeException](../android/net/ipsec/ike/exceptions/IkeException.md) IkeException represents a generic exception that includes internal and protocol exceptions.
[ImsException](../android/telephony/ims/ImsException.md) This class defines an IMS-related exception that has been thrown while interacting with a device or carrier provided ImsService implementation.
[InterruptedException](../java/lang/InterruptedException.md) Thrown when a thread is waiting, sleeping, or otherwise occupied, and the thread is interrupted, either before or during the activity.
[InvalidPreferencesFormatException](../java/util/prefs/InvalidPreferencesFormatException.md) Thrown to indicate that an operation could not complete because the input did not conform to the appropriate XML document type for a collection of preferences, as per the `https://developer.android.com/reference/kotlin/java/util/prefs/Preferences.html#` specification.
[IsolatedServiceException](../android/adservices/ondevicepersonalization/IsolatedServiceException.md) A class that an `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService.html#` can use to signal a failure in handling a request and return an error to be logged and aggregated.
[JSONException](../org/json/JSONException.md) Thrown to indicate a problem with the JSON API.
[KeyChainException](../android/security/KeyChainException.md) Thrown on problems accessing the `https://developer.android.com/reference/kotlin/android/security/KeyChain.html#`.
[KeyStoreException](../android/security/KeyStoreException.md) Exception containing information about the failure at the Keystore / KeyMint layer while generating or using a key.
[LambdaConversionException](../java/lang/invoke/LambdaConversionException.md) LambdaConversionException
[LastOwnerException](../java/security/acl/LastOwnerException.md) This is an exception that is thrown whenever an attempt is made to delete the last owner of an Access Control List.
[LoadSdkException](../android/app/sdksandbox/LoadSdkException.md) Exception thrown by `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager.html#loadSdk(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`
[MediaCasException](../android/media/MediaCasException.md) Base class for MediaCas exceptions
[MediaCryptoException](../android/media/MediaCryptoException.md) Exception thrown if MediaCrypto object could not be instantiated or if unable to perform an operation on the MediaCrypto object.
[MediaDrmException](../android/media/MediaDrmException.md) Base class for MediaDrm exceptions
[MigrationException](../android/app/privatecompute/MigrationException.md) Exception thrown when a migration request fails.
[NotOwnerException](../java/security/acl/NotOwnerException.md) This is an exception that is thrown whenever the modification of an object (such as an Access Control List) is only allowed to be done by an owner of the object, but the Principal attempting the modification is not an owner.
[OnDevicePersonalizationException](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md) Exception thrown by OnDevicePersonalization APIs.
[OperationApplicationException](../android/content/OperationApplicationException.md) Thrown when an application of a `https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.html#` fails due the specified constraints.
[ParseException](../java/text/ParseException.md) Signals that an error has been reached unexpectedly while parsing.
[ParserConfigurationException](../javax/xml/parsers/ParserConfigurationException.md) Indicates a serious configuration error.
[PccEgressException](../android/app/privatecompute/PccEgressException.md) Exception thrown when an egress request fails inside the PCC sandbox.
[PrivilegedActionException](../java/security/PrivilegedActionException.md) Legacy security code; do not use.
[ReflectiveOperationException](../java/lang/ReflectiveOperationException.md) Common superclass of exceptions thrown by reflective operations in core reflection.
[RequestSurfacePackageException](../android/app/sdksandbox/RequestSurfacePackageException.md) Exception thrown by `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager.html#requestSurfacePackage(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`
[RuntimeException](../java/lang/RuntimeException.md) `RuntimeException` is the superclass of those exceptions that can be thrown during the normal operation of the Java Virtual Machine.
[SAXException](../org/xml/sax/SAXException.md) Encapsulate a general SAX error or warning.
[SQLException](../java/sql/SQLException.md) An exception that provides information on a database access error or other errors.
[SigningInfoException](../android/content/pm/SigningInfoException.md) Indicates an error when verifying the [app signing](https://source.android.com/docs/security/features/apksigning) information.
[SipException](../android/net/sip/SipException.md) Indicates a general SIP-related exception.
[StringConcatException](../java/lang/invoke/StringConcatException.md) StringConcatException is thrown by `https://developer.android.com/reference/kotlin/java/lang/Exception#` when linkage invariants are violated.
[SurfaceTexture.OutOfResourcesException](../android/graphics/SurfaceTexture.OutOfResourcesException.md) Exception thrown when a SurfaceTexture couldn't be created or resized.
[TelephonyManager.CallComposerException](../android/telephony/TelephonyManager.CallComposerException.md) Exception that may be supplied to the callback in #uploadCallComposerPicture if something goes awry.
[TelephonyManager.NetworkSlicingException](../android/telephony/TelephonyManager.NetworkSlicingException.md) Exception that may be supplied to the callback in `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#getNetworkSlicingConfiguration(java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` if something goes awry.
[TimeoutException](../java/util/concurrent/TimeoutException.md) Exception thrown when a blocking operation times out.
[TooManyListenersException](../java/util/TooManyListenersException.md) The `TooManyListenersException ` Exception is used as part of the Java Event model to annotate and implement a unicast special case of a multicast Event Source.
[TransformerException](../javax/xml/transform/TransformerException.md) This class specifies an exceptional condition that occurred during the transformation process.
[URISyntaxException](../java/net/URISyntaxException.md) Checked exception thrown to indicate that a string could not be parsed as a URI reference.
[UnsupportedCallbackException](../javax/security/auth/callback/UnsupportedCallbackException.md) Signals that a `CallbackHandler` does not recognize a particular `Callback`.
[XPathException](../javax/xml/xpath/XPathException.md) `XPathException` represents a generic XPath exception.
[XmlPullParserException](../org/xmlpull/v1/XmlPullParserException.md) This exception is thrown to signal XML Pull Parser related faults.
Known Indirect Subclasses [AEADBadTagException](../javax/crypto/AEADBadTagException.md), [AcceptPendingException](../java/nio/channels/AcceptPendingException.md), [AccessControlException](../java/security/AccessControlException.md), [AccessDeniedException](../java/nio/file/AccessDeniedException.md), [AconfigStorageReadException](../android/os/flagging/AconfigStorageReadException.md), [ActivityNotFoundException](../android/content/ActivityNotFoundException.md), [AlreadyBoundException](../java/nio/channels/AlreadyBoundException.md), [AlreadyConnectedException](../java/nio/channels/AlreadyConnectedException.md), [AlreadyPersonalizedException](../android/security/identity/AlreadyPersonalizedException.md), [AndroidRuntimeException](../android/util/AndroidRuntimeException.md), [AnnotationTypeMismatchException](../java/lang/annotation/AnnotationTypeMismatchException.md), [AppInteractionDeniedException](../android/app/AppInteractionDeniedException.md), and 354 others. [AEADBadTagException](../javax/crypto/AEADBadTagException.md) This exception is thrown when a `https://developer.android.com/reference/kotlin/javax/crypto/Cipher.html#` operating in an AEAD mode (such as GCM/CCM) is unable to verify the supplied authentication tag.
[AcceptPendingException](../java/nio/channels/AcceptPendingException.md) Unchecked exception thrown when an attempt is made to initiate an accept operation on a channel and a previous accept operation has not completed.
[AccessControlException](../java/security/AccessControlException.md) This exception is thrown by the AccessController to indicate that a requested access (to a critical system resource such as the file system or the network) is denied.
[AccessDeniedException](../java/nio/file/AccessDeniedException.md) Checked exception thrown when a file system operation is denied, typically due to a file permission or other access check.
[AconfigStorageReadException](../android/os/flagging/AconfigStorageReadException.md) Exception thrown when an error occurs while reading from Aconfig Storage.
[ActivityNotFoundException](../android/content/ActivityNotFoundException.md) This exception is thrown when a call to android.
[AlreadyBoundException](../java/nio/channels/AlreadyBoundException.md) Unchecked exception thrown when an attempt is made to bind the socket a network oriented channel that is already bound.
[AlreadyConnectedException](../java/nio/channels/AlreadyConnectedException.md) Unchecked exception thrown when an attempt is made to connect a `https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel.html#` that is already connected.
[AlreadyPersonalizedException](../android/security/identity/AlreadyPersonalizedException.md) Thrown if trying to create a credential which already exists.
[AndroidRuntimeException](../android/util/AndroidRuntimeException.md) Base class for all unchecked exceptions thrown by the Android frameworks.
[AnnotationTypeMismatchException](../java/lang/annotation/AnnotationTypeMismatchException.md) Thrown to indicate that a program has attempted to access an element of an annotation whose type has changed after the annotation was compiled (or serialized).
[AppInteractionDeniedException](../android/app/AppInteractionDeniedException.md) Exception thrown when an app interaction is denied.
[ArithmeticException](../java/lang/ArithmeticException.md) Thrown when an exceptional arithmetic condition has occurred.
[ArrayIndexOutOfBoundsException](../java/lang/ArrayIndexOutOfBoundsException.md) Thrown to indicate that an array has been accessed with an illegal index.
[ArrayStoreException](../java/lang/ArrayStoreException.md) Thrown to indicate that an attempt has been made to store the wrong type of object into an array of objects.
[AsynchronousCloseException](../java/nio/channels/AsynchronousCloseException.md) Checked exception received by a thread when another thread closes the channel or the part of the channel upon which it is blocked in an I/O operation.
[AtomicMoveNotSupportedException](../java/nio/file/AtomicMoveNotSupportedException.md) Checked exception thrown when a file cannot be moved as an atomic file system operation.
[AuthenticationRequiredException](../android/app/AuthenticationRequiredException.md) Specialization of `https://developer.android.com/reference/kotlin/java/lang/SecurityException` that is thrown when authentication is needed from the end user before viewing the content.
[AuthenticatorException](../android/accounts/AuthenticatorException.md) <br />

[BackendBusyException](../android/security/keystore/BackendBusyException.md) Indicates a transient error that prevented a key operation from being created.
[BackgroundServiceStartNotAllowedException](../android/app/BackgroundServiceStartNotAllowedException.md) Exception thrown when an app tries to start a background `https://developer.android.com/reference/kotlin/android/app/Service.html#` when it's not allowed to do so.
[BadPaddingException](../javax/crypto/BadPaddingException.md) This exception is thrown when a particular padding mechanism is expected for the input data but the data is not padded properly.
[BadParcelableException](../android/os/BadParcelableException.md) Exception thrown when a `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` is malformed or otherwise invalid.
[Base64DataException](../android/util/Base64DataException.md) This exception is thrown by `https://developer.android.com/reference/kotlin/android/util/Base64InputStream.html#` or `https://developer.android.com/reference/kotlin/android/util/Base64OutputStream.html#` when an error is detected in the data being decoded.
[BatchUpdateException](../java/sql/BatchUpdateException.md) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` thrown when an error occurs during a batch update operation.
[BindException](../java/net/BindException.md) Signals that an error occurred while attempting to bind a socket to a local address and port.
[BluetoothSocketException](../android/bluetooth/BluetoothSocketException.md) Thrown when an error occurs during a Bluetooth Socket related exception.
[BufferOverflowException](../java/nio/BufferOverflowException.md) Unchecked exception thrown when a relative *put* operation reaches the target buffer's limit.
[BufferUnderflowException](../java/nio/BufferUnderflowException.md) Unchecked exception thrown when a relative *get* operation reaches the source buffer's limit.
[CRLException](../java/security/cert/CRLException.md) CRL (Certificate Revocation List) Exception.
[CallEndpointException](../android/telecom/CallEndpointException.md) This class represents a set of exceptions that can occur when requesting a `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint.html#` change.
[CallException](../android/telecom/CallException.md) This class defines exceptions that can be thrown when using Telecom APIs with `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#`s.
[CallbackException](../android/net/http/CallbackException.md) Exception passed to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback.html#onFailed(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)` when `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback.html#` or `https://developer.android.com/reference/kotlin/android/net/http/UploadDataProvider.html#` method throws an exception.
[CameraAccessException](../android/hardware/camera2/CameraAccessException.md) `CameraAccessException` is thrown if a camera device could not be queried or opened by the `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.html#`, or if the connection to an opened `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#` is no longer valid.
[CancellationException](../java/util/concurrent/CancellationException.md) Exception indicating that the result of a value-producing task, such as a `https://developer.android.com/reference/kotlin/java/util/concurrent/FutureTask.html#`, cannot be retrieved because the task was cancelled.
[CancelledKeyException](../java/nio/channels/CancelledKeyException.md) Unchecked exception thrown when an attempt is made to use a selection key that is no longer valid.
[CertPathBuilderException](../java/security/cert/CertPathBuilderException.md) An exception indicating one of a variety of problems encountered when building a certification path with a `CertPathBuilder`.
[CertPathValidatorException](../java/security/cert/CertPathValidatorException.md) An exception indicating one of a variety of problems encountered when validating a certification path.
[CertStoreException](../java/security/cert/CertStoreException.md) An exception indicating one of a variety of problems retrieving certificates and CRLs from a `CertStore`.
[CertificateEncodingException](../javax/security/cert/CertificateEncodingException.md) Certificate Encoding Exception.
[CertificateEncodingException](../java/security/cert/CertificateEncodingException.md) Certificate Encoding Exception.
[CertificateException](../java/security/cert/CertificateException.md) This exception indicates one of a variety of certificate problems.
[CertificateExpiredException](../javax/security/cert/CertificateExpiredException.md) Certificate Expired Exception.
[CertificateExpiredException](../java/security/cert/CertificateExpiredException.md) Certificate Expired Exception.
[CertificateNotYetValidException](../javax/security/cert/CertificateNotYetValidException.md) Certificate is not yet valid exception.
[CertificateNotYetValidException](../java/security/cert/CertificateNotYetValidException.md) Certificate is not yet valid exception.
[CertificateParsingException](../javax/security/cert/CertificateParsingException.md) Certificate Parsing Exception.
[CertificateParsingException](../java/security/cert/CertificateParsingException.md) Certificate Parsing Exception.
[CertificateRevokedException](../java/security/cert/CertificateRevokedException.md) An exception that indicates an X.
[CharConversionException](../java/io/CharConversionException.md) Base class for character conversion exceptions.
[CharacterCodingException](../java/nio/charset/CharacterCodingException.md) Checked exception thrown when a character encoding or decoding error occurs.
[CipherSuiteNotSupportedException](../android/security/identity/CipherSuiteNotSupportedException.md) Thrown if trying to use a cipher suite which isn't supported.
[ClassCastException](../java/lang/ClassCastException.md) Thrown to indicate that the code has attempted to cast an object to a subclass of which it is not an instance.
[ClassNotFoundException](../java/lang/ClassNotFoundException.md) Thrown when an application tries to load in a class through its string name using:

- The `forName` method in class `Class`.
- The `findSystemClass` method in class `ClassLoader` .
- The `loadClass` method in class `ClassLoader`.

<br />

[ClosedByInterruptException](../java/nio/channels/ClosedByInterruptException.md) Checked exception received by a thread when another thread interrupts it while it is blocked in an I/O operation upon a channel.
[ClosedChannelException](../java/nio/channels/ClosedChannelException.md) Checked exception thrown when an attempt is made to invoke or complete an I/O operation upon channel that is closed, or at least closed to that operation.
[ClosedDirectoryStreamException](../java/nio/file/ClosedDirectoryStreamException.md) Unchecked exception thrown when an attempt is made to invoke an operation on a directory stream that is closed.
[ClosedFileSystemException](../java/nio/file/ClosedFileSystemException.md) Unchecked exception thrown when an attempt is made to invoke an operation on a file and the file system is closed.
[ClosedSelectorException](../java/nio/channels/ClosedSelectorException.md) Unchecked exception thrown when an attempt is made to invoke an I/O operation upon a closed selector.
[ClosedWatchServiceException](../java/nio/file/ClosedWatchServiceException.md) Unchecked exception thrown when an attempt is made to invoke an operation on a watch service that is closed.
[CompanionException](../android/companion/CompanionException.md) `CompanionException` can be thrown during the companion system data transfer process.
[CompletionException](../java/util/concurrent/CompletionException.md) Exception thrown when an error or other exception is encountered in the course of completing a result or task.
[ConcurrentModificationException](../java/util/ConcurrentModificationException.md) This exception may be thrown by methods that have detected concurrent modification of an object when such modification is not permissible.
[ConnectException](../java/net/ConnectException.md) Signals that an error occurred while attempting to connect a socket to a remote address and port.
[ConnectTimeoutException](../org/apache/http/conn/ConnectTimeoutException.md) A timeout while connecting to an HTTP server or waiting for an available connection from an HttpConnectionManager.
[ConnectionPendingException](../java/nio/channels/ConnectionPendingException.md) Unchecked exception thrown when an attempt is made to connect a `https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel.html#` for which a non-blocking connection operation is already in progress.
[CursorIndexOutOfBoundsException](../android/database/CursorIndexOutOfBoundsException.md) An exception indicating that a cursor is out of bounds.
[CursorWindowAllocationException](../android/database/CursorWindowAllocationException.md) This exception is thrown when a CursorWindow couldn't be allocated, most probably due to memory not being available.
[DOMException](../org/w3c/dom/DOMException.md) DOM operations only raise exceptions in "exceptional" circumstances, i.
[DataTruncation](../java/sql/DataTruncation.md) An exception thrown as a `DataTruncation` exception (on writes) or reported as a `DataTruncation` warning (on reads) when a data values is unexpectedly truncated for reasons other than its having execeeded `MaxFieldSize`.
[DateTimeException](../java/time/DateTimeException.md) Exception used to indicate a problem while calculating a date-time.
[DateTimeParseException](../java/time/format/DateTimeParseException.md) An exception thrown when an error occurs during parsing.
[DeadObjectException](../android/os/DeadObjectException.md) The object you are calling has died, because its hosting process no longer exists, or there has been a low-level binder error.
[DeadSystemException](../android/os/DeadSystemException.md) The core Android system has died and is going through a runtime restart.
[DeniedByServerException](../android/media/DeniedByServerException.md) Exception thrown when the provisioning server or key server denies a certficate or license for a device.
[DeviceNotAssociatedException](../android/companion/DeviceNotAssociatedException.md) An exception for a case when a given device was not android.
[DigestException](../java/security/DigestException.md) This is the generic Message Digest exception.
[DirectoryIteratorException](../java/nio/file/DirectoryIteratorException.md) Runtime exception thrown if an I/O error is encountered when iterating over the entries in a directory.
[DirectoryNotEmptyException](../java/nio/file/DirectoryNotEmptyException.md) Checked exception thrown when a file system operation fails because a directory is not empty.
[DocTypeNotSupportedException](../android/security/identity/DocTypeNotSupportedException.md) Thrown if trying to create a credential with an unsupported document type.
[DuplicateFormatFlagsException](../java/util/DuplicateFormatFlagsException.md) Unchecked exception thrown when duplicate flags are provided in the format specifier.
[EOFException](../java/io/EOFException.md) Signals that an end of file or end of stream has been reached unexpectedly during input.
[EchConfigMismatchException](../android/net/ssl/EchConfigMismatchException.md) Exception thrown when the provided ECH (Encrypted Client Hello) config does not match the server.
[EmptyStackException](../java/util/EmptyStackException.md) Thrown by methods in the `Stack` class to indicate that the stack is empty.
[EnumConstantNotPresentException](../java/lang/EnumConstantNotPresentException.md) Thrown when an application tries to access an enum constant by name and the enum type contains no constant with the specified name.
[EphemeralPublicKeyNotFoundException](../android/security/identity/EphemeralPublicKeyNotFoundException.md) Thrown if the ephemeral public key was not found in the session transcript passed to `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredential.html#getEntries(kotlin.ByteArray,%20kotlin.collections.MutableMap,%20kotlin.ByteArray,%20kotlin.ByteArray)`.
[ExemptionMechanismException](../javax/crypto/ExemptionMechanismException.md) This is the generic ExemptionMechanism exception.
[FileAlreadyExistsException](../java/nio/file/FileAlreadyExistsException.md) Checked exception thrown when an attempt is made to create a file or directory and a file of that name already exists.
[FileLockInterruptionException](../java/nio/channels/FileLockInterruptionException.md) Checked exception received by a thread when another thread interrupts it while it is waiting to acquire a file lock.
[FileNotFoundException](../java/io/FileNotFoundException.md) Signals that an attempt to open the file denoted by a specified pathname has failed.
[FileSystemAlreadyExistsException](../java/nio/file/FileSystemAlreadyExistsException.md) Runtime exception thrown when an attempt is made to create a file system that already exists.
[FileSystemException](../java/nio/file/FileSystemException.md) Thrown when a file system operation fails on one or two files.
[FileSystemLoopException](../java/nio/file/FileSystemLoopException.md) Checked exception thrown when a file system loop, or cycle, is encountered.
[FileSystemNotFoundException](../java/nio/file/FileSystemNotFoundException.md) Runtime exception thrown when a file system cannot be found.
[FileUriExposedException](../android/os/FileUriExposedException.md) The exception that may be thrown when an application exposes a `file://` `https://developer.android.com/reference/kotlin/android/net/Uri.html#` to another app.
[ForegroundServiceStartNotAllowedException](../android/app/ForegroundServiceStartNotAllowedException.md) Exception thrown when an app tries to start a foreground `https://developer.android.com/reference/kotlin/android/app/Service.html#` when it's not allowed to do so.
[ForegroundServiceTypeException](../android/app/ForegroundServiceTypeException.md) Base exception thrown when an app tries to start a foreground `https://developer.android.com/reference/kotlin/android/app/Service.html#` without a valid type.
[FormatFlagsConversionMismatchException](../java/util/FormatFlagsConversionMismatchException.md) Unchecked exception thrown when a conversion and flag are incompatible.
[FormatterClosedException](../java/util/FormatterClosedException.md) Unchecked exception thrown when the formatter has been closed.
[Fragment.InstantiationException](../android/app/Fragment.InstantiationException.md) Thrown by `https://developer.android.com/reference/kotlin/android/app/Fragment.html#instantiate(android.content.Context,%20kotlin.String,%20android.os.Bundle)` when there is an instantiation failure.
[GLException](../android/opengl/GLException.md) An exception class for OpenGL errors.
[HealthConnectException](../android/health/connect/HealthConnectException.md) Class representing health connect exceptions.
[HttpException](../android/net/http/HttpException.md) Base exception passed to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback.html#onFailed(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)`.
[HttpRetryException](../java/net/HttpRetryException.md) Thrown to indicate that a HTTP request needs to be retried but cannot be retried automatically, due to streaming mode being enabled.
[ICUUncheckedIOException](../android/icu/util/ICUUncheckedIOException.md) Unchecked version of `https://developer.android.com/reference/kotlin/java/io/IOException.html#`.
[IkeIOException](../android/net/ipsec/ike/exceptions/IkeIOException.md) Wrapper for I/O exceptions encountered during IKE operations.
[IkeInternalException](../android/net/ipsec/ike/exceptions/IkeInternalException.md) IkeInternalException encapsulates all local implementation or resource related exceptions.
[IkeNetworkLostException](../android/net/ipsec/ike/exceptions/IkeNetworkLostException.md) IkeNetworkLostException is returned to the caller via `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback.html#onError(android.net.ipsec.ike.exceptions.IkeException)` if the underlying Network for the `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession.html#` was lost with no alternatives.
[IkeNonProtocolException](../android/net/ipsec/ike/exceptions/IkeNonProtocolException.md) IkeNonProtocolException encapsulates all implementation-specific non-protocol IKE errors.
[IkeProtocolException](../android/net/ipsec/ike/exceptions/IkeProtocolException.md) IkeProtocolException is an abstract class that represents the common information for all IKE protocol errors.
[IkeTimeoutException](../android/net/ipsec/ike/exceptions/IkeTimeoutException.md) This exception is thrown when there is an IKE retransmission timeout.
[IllegalAccessException](../java/lang/IllegalAccessException.md) An IllegalAccessException is thrown when an application tries to reflectively create an instance (other than an array), set or get a field, or invoke a method, but the currently executing method does not have access to the definition of the specified class, field, method or constructor.
[IllegalArgumentException](../java/lang/IllegalArgumentException.md) Thrown to indicate that a method has been passed an illegal or inappropriate argument.
[IllegalBlockSizeException](../javax/crypto/IllegalBlockSizeException.md) This exception is thrown when the length of data provided to a block cipher is incorrect, i.
[IllegalBlockingModeException](../java/nio/channels/IllegalBlockingModeException.md) Unchecked exception thrown when a blocking-mode-specific operation is invoked upon a channel in the incorrect blocking mode.
[IllegalCallerException](../java/lang/IllegalCallerException.md) Thrown to indicate that a method has been called by an inappropriate caller.
[IllegalChannelGroupException](../java/nio/channels/IllegalChannelGroupException.md) Unchecked exception thrown when an attempt is made to open a channel in a group that was not created by the same provider.
[IllegalCharsetNameException](../java/nio/charset/IllegalCharsetNameException.md) Unchecked exception thrown when a string that is not a [legal charset name](../java/nio/charset/Charset.md) is used as such.
[IllegalFormatCodePointException](../java/util/IllegalFormatCodePointException.md) Unchecked exception thrown when a character with an invalid Unicode code point as defined by `https://developer.android.com/reference/kotlin/java/lang/Character#isValidCodePoint(kotlin.Int)` is passed to the `https://developer.android.com/reference/kotlin/java/util/Formatter.html#`.
[IllegalFormatConversionException](../java/util/IllegalFormatConversionException.md) Unchecked exception thrown when the argument corresponding to the format specifier is of an incompatible type.
[IllegalFormatException](../java/util/IllegalFormatException.md) Unchecked exception thrown when a format string contains an illegal syntax or a format specifier that is incompatible with the given arguments.
[IllegalFormatFlagsException](../java/util/IllegalFormatFlagsException.md) Unchecked exception thrown when an illegal combination flags is given.
[IllegalFormatPrecisionException](../java/util/IllegalFormatPrecisionException.md) Unchecked exception thrown when the precision is a negative value other than `-1`, the conversion does not support a precision, or the value is otherwise unsupported.
[IllegalFormatWidthException](../java/util/IllegalFormatWidthException.md) Unchecked exception thrown when the format width is a negative value other than `-1` or is otherwise unsupported.
[IllegalMonitorStateException](../java/lang/IllegalMonitorStateException.md) Thrown to indicate that a thread has attempted to wait on an object's monitor or to notify other threads waiting on an object's monitor without owning the specified monitor.
[IllegalSelectorException](../java/nio/channels/IllegalSelectorException.md) Unchecked exception thrown when an attempt is made to register a channel with a selector that was not created by the provider that created the channel.
[IllegalStateException](../java/lang/IllegalStateException.md) Signals that a method has been invoked at an illegal or inappropriate time.
[IllegalThreadStateException](../java/lang/IllegalThreadStateException.md) Thrown to indicate that a thread is not in an appropriate state for the requested operation.
[IllformedLocaleException](../java/util/IllformedLocaleException.md) Thrown by methods in `https://developer.android.com/reference/kotlin/java/util/Locale.html#` and `https://developer.android.com/reference/kotlin/java/util/Locale.Builder.html#` to indicate that an argument is not a well-formed BCP 47 tag.
[IllformedLocaleException](../android/icu/util/IllformedLocaleException.md) Thrown by methods in `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#` and `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Builder.html#` to indicate that an argument is not a well-formed BCP 47 tag.
[ImageDecoder.DecodeException](../android/graphics/ImageDecoder.DecodeException.md) Information about an interrupted decode.
[IncompleteAnnotationException](../java/lang/annotation/IncompleteAnnotationException.md) Thrown to indicate that a program has attempted to access an element of an annotation interface that was added to the annotation interface definition after the annotation was compiled (or serialized).
[IndexOutOfBoundsException](../java/lang/IndexOutOfBoundsException.md) Thrown to indicate that an index of some sort (such as to an array, to a string, or to a vector) is out of range.
[InfeasibleActivityOptionsException](../android/app/InfeasibleActivityOptionsException.md) This exception is thrown when a call to android.
[InflateException](../android/view/InflateException.md) This exception is thrown by an inflater on error conditions.
[InlineExecutionProhibitedException](../android/net/http/InlineExecutionProhibitedException.md) Thrown when an executor runs a submitted runnable inline in `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#execute(java.lang.Runnable)` and `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder.html#setDirectExecutorAllowed(kotlin.Boolean)` was not called.
[InputMismatchException](../java/util/InputMismatchException.md) Thrown by a `Scanner` to indicate that the token retrieved does not match the pattern for the expected type, or that the token is out of range for the expected type.
[InspectionCompanion.UninitializedPropertyMapException](../android/view/inspector/InspectionCompanion.UninitializedPropertyMapException.md) Thrown by `https://developer.android.com/reference/kotlin/android/view/inspector/InspectionCompanion.html#readProperties(android.view.inspector.InspectionCompanion.T,%20android.view.inspector.PropertyReader)` if called before `https://developer.android.com/reference/kotlin/android/view/inspector/InspectionCompanion.html#mapProperties(android.view.inspector.PropertyMapper)`.
[InstantiationException](../java/lang/InstantiationException.md) Thrown when an application tries to create an instance of a class using the `newInstance` method in class `Class`, but the specified class object cannot be instantiated.
[IntentFilter.MalformedMimeTypeException](../android/content/IntentFilter.MalformedMimeTypeException.md) This exception is thrown when a given MIME type does not have a valid syntax.
[IntentSender.SendIntentException](../android/content/IntentSender.SendIntentException.md) Exception thrown when trying to send through a PendingIntent that has been canceled or is otherwise no longer able to execute the request.
[InterruptedByTimeoutException](../java/nio/channels/InterruptedByTimeoutException.md) Checked exception received by a thread when a timeout elapses before an asynchronous operation completes.
[InterruptedIOException](../java/io/InterruptedIOException.md) Signals that an I/O operation has been interrupted.
[InvalidAlgorithmParameterException](../java/security/InvalidAlgorithmParameterException.md) This is the exception for invalid or inappropriate algorithm parameters.
[InvalidClassException](../java/io/InvalidClassException.md) Thrown when the Serialization runtime detects one of the following problems with a Class.
[InvalidEchDataException](../android/net/ssl/InvalidEchDataException.md) Exception thrown when the ECH (Encrypted Client Hello) data is empty or invalid.
[InvalidForegroundServiceTypeException](../android/app/InvalidForegroundServiceTypeException.md) Exception thrown when an app tries to start a foreground `https://developer.android.com/reference/kotlin/android/app/Service.html#` with an invalid type.
[InvalidKeException](../android/net/ipsec/ike/exceptions/InvalidKeException.md) This exception is thrown when the remote server expected a different Diffie-Hellman group.
[InvalidKeyException](../java/security/InvalidKeyException.md) This is the exception for invalid Keys (invalid encoding, wrong length, uninitialized, etc).
[InvalidKeySpecException](../java/security/spec/InvalidKeySpecException.md) This is the exception for invalid key specifications.
[InvalidMajorVersionException](../android/net/ipsec/ike/exceptions/InvalidMajorVersionException.md) This exception is thrown when major version of an inbound message is higher than 2.
[InvalidMarkException](../java/nio/InvalidMarkException.md) Unchecked exception thrown when an attempt is made to reset a buffer when its mark is not defined.
[InvalidObjectException](../java/io/InvalidObjectException.md) Indicates that one or more deserialized objects failed validation tests.
[InvalidParameterException](../java/security/InvalidParameterException.md) This exception, designed for use by the JCA/JCE engine classes, is thrown when an invalid parameter is passed to a method.
[InvalidParameterSpecException](../java/security/spec/InvalidParameterSpecException.md) This is the exception for invalid parameter specifications.
[InvalidPathException](../java/nio/file/InvalidPathException.md) Unchecked exception thrown when path string cannot be converted into a `https://developer.android.com/reference/kotlin/java/nio/file/Path.html#` because the path string contains invalid characters, or the path string is invalid for other file system specific reasons.
[InvalidPropertiesFormatException](../java/util/InvalidPropertiesFormatException.md) Thrown to indicate that an operation could not complete because the input did not conform to the appropriate XML document type for a collection of properties, as per the `https://developer.android.com/reference/kotlin/java/util/Properties.html#` specification.
[InvalidReaderSignatureException](../android/security/identity/InvalidReaderSignatureException.md) Thrown if the reader signature is invalid, or it doesn't contain a certificate chain, or if the signature failed to validate.
[InvalidRequestMessageException](../android/security/identity/InvalidRequestMessageException.md) Thrown if message with the request doesn't satisfy the requirements documented in `https://developer.android.com/reference/kotlin/android/security/identity/IdentityCredential.html#getEntries(kotlin.ByteArray,%20kotlin.collections.MutableMap,%20kotlin.ByteArray,%20kotlin.ByteArray)`.
[InvalidSelectorsException](../android/net/ipsec/ike/exceptions/InvalidSelectorsException.md) This exception is thrown if the remote server received an IPsec packet with mismatched selectors.
[InvocationTargetException](../java/lang/reflect/InvocationTargetException.md) InvocationTargetException is a checked exception that wraps an exception thrown by an invoked method or constructor.
[IpSecManager.ResourceUnavailableException](../android/net/IpSecManager.ResourceUnavailableException.md) Thrown to indicate that an IPsec resource is unavailable.
[IpSecManager.SpiUnavailableException](../android/net/IpSecManager.SpiUnavailableException.md) Thrown to indicate that a requested SPI is in use.
[JarException](../java/util/jar/JarException.md) Signals that an error of some sort has occurred while reading from or writing to a JAR file.
[KeyCharacterMap.UnavailableException](../android/view/KeyCharacterMap.UnavailableException.md) Thrown by `https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap.html#load(kotlin.Int)` when a key character map could not be loaded.
[KeyException](../java/security/KeyException.md) This is the basic key exception.
[KeyExpiredException](../android/security/keystore/KeyExpiredException.md) Indicates that a cryptographic operation failed because the employed key's validity end date is in the past.
[KeyManagementException](../java/security/KeyManagementException.md) This is the general key management exception for all operations dealing with key management.
[KeyNotYetValidException](../android/security/keystore/KeyNotYetValidException.md) Indicates that a cryptographic operation failed because the employed key's validity start date is in the future.
[KeyPermanentlyInvalidatedException](../android/security/keystore/KeyPermanentlyInvalidatedException.md) Indicates that the key can no longer be used because it has been permanently invalidated.
[KeyStoreException](../java/security/KeyStoreException.md) This is the generic KeyStore exception.
[LSException](../org/w3c/dom/ls/LSException.md) Parser or write operations may throw an `LSException` if the processing is stopped.
[LimitExceededException](../android/os/LimitExceededException.md) Indicates that the app has exceeded a limit set by the System.
[LoginException](../javax/security/auth/login/LoginException.md) This is the basic login exception.
[MalformedInputException](../java/nio/charset/MalformedInputException.md) Checked exception thrown when an input byte sequence is not legal for given charset, or an input character sequence is not a legal sixteen-bit Unicode sequence.
[MalformedJsonException](../android/util/MalformedJsonException.md) Thrown when a reader encounters malformed JSON.
[MalformedParameterizedTypeException](../java/lang/reflect/MalformedParameterizedTypeException.md) Thrown when a semantically malformed parameterized type is encountered by a reflective method that needs to instantiate it.
[MalformedParametersException](../java/lang/reflect/MalformedParametersException.md) Thrown when `https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#getParameters()` attempts to read method parameters from a class file and determines that one or more parameters are malformed.
[MalformedURLException](../java/net/MalformedURLException.md) Thrown to indicate that a malformed URL has occurred.
[MatchException](../java/lang/MatchException.md) Thrown to indicate an unexpected failure in pattern matching.
[MediaCasException.DeniedByServerException](../android/media/MediaCasException.DeniedByServerException.md) Exception thrown when the provisioning server or key server denies a license for a device.
[MediaCasException.InsufficientResourceException](../android/media/MediaCasException.InsufficientResourceException.md) Exception thrown when an operation on a MediaCas object is attempted and hardware resources are not sufficient to allocate, due to client's lower priority.
[MediaCasException.NotProvisionedException](../android/media/MediaCasException.NotProvisionedException.md) Exception thrown when an operation on a MediaCas object is attempted before it's provisioned successfully.
[MediaCasException.ResourceBusyException](../android/media/MediaCasException.ResourceBusyException.md) Exception thrown when an operation on a MediaCas object is attempted and hardware resources are not available, due to being in use.
[MediaCasException.UnsupportedCasException](../android/media/MediaCasException.UnsupportedCasException.md) Exception thrown when an attempt is made to construct a MediaCas object using a CA_system_id that is not supported by the device
[MediaCasStateException](../android/media/MediaCasStateException.md) Base class for MediaCas runtime exceptions
[MediaCodec.CodecException](../android/media/MediaCodec.CodecException.md) Thrown when an internal codec error occurs.
[MediaCodec.CryptoException](../android/media/MediaCodec.CryptoException.md) Thrown when a crypto error occurs while queueing a secure input buffer.
[MediaCodec.IncompatibleWithBlockModelException](../android/media/MediaCodec.IncompatibleWithBlockModelException.md) Thrown when the codec is configured for block model and an incompatible API is called.
[MediaCodec.InvalidBufferFlagsException](../android/media/MediaCodec.InvalidBufferFlagsException.md) Thrown when a buffer is marked with an invalid combination of flags (e.g. both
[MediaDrm.MediaDrmStateException](../android/media/MediaDrm.MediaDrmStateException.md) Thrown when a general failure occurs during a MediaDrm operation.
[MediaDrm.SessionException](../android/media/MediaDrm.SessionException.md) `https://developer.android.com/reference/kotlin/android/media/MediaDrm.SessionException.html#` is a misnomer because it may occur in methods **without** a session context.
[MediaDrmResetException](../android/media/MediaDrmResetException.md) This exception is thrown when the MediaDrm instance has become unusable due to a restart of the mediaserver process.
[MediaParser.ParsingException](../android/media/MediaParser.ParsingException.md) Thrown when an error occurs while parsing a media stream.
[MediaParser.UnrecognizedInputFormatException](../android/media/MediaParser.UnrecognizedInputFormatException.md) Thrown if all parser implementations provided to `https://developer.android.com/reference/kotlin/android/media/MediaParser.html#create(android.media.MediaParser.OutputConsumer,%20kotlin.String)` failed to sniff the input content.
[MediaPlayer.NoDrmSchemeException](../android/media/MediaPlayer.NoDrmSchemeException.md) Thrown when a DRM method is called before preparing a DRM scheme through prepareDrm().
[MediaPlayer.ProvisioningNetworkErrorException](../android/media/MediaPlayer.ProvisioningNetworkErrorException.md) Thrown when the device requires DRM provisioning but the provisioning attempt has failed due to a network error (Internet reachability, timeout, etc.).
[MediaPlayer.ProvisioningServerErrorException](../android/media/MediaPlayer.ProvisioningServerErrorException.md) Thrown when the device requires DRM provisioning but the provisioning attempt has failed due to the provisioning server denying the request.
[MessageDecryptionException](../android/security/identity/MessageDecryptionException.md) Thrown when failing to decrypt a message from the reader device.
[MissingForegroundServiceTypeException](../android/app/MissingForegroundServiceTypeException.md) Exception thrown when an app tries to start a foreground `https://developer.android.com/reference/kotlin/android/app/Service.html#` without a type.
[MissingFormatArgumentException](../java/util/MissingFormatArgumentException.md) Unchecked exception thrown when there is a format specifier which does not have a corresponding argument or if an argument index refers to an argument that does not exist.
[MissingFormatWidthException](../java/util/MissingFormatWidthException.md) Unchecked exception thrown when the format width is required.
[MissingResourceException](../java/util/MissingResourceException.md) Signals that a resource is missing.
[NegativeArraySizeException](../java/lang/NegativeArraySizeException.md) Thrown if an application tries to create an array with negative size.
[NetworkErrorException](../android/accounts/NetworkErrorException.md) <br />

[NetworkException](../android/net/http/NetworkException.md) Exception passed to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback.html#onFailed(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)` when the HTTP stack fails to process a network request.
[NetworkOnMainThreadException](../android/os/NetworkOnMainThreadException.md) The exception that is thrown when an application attempts to perform a networking operation on its main thread.
[NoAuthenticationKeyAvailableException](../android/security/identity/NoAuthenticationKeyAvailableException.md) Thrown if no dynamic authentication keys are available.
[NoConnectionPendingException](../java/nio/channels/NoConnectionPendingException.md) Unchecked exception thrown when the `https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel.html#finishConnect()` method of a `https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel.html#` is invoked without first successfully invoking its `https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel.html#connect(java.net.SocketAddress)` method.
[NoRouteToHostException](../java/net/NoRouteToHostException.md) Signals that an error occurred while attempting to connect a socket to a remote address and port.
[NoSuchAlgorithmException](../java/security/NoSuchAlgorithmException.md) This exception is thrown when a particular cryptographic algorithm is requested but is not available in the environment.
[NoSuchElementException](../java/util/NoSuchElementException.md) Thrown by various accessor methods to indicate that the element being requested does not exist.
[NoSuchFieldException](../java/lang/NoSuchFieldException.md) Signals that the class doesn't have a field of a specified name.
[NoSuchFileException](../java/nio/file/NoSuchFileException.md) Checked exception thrown when an attempt is made to access a file that does not exist.
[NoSuchMethodException](../java/lang/NoSuchMethodException.md) Thrown when a particular method cannot be found.
[NoSuchPaddingException](../javax/crypto/NoSuchPaddingException.md) This exception is thrown when a particular padding mechanism is requested but is not available in the environment.
[NoSuchPropertyException](../android/util/NoSuchPropertyException.md) Thrown when code requests a `https://developer.android.com/reference/kotlin/android/util/Property.html#` on a class that does not expose the appropriate method or field.
[NoSuchProviderException](../java/security/NoSuchProviderException.md) This exception is thrown when a particular security provider is requested but is not available in the environment.
[NonReadableChannelException](../java/nio/channels/NonReadableChannelException.md) Unchecked exception thrown when an attempt is made to read from a channel that was not originally opened for reading.
[NonWritableChannelException](../java/nio/channels/NonWritableChannelException.md) Unchecked exception thrown when an attempt is made to write to a channel that was not originally opened for writing.
[NotActiveException](../java/io/NotActiveException.md) Thrown when serialization or deserialization is not active.
[NotDirectoryException](../java/nio/file/NotDirectoryException.md) Checked exception thrown when a file system operation, intended for a directory, fails because the file is not a directory.
[NotLinkException](../java/nio/file/NotLinkException.md) Checked exception thrown when a file system operation fails because a file is not a symbolic link.
[NotProvisionedException](../android/media/NotProvisionedException.md) Exception thrown when an operation on a MediaDrm object is attempted and the device does not have a certificate.
[NotSerializableException](../java/io/NotSerializableException.md) Thrown when an instance is required to have a Serializable interface.
[NotYetBoundException](../java/nio/channels/NotYetBoundException.md) Unchecked exception thrown when an attempt is made to invoke an I/O operation upon a server socket channel that is not yet bound.
[NotYetConnectedException](../java/nio/channels/NotYetConnectedException.md) Unchecked exception thrown when an attempt is made to invoke an I/O operation upon a socket channel that is not yet connected.
[NullPointerException](../java/lang/NullPointerException.md) Thrown when an application attempts to use `null` in a case where an object is required.
[NumberFormatException](../java/lang/NumberFormatException.md) Thrown to indicate that the application has attempted to convert a string to one of the numeric types, but that the string does not have the appropriate format.
[ObjectStreamException](../java/io/ObjectStreamException.md) Superclass of all exceptions specific to Object Stream classes.
[OperationCanceledException](../android/os/OperationCanceledException.md) An exception type that is thrown when an operation in progress is canceled.
[OperationCanceledException](../android/accounts/OperationCanceledException.md) <br />

[OptionalDataException](../java/io/OptionalDataException.md) Exception indicating the failure of an object read operation due to unread primitive data, or the end of data belonging to a serialized object in the stream.
[OverlappingFileLockException](../java/nio/channels/OverlappingFileLockException.md) Unchecked exception thrown when an attempt is made to acquire a lock on a region of a file that overlaps a region already locked by the same Java virtual machine, or when another thread is already waiting to lock an overlapping region of the same file.
[PackageManager.NameNotFoundException](../android/content/pm/PackageManager.NameNotFoundException.md) This exception is thrown when a given package, application, or component name cannot be found.
[ParcelFileDescriptor.FileDescriptorDetachedException](../android/os/ParcelFileDescriptor.FileDescriptorDetachedException.md) Exception that indicates that the file descriptor was detached.
[ParcelFormatException](../android/os/ParcelFormatException.md) The contents of a Parcel (usually during unmarshalling) does not contain the expected data.
[ParseException](../android/net/ParseException.md) Thrown when parsing failed.
[PatternSyntaxException](../java/util/regex/PatternSyntaxException.md) Unchecked exception thrown to indicate a syntax error in a regular-expression pattern.
[PendingIntent.CanceledException](../android/app/PendingIntent.CanceledException.md) Exception thrown when trying to send through a PendingIntent that has been canceled or is otherwise no longer able to execute the request.
[PortUnreachableException](../java/net/PortUnreachableException.md) Signals that an ICMP Port Unreachable message has been received on a connected datagram.
[PropertyMapper.PropertyConflictException](../android/view/inspector/PropertyMapper.PropertyConflictException.md) Thrown from a map method if a property name is already mapped as different type.
[PropertyReader.PropertyTypeMismatchException](../android/view/inspector/PropertyReader.PropertyTypeMismatchException.md) Thrown if a client calls a typed read method for a property of a different type.
[ProtocolException](../java/net/ProtocolException.md) Thrown to indicate that there is an error in the underlying protocol, such as a TCP error.
[ProviderException](../java/security/ProviderException.md) A runtime exception for Provider exceptions (such as misconfiguration errors or unrecoverable internal errors), which may be subclassed by Providers to throw specialized, provider-specific runtime errors.
[ProviderMismatchException](../java/nio/file/ProviderMismatchException.md) Unchecked exception thrown when an attempt is made to invoke a method on an object created by one file system provider with a parameter created by a different file system provider.
[ProviderNotFoundException](../java/nio/file/ProviderNotFoundException.md) Runtime exception thrown when a provider of the required type cannot be found.
[QueryLocationException](../android/telecom/QueryLocationException.md) This class represents a set of exceptions that can occur when requesting a `https://developer.android.com/reference/kotlin/android/telecom/Connection.html#queryLocationForEmergency(kotlin.Long,%20kotlin.String,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`
[QuicException](../android/net/http/QuicException.md) Subclass of `https://developer.android.com/reference/kotlin/android/net/http/NetworkException.html#` which contains a detailed [QUIC](https://www.chromium.org/quic) error code from [QuicErrorCode](https://cs.chromium.org/search/?q=symbol:%5CbQuicErrorCode%5Cb).
[RSDriverException](../android/renderscript/RSDriverException.md) Base class for all exceptions thrown by the Android RenderScript
[RSIllegalArgumentException](../android/renderscript/RSIllegalArgumentException.md) Base class for all exceptions thrown by the Android RenderScript
[RSInvalidStateException](../android/renderscript/RSInvalidStateException.md) Base class for all exceptions thrown by the Android RenderScript
[RSRuntimeException](../android/renderscript/RSRuntimeException.md) Base class for all exceptions thrown by the Android RenderScript
[ReadOnlyBufferException](../java/nio/ReadOnlyBufferException.md) Unchecked exception thrown when a content-mutation method such as put or compact is invoked upon a read-only buffer.
[ReadOnlyFileSystemException](../java/nio/file/ReadOnlyFileSystemException.md) Unchecked exception thrown when an attempt is made to update an object associated with a `https://developer.android.com/reference/kotlin/java/nio/file/FileSystem.html#isReadOnly()` `FileSystem`.
[ReadPendingException](../java/nio/channels/ReadPendingException.md) Unchecked exception thrown when an attempt is made to read from an asynchronous socket channel and a previous read has not completed.
[ReceiverCallNotAllowedException](../android/content/ReceiverCallNotAllowedException.md) This exception is thrown from android.
[RecoverableSecurityException](../android/app/RecoverableSecurityException.md) Specialization of `https://developer.android.com/reference/kotlin/java/lang/SecurityException` that contains additional information about how to involve the end user to recover from the exception.
[RejectedExecutionException](../java/util/concurrent/RejectedExecutionException.md) Exception thrown by an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` when a task cannot be accepted for execution.
[RemoteException](../android/os/RemoteException.md) Parent exception for all Binder remote-invocation errors Note: not all exceptions from binder services will be subclasses of this.
[RemoteViews.ActionException](../android/widget/RemoteViews.ActionException.md) Exception to send when something goes wrong executing an action
[ResourceBusyException](../android/media/ResourceBusyException.md) Exception thrown when an operation on a MediaDrm object is attempted and hardware resources are not available, due to being in use.
[Resources.NotFoundException](../android/content/res/Resources.NotFoundException.md) This exception is thrown by the resource APIs when a requested resource can not be found.
[SAXNotRecognizedException](../org/xml/sax/SAXNotRecognizedException.md) Exception class for an unrecognized identifier.
[SAXNotSupportedException](../org/xml/sax/SAXNotSupportedException.md) Exception class for an unsupported operation.
[SAXParseException](../org/xml/sax/SAXParseException.md) Encapsulate an XML parse error or warning.
[SQLClientInfoException](../java/sql/SQLClientInfoException.md) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` is thrown when one or more client info properties could not be set on a `Connection`.
[SQLDataException](../java/sql/SQLDataException.md) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` thrown when the SQLState class value is '*22*', or under vendor-specified conditions.
[SQLException](../android/database/SQLException.md) An exception that indicates there was an error with SQL parsing or execution.
[SQLFeatureNotSupportedException](../java/sql/SQLFeatureNotSupportedException.md) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` thrown when the SQLState class value is '*0A*' ( the value is 'zero' A).
[SQLIntegrityConstraintViolationException](../java/sql/SQLIntegrityConstraintViolationException.md) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` thrown when the SQLState class value is '*23*', or under vendor-specified conditions.
[SQLInvalidAuthorizationSpecException](../java/sql/SQLInvalidAuthorizationSpecException.md) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` thrown when the SQLState class value is '*28*', or under vendor-specified conditions.
[SQLNonTransientConnectionException](../java/sql/SQLNonTransientConnectionException.md) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` thrown for the SQLState class value '*08*', or under vendor-specified conditions.
[SQLNonTransientException](../java/sql/SQLNonTransientException.md) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` thrown when an instance where a retry of the same operation would fail unless the cause of the `SQLException` is corrected.
[SQLRecoverableException](../java/sql/SQLRecoverableException.md) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` thrown in situations where a previously failed operation might be able to succeed if the application performs some recovery steps and retries the entire transaction or in the case of a distributed transaction, the transaction branch.
[SQLSyntaxErrorException](../java/sql/SQLSyntaxErrorException.md) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` thrown when the SQLState class value is '*42*', or under vendor-specified conditions.
[SQLTimeoutException](../java/sql/SQLTimeoutException.md) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` thrown when the timeout specified by `Statement` has expired.
[SQLTransactionRollbackException](../java/sql/SQLTransactionRollbackException.md) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` thrown when the SQLState class value is '*40*', or under vendor-specified conditions.
[SQLTransientConnectionException](../java/sql/SQLTransientConnectionException.md) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` for the SQLState class value '*08*', or under vendor-specified conditions.
[SQLTransientException](../java/sql/SQLTransientException.md) The subclass of `https://developer.android.com/reference/kotlin/java/sql/SQLException.html#` is thrown in situations where a previoulsy failed operation might be able to succeed when the operation is retried without any intervention by application-level functionality.
[SQLWarning](../java/sql/SQLWarning.md) An exception that provides information on database access warnings.
[SQLiteAbortException](../android/database/sqlite/SQLiteAbortException.md) An exception that indicates that the SQLite program was aborted.
[SQLiteAccessPermException](../android/database/sqlite/SQLiteAccessPermException.md) This exception class is used when sqlite can't access the database file due to lack of permissions on the file.
[SQLiteBindOrColumnIndexOutOfRangeException](../android/database/sqlite/SQLiteBindOrColumnIndexOutOfRangeException.md) Thrown if the bind or column parameter index is out of range.
[SQLiteBlobTooBigException](../android/database/sqlite/SQLiteBlobTooBigException.md) <br />

[SQLiteCantOpenDatabaseException](../android/database/sqlite/SQLiteCantOpenDatabaseException.md) <br />

[SQLiteConstraintException](../android/database/sqlite/SQLiteConstraintException.md) An exception that indicates that an integrity constraint was violated.
[SQLiteDatabaseCorruptException](../android/database/sqlite/SQLiteDatabaseCorruptException.md) An exception that indicates that the SQLite database file is corrupt.
[SQLiteDatabaseLockedException](../android/database/sqlite/SQLiteDatabaseLockedException.md) Thrown if the database engine was unable to acquire the database locks it needs to do its job.
[SQLiteDatatypeMismatchException](../android/database/sqlite/SQLiteDatatypeMismatchException.md) <br />

[SQLiteDiskIOException](../android/database/sqlite/SQLiteDiskIOException.md) Indicates that an IO error occurred while accessing the SQLite database file.
[SQLiteDoneException](../android/database/sqlite/SQLiteDoneException.md) An exception that indicates that the SQLite program is done.
[SQLiteException](../android/database/sqlite/SQLiteException.md) A SQLite exception that indicates there was an error with SQL parsing or execution.
[SQLiteFullException](../android/database/sqlite/SQLiteFullException.md) An exception that indicates that the SQLite database is full.
[SQLiteMisuseException](../android/database/sqlite/SQLiteMisuseException.md) This error can occur if the application creates a SQLiteStatement object and allows multiple threads in the application use it at the same time.
[SQLiteOutOfMemoryException](../android/database/sqlite/SQLiteOutOfMemoryException.md) <br />

[SQLiteReadOnlyDatabaseException](../android/database/sqlite/SQLiteReadOnlyDatabaseException.md) <br />

[SQLiteTableLockedException](../android/database/sqlite/SQLiteTableLockedException.md) <br />

[SSLException](../javax/net/ssl/SSLException.md) Indicates some kind of error detected by an SSL subsystem.
[SSLHandshakeException](../javax/net/ssl/SSLHandshakeException.md) Indicates that the client and server could not negotiate the desired level of security.
[SSLKeyException](../javax/net/ssl/SSLKeyException.md) Reports a bad SSL key.
[SSLPeerUnverifiedException](../javax/net/ssl/SSLPeerUnverifiedException.md) Indicates that the peer's identity has not been verified.
[SSLProtocolException](../javax/net/ssl/SSLProtocolException.md) Reports an error in the operation of the SSL protocol.
[SecureKeyImportUnavailableException](../android/security/keystore/SecureKeyImportUnavailableException.md) Indicates that the Keystore does not support securely importing wrapped keys.
[SecurityException](../java/lang/SecurityException.md) Thrown by the security manager to indicate a security violation.
[ServiceStartNotAllowedException](../android/app/ServiceStartNotAllowedException.md) Exception thrown when an app tries to start a `https://developer.android.com/reference/kotlin/android/app/Service.html#` when it's not allowed to do so.
[SessionTranscriptMismatchException](../android/security/identity/SessionTranscriptMismatchException.md) Thrown when trying use multiple different session transcripts in the same presentation session.
[Settings.SettingNotFoundException](../android/provider/Settings.SettingNotFoundException.md) <br />

[ShortBufferException](../javax/crypto/ShortBufferException.md) This exception is thrown when an output buffer provided by the user is too short to hold the operation result.
[ShutdownChannelGroupException](../java/nio/channels/ShutdownChannelGroupException.md) Unchecked exception thrown when an attempt is made to construct a channel in a group that is shutdown or the completion handler for an I/O operation cannot be invoked because the channel group has terminated.
[SignatureException](../java/security/SignatureException.md) This is the generic Signature exception.
[SkeletonSyntaxException](../android/icu/number/SkeletonSyntaxException.md) Exception used for illegal number skeleton strings.
[SocketException](../java/net/SocketException.md) Thrown to indicate that there is an error creating or accessing a Socket.
[SocketTimeoutException](../java/net/SocketTimeoutException.md) Signals that a timeout has occurred on a socket read or accept.
[StaleDataException](../android/database/StaleDataException.md) This exception is thrown when a Cursor contains stale data and must be requeried before being used again.
[StartForegroundCalledOnStoppedServiceException](../android/app/StartForegroundCalledOnStoppedServiceException.md) Exception thrown when android.
[StreamCorruptedException](../java/io/StreamCorruptedException.md) Thrown when control information that was read from an object stream violates internal consistency checks.
[StringIndexOutOfBoundsException](../java/lang/StringIndexOutOfBoundsException.md) Thrown by `String` methods to indicate that an index is either negative or greater than the size of the string.
[StringPrepParseException](../android/icu/text/StringPrepParseException.md) Exception that signals an error has occurred while parsing the input to StringPrep or IDNA.
[StrongBoxUnavailableException](../android/security/keystore/StrongBoxUnavailableException.md) Indicates that an operation could not be performed because the requested security hardware is not available.
[Surface.OutOfResourcesException](../android/view/Surface.OutOfResourcesException.md) Exception thrown when a Canvas couldn't be locked with `https://developer.android.com/reference/kotlin/android/view/Surface.html#lockCanvas(android.graphics.Rect)`, or when a SurfaceTexture could not successfully be allocated.
[SurfaceHolder.BadSurfaceTypeException](../android/view/SurfaceHolder.BadSurfaceTypeException.md) Exception that is thrown from #lockCanvas when called on a Surface whose type is SURFACE_TYPE_PUSH_BUFFERS.
[SyncFailedException](../java/io/SyncFailedException.md) Signals that a sync operation has failed.
[SystemUpdatePolicy.ValidationFailedException](../android/app/admin/SystemUpdatePolicy.ValidationFailedException.md) An exception class that represents various validation errors thrown from `https://developer.android.com/reference/kotlin/android/app/admin/SystemUpdatePolicy.html#setFreezePeriods(kotlin.collections.MutableList)` and `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#setSystemUpdatePolicy(android.content.ComponentName,%20android.app.admin.SystemUpdatePolicy)`
[TagLostException](../android/nfc/TagLostException.md) <br />

[TelephonyManager.ModemErrorException](../android/telephony/TelephonyManager.ModemErrorException.md) Exception that is supplied to the callback in `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#getNetworkSlicingConfiguration(java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` if the modem returned a failure.
[TelephonyManager.TimeoutException](../android/telephony/TelephonyManager.TimeoutException.md) Exception that is supplied to the callback in `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#getNetworkSlicingConfiguration(java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` if the system timed out waiting for a response from the Radio.
[TimeFormatException](../android/util/TimeFormatException.md) <br />

[TransactionTooLargeException](../android/os/TransactionTooLargeException.md) The Binder transaction failed because it was too large.
[TransformerConfigurationException](../javax/xml/transform/TransformerConfigurationException.md) Indicates a serious configuration error.
[TypeNotPresentException](../java/lang/TypeNotPresentException.md) Thrown when an application tries to access a type using a string representing the type's name, but no definition for the type with the specified name can be found.
[UTFDataFormatException](../java/io/UTFDataFormatException.md) Signals that a malformed string in [modified UTF-8](../java/io/DataInput.md) format has been read in a data input stream or by any class that implements the data input interface.
[UncheckedIOException](../java/io/UncheckedIOException.md) Wraps an `https://developer.android.com/reference/kotlin/java/io/IOException.html#` with an unchecked exception.
[UndeclaredThrowableException](../java/lang/reflect/UndeclaredThrowableException.md) Thrown by a method invocation on a proxy instance if its invocation handler's `https://developer.android.com/reference/kotlin/java/lang/reflect/InvocationHandler#invoke(kotlin.Any,%20java.lang.reflect.Method,%20kotlin.Array)` method throws a checked exception (a `Throwable` that is not assignable to `RuntimeException` or `Error`) that is not assignable to any of the exception types declared in the `throws` clause of the method that was invoked on the proxy instance and dispatched to the invocation handler.
[UnknownAuthenticationKeyException](../android/security/identity/UnknownAuthenticationKeyException.md) Thrown if trying to certify an unknown dynamic authentication key.
[UnknownFormatConversionException](../java/util/UnknownFormatConversionException.md) Unchecked exception thrown when an unknown conversion is given.
[UnknownFormatFlagsException](../java/util/UnknownFormatFlagsException.md) Unchecked exception thrown when an unknown flag is given.
[UnknownHostException](../java/net/UnknownHostException.md) Thrown to indicate that the IP address of a host could not be determined.
[UnknownServiceException](../java/net/UnknownServiceException.md) Thrown to indicate that an unknown service exception has occurred.
[UnmappableCharacterException](../java/nio/charset/UnmappableCharacterException.md) Checked exception thrown when an input character (or byte) sequence is valid but cannot be mapped to an output byte (or character) sequence.
[UnrecoverableEntryException](../java/security/UnrecoverableEntryException.md) This exception is thrown if an entry in the keystore cannot be recovered.
[UnrecoverableKeyException](../java/security/UnrecoverableKeyException.md) This exception is thrown if a key in the keystore cannot be recovered.
[UnresolvedAddressException](../java/nio/channels/UnresolvedAddressException.md) Unchecked exception thrown when an attempt is made to invoke a network operation upon an unresolved socket address.
[UnsafeStateException](../android/app/admin/UnsafeStateException.md) Exception thrown when a `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#` operation failed because it was not safe to be executed at that moment.
[UnsupportedAddressTypeException](../java/nio/channels/UnsupportedAddressTypeException.md) Unchecked exception thrown when an attempt is made to bind or connect to a socket address of a type that is not supported.
[UnsupportedCharsetException](../java/nio/charset/UnsupportedCharsetException.md) Unchecked exception thrown when no support is available for a requested charset.
[UnsupportedEncodingException](../java/io/UnsupportedEncodingException.md) The Character Encoding is not supported.
[UnsupportedOperationException](../java/lang/UnsupportedOperationException.md) Thrown to indicate that the requested operation is not supported.
[UnsupportedSchemeException](../android/media/UnsupportedSchemeException.md) Exception thrown when an attempt is made to construct a MediaDrm object using a crypto scheme UUID that is not supported by the device
[UnsupportedTemporalTypeException](../java/time/temporal/UnsupportedTemporalTypeException.md) UnsupportedTemporalTypeException indicates that a ChronoField or ChronoUnit is not supported for a Temporal class.
[UserManager.UserOperationException](../android/os/UserManager.UserOperationException.md) Thrown to indicate user operation failed.
[UserNotAuthenticatedException](../android/security/keystore/UserNotAuthenticatedException.md) Indicates that a cryptographic operation could not be performed because the user has not been authenticated recently enough.
[UserPresenceUnavailableException](../android/security/keystore/UserPresenceUnavailableException.md) Indicates the condition that a proof of user-presence was requested but this proof was not presented.
[UserPrincipalNotFoundException](../java/nio/file/attribute/UserPrincipalNotFoundException.md) Checked exception thrown when a lookup of `https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipal.html#` fails because the principal does not exist.
[VibrationEffect.VibrationParseException](../android/os/VibrationEffect.VibrationParseException.md) Exception thrown when parsing a vibration XML fails due to invalid format or values.
[WindowManager.BadTokenException](../android/view/WindowManager.BadTokenException.md) Exception that is thrown when trying to add view whose `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#` `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#token:android.os.IBinder` is invalid.
[WindowManager.InvalidDisplayException](../android/view/WindowManager.InvalidDisplayException.md) Exception that is thrown when calling `https://developer.android.com/reference/kotlin/android/view/ViewManager.html#addView(android.view.View,%20android.view.ViewGroup.LayoutParams)` to a secondary display that cannot be found.
[WriteAbortedException](../java/io/WriteAbortedException.md) Signals that one of the ObjectStreamExceptions was thrown during a write operation.
[WritePendingException](../java/nio/channels/WritePendingException.md) Unchecked exception thrown when an attempt is made to write to an asynchronous socket channel and a previous write has not completed.
[WrongMethodTypeException](../java/lang/invoke/WrongMethodTypeException.md) Thrown to indicate that code has attempted to call a method handle via the wrong method type.
[WrongThreadException](../java/lang/WrongThreadException.md) Thrown to indicate that a method has been called on the wrong thread.
[XPathExpressionException](../javax/xml/xpath/XPathExpressionException.md) `XPathExpressionException` represents an error in an XPath expression.
[XPathFactoryConfigurationException](../javax/xml/xpath/XPathFactoryConfigurationException.md) `XPathFactoryConfigurationException` represents a configuration error in a `XPathFactory` environment.
[XPathFunctionException](../javax/xml/xpath/XPathFunctionException.md) `XPathFunctionException` represents an error with an XPath function.
[ZipException](../java/util/zip/ZipException.md) Signals that a Zip exception of some sort has occurred.
[ZoneRulesException](../java/time/zone/ZoneRulesException.md) Thrown to indicate a problem with time-zone configuration.

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
| --- | --- |
| `writableStackTrace` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether or not the stack trace should be writable |
