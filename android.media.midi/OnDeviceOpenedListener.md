# MidiManager.OnDeviceOpenedListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDeviceOpenedListener

Kotlin| [Java](https://developer.android.com/reference/android/media/midi/MidiManager.OnDeviceOpenedListener "View this page in Java") 

```
interface OnDeviceOpenedListener
```

| [android.media.midi.MidiManager.OnDeviceOpenedListener](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.OnDeviceOpenedListener#) |

Listener class used for receiving the results of [openDevice](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#openDevice(android.media.midi.MidiDeviceInfo,%20android.media.midi.MidiManager.OnDeviceOpenedListener,%20android.os.Handler))and [openBluetoothDevice](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#openBluetoothDevice(android.bluetooth.BluetoothDevice,%20android.media.midi.MidiManager.OnDeviceOpenedListener,%20android.os.Handler))

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDeviceOpened](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.OnDeviceOpenedListener#onDeviceOpened(android.media.midi.MidiDevice))`(`device:` ` [MidiDevice](https://developer.android.com/reference/kotlin/android/media/midi/MidiDevice)!`)` Called to respond to a [openDevice](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#openDevice(android.media.midi.MidiDeviceInfo,%20android.media.midi.MidiManager.OnDeviceOpenedListener,%20android.os.Handler))request |

## Public methods

### onDeviceOpened

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDeviceOpened(device: MidiDevice!): Unit
```

Called to respond to a [openDevice](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#openDevice(android.media.midi.MidiDeviceInfo,%20android.media.midi.MidiManager.OnDeviceOpenedListener,%20android.os.Handler))request

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [MidiDevice](https://developer.android.com/reference/kotlin/android/media/midi/MidiDevice)!:a [MidiDevice](https://developer.android.com/reference/kotlin/android/media/midi/MidiDevice) for opened device, or null if opening failed |
