# Optional

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Optional

```
class Optional<T : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.Optional](Optional.md) |

A container object which may or may not contain a non-`null`value. If a value is present,`isPresent()`returns`true`. If no value is present, the object is considered*empty* and`isPresent()`returns`false`.

Additional methods that depend on the presence or absence of a contained value are provided, such as [orElse()](Optional.md))(returns a default value if no value is present) and [ifPresent()](Optional.md))(performs an action if a value is present).

This is a [value-based](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/doc-files/ValueBased.html) class; programmers should treat instances that are [equal](Optional.md))as interchangeable and should not use instances for synchronization, or unpredictable behavior may occur. For example, in a future release, synchronization may fail.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Optional](Optional.md)\<T\> | [empty](Optional.md))`()` Returns an empty`Optional`instance. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](Optional.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this`Optional`. |
| [Optional](Optional.md)\<T\>! | [filter](Optional.md))`(`predicate:` ` [Predicate](../java.util.function/Predicate.md)<in` `T>!`)` If a value is present, and the value matches the given predicate, returns an`Optional`describing the value, otherwise returns an empty`Optional`. |
| --- | --- |
| [Optional](Optional.md)\<U\>! | [flatMap](Optional.md))`(`mapper:` ` [Function](../java.util.function/Function.md)<in` `T,` `out` ` [Optional](Optional.md)<out` `U>!>!`)` If a value is present, returns the result of applying the given`Optional`-bearing mapping function to the value, otherwise returns an empty`Optional`. |
| T | [get](Optional.md))`()` If a value is present, returns the value, otherwise throws`NoSuchElementException`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](Optional.md))`()` Returns the hash code of the value, if present, otherwise`0`(zero) if no value is present. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ifPresent](Optional.md))`(`action:` ` [Consumer](../java.util.function/Consumer.md)<in` `T>`)` If a value is present, performs the given action with the value, otherwise does nothing. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ifPresentOrElse](Optional.md))`(`action:` ` [Consumer](../java.util.function/Consumer.md)<in` `T>!`, `emptyAction:` ` [Runnable](../java.lang/Runnable.md)!`)` If a value is present, performs the given action with the value, otherwise performs the given empty-based action. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](Optional.md))`()` If a value is not present, returns`true`, otherwise`false`. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPresent](Optional.md))`()` If a value is present, returns`true`, otherwise`false`. |
| [Optional](Optional.md)\<U\>! | [map](Optional.md))`(`mapper:` ` [Function](../java.util.function/Function.md)<in` `T,` `out` `U>!`)` If a value is present, returns an`Optional`describing (as if by [ofNullable](Optional.md))) the result of applying the given mapping function to the value, otherwise returns an empty`Optional`. |
| static [Optional](Optional.md)\<T\> | [of](Optional.md))`(`value:` `T`)` Returns an`Optional`describing the given non-`null`value. |
| --- | --- |
| static [Optional](Optional.md)\<T\> | [ofNullable](Optional.md))`(`value:` `T?`)` Returns an`Optional`describing the given value, if non-`null`, otherwise returns an empty`Optional`. |
| [Optional](Optional.md)\<T\>! | [or](Optional.md))`(`supplier:` ` [Supplier](../java.util.function/Supplier.md)<out` ` [Optional](Optional.md)<out` `T>!>!`)` If a value is present, returns an`Optional`describing the value, otherwise returns an`Optional`produced by the supplying function. |
| T | [orElse](Optional.md))`(`other:` `T`)` If a value is present, returns the value, otherwise returns`other`. |
| --- | --- |
| T | [orElseGet](Optional.md))`(`supplier:` ` [Supplier](../java.util.function/Supplier.md)<out` `T>!`)` If a value is present, returns the value, otherwise returns the result produced by the supplying function. |
| T | [orElseThrow](Optional.md))`()` If a value is present, returns the value, otherwise throws`NoSuchElementException`. |
| T | [orElseThrow](Optional.md))`(`exceptionSupplier:` ` [Supplier](../java.util.function/Supplier.md)<out` `X>!`)` If a value is present, returns the value, otherwise throws an exception produced by the exception supplying function. |
| --- | --- |
| [Stream](../java.util.stream/Stream.md)\<T\>! | [stream](Optional.md))`()` If a value is present, returns a sequential [Stream](../java.util.stream/Stream.md) containing only that value, otherwise returns an empty`Stream`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Optional.md))`()` Returns a non-empty string representation of this`Optional`suitable for debugging. |

## Public methods

### empty

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> empty(): Optional<T>
```

Returns an empty`Optional`instance. No value is present for this`Optional`.

| Parameters ||
|-------|------------------------------------|
| `<T>` | The type of the non-existent value |

| Return ||
|-----------------------------------------------------------------------------------|--------------------|
| [Optional](Optional.md)<T> | an empty`Optional` |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this`Optional`. The other object is considered equal if:

- it is also an`Optional`and;
- both instances have no value present or;
- the present values are "equal to" each other via`equals()`.

<br />

| Parameters ||
|-------|-------------------------------------|
| `obj` | an object to be tested for equality |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the other object is "equal to" this object otherwise`false` |

### filter

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun filter(predicate: Predicate<in T>!): Optional<T>!
```

If a value is present, and the value matches the given predicate, returns an`Optional`describing the value, otherwise returns an empty`Optional`.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `predicate` | [Predicate](../java.util.function/Predicate.md)\<inT\>!:the predicate to apply to a value, if present |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Optional](Optional.md)<T>! | an`Optional`describing the value of this`Optional`, if a value is present and the value matches the given predicate, otherwise an empty`Optional` |

| Exceptions ||
|----------------------------------|---------------------------|
| `java.lang.NullPointerException` | if the predicate is`null` |

### flatMap

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <U : Any!> flatMap(mapper: Function<in T, out Optional<out U>!>!): Optional<U>!
```

If a value is present, returns the result of applying the given`Optional`-bearing mapping function to the value, otherwise returns an empty`Optional`.

This method is similar to [map(java.util.function.Function)](Optional.md)), but the mapping function is one whose result is already an`Optional`, and if invoked,`flatMap`does not wrap it within an additional`Optional`.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<U>` | The type of value of the`Optional`returned by the mapping function |
| `mapper` | [Function](../java.util.function/Function.md)\<inT,out [Optional](Optional.md)\<outU\>!\>!:the mapping function to apply to a value, if present |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Optional](Optional.md)<U>! | the result of applying an`Optional`-bearing mapping function to the value of this`Optional`, if a value is present, otherwise an empty`Optional` |

| Exceptions ||
|----------------------------------|----------------------------------------------------------|
| `java.lang.NullPointerException` | if the mapping function is`null`or returns a`null`result |

### get

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(): T
```

If a value is present, returns the value, otherwise throws`NoSuchElementException`.

| Return ||
|---|-------------------------------------------------|
| T | the non-`null`value described by this`Optional` |

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
fun ifPresent(action: Consumer<in T>): Unit
```

If a value is present, performs the given action with the value, otherwise does nothing.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [Consumer](../java.util.function/Consumer.md)\<inT\>:the action to be performed, if a value is present |

| Exceptions ||
|----------------------------------|---------------------------------------------------|
| `java.lang.NullPointerException` | if value is present and the given action is`null` |

### ifPresentOrElse

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun ifPresentOrElse(
    action: Consumer<in T>!, 
    emptyAction: Runnable!
): Unit
```

If a value is present, performs the given action with the value, otherwise performs the given empty-based action.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [Consumer](../java.util.function/Consumer.md)\<inT\>!:the action to be performed, if a value is present |
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

### map

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <U : Any!> map(mapper: Function<in T, out U>!): Optional<U>!
```

If a value is present, returns an`Optional`describing (as if by [ofNullable](Optional.md))) the result of applying the given mapping function to the value, otherwise returns an empty`Optional`.

If the mapping function returns a`null`result then this method returns an empty`Optional`.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [Function](../java.util.function/Function.md)\<inT,outU\>!:the mapping function to apply to a value, if present |
| `<U>` | The type of the value returned from the mapping function |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Optional](Optional.md)<U>! | an`Optional`describing the result of applying a mapping function to the value of this`Optional`, if a value is present, otherwise an empty`Optional` |

| Exceptions ||
|----------------------------------|----------------------------------|
| `java.lang.NullPointerException` | if the mapping function is`null` |

### of

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> of(value: T): Optional<T>
```

Returns an`Optional`describing the given non-`null`value.

| Parameters ||
|---------|---------------------------------------------------|
| `value` | T:the value to describe, which must be non-`null` |
| `<T>` | the type of the value |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------|
| [Optional](Optional.md)<T> | an`Optional`with the value present |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if value is`null` |

### ofNullable

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> ofNullable(value: T?): Optional<T>
```

Returns an`Optional`describing the given value, if non-`null`, otherwise returns an empty`Optional`.

| Parameters ||
|---------|-----------------------------------------|
| `value` | T?:the possibly-`null`value to describe |
| `<T>` | the type of the value |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Optional](Optional.md)<T> | an`Optional`with a present value if the specified value is non-`null`, otherwise an empty`Optional` |

### or

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun or(supplier: Supplier<out Optional<out T>!>!): Optional<T>!
```

If a value is present, returns an`Optional`describing the value, otherwise returns an`Optional`produced by the supplying function.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `supplier` | [Supplier](../java.util.function/Supplier.md)\<out [Optional](Optional.md)\<outT\>!\>!:the supplying function that produces an`Optional`to be returned |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Optional](Optional.md)<T>! | returns an`Optional`describing the value of this`Optional`, if a value is present, otherwise an`Optional`produced by the supplying function. |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------|
| `java.lang.NullPointerException` | if the supplying function is`null`or produces a`null`result |

### orElse

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun orElse(other: T): T
```

If a value is present, returns the value, otherwise returns`other`.

| Parameters ||
|---------|-------------------------------------------------------------------|
| `other` | T:the value to be returned, if no value is present. May be`null`. |

| Return ||
|---|-----------------------------------------|
| T | the value, if present, otherwise`other` |

### orElseGet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun orElseGet(supplier: Supplier<out T>!): T
```

If a value is present, returns the value, otherwise returns the result produced by the supplying function.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `supplier` | [Supplier](../java.util.function/Supplier.md)\<outT\>!:the supplying function that produces a value to be returned |

| Return ||
|---|--------------------------------------------------------------------------------|
| T | the value, if present, otherwise the result produced by the supplying function |

| Exceptions ||
|----------------------------------|------------------------------------------------------------|
| `java.lang.NullPointerException` | if no value is present and the supplying function is`null` |

### orElseThrow

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun orElseThrow(): T
```

If a value is present, returns the value, otherwise throws`NoSuchElementException`.

| Return ||
|---|-------------------------------------------------|
| T | the non-`null`value described by this`Optional` |

| Exceptions ||
|------------------------------------|------------------------|
| `java.util.NoSuchElementException` | if no value is present |

### orElseThrow

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <X : Throwable!> orElseThrow(exceptionSupplier: Supplier<out X>!): T
```

If a value is present, returns the value, otherwise throws an exception produced by the exception supplying function.

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<X>` | Type of the exception to be thrown |
| `exceptionSupplier` | [Supplier](../java.util.function/Supplier.md)\<outX\>!:the supplying function that produces an exception to be thrown |

| Return ||
|---|-----------------------|
| T | the value, if present |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------------|
| `X` | if no value is present |
| `java.lang.NullPointerException` | if no value is present and the exception supplying function is`null` |

### stream

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun stream(): Stream<T>!
```

If a value is present, returns a sequential [Stream](../java.util.stream/Stream.md) containing only that value, otherwise returns an empty`Stream`.

| Return ||
|--------------------------------------------------------------------------------------|---------------------------------|
| [Stream](../java.util.stream/Stream.md)<T>! | the optional value as a`Stream` |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a non-empty string representation of this`Optional`suitable for debugging. The exact presentation format is unspecified and may vary between implementations and versions.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the string representation of this instance |
