# MidiManager.OnDeviceOpenedListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDeviceOpenedListener

Kotlin| [Java](../android/media/midi/MidiManager.OnDeviceOpenedListener.md) 
| --- | --- |

```
interface OnDeviceOpenedListener
```

| [android.media.midi.MidiManager.OnDeviceOpenedListener](../android/media/midi/MidiManager.OnDeviceOpenedListener.md) |

Listener class used for receiving the results of [openDevice](MidiManager.md))and [openBluetoothDevice](MidiManager.md))

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDeviceOpened](../android/media/midi/MidiManager.OnDeviceOpenedListener.md))`(`device:` ` [MidiDevice](MidiDevice.md)!`)` Called to respond to a [openDevice](MidiManager.md))request |

## Public methods

### onDeviceOpened

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDeviceOpened(device: MidiDevice!): Unit
```

Called to respond to a [openDevice](MidiManager.md))request

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [MidiDevice](MidiDevice.md)!:a [MidiDevice](MidiDevice.md) for opened device, or null if opening failed |
