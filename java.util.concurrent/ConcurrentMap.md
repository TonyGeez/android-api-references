# ConcurrentMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConcurrentMap

```
interface ConcurrentMap<K : Any!, V : Any!> : MutableMap<K, V>
```

| [java.util.concurrent.ConcurrentMap](ConcurrentMap.md) |

| Known Direct Subclasses [ConcurrentHashMap](ConcurrentHashMap.md), [ConcurrentNavigableMap](ConcurrentNavigableMap.md) |----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ConcurrentHashMap](ConcurrentHashMap.md) | A hash table supporting full concurrency of retrievals and high expected concurrency for updates. | | [ConcurrentNavigableMap](ConcurrentNavigableMap.md) | A [ConcurrentMap](ConcurrentMap.md) supporting [NavigableMap](../java.util/NavigableMap.md) operations, and recursively so for its navigable sub-maps. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ConcurrentSkipListMap](ConcurrentSkipListMap.md) |--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------| | [ConcurrentSkipListMap](ConcurrentSkipListMap.md) | A scalable concurrent [ConcurrentNavigableMap](ConcurrentNavigableMap.md) implementation. | |
| --- | --- | --- | --- | --- | --- | --- |

A [Map](../java.util/Map.md) providing thread safety and atomicity guarantees.

To maintain the specified guarantees, default implementations of methods including [putIfAbsent](ConcurrentMap.md))inherited from [Map](../java.util/Map.md) must be overridden by implementations of this interface. Similarly, implementations of the collections returned by methods [keySet](../java.util/Map.md)), [values](../java.util/Map.md)), and [entrySet](../java.util/Map.md))must override methods such as`removeIf`when necessary to preserve atomicity guarantees.

Memory consistency effects: As with other concurrent collections, actions in a thread prior to placing an object into a`ConcurrentMap`as a key or value [*happen-before*](_package.md) actions subsequent to the access or removal of that object from the`ConcurrentMap`in another thread.

This interface is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openV? | [compute](ConcurrentMap.md))`(`key:` `K`, `remappingFunction:` ` [BiFunction](../java.util.function/BiFunction.md)<in` `K,` `in` `V?,` `out` `V?>`)` Attempts to compute a mapping for the specified key and its current mapped value (or`null`if there is no current mapping). |
| openV | [computeIfAbsent](ConcurrentMap.md))`(`key:` `K`, `mappingFunction:` ` [Function](../java.util.function/Function.md)<in` `K,` `out` `V>`)` If the specified key is not already associated with a value (or is mapped to`null`), attempts to compute its value using the given mapping function and enters it into this map unless`null`. |
| openV? | [computeIfPresent](ConcurrentMap.md))`(`key:` `K`, `remappingFunction:` ` [BiFunction](../java.util.function/BiFunction.md)<in` `K,` `in` `V,` `out` `V?>`)` If the value for the specified key is present and non-null, attempts to compute a new mapping given the key and its current mapped value. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](ConcurrentMap.md))`(`action:` ` [BiConsumer](../java.util.function/BiConsumer.md)<in` `K,` `in` `V>`)` Performs the given action for each entry in this map until all entries have been processed or the action throws an exception. |
| openV | [getOrDefault](ConcurrentMap.md))`(`key:` `K`, `defaultValue:` `V`)` Returns the value to which the specified key is mapped, or`defaultValue`if this map contains no mapping for the key. |
| openV? | [merge](ConcurrentMap.md))`(`key:` `K`, `value:` `V`, `remappingFunction:` ` [BiFunction](../java.util.function/BiFunction.md)<in` `V,` `in` `V,` `out` `V?>`)` If the specified key is not already associated with a value or is associated with null, associates it with the given non-null value. |
| --- | --- |
| abstractV? | [putIfAbsent](ConcurrentMap.md))`(`key:` `K`, `value:` `V`)` If the specified key is not already associated with a value, associates it with the given value. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](ConcurrentMap.md))`(`key:` `K`, `value:` `V`)` Removes the entry for a key only if currently mapped to a given value. |
| abstractV? | [replace](ConcurrentMap.md))`(`key:` `K`, `value:` `V`)` Replaces the entry for a key only if currently mapped to some value. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [replace](ConcurrentMap.md))`(`key:` `K`, `oldValue:` `V`, `newValue:` `V`)` Replaces the entry for a key only if currently mapped to a given value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [replaceAll](ConcurrentMap.md))`(`function:` ` [BiFunction](../java.util.function/BiFunction.md)<in` `K,` `in` `V,` `out` `V>`)` Replaces each entry's value with the result of invoking the given function on that entry until all entries have been processed or the function throws an exception. |

## Public methods

### compute

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compute(
    key: K, 
    remappingFunction: BiFunction<in K, in V?, out V?>
): V?
```

Attempts to compute a mapping for the specified key and its current mapped value (or`null`if there is no current mapping). For example, to either create or append a`String`msg to a value mapping: 

```kotlin
<code>map.compute(key, (k, v) -&gt; (v == null) ? msg : v.concat(msg))</code>
```
(Method [merge()](../java.util/Map.md))is often simpler to use for such purposes.)

<br />

If the remapping function returns`null`, the mapping is removed (or remains absent if initially absent). If the remapping function itself throws an (unchecked) exception, the exception is rethrown, and the current mapping is left unchanged.

The remapping function should not modify this map during computation.

| Parameters ||
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | K:key with which the specified value is to be associated |
| `remappingFunction` | [BiFunction](../java.util.function/BiFunction.md)\<inK,inV?,outV?\>:the remapping function to compute a value |

| Return ||
|----|------------------------------------------------------------------|
| V? | the new value associated with the specified key, or null if none |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified key is null and this map does not support null keys, or the remappingFunction is null |
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map (java.util.Collection#) |
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |

### computeIfAbsent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun computeIfAbsent(
    key: K, 
    mappingFunction: Function<in K, out V>
): V
```

If the specified key is not already associated with a value (or is mapped to`null`), attempts to compute its value using the given mapping function and enters it into this map unless`null`.

If the mapping function returns`null`, no mapping is recorded. If the mapping function itself throws an (unchecked) exception, the exception is rethrown, and no mapping is recorded. The most common usage is to construct a new object serving as an initial mapped value or memoized result, as in: 

```kotlin
<code>map.computeIfAbsent(key, k -&gt; new Value(f(k)));
  </code>
```

Or to implement a multi-value map,`Map<K,Collection<V>>`, supporting multiple values per key: 

```kotlin
<code>map.computeIfAbsent(key, k -&gt; new HashSet&lt;V&gt;()).add(v);
  </code>
```

The mapping function should not modify this map during computation.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | K:key with which the specified value is to be associated |
| `mappingFunction` | [Function](../java.util.function/Function.md)\<inK,outV\>:the mapping function to compute a value |

| Return ||
|---|-------------------------------------------------------------------------------------------------------------------|
| V | the current (existing or computed) value associated with the specified key, or null if the computed value is null |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified key is null and this map does not support null keys, or the mappingFunction is null |
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map (java.util.Collection#) |
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |

### computeIfPresent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun computeIfPresent(
    key: K, 
    remappingFunction: BiFunction<in K, in V, out V?>
): V?
```

If the value for the specified key is present and non-null, attempts to compute a new mapping given the key and its current mapped value.

If the remapping function returns`null`, the mapping is removed. If the remapping function itself throws an (unchecked) exception, the exception is rethrown, and the current mapping is left unchanged.

The remapping function should not modify this map during computation.

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | K:key with which the specified value is to be associated |
| `remappingFunction` | [BiFunction](../java.util.function/BiFunction.md)\<inK,inV,outV?\>:the remapping function to compute a value |

| Return ||
|----|------------------------------------------------------------------|
| V? | the new value associated with the specified key, or null if none |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified key is null and this map does not support null keys, or the remappingFunction is null |
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map (java.util.Collection#) |
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEach(action: BiConsumer<in K, in V>): Unit
```

Performs the given action for each entry in this map until all entries have been processed or the action throws an exception. Unless otherwise specified by the implementing class, actions are performed in the order of entry set iteration (if an iteration order is specified.) Exceptions thrown by the action are relayed to the caller.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [BiConsumer](../java.util.function/BiConsumer.md)\<inK,inV\>:The action to be performed for each entry |

| Exceptions ||
|---------------------------------------------|-----------------------------------------------------|
| `java.lang.NullPointerException` | if the specified action is null |
| `java.util.ConcurrentModificationException` | if an entry is found to be removed during iteration |

### getOrDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOrDefault(
    key: K, 
    defaultValue: V
): V
```

Returns the value to which the specified key is mapped, or`defaultValue`if this map contains no mapping for the key.

| Parameters ||
|----------------|----------------------------------------------------|
| `key` | K:the key whose associated value is to be returned |
| `defaultValue` | V:the default mapping of the key |

| Return ||
|---|-------------------------------------------------------------------------------------------------------------|
| V | the value to which the specified key is mapped, or`defaultValue`if this map contains no mapping for the key |

| Exceptions ||
|----------------------------------|---------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the key is of an inappropriate type for this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified key is null and this map does not permit null keys (java.util.Collection#) |

### merge

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun merge(
    key: K, 
    value: V, 
    remappingFunction: BiFunction<in V, in V, out V?>
): V?
```

If the specified key is not already associated with a value or is associated with null, associates it with the given non-null value. Otherwise, replaces the associated value with the results of the given remapping function, or removes if the result is`null`. This method may be of use when combining multiple mapped values for a key. For example, to either create or append a`String msg`to a value mapping: 

```kotlin
<code>map.merge(key, msg, String::concat)
  </code>
```

<br />

If the remapping function returns`null`, the mapping is removed. If the remapping function itself throws an (unchecked) exception, the exception is rethrown, and the current mapping is left unchanged.

The remapping function should not modify this map during computation.

| Parameters ||
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | K:key with which the resulting value is to be associated |
| `value` | V:the non-null value to be merged with the existing value associated with the key or, if no existing value or a null value is associated with the key, to be associated with the key |
| `remappingFunction` | [BiFunction](../java.util.function/BiFunction.md)\<inV,inV,outV?\>:the remapping function to recompute a value if present |
| --- | --- |

| Return ||
|----|-------------------------------------------------------------------------------------------------|
| V? | the new value associated with the specified key, or null if no value is associated with the key |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map (java.util.Collection#) |
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map (java.util.Collection#) |
| --- | --- |
| `java.lang.NullPointerException` | if the specified key is null and this map does not support null keys or the value or remappingFunction is null |

### putIfAbsent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun putIfAbsent(
    key: K, 
    value: V
): V?
```

If the specified key is not already associated with a value, associates it with the given value. This is equivalent to, for this`map`: 

```kotlin
<code>if (!map.containsKey(key))
    return map.put(key, value);
  else
    return map.get(key);</code>
```
except that the action is performed atomically.

<br />

| Parameters ||
|---------|----------------------------------------------------------|
| `key` | K:key with which the specified value is to be associated |
| `value` | V:value to be associated with the specified key |

| Return ||
|----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| V? | the previous value associated with the specified key, or`null`if there was no mapping for the key. (A`null`return can also indicate that the map previously associated`null`with the key, if the implementation supports null values.) |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map |
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified key or value is null, and this map does not permit null keys or values |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun remove(
    key: K, 
    value: V
): Boolean
```

Removes the entry for a key only if currently mapped to a given value. This is equivalent to, for this`map`: 

```kotlin
<code>if (map.containsKey(key)
      &amp;&amp; Objects.equals(map.get(key), value)) {
    map.remove(key);
    return true;
  } else {
    return false;
  }</code>
```
except that the action is performed atomically.

<br />

| Parameters ||
|---------|----------------------------------------------------------|
| `key` | K:key with which the specified value is associated |
| `value` | V:value expected to be associated with the specified key |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the value was removed |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this map |
| `java.lang.ClassCastException` | if the key or value is of an inappropriate type for this map ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified key or value is null, and this map does not permit null keys or values ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
| --- | --- |

### replace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun replace(
    key: K, 
    value: V
): V?
```

Replaces the entry for a key only if currently mapped to some value. This is equivalent to, for this`map`: 

```kotlin
<code>if (map.containsKey(key))
    return map.put(key, value);
  else
    return null;</code>
```
except that the action is performed atomically.

<br />

| Parameters ||
|---------|----------------------------------------------------|
| `key` | K:key with which the specified value is associated |
| `value` | V:value to be associated with the specified key |

| Return ||
|----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| V? | the previous value associated with the specified key, or`null`if there was no mapping for the key. (A`null`return can also indicate that the map previously associated`null`with the key, if the implementation supports null values.) |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map |
| `java.lang.ClassCastException` | if the class of the specified key or value prevents it from being stored in this map |
| `java.lang.NullPointerException` | if the specified key or value is null, and this map does not permit null keys or values |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified key or value prevents it from being stored in this map |

### replace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun replace(
    key: K, 
    oldValue: V, 
    newValue: V
): Boolean
```

Replaces the entry for a key only if currently mapped to a given value. This is equivalent to, for this`map`: 

```kotlin
<code>if (map.containsKey(key)
      &amp;&amp; Objects.equals(map.get(key), oldValue)) {
    map.put(key, newValue);
    return true;
  } else {
    return false;
  }</code>
```
except that the action is performed atomically.

<br />

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
| `java.lang.UnsupportedOperationException` | if the`put`operation is not supported by this map |
| `java.lang.ClassCastException` | if the class of a specified key or value prevents it from being stored in this map |
| `java.lang.NullPointerException` | if a specified key or value is null, and this map does not permit null keys or values |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of a specified key or value prevents it from being stored in this map |

### replaceAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun replaceAll(function: BiFunction<in K, in V, out V>): Unit
```

Replaces each entry's value with the result of invoking the given function on that entry until all entries have been processed or the function throws an exception. Exceptions thrown by the function are relayed to the caller.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `function` | [BiFunction](../java.util.function/BiFunction.md)\<inK,inV,outV\>:the function to apply to each entry |

| Exceptions ||
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`set`operation is not supported by this map's entry set iterator. |
| `java.lang.ClassCastException` | if the class of a replacement value prevents it from being stored in this map (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified function is null, or if a replacement value is null and this map does not permit null values (java.util.Collection#) |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of a replacement value prevents it from being stored in this map (java.util.Collection#) |
| `java.util.ConcurrentModificationException` | if an entry is found to be removed during iteration |
