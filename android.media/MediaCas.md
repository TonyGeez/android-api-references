# MediaCas

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaCas

Kotlin| [Java](../android/media/MediaCas.md) 
| --- | --- |

```
class MediaCas : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MediaCas](../android/media/MediaCas.md) |

MediaCas can be used to obtain keys for descrambling protected media streams, in conjunction with [android.media.MediaDescrambler](../android/media/MediaDescrambler.md). The MediaCas APIs are designed to support conditional access such as those in the ISO/IEC13818-1. The CA system is identified by a 16-bit integer CA_system_id. The scrambling algorithms are usually proprietary and implemented by vendor-specific CA plugins installed on the device.

The app is responsible for constructing a MediaCas object for the CA system it intends to use. The app can query if a certain CA system is supported using static method [isSystemIdSupported](../android/media/MediaCas.md)). It can also obtain the entire list of supported CA systems using static method [enumeratePlugins](../android/media/MediaCas.md)).

Once the MediaCas object is constructed, the app should properly provision it by using method [provision](../android/media/MediaCas.md))and/or #processEmm. The EMMs (Entitlement management messages) can be distributed out-of-band, or in-band with the stream.

To descramble elementary streams, the app first calls #openSession to generate a [Session](../android/media/MediaCas.Session.md) object that will uniquely identify a session. A session provides a context for subsequent key updates and descrambling activities. The ECMs (Entitlement control messages) are sent to the session via method android.media.MediaCas.Session#processEcm.

The app next constructs a MediaDescrambler object, and initializes it with the session using [MediaDescrambler.setMediaCasSession](../android/media/MediaDescrambler.md)). This ties the descrambler to the session, and the descrambler can then be used to descramble content secured with the session's key, either during extraction, or during decoding with [android.media.MediaCodec](../android/media/MediaCodec.md).

If the app handles sample extraction using its own extractor, it can use MediaDescrambler to descramble samples into clear buffers (if the session's license doesn't require secure decoders), or descramble a small amount of data to retrieve information necessary for the downstream pipeline to process the sample (if the session's license requires secure decoders).

If the session requires a secure decoder, a MediaDescrambler needs to be provided to MediaCodec to descramble samples queued by [MediaCodec.queueSecureInputBuffer](../android/media/MediaCodec.md))into protected buffers. The app should use [MediaCodec.configure(MediaFormat,](../android/media/MediaCodec.md))instead of the normal [android.media.MediaCodec#configure(android.media.MediaFormat,android.view.Surface,android.media.MediaCrypto,int)](../android/media/MediaCodec.md))method to configure MediaCodec.

<br />

### Using Android's MediaExtractor

If the app uses [MediaExtractor](../android/media/MediaExtractor.md), it can delegate the CAS session management to MediaExtractor by calling [MediaExtractor.setMediaCas](../android/media/MediaExtractor.md)). MediaExtractor will take over and call #openSession, #processEmm and/or android.media.MediaCas.Session#processEcm, etc.. if necessary.

When using [MediaExtractor](../android/media/MediaExtractor.md), the app would still need a MediaDescrambler to use with [MediaCodec](../android/media/MediaCodec.md) if the licensing requires a secure decoder. The session associated with the descrambler of a track can be retrieved by calling [MediaExtractor.getCasInfo](../android/media/MediaExtractor.md)), and used to initialize a MediaDescrambler object for MediaCodec.

<br />

### Listeners

The app may register a listener to receive events from the CA system using method [setEventListener](../android/media/MediaCas.md)). The exact format of the event is scheme-specific and is not specified by this API.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [EventListener](../android/media/MediaCas.EventListener.md) An interface registered by the caller to [setEventListener](../android/media/MediaCas.md))to receives scheme-specific notifications from a MediaCas instance. |
| | [PluginDescriptor](../android/media/MediaCas.PluginDescriptor.md) Describe a CAS plugin with its CA_system_ID and string name. |
| | [Session](../android/media/MediaCas.Session.md) Class for an open session with the CA system. |
| --- | --- |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLUGIN_STATUS_PHYSICAL_MODULE_CHANGED](../android/media/MediaCas.md) The event to indicate that the status of CAS system is changed by the removal or insertion of physical CAS modules. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLUGIN_STATUS_SESSION_NUMBER_CHANGED](../android/media/MediaCas.md) The event to indicate that the number of CAS system's session is changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCRAMBLING_MODE_AES128](../android/media/MediaCas.md) Advanced Encryption System (AES) 128-bit Encryption mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCRAMBLING_MODE_AES_CBC](../android/media/MediaCas.md) Advanced Encryption System (AES) Cipher Block Chaining (CBC) mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCRAMBLING_MODE_AES_ECB](../android/media/MediaCas.md) Advanced Encryption System (AES) Electronic Code Book (ECB) mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCRAMBLING_MODE_AES_SCTE52](../android/media/MediaCas.md) Advanced Encryption System (AES) Society of Cable Telecommunications Engineers (SCTE) 52 mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCRAMBLING_MODE_DVB_CISSA_V1](../android/media/MediaCas.md) DVB Common IPTV Software-oriented Scrambling Algorithm (CISSA) Version 1. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCRAMBLING_MODE_DVB_CSA1](../android/media/MediaCas.md) DVB (Digital Video Broadcasting) Common Scrambling Algorithm (CSA) 1. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCRAMBLING_MODE_DVB_CSA2](../android/media/MediaCas.md) DVB CSA 2. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCRAMBLING_MODE_DVB_CSA3_ENHANCE](../android/media/MediaCas.md) DVB CSA 3 in fully enhanced mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCRAMBLING_MODE_DVB_CSA3_MINIMAL](../android/media/MediaCas.md) DVB CSA 3 in minimally enhanced mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCRAMBLING_MODE_DVB_CSA3_STANDARD](../android/media/MediaCas.md) DVB CSA 3 in standard mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCRAMBLING_MODE_DVB_IDSA](../android/media/MediaCas.md) ATIS-0800006 IIF Default Scrambling Algorithm (IDSA). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCRAMBLING_MODE_MULTI2](../android/media/MediaCas.md) A symmetric key algorithm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCRAMBLING_MODE_RESERVED](../android/media/MediaCas.md) DVB (Digital Video Broadcasting) reserved mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCRAMBLING_MODE_TDES_ECB](../android/media/MediaCas.md) Triple Data Encryption Algorithm (TDES) Electronic Code Book (ECB) mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCRAMBLING_MODE_TDES_SCTE52](../android/media/MediaCas.md) Triple Data Encryption Algorithm (TDES) Society of Cable Telecommunications Engineers (SCTE) 52 mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SESSION_USAGE_LIVE](../android/media/MediaCas.md) Cas session is used to descramble live streams. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SESSION_USAGE_PLAYBACK](../android/media/MediaCas.md) Cas session is used to descramble recoreded streams. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SESSION_USAGE_RECORD](../android/media/MediaCas.md) Cas session is used to descramble live streams and encrypt local recorded content |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SESSION_USAGE_TIMESHIFT](../android/media/MediaCas.md) Cas session is used to descramble live streams , encrypt local recorded content and playback local encrypted content. |
| --- | --- |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MediaCas](../android/media/MediaCas.md))`(`context:` ` [Context](../android/content/Context.md)`, `casSystemId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tvInputServiceSessionId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `priorityHint:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Instantiate a CA system of the specified system id. |
| [MediaCas](../android/media/MediaCas.md))`(`context:` ` [Context](../android/content/Context.md)`, `casSystemId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tvInputServiceSessionId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `priorityHint:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `handler:` ` [Handler](../android/os/Handler.md)?`, `listener:` ` [MediaCas.EventListener](../android/media/MediaCas.EventListener.md)?`)` Instantiate a CA system of the specified system id with EvenListener. |
| [MediaCas](../android/media/MediaCas.md))`(`casSystemId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Instantiate a CA system of the specified system id. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/media/MediaCas.md))`()` <br /> |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MediaCas.PluginDescriptor](../android/media/MediaCas.PluginDescriptor.md)!\>! | [enumeratePlugins](../android/media/MediaCas.md))`()` List all available CA plugins on the device. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSystemIdSupported](../android/media/MediaCas.md))`(`CA_system_id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Query if a certain CA system is supported on this device. |
| --- | --- |
| [MediaCas.Session](../android/media/MediaCas.Session.md)! | [openSession](../android/media/MediaCas.md))`()` Open a session to descramble one or more streams scrambled by the conditional access system. |
| [MediaCas.Session](../android/media/MediaCas.Session.md)? | [openSession](../android/media/MediaCas.md))`(`sessionUsage:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `scramblingMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Open a session with usage and scrambling information, so that descrambler can be configured to descramble one or more streams scrambled by the conditional access system. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [processEmm](../android/media/MediaCas.md))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Send a received EMM packet to the CA system. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [processEmm](../android/media/MediaCas.md))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Send a received EMM packet to the CA system. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [provision](../android/media/MediaCas.md))`(`provisionString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Initiate a provisioning operation for a CA system. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [refreshEntitlements](../android/media/MediaCas.md))`(`refreshType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `refreshData:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`)` Notify the CA system to refresh entitlement keys. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendEvent](../android/media/MediaCas.md))`(`event:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arg:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`)` Send an event to a CA system. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEventListener](../android/media/MediaCas.md))`(`listener:` ` [MediaCas.EventListener](../android/media/MediaCas.EventListener.md)?`, `handler:` ` [Handler](../android/os/Handler.md)?`)` Set an event listener to receive notifications from the MediaCas instance. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPrivateData](../android/media/MediaCas.md))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Send the private data for the CA system. |
| --- | --- |

| Protected methods ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/media/MediaCas.md))`()` <br /> |

## Constants

### PLUGIN_STATUS_PHYSICAL_MODULE_CHANGED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLUGIN_STATUS_PHYSICAL_MODULE_CHANGED: Int
```

The event to indicate that the status of CAS system is changed by the removal or insertion of physical CAS modules. 

 Value: 0

### PLUGIN_STATUS_SESSION_NUMBER_CHANGED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLUGIN_STATUS_SESSION_NUMBER_CHANGED: Int
```

The event to indicate that the number of CAS system's session is changed. 

 Value: 1

### SCRAMBLING_MODE_AES128

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCRAMBLING_MODE_AES128: Int
```

Advanced Encryption System (AES) 128-bit Encryption mode. 

 Value: 9

### SCRAMBLING_MODE_AES_CBC

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCRAMBLING_MODE_AES_CBC: Int
```

Advanced Encryption System (AES) Cipher Block Chaining (CBC) mode. 

 Value: 14

### SCRAMBLING_MODE_AES_ECB

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCRAMBLING_MODE_AES_ECB: Int
```

Advanced Encryption System (AES) Electronic Code Book (ECB) mode. 

 Value: 10

### SCRAMBLING_MODE_AES_SCTE52

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCRAMBLING_MODE_AES_SCTE52: Int
```

Advanced Encryption System (AES) Society of Cable Telecommunications Engineers (SCTE) 52 mode. 

 Value: 11

### SCRAMBLING_MODE_DVB_CISSA_V1

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCRAMBLING_MODE_DVB_CISSA_V1: Int
```

DVB Common IPTV Software-oriented Scrambling Algorithm (CISSA) Version 1. 

 Value: 6

### SCRAMBLING_MODE_DVB_CSA1

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCRAMBLING_MODE_DVB_CSA1: Int
```

DVB (Digital Video Broadcasting) Common Scrambling Algorithm (CSA) 1. 

 Value: 1

### SCRAMBLING_MODE_DVB_CSA2

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCRAMBLING_MODE_DVB_CSA2: Int
```

DVB CSA 2. 

 Value: 2

### SCRAMBLING_MODE_DVB_CSA3_ENHANCE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCRAMBLING_MODE_DVB_CSA3_ENHANCE: Int
```

DVB CSA 3 in fully enhanced mode. 

 Value: 5

### SCRAMBLING_MODE_DVB_CSA3_MINIMAL

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCRAMBLING_MODE_DVB_CSA3_MINIMAL: Int
```

DVB CSA 3 in minimally enhanced mode. 

 Value: 4

### SCRAMBLING_MODE_DVB_CSA3_STANDARD

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCRAMBLING_MODE_DVB_CSA3_STANDARD: Int
```

DVB CSA 3 in standard mode. 

 Value: 3

### SCRAMBLING_MODE_DVB_IDSA

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCRAMBLING_MODE_DVB_IDSA: Int
```

ATIS-0800006 IIF Default Scrambling Algorithm (IDSA). 

 Value: 7

### SCRAMBLING_MODE_MULTI2

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCRAMBLING_MODE_MULTI2: Int
```

A symmetric key algorithm. 

 Value: 8

### SCRAMBLING_MODE_RESERVED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCRAMBLING_MODE_RESERVED: Int
```

DVB (Digital Video Broadcasting) reserved mode. 

 Value: 0

### SCRAMBLING_MODE_TDES_ECB

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCRAMBLING_MODE_TDES_ECB: Int
```

Triple Data Encryption Algorithm (TDES) Electronic Code Book (ECB) mode. 

 Value: 12

### SCRAMBLING_MODE_TDES_SCTE52

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCRAMBLING_MODE_TDES_SCTE52: Int
```

Triple Data Encryption Algorithm (TDES) Society of Cable Telecommunications Engineers (SCTE) 52 mode. 

 Value: 13

### SESSION_USAGE_LIVE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_USAGE_LIVE: Int
```

Cas session is used to descramble live streams. 

 Value: 0

### SESSION_USAGE_PLAYBACK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_USAGE_PLAYBACK: Int
```

Cas session is used to descramble recoreded streams. 

 Value: 1

### SESSION_USAGE_RECORD

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_USAGE_RECORD: Int
```

Cas session is used to descramble live streams and encrypt local recorded content 

 Value: 2

### SESSION_USAGE_TIMESHIFT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SESSION_USAGE_TIMESHIFT: Int
```

Cas session is used to descramble live streams , encrypt local recorded content and playback local encrypted content. 

 Value: 3

## Public constructors

### MediaCas

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MediaCas(
    context: Context, 
    casSystemId: Int, 
    tvInputServiceSessionId: String?, 
    priorityHint: Int)
```

Instantiate a CA system of the specified system id.

| Parameters ||
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):the context of the caller. This value cannot be`null`. |
| `casSystemId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The system id of the CA system. |
| `tvInputServiceSessionId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The Id of the session opened in TV Input Service (TIS) [android.media.tv.TvInputService#onCreateSession(String, String)](../android/media/tv/TvInputService.md))This value may be`null`. |
| --- | --- |
| `priorityHint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):priority hint from the use case type for new created CAS system. Value is [android.media.tv.TvInputService#PRIORITY_HINT_USE_CASE_TYPE_BACKGROUND](../android/media/tv/TvInputService.md), [android.media.tv.TvInputService#PRIORITY_HINT_USE_CASE_TYPE_SCAN](../android/media/tv/TvInputService.md), [android.media.tv.TvInputService#PRIORITY_HINT_USE_CASE_TYPE_PLAYBACK](../android/media/tv/TvInputService.md), [android.media.tv.TvInputService#PRIORITY_HINT_USE_CASE_TYPE_LIVE](../android/media/tv/TvInputService.md), or [android.media.tv.TvInputService#PRIORITY_HINT_USE_CASE_TYPE_RECORD](../android/media/tv/TvInputService.md) |

| Exceptions ||
|-----------------------------------------------------------|---------------------------------------------------------|
| `android.media.MediaCasException.UnsupportedCasException` | if the device does not support the specified CA system. |

### MediaCas

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MediaCas(
    context: Context, 
    casSystemId: Int, 
    tvInputServiceSessionId: String?, 
    priorityHint: Int, 
    handler: Handler?, 
    listener: MediaCas.EventListener?)
```

Instantiate a CA system of the specified system id with EvenListener.

| Parameters ||
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):the context of the caller. This value cannot be`null`. |
| `casSystemId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The system id of the CA system. |
| `tvInputServiceSessionId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The Id of the session opened in TV Input Service (TIS) [android.media.tv.TvInputService#onCreateSession(String, String)](../android/media/tv/TvInputService.md))This value may be`null`. |
| --- | --- |
| `priorityHint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):priority hint from the use case type for new created CAS system. Value is [android.media.tv.TvInputService#PRIORITY_HINT_USE_CASE_TYPE_BACKGROUND](../android/media/tv/TvInputService.md), [android.media.tv.TvInputService#PRIORITY_HINT_USE_CASE_TYPE_SCAN](../android/media/tv/TvInputService.md), [android.media.tv.TvInputService#PRIORITY_HINT_USE_CASE_TYPE_PLAYBACK](../android/media/tv/TvInputService.md), [android.media.tv.TvInputService#PRIORITY_HINT_USE_CASE_TYPE_LIVE](../android/media/tv/TvInputService.md), or [android.media.tv.TvInputService#PRIORITY_HINT_USE_CASE_TYPE_RECORD](../android/media/tv/TvInputService.md) |
| `listener` | [MediaCas.EventListener](../android/media/MediaCas.EventListener.md)?:the event listener to be set. This value may be`null`. |
| `handler` | [Handler](../android/os/Handler.md)?:the handler whose looper the event listener will be called on. If handler is null, we'll try to use current thread's looper, or the main looper. If neither are available, an internal thread will be created instead. |
| --- | --- |

| Exceptions ||
|-----------------------------------------------------------|---------------------------------------------------------|
| `android.media.MediaCasException.UnsupportedCasException` | if the device does not support the specified CA system. |

### MediaCas

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MediaCas(casSystemId: Int)
```

Instantiate a CA system of the specified system id.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------|
| `casSystemId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The system id of the CA system. |

| Exceptions ||
|-----------------------------------------------------------|---------------------------------------------------------|
| `android.media.MediaCasException.UnsupportedCasException` | if the device does not support the specified CA system. |

## Public methods

### close

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |

### enumeratePlugins

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun enumeratePlugins(): Array<MediaCas.PluginDescriptor!>!
```

List all available CA plugins on the device.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MediaCas.PluginDescriptor](../android/media/MediaCas.PluginDescriptor.md)!>! | an array of descriptors for the available CA plugins. |

### isSystemIdSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isSystemIdSupported(CA_system_id: Int): Boolean
```

Query if a certain CA system is supported on this device.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------|
| `CA_system_id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the id of the CA system. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the specified CA system is supported on this device. |

### openSession

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openSession(): MediaCas.Session!
```

Open a session to descramble one or more streams scrambled by the conditional access system.

Tuner resource manager (TRM) uses the client priority value to decide whether it is able to get cas session resource if cas session resources is limited. If the client can't get the resource, this call returns [MediaCasException.InsufficientResourceException](../android/media/MediaCasException.InsufficientResourceException.md).

| Return ||
|----------------------------------------------------------------------------------------------------|-----------------------------------|
| [MediaCas.Session](../android/media/MediaCas.Session.md)! | session the newly opened session. |

| Exceptions ||
|----------------------------------------|----------------------------------------|
| `java.lang.IllegalStateException` | if the MediaCas instance is not valid. |
| `android.media.MediaCasException` | for CAS-specific errors. |
| `android.media.MediaCasStateException` | for CAS-specific state exceptions. |
| --- | --- |

### openSession

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openSession(
    sessionUsage: Int, 
    scramblingMode: Int
): MediaCas.Session?
```

Open a session with usage and scrambling information, so that descrambler can be configured to descramble one or more streams scrambled by the conditional access system.

Tuner resource manager (TRM) uses the client priority value to decide whether it is able to get cas session resource if cas session resources is limited. If the client can't get the resource, this call returns [MediaCasException.InsufficientResourceException](../android/media/MediaCasException.InsufficientResourceException.md).

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionUsage` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):used for the created session. Value is [android.media.MediaCas#SESSION_USAGE_LIVE](../android/media/MediaCas.md), [android.media.MediaCas#SESSION_USAGE_PLAYBACK](../android/media/MediaCas.md), [android.media.MediaCas#SESSION_USAGE_RECORD](../android/media/MediaCas.md), or [android.media.MediaCas#SESSION_USAGE_TIMESHIFT](../android/media/MediaCas.md) |
| `scramblingMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):used for the created session. Value is [android.media.MediaCas#SCRAMBLING_MODE_RESERVED](../android/media/MediaCas.md), [android.media.MediaCas#SCRAMBLING_MODE_DVB_CSA1](../android/media/MediaCas.md), [android.media.MediaCas#SCRAMBLING_MODE_DVB_CSA2](../android/media/MediaCas.md), [android.media.MediaCas#SCRAMBLING_MODE_DVB_CSA3_STANDARD](../android/media/MediaCas.md), [android.media.MediaCas#SCRAMBLING_MODE_DVB_CSA3_MINIMAL](../android/media/MediaCas.md), [android.media.MediaCas#SCRAMBLING_MODE_DVB_CSA3_ENHANCE](../android/media/MediaCas.md), [android.media.MediaCas#SCRAMBLING_MODE_DVB_CISSA_V1](../android/media/MediaCas.md), [android.media.MediaCas#SCRAMBLING_MODE_DVB_IDSA](../android/media/MediaCas.md), [android.media.MediaCas#SCRAMBLING_MODE_MULTI2](../android/media/MediaCas.md), [android.media.MediaCas#SCRAMBLING_MODE_AES128](../android/media/MediaCas.md), [android.media.MediaCas#SCRAMBLING_MODE_AES_CBC](../android/media/MediaCas.md), [android.media.MediaCas#SCRAMBLING_MODE_AES_ECB](../android/media/MediaCas.md), [android.media.MediaCas#SCRAMBLING_MODE_AES_SCTE52](../android/media/MediaCas.md), [android.media.MediaCas#SCRAMBLING_MODE_TDES_ECB](../android/media/MediaCas.md), or [android.media.MediaCas#SCRAMBLING_MODE_TDES_SCTE52](../android/media/MediaCas.md) |

| Return ||
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [MediaCas.Session](../android/media/MediaCas.Session.md)? | session the newly opened session. This value may be`null`. |

| Exceptions ||
|----------------------------------------|----------------------------------------|
| `java.lang.IllegalStateException` | if the MediaCas instance is not valid. |
| `android.media.MediaCasException` | for CAS-specific errors. |
| `android.media.MediaCasStateException` | for CAS-specific state exceptions. |
| --- | --- |

### processEmm

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun processEmm(data: ByteArray): Unit
```

Send a received EMM packet to the CA system. This is similar to[processEmm(byte[],int,int)](https://developer.android.com/reference/kotlin/android/media/MediaCas#processEmm(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))except that the entire byte array is sent.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):byte array of the EMM data. This value cannot be`null`. |

| Exceptions ||
|----------------------------------------|----------------------------------------|
| `java.lang.IllegalStateException` | if the MediaCas instance is not valid. |
| `android.media.MediaCasException` | for CAS-specific errors. |
| `android.media.MediaCasStateException` | for CAS-specific state exceptions. |
| --- | --- |

### processEmm

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun processEmm(
    data: ByteArray, 
    offset: Int, 
    length: Int
): Unit
```

Send a received EMM packet to the CA system.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):byte array of the EMM data. This value cannot be`null`. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):position within data where the EMM data begins. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):length of the data (starting from offset). |
| --- | --- |

| Exceptions ||
|----------------------------------------|----------------------------------------|
| `java.lang.IllegalStateException` | if the MediaCas instance is not valid. |
| `android.media.MediaCasException` | for CAS-specific errors. |
| `android.media.MediaCasStateException` | for CAS-specific state exceptions. |
| --- | --- |

### provision

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun provision(provisionString: String): Unit
```

Initiate a provisioning operation for a CA system.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provisionString` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):string containing information needed for the provisioning operation, the format of which is scheme and implementation specific. This value cannot be`null`. |

| Exceptions ||
|----------------------------------------|----------------------------------------|
| `java.lang.IllegalStateException` | if the MediaCas instance is not valid. |
| `android.media.MediaCasException` | for CAS-specific errors. |
| `android.media.MediaCasStateException` | for CAS-specific state exceptions. |
| --- | --- |

### refreshEntitlements

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun refreshEntitlements(
    refreshType: Int, 
    refreshData: ByteArray?
): Unit
```

Notify the CA system to refresh entitlement keys.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `refreshType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the type of the refreshment. |
| `refreshData` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:private data associated with the refreshment. This value may be`null`. |

| Exceptions ||
|----------------------------------------|----------------------------------------|
| `java.lang.IllegalStateException` | if the MediaCas instance is not valid. |
| `android.media.MediaCasException` | for CAS-specific errors. |
| `android.media.MediaCasStateException` | for CAS-specific state exceptions. |
| --- | --- |

### sendEvent

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun sendEvent(
    event: Int, 
    arg: Int, 
    data: ByteArray?
): Unit
```

Send an event to a CA system. The format of the event is scheme-specific and is opaque to the framework.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an integer denoting a scheme-specific event to be sent. |
| `arg` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a scheme-specific integer argument for the event. |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:a byte array containing scheme-specific data for the event. This value may be`null`. |
| --- | --- |

| Exceptions ||
|----------------------------------------|----------------------------------------|
| `java.lang.IllegalStateException` | if the MediaCas instance is not valid. |
| `android.media.MediaCasException` | for CAS-specific errors. |
| `android.media.MediaCasStateException` | for CAS-specific state exceptions. |
| --- | --- |

### setEventListener

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setEventListener(
    listener: MediaCas.EventListener?, 
    handler: Handler?
): Unit
```

Set an event listener to receive notifications from the MediaCas instance.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MediaCas.EventListener](../android/media/MediaCas.EventListener.md)?:the event listener to be set. This value may be`null`. |
| `handler` | [Handler](../android/os/Handler.md)?:the handler whose looper the event listener will be called on. If handler is null, we'll try to use current thread's looper, or the main looper. If neither are available, an internal thread will be created instead. |

### setPrivateData

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPrivateData(data: ByteArray): Unit
```

Send the private data for the CA system.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):byte array of the private data. This value cannot be`null`. |

| Exceptions ||
|----------------------------------------|----------------------------------------|
| `java.lang.IllegalStateException` | if the MediaCas instance is not valid. |
| `android.media.MediaCasException` | for CAS-specific errors. |
| `android.media.MediaCasStateException` | for CAS-specific state exceptions. |
| --- | --- |

## Protected methods

### finalize

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
