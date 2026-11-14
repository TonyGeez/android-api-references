Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Collectors

```
class Collectors
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.stream.Collectors](https://developer.android.com/reference/kotlin/java/util/stream/Collectors#) |

Implementations of `https://developer.android.com/reference/kotlin/java/util/stream/Collector` that implement various useful reduction operations, such as accumulating elements into collections, summarizing elements according to various criteria, etc.

The following are examples of using the predefined collectors to perform common mutable reduction tasks:

```kotlin
<code>// Accumulate names into a List
  List&lt;String&gt; list = people.stream()
    .map(Person::getName)
    .collect(Collectors.toList());
 
  // Accumulate names into a TreeSet
  Set&lt;String&gt; set = people.stream()
    .map(Person::getName)
    .collect(Collectors.toCollection(TreeSet::new));
 
  // Convert elements to strings and concatenate them, separated by commas
  String joined = things.stream()
    .map(Object::toString)
    .collect(Collectors.joining(", "));
 
  // Compute sum of salaries of employee
  int total = employees.stream()
    .collect(Collectors.summingInt(Employee::getSalary));
 
  // Group employees by department
  Map&lt;Department, List&lt;Employee&gt;&gt; byDept = employees.stream()
    .collect(Collectors.groupingBy(Employee::getDepartment));
 
  // Compute sum of salaries by department
  Map&lt;Department, Integer&gt; totalByDept = employees.stream()
    .collect(Collectors.groupingBy(Employee::getDepartment,
                                   Collectors.summingInt(Employee::getSalary)));
 
  // Partition students into passing and failing
  Map&lt;Boolean, List&lt;Student&gt;&gt; passingFailing = students.stream()
    .collect(Collectors.partitioningBy(s -&gt; s.getGrade() &gt;= PASS_THRESHOLD));
 
  </code>
```

## Summary

| Public methods ||
|---|---|
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#averagingDouble(java.util.function.ToDoubleFunction)(mapper: https://developer.android.com/reference/kotlin/java/util/function/ToDoubleFunction.html#<in T>!)` Returns a `Collector` that produces the arithmetic mean of a double-valued function applied to the input elements. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#averagingInt(java.util.function.ToIntFunction)(mapper: https://developer.android.com/reference/kotlin/java/util/function/ToIntFunction.html#<in T>!)` Returns a `Collector` that produces the arithmetic mean of an integer-valued function applied to the input elements. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#averagingLong(java.util.function.ToLongFunction)(mapper: https://developer.android.com/reference/kotlin/java/util/function/ToLongFunction.html#<in T>!)` Returns a `Collector` that produces the arithmetic mean of a long-valued function applied to the input elements. |
| --- | --- |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, A, RR\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#collectingAndThen(java.util.stream.Collector,%20java.util.function.Function)(downstream: https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, A, R>!, finisher: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<R, RR>!)` Adapts a `Collector` to perform an additional finishing transformation. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#counting()()` Returns a `Collector` accepting elements of type `T` that counts the number of input elements. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, R\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#filtering(java.util.function.Predicate,%20java.util.stream.Collector)(predicate: https://developer.android.com/reference/kotlin/java/util/function/Predicate.html#<in T>!, downstream: https://developer.android.com/reference/kotlin/java/util/stream/Collector<in T, A, R>!)` Adapts a `Collector` to one accepting elements of the same type `T` by applying the predicate to each input element and only accumulating if the predicate returns `true`. |
| --- | --- |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, R\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#flatMapping(java.util.function.Function,%20java.util.stream.Collector)(mapper: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out https://developer.android.com/reference/kotlin/java/util/stream/Stream<out U>!>!, downstream: https://developer.android.com/reference/kotlin/java/util/stream/Collector<in U, A, R>!)` Adapts a `Collector` accepting elements of type `U` to one accepting elements of type `T` by applying a flat mapping function to each input element before accumulation. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\>!\>!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#groupingBy(java.util.function.Function)(classifier: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out K>!)` Returns a `Collector` implementing a "group by" operation on input elements of type `T`, grouping elements according to a classification function, and returning the results in a `Map`. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, M\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#groupingBy(java.util.function.Function,%20java.util.function.Supplier,%20java.util.stream.Collector)(classifier: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out K>!, mapFactory: https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#<M>!, downstream: https://developer.android.com/reference/kotlin/java/util/stream/Collector<in T, A, D>!)` Returns a `Collector` implementing a cascaded "group by" operation on input elements of type `T`, grouping elements according to a classification function, and then performing a reduction operation on the values associated with a given key using the specified downstream `Collector`. |
| --- | --- |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K, D\>!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#groupingBy(java.util.function.Function,%20java.util.stream.Collector)(classifier: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out K>!, downstream: https://developer.android.com/reference/kotlin/java/util/stream/Collector<in T, A, D>!)` Returns a `Collector` implementing a cascaded "group by" operation on input elements of type `T`, grouping elements according to a classification function, and then performing a reduction operation on the values associated with a given key using the specified downstream `Collector`. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [ConcurrentMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentMap.html#)\<K, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\>!\>!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#groupingByConcurrent(java.util.function.Function)(classifier: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out K>!)` Returns a concurrent `Collector` implementing a "group by" operation on input elements of type `T`, grouping elements according to a classification function. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, M\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#groupingByConcurrent(java.util.function.Function,%20java.util.function.Supplier,%20java.util.stream.Collector)(classifier: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out K>!, mapFactory: https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#<M>!, downstream: https://developer.android.com/reference/kotlin/java/util/stream/Collector<in T, A, D>!)` Returns a concurrent `Collector` implementing a cascaded "group by" operation on input elements of type `T`, grouping elements according to a classification function, and then performing a reduction operation on the values associated with a given key using the specified downstream `Collector`. |
| --- | --- |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [ConcurrentMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentMap.html#)\<K, D\>!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#groupingByConcurrent(java.util.function.Function,%20java.util.stream.Collector)(classifier: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out K>!, downstream: https://developer.android.com/reference/kotlin/java/util/stream/Collector<in T, A, D>!)` Returns a concurrent `Collector` implementing a cascaded "group by" operation on input elements of type `T`, grouping elements according to a classification function, and then performing a reduction operation on the values associated with a given key using the specified downstream `Collector`. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!, \*, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#joining()()` Returns a `Collector` that concatenates the input elements into a `String`, in encounter order. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!, \*, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#joining(kotlin.CharSequence)(delimiter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Returns a `Collector` that concatenates the input elements, separated by the specified delimiter, in encounter order. |
| --- | --- |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!, \*, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#joining(kotlin.CharSequence,%20kotlin.CharSequence,%20kotlin.CharSequence)(delimiter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, suffix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Returns a `Collector` that concatenates the input elements, separated by the specified delimiter, with the specified prefix and suffix, in encounter order. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, R\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#mapping(java.util.function.Function,%20java.util.stream.Collector)(mapper: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out U>!, downstream: https://developer.android.com/reference/kotlin/java/util/stream/Collector<in U, A, R>!)` Adapts a `Collector` accepting elements of type `U` to one accepting elements of type `T` by applying a mapping function to each input element before accumulation. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [Optional](https://developer.android.com/reference/kotlin/java/util/Optional.html#)\<T\>!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#maxBy(java.util.Comparator)(comparator: https://developer.android.com/reference/kotlin/java/util/Comparator.html#<in T>!)` Returns a `Collector` that produces the maximal element according to a given `Comparator`, described as an `Optional<T>`. |
| --- | --- |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [Optional](https://developer.android.com/reference/kotlin/java/util/Optional.html#)\<T\>!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#minBy(java.util.Comparator)(comparator: https://developer.android.com/reference/kotlin/java/util/Comparator.html#<in T>!)` Returns a `Collector` that produces the minimal element according to a given `Comparator`, described as an `Optional<T>`. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\>!\>!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#partitioningBy(java.util.function.Predicate)(predicate: https://developer.android.com/reference/kotlin/java/util/function/Predicate.html#<in T>!)` Returns a `Collector` which partitions the input elements according to a `Predicate`, and organizes them into a `Map<Boolean, List<T>>`. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!, D\>!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#partitioningBy(java.util.function.Predicate,%20java.util.stream.Collector)(predicate: https://developer.android.com/reference/kotlin/java/util/function/Predicate.html#<in T>!, downstream: https://developer.android.com/reference/kotlin/java/util/stream/Collector<in T, A, D>!)` Returns a `Collector` which partitions the input elements according to a `Predicate`, reduces the values in each partition according to another `Collector`, and organizes them into a `Map<Boolean, D>` whose values are the result of the downstream reduction. |
| --- | --- |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [Optional](https://developer.android.com/reference/kotlin/java/util/Optional.html#)\<T\>!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#reducing(java.util.function.BinaryOperator)(op: https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#<T>!)` Returns a `Collector` which performs a reduction of its input elements under a specified `BinaryOperator`. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, T\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#reducing(java.util.stream.Collectors.reducing.T,%20java.util.function.BinaryOperator)(identity: T, op: https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#<T>!)` Returns a `Collector` which performs a reduction of its input elements under a specified `BinaryOperator` using the provided identity. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, U\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#reducing(java.util.stream.Collectors.reducing.U,%20java.util.function.Function,%20java.util.function.BinaryOperator)(identity: U, mapper: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out U>!, op: https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#<U>!)` Returns a `Collector` which performs a reduction of its input elements under a specified mapping function and `BinaryOperator`. |
| --- | --- |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [DoubleSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/DoubleSummaryStatistics.html#)!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#summarizingDouble(java.util.function.ToDoubleFunction)(mapper: https://developer.android.com/reference/kotlin/java/util/function/ToDoubleFunction.html#<in T>!)` Returns a `Collector` which applies an `double`-producing mapping function to each input element, and returns summary statistics for the resulting values. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [IntSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/IntSummaryStatistics.html#)!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#summarizingInt(java.util.function.ToIntFunction)(mapper: https://developer.android.com/reference/kotlin/java/util/function/ToIntFunction.html#<in T>!)` Returns a `Collector` which applies an `int`-producing mapping function to each input element, and returns summary statistics for the resulting values. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [LongSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/LongSummaryStatistics.html#)!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#summarizingLong(java.util.function.ToLongFunction)(mapper: https://developer.android.com/reference/kotlin/java/util/function/ToLongFunction.html#<in T>!)` Returns a `Collector` which applies an `long`-producing mapping function to each input element, and returns summary statistics for the resulting values. |
| --- | --- |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#summingDouble(java.util.function.ToDoubleFunction)(mapper: https://developer.android.com/reference/kotlin/java/util/function/ToDoubleFunction.html#<in T>!)` Returns a `Collector` that produces the sum of a double-valued function applied to the input elements. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#summingInt(java.util.function.ToIntFunction)(mapper: https://developer.android.com/reference/kotlin/java/util/function/ToIntFunction.html#<in T>!)` Returns a `Collector` that produces the sum of an integer-valued function applied to the input elements. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#summingLong(java.util.function.ToLongFunction)(mapper: https://developer.android.com/reference/kotlin/java/util/function/ToLongFunction.html#<in T>!)` Returns a `Collector` that produces the sum of a long-valued function applied to the input elements. |
| --- | --- |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, R\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#teeing(java.util.stream.Collector,%20java.util.stream.Collector,%20java.util.function.BiFunction)(downstream1: https://developer.android.com/reference/kotlin/java/util/stream/Collector<in T, *, R1>!, downstream2: https://developer.android.com/reference/kotlin/java/util/stream/Collector<in T, *, R2>!, merger: https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#<in R1, in R2, R>!)` Returns a `Collector` that is a composite of two downstream collectors. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, C\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toCollection(java.util.function.Supplier)(collectionFactory: https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#<C>!)` Returns a `Collector` that accumulates the input elements into a new `Collection`, in encounter order. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [ConcurrentMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentMap.html#)\<K, U\>!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toConcurrentMap(java.util.function.Function,%20java.util.function.Function)(keyMapper: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out K>!, valueMapper: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out U>!)` Returns a concurrent `Collector` that accumulates elements into a `ConcurrentMap` whose keys and values are the result of applying the provided mapping functions to the input elements. |
| --- | --- |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [ConcurrentMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentMap.html#)\<K, U\>!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toConcurrentMap(java.util.function.Function,%20java.util.function.Function,%20java.util.function.BinaryOperator)(keyMapper: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out K>!, valueMapper: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out U>!, mergeFunction: https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#<U>!)` Returns a concurrent `Collector` that accumulates elements into a `ConcurrentMap` whose keys and values are the result of applying the provided mapping functions to the input elements. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, M\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toConcurrentMap(java.util.function.Function,%20java.util.function.Function,%20java.util.function.BinaryOperator,%20java.util.function.Supplier)(keyMapper: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out K>!, valueMapper: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out U>!, mergeFunction: https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#<U>!, mapFactory: https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#<M>!)` Returns a concurrent `Collector` that accumulates elements into a `ConcurrentMap` whose keys and values are the result of applying the provided mapping functions to the input elements. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\>!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toList()()` Returns a `Collector` that accumulates the input elements into a new `List`. |
| --- | --- |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K, U\>!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toMap(java.util.function.Function,%20java.util.function.Function)(keyMapper: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out K>!, valueMapper: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out U>!)` Returns a `Collector` that accumulates elements into a `Map` whose keys and values are the result of applying the provided mapping functions to the input elements. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K, U\>!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toMap(java.util.function.Function,%20java.util.function.Function,%20java.util.function.BinaryOperator)(keyMapper: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out K>!, valueMapper: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out U>!, mergeFunction: https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#<U>!)` Returns a `Collector` that accumulates elements into a `Map` whose keys and values are the result of applying the provided mapping functions to the input elements. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, M\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toMap(java.util.function.Function,%20java.util.function.Function,%20java.util.function.BinaryOperator,%20java.util.function.Supplier)(keyMapper: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out K>!, valueMapper: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out U>!, mergeFunction: https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#<U>!, mapFactory: https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#<M>!)` Returns a `Collector` that accumulates elements into a `Map` whose keys and values are the result of applying the provided mapping functions to the input elements. |
| --- | --- |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<T\>!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toSet()()` Returns a `Collector` that accumulates the input elements into a new `Set`. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\>!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toUnmodifiableList()()` Returns a `Collector` that accumulates the input elements into an [unmodifiable List](https://developer.android.com/reference/kotlin/java/util/List.html#unmodifiable) in encounter order. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K, U\>!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toUnmodifiableMap(java.util.function.Function,%20java.util.function.Function)(keyMapper: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out K>!, valueMapper: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out U>!)` Returns a `Collector` that accumulates the input elements into an [unmodifiable Map](https://developer.android.com/reference/kotlin/java/util/Map.html#unmodifiable), whose keys and values are the result of applying the provided mapping functions to the input elements. |
| --- | --- |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K, U\>!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toUnmodifiableMap(java.util.function.Function,%20java.util.function.Function,%20java.util.function.BinaryOperator)(keyMapper: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out K>!, valueMapper: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out U>!, mergeFunction: https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#<U>!)` Returns a `Collector` that accumulates the input elements into an [unmodifiable Map](https://developer.android.com/reference/kotlin/java/util/Map.html#unmodifiable), whose keys and values are the result of applying the provided mapping functions to the input elements. |
| static [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, \*, [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<T\>!\>! | `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toUnmodifiableSet()()` Returns a `Collector` that accumulates the input elements into an [unmodifiable Set](https://developer.android.com/reference/kotlin/java/util/Set.html#unmodifiable). |

## Public methods

### averagingDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> averagingDouble(mapper: ToDoubleFunction<in T>!): Collector<T, *, Double!>!
```

Returns a `Collector` that produces the arithmetic mean of a double-valued function applied to the input elements. If no elements are present, the result is 0.

The average returned can vary depending upon the order in which values are recorded, due to accumulated rounding error in addition of values of differing magnitudes. Values sorted by increasing absolute magnitude tend to yield more accurate results. If any recorded value is a `NaN` or the sum is at any point a `NaN` then the average will be `NaN`.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `mapper` | [ToDoubleFunction](https://developer.android.com/reference/kotlin/java/util/function/ToDoubleFunction.html#)\<in T\>!: a function extracting the property to be averaged |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html!>!` | a `Collector` that produces the arithmetic mean of a derived property |

### averagingInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> averagingInt(mapper: ToIntFunction<in T>!): Collector<T, *, Double!>!
```

Returns a `Collector` that produces the arithmetic mean of an integer-valued function applied to the input elements. If no elements are present, the result is 0.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `mapper` | [ToIntFunction](https://developer.android.com/reference/kotlin/java/util/function/ToIntFunction.html#)\<in T\>!: a function extracting the property to be averaged |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html!>!` | a `Collector` that produces the arithmetic mean of a derived property |

### averagingLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> averagingLong(mapper: ToLongFunction<in T>!): Collector<T, *, Double!>!
```

Returns a `Collector` that produces the arithmetic mean of a long-valued function applied to the input elements. If no elements are present, the result is 0.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `mapper` | [ToLongFunction](https://developer.android.com/reference/kotlin/java/util/function/ToLongFunction.html#)\<in T\>!: a function extracting the property to be averaged |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html!>!` | a `Collector` that produces the arithmetic mean of a derived property |

### collectingAndThen

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!, A : Any!, R : Any!, RR : Any!> collectingAndThen(
    downstream: Collector<T, A, R>!, 
    finisher: Function<R, RR>!
): Collector<T, A, RR>!
```

Adapts a `Collector` to perform an additional finishing transformation. For example, one could adapt the `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toList()` collector to always produce an immutable list with:

```kotlin
<code>List&lt;String&gt; list = people.stream().collect(
    collectingAndThen(toList(),
                      Collections::unmodifiableList));
  </code>
```

<br />

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `<A>` | intermediate accumulation type of the downstream collector |
| `<R>` | result type of the downstream collector |
| --- | --- |
| `<RR>` | result type of the resulting collector |
| `downstream` | [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<T, A, R\>!: a collector |
| `finisher` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<R, RR\>!: a function to be applied to the final result of the downstream collector |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, A, RR>!` | a collector which performs the action of the downstream collector, followed by an additional finishing step |

### counting

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> counting(): Collector<T, *, Long!>!
```

Returns a `Collector` accepting elements of type `T` that counts the number of input elements. If no elements are present, the result is 0.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html!>!` | a `Collector` that counts the input elements |

### filtering

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!, A : Any!, R : Any!> filtering(
    predicate: Predicate<in T>!, 
    downstream: Collector<in T, A, R>!
): Collector<T, *, R>!
```

Adapts a `Collector` to one accepting elements of the same type `T` by applying the predicate to each input element and only accumulating if the predicate returns `true`.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `<A>` | intermediate accumulation type of the downstream collector |
| `<R>` | result type of collector |
| --- | --- |
| `predicate` | [Predicate](https://developer.android.com/reference/kotlin/java/util/function/Predicate.html#)\<in T\>!: a predicate to be applied to the input elements |
| `downstream` | [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<in T, A, R\>!: a collector which will accept values that match the predicate |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, R>!` | a collector which applies the predicate to the input elements and provides matching elements to the downstream collector |

### flatMapping

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!, U : Any!, A : Any!, R : Any!> flatMapping(
    mapper: Function<in T, out Stream<out U>!>!, 
    downstream: Collector<in U, A, R>!
): Collector<T, *, R>!
```

Adapts a `Collector` accepting elements of type `U` to one accepting elements of type `T` by applying a flat mapping function to each input element before accumulation. The flat mapping function maps an input element to a `https://developer.android.com/reference/kotlin/java/util/stream/Stream` covering zero or more output elements that are then accumulated downstream. Each mapped stream is `https://developer.android.com/reference/kotlin/java/util/stream/BaseStream#close()` after its contents have been placed downstream. (If a mapped stream is `null` an empty stream is used, instead.)

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `<U>` | type of elements accepted by downstream collector |
| `<A>` | intermediate accumulation type of the downstream collector |
| --- | --- |
| `<R>` | result type of collector |
| `mapper` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream)\<out U\>!\>!: a function to be applied to the input elements, which returns a stream of results |
| `downstream` | [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<in U, A, R\>!: a collector which will receive the elements of the stream returned by mapper |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, R>!` | a collector which applies the mapping function to the input elements and provides the flat mapped results to the downstream collector |

### groupingBy

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!, K : Any!> groupingBy(classifier: Function<in T, out K>!): Collector<T, *, MutableMap<K, MutableList<T>!>!>!
```

Returns a `Collector` implementing a "group by" operation on input elements of type `T`, grouping elements according to a classification function, and returning the results in a `Map`.

The classification function maps elements to some key type `K`. The collector produces a `Map<K, List<T>>` whose keys are the values resulting from applying the classification function to the input elements, and whose corresponding values are `List`s containing the input elements which map to the associated key under the classification function.

There are no guarantees on the type, mutability, serializability, or thread-safety of the `Map` or `List` objects returned.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `<K>` | the type of the keys |
| `classifier` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out K\>!: the classifier function mapping input elements to keys |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<K, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<T>!>!>!` | a `Collector` implementing the group-by operation |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#groupingBy(java.util.function.Function,%20java.util.stream.Collector)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#groupingBy(java.util.function.Function,%20java.util.function.Supplier,%20java.util.stream.Collector)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#groupingByConcurrent(java.util.function.Function)`

### groupingBy

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!, K : Any!, D : Any!, A : Any!, M : MutableMap<K, D>!> groupingBy(
    classifier: Function<in T, out K>!, 
    mapFactory: Supplier<M>!, 
    downstream: Collector<in T, A, D>!
): Collector<T, *, M>!
```

Returns a `Collector` implementing a cascaded "group by" operation on input elements of type `T`, grouping elements according to a classification function, and then performing a reduction operation on the values associated with a given key using the specified downstream `Collector`. The `Map` produced by the Collector is created with the supplied factory function.

The classification function maps elements to some key type `K`. The downstream collector operates on elements of type `T` and produces a result of type `D`. The resulting collector produces a `Map<K, D>`.

For example, to compute the set of last names of people in each city, where the city names are sorted:

```kotlin
<code>Map&lt;City, Set&lt;String&gt;&gt; namesByCity
    = people.stream().collect(
      groupingBy(Person::getCity,
                 TreeMap::new,
                 mapping(Person::getLastName,
                         toSet())));
  </code>
```

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `<K>` | the type of the keys |
| `<D>` | the result type of the downstream reduction |
| --- | --- |
| `<A>` | the intermediate accumulation type of the downstream collector |
| `<M>` | the type of the resulting `Map` |
| `classifier` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out K\>!: a classifier function mapping input elements to keys |
| --- | --- |
| `mapFactory` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\<M\>!: a supplier providing a new empty `Map` into which the results will be inserted |
| `downstream` | [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<in T, A, D\>!: a `Collector` implementing the downstream reduction |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, M>!` | a `Collector` implementing the cascaded group-by operation |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#groupingBy(java.util.function.Function,%20java.util.stream.Collector)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#groupingBy(java.util.function.Function)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#groupingByConcurrent(java.util.function.Function,%20java.util.function.Supplier,%20java.util.stream.Collector)`

### groupingBy

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!, K : Any!, A : Any!, D : Any!> groupingBy(
    classifier: Function<in T, out K>!, 
    downstream: Collector<in T, A, D>!
): Collector<T, *, MutableMap<K, D>!>!
```

Returns a `Collector` implementing a cascaded "group by" operation on input elements of type `T`, grouping elements according to a classification function, and then performing a reduction operation on the values associated with a given key using the specified downstream `Collector`.

The classification function maps elements to some key type `K`. The downstream collector operates on elements of type `T` and produces a result of type `D`. The resulting collector produces a `Map<K, D>`.

There are no guarantees on the type, mutability, serializability, or thread-safety of the `Map` returned.

For example, to compute the set of last names of people in each city:

```kotlin
<code>Map&lt;City, Set&lt;String&gt;&gt; namesByCity
    = people.stream().collect(
      groupingBy(Person::getCity,
                 mapping(Person::getLastName,
                         toSet())));
  </code>
```

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `<K>` | the type of the keys |
| `<A>` | the intermediate accumulation type of the downstream collector |
| --- | --- |
| `<D>` | the result type of the downstream reduction |
| `classifier` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out K\>!: a classifier function mapping input elements to keys |
| `downstream` | [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<in T, A, D\>!: a `Collector` implementing the downstream reduction |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<K, D>!>!` | a `Collector` implementing the cascaded group-by operation |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#groupingBy(java.util.function.Function)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#groupingBy(java.util.function.Function,%20java.util.function.Supplier,%20java.util.stream.Collector)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#groupingByConcurrent(java.util.function.Function,%20java.util.stream.Collector)`

### groupingByConcurrent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!, K : Any!> groupingByConcurrent(classifier: Function<in T, out K>!): Collector<T, *, ConcurrentMap<K, MutableList<T>!>!>!
```

Returns a concurrent `Collector` implementing a "group by" operation on input elements of type `T`, grouping elements according to a classification function.

This is a `https://developer.android.com/reference/kotlin/java/util/stream/Collector.Characteristics` and `https://developer.android.com/reference/kotlin/java/util/stream/Collector.Characteristics` Collector.

The classification function maps elements to some key type `K`. The collector produces a `ConcurrentMap<K, List<T>>` whose keys are the values resulting from applying the classification function to the input elements, and whose corresponding values are `List`s containing the input elements which map to the associated key under the classification function.

There are no guarantees on the type, mutability, or serializability of the `ConcurrentMap` or `List` objects returned, or of the thread-safety of the `List` objects returned.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `<K>` | the type of the keys |
| `classifier` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out K\>!: a classifier function mapping input elements to keys |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentMap.html#<K, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<T>!>!>!` | a concurrent, unordered `Collector` implementing the group-by operation |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#groupingBy(java.util.function.Function)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#groupingByConcurrent(java.util.function.Function,%20java.util.stream.Collector)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#groupingByConcurrent(java.util.function.Function,%20java.util.function.Supplier,%20java.util.stream.Collector)`

### groupingByConcurrent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!, K : Any!, A : Any!, D : Any!, M : ConcurrentMap<K, D>!> groupingByConcurrent(
    classifier: Function<in T, out K>!, 
    mapFactory: Supplier<M>!, 
    downstream: Collector<in T, A, D>!
): Collector<T, *, M>!
```

Returns a concurrent `Collector` implementing a cascaded "group by" operation on input elements of type `T`, grouping elements according to a classification function, and then performing a reduction operation on the values associated with a given key using the specified downstream `Collector`. The `ConcurrentMap` produced by the Collector is created with the supplied factory function.

This is a `https://developer.android.com/reference/kotlin/java/util/stream/Collector.Characteristics` and `https://developer.android.com/reference/kotlin/java/util/stream/Collector.Characteristics` Collector.

The classification function maps elements to some key type `K`. The downstream collector operates on elements of type `T` and produces a result of type `D`. The resulting collector produces a `ConcurrentMap<K, D>`.

For example, to compute the set of last names of people in each city, where the city names are sorted:

```kotlin
<code>ConcurrentMap&lt;City, Set&lt;String&gt;&gt; namesByCity
    = people.stream().collect(
      groupingByConcurrent(Person::getCity,
                           ConcurrentSkipListMap::new,
                           mapping(Person::getLastName,
                                   toSet())));
  </code>
```

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `<K>` | the type of the keys |
| `<A>` | the intermediate accumulation type of the downstream collector |
| --- | --- |
| `<D>` | the result type of the downstream reduction |
| `<M>` | the type of the resulting `ConcurrentMap` |
| `classifier` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out K\>!: a classifier function mapping input elements to keys |
| --- | --- |
| `mapFactory` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\<M\>!: a supplier providing a new empty `ConcurrentMap` into which the results will be inserted |
| `downstream` | [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<in T, A, D\>!: a `Collector` implementing the downstream reduction |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, M>!` | a concurrent, unordered `Collector` implementing the cascaded group-by operation |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#groupingByConcurrent(java.util.function.Function)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#groupingByConcurrent(java.util.function.Function,%20java.util.stream.Collector)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#groupingBy(java.util.function.Function,%20java.util.function.Supplier,%20java.util.stream.Collector)`

### groupingByConcurrent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!, K : Any!, A : Any!, D : Any!> groupingByConcurrent(
    classifier: Function<in T, out K>!, 
    downstream: Collector<in T, A, D>!
): Collector<T, *, ConcurrentMap<K, D>!>!
```

Returns a concurrent `Collector` implementing a cascaded "group by" operation on input elements of type `T`, grouping elements according to a classification function, and then performing a reduction operation on the values associated with a given key using the specified downstream `Collector`.

This is a `https://developer.android.com/reference/kotlin/java/util/stream/Collector.Characteristics` and `https://developer.android.com/reference/kotlin/java/util/stream/Collector.Characteristics` Collector.

The classification function maps elements to some key type `K`. The downstream collector operates on elements of type `T` and produces a result of type `D`. The resulting collector produces a `ConcurrentMap<K, D>`.

There are no guarantees on the type, mutability, or serializability of the `ConcurrentMap` returned.

For example, to compute the set of last names of people in each city, where the city names are sorted:

```kotlin
<code>ConcurrentMap&lt;City, Set&lt;String&gt;&gt; namesByCity
    = people.stream().collect(
      groupingByConcurrent(Person::getCity,
                           mapping(Person::getLastName,
                                   toSet())));
  </code>
```

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `<K>` | the type of the keys |
| `<A>` | the intermediate accumulation type of the downstream collector |
| --- | --- |
| `<D>` | the result type of the downstream reduction |
| `classifier` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out K\>!: a classifier function mapping input elements to keys |
| `downstream` | [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<in T, A, D\>!: a `Collector` implementing the downstream reduction |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentMap.html#<K, D>!>!` | a concurrent, unordered `Collector` implementing the cascaded group-by operation |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#groupingBy(java.util.function.Function,%20java.util.stream.Collector)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#groupingByConcurrent(java.util.function.Function)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#groupingByConcurrent(java.util.function.Function,%20java.util.function.Supplier,%20java.util.stream.Collector)`

### joining

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun joining(): Collector<CharSequence!, *, String!>!
```

Returns a `Collector` that concatenates the input elements into a `String`, in encounter order.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, *, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | a `Collector` that concatenates the input elements into a `String`, in encounter order |

### joining

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun joining(delimiter: CharSequence!): Collector<CharSequence!, *, String!>!
```

Returns a `Collector` that concatenates the input elements, separated by the specified delimiter, in encounter order.

| Parameters ||
|---|---|
| `delimiter` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the delimiter to be used between each element |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, *, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | A `Collector` which concatenates CharSequence elements, separated by the specified delimiter, in encounter order |

### joining

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun joining(
    delimiter: CharSequence!, 
    prefix: CharSequence!, 
    suffix: CharSequence!
): Collector<CharSequence!, *, String!>!
```

Returns a `Collector` that concatenates the input elements, separated by the specified delimiter, with the specified prefix and suffix, in encounter order.

| Parameters ||
|---|---|
| `delimiter` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the delimiter to be used between each element |
| `prefix` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the sequence of characters to be used at the beginning of the joined result |
| `suffix` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the sequence of characters to be used at the end of the joined result |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, *, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | A `Collector` which concatenates CharSequence elements, separated by the specified delimiter, in encounter order |

### mapping

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!, U : Any!, A : Any!, R : Any!> mapping(
    mapper: Function<in T, out U>!, 
    downstream: Collector<in U, A, R>!
): Collector<T, *, R>!
```

Adapts a `Collector` accepting elements of type `U` to one accepting elements of type `T` by applying a mapping function to each input element before accumulation.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `<U>` | type of elements accepted by downstream collector |
| `<A>` | intermediate accumulation type of the downstream collector |
| --- | --- |
| `<R>` | result type of collector |
| `mapper` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out U\>!: a function to be applied to the input elements |
| `downstream` | [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<in U, A, R\>!: a collector which will accept mapped values |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, R>!` | a collector which applies the mapping function to the input elements and provides the mapped results to the downstream collector |

### maxBy

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> maxBy(comparator: Comparator<in T>!): Collector<T, *, Optional<T>!>!
```

Returns a `Collector` that produces the maximal element according to a given `Comparator`, described as an `Optional<T>`.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `comparator` | [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator.html#)\<in T\>!: a `Comparator` for comparing elements |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://developer.android.com/reference/kotlin/java/util/Optional.html#<T>!>!` | a `Collector` that produces the maximal value |

### minBy

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> minBy(comparator: Comparator<in T>!): Collector<T, *, Optional<T>!>!
```

Returns a `Collector` that produces the minimal element according to a given `Comparator`, described as an `Optional<T>`.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `comparator` | [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator.html#)\<in T\>!: a `Comparator` for comparing elements |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://developer.android.com/reference/kotlin/java/util/Optional.html#<T>!>!` | a `Collector` that produces the minimal value |

### partitioningBy

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> partitioningBy(predicate: Predicate<in T>!): Collector<T, *, MutableMap<Boolean!, MutableList<T>!>!>!
```

Returns a `Collector` which partitions the input elements according to a `Predicate`, and organizes them into a `Map<Boolean, List<T>>`. The returned `Map` always contains mappings for both `false` and `true` keys. There are no guarantees on the type, mutability, serializability, or thread-safety of the `Map` or `List` returned.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `predicate` | [Predicate](https://developer.android.com/reference/kotlin/java/util/function/Predicate.html#)\<in T\>!: a predicate used for classifying input elements |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<T>!>!>!` | a `Collector` implementing the partitioning operation |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#partitioningBy(java.util.function.Predicate,%20java.util.stream.Collector)`

### partitioningBy

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!, D : Any!, A : Any!> partitioningBy(
    predicate: Predicate<in T>!, 
    downstream: Collector<in T, A, D>!
): Collector<T, *, MutableMap<Boolean!, D>!>!
```

Returns a `Collector` which partitions the input elements according to a `Predicate`, reduces the values in each partition according to another `Collector`, and organizes them into a `Map<Boolean, D>` whose values are the result of the downstream reduction.

The returned `Map` always contains mappings for both `false` and `true` keys. There are no guarantees on the type, mutability, serializability, or thread-safety of the `Map` returned.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `<D>` | the result type of the downstream reduction |
| `<A>` | the intermediate accumulation type of the downstream collector |
| --- | --- |
| `predicate` | [Predicate](https://developer.android.com/reference/kotlin/java/util/function/Predicate.html#)\<in T\>!: a predicate used for classifying input elements |
| `downstream` | [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<in T, A, D\>!: a `Collector` implementing the downstream reduction |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!, D>!>!` | a `Collector` implementing the cascaded partitioning operation |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#partitioningBy(java.util.function.Predicate)`

### reducing

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> reducing(op: BinaryOperator<T>!): Collector<T, *, Optional<T>!>!
```

Returns a `Collector` which performs a reduction of its input elements under a specified `BinaryOperator`. The result is described as an `Optional<T>`.

| Parameters ||
|---|---|
| `<T>` | element type for the input and output of the reduction |
| `op` | [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#)\<T\>!: a `BinaryOperator<T>` used to reduce the input elements |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://developer.android.com/reference/kotlin/java/util/Optional.html#<T>!>!` | a `Collector` which implements the reduction operation |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#reducing(java.util.stream.Collectors.reducing.T,%20java.util.function.BinaryOperator)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#reducing(java.util.stream.Collectors.reducing.U,%20java.util.function.Function,%20java.util.function.BinaryOperator)`

### reducing

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> reducing(
    identity: T, 
    op: BinaryOperator<T>!
): Collector<T, *, T>!
```

Returns a `Collector` which performs a reduction of its input elements under a specified `BinaryOperator` using the provided identity.

| Parameters ||
|---|---|
| `<T>` | element type for the input and output of the reduction |
| `identity` | T: the identity value for the reduction (also, the value that is returned when there are no input elements) |
| `op` | [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#)\<T\>!: a `BinaryOperator<T>` used to reduce the input elements |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, T>!` | a `Collector` which implements the reduction operation |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#reducing(java.util.function.BinaryOperator)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#reducing(java.util.stream.Collectors.reducing.U,%20java.util.function.Function,%20java.util.function.BinaryOperator)`

### reducing

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!, U : Any!> reducing(
    identity: U, 
    mapper: Function<in T, out U>!, 
    op: BinaryOperator<U>!
): Collector<T, *, U>!
```

Returns a `Collector` which performs a reduction of its input elements under a specified mapping function and `BinaryOperator`. This is a generalization of `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#reducing(java.util.stream.Collectors.reducing.T,%20java.util.function.BinaryOperator)` which allows a transformation of the elements before reduction.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `<U>` | the type of the mapped values |
| `identity` | U: the identity value for the reduction (also, the value that is returned when there are no input elements) |
| --- | --- |
| `mapper` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out U\>!: a mapping function to apply to each input value |
| `op` | [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#)\<U\>!: a `BinaryOperator<U>` used to reduce the mapped values |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, U>!` | a `Collector` implementing the map-reduce operation |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#reducing(java.util.stream.Collectors.reducing.T,%20java.util.function.BinaryOperator)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#reducing(java.util.function.BinaryOperator)`

### summarizingDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> summarizingDouble(mapper: ToDoubleFunction<in T>!): Collector<T, *, DoubleSummaryStatistics!>!
```

Returns a `Collector` which applies an `double`-producing mapping function to each input element, and returns summary statistics for the resulting values.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `mapper` | [ToDoubleFunction](https://developer.android.com/reference/kotlin/java/util/function/ToDoubleFunction.html#)\<in T\>!: a mapping function to apply to each element |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://developer.android.com/reference/kotlin/java/util/DoubleSummaryStatistics.html#!>!` | a `Collector` implementing the summary-statistics reduction |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#summarizingLong(java.util.function.ToLongFunction)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#summarizingInt(java.util.function.ToIntFunction)`

### summarizingInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> summarizingInt(mapper: ToIntFunction<in T>!): Collector<T, *, IntSummaryStatistics!>!
```

Returns a `Collector` which applies an `int`-producing mapping function to each input element, and returns summary statistics for the resulting values.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `mapper` | [ToIntFunction](https://developer.android.com/reference/kotlin/java/util/function/ToIntFunction.html#)\<in T\>!: a mapping function to apply to each element |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://developer.android.com/reference/kotlin/java/util/IntSummaryStatistics.html#!>!` | a `Collector` implementing the summary-statistics reduction |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#summarizingDouble(java.util.function.ToDoubleFunction)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#summarizingLong(java.util.function.ToLongFunction)`

### summarizingLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> summarizingLong(mapper: ToLongFunction<in T>!): Collector<T, *, LongSummaryStatistics!>!
```

Returns a `Collector` which applies an `long`-producing mapping function to each input element, and returns summary statistics for the resulting values.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `mapper` | [ToLongFunction](https://developer.android.com/reference/kotlin/java/util/function/ToLongFunction.html#)\<in T\>!: the mapping function to apply to each element |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://developer.android.com/reference/kotlin/java/util/LongSummaryStatistics.html#!>!` | a `Collector` implementing the summary-statistics reduction |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#summarizingDouble(java.util.function.ToDoubleFunction)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#summarizingInt(java.util.function.ToIntFunction)`

### summingDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> summingDouble(mapper: ToDoubleFunction<in T>!): Collector<T, *, Double!>!
```

Returns a `Collector` that produces the sum of a double-valued function applied to the input elements. If no elements are present, the result is 0.

The sum returned can vary depending upon the order in which values are recorded, due to accumulated rounding error in addition of values of differing magnitudes. Values sorted by increasing absolute magnitude tend to yield more accurate results. If any recorded value is a `NaN` or the sum is at any point a `NaN` then the sum will be `NaN`.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `mapper` | [ToDoubleFunction](https://developer.android.com/reference/kotlin/java/util/function/ToDoubleFunction.html#)\<in T\>!: a function extracting the property to be summed |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html!>!` | a `Collector` that produces the sum of a derived property |

### summingInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> summingInt(mapper: ToIntFunction<in T>!): Collector<T, *, Int!>!
```

Returns a `Collector` that produces the sum of an integer-valued function applied to the input elements. If no elements are present, the result is 0.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `mapper` | [ToIntFunction](https://developer.android.com/reference/kotlin/java/util/function/ToIntFunction.html#)\<in T\>!: a function extracting the property to be summed |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>!` | a `Collector` that produces the sum of a derived property |

### summingLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> summingLong(mapper: ToLongFunction<in T>!): Collector<T, *, Long!>!
```

Returns a `Collector` that produces the sum of a long-valued function applied to the input elements. If no elements are present, the result is 0.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `mapper` | [ToLongFunction](https://developer.android.com/reference/kotlin/java/util/function/ToLongFunction.html#)\<in T\>!: a function extracting the property to be summed |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html!>!` | a `Collector` that produces the sum of a derived property |

### teeing

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!, R1 : Any!, R2 : Any!, R : Any!> teeing(
    downstream1: Collector<in T, *, R1>!, 
    downstream2: Collector<in T, *, R2>!, 
    merger: BiFunction<in R1, in R2, R>!
): Collector<T, *, R>!
```

Returns a `Collector` that is a composite of two downstream collectors. Every element passed to the resulting collector is processed by both downstream collectors, then their results are merged using the specified merge function into the final result.

The resulting collector functions do the following:

- supplier: creates a result container that contains result containers obtained by calling each collector's supplier
- accumulator: calls each collector's accumulator with its result container and the input element
- combiner: calls each collector's combiner with two result containers
- finisher: calls each collector's finisher with its result container, then calls the supplied merger and returns its result.

The resulting collector is `https://developer.android.com/reference/kotlin/java/util/stream/Collector.Characteristics` if both downstream collectors are unordered and `https://developer.android.com/reference/kotlin/java/util/stream/Collector.Characteristics` if both downstream collectors are concurrent.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `<R1>` | the result type of the first collector |
| `<R2>` | the result type of the second collector |
| --- | --- |
| `<R>` | the final result type |
| `downstream1` | [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<in T, \*, R1\>!: the first downstream collector |
| `downstream2` | [Collector](https://developer.android.com/reference/kotlin/java/util/stream/Collector)\<in T, \*, R2\>!: the second downstream collector |
| --- | --- |
| `merger` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)\<in R1, in R2, R\>!: the function which merges two results into the single one |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, R>!` | a `Collector` which aggregates the results of two supplied collectors. |

### toCollection

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!, C : MutableCollection<T>!> toCollection(collectionFactory: Supplier<C>!): Collector<T, *, C>!
```

Returns a `Collector` that accumulates the input elements into a new `Collection`, in encounter order. The `Collection` is created by the provided factory.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `<C>` | the type of the resulting `Collection` |
| `collectionFactory` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\<C\>!: a supplier providing a new empty `Collection` into which the results will be inserted |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, C>!` | a `Collector` which collects all the input elements into a `Collection`, in encounter order |

### toConcurrentMap

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!, K : Any!, U : Any!> toConcurrentMap(
    keyMapper: Function<in T, out K>!, 
    valueMapper: Function<in T, out U>!
): Collector<T, *, ConcurrentMap<K, U>!>!
```

Returns a concurrent `Collector` that accumulates elements into a `ConcurrentMap` whose keys and values are the result of applying the provided mapping functions to the input elements.

If the mapped keys contain duplicates (according to `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)`), an `IllegalStateException` is thrown when the collection operation is performed. If the mapped keys may have duplicates, use `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toConcurrentMap(java.util.function.Function,%20java.util.function.Function,%20java.util.function.BinaryOperator)` instead.

There are no guarantees on the type, mutability, or serializability of the `ConcurrentMap` returned.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `<K>` | the output type of the key mapping function |
| `<U>` | the output type of the value mapping function |
| --- | --- |
| `keyMapper` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out K\>!: the mapping function to produce keys |
| `valueMapper` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out U\>!: the mapping function to produce values |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentMap.html#<K, U>!>!` | a concurrent, unordered `Collector` which collects elements into a `ConcurrentMap` whose keys are the result of applying a key mapping function to the input elements, and whose values are the result of applying a value mapping function to the input elements |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toMap(java.util.function.Function,%20java.util.function.Function)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toConcurrentMap(java.util.function.Function,%20java.util.function.Function,%20java.util.function.BinaryOperator)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toConcurrentMap(java.util.function.Function,%20java.util.function.Function,%20java.util.function.BinaryOperator,%20java.util.function.Supplier)`

### toConcurrentMap

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!, K : Any!, U : Any!> toConcurrentMap(
    keyMapper: Function<in T, out K>!, 
    valueMapper: Function<in T, out U>!, 
    mergeFunction: BinaryOperator<U>!
): Collector<T, *, ConcurrentMap<K, U>!>!
```

Returns a concurrent `Collector` that accumulates elements into a `ConcurrentMap` whose keys and values are the result of applying the provided mapping functions to the input elements.

If the mapped keys contain duplicates (according to `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)`), the value mapping function is applied to each equal element, and the results are merged using the provided merging function.

There are no guarantees on the type, mutability, or serializability of the `ConcurrentMap` returned.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `<K>` | the output type of the key mapping function |
| `<U>` | the output type of the value mapping function |
| --- | --- |
| `keyMapper` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out K\>!: a mapping function to produce keys |
| `valueMapper` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out U\>!: a mapping function to produce values |
| `mergeFunction` | [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#)\<U\>!: a merge function, used to resolve collisions between values associated with the same key, as supplied to `https://developer.android.com/reference/kotlin/java/util/Map.html#merge(java.util.Map.K,%20java.util.Map.V,%20java.util.function.BiFunction)` |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentMap.html#<K, U>!>!` | a concurrent, unordered `Collector` which collects elements into a `ConcurrentMap` whose keys are the result of applying a key mapping function to the input elements, and whose values are the result of applying a value mapping function to all input elements equal to the key and combining them using the merge function |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toConcurrentMap(java.util.function.Function,%20java.util.function.Function)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toConcurrentMap(java.util.function.Function,%20java.util.function.Function,%20java.util.function.BinaryOperator,%20java.util.function.Supplier)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toMap(java.util.function.Function,%20java.util.function.Function,%20java.util.function.BinaryOperator)`

### toConcurrentMap

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!, K : Any!, U : Any!, M : ConcurrentMap<K, U>!> toConcurrentMap(
    keyMapper: Function<in T, out K>!, 
    valueMapper: Function<in T, out U>!, 
    mergeFunction: BinaryOperator<U>!, 
    mapFactory: Supplier<M>!
): Collector<T, *, M>!
```

Returns a concurrent `Collector` that accumulates elements into a `ConcurrentMap` whose keys and values are the result of applying the provided mapping functions to the input elements.

If the mapped keys contain duplicates (according to `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)`), the value mapping function is applied to each equal element, and the results are merged using the provided merging function. The `ConcurrentMap` is created by a provided supplier function.

This is a `https://developer.android.com/reference/kotlin/java/util/stream/Collector.Characteristics` and `https://developer.android.com/reference/kotlin/java/util/stream/Collector.Characteristics` Collector.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `<K>` | the output type of the key mapping function |
| `<U>` | the output type of the value mapping function |
| --- | --- |
| `<M>` | the type of the resulting `ConcurrentMap` |
| `keyMapper` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out K\>!: a mapping function to produce keys |
| `valueMapper` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out U\>!: a mapping function to produce values |
| --- | --- |
| `mergeFunction` | [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#)\<U\>!: a merge function, used to resolve collisions between values associated with the same key, as supplied to `https://developer.android.com/reference/kotlin/java/util/Map.html#merge(java.util.Map.K,%20java.util.Map.V,%20java.util.function.BiFunction)` |
| `mapFactory` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\<M\>!: a supplier providing a new empty `ConcurrentMap` into which the results will be inserted |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, M>!` | a concurrent, unordered `Collector` which collects elements into a `ConcurrentMap` whose keys are the result of applying a key mapping function to the input elements, and whose values are the result of applying a value mapping function to all input elements equal to the key and combining them using the merge function |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toConcurrentMap(java.util.function.Function,%20java.util.function.Function)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toConcurrentMap(java.util.function.Function,%20java.util.function.Function,%20java.util.function.BinaryOperator)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toMap(java.util.function.Function,%20java.util.function.Function,%20java.util.function.BinaryOperator,%20java.util.function.Supplier)`

### toList

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> toList(): Collector<T, *, MutableList<T>!>!
```

Returns a `Collector` that accumulates the input elements into a new `List`. There are no guarantees on the type, mutability, serializability, or thread-safety of the `List` returned; if more control over the returned `List` is required, use `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toCollection(java.util.function.Supplier)`.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<T>!>!` | a `Collector` which collects all the input elements into a `List`, in encounter order |

### toMap

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!, K : Any!, U : Any!> toMap(
    keyMapper: Function<in T, out K>!, 
    valueMapper: Function<in T, out U>!
): Collector<T, *, MutableMap<K, U>!>!
```

Returns a `Collector` that accumulates elements into a `Map` whose keys and values are the result of applying the provided mapping functions to the input elements.

If the mapped keys contain duplicates (according to `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)`), an `IllegalStateException` is thrown when the collection operation is performed. If the mapped keys might have duplicates, use `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toMap(java.util.function.Function,%20java.util.function.Function,%20java.util.function.BinaryOperator)` instead.

There are no guarantees on the type, mutability, serializability, or thread-safety of the `Map` returned.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `<K>` | the output type of the key mapping function |
| `<U>` | the output type of the value mapping function |
| --- | --- |
| `keyMapper` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out K\>!: a mapping function to produce keys |
| `valueMapper` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out U\>!: a mapping function to produce values |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<K, U>!>!` | a `Collector` which collects elements into a `Map` whose keys and values are the result of applying mapping functions to the input elements |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toMap(java.util.function.Function,%20java.util.function.Function,%20java.util.function.BinaryOperator)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toMap(java.util.function.Function,%20java.util.function.Function,%20java.util.function.BinaryOperator,%20java.util.function.Supplier)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toConcurrentMap(java.util.function.Function,%20java.util.function.Function)`

### toMap

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!, K : Any!, U : Any!> toMap(
    keyMapper: Function<in T, out K>!, 
    valueMapper: Function<in T, out U>!, 
    mergeFunction: BinaryOperator<U>!
): Collector<T, *, MutableMap<K, U>!>!
```

Returns a `Collector` that accumulates elements into a `Map` whose keys and values are the result of applying the provided mapping functions to the input elements.

If the mapped keys contain duplicates (according to `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)`), the value mapping function is applied to each equal element, and the results are merged using the provided merging function.

There are no guarantees on the type, mutability, serializability, or thread-safety of the `Map` returned.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `<K>` | the output type of the key mapping function |
| `<U>` | the output type of the value mapping function |
| --- | --- |
| `keyMapper` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out K\>!: a mapping function to produce keys |
| `valueMapper` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out U\>!: a mapping function to produce values |
| `mergeFunction` | [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#)\<U\>!: a merge function, used to resolve collisions between values associated with the same key, as supplied to `https://developer.android.com/reference/kotlin/java/util/Map.html#merge(java.util.Map.K,%20java.util.Map.V,%20java.util.function.BiFunction)` |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<K, U>!>!` | a `Collector` which collects elements into a `Map` whose keys are the result of applying a key mapping function to the input elements, and whose values are the result of applying a value mapping function to all input elements equal to the key and combining them using the merge function |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toMap(java.util.function.Function,%20java.util.function.Function)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toMap(java.util.function.Function,%20java.util.function.Function,%20java.util.function.BinaryOperator,%20java.util.function.Supplier)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toConcurrentMap(java.util.function.Function,%20java.util.function.Function,%20java.util.function.BinaryOperator)`

### toMap

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!, K : Any!, U : Any!, M : MutableMap<K, U>!> toMap(
    keyMapper: Function<in T, out K>!, 
    valueMapper: Function<in T, out U>!, 
    mergeFunction: BinaryOperator<U>!, 
    mapFactory: Supplier<M>!
): Collector<T, *, M>!
```

Returns a `Collector` that accumulates elements into a `Map` whose keys and values are the result of applying the provided mapping functions to the input elements.

If the mapped keys contain duplicates (according to `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)`), the value mapping function is applied to each equal element, and the results are merged using the provided merging function. The `Map` is created by a provided supplier function.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `<K>` | the output type of the key mapping function |
| `<U>` | the output type of the value mapping function |
| --- | --- |
| `<M>` | the type of the resulting `Map` |
| `keyMapper` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out K\>!: a mapping function to produce keys |
| `valueMapper` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out U\>!: a mapping function to produce values |
| --- | --- |
| `mergeFunction` | [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#)\<U\>!: a merge function, used to resolve collisions between values associated with the same key, as supplied to `https://developer.android.com/reference/kotlin/java/util/Map.html#merge(java.util.Map.K,%20java.util.Map.V,%20java.util.function.BiFunction)` |
| `mapFactory` | [Supplier](https://developer.android.com/reference/kotlin/java/util/function/Supplier.html#)\<M\>!: a supplier providing a new empty `Map` into which the results will be inserted |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, M>!` | a `Collector` which collects elements into a `Map` whose keys are the result of applying a key mapping function to the input elements, and whose values are the result of applying a value mapping function to all input elements equal to the key and combining them using the merge function |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toMap(java.util.function.Function,%20java.util.function.Function)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toMap(java.util.function.Function,%20java.util.function.Function,%20java.util.function.BinaryOperator)`
- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toConcurrentMap(java.util.function.Function,%20java.util.function.Function,%20java.util.function.BinaryOperator,%20java.util.function.Supplier)`

### toSet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> toSet(): Collector<T, *, MutableSet<T>!>!
```

Returns a `Collector` that accumulates the input elements into a new `Set`. There are no guarantees on the type, mutability, serializability, or thread-safety of the `Set` returned; if more control over the returned `Set` is required, use `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toCollection(java.util.function.Supplier)`.

This is an `https://developer.android.com/reference/kotlin/java/util/stream/Collector.Characteristics` Collector.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<T>!>!` | a `Collector` which collects all the input elements into a `Set` |

### toUnmodifiableList

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> toUnmodifiableList(): Collector<T, *, MutableList<T>!>!
```

Returns a `Collector` that accumulates the input elements into an [unmodifiable List](https://developer.android.com/reference/kotlin/java/util/List.html#unmodifiable) in encounter order. The returned Collector disallows null values and will throw `NullPointerException` if it is presented with a null value.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<T>!>!` | a `Collector` that accumulates the input elements into an [unmodifiable List](https://developer.android.com/reference/kotlin/java/util/List.html#unmodifiable) in encounter order |

### toUnmodifiableMap

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!, K : Any!, U : Any!> toUnmodifiableMap(
    keyMapper: Function<in T, out K>!, 
    valueMapper: Function<in T, out U>!
): Collector<T, *, MutableMap<K, U>!>!
```

Returns a `Collector` that accumulates the input elements into an [unmodifiable Map](https://developer.android.com/reference/kotlin/java/util/Map.html#unmodifiable), whose keys and values are the result of applying the provided mapping functions to the input elements.

If the mapped keys contain duplicates (according to `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)`), an `IllegalStateException` is thrown when the collection operation is performed. If the mapped keys might have duplicates, use `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toUnmodifiableMap(java.util.function.Function,%20java.util.function.Function,%20java.util.function.BinaryOperator)` to handle merging of the values.

The returned Collector disallows null keys and values. If either mapping function returns null, `NullPointerException` will be thrown.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `<K>` | the output type of the key mapping function |
| `<U>` | the output type of the value mapping function |
| --- | --- |
| `keyMapper` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out K\>!: a mapping function to produce keys, must be non-null |
| `valueMapper` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out U\>!: a mapping function to produce values, must be non-null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<K, U>!>!` | a `Collector` that accumulates the input elements into an [unmodifiable Map](https://developer.android.com/reference/kotlin/java/util/Map.html#unmodifiable), whose keys and values are the result of applying the provided mapping functions to the input elements |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if either keyMapper or valueMapper is null |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toUnmodifiableMap(java.util.function.Function,%20java.util.function.Function,%20java.util.function.BinaryOperator)`

### toUnmodifiableMap

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!, K : Any!, U : Any!> toUnmodifiableMap(
    keyMapper: Function<in T, out K>!, 
    valueMapper: Function<in T, out U>!, 
    mergeFunction: BinaryOperator<U>!
): Collector<T, *, MutableMap<K, U>!>!
```

Returns a `Collector` that accumulates the input elements into an [unmodifiable Map](https://developer.android.com/reference/kotlin/java/util/Map.html#unmodifiable), whose keys and values are the result of applying the provided mapping functions to the input elements.

If the mapped keys contain duplicates (according to `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)`), the value mapping function is applied to each equal element, and the results are merged using the provided merging function.

The returned Collector disallows null keys and values. If either mapping function returns null, `NullPointerException` will be thrown.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |
| `<K>` | the output type of the key mapping function |
| `<U>` | the output type of the value mapping function |
| --- | --- |
| `keyMapper` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out K\>!: a mapping function to produce keys, must be non-null |
| `valueMapper` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<in T, out U\>!: a mapping function to produce values, must be non-null |
| `mergeFunction` | [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#)\<U\>!: a merge function, used to resolve collisions between values associated with the same key, as supplied to `https://developer.android.com/reference/kotlin/java/util/Map.html#merge(java.util.Map.K,%20java.util.Map.V,%20java.util.function.BiFunction)`, must be non-null |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<K, U>!>!` | a `Collector` that accumulates the input elements into an [unmodifiable Map](https://developer.android.com/reference/kotlin/java/util/Map.html#unmodifiable), whose keys and values are the result of applying the provided mapping functions to the input elements |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the keyMapper, valueMapper, or mergeFunction is null |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/stream/Collectors#toUnmodifiableMap(java.util.function.Function,%20java.util.function.Function)`

### toUnmodifiableSet

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> toUnmodifiableSet(): Collector<T, *, MutableSet<T>!>!
```

Returns a `Collector` that accumulates the input elements into an [unmodifiable Set](https://developer.android.com/reference/kotlin/java/util/Set.html#unmodifiable). The returned Collector disallows null values and will throw `NullPointerException` if it is presented with a null value. If the input contains duplicate elements, an arbitrary element of the duplicates is preserved.

This is an `https://developer.android.com/reference/kotlin/java/util/stream/Collector.Characteristics` Collector.

| Parameters ||
|---|---|
| `<T>` | the type of the input elements |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Collector<T, *, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<T>!>!` | a `Collector` that accumulates the input elements into an [unmodifiable Set](https://developer.android.com/reference/kotlin/java/util/Set.html#unmodifiable) |
