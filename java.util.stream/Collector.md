# Collector

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Collector

```
interface Collector<T : Any!, A : Any!, R : Any!>
```

| [java.util.stream.Collector](../java/util/stream/Collector.md) |

A [mutable reduction operation](../java/util/stream/_package.md) that accumulates input elements into a mutable result container, optionally transforming the accumulated result into a final representation after all input elements have been processed. Reduction operations can be performed either sequentially or in parallel.

Examples of mutable reduction operations include: accumulating elements into a`Collection`; concatenating strings using a`StringBuilder`; computing summary information about elements such as sum, min, max, or average; computing "pivot table" summaries such as "maximum valued transaction by seller", etc. The class [Collectors](../java/util/stream/Collectors.md) provides implementations of many common mutable reductions.

A`Collector`is specified by four functions that work together to accumulate entries into a mutable result container, and optionally perform a final transform on the result. They are:

- creation of a new result container ([supplier()](../java/util/stream/Collector.md)))
- incorporating a new data element into a result container ([accumulator()](../java/util/stream/Collector.md)))
- combining two result containers into one ([combiner()](../java/util/stream/Collector.md)))
- performing an optional final transform on the container ([finisher()](../java/util/stream/Collector.md)))

Collectors also have a set of characteristics, such as [Characteristics.CONCURRENT](../java/util/stream/Collector.Characteristics.md), that provide hints that can be used by a reduction implementation to provide better performance.

A sequential implementation of a reduction using a collector would create a single result container using the supplier function, and invoke the accumulator function once for each input element. A parallel implementation would partition the input, create a result container for each partition, accumulate the contents of each partition into a subresult for that partition, and then use the combiner function to merge the subresults into a combined result.

To ensure that sequential and parallel executions produce equivalent results, the collector functions must satisfy an*identity* and an [associativity](../java/util/stream/_package.md) constraints.

The identity constraint says that for any partially accumulated result, combining it with an empty result container must produce an equivalent result. That is, for a partially accumulated result`a`that is the result of any series of accumulator and combiner invocations,`a`must be equivalent to`combiner.apply(a, supplier.get())`.

The associativity constraint says that splitting the computation must produce an equivalent result. That is, for any input elements`t1`and`t2`, the results`r1`and`r2`in the computation below must be equivalent: 

```kotlin
<code>A a1 = supplier.get();
      accumulator.accept(a1, t1);
      accumulator.accept(a1, t2);
      R r1 = finisher.apply(a1);  // result without splitting
 
      A a2 = supplier.get();
      accumulator.accept(a2, t1);
      A a3 = supplier.get();
      accumulator.accept(a3, t2);
      R r2 = finisher.apply(combiner.apply(a2, a3));  // result with splitting
  </code>
```

For collectors that do not have the`UNORDERED`characteristic, two accumulated results`a1`and`a2`are equivalent if`finisher.apply(a1).equals(finisher.apply(a2))`. For unordered collectors, equivalence is relaxed to allow for non-equality related to differences in order. (For example, an unordered collector that accumulated elements to a`List`would consider two lists equivalent if they contained the same elements, ignoring order.)

Libraries that implement reduction based on`Collector`, such as [Stream.collect(Collector)](../java/util/stream/Stream.md)), must adhere to the following constraints:

- The first argument passed to the accumulator function, both arguments passed to the combiner function, and the argument passed to the finisher function must be the result of a previous invocation of the result supplier, accumulator, or combiner functions.
- The implementation should not do anything with the result of any of the result supplier, accumulator, or combiner functions other than to pass them again to the accumulator, combiner, or finisher functions, or return them to the caller of the reduction operation.
- If a result is passed to the combiner or finisher function, and the same object is not returned from that function, it is never used again.
- Once a result is passed to the combiner or finisher function, it is never passed to the accumulator function again.
- For non-concurrent collectors, any result returned from the result supplier, accumulator, or combiner functions must be serially thread-confined. This enables collection to occur in parallel without the`Collector`needing to implement any additional synchronization. The reduction implementation must manage that the input is properly partitioned, that partitions are processed in isolation, and combining happens only after accumulation is complete.
- For concurrent collectors, an implementation is free to (but not required to) implement reduction concurrently. A concurrent reduction is one where the accumulator function is called concurrently from multiple threads, using the same concurrently-modifiable result container, rather than keeping the result isolated during accumulation. A concurrent reduction should only be applied if the collector has the [Characteristics.UNORDERED](../java/util/stream/Collector.Characteristics.md) characteristics or if the originating data is unordered.

In addition to the predefined implementations in [Collectors](../java/util/stream/Collectors.md), the static factory methods [of(java.util.function.Supplier,java.util.function.BiConsumer,java.util.function.BinaryOperator,java.util.stream.Collector.Characteristics...)](../java/util/stream/Collector.md))can be used to construct collectors. For example, you could create a collector that accumulates widgets into a`TreeSet`with: 

```kotlin
<code>Collector&lt;Widget, ?, TreeSet&lt;Widget&gt;&gt; intoSet =
          Collector.of(TreeSet::new, TreeSet::add,
                       (left, right) -&gt; { left.addAll(right); return left; });
  </code>
```
(This behavior is also implemented by the predefined collector [Collectors.toCollection(Supplier)](../java/util/stream/Collectors.md))).

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Characteristics](../java/util/stream/Collector.Characteristics.md) Characteristics indicating properties of a`Collector`, which can be used to optimize reduction implementations. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [BiConsumer](../java/util/function/BiConsumer.md)\<A,T\>! | [accumulator](../java/util/stream/Collector.md))`()` A function that folds a value into a mutable result container. |
| abstract [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Collector.Characteristics](../java/util/stream/Collector.Characteristics.md)!\>! | [characteristics](../java/util/stream/Collector.md))`()` Returns a`Set`of`Collector.Characteristics`indicating the characteristics of this Collector. |
| abstract [BinaryOperator](../java/util/function/BinaryOperator.md)\<A\>! | [combiner](../java/util/stream/Collector.md))`()` A function that accepts two partial results and merges them. |
| --- | --- |
| abstract [Function](../java/util/function/Function.md)\<A,R\>! | [finisher](../java/util/stream/Collector.md))`()` Perform the final transformation from the intermediate accumulation type`A`to the final result type`R`. |
| openstatic [Collector](../java/util/stream/Collector.md)\<T,A,R\>! | [of](../java/util/stream/Collector.md))`(`supplier:` ` [Supplier](../java/util/function/Supplier.md)<A>!`, `accumulator:` ` [BiConsumer](../java/util/function/BiConsumer.md)<A,` `T>!`, `combiner:` ` [BinaryOperator](../java/util/function/BinaryOperator.md)<A>!`, `finisher:` ` [Function](../java/util/function/Function.md)<A,` `R>!`, `vararg` `characteristics:` ` [Collector.Characteristics](../java/util/stream/Collector.Characteristics.md)!`)` Returns a new`Collector`described by the given`supplier`,`accumulator`,`combiner`, and`finisher`functions. |
| openstatic [Collector](../java/util/stream/Collector.md)\<T,R,R\>! | [of](../java/util/stream/Collector.md))`(`supplier:` ` [Supplier](../java/util/function/Supplier.md)<R>!`, `accumulator:` ` [BiConsumer](../java/util/function/BiConsumer.md)<R,` `T>!`, `combiner:` ` [BinaryOperator](../java/util/function/BinaryOperator.md)<R>!`, `vararg` `characteristics:` ` [Collector.Characteristics](../java/util/stream/Collector.Characteristics.md)!`)` Returns a new`Collector`described by the given`supplier`,`accumulator`, and`combiner`functions. |
| --- | --- |
| abstract [Supplier](../java/util/function/Supplier.md)\<A\>! | [supplier](../java/util/stream/Collector.md))`()` A function that creates and returns a new mutable result container. |

## Public methods

### accumulator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun accumulator(): BiConsumer<A, T>!
```

A function that folds a value into a mutable result container.

| Return ||
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [BiConsumer](../java/util/function/BiConsumer.md)<A,` `T>! | a function which folds a value into a mutable result container |

### characteristics

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun characteristics(): MutableSet<Collector.Characteristics!>!
```

Returns a`Set`of`Collector.Characteristics`indicating the characteristics of this Collector. This set should be immutable.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [Collector.Characteristics](../java/util/stream/Collector.Characteristics.md)!>! | an immutable set of collector characteristics |

### combiner

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun combiner(): BinaryOperator<A>!
```

A function that accepts two partial results and merges them. The combiner function may fold state from one argument into the other and return that, or may return a new result container.

| Return ||
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [BinaryOperator](../java/util/function/BinaryOperator.md)<A>! | a function which combines two partial results into a combined result |

### finisher

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun finisher(): Function<A, R>!
```

Perform the final transformation from the intermediate accumulation type`A`to the final result type`R`.

If the characteristic`IDENTITY_FINISH`is set, this function may be presumed to be an identity transform with an unchecked cast from`A`to`R`.

| Return ||
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Function](../java/util/function/Function.md)<A,` `R>! | a function which transforms the intermediate result to the final result |

### of

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!, A : Any!, R : Any!> of(
    supplier: Supplier<A>!, 
    accumulator: BiConsumer<A, T>!, 
    combiner: BinaryOperator<A>!, 
    finisher: Function<A, R>!, 
    vararg characteristics: Collector.Characteristics!
): Collector<T, A, R>!
```

Returns a new`Collector`described by the given`supplier`,`accumulator`,`combiner`, and`finisher`functions.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `supplier` | [Supplier](../java/util/function/Supplier.md)\<A\>!:The supplier function for the new collector |
| `accumulator` | [BiConsumer](../java/util/function/BiConsumer.md)\<A,T\>!:The accumulator function for the new collector |
| `combiner` | [BinaryOperator](../java/util/function/BinaryOperator.md)\<A\>!:The combiner function for the new collector |
| --- | --- |
| `finisher` | [Function](../java/util/function/Function.md)\<A,R\>!:The finisher function for the new collector |
| `characteristics` | [Collector.Characteristics](../java/util/stream/Collector.Characteristics.md)!:The collector characteristics for the new collector |
| `<T>` | The type of input elements for the new collector |
| --- | --- |
| `<A>` | The intermediate accumulation type of the new collector |
| `<R>` | The final result type of the new collector |

| Return ||
|-------------------------------------------------------------------------------------------------------|--------------------|
| [Collector](../java/util/stream/Collector.md)<T,` `A,` `R>! | the new`Collector` |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.lang.NullPointerException` | if any argument is null |

### of

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!, R : Any!> of(
    supplier: Supplier<R>!, 
    accumulator: BiConsumer<R, T>!, 
    combiner: BinaryOperator<R>!, 
    vararg characteristics: Collector.Characteristics!
): Collector<T, R, R>!
```

Returns a new`Collector`described by the given`supplier`,`accumulator`, and`combiner`functions. The resulting`Collector`has the`Collector.Characteristics.IDENTITY_FINISH`characteristic.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `supplier` | [Supplier](../java/util/function/Supplier.md)\<R\>!:The supplier function for the new collector |
| `accumulator` | [BiConsumer](../java/util/function/BiConsumer.md)\<R,T\>!:The accumulator function for the new collector |
| `combiner` | [BinaryOperator](../java/util/function/BinaryOperator.md)\<R\>!:The combiner function for the new collector |
| --- | --- |
| `characteristics` | [Collector.Characteristics](../java/util/stream/Collector.Characteristics.md)!:The collector characteristics for the new collector |
| `<T>` | The type of input elements for the new collector |
| `<R>` | The type of intermediate accumulation result, and final result, for the new collector |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------------------|--------------------|
| [Collector](../java/util/stream/Collector.md)<T,` `R,` `R>! | the new`Collector` |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.lang.NullPointerException` | if any argument is null |

### supplier

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun supplier(): Supplier<A>!
```

A function that creates and returns a new mutable result container.

| Return ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Supplier](../java/util/function/Supplier.md)<A>! | a function which returns a new, mutable result container |
