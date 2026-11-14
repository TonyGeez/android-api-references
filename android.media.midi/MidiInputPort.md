# MidiInputPort

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MidiInputPort

Kotlin| [Java](MidiInputPort.md) 
| --- | --- |

```
class MidiInputPort : MidiReceiver, Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.media.midi.MidiReceiver](MidiReceiver.md) ||
| | ↳ | [android.media.midi.MidiInputPort](MidiInputPort.md) |

This class is used for sending data to a port on a MIDI device

## Summary

| Public methods ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](MidiInputPort.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPortNumber](MidiInputPort.md))`()` Returns the port number of this port |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFlush](MidiInputPort.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSend](MidiInputPort.md))`(`msg:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timestamp:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> |

| Protected methods ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](MidiInputPort.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [MidiReceiver](MidiReceiver.md) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](MidiReceiver.md))`()` <br /> Instructs the receiver to discard all pending MIDI data. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxMessageSize](MidiReceiver.md))`()` <br /> Returns the maximum size of a message this receiver can receive. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [send](MidiReceiver.md))`(`msg:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Called to send MIDI data to the receiver without a timestamp. Data will be processed by receiver in the order sent. Data will get split into multiple calls to [onSend](MidiReceiver.md))if count exceeds [getMaxMessageSize](MidiReceiver.md)). Blocks until all the data is sent or an exception occurs. In the latter case, the amount of data sent prior to the exception is not provided to caller. The communication should be considered corrupt. The sender should reestablish communication, reset all controllers and send all notes off. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [send](MidiReceiver.md))`(`msg:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timestamp:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Called to send MIDI data to the receiver with a specified timestamp. Data will be processed by receiver in order first by timestamp, then in the order sent. Data will get split into multiple calls to [onSend](MidiReceiver.md))if count exceeds [getMaxMessageSize](MidiReceiver.md)). Blocks until all the data is sent or an exception occurs. In the latter case, the amount of data sent prior to the exception is not provided to caller. The communication should be considered corrupt. The sender should reestablish communication, reset all controllers and send all notes off. <br /> | ||

## Public methods

### close

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

### getPortNumber

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPortNumber(): Int
```

Returns the port number of this port

| Return ||
|----------------------------------------------------------------------------|------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the port's port number |

### onFlush

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun onFlush(): Unit
```

| Exceptions ||
|-----------------------|---|
| `java.io.IOException` | |

### onSend

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun onSend(
    msg: ByteArray!, 
    offset: Int, 
    count: Int, 
    timestamp: Long
): Unit
```

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `msg` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:a byte array containing the MIDI data |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset of the first byte of the data in the array to be processed |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes of MIDI data in the array to be processed |
| --- | --- |
| `timestamp` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the timestamp of the message (based on [java.lang.System#nanoTime](../java.lang/System.md)) |

| Exceptions ||
|-----------------------|---|
| `java.io.IOException` | |

## Protected methods

### finalize

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
