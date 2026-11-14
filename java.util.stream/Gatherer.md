# Gatherer

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Gatherer

```
interface Gatherer<T : Any!, A : Any!, R : Any!>
```

| [java.util.stream.Gatherer](Gatherer.md) |

An intermediate operation that transforms a stream of input elements into a stream of output elements, optionally applying a final action when the end of the upstream is reached. The transformation may be stateless or stateful, and may buffer input before producing any output.

Gatherer operations can be performed either sequentially, or be parallelized -- if a combiner function is supplied.

There are many examples of gathering operations, including but not limited to: grouping elements into batches (windowing functions); de-duplicating consecutively similar elements; incremental accumulation functions (prefix scan); incremental reordering functions, etc. The class [java.util.stream.Gatherers](Gatherers.md) provides implementations of common gathering operations.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Downstream](../java/util/stream/Gatherer.Downstream.md) A Downstream object is the next stage in a pipeline of operations, to which elements can be sent. |
| abstract | [Integrator](../java/util/stream/Gatherer.Integrator.md) An Integrator receives elements and processes them, optionally using the supplied state, and optionally sends incremental results downstream. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Gatherer](Gatherer.md)\<T,\*,RR\>! | [andThen](Gatherer.md))`(`that:` ` [Gatherer](Gatherer.md)<in` `R,` `*,` `out` `RR>!`)` Returns a composed Gatherer which connects the output of this Gatherer to the input of that Gatherer. |
| open [BinaryOperator](../java.util.function/BinaryOperator.md)\<A\>! | [combiner](Gatherer.md))`()` A function which accepts two intermediate states and combines them into one. |
| openstatic [BinaryOperator](../java.util.function/BinaryOperator.md)\<A\>! | [defaultCombiner](Gatherer.md))`()` Returns a combiner which is the default combiner of a Gatherer. |
| --- | --- |
| openstatic [BiConsumer](../java.util.function/BiConsumer.md)\<A, [Gatherer.Downstream](../java/util/stream/Gatherer.Downstream.md)\<inR\>!\>! | [defaultFinisher](Gatherer.md))`()` Returns a`finisher`which is the default finisher of a`Gatherer`. |
| openstatic [Supplier](../java.util.function/Supplier.md)\<A\>! | [defaultInitializer](Gatherer.md))`()` Returns an initializer which is the default initializer of a Gatherer. |
| open [BiConsumer](../java.util.function/BiConsumer.md)\<A, [Gatherer.Downstream](../java/util/stream/Gatherer.Downstream.md)\<inR\>!\>! | [finisher](Gatherer.md))`()` A function which accepts the final intermediate state and a [Downstream](../java/util/stream/Gatherer.Downstream.md) object, allowing to perform a final action at the end of input elements. |
| --- | --- |
| open [Supplier](../java.util.function/Supplier.md)\<A\>! | [initializer](Gatherer.md))`()` A function that produces an instance of the intermediate state used for this gathering operation. |
| abstract [Gatherer.Integrator](../java/util/stream/Gatherer.Integrator.md)\<A,T,R\>! | [integrator](Gatherer.md))`()` A function which integrates provided elements, potentially using the provided intermediate state, optionally producing output to the provided [Downstream](../java/util/stream/Gatherer.Downstream.md). |
| openstatic [Gatherer](Gatherer.md)\<T,A,R\>! | [of](Gatherer.md))`(`initializer:` ` [Supplier](../java.util.function/Supplier.md)<A>!`, `integrator:` ` [Gatherer.Integrator](../java/util/stream/Gatherer.Integrator.md)<A,` `T,` `R>!`, `combiner:` ` [BinaryOperator](../java.util.function/BinaryOperator.md)<A>!`, `finisher:` ` [BiConsumer](../java.util.function/BiConsumer.md)<A,` ` [Gatherer.Downstream](../java/util/stream/Gatherer.Downstream.md)<in` `R>!>!`)` Returns a new, parallelizable,`Gatherer`described by the given`initializer`,`integrator`,`combiner`and`finisher`. |
| --- | --- |
| openstatic [Gatherer](Gatherer.md)\<T, [Void](../java.lang/Void.md)!,R\>! | [of](Gatherer.md))`(`integrator:` ` [Gatherer.Integrator](../java/util/stream/Gatherer.Integrator.md)< [Void](../java.lang/Void.md)!,` `T,` `R>!`)` Returns a new, parallelizable, and stateless`Gatherer`described by the given`integrator`. |
| openstatic [Gatherer](Gatherer.md)\<T, [Void](../java.lang/Void.md)!,R\>! | [of](Gatherer.md))`(`integrator:` ` [Gatherer.Integrator](../java/util/stream/Gatherer.Integrator.md)< [Void](../java.lang/Void.md)!,` `T,` `R>!`, `finisher:` ` [BiConsumer](../java.util.function/BiConsumer.md)< [Void](../java.lang/Void.md)!,` ` [Gatherer.Downstream](../java/util/stream/Gatherer.Downstream.md)<in` `R>!>!`)` Returns a new, parallelizable, and stateless`Gatherer`described by the given`integrator`and`finisher`. |
| openstatic [Gatherer](Gatherer.md)\<T,A,R\>! | [ofSequential](Gatherer.md))`(`initializer:` ` [Supplier](../java.util.function/Supplier.md)<A>!`, `integrator:` ` [Gatherer.Integrator](../java/util/stream/Gatherer.Integrator.md)<A,` `T,` `R>!`)` Returns a new, sequential,`Gatherer`described by the given`initializer`and`integrator`. |
| --- | --- |
| openstatic [Gatherer](Gatherer.md)\<T,A,R\>! | [ofSequential](Gatherer.md))`(`initializer:` ` [Supplier](../java.util.function/Supplier.md)<A>!`, `integrator:` ` [Gatherer.Integrator](../java/util/stream/Gatherer.Integrator.md)<A,` `T,` `R>!`, `finisher:` ` [BiConsumer](../java.util.function/BiConsumer.md)<A,` ` [Gatherer.Downstream](../java/util/stream/Gatherer.Downstream.md)<in` `R>!>!`)` Returns a new, sequential,`Gatherer`described by the given`initializer`,`integrator`, and`finisher`. |
| openstatic [Gatherer](Gatherer.md)\<T, [Void](../java.lang/Void.md)!,R\>! | [ofSequential](Gatherer.md))`(`integrator:` ` [Gatherer.Integrator](../java/util/stream/Gatherer.Integrator.md)< [Void](../java.lang/Void.md)!,` `T,` `R>!`)` Returns a new, sequential, and stateless`Gatherer`described by the given`integrator`. |
| openstatic [Gatherer](Gatherer.md)\<T, [Void](../java.lang/Void.md)!,R\>! | [ofSequential](Gatherer.md))`(`integrator:` ` [Gatherer.Integrator](../java/util/stream/Gatherer.Integrator.md)< [Void](../java.lang/Void.md)!,` `T,` `R>!`, `finisher:` ` [BiConsumer](../java.util.function/BiConsumer.md)< [Void](../java.lang/Void.md)!,` ` [Gatherer.Downstream](../java/util/stream/Gatherer.Downstream.md)<in` `R>!>!`)` Returns a new, sequential, and stateless`Gatherer`described by the given`integrator`and`finisher`. |
| --- | --- |

## Public methods

### andThen

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <RR : Any!> andThen(that: Gatherer<in R, *, out RR>!): Gatherer<T, *, RR>!
```

Returns a composed Gatherer which connects the output of this Gatherer to the input of that Gatherer.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------|
| `that` | [Gatherer](Gatherer.md)\<inR,\*,outRR\>!:the other gatherer |
| `<RR>` | The type of output of that Gatherer |

| Return ||
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Gatherer](Gatherer.md)<T,` `*,` `RR>! | returns a composed Gatherer which connects the output of this Gatherer as input that Gatherer |

| Exceptions ||
|----------------------------------|--------------------------|
| `java.lang.NullPointerException` | if the argument is`null` |

### combiner

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun combiner(): BinaryOperator<A>!
```

A function which accepts two intermediate states and combines them into one.

| Return ||
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [BinaryOperator](../java.util.function/BinaryOperator.md)<A>! | a function which accepts two intermediate states and combines them into one |

### defaultCombiner

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <A : Any!> defaultCombiner(): BinaryOperator<A>!
```

Returns a combiner which is the default combiner of a Gatherer. The returned combiner identifies that the owning Gatherer must only be evaluated sequentially.

| Parameters ||
|-------|------------------------------------------------|
| `<A>` | the type of the state of the returned combiner |

| Return ||
|--------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [BinaryOperator](../java.util.function/BinaryOperator.md)<A>! | the instance of the default combiner |

**See Also**

- [java.util.stream.Gatherer#combiner()](Gatherer.md)) 

### defaultFinisher

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <A : Any!, R : Any!> defaultFinisher(): BiConsumer<A, Gatherer.Downstream<in R>!>!
```

Returns a`finisher`which is the default finisher of a`Gatherer`. The returned finisher identifies that the owning Gatherer performs no additional actions at the end of input.

| Parameters ||
|-------|-----------------------------------------------------|
| `<A>` | the type of the state of the returned finisher |
| `<R>` | the type of the Downstream of the returned finisher |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [BiConsumer](../java.util.function/BiConsumer.md)<A,` ` [Gatherer.Downstream](../java/util/stream/Gatherer.Downstream.md)<in` `R>!>! | the instance of the default finisher |

**See Also**

- [java.util.stream.Gatherer#finisher()](Gatherer.md)) 

### defaultInitializer

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <A : Any!> defaultInitializer(): Supplier<A>!
```

Returns an initializer which is the default initializer of a Gatherer. The returned initializer identifies that the owner Gatherer is stateless.

| Parameters ||
|-------|---------------------------------------------------|
| `<A>` | the type of the state of the returned initializer |

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------------------|
| [Supplier](../java.util.function/Supplier.md)<A>! | the instance of the default initializer |

**See Also**

- [java.util.stream.Gatherer#initializer()](Gatherer.md)) 

### finisher

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun finisher(): BiConsumer<A, Gatherer.Downstream<in R>!>!
```

A function which accepts the final intermediate state and a [Downstream](../java/util/stream/Gatherer.Downstream.md) object, allowing to perform a final action at the end of input elements.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [BiConsumer](../java.util.function/BiConsumer.md)<A,` ` [Gatherer.Downstream](../java/util/stream/Gatherer.Downstream.md)<in` `R>!>! | a function which transforms the intermediate result to the final result(s) which are then passed on to the provided Downstream |

### initializer

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun initializer(): Supplier<A>!
```

A function that produces an instance of the intermediate state used for this gathering operation.

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Supplier](../java.util.function/Supplier.md)<A>! | A function that produces an instance of the intermediate state used for this gathering operation |

### integrator

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun integrator(): Gatherer.Integrator<A, T, R>!
```

A function which integrates provided elements, potentially using the provided intermediate state, optionally producing output to the provided [Downstream](../java/util/stream/Gatherer.Downstream.md).

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Gatherer.Integrator](../java/util/stream/Gatherer.Integrator.md)<A,` `T,` `R>! | a function which integrates provided elements, potentially using the provided state, optionally producing output to the provided Downstream |

### of

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!, A : Any!, R : Any!> of(
    initializer: Supplier<A>!, 
    integrator: Gatherer.Integrator<A, T, R>!, 
    combiner: BinaryOperator<A>!, 
    finisher: BiConsumer<A, Gatherer.Downstream<in R>!>!
): Gatherer<T, A, R>!
```

Returns a new, parallelizable,`Gatherer`described by the given`initializer`,`integrator`,`combiner`and`finisher`.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `initializer` | [Supplier](../java.util.function/Supplier.md)\<A\>!:the initializer function for the new gatherer |
| `integrator` | [Gatherer.Integrator](../java/util/stream/Gatherer.Integrator.md)\<A,T,R\>!:the integrator function for the new gatherer |
| `combiner` | [BinaryOperator](../java.util.function/BinaryOperator.md)\<A\>!:the combiner function for the new gatherer |
| --- | --- |
| `finisher` | [BiConsumer](../java.util.function/BiConsumer.md)\<A, [Gatherer.Downstream](../java/util/stream/Gatherer.Downstream.md)\<inR\>!\>!:the finisher function for the new gatherer |
| `<T>` | the type of input elements for the new gatherer |
| `<A>` | the type of state for the new gatherer |
| --- | --- |
| `<R>` | the type of results for the new gatherer |

| Return ||
|-----------------------------------------------------------------------------------------------------|-------------------|
| [Gatherer](Gatherer.md)<T,` `A,` `R>! | the new`Gatherer` |

| Exceptions ||
|----------------------------------|--------------------------|
| `java.lang.NullPointerException` | if any argument is`null` |

### of

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!, R : Any!> of(integrator: Gatherer.Integrator<Void!, T, R>!): Gatherer<T, Void!, R>!
```

Returns a new, parallelizable, and stateless`Gatherer`described by the given`integrator`.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `integrator` | [Gatherer.Integrator](../java/util/stream/Gatherer.Integrator.md)\< [Void](../java.lang/Void.md)!,T,R\>!:the integrator function for the new gatherer |
| `<T>` | the type of input elements for the new gatherer |
| `<R>` | the type of results for the new gatherer |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
| [Gatherer](Gatherer.md)<T,` ` [Void](../java.lang/Void.md)!,` `R>! | the new`Gatherer` |

| Exceptions ||
|----------------------------------|--------------------------|
| `java.lang.NullPointerException` | if any argument is`null` |

### of

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!, R : Any!> of(
    integrator: Gatherer.Integrator<Void!, T, R>!, 
    finisher: BiConsumer<Void!, Gatherer.Downstream<in R>!>!
): Gatherer<T, Void!, R>!
```

Returns a new, parallelizable, and stateless`Gatherer`described by the given`integrator`and`finisher`.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `integrator` | [Gatherer.Integrator](../java/util/stream/Gatherer.Integrator.md)\< [Void](../java.lang/Void.md)!,T,R\>!:the integrator function for the new gatherer |
| `finisher` | [BiConsumer](../java.util.function/BiConsumer.md)\< [Void](../java.lang/Void.md)!, [Gatherer.Downstream](../java/util/stream/Gatherer.Downstream.md)\<inR\>!\>!:the finisher function for the new gatherer |
| `<T>` | the type of input elements for the new gatherer |
| --- | --- |
| `<R>` | the type of results for the new gatherer |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
| [Gatherer](Gatherer.md)<T,` ` [Void](../java.lang/Void.md)!,` `R>! | the new`Gatherer` |

| Exceptions ||
|----------------------------------|--------------------------|
| `java.lang.NullPointerException` | if any argument is`null` |

### ofSequential

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!, A : Any!, R : Any!> ofSequential(
    initializer: Supplier<A>!, 
    integrator: Gatherer.Integrator<A, T, R>!
): Gatherer<T, A, R>!
```

Returns a new, sequential,`Gatherer`described by the given`initializer`and`integrator`.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `initializer` | [Supplier](../java.util.function/Supplier.md)\<A\>!:the initializer function for the new gatherer |
| `integrator` | [Gatherer.Integrator](../java/util/stream/Gatherer.Integrator.md)\<A,T,R\>!:the integrator function for the new gatherer |
| `<T>` | the type of input elements for the new gatherer |
| --- | --- |
| `<A>` | the type of state for the new gatherer |
| `<R>` | the type of results for the new gatherer |

| Return ||
|-----------------------------------------------------------------------------------------------------|-------------------|
| [Gatherer](Gatherer.md)<T,` `A,` `R>! | the new`Gatherer` |

| Exceptions ||
|----------------------------------|--------------------------|
| `java.lang.NullPointerException` | if any argument is`null` |

### ofSequential

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!, A : Any!, R : Any!> ofSequential(
    initializer: Supplier<A>!, 
    integrator: Gatherer.Integrator<A, T, R>!, 
    finisher: BiConsumer<A, Gatherer.Downstream<in R>!>!
): Gatherer<T, A, R>!
```

Returns a new, sequential,`Gatherer`described by the given`initializer`,`integrator`, and`finisher`.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `initializer` | [Supplier](../java.util.function/Supplier.md)\<A\>!:the initializer function for the new gatherer |
| `integrator` | [Gatherer.Integrator](../java/util/stream/Gatherer.Integrator.md)\<A,T,R\>!:the integrator function for the new gatherer |
| `finisher` | [BiConsumer](../java.util.function/BiConsumer.md)\<A, [Gatherer.Downstream](../java/util/stream/Gatherer.Downstream.md)\<inR\>!\>!:the finisher function for the new gatherer |
| --- | --- |
| `<T>` | the type of input elements for the new gatherer |
| `<A>` | the type of state for the new gatherer |
| `<R>` | the type of results for the new gatherer |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------------|-------------------|
| [Gatherer](Gatherer.md)<T,` `A,` `R>! | the new`Gatherer` |

| Exceptions ||
|----------------------------------|--------------------------|
| `java.lang.NullPointerException` | if any argument is`null` |

### ofSequential

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!, R : Any!> ofSequential(integrator: Gatherer.Integrator<Void!, T, R>!): Gatherer<T, Void!, R>!
```

Returns a new, sequential, and stateless`Gatherer`described by the given`integrator`.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `integrator` | [Gatherer.Integrator](../java/util/stream/Gatherer.Integrator.md)\< [Void](../java.lang/Void.md)!,T,R\>!:the integrator function for the new gatherer |
| `<T>` | the type of input elements for the new gatherer |
| `<R>` | the type of results for the new gatherer |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
| [Gatherer](Gatherer.md)<T,` ` [Void](../java.lang/Void.md)!,` `R>! | the new`Gatherer` |

| Exceptions ||
|----------------------------------|--------------------------|
| `java.lang.NullPointerException` | if the argument is`null` |

### ofSequential

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!, R : Any!> ofSequential(
    integrator: Gatherer.Integrator<Void!, T, R>!, 
    finisher: BiConsumer<Void!, Gatherer.Downstream<in R>!>!
): Gatherer<T, Void!, R>!
```

Returns a new, sequential, and stateless`Gatherer`described by the given`integrator`and`finisher`.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `integrator` | [Gatherer.Integrator](../java/util/stream/Gatherer.Integrator.md)\< [Void](../java.lang/Void.md)!,T,R\>!:the integrator function for the new gatherer |
| `finisher` | [BiConsumer](../java.util.function/BiConsumer.md)\< [Void](../java.lang/Void.md)!, [Gatherer.Downstream](../java/util/stream/Gatherer.Downstream.md)\<inR\>!\>!:the finisher function for the new gatherer |
| `<T>` | the type of input elements for the new gatherer |
| --- | --- |
| `<R>` | the type of results for the new gatherer |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
| [Gatherer](Gatherer.md)<T,` ` [Void](../java.lang/Void.md)!,` `R>! | the new`Gatherer` |

| Exceptions ||
|----------------------------------|--------------------------|
| `java.lang.NullPointerException` | if any argument is`null` |
