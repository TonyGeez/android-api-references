# DOMImplementationLS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DOMImplementationLS

```
interface DOMImplementationLS
```

| [org.w3c.dom.ls.DOMImplementationLS](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/DOMImplementationLS#) |

`DOMImplementationLS` contains the factory methods for creating Load and Save objects.

The expectation is that an instance of the `DOMImplementationLS` interface can be obtained by using binding-specific casting methods on an instance of the `DOMImplementation` interface or, if the `Document` supports the feature `"Core"` version `"3.0"` defined in \ [[DOM Level 3 Core](http://www.w3.org/TR/2004/REC-DOM-Level-3-Core-20040407)\] , by using the method `DOMImplementation.getFeature` with parameter values `"LS"` (or `"LS-Async"`) and `"3.0"` (respectively).

See also the [Document Object Model (DOM) Level 3 Load and Save Specification](http://www.w3.org/TR/2004/REC-DOM-Level-3-LS-20040407).

## Summary

| Constants ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [MODE_ASYNCHRONOUS](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/DOMImplementationLS#MODE_ASYNCHRONOUS:kotlin.Short) Create an asynchronous `LSParser`. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [MODE_SYNCHRONOUS](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/DOMImplementationLS#MODE_SYNCHRONOUS:kotlin.Short) Create a synchronous `LSParser`. |

| Public methods ||
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [LSInput](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSInput)! | [createLSInput](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/DOMImplementationLS#createLSInput())`()` Create a new empty input source object where `LSInput.characterStream`, `LSInput.byteStream` , `LSInput.stringData` `LSInput.systemId`, `LSInput.publicId`, `LSInput.baseURI`, and `LSInput.encoding` are null, and `LSInput.certifiedText` is false. |
| abstract [LSOutput](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSOutput)! | [createLSOutput](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/DOMImplementationLS#createLSOutput())`()` Create a new empty output destination object where `LSOutput.characterStream`, `LSOutput.byteStream`, `LSOutput.systemId`, `LSOutput.encoding` are null. |
| abstract [LSParser](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSParser)! | [createLSParser](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/DOMImplementationLS#createLSParser(kotlin.Short,%20kotlin.String))`(`mode:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`, `schemaType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a new `LSParser`. |
| --- | --- |
| abstract [LSSerializer](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSSerializer)! | [createLSSerializer](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/DOMImplementationLS#createLSSerializer())`()` Create a new `LSSerializer` object. |

## Constants

### MODE_ASYNCHRONOUS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_ASYNCHRONOUS: Short
```

Create an asynchronous `LSParser`. 

 Value: 2

### MODE_SYNCHRONOUS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_SYNCHRONOUS: Short
```

Create a synchronous `LSParser`. 

 Value: 1

## Public methods

### createLSInput

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createLSInput(): LSInput!
```

Create a new empty input source object where `LSInput.characterStream`, `LSInput.byteStream` , `LSInput.stringData` `LSInput.systemId`, `LSInput.publicId`, `LSInput.baseURI`, and `LSInput.encoding` are null, and `LSInput.certifiedText` is false.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------|
| [LSInput](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSInput)! | The newly created input object. |

### createLSOutput

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createLSOutput(): LSOutput!
```

Create a new empty output destination object where `LSOutput.characterStream`, `LSOutput.byteStream`, `LSOutput.systemId`, `LSOutput.encoding` are null.

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------|
| [LSOutput](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSOutput)! | The newly created output object. |

### createLSParser

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createLSParser(
    mode: Short, 
    schemaType: String!
): LSParser!
```

Create a new `LSParser`. The newly constructed parser may then be configured by means of its `DOMConfiguration` object, and used to parse documents by means of its `parse` method.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): The `mode` argument is either `MODE_SYNCHRONOUS` or `MODE_ASYNCHRONOUS`, if `mode` is `MODE_SYNCHRONOUS` then the `LSParser` that is created will operate in synchronous mode, if it's `MODE_ASYNCHRONOUS` then the `LSParser` that is created will operate in asynchronous mode. |
| `schemaType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: An absolute URI representing the type of the schema language used during the load of a `Document` using the newly created `LSParser`. Note that no lexical checking is done on the absolute URI. In order to create a `LSParser` for any kind of schema types (i.e. the LSParser will be free to use any schema found), use the value `null`. **Note:** For W3C XML Schema \ [[XML Schema Part 1](http://www.w3.org/TR/2001/REC-xmlschema-1-20010502/)\] , applications must use the value `"http://www.w3.org/2001/XMLSchema"`. For XML DTD \ [[XML 1.0](http://www.w3.org/TR/2004/REC-xml-20040204)\], applications must use the value `"http://www.w3.org/TR/REC-xml"`. Other Schema languages are outside the scope of the W3C and therefore should recommend an absolute URI in order to use this method. |

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LSParser](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSParser)! | The newly created `LSParser` object. This `LSParser` is either synchronous or asynchronous depending on the value of the `mode` argument. **Note:** By default, the newly created `LSParser` does not contain a `DOMErrorHandler`, i.e. the value of the " [error-handler](http://www.w3.org/TR/DOM-Level-3-Core/core.html#parameter-error-handler)" configuration parameter is `null`. However, implementations may provide a default error handler at creation time. In that case, the initial value of the `"error-handler"` configuration parameter on the new `LSParser` object contains a reference to the default error handler. |

| Exceptions ||
|----------------------------|----------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | NOT_SUPPORTED_ERR: Raised if the requested mode or schema type is not supported. |

### createLSSerializer

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createLSSerializer(): LSSerializer!
```

Create a new `LSSerializer` object.

| Return ||
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LSSerializer](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSSerializer)! | The newly created `LSSerializer` object. **Note:** By default, the newly created `LSSerializer` has no `DOMErrorHandler`, i.e. the value of the `"error-handler"` configuration parameter is `null`. However, implementations may provide a default error handler at creation time. In that case, the initial value of the `"error-handler"` configuration parameter on the new `LSSerializer` object contains a reference to the default error handler. |
