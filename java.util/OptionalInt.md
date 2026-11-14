# OptionalInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OptionalInt

```
class OptionalInt
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.OptionalInt](../java/util/OptionalInt.md) |

A container object which may or may not contain an`int`value. If a value is present,`isPresent()`returns`true`. If no value is present, the object is considered*empty* and`isPresent()`returns`false`.

Additional methods that depend on the presence or absence of a contained value are provided, such as [orElse()](../java/util/OptionalInt.md))(returns a default value if no value is present) and [ifPresent()](../java/util/OptionalInt.md))(performs an action if a value is present).

This is a [value-based](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/doc-files/ValueBased.html) class; programmers should treat instances that are [equal](../java/util/OptionalInt.md))as interchangeable and should not use instances for synchronization, or unpredictable behavior may occur. For example, in a future release, synchronization may fail.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [OptionalInt](../java/util/OptionalInt.md)! | [empty](../java/util/OptionalInt.md))`()` Returns an empty`OptionalInt`instance. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/util/OptionalInt.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this`OptionalInt`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAsInt](../java/util/OptionalInt.md))`()` If a value is present, returns the value, otherwise throws`NoSuchElementException`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/util/OptionalInt.md))`()` Returns the hash code of the value, if present, otherwise`0`(zero) if no value is present. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ifPresent](../java/util/OptionalInt.md))`(`action:` ` [IntConsumer](../java/util/function/IntConsumer.md)!`)` If a value is present, performs the given action with the value, otherwise does nothing. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ifPresentOrElse](../java/util/OptionalInt.md))`(`action:` ` [IntConsumer](../java/util/function/IntConsumer.md)!`, `emptyAction:` ` [Runnable](../java/lang/Runnable.md)!`)` If a value is present, performs the given action with the value, otherwise performs the given empty-based action. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](../java/util/OptionalInt.md))`()` If a value is not present, returns`true`, otherwise`false`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPresent](../java/util/OptionalInt.md))`()` If a value is present, returns`true`, otherwise`false`. |
| static [OptionalInt](../java/util/OptionalInt.md)! | [of](../java/util/OptionalInt.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns an`OptionalInt`describing the given value. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [orElse](../java/util/OptionalInt.md))`(`other:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` If a value is present, returns the value, otherwise returns`other`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [orElseGet](../java/util/OptionalInt.md))`(`supplier:` ` [IntSupplier](../java/util/function/IntSupplier.md)!`)` If a value is present, returns the value, otherwise returns the result produced by the supplying function. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [orElseThrow](../java/util/OptionalInt.md))`()` If a value is present, returns the value, otherwise throws`NoSuchElementException`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [orElseThrow](../java/util/OptionalInt.md))`(`exceptionSupplier:` ` [Supplier](../java/util/function/Supplier.md)<out` `X>!`)` If a value is present, returns the value, otherwise throws an exception produced by the exception supplying function. |
| [IntStream](../java/util/stream/IntStream.md)! | [stream](../java/util/OptionalInt.md))`()` If a value is present, returns a sequential [IntStream](../java/util/stream/IntStream.md) containing only that value, otherwise returns an empty`IntStream`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/util/OptionalInt.md))`()` Returns a non-empty string representation of this`OptionalInt`suitable for debugging. |
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
| [OptionalInt](../java/util/OptionalInt.md)! | an empty`OptionalInt` |

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
| `action` | [IntConsumer](../java/util/function/IntConsumer.md)!:the action to be performed, if a value is present |

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
| `action` | [IntConsumer](../java/util/function/IntConsumer.md)!:the action to be performed, if a value is present |
| `emptyAction` | [Runnable](../java/lang/Runnable.md)!:the empty-based action to be performed, if no value is present |

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
| [OptionalInt](../java/util/OptionalInt.md)! | an`OptionalInt`with the value present |

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
| `supplier` | [IntSupplier](../java/util/function/IntSupplier.md)!:the supplying function that produces a value to be returned |

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
| `exceptionSupplier` | [Supplier](../java/util/function/Supplier.md)\<outX\>!:the supplying function that produces an exception to be thrown |

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

If a value is present, returns a sequential [IntStream](../java/util/stream/IntStream.md) containing only that value, otherwise returns an empty`IntStream`.

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------------------|
| [IntStream](../java/util/stream/IntStream.md)! | the optional value as an`IntStream` |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a non-empty string representation of this`OptionalInt`suitable for debugging. The exact presentation format is unspecified and may vary between implementations and versions.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the string representation of this instance |
