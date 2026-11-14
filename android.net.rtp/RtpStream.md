# RtpStream

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RtpStream

Kotlin| [Java](https://developer.android.com/reference/android/net/rtp/RtpStream "View this page in Java") 

```
open class RtpStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.rtp.RtpStream](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#) |

| Known Direct Subclasses [AudioStream](https://developer.android.com/reference/kotlin/android/net/rtp/AudioStream) |-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AudioStream](https://developer.android.com/reference/kotlin/android/net/rtp/AudioStream) | An AudioStream is a [RtpStream](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#) which carrys audio payloads over Real-time Transport Protocol (RTP). | |

| **This class was deprecated in API level 31.**
|
| [android.net.sip.SipManager](https://developer.android.com/reference/kotlin/android/net/sip/SipManager.html#) and associated classes are no longer supported and should not be used as the basis of future VOIP apps.

RtpStream represents the base class of streams which send and receive network packets with media payloads over Real-time Transport Protocol (RTP).

Using this class requires [android.Manifest.permission#INTERNET](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#INTERNET:kotlin.String) permission.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_NORMAL](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#MODE_NORMAL:kotlin.Int) This mode indicates that the stream sends and receives packets at the same time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_RECEIVE_ONLY](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#MODE_RECEIVE_ONLY:kotlin.Int) This mode indicates that the stream only receives packets. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_SEND_ONLY](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#MODE_SEND_ONLY:kotlin.Int) This mode indicates that the stream only sends packets. |

| Public methods ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [associate](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#associate(java.net.InetAddress,%20kotlin.Int))`(`address:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Associates with a remote host. |
| open [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)! | [getLocalAddress](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#getLocalAddress())`()` Returns the network address of the local host. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLocalPort](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#getLocalPort())`()` Returns the network port of the local host. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMode](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#getMode())`()` Returns the current mode. |
| open [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)! | [getRemoteAddress](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#getRemoteAddress())`()` Returns the network address of the remote host or`null`if the stream is not associated. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRemotePort](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#getRemotePort())`()` Returns the network port of the remote host or`-1`if the stream is not associated. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBusy](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#isBusy())`()` Returns`true`if the stream is busy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#release())`()` Releases allocated resources. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMode](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#setMode(kotlin.Int))`(`mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Changes the current mode. |

| Protected methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#finalize())`()` <br /> |

## Constants

### MODE_NORMAL

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_NORMAL: Int
```

**Deprecated:** *Deprecated in Java.*

This mode indicates that the stream sends and receives packets at the same time. This is the initial mode for new streams. 

 Value: 0

### MODE_RECEIVE_ONLY

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_RECEIVE_ONLY: Int
```

**Deprecated:** *Deprecated in Java.*

This mode indicates that the stream only receives packets. 

 Value: 2

### MODE_SEND_ONLY

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_SEND_ONLY: Int
```

**Deprecated:** *Deprecated in Java.*

This mode indicates that the stream only sends packets. 

 Value: 1

## Public methods

### associate

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun associate(
    address: InetAddress!, 
    port: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Associates with a remote host. This defines the destination of the outgoing packets.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| `address` | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!:The network address of the remote host. |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The network port of the remote host. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the address is not supported or the port is invalid. |
| `java.lang.IllegalStateException` | if the stream is busy. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#isBusy()> 

### getLocalAddress

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocalAddress(): InetAddress!
```

**Deprecated:** *Deprecated in Java.*

Returns the network address of the local host. 

### getLocalPort

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocalPort(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the network port of the local host. 

### getMode

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMode(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the current mode. 

### getRemoteAddress

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRemoteAddress(): InetAddress!
```

**Deprecated:** *Deprecated in Java.*

Returns the network address of the remote host or`null`if the stream is not associated. 

### getRemotePort

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRemotePort(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the network port of the remote host or`-1`if the stream is not associated. 

### isBusy

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isBusy(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns`true`if the stream is busy. In this case most of the setter methods are disabled. This method is intended to be overridden by subclasses. 

### release

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun release(): Unit
```

**Deprecated:** *Deprecated in Java.*

Releases allocated resources. The stream becomes inoperable after calling this method.

| Exceptions ||
|-----------------------------------|------------------------|
| `java.lang.IllegalStateException` | if the stream is busy. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#isBusy()> 

### setMode

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMode(mode: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Changes the current mode. It must be one of [MODE_NORMAL](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#MODE_NORMAL:kotlin.Int), [MODE_SEND_ONLY](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#MODE_SEND_ONLY:kotlin.Int), and [MODE_RECEIVE_ONLY](https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#MODE_RECEIVE_ONLY:kotlin.Int).

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The mode to change to. |

| Exceptions ||
|--------------------------------------|-------------------------|
| `java.lang.IllegalArgumentException` | if the mode is invalid. |
| `java.lang.IllegalStateException` | if the stream is busy. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/net/rtp/RtpStream#isBusy()>

## Protected methods

### finalize

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

**Deprecated:** *Deprecated in Java.*

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
