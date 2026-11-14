# SAXResult

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SAXResult

```
open class SAXResult : Result
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.transform.sax.SAXResult](../javax/xml/transform/sax/SAXResult.md) |

Acts as an holder for a transformation Result.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE](../javax/xml/transform/sax/SAXResult.md) If [javax.xml.transform.TransformerFactory#getFeature](../javax/xml/transform/TransformerFactory.md))returns true when passed this value as an argument, the Transformer supports Result output of this type. |

| Inherited constants ||
|---|---|
| From class [Result](../javax/xml/transform/Result.md) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PI_DISABLE_OUTPUT_ESCAPING](../javax/xml/transform/Result.md) <br /> The name of the processing instruction that is sent if the result tree disables output escaping. Normally, result tree serialization escapes \& and \< (and possibly other characters) when outputting text nodes. This ensures that the output is well-formed XML. However, it is sometimes convenient to be able to produce output that is almost, but not quite well-formed XML; for example, the output may include ill-formed sections that will be transformed into well-formed XML by a subsequent non-XML aware process. If a processing instruction is sent with this name, serialization should be output without any escaping. Result DOM trees may also have PI_DISABLE_OUTPUT_ESCAPING and PI_ENABLE_OUTPUT_ESCAPING inserted into the tree. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PI_ENABLE_OUTPUT_ESCAPING](../javax/xml/transform/Result.md) <br /> The name of the processing instruction that is sent if the result tree enables output escaping at some point after having received a PI_DISABLE_OUTPUT_ESCAPING processing instruction. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SAXResult](../javax/xml/transform/sax/SAXResult.md))`()` Zero-argument default constructor. |
| [SAXResult](../javax/xml/transform/sax/SAXResult.md))`(`handler:` ` [ContentHandler](../org/xml/sax/ContentHandler.md)!`)` Create a SAXResult that targets a SAX2 [org.xml.sax.ContentHandler](../org/xml/sax/ContentHandler.md). |

| Public methods ||
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ContentHandler](../org/xml/sax/ContentHandler.md)! | [getHandler](../javax/xml/transform/sax/SAXResult.md))`()` Get the [org.xml.sax.ContentHandler](../org/xml/sax/ContentHandler.md) that is the Result. |
| open [LexicalHandler](../org/xml/sax/ext/LexicalHandler.md)! | [getLexicalHandler](../javax/xml/transform/sax/SAXResult.md))`()` Get a SAX2 [org.xml.sax.ext.LexicalHandler](../org/xml/sax/ext/LexicalHandler.md) for the output. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSystemId](../javax/xml/transform/sax/SAXResult.md))`()` Get the system identifier that was set with setSystemId. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHandler](../javax/xml/transform/sax/SAXResult.md))`(`handler:` ` [ContentHandler](../org/xml/sax/ContentHandler.md)!`)` Set the target to be a SAX2 [org.xml.sax.ContentHandler](../org/xml/sax/ContentHandler.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLexicalHandler](../javax/xml/transform/sax/SAXResult.md))`(`handler:` ` [LexicalHandler](../org/xml/sax/ext/LexicalHandler.md)!`)` Set the SAX2 [org.xml.sax.ext.LexicalHandler](../org/xml/sax/ext/LexicalHandler.md) for the output. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSystemId](../javax/xml/transform/sax/SAXResult.md))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Method setSystemId Set the systemID that may be used in association with the [org.xml.sax.ContentHandler](../org/xml/sax/ContentHandler.md). |
| --- | --- |

## Constants

### FEATURE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE: String
```

If [javax.xml.transform.TransformerFactory#getFeature](../javax/xml/transform/TransformerFactory.md))returns true when passed this value as an argument, the Transformer supports Result output of this type. 

 Value: "http://javax.xml.transform.sax.SAXResult/feature"

## Public constructors

### SAXResult

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SAXResult()
```

Zero-argument default constructor. 

### SAXResult

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SAXResult(handler: ContentHandler!)
```

Create a SAXResult that targets a SAX2 [org.xml.sax.ContentHandler](../org/xml/sax/ContentHandler.md).

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `handler` | [ContentHandler](../org/xml/sax/ContentHandler.md)!:Must be a non-null ContentHandler reference. |

## Public methods

### getHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHandler(): ContentHandler!
```

Get the [org.xml.sax.ContentHandler](../org/xml/sax/ContentHandler.md) that is the Result.

| Return ||
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [ContentHandler](../org/xml/sax/ContentHandler.md)! | The ContentHandler that is to be transformation output. |

### getLexicalHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLexicalHandler(): LexicalHandler!
```

Get a SAX2 [org.xml.sax.ext.LexicalHandler](../org/xml/sax/ext/LexicalHandler.md) for the output.

| Return ||
|--------------------------------------------------------------------------------------------------------|-----------------------------|
| [LexicalHandler](../org/xml/sax/ext/LexicalHandler.md)! | A`LexicalHandler`, or null. |

### getSystemId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSystemId(): String!
```

Get the system identifier that was set with setSystemId.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The system identifier that was set with setSystemId, or null if setSystemId was not called. |

### setHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setHandler(handler: ContentHandler!): Unit
```

Set the target to be a SAX2 [org.xml.sax.ContentHandler](../org/xml/sax/ContentHandler.md).

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `handler` | [ContentHandler](../org/xml/sax/ContentHandler.md)!:Must be a non-null ContentHandler reference. |

### setLexicalHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLexicalHandler(handler: LexicalHandler!): Unit
```

Set the SAX2 [org.xml.sax.ext.LexicalHandler](../org/xml/sax/ext/LexicalHandler.md) for the output.

This is needed to handle XML comments and the like. If the lexical handler is not set, an attempt should be made by the transformer to cast the [org.xml.sax.ContentHandler](../org/xml/sax/ContentHandler.md) to a`LexicalHandler`.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `handler` | [LexicalHandler](../org/xml/sax/ext/LexicalHandler.md)!:A non-null`LexicalHandler`for handling lexical parse events. |

### setSystemId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSystemId(systemId: String!): Unit
```

Method setSystemId Set the systemID that may be used in association with the [org.xml.sax.ContentHandler](../org/xml/sax/ContentHandler.md).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------|
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The system identifier as a URI string. |
