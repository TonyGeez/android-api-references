# ConstrainedFieldPosition

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConstrainedFieldPosition

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/ConstrainedFieldPosition "View this page in Java") 

```
open class ConstrainedFieldPosition
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.icu.text.ConstrainedFieldPosition](https://developer.android.com/reference/kotlin/android/icu/text/ConstrainedFieldPosition#) |

Represents a span of a string containing a given field. This class differs from FieldPosition in the following ways: 1. It has information on the field category. 2. It allows you to set constraints to use when iterating over field positions. 3. It is used for the newer FormattedValue APIs.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ConstrainedFieldPosition](https://developer.android.com/reference/kotlin/android/icu/text/ConstrainedFieldPosition#ConstrainedFieldPosition())`()` Initializes a CategoryFieldPosition. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [constrainClass](https://developer.android.com/reference/kotlin/android/icu/text/ConstrainedFieldPosition#constrainClass(java.lang.Class))`(`classConstraint:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!`)` Sets a constraint on the field class. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [constrainField](https://developer.android.com/reference/kotlin/android/icu/text/ConstrainedFieldPosition#constrainField(java.text.Format.Field))`(`field:` ` [Format.Field](https://developer.android.com/reference/kotlin/java/text/Format.Field.html#)!`)` Sets a constraint on the field. |
| open [Format.Field](https://developer.android.com/reference/kotlin/java/text/Format.Field.html#)! | [getField](https://developer.android.com/reference/kotlin/android/icu/text/ConstrainedFieldPosition#getField())`()` Gets the field for the current position. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getFieldValue](https://developer.android.com/reference/kotlin/android/icu/text/ConstrainedFieldPosition#getFieldValue())`()` Gets the value associated with the current field position. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getInt64IterationContext](https://developer.android.com/reference/kotlin/android/icu/text/ConstrainedFieldPosition#getInt64IterationContext())`()` Gets an int64 that FormattedValue implementations may use for storage. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLimit](https://developer.android.com/reference/kotlin/android/icu/text/ConstrainedFieldPosition#getLimit())`()` Gets the EXCLUSIVE end index stored for the current position. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStart](https://developer.android.com/reference/kotlin/android/icu/text/ConstrainedFieldPosition#getStart())`()` Gets the INCLUSIVE start index for the current position. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [matchesField](https://developer.android.com/reference/kotlin/android/icu/text/ConstrainedFieldPosition#matchesField(java.text.Format.Field,%20kotlin.Any))`(`field:` ` [Format.Field](https://developer.android.com/reference/kotlin/java/text/Format.Field.html#)!`, `fieldValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Determines whether a given field and value should be included given the constraints. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/android/icu/text/ConstrainedFieldPosition#reset())`()` Resets this ConstrainedFieldPosition to its initial state, as if it were newly created: - Removes any constraints that may have been set on the instance. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInt64IterationContext](https://developer.android.com/reference/kotlin/android/icu/text/ConstrainedFieldPosition#setInt64IterationContext(kotlin.Long))`(`context:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets an int64 that FormattedValue implementations may use for storage. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setState](https://developer.android.com/reference/kotlin/android/icu/text/ConstrainedFieldPosition#setState(java.text.Format.Field,%20kotlin.Any,%20kotlin.Int,%20kotlin.Int))`(`field:` ` [Format.Field](https://developer.android.com/reference/kotlin/java/text/Format.Field.html#)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets new values for the primary public getters. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/icu/text/ConstrainedFieldPosition#toString())`()` Returns a string representation of the object. |

## Public constructors

### ConstrainedFieldPosition

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ConstrainedFieldPosition()
```

Initializes a CategoryFieldPosition. By default, the CategoryFieldPosition has no iteration constraints.

## Public methods

### constrainClass

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun constrainClass(classConstraint: Class<*>!): Unit
```

Sets a constraint on the field class. When this instance of ConstrainedFieldPosition is passed to [FormattedValue.nextPosition](https://developer.android.com/reference/kotlin/android/icu/text/FormattedValue#nextPosition(android.icu.text.ConstrainedFieldPosition)), positions are skipped unless the field is an instance of the class constraint, including subclasses. Any previously set constraints are cleared. For example, to loop over only the number-related fields: 

```kotlin
ConstrainedFieldPosition cfpos;
  cfpos.constrainClass(NumberFormat.Field.class);
  while (fmtval.nextPosition(cfpos)) {
    // handle the number-related field position
  }
  
```

<br />

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `classConstraint` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<\*\>!:The field class to fix when iterating. |

### constrainField

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun constrainField(field: Format.Field!): Unit
```

Sets a constraint on the field. When this instance of ConstrainedFieldPosition is passed to [FormattedValue.nextPosition](https://developer.android.com/reference/kotlin/android/icu/text/FormattedValue#nextPosition(android.icu.text.ConstrainedFieldPosition)), positions are skipped unless they have the given field. Any previously set constraints are cleared. For example, to loop over all grouping separators: 

```kotlin
ConstrainedFieldPosition cfpos;
  cfpos.constrainField(NumberFormat.Field.GROUPING_SEPARATOR);
  while (fmtval.nextPosition(cfpos)) {
    // handle the grouping separator position
  }
  
```
Changing the constraint while in the middle of iterating over a FormattedValue does not generally have well-defined behavior.

<br />

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------|
| `field` | [Format.Field](https://developer.android.com/reference/kotlin/java/text/Format.Field.html#)!:The field to fix when iterating. |

### getField

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getField(): Format.Field!
```

Gets the field for the current position. The return value is well-defined and non-null only after FormattedValue#nextPosition returns true.

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Format.Field](https://developer.android.com/reference/kotlin/java/text/Format.Field.html#)! | The field saved in the instance. See above for null conditions. |

### getFieldValue

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFieldValue(): Any!
```

Gets the value associated with the current field position. The field value is often not set. The return value is well-defined only after FormattedValue#nextPosition returns true.

| Return ||
|-----------------------------------------------------------------------------|----------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The value for the current position. Might be null. |

### getInt64IterationContext

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInt64IterationContext(): Long
```

Gets an int64 that FormattedValue implementations may use for storage. The initial value is zero. Users of FormattedValue should not need to call this method.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The current iteration context from [setInt64IterationContext](https://developer.android.com/reference/kotlin/android/icu/text/ConstrainedFieldPosition#setInt64IterationContext(kotlin.Long)). |

### getLimit

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLimit(): Int
```

Gets the EXCLUSIVE end index stored for the current position. The return value is well-defined only after FormattedValue#nextPosition returns true.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The end index saved in the instance. |

### getStart

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStart(): Int
```

Gets the INCLUSIVE start index for the current position. The return value is well-defined only after FormattedValue#nextPosition returns true.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The start index saved in the instance. |

### matchesField

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun matchesField(
    field: Format.Field!, 
    fieldValue: Any!
): Boolean
```

Determines whether a given field and value should be included given the constraints. Intended to be used by FormattedValue implementations.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [Format.Field](https://developer.android.com/reference/kotlin/java/text/Format.Field.html#)!:The field to test. |
| `fieldValue` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The field value to test. Should be null if there is no value. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the field should be included given the constraints. |

### reset

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Resets this ConstrainedFieldPosition to its initial state, as if it were newly created: - Removes any constraints that may have been set on the instance. - Resets the iteration position. 

### setInt64IterationContext

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInt64IterationContext(context: Long): Unit
```

Sets an int64 that FormattedValue implementations may use for storage. Intended to be used by FormattedValue implementations.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------|
| `context` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The new iteration context. |

### setState

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setState(
    field: Format.Field!, 
    value: Any!, 
    start: Int, 
    limit: Int
): Unit
```

Sets new values for the primary public getters. Intended to be used by FormattedValue implementations. It is up to the implementation to ensure that the user-requested constraints are satisfied. This method does not check!

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [Format.Field](https://developer.android.com/reference/kotlin/java/text/Format.Field.html#)!:The new field. |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The new field value. Should be null if there is no value. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new inclusive start index. |
| `limit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new exclusive end index. |

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
