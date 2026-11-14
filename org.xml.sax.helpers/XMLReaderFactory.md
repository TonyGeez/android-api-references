# XMLReaderFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XMLReaderFactory

```
class XMLReaderFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [org.xml.sax.helpers.XMLReaderFactory](../org/xml/sax/helpers/XMLReaderFactory.md) |

Factory for creating an XML reader.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

This class contains static methods for creating an XML reader from an explicit class name, or based on runtime defaults: 

```kotlin
try {
    XMLReader myReader = XMLReaderFactory.createXMLReader();
  } catch (SAXException e) {
    System.err.println(e.getMessage());
  }
  
```

**Note to Distributions bundled with parsers:** You should modify the implementation of the no-arguments*createXMLReader* to handle cases where the external configuration mechanisms aren't set up. That method should do its best to return a parser when one is in the class path, even when nothing bound its class name to`org.xml.sax.driver`so those configuration mechanisms would see it.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [XMLReader](../org/xml/sax/XMLReader.md)! | [createXMLReader](../org/xml/sax/helpers/XMLReaderFactory.md))`()` Attempt to create an XMLReader from system defaults. |
| static [XMLReader](../org/xml/sax/XMLReader.md)! | [createXMLReader](../org/xml/sax/helpers/XMLReaderFactory.md))`(`className:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Attempt to create an XML reader from a class name. |

## Public methods

### createXMLReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createXMLReader(): XMLReader!
```

Attempt to create an XMLReader from system defaults. In environments which can support it, the name of the XMLReader class is determined by trying each these options in order, and using the first one which succeeds:

<br />

- If the system property`org.xml.sax.driver`has a value, that is used as an XMLReader class name.
- The JAR "Services API" is used to look for a class name in the*META-INF/services/org.xml.sax.driver*file in jarfiles available to the runtime.
- SAX parser distributions are strongly encouraged to provide a default XMLReader class name that will take effect only when previous options (on this list) are not successful.
- Finally, if [ParserFactory.makeParser()](../org/xml/sax/helpers/ParserFactory.md))can return a system default SAX1 parser, that parser is wrapped in a [ParserAdapter](../org/xml/sax/helpers/ParserAdapter.md). (This is a migration aid for SAX1 environments, where the`org.xml.sax.parser`system property will often be usable.)

In environments such as small embedded systems, which can not support that flexibility, other mechanisms to determine the default may be used.

Note that many Java environments allow system properties to be initialized on a command line. This means that*in most cases*setting a good value for that property ensures that calls to this method will succeed, except when security policies intervene. This will also maximize application portability to older SAX environments, with less robust implementations of this method.

| Return ||
|------------------------------------------------------------------------------------------|------------------|
| [XMLReader](../org/xml/sax/XMLReader.md)! | A new XMLReader. |

| Exceptions ||
|----------------------------|-------------------------------------------------------------------|
| `org.xml.sax.SAXException` | If no default XMLReader class can be identified and instantiated. |

**See Also**

- [#createXMLReader(java.lang.String)](../org/xml/sax/helpers/XMLReaderFactory.md)) 

### createXMLReader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createXMLReader(className: String!): XMLReader!
```

Attempt to create an XML reader from a class name.

Given a class name, this method attempts to load and instantiate the class as an XML reader.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `className` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the class that should be instantiated. Note that this method will not be usable in environments where the caller (perhaps an applet) is not permitted to load classes dynamically. |

| Return ||
|------------------------------------------------------------------------------------------|-------------------|
| [XMLReader](../org/xml/sax/XMLReader.md)! | A new XML reader. |

| Exceptions ||
|----------------------------|---------------------------------------------------------------------|
| `org.xml.sax.SAXException` | If the class cannot be loaded, instantiated, and cast to XMLReader. |

**See Also**

- <https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderFactory#createXMLReader()>
