# ConcurrentHashMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConcurrentHashMap

```
open class ConcurrentHashMap<K : Any!, V : Any!> : AbstractMap<K, V>, ConcurrentMap<K, V>, Serializable, MutableMap<K, V>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.util.AbstractMap](https://developer.android.com/reference/kotlin/java/util/AbstractMap.html#)\<K, V\> ||
| | ↳ | [java.util.concurrent.ConcurrentHashMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#) |

A hash table supporting full concurrency of retrievals and high expected concurrency for updates. This class obeys the same functional specification as [java.util.Hashtable](https://developer.android.com/reference/kotlin/java/util/Hashtable.html#), and includes versions of methods corresponding to each method of`Hashtable`. However, even though all operations are thread-safe, retrieval operations do*not* entail locking, and there is*not* any support for locking the entire table in a way that prevents all access. This class is fully interoperable with`Hashtable`in programs that rely on its thread safety but not on its synchronization details.

Retrieval operations (including`get`) generally do not block, so may overlap with update operations (including`put`and`remove`). Retrievals reflect the results of the most recently*completed* update operations holding upon their onset. (More formally, an update operation for a given key bears a*happens-before* relation with any (non-null) retrieval for that key reporting the updated value.) For aggregate operations such as`putAll`and`clear`, concurrent retrievals may reflect insertion or removal of only some entries. Similarly, Iterators, Spliterators and Enumerations return elements reflecting the state of the hash table at some point at or since the creation of the iterator/enumeration. They do*not* throw . However, iterators are designed to be used by only one thread at a time. Bear in mind that the results of aggregate status methods including`size`,`isEmpty`, and`containsValue`are typically useful only when a map is not undergoing concurrent updates in other threads. Otherwise the results of these methods reflect transient states that may be adequate for monitoring or estimation purposes, but not for program control.

The table is dynamically expanded when there are too many collisions (i.e., keys that have distinct hash codes but fall into the same slot modulo the table size), with the expected average effect of maintaining roughly two bins per mapping (corresponding to a 0.75 load factor threshold for resizing). There may be much variance around this average as mappings are added and removed, but overall, this maintains a commonly accepted time/space tradeoff for hash tables. However, resizing this or any other kind of hash table may be a relatively slow operation. When possible, it is a good idea to provide a size estimate as an optional`initialCapacity`constructor argument. An additional optional`loadFactor`constructor argument provides a further means of customizing initial table capacity by specifying the table density to be used in calculating the amount of space to allocate for the given number of elements. Also, for compatibility with previous versions of this class, constructors may optionally specify an expected`concurrencyLevel`as an additional hint for internal sizing. Note that using many keys with exactly the same`hashCode()`is a sure way to slow down performance of any hash table. To ameliorate impact, when keys are [Comparable](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#), this class may use comparison order among keys to help break ties.

A [Set](https://developer.android.com/reference/kotlin/java/util/Set.html#) projection of a ConcurrentHashMap may be created (using [newKeySet()](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#newKeySet())or [newKeySet(int)](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#newKeySet(kotlin.Int))), or viewed (using [keySet(java.lang.Object)](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#keySet(java.util.concurrent.ConcurrentHashMap.V))when only keys are of interest, and the mapped values are (perhaps transiently) not used or all take the same mapping value.

A ConcurrentHashMap can be used as a scalable frequency map (a form of histogram or multiset) by using values and initializing via [computeIfAbsent](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#computeIfAbsent(java.util.concurrent.ConcurrentHashMap.K,%20java.util.function.Function)). For example, to add a count to a`ConcurrentHashMap<String,LongAdder> freqs`, you can use`freqs.computeIfAbsent(key, k -> new LongAdder()).increment();`

This class and its views and iterators implement all of the*optional* methods of the [Map](https://developer.android.com/reference/kotlin/java/util/Map.html#) and [Iterator](https://developer.android.com/reference/kotlin/java/util/Iterator.html#) interfaces.

Like [Hashtable](https://developer.android.com/reference/kotlin/java/util/Hashtable.html#) but unlike [HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#), this class does*not* allow`null`to be used as a key or value.

ConcurrentHashMaps support a set of sequential and parallel bulk operations that, unlike most [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#) methods, are designed to be safely, and often sensibly, applied even with maps that are being concurrently updated by other threads; for example, when computing a snapshot summary of the values in a shared registry. There are three kinds of operation, each with four forms, accepting functions with keys, values, entries, and (key, value) pairs as arguments and/or return values. Because the elements of a ConcurrentHashMap are not ordered in any particular way, and may be processed in different orders in different parallel executions, the correctness of supplied functions should not depend on any ordering, or on any other objects or values that may transiently change while computation is in progress; and except for forEach actions, should ideally be side-effect-free. Bulk operations on [Map.Entry](https://developer.android.com/reference/kotlin/java/util/Map.Entry.html#) objects do not support method`setValue`.

- forEach: Performs a given action on each element. A variant form applies a given transformation on each element before performing the action.
- search: Returns the first available non-null result of applying a given function on each element; skipping further search when a result is found.
- reduce: Accumulates each element. The supplied reduction function cannot rely on ordering (more formally, it should be both associative and commutative). There are five variants:
 - Plain reductions. (There is not a form of this method for (key, value) function arguments since there is no corresponding return type.)
 - Mapped reductions that accumulate the results of a given function applied to each element.
 - Reductions to scalar doubles, longs, and ints, using a given basis value.

These bulk operations accept a`parallelismThreshold`argument. Methods proceed sequentially if the current map size is estimated to be less than the given threshold. Using a value of`Long.MAX_VALUE`suppresses all parallelism. Using a value of`1`results in maximal parallelism by partitioning into enough subtasks to fully utilize the [java.util.concurrent.ForkJoinPool#commonPool()](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool#commonPool())that is used for all parallel computations. Normally, you would initially choose one of these extreme values, and then measure performance of using in-between values that trade off overhead versus throughput.

The concurrency properties of bulk operations follow from those of ConcurrentHashMap: Any non-null result returned from`get(key)`and related access methods bears a happens-before relation with the associated insertion or update. The result of any bulk operation reflects the composition of these per-element relations (but is not necessarily atomic with respect to the map as a whole unless it is somehow known to be quiescent). Conversely, because keys and values in the map are never null, null serves as a reliable atomic indicator of the current lack of any result. To maintain this property, null serves as an implicit basis for all non-scalar reduction operations. For the double, long, and int versions, the basis should be one that, when combined with any other value, returns that other value (more formally, it should be the identity element for the reduction). Most common reductions have these properties; for example, computing a sum with basis 0 or a minimum with basis MAX_VALUE.

Search and transformation functions provided as arguments should similarly return null to indicate the lack of any result (in which case it is not used). In the case of mapped reductions, this also enables transformations to serve as filters, returning null (or, in the case of primitive specializations, the identity basis) if the element should not be combined. You can create compound transformations and filterings by composing them yourself under this "null means there is nothing there now" rule before using them in search or reduce operations.

Methods accepting and/or returning Entry arguments maintain key-value associations. They may be useful for example when finding the key for the greatest value. Note that "plain" Entry arguments can be supplied using`new AbstractMap.SimpleEntry(k,v)`.

Bulk operations may complete abruptly, throwing an exception encountered in the application of a supplied function. Bear in mind when handling such exceptions that other concurrently executing functions could also have thrown exceptions, or would have done so if the first exception had not occurred.

Speedups for parallel compared to sequential forms are common but not guaranteed. Parallel operations involving brief functions on small maps may execute more slowly than sequential forms if the underlying work to parallelize the computation is more expensive than the computation itself. Similarly, parallelization may not lead to much actual parallelism if all processors are busy performing unrelated tasks.

All arguments to all task methods must be non-null.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [KeySetView](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap.KeySetView) A view of a ConcurrentHashMap as a [Set](https://developer.android.com/reference/kotlin/java/util/Set.html#) of keys, in which additions may optionally be enabled by mapping to a common value. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ConcurrentHashMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#ConcurrentHashMap())`()` Creates a new, empty map with the default initial table size (16). |
| [ConcurrentHashMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#ConcurrentHashMap(kotlin.Int))`(`initialCapacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new, empty map with an initial table size accommodating the specified number of elements without the need to dynamically resize. |
| [ConcurrentHashMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#ConcurrentHashMap(kotlin.Int,%20kotlin.Float))`(`initialCapacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `loadFactor:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Creates a new, empty map with an initial table size based on the given number of elements (`initialCapacity`) and initial table density (`loadFactor`). |
| [ConcurrentHashMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#ConcurrentHashMap(kotlin.Int,%20kotlin.Float,%20kotlin.Int))`(`initialCapacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `loadFactor:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `concurrencyLevel:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new, empty map with an initial table size based on the given number of elements (`initialCapacity`), initial table density (`loadFactor`), and number of concurrently updating threads (`concurrencyLevel`). |
| [ConcurrentHashMap](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#ConcurrentHashMap(kotlin.collections.MutableMap))`(`m:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)<out` `K,` `out` `V>`)` Creates a new map with the same mappings as the given map. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#clear())`()` Removes all of the mappings from this map. |
| openV? | [compute](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#compute(java.util.concurrent.ConcurrentHashMap.K,%20java.util.function.BiFunction))`(`key:` `K`, `remappingFunction:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)<in` `K,` `in` `V?,` `out` `V?>`)` Attempts to compute a mapping for the specified key and its current mapped value (or`null`if there is no current mapping). |
| openV | [computeIfAbsent](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#computeIfAbsent(java.util.concurrent.ConcurrentHashMap.K,%20java.util.function.Function))`(`key:` `K`, `mappingFunction:` ` [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)<in` `K,` `out` `V>`)` If the specified key is not already associated with a value, attempts to compute its value using the given mapping function and enters it into this map unless`null`. |
| openV? | [computeIfPresent](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#computeIfPresent(java.util.concurrent.ConcurrentHashMap.K,%20java.util.function.BiFunction))`(`key:` `K`, `remappingFunction:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)<in` `K,` `in` `V,` `out` `V?>`)` If the value for the specified key is present, attempts to compute a new mapping given the key and its current mapped value. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#contains(kotlin.Any))`(`value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`)` Tests if some key maps into the specified value in this table. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsKey](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#containsKey(java.util.concurrent.ConcurrentHashMap.K))`(`key:` `K`)` Tests if the specified object is a key in this table. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsKey](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#containsKey(java.util.concurrent.ConcurrentHashMap.K))`(`key:` `K`)` Tests if the specified object is a key in this table. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsValue](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#containsValue(java.util.concurrent.ConcurrentHashMap.V))`(`value:` `V`)` Returns`true`if this map maps one or more keys to the specified value. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsValue](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#containsValue(java.util.concurrent.ConcurrentHashMap.V))`(`value:` `V`)` Returns`true`if this map maps one or more keys to the specified value. |
| open [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration.html#)\<V\> | [elements](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#elements())`()` Returns an enumeration of the values in this table. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares the specified object with this map for equality. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#forEach(java.util.function.BiConsumer))`(`action:` ` [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#)<in` `K,` `in` `V>`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#forEach(kotlin.Long,%20java.util.function.BiConsumer))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `action:` ` [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#)<in` `K,` `in` `V>`)` Performs the given action for each (key, value). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#forEach(kotlin.Long,%20java.util.function.BiFunction,%20java.util.function.Consumer))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `transformer:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)<in` `K,` `in` `V,` `out` `U>`, `action:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)<in` `U>`)` Performs the given action for each non-null transformation of each (key, value). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachEntry](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#forEachEntry(kotlin.Long,%20java.util.function.Consumer))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `action:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)<in` ` [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>!>`)` Performs the given action for each entry. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachEntry](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#forEachEntry(kotlin.Long,%20java.util.function.Function,%20java.util.function.Consumer))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `transformer:` ` [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>!,` `out` `U>`, `action:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)<in` `U>`)` Performs the given action for each non-null transformation of each entry. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachKey](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#forEachKey(kotlin.Long,%20java.util.function.Consumer))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `action:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)<in` `K>`)` Performs the given action for each key. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachKey](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#forEachKey(kotlin.Long,%20java.util.function.Function,%20java.util.function.Consumer))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `transformer:` ` [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)<in` `K,` `out` `U>`, `action:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)<in` `U>`)` Performs the given action for each non-null transformation of each key. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachValue](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#forEachValue(kotlin.Long,%20java.util.function.Consumer))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `action:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)<in` `V>`)` Performs the given action for each value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachValue](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#forEachValue(kotlin.Long,%20java.util.function.Function,%20java.util.function.Consumer))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `transformer:` ` [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)<in` `V,` `out` `U>`, `action:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)<in` `U>`)` Performs the given action for each non-null transformation of each value. |
| openV? | [get](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#get(java.util.concurrent.ConcurrentHashMap.K))`(`key:` `K`)` Returns the value to which the specified key is mapped, or`null`if this map contains no mapping for the key. |
| openV? | [get](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#get(java.util.concurrent.ConcurrentHashMap.K))`(`key:` `K`)` Returns the value to which the specified key is mapped, or`null`if this map contains no mapping for the key. |
| openV | [getOrDefault](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#getOrDefault(java.util.concurrent.ConcurrentHashMap.K,%20java.util.concurrent.ConcurrentHashMap.V))`(`key:` `K`, `defaultValue:` `V`)` Returns the value to which the specified key is mapped, or the given default value if this map contains no mapping for the key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#hashCode())`()` Returns the hash code value for this [Map](https://developer.android.com/reference/kotlin/java/util/Map.html#), i. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#isEmpty())`()` Returns`true`if this map contains no key-value mappings. |
| open [ConcurrentHashMap.KeySetView](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap.KeySetView)\<K,V\> | [keySet](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#keySet(java.util.concurrent.ConcurrentHashMap.V))`(`mappedValue:` `V`)` Returns a [Set](https://developer.android.com/reference/kotlin/java/util/Set.html#) view of the keys in this map, using the given common mapped value for any additions (i.e., |
| open [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration.html#)\<K\> | [keys](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#keys())`()` Returns an enumeration of the keys in this table. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [mappingCount](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#mappingCount())`()` Returns the number of mappings. |
| openV? | [merge](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#merge(java.util.concurrent.ConcurrentHashMap.K,%20java.util.concurrent.ConcurrentHashMap.V,%20java.util.function.BiFunction))`(`key:` `K`, `value:` `V`, `remappingFunction:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)<in` `V,` `in` `V,` `out` `V?>`)` If the specified key is not already associated with a (non-null) value, associates it with the given value. |
| openstatic [ConcurrentHashMap.KeySetView](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap.KeySetView)\<K, [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\> | [newKeySet](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#newKeySet())`()` Creates a new [Set](https://developer.android.com/reference/kotlin/java/util/Set.html#) backed by a ConcurrentHashMap from the given type to`Boolean.TRUE`. |
| openstatic [ConcurrentHashMap.KeySetView](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap.KeySetView)\<K, [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\> | [newKeySet](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#newKeySet(kotlin.Int))`(`initialCapacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new [Set](https://developer.android.com/reference/kotlin/java/util/Set.html#) backed by a ConcurrentHashMap from the given type to`Boolean.TRUE`. |
| openV? | [put](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#put(java.util.concurrent.ConcurrentHashMap.K,%20java.util.concurrent.ConcurrentHashMap.V))`(`key:` `K`, `value:` `V`)` Maps the specified key to the specified value in this table. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putAll](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#putAll(kotlin.collections.Map))`(`from:` ` [Map](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-map/index.html)<out` `K,` `V>`)` Copies all of the mappings from the specified map to this one. |
| openV? | [putIfAbsent](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#putIfAbsent(java.util.concurrent.ConcurrentHashMap.K,%20java.util.concurrent.ConcurrentHashMap.V))`(`key:` `K`, `value:` `V`)` If the specified key is not already associated with a value (or is mapped to`null`) associates it with the given value and returns`null`, else returns the current value. |
| openU? | [reduce](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#reduce(kotlin.Long,%20java.util.function.BiFunction,%20java.util.function.BiFunction))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `transformer:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)<in` `K,` `in` `V,` `out` `U>`, `reducer:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)<in` `U,` `in` `U,` `out` `U>`)` Returns the result of accumulating the given transformation of all (key, value) pairs using the given reducer to combine values, or null if none. |
| open [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>? | [reduceEntries](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#reduceEntries(kotlin.Long,%20java.util.function.BiFunction))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `reducer:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>!,` ` [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>!,` `out` ` [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>!>`)` Returns the result of accumulating all entries using the given reducer to combine values, or null if none. |
| openU? | [reduceEntries](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#reduceEntries(kotlin.Long,%20java.util.function.Function,%20java.util.function.BiFunction))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `transformer:` ` [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>!,` `out` `U>`, `reducer:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)<in` `U,` `in` `U,` `out` `U>`)` Returns the result of accumulating the given transformation of all entries using the given reducer to combine values, or null if none. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [reduceEntriesToDouble](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#reduceEntriesToDouble(kotlin.Long,%20java.util.function.ToDoubleFunction,%20kotlin.Double,%20java.util.function.DoubleBinaryOperator))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `transformer:` ` [ToDoubleFunction](https://developer.android.com/reference/kotlin/java/util/function/ToDoubleFunction.html#)< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>!>`, `basis:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `reducer:` ` [DoubleBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleBinaryOperator.html#)`)` Returns the result of accumulating the given transformation of all entries using the given reducer to combine values, and the given basis as an identity value. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [reduceEntriesToInt](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#reduceEntriesToInt(kotlin.Long,%20java.util.function.ToIntFunction,%20kotlin.Int,%20java.util.function.IntBinaryOperator))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `transformer:` ` [ToIntFunction](https://developer.android.com/reference/kotlin/java/util/function/ToIntFunction.html#)< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>!>`, `basis:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reducer:` ` [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#)`)` Returns the result of accumulating the given transformation of all entries using the given reducer to combine values, and the given basis as an identity value. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [reduceEntriesToLong](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#reduceEntriesToLong(kotlin.Long,%20java.util.function.ToLongFunction,%20kotlin.Long,%20java.util.function.LongBinaryOperator))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `transformer:` ` [ToLongFunction](https://developer.android.com/reference/kotlin/java/util/function/ToLongFunction.html#)< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>!>`, `basis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `reducer:` ` [LongBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator.html#)`)` Returns the result of accumulating the given transformation of all entries using the given reducer to combine values, and the given basis as an identity value. |
| openK? | [reduceKeys](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#reduceKeys(kotlin.Long,%20java.util.function.BiFunction))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `reducer:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)<in` `K,` `in` `K,` `out` `K>`)` Returns the result of accumulating all keys using the given reducer to combine values, or null if none. |
| openU? | [reduceKeys](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#reduceKeys(kotlin.Long,%20java.util.function.Function,%20java.util.function.BiFunction))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `transformer:` ` [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)<in` `K,` `out` `U>`, `reducer:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)<in` `U,` `in` `U,` `out` `U>`)` Returns the result of accumulating the given transformation of all keys using the given reducer to combine values, or null if none. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [reduceKeysToDouble](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#reduceKeysToDouble(kotlin.Long,%20java.util.function.ToDoubleFunction,%20kotlin.Double,%20java.util.function.DoubleBinaryOperator))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `transformer:` ` [ToDoubleFunction](https://developer.android.com/reference/kotlin/java/util/function/ToDoubleFunction.html#)<in` `K>`, `basis:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `reducer:` ` [DoubleBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleBinaryOperator.html#)`)` Returns the result of accumulating the given transformation of all keys using the given reducer to combine values, and the given basis as an identity value. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [reduceKeysToInt](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#reduceKeysToInt(kotlin.Long,%20java.util.function.ToIntFunction,%20kotlin.Int,%20java.util.function.IntBinaryOperator))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `transformer:` ` [ToIntFunction](https://developer.android.com/reference/kotlin/java/util/function/ToIntFunction.html#)<in` `K>`, `basis:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reducer:` ` [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#)`)` Returns the result of accumulating the given transformation of all keys using the given reducer to combine values, and the given basis as an identity value. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [reduceKeysToLong](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#reduceKeysToLong(kotlin.Long,%20java.util.function.ToLongFunction,%20kotlin.Long,%20java.util.function.LongBinaryOperator))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `transformer:` ` [ToLongFunction](https://developer.android.com/reference/kotlin/java/util/function/ToLongFunction.html#)<in` `K>`, `basis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `reducer:` ` [LongBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator.html#)`)` Returns the result of accumulating the given transformation of all keys using the given reducer to combine values, and the given basis as an identity value. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [reduceToDouble](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#reduceToDouble(kotlin.Long,%20java.util.function.ToDoubleBiFunction,%20kotlin.Double,%20java.util.function.DoubleBinaryOperator))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `transformer:` ` [ToDoubleBiFunction](https://developer.android.com/reference/kotlin/java/util/function/ToDoubleBiFunction.html#)<in` `K,` `in` `V>`, `basis:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `reducer:` ` [DoubleBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleBinaryOperator.html#)`)` Returns the result of accumulating the given transformation of all (key, value) pairs using the given reducer to combine values, and the given basis as an identity value. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [reduceToInt](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#reduceToInt(kotlin.Long,%20java.util.function.ToIntBiFunction,%20kotlin.Int,%20java.util.function.IntBinaryOperator))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `transformer:` ` [ToIntBiFunction](https://developer.android.com/reference/kotlin/java/util/function/ToIntBiFunction.html#)<in` `K,` `in` `V>`, `basis:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reducer:` ` [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#)`)` Returns the result of accumulating the given transformation of all (key, value) pairs using the given reducer to combine values, and the given basis as an identity value. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [reduceToLong](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#reduceToLong(kotlin.Long,%20java.util.function.ToLongBiFunction,%20kotlin.Long,%20java.util.function.LongBinaryOperator))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `transformer:` ` [ToLongBiFunction](https://developer.android.com/reference/kotlin/java/util/function/ToLongBiFunction.html#)<in` `K,` `in` `V>`, `basis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `reducer:` ` [LongBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator.html#)`)` Returns the result of accumulating the given transformation of all (key, value) pairs using the given reducer to combine values, and the given basis as an identity value. |
| openV? | [reduceValues](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#reduceValues(kotlin.Long,%20java.util.function.BiFunction))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `reducer:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)<in` `V,` `in` `V,` `out` `V>`)` Returns the result of accumulating all values using the given reducer to combine values, or null if none. |
| openU? | [reduceValues](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#reduceValues(kotlin.Long,%20java.util.function.Function,%20java.util.function.BiFunction))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `transformer:` ` [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)<in` `V,` `out` `U>`, `reducer:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)<in` `U,` `in` `U,` `out` `U>`)` Returns the result of accumulating the given transformation of all values using the given reducer to combine values, or null if none. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [reduceValuesToDouble](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#reduceValuesToDouble(kotlin.Long,%20java.util.function.ToDoubleFunction,%20kotlin.Double,%20java.util.function.DoubleBinaryOperator))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `transformer:` ` [ToDoubleFunction](https://developer.android.com/reference/kotlin/java/util/function/ToDoubleFunction.html#)<in` `V>`, `basis:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `reducer:` ` [DoubleBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleBinaryOperator.html#)`)` Returns the result of accumulating the given transformation of all values using the given reducer to combine values, and the given basis as an identity value. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [reduceValuesToInt](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#reduceValuesToInt(kotlin.Long,%20java.util.function.ToIntFunction,%20kotlin.Int,%20java.util.function.IntBinaryOperator))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `transformer:` ` [ToIntFunction](https://developer.android.com/reference/kotlin/java/util/function/ToIntFunction.html#)<in` `V>`, `basis:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reducer:` ` [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#)`)` Returns the result of accumulating the given transformation of all values using the given reducer to combine values, and the given basis as an identity value. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [reduceValuesToLong](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#reduceValuesToLong(kotlin.Long,%20java.util.function.ToLongFunction,%20kotlin.Long,%20java.util.function.LongBinaryOperator))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `transformer:` ` [ToLongFunction](https://developer.android.com/reference/kotlin/java/util/function/ToLongFunction.html#)<in` `V>`, `basis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `reducer:` ` [LongBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator.html#)`)` Returns the result of accumulating the given transformation of all values using the given reducer to combine values, and the given basis as an identity value. |
| openV? | [remove](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#remove(java.util.concurrent.ConcurrentHashMap.K))`(`key:` `K`)` Removes the key (and its corresponding value) from this map. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#remove(java.util.concurrent.ConcurrentHashMap.K,%20java.util.concurrent.ConcurrentHashMap.V))`(`key:` `K`, `value:` `V`)` Removes the entry for the specified key only if it is currently mapped to the specified value. |
| openV? | [remove](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#remove(java.util.concurrent.ConcurrentHashMap.K))`(`key:` `K`)` Removes the key (and its corresponding value) from this map. |
| openV? | [replace](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#replace(java.util.concurrent.ConcurrentHashMap.K,%20java.util.concurrent.ConcurrentHashMap.V))`(`key:` `K`, `value:` `V`)` Replaces the entry for the specified key only if it is currently mapped to some value. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [replace](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#replace(java.util.concurrent.ConcurrentHashMap.K,%20java.util.concurrent.ConcurrentHashMap.V,%20java.util.concurrent.ConcurrentHashMap.V))`(`key:` `K`, `oldValue:` `V`, `newValue:` `V`)` Replaces the entry for the specified key only if currently mapped to the specified value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [replaceAll](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#replaceAll(java.util.function.BiFunction))`(`function:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)<in` `K,` `in` `V,` `out` `V>`)` <br /> |
| openU? | [search](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#search(kotlin.Long,%20java.util.function.BiFunction))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `searchFunction:` ` [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)<in` `K,` `in` `V,` `out` `U>`)` Returns a non-null result from applying the given search function on each (key, value), or null if none. |
| openU? | [searchEntries](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#searchEntries(kotlin.Long,%20java.util.function.Function))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `searchFunction:` ` [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>!,` `out` `U>`)` Returns a non-null result from applying the given search function on each entry, or null if none. |
| openU? | [searchKeys](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#searchKeys(kotlin.Long,%20java.util.function.Function))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `searchFunction:` ` [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)<in` `K,` `out` `U>`)` Returns a non-null result from applying the given search function on each key, or null if none. |
| openU? | [searchValues](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#searchValues(kotlin.Long,%20java.util.function.Function))`(`parallelismThreshold:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `searchFunction:` ` [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)<in` `V,` `out` `U>`)` Returns a non-null result from applying the given search function on each value, or null if none. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#toString())`()` Returns a string representation of this map. |

| Inherited functions ||
|---|---|
| From class [AbstractMap](https://developer.android.com/reference/kotlin/java/util/AbstractMap.html#) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/util/AbstractMap.html#clone())`()` <br /> Returns a shallow copy of this`AbstractMap`instance: the keys and values themselves are not cloned. <br /> | ||

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>\> | [entries](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#entries:kotlin.collections.MutableSet) Returns a [Set](https://developer.android.com/reference/kotlin/java/util/Set.html#) view of the mappings contained in this map. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<K\> | [keys](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#keys:kotlin.collections.MutableSet) Returns a [Set](https://developer.android.com/reference/kotlin/java/util/Set.html#) view of the keys contained in this map. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#size:kotlin.Int) Returns the number of key-value mappings in this map. |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<V\> | [values](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#values:kotlin.collections.MutableCollection) Returns a [Collection](https://developer.android.com/reference/kotlin/java/util/Collection.html#) view of the values contained in this map. |

## Public constructors

### ConcurrentHashMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ConcurrentHashMap()
```

Creates a new, empty map with the default initial table size (16). 

### ConcurrentHashMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ConcurrentHashMap(initialCapacity: Int)
```

Creates a new, empty map with an initial table size accommodating the specified number of elements without the need to dynamically resize.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `initialCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The implementation performs internal sizing to accommodate this many elements. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the initial capacity of elements is negative |

### ConcurrentHashMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ConcurrentHashMap(
    initialCapacity: Int, 
    loadFactor: Float)
```

Creates a new, empty map with an initial table size based on the given number of elements (`initialCapacity`) and initial table density (`loadFactor`).

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `initialCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial capacity. The implementation performs internal sizing to accommodate this many elements, given the specified load factor. |
| `loadFactor` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the load factor (table density) for establishing the initial table size |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the initial capacity of elements is negative or the load factor is nonpositive |

### ConcurrentHashMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ConcurrentHashMap(
    initialCapacity: Int, 
    loadFactor: Float, 
    concurrencyLevel: Int)
```

Creates a new, empty map with an initial table size based on the given number of elements (`initialCapacity`), initial table density (`loadFactor`), and number of concurrently updating threads (`concurrencyLevel`).

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `initialCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial capacity. The implementation performs internal sizing to accommodate this many elements, given the specified load factor. |
| `loadFactor` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the load factor (table density) for establishing the initial table size |
| `concurrencyLevel` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the estimated number of concurrently updating threads. The implementation may use this value as a sizing hint. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the initial capacity is negative or the load factor or concurrencyLevel are nonpositive |

### ConcurrentHashMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ConcurrentHashMap(m: MutableMap<out K, out V>)
```

Creates a new map with the same mappings as the given map.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------|
| `m` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<outK,outV\>:the map |

## Public methods

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Removes all of the mappings from this map.

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`clear`operation is not supported by this map |

### compute

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compute(
    key: K, 
    remappingFunction: BiFunction<in K, in V?, out V?>
): V?
```

Attempts to compute a mapping for the specified key and its current mapped value (or`null`if there is no current mapping). The entire method invocation is performed atomically. The supplied function is invoked exactly once per invocation of this method. Some attempted update operations on this map by other threads may be blocked while computation is in progress, so the computation should be short and simple.

The remapping function must not modify this map during computation.

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | K:key with which the specified value is to be associated |
| `remappingFunction` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)\<inK,inV?,outV?\>:the function to compute a value |

| Return ||
|----|------------------------------------------------------------------|
| V? | the new value associated with the specified key, or null if none |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified key or remappingFunction is null |
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map (java.util.Collection#) |
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalStateException` | if the computation detectably attempts a recursive update to this map that would otherwise never complete |
| `java.lang.RuntimeException` | or Error if the remappingFunction does so, in which case the mapping is unchanged |

### computeIfAbsent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun computeIfAbsent(
    key: K, 
    mappingFunction: Function<in K, out V>
): V
```

If the specified key is not already associated with a value, attempts to compute its value using the given mapping function and enters it into this map unless`null`. The entire method invocation is performed atomically. The supplied function is invoked exactly once per invocation of this method if the key is absent, else not at all. Some attempted update operations on this map by other threads may be blocked while computation is in progress, so the computation should be short and simple.

The mapping function must not modify this map during computation.

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | K:key with which the specified value is to be associated |
| `mappingFunction` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<inK,outV\>:the function to compute a value |

| Return ||
|---|-------------------------------------------------------------------------------------------------------------------|
| V | the current (existing or computed) value associated with the specified key, or null if the computed value is null |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified key or mappingFunction is null |
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map (java.util.Collection#) |
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalStateException` | if the computation detectably attempts a recursive update to this map that would otherwise never complete |
| `java.lang.RuntimeException` | or Error if the mappingFunction does so, in which case the mapping is left unestablished |

### computeIfPresent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun computeIfPresent(
    key: K, 
    remappingFunction: BiFunction<in K, in V, out V?>
): V?
```

If the value for the specified key is present, attempts to compute a new mapping given the key and its current mapped value. The entire method invocation is performed atomically. The supplied function is invoked exactly once per invocation of this method if the key is present, else not at all. Some attempted update operations on this map by other threads may be blocked while computation is in progress, so the computation should be short and simple.

The remapping function must not modify this map during computation.

| Parameters ||
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | K:key with which a value may be associated |
| `remappingFunction` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)\<inK,inV,outV?\>:the function to compute a value |

| Return ||
|----|------------------------------------------------------------------|
| V? | the new value associated with the specified key, or null if none |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified key or remappingFunction is null |
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map (java.util.Collection#) |
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalStateException` | if the computation detectably attempts a recursive update to this map that would otherwise never complete |
| `java.lang.RuntimeException` | or Error if the remappingFunction does so, in which case the mapping is unchanged |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun contains(value: Any): Boolean
```

Tests if some key maps into the specified value in this table.

Note that this method is identical in functionality to [containsValue(java.lang.Object)](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#containsValue(java.util.concurrent.ConcurrentHashMap.V)), and exists solely to ensure full compatibility with class [java.util.Hashtable](https://developer.android.com/reference/kotlin/java/util/Hashtable.html#), which supported this method prior to introduction of the Java Collections Framework.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------|
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):a value to search for |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if and only if some key maps to the`value`argument in this table as determined by the`equals`method;`false`otherwise |

| Exceptions ||
|----------------------------------|--------------------------------|
| `java.lang.NullPointerException` | if the specified value is null |

### containsKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun containsKey(key: K): Boolean
```

Tests if the specified object is a key in this table.

| Parameters ||
|-------|----------------|
| `key` | K:possible key |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if and only if the specified object is a key in this table, as determined by the`equals`method;`false`otherwise |

| Exceptions ||
|----------------------------------|-----------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null |

### containsKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun containsKey(key: K): Boolean
```

Tests if the specified object is a key in this table.

| Parameters ||
|-------|----------------|
| `key` | K:possible key |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if and only if the specified object is a key in this table, as determined by the`equals`method;`false`otherwise |

| Exceptions ||
|----------------------------------|-----------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null |

### containsValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun containsValue(value: V): Boolean
```

Returns`true`if this map maps one or more keys to the specified value. Note: This method may require a full traversal of the map, and is much slower than method`containsKey`.

| Parameters ||
|---------|----------------------------------------------------|
| `value` | V:value whose presence in this map is to be tested |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this map maps one or more keys to the specified value |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the value is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified value is null |

### containsValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun containsValue(value: V): Boolean
```

Returns`true`if this map maps one or more keys to the specified value. Note: This method may require a full traversal of the map, and is much slower than method`containsKey`.

| Parameters ||
|---------|----------------------------------------------------|
| `value` | V:value whose presence in this map is to be tested |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this map maps one or more keys to the specified value |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the value is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified value is null |

### elements

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun elements(): Enumeration<V>
```

Returns an enumeration of the values in this table.

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration.html#)<V> | an enumeration of the values in this table |

**See Also**

- [#values()](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#values:kotlin.collections.MutableCollection) 

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares the specified object with this map for equality. Returns`true`if the given object is a map with the same mappings as this map. This operation may return misleading results if either map is concurrently modified during execution of this method.

| Parameters ||
|-------|--------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | object to be compared for equality with this map |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the specified object is equal to this map |

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEach(action: BiConsumer<in K, in V>): Unit
```

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#)\<inK,inV\>:The action to be performed for each entry |

| Exceptions ||
|---------------------------------------------|-----------------------------------------------------|
| `java.lang.NullPointerException` | if the specified action is null |
| `java.util.ConcurrentModificationException` | if an entry is found to be removed during iteration |

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEach(
    parallelismThreshold: Long, 
    action: BiConsumer<in K, in V>
): Unit
```

Performs the given action for each (key, value).

| Parameters ||
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `action` | [BiConsumer](https://developer.android.com/reference/kotlin/java/util/function/BiConsumer.html#)\<inK,inV\>:the action |

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <U : Any!> forEach(
    parallelismThreshold: Long, 
    transformer: BiFunction<in K, in V, out U>, 
    action: Consumer<in U>
): Unit
```

Performs the given action for each non-null transformation of each (key, value).

| Parameters ||
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `transformer` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)\<inK,inV,outU\>:a function returning the transformation for an element, or null if there is no transformation (in which case the action is not applied) |
| `action` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\<inU\>:the action |
| `<U>` | the return type of the transformer |

### forEachEntry

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachEntry(
    parallelismThreshold: Long, 
    action: Consumer<in MutableEntry<K, V>!>
): Unit
```

Performs the given action for each entry.

| Parameters ||
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `action` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\<in [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>!\>:the action |

### forEachEntry

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <U : Any!> forEachEntry(
    parallelismThreshold: Long, 
    transformer: Function<MutableEntry<K, V>!, out U>, 
    action: Consumer<in U>
): Unit
```

Performs the given action for each non-null transformation of each entry.

| Parameters ||
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `transformer` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>!,outU\>:a function returning the transformation for an element, or null if there is no transformation (in which case the action is not applied) |
| `action` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\<inU\>:the action |
| `<U>` | the return type of the transformer |

### forEachKey

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachKey(
    parallelismThreshold: Long, 
    action: Consumer<in K>
): Unit
```

Performs the given action for each key.

| Parameters ||
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `action` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\<inK\>:the action |

### forEachKey

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <U : Any!> forEachKey(
    parallelismThreshold: Long, 
    transformer: Function<in K, out U>, 
    action: Consumer<in U>
): Unit
```

Performs the given action for each non-null transformation of each key.

| Parameters ||
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `transformer` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<inK,outU\>:a function returning the transformation for an element, or null if there is no transformation (in which case the action is not applied) |
| `action` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\<inU\>:the action |
| `<U>` | the return type of the transformer |

### forEachValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachValue(
    parallelismThreshold: Long, 
    action: Consumer<in V>
): Unit
```

Performs the given action for each value.

| Parameters ||
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `action` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\<inV\>:the action |

### forEachValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <U : Any!> forEachValue(
    parallelismThreshold: Long, 
    transformer: Function<in V, out U>, 
    action: Consumer<in U>
): Unit
```

Performs the given action for each non-null transformation of each value.

| Parameters ||
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `transformer` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<inV,outU\>:a function returning the transformation for an element, or null if there is no transformation (in which case the action is not applied) |
| `action` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\<inU\>:the action |
| `<U>` | the return type of the transformer |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(key: K): V?
```

Returns the value to which the specified key is mapped, or`null`if this map contains no mapping for the key.

More formally, if this map contains a mapping from a key`k`to a value`v`such that`key.equals(k)`, then this method returns`v`; otherwise it returns`null`. (There can be at most one such mapping.)

| Parameters ||
|-------|----------------------------------------------------|
| `key` | K:the key whose associated value is to be returned |

| Return ||
|----|-----------------------------------------------------------------------------------------------------|
| V? | the value to which the specified key is mapped, or`null`if this map contains no mapping for the key |

| Exceptions ||
|----------------------------------|-----------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(key: K): V?
```

Returns the value to which the specified key is mapped, or`null`if this map contains no mapping for the key.

More formally, if this map contains a mapping from a key`k`to a value`v`such that`key.equals(k)`, then this method returns`v`; otherwise it returns`null`. (There can be at most one such mapping.)

| Parameters ||
|-------|----------------------------------------------------|
| `key` | K:the key whose associated value is to be returned |

| Return ||
|----|-----------------------------------------------------------------------------------------------------|
| V? | the value to which the specified key is mapped, or`null`if this map contains no mapping for the key |

| Exceptions ||
|----------------------------------|-----------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null |

### getOrDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOrDefault(
    key: K, 
    defaultValue: V
): V
```

Returns the value to which the specified key is mapped, or the given default value if this map contains no mapping for the key.

| Parameters ||
|----------------|-------------------------------------------------------------------------|
| `key` | K:the key whose associated value is to be returned |
| `defaultValue` | V:the value to return if this map contains no mapping for the given key |

| Return ||
|---|-------------------------------------------------------------|
| V | the mapping for the key, if present; else the default value |

| Exceptions ||
|----------------------------------|-----------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns the hash code value for this [Map](https://developer.android.com/reference/kotlin/java/util/Map.html#), i.e., the sum of, for each key-value pair in the map,`key.hashCode() ^ value.hashCode()`.

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hash code value for this map |

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEmpty(): Boolean
```

Returns`true`if this map contains no key-value mappings.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this map contains no key-value mappings |

### keySet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun keySet(mappedValue: V): ConcurrentHashMap.KeySetView<K, V>
```

Returns a [Set](https://developer.android.com/reference/kotlin/java/util/Set.html#) view of the keys in this map, using the given common mapped value for any additions (i.e., [java.util.Collection#add](https://developer.android.com/reference/kotlin/java/util/Collection.html#add(java.util.Collection.E))and [Collection.addAll(Collection)](https://developer.android.com/reference/kotlin/java/util/Collection.html#addAll(kotlin.collections.MutableCollection))). This is of course only appropriate if it is acceptable to use the same value for all additions from this view.

| Parameters ||
|---------------|---------------------------------------------|
| `mappedValue` | V:the mapped value to use for any additions |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [ConcurrentHashMap.KeySetView](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap.KeySetView)<K,` `V> | the set view |

| Exceptions ||
|----------------------------------|----------------------------|
| `java.lang.NullPointerException` | if the mappedValue is null |

### keys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun keys(): Enumeration<K>
```

Returns an enumeration of the keys in this table.

| Return ||
|----------------------------------------------------------------------------------------------|------------------------------------------|
| [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration.html#)<K> | an enumeration of the keys in this table |

**See Also**

- [#keySet()](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#keys:kotlin.collections.MutableSet) 

### mappingCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mappingCount(): Long
```

Returns the number of mappings. This method should be used instead of [size](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap#size:kotlin.Int) because a ConcurrentHashMap may contain more mappings than can be represented as an int. The value returned is an estimate; the actual count may differ if there are concurrent insertions or removals.

| Return ||
|------------------------------------------------------------------------------|------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the number of mappings |

### merge

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun merge(
    key: K, 
    value: V, 
    remappingFunction: BiFunction<in V, in V, out V?>
): V?
```

If the specified key is not already associated with a (non-null) value, associates it with the given value. Otherwise, replaces the value with the results of the given remapping function, or removes if`null`. The entire method invocation is performed atomically. Some attempted update operations on this map by other threads may be blocked while computation is in progress, so the computation should be short and simple, and must not attempt to update any other mappings of this Map.

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | K:key with which the specified value is to be associated |
| `value` | V:the value to use if absent |
| `remappingFunction` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)\<inV,inV,outV?\>:the function to recompute a value if present |

| Return ||
|----|------------------------------------------------------------------|
| V? | the new value associated with the specified key, or null if none |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map (java.util.Collection#) |
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key or the remappingFunction is null |
| `java.lang.RuntimeException` | or Error if the remappingFunction does so, in which case the mapping is unchanged |

### newKeySet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <K : Any!> newKeySet(): ConcurrentHashMap.KeySetView<K, Boolean!>
```

Creates a new [Set](https://developer.android.com/reference/kotlin/java/util/Set.html#) backed by a ConcurrentHashMap from the given type to`Boolean.TRUE`.

| Parameters ||
|-------|--------------------------------------|
| `<K>` | the element type of the returned set |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| [ConcurrentHashMap.KeySetView](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap.KeySetView)<K,` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!> | the new set |

### newKeySet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <K : Any!> newKeySet(initialCapacity: Int): ConcurrentHashMap.KeySetView<K, Boolean!>
```

Creates a new [Set](https://developer.android.com/reference/kotlin/java/util/Set.html#) backed by a ConcurrentHashMap from the given type to`Boolean.TRUE`.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `initialCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The implementation performs internal sizing to accommodate this many elements. |
| `<K>` | the element type of the returned set |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| [ConcurrentHashMap.KeySetView](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap.KeySetView)<K,` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!> | the new set |

| Exceptions ||
|--------------------------------------|-------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the initial capacity of elements is negative |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    key: K, 
    value: V
): V?
```

Maps the specified key to the specified value in this table. Neither the key nor the value can be null.

The value can be retrieved by calling the`get`method with a key that is equal to the original key.

| Parameters ||
|---------|----------------------------------------------------------|
| `key` | K:key with which the specified value is to be associated |
| `value` | V:value to be associated with the specified key |

| Return ||
|----|-----------------------------------------------------------------------------------|
| V? | the previous value associated with`key`, or`null`if there was no mapping for`key` |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map |
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified key or value is null |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map |

### putAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putAll(from: Map<out K, V>): Unit
```

Copies all of the mappings from the specified map to this one. These mappings replace any mappings that this map had for any of the keys currently in the specified map.

| Parameters ||
|-----|-----------------------------------|
| `m` | mappings to be stored in this map |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`putAll`operation is not supported by this map |
| `java.lang.ClassCastException` | if the class of a key or value in the specified map prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified map is null, or if this map does not permit null keys or values, and the specified map contains null keys or values |
| `java.lang.IllegalArgumentException` | if some property of a key or value in the specified map prevents it from being stored in this map |

### putIfAbsent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putIfAbsent(
    key: K, 
    value: V
): V?
```

If the specified key is not already associated with a value (or is mapped to`null`) associates it with the given value and returns`null`, else returns the current value.

| Parameters ||
|---------|----------------------------------------------------------|
| `key` | K:key with which the specified value is to be associated |
| `value` | V:value to be associated with the specified key |

| Return ||
|----|---------------------------------------------------------------------------------------------------|
| V? | the previous value associated with the specified key, or`null`if there was no mapping for the key |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map |
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified key or value is null |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map |

### reduce

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <U : Any!> reduce(
    parallelismThreshold: Long, 
    transformer: BiFunction<in K, in V, out U>, 
    reducer: BiFunction<in U, in U, out U>
): U?
```

Returns the result of accumulating the given transformation of all (key, value) pairs using the given reducer to combine values, or null if none.

| Parameters ||
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `transformer` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)\<inK,inV,outU\>:a function returning the transformation for an element, or null if there is no transformation (in which case it is not combined) |
| `reducer` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)\<inU,inU,outU\>:a commutative associative combining function |
| `<U>` | the return type of the transformer |

| Return ||
|----|-------------------------------------------------------------------------------|
| U? | the result of accumulating the given transformation of all (key, value) pairs |

### reduceEntries

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reduceEntries(
    parallelismThreshold: Long, 
    reducer: BiFunction<MutableEntry<K, V>!, MutableEntry<K, V>!, out MutableEntry<K, V>!>
): MutableEntry<K, V>?
```

Returns the result of accumulating all entries using the given reducer to combine values, or null if none.

| Parameters ||
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `reducer` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>!, [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>!,out [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>!\>:a commutative associative combining function |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>? | the result of accumulating all entries |

### reduceEntries

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <U : Any!> reduceEntries(
    parallelismThreshold: Long, 
    transformer: Function<MutableEntry<K, V>!, out U>, 
    reducer: BiFunction<in U, in U, out U>
): U?
```

Returns the result of accumulating the given transformation of all entries using the given reducer to combine values, or null if none.

| Parameters ||
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `transformer` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>!,outU\>:a function returning the transformation for an element, or null if there is no transformation (in which case it is not combined) |
| `reducer` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)\<inU,inU,outU\>:a commutative associative combining function |
| `<U>` | the return type of the transformer |

| Return ||
|----|--------------------------------------------------------------------|
| U? | the result of accumulating the given transformation of all entries |

### reduceEntriesToDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reduceEntriesToDouble(
    parallelismThreshold: Long, 
    transformer: ToDoubleFunction<MutableEntry<K, V>!>, 
    basis: Double, 
    reducer: DoubleBinaryOperator
): Double
```

Returns the result of accumulating the given transformation of all entries using the given reducer to combine values, and the given basis as an identity value.

| Parameters ||
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `transformer` | [ToDoubleFunction](https://developer.android.com/reference/kotlin/java/util/function/ToDoubleFunction.html#)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>!\>:a function returning the transformation for an element |
| `basis` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the identity (initial default value) for the reduction |
| `reducer` | [DoubleBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleBinaryOperator.html#):a commutative associative combining function |

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the result of accumulating the given transformation of all entries |

### reduceEntriesToInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reduceEntriesToInt(
    parallelismThreshold: Long, 
    transformer: ToIntFunction<MutableEntry<K, V>!>, 
    basis: Int, 
    reducer: IntBinaryOperator
): Int
```

Returns the result of accumulating the given transformation of all entries using the given reducer to combine values, and the given basis as an identity value.

| Parameters ||
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `transformer` | [ToIntFunction](https://developer.android.com/reference/kotlin/java/util/function/ToIntFunction.html#)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>!\>:a function returning the transformation for an element |
| `basis` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the identity (initial default value) for the reduction |
| `reducer` | [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#):a commutative associative combining function |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the result of accumulating the given transformation of all entries |

### reduceEntriesToLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reduceEntriesToLong(
    parallelismThreshold: Long, 
    transformer: ToLongFunction<MutableEntry<K, V>!>, 
    basis: Long, 
    reducer: LongBinaryOperator
): Long
```

Returns the result of accumulating the given transformation of all entries using the given reducer to combine values, and the given basis as an identity value.

| Parameters ||
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `transformer` | [ToLongFunction](https://developer.android.com/reference/kotlin/java/util/function/ToLongFunction.html#)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>!\>:a function returning the transformation for an element |
| `basis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the identity (initial default value) for the reduction |
| `reducer` | [LongBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator.html#):a commutative associative combining function |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the result of accumulating the given transformation of all entries |

### reduceKeys

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reduceKeys(
    parallelismThreshold: Long, 
    reducer: BiFunction<in K, in K, out K>
): K?
```

Returns the result of accumulating all keys using the given reducer to combine values, or null if none.

| Parameters ||
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `reducer` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)\<inK,inK,outK\>:a commutative associative combining function |

| Return ||
|----|------------------------------------------------------------------------------------------------|
| K? | the result of accumulating all keys using the given reducer to combine values, or null if none |

### reduceKeys

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <U : Any!> reduceKeys(
    parallelismThreshold: Long, 
    transformer: Function<in K, out U>, 
    reducer: BiFunction<in U, in U, out U>
): U?
```

Returns the result of accumulating the given transformation of all keys using the given reducer to combine values, or null if none.

| Parameters ||
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `transformer` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<inK,outU\>:a function returning the transformation for an element, or null if there is no transformation (in which case it is not combined) |
| `reducer` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)\<inU,inU,outU\>:a commutative associative combining function |
| `<U>` | the return type of the transformer |

| Return ||
|----|-----------------------------------------------------------------|
| U? | the result of accumulating the given transformation of all keys |

### reduceKeysToDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reduceKeysToDouble(
    parallelismThreshold: Long, 
    transformer: ToDoubleFunction<in K>, 
    basis: Double, 
    reducer: DoubleBinaryOperator
): Double
```

Returns the result of accumulating the given transformation of all keys using the given reducer to combine values, and the given basis as an identity value.

| Parameters ||
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `transformer` | [ToDoubleFunction](https://developer.android.com/reference/kotlin/java/util/function/ToDoubleFunction.html#)\<inK\>:a function returning the transformation for an element |
| `basis` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the identity (initial default value) for the reduction |
| `reducer` | [DoubleBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleBinaryOperator.html#):a commutative associative combining function |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the result of accumulating the given transformation of all keys |

### reduceKeysToInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reduceKeysToInt(
    parallelismThreshold: Long, 
    transformer: ToIntFunction<in K>, 
    basis: Int, 
    reducer: IntBinaryOperator
): Int
```

Returns the result of accumulating the given transformation of all keys using the given reducer to combine values, and the given basis as an identity value.

| Parameters ||
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `transformer` | [ToIntFunction](https://developer.android.com/reference/kotlin/java/util/function/ToIntFunction.html#)\<inK\>:a function returning the transformation for an element |
| `basis` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the identity (initial default value) for the reduction |
| `reducer` | [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#):a commutative associative combining function |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the result of accumulating the given transformation of all keys |

### reduceKeysToLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reduceKeysToLong(
    parallelismThreshold: Long, 
    transformer: ToLongFunction<in K>, 
    basis: Long, 
    reducer: LongBinaryOperator
): Long
```

Returns the result of accumulating the given transformation of all keys using the given reducer to combine values, and the given basis as an identity value.

| Parameters ||
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `transformer` | [ToLongFunction](https://developer.android.com/reference/kotlin/java/util/function/ToLongFunction.html#)\<inK\>:a function returning the transformation for an element |
| `basis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the identity (initial default value) for the reduction |
| `reducer` | [LongBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator.html#):a commutative associative combining function |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the result of accumulating the given transformation of all keys |

### reduceToDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reduceToDouble(
    parallelismThreshold: Long, 
    transformer: ToDoubleBiFunction<in K, in V>, 
    basis: Double, 
    reducer: DoubleBinaryOperator
): Double
```

Returns the result of accumulating the given transformation of all (key, value) pairs using the given reducer to combine values, and the given basis as an identity value.

| Parameters ||
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `transformer` | [ToDoubleBiFunction](https://developer.android.com/reference/kotlin/java/util/function/ToDoubleBiFunction.html#)\<inK,inV\>:a function returning the transformation for an element |
| `basis` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the identity (initial default value) for the reduction |
| `reducer` | [DoubleBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleBinaryOperator.html#):a commutative associative combining function |

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the result of accumulating the given transformation of all (key, value) pairs |

### reduceToInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reduceToInt(
    parallelismThreshold: Long, 
    transformer: ToIntBiFunction<in K, in V>, 
    basis: Int, 
    reducer: IntBinaryOperator
): Int
```

Returns the result of accumulating the given transformation of all (key, value) pairs using the given reducer to combine values, and the given basis as an identity value.

| Parameters ||
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `transformer` | [ToIntBiFunction](https://developer.android.com/reference/kotlin/java/util/function/ToIntBiFunction.html#)\<inK,inV\>:a function returning the transformation for an element |
| `basis` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the identity (initial default value) for the reduction |
| `reducer` | [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#):a commutative associative combining function |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the result of accumulating the given transformation of all (key, value) pairs |

### reduceToLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reduceToLong(
    parallelismThreshold: Long, 
    transformer: ToLongBiFunction<in K, in V>, 
    basis: Long, 
    reducer: LongBinaryOperator
): Long
```

Returns the result of accumulating the given transformation of all (key, value) pairs using the given reducer to combine values, and the given basis as an identity value.

| Parameters ||
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `transformer` | [ToLongBiFunction](https://developer.android.com/reference/kotlin/java/util/function/ToLongBiFunction.html#)\<inK,inV\>:a function returning the transformation for an element |
| `basis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the identity (initial default value) for the reduction |
| `reducer` | [LongBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator.html#):a commutative associative combining function |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the result of accumulating the given transformation of all (key, value) pairs |

### reduceValues

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reduceValues(
    parallelismThreshold: Long, 
    reducer: BiFunction<in V, in V, out V>
): V?
```

Returns the result of accumulating all values using the given reducer to combine values, or null if none.

| Parameters ||
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `reducer` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)\<inV,inV,outV\>:a commutative associative combining function |

| Return ||
|----|---------------------------------------|
| V? | the result of accumulating all values |

### reduceValues

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <U : Any!> reduceValues(
    parallelismThreshold: Long, 
    transformer: Function<in V, out U>, 
    reducer: BiFunction<in U, in U, out U>
): U?
```

Returns the result of accumulating the given transformation of all values using the given reducer to combine values, or null if none.

| Parameters ||
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `transformer` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<inV,outU\>:a function returning the transformation for an element, or null if there is no transformation (in which case it is not combined) |
| `reducer` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)\<inU,inU,outU\>:a commutative associative combining function |
| `<U>` | the return type of the transformer |

| Return ||
|----|-------------------------------------------------------------------|
| U? | the result of accumulating the given transformation of all values |

### reduceValuesToDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reduceValuesToDouble(
    parallelismThreshold: Long, 
    transformer: ToDoubleFunction<in V>, 
    basis: Double, 
    reducer: DoubleBinaryOperator
): Double
```

Returns the result of accumulating the given transformation of all values using the given reducer to combine values, and the given basis as an identity value.

| Parameters ||
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `transformer` | [ToDoubleFunction](https://developer.android.com/reference/kotlin/java/util/function/ToDoubleFunction.html#)\<inV\>:a function returning the transformation for an element |
| `basis` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the identity (initial default value) for the reduction |
| `reducer` | [DoubleBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleBinaryOperator.html#):a commutative associative combining function |

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the result of accumulating the given transformation of all values |

### reduceValuesToInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reduceValuesToInt(
    parallelismThreshold: Long, 
    transformer: ToIntFunction<in V>, 
    basis: Int, 
    reducer: IntBinaryOperator
): Int
```

Returns the result of accumulating the given transformation of all values using the given reducer to combine values, and the given basis as an identity value.

| Parameters ||
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `transformer` | [ToIntFunction](https://developer.android.com/reference/kotlin/java/util/function/ToIntFunction.html#)\<inV\>:a function returning the transformation for an element |
| `basis` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the identity (initial default value) for the reduction |
| `reducer` | [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#):a commutative associative combining function |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the result of accumulating the given transformation of all values |

### reduceValuesToLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reduceValuesToLong(
    parallelismThreshold: Long, 
    transformer: ToLongFunction<in V>, 
    basis: Long, 
    reducer: LongBinaryOperator
): Long
```

Returns the result of accumulating the given transformation of all values using the given reducer to combine values, and the given basis as an identity value.

| Parameters ||
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `transformer` | [ToLongFunction](https://developer.android.com/reference/kotlin/java/util/function/ToLongFunction.html#)\<inV\>:a function returning the transformation for an element |
| `basis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the identity (initial default value) for the reduction |
| `reducer` | [LongBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator.html#):a commutative associative combining function |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the result of accumulating the given transformation of all values |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(key: K): V?
```

Removes the key (and its corresponding value) from this map. This method does nothing if the key is not in the map.

| Parameters ||
|-------|------------------------------------|
| `key` | K:the key that needs to be removed |

| Return ||
|----|-----------------------------------------------------------------------------------|
| V? | the previous value associated with`key`, or`null`if there was no mapping for`key` |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this map |
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(
    key: K, 
    value: V
): Boolean
```

Removes the entry for the specified key only if it is currently mapped to the specified value.

| Parameters ||
|---------|----------------------------------------------------------|
| `key` | K:key with which the specified value is associated |
| `value` | V:value expected to be associated with the specified key |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the value was removed |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this map |
| `java.lang.ClassCastException` | if the key or value is of an inappropriate type for this map ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified key is null |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(key: K): V?
```

Removes the key (and its corresponding value) from this map. This method does nothing if the key is not in the map.

| Parameters ||
|-------|------------------------------------|
| `key` | K:the key that needs to be removed |

| Return ||
|----|-----------------------------------------------------------------------------------|
| V? | the previous value associated with`key`, or`null`if there was no mapping for`key` |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this map |
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null |

### replace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun replace(
    key: K, 
    value: V
): V?
```

Replaces the entry for the specified key only if it is currently mapped to some value.

| Parameters ||
|---------|----------------------------------------------------|
| `key` | K:key with which the specified value is associated |
| `value` | V:value to be associated with the specified key |

| Return ||
|----|---------------------------------------------------------------------------------------------------|
| V? | the previous value associated with the specified key, or`null`if there was no mapping for the key |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map |
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified key or value is null |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map |

### replace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun replace(
    key: K, 
    oldValue: V, 
    newValue: V
): Boolean
```

Replaces the entry for the specified key only if currently mapped to the specified value.

| Parameters ||
|------------|----------------------------------------------------------|
| `key` | K:key with which the specified value is associated |
| `oldValue` | V:value expected to be associated with the specified key |
| `newValue` | V:value to be associated with the specified key |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the value was replaced |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map |
| `java.lang.ClassCastException` | if the class of a specified key or value prevents it from being stored in this map |
| `java.lang.NullPointerException` | if any of the arguments are null |
| `java.lang.IllegalArgumentException` | if some property of a specified key or value prevents it from being stored in this map |

### replaceAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun replaceAll(function: BiFunction<in K, in V, out V>): Unit
```

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `function` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)\<inK,inV,outV\>:the function to apply to each entry |

| Exceptions ||
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`set`operation is not supported by this map's entry set iterator. |
| `java.lang.ClassCastException` | if the class of a replacement value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified function is null, or if a replacement value is null and this map does not permit null values (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of a replacement value prevents it from being stored in this map (java.util.Collection#) |
| `java.util.ConcurrentModificationException` | if an entry is found to be removed during iteration |

### search

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <U : Any!> search(
    parallelismThreshold: Long, 
    searchFunction: BiFunction<in K, in V, out U>
): U?
```

Returns a non-null result from applying the given search function on each (key, value), or null if none. Upon success, further element processing is suppressed and the results of any other parallel invocations of the search function are ignored.

| Parameters ||
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `searchFunction` | [BiFunction](https://developer.android.com/reference/kotlin/java/util/function/BiFunction.html#)\<inK,inV,outU\>:a function returning a non-null result on success, else null |
| `<U>` | the return type of the search function |

| Return ||
|----|-------------------------------------------------------------------------------------------------|
| U? | a non-null result from applying the given search function on each (key, value), or null if none |

### searchEntries

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <U : Any!> searchEntries(
    parallelismThreshold: Long, 
    searchFunction: Function<MutableEntry<K, V>!, out U>
): U?
```

Returns a non-null result from applying the given search function on each entry, or null if none. Upon success, further element processing is suppressed and the results of any other parallel invocations of the search function are ignored.

| Parameters ||
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `searchFunction` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>!,outU\>:a function returning a non-null result on success, else null |
| `<U>` | the return type of the search function |

| Return ||
|----|------------------------------------------------------------------------------------------|
| U? | a non-null result from applying the given search function on each entry, or null if none |

### searchKeys

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <U : Any!> searchKeys(
    parallelismThreshold: Long, 
    searchFunction: Function<in K, out U>
): U?
```

Returns a non-null result from applying the given search function on each key, or null if none. Upon success, further element processing is suppressed and the results of any other parallel invocations of the search function are ignored.

| Parameters ||
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `searchFunction` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<inK,outU\>:a function returning a non-null result on success, else null |
| `<U>` | the return type of the search function |

| Return ||
|----|----------------------------------------------------------------------------------------|
| U? | a non-null result from applying the given search function on each key, or null if none |

### searchValues

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <U : Any!> searchValues(
    parallelismThreshold: Long, 
    searchFunction: Function<in V, out U>
): U?
```

Returns a non-null result from applying the given search function on each value, or null if none. Upon success, further element processing is suppressed and the results of any other parallel invocations of the search function are ignored.

| Parameters ||
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parallelismThreshold` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the (estimated) number of elements needed for this operation to be executed in parallel |
| `searchFunction` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\<inV,outU\>:a function returning a non-null result on success, else null |
| `<U>` | the return type of the search function |

| Return ||
|----|------------------------------------------------------------------------------------------|
| U? | a non-null result from applying the given search function on each value, or null if none |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of this map. The string representation consists of a list of key-value mappings (in no particular order) enclosed in braces ("`{}`"). Adjacent mappings are separated by the characters`", "`(comma and space). Each key-value mapping is rendered as the key followed by an equals sign ("`=`") followed by the associated value.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this map |

## Properties

### entries

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val entries: MutableSet<MutableEntry<K, V>>
```

Returns a [Set](https://developer.android.com/reference/kotlin/java/util/Set.html#) view of the mappings contained in this map. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. The set supports element removal, which removes the corresponding mapping from the map, via the`Iterator.remove`,`Set.remove`,`removeAll`,`retainAll`, and`clear`operations.

The view's iterators and spliterators are [*weakly consistent*](https://developer.android.com/reference/kotlin/java/util/concurrent/package-summary#Weakly).

The view's`spliterator`reports [Spliterator.CONCURRENT](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#CONCURRENT:kotlin.Int), [Spliterator.DISTINCT](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#DISTINCT:kotlin.Int), and [Spliterator.NONNULL](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#NONNULL:kotlin.Int).

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>> | the set view |

### keys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val keys: MutableSet<K>
```

Returns a [Set](https://developer.android.com/reference/kotlin/java/util/Set.html#) view of the keys contained in this map. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. The set supports element removal, which removes the corresponding mapping from this map, via the`Iterator.remove`,`Set.remove`,`removeAll`,`retainAll`, and`clear`operations. It does not support the`add`or`addAll`operations.

The set returned by this method is guaranteed to an instance of [KeySetView](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentHashMap.KeySetView).

The view's iterators and spliterators are [*weakly consistent*](https://developer.android.com/reference/kotlin/java/util/concurrent/package-summary#Weakly).

The view's`spliterator`reports [Spliterator.CONCURRENT](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#CONCURRENT:kotlin.Int), [Spliterator.DISTINCT](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#DISTINCT:kotlin.Int), and [Spliterator.NONNULL](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#NONNULL:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------------------------------------|--------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<K> | the set view |

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val size: Int
```

Returns the number of key-value mappings in this map. If the map contains more than`Integer.MAX_VALUE`elements, returns`Integer.MAX_VALUE`.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of key-value mappings in this map |

### values

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val values: MutableCollection<V>
```

Returns a [Collection](https://developer.android.com/reference/kotlin/java/util/Collection.html#) view of the values contained in this map. The collection is backed by the map, so changes to the map are reflected in the collection, and vice-versa. The collection supports element removal, which removes the corresponding mapping from this map, via the`Iterator.remove`,`Collection.remove`,`removeAll`,`retainAll`, and`clear`operations. It does not support the`add`or`addAll`operations.

The view's iterators and spliterators are [*weakly consistent*](https://developer.android.com/reference/kotlin/java/util/concurrent/package-summary#Weakly).

The view's`spliterator`reports [Spliterator.CONCURRENT](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#CONCURRENT:kotlin.Int) and [Spliterator.NONNULL](https://developer.android.com/reference/kotlin/java/util/Spliterator.html#NONNULL:kotlin.Int).

| Return ||
|------------------------------------------------------------------------------------------------------------------------|---------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<V> | the collection view |
