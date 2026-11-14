# IdentityHashMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IdentityHashMap

```
open class IdentityHashMap<K : Any!, V : Any!> : AbstractMap<K, V>, Cloneable, MutableMap<K, V>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.AbstractMap](AbstractMap.md)\<K, V\> ||
| | ↳ | [java.util.IdentityHashMap](IdentityHashMap.md) |

This class implements the`Map`interface with a hash table, using reference-equality in place of object-equality when comparing keys (and values). In other words, in an`IdentityHashMap`, two keys`k1`and`k2`are considered equal if and only if`(k1==k2)`. (In normal`Map`implementations (like`HashMap`) two keys`k1`and`k2`are considered equal if and only if`(k1==null ? k2==null : k1.equals(k2))`.)

**This class is*not* a general-purpose`Map`implementation! While this class implements the`Map`interface, it intentionally violates`Map's`general contract, which mandates the use of the`equals`method when comparing objects. This class is designed for use only in the rare cases wherein reference-equality semantics are required.**

The view collections of this map also have reference-equality semantics for their elements. See the (, (, and ( methods for further information.

A typical use of this class is*topology-preserving object graph transformations* , such as serialization or deep-copying. To perform such a transformation, a program must maintain a "node table" that keeps track of all the object references that have already been processed. The node table must not equate distinct objects even if they happen to be equal. Another typical use of this class is to maintain*proxy objects*. For example, a debugging facility might wish to maintain a proxy object for each object in the program being debugged.

This class provides all of the optional map operations, and permits`null`values and the`null`key. This class makes no guarantees as to the order of the map; in particular, it does not guarantee that the order will remain constant over time.

This class provides constant-time performance for the basic operations (`get`and`put`), assuming the system identity hash function ([System.identityHashCode(Object)](../java.lang/System.md))) disperses elements properly among the buckets.

This class has one tuning parameter (which affects performance but not semantics):*expected maximum size*. This parameter is the maximum number of key-value mappings that the map is expected to hold. Internally, this parameter is used to determine the number of buckets initially comprising the hash table. The precise relationship between the expected maximum size and the number of buckets is unspecified.

If the size of the map (the number of key-value mappings) sufficiently exceeds the expected maximum size, the number of buckets is increased. Increasing the number of buckets ("rehashing") may be fairly expensive, so it pays to create identity hash maps with a sufficiently large expected maximum size. On the other hand, iteration over collection views requires time proportional to the number of buckets in the hash table, so it pays not to set the expected maximum size too high if you are especially concerned with iteration performance or memory usage.

**Note that this implementation is not synchronized.** If multiple threads access an identity hash map concurrently, and at least one of the threads modifies the map structurally, it*must* be synchronized externally. (A structural modification is any operation that adds or deletes one or more mappings; merely changing the value associated with a key that an instance already contains is not a structural modification.) This is typically accomplished by synchronizing on some object that naturally encapsulates the map. If no such object exists, the map should be "wrapped" using the [Collections.synchronizedMap](Collections.md))method. This is best done at creation time, to prevent accidental unsynchronized access to the map: 

```kotlin
Map m = Collections.synchronizedMap(new IdentityHashMap(...));
```

The iterators returned by the`iterator`method of the collections returned by all of this class's "collection view methods" are*fail-fast* : if the map is structurally modified at any time after the iterator is created, in any way except through the iterator's own`remove`method, the iterator will throw a [ConcurrentModificationException](ConcurrentModificationException.md). Thus, in the face of concurrent modification, the iterator fails quickly and cleanly, rather than risking arbitrary, non-deterministic behavior at an undetermined time in the future.

Note that the fail-fast behavior of an iterator cannot be guaranteed as it is, generally speaking, impossible to make any hard guarantees in the presence of unsynchronized concurrent modification. Fail-fast iterators throw`ConcurrentModificationException`on a best-effort basis. Therefore, it would be wrong to write a program that depended on this exception for its correctness:*fail-fast iterators should be used only to detect bugs.*

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IdentityHashMap](IdentityHashMap.md))`()` Constructs a new, empty identity hash map with a default expected maximum size (21). |
| [IdentityHashMap](IdentityHashMap.md))`(`expectedMaxSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a new, empty map with the specified expected maximum size. |
| [IdentityHashMap](IdentityHashMap.md))`(`m:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)<out` `K,` `out` `V>!`)` Constructs a new identity hash map containing the keys-value mappings in the specified map. |

| Public methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](IdentityHashMap.md))`()` Removes all of the mappings from this map. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](IdentityHashMap.md))`()` Returns a shallow copy of this identity hash map: the keys and values themselves are not cloned. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsKey](IdentityHashMap.md))`(`key:` `K?`)` Tests whether the specified object reference is a key in this identity hash map. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsValue](IdentityHashMap.md))`(`value:` `V?`)` Tests whether the specified object reference is a value in this identity hash map. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](IdentityHashMap.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares the specified object with this map for equality. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](IdentityHashMap.md))`(`action:` ` [BiConsumer](../java.util.function/BiConsumer.md)<in` `K,` `in` `V>`)` <br /> |
| --- | --- |
| openV? | [get](IdentityHashMap.md))`(`key:` `K?`)` Returns the value to which the specified key is mapped, or`null`if this map contains no mapping for the key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](IdentityHashMap.md))`()` Returns the hash code value for this map. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](IdentityHashMap.md))`()` Returns`true`if this identity hash map contains no key-value mappings. |
| --- | --- |
| openV? | [put](IdentityHashMap.md))`(`key:` `K`, `value:` `V`)` Associates the specified value with the specified key in this identity hash map. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putAll](IdentityHashMap.md))`(`from:` ` [Map](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-map/index.html)<out` `K,` `V>`)` Copies all of the mappings from the specified map to this map. |
| openV? | [remove](IdentityHashMap.md))`(`key:` `K?`)` Removes the mapping for this key from this map if present. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](IdentityHashMap.md))`(`key:` `K`, `value:` `V`)` Removes the entry for the specified key only if it is currently mapped to the specified value. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [replace](IdentityHashMap.md))`(`key:` `K`, `oldValue:` `V`, `newValue:` `V`)` Replaces the entry for the specified key only if currently mapped to the specified value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [replaceAll](IdentityHashMap.md))`(`function:` ` [BiFunction](../java.util.function/BiFunction.md)<in` `K,` `in` `V,` `out` `V>`)` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [AbstractMap](AbstractMap.md) |----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](AbstractMap.md))`()` <br /> Returns a string representation of this map. The string representation consists of a list of key-value mappings in the order returned by the map's`entrySet`view's iterator, enclosed in braces (`"{}"`). Adjacent mappings are separated by the characters`", "`(comma and space). Each key-value mapping is rendered as the key followed by an equals sign (`"="`) followed by the associated value. Keys and values are converted to strings as by [String.valueOf(Object)](../java.lang/String.md)). <br /> | ||

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>\> | [entries](IdentityHashMap.md) Returns a [Set](Set.md) view of the mappings contained in this map. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<K\> | [keys](IdentityHashMap.md) Returns an identity-based set view of the keys contained in this map. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](IdentityHashMap.md) Returns the number of key-value mappings in this identity hash map. |
| --- | --- |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<V\> | [values](IdentityHashMap.md) Returns a [Collection](Collection.md) view of the values contained in this map. |

## Public constructors

### IdentityHashMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IdentityHashMap()
```

Constructs a new, empty identity hash map with a default expected maximum size (21). 

### IdentityHashMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IdentityHashMap(expectedMaxSize: Int)
```

Constructs a new, empty map with the specified expected maximum size. Putting more than the expected number of key-value mappings into the map may cause the internal data structure to grow, which may be somewhat time-consuming.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------|
| `expectedMaxSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected maximum size of the map |

| Exceptions ||
|--------------------------------------|--------------------------------|
| `java.lang.IllegalArgumentException` | if`expectedMaxSize`is negative |

### IdentityHashMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IdentityHashMap(m: MutableMap<out K, out V>!)
```

Constructs a new identity hash map containing the keys-value mappings in the specified map.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `m` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<outK,outV\>!:the map whose mappings are to be placed into this map |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.NullPointerException` | if the specified map is null |

## Public methods

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Removes all of the mappings from this map. The map will be empty after this call returns.

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`clear`operation is not supported by this map |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Returns a shallow copy of this identity hash map: the keys and values themselves are not cloned.

| Return ||
|----------------------------------------------------------------------------|----------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a shallow copy of this map |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### containsKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun containsKey(key: K?): Boolean
```

Tests whether the specified object reference is a key in this identity hash map. Returns`true`if and only if this map contains a mapping with key`k`such that`(key == k)`.

| Parameters ||
|-------|-----------------|
| `key` | K?:possible key |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the specified object reference is a key in this map |

| Exceptions ||
|----------------------------------|---------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |

**See Also**

- [#containsValue(Object)](IdentityHashMap.md)) 

### containsValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun containsValue(value: V?): Boolean
```

Tests whether the specified object reference is a value in this identity hash map. Returns`true`if and only if this map contains a mapping with value`v`such that`(value == v)`.

| Parameters ||
|---------|-----------------------------------------------------|
| `value` | V?:value whose presence in this map is to be tested |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this map maps one or more keys to the specified object reference |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the value is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified value is null and this map does not permit null values (java.util.Collection#) |

**See Also**

- [#containsKey(Object)](IdentityHashMap.md)) 

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares the specified object with this map for equality. Returns`true`if the given object is also a map and the two maps represent identical object-reference mappings. More formally, this map is equal to another map`m`if and only if`this.entrySet().equals(m.entrySet())`. See the ( method for the specification of equality of this map's entries.

**Owing to the reference-equality-based semantics of this map it is possible that the symmetry and transitivity requirements of the`Object.equals`contract may be violated if this map is compared to a normal map. However, the`Object.equals`contract is guaranteed to hold among`IdentityHashMap`instances.**

| Parameters ||
|-------|--------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | object to be compared for equality with this map |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the specified object is equal to this map |

**See Also**

- [java.lang.Object#equals(Object)](../java.lang/Object.md)) 

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEach(action: BiConsumer<in K, in V>): Unit
```

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [BiConsumer](../java.util.function/BiConsumer.md)\<inK,inV\>:The action to be performed for each entry |

| Exceptions ||
|---------------------------------------------|-----------------------------------------------------|
| `java.lang.NullPointerException` | if the specified action is null |
| `java.util.ConcurrentModificationException` | if an entry is found to be removed during iteration |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(key: K?): V?
```

Returns the value to which the specified key is mapped, or`null`if this map contains no mapping for the key.

More formally, if this map contains a mapping from a key`k`to a value`v`such that`(key == k)`, then this method returns`v`; otherwise it returns`null`. (There can be at most one such mapping.)

A return value of`null`does not*necessarily* indicate that the map contains no mapping for the key; it's also possible that the map explicitly maps the key to`null`. The [containsKey](IdentityHashMap.md))operation may be used to distinguish these two cases.

| Parameters ||
|-------|-----------------------------------------------------|
| `key` | K?:the key whose associated value is to be returned |

| Return ||
|----|-----------------------------------------------------------------------------------------------------|
| V? | the value to which the specified key is mapped, or`null`if this map contains no mapping for the key |

| Exceptions ||
|----------------------------------|---------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |

**See Also**

- [#put(Object, Object)](IdentityHashMap.md)) 

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns the hash code value for this map. The hash code of a map is defined to be the sum of the hash codes of each entry of this map. See the ( method for a specification of the hash code of this map's entries.

This specification ensures that`m1.equals(m2)`implies that`m1.hashCode()==m2.hashCode()`for any two`IdentityHashMap`instances`m1`and`m2`, as required by the general contract of [Object.hashCode](../java.lang/Object.md)).

**Owing to the reference-equality-based semantics of the`Map.Entry`instances in the set returned by this map's`entrySet`method, it is possible that the contractual requirement of`Object.hashCode`mentioned in the previous paragraph will be violated if one of the two objects being compared is an`IdentityHashMap`instance and the other is a normal map.**

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hash code value for this map |

**See Also**

- [java.lang.Object#equals(Object)](../java.lang/Object.md))
- [#equals(Object)](IdentityHashMap.md)) 

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEmpty(): Boolean
```

Returns`true`if this identity hash map contains no key-value mappings.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this identity hash map contains no key-value mappings |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    key: K, 
    value: V
): V?
```

Associates the specified value with the specified key in this identity hash map. If this map already ( a mapping for the key, the old value is replaced, otherwise, a new mapping is inserted into this map.

| Parameters ||
|---------|--------------------------------------------------------------|
| `key` | K:the key with which the specified value is to be associated |
| `value` | V:the value to be associated with the specified key |

| Return ||
|----|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| V? | the previous value associated with`key`, or`null`if there was no mapping for`key`. (A`null`return can also indicate that the map previously associated`null`with`key`.) |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map |
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified key or value is null and this map does not permit null keys or values |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map |

**See Also**

- [java.lang.Object#equals(Object)](../java.lang/Object.md))
- [#get(Object)](IdentityHashMap.md))
- [#containsKey(Object)](IdentityHashMap.md)) 

### putAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putAll(from: Map<out K, V>): Unit
```

Copies all of the mappings from the specified map to this map. For each mapping in the specified map, if this map already ( a mapping for the key, its value is replaced with the value from the specified map; otherwise, a new mapping is inserted into this map.

| Parameters ||
|-----|-----------------------------------|
| `m` | mappings to be stored in this map |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`putAll`operation is not supported by this map |
| `java.lang.ClassCastException` | if the class of a key or value in the specified map prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified map is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of a key or value in the specified map prevents it from being stored in this map |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(key: K?): V?
```

Removes the mapping for this key from this map if present. The mapping is removed if and only if the mapping has a key`k`such that (key == k).

| Parameters ||
|-------|----------------------------------------------------|
| `key` | K?:key whose mapping is to be removed from the map |

| Return ||
|----|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| V? | the previous value associated with`key`, or`null`if there was no mapping for`key`. (A`null`return can also indicate that the map previously associated`null`with`key`.) |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this map |
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |
| --- | --- |

### remove

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(
    key: K, 
    value: V
): Boolean
```

Removes the entry for the specified key only if it is currently mapped to the specified value.

More formally, if this map contains a mapping from a key`k`to a value`v`such that`(key == k)`and`(value == v)`, then this method removes the mapping for this key and returns`true`; otherwise it returns`false`.

| Parameters ||
|---------|----------------------------------------------------------|
| `key` | K:key with which the specified value is associated |
| `value` | V:value expected to be associated with the specified key |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the value was removed |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this map (java.util.Collection#) |
| `java.lang.ClassCastException` | if the key or value is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key or value is null, and this map does not permit null keys or values (java.util.Collection#) |
| --- | --- |

### replace

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun replace(
    key: K, 
    oldValue: V, 
    newValue: V
): Boolean
```

Replaces the entry for the specified key only if currently mapped to the specified value.

More formally, if this map contains a mapping from a key`k`to a value`v`such that`(key == k)`and`(oldValue == v)`, then this method associates`k`with`newValue`and returns`true`; otherwise it returns`false`.

| Parameters ||
|------------|----------------------------------------------------------|
| `key` | K:key with which the specified value is associated |
| `oldValue` | V:value expected to be associated with the specified key |
| `newValue` | V:value to be associated with the specified key |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the value was replaced |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map (java.util.Collection#) |
| `java.lang.ClassCastException` | if the class of a specified key or value prevents it from being stored in this map |
| `java.lang.NullPointerException` | if oldValue is null and this map does not permit null values (java.util.Collection#) |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of a specified key or value prevents it from being stored in this map |

### replaceAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun replaceAll(function: BiFunction<in K, in V, out V>): Unit
```

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `function` | [BiFunction](../java.util.function/BiFunction.md)\<inK,inV,outV\>:the function to apply to each entry |

| Exceptions ||
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`set`operation is not supported by this map's entry set iterator. |
| `java.lang.ClassCastException` | if the class of a replacement value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified function is null, or if a replacement value is null and this map does not permit null values (java.util.Collection#) |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of a replacement value prevents it from being stored in this map (java.util.Collection#) |
| `java.util.ConcurrentModificationException` | if an entry is found to be removed during iteration |

## Properties

### entries

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val entries: MutableSet<MutableEntry<K, V>>
```

Returns a [Set](Set.md) view of the mappings contained in this map. Each element in the returned set is a reference-equality-based`Map.Entry`. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress, the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the`Iterator.remove`,`Set.remove`,`removeAll`,`retainAll`and`clear`methods. It does not support the`add`or`addAll`methods.

Like the backing map, the`Map.Entry`objects in the set returned by this method define key and value equality as reference-equality rather than object-equality. This affects the behavior of the`equals`and`hashCode`methods of these`Map.Entry`objects. A reference-equality based`Map.Entry e`is equal to an object`o`if and only if`o`is a`Map.Entry`and`e.getKey()==o.getKey() && e.getValue()==o.getValue()`. To accommodate these equals semantics, the`hashCode`method returns`System.identityHashCode(e.getKey()) ^ System.identityHashCode(e.getValue())`. (While the keys and values are compared using reference equality, the`Map.Entry`objects themselves are not.)

**Owing to the reference-equality-based semantics of the`Map.Entry`instances in the set returned by this method, it is possible that the symmetry and transitivity requirements of the [Object.equals(Object)](../java.lang/Object.md))contract may be violated if any of the entries in the set is compared to a normal map entry, or if the set returned by this method is compared to a set of normal map entries (such as would be returned by a call to this method on a normal map). However, the`Object.equals`contract is guaranteed to hold among identity-based map entries, and among sets of such entries.**

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>> | a set view of the identity-mappings contained in this map |

### keys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val keys: MutableSet<K>
```

Returns an identity-based set view of the keys contained in this map. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress, the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the`Iterator.remove`,`Set.remove`,`removeAll`,`retainAll`, and`clear`methods. It does not support the`add`or`addAll`methods.

**While the object returned by this method implements the`Set`interface, it does*not* obey`Set's`general contract. Like its backing map, the set returned by this method defines element equality as reference-equality rather than object-equality. This affects the behavior of its`contains`,`remove`,`containsAll`,`equals`, and`hashCode`methods.**

**The`equals`method of the returned set returns`true`only if the specified object is a set containing exactly the same object references as the returned set. The symmetry and transitivity requirements of the`Object.equals`contract may be violated if the set returned by this method is compared to a normal set. However, the`Object.equals`contract is guaranteed to hold among sets returned by this method.**

The`hashCode`method of the returned set returns the sum of the*identity hashcodes* of the elements in the set, rather than the sum of their hashcodes. This is mandated by the change in the semantics of the`equals`method, in order to enforce the general contract of the`Object.hashCode`method among sets returned by this method.

| Return ||
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<K> | an identity-based set view of the keys contained in this map |

**See Also**

- [java.lang.Object#equals(Object)](../java.lang/Object.md))
- [java.lang.System#identityHashCode(Object)](../java.lang/System.md)) 

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val size: Int
```

Returns the number of key-value mappings in this identity hash map.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of key-value mappings in this map |

### values

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val values: MutableCollection<V>
```

Returns a [Collection](Collection.md) view of the values contained in this map. The collection is backed by the map, so changes to the map are reflected in the collection, and vice-versa. If the map is modified while an iteration over the collection is in progress, the results of the iteration are undefined. The collection supports element removal, which removes the corresponding mapping from the map, via the`Iterator.remove`,`Collection.remove`,`removeAll`,`retainAll`and`clear`methods. It does not support the`add`or`addAll`methods.

**While the object returned by this method implements the`Collection`interface, it does*not* obey`Collection's`general contract. Like its backing map, the collection returned by this method defines element equality as reference-equality rather than object-equality. This affects the behavior of its`contains`,`remove`and`containsAll`methods.**

| Return ||
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<V> | a collection view of the values contained in this map |
