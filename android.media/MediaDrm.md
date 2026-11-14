# MediaDrm

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaDrm

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaDrm "View this page in Java") 

```
class MediaDrm : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm#) |

MediaDrm can be used to obtain keys for decrypting protected media streams, in conjunction with [android.media.MediaCrypto](https://developer.android.com/reference/kotlin/android/media/MediaCrypto). The MediaDrm APIs are designed to support the ISO/IEC 23001-7: Common Encryption standard, but may also be used to implement other encryption schemes.

Encrypted content is prepared using an encryption server and stored in a content library. The encrypted content is streamed or downloaded from the content library to client devices via content servers. Licenses to view the content are obtained from a License Server.

<br />

<br />

Keys are requested from the license server using a key request. The key response is delivered to the client app, which provides the response to the MediaDrm API.

A Provisioning server may be required to distribute device-unique credentials to the devices.

Enforcing requirements related to the number of devices that may play content simultaneously can be performed either through key renewal or using the secure stop methods.

The following sequence diagram shows the interactions between the objects involved while playing back encrypted content:

<br />

<br />

The app first constructs [android.media.MediaExtractor](https://developer.android.com/reference/kotlin/android/media/MediaExtractor) and [android.media.MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec) objects. It accesses the DRM-scheme-identifying UUID, typically from metadata in the content, and uses this UUID to construct an instance of a MediaDrm object that is able to support the DRM scheme required by the content. Crypto schemes are assigned 16 byte UUIDs. The method #isCryptoSchemeSupported can be used to query if a given scheme is supported on the device.

The app calls #openSession to generate a sessionId that will uniquely identify the session in subsequent interactions. The app next uses the MediaDrm object to obtain a key request message and send it to the license server, then provide the server's response to the MediaDrm object.

Once the app has a sessionId, it can construct a MediaCrypto object from the UUID and sessionId. The MediaCrypto object is registered with the MediaCodec in the android.media.MediaCodec#configure method to enable the codec to decrypt content.

When the app has constructed [android.media.MediaExtractor](https://developer.android.com/reference/kotlin/android/media/MediaExtractor), [android.media.MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec) and [android.media.MediaCrypto](https://developer.android.com/reference/kotlin/android/media/MediaCrypto) objects, it proceeds to pull samples from the extractor and queue them into the decoder. For encrypted content, the samples returned from the extractor remain encrypted, they are only decrypted when the samples are delivered to the decoder.

MediaDrm methods throw [android.media.MediaDrm.MediaDrmStateException](https://developer.android.com/reference/kotlin/android/media/MediaDrm.MediaDrmStateException) when a method is called on a MediaDrm object that has had an unrecoverable failure in the DRM plugin or security hardware. [android.media.MediaDrm.MediaDrmStateException](https://developer.android.com/reference/kotlin/android/media/MediaDrm.MediaDrmStateException) extends [java.lang.IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) with the addition of a developer-readable diagnostic information string associated with the exception.

In the event of a mediaserver process crash or restart while a MediaDrm object is active, MediaDrm methods may throw [android.media.MediaDrmResetException](https://developer.android.com/reference/kotlin/android/media/MediaDrmResetException). To recover, the app must release the MediaDrm object, then create and initialize a new one.

As [android.media.MediaDrmResetException](https://developer.android.com/reference/kotlin/android/media/MediaDrmResetException) and [android.media.MediaDrm.MediaDrmStateException](https://developer.android.com/reference/kotlin/android/media/MediaDrm.MediaDrmStateException) both extend [java.lang.IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#), they should be in an earlier catch() block than [java.lang.IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) if handled separately.

### Callbacks

Applications should register for informational events in order to be informed of key state updates during playback or streaming. Registration for these events is done via a call to #setOnEventListener. In order to receive the respective callback associated with this listener, applications are required to create MediaDrm objects on a thread with its own Looper running (main UI thread by default has a Looper running).

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [CryptoSession](https://developer.android.com/reference/kotlin/android/media/MediaDrm.CryptoSession) In addition to supporting decryption of DASH Common Encrypted Media, the MediaDrm APIs provide the ability to securely deliver session keys from an operator's session key server to a client device, based on the factory-installed root of trust, and then perform encrypt, decrypt, sign and verify operations with the session key on arbitrary user data. |
| | [ErrorCodes](https://developer.android.com/reference/kotlin/android/media/MediaDrm.ErrorCodes) Error codes that may be returned from [android.media.MediaDrm.MediaDrmStateException#getErrorCode()](https://developer.android.com/reference/kotlin/android/media/MediaDrm.MediaDrmStateException#getErrorCode())and [android.media.MediaCodec.CryptoException#getErrorCode()](https://developer.android.com/reference/kotlin/android/media/MediaCodec.CryptoException#getErrorCode()) |
| | [KeyRequest](https://developer.android.com/reference/kotlin/android/media/MediaDrm.KeyRequest) Contains the opaque data an app uses to request keys from a license server. |
| | [KeyStatus](https://developer.android.com/reference/kotlin/android/media/MediaDrm.KeyStatus) Defines the status of a key. |
| | [LogMessage](https://developer.android.com/reference/kotlin/android/media/MediaDrm.LogMessage) A [LogMessage](https://developer.android.com/reference/kotlin/android/media/MediaDrm.LogMessage) records an event in the [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm#) framework or vendor plugin. |
| | [MediaDrmStateException](https://developer.android.com/reference/kotlin/android/media/MediaDrm.MediaDrmStateException) Thrown when a general failure occurs during a MediaDrm operation. |
| | [MetricsConstants](https://developer.android.com/reference/kotlin/android/media/MediaDrm.MetricsConstants) Definitions for the metrics that are reported via the [getMetrics](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getMetrics())call. |
| abstract | [OnEventListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnEventListener) Interface definition for a callback to be invoked when a drm event occurs |
| abstract | [OnExpirationUpdateListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnExpirationUpdateListener) Interface definition for a callback to be invoked when a drm session expiration update occurs |
| abstract | [OnKeyStatusChangeListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnKeyStatusChangeListener) Interface definition for a callback to be invoked when the keys in a drm session change states. |
| abstract | [OnSessionLostStateListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnSessionLostStateListener) Interface definition for a callback to be invoked when the session state has been lost and is now invalid |
| | [PlaybackComponent](https://developer.android.com/reference/kotlin/android/media/MediaDrm.PlaybackComponent) This class contains the Drm session ID and log session ID |
| | [ProvisionRequest](https://developer.android.com/reference/kotlin/android/media/MediaDrm.ProvisionRequest) Contains the opaque data an app uses to request a certificate from a provisioning server |
| | [SessionException](https://developer.android.com/reference/kotlin/android/media/MediaDrm.SessionException) [SessionException](https://developer.android.com/reference/kotlin/android/media/MediaDrm.SessionException) is a misnomer because it may occur in methods**without**a session context. |

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_KEY_EXPIRED](https://developer.android.com/reference/kotlin/android/media/MediaDrm#EVENT_KEY_EXPIRED:kotlin.Int) This event type indicates that the licensed usage duration for keys in a session has expired. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_KEY_REQUIRED](https://developer.android.com/reference/kotlin/android/media/MediaDrm#EVENT_KEY_REQUIRED:kotlin.Int) This event type indicates that the app needs to request keys from a license server. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_PROVISION_REQUIRED](https://developer.android.com/reference/kotlin/android/media/MediaDrm#EVENT_PROVISION_REQUIRED:kotlin.Int) This event type indicates that the app needs to request a certificate from the provisioning server. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_SESSION_RECLAIMED](https://developer.android.com/reference/kotlin/android/media/MediaDrm#EVENT_SESSION_RECLAIMED:kotlin.Int) This event indicates that a session opened by the app has been reclaimed by the resource manager. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_VENDOR_DEFINED](https://developer.android.com/reference/kotlin/android/media/MediaDrm#EVENT_VENDOR_DEFINED:kotlin.Int) This event may indicate some specific vendor-defined condition, see your DRM provider documentation for details |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HDCP_LEVEL_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MediaDrm#HDCP_LEVEL_UNKNOWN:kotlin.Int) The DRM plugin did not report an HDCP level, or an error occurred accessing it |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HDCP_NONE](https://developer.android.com/reference/kotlin/android/media/MediaDrm#HDCP_NONE:kotlin.Int) HDCP is not supported on this device, content is unprotected |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HDCP_NO_DIGITAL_OUTPUT](https://developer.android.com/reference/kotlin/android/media/MediaDrm#HDCP_NO_DIGITAL_OUTPUT:kotlin.Int) No digital output, implicitly secure |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HDCP_V1](https://developer.android.com/reference/kotlin/android/media/MediaDrm#HDCP_V1:kotlin.Int) HDCP version 1. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HDCP_V2](https://developer.android.com/reference/kotlin/android/media/MediaDrm#HDCP_V2:kotlin.Int) HDCP version 2. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HDCP_V2_1](https://developer.android.com/reference/kotlin/android/media/MediaDrm#HDCP_V2_1:kotlin.Int) HDCP version 2. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HDCP_V2_2](https://developer.android.com/reference/kotlin/android/media/MediaDrm#HDCP_V2_2:kotlin.Int) HDCP version 2. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HDCP_V2_3](https://developer.android.com/reference/kotlin/android/media/MediaDrm#HDCP_V2_3:kotlin.Int) HDCP version 2. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KEY_TYPE_OFFLINE](https://developer.android.com/reference/kotlin/android/media/MediaDrm#KEY_TYPE_OFFLINE:kotlin.Int) This key request type specifies that the keys will be for offline use, they will be saved to the device for use when the device is not connected to a network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KEY_TYPE_RELEASE](https://developer.android.com/reference/kotlin/android/media/MediaDrm#KEY_TYPE_RELEASE:kotlin.Int) This key request type specifies that previously saved offline keys should be released. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KEY_TYPE_STREAMING](https://developer.android.com/reference/kotlin/android/media/MediaDrm#KEY_TYPE_STREAMING:kotlin.Int) This key request type species that the keys will be for online use, they will not be saved to the device for subsequent use when the device is not connected to a network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OFFLINE_LICENSE_STATE_RELEASED](https://developer.android.com/reference/kotlin/android/media/MediaDrm#OFFLINE_LICENSE_STATE_RELEASED:kotlin.Int) Offline license is released, the keys have been marked for release using [getKeyRequest](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getKeyRequest(kotlin.ByteArray,%20kotlin.ByteArray,%20kotlin.String,%20kotlin.Int,%20java.util.HashMap))with KEY_TYPE_RELEASE but the key response has not been received. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OFFLINE_LICENSE_STATE_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MediaDrm#OFFLINE_LICENSE_STATE_UNKNOWN:kotlin.Int) Offline license state is unknown, an error occurred while trying to access it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OFFLINE_LICENSE_STATE_USABLE](https://developer.android.com/reference/kotlin/android/media/MediaDrm#OFFLINE_LICENSE_STATE_USABLE:kotlin.Int) Offline license is usable, the keys may be used for decryption. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PROPERTY_ALGORITHMS](https://developer.android.com/reference/kotlin/android/media/MediaDrm#PROPERTY_ALGORITHMS:kotlin.String) String property name: a comma-separated list of cipher and mac algorithms supported by CryptoSession. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PROPERTY_DESCRIPTION](https://developer.android.com/reference/kotlin/android/media/MediaDrm#PROPERTY_DESCRIPTION:kotlin.String) String property name: describes the DRM plugin |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PROPERTY_DEVICE_UNIQUE_ID](https://developer.android.com/reference/kotlin/android/media/MediaDrm#PROPERTY_DEVICE_UNIQUE_ID:kotlin.String) Byte array property name: the device unique identifier is established during device provisioning and provides a means of uniquely identifying each device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PROPERTY_VENDOR](https://developer.android.com/reference/kotlin/android/media/MediaDrm#PROPERTY_VENDOR:kotlin.String) String property name: identifies the maker of the DRM plugin |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PROPERTY_VERSION](https://developer.android.com/reference/kotlin/android/media/MediaDrm#PROPERTY_VERSION:kotlin.String) String property name: identifies the version of the DRM plugin |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_LEVEL_HW_SECURE_ALL](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_HW_SECURE_ALL:kotlin.Int) DRM key management, crypto operations, decoding of content and all handling of the media (compressed and uncompressed) is handled within a hardware backed trusted execution environment. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_LEVEL_HW_SECURE_CRYPTO](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_HW_SECURE_CRYPTO:kotlin.Int) DRM key management and crypto operations are performed within a hardware backed trusted execution environment. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_LEVEL_HW_SECURE_DECODE](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_HW_SECURE_DECODE:kotlin.Int) DRM key management, crypto operations and decoding of content are performed within a hardware backed trusted execution environment. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_LEVEL_SW_SECURE_CRYPTO](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_SW_SECURE_CRYPTO:kotlin.Int) DRM key management uses software-based whitebox crypto. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_LEVEL_SW_SECURE_DECODE](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_SW_SECURE_DECODE:kotlin.Int) DRM key management and decoding use software-based whitebox crypto. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECURITY_LEVEL_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_UNKNOWN:kotlin.Int) The DRM plugin did not report a security level, or an error occurred accessing it |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm#MediaDrm(java.util.UUID))`(`uuid:` ` [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)`)` Instantiate a MediaDrm object |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearOnEventListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm#clearOnEventListener())`()` Clear the [OnEventListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnEventListener). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearOnExpirationUpdateListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm#clearOnExpirationUpdateListener())`()` Clear the [OnExpirationUpdateListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnExpirationUpdateListener). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearOnKeyStatusChangeListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm#clearOnKeyStatusChangeListener())`()` Clear the [OnKeyStatusChangeListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnKeyStatusChangeListener). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearOnSessionLostStateListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm#clearOnSessionLostStateListener())`()` Clear the [OnSessionLostStateListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnSessionLostStateListener). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/media/MediaDrm#close())`()` Releases resources associated with the current session of MediaDrm. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [closeSession](https://developer.android.com/reference/kotlin/android/media/MediaDrm#closeSession(kotlin.ByteArray))`(`sessionId:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Close a session on the MediaDrm object that was previously opened with #openSession. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConnectedHdcpLevel](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getConnectedHdcpLevel())`()` Return the HDCP level negotiated with downstream receivers the device is connected to. |
| [MediaDrm.CryptoSession](https://developer.android.com/reference/kotlin/android/media/MediaDrm.CryptoSession)! | [getCryptoSession](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getCryptoSession(kotlin.ByteArray,%20kotlin.String,%20kotlin.String))`(`sessionId:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `cipherAlgorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `macAlgorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Obtain a CryptoSession object which can be used to encrypt, decrypt, sign and verify messages or data using the session keys established for the session using methods [getKeyRequest](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getKeyRequest(kotlin.ByteArray,%20kotlin.ByteArray,%20kotlin.String,%20kotlin.Int,%20java.util.HashMap))and [provideKeyResponse](https://developer.android.com/reference/kotlin/android/media/MediaDrm#provideKeyResponse(kotlin.ByteArray,%20kotlin.ByteArray))using a session key server. |
| [MediaDrm.KeyRequest](https://developer.android.com/reference/kotlin/android/media/MediaDrm.KeyRequest) | [getKeyRequest](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getKeyRequest(kotlin.ByteArray,%20kotlin.ByteArray,%20kotlin.String,%20kotlin.Int,%20java.util.HashMap))`(`scope:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `init:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `keyType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `optionalParameters:` ` [HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` A key request/response exchange occurs between the app and a license server to obtain or release keys used to decrypt encrypted content. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MediaDrm.LogMessage](https://developer.android.com/reference/kotlin/android/media/MediaDrm.LogMessage)!\> | [getLogMessages](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getLogMessages())`()` Returns recent [LogMessages](https://developer.android.com/reference/kotlin/android/media/MediaDrm.LogMessage) associated with this [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm#) instance. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxHdcpLevel](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getMaxHdcpLevel())`()` Return the maximum supported HDCP level. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxSecurityLevel](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getMaxSecurityLevel())`()` Returns a value that may be passed as a parameter to [openSession(int)](https://developer.android.com/reference/kotlin/android/media/MediaDrm#openSession(kotlin.Int))requesting that the session be opened at the maximum security level of the device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxSessionCount](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getMaxSessionCount())`()` Return the maximum number of MediaDrm sessions that may be opened simultaneosly among all MediaDrm instances for the active DRM scheme. |
| [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#)! | [getMetrics](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getMetrics())`()` Return Metrics data about the current MediaDrm instance. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\> | [getOfflineLicenseKeySetIds](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getOfflineLicenseKeySetIds())`()` The keys in an offline license allow protected content to be played even if the device is not connected to a network. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOfflineLicenseState](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getOfflineLicenseState(kotlin.ByteArray))`(`keySetId:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Request the state of an offline license. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOpenSessionCount](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getOpenSessionCount())`()` Return the number of MediaDrm sessions that are currently opened simultaneously among all MediaDrm instances for the active DRM scheme. |
| [MediaDrm.PlaybackComponent](https://developer.android.com/reference/kotlin/android/media/MediaDrm.PlaybackComponent)? | [getPlaybackComponent](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getPlaybackComponent(kotlin.ByteArray))`(`sessionId:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Obtain a [PlaybackComponent](https://developer.android.com/reference/kotlin/android/media/MediaDrm.PlaybackComponent) associated with a DRM session. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [getPropertyByteArray](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getPropertyByteArray(kotlin.String))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Read a MediaDrm byte array property value, given the property name string. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getPropertyString](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getPropertyString(kotlin.String))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Read a MediaDrm String property value, given the property name string. |
| [MediaDrm.ProvisionRequest](https://developer.android.com/reference/kotlin/android/media/MediaDrm.ProvisionRequest) | [getProvisionRequest](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getProvisionRequest())`()` A provision request/response exchange occurs between the app and a provisioning server to retrieve a device certificate. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [getSecureStop](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getSecureStop(kotlin.ByteArray))`(`ssid:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Access a specific secure stop given its secure stop ID. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\> | [getSecureStopIds](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getSecureStopIds())`()` Return a list of all secure stop IDs currently in persistent memory. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\> | [getSecureStops](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getSecureStops())`()` Secure stops are a way to enforce limits on the number of concurrent streams per subscriber across devices. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSecurityLevel](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getSecurityLevel(kotlin.ByteArray))`(`sessionId:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Return the current security level of a session. |
| static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)!\> | [getSupportedCryptoSchemes](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getSupportedCryptoSchemes())`()` <br /> |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCryptoSchemeSupported](https://developer.android.com/reference/kotlin/android/media/MediaDrm#isCryptoSchemeSupported(java.util.UUID))`(`uuid:` ` [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)`)` Query if the given scheme identified by its UUID is supported on this device. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCryptoSchemeSupported](https://developer.android.com/reference/kotlin/android/media/MediaDrm#isCryptoSchemeSupported(java.util.UUID,%20kotlin.String))`(`uuid:` ` [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Query if the given scheme identified by its UUID is supported on this device, and whether the DRM plugin is able to handle the media container format specified by mimeType. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCryptoSchemeSupported](https://developer.android.com/reference/kotlin/android/media/MediaDrm#isCryptoSchemeSupported(java.util.UUID,%20kotlin.String,%20kotlin.Int))`(`uuid:` ` [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `securityLevel:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Query if the given scheme identified by its UUID is supported on this device, and whether the DRM plugin is able to handle the media container format specified by mimeType at the requested security level. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [openSession](https://developer.android.com/reference/kotlin/android/media/MediaDrm#openSession())`()` Open a new session with the MediaDrm object. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [openSession](https://developer.android.com/reference/kotlin/android/media/MediaDrm#openSession(kotlin.Int))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Open a new session at a requested security level. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [provideKeyResponse](https://developer.android.com/reference/kotlin/android/media/MediaDrm#provideKeyResponse(kotlin.ByteArray,%20kotlin.ByteArray))`(`scope:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `response:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` A key response is received from the license server by the app, then it is provided to the MediaDrm instance using provideKeyResponse. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [provideProvisionResponse](https://developer.android.com/reference/kotlin/android/media/MediaDrm#provideProvisionResponse(kotlin.ByteArray))`(`response:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` After a provision response is received by the app, it is provided to the MediaDrm instance using this method. |
| [HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [queryKeyStatus](https://developer.android.com/reference/kotlin/android/media/MediaDrm#queryKeyStatus(kotlin.ByteArray))`(`sessionId:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Request an informative description of the key status for the session. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](https://developer.android.com/reference/kotlin/android/media/MediaDrm#release())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseAllSecureStops](https://developer.android.com/reference/kotlin/android/media/MediaDrm#releaseAllSecureStops())`()` Remove all secure stops without requiring a secure stop release message from the license server. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseSecureStops](https://developer.android.com/reference/kotlin/android/media/MediaDrm#releaseSecureStops(kotlin.ByteArray))`(`ssRelease:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Process the secure stop server response message ssRelease. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAllSecureStops](https://developer.android.com/reference/kotlin/android/media/MediaDrm#removeAllSecureStops())`()` Remove all secure stops without requiring a secure stop release message from the license server. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeKeys](https://developer.android.com/reference/kotlin/android/media/MediaDrm#removeKeys(kotlin.ByteArray))`(`sessionId:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Remove the current keys from a session. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeOfflineLicense](https://developer.android.com/reference/kotlin/android/media/MediaDrm#removeOfflineLicense(kotlin.ByteArray))`(`keySetId:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Normally offline licenses are released using a key request/response exchange using [getKeyRequest](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getKeyRequest(kotlin.ByteArray,%20kotlin.ByteArray,%20kotlin.String,%20kotlin.Int,%20java.util.HashMap))where the key type is KEY_TYPE_RELEASE, followed by [provideKeyResponse](https://developer.android.com/reference/kotlin/android/media/MediaDrm#provideKeyResponse(kotlin.ByteArray,%20kotlin.ByteArray)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeSecureStop](https://developer.android.com/reference/kotlin/android/media/MediaDrm#removeSecureStop(kotlin.ByteArray))`(`ssid:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Remove a specific secure stop without requiring a secure stop release message from the license server. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requiresSecureDecoder](https://developer.android.com/reference/kotlin/android/media/MediaDrm#requiresSecureDecoder(kotlin.String))`(`mime:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Query if the crypto scheme requires the use of a secure decoder to decode data of the given mime type at the default security level. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requiresSecureDecoder](https://developer.android.com/reference/kotlin/android/media/MediaDrm#requiresSecureDecoder(kotlin.String,%20kotlin.Int))`(`mime:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Query if the crypto scheme requires the use of a secure decoder to decode data of the given mime type at the given security level. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreKeys](https://developer.android.com/reference/kotlin/android/media/MediaDrm#restoreKeys(kotlin.ByteArray,%20kotlin.ByteArray))`(`sessionId:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `keySetId:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Restore persisted offline keys into a new session. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnEventListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm#setOnEventListener(android.media.MediaDrm.OnEventListener))`(`listener:` ` [MediaDrm.OnEventListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnEventListener)?`)` Register a callback to be invoked when an event occurs |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnEventListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm#setOnEventListener(android.media.MediaDrm.OnEventListener,%20android.os.Handler))`(`listener:` ` [MediaDrm.OnEventListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnEventListener)?`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?`)` Register a callback to be invoked when an event occurs |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnEventListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm#setOnEventListener(java.util.concurrent.Executor,%20android.media.MediaDrm.OnEventListener))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `listener:` ` [MediaDrm.OnEventListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnEventListener)`)` Register a callback to be invoked when an event occurs |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnExpirationUpdateListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm#setOnExpirationUpdateListener(android.media.MediaDrm.OnExpirationUpdateListener,%20android.os.Handler))`(`listener:` ` [MediaDrm.OnExpirationUpdateListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnExpirationUpdateListener)?`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?`)` Register a callback to be invoked when a session expiration update occurs. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnExpirationUpdateListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm#setOnExpirationUpdateListener(java.util.concurrent.Executor,%20android.media.MediaDrm.OnExpirationUpdateListener))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `listener:` ` [MediaDrm.OnExpirationUpdateListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnExpirationUpdateListener)`)` Register a callback to be invoked when a session expiration update occurs. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnKeyStatusChangeListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm#setOnKeyStatusChangeListener(android.media.MediaDrm.OnKeyStatusChangeListener,%20android.os.Handler))`(`listener:` ` [MediaDrm.OnKeyStatusChangeListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnKeyStatusChangeListener)?`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?`)` Register a callback to be invoked when the state of keys in a session change, e. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnKeyStatusChangeListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm#setOnKeyStatusChangeListener(java.util.concurrent.Executor,%20android.media.MediaDrm.OnKeyStatusChangeListener))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `listener:` ` [MediaDrm.OnKeyStatusChangeListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnKeyStatusChangeListener)`)` Register a callback to be invoked when the state of keys in a session change. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnSessionLostStateListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm#setOnSessionLostStateListener(android.media.MediaDrm.OnSessionLostStateListener,%20android.os.Handler))`(`listener:` ` [MediaDrm.OnSessionLostStateListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnSessionLostStateListener)?`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?`)` Register a callback to be invoked when session state has been lost. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnSessionLostStateListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm#setOnSessionLostStateListener(java.util.concurrent.Executor,%20android.media.MediaDrm.OnSessionLostStateListener))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `listener:` ` [MediaDrm.OnSessionLostStateListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnSessionLostStateListener)?`)` Register a callback to be invoked when session state has been lost. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPropertyByteArray](https://developer.android.com/reference/kotlin/android/media/MediaDrm#setPropertyByteArray(kotlin.String,%20kotlin.ByteArray))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Set a MediaDrm byte array property value, given the property name string and new value for the property. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPropertyString](https://developer.android.com/reference/kotlin/android/media/MediaDrm#setPropertyString(kotlin.String,%20kotlin.String))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Set a MediaDrm String property value, given the property name string and new value for the property. |

| Protected methods ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/media/MediaDrm#finalize())`()` <br /> |

## Constants

### EVENT_KEY_EXPIRED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_KEY_EXPIRED: Int
```

**Deprecated:** *Use [OnKeyStatusChangeListener.onKeyStatusChange](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnKeyStatusChangeListener#onKeyStatusChange(android.media.MediaDrm,%20kotlin.ByteArray,%20kotlin.collections.MutableList,%20kotlin.Boolean))and check for [MediaDrm.KeyStatus.STATUS_EXPIRED](https://developer.android.com/reference/kotlin/android/media/MediaDrm.KeyStatus#STATUS_EXPIRED:kotlin.Int) in the [MediaDrm.KeyStatus](https://developer.android.com/reference/kotlin/android/media/MediaDrm.KeyStatus) instead.*

This event type indicates that the licensed usage duration for keys in a session has expired. The keys are no longer valid. 

 Value: 3

### EVENT_KEY_REQUIRED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_KEY_REQUIRED: Int
```

This event type indicates that the app needs to request keys from a license server. The request message data is obtained using [getKeyRequest](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getKeyRequest(kotlin.ByteArray,%20kotlin.ByteArray,%20kotlin.String,%20kotlin.Int,%20java.util.HashMap)). 

 Value: 2

### EVENT_PROVISION_REQUIRED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_PROVISION_REQUIRED: Int
```

**Deprecated:** *Handle provisioning via [android.media.NotProvisionedException](https://developer.android.com/reference/kotlin/android/media/NotProvisionedException) instead.*

This event type indicates that the app needs to request a certificate from the provisioning server. The request message data is obtained using [getProvisionRequest](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getProvisionRequest()) 

 Value: 1

### EVENT_SESSION_RECLAIMED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_SESSION_RECLAIMED: Int
```

This event indicates that a session opened by the app has been reclaimed by the resource manager. 

 Value: 5

### EVENT_VENDOR_DEFINED

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_VENDOR_DEFINED: Int
```

This event may indicate some specific vendor-defined condition, see your DRM provider documentation for details 

 Value: 4

### HDCP_LEVEL_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HDCP_LEVEL_UNKNOWN: Int
```

The DRM plugin did not report an HDCP level, or an error occurred accessing it 

 Value: 0

### HDCP_NONE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HDCP_NONE: Int
```

HDCP is not supported on this device, content is unprotected 

 Value: 1

### HDCP_NO_DIGITAL_OUTPUT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HDCP_NO_DIGITAL_OUTPUT: Int
```

No digital output, implicitly secure 

 Value: 2147483647

### HDCP_V1

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HDCP_V1: Int
```

HDCP version 1.0 

 Value: 2

### HDCP_V2

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HDCP_V2: Int
```

HDCP version 2.0 Type 1. 

 Value: 3

### HDCP_V2_1

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HDCP_V2_1: Int
```

HDCP version 2.1 Type 1. 

 Value: 4

### HDCP_V2_2

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HDCP_V2_2: Int
```

HDCP version 2.2 Type 1. 

 Value: 5

### HDCP_V2_3

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HDCP_V2_3: Int
```

HDCP version 2.3 Type 1. 

 Value: 6

### KEY_TYPE_OFFLINE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_TYPE_OFFLINE: Int
```

This key request type specifies that the keys will be for offline use, they will be saved to the device for use when the device is not connected to a network. 

 Value: 2

### KEY_TYPE_RELEASE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_TYPE_RELEASE: Int
```

This key request type specifies that previously saved offline keys should be released. 

 Value: 3

### KEY_TYPE_STREAMING

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_TYPE_STREAMING: Int
```

This key request type species that the keys will be for online use, they will not be saved to the device for subsequent use when the device is not connected to a network. 

 Value: 1

### OFFLINE_LICENSE_STATE_RELEASED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OFFLINE_LICENSE_STATE_RELEASED: Int
```

Offline license is released, the keys have been marked for release using [getKeyRequest](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getKeyRequest(kotlin.ByteArray,%20kotlin.ByteArray,%20kotlin.String,%20kotlin.Int,%20java.util.HashMap))with KEY_TYPE_RELEASE but the key response has not been received. 

 Value: 2

### OFFLINE_LICENSE_STATE_UNKNOWN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OFFLINE_LICENSE_STATE_UNKNOWN: Int
```

Offline license state is unknown, an error occurred while trying to access it. 

 Value: 0

### OFFLINE_LICENSE_STATE_USABLE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OFFLINE_LICENSE_STATE_USABLE: Int
```

Offline license is usable, the keys may be used for decryption. 

 Value: 1

### PROPERTY_ALGORITHMS

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROPERTY_ALGORITHMS: String
```

String property name: a comma-separated list of cipher and mac algorithms supported by CryptoSession. The list may be empty if the DRM plugin does not support CryptoSession operations. 

 Value: "algorithms"

### PROPERTY_DESCRIPTION

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROPERTY_DESCRIPTION: String
```

String property name: describes the DRM plugin 

 Value: "description"

### PROPERTY_DEVICE_UNIQUE_ID

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROPERTY_DEVICE_UNIQUE_ID: String
```

Byte array property name: the device unique identifier is established during device provisioning and provides a means of uniquely identifying each device. 

 Value: "deviceUniqueId"

### PROPERTY_VENDOR

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROPERTY_VENDOR: String
```

String property name: identifies the maker of the DRM plugin 

 Value: "vendor"

### PROPERTY_VERSION

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROPERTY_VERSION: String
```

String property name: identifies the version of the DRM plugin 

 Value: "version"

### SECURITY_LEVEL_HW_SECURE_ALL

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_LEVEL_HW_SECURE_ALL: Int
```

DRM key management, crypto operations, decoding of content and all handling of the media (compressed and uncompressed) is handled within a hardware backed trusted execution environment. 

 Value: 5

### SECURITY_LEVEL_HW_SECURE_CRYPTO

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_LEVEL_HW_SECURE_CRYPTO: Int
```

DRM key management and crypto operations are performed within a hardware backed trusted execution environment. 

 Value: 3

### SECURITY_LEVEL_HW_SECURE_DECODE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_LEVEL_HW_SECURE_DECODE: Int
```

DRM key management, crypto operations and decoding of content are performed within a hardware backed trusted execution environment. 

 Value: 4

### SECURITY_LEVEL_SW_SECURE_CRYPTO

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_LEVEL_SW_SECURE_CRYPTO: Int
```

DRM key management uses software-based whitebox crypto. 

 Value: 1

### SECURITY_LEVEL_SW_SECURE_DECODE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_LEVEL_SW_SECURE_DECODE: Int
```

DRM key management and decoding use software-based whitebox crypto. 

 Value: 2

### SECURITY_LEVEL_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECURITY_LEVEL_UNKNOWN: Int
```

The DRM plugin did not report a security level, or an error occurred accessing it 

 Value: 0

## Public constructors

### MediaDrm

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MediaDrm(uuid: UUID)
```

Instantiate a MediaDrm object

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------|
| `uuid` | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#):The UUID of the crypto scheme. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------|
| `android.media.UnsupportedSchemeException` | if the device does not support the specified scheme UUID |

## Public methods

### clearOnEventListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clearOnEventListener(): Unit
```

Clear the [OnEventListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnEventListener). 

### clearOnExpirationUpdateListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clearOnExpirationUpdateListener(): Unit
```

Clear the [OnExpirationUpdateListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnExpirationUpdateListener). 

### clearOnKeyStatusChangeListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clearOnKeyStatusChangeListener(): Unit
```

Clear the [OnKeyStatusChangeListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnKeyStatusChangeListener). 

### clearOnSessionLostStateListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clearOnSessionLostStateListener(): Unit
```

Clear the [OnSessionLostStateListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnSessionLostStateListener). 

### close

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

Releases resources associated with the current session of MediaDrm. It is considered good practice to call this method when the [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm#) object is no longer needed in your application. After this method is called, [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm#) is no longer usable since it has lost all of its required resource. This method was added in API 28. In API versions 18 through 27, release() should be called instead. There is no need to do anything for API versions prior to 18.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |

### closeSession

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun closeSession(sessionId: ByteArray): Unit
```

Close a session on the MediaDrm object that was previously opened with #openSession.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------|
| `sessionId` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):This value cannot be`null`. |

### getConnectedHdcpLevel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnectedHdcpLevel(): Int
```

Return the HDCP level negotiated with downstream receivers the device is connected to. If multiple HDCP-capable displays are simultaneously connected to separate interfaces, this method returns the lowest negotiated level of all interfaces.

This method should only be used for informational purposes, not for enforcing compliance with HDCP requirements. Trusted enforcement of HDCP policies must be handled by the DRM system.

<br />

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the connected HDCP level Value is [android.media.MediaDrm#HDCP_LEVEL_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MediaDrm#HDCP_LEVEL_UNKNOWN:kotlin.Int), [android.media.MediaDrm#HDCP_NONE](https://developer.android.com/reference/kotlin/android/media/MediaDrm#HDCP_NONE:kotlin.Int), [android.media.MediaDrm#HDCP_V1](https://developer.android.com/reference/kotlin/android/media/MediaDrm#HDCP_V1:kotlin.Int), [android.media.MediaDrm#HDCP_V2](https://developer.android.com/reference/kotlin/android/media/MediaDrm#HDCP_V2:kotlin.Int), [android.media.MediaDrm#HDCP_V2_1](https://developer.android.com/reference/kotlin/android/media/MediaDrm#HDCP_V2_1:kotlin.Int), [android.media.MediaDrm#HDCP_V2_2](https://developer.android.com/reference/kotlin/android/media/MediaDrm#HDCP_V2_2:kotlin.Int), [android.media.MediaDrm#HDCP_V2_3](https://developer.android.com/reference/kotlin/android/media/MediaDrm#HDCP_V2_3:kotlin.Int), or [android.media.MediaDrm#HDCP_NO_DIGITAL_OUTPUT](https://developer.android.com/reference/kotlin/android/media/MediaDrm#HDCP_NO_DIGITAL_OUTPUT:kotlin.Int) |

### getCryptoSession

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCryptoSession(
    sessionId: ByteArray, 
    cipherAlgorithm: String, 
    macAlgorithm: String
): MediaDrm.CryptoSession!
```

Obtain a CryptoSession object which can be used to encrypt, decrypt, sign and verify messages or data using the session keys established for the session using methods [getKeyRequest](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getKeyRequest(kotlin.ByteArray,%20kotlin.ByteArray,%20kotlin.String,%20kotlin.Int,%20java.util.HashMap))and [provideKeyResponse](https://developer.android.com/reference/kotlin/android/media/MediaDrm#provideKeyResponse(kotlin.ByteArray,%20kotlin.ByteArray))using a session key server.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionId` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the session ID for the session containing keys to be used for encrypt, decrypt, sign and/or verify This value cannot be`null`. |
| `cipherAlgorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the algorithm to use for encryption and decryption ciphers. The algorithm string conforms to JCA Standard Names for Cipher Transforms and is case insensitive. For example "AES/CBC/NoPadding". This value cannot be`null`. |
| `macAlgorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the algorithm to use for sign and verify The algorithm string conforms to JCA Standard Names for Mac Algorithms and is case insensitive. For example "HmacSHA256". The list of supported algorithms for a DRM plugin can be obtained using the method [getPropertyString](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getPropertyString(kotlin.String))with the property name "algorithms". This value cannot be`null`. |

### getKeyRequest

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getKeyRequest(
    scope: ByteArray, 
    init: ByteArray?, 
    mimeType: String?, 
    keyType: Int, 
    optionalParameters: HashMap<String!, String!>?
): MediaDrm.KeyRequest
```

A key request/response exchange occurs between the app and a license server to obtain or release keys used to decrypt encrypted content.

getKeyRequest() is used to obtain an opaque key request byte array that is delivered to the license server. The opaque key request byte array is returned in KeyRequest.data. The recommended URL to deliver the key request to is returned in KeyRequest.defaultUrl.

After the app has received the key request response from the server, it should deliver to the response to the MediaDrm instance using the method [provideKeyResponse](https://developer.android.com/reference/kotlin/android/media/MediaDrm#provideKeyResponse(kotlin.ByteArray,%20kotlin.ByteArray)).

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `scope` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):may be a sessionId or a keySetId, depending on the specified keyType. When the keyType is KEY_TYPE_STREAMING or KEY_TYPE_OFFLINE, scope should be set to the sessionId the keys will be provided to. When the keyType is KEY_TYPE_RELEASE, scope should be set to the keySetId of the keys being released. Releasing keys from a device invalidates them for all sessions. This value cannot be`null`. |
| `init` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:container-specific data, its meaning is interpreted based on the mime type provided in the mimeType parameter. It could contain, for example, the content ID, key ID or other data obtained from the content metadata that is required in generating the key request. May be null when keyType is KEY_TYPE_RELEASE or if the request is a renewal, i.e. not the first key request for the session. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:identifies the mime type of the content. May be null if the keyType is KEY_TYPE_RELEASE or if the request is a renewal, i.e. not the first key request for the session. |
| `keyType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):specifes the type of the request. The request may be to acquire keys for streaming or offline content, or to release previously acquired keys, which are identified by a keySetId. Value is [android.media.MediaDrm#KEY_TYPE_STREAMING](https://developer.android.com/reference/kotlin/android/media/MediaDrm#KEY_TYPE_STREAMING:kotlin.Int), [android.media.MediaDrm#KEY_TYPE_OFFLINE](https://developer.android.com/reference/kotlin/android/media/MediaDrm#KEY_TYPE_OFFLINE:kotlin.Int), or [android.media.MediaDrm#KEY_TYPE_RELEASE](https://developer.android.com/reference/kotlin/android/media/MediaDrm#KEY_TYPE_RELEASE:kotlin.Int) |
| `optionalParameters` | [HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:are included in the key request message to allow a client application to provide additional message parameters to the server. This may be`null`if no additional parameters are to be sent. |

| Return ||
|---------------------------------------------------------------------------------------------------------|-----------------------------|
| [MediaDrm.KeyRequest](https://developer.android.com/reference/kotlin/android/media/MediaDrm.KeyRequest) | This value cannot be`null`. |

| Exceptions ||
|-----------------------------------------|--------------------------------------------------------------------|
| `android.media.NotProvisionedException` | if reprovisioning is needed, due to a problem with the certificate |

### getLogMessages

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLogMessages(): MutableList<MediaDrm.LogMessage!>
```

Returns recent [LogMessages](https://developer.android.com/reference/kotlin/android/media/MediaDrm.LogMessage) associated with this [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm#) instance.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MediaDrm.LogMessage](https://developer.android.com/reference/kotlin/android/media/MediaDrm.LogMessage)!> | This value cannot be`null`. |

### getMaxHdcpLevel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxHdcpLevel(): Int
```

Return the maximum supported HDCP level. The maximum HDCP level is a constant for a given device, it does not depend on downstream receivers that may be connected. If multiple HDCP-capable interfaces are present, it indicates the highest of the maximum HDCP levels of all interfaces.

<br />

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum supported HDCP level Value is [android.media.MediaDrm#HDCP_LEVEL_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MediaDrm#HDCP_LEVEL_UNKNOWN:kotlin.Int), [android.media.MediaDrm#HDCP_NONE](https://developer.android.com/reference/kotlin/android/media/MediaDrm#HDCP_NONE:kotlin.Int), [android.media.MediaDrm#HDCP_V1](https://developer.android.com/reference/kotlin/android/media/MediaDrm#HDCP_V1:kotlin.Int), [android.media.MediaDrm#HDCP_V2](https://developer.android.com/reference/kotlin/android/media/MediaDrm#HDCP_V2:kotlin.Int), [android.media.MediaDrm#HDCP_V2_1](https://developer.android.com/reference/kotlin/android/media/MediaDrm#HDCP_V2_1:kotlin.Int), [android.media.MediaDrm#HDCP_V2_2](https://developer.android.com/reference/kotlin/android/media/MediaDrm#HDCP_V2_2:kotlin.Int), [android.media.MediaDrm#HDCP_V2_3](https://developer.android.com/reference/kotlin/android/media/MediaDrm#HDCP_V2_3:kotlin.Int), or [android.media.MediaDrm#HDCP_NO_DIGITAL_OUTPUT](https://developer.android.com/reference/kotlin/android/media/MediaDrm#HDCP_NO_DIGITAL_OUTPUT:kotlin.Int) |

### getMaxSecurityLevel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getMaxSecurityLevel(): Int
```

Returns a value that may be passed as a parameter to [openSession(int)](https://developer.android.com/reference/kotlin/android/media/MediaDrm#openSession(kotlin.Int))requesting that the session be opened at the maximum security level of the device. This security level is only valid for the application running on the physical Android device (e.g. [android.content.Context#DEVICE_ID_DEFAULT](https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_ID_DEFAULT:kotlin.Int)). While running on a [android.companion.virtual.VirtualDevice](https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice.html#) the maximum supported security level might be different. 

### getMaxSessionCount

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxSessionCount(): Int
```

Return the maximum number of MediaDrm sessions that may be opened simultaneosly among all MediaDrm instances for the active DRM scheme. The maximum number of sessions is not affected by any sessions that may have already been opened.

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | maximum sessions. |

### getMetrics

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMetrics(): PersistableBundle!
```

Return Metrics data about the current MediaDrm instance.

| Return ||
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#)! | a [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#) containing the set of attributes and values available for this instance of MediaDrm. The attributes are described in [MetricsConstants](https://developer.android.com/reference/kotlin/android/media/MediaDrm.MetricsConstants). Additional vendor-specific fields may also be present in the return value. |

### getOfflineLicenseKeySetIds

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOfflineLicenseKeySetIds(): MutableList<ByteArray!>
```

The keys in an offline license allow protected content to be played even if the device is not connected to a network. Offline licenses are stored on the device after a key request/response exchange when the key request KeyType is OFFLINE. Normally each app is responsible for keeping track of the keySetIds it has created. If an app loses the keySetId for any stored licenses that it created, however, it must be able to recover the stored keySetIds so those licenses can be removed when they expire or when the app is uninstalled.

This method returns a list of the keySetIds for all offline licenses. The offline license keySetId may be used to query the status of an offline license with [getOfflineLicenseState](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getOfflineLicenseState(kotlin.ByteArray))or remove it with [removeOfflineLicense](https://developer.android.com/reference/kotlin/android/media/MediaDrm#removeOfflineLicense(kotlin.ByteArray)).

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!> | a list of offline license keySetIds This value cannot be`null`. |

### getOfflineLicenseState

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOfflineLicenseState(keySetId: ByteArray): Int
```

Request the state of an offline license. An offline license may be usable or inactive. The keys in a usable offline license are available for decryption. When the offline license state is inactive, the keys have been marked for release using [getKeyRequest](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getKeyRequest(kotlin.ByteArray,%20kotlin.ByteArray,%20kotlin.String,%20kotlin.Int,%20java.util.HashMap))with KEY_TYPE_RELEASE but the key response has not been received. The keys in an inactive offline license are not usable for decryption.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `keySetId` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):selects the offline license This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the offline license state Value is [android.media.MediaDrm#OFFLINE_LICENSE_STATE_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MediaDrm#OFFLINE_LICENSE_STATE_UNKNOWN:kotlin.Int), [android.media.MediaDrm#OFFLINE_LICENSE_STATE_USABLE](https://developer.android.com/reference/kotlin/android/media/MediaDrm#OFFLINE_LICENSE_STATE_USABLE:kotlin.Int), or [android.media.MediaDrm#OFFLINE_LICENSE_STATE_RELEASED](https://developer.android.com/reference/kotlin/android/media/MediaDrm#OFFLINE_LICENSE_STATE_RELEASED:kotlin.Int) |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the keySetId does not refer to an offline license. |

### getOpenSessionCount

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOpenSessionCount(): Int
```

Return the number of MediaDrm sessions that are currently opened simultaneously among all MediaDrm instances for the active DRM scheme.

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of open sessions. |

### getPlaybackComponent

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPlaybackComponent(sessionId: ByteArray): MediaDrm.PlaybackComponent?
```

Obtain a [PlaybackComponent](https://developer.android.com/reference/kotlin/android/media/MediaDrm.PlaybackComponent) associated with a DRM session. Call [PlaybackComponent.setLogSessionId(LogSessionId)](https://developer.android.com/reference/kotlin/android/media/MediaDrm.PlaybackComponent#setLogSessionId(android.media.metrics.LogSessionId))on the returned object to associate a playback session with the DRM session.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionId` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):a DRM session ID obtained from [openSession()](https://developer.android.com/reference/kotlin/android/media/MediaDrm#openSession())This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MediaDrm.PlaybackComponent](https://developer.android.com/reference/kotlin/android/media/MediaDrm.PlaybackComponent)? | a [PlaybackComponent](https://developer.android.com/reference/kotlin/android/media/MediaDrm.PlaybackComponent) associated with the session, or`null`if the session is closed or does not exist. |

**See Also**

- [android.media.MediaDrm.PlaybackComponent](https://developer.android.com/reference/kotlin/android/media/MediaDrm.PlaybackComponent) 

### getPropertyByteArray

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPropertyByteArray(propertyName: String!): ByteArray
```

Read a MediaDrm byte array property value, given the property name string.

Standard fields names are [PROPERTY_DEVICE_UNIQUE_ID](https://developer.android.com/reference/kotlin/android/media/MediaDrm#PROPERTY_DEVICE_UNIQUE_ID:kotlin.String)

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | This value cannot be`null`. |

### getPropertyString

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPropertyString(propertyName: String): String
```

Read a MediaDrm String property value, given the property name string.

Standard fields names are: [PROPERTY_VENDOR](https://developer.android.com/reference/kotlin/android/media/MediaDrm#PROPERTY_VENDOR:kotlin.String), [PROPERTY_VERSION](https://developer.android.com/reference/kotlin/android/media/MediaDrm#PROPERTY_VERSION:kotlin.String), [PROPERTY_DESCRIPTION](https://developer.android.com/reference/kotlin/android/media/MediaDrm#PROPERTY_DESCRIPTION:kotlin.String), [PROPERTY_ALGORITHMS](https://developer.android.com/reference/kotlin/android/media/MediaDrm#PROPERTY_ALGORITHMS:kotlin.String)

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getProvisionRequest

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProvisionRequest(): MediaDrm.ProvisionRequest
```

A provision request/response exchange occurs between the app and a provisioning server to retrieve a device certificate. If provisioning is required, the EVENT_PROVISION_REQUIRED event will be sent to the event handler. getProvisionRequest is used to obtain the opaque provision request byte array that should be delivered to the provisioning server. The provision request byte array is returned in ProvisionRequest.data. The recommended URL to deliver the provision request to is returned in ProvisionRequest.defaultUrl.

| Return ||
|---------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MediaDrm.ProvisionRequest](https://developer.android.com/reference/kotlin/android/media/MediaDrm.ProvisionRequest) | This value cannot be`null`. |

### getSecureStop

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSecureStop(ssid: ByteArray): ByteArray
```

**Deprecated:** *This method is deprecated and may be removed in a future release. Use renewals by calling [getKeyRequest](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getKeyRequest(kotlin.ByteArray,%20kotlin.ByteArray,%20kotlin.String,%20kotlin.Int,%20java.util.HashMap))to track concurrent playback. See additional information in [getSecureStops](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getSecureStops())*

Access a specific secure stop given its secure stop ID. Each secure stop has a unique ID.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ssid` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the ID of the secure stop to return This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | the secure stop identified by ssid This value cannot be`null`. |

### getSecureStopIds

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSecureStopIds(): MutableList<ByteArray!>
```

**Deprecated:** *This method is deprecated and may be removed in a future release. Use renewals by calling [getKeyRequest](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getKeyRequest(kotlin.ByteArray,%20kotlin.ByteArray,%20kotlin.String,%20kotlin.Int,%20java.util.HashMap))to track concurrent playback. See additional information in [getSecureStops](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getSecureStops())*

Return a list of all secure stop IDs currently in persistent memory. The secure stop ID can be used to access or remove the corresponding secure stop.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!> | a list of secure stop IDs This value cannot be`null`. |

### getSecureStops

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSecureStops(): MutableList<ByteArray!>
```

**Deprecated:** *This method is deprecated and may be removed in a future release. Secure stops are a way to enforce limits on the number of concurrent streams per subscriber across devices. They provide secure monitoring of the lifetime of content decryption keys in MediaDrm sessions. Limits on concurrent streams may also be enforced by periodically renewing licenses. This can be achieved by calling [getKeyRequest](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getKeyRequest(kotlin.ByteArray,%20kotlin.ByteArray,%20kotlin.String,%20kotlin.Int,%20java.util.HashMap))to initiate a renewal. MediaDrm users should transition away from secure stops to periodic renewals.*

Secure stops are a way to enforce limits on the number of concurrent streams per subscriber across devices. They provide secure monitoring of the lifetime of content decryption keys in MediaDrm sessions.

A secure stop is written to secure persistent memory when keys are loaded into a MediaDrm session. The secure stop state indicates that the keys are available for use. When playback completes and the keys are removed or the session is destroyed, the secure stop state is updated to indicate that keys are no longer usable.

After playback, the app can query the secure stop and send it in a message to the license server confirming that the keys are no longer active. The license server returns a secure stop release response message to the app which then deletes the secure stop from persistent memory using [releaseSecureStops](https://developer.android.com/reference/kotlin/android/media/MediaDrm#releaseSecureStops(kotlin.ByteArray)).

Each secure stop has a unique ID that can be used to identify it during enumeration, access and removal.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!> | a list of all secure stops from secure persistent memory This value cannot be`null`. |

### getSecurityLevel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSecurityLevel(sessionId: ByteArray): Int
```

Return the current security level of a session. A session has an initial security level determined by the robustness of the DRM system's implementation on the device. The security level may be changed at the time a session is opened using #openSession.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionId` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the session to query. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the security level of the session Value is [android.media.MediaDrm#SECURITY_LEVEL_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_UNKNOWN:kotlin.Int), [android.media.MediaDrm#SECURITY_LEVEL_SW_SECURE_CRYPTO](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_SW_SECURE_CRYPTO:kotlin.Int), [android.media.MediaDrm#SECURITY_LEVEL_SW_SECURE_DECODE](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_SW_SECURE_DECODE:kotlin.Int), [android.media.MediaDrm#SECURITY_LEVEL_HW_SECURE_CRYPTO](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_HW_SECURE_CRYPTO:kotlin.Int), [android.media.MediaDrm#SECURITY_LEVEL_HW_SECURE_DECODE](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_HW_SECURE_DECODE:kotlin.Int), or [android.media.MediaDrm#SECURITY_LEVEL_HW_SECURE_ALL](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_HW_SECURE_ALL:kotlin.Int) |

### getSupportedCryptoSchemes

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getSupportedCryptoSchemes(): MutableList<UUID!>
```

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)!> | list of crypto schemes (as [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#) s) for which [isCryptoSchemeSupported(java.util.UUID)](https://developer.android.com/reference/kotlin/android/media/MediaDrm#isCryptoSchemeSupported(java.util.UUID))returns true; each [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#) can be used as input to create [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm#) objects via [MediaDrm(java.util.UUID)](https://developer.android.com/reference/kotlin/android/media/MediaDrm#MediaDrm(java.util.UUID)). This value cannot be`null`. |

### isCryptoSchemeSupported

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isCryptoSchemeSupported(uuid: UUID): Boolean
```

Query if the given scheme identified by its UUID is supported on this device.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------|
| `uuid` | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#):The UUID of the crypto scheme. This value cannot be`null`. |

### isCryptoSchemeSupported

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isCryptoSchemeSupported(
    uuid: UUID, 
    mimeType: String
): Boolean
```

Query if the given scheme identified by its UUID is supported on this device, and whether the DRM plugin is able to handle the media container format specified by mimeType.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uuid` | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#):The UUID of the crypto scheme. This value cannot be`null`. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The MIME type of the media container, e.g. "video/mp4" or "video/webm" This value cannot be`null`. |

### isCryptoSchemeSupported

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isCryptoSchemeSupported(
    uuid: UUID, 
    mimeType: String, 
    securityLevel: Int
): Boolean
```

Query if the given scheme identified by its UUID is supported on this device, and whether the DRM plugin is able to handle the media container format specified by mimeType at the requested security level. Calling this method while the application is running on the physical Android device or a [android.companion.virtual.VirtualDevice](https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice.html#) may lead to different results, based on the different DRM capabilities of the devices.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uuid` | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#):The UUID of the crypto scheme. This value cannot be`null`. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The MIME type of the media container, e.g. "video/mp4" or "video/webm" This value cannot be`null`. |
| `securityLevel` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the security level requested Value is [android.media.MediaDrm#SECURITY_LEVEL_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_UNKNOWN:kotlin.Int), [android.media.MediaDrm#SECURITY_LEVEL_SW_SECURE_CRYPTO](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_SW_SECURE_CRYPTO:kotlin.Int), [android.media.MediaDrm#SECURITY_LEVEL_SW_SECURE_DECODE](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_SW_SECURE_DECODE:kotlin.Int), [android.media.MediaDrm#SECURITY_LEVEL_HW_SECURE_CRYPTO](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_HW_SECURE_CRYPTO:kotlin.Int), [android.media.MediaDrm#SECURITY_LEVEL_HW_SECURE_DECODE](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_HW_SECURE_DECODE:kotlin.Int), or [android.media.MediaDrm#SECURITY_LEVEL_HW_SECURE_ALL](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_HW_SECURE_ALL:kotlin.Int) |

### openSession

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openSession(): ByteArray
```

Open a new session with the MediaDrm object. A session ID is returned. By default, sessions are opened at the native security level of the device. If the application is currently running on a [android.companion.virtual.VirtualDevice](https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice.html#) the security level will be adjusted accordingly to the maximum supported level for the display.

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | This value cannot be`null`. |

| Exceptions ||
|-----------------------------------------|----------------------------------|
| `android.media.NotProvisionedException` | if provisioning is needed |
| `android.media.ResourceBusyException` | if required resources are in use |

### openSession

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openSession(level: Int): ByteArray
```

Open a new session at a requested security level. The security level represents the robustness of the device's DRM implementation. By default, sessions are opened at the native security level of the device. Overriding the security level is necessary when the decrypted frames need to be manipulated, such as for image compositing. The security level parameter must be lower than the native level. Reducing the security level will typically limit the content to lower resolutions, as determined by the license policy. If the requested level is not supported, the next lower supported security level will be set. The level can be queried using [getSecurityLevel](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getSecurityLevel(kotlin.ByteArray)). A session ID is returned. If the application is currently running on a [android.companion.virtual.VirtualDevice](https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice.html#) the security level will be adjusted accordingly to the maximum supported level for the display.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new security level Value is [android.media.MediaDrm#SECURITY_LEVEL_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_UNKNOWN:kotlin.Int), [android.media.MediaDrm#SECURITY_LEVEL_SW_SECURE_CRYPTO](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_SW_SECURE_CRYPTO:kotlin.Int), [android.media.MediaDrm#SECURITY_LEVEL_SW_SECURE_DECODE](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_SW_SECURE_DECODE:kotlin.Int), [android.media.MediaDrm#SECURITY_LEVEL_HW_SECURE_CRYPTO](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_HW_SECURE_CRYPTO:kotlin.Int), [android.media.MediaDrm#SECURITY_LEVEL_HW_SECURE_DECODE](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_HW_SECURE_DECODE:kotlin.Int), or [android.media.MediaDrm#SECURITY_LEVEL_HW_SECURE_ALL](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_HW_SECURE_ALL:kotlin.Int) |

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | This value cannot be`null`. |

| Exceptions ||
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.media.NotProvisionedException` | if provisioning is needed |
| `android.media.ResourceBusyException` | if required resources are in use |
| `java.lang.IllegalArgumentException` | if the requested security level is higher than the native level or lower than the lowest supported level or if the device does not support specifying the security level when opening a session |

### provideKeyResponse

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun provideKeyResponse(
    scope: ByteArray, 
    response: ByteArray
): ByteArray?
```

A key response is received from the license server by the app, then it is provided to the MediaDrm instance using provideKeyResponse. When the response is for an offline key request, a keySetId is returned that can be used to later restore the keys to a new session with the method [restoreKeys](https://developer.android.com/reference/kotlin/android/media/MediaDrm#restoreKeys(kotlin.ByteArray,%20kotlin.ByteArray)). When the response is for a streaming or release request, an empty byte array is returned.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `scope` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):may be a sessionId or keySetId depending on the type of the response. Scope should be set to the sessionId when the response is for either streaming or offline key requests. Scope should be set to the keySetId when the response is for a release request. This value cannot be`null`. |
| `response` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the byte array response from the server This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | If the response is for an offline request, the keySetId for the offline keys will be returned. If the response is for a streaming or release request an empty byte array will be returned. This value may be`null`. |

| Exceptions ||
|-----------------------------------------|----------------------------------------------------------------|
| `android.media.NotProvisionedException` | if the response indicates that reprovisioning is required |
| `android.media.DeniedByServerException` | if the response indicates that the server rejected the request |

### provideProvisionResponse

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun provideProvisionResponse(response: ByteArray): Unit
```

After a provision response is received by the app, it is provided to the MediaDrm instance using this method.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `response` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the opaque provisioning response byte array to provide to the MediaDrm instance. This value cannot be`null`. |

| Exceptions ||
|-----------------------------------------|----------------------------------------------------------------|
| `android.media.DeniedByServerException` | if the response indicates that the server rejected the request |

### queryKeyStatus

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun queryKeyStatus(sessionId: ByteArray): HashMap<String!, String!>
```

Request an informative description of the key status for the session. The status is in the form of {name, value} pairs. Since DRM license policies vary by vendor, the specific status field names are determined by each DRM vendor. Refer to your DRM provider documentation for definitions of the field names for a particular DRM plugin.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionId` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the session ID for the DRM session This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. |

### release

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun release(): Unit
```

**Deprecated:** *replaced by [close()](https://developer.android.com/reference/kotlin/android/media/MediaDrm#close()).* 

### releaseAllSecureStops

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun releaseAllSecureStops(): Unit
```

**Deprecated:** *Remove all secure stops using [removeAllSecureStops](https://developer.android.com/reference/kotlin/android/media/MediaDrm#removeAllSecureStops())instead.*

Remove all secure stops without requiring a secure stop release message from the license server. 

### releaseSecureStops

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun releaseSecureStops(ssRelease: ByteArray): Unit
```

**Deprecated:** *This method is deprecated and may be removed in a future release. Use renewals by calling [getKeyRequest](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getKeyRequest(kotlin.ByteArray,%20kotlin.ByteArray,%20kotlin.String,%20kotlin.Int,%20java.util.HashMap))to track concurrent playback. See additional information in [getSecureStops](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getSecureStops())*

Process the secure stop server response message ssRelease. After authenticating the message, remove the secure stops identified in the response.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ssRelease` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the server response indicating which secure stops to release This value cannot be`null`. |

### removeAllSecureStops

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeAllSecureStops(): Unit
```

**Deprecated:** *This method is deprecated and may be removed in a future release. Use renewals by calling [getKeyRequest](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getKeyRequest(kotlin.ByteArray,%20kotlin.ByteArray,%20kotlin.String,%20kotlin.Int,%20java.util.HashMap))to track concurrent playback. See additional information in [getSecureStops](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getSecureStops())*

Remove all secure stops without requiring a secure stop release message from the license server. This method was added in API 28. In API versions 18 through 27, [releaseAllSecureStops](https://developer.android.com/reference/kotlin/android/media/MediaDrm#releaseAllSecureStops())should be called instead. There is no need to do anything for API versions prior to 18. 

### removeKeys

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeKeys(sessionId: ByteArray): Unit
```

Remove the current keys from a session.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionId` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the session ID for the DRM session This value cannot be`null`. |

### removeOfflineLicense

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeOfflineLicense(keySetId: ByteArray): Unit
```

Normally offline licenses are released using a key request/response exchange using [getKeyRequest](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getKeyRequest(kotlin.ByteArray,%20kotlin.ByteArray,%20kotlin.String,%20kotlin.Int,%20java.util.HashMap))where the key type is KEY_TYPE_RELEASE, followed by [provideKeyResponse](https://developer.android.com/reference/kotlin/android/media/MediaDrm#provideKeyResponse(kotlin.ByteArray,%20kotlin.ByteArray)). This allows the server to cryptographically confirm that the license has been removed and then adjust the count of offline licenses allocated to the device.

In some exceptional situations it may be necessary to directly remove offline licenses without notifying the server, which may be performed using this method.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keySetId` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the id of the offline license to remove This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the keySetId does not refer to an offline license. |

### removeSecureStop

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeSecureStop(ssid: ByteArray): Unit
```

**Deprecated:** *This method is deprecated and may be removed in a future release. Use renewals by calling [getKeyRequest](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getKeyRequest(kotlin.ByteArray,%20kotlin.ByteArray,%20kotlin.String,%20kotlin.Int,%20java.util.HashMap))to track concurrent playback. See additional information in [getSecureStops](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getSecureStops())*

Remove a specific secure stop without requiring a secure stop release message from the license server.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ssid` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the ID of the secure stop to remove This value cannot be`null`. |

### requiresSecureDecoder

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun requiresSecureDecoder(mime: String): Boolean
```

Query if the crypto scheme requires the use of a secure decoder to decode data of the given mime type at the default security level. The default security level is defined as the highest security level supported on the device.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mime` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The mime type of the media data. Please use [isCryptoSchemeSupported(java.util.UUID,java.lang.String)](https://developer.android.com/reference/kotlin/android/media/MediaDrm#isCryptoSchemeSupported(java.util.UUID,%20kotlin.String))to query mime type support separately; for unsupported mime types the return value of [requiresSecureDecoder(java.lang.String)](https://developer.android.com/reference/kotlin/android/media/MediaDrm#requiresSecureDecoder(kotlin.String))is crypto scheme dependent. This value cannot be`null`. |

### requiresSecureDecoder

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun requiresSecureDecoder(
    mime: String, 
    level: Int
): Boolean
```

Query if the crypto scheme requires the use of a secure decoder to decode data of the given mime type at the given security level.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mime` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The mime type of the media data. Please use [isCryptoSchemeSupported(java.util.UUID,java.lang.String,int)](https://developer.android.com/reference/kotlin/android/media/MediaDrm#isCryptoSchemeSupported(java.util.UUID,%20kotlin.String,%20kotlin.Int))to query mime type support separately; for unsupported mime types the return value of [requiresSecureDecoder(java.lang.String,int)](https://developer.android.com/reference/kotlin/android/media/MediaDrm#requiresSecureDecoder(kotlin.String,%20kotlin.Int))is crypto scheme dependent. This value cannot be`null`. |
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a security level between [SECURITY_LEVEL_SW_SECURE_CRYPTO](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_SW_SECURE_CRYPTO:kotlin.Int) and [SECURITY_LEVEL_HW_SECURE_ALL](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_HW_SECURE_ALL:kotlin.Int). Otherwise the special value [getMaxSecurityLevel()](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getMaxSecurityLevel())is also permitted; use [getMaxSecurityLevel()](https://developer.android.com/reference/kotlin/android/media/MediaDrm#getMaxSecurityLevel())to indicate the maximum security level supported by the device. Value is [android.media.MediaDrm#SECURITY_LEVEL_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_UNKNOWN:kotlin.Int), [android.media.MediaDrm#SECURITY_LEVEL_SW_SECURE_CRYPTO](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_SW_SECURE_CRYPTO:kotlin.Int), [android.media.MediaDrm#SECURITY_LEVEL_SW_SECURE_DECODE](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_SW_SECURE_DECODE:kotlin.Int), [android.media.MediaDrm#SECURITY_LEVEL_HW_SECURE_CRYPTO](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_HW_SECURE_CRYPTO:kotlin.Int), [android.media.MediaDrm#SECURITY_LEVEL_HW_SECURE_DECODE](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_HW_SECURE_DECODE:kotlin.Int), or [android.media.MediaDrm#SECURITY_LEVEL_HW_SECURE_ALL](https://developer.android.com/reference/kotlin/android/media/MediaDrm#SECURITY_LEVEL_HW_SECURE_ALL:kotlin.Int) |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the requested security level is none of the documented values for the parameter`level`. |

### restoreKeys

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun restoreKeys(
    sessionId: ByteArray, 
    keySetId: ByteArray
): Unit
```

Restore persisted offline keys into a new session. keySetId identifies the keys to load, obtained from a prior call to [provideKeyResponse](https://developer.android.com/reference/kotlin/android/media/MediaDrm#provideKeyResponse(kotlin.ByteArray,%20kotlin.ByteArray)).

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionId` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the session ID for the DRM session This value cannot be`null`. |
| `keySetId` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):identifies the saved key set to restore This value cannot be`null`. |

### setOnEventListener

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOnEventListener(listener: MediaDrm.OnEventListener?): Unit
```

Register a callback to be invoked when an event occurs

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaDrm.OnEventListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnEventListener)?:the callback that will be run. Use`null`to stop receiving event callbacks. |

**See Also**

- [#setOnEventListener(OnEventListener, Handler)](https://developer.android.com/reference/kotlin/android/media/MediaDrm#setOnEventListener(android.media.MediaDrm.OnEventListener,%20android.os.Handler)) 

### setOnEventListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOnEventListener(
    listener: MediaDrm.OnEventListener?, 
    handler: Handler?
): Unit
```

Register a callback to be invoked when an event occurs

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaDrm.OnEventListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnEventListener)?:the callback that will be run. Use`null`to stop receiving event callbacks. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?:the handler on which the listener should be invoked, or null if the listener should be invoked on the calling thread's looper. |

### setOnEventListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOnEventListener(
    executor: Executor, 
    listener: MediaDrm.OnEventListener
): Unit
```

Register a callback to be invoked when an event occurs

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the executor through which the listener should be invoked This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `listener` | [MediaDrm.OnEventListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnEventListener):the callback that will be run. This value cannot be`null`. |

**See Also**

- [#setOnEventListener(OnEventListener)](https://developer.android.com/reference/kotlin/android/media/MediaDrm#setOnEventListener(android.media.MediaDrm.OnEventListener)) 

### setOnExpirationUpdateListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOnExpirationUpdateListener(
    listener: MediaDrm.OnExpirationUpdateListener?, 
    handler: Handler?
): Unit
```

Register a callback to be invoked when a session expiration update occurs. The app's OnExpirationUpdateListener will be notified when the expiration time of the keys in the session have changed.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaDrm.OnExpirationUpdateListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnExpirationUpdateListener)?:the callback that will be run, or`null`to unregister the previously registered callback. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?:the handler on which the listener should be invoked, or`null`if the listener should be invoked on the calling thread's looper. |

### setOnExpirationUpdateListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOnExpirationUpdateListener(
    executor: Executor, 
    listener: MediaDrm.OnExpirationUpdateListener
): Unit
```

Register a callback to be invoked when a session expiration update occurs.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the executor through which the listener should be invoked This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `listener` | [MediaDrm.OnExpirationUpdateListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnExpirationUpdateListener):the callback that will be run. This value cannot be`null`. |

**See Also**

- [#setOnExpirationUpdateListener(OnExpirationUpdateListener, Handler)](https://developer.android.com/reference/kotlin/android/media/MediaDrm#setOnExpirationUpdateListener(android.media.MediaDrm.OnExpirationUpdateListener,%20android.os.Handler)) 

### setOnKeyStatusChangeListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOnKeyStatusChangeListener(
    listener: MediaDrm.OnKeyStatusChangeListener?, 
    handler: Handler?
): Unit
```

Register a callback to be invoked when the state of keys in a session change, e.g. when a license update occurs or when a license expires.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaDrm.OnKeyStatusChangeListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnKeyStatusChangeListener)?:the callback that will be run when key status changes, or`null`to unregister the previously registered callback. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?:the handler on which the listener should be invoked, or null if the listener should be invoked on the calling thread's looper. |

### setOnKeyStatusChangeListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOnKeyStatusChangeListener(
    executor: Executor, 
    listener: MediaDrm.OnKeyStatusChangeListener
): Unit
```

Register a callback to be invoked when the state of keys in a session change.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaDrm.OnKeyStatusChangeListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnKeyStatusChangeListener):the callback that will be run when key status changes. This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the executor on which the listener should be invoked. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |

**See Also**

- [#setOnKeyStatusChangeListener(OnKeyStatusChangeListener, Handler)](https://developer.android.com/reference/kotlin/android/media/MediaDrm#setOnKeyStatusChangeListener(android.media.MediaDrm.OnKeyStatusChangeListener,%20android.os.Handler)) 

### setOnSessionLostStateListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOnSessionLostStateListener(
    listener: MediaDrm.OnSessionLostStateListener?, 
    handler: Handler?
): Unit
```

Register a callback to be invoked when session state has been lost. This event can occur on devices that are not capable of retaining crypto session state across device suspend/resume cycles. When this event occurs, the session must be closed and a new session opened to resume operation.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaDrm.OnSessionLostStateListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnSessionLostStateListener)?:the callback that will be run, or`null`to unregister the previously registered callback. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?:the handler on which the listener should be invoked, or`null`if the listener should be invoked on the calling thread's looper. |

### setOnSessionLostStateListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOnSessionLostStateListener(
    executor: Executor, 
    listener: MediaDrm.OnSessionLostStateListener?
): Unit
```

Register a callback to be invoked when session state has been lost.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaDrm.OnSessionLostStateListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnSessionLostStateListener)?:the callback that will be run. This value may be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the executor on which the listener should be invoked. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |

**See Also**

- [#setOnSessionLostStateListener(OnSessionLostStateListener, Handler)](https://developer.android.com/reference/kotlin/android/media/MediaDrm#setOnSessionLostStateListener(android.media.MediaDrm.OnSessionLostStateListener,%20android.os.Handler)) 

### setPropertyByteArray

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPropertyByteArray(
    propertyName: String, 
    value: ByteArray
): Unit
```

Set a MediaDrm byte array property value, given the property name string and new value for the property.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `value` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):This value cannot be`null`. |

### setPropertyString

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPropertyString(
    propertyName: String, 
    value: String
): Unit
```

Set a MediaDrm String property value, given the property name string and new value for the property.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

## Protected methods

### finalize

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
