Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Comparator

```
@FunctionalInterface interface Comparator<T : Any!>
```

| [java.util.Comparator](Comparator.md) |

| Known Direct Subclasses [ApplicationInfo.DisplayNameComparator](../android/content/pm/ApplicationInfo.DisplayNameComparator.md), [Collator](../java.text/Collator.md), [Collator](../android.icu.text/Collator.md), [PackageItemInfo.DisplayNameComparator](../android/content/pm/PackageItemInfo.DisplayNameComparator.md), [ResolveInfo.DisplayNameComparator](../android/content/pm/ResolveInfo.DisplayNameComparator.md) |---|---| | [ApplicationInfo.DisplayNameComparator](../android/content/pm/ApplicationInfo.DisplayNameComparator.md) | <br /> | | [Collator](../java.text/Collator.md) | The `Collator` class performs locale-sensitive `String` comparison. | | [Collator](../android.icu.text/Collator.md) | **\[icu enhancement\]** ICU's replacement for `https://developer.android.com/reference/kotlin/java/text/Collator.html#`. | | [PackageItemInfo.DisplayNameComparator](../android/content/pm/PackageItemInfo.DisplayNameComparator.md) | <br /> | | [ResolveInfo.DisplayNameComparator](../android/content/pm/ResolveInfo.DisplayNameComparator.md) | <br /> | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [RuleBasedCollator](../java.text/RuleBasedCollator.md), [RuleBasedCollator](../android.icu.text/RuleBasedCollator.md) |---|---| | [RuleBasedCollator](../java.text/RuleBasedCollator.md) | The class is a concrete subclass of `Collator` that provides a simple, data-driven, table collator. | | [RuleBasedCollator](../android.icu.text/RuleBasedCollator.md) | RuleBasedCollator is a concrete subclass of Collator. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A comparison function, which imposes a *total ordering* on some collection of objects. Comparators can be passed to a sort method (such as sort or sort) to allow precise control over the sort order. Comparators can also be used to control the order of certain data structures (such as [sorted sets](SortedSet.md) or [sorted maps](SortedMap.md)), or to provide an ordering for collections of objects that don't have a [natural ordering](../java.lang/Comparable.md).

The ordering imposed by a comparator `c` on a set of elements `S` is said to be *consistent with equals* if and only if `c.compare(e1, e2)==0` has the same boolean value as `e1.equals(e2)` for every `e1` and `e2` in `S`.

Caution should be exercised when using a comparator capable of imposing an ordering inconsistent with equals to order a sorted set (or sorted map). Suppose a sorted set (or sorted map) with an explicit comparator `c` is used with elements (or keys) drawn from a set `S`. If the ordering imposed by `c` on `S` is inconsistent with equals, the sorted set (or sorted map) will behave "strangely." In particular the sorted set (or sorted map) will violate the general contract for set (or map), which is defined in terms of `equals`.

For example, suppose one adds two elements `a` and `b` such that `(a.equals(b) && c.compare(a, b) != 0)` to an empty `TreeSet` with comparator `c`. The second `add` operation will return true (and the size of the tree set will increase) because `a` and `b` are not equivalent from the tree set's perspective, even though this is contrary to the specification of the add method.

Note: It is generally a good idea for comparators to also implement `java.io.Serializable`, as they may be used as ordering methods in serializable data structures (like TreeSet, TreeMap). In order for the data structure to serialize successfully, the comparator (if provided) must implement `Serializable`.

For the mathematically inclined, the *relation* that defines the *imposed ordering* that a given comparator `c` imposes on a given set of objects `S` is:

```kotlin
{(x, y) such that c.compare(x, y) <= 0}.
  
```
The *quotient* for this total order is:

```kotlin
{(x, y) such that c.compare(x, y) == 0}.
  
```
It follows immediately from the contract for `compare` that the quotient is an *equivalence relation* on `S`, and that the imposed ordering is a *total order* on `S`. When we say that the ordering imposed by `c` on `S` is *consistent with equals* , we mean that the quotient for the ordering is the equivalence relation defined by the objects' equals method(s):

```kotlin
{(x, y) such that x.equals(y)}. 
```
In other words, when the imposed ordering is consistent with equals, the equivalence classes defined by the equivalence relation of the `equals` method and the equivalence classes defined by the quotient of the `compare` method are the same.

Unlike `Comparable`, a comparator may optionally permit comparison of null arguments, while maintaining the requirements for an equivalence relation.

This interface is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public methods ||
|---|---|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compare Compares its two arguments for order. |
| open static [Comparator](Comparator.md)\<T\>! | comparing Accepts a function that extracts a `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` sort key from a type `T`, and returns a `Comparator<T>` that compares by that sort key. |
| open static [Comparator](Comparator.md)\<T\>! | comparing Accepts a function that extracts a sort key from a type `T`, and returns a `Comparator<T>` that compares by that sort key using the specified Comparator. |
| --- | --- |
| open static [Comparator](Comparator.md)\<T\>! | comparingDouble Accepts a function that extracts a `double` sort key from a type `T`, and returns a `Comparator<T>` that compares by that sort key. |
| open static [Comparator](Comparator.md)\<T\>! | comparingInt Accepts a function that extracts an `int` sort key from a type `T`, and returns a `Comparator<T>` that compares by that sort key. |
| open static [Comparator](Comparator.md)\<T\>! | comparingLong Accepts a function that extracts a `long` sort key from a type `T`, and returns a `Comparator<T>` that compares by that sort key. |
| --- | --- |
| open static [Comparator](Comparator.md)\<T\>! | naturalOrder Returns a comparator that compares `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` objects in natural order. |
| open static [Comparator](Comparator.md)\<T\>! | nullsFirst Returns a null-friendly comparator that considers `null` to be less than non-null. |
| open static [Comparator](Comparator.md)\<T\>! | nullsLast Returns a null-friendly comparator that considers `null` to be greater than non-null. |
| --- | --- |
| open static [Comparator](Comparator.md)\<T\>! | reverseOrder Returns a comparator that imposes the reverse of the *natural ordering*. |
| open [Comparator](Comparator.md)\<T\>! | reversed Returns a comparator that imposes the reverse ordering of this comparator. |
| open [Comparator](Comparator.md)\<T\>! | thenComparing Returns a lexicographic-order comparator with another comparator. |
| --- | --- |
| open [Comparator](Comparator.md)\<T\>! | thenComparing Returns a lexicographic-order comparator with a function that extracts a `Comparable` sort key. |
| open [Comparator](Comparator.md)\<T\>! | thenComparing Returns a lexicographic-order comparator with a function that extracts a key to be compared with the given `Comparator`. |
| open [Comparator](Comparator.md)\<T\>! | thenComparingDouble Returns a lexicographic-order comparator with a function that extracts a `double` sort key. |
| --- | --- |
| open [Comparator](Comparator.md)\<T\>! | thenComparingInt Returns a lexicographic-order comparator with a function that extracts an `int` sort key. |
| open [Comparator](Comparator.md)\<T\>! | thenComparingLong Returns a lexicographic-order comparator with a function that extracts a `long` sort key. |

## Public methods

### compare

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun compare(
    o1: T, 
    o2: T
): Int
```

Compares its two arguments for order. Returns a negative integer, zero, or a positive integer as the first argument is less than, equal to, or greater than the second.

The implementor must ensure that signum`(compare(x, y)) == -signum(compare(y, x))` for all `x` and `y`. (This implies that `compare(x, y)` must throw an exception if and only if `compare(y, x)` throws an exception.)

The implementor must also ensure that the relation is transitive: `((compare(x, y)>0) && (compare(y, z)>0))` implies `compare(x, z)>0`.

Finally, the implementor must ensure that `compare(x, y)==0` implies that `signum(compare(x, z))==signum(compare(y, z))` for all `z`.

| Parameters ||
|---|---|
| `o1` | T: the first object to be compared. |
| `o2` | T: the second object to be compared. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a negative integer, zero, or a positive integer as the first argument is less than, equal to, or greater than the second. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the arguments' types prevent them from being compared by this comparator. |
| `java.lang.NullPointerException` | if an argument is null and this comparator does not permit null arguments |

### comparing

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <T : Any!, U : Comparable<U>!> comparing(keyExtractor: Function<in T, out U>!): Comparator<T>!
```

Accepts a function that extracts a `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` sort key from a type `T`, and returns a `Comparator<T>` that compares by that sort key.

The returned comparator is serializable if the specified function is also serializable.

| Parameters ||
|---|---|
| `<T>` | the type of element to be compared |
| `<U>` | the type of the `Comparable` sort key |
| `keyExtractor` | [Function](../java.util.function/Function.md)\<in T, out U\>!: the function used to extract the `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` sort key |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Comparator#<T>!` | a comparator that compares by an extracted key |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the argument is null |

### comparing

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <T : Any!, U : Any!> comparing(
    keyExtractor: Function<in T, out U>!, 
    keyComparator: Comparator<in U>!
): Comparator<T>!
```

Accepts a function that extracts a sort key from a type `T`, and returns a `Comparator<T>` that compares by that sort key using the specified Comparator.

The returned comparator is serializable if the specified function and comparator are both serializable.

| Parameters ||
|---|---|
| `<T>` | the type of element to be compared |
| `<U>` | the type of the sort key |
| `keyExtractor` | [Function](../java.util.function/Function.md)\<in T, out U\>!: the function used to extract the sort key |
| --- | --- |
| `keyComparator` | [Comparator](Comparator.md)\<in U\>!: the `Comparator` used to compare the sort key |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Comparator#<T>!` | a comparator that compares by an extracted key using the specified `Comparator` |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if either argument is null |

### comparingDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <T : Any!> comparingDouble(keyExtractor: ToDoubleFunction<in T>!): Comparator<T>!
```

Accepts a function that extracts a `double` sort key from a type `T`, and returns a `Comparator<T>` that compares by that sort key.

The returned comparator is serializable if the specified function is also serializable.

| Parameters ||
|---|---|
| `<T>` | the type of element to be compared |
| `keyExtractor` | [ToDoubleFunction](../java.util.function/ToDoubleFunction.md)\<in T\>!: the function used to extract the double sort key |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Comparator#<T>!` | a comparator that compares by an extracted key |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the argument is null |

**See Also**

- comparing

### comparingInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <T : Any!> comparingInt(keyExtractor: ToIntFunction<in T>!): Comparator<T>!
```

Accepts a function that extracts an `int` sort key from a type `T`, and returns a `Comparator<T>` that compares by that sort key.

The returned comparator is serializable if the specified function is also serializable.

| Parameters ||
|---|---|
| `<T>` | the type of element to be compared |
| `keyExtractor` | [ToIntFunction](../java.util.function/ToIntFunction.md)\<in T\>!: the function used to extract the integer sort key |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Comparator#<T>!` | a comparator that compares by an extracted key |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the argument is null |

**See Also**

- comparing

### comparingLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <T : Any!> comparingLong(keyExtractor: ToLongFunction<in T>!): Comparator<T>!
```

Accepts a function that extracts a `long` sort key from a type `T`, and returns a `Comparator<T>` that compares by that sort key.

The returned comparator is serializable if the specified function is also serializable.

| Parameters ||
|---|---|
| `<T>` | the type of element to be compared |
| `keyExtractor` | [ToLongFunction](../java.util.function/ToLongFunction.md)\<in T\>!: the function used to extract the long sort key |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Comparator#<T>!` | a comparator that compares by an extracted key |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the argument is null |

**See Also**

- comparing

### naturalOrder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <T : Comparable<T>!> naturalOrder(): Comparator<T>!
```

Returns a comparator that compares `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` objects in natural order.

The returned comparator is serializable and throws `https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#` when comparing `null`.

| Parameters ||
|---|---|
| `<T>` | the `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` type of element to be compared |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Comparator#<T>!` | a comparator that imposes the *natural ordering* on `Comparable` objects. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`

### nullsFirst

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <T : Any!> nullsFirst(comparator: Comparator<in T>!): Comparator<T>!
```

Returns a null-friendly comparator that considers `null` to be less than non-null. When both are `null`, they are considered equal. If both are non-null, the specified `Comparator` is used to determine the order. If the specified comparator is `null`, then the returned comparator considers all non-null values to be equal.

The returned comparator is serializable if the specified comparator is serializable.

| Parameters ||
|---|---|
| `<T>` | the type of the elements to be compared |
| `comparator` | [Comparator](Comparator.md)\<in T\>!: a `Comparator` for comparing non-null values |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Comparator#<T>!` | a comparator that considers `null` to be less than non-null, and compares non-null objects with the supplied `Comparator`. |

### nullsLast

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <T : Any!> nullsLast(comparator: Comparator<in T>!): Comparator<T>!
```

Returns a null-friendly comparator that considers `null` to be greater than non-null. When both are `null`, they are considered equal. If both are non-null, the specified `Comparator` is used to determine the order. If the specified comparator is `null`, then the returned comparator considers all non-null values to be equal.

The returned comparator is serializable if the specified comparator is serializable.

| Parameters ||
|---|---|
| `<T>` | the type of the elements to be compared |
| `comparator` | [Comparator](Comparator.md)\<in T\>!: a `Comparator` for comparing non-null values |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Comparator#<T>!` | a comparator that considers `null` to be greater than non-null, and compares non-null objects with the supplied `Comparator`. |

### reverseOrder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <T : Comparable<T>!> reverseOrder(): Comparator<T>!
```

Returns a comparator that imposes the reverse of the *natural ordering*.

The returned comparator is serializable and throws `https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#` when comparing `null`.

| Parameters ||
|---|---|
| `<T>` | the `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` type of element to be compared |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Comparator#<T>!` | a comparator that imposes the reverse of the *natural ordering* on `Comparable` objects. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`

### reversed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reversed(): Comparator<T>!
```

Returns a comparator that imposes the reverse ordering of this comparator.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Comparator#<T>!` | a comparator that imposes the reverse ordering of this comparator. |

### thenComparing

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun thenComparing(other: Comparator<in T>!): Comparator<T>!
```

Returns a lexicographic-order comparator with another comparator. If this `Comparator` considers two elements equal, i.e. `compare(a, b) == 0`, `other` is used to determine the order.

The returned comparator is serializable if the specified comparator is also serializable.

| Parameters ||
|---|---|
| `other` | [Comparator](Comparator.md)\<in T\>!: the other comparator to be used when this comparator compares two objects that are equal. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Comparator#<T>!` | a lexicographic-order comparator composed of this and then the other comparator |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the argument is null. |

### thenComparing

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <U : Comparable<U>!> thenComparing(keyExtractor: Function<in T, out U>!): Comparator<T>!
```

Returns a lexicographic-order comparator with a function that extracts a `Comparable` sort key.

| Parameters ||
|---|---|
| `<U>` | the type of the `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` sort key |
| `keyExtractor` | [Function](../java.util.function/Function.md)\<in T, out U\>!: the function used to extract the `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` sort key |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Comparator#<T>!` | a lexicographic-order comparator composed of this and then the `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` sort key. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the argument is null. |

**See Also**

- comparing
- thenComparing

### thenComparing

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <U : Any!> thenComparing(
    keyExtractor: Function<in T, out U>!, 
    keyComparator: Comparator<in U>!
): Comparator<T>!
```

Returns a lexicographic-order comparator with a function that extracts a key to be compared with the given `Comparator`.

| Parameters ||
|---|---|
| `<U>` | the type of the sort key |
| `keyExtractor` | [Function](../java.util.function/Function.md)\<in T, out U\>!: the function used to extract the sort key |
| `keyComparator` | [Comparator](Comparator.md)\<in U\>!: the `Comparator` used to compare the sort key |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Comparator#<T>!` | a lexicographic-order comparator composed of this comparator and then comparing on the key extracted by the keyExtractor function |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if either argument is null. |

**See Also**

- comparing
- thenComparing

### thenComparingDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun thenComparingDouble(keyExtractor: ToDoubleFunction<in T>!): Comparator<T>!
```

Returns a lexicographic-order comparator with a function that extracts a `double` sort key.

| Parameters ||
|---|---|
| `keyExtractor` | [ToDoubleFunction](../java.util.function/ToDoubleFunction.md)\<in T\>!: the function used to extract the double sort key |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Comparator#<T>!` | a lexicographic-order comparator composed of this and then the `double` sort key |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the argument is null. |

**See Also**

- comparingDouble
- thenComparing

### thenComparingInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun thenComparingInt(keyExtractor: ToIntFunction<in T>!): Comparator<T>!
```

Returns a lexicographic-order comparator with a function that extracts an `int` sort key.

| Parameters ||
|---|---|
| `keyExtractor` | [ToIntFunction](../java.util.function/ToIntFunction.md)\<in T\>!: the function used to extract the integer sort key |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Comparator#<T>!` | a lexicographic-order comparator composed of this and then the `int` sort key |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the argument is null. |

**See Also**

- comparingInt
- thenComparing

### thenComparingLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun thenComparingLong(keyExtractor: ToLongFunction<in T>!): Comparator<T>!
```

Returns a lexicographic-order comparator with a function that extracts a `long` sort key.

| Parameters ||
|---|---|
| `keyExtractor` | [ToLongFunction](../java.util.function/ToLongFunction.md)\<in T\>!: the function used to extract the long sort key |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Comparator#<T>!` | a lexicographic-order comparator composed of this and then the `long` sort key |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the argument is null. |

**See Also**

- comparingLong
- thenComparing
