# Optional

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Optional

```
class Optional<T : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.util.Optional](https://developer.android.com/reference/kotlin/java/util/Optional#) |

A container object which may or may not contain a non-`null`value. If a value is present,`isPresent()`returns`true`. If no value is present, the object is considered*empty* and`isPresent()`returns`false`.

Additional methods that depend on the presence or absence of a contained value are provided, such as [orElse()](https://developer.android.com/reference/kotlin/java/util/Optional#orElse(java.util.Optional.T))(returns a default value if no value is present) and [ifPresent()](https://developer.android.com/reference/kotlin/java/util/Optional#ifPresent(java.util.function.Consumer))(performs an action if a value is present).

This is a [value-based](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/doc-files/ValueBased.html) class; programmers should treat instances that are [equal](https://developer.android.com/reference/kotlin/java/util/Optional#equals(kotlin.Any))as interchangeable and should not use instances for synchronization, or unpredictable behavior may occur. For example, in a future release, synchronization may fail.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Optional](https://developer.android.com/reference/kotlin/java/util/Optional#)\<T\> | [empty](https://developer.android.com/reference/kotlin/java/util/Optional#empty())`()` Returns an empty`Optional`instance. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/util/Optional#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this`Optional`. |
| [Optional](https://developer.android.com/reference/kotlin/java/util/Optional#)\<T\>! | [filter](https://developer.android.com/reference/kotlin/java/util/Optional#filter(java.util.function.Predicate))`(`predicate:` ` [Predicate](https://developer.android.com/reference/kotlin/java/util/function/Predicate)<in` `T>!`)` If a value is present, and the value matches the given predicate, returns an`Optional`describing the value, otherwise returns an empty`Optional`. |
| [Optional](https://developer.android.com/reference/kotlin/java/util/Optional#)\<U\>! | [flatMap](https://developer.android.com/reference/kotlin/java/util/Optional#flatMap(java.util.function.Function))`(`mapper:` ` [Function](https://developer.android.com/reference/kotlin/java/util/function/Function)<in` `T,` `out` ` [Optional](https://developer.android.com/reference/kotlin/java/util/Optional#)<out` `U>!>!`)` If a value is present, returns the result of applying the given`Optional`-bearing mapping function to the value, otherwise returns an empty`Optional`. |
| T | [get](https://developer.android.com/reference/kotlin/java/util/Optional#get())`()` If a value is present, returns the value, otherwise throws`NoSuchElementException`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/util/Optional#hashCode())`()` Returns the hash code of the value, if present, otherwise`0`(zero) if no value is present. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ifPresent](https://developer.android.com/reference/kotlin/java/util/Optional#ifPresent(java.util.function.Consumer))`(`action:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer)<in` `T>`)` If a value is present, performs the given action with the value, otherwise does nothing. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ifPresentOrElse](https://developer.android.com/reference/kotlin/java/util/Optional#ifPresentOrElse(java.util.function.Consumer,%20java.lang.Runnable))`(`action:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer)<in` `T>!`, `emptyAction:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` If a value is present, performs the given action with the value, otherwise performs the given empty-based action. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/java/util/Optional#isEmpty())`()` If a value is not present, returns`true`, otherwise`false`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPresent](https://developer.android.com/reference/kotlin/java/util/Optional#isPresent())`()` If a value is present, returns`true`, otherwise`false`. |
| [Optional](https://developer.android.com/reference/kotlin/java/util/Optional#)\<U\>! | [map](https://developer.android.com/reference/kotlin/java/util/Optional#map(java.util.function.Function))`(`mapper:` ` [Function](https://developer.android.com/reference/kotlin/java/util/function/Function)<in` `T,` `out` `U>!`)` If a value is present, returns an`Optional`describing (as if by [ofNullable](https://developer.android.com/reference/kotlin/java/util/Optional#ofNullable(java.util.Optional.ofNullable.T))) the result of applying the given mapping function to the value, otherwise returns an empty`Optional`. |
| static [Optional](https://developer.android.com/reference/kotlin/java/util/Optional#)\<T\> | [of](https://developer.android.com/reference/kotlin/java/util/Optional#of(java.util.Optional.of.T))`(`value:` `T`)` Returns an`Optional`describing the given non-`null`value. |
| static [Optional](https://developer.android.com/reference/kotlin/java/util/Optional#)\<T\> | [ofNullable](https://developer.android.com/reference/kotlin/java/util/Optional#ofNullable(java.util.Optional.ofNullable.T))`(`value:` `T?`)` Returns an`Optional`describing the given value, if non-`null`, otherwise returns an empty`Optional`. |
| [Optional](https://developer.android.com/reference/kotlin/java/util/Optional#)\<T\>! | [or](https://developer.android.com/reference/kotlin/java/util/Optional#or(java.util.function.Supplier))`(`supplier:` ` [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier)<out` ` [Optional](https://developer.android.com/reference/kotlin/java/util/Optional#)<out` `T>!>!`)` If a value is present, returns an`Optional`describing the value, otherwise returns an`Optional`produced by the supplying function. |
| T | [orElse](https://developer.android.com/reference/kotlin/java/util/Optional#orElse(java.util.Optional.T))`(`other:` `T`)` If a value is present, returns the value, otherwise returns`other`. |
| T | [orElseGet](https://developer.android.com/reference/kotlin/java/util/Optional#orElseGet(java.util.function.Supplier))`(`supplier:` ` [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier)<out` `T>!`)` If a value is present, returns the value, otherwise returns the result produced by the supplying function. |
| T | [orElseThrow](https://developer.android.com/reference/kotlin/java/util/Optional#orElseThrow())`()` If a value is present, returns the value, otherwise throws`NoSuchElementException`. |
| T | [orElseThrow](https://developer.android.com/reference/kotlin/java/util/Optional#orElseThrow(java.util.function.Supplier))`(`exceptionSupplier:` ` [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier)<out` `X>!`)` If a value is present, returns the value, otherwise throws an exception produced by the exception supplying function. |
| [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream)\<T\>! | [stream](https://developer.android.com/reference/kotlin/java/util/Optional#stream())`()` If a value is present, returns a sequential [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream) containing only that value, otherwise returns an empty`Stream`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/Optional#toString())`()` Returns a non-empty string representation of this`Optional`suitable for debugging. |

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
| [Optional](https://developer.android.com/reference/kotlin/java/util/Optional#)<T> | an empty`Optional` |

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
| `predicate` | [Predicate](https://developer.android.com/reference/kotlin/java/util/function/Predicate)\<inT\>!:the predicate to apply to a value, if present |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Optional](https://developer.android.com/reference/kotlin/java/util/Optional#)<T>! | an`Optional`describing the value of this`Optional`, if a value is present and the value matches the given predicate, otherwise an empty`Optional` |

| Exceptions ||
|----------------------------------|---------------------------|
| `java.lang.NullPointerException` | if the predicate is`null` |

### flatMap

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <U : Any!> flatMap(mapper: Function<in T, out Optional<out U>!>!): Optional<U>!
```

If a value is present, returns the result of applying the given`Optional`-bearing mapping function to the value, otherwise returns an empty`Optional`.

This method is similar to [map(java.util.function.Function)](https://developer.android.com/reference/kotlin/java/util/Optional#map(java.util.function.Function)), but the mapping function is one whose result is already an`Optional`, and if invoked,`flatMap`does not wrap it within an additional`Optional`.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<U>` | The type of value of the`Optional`returned by the mapping function |
| `mapper` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function)\<inT,out [Optional](https://developer.android.com/reference/kotlin/java/util/Optional#)\<outU\>!\>!:the mapping function to apply to a value, if present |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Optional](https://developer.android.com/reference/kotlin/java/util/Optional#)<U>! | the result of applying an`Optional`-bearing mapping function to the value of this`Optional`, if a value is present, otherwise an empty`Optional` |

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
| `action` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer)\<inT\>:the action to be performed, if a value is present |

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
| `action` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer)\<inT\>!:the action to be performed, if a value is present |
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

### map

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <U : Any!> map(mapper: Function<in T, out U>!): Optional<U>!
```

If a value is present, returns an`Optional`describing (as if by [ofNullable](https://developer.android.com/reference/kotlin/java/util/Optional#ofNullable(java.util.Optional.ofNullable.T))) the result of applying the given mapping function to the value, otherwise returns an empty`Optional`.

If the mapping function returns a`null`result then this method returns an empty`Optional`.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mapper` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function)\<inT,outU\>!:the mapping function to apply to a value, if present |
| `<U>` | The type of the value returned from the mapping function |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Optional](https://developer.android.com/reference/kotlin/java/util/Optional#)<U>! | an`Optional`describing the result of applying a mapping function to the value of this`Optional`, if a value is present, otherwise an empty`Optional` |

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
| [Optional](https://developer.android.com/reference/kotlin/java/util/Optional#)<T> | an`Optional`with the value present |

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
| [Optional](https://developer.android.com/reference/kotlin/java/util/Optional#)<T> | an`Optional`with a present value if the specified value is non-`null`, otherwise an empty`Optional` |

### or

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun or(supplier: Supplier<out Optional<out T>!>!): Optional<T>!
```

If a value is present, returns an`Optional`describing the value, otherwise returns an`Optional`produced by the supplying function.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `supplier` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier)\<out [Optional](https://developer.android.com/reference/kotlin/java/util/Optional#)\<outT\>!\>!:the supplying function that produces an`Optional`to be returned |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Optional](https://developer.android.com/reference/kotlin/java/util/Optional#)<T>! | returns an`Optional`describing the value of this`Optional`, if a value is present, otherwise an`Optional`produced by the supplying function. |

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
| `supplier` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier)\<outT\>!:the supplying function that produces a value to be returned |

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
| `exceptionSupplier` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier)\<outX\>!:the supplying function that produces an exception to be thrown |

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

If a value is present, returns a sequential [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream) containing only that value, otherwise returns an empty`Stream`.

| Return ||
|--------------------------------------------------------------------------------------|---------------------------------|
| [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream)<T>! | the optional value as a`Stream` |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a non-empty string representation of this`Optional`suitable for debugging. The exact presentation format is unspecified and may vary between implementations and versions.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the string representation of this instance |
