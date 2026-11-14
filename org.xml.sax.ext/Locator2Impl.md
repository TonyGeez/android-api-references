# Locator2Impl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Locator2Impl

```
open class Locator2Impl : LocatorImpl, Locator2
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [org.xml.sax.helpers.LocatorImpl](../org.xml.sax.helpers/LocatorImpl.md) ||
| | ↳ | [org.xml.sax.ext.Locator2Impl](Locator2Impl.md) |

SAX2 extension helper for holding additional Entity information, implementing the [Locator2](Locator2.md) interface.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.*

This is not part of core-only SAX2 distributions.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Locator2Impl](Locator2Impl.md))`()` Construct a new, empty Locator2Impl object. |
| [Locator2Impl](Locator2Impl.md))`(`locator:` ` [Locator](../org.xml.sax/Locator.md)!`)` Copy an existing Locator or Locator2 object. |

| Public methods ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEncoding](Locator2Impl.md))`()` Returns the current value of the encoding property. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getXMLVersion](Locator2Impl.md))`()` Returns the current value of the version property. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEncoding](Locator2Impl.md))`(`encoding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Assigns the current value of the encoding property. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setXMLVersion](Locator2Impl.md))`(`version:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Assigns the current value of the version property. |

| Inherited functions ||
|---|---|
| From class [LocatorImpl](../org.xml.sax.helpers/LocatorImpl.md) |-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnNumber](../org.xml.sax.helpers/LocatorImpl.md))`()` <br /> Return the saved column number (1-based). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineNumber](../org.xml.sax.helpers/LocatorImpl.md))`()` <br /> Return the saved line number (1-based). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPublicId](../org.xml.sax.helpers/LocatorImpl.md))`()` <br /> Return the saved public identifier. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSystemId](../org.xml.sax.helpers/LocatorImpl.md))`()` <br /> Return the saved system identifier. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColumnNumber](../org.xml.sax.helpers/LocatorImpl.md))`(`columnNumber:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set the column number for this locator (1-based). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLineNumber](../org.xml.sax.helpers/LocatorImpl.md))`(`lineNumber:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set the line number for this locator (1-based). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPublicId](../org.xml.sax.helpers/LocatorImpl.md))`(`publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Set the public identifier for this locator. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSystemId](../org.xml.sax.helpers/LocatorImpl.md))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Set the system identifier for this locator. <br /> | ||

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
| `locator` | [Locator](../org.xml.sax/Locator.md)!:The existing Locator object. |

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

- [#setEncoding](Locator2Impl.md)) 

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

- [#setXMLVersion](Locator2Impl.md)) 

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

- [#getEncoding](Locator2Impl.md)) 

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

- [#getXMLVersion](Locator2Impl.md))
