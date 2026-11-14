# AbstractMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractMap

```
abstract class AbstractMap<K : Any!, V : Any!> : MutableMap<K, V>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.AbstractMap](AbstractMap.md) |

| Known Direct Subclasses [ConcurrentHashMap](../java.util.concurrent/ConcurrentHashMap.md), [ConcurrentSkipListMap](../java.util.concurrent/ConcurrentSkipListMap.md), [EnumMap](EnumMap.md), [HashMap](HashMap.md), [IdentityHashMap](IdentityHashMap.md), [TreeMap](TreeMap.md), [WeakHashMap](WeakHashMap.md) |--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------| | [ConcurrentHashMap](../java.util.concurrent/ConcurrentHashMap.md) | A hash table supporting full concurrency of retrievals and high expected concurrency for updates. | | [ConcurrentSkipListMap](../java.util.concurrent/ConcurrentSkipListMap.md) | A scalable concurrent [ConcurrentNavigableMap](../java.util.concurrent/ConcurrentNavigableMap.md) implementation. | | [EnumMap](EnumMap.md) | A specialized [Map](Map.md) implementation for use with enum type keys. | | [HashMap](HashMap.md) | Hash table based implementation of the`Map`interface. | | [IdentityHashMap](IdentityHashMap.md) | This class implements the`Map`interface with a hash table, using reference-equality in place of object-equality when comparing keys (and values). | | [TreeMap](TreeMap.md) | A Red-Black tree based [NavigableMap](NavigableMap.md) implementation. | | [WeakHashMap](WeakHashMap.md) | Hash table based implementation of the`Map`interface, with*weak keys*. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [LinkedHashMap](LinkedHashMap.md) |-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------| | [LinkedHashMap](LinkedHashMap.md) | Hash table and linked list implementation of the`Map`interface, with well-defined encounter order. | |
| --- | --- | --- | --- | --- | --- | --- |

This class provides a skeletal implementation of the`Map`interface, to minimize the effort required to implement this interface.

To implement an unmodifiable map, the programmer needs only to extend this class and provide an implementation for the`entrySet`method, which returns a set-view of the map's mappings. Typically, the returned set will, in turn, be implemented atop`AbstractSet`. This set should not support the`add`or`remove`methods, and its iterator should not support the`remove`method.

To implement a modifiable map, the programmer must additionally override this class's`put`method (which otherwise throws an`UnsupportedOperationException`), and the iterator returned by`entrySet().iterator()`must additionally implement its`remove`method.

The programmer should generally provide a void (no argument) and map constructor, as per the recommendation in the`Map`interface specification.

The documentation for each non-abstract method in this class describes its implementation in detail. Each of these methods may be overridden if the map being implemented admits a more efficient implementation.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [SimpleEntry](../java/util/AbstractMap.SimpleEntry.md) An Entry maintaining a key and a value. |
| open | [SimpleImmutableEntry](../java/util/AbstractMap.SimpleImmutableEntry.md) An unmodifiable Entry maintaining a key and a value. |

| Protected constructors ||
|-------------------------------------------------------------------------------------------------------------------------|---|
| [AbstractMap](AbstractMap.md))`()` Sole constructor. |

| Public methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](AbstractMap.md))`()` Removes all of the mappings from this map (optional operation). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsKey](AbstractMap.md))`(`key:` `K?`)` Returns`true`if this map contains a mapping for the specified key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsValue](AbstractMap.md))`(`value:` `V?`)` Returns`true`if this map maps one or more keys to the specified value. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](AbstractMap.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares the specified object with this map for equality. |
| openV? | [get](AbstractMap.md))`(`key:` `K?`)` Returns the value to which the specified key is mapped, or`null`if this map contains no mapping for the key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](AbstractMap.md))`()` Returns the hash code value for this map. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](AbstractMap.md))`()` Returns`true`if this map contains no key-value mappings. |
| openV? | [put](AbstractMap.md))`(`key:` `K`, `value:` `V`)` Associates the specified value with the specified key in this map (optional operation). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putAll](AbstractMap.md))`(`from:` ` [Map](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-map/index.html)<out` `K,` `V>`)` Copies all of the mappings from the specified map to this map (optional operation). |
| --- | --- |
| openV? | [remove](AbstractMap.md))`(`key:` `K?`)` Removes the mapping for a key from this map if it is present (optional operation). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](AbstractMap.md))`()` Returns a string representation of this map. |

| Protected methods ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](AbstractMap.md))`()` Returns a shallow copy of this`AbstractMap`instance: the keys and values themselves are not cloned. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>\> | [entries](AbstractMap.md) <br /> |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<K\> | [keys](AbstractMap.md) Returns a [Set](Set.md) view of the keys contained in this map. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](AbstractMap.md) Returns the number of key-value mappings in this map. |
| --- | --- |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<V\> | [values](AbstractMap.md) Returns a [Collection](Collection.md) view of the values contained in this map. |

## Protected constructors

### AbstractMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected AbstractMap()
```

Sole constructor. (For invocation by subclass constructors, typically implicit.)

## Public methods

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Removes all of the mappings from this map (optional operation). The map will be empty after this call returns.

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`clear`operation is not supported by this map |

### containsKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun containsKey(key: K?): Boolean
```

Returns`true`if this map contains a mapping for the specified key. More formally, returns`true`if and only if this map contains a mapping for a key`k`such that`Objects.equals(key, k)`. (There can be at most one such mapping.)

| Parameters ||
|-------|---------------------------------------------------|
| `key` | K?:key whose presence in this map is to be tested |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this map contains a mapping for the specified key |

| Exceptions ||
|----------------------------------|---------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |

### containsValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun containsValue(value: V?): Boolean
```

Returns`true`if this map maps one or more keys to the specified value. More formally, returns`true`if and only if this map contains at least one mapping to a value`v`such that`Objects.equals(value, v)`. This operation will probably require time linear in the map size for most implementations of the`Map`interface.

| Parameters ||
|---------|-----------------------------------------------------|
| `value` | V?:value whose presence in this map is to be tested |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this map maps one or more keys to the specified value |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the value is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified value is null and this map does not permit null values (java.util.Collection#) |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares the specified object with this map for equality. Returns`true`if the given object is also a map and the two maps represent the same mappings. More formally, two maps`m1`and`m2`represent the same mappings if`m1.entrySet().equals(m2.entrySet())`. This ensures that the`equals`method works properly across different implementations of the`Map`interface.

| Parameters ||
|-------|--------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | object to be compared for equality with this map |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the specified object is equal to this map |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(key: K?): V?
```

Returns the value to which the specified key is mapped, or`null`if this map contains no mapping for the key.

More formally, if this map contains a mapping from a key`k`to a value`v`such that`Objects.equals(key, k)`, then this method returns`v`; otherwise it returns`null`. (There can be at most one such mapping.)

If this map permits null values, then a return value of`null`does not*necessarily* indicate that the map contains no mapping for the key; it's also possible that the map explicitly maps the key to`null`. The [containsKey](Map.md))operation may be used to distinguish these two cases.

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

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns the hash code value for this map. The hash code of a map is defined to be the sum of the hash codes of each entry in the map's`entrySet()`view. This ensures that`m1.equals(m2)`implies that`m1.hashCode()==m2.hashCode()`for any two maps`m1`and`m2`, as required by the general contract of [Object.hashCode](../java.lang/Object.md)).

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hash code value for this map |

**See Also**

- [java.util.Map.Entry#hashCode()](AbstractMap.md)
- [java.lang.Object#equals(Object)](../java.lang/Object.md)) 

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEmpty(): Boolean
```

Returns`true`if this map contains no key-value mappings.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this map contains no key-value mappings |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    key: K, 
    value: V
): V?
```

Associates the specified value with the specified key in this map (optional operation). If the map previously contained a mapping for the key, the old value is replaced by the specified value. (A map`m`is said to contain a mapping for a key`k`if and only if [m.containsKey(k)](Map.md))would return`true`.)

| Parameters ||
|---------|----------------------------------------------------------|
| `key` | K:key with which the specified value is to be associated |
| `value` | V:value to be associated with the specified key |

| Return ||
|----|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| V? | the previous value associated with`key`, or`null`if there was no mapping for`key`. (A`null`return can also indicate that the map previously associated`null`with`key`, if the implementation supports`null`values.) |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map |
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified key or value is null and this map does not permit null keys or values |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map |

### putAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putAll(from: Map<out K, V>): Unit
```

Copies all of the mappings from the specified map to this map (optional operation). The effect of this call is equivalent to that of calling [put(k, v)](Map.md))on this map once for each mapping from key`k`to value`v`in the specified map. The behavior of this operation is undefined if the specified map is modified while the operation is in progress. If the specified map has a defined [encounter order](SequencedCollection.md), processing of its mappings generally occurs in that order.

| Parameters ||
|-----|-----------------------------------|
| `m` | mappings to be stored in this map |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`putAll`operation is not supported by this map |
| `java.lang.ClassCastException` | if the class of a key or value in the specified map prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified map is null, or if this map does not permit null keys or values, and the specified map contains null keys or values |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of a key or value in the specified map prevents it from being stored in this map |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(key: K?): V?
```

Removes the mapping for a key from this map if it is present (optional operation). More formally, if this map contains a mapping from key`k`to value`v`such that`Objects.equals(key, k)`, that mapping is removed. (The map can contain at most one such mapping.)

Returns the value to which this map previously associated the key, or`null`if the map contained no mapping for the key.

If this map permits null values, then a return value of`null`does not*necessarily* indicate that the map contained no mapping for the key; it's also possible that the map explicitly mapped the key to`null`.

The map will not contain a mapping for the specified key once the call returns.

| Parameters ||
|-------|----------------------------------------------------|
| `key` | K?:key whose mapping is to be removed from the map |

| Return ||
|----|------------------------------------------------------------------------------------|
| V? | the previous value associated with`key`, or`null`if there was no mapping for`key`. |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this map |
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |
| --- | --- |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of this map. The string representation consists of a list of key-value mappings in the order returned by the map's`entrySet`view's iterator, enclosed in braces (`"{}"`). Adjacent mappings are separated by the characters`", "`(comma and space). Each key-value mapping is rendered as the key followed by an equals sign (`"="`) followed by the associated value. Keys and values are converted to strings as by [String.valueOf(Object)](../java.lang/String.md)).

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this map |

## Protected methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun clone(): Any
```

Returns a shallow copy of this`AbstractMap`instance: the keys and values themselves are not cloned.

| Return ||
|----------------------------------------------------------------------------|----------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a shallow copy of this map |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

## Properties

### entries

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract val entries: MutableSet<MutableEntry<K, V>>
```

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>> | a set view of the mappings contained in this map |

### keys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val keys: MutableSet<K>
```

Returns a [Set](Set.md) view of the keys contained in this map. The set is backed by the map, so changes to the map are reflected in the set, and vice-versa. If the map is modified while an iteration over the set is in progress (except through the iterator's own`remove`operation), the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the map, via the`Iterator.remove`,`Set.remove`,`removeAll`,`retainAll`, and`clear`operations. It does not support the`add`or`addAll`operations.

| Return ||
|----------------------------------------------------------------------------------------------------------|----------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<K> | a set view of the keys contained in this map |

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

Returns a [Collection](Collection.md) view of the values contained in this map. The collection is backed by the map, so changes to the map are reflected in the collection, and vice-versa. If the map is modified while an iteration over the collection is in progress (except through the iterator's own`remove`operation), the results of the iteration are undefined. The collection supports element removal, which removes the corresponding mapping from the map, via the`Iterator.remove`,`Collection.remove`,`removeAll`,`retainAll`and`clear`operations. It does not support the`add`or`addAll`operations.

| Return ||
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<V> | a collection view of the values contained in this map |
