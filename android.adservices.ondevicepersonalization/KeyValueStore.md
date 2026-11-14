# KeyValueStore

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyValueStore

Kotlin| [Java](https://developer.android.com/reference/android/adservices/ondevicepersonalization/KeyValueStore "View this page in Java") 

```
interface KeyValueStore
```

| [android.adservices.ondevicepersonalization.KeyValueStore](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/KeyValueStore#) |

| Known Direct Subclasses [MutableKeyValueStore](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/MutableKeyValueStore) |----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------| | [MutableKeyValueStore](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/MutableKeyValueStore) | An interface to a read-write key-value store. | |

An interface to a read-only key-value store. Used as a Data Access Object for the REMOTE_DATA table.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [get](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/KeyValueStore#get(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Looks up a key in a read-only store. |
| abstract [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [keySet](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/KeyValueStore#keySet())`()` Returns a Set view of the keys contained in the REMOTE_DATA table. |

## Public methods

### get

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun get(key: String): ByteArray?
```

Looks up a key in a read-only store. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The key to look up. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | the value to which the specified key is mapped, or null if there contains no mapping for the key. |

### keySet

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun keySet(): MutableSet<String!>
```

Returns a Set view of the keys contained in the REMOTE_DATA table. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. |
