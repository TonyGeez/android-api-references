# android.media.midi

# android.media.midi

Kotlin| [Java](https://developer.android.com/reference/android/media/midi/package-summary "View this page in Java")
| --- | --- |

## Interfaces

| [OnDeviceOpenedListener](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.OnDeviceOpenedListener) | Listener class used for receiving the results of [openDevice](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#openDevice(android.media.midi.MidiDeviceInfo,%20android.media.midi.MidiManager.OnDeviceOpenedListener,%20android.os.Handler))and [openBluetoothDevice](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#openBluetoothDevice(android.bluetooth.BluetoothDevice,%20android.media.midi.MidiManager.OnDeviceOpenedListener,%20android.os.Handler)) |
| --- | --- |

## Classes

| [MidiDevice](https://developer.android.com/reference/kotlin/android/media/midi/MidiDevice) | This class is used for sending and receiving data to and from a MIDI device Instances of this class are created by [MidiManager.openDevice](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#openDevice(android.media.midi.MidiDeviceInfo,%20android.media.midi.MidiManager.OnDeviceOpenedListener,%20android.os.Handler)). |
| --- | --- |
| [MidiDeviceInfo](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo) | This class contains information to describe a MIDI device. |
| [MidiDeviceService](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceService) | A service that implements a virtual MIDI device. |
| [MidiDeviceStatus](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceStatus) | This is an immutable class that describes the current status of a MIDI device's ports. |
| --- | --- |
| [MidiInputPort](https://developer.android.com/reference/kotlin/android/media/midi/MidiInputPort) | This class is used for sending data to a port on a MIDI device |
| [MidiManager](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager) | This class is the public application interface to the MIDI service. |
| [MidiOutputPort](https://developer.android.com/reference/kotlin/android/media/midi/MidiOutputPort) | This class is used for receiving data from a port on a MIDI device |
| --- | --- |
| [MidiReceiver](https://developer.android.com/reference/kotlin/android/media/midi/MidiReceiver) | Interface for sending and receiving data to and from a MIDI device. |
| [MidiSender](https://developer.android.com/reference/kotlin/android/media/midi/MidiSender) | Interface provided by a device to allow attaching MidiReceivers to a MIDI device. |
| [MidiUmpDeviceService](https://developer.android.com/reference/kotlin/android/media/midi/MidiUmpDeviceService) | A service that implements a virtual MIDI device for Universal MIDI Packets (UMP). |
| --- | --- |
