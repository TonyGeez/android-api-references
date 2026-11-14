Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaDescrambler

Kotlin | [Java](https://developer.android.com/reference/android/media/MediaDescrambler "View this page in Java")

```
class MediaDescrambler : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.MediaDescrambler](https://developer.android.com/reference/kotlin/android/media/MediaDescrambler#) |

MediaDescrambler class can be used in conjunction with `https://developer.android.com/reference/kotlin/android/media/MediaCodec` and `https://developer.android.com/reference/kotlin/android/media/MediaExtractor` to decode media data scrambled by conditional access (CA) systems such as those in the ISO/IEC13818-1. A MediaDescrambler object is initialized from a session opened by a MediaCas object, and can be used to descramble media streams scrambled with that session's keys. Scrambling schemes are identified by 16-bit unsigned integer as in CA_system_id.

## Summary

| Constants ||
|---|---|
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaDescrambler#SCRAMBLE_CONTROL_EVEN_KEY:kotlin.Byte` Scramble control value indicating that the even key is used. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaDescrambler#SCRAMBLE_CONTROL_ODD_KEY:kotlin.Byte` Scramble control value indicating that the odd key is used. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaDescrambler#SCRAMBLE_CONTROL_RESERVED:kotlin.Byte` Scramble control value reserved and shouldn't be used currently. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaDescrambler#SCRAMBLE_CONTROL_UNSCRAMBLED:kotlin.Byte` Scramble control value indicating that the samples are not scrambled. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaDescrambler#SCRAMBLE_FLAG_PES_HEADER:kotlin.Byte` Scramble flag for a hint indicating that the descrambling request is for retrieving the PES header info only. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/MediaDescrambler#MediaDescrambler(kotlin.Int)(CA_system_id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Instantiate a MediaDescrambler. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaDescrambler#close()()` Closes this resource, relinquishing any underlying resources. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaDescrambler#descramble(java.nio.ByteBuffer,%20java.nio.ByteBuffer,%20android.media.MediaCodec.CryptoInfo)(srcBuf: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#, dstBuf: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#, cryptoInfo: https://developer.android.com/reference/kotlin/android/media/MediaCodec.CryptoInfo)` Descramble a ByteBuffer of data described by a `https://developer.android.com/reference/kotlin/android/media/MediaCodec.CryptoInfo` structure. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaDescrambler#requiresSecureDecoderComponent(kotlin.String)(mime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Query if the scrambling scheme requires the use of a secure decoder to decode data of the given mime type. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaDescrambler#setMediaCasSession(android.media.MediaCas.Session)(session: https://developer.android.com/reference/kotlin/android/media/MediaCas.Session)` Associate a MediaCas session with this MediaDescrambler instance. |

| Protected methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaDescrambler#finalize()()` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

## Constants

### SCRAMBLE_CONTROL_EVEN_KEY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCRAMBLE_CONTROL_EVEN_KEY: Byte
```

Scramble control value indicating that the even key is used.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaDescrambler#descramble(java.nio.ByteBuffer,%20java.nio.ByteBuffer,%20android.media.MediaCodec.CryptoInfo)`

### SCRAMBLE_CONTROL_ODD_KEY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCRAMBLE_CONTROL_ODD_KEY: Byte
```

Scramble control value indicating that the odd key is used.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaDescrambler#descramble(java.nio.ByteBuffer,%20java.nio.ByteBuffer,%20android.media.MediaCodec.CryptoInfo)`

### SCRAMBLE_CONTROL_RESERVED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCRAMBLE_CONTROL_RESERVED: Byte
```

Scramble control value reserved and shouldn't be used currently.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaDescrambler#descramble(java.nio.ByteBuffer,%20java.nio.ByteBuffer,%20android.media.MediaCodec.CryptoInfo)`

### SCRAMBLE_CONTROL_UNSCRAMBLED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCRAMBLE_CONTROL_UNSCRAMBLED: Byte
```

Scramble control value indicating that the samples are not scrambled.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaDescrambler#descramble(java.nio.ByteBuffer,%20java.nio.ByteBuffer,%20android.media.MediaCodec.CryptoInfo)`

### SCRAMBLE_FLAG_PES_HEADER

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCRAMBLE_FLAG_PES_HEADER: Byte
```

Scramble flag for a hint indicating that the descrambling request is for retrieving the PES header info only.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaDescrambler#descramble(java.nio.ByteBuffer,%20java.nio.ByteBuffer,%20android.media.MediaCodec.CryptoInfo)`

## Public constructors

### MediaDescrambler

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MediaDescrambler(CA_system_id: Int)
```

Instantiate a MediaDescrambler.

| Parameters ||
|---|---|
| `CA_system_id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The system id of the scrambling scheme. |

| Exceptions ||
|---|---|
| `android.media.MediaCasException.UnsupportedCasException` | if the scrambling scheme is not supported. |

## Public methods

### close

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun close(): Unit
```

Closes this resource, relinquishing any underlying resources. This method is invoked automatically on objects managed by the `try`-with-resources statement.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |

### descramble

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun descramble(
    srcBuf: ByteBuffer, 
    dstBuf: ByteBuffer, 
    cryptoInfo: MediaCodec.CryptoInfo
): Int
```

Descramble a ByteBuffer of data described by a `https://developer.android.com/reference/kotlin/android/media/MediaCodec.CryptoInfo` structure.

| Parameters ||
|---|---|
| `srcBuf` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#): ByteBuffer containing the scrambled data, which starts at srcBuf.position(). This value cannot be `null`. |
| `dstBuf` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#): ByteBuffer to hold the descrambled data, which starts at dstBuf.position(). This value cannot be `null`. |
| `cryptoInfo` | [MediaCodec.CryptoInfo](https://developer.android.com/reference/kotlin/android/media/MediaCodec.CryptoInfo): a `https://developer.android.com/reference/kotlin/android/media/MediaCodec.CryptoInfo` structure describing the subsamples contained in srcBuf. The iv and mode fields in CryptoInfo are not used. key\[0\] contains the MPEG2TS scrambling control bits (as defined in ETSI TS 100 289 (2011): "Digital Video Broadcasting (DVB); Support for use of the DVB Scrambling Algorithm version 3 within digital broadcasting systems"), and the value must be one of `https://developer.android.com/reference/kotlin/android/media/MediaDescrambler#SCRAMBLE_CONTROL_UNSCRAMBLED:kotlin.Byte`, `https://developer.android.com/reference/kotlin/android/media/MediaDescrambler#SCRAMBLE_CONTROL_RESERVED:kotlin.Byte`, `https://developer.android.com/reference/kotlin/android/media/MediaDescrambler#SCRAMBLE_CONTROL_EVEN_KEY:kotlin.Byte` or `https://developer.android.com/reference/kotlin/android/media/MediaDescrambler#SCRAMBLE_CONTROL_ODD_KEY:kotlin.Byte`. key\[1\] is a set of bit flags, with the only possible bit being `https://developer.android.com/reference/kotlin/android/media/MediaDescrambler#SCRAMBLE_FLAG_PES_HEADER:kotlin.Byte` currently. key\[2\~15\] are not used. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | number of bytes that have been successfully descrambled, with negative values indicating errors. |

| Exceptions ||
|---|---|
| `android.media.MediaCasStateException` | for CAS-specific state exceptions. |
| `java.lang.IllegalStateException` | if the descrambler instance is not valid. |

### requiresSecureDecoderComponent

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun requiresSecureDecoderComponent(mime: String): Boolean
```

Query if the scrambling scheme requires the use of a secure decoder to decode data of the given mime type.

| Parameters ||
|---|---|
| `mime` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The mime type of the media data. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the descrambler instance is not valid. |

### setMediaCasSession

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setMediaCasSession(session: MediaCas.Session): Unit
```

Associate a MediaCas session with this MediaDescrambler instance. The MediaCas session is used to securely load decryption keys for the descrambler. The crypto keys loaded through the MediaCas session may be selected for use during the descrambling operation performed by `https://developer.android.com/reference/kotlin/android/media/MediaExtractor` by specifying even or odd key in the `https://developer.android.com/reference/kotlin/android/media/MediaCodec.CryptoInfo#key:kotlin.ByteArray` field.

| Parameters ||
|---|---|
| `session` | [MediaCas.Session](https://developer.android.com/reference/kotlin/android/media/MediaCas.Session): the MediaCas session to associate with this MediaDescrambler instance. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.media.MediaCasStateException` | for CAS-specific state exceptions. |
| `java.lang.IllegalStateException` | if the descrambler instance is not valid. |

## Protected methods

### finalize

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun finalize(): Unit
```

Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup.

The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded.

The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition.

The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates.

After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded.

The `finalize` method is never invoked more than once by a Java virtual machine for any given object.

Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored.

| Exceptions ||
|---|---|
| `java.lang.Throwable` | the `Exception` raised by this method |
