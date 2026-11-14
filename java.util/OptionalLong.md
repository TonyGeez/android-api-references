# OptionalLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OptionalLong

```
class OptionalLong
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.util.OptionalLong](https://developer.android.com/reference/kotlin/java/util/OptionalLong#) |

A container object which may or may not contain a`long`value. If a value is present,`isPresent()`returns`true`. If no value is present, the object is considered*empty* and`isPresent()`returns`false`.

Additional methods that depend on the presence or absence of a contained value are provided, such as [orElse()](https://developer.android.com/reference/kotlin/java/util/OptionalLong#orElse(kotlin.Long))(returns a default value if no value is present) and [ifPresent()](https://developer.android.com/reference/kotlin/java/util/OptionalLong#ifPresent(java.util.function.LongConsumer))(performs an action if a value is present).

This is a [value-based](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/doc-files/ValueBased.html) class; programmers should treat instances that are [equal](https://developer.android.com/reference/kotlin/java/util/OptionalLong#equals(kotlin.Any))as interchangeable and should not use instances for synchronization, or unpredictable behavior may occur. For example, in a future release, synchronization may fail.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [OptionalLong](https://developer.android.com/reference/kotlin/java/util/OptionalLong#)! | [empty](https://developer.android.com/reference/kotlin/java/util/OptionalLong#empty())`()` Returns an empty`OptionalLong`instance. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/util/OptionalLong#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this`OptionalLong`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAsLong](https://developer.android.com/reference/kotlin/java/util/OptionalLong#getAsLong())`()` If a value is present, returns the value, otherwise throws`NoSuchElementException`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/util/OptionalLong#hashCode())`()` Returns the hash code of the value, if present, otherwise`0`(zero) if no value is present. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ifPresent](https://developer.android.com/reference/kotlin/java/util/OptionalLong#ifPresent(java.util.function.LongConsumer))`(`action:` ` [LongConsumer](https://developer.android.com/reference/kotlin/java/util/function/LongConsumer)!`)` If a value is present, performs the given action with the value, otherwise does nothing. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ifPresentOrElse](https://developer.android.com/reference/kotlin/java/util/OptionalLong#ifPresentOrElse(java.util.function.LongConsumer,%20java.lang.Runnable))`(`action:` ` [LongConsumer](https://developer.android.com/reference/kotlin/java/util/function/LongConsumer)!`, `emptyAction:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` If a value is present, performs the given action with the value, otherwise performs the given empty-based action. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/java/util/OptionalLong#isEmpty())`()` If a value is not present, returns`true`, otherwise`false`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPresent](https://developer.android.com/reference/kotlin/java/util/OptionalLong#isPresent())`()` If a value is present, returns`true`, otherwise`false`. |
| static [OptionalLong](https://developer.android.com/reference/kotlin/java/util/OptionalLong#)! | [of](https://developer.android.com/reference/kotlin/java/util/OptionalLong#of(kotlin.Long))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns an`OptionalLong`describing the given value. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [orElse](https://developer.android.com/reference/kotlin/java/util/OptionalLong#orElse(kotlin.Long))`(`other:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` If a value is present, returns the value, otherwise returns`other`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [orElseGet](https://developer.android.com/reference/kotlin/java/util/OptionalLong#orElseGet(java.util.function.LongSupplier))`(`supplier:` ` [LongSupplier](https://developer.android.com/reference/kotlin/java/util/function/LongSupplier)!`)` If a value is present, returns the value, otherwise returns the result produced by the supplying function. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [orElseThrow](https://developer.android.com/reference/kotlin/java/util/OptionalLong#orElseThrow())`()` If a value is present, returns the value, otherwise throws`NoSuchElementException`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [orElseThrow](https://developer.android.com/reference/kotlin/java/util/OptionalLong#orElseThrow(java.util.function.Supplier))`(`exceptionSupplier:` ` [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier)<out` `X>!`)` If a value is present, returns the value, otherwise throws an exception produced by the exception supplying function. |
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream)! | [stream](https://developer.android.com/reference/kotlin/java/util/OptionalLong#stream())`()` If a value is present, returns a sequential [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream) containing only that value, otherwise returns an empty`LongStream`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/OptionalLong#toString())`()` Returns a non-empty string representation of this`OptionalLong`suitable for debugging. |

## Public methods

### empty

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun empty(): OptionalLong!
```

Returns an empty`OptionalLong`instance. No value is present for this`OptionalLong`.

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------|
| [OptionalLong](https://developer.android.com/reference/kotlin/java/util/OptionalLong#)! | an empty`OptionalLong`. |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this`OptionalLong`. The other object is considered equal if:

- it is also an`OptionalLong`and;
- both instances have no value present or;
- the present values are "equal to" each other via`==`.

<br />

| Parameters ||
|-------|-------------------------------------|
| `obj` | an object to be tested for equality |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the other object is "equal to" this object otherwise`false` |

### getAsLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAsLong(): Long
```

If a value is present, returns the value, otherwise throws`NoSuchElementException`.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value described by this`OptionalLong` |

| Exceptions ||
|------------------------------------|------------------------|
| `java.util.NoSuchElementException` | if no value is present |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns the hash code of the value, if present, otherwise`0`(zero) if no value is present.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hash code value of the present value or`0`if no value is present |

### ifPresent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun ifPresent(action: LongConsumer!): Unit
```

If a value is present, performs the given action with the value, otherwise does nothing.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [LongConsumer](https://developer.android.com/reference/kotlin/java/util/function/LongConsumer)!:the action to be performed, if a value is present |

| Exceptions ||
|----------------------------------|---------------------------------------------------|
| `java.lang.NullPointerException` | if value is present and the given action is`null` |

### ifPresentOrElse

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun ifPresentOrElse(
    action: LongConsumer!, 
    emptyAction: Runnable!
): Unit
```

If a value is present, performs the given action with the value, otherwise performs the given empty-based action.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [LongConsumer](https://developer.android.com/reference/kotlin/java/util/function/LongConsumer)!:the action to be performed, if a value is present |
| `emptyAction` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!:the empty-based action to be performed, if no value is present |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if a value is present and the given action is`null`, or no value is present and the given empty-based action is`null`. |

### isEmpty

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isEmpty(): Boolean
```

If a value is not present, returns`true`, otherwise`false`.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if a value is not present, otherwise`false` |

### isPresent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isPresent(): Boolean
```

If a value is present, returns`true`, otherwise`false`.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if a value is present, otherwise`false` |

### of

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun of(value: Long): OptionalLong!
```

Returns an`OptionalLong`describing the given value.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value to describe |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------|
| [OptionalLong](https://developer.android.com/reference/kotlin/java/util/OptionalLong#)! | an`OptionalLong`with the value present |

### orElse

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun orElse(other: Long): Long
```

If a value is present, returns the value, otherwise returns`other`.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------|
| `other` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value to be returned, if no value is present |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value, if present, otherwise`other` |

### orElseGet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun orElseGet(supplier: LongSupplier!): Long
```

If a value is present, returns the value, otherwise returns the result produced by the supplying function.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `supplier` | [LongSupplier](https://developer.android.com/reference/kotlin/java/util/function/LongSupplier)!:the supplying function that produces a value to be returned |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value, if present, otherwise the result produced by the supplying function |

| Exceptions ||
|----------------------------------|------------------------------------------------------------|
| `java.lang.NullPointerException` | if no value is present and the supplying function is`null` |

### orElseThrow

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun orElseThrow(): Long
```

If a value is present, returns the value, otherwise throws`NoSuchElementException`.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value described by this`OptionalLong` |

| Exceptions ||
|------------------------------------|------------------------|
| `java.util.NoSuchElementException` | if no value is present |

### orElseThrow

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <X : Throwable!> orElseThrow(exceptionSupplier: Supplier<out X>!): Long
```

If a value is present, returns the value, otherwise throws an exception produced by the exception supplying function.

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<X>` | Type of the exception to be thrown |
| `exceptionSupplier` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier)\<outX\>!:the supplying function that produces an exception to be thrown |

| Return ||
|------------------------------------------------------------------------------|-----------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value, if present |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------------|
| `X` | if no value is present |
| `java.lang.NullPointerException` | if no value is present and the exception supplying function is`null` |

### stream

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun stream(): LongStream!
```

If a value is present, returns a sequential [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream) containing only that value, otherwise returns an empty`LongStream`.

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------|
| [LongStream](https://developer.android.com/reference/kotlin/java/util/stream/LongStream)! | the optional value as an`LongStream` |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a non-empty string representation of this`OptionalLong`suitable for debugging. The exact presentation format is unspecified and may vary between implementations and versions.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the string representation of this instance |
