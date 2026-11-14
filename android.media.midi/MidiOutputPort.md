# MidiOutputPort

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MidiOutputPort

Kotlin| [Java](MidiOutputPort.md) 
| --- | --- |

```
class MidiOutputPort : MidiSender, Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.media.midi.MidiSender](MidiSender.md) ||
| | ↳ | [android.media.midi.MidiOutputPort](MidiOutputPort.md) |

This class is used for receiving data from a port on a MIDI device

## Summary

| Public methods ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](MidiOutputPort.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPortNumber](MidiOutputPort.md))`()` Returns the port number of this port |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConnect](MidiOutputPort.md))`(`receiver:` ` [MidiReceiver](MidiReceiver.md)!`)` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDisconnect](MidiOutputPort.md))`(`receiver:` ` [MidiReceiver](MidiReceiver.md)!`)` <br /> |

| Protected methods ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](MidiOutputPort.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [MidiSender](MidiSender.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](MidiSender.md))`(`receiver:` ` [MidiReceiver](MidiReceiver.md)!`)` <br /> Connects a [MidiReceiver](MidiReceiver.md) to the sender <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disconnect](MidiSender.md))`(`receiver:` ` [MidiReceiver](MidiReceiver.md)!`)` <br /> Disconnects a [MidiReceiver](MidiReceiver.md) from the sender <br /> | ||

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
| `receiver` | [MidiReceiver](MidiReceiver.md)!:the receiver to connect |

### onDisconnect

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun onDisconnect(receiver: MidiReceiver!): Unit
```

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------|
| `receiver` | [MidiReceiver](MidiReceiver.md)!:the receiver to disconnect |

## Protected methods

### finalize

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
