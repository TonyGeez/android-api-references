# Channels

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Channels

```
class Channels
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.channels.Channels](https://developer.android.com/reference/kotlin/java/nio/channels/Channels#) |

Utility methods for channels and streams.

This class defines static methods that support the interoperation of the stream classes of the [java.io](https://developer.android.com/reference/kotlin/java/io/package-summary.html) package with the channel classes of this package.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ReadableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ReadableByteChannel)! | [newChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Channels#newChannel(java.io.InputStream))`(`in:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` Constructs a channel that reads bytes from the given stream. |
| static [WritableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/WritableByteChannel)! | [newChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Channels#newChannel(java.io.OutputStream))`(`out:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`)` Constructs a channel that writes bytes to the given stream. |
| static [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | [newInputStream](https://developer.android.com/reference/kotlin/java/nio/channels/Channels#newInputStream(java.nio.channels.AsynchronousByteChannel))`(`ch:` ` [AsynchronousByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousByteChannel)!`)` Constructs a stream that reads bytes from the given channel. |
| --- | --- |
| static [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | [newInputStream](https://developer.android.com/reference/kotlin/java/nio/channels/Channels#newInputStream(java.nio.channels.ReadableByteChannel))`(`ch:` ` [ReadableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ReadableByteChannel)!`)` Constructs a stream that reads bytes from the given channel. |
| static [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | [newOutputStream](https://developer.android.com/reference/kotlin/java/nio/channels/Channels#newOutputStream(java.nio.channels.AsynchronousByteChannel))`(`ch:` ` [AsynchronousByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousByteChannel)!`)` Constructs a stream that writes bytes to the given channel. |
| static [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | [newOutputStream](https://developer.android.com/reference/kotlin/java/nio/channels/Channels#newOutputStream(java.nio.channels.WritableByteChannel))`(`ch:` ` [WritableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/WritableByteChannel)!`)` Constructs a stream that writes bytes to the given channel. |
| --- | --- |
| static [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)! | [newReader](https://developer.android.com/reference/kotlin/java/nio/channels/Channels#newReader(java.nio.channels.ReadableByteChannel,%20kotlin.String))`(`ch:` ` [ReadableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ReadableByteChannel)!`, `csName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a reader that decodes bytes from the given channel according to the named charset. |
| static [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)! | [newReader](https://developer.android.com/reference/kotlin/java/nio/channels/Channels#newReader(java.nio.channels.ReadableByteChannel,%20java.nio.charset.Charset))`(`ch:` ` [ReadableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ReadableByteChannel)!`, `charset:` ` [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!`)` Constructs a reader that decodes bytes from the given channel according to the given charset. |
| static [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)! | [newReader](https://developer.android.com/reference/kotlin/java/nio/channels/Channels#newReader(java.nio.channels.ReadableByteChannel,%20java.nio.charset.CharsetDecoder,%20kotlin.Int))`(`ch:` ` [ReadableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ReadableByteChannel)!`, `dec:` ` [CharsetDecoder](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetDecoder.html#)!`, `minBufferCap:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a reader that decodes bytes from the given channel using the given decoder. |
| --- | --- |
| static [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#)! | [newWriter](https://developer.android.com/reference/kotlin/java/nio/channels/Channels#newWriter(java.nio.channels.WritableByteChannel,%20kotlin.String))`(`ch:` ` [WritableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/WritableByteChannel)!`, `csName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a writer that encodes characters according to the named charset and writes the resulting bytes to the given channel. |
| static [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#)! | [newWriter](https://developer.android.com/reference/kotlin/java/nio/channels/Channels#newWriter(java.nio.channels.WritableByteChannel,%20java.nio.charset.Charset))`(`ch:` ` [WritableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/WritableByteChannel)!`, `charset:` ` [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!`)` Constructs a writer that encodes characters according to the given charset and writes the resulting bytes to the given channel. |
| static [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#)! | [newWriter](https://developer.android.com/reference/kotlin/java/nio/channels/Channels#newWriter(java.nio.channels.WritableByteChannel,%20java.nio.charset.CharsetEncoder,%20kotlin.Int))`(`ch:` ` [WritableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/WritableByteChannel)!`, `enc:` ` [CharsetEncoder](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder.html#)!`, `minBufferCap:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a writer that encodes characters using the given encoder and writes the resulting bytes to the given channel. |
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
| `in` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:The stream from which bytes are to be read |

| Return ||
|--------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ReadableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ReadableByteChannel)! | A new readable byte channel |

### newChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newChannel(out: OutputStream!): WritableByteChannel!
```

Constructs a channel that writes bytes to the given stream.

The resulting channel will not be buffered; it will simply redirect its I/O operations to the given stream. Closing the channel will in turn cause the stream to be closed.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!:The stream to which bytes are to be written |

| Return ||
|--------------------------------------------------------------------------------------------------------------|-----------------------------|
| [WritableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/WritableByteChannel)! | A new writable byte channel |

### newInputStream

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newInputStream(ch: AsynchronousByteChannel!): InputStream!
```

Constructs a stream that reads bytes from the given channel.

The stream will not be buffered, and it will not support the [mark](https://developer.android.com/reference/kotlin/java/io/InputStream.html#mark(kotlin.Int))or [reset](https://developer.android.com/reference/kotlin/java/io/InputStream.html#reset())methods. The stream will be safe for access by multiple concurrent threads. Closing the stream will in turn cause the channel to be closed.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [AsynchronousByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousByteChannel)!:The channel from which bytes will be read |

| Return ||
|------------------------------------------------------------------------------------------|--------------------|
| [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | A new input stream |

### newInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newInputStream(ch: ReadableByteChannel!): InputStream!
```

Constructs a stream that reads bytes from the given channel.

The`read`methods of the resulting stream will throw an [IllegalBlockingModeException](https://developer.android.com/reference/kotlin/java/nio/channels/IllegalBlockingModeException) if invoked while the underlying channel is in non-blocking mode. The stream will not be buffered, and it will not support the [mark](https://developer.android.com/reference/kotlin/java/io/InputStream.html#mark(kotlin.Int))or [reset](https://developer.android.com/reference/kotlin/java/io/InputStream.html#reset())methods. The stream will be safe for access by multiple concurrent threads. Closing the stream will in turn cause the channel to be closed.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [ReadableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ReadableByteChannel)!:The channel from which bytes will be read |

| Return ||
|------------------------------------------------------------------------------------------|--------------------|
| [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | A new input stream |

### newOutputStream

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newOutputStream(ch: AsynchronousByteChannel!): OutputStream!
```

Constructs a stream that writes bytes to the given channel.

The stream will not be buffered. The stream will be safe for access by multiple concurrent threads. Closing the stream will in turn cause the channel to be closed.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [AsynchronousByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousByteChannel)!:The channel to which bytes will be written |

| Return ||
|--------------------------------------------------------------------------------------------|---------------------|
| [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | A new output stream |

### newOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newOutputStream(ch: WritableByteChannel!): OutputStream!
```

Constructs a stream that writes bytes to the given channel.

The`write`methods of the resulting stream will throw an [IllegalBlockingModeException](https://developer.android.com/reference/kotlin/java/nio/channels/IllegalBlockingModeException) if invoked while the underlying channel is in non-blocking mode. The stream will not be buffered. The stream will be safe for access by multiple concurrent threads. Closing the stream will in turn cause the channel to be closed.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [WritableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/WritableByteChannel)!:The channel to which bytes will be written |

| Return ||
|--------------------------------------------------------------------------------------------|---------------------|
| [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | A new output stream |

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
| `ch` | [ReadableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ReadableByteChannel)!:The channel from which bytes will be read |
| `csName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the charset to be used |

| Return ||
|--------------------------------------------------------------------------------|--------------|
| [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)! | A new reader |

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

The reader's default action for malformed-input and unmappable-character errors is to [report](https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction.html#REPORT:java.nio.charset.CodingErrorAction) them. When more control over the error handling is required, the constructor that takes a [java.nio.charset.CharsetDecoder](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetDecoder.html#) should be used.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [ReadableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ReadableByteChannel)!:The channel from which bytes will be read |
| `charset` | [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!:The charset to be used |

| Return ||
|--------------------------------------------------------------------------------|--------------|
| [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)! | A new reader |

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

The resulting stream will contain an internal input buffer of at least`minBufferCap`bytes. The stream's`read`methods will, as needed, fill the buffer by reading bytes from the underlying channel; if the channel is in non-blocking mode when bytes are to be read then an [IllegalBlockingModeException](https://developer.android.com/reference/kotlin/java/nio/channels/IllegalBlockingModeException) will be thrown. The resulting stream will not otherwise be buffered, and it will not support the [mark](https://developer.android.com/reference/kotlin/java/io/Reader.html#mark(kotlin.Int))or [reset](https://developer.android.com/reference/kotlin/java/io/Reader.html#reset())methods. Closing the stream will in turn cause the channel to be closed.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [ReadableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ReadableByteChannel)!:The channel from which bytes will be read |
| `dec` | [CharsetDecoder](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetDecoder.html#)!:The charset decoder to be used |
| `minBufferCap` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The minimum capacity of the internal byte buffer, or`-1`if an implementation-dependent default capacity is to be used |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------|--------------|
| [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)! | A new reader |

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
| `ch` | [WritableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/WritableByteChannel)!:The channel to which bytes will be written |
| `csName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the charset to be used |

| Return ||
|--------------------------------------------------------------------------------|--------------|
| [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#)! | A new writer |

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

The writer's default action for malformed-input and unmappable-character errors is to [report](https://developer.android.com/reference/kotlin/java/nio/charset/CodingErrorAction.html#REPORT:java.nio.charset.CodingErrorAction) them. When more control over the error handling is required, the constructor that takes a [java.nio.charset.CharsetEncoder](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder.html#) should be used.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [WritableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/WritableByteChannel)!:The channel to which bytes will be written |
| `charset` | [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)!:The charset to be used |

| Return ||
|--------------------------------------------------------------------------------|--------------|
| [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#)! | A new writer |

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

The resulting stream will contain an internal output buffer of at least`minBufferCap`bytes. The stream's`write`methods will, as needed, flush the buffer by writing bytes to the underlying channel; if the channel is in non-blocking mode when bytes are to be written then an [IllegalBlockingModeException](https://developer.android.com/reference/kotlin/java/nio/channels/IllegalBlockingModeException) will be thrown. The resulting stream will not otherwise be buffered. Closing the stream will in turn cause the channel to be closed.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [WritableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/WritableByteChannel)!:The channel to which bytes will be written |
| `enc` | [CharsetEncoder](https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder.html#)!:The charset encoder to be used |
| `minBufferCap` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The minimum capacity of the internal byte buffer, or`-1`if an implementation-dependent default capacity is to be used |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------|--------------|
| [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#)! | A new writer |
