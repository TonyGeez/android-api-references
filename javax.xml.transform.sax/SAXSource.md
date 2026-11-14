Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SAXSource

```
open class SAXSource : Source
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.transform.sax.SAXSource](https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXSource#) |

Acts as an holder for SAX-style Source.

Note that XSLT requires namespace support. Attempting to transform an input source that is not generated with a namespace-aware parser may result in errors. Parsers can be made namespace aware by calling the `https://developer.android.com/reference/kotlin/javax/xml/parsers/SAXParserFactory.html#setNamespaceAware(kotlin.Boolean)` method.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXSource#FEATURE:kotlin.String` If `https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#getFeature(kotlin.String)` returns true when passed this value as an argument, the Transformer supports Source input of this type. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXSource#SAXSource()()` Zero-argument default constructor. |
| `https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXSource#SAXSource(org.xml.sax.InputSource)(inputSource: https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#!)` Create a `SAXSource`, using a SAX `InputSource`. |
| `https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXSource#SAXSource(org.xml.sax.XMLReader,%20org.xml.sax.InputSource)(reader: https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#!, inputSource: https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#!)` Create a `SAXSource`, using an `https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#` and a SAX InputSource. |

| Public methods ||
|---|---|
| open [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)! | `https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXSource#getInputSource()()` Get the SAX InputSource to be used for the Source. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXSource#getSystemId()()` Get the base ID (URI or system ID) from where URIs will be resolved. |
| open [XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#)! | `https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXSource#getXMLReader()()` Get the XMLReader to be used for the Source. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXSource#setInputSource(org.xml.sax.InputSource)(inputSource: https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#!)` Set the SAX InputSource to be used for the Source. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXSource#setSystemId(kotlin.String)(systemId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Set the system identifier for this Source. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXSource#setXMLReader(org.xml.sax.XMLReader)(reader: https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#!)` Set the XMLReader to be used for the Source. |
| --- | --- |
| open static [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)! | `https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXSource#sourceToInputSource(javax.xml.transform.Source)(source: https://developer.android.com/reference/kotlin/javax/xml/transform/Source.html#!)` Attempt to obtain a SAX InputSource object from a Source object. |

## Constants

### FEATURE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE: String
```

If `https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#getFeature(kotlin.String)` returns true when passed this value as an argument, the Transformer supports Source input of this type.

 Value: "http://javax.xml.transform.sax.SAXSource/feature"

## Public constructors

### SAXSource

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SAXSource()
```

Zero-argument default constructor. If this constructor is used, and no SAX source is set using `https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXSource#setInputSource(org.xml.sax.InputSource)` , then the `Transformer` will create an empty source `https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#` using `https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#InputSource()`.
**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer.html#transform(javax.xml.transform.Source,%20javax.xml.transform.Result)`

### SAXSource

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SAXSource(inputSource: InputSource!)
```

Create a `SAXSource`, using a SAX `InputSource`. The `https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer.html#` or `https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXTransformerFactory` creates a reader via `https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderFactory.html#` (if setXMLReader is not used), sets itself as the reader's `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#`, and calls reader.parse(inputSource).

| Parameters ||
|---|---|
| `inputSource` | [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)!: An input source reference that must be non-null and that will be passed to the parse method of the reader. |

### SAXSource

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SAXSource(
    reader: XMLReader!, 
    inputSource: InputSource!)
```

Create a `SAXSource`, using an `https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#` and a SAX InputSource. The `https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer.html#` or `https://developer.android.com/reference/kotlin/javax/xml/transform/sax/SAXTransformerFactory` will set itself to be the reader's `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#`, and then will call reader.parse(inputSource).

| Parameters ||
|---|---|
| `reader` | [XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#)!: An XMLReader to be used for the parse. |
| `inputSource` | [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)!: A SAX input source reference that must be non-null and that will be passed to the reader parse method. |

## Public methods

### getInputSource

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInputSource(): InputSource!
```

Get the SAX InputSource to be used for the Source.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#!` | A valid InputSource reference, or null. |

### getSystemId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSystemId(): String!
```

Get the base ID (URI or system ID) from where URIs will be resolved.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | Base URL for the `Source`, or `null`. |

### getXMLReader

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getXMLReader(): XMLReader!
```

Get the XMLReader to be used for the Source.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#!` | A valid XMLReader or XMLFilter reference, or null. |

### setInputSource

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setInputSource(inputSource: InputSource!): Unit
```

Set the SAX InputSource to be used for the Source.

| Parameters ||
|---|---|
| `inputSource` | [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#)!: A valid InputSource reference. |

### setSystemId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSystemId(systemId: String!): Unit
```

Set the system identifier for this Source. If an input source has already been set, it will set the system ID or that input source, otherwise it will create a new input source.

The system identifier is optional if there is a byte stream or a character stream, but it is still useful to provide one, since the application can use it to resolve relative URIs and can include it in error messages and warnings (the parser will attempt to open a connection to the URI only if no byte stream or character stream is specified).

| Parameters ||
|---|---|
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The system identifier as a URI string. |

### setXMLReader

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setXMLReader(reader: XMLReader!): Unit
```

Set the XMLReader to be used for the Source.

| Parameters ||
|---|---|
| `reader` | [XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#)!: A valid XMLReader or XMLFilter reference. |

### sourceToInputSource

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun sourceToInputSource(source: Source!): InputSource!
```

Attempt to obtain a SAX InputSource object from a Source object.

| Parameters ||
|---|---|
| `source` | [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source.html#)!: Must be a non-null Source reference. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#!` | An InputSource, or null if Source can not be converted. |
