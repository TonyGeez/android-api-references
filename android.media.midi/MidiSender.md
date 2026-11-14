# MidiSender

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MidiSender

Kotlin| [Java](https://developer.android.com/reference/android/media/midi/MidiSender "View this page in Java") 
| --- | --- |

```
abstract class MidiSender
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.midi.MidiSender](https://developer.android.com/reference/kotlin/android/media/midi/MidiSender#) |

| Known Direct Subclasses [MidiOutputPort](https://developer.android.com/reference/kotlin/android/media/midi/MidiOutputPort) |----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------| | [MidiOutputPort](https://developer.android.com/reference/kotlin/android/media/midi/MidiOutputPort) | This class is used for receiving data from a port on a MIDI device | |
| --- | --- | --- | --- | --- | --- | --- |

Interface provided by a device to allow attaching MidiReceivers to a MIDI device.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------|---|
| [MidiSender](https://developer.android.com/reference/kotlin/android/media/midi/MidiSender#MidiSender())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/android/media/midi/MidiSender#connect(android.media.midi.MidiReceiver))`(`receiver:` ` [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver)!`)` Connects a [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver) to the sender |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disconnect](https://developer.android.com/reference/kotlin/android/media/midi/MidiSender#disconnect(android.media.midi.MidiReceiver))`(`receiver:` ` [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver)!`)` Disconnects a [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver) from the sender |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConnect](https://developer.android.com/reference/kotlin/android/media/midi/MidiSender#onConnect(android.media.midi.MidiReceiver))`(`receiver:` ` [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver)!`)` Called to connect a [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver) to the sender |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDisconnect](https://developer.android.com/reference/kotlin/android/media/midi/MidiSender#onDisconnect(android.media.midi.MidiReceiver))`(`receiver:` ` [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver)!`)` Called to disconnect a [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver) from the sender |

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

Connects a [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver) to the sender

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `receiver` | [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver)!:the receiver to connect |

### disconnect

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun disconnect(receiver: MidiReceiver!): Unit
```

Disconnects a [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver) from the sender

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------|
| `receiver` | [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver)!:the receiver to disconnect |

### onConnect

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onConnect(receiver: MidiReceiver!): Unit
```

Called to connect a [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver) to the sender

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `receiver` | [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver)!:the receiver to connect |

### onDisconnect

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDisconnect(receiver: MidiReceiver!): Unit
```

Called to disconnect a [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver) from the sender

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------|
| `receiver` | [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver)!:the receiver to disconnect |
