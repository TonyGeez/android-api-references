# StreamResult

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StreamResult

```
open class StreamResult : Result
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [javax.xml.transform.stream.StreamResult](https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamResult#) |

Acts as an holder for a transformation result, which may be XML, plain Text, HTML, or some other form of markup.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE](https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamResult#FEATURE:kotlin.String) If [javax.xml.transform.TransformerFactory#getFeature](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#getFeature(kotlin.String))returns true when passed this value as an argument, the Transformer supports Result output of this type. |

| Inherited constants ||
|---|---|
| From class [Result](https://developer.android.com/reference/kotlin/javax/xml/transform/Result.html#) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PI_DISABLE_OUTPUT_ESCAPING](https://developer.android.com/reference/kotlin/javax/xml/transform/Result.html#PI_DISABLE_OUTPUT_ESCAPING:kotlin.String) <br /> The name of the processing instruction that is sent if the result tree disables output escaping. Normally, result tree serialization escapes \& and \< (and possibly other characters) when outputting text nodes. This ensures that the output is well-formed XML. However, it is sometimes convenient to be able to produce output that is almost, but not quite well-formed XML; for example, the output may include ill-formed sections that will be transformed into well-formed XML by a subsequent non-XML aware process. If a processing instruction is sent with this name, serialization should be output without any escaping. Result DOM trees may also have PI_DISABLE_OUTPUT_ESCAPING and PI_ENABLE_OUTPUT_ESCAPING inserted into the tree. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PI_ENABLE_OUTPUT_ESCAPING](https://developer.android.com/reference/kotlin/javax/xml/transform/Result.html#PI_ENABLE_OUTPUT_ESCAPING:kotlin.String) <br /> The name of the processing instruction that is sent if the result tree enables output escaping at some point after having received a PI_DISABLE_OUTPUT_ESCAPING processing instruction. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StreamResult](https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamResult#StreamResult())`()` Zero-argument default constructor. |
| [StreamResult](https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamResult#StreamResult(java.io.File))`(`f:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`)` Construct a StreamResult from a File. |
| [StreamResult](https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamResult#StreamResult(java.io.OutputStream))`(`outputStream:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`)` Construct a StreamResult from a byte stream. |
| [StreamResult](https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamResult#StreamResult(java.io.Writer))`(`writer:` ` [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#)!`)` Construct a StreamResult from a character stream. |
| [StreamResult](https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamResult#StreamResult(kotlin.String))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Construct a StreamResult from a URL. |

| Public methods ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | [getOutputStream](https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamResult#getOutputStream())`()` Get the byte stream that was set with setOutputStream. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSystemId](https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamResult#getSystemId())`()` Get the system identifier that was set with setSystemId. |
| open [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#)! | [getWriter](https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamResult#getWriter())`()` Get the character stream that was set with setWriter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOutputStream](https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamResult#setOutputStream(java.io.OutputStream))`(`outputStream:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`)` Set the ByteStream that is to be written to. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSystemId](https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamResult#setSystemId(java.io.File))`(`f:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`)` Set the system ID from a`File`reference. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSystemId](https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamResult#setSystemId(kotlin.String))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the systemID that may be used in association with the byte or character stream, or, if neither is set, use this value as a writeable URI (probably a file name). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWriter](https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamResult#setWriter(java.io.Writer))`(`writer:` ` [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#)!`)` Set the writer that is to receive the result. |

## Constants

### FEATURE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE: String
```

If [javax.xml.transform.TransformerFactory#getFeature](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#getFeature(kotlin.String))returns true when passed this value as an argument, the Transformer supports Result output of this type. 

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
| `f` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!:Must a non-null File reference. |

### StreamResult

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StreamResult(outputStream: OutputStream!)
```

Construct a StreamResult from a byte stream. Normally, a stream should be used rather than a reader, so that the transformer may use instructions contained in the transformation instructions to control the encoding.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| `outputStream` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!:A valid OutputStream reference. |

### StreamResult

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StreamResult(writer: Writer!)
```

Construct a StreamResult from a character stream. Normally, a stream should be used rather than a reader, so that the transformer may use instructions contained in the transformation instructions to control the encoding. However, there are times when it is useful to write to a character stream, such as when using a StringWriter.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------|
| `writer` | [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#)!:A valid Writer reference. |

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
| [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | The byte stream that was set with setOutputStream, or null if setOutputStream or the ByteStream constructor was not called. |

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
| [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#)! | The character stream that was set with setWriter, or null if setWriter or the Writer constructor was not called. |

### setOutputStream

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOutputStream(outputStream: OutputStream!): Unit
```

Set the ByteStream that is to be written to. Normally, a stream should be used rather than a reader, so that the transformer may use instructions contained in the transformation instructions to control the encoding.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| `outputStream` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!:A valid OutputStream reference. |

### setSystemId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSystemId(f: File!): Unit
```

Set the system ID from a`File`reference.

Note the use of [File.toURI()](https://developer.android.com/reference/kotlin/java/io/File.html#toURI())and [File.toURL()](https://developer.android.com/reference/kotlin/java/io/File.html#toURL()).`toURI()`is preferred and used if possible. To allow JAXP 1.3 to run on J2SE 1.3,`toURL()`is used if a [NoSuchMethodException](https://developer.android.com/reference/kotlin/java/lang/NoSuchMethodException.html#) is thrown by the attempt to use`toURI()`.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------|
| `f` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!:Must a non-null File reference. |

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
| `writer` | [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#)!:A valid Writer reference. |
