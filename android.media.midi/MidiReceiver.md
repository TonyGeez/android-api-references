# MidiReceiver

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MidiReceiver

Kotlin| [Java](../android/media/midi/MidiReceiver.md) 
| --- | --- |

```
abstract class MidiReceiver
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.midi.MidiReceiver](../android/media/midi/MidiReceiver.md) |

| Known Direct Subclasses [MidiInputPort](../android/media/midi/MidiInputPort.md) |--------------------------------------------------------------------------------------------------|----------------------------------------------------------------| | [MidiInputPort](../android/media/midi/MidiInputPort.md) | This class is used for sending data to a port on a MIDI device | |
| --- | --- | --- | --- | --- | --- | --- |

Interface for sending and receiving data to and from a MIDI device.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MidiReceiver](../android/media/midi/MidiReceiver.md))`()` Default MidiReceiver constructor. |
| [MidiReceiver](../android/media/midi/MidiReceiver.md))`(`maxMessageSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` MidiReceiver constructor. |

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](../android/media/midi/MidiReceiver.md))`()` Instructs the receiver to discard all pending MIDI data. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxMessageSize](../android/media/midi/MidiReceiver.md))`()` Returns the maximum size of a message this receiver can receive. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFlush](../android/media/midi/MidiReceiver.md))`()` Called when the receiver is instructed to discard all pending MIDI data. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSend](../android/media/midi/MidiReceiver.md))`(`msg:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timestamp:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Called whenever the receiver is passed new MIDI data. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [send](../android/media/midi/MidiReceiver.md))`(`msg:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called to send MIDI data to the receiver without a timestamp. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [send](../android/media/midi/MidiReceiver.md))`(`msg:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timestamp:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Called to send MIDI data to the receiver with a specified timestamp. |
| --- | --- |

## Public constructors

### MidiReceiver

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MidiReceiver()
```

Default MidiReceiver constructor. Maximum message size is set to [java.lang.Integer#MAX_VALUE](../java/lang/Integer.md) 

### MidiReceiver

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MidiReceiver(maxMessageSize: Int)
```

MidiReceiver constructor.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `maxMessageSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum size of a message this receiver can receive |

## Public methods

### flush

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun flush(): Unit
```

Instructs the receiver to discard all pending MIDI data.

| Exceptions ||
|-----------------------|---|
| `java.io.IOException` | |

### getMaxMessageSize

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxMessageSize(): Int
```

Returns the maximum size of a message this receiver can receive.

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | maximum message size |

### onFlush

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onFlush(): Unit
```

Called when the receiver is instructed to discard all pending MIDI data. Subclasses should override this method if they maintain a list or queue of MIDI data to be processed in the future.

| Exceptions ||
|-----------------------|---|
| `java.io.IOException` | |

### onSend

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSend(
    msg: ByteArray!, 
    offset: Int, 
    count: Int, 
    timestamp: Long
): Unit
```

Called whenever the receiver is passed new MIDI data. Subclasses override this method to receive MIDI data. May fail if count exceeds [getMaxMessageSize](../android/media/midi/MidiReceiver.md)). NOTE: the msg array parameter is only valid within the context of this call. The msg bytes should be copied by the receiver rather than retaining a reference to this parameter. Also, modifying the contents of the msg array parameter may result in other receivers in the same application receiving incorrect values in their {link #onSend} method.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `msg` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:a byte array containing the MIDI data |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset of the first byte of the data in the array to be processed |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes of MIDI data in the array to be processed |
| --- | --- |
| `timestamp` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the timestamp of the message (based on [java.lang.System#nanoTime](../java/lang/System.md)) |

| Exceptions ||
|-----------------------|---|
| `java.io.IOException` | |

### send

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun send(
    msg: ByteArray!, 
    offset: Int, 
    count: Int
): Unit
```

Called to send MIDI data to the receiver without a timestamp. Data will be processed by receiver in the order sent. Data will get split into multiple calls to [onSend](../android/media/midi/MidiReceiver.md))if count exceeds [getMaxMessageSize](../android/media/midi/MidiReceiver.md)). Blocks until all the data is sent or an exception occurs. In the latter case, the amount of data sent prior to the exception is not provided to caller. The communication should be considered corrupt. The sender should reestablish communication, reset all controllers and send all notes off.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `msg` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:a byte array containing the MIDI data |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset of the first byte of the data in the array to be sent |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes of MIDI data in the array to be sent |
| --- | --- |

| Exceptions ||
|-----------------------|-------------------------------------------|
| `java.io.IOException` | if the data could not be sent in entirety |

### send

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun send(
    msg: ByteArray!, 
    offset: Int, 
    count: Int, 
    timestamp: Long
): Unit
```

Called to send MIDI data to the receiver with a specified timestamp. Data will be processed by receiver in order first by timestamp, then in the order sent. Data will get split into multiple calls to [onSend](../android/media/midi/MidiReceiver.md))if count exceeds [getMaxMessageSize](../android/media/midi/MidiReceiver.md)). Blocks until all the data is sent or an exception occurs. In the latter case, the amount of data sent prior to the exception is not provided to caller. The communication should be considered corrupt. The sender should reestablish communication, reset all controllers and send all notes off.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `msg` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:a byte array containing the MIDI data |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset of the first byte of the data in the array to be sent |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes of MIDI data in the array to be sent |
| --- | --- |
| `timestamp` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the timestamp of the message, based on [java.lang.System#nanoTime](../java/lang/System.md)) |

| Exceptions ||
|-----------------------|-------------------------------------------|
| `java.io.IOException` | if the data could not be sent in entirety |
