# MidiSender

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MidiSender

Kotlin| [Java](../android/media/midi/MidiSender.md) 
| --- | --- |

```
abstract class MidiSender
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.midi.MidiSender](../android/media/midi/MidiSender.md) |

| Known Direct Subclasses [MidiOutputPort](../android/media/midi/MidiOutputPort.md) |----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------| | [MidiOutputPort](../android/media/midi/MidiOutputPort.md) | This class is used for receiving data from a port on a MIDI device | |
| --- | --- | --- | --- | --- | --- | --- |

Interface provided by a device to allow attaching MidiReceivers to a MIDI device.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------|---|
| [MidiSender](../android/media/midi/MidiSender.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](../android/media/midi/MidiSender.md))`(`receiver:` ` [MidiReceiver](../android/media/midi/MidiReceiver.md)!`)` Connects a [MidiReceiver](../android/media/midi/MidiReceiver.md) to the sender |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disconnect](../android/media/midi/MidiSender.md))`(`receiver:` ` [MidiReceiver](../android/media/midi/MidiReceiver.md)!`)` Disconnects a [MidiReceiver](../android/media/midi/MidiReceiver.md) from the sender |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConnect](../android/media/midi/MidiSender.md))`(`receiver:` ` [MidiReceiver](../android/media/midi/MidiReceiver.md)!`)` Called to connect a [MidiReceiver](../android/media/midi/MidiReceiver.md) to the sender |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDisconnect](../android/media/midi/MidiSender.md))`(`receiver:` ` [MidiReceiver](../android/media/midi/MidiReceiver.md)!`)` Called to disconnect a [MidiReceiver](../android/media/midi/MidiReceiver.md) from the sender |

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

Connects a [MidiReceiver](../android/media/midi/MidiReceiver.md) to the sender

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `receiver` | [MidiReceiver](../android/media/midi/MidiReceiver.md)!:the receiver to connect |

### disconnect

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun disconnect(receiver: MidiReceiver!): Unit
```

Disconnects a [MidiReceiver](../android/media/midi/MidiReceiver.md) from the sender

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------|
| `receiver` | [MidiReceiver](../android/media/midi/MidiReceiver.md)!:the receiver to disconnect |

### onConnect

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onConnect(receiver: MidiReceiver!): Unit
```

Called to connect a [MidiReceiver](../android/media/midi/MidiReceiver.md) to the sender

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `receiver` | [MidiReceiver](../android/media/midi/MidiReceiver.md)!:the receiver to connect |

### onDisconnect

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDisconnect(receiver: MidiReceiver!): Unit
```

Called to disconnect a [MidiReceiver](../android/media/midi/MidiReceiver.md) from the sender

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------|
| `receiver` | [MidiReceiver](../android/media/midi/MidiReceiver.md)!:the receiver to disconnect |
