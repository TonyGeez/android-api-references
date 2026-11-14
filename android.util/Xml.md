# Xml

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Xml

Kotlin| [Java](Xml.md) 
| --- | --- |

```
open class Xml
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.Xml](Xml.md) |

XML utility methods.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------|
| | [Encoding](../android/util/Xml.Encoding.md) Supported character encodings. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [AttributeSet](AttributeSet.md)! | [asAttributeSet](Xml.md))`(`parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)!`)` Return an AttributeSet interface for use with the given XmlPullParser. |
| openstatic [Xml.Encoding](../android/util/Xml.Encoding.md)! | [findEncodingByName](Xml.md))`(`encodingName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Finds an encoding by name. |
| openstatic [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)! | [newPullParser](Xml.md))`()` Returns a new pull parser with namespace support. |
| --- | --- |
| openstatic [XmlSerializer](../org.xmlpull.v1/XmlSerializer.md)! | [newSerializer](Xml.md))`()` Creates a new xml serializer. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](Xml.md))`(`in:` ` [InputStream](../java.io/InputStream.md)!`, `encoding:` ` [Xml.Encoding](../android/util/Xml.Encoding.md)!`, `contentHandler:` ` [ContentHandler](../org.xml.sax/ContentHandler.md)!`)` Parses xml from the given input stream and fires events on the given SAX handler. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](Xml.md))`(`in:` ` [Reader](../java.io/Reader.md)!`, `contentHandler:` ` [ContentHandler](../org.xml.sax/ContentHandler.md)!`)` Parses xml from the given reader and fires events on the given SAX handler. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parse](Xml.md))`(`xml:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `contentHandler:` ` [ContentHandler](../org.xml.sax/ContentHandler.md)!`)` Parses the given xml string and fires events on the given SAX handler. |

| Properties ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [FEATURE_RELAXED](Xml.md) [org.xmlpull.v1.XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)"relaxed" feature name. |

## Public methods

### asAttributeSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun asAttributeSet(parser: XmlPullParser!): AttributeSet!
```

Return an AttributeSet interface for use with the given XmlPullParser. If the given parser itself implements AttributeSet, that implementation is simply returned. Otherwise a wrapper class is instantiated on top of the XmlPullParser, as a proxy for retrieving its attributes, and returned to you.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parser` | [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)!:The existing parser for which you would like an AttributeSet. |

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [AttributeSet](AttributeSet.md)! | An AttributeSet you can use to retrieve the attribute values at each of the tags as the parser moves through its XML document. |

**See Also**

- [android.util.AttributeSet](AttributeSet.md) 

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

[org.xmlpull.v1.XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)"relaxed" feature name. 
**See Also**
