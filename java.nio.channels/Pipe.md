# Pipe

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Pipe

```
abstract class Pipe
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.nio.channels.Pipe](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe#) |

A pair of channels that implements a unidirectional pipe.

A pipe consists of a pair of channels: A writable [sink](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SinkChannel) channel and a readable [source](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SourceChannel) channel. Once some bytes are written to the sink channel they can be read from the source channel in exactly the order in which they were written.

Whether or not a thread writing bytes to a pipe will block until another thread reads those bytes, or some previously-written bytes, from the pipe is system-dependent and therefore unspecified. Many pipe implementations will buffer up to a certain number of bytes between the sink and source channels, but such buffering should not be assumed.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [SinkChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SinkChannel) A channel representing the writable end of a [Pipe](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe#). |
| abstract | [SourceChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SourceChannel) A channel representing the readable end of a [Pipe](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe#). |

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------------------|---|
| [Pipe](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe#Pipe())`()` Initializes a new instance of this class. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Pipe](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe#)! | [open](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe#open())`()` Opens a pipe. |
| abstract [Pipe.SinkChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SinkChannel)! | [sink](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe#sink())`()` Returns this pipe's sink channel. |
| abstract [Pipe.SourceChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SourceChannel)! | [source](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe#source())`()` Returns this pipe's source channel. |

## Protected constructors

### Pipe

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Pipe()
```

Initializes a new instance of this class.

## Public methods

### open

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun open(): Pipe!
```

Opens a pipe.

The new pipe is created by invoking the [openPipe](https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider#openPipe())method of the system-wide default [java.nio.channels.spi.SelectorProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider) object.

| Return ||
|---------------------------------------------------------------------------------|------------|
| [Pipe](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe#)! | A new pipe |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### sink

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun sink(): Pipe.SinkChannel!
```

Returns this pipe's sink channel.

| Return ||
|--------------------------------------------------------------------------------------------------------|--------------------------|
| [Pipe.SinkChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SinkChannel)! | This pipe's sink channel |

### source

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun source(): Pipe.SourceChannel!
```

Returns this pipe's source channel.

| Return ||
|------------------------------------------------------------------------------------------------------------|----------------------------|
| [Pipe.SourceChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SourceChannel)! | This pipe's source channel |
