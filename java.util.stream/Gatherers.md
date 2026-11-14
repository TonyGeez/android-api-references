# Gatherers

Added in [API level Baklava](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Gatherers

```
class Gatherers
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.stream.Gatherers](https://developer.android.com/reference/kotlin/java/util/stream/Gatherers#) |

Implementations of [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer) that provide useful intermediate operations, such as windowing functions, folding functions, transforming elements concurrently, etc.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer)\<T, \*, R\>! | [fold](https://developer.android.com/reference/kotlin/java/util/stream/Gatherers#fold(java.util.function.Supplier,%20java.util.function.BiFunction))`(`initial:` ` [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)<R>!`, `folder:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)<in` `R,` `in` `T,` `out` `R>!`)` Returns a Gatherer that performs an ordered, *reduction-like*, transformation for scenarios where no combiner-function can be implemented, or for reductions which are intrinsically order-dependent. |
| static [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer)\<T, \*, R\>! | [scan](https://developer.android.com/reference/kotlin/java/util/stream/Gatherers#scan(java.util.function.Supplier,%20java.util.function.BiFunction))`(`initial:` ` [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)<R>!`, `scanner:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)<in` `R,` `in` `T,` `out` `R>!`)` Returns a Gatherer that performs a Prefix Scan -- an incremental accumulation -- using the provided functions. |
| static [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer)\<TR, \*, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<TR\>!\>! | [windowFixed](https://developer.android.com/reference/kotlin/java/util/stream/Gatherers#windowFixed(kotlin.Int))`(`windowSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a Gatherer that gathers elements into windows -- encounter-ordered groups of elements -- of a fixed size. |
| --- | --- |
| static [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer)\<TR, \*, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<TR\>!\>! | [windowSliding](https://developer.android.com/reference/kotlin/java/util/stream/Gatherers#windowSliding(kotlin.Int))`(`windowSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a Gatherer that gathers elements into windows -- encounter-ordered groups of elements -- of a given size, where each subsequent window includes all elements of the previous window except for the least recent, and adds the next element in the stream. |

## Public methods

### fold

Added in [API level Baklava](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!, R : Any!> fold(
    initial: Supplier<R>!, 
    folder: BiFunction<in R, in T, out R>!
): Gatherer<T, *, R>!
```

Returns a Gatherer that performs an ordered, *reduction-like*, transformation for scenarios where no combiner-function can be implemented, or for reductions which are intrinsically order-dependent.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `initial` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\<R\>!: the identity value for the fold operation |
| `folder` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)\<in R, in T, out R\>!: the folding function |
| `<T>` | the type of elements the returned gatherer consumes |
| --- | --- |
| `<R>` | the type of elements the returned gatherer produces |

| Return ||
|----------------------------------------------------------------------------------------------------|----------------|
| [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer)<T,` `*,` `R>! | a new Gatherer |

| Exceptions ||
|----------------------------------|-------------------------------------|
| `java.lang.NullPointerException` | if any of the parameters are `null` |

**See Also**

- [java.util.stream.Stream#reduce(Object, BinaryOperator)](https://developer.android.com/reference/kotlin/java/util/stream/Stream#reduce(java.util.stream.Stream.T,%20java.util.function.BinaryOperator)) 

### scan

Added in [API level Baklava](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!, R : Any!> scan(
    initial: Supplier<R>!, 
    scanner: BiFunction<in R, in T, out R>!
): Gatherer<T, *, R>!
```

Returns a Gatherer that performs a Prefix Scan -- an incremental accumulation -- using the provided functions. Starting with an initial value obtained from the `Supplier`, each subsequent value is obtained by applying the `BiFunction` to the current value and the next input element, after which the resulting value is produced downstream.

Example: {@snippet lang = java: \* // will contain: \["1", "12", "123", "1234", "12345", "123456", "1234567", "12345678", "123456789"\] \* List numberStrings = \* Stream.of(1,2,3,4,5,6,7,8,9) \* .gather( \* Gatherers.scan(() -\> "", (string, number) -\> string + number) \* ) \* .toList(); \* }

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `initial` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\<R\>!: the supplier of the initial value for the scanner |
| `scanner` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)\<in R, in T, out R\>!: the function to apply for each element |
| `<T>` | the type of element which this gatherer consumes |
| --- | --- |
| `<R>` | the type of element which this gatherer produces |

| Return ||
|----------------------------------------------------------------------------------------------------|---------------------------------------------|
| [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer)<T,` `*,` `R>! | a new Gatherer which performs a prefix scan |

| Exceptions ||
|----------------------------------|-------------------------------------|
| `java.lang.NullPointerException` | if any of the parameters are `null` |

### windowFixed

Added in [API level Baklava](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <TR : Any!> windowFixed(windowSize: Int): Gatherer<TR, *, MutableList<TR>!>!
```

Returns a Gatherer that gathers elements into windows -- encounter-ordered groups of elements -- of a fixed size. If the stream is empty then no window will be produced. The last window may contain fewer elements than the supplied window size.

Example: {@snippet lang = java: \* // will contain: \[\[1, 2, 3\], \[4, 5, 6\], \[7, 8\]\] \* List\> windows = \* Stream.of(1,2,3,4,5,6,7,8).gather(Gatherers.windowFixed(3)).toList(); \* }

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------|
| `windowSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the size of the windows |
| `<TR>` | the type of elements the returned gatherer consumes and the contents of the windows it produces |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer)<TR,` `*,` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<TR>!>! | a new gatherer which groups elements into fixed-size windows |

| Exceptions ||
|--------------------------------------|----------------------------------|
| `java.lang.IllegalArgumentException` | when `windowSize` is less than 1 |

### windowSliding

Added in [API level Baklava](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <TR : Any!> windowSliding(windowSize: Int): Gatherer<TR, *, MutableList<TR>!>!
```

Returns a Gatherer that gathers elements into windows -- encounter-ordered groups of elements -- of a given size, where each subsequent window includes all elements of the previous window except for the least recent, and adds the next element in the stream. If the stream is empty then no window will be produced. If the size of the stream is smaller than the window size then only one window will be produced, containing all elements in the stream.

Example: {@snippet lang = java: \* // will contain: \[\[1, 2\], \[2, 3\], \[3, 4\], \[4, 5\], \[5, 6\], \[6, 7\], \[7, 8\]\] \* List\> windows2 = \* Stream.of(1,2,3,4,5,6,7,8).gather(Gatherers.windowSliding(2)).toList(); \* \* // will contain: \[\[1, 2, 3, 4, 5, 6\], \[2, 3, 4, 5, 6, 7\], \[3, 4, 5, 6, 7, 8\]\] \* List\> windows6 = \* Stream.of(1,2,3,4,5,6,7,8).gather(Gatherers.windowSliding(6)).toList(); \* }

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------|
| `windowSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the size of the windows |
| `<TR>` | the type of elements the returned gatherer consumes and the contents of the windows it produces |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Gatherer](https://developer.android.com/reference/kotlin/java/util/stream/Gatherer)<TR,` `*,` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<TR>!>! | a new gatherer which groups elements into sliding windows |

| Exceptions ||
|--------------------------------------|--------------------------------|
| `java.lang.IllegalArgumentException` | when windowSize is less than 1 |
