# LocatorImpl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocatorImpl

```
open class LocatorImpl : Locator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [org.xml.sax.helpers.LocatorImpl](../org/xml/sax/helpers/LocatorImpl.md) |

| Known Direct Subclasses [Locator2Impl](../org/xml/sax/ext/Locator2Impl.md) |---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Locator2Impl](../org/xml/sax/ext/Locator2Impl.md) | SAX2 extension helper for holding additional Entity information, implementing the [Locator2](../org/xml/sax/ext/Locator2.md) interface. | |
| --- | --- | --- | --- | --- | --- | --- |

Provide an optional convenience implementation of Locator.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

This class is available mainly for application writers, who can use it to make a persistent snapshot of a locator at any point during a document parse: 

```kotlin
Locator locator;
  Locator startloc;
 
  public void setLocator (Locator locator)
  {
          // note the locator
    this.locator = locator;
  }
 
  public void startDocument ()
  {
          // save the location of the start of the document
          // for future use.
    Locator startloc = new LocatorImpl(locator);
  }
 
```

Normally, parser writers will not use this class, since it is more efficient to provide location information only when requested, rather than constantly updating a Locator object.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LocatorImpl](../org/xml/sax/helpers/LocatorImpl.md))`()` Zero-argument constructor. |
| [LocatorImpl](../org/xml/sax/helpers/LocatorImpl.md))`(`locator:` ` [Locator](../org/xml/sax/Locator.md)!`)` Copy constructor. |

| Public methods ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnNumber](../org/xml/sax/helpers/LocatorImpl.md))`()` Return the saved column number (1-based). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineNumber](../org/xml/sax/helpers/LocatorImpl.md))`()` Return the saved line number (1-based). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPublicId](../org/xml/sax/helpers/LocatorImpl.md))`()` Return the saved public identifier. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSystemId](../org/xml/sax/helpers/LocatorImpl.md))`()` Return the saved system identifier. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColumnNumber](../org/xml/sax/helpers/LocatorImpl.md))`(`columnNumber:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the column number for this locator (1-based). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLineNumber](../org/xml/sax/helpers/LocatorImpl.md))`(`lineNumber:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the line number for this locator (1-based). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPublicId](../org/xml/sax/helpers/LocatorImpl.md))`(`publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the public identifier for this locator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSystemId](../org/xml/sax/helpers/LocatorImpl.md))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the system identifier for this locator. |

## Public constructors

### LocatorImpl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LocatorImpl()
```

Zero-argument constructor.

This will not normally be useful, since the main purpose of this class is to make a snapshot of an existing Locator. 

### LocatorImpl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LocatorImpl(locator: Locator!)
```

Copy constructor.

Create a persistent copy of the current state of a locator. When the original locator changes, this copy will still keep the original values (and it can be used outside the scope of DocumentHandler methods).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------|
| `locator` | [Locator](../org/xml/sax/Locator.md)!:The locator to copy. |

## Public methods

### getColumnNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColumnNumber(): Int
```

Return the saved column number (1-based).

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The column number as an integer, or -1 if none is available. |

**See Also**

- [org.xml.sax.Locator#getColumnNumber](../org/xml/sax/Locator.md))
- [#setColumnNumber](../org/xml/sax/helpers/LocatorImpl.md)) 

### getLineNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLineNumber(): Int
```

Return the saved line number (1-based).

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The line number as an integer, or -1 if none is available. |

**See Also**

- [org.xml.sax.Locator#getLineNumber](../org/xml/sax/Locator.md))
- [#setLineNumber](../org/xml/sax/helpers/LocatorImpl.md)) 

### getPublicId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPublicId(): String!
```

Return the saved public identifier.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The public identifier as a string, or null if none is available. |

**See Also**

- [org.xml.sax.Locator#getPublicId](../org/xml/sax/Locator.md))
- [#setPublicId](../org/xml/sax/helpers/LocatorImpl.md)) 

### getSystemId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSystemId(): String!
```

Return the saved system identifier.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The system identifier as a string, or null if none is available. |

**See Also**

- [org.xml.sax.Locator#getSystemId](../org/xml/sax/Locator.md))
- [#setSystemId](../org/xml/sax/helpers/LocatorImpl.md)) 

### setColumnNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setColumnNumber(columnNumber: Int): Unit
```

Set the column number for this locator (1-based).

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------|
| `columnNumber` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The column number, or -1 if none is available. |

**See Also**

- [#getColumnNumber](../org/xml/sax/helpers/LocatorImpl.md)) 

### setLineNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLineNumber(lineNumber: Int): Unit
```

Set the line number for this locator (1-based).

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------|
| `lineNumber` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The line number, or -1 if none is available. |

**See Also**

- [#getLineNumber](../org/xml/sax/helpers/LocatorImpl.md)) 

### setPublicId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPublicId(publicId: String!): Unit
```

Set the public identifier for this locator.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The new public identifier, or null if none is available. |

**See Also**

- [#getPublicId](../org/xml/sax/helpers/LocatorImpl.md)) 

### setSystemId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSystemId(systemId: String!): Unit
```

Set the system identifier for this locator.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The new system identifier, or null if none is available. |

**See Also**

- [#getSystemId](../org/xml/sax/helpers/LocatorImpl.md))
