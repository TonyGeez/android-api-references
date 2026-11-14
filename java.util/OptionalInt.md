# OptionalInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OptionalInt

```
class OptionalInt
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.OptionalInt](https://developer.android.com/reference/kotlin/java/util/OptionalInt#) |

A container object which may or may not contain an`int`value. If a value is present,`isPresent()`returns`true`. If no value is present, the object is considered*empty* and`isPresent()`returns`false`.

Additional methods that depend on the presence or absence of a contained value are provided, such as [orElse()](https://developer.android.com/reference/kotlin/java/util/OptionalInt#orElse(kotlin.Int))(returns a default value if no value is present) and [ifPresent()](https://developer.android.com/reference/kotlin/java/util/OptionalInt#ifPresent(java.util.function.IntConsumer))(performs an action if a value is present).

This is a [value-based](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/doc-files/ValueBased.html) class; programmers should treat instances that are [equal](https://developer.android.com/reference/kotlin/java/util/OptionalInt#equals(kotlin.Any))as interchangeable and should not use instances for synchronization, or unpredictable behavior may occur. For example, in a future release, synchronization may fail.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [OptionalInt](https://developer.android.com/reference/kotlin/java/util/OptionalInt#)! | [empty](https://developer.android.com/reference/kotlin/java/util/OptionalInt#empty())`()` Returns an empty`OptionalInt`instance. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/util/OptionalInt#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this`OptionalInt`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAsInt](https://developer.android.com/reference/kotlin/java/util/OptionalInt#getAsInt())`()` If a value is present, returns the value, otherwise throws`NoSuchElementException`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/util/OptionalInt#hashCode())`()` Returns the hash code of the value, if present, otherwise`0`(zero) if no value is present. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ifPresent](https://developer.android.com/reference/kotlin/java/util/OptionalInt#ifPresent(java.util.function.IntConsumer))`(`action:` ` [IntConsumer](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer)!`)` If a value is present, performs the given action with the value, otherwise does nothing. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ifPresentOrElse](https://developer.android.com/reference/kotlin/java/util/OptionalInt#ifPresentOrElse(java.util.function.IntConsumer,%20java.lang.Runnable))`(`action:` ` [IntConsumer](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer)!`, `emptyAction:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` If a value is present, performs the given action with the value, otherwise performs the given empty-based action. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/java/util/OptionalInt#isEmpty())`()` If a value is not present, returns`true`, otherwise`false`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPresent](https://developer.android.com/reference/kotlin/java/util/OptionalInt#isPresent())`()` If a value is present, returns`true`, otherwise`false`. |
| static [OptionalInt](https://developer.android.com/reference/kotlin/java/util/OptionalInt#)! | [of](https://developer.android.com/reference/kotlin/java/util/OptionalInt#of(kotlin.Int))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns an`OptionalInt`describing the given value. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [orElse](https://developer.android.com/reference/kotlin/java/util/OptionalInt#orElse(kotlin.Int))`(`other:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` If a value is present, returns the value, otherwise returns`other`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [orElseGet](https://developer.android.com/reference/kotlin/java/util/OptionalInt#orElseGet(java.util.function.IntSupplier))`(`supplier:` ` [IntSupplier](https://developer.android.com/reference/kotlin/java/util/function/IntSupplier)!`)` If a value is present, returns the value, otherwise returns the result produced by the supplying function. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [orElseThrow](https://developer.android.com/reference/kotlin/java/util/OptionalInt#orElseThrow())`()` If a value is present, returns the value, otherwise throws`NoSuchElementException`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [orElseThrow](https://developer.android.com/reference/kotlin/java/util/OptionalInt#orElseThrow(java.util.function.Supplier))`(`exceptionSupplier:` ` [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier)<out` `X>!`)` If a value is present, returns the value, otherwise throws an exception produced by the exception supplying function. |
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream)! | [stream](https://developer.android.com/reference/kotlin/java/util/OptionalInt#stream())`()` If a value is present, returns a sequential [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream) containing only that value, otherwise returns an empty`IntStream`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/OptionalInt#toString())`()` Returns a non-empty string representation of this`OptionalInt`suitable for debugging. |
| --- | --- |

## Public methods

### empty

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun empty(): OptionalInt!
```

Returns an empty`OptionalInt`instance. No value is present for this`OptionalInt`.

| Return ||
|---------------------------------------------------------------------------------------|-----------------------|
| [OptionalInt](https://developer.android.com/reference/kotlin/java/util/OptionalInt#)! | an empty`OptionalInt` |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this`OptionalInt`. The other object is considered equal if:

- it is also an`OptionalInt`and;
- both instances have no value present or;
- the present values are "equal to" each other via`==`.

<br />

| Parameters ||
|-------|-------------------------------------|
| `obj` | an object to be tested for equality |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the other object is "equal to" this object otherwise`false` |

### getAsInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAsInt(): Int
```

If a value is present, returns the value, otherwise throws`NoSuchElementException`.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value described by this`OptionalInt` |

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
fun ifPresent(action: IntConsumer!): Unit
```

If a value is present, performs the given action with the value, otherwise does nothing.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [IntConsumer](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer)!:the action to be performed, if a value is present |

| Exceptions ||
|----------------------------------|---------------------------------------------------|
| `java.lang.NullPointerException` | if value is present and the given action is`null` |

### ifPresentOrElse

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun ifPresentOrElse(
    action: IntConsumer!, 
    emptyAction: Runnable!
): Unit
```

If a value is present, performs the given action with the value, otherwise performs the given empty-based action.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [IntConsumer](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer)!:the action to be performed, if a value is present |
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
static fun of(value: Int): OptionalInt!
```

Returns an`OptionalInt`describing the given value.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value to describe |

| Return ||
|---------------------------------------------------------------------------------------|---------------------------------------|
| [OptionalInt](https://developer.android.com/reference/kotlin/java/util/OptionalInt#)! | an`OptionalInt`with the value present |

### orElse

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun orElse(other: Int): Int
```

If a value is present, returns the value, otherwise returns`other`.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------|
| `other` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value to be returned, if no value is present |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value, if present, otherwise`other` |

### orElseGet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun orElseGet(supplier: IntSupplier!): Int
```

If a value is present, returns the value, otherwise returns the result produced by the supplying function.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `supplier` | [IntSupplier](https://developer.android.com/reference/kotlin/java/util/function/IntSupplier)!:the supplying function that produces a value to be returned |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value, if present, otherwise the result produced by the supplying function |

| Exceptions ||
|----------------------------------|------------------------------------------------------------|
| `java.lang.NullPointerException` | if no value is present and the supplying function is`null` |

### orElseThrow

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun orElseThrow(): Int
```

If a value is present, returns the value, otherwise throws`NoSuchElementException`.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value described by this`OptionalInt` |

| Exceptions ||
|------------------------------------|------------------------|
| `java.util.NoSuchElementException` | if no value is present |

### orElseThrow

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <X : Throwable!> orElseThrow(exceptionSupplier: Supplier<out X>!): Int
```

If a value is present, returns the value, otherwise throws an exception produced by the exception supplying function.

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<X>` | Type of the exception to be thrown |
| `exceptionSupplier` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier)\<outX\>!:the supplying function that produces an exception to be thrown |

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value, if present |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------------|
| `X` | if no value is present |
| `java.lang.NullPointerException` | if no value is present and the exception supplying function is`null` |

### stream

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun stream(): IntStream!
```

If a value is present, returns a sequential [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream) containing only that value, otherwise returns an empty`IntStream`.

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------------------|
| [IntStream](https://developer.android.com/reference/kotlin/java/util/stream/IntStream)! | the optional value as an`IntStream` |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a non-empty string representation of this`OptionalInt`suitable for debugging. The exact presentation format is unspecified and may vary between implementations and versions.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the string representation of this instance |
