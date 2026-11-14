# Xml

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Xml

Kotlin| [Java](https://developer.android.com/reference/android/util/Xml "View this page in Java") 
| --- | --- |

```
open class Xml
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.Xml](https://developer.android.com/reference/kotlin/android/util/Xml#) |

XML utility methods.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------|
| | [Encoding](https://developer.android.com/reference/kotlin/android/util/Xml.Encoding) Supported character encodings. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet)! | [asAttributeSet](https://developer.android.com/reference/kotlin/android/util/Xml#asAttributeSet(org.xmlpull.v1.XmlPullParser))`(`parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)!`)` Return an AttributeSet interface for use with the given XmlPullParser. |
| openstatic [Xml.Encoding](https://developer.android.com/reference/kotlin/android/util/Xml.Encoding)! | [findEncodingByName](https://developer.android.com/reference/kotlin/android/util/Xml#findEncodingByName(kotlin.String))`(`encodingName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Finds an encoding by name. |
| openstatic [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)! | [newPullParser](https://developer.android.com/reference/kotlin/android/util/Xml#newPullParser())`()` Returns a new pull parser with namespace support. |
| --- | --- |
| openstatic [XmlSerializer](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlSerializer.html#)! | [newSerializer](https://developer.android.com/reference/kotlin/android/util/Xml#newSerializer())`()` Creates a new xml serializer. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/android/util/Xml#parse(java.io.InputStream,%20android.util.Xml.Encoding,%20org.xml.sax.ContentHandler))`(`in:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `encoding:` ` [Xml.Encoding](https://developer.android.com/reference/kotlin/android/util/Xml.Encoding)!`, `contentHandler:` ` [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#)!`)` Parses xml from the given input stream and fires events on the given SAX handler. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/android/util/Xml#parse(java.io.Reader,%20org.xml.sax.ContentHandler))`(`in:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`, `contentHandler:` ` [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#)!`)` Parses xml from the given reader and fires events on the given SAX handler. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](https://developer.android.com/reference/kotlin/android/util/Xml#parse(kotlin.String,%20org.xml.sax.ContentHandler))`(`xml:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `contentHandler:` ` [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#)!`)` Parses the given xml string and fires events on the given SAX handler. |

| Properties ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [FEATURE_RELAXED](https://developer.android.com/reference/kotlin/android/util/Xml#FEATURE_RELAXED:kotlin.String) [org.xmlpull.v1.XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)"relaxed" feature name. |

## Public methods

### asAttributeSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun asAttributeSet(parser: XmlPullParser!): AttributeSet!
```

Return an AttributeSet interface for use with the given XmlPullParser. If the given parser itself implements AttributeSet, that implementation is simply returned. Otherwise a wrapper class is instantiated on top of the XmlPullParser, as a proxy for retrieving its attributes, and returned to you.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parser` | [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)!:The existing parser for which you would like an AttributeSet. |

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet)! | An AttributeSet you can use to retrieve the attribute values at each of the tags as the parser moves through its XML document. |

**See Also**

- [android.util.AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet) 

### findEncodingByName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun findEncodingByName(encodingName: String!): Xml.Encoding!
```

Finds an encoding by name. Returns UTF-8 if you pass`null`. 

### newPullParser

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newPullParser(): XmlPullParser!
```

Returns a new pull parser with namespace support. 

### newSerializer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newSerializer(): XmlSerializer!
```

Creates a new xml serializer. 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun parse(
    in: InputStream!, 
    encoding: Xml.Encoding!, 
    contentHandler: ContentHandler!
): Unit
```

Parses xml from the given input stream and fires events on the given SAX handler. 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun parse(
    in: Reader!, 
    contentHandler: ContentHandler!
): Unit
```

Parses xml from the given reader and fires events on the given SAX handler. 

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun parse(
    xml: String!, 
    contentHandler: ContentHandler!
): Unit
```

Parses the given xml string and fires events on the given SAX handler.

## Properties

### FEATURE_RELAXED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static var FEATURE_RELAXED: String!
```

[org.xmlpull.v1.XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)"relaxed" feature name. 
**See Also**
