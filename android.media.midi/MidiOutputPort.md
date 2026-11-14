# MidiOutputPort

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MidiOutputPort

Kotlin| [Java](https://developer.android.com/reference/android/media/midi/MidiOutputPort "View this page in Java") 
| --- | --- |

```
class MidiOutputPort : MidiSender, Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.media.midi.MidiSender](https://developer.android.com/reference/kotlin/android/media/midi/MidiSender) ||
| | ↳ | [android.media.midi.MidiOutputPort](https://developer.android.com/reference/kotlin/android/media/midi/MidiOutputPort#) |

This class is used for receiving data from a port on a MIDI device

## Summary

| Public methods ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/media/midi/MidiOutputPort#close())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPortNumber](https://developer.android.com/reference/kotlin/android/media/midi/MidiOutputPort#getPortNumber())`()` Returns the port number of this port |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConnect](https://developer.android.com/reference/kotlin/android/media/midi/MidiOutputPort#onConnect(android.media.midi.MidiReceiver))`(`receiver:` ` [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver)!`)` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDisconnect](https://developer.android.com/reference/kotlin/android/media/midi/MidiOutputPort#onDisconnect(android.media.midi.MidiReceiver))`(`receiver:` ` [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver)!`)` <br /> |

| Protected methods ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/media/midi/MidiOutputPort#finalize())`()` <br /> |

| Inherited functions ||
|---|---|
| From class [MidiSender](https://developer.android.com/reference/kotlin/android/media/midi/MidiSender) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/android/media/midi/MidiSender#connect(android.media.midi.MidiReceiver))`(`receiver:` ` [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver)!`)` <br /> Connects a [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver) to the sender <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disconnect](https://developer.android.com/reference/kotlin/android/media/midi/MidiSender#disconnect(android.media.midi.MidiReceiver))`(`receiver:` ` [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver)!`)` <br /> Disconnects a [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver) from the sender <br /> | ||

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
| `receiver` | [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver)!:the receiver to connect |

### onDisconnect

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun onDisconnect(receiver: MidiReceiver!): Unit
```

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------|
| `receiver` | [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver)!:the receiver to disconnect |

## Protected methods

### finalize

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
