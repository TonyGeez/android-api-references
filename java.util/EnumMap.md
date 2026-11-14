# EnumMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EnumMap

```
open class EnumMap<K : Enum<K>!, V : Any!> : AbstractMap<K, V>, Cloneable, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.AbstractMap](AbstractMap.md)\<K, V\> ||
| | ↳ | [java.util.EnumMap](EnumMap.md) |

A specialized [Map](Map.md) implementation for use with enum type keys. All of the keys in an enum map must come from a single enum type that is specified, explicitly or implicitly, when the map is created. Enum maps are represented internally as arrays. This representation is extremely compact and efficient.

Enum maps are maintained in the*natural order*of their keys (the order in which the enum constants are declared). This is reflected in the iterators returned by the collections views (#keySet(), #entrySet(), and #values()).

Iterators returned by the collection views are*weakly consistent* : they will never throw [ConcurrentModificationException](ConcurrentModificationException.md) and they may or may not show the effects of any modifications to the map that occur while the iteration is in progress.

Null keys are not permitted. Attempts to insert a null key will throw [NullPointerException](../java.lang/NullPointerException.md). Attempts to test for the presence of a null key or to remove one will, however, function properly. Null values are permitted.

Like most collection implementations`EnumMap`is not synchronized. If multiple threads access an enum map concurrently, and at least one of the threads modifies the map, it should be synchronized externally. This is typically accomplished by synchronizing on some object that naturally encapsulates the enum map. If no such object exists, the map should be "wrapped" using the [Collections.synchronizedMap](Collections.md))method. This is best done at creation time, to prevent accidental unsynchronized access: 

```kotlin
Map<EnumKey, V> m
          = Collections.synchronizedMap(new EnumMap<EnumKey, V>(...));
  
```

Implementation note: All basic operations execute in constant time. They are likely (though not guaranteed) to be faster than their [HashMap](HashMap.md) counterparts.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EnumMap](EnumMap.md))`(`keyType:` ` [Class](../java.lang/Class.md)<K>!`)` Creates an empty enum map with the specified key type. |
| [EnumMap](EnumMap.md))`(`m:` ` [EnumMap](EnumMap.md)<K,` `out` `V>!`)` Creates an enum map with the same key type as the specified enum map, initially containing the same mappings (if any). |
| [EnumMap](EnumMap.md))`(`m:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)<K,` `out` `V>!`)` Creates an enum map initialized from the specified map. |

| Public methods ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](EnumMap.md))`()` Removes all mappings from this map. |
| open [EnumMap](EnumMap.md)\<K,V\> | [clone](EnumMap.md))`()` Returns a shallow copy of this enum map. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsKey](EnumMap.md))`(`key:` `K?`)` Returns`true`if this map contains a mapping for the specified key. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsValue](EnumMap.md))`(`value:` `V?`)` Returns`true`if this map maps one or more keys to the specified value. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](EnumMap.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares the specified object with this map for equality. |
| openV? | [get](EnumMap.md))`(`key:` `K?`)` Returns the value to which the specified key is mapped, or`null`if this map contains no mapping for the key. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](EnumMap.md))`()` Returns the hash code value for this map. |
| openV? | [put](EnumMap.md))`(`key:` `K`, `value:` `V`)` Associates the specified value with the specified key in this map. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putAll](EnumMap.md))`(`from:` ` [Map](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-map/index.html)<out` `K,` `V>`)` Copies all of the mappings from the specified map to this map. |
| --- | --- |
| openV? | [remove](EnumMap.md))`(`key:` `K?`)` Removes the mapping for this key from this map if present. |

| Inherited functions ||
|---|---|
| From class [AbstractMap](AbstractMap.md) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](AbstractMap.md))`()` <br /> Returns`true`if this map contains no key-value mappings. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](AbstractMap.md))`()` <br /> Returns a string representation of this map. The string representation consists of a list of key-value mappings in the order returned by the map's`entrySet`view's iterator, enclosed in braces (`"{}"`). Adjacent mappings are separated by the characters`", "`(comma and space). Each key-value mapping is rendered as the key followed by an equals sign (`"="`) followed by the associated value. Keys and values are converted to strings as by [String.valueOf(Object)](../java.lang/String.md)). <br /> | ||

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)\<K,V\>\> | [entries](EnumMap.md) Returns a [Set](Set.md) view of the mappings contained in this map. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<K\> | [keys](EnumMap.md) Returns a [Set](Set.md) view of the keys contained in this map. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](EnumMap.md) Returns the number of key-value mappings in this map. |
| --- | --- |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<V\> | [values](EnumMap.md) Returns a [Collection](Collection.md) view of the values contained in this map. |

## Public constructors

### EnumMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EnumMap(keyType: Class<K>!)
```

Creates an empty enum map with the specified key type.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `keyType` | [Class](../java.lang/Class.md)\<K\>!:the class object of the key type for this enum map |

| Exceptions ||
|----------------------------------|--------------------|
| `java.lang.NullPointerException` | if`keyType`is null |

### EnumMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EnumMap(m: EnumMap<K, out V>!)
```

Creates an enum map with the same key type as the specified enum map, initially containing the same mappings (if any).

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------|
| `m` | [EnumMap](EnumMap.md)\<K,outV\>!:the enum map from which to initialize this enum map |

| Exceptions ||
|----------------------------------|--------------|
| `java.lang.NullPointerException` | if`m`is null |

### EnumMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EnumMap(m: MutableMap<K, out V>!)
```

Creates an enum map initialized from the specified map. If the specified map is an`EnumMap`instance, this constructor behaves identically to [EnumMap(java.util.EnumMap)](EnumMap.md)). Otherwise, the specified map must contain at least one mapping (in order to determine the new enum map's key type).

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `m` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K,outV\>!:the map from which to initialize this enum map |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`m`is not an`EnumMap`instance and contains no mappings |
| `java.lang.NullPointerException` | if`m`is null |

## Public methods

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Removes all mappings from this map.

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`clear`operation is not supported by this map |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): EnumMap<K, V>
```

Returns a shallow copy of this enum map. The values themselves are not cloned.

| Return ||
|--------------------------------------------------------------------------------------|---------------------------------|
| [EnumMap](EnumMap.md)<K,` `V> | a shallow copy of this enum map |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### containsKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun containsKey(key: K?): Boolean
```

Returns`true`if this map contains a mapping for the specified key.

| Parameters ||
|-------|-------------------------------------------------------|
| `key` | K?:the key whose presence in this map is to be tested |

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

Returns`true`if this map maps one or more keys to the specified value.

| Parameters ||
|---------|---------------------------------------------------------|
| `value` | V?:the value whose presence in this map is to be tested |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this map maps one or more keys to this value |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the value is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified value is null and this map does not permit null values (java.util.Collection#) |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares the specified object with this map for equality. Returns`true`if the given object is also a map and the two maps represent the same mappings, as specified in the [java.util.Map#equals(java.lang.Object)](EnumMap.md) contract.

| Parameters ||
|-------|------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | the object to be compared for equality with this map |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the specified object is equal to this map |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(key: K?): V?
```

Returns the value to which the specified key is mapped, or`null`if this map contains no mapping for the key.

More formally, if this map contains a mapping from a key`k`to a value`v`such that`(key == k)`, then this method returns`v`; otherwise it returns`null`. (There can be at most one such mapping.)

A return value of`null`does not*necessarily* indicate that the map contains no mapping for the key; it's also possible that the map explicitly maps the key to`null`. The #containsKey operation may be used to distinguish these two cases.

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

Returns the hash code value for this map. The hash code of a map is defined to be the sum of the hash codes of each entry in the map.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    key: K, 
    value: V
): V?
```

Associates the specified value with the specified key in this map. If the map previously contained a mapping for this key, the old value is replaced.

| Parameters ||
|---------|--------------------------------------------------------------|
| `key` | K:the key with which the specified value is to be associated |
| `value` | V:the value to be associated with the specified key |

| Return ||
|----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| V? | the previous value associated with specified key, or`null`if there was no mapping for key. (A`null`return can also indicate that the map previously associated`null`with the specified key.) |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map |
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified key is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map |

### putAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putAll(from: Map<out K, V>): Unit
```

Copies all of the mappings from the specified map to this map. These mappings will replace any mappings that this map had for any of the keys currently in the specified map.

| Parameters ||
|-----|---------------------------------------|
| `m` | the mappings to be stored in this map |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`putAll`operation is not supported by this map |
| `java.lang.ClassCastException` | if the class of a key or value in the specified map prevents it from being stored in this map |
| `java.lang.NullPointerException` | the specified map is null, or if one or more keys in the specified map are null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of a key or value in the specified map prevents it from being stored in this map |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(key: K?): V?
```

Removes the mapping for this key from this map if present.

| Parameters ||
|-------|--------------------------------------------------------|
| `key` | K?:the key whose mapping is to be removed from the map |

| Return ||
|----|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| V? | the previous value associated with specified key, or`null`if there was no entry for key. (A`null`return can also indicate that the map previously associated`null`with the specified key.) |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this map |
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |
| --- | --- |

## Properties

### entries

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val entries: MutableSet<MutableEntry<K, V>>
```

Returns a [Set](Set.md) view of the mappings contained in this map. The returned set obeys the general contract outlined in [Map.keySet()](Map.md)). The set's iterator will return the mappings in the order their keys appear in map, which is their natural order (the order in which the enum constants are declared).

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [MutableEntry](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/-mutable-entry/index.html)<K,` `V>> | a set view of the mappings contained in this enum map |

### keys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val keys: MutableSet<K>
```

Returns a [Set](Set.md) view of the keys contained in this map. The returned set obeys the general contract outlined in [Map.keySet()](Map.md)). The set's iterator will return the keys in their natural order (the order in which the enum constants are declared).

| Return ||
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<K> | a set view of the keys contained in this enum map |

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val size: Int
```

Returns the number of key-value mappings in this map.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of key-value mappings in this map |

### values

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val values: MutableCollection<V>
```

Returns a [Collection](Collection.md) view of the values contained in this map. The returned collection obeys the general contract outlined in [Map.values()](Map.md)). The collection's iterator will return the values in the order their corresponding keys appear in map, which is their natural order (the order in which the enum constants are declared).

| Return ||
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<V> | a collection view of the values contained in this map |
