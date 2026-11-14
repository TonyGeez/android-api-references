# Gatherer

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Gatherer

```
interface Gatherer<T : Any!, A : Any!, R : Any!>
```

| [java.util.stream.Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#) |

An intermediate operation that transforms a stream of input elements into a stream of output elements, optionally applying a final action when the end of the upstream is reached. The transformation may be stateless or stateful, and may buffer input before producing any output.

Gatherer operations can be performed either sequentially, or be parallelized -- if a combiner function is supplied.

There are many examples of gathering operations, including but not limited to: grouping elements into batches (windowing functions); de-duplicating consecutively similar elements; incremental accumulation functions (prefix scan); incremental reordering functions, etc. The class [java.util.stream.Gatherers](https://developer.android.com/reference/kotlin/java/util/stream/Gatherers) provides implementations of common gathering operations.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Downstream](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Downstream) A Downstream object is the next stage in a pipeline of operations, to which elements can be sent. |
| abstract | [Integrator](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Integrator) An Integrator receives elements and processes them, optionally using the supplied state, and optionally sends incremental results downstream. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#)\<T,\*,RR\>! | [andThen](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#andThen(java.util.stream.Gatherer))`(`that:` ` [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#)<in` `R,` `*,` `out` `RR>!`)` Returns a composed Gatherer which connects the output of this Gatherer to the input of that Gatherer. |
| open [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#)\<A\>! | [combiner](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#combiner())`()` A function which accepts two intermediate states and combines them into one. |
| openstatic [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#)\<A\>! | [defaultCombiner](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#defaultCombiner())`()` Returns a combiner which is the default combiner of a Gatherer. |
| openstatic [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#)\<A, [Gatherer.Downstream](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Downstream)\<inR\>!\>! | [defaultFinisher](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#defaultFinisher())`()` Returns a`finisher`which is the default finisher of a`Gatherer`. |
| openstatic [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\<A\>! | [defaultInitializer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#defaultInitializer())`()` Returns an initializer which is the default initializer of a Gatherer. |
| open [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#)\<A, [Gatherer.Downstream](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Downstream)\<inR\>!\>! | [finisher](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#finisher())`()` A function which accepts the final intermediate state and a [Downstream](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Downstream) object, allowing to perform a final action at the end of input elements. |
| open [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\<A\>! | [initializer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#initializer())`()` A function that produces an instance of the intermediate state used for this gathering operation. |
| abstract [Gatherer.Integrator](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Integrator)\<A,T,R\>! | [integrator](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#integrator())`()` A function which integrates provided elements, potentially using the provided intermediate state, optionally producing output to the provided [Downstream](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Downstream). |
| openstatic [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#)\<T,A,R\>! | [of](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#of(java.util.function.Supplier,%20java.util.stream.Gatherer.Integrator,%20java.util.function.BinaryOperator,%20java.util.function.BiConsumer))`(`initializer:` ` [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)<A>!`, `integrator:` ` [Gatherer.Integrator](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Integrator)<A,` `T,` `R>!`, `combiner:` ` [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#)<A>!`, `finisher:` ` [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#)<A,` ` [Gatherer.Downstream](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Downstream)<in` `R>!>!`)` Returns a new, parallelizable,`Gatherer`described by the given`initializer`,`integrator`,`combiner`and`finisher`. |
| openstatic [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#)\<T, [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!,R\>! | [of](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#of(java.util.stream.Gatherer.Integrator))`(`integrator:` ` [Gatherer.Integrator](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Integrator)< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!,` `T,` `R>!`)` Returns a new, parallelizable, and stateless`Gatherer`described by the given`integrator`. |
| openstatic [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#)\<T, [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!,R\>! | [of](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#of(java.util.stream.Gatherer.Integrator,%20java.util.function.BiConsumer))`(`integrator:` ` [Gatherer.Integrator](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Integrator)< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!,` `T,` `R>!`, `finisher:` ` [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#)< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!,` ` [Gatherer.Downstream](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Downstream)<in` `R>!>!`)` Returns a new, parallelizable, and stateless`Gatherer`described by the given`integrator`and`finisher`. |
| openstatic [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#)\<T,A,R\>! | [ofSequential](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#ofSequential(java.util.function.Supplier,%20java.util.stream.Gatherer.Integrator))`(`initializer:` ` [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)<A>!`, `integrator:` ` [Gatherer.Integrator](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Integrator)<A,` `T,` `R>!`)` Returns a new, sequential,`Gatherer`described by the given`initializer`and`integrator`. |
| openstatic [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#)\<T,A,R\>! | [ofSequential](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#ofSequential(java.util.function.Supplier,%20java.util.stream.Gatherer.Integrator,%20java.util.function.BiConsumer))`(`initializer:` ` [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)<A>!`, `integrator:` ` [Gatherer.Integrator](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Integrator)<A,` `T,` `R>!`, `finisher:` ` [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#)<A,` ` [Gatherer.Downstream](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Downstream)<in` `R>!>!`)` Returns a new, sequential,`Gatherer`described by the given`initializer`,`integrator`, and`finisher`. |
| openstatic [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#)\<T, [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!,R\>! | [ofSequential](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#ofSequential(java.util.stream.Gatherer.Integrator))`(`integrator:` ` [Gatherer.Integrator](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Integrator)< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!,` `T,` `R>!`)` Returns a new, sequential, and stateless`Gatherer`described by the given`integrator`. |
| openstatic [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#)\<T, [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!,R\>! | [ofSequential](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#ofSequential(java.util.stream.Gatherer.Integrator,%20java.util.function.BiConsumer))`(`integrator:` ` [Gatherer.Integrator](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Integrator)< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!,` `T,` `R>!`, `finisher:` ` [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#)< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!,` ` [Gatherer.Downstream](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Downstream)<in` `R>!>!`)` Returns a new, sequential, and stateless`Gatherer`described by the given`integrator`and`finisher`. |

## Public methods

### andThen

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <RR : Any!> andThen(that: Gatherer<in R, *, out RR>!): Gatherer<T, *, RR>!
```

Returns a composed Gatherer which connects the output of this Gatherer to the input of that Gatherer.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------|
| `that` | [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#)\<inR,\*,outRR\>!:the other gatherer |
| `<RR>` | The type of output of that Gatherer |

| Return ||
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#)<T,` `*,` `RR>! | returns a composed Gatherer which connects the output of this Gatherer as input that Gatherer |

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
| [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#)<A>! | a function which accepts two intermediate states and combines them into one |

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
| [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#)<A>! | the instance of the default combiner |

**See Also**

- [java.util.stream.Gatherer#combiner()](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#combiner()) 

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
| [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#)<A,` ` [Gatherer.Downstream](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Downstream)<in` `R>!>! | the instance of the default finisher |

**See Also**

- [java.util.stream.Gatherer#finisher()](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#finisher()) 

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
| [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)<A>! | the instance of the default initializer |

**See Also**

- [java.util.stream.Gatherer#initializer()](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#initializer()) 

### finisher

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun finisher(): BiConsumer<A, Gatherer.Downstream<in R>!>!
```

A function which accepts the final intermediate state and a [Downstream](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Downstream) object, allowing to perform a final action at the end of input elements.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#)<A,` ` [Gatherer.Downstream](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Downstream)<in` `R>!>! | a function which transforms the intermediate result to the final result(s) which are then passed on to the provided Downstream |

### initializer

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun initializer(): Supplier<A>!
```

A function that produces an instance of the intermediate state used for this gathering operation.

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)<A>! | A function that produces an instance of the intermediate state used for this gathering operation |

### integrator

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun integrator(): Gatherer.Integrator<A, T, R>!
```

A function which integrates provided elements, potentially using the provided intermediate state, optionally producing output to the provided [Downstream](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Downstream).

| Return ||
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Gatherer.Integrator](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Integrator)<A,` `T,` `R>! | a function which integrates provided elements, potentially using the provided state, optionally producing output to the provided Downstream |

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
| `initializer` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\<A\>!:the initializer function for the new gatherer |
| `integrator` | [Gatherer.Integrator](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Integrator)\<A,T,R\>!:the integrator function for the new gatherer |
| `combiner` | [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#)\<A\>!:the combiner function for the new gatherer |
| `finisher` | [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#)\<A, [Gatherer.Downstream](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Downstream)\<inR\>!\>!:the finisher function for the new gatherer |
| `<T>` | the type of input elements for the new gatherer |
| `<A>` | the type of state for the new gatherer |
| `<R>` | the type of results for the new gatherer |

| Return ||
|-----------------------------------------------------------------------------------------------------|-------------------|
| [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#)<T,` `A,` `R>! | the new`Gatherer` |

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
| `integrator` | [Gatherer.Integrator](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Integrator)\< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!,T,R\>!:the integrator function for the new gatherer |
| `<T>` | the type of input elements for the new gatherer |
| `<R>` | the type of results for the new gatherer |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
| [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#)<T,` ` [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!,` `R>! | the new`Gatherer` |

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
| `integrator` | [Gatherer.Integrator](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Integrator)\< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!,T,R\>!:the integrator function for the new gatherer |
| `finisher` | [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#)\< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!, [Gatherer.Downstream](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Downstream)\<inR\>!\>!:the finisher function for the new gatherer |
| `<T>` | the type of input elements for the new gatherer |
| `<R>` | the type of results for the new gatherer |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
| [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#)<T,` ` [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!,` `R>! | the new`Gatherer` |

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
| `initializer` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\<A\>!:the initializer function for the new gatherer |
| `integrator` | [Gatherer.Integrator](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Integrator)\<A,T,R\>!:the integrator function for the new gatherer |
| `<T>` | the type of input elements for the new gatherer |
| `<A>` | the type of state for the new gatherer |
| `<R>` | the type of results for the new gatherer |

| Return ||
|-----------------------------------------------------------------------------------------------------|-------------------|
| [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#)<T,` `A,` `R>! | the new`Gatherer` |

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
| `initializer` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\<A\>!:the initializer function for the new gatherer |
| `integrator` | [Gatherer.Integrator](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Integrator)\<A,T,R\>!:the integrator function for the new gatherer |
| `finisher` | [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#)\<A, [Gatherer.Downstream](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Downstream)\<inR\>!\>!:the finisher function for the new gatherer |
| `<T>` | the type of input elements for the new gatherer |
| `<A>` | the type of state for the new gatherer |
| `<R>` | the type of results for the new gatherer |

| Return ||
|-----------------------------------------------------------------------------------------------------|-------------------|
| [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#)<T,` `A,` `R>! | the new`Gatherer` |

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
| `integrator` | [Gatherer.Integrator](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Integrator)\< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!,T,R\>!:the integrator function for the new gatherer |
| `<T>` | the type of input elements for the new gatherer |
| `<R>` | the type of results for the new gatherer |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
| [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#)<T,` ` [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!,` `R>! | the new`Gatherer` |

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
| `integrator` | [Gatherer.Integrator](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Integrator)\< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!,T,R\>!:the integrator function for the new gatherer |
| `finisher` | [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#)\< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!, [Gatherer.Downstream](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer.Downstream)\<inR\>!\>!:the finisher function for the new gatherer |
| `<T>` | the type of input elements for the new gatherer |
| `<R>` | the type of results for the new gatherer |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
| [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer#)<T,` ` [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!,` `R>! | the new`Gatherer` |

| Exceptions ||
|----------------------------------|--------------------------|
| `java.lang.NullPointerException` | if any argument is`null` |
