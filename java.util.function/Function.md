# Function

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Function

```
@FunctionalInterface interface Function<T : Any!, R : Any!>
```

| [java.util.function.Function](Function.md) |

| Known Direct Subclasses [UnaryOperator](UnaryOperator.md) |--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------| | [UnaryOperator](UnaryOperator.md) | Represents an operation on a single operand that produces a result of the same type as its operand. | |
| --- | --- | --- | --- | --- | --- | --- |

Represents a function that accepts one argument and produces a result.

This is a [functional interface](_package.md) whose functional method is [apply(java.lang.Object)](Function.md)).

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Function](Function.md)\<T,V\>! | [andThen](Function.md))`(`after:` ` [Function](Function.md)<in` `R,` `out` `V>!`)` Returns a composed function that first applies this function to its input, and then applies the`after`function to the result. |
| abstractR | [apply](Function.md))`(`t:` `T`)` Applies this function to the given argument. |
| open [Function](Function.md)\<V,R\>! | [compose](Function.md))`(`before:` ` [Function](Function.md)<in` `V,` `out` `T>!`)` Returns a composed function that first applies the`before`function to its input, and then applies this function to the result. |
| --- | --- |
| openstatic [Function](Function.md)\<T,T\>! | [identity](Function.md))`()` Returns a function that always returns its input argument. |

## Public methods

### andThen

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <V : Any!> andThen(after: Function<in R, out V>!): Function<T, V>!
```

Returns a composed function that first applies this function to its input, and then applies the`after`function to the result. If evaluation of either function throws an exception, it is relayed to the caller of the composed function.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<V>` | the type of output of the`after`function, and of the composed function |
| `after` | [Function](Function.md)\<inR,outV\>!:the function to apply after this function is applied |

| Return ||
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Function](Function.md)<T,` `V>! | a composed function that first applies this function and then applies the`after`function |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if after is null |

**See Also**

- [#compose(Function)](Function.md)) 

### apply

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun apply(t: T): R
```

Applies this function to the given argument.

| Parameters ||
|-----|-------------------------|
| `t` | T:the function argument |

| Return ||
|---|---------------------|
| R | the function result |

### compose

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <V : Any!> compose(before: Function<in V, out T>!): Function<V, R>!
```

Returns a composed function that first applies the`before`function to its input, and then applies this function to the result. If evaluation of either function throws an exception, it is relayed to the caller of the composed function.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<V>` | the type of input to the`before`function, and to the composed function |
| `before` | [Function](Function.md)\<inV,outT\>!:the function to apply before this function is applied |

| Return ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Function](Function.md)<V,` `R>! | a composed function that first applies the`before`function and then applies this function |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if before is null |

**See Also**

- [#andThen(Function)](Function.md)) 

### identity

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> identity(): Function<T, T>!
```

Returns a function that always returns its input argument.

| Parameters ||
|-------|----------------------------------------------------------|
| `<T>` | the type of the input and output objects to the function |

| Return ||
|--------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [Function](Function.md)<T,` `T>! | a function that always returns its input argument |
