# OptionalDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OptionalDouble

```
class OptionalDouble
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.OptionalDouble](OptionalDouble.md) |

A container object which may or may not contain a`double`value. If a value is present,`isPresent()`returns`true`. If no value is present, the object is considered*empty* and`isPresent()`returns`false`.

Additional methods that depend on the presence or absence of a contained value are provided, such as [orElse()](OptionalDouble.md))(returns a default value if no value is present) and [ifPresent()](OptionalDouble.md))(performs an action if a value is present).

This is a [value-based](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/doc-files/ValueBased.html) class; programmers should treat instances that are [equal](OptionalDouble.md))as interchangeable and should not use instances for synchronization, or unpredictable behavior may occur. For example, in a future release, synchronization may fail.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [OptionalDouble](OptionalDouble.md)! | [empty](OptionalDouble.md))`()` Returns an empty`OptionalDouble`instance. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](OptionalDouble.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this`OptionalDouble`. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getAsDouble](OptionalDouble.md))`()` If a value is present, returns the value, otherwise throws`NoSuchElementException`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](OptionalDouble.md))`()` Returns the hash code of the value, if present, otherwise`0`(zero) if no value is present. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ifPresent](OptionalDouble.md))`(`action:` ` [DoubleConsumer](../java.util.function/DoubleConsumer.md)!`)` If a value is present, performs the given action with the value, otherwise does nothing. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ifPresentOrElse](OptionalDouble.md))`(`action:` ` [DoubleConsumer](../java.util.function/DoubleConsumer.md)!`, `emptyAction:` ` [Runnable](../java.lang/Runnable.md)!`)` If a value is present, performs the given action with the value, otherwise performs the given empty-based action. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](OptionalDouble.md))`()` If a value is not present, returns`true`, otherwise`false`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPresent](OptionalDouble.md))`()` If a value is present, returns`true`, otherwise`false`. |
| static [OptionalDouble](OptionalDouble.md)! | [of](OptionalDouble.md))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns an`OptionalDouble`describing the given value. |
| --- | --- |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [orElse](OptionalDouble.md))`(`other:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` If a value is present, returns the value, otherwise returns`other`. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [orElseGet](OptionalDouble.md))`(`supplier:` ` [DoubleSupplier](../java.util.function/DoubleSupplier.md)!`)` If a value is present, returns the value, otherwise returns the result produced by the supplying function. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [orElseThrow](OptionalDouble.md))`()` If a value is present, returns the value, otherwise throws`NoSuchElementException`. |
| --- | --- |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [orElseThrow](OptionalDouble.md))`(`exceptionSupplier:` ` [Supplier](../java.util.function/Supplier.md)<out` `X>!`)` If a value is present, returns the value, otherwise throws an exception produced by the exception supplying function. |
| [DoubleStream](../java.util.stream/DoubleStream.md)! | [stream](OptionalDouble.md))`()` If a value is present, returns a sequential [DoubleStream](../java.util.stream/DoubleStream.md) containing only that value, otherwise returns an empty`DoubleStream`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](OptionalDouble.md))`()` Returns a non-empty string representation of this`OptionalDouble`suitable for debugging. |
| --- | --- |

## Public methods

### empty

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun empty(): OptionalDouble!
```

Returns an empty`OptionalDouble`instance. No value is present for this`OptionalDouble`.

| Return ||
|---------------------------------------------------------------------------------------------|---------------------------|
| [OptionalDouble](OptionalDouble.md)! | an empty`OptionalDouble`. |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this`OptionalDouble`. The other object is considered equal if:

- it is also an`OptionalDouble`and;
- both instances have no value present or;
- the present values are "equal to" each other via`Double.compare() == 0`.

<br />

| Parameters ||
|-------|-------------------------------------|
| `obj` | an object to be tested for equality |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the other object is "equal to" this object otherwise`false` |

### getAsDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAsDouble(): Double
```

If a value is present, returns the value, otherwise throws`NoSuchElementException`.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the value described by this`OptionalDouble` |

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
fun ifPresent(action: DoubleConsumer!): Unit
```

If a value is present, performs the given action with the value, otherwise does nothing.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [DoubleConsumer](../java.util.function/DoubleConsumer.md)!:the action to be performed, if a value is present |

| Exceptions ||
|----------------------------------|---------------------------------------------------|
| `java.lang.NullPointerException` | if value is present and the given action is`null` |

### ifPresentOrElse

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun ifPresentOrElse(
    action: DoubleConsumer!, 
    emptyAction: Runnable!
): Unit
```

If a value is present, performs the given action with the value, otherwise performs the given empty-based action.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [DoubleConsumer](../java.util.function/DoubleConsumer.md)!:the action to be performed, if a value is present |
| `emptyAction` | [Runnable](../java.lang/Runnable.md)!:the empty-based action to be performed, if no value is present |

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
static fun of(value: Double): OptionalDouble!
```

Returns an`OptionalDouble`describing the given value.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the value to describe |

| Return ||
|---------------------------------------------------------------------------------------------|------------------------------------------|
| [OptionalDouble](OptionalDouble.md)! | an`OptionalDouble`with the value present |

### orElse

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun orElse(other: Double): Double
```

If a value is present, returns the value, otherwise returns`other`.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| `other` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the value to be returned, if no value is present |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the value, if present, otherwise`other` |

### orElseGet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun orElseGet(supplier: DoubleSupplier!): Double
```

If a value is present, returns the value, otherwise returns the result produced by the supplying function.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `supplier` | [DoubleSupplier](../java.util.function/DoubleSupplier.md)!:the supplying function that produces a value to be returned |

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the value, if present, otherwise the result produced by the supplying function |

| Exceptions ||
|----------------------------------|------------------------------------------------------------|
| `java.lang.NullPointerException` | if no value is present and the supplying function is`null` |

### orElseThrow

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun orElseThrow(): Double
```

If a value is present, returns the value, otherwise throws`NoSuchElementException`.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the value described by this`OptionalDouble` |

| Exceptions ||
|------------------------------------|------------------------|
| `java.util.NoSuchElementException` | if no value is present |

### orElseThrow

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <X : Throwable!> orElseThrow(exceptionSupplier: Supplier<out X>!): Double
```

If a value is present, returns the value, otherwise throws an exception produced by the exception supplying function.

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<X>` | Type of the exception to be thrown |
| `exceptionSupplier` | [Supplier](../java.util.function/Supplier.md)\<outX\>!:the supplying function that produces an exception to be thrown |

| Return ||
|----------------------------------------------------------------------------------|-----------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the value, if present |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------------|
| `X` | if no value is present |
| `java.lang.NullPointerException` | if no value is present and the exception supplying function is`null` |

### stream

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun stream(): DoubleStream!
```

If a value is present, returns a sequential [DoubleStream](../java.util.stream/DoubleStream.md) containing only that value, otherwise returns an empty`DoubleStream`.

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| [DoubleStream](../java.util.stream/DoubleStream.md)! | the optional value as a`DoubleStream` |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a non-empty string representation of this`OptionalDouble`suitable for debugging. The exact presentation format is unspecified and may vary between implementations and versions.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the string representation of this instance |
