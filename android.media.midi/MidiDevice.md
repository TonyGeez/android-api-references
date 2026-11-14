Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MidiDevice

Kotlin | [Java](MidiDevice.md)
| --- | --- |

```
class MidiDevice : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.midi.MidiDevice](MidiDevice.md) |

This class is used for sending and receiving data to and from a MIDI device Instances of this class are created by openDevice.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/media/midi/MidiDevice.MidiConnection` This class represents a connection between the output port of one device and the input port of another. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | close Closes this stream and releases any system resources associated with it. |
| [MidiDevice.MidiConnection](../android/media/midi/MidiDevice.MidiConnection.md)! | connectPorts Connects the supplied MidiInputPort to the output port of this device with the specified port number. |
| [MidiDeviceInfo](MidiDeviceInfo.md)! | getInfo Returns a MidiDeviceInfo object, which describes this device. |
| --- | --- |
| [MidiInputPort](MidiInputPort.md)! | openInputPort Called to open a MidiInputPort for the specified port number. |
| [MidiOutputPort](MidiOutputPort.md)! | openOutputPort Called to open a MidiOutputPort for the specified port number. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| --- | --- |

| Protected methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | finalize Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

## Public methods

### close

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun close(): Unit
```

Closes this stream and releases any system resources associated with it. If the stream is already closed then invoking this method has no effect.

As noted in close, cases where the close may fail require careful attention. It is strongly advised to relinquish the underlying resources and to internally *mark* the `Closeable` as closed, prior to throwing the `IOException`.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

### connectPorts

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun connectPorts(
    inputPort: MidiInputPort!, 
    outputPortNumber: Int
): MidiDevice.MidiConnection!
```

Connects the supplied MidiInputPort to the output port of this device with the specified port number. Once the connection is made, the MidiInput port instance can no longer receive data via its onSend method. This method returns a `https://developer.android.com/reference/kotlin/android/media/midi/MidiDevice.MidiConnection` object, which can be used to close the connection.

| Parameters ||
|---|---|
| `inputPort` | [MidiInputPort](MidiInputPort.md)!: the inputPort to connect |
| `outputPortNumber` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the port number of the output port to connect inputPort to. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/midi/MidiDevice.MidiConnection!` | `https://developer.android.com/reference/kotlin/android/media/midi/MidiDevice.MidiConnection` object if the connection is successful, or null in case of failure. |

### getInfo

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInfo(): MidiDeviceInfo!
```

Returns a MidiDeviceInfo object, which describes this device.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo!` | the MidiDeviceInfo object |

### openInputPort

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun openInputPort(portNumber: Int): MidiInputPort!
```

Called to open a MidiInputPort for the specified port number. An input port can only be used by one sender at a time. Opening an input port will fail if another application has already opened it for use. A MidiDeviceStatus can be used to determine if an input port is already open.

| Parameters ||
|---|---|
| `portNumber` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of the input port to open |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/midi/MidiInputPort!` | the MidiInputPort if the open is successful, or null in case of failure. |

### openOutputPort

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun openOutputPort(portNumber: Int): MidiOutputPort!
```

Called to open a MidiOutputPort for the specified port number. An output port may be opened by multiple applications.

| Parameters ||
|---|---|
| `portNumber` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of the output port to open |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/midi/MidiOutputPort!` | the MidiOutputPort if the open is successful, or null in case of failure. |

### toString

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

## Protected methods

### finalize

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun finalize(): Unit
```

Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup.

The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded.

The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition.

The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates.

After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded.

The `finalize` method is never invoked more than once by a Java virtual machine for any given object.

Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored.

| Exceptions ||
|---|---|
| `java.lang.Throwable` | the `Exception` raised by this method |
