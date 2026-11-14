# MidiOutputPort

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MidiOutputPort

Kotlin| [Java](../android/media/midi/MidiOutputPort.md) 
| --- | --- |

```
class MidiOutputPort : MidiSender, Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.media.midi.MidiSender](../android/media/midi/MidiSender.md) ||
| | ↳ | [android.media.midi.MidiOutputPort](../android/media/midi/MidiOutputPort.md) |

This class is used for receiving data from a port on a MIDI device

## Summary

| Public methods ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/media/midi/MidiOutputPort.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPortNumber](../android/media/midi/MidiOutputPort.md))`()` Returns the port number of this port |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConnect](../android/media/midi/MidiOutputPort.md))`(`receiver:` ` [MidiReceiver](../android/media/midi/MidiReceiver.md)!`)` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDisconnect](../android/media/midi/MidiOutputPort.md))`(`receiver:` ` [MidiReceiver](../android/media/midi/MidiReceiver.md)!`)` <br /> |

| Protected methods ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/media/midi/MidiOutputPort.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [MidiSender](../android/media/midi/MidiSender.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](../android/media/midi/MidiSender.md))`(`receiver:` ` [MidiReceiver](../android/media/midi/MidiReceiver.md)!`)` <br /> Connects a [MidiReceiver](../android/media/midi/MidiReceiver.md) to the sender <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disconnect](../android/media/midi/MidiSender.md))`(`receiver:` ` [MidiReceiver](../android/media/midi/MidiReceiver.md)!`)` <br /> Disconnects a [MidiReceiver](../android/media/midi/MidiReceiver.md) from the sender <br /> | ||

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

### onConnect

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun onConnect(receiver: MidiReceiver!): Unit
```

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `receiver` | [MidiReceiver](../android/media/midi/MidiReceiver.md)!:the receiver to connect |

### onDisconnect

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun onDisconnect(receiver: MidiReceiver!): Unit
```

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------|
| `receiver` | [MidiReceiver](../android/media/midi/MidiReceiver.md)!:the receiver to disconnect |

## Protected methods

### finalize

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
