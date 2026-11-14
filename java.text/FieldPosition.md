# FieldPosition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FieldPosition

```
open class FieldPosition
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.text.FieldPosition](FieldPosition.md) |

`FieldPosition`is a simple class used by`Format`and its subclasses to identify fields in formatted output. Fields can be identified in two ways:

- By an integer constant, whose names typically end with`_FIELD`. The constants are defined in the various subclasses of`Format`.
- By a`Format.Field`constant, see`ERA_FIELD`and its friends in`DateFormat`for an example.

<br />

`FieldPosition`keeps track of the position of the field within the formatted output with two indices: the index of the first character of the field and the index of the last character of the field.

One version of the`format`method in the various`Format`classes requires a`FieldPosition`object as an argument. You use this`format`method to perform partial formatting or to get information about the formatted output (such as the position of a field).

If you are interested in the positions of all attributes in the formatted string use the`Format`method`formatToCharacterIterator`.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FieldPosition](FieldPosition.md))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a FieldPosition object for the given field. |
| [FieldPosition](FieldPosition.md))`(`attribute:` ` [Format.Field](../java/text/Format.Field.md)!`)` Creates a FieldPosition object for the given field constant. |
| [FieldPosition](FieldPosition.md))`(`attribute:` ` [Format.Field](../java/text/Format.Field.md)!`, `fieldID:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a`FieldPosition`object for the given field. |

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](FieldPosition.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Overrides equals |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBeginIndex](FieldPosition.md))`()` Retrieves the index of the first character in the requested field. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEndIndex](FieldPosition.md))`()` Retrieves the index of the character following the last character in the requested field. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getField](FieldPosition.md))`()` Retrieves the field identifier. |
| open [Format.Field](../java/text/Format.Field.md)! | [getFieldAttribute](FieldPosition.md))`()` Returns the field identifier as an attribute constant from one of the`Field`subclasses. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](FieldPosition.md))`()` Returns a hash code for this FieldPosition. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBeginIndex](FieldPosition.md))`(`bi:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the begin index. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEndIndex](FieldPosition.md))`(`ei:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the end index. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](FieldPosition.md))`()` Return a string representation of this FieldPosition. |
| --- | --- |

## Public constructors

### FieldPosition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FieldPosition(field: Int)
```

Creates a FieldPosition object for the given field. Fields are identified by constants, whose names typically end with _FIELD, in the various subclasses of Format.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the field identifier |

**See Also**

- [java.text.NumberFormat#INTEGER_FIELD](NumberFormat.md)
- [java.text.NumberFormat#FRACTION_FIELD](NumberFormat.md)
- [java.text.DateFormat#YEAR_FIELD](DateFormat.md)
- [java.text.DateFormat#MONTH_FIELD](DateFormat.md) 

### FieldPosition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FieldPosition(attribute: Format.Field!)
```

Creates a FieldPosition object for the given field constant. Fields are identified by constants defined in the various`Format`subclasses. This is equivalent to calling`new FieldPosition(attribute, -1)`.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------|
| `attribute` | [Format.Field](../java/text/Format.Field.md)!:Format.Field constant identifying a field |

### FieldPosition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FieldPosition(
    attribute: Format.Field!, 
    fieldID: Int)
```

Creates a`FieldPosition`object for the given field. The field is identified by an attribute constant from one of the`Field`subclasses as well as an integer field ID defined by the`Format`subclasses.`Format`subclasses that are aware of`Field`should give precedence to`attribute`and ignore`fieldID`if`attribute`is not null. However, older`Format`subclasses may not be aware of`Field`and rely on`fieldID`. If the field has no corresponding integer constant,`fieldID`should be -1.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------|
| `attribute` | [Format.Field](../java/text/Format.Field.md)!:Format.Field constant identifying a field |
| `fieldID` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):integer constant identifying a field |

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Overrides equals

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getBeginIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBeginIndex(): Int
```

Retrieves the index of the first character in the requested field.

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the begin index |

### getEndIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEndIndex(): Int
```

Retrieves the index of the character following the last character in the requested field.

| Return ||
|----------------------------------------------------------------------------|---------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the end index |

### getField

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getField(): Int
```

Retrieves the field identifier.

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the field identifier |

### getFieldAttribute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFieldAttribute(): Format.Field!
```

Returns the field identifier as an attribute constant from one of the`Field`subclasses. May return null if the field is specified only by an integer field ID.

| Return ||
|----------------------------------------------------------------------------------------|--------------------------|
| [Format.Field](../java/text/Format.Field.md)! | Identifier for the field |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns a hash code for this FieldPosition.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object |

### setBeginIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setBeginIndex(bi: Int): Unit
```

Sets the begin index. For use by subclasses of Format.

| Parameters ||
|------|--------------------------------------------------------------------------------------------|
| `bi` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the begin index |

### setEndIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEndIndex(ei: Int): Unit
```

Sets the end index. For use by subclasses of Format.

| Parameters ||
|------|------------------------------------------------------------------------------------------|
| `ei` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the end index |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Return a string representation of this FieldPosition.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this object |
