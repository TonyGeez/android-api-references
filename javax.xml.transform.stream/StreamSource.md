Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StreamSource

```
open class StreamSource : Source
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.transform.stream.StreamSource](StreamSource.md) |

Acts as an holder for a transformation Source in the form of a stream of XML markup.

*Note:* Due to their internal use of either a `https://developer.android.com/reference/kotlin/java/io/Reader.html#` or `https://developer.android.com/reference/kotlin/java/io/InputStream.html#` instance, `StreamSource` instances may only be used once.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamSource#FEATURE:kotlin.String` If `https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#getFeature(kotlin.String)` returns true when passed this value as an argument, the Transformer supports Source input of this type. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamSource#StreamSource()()` Zero-argument default constructor. |
| `https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamSource#StreamSource(java.io.File)(f: https://developer.android.com/reference/kotlin/java/io/File.html#!)` Construct a StreamSource from a File. |
| `https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamSource#StreamSource(java.io.InputStream)(inputStream: https://developer.android.com/reference/kotlin/java/io/InputStream.html#!)` Construct a StreamSource from a byte stream. |
| `https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamSource#StreamSource(java.io.InputStream,%20kotlin.String)(inputStream: https://developer.android.com/reference/kotlin/java/io/InputStream.html#!, systemId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Construct a StreamSource from a byte stream. |
| `https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamSource#StreamSource(java.io.Reader)(reader: https://developer.android.com/reference/kotlin/java/io/Reader.html#!)` Construct a StreamSource from a character reader. |
| `https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamSource#StreamSource(java.io.Reader,%20kotlin.String)(reader: https://developer.android.com/reference/kotlin/java/io/Reader.html#!, systemId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Construct a StreamSource from a character reader. |
| `https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamSource#StreamSource(kotlin.String)(systemId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Construct a StreamSource from a URL. |

| Public methods ||
|---|---|
| open [InputStream](../java.io/InputStream.md)! | `https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamSource#getInputStream()()` Get the byte stream that was set with setByteStream. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamSource#getPublicId()()` Get the public identifier that was set with setPublicId. |
| open [Reader](../java.io/Reader.md)! | `https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamSource#getReader()()` Get the character stream that was set with setReader. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamSource#getSystemId()()` Get the system identifier that was set with setSystemId. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamSource#setInputStream(java.io.InputStream)(inputStream: https://developer.android.com/reference/kotlin/java/io/InputStream.html#!)` Set the byte stream to be used as input. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamSource#setPublicId(kotlin.String)(publicId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Set the public identifier for this Source. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamSource#setReader(java.io.Reader)(reader: https://developer.android.com/reference/kotlin/java/io/Reader.html#!)` Set the input to be a character reader. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamSource#setSystemId(java.io.File)(f: https://developer.android.com/reference/kotlin/java/io/File.html#!)` Set the system ID from a File reference. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamSource#setSystemId(kotlin.String)(systemId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Set the system identifier for this Source. |
| --- | --- |

## Constants

### FEATURE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE: String
```

If `https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#getFeature(kotlin.String)` returns true when passed this value as an argument, the Transformer supports Source input of this type.

 Value: "http://javax.xml.transform.stream.StreamSource/feature"

## Public constructors

### StreamSource

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StreamSource()
```

Zero-argument default constructor. If this constructor is used, and no Stream source is set using `https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamSource#setInputStream(java.io.InputStream)` or `https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamSource#setReader(java.io.Reader)`, then the `Transformer` will create an empty source `https://developer.android.com/reference/kotlin/java/io/InputStream.html#` using `https://developer.android.com/reference/kotlin/java/io/InputStream.html#InputStream()`.
**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer.html#transform(javax.xml.transform.Source,%20javax.xml.transform.Result)`

### StreamSource

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StreamSource(f: File!)
```

Construct a StreamSource from a File.

| Parameters ||
|---|---|
| `f` | [File](../java.io/File.md)!: Must a non-null File reference. |

### StreamSource

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StreamSource(inputStream: InputStream!)
```

Construct a StreamSource from a byte stream. Normally, a stream should be used rather than a reader, so the XML parser can resolve character encoding specified by the XML declaration.

If this constructor is used to process a stylesheet, normally setSystemId should also be called, so that relative URI references can be resolved.

| Parameters ||
|---|---|
| `inputStream` | [InputStream](../java.io/InputStream.md)!: A valid InputStream reference to an XML stream. |

### StreamSource

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StreamSource(
    inputStream: InputStream!, 
    systemId: String!)
```

Construct a StreamSource from a byte stream. Normally, a stream should be used rather than a reader, so that the XML parser can resolve character encoding specified by the XML declaration.

This constructor allows the systemID to be set in addition to the input stream, which allows relative URIs to be processed.

| Parameters ||
|---|---|
| `inputStream` | [InputStream](../java.io/InputStream.md)!: A valid InputStream reference to an XML stream. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Must be a String that conforms to the URI syntax. |

### StreamSource

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StreamSource(reader: Reader!)
```

Construct a StreamSource from a character reader. Normally, a stream should be used rather than a reader, so that the XML parser can resolve character encoding specified by the XML declaration. However, in many cases the encoding of the input stream is already resolved, as in the case of reading XML from a StringReader.

| Parameters ||
|---|---|
| `reader` | [Reader](../java.io/Reader.md)!: A valid Reader reference to an XML character stream. |

### StreamSource

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StreamSource(
    reader: Reader!, 
    systemId: String!)
```

Construct a StreamSource from a character reader. Normally, a stream should be used rather than a reader, so that the XML parser may resolve character encoding specified by the XML declaration. However, in many cases the encoding of the input stream is already resolved, as in the case of reading XML from a StringReader.

| Parameters ||
|---|---|
| `reader` | [Reader](../java.io/Reader.md)!: A valid Reader reference to an XML character stream. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Must be a String that conforms to the URI syntax. |

### StreamSource

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StreamSource(systemId: String!)
```

Construct a StreamSource from a URL.

| Parameters ||
|---|---|
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Must be a String that conforms to the URI syntax. |

## Public methods

### getInputStream

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInputStream(): InputStream!
```

Get the byte stream that was set with setByteStream.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/InputStream.html#!` | The byte stream that was set with setByteStream, or null if setByteStream or the ByteStream constructor was not called. |

### getPublicId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPublicId(): String!
```

Get the public identifier that was set with setPublicId.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The public identifier that was set with setPublicId, or null if setPublicId was not called. |

### getReader

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getReader(): Reader!
```

Get the character stream that was set with setReader.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/Reader.html#!` | The character stream that was set with setReader, or null if setReader or the Reader constructor was not called. |

### getSystemId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSystemId(): String!
```

Get the system identifier that was set with setSystemId.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The system identifier that was set with setSystemId, or null if setSystemId was not called. |

### setInputStream

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setInputStream(inputStream: InputStream!): Unit
```

Set the byte stream to be used as input. Normally, a stream should be used rather than a reader, so that the XML parser can resolve character encoding specified by the XML declaration.

If this Source object is used to process a stylesheet, normally setSystemId should also be called, so that relative URL references can be resolved.

| Parameters ||
|---|---|
| `inputStream` | [InputStream](../java.io/InputStream.md)!: A valid InputStream reference to an XML stream. |

### setPublicId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPublicId(publicId: String!): Unit
```

Set the public identifier for this Source.

The public identifier is always optional: if the application writer includes one, it will be provided as part of the location information.

| Parameters ||
|---|---|
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The public identifier as a string. |

### setReader

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setReader(reader: Reader!): Unit
```

Set the input to be a character reader. Normally, a stream should be used rather than a reader, so that the XML parser can resolve character encoding specified by the XML declaration. However, in many cases the encoding of the input stream is already resolved, as in the case of reading XML from a StringReader.

| Parameters ||
|---|---|
| `reader` | [Reader](../java.io/Reader.md)!: A valid Reader reference to an XML CharacterStream. |

### setSystemId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSystemId(f: File!): Unit
```

Set the system ID from a File reference.

| Parameters ||
|---|---|
| `f` | [File](../java.io/File.md)!: Must a non-null File reference. |

### setSystemId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSystemId(systemId: String!): Unit
```

Set the system identifier for this Source.

The system identifier is optional if there is a byte stream or a character stream, but it is still useful to provide one, since the application can use it to resolve relative URIs and can include it in error messages and warnings (the parser will attempt to open a connection to the URI only if there is no byte stream or character stream specified).

| Parameters ||
|---|---|
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The system identifier as a URL string. |
