# Consumer

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Consumer

```
@FunctionalInterface interface Consumer<T : Any!>
```

| [java.util.function.Consumer](../java/util/function/Consumer.md) |

| Known Direct Subclasses [Stream.Builder](../java/util/stream/Stream.Builder.md) |--------------------------------------------------------------------------------------------------------|-----------------------------------| | [Stream.Builder](../java/util/stream/Stream.Builder.md) | A mutable builder for a `Stream`. | |
| --- | --- | --- | --- | --- | --- | --- |

Represents an operation that accepts a single input argument and returns no result. Unlike most other functional interfaces, `Consumer` is expected to operate via side-effects.

This is a [functional interface](../java/util/function/_package.md) whose functional method is [accept(java.lang.Object)](../java/util/function/Consumer.md)).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [accept](../java/util/function/Consumer.md))`(`t:` `T`)` Performs this operation on the given argument. |
| open [Consumer](../java/util/function/Consumer.md)\<T\>! | [andThen](../java/util/function/Consumer.md))`(`after:` ` [Consumer](../java/util/function/Consumer.md)<in` `T>!`)` Returns a composed `Consumer` that performs, in sequence, this operation followed by the `after` operation. |

## Public methods

### accept

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun accept(t: T): Unit
```

Performs this operation on the given argument.

| Parameters ||
|-----|-----------------------|
| `t` | T: the input argument |

### andThen

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun andThen(after: Consumer<in T>!): Consumer<T>!
```

Returns a composed `Consumer` that performs, in sequence, this operation followed by the `after` operation. If performing either operation throws an exception, it is relayed to the caller of the composed operation. If performing this operation throws an exception, the `after` operation will not be performed.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `after` | [Consumer](../java/util/function/Consumer.md)\<in T\>!: the operation to perform after this operation |

| Return ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Consumer](../java/util/function/Consumer.md)<T>! | a composed `Consumer` that performs in sequence this operation followed by the `after` operation |

| Exceptions ||
|----------------------------------|--------------------|
| `java.lang.NullPointerException` | if `after` is null |
