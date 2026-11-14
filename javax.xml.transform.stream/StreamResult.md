# StreamResult

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StreamResult

```
open class StreamResult : Result
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.transform.stream.StreamResult](../javax/xml/transform/stream/StreamResult.md) |

Acts as an holder for a transformation result, which may be XML, plain Text, HTML, or some other form of markup.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE](../javax/xml/transform/stream/StreamResult.md) If [javax.xml.transform.TransformerFactory#getFeature](../javax/xml/transform/TransformerFactory.md))returns true when passed this value as an argument, the Transformer supports Result output of this type. |

| Inherited constants ||
|---|---|
| From class [Result](../javax/xml/transform/Result.md) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PI_DISABLE_OUTPUT_ESCAPING](../javax/xml/transform/Result.md) <br /> The name of the processing instruction that is sent if the result tree disables output escaping. Normally, result tree serialization escapes \& and \< (and possibly other characters) when outputting text nodes. This ensures that the output is well-formed XML. However, it is sometimes convenient to be able to produce output that is almost, but not quite well-formed XML; for example, the output may include ill-formed sections that will be transformed into well-formed XML by a subsequent non-XML aware process. If a processing instruction is sent with this name, serialization should be output without any escaping. Result DOM trees may also have PI_DISABLE_OUTPUT_ESCAPING and PI_ENABLE_OUTPUT_ESCAPING inserted into the tree. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PI_ENABLE_OUTPUT_ESCAPING](../javax/xml/transform/Result.md) <br /> The name of the processing instruction that is sent if the result tree enables output escaping at some point after having received a PI_DISABLE_OUTPUT_ESCAPING processing instruction. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StreamResult](../javax/xml/transform/stream/StreamResult.md))`()` Zero-argument default constructor. |
| [StreamResult](../javax/xml/transform/stream/StreamResult.md))`(`f:` ` [File](../java/io/File.md)!`)` Construct a StreamResult from a File. |
| [StreamResult](../javax/xml/transform/stream/StreamResult.md))`(`outputStream:` ` [OutputStream](../java/io/OutputStream.md)!`)` Construct a StreamResult from a byte stream. |
| [StreamResult](../javax/xml/transform/stream/StreamResult.md))`(`writer:` ` [Writer](../java/io/Writer.md)!`)` Construct a StreamResult from a character stream. |
| [StreamResult](../javax/xml/transform/stream/StreamResult.md))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Construct a StreamResult from a URL. |

| Public methods ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [OutputStream](../java/io/OutputStream.md)! | [getOutputStream](../javax/xml/transform/stream/StreamResult.md))`()` Get the byte stream that was set with setOutputStream. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSystemId](../javax/xml/transform/stream/StreamResult.md))`()` Get the system identifier that was set with setSystemId. |
| open [Writer](../java/io/Writer.md)! | [getWriter](../javax/xml/transform/stream/StreamResult.md))`()` Get the character stream that was set with setWriter. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOutputStream](../javax/xml/transform/stream/StreamResult.md))`(`outputStream:` ` [OutputStream](../java/io/OutputStream.md)!`)` Set the ByteStream that is to be written to. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSystemId](../javax/xml/transform/stream/StreamResult.md))`(`f:` ` [File](../java/io/File.md)!`)` Set the system ID from a`File`reference. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSystemId](../javax/xml/transform/stream/StreamResult.md))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the systemID that may be used in association with the byte or character stream, or, if neither is set, use this value as a writeable URI (probably a file name). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWriter](../javax/xml/transform/stream/StreamResult.md))`(`writer:` ` [Writer](../java/io/Writer.md)!`)` Set the writer that is to receive the result. |

## Constants

### FEATURE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE: String
```

If [javax.xml.transform.TransformerFactory#getFeature](../javax/xml/transform/TransformerFactory.md))returns true when passed this value as an argument, the Transformer supports Result output of this type. 

 Value: "http://javax.xml.transform.stream.StreamResult/feature"

## Public constructors

### StreamResult

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StreamResult()
```

Zero-argument default constructor. 

### StreamResult

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StreamResult(f: File!)
```

Construct a StreamResult from a File.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------|
| `f` | [File](../java/io/File.md)!:Must a non-null File reference. |

### StreamResult

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StreamResult(outputStream: OutputStream!)
```

Construct a StreamResult from a byte stream. Normally, a stream should be used rather than a reader, so that the transformer may use instructions contained in the transformation instructions to control the encoding.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| `outputStream` | [OutputStream](../java/io/OutputStream.md)!:A valid OutputStream reference. |

### StreamResult

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StreamResult(writer: Writer!)
```

Construct a StreamResult from a character stream. Normally, a stream should be used rather than a reader, so that the transformer may use instructions contained in the transformation instructions to control the encoding. However, there are times when it is useful to write to a character stream, such as when using a StringWriter.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------|
| `writer` | [Writer](../java/io/Writer.md)!:A valid Writer reference. |

### StreamResult

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StreamResult(systemId: String!)
```

Construct a StreamResult from a URL.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Must be a String that conforms to the URI syntax. |

## Public methods

### getOutputStream

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOutputStream(): OutputStream!
```

Get the byte stream that was set with setOutputStream.

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [OutputStream](../java/io/OutputStream.md)! | The byte stream that was set with setOutputStream, or null if setOutputStream or the ByteStream constructor was not called. |

### getSystemId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSystemId(): String!
```

Get the system identifier that was set with setSystemId.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The system identifier that was set with setSystemId, or null if setSystemId was not called. |

### getWriter

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWriter(): Writer!
```

Get the character stream that was set with setWriter.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Writer](../java/io/Writer.md)! | The character stream that was set with setWriter, or null if setWriter or the Writer constructor was not called. |

### setOutputStream

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOutputStream(outputStream: OutputStream!): Unit
```

Set the ByteStream that is to be written to. Normally, a stream should be used rather than a reader, so that the transformer may use instructions contained in the transformation instructions to control the encoding.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| `outputStream` | [OutputStream](../java/io/OutputStream.md)!:A valid OutputStream reference. |

### setSystemId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSystemId(f: File!): Unit
```

Set the system ID from a`File`reference.

Note the use of [File.toURI()](../java/io/File.md))and [File.toURL()](../java/io/File.md)).`toURI()`is preferred and used if possible. To allow JAXP 1.3 to run on J2SE 1.3,`toURL()`is used if a [NoSuchMethodException](../java/lang/NoSuchMethodException.md) is thrown by the attempt to use`toURI()`.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------|
| `f` | [File](../java/io/File.md)!:Must a non-null File reference. |

### setSystemId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSystemId(systemId: String!): Unit
```

Set the systemID that may be used in association with the byte or character stream, or, if neither is set, use this value as a writeable URI (probably a file name).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------|
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The system identifier as a URI string. |

### setWriter

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setWriter(writer: Writer!): Unit
```

Set the writer that is to receive the result. Normally, a stream should be used rather than a writer, so that the transformer may use instructions contained in the transformation instructions to control the encoding. However, there are times when it is useful to write to a writer, such as when using a StringWriter.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------|
| `writer` | [Writer](../java/io/Writer.md)!:A valid Writer reference. |
