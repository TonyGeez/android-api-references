# Result

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Result

```
interface Result
```

| [javax.xml.transform.Result](https://developer.android.com/reference/kotlin/javax/xml/transform/Result#) |

| Known Direct Subclasses [DOMResult](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult), [SAXResult](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXResult), [StreamResult](https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamResult) |--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------| | [DOMResult](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult) | Acts as a holder for a transformation result tree in the form of a Document Object Model (DOM) tree. | | [SAXResult](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXResult) | Acts as an holder for a transformation Result. | | [StreamResult](https://developer.android.com/reference/kotlin/javax/xml/transform/stream/StreamResult) | Acts as an holder for a transformation result, which may be XML, plain Text, HTML, or some other form of markup. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An object that implements this interface contains the information needed to build a transformation result tree.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PI_DISABLE_OUTPUT_ESCAPING](https://developer.android.com/reference/kotlin/javax/xml/transform/Result#PI_DISABLE_OUTPUT_ESCAPING:kotlin.String) The name of the processing instruction that is sent if the result tree disables output escaping. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PI_ENABLE_OUTPUT_ESCAPING](https://developer.android.com/reference/kotlin/javax/xml/transform/Result#PI_ENABLE_OUTPUT_ESCAPING:kotlin.String) The name of the processing instruction that is sent if the result tree enables output escaping at some point after having received a PI_DISABLE_OUTPUT_ESCAPING processing instruction. |

| Public methods ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSystemId](https://developer.android.com/reference/kotlin/javax/xml/transform/Result#getSystemId())`()` Get the system identifier that was set with setSystemId. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSystemId](https://developer.android.com/reference/kotlin/javax/xml/transform/Result#setSystemId(kotlin.String))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the system identifier for this Result. |

## Constants

### PI_DISABLE_OUTPUT_ESCAPING

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PI_DISABLE_OUTPUT_ESCAPING: String
```

The name of the processing instruction that is sent if the result tree disables output escaping.

Normally, result tree serialization escapes \& and \< (and possibly other characters) when outputting text nodes. This ensures that the output is well-formed XML. However, it is sometimes convenient to be able to produce output that is almost, but not quite well-formed XML; for example, the output may include ill-formed sections that will be transformed into well-formed XML by a subsequent non-XML aware process. If a processing instruction is sent with this name, serialization should be output without any escaping.

Result DOM trees may also have PI_DISABLE_OUTPUT_ESCAPING and PI_ENABLE_OUTPUT_ESCAPING inserted into the tree. 

 Value: "javax.xml.transform.disable-output-escaping"

**See Also**

### PI_ENABLE_OUTPUT_ESCAPING

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PI_ENABLE_OUTPUT_ESCAPING: String
```

The name of the processing instruction that is sent if the result tree enables output escaping at some point after having received a PI_DISABLE_OUTPUT_ESCAPING processing instruction. 

 Value: "javax.xml.transform.enable-output-escaping"

**See Also**

## Public methods

### getSystemId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSystemId(): String!
```

Get the system identifier that was set with setSystemId.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The system identifier that was set with setSystemId, or null if setSystemId was not called. |

### setSystemId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSystemId(systemId: String!): Unit
```

Set the system identifier for this Result.

If the Result is not to be written to a file, the system identifier is optional. The application may still want to provide one, however, for use in error messages and warnings, or to resolve relative output identifiers.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------|
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The system identifier as a URI string. |
