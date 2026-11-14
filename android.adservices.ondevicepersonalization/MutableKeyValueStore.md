Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MutableKeyValueStore

```
interface MutableKeyValueStore : KeyValueStore
```

| [android.adservices.ondevicepersonalization.MutableKeyValueStore](MutableKeyValueStore.md) |

> [!CAUTION]
> **This interface was deprecated in API level 37.**
>
> The ODP APIs are deprecated and will not be supported in future Android releases. There is no direct replacement API available. Developers currently integrated with these APIs must cease further integration efforts. For comprehensive details regarding this deprecation and the future roadmap of Privacy Sandbox on Android, please consult the official Privacy Sandbox developer documentation and announcements: <https://privacysandbox.google.com>

An interface to a read-write key-value store. Used as a Data Access Object for the LOCAL_DATA table.

## Summary

| Public methods ||
|---|---|
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/MutableKeyValueStore#put(kotlin.String,%20kotlin.ByteArray)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)` Associates the specified value with the specified key. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/MutableKeyValueStore#remove(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Removes the mapping for the specified key. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/KeyValueStore` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/KeyValueStore#get(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Looks up a key in a read-only store. This method may take several seconds to complete, so it should only be called from a worker thread. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/KeyValueStore#keySet()()` Returns a Set view of the keys contained in the REMOTE_DATA table. This method may take several seconds to complete, so it should only be called from a worker thread. <br /> | ||

## Public methods

### put

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun put(
    key: String, 
    value: ByteArray
): ByteArray?
```

**Deprecated:** *Deprecated in Java.*

Associates the specified value with the specified key. If a value already exists for that key, the old value is replaced. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): key with which the specified value is to be associated. This value cannot be `null`. |
| `value` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): value to be associated with the specified key. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | the previous value associated with key, or null if there was no mapping for key. |

### remove

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun remove(key: String): ByteArray?
```

**Deprecated:** *Deprecated in Java.*

Removes the mapping for the specified key. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): key whose mapping is to be removed. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | the previous value associated with key, or null if there was no mapping for key. |
