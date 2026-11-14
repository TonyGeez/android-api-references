Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LruCache

Kotlin | [Java](LruCache.md)
| --- | --- |

```
open class LruCache<K : Any!, V : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.LruCache](LruCache.md) |

A cache that holds strong references to a limited number of values. Each time a value is accessed, it is moved to the head of a queue. When a value is added to a full cache, the value at the end of that queue is evicted and may become eligible for garbage collection.

If your cached values hold resources that need to be explicitly released, override `https://developer.android.com/reference/kotlin/android/util/LruCache#entryRemoved(kotlin.Boolean,%20android.util.LruCache.K,%20android.util.LruCache.V,%20android.util.LruCache.V)`.

If a cache miss should be computed on demand for the corresponding keys, override `https://developer.android.com/reference/kotlin/android/util/LruCache#create(android.util.LruCache.K)`. This simplifies the calling code, allowing it to assume a value will always be returned, even when there's a cache miss.

By default, the cache size is measured in the number of entries. Override `https://developer.android.com/reference/kotlin/android/util/LruCache#sizeOf(android.util.LruCache.K,%20android.util.LruCache.V)` to size the cache in different units. For example, this cache is limited to 4MiB of bitmaps:

```kotlin
<code>int cacheSize = 4 * 1024 * 1024; // 4MiB
    LruCache&lt;String, Bitmap&gt; bitmapCache = new LruCache&lt;String, Bitmap&gt;(cacheSize) {
        protected int sizeOf(String key, Bitmap value) {
            return value.getByteCount();
        }
    }</code>
```

This class is thread-safe. Perform multiple cache operations atomically by synchronizing on the cache:

```kotlin
<code>synchronized (cache) {
      if (cache.get(key) == null) {
          cache.put(key, value);
      }
    }</code>
```

This class does not allow null to be used as a key or value. A return value of null from `https://developer.android.com/reference/kotlin/android/util/LruCache#get(android.util.LruCache.K)`, `https://developer.android.com/reference/kotlin/android/util/LruCache#put(android.util.LruCache.K,%20android.util.LruCache.V)` or `https://developer.android.com/reference/kotlin/android/util/LruCache#remove(android.util.LruCache.K)` is unambiguous: the key was not in the cache.

This class appeared in Android 3.1 (Honeycomb MR1); it's available as part of [Android's Support Package](http://developer.android.com/sdk/compatibility-library.html) for earlier releases.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/LruCache#LruCache(kotlin.Int)(maxSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/LruCache#createCount()()` Returns the number of times `https://developer.android.com/reference/kotlin/android/util/LruCache#create(android.util.LruCache.K)` returned a value. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/LruCache#evictAll()()` Clear the cache, calling `https://developer.android.com/reference/kotlin/android/util/LruCache#entryRemoved(kotlin.Boolean,%20android.util.LruCache.K,%20android.util.LruCache.V,%20android.util.LruCache.V)` on each removed entry. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/LruCache#evictionCount()()` Returns the number of values that have been evicted. |
| --- | --- |
| V | `https://developer.android.com/reference/kotlin/android/util/LruCache#get(android.util.LruCache.K)(key: K)` Returns the value for `key` if it exists in the cache or can be created by `create`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/LruCache#hitCount()()` Returns the number of times `https://developer.android.com/reference/kotlin/android/util/LruCache#get(android.util.LruCache.K)` returned a value that was already present in the cache. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/LruCache#maxSize()()` For caches that do not override `https://developer.android.com/reference/kotlin/android/util/LruCache#sizeOf(android.util.LruCache.K,%20android.util.LruCache.V)`, this returns the maximum number of entries in the cache. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/LruCache#missCount()()` Returns the number of times `https://developer.android.com/reference/kotlin/android/util/LruCache#get(android.util.LruCache.K)` returned null or required a new value to be created. |
| V | `https://developer.android.com/reference/kotlin/android/util/LruCache#put(android.util.LruCache.K,%20android.util.LruCache.V)(key: K, value: V)` Caches `value` for `key`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/LruCache#putCount()()` Returns the number of times `https://developer.android.com/reference/kotlin/android/util/LruCache#put(android.util.LruCache.K,%20android.util.LruCache.V)` was called. |
| --- | --- |
| V | `https://developer.android.com/reference/kotlin/android/util/LruCache#remove(android.util.LruCache.K)(key: K)` Removes the entry for `key` if it exists. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/LruCache#resize(kotlin.Int)(maxSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the size of the cache. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/LruCache#size()()` For caches that do not override `https://developer.android.com/reference/kotlin/android/util/LruCache#sizeOf(android.util.LruCache.K,%20android.util.LruCache.V)`, this returns the number of entries in the cache. |
| --- | --- |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K, V\>! | `https://developer.android.com/reference/kotlin/android/util/LruCache#snapshot()()` Returns a copy of the current contents of the cache, ordered from least recently accessed to most recently accessed. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/util/LruCache#toString()()` Returns a string representation of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/LruCache#trimToSize(kotlin.Int)(maxSize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Remove the eldest entries until the total of remaining entries is at or below the requested size. |
| --- | --- |

| Protected methods ||
|---|---|
| open V | `https://developer.android.com/reference/kotlin/android/util/LruCache#create(android.util.LruCache.K)(key: K)` Called after a cache miss to compute a value for the corresponding key. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/LruCache#entryRemoved(kotlin.Boolean,%20android.util.LruCache.K,%20android.util.LruCache.V,%20android.util.LruCache.V)(evicted: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, key: K, oldValue: V, newValue: V)` Called for entries that have been evicted or removed. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/util/LruCache#sizeOf(android.util.LruCache.K,%20android.util.LruCache.V)(key: K, value: V)` Returns the size of the entry for `key` and `value` in user-defined units. |
| --- | --- |

## Public constructors

### LruCache

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
LruCache(maxSize: Int)
```

| Parameters ||
|---|---|
| `maxSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): for caches that do not override `https://developer.android.com/reference/kotlin/android/util/LruCache#sizeOf(android.util.LruCache.K,%20android.util.LruCache.V)`, this is the maximum number of entries in the cache. For all other caches, this is the maximum sum of the sizes of the entries in this cache. |

## Public methods

### createCount

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createCount(): Int
```

Returns the number of times `https://developer.android.com/reference/kotlin/android/util/LruCache#create(android.util.LruCache.K)` returned a value.

### evictAll

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun evictAll(): Unit
```

Clear the cache, calling `https://developer.android.com/reference/kotlin/android/util/LruCache#entryRemoved(kotlin.Boolean,%20android.util.LruCache.K,%20android.util.LruCache.V,%20android.util.LruCache.V)` on each removed entry.

### evictionCount

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun evictionCount(): Int
```

Returns the number of values that have been evicted.

### get

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun get(key: K): V
```

Returns the value for `key` if it exists in the cache or can be created by `create`. If a value was returned, it is moved to the head of the queue. This returns null if a value is not cached and cannot be created.

### hitCount

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hitCount(): Int
```

Returns the number of times `https://developer.android.com/reference/kotlin/android/util/LruCache#get(android.util.LruCache.K)` returned a value that was already present in the cache.

### maxSize

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun maxSize(): Int
```

For caches that do not override `https://developer.android.com/reference/kotlin/android/util/LruCache#sizeOf(android.util.LruCache.K,%20android.util.LruCache.V)`, this returns the maximum number of entries in the cache. For all other caches, this returns the maximum sum of the sizes of the entries in this cache.

### missCount

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun missCount(): Int
```

Returns the number of times `https://developer.android.com/reference/kotlin/android/util/LruCache#get(android.util.LruCache.K)` returned null or required a new value to be created.

### put

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun put(
    key: K, 
    value: V
): V
```

Caches `value` for `key`. The value is moved to the head of the queue.

| Return ||
|---|---|
| `V` | the previous value mapped by `key`. |

### putCount

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun putCount(): Int
```

Returns the number of times `https://developer.android.com/reference/kotlin/android/util/LruCache#put(android.util.LruCache.K,%20android.util.LruCache.V)` was called.

### remove

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun remove(key: K): V
```

Removes the entry for `key` if it exists.

| Return ||
|---|---|
| `V` | the previous value mapped by `key`. |

### resize

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun resize(maxSize: Int): Unit
```

Sets the size of the cache.

| Parameters ||
|---|---|
| `maxSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new maximum size. |

### size

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun size(): Int
```

For caches that do not override `https://developer.android.com/reference/kotlin/android/util/LruCache#sizeOf(android.util.LruCache.K,%20android.util.LruCache.V)`, this returns the number of entries in the cache. For all other caches, this returns the sum of the sizes of the entries in this cache.

### snapshot

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun snapshot(): MutableMap<K, V>!
```

Returns a copy of the current contents of the cache, ordered from least recently accessed to most recently accessed.

### toString

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### trimToSize

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun trimToSize(maxSize: Int): Unit
```

Remove the eldest entries until the total of remaining entries is at or below the requested size.

| Parameters ||
|---|---|
| `maxSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum size of the cache before returning. May be -1 to evict even 0-sized elements. |

## Protected methods

### create

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun create(key: K): V
```

Called after a cache miss to compute a value for the corresponding key. Returns the computed value or null if no value can be computed. The default implementation returns null.

The method is called without synchronization: other threads may access the cache while this method is executing.

If a value for `key` exists in the cache when this method returns, the created value will be released with `https://developer.android.com/reference/kotlin/android/util/LruCache#entryRemoved(kotlin.Boolean,%20android.util.LruCache.K,%20android.util.LruCache.V,%20android.util.LruCache.V)` and discarded. This can occur when multiple threads request the same key at the same time (causing multiple values to be created), or when one thread calls `https://developer.android.com/reference/kotlin/android/util/LruCache#put(android.util.LruCache.K,%20android.util.LruCache.V)` while another is creating a value for the same key.

### entryRemoved

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun entryRemoved(
    evicted: Boolean, 
    key: K, 
    oldValue: V, 
    newValue: V
): Unit
```

Called for entries that have been evicted or removed. This method is invoked when a value is evicted to make space, removed by a call to `https://developer.android.com/reference/kotlin/android/util/LruCache#remove(android.util.LruCache.K)`, or replaced by a call to `https://developer.android.com/reference/kotlin/android/util/LruCache#put(android.util.LruCache.K,%20android.util.LruCache.V)`. The default implementation does nothing.

The method is called without synchronization: other threads may access the cache while this method is executing.

| Parameters ||
|---|---|
| `evicted` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the entry is being removed to make space, false if the removal was caused by a `https://developer.android.com/reference/kotlin/android/util/LruCache#put(android.util.LruCache.K,%20android.util.LruCache.V)` or `https://developer.android.com/reference/kotlin/android/util/LruCache#remove(android.util.LruCache.K)`. |
| `newValue` | V: the new value for `key`, if it exists. If non-null, this removal was caused by a `https://developer.android.com/reference/kotlin/android/util/LruCache#put(android.util.LruCache.K,%20android.util.LruCache.V)` or a `https://developer.android.com/reference/kotlin/android/util/LruCache#get(android.util.LruCache.K)`. Otherwise it was caused by an eviction or a `https://developer.android.com/reference/kotlin/android/util/LruCache#remove(android.util.LruCache.K)`. |

### sizeOf

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun sizeOf(
    key: K, 
    value: V
): Int
```

Returns the size of the entry for `key` and `value` in user-defined units. The default implementation returns 1 so that size is the number of entries and max size is the maximum number of entries.

An entry's size must not change while it is in the cache.
