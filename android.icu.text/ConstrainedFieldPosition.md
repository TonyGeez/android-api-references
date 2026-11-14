# ConstrainedFieldPosition

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConstrainedFieldPosition

Kotlin| [Java](ConstrainedFieldPosition.md) 
| --- | --- |

```
open class ConstrainedFieldPosition
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.ConstrainedFieldPosition](ConstrainedFieldPosition.md) |

Represents a span of a string containing a given field. This class differs from FieldPosition in the following ways: 1. It has information on the field category. 2. It allows you to set constraints to use when iterating over field positions. 3. It is used for the newer FormattedValue APIs.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ConstrainedFieldPosition](ConstrainedFieldPosition.md))`()` Initializes a CategoryFieldPosition. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [constrainClass](ConstrainedFieldPosition.md))`(`classConstraint:` ` [Class](../java.lang/Class.md)<*>!`)` Sets a constraint on the field class. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [constrainField](ConstrainedFieldPosition.md))`(`field:` ` [Format.Field](../java/text/Format.Field.md)!`)` Sets a constraint on the field. |
| open [Format.Field](../java/text/Format.Field.md)! | [getField](ConstrainedFieldPosition.md))`()` Gets the field for the current position. |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getFieldValue](ConstrainedFieldPosition.md))`()` Gets the value associated with the current field position. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getInt64IterationContext](ConstrainedFieldPosition.md))`()` Gets an int64 that FormattedValue implementations may use for storage. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLimit](ConstrainedFieldPosition.md))`()` Gets the EXCLUSIVE end index stored for the current position. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStart](ConstrainedFieldPosition.md))`()` Gets the INCLUSIVE start index for the current position. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [matchesField](ConstrainedFieldPosition.md))`(`field:` ` [Format.Field](../java/text/Format.Field.md)!`, `fieldValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Determines whether a given field and value should be included given the constraints. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](ConstrainedFieldPosition.md))`()` Resets this ConstrainedFieldPosition to its initial state, as if it were newly created: - Removes any constraints that may have been set on the instance. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInt64IterationContext](ConstrainedFieldPosition.md))`(`context:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets an int64 that FormattedValue implementations may use for storage. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setState](ConstrainedFieldPosition.md))`(`field:` ` [Format.Field](../java/text/Format.Field.md)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets new values for the primary public getters. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](ConstrainedFieldPosition.md))`()` Returns a string representation of the object. |
| --- | --- |

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

Sets a constraint on the field class. When this instance of ConstrainedFieldPosition is passed to [FormattedValue.nextPosition](FormattedValue.md)), positions are skipped unless the field is an instance of the class constraint, including subclasses. Any previously set constraints are cleared. For example, to loop over only the number-related fields: 

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
| `classConstraint` | [Class](../java.lang/Class.md)\<\*\>!:The field class to fix when iterating. |

### constrainField

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun constrainField(field: Format.Field!): Unit
```

Sets a constraint on the field. When this instance of ConstrainedFieldPosition is passed to [FormattedValue.nextPosition](FormattedValue.md)), positions are skipped unless they have the given field. Any previously set constraints are cleared. For example, to loop over all grouping separators: 

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
| `field` | [Format.Field](../java/text/Format.Field.md)!:The field to fix when iterating. |

### getField

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getField(): Format.Field!
```

Gets the field for the current position. The return value is well-defined and non-null only after FormattedValue#nextPosition returns true.

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Format.Field](../java/text/Format.Field.md)! | The field saved in the instance. See above for null conditions. |

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
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The current iteration context from [setInt64IterationContext](ConstrainedFieldPosition.md)). |

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
| `field` | [Format.Field](../java/text/Format.Field.md)!:The field to test. |
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
| `field` | [Format.Field](../java/text/Format.Field.md)!:The new field. |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The new field value. Should be null if there is no value. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new inclusive start index. |
| --- | --- |
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
