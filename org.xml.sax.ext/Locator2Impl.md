# Locator2Impl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Locator2Impl

```
open class Locator2Impl : LocatorImpl, Locator2
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [org.xml.sax.helpers.LocatorImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/LocatorImpl.html#) ||
| | ↳ | [org.xml.sax.ext.Locator2Impl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2Impl#) |

SAX2 extension helper for holding additional Entity information, implementing the [Locator2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2) interface.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.*

This is not part of core-only SAX2 distributions.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Locator2Impl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2Impl#Locator2Impl())`()` Construct a new, empty Locator2Impl object. |
| [Locator2Impl](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2Impl#Locator2Impl(org.xml.sax.Locator))`(`locator:` ` [Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator.html#)!`)` Copy an existing Locator or Locator2 object. |

| Public methods ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEncoding](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2Impl#getEncoding())`()` Returns the current value of the encoding property. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getXMLVersion](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2Impl#getXMLVersion())`()` Returns the current value of the version property. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEncoding](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2Impl#setEncoding(kotlin.String))`(`encoding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Assigns the current value of the encoding property. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setXMLVersion](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2Impl#setXMLVersion(kotlin.String))`(`version:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Assigns the current value of the version property. |

| Inherited functions ||
|---|---|
| From class [LocatorImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/LocatorImpl.html#) |-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnNumber](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/LocatorImpl.html#getColumnNumber())`()` <br /> Return the saved column number (1-based). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineNumber](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/LocatorImpl.html#getLineNumber())`()` <br /> Return the saved line number (1-based). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPublicId](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/LocatorImpl.html#getPublicId())`()` <br /> Return the saved public identifier. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSystemId](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/LocatorImpl.html#getSystemId())`()` <br /> Return the saved system identifier. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColumnNumber](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/LocatorImpl.html#setColumnNumber(kotlin.Int))`(`columnNumber:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set the column number for this locator (1-based). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLineNumber](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/LocatorImpl.html#setLineNumber(kotlin.Int))`(`lineNumber:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set the line number for this locator (1-based). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPublicId](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/LocatorImpl.html#setPublicId(kotlin.String))`(`publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Set the public identifier for this locator. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSystemId](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/LocatorImpl.html#setSystemId(kotlin.String))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Set the system identifier for this locator. <br /> | ||

## Public constructors

### Locator2Impl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Locator2Impl()
```

Construct a new, empty Locator2Impl object. This will not normally be useful, since the main purpose of this class is to make a snapshot of an existing Locator. 

### Locator2Impl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Locator2Impl(locator: Locator!)
```

Copy an existing Locator or Locator2 object. If the object implements Locator2, values of the*encoding* and*version* strings are copied, otherwise they set to*null*.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------|
| `locator` | [Locator](https://developer.android.com/reference/kotlin/org/xml/sax/Locator.html#)!:The existing Locator object. |

## Public methods

### getEncoding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEncoding(): String!
```

Returns the current value of the encoding property.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the current value of the encoding property. |

**See Also**

- [#setEncoding](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2Impl#setEncoding(kotlin.String)) 

### getXMLVersion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getXMLVersion(): String!
```

Returns the current value of the version property.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the current value of the version property. |

**See Also**

- [#setXMLVersion](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2Impl#setXMLVersion(kotlin.String)) 

### setEncoding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEncoding(encoding: String!): Unit
```

Assigns the current value of the encoding property.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------|
| `encoding` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the new "encoding" value |

**See Also**

- [#getEncoding](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2Impl#getEncoding()) 

### setXMLVersion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setXMLVersion(version: String!): Unit
```

Assigns the current value of the version property.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------|
| `version` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the new "version" value |

**See Also**

- [#getXMLVersion](https://developer.android.com/reference/kotlin/org/xml/sax/ext/Locator2Impl#getXMLVersion())
