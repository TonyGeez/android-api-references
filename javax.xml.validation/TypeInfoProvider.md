# TypeInfoProvider

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TypeInfoProvider

```
abstract class TypeInfoProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [javax.xml.validation.TypeInfoProvider](https://developer.android.com/reference/kotlin/javax/xml/validation/TypeInfoProvider#) |

This class provides access to the type information determined by [ValidatorHandler](https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler).

Some schema languages, such as W3C XML Schema, encourages a validator to report the "type" it assigns to each attribute/element. Those applications who wish to access this type information can invoke methods defined on this "interface" to access such type information.

Implementation of this "interface" can be obtained through the [ValidatorHandler.getTypeInfoProvider()](https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler#getTypeInfoProvider())method.

## Summary

| Protected constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TypeInfoProvider](https://developer.android.com/reference/kotlin/javax/xml/validation/TypeInfoProvider#TypeInfoProvider())`()` Constructor for the derived class. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [TypeInfo](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-type-info/index.html)! | [getAttributeTypeInfo](https://developer.android.com/reference/kotlin/javax/xml/validation/TypeInfoProvider#getAttributeTypeInfo(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the immutable [TypeInfo](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-type-info/index.html) object for the specified attribute of the current element. |
| abstract [TypeInfo](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-type-info/index.html)! | [getElementTypeInfo](https://developer.android.com/reference/kotlin/javax/xml/validation/TypeInfoProvider#getElementTypeInfo())`()` Returns the immutable [TypeInfo](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-type-info/index.html) object for the current element. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isIdAttribute](https://developer.android.com/reference/kotlin/javax/xml/validation/TypeInfoProvider#isIdAttribute(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if the specified attribute is determined to be ID. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSpecified](https://developer.android.com/reference/kotlin/javax/xml/validation/TypeInfoProvider#isSpecified(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns false if the attribute was added by the validator. |

## Protected constructors

### TypeInfoProvider

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected TypeInfoProvider()
```

Constructor for the derived class.

The constructor does nothing.

## Public methods

### getAttributeTypeInfo

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAttributeTypeInfo(index: Int): TypeInfo!
```

Returns the immutable [TypeInfo](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-type-info/index.html) object for the specified attribute of the current element.

The method may only be called by the startElement event of the [org.xml.sax.ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#) that the application sets to the [ValidatorHandler](https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler).

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the attribute. The same index for the [org.xml.sax.Attributes](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#) object passed to the startElement callback. |

| Return ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [TypeInfo](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-type-info/index.html)! | An immutable [TypeInfo](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-type-info/index.html) object that represents the type of the specified attribute. Note that the caller can keep references to the obtained [TypeInfo](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-type-info/index.html) longer than the callback scope. Otherwise, this method returns null if the validator is unable to determine the type. |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the index is invalid. |
| `java.lang.IllegalStateException` | If this method is called from other [org.xml.sax.ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#) methods. |

### getElementTypeInfo

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getElementTypeInfo(): TypeInfo!
```

Returns the immutable [TypeInfo](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-type-info/index.html) object for the current element.

The method may only be called by the startElement and endElement event of the [org.xml.sax.ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#) that the application sets to the [ValidatorHandler](https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler).

| Return ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [TypeInfo](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-type-info/index.html)! | An immutable [TypeInfo](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-type-info/index.html) object that represents the type of the current element. Note that the caller can keep references to the obtained [TypeInfo](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-type-info/index.html) longer than the callback scope. Otherwise, this method returns null if the validator is unable to determine the type of the current element for some reason (for example, if the validator is recovering from an earlier error.) |

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If this method is called from other [org.xml.sax.ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#) methods. |

### isIdAttribute

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isIdAttribute(index: Int): Boolean
```

Returns true if the specified attribute is determined to be ID.

Exactly how an attribute is "determined to be ID" is up to the schema language. In case of W3C XML Schema, this means that the actual type of the attribute is the built-in ID type or its derived type.

A [javax.xml.parsers.DocumentBuilder](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder.html#) uses this information to properly implement [org.w3c.dom.Attr#isId()](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-attr/is-id.html).

The method may only be called by the startElement event of the [org.xml.sax.ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#) that the application sets to the [ValidatorHandler](https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler).

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the attribute. The same index for the [org.xml.sax.Attributes](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#) object passed to the startElement callback. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the type of the specified attribute is ID. |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the index is invalid. |
| `java.lang.IllegalStateException` | If this method is called from other [org.xml.sax.ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#) methods. |

### isSpecified

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isSpecified(index: Int): Boolean
```

Returns false if the attribute was added by the validator.

This method provides information necessary for a [javax.xml.parsers.DocumentBuilder](https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder.html#) to determine what the DOM tree should return from the [org.w3c.dom.Attr#getSpecified()](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-attr/get-specified.html) method.

The method may only be called by the startElement event of the [org.xml.sax.ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#) that the application sets to the [ValidatorHandler](https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler).

A general guideline for validators is to return true if the attribute was originally present in the pipeline, and false if it was added by the validator.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the attribute. The same index for the [org.xml.sax.Attributes](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#) object passed to the startElement callback. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the attribute was present before the validator processes input. false if the attribute was added by the validator. |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the index is invalid. |
| `java.lang.IllegalStateException` | If this method is called from other [org.xml.sax.ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#) methods. |
