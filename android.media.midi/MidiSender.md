# MidiSender

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MidiSender

Kotlin| [Java](MidiSender.md) 
| --- | --- |

```
abstract class MidiSender
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.midi.MidiSender](MidiSender.md) |

| Known Direct Subclasses [MidiOutputPort](MidiOutputPort.md) |----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------| | [MidiOutputPort](MidiOutputPort.md) | This class is used for receiving data from a port on a MIDI device | |
| --- | --- | --- | --- | --- | --- | --- |

Interface provided by a device to allow attaching MidiReceivers to a MIDI device.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------|---|
| [MidiSender](MidiSender.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](MidiSender.md))`(`receiver:` ` [MidiReceiver](MidiReceiver.md)!`)` Connects a [MidiReceiver](MidiReceiver.md) to the sender |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disconnect](MidiSender.md))`(`receiver:` ` [MidiReceiver](MidiReceiver.md)!`)` Disconnects a [MidiReceiver](MidiReceiver.md) from the sender |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConnect](MidiSender.md))`(`receiver:` ` [MidiReceiver](MidiReceiver.md)!`)` Called to connect a [MidiReceiver](MidiReceiver.md) to the sender |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDisconnect](MidiSender.md))`(`receiver:` ` [MidiReceiver](MidiReceiver.md)!`)` Called to disconnect a [MidiReceiver](MidiReceiver.md) from the sender |

## Public constructors

### MidiSender

```
MidiSender()
```

## Public methods

### connect

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun connect(receiver: MidiReceiver!): Unit
```

Connects a [MidiReceiver](MidiReceiver.md) to the sender

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `receiver` | [MidiReceiver](MidiReceiver.md)!:the receiver to connect |

### disconnect

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun disconnect(receiver: MidiReceiver!): Unit
```

Disconnects a [MidiReceiver](MidiReceiver.md) from the sender

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------|
| `receiver` | [MidiReceiver](MidiReceiver.md)!:the receiver to disconnect |

### onConnect

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onConnect(receiver: MidiReceiver!): Unit
```

Called to connect a [MidiReceiver](MidiReceiver.md) to the sender

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `receiver` | [MidiReceiver](MidiReceiver.md)!:the receiver to connect |

### onDisconnect

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDisconnect(receiver: MidiReceiver!): Unit
```

Called to disconnect a [MidiReceiver](MidiReceiver.md) from the sender

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------|
| `receiver` | [MidiReceiver](MidiReceiver.md)!:the receiver to disconnect |
