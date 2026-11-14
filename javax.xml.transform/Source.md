# Source

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Source

```
interface Source
```

| [javax.xml.transform.Source](Source.md) |

| Known Direct Subclasses [DOMSource](../javax.xml.transform.dom/DOMSource.md), [SAXSource](../javax.xml.transform.sax/SAXSource.md), [StreamSource](../javax.xml.transform.stream/StreamSource.md) |--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------| | [DOMSource](../javax.xml.transform.dom/DOMSource.md) | Acts as a holder for a transformation Source tree in the form of a Document Object Model (DOM) tree. | | [SAXSource](../javax.xml.transform.sax/SAXSource.md) | Acts as an holder for SAX-style Source. | | [StreamSource](../javax.xml.transform.stream/StreamSource.md) | Acts as an holder for a transformation Source in the form of a stream of XML markup. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An object that implements this interface contains the information needed to act as source input (XML source or transformation instructions).

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSystemId](Source.md))`()` Get the system identifier that was set with setSystemId. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSystemId](Source.md))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the system identifier for this Source. |

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

Set the system identifier for this Source.

The system identifier is optional if the source does not get its data from a URL, but it may still be useful to provide one. The application can use a system identifier, for example, to resolve relative URIs and to include in error messages and warnings.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------|
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The system identifier as a URL string. |
