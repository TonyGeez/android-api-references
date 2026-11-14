# Channels

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Channels

```
class Channels
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.channels.Channels](Channels.md) |

Utility methods for channels and streams.

This class defines static methods that support the interoperation of the stream classes of the [java.io](../java.io/_package.md) package with the channel classes of this package.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ReadableByteChannel](ReadableByteChannel.md)! | [newChannel](Channels.md))`(`in:` ` [InputStream](../java.io/InputStream.md)!`)` Constructs a channel that reads bytes from the given stream. |
| static [WritableByteChannel](WritableByteChannel.md)! | [newChannel](Channels.md))`(`out:` ` [OutputStream](../java.io/OutputStream.md)!`)` Constructs a channel that writes bytes to the given stream. |
| static [InputStream](../java.io/InputStream.md)! | [newInputStream](Channels.md))`(`ch:` ` [AsynchronousByteChannel](AsynchronousByteChannel.md)!`)` Constructs a stream that reads bytes from the given channel. |
| --- | --- |
| static [InputStream](../java.io/InputStream.md)! | [newInputStream](Channels.md))`(`ch:` ` [ReadableByteChannel](ReadableByteChannel.md)!`)` Constructs a stream that reads bytes from the given channel. |
| static [OutputStream](../java.io/OutputStream.md)! | [newOutputStream](Channels.md))`(`ch:` ` [AsynchronousByteChannel](AsynchronousByteChannel.md)!`)` Constructs a stream that writes bytes to the given channel. |
| static [OutputStream](../java.io/OutputStream.md)! | [newOutputStream](Channels.md))`(`ch:` ` [WritableByteChannel](WritableByteChannel.md)!`)` Constructs a stream that writes bytes to the given channel. |
| --- | --- |
| static [Reader](../java.io/Reader.md)! | [newReader](Channels.md))`(`ch:` ` [ReadableByteChannel](ReadableByteChannel.md)!`, `csName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a reader that decodes bytes from the given channel according to the named charset. |
| static [Reader](../java.io/Reader.md)! | [newReader](Channels.md))`(`ch:` ` [ReadableByteChannel](ReadableByteChannel.md)!`, `charset:` ` [Charset](../java.nio.charset/Charset.md)!`)` Constructs a reader that decodes bytes from the given channel according to the given charset. |
| static [Reader](../java.io/Reader.md)! | [newReader](Channels.md))`(`ch:` ` [ReadableByteChannel](ReadableByteChannel.md)!`, `dec:` ` [CharsetDecoder](../java.nio.charset/CharsetDecoder.md)!`, `minBufferCap:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a reader that decodes bytes from the given channel using the given decoder. |
| --- | --- |
| static [Writer](../java.io/Writer.md)! | [newWriter](Channels.md))`(`ch:` ` [WritableByteChannel](WritableByteChannel.md)!`, `csName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a writer that encodes characters according to the named charset and writes the resulting bytes to the given channel. |
| static [Writer](../java.io/Writer.md)! | [newWriter](Channels.md))`(`ch:` ` [WritableByteChannel](WritableByteChannel.md)!`, `charset:` ` [Charset](../java.nio.charset/Charset.md)!`)` Constructs a writer that encodes characters according to the given charset and writes the resulting bytes to the given channel. |
| static [Writer](../java.io/Writer.md)! | [newWriter](Channels.md))`(`ch:` ` [WritableByteChannel](WritableByteChannel.md)!`, `enc:` ` [CharsetEncoder](../java.nio.charset/CharsetEncoder.md)!`, `minBufferCap:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a writer that encodes characters using the given encoder and writes the resulting bytes to the given channel. |
| --- | --- |

## Public methods

### newChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newChannel(in: InputStream!): ReadableByteChannel!
```

Constructs a channel that reads bytes from the given stream.

The resulting channel will not be buffered; it will simply redirect its I/O operations to the given stream. Closing the channel will in turn cause the stream to be closed.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------|
| `in` | [InputStream](../java.io/InputStream.md)!:The stream from which bytes are to be read |

| Return ||
|--------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ReadableByteChannel](ReadableByteChannel.md)! | A new readable byte channel |

### newChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newChannel(out: OutputStream!): WritableByteChannel!
```

Constructs a channel that writes bytes to the given stream.

The resulting channel will not be buffered; it will simply redirect its I/O operations to the given stream. Closing the channel will in turn cause the stream to be closed.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](../java.io/OutputStream.md)!:The stream to which bytes are to be written |

| Return ||
|--------------------------------------------------------------------------------------------------------------|-----------------------------|
| [WritableByteChannel](WritableByteChannel.md)! | A new writable byte channel |

### newInputStream

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newInputStream(ch: AsynchronousByteChannel!): InputStream!
```

Constructs a stream that reads bytes from the given channel.

The stream will not be buffered, and it will not support the [mark](../java.io/InputStream.md))or [reset](../java.io/InputStream.md))methods. The stream will be safe for access by multiple concurrent threads. Closing the stream will in turn cause the channel to be closed.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [AsynchronousByteChannel](AsynchronousByteChannel.md)!:The channel from which bytes will be read |

| Return ||
|------------------------------------------------------------------------------------------|--------------------|
| [InputStream](../java.io/InputStream.md)! | A new input stream |

### newInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newInputStream(ch: ReadableByteChannel!): InputStream!
```

Constructs a stream that reads bytes from the given channel.

The`read`methods of the resulting stream will throw an [IllegalBlockingModeException](IllegalBlockingModeException.md) if invoked while the underlying channel is in non-blocking mode. The stream will not be buffered, and it will not support the [mark](../java.io/InputStream.md))or [reset](../java.io/InputStream.md))methods. The stream will be safe for access by multiple concurrent threads. Closing the stream will in turn cause the channel to be closed.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [ReadableByteChannel](ReadableByteChannel.md)!:The channel from which bytes will be read |

| Return ||
|------------------------------------------------------------------------------------------|--------------------|
| [InputStream](../java.io/InputStream.md)! | A new input stream |

### newOutputStream

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newOutputStream(ch: AsynchronousByteChannel!): OutputStream!
```

Constructs a stream that writes bytes to the given channel.

The stream will not be buffered. The stream will be safe for access by multiple concurrent threads. Closing the stream will in turn cause the channel to be closed.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [AsynchronousByteChannel](AsynchronousByteChannel.md)!:The channel to which bytes will be written |

| Return ||
|--------------------------------------------------------------------------------------------|---------------------|
| [OutputStream](../java.io/OutputStream.md)! | A new output stream |

### newOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newOutputStream(ch: WritableByteChannel!): OutputStream!
```

Constructs a stream that writes bytes to the given channel.

The`write`methods of the resulting stream will throw an [IllegalBlockingModeException](IllegalBlockingModeException.md) if invoked while the underlying channel is in non-blocking mode. The stream will not be buffered. The stream will be safe for access by multiple concurrent threads. Closing the stream will in turn cause the channel to be closed.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [WritableByteChannel](WritableByteChannel.md)!:The channel to which bytes will be written |

| Return ||
|--------------------------------------------------------------------------------------------|---------------------|
| [OutputStream](../java.io/OutputStream.md)! | A new output stream |

### newReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newReader(
    ch: ReadableByteChannel!, 
    csName: String!
): Reader!
```

Constructs a reader that decodes bytes from the given channel according to the named charset.

An invocation of this method of the form 

```kotlin
<code>Channels.newReader(ch, csname)
  </code>
```
behaves in exactly the same way as the expression 

```kotlin
<code>Channels.newReader(ch, Charset.forName(csName))
  </code>
```

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [ReadableByteChannel](ReadableByteChannel.md)!:The channel from which bytes will be read |
| `csName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the charset to be used |

| Return ||
|--------------------------------------------------------------------------------|--------------|
| [Reader](../java.io/Reader.md)! | A new reader |

| Exceptions ||
|------------------------------------------------|-----------------------------------------------------------------------------------------------|
| `java.nio.charset.UnsupportedCharsetException` | If no support for the named charset is available in this instance of the Java virtual machine |

### newReader

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newReader(
    ch: ReadableByteChannel!, 
    charset: Charset!
): Reader!
```

Constructs a reader that decodes bytes from the given channel according to the given charset.

An invocation of this method of the form 

```kotlin
<code>Channels.newReader(ch, charset)
  </code>
```
behaves in exactly the same way as the expression 

```kotlin
<code>Channels.newReader(ch, Charset.forName(csName).newDecoder(), -1)
  </code>
```

The reader's default action for malformed-input and unmappable-character errors is to [report](../java.nio.charset/CodingErrorAction.md) them. When more control over the error handling is required, the constructor that takes a [java.nio.charset.CharsetDecoder](../java.nio.charset/CharsetDecoder.md) should be used.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [ReadableByteChannel](ReadableByteChannel.md)!:The channel from which bytes will be read |
| `charset` | [Charset](../java.nio.charset/Charset.md)!:The charset to be used |

| Return ||
|--------------------------------------------------------------------------------|--------------|
| [Reader](../java.io/Reader.md)! | A new reader |

### newReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newReader(
    ch: ReadableByteChannel!, 
    dec: CharsetDecoder!, 
    minBufferCap: Int
): Reader!
```

Constructs a reader that decodes bytes from the given channel using the given decoder.

The resulting stream will contain an internal input buffer of at least`minBufferCap`bytes. The stream's`read`methods will, as needed, fill the buffer by reading bytes from the underlying channel; if the channel is in non-blocking mode when bytes are to be read then an [IllegalBlockingModeException](IllegalBlockingModeException.md) will be thrown. The resulting stream will not otherwise be buffered, and it will not support the [mark](../java.io/Reader.md))or [reset](../java.io/Reader.md))methods. Closing the stream will in turn cause the channel to be closed.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [ReadableByteChannel](ReadableByteChannel.md)!:The channel from which bytes will be read |
| `dec` | [CharsetDecoder](../java.nio.charset/CharsetDecoder.md)!:The charset decoder to be used |
| `minBufferCap` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The minimum capacity of the internal byte buffer, or`-1`if an implementation-dependent default capacity is to be used |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------|--------------|
| [Reader](../java.io/Reader.md)! | A new reader |

### newWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newWriter(
    ch: WritableByteChannel!, 
    csName: String!
): Writer!
```

Constructs a writer that encodes characters according to the named charset and writes the resulting bytes to the given channel.

An invocation of this method of the form 

```kotlin
<code>Channels.newWriter(ch, csname)
  </code>
```
behaves in exactly the same way as the expression 

```kotlin
<code>Channels.newWriter(ch, Charset.forName(csName))
  </code>
```

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [WritableByteChannel](WritableByteChannel.md)!:The channel to which bytes will be written |
| `csName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the charset to be used |

| Return ||
|--------------------------------------------------------------------------------|--------------|
| [Writer](../java.io/Writer.md)! | A new writer |

| Exceptions ||
|------------------------------------------------|-----------------------------------------------------------------------------------------------|
| `java.nio.charset.UnsupportedCharsetException` | If no support for the named charset is available in this instance of the Java virtual machine |

### newWriter

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newWriter(
    ch: WritableByteChannel!, 
    charset: Charset!
): Writer!
```

Constructs a writer that encodes characters according to the given charset and writes the resulting bytes to the given channel.

An invocation of this method of the form 

```kotlin
<code>Channels.newWriter(ch, charset)
  </code>
```
behaves in exactly the same way as the expression 

```kotlin
<code>Channels.newWriter(ch, Charset.forName(csName).newEncoder(), -1)
  </code>
```

The writer's default action for malformed-input and unmappable-character errors is to [report](../java.nio.charset/CodingErrorAction.md) them. When more control over the error handling is required, the constructor that takes a [java.nio.charset.CharsetEncoder](../java.nio.charset/CharsetEncoder.md) should be used.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [WritableByteChannel](WritableByteChannel.md)!:The channel to which bytes will be written |
| `charset` | [Charset](../java.nio.charset/Charset.md)!:The charset to be used |

| Return ||
|--------------------------------------------------------------------------------|--------------|
| [Writer](../java.io/Writer.md)! | A new writer |

### newWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newWriter(
    ch: WritableByteChannel!, 
    enc: CharsetEncoder!, 
    minBufferCap: Int
): Writer!
```

Constructs a writer that encodes characters using the given encoder and writes the resulting bytes to the given channel.

The resulting stream will contain an internal output buffer of at least`minBufferCap`bytes. The stream's`write`methods will, as needed, flush the buffer by writing bytes to the underlying channel; if the channel is in non-blocking mode when bytes are to be written then an [IllegalBlockingModeException](IllegalBlockingModeException.md) will be thrown. The resulting stream will not otherwise be buffered. Closing the stream will in turn cause the channel to be closed.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [WritableByteChannel](WritableByteChannel.md)!:The channel to which bytes will be written |
| `enc` | [CharsetEncoder](../java.nio.charset/CharsetEncoder.md)!:The charset encoder to be used |
| `minBufferCap` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The minimum capacity of the internal byte buffer, or`-1`if an implementation-dependent default capacity is to be used |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------|--------------|
| [Writer](../java.io/Writer.md)! | A new writer |
