Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ParserFactory

```
open class ParserFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [org.xml.sax.helpers.ParserFactory](ParserFactory.md) |

| **This class was deprecated in API level 9.**
|
| This class works with the deprecated `https://developer.android.com/reference/kotlin/org/xml/sax/Parser.html#` interface.

Java-specific class for dynamically loading SAX parsers. *This module, both source code and documentation, is in the Public Domain, and comes with **NO WARRANTY**.* See <http://www.saxproject.org> for further information.

**Note:** This class is designed to work with the now-deprecated SAX1 `https://developer.android.com/reference/kotlin/org/xml/sax/Parser.html#` class. SAX2 applications should use `https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLReaderFactory` instead.

ParserFactory is not part of the platform-independent definition of SAX; it is an additional convenience class designed specifically for Java XML application writers. SAX applications can use the static methods in this class to allocate a SAX parser dynamically at run-time based either on the value of the \`org.xml.sax.parser' system property or on a string containing the class name.

Note that the application still requires an XML parser that implements SAX1.

## Summary

| Public methods ||
|---|---|
| open static [Parser](../org.xml.sax/Parser.md)! | `https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserFactory#makeParser()()` Create a new SAX parser using the \`org. |
| open static [Parser](../org.xml.sax/Parser.md)! | `https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserFactory#makeParser(kotlin.String)(className: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Create a new SAX parser object using the class name provided. |

## Public methods

### makeParser

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun makeParser(): Parser!
```

**Deprecated:** *Deprecated in Java.*

Create a new SAX parser using the \`org.xml.sax.parser' system property.

The named class must exist and must implement the `https://developer.android.com/reference/kotlin/org/xml/sax/Parser.html#` interface.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/org/xml/sax/Parser.html#!` | the newly created parser. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | The SAX parser class was found and instantiated, but does not implement org.xml.sax.Parser. |
| `java.lang.ClassNotFoundException` | The SAX parser class was not found (check your CLASSPATH). |
| `java.lang.IllegalAccessException` | The SAX parser class was found, but you do not have permission to load it. |
| --- | --- |
| `java.lang.InstantiationException` | The SAX parser class was found but could not be instantiated. |
| `java.lang.NullPointerException` | There is no value for the \`org.xml.sax.parser' system property. |

**See Also**

- `https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserFactory#makeParser(kotlin.String)`
- `https://developer.android.com/reference/kotlin/org/xml/sax/Parser.html#`

### makeParser

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun makeParser(className: String!): Parser!
```

**Deprecated:** *Deprecated in Java.*

Create a new SAX parser object using the class name provided.

The named class must exist and must implement the `https://developer.android.com/reference/kotlin/org/xml/sax/Parser.html#` interface.

| Parameters ||
|---|---|
| `className` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A string containing the name of the SAX parser class. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/org/xml/sax/Parser.html#!` | the newly created parser. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | The SAX parser class was found and instantiated, but does not implement org.xml.sax.Parser. |
| `java.lang.ClassNotFoundException` | The SAX parser class was not found (check your CLASSPATH). |
| `java.lang.IllegalAccessException` | The SAX parser class was found, but you do not have permission to load it. |
| --- | --- |
| `java.lang.InstantiationException` | The SAX parser class was found but could not be instantiated. |

**See Also**

- `https://developer.android.com/reference/kotlin/org/xml/sax/helpers/ParserFactory#makeParser()`
- `https://developer.android.com/reference/kotlin/org/xml/sax/Parser.html#`
