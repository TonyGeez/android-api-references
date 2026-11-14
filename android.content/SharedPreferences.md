Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SharedPreferences

```
interface SharedPreferences
```

| [android.content.SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences#) |

Interface for accessing and modifying preference data returned by `https://developer.android.com/reference/kotlin/android/content/Context#getSharedPreferences(kotlin.String,%20kotlin.Int)`. For any particular set of preferences, there is a single instance of this class that all clients share. Modifications to the preferences must go through an `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor` object to ensure the preference values remain in a consistent state and control when they are committed to storage. Objects that are returned from the various `get` methods must be treated as immutable by the application.

**Note: The Android team strongly recommends against using `SharedPreferences` for new data storage needs.** Instead, consider using [Jetpack DataStore](https://d.android.com/datastore) for storing small amounts of data, or [Room](https://d.android.com/room) for relational data and larger datasets.

There are several significant drawbacks to using `SharedPreferences`:

- **UI Thread Blocking and ANRs:** Since `SharedPreferences` provides a synchronous API, reading and writing to disk can block the UI thread, leading to jank and StrictMode violations. Additionally, pending `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor#apply()` calls will block the main thread during component lifecycle transitions (such as when Activities or Services start or stop) to ensure data is persisted. This is a common source of Application Not Responding (ANR) errors.
- **Error Handling:** The asynchronous `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor#apply()` method has no mechanism to signal errors to the caller. The synchronous `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor#commit()` method only returns a boolean, providing no detailed information about failures, and can sometimes return `false` even when a write succeeds.
- **Durability and Consistency:** Changes are reflected in memory immediately, before being successfully persisted to disk. This can result in data loss if the app crashes or is terminated. For instance, a user might change a privacy-sensitive preference, but if the app terminates before the change is durably written, the app will load the old value upon restart. Furthermore, the lack of transactional semantics makes operations like incrementing a counter unsafe without external locking.
- **Data Safety:** Data corruption can lead to silent failures or uncatchable exceptions. Additionally, writing malformed UTF-16 strings (such as unpaired surrogates) can result in silent data corruption. Modifying the collections returned by methods like `https://developer.android.com/reference/kotlin/android/content/SharedPreferences#getStringSet(kotlin.String,%20kotlin.collections.MutableSet)` can also lead to unexpected behavior and crashes.

*Note: This class does not support use across multiple processes.*

> [!NOTE]
>
> ### Developer Guides
>
> For more information about using SharedPreferences, read the [Data Storage](https://developer.android.com/guide/topics/data/data-storage.html#pref) developer guide.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor` Interface used for modifying values in a `https://developer.android.com/reference/kotlin/android/content/SharedPreferences#` object. |
| abstract | `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.OnSharedPreferenceChangeListener` Interface definition for a callback to be invoked when a shared preference is changed. |

| Public methods ||
|---|---|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/SharedPreferences#contains(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Checks whether the preferences contains a preference. |
| abstract [SharedPreferences.Editor](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor)! | `https://developer.android.com/reference/kotlin/android/content/SharedPreferences#edit()()` Create a new Editor for these preferences, through which you can make modifications to the data in the preferences and atomically commit those changes back to the SharedPreferences object. |
| abstract [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, \*\>! | `https://developer.android.com/reference/kotlin/android/content/SharedPreferences#getAll()()` Retrieve all values from the preferences. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/SharedPreferences#getBoolean(kotlin.String,%20kotlin.Boolean)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Retrieve a boolean value from the preferences. |
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/content/SharedPreferences#getFloat(kotlin.String,%20kotlin.Float)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Retrieve a float value from the preferences. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/SharedPreferences#getInt(kotlin.String,%20kotlin.Int)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve an int value from the preferences. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/content/SharedPreferences#getLong(kotlin.String,%20kotlin.Long)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Retrieve a long value from the preferences. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/content/SharedPreferences#getString(kotlin.String,%20kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Retrieve a String value from the preferences. |
| abstract [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | `https://developer.android.com/reference/kotlin/android/content/SharedPreferences#getStringSet(kotlin.String,%20kotlin.collections.MutableSet)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?)` Retrieve a set of String values from the preferences. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/SharedPreferences#registerOnSharedPreferenceChangeListener(android.content.SharedPreferences.OnSharedPreferenceChangeListener)(listener: https://developer.android.com/reference/kotlin/android/content/SharedPreferences.OnSharedPreferenceChangeListener!)` Registers a callback to be invoked when a change happens to a preference. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/SharedPreferences#unregisterOnSharedPreferenceChangeListener(android.content.SharedPreferences.OnSharedPreferenceChangeListener)(listener: https://developer.android.com/reference/kotlin/android/content/SharedPreferences.OnSharedPreferenceChangeListener!)` Unregisters a previous callback. |

## Public methods

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun contains(key: String!): Boolean
```

Checks whether the preferences contains a preference.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the preference to check. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the preference exists in the preferences, otherwise false. |

### edit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun edit(): SharedPreferences.Editor!
```

Create a new Editor for these preferences, through which you can make modifications to the data in the preferences and atomically commit those changes back to the SharedPreferences object.

Note that you *must* call `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor#commit()` to have any changes you perform in the Editor actually show up in the SharedPreferences.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor!` | Returns a new instance of the `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor` interface, allowing you to modify the values in this SharedPreferences object. |

### getAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getAll(): MutableMap<String!, *>!
```

Retrieve all values from the preferences.

Note that you *must not* modify the collection returned by this method, or alter any of its contents. The consistency of your stored data is not guaranteed if you do.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, *>!` | Returns a map containing a list of pairs key/value representing the preferences. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | |

### getBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getBoolean(
    key: String!, 
    defValue: Boolean
): Boolean
```

Retrieve a boolean value from the preferences.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the preference to retrieve. |
| `defValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Value to return if this preference does not exist. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns the preference value if it exists, or defValue. Throws ClassCastException if there is a preference with this name that is not a boolean. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | |

### getFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getFloat(
    key: String!, 
    defValue: Float
): Float
```

Retrieve a float value from the preferences.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the preference to retrieve. |
| `defValue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Value to return if this preference does not exist. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Returns the preference value if it exists, or defValue. Throws ClassCastException if there is a preference with this name that is not a float. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | |

### getInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getInt(
    key: String!, 
    defValue: Int
): Int
```

Retrieve an int value from the preferences.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the preference to retrieve. |
| `defValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value to return if this preference does not exist. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns the preference value if it exists, or defValue. Throws ClassCastException if there is a preference with this name that is not an int. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | |

### getLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getLong(
    key: String!, 
    defValue: Long
): Long
```

Retrieve a long value from the preferences.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the preference to retrieve. |
| `defValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Value to return if this preference does not exist. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Returns the preference value if it exists, or defValue. Throws ClassCastException if there is a preference with this name that is not a long. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | |

### getString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getString(
    key: String!, 
    defValue: String?
): String?
```

Retrieve a String value from the preferences.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the preference to retrieve. |
| `defValue` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: Value to return if this preference does not exist. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | Returns the preference value if it exists, or defValue. Throws ClassCastException if there is a preference with this name that is not a String. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | |

### getStringSet

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getStringSet(
    key: String!, 
    defValues: MutableSet<String!>?
): MutableSet<String!>?
```

Retrieve a set of String values from the preferences.

Note that you *must not* modify the set instance returned by this call. The consistency of the stored data is not guaranteed if you do, nor is your ability to modify the instance at all.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the preference to retrieve. |
| `defValues` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: Values to return if this preference does not exist. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` | Returns the preference values if they exist, or defValues. Throws ClassCastException if there is a preference with this name that is not a Set. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | |

### registerOnSharedPreferenceChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun registerOnSharedPreferenceChangeListener(listener: SharedPreferences.OnSharedPreferenceChangeListener!): Unit
```

Registers a callback to be invoked when a change happens to a preference.

**Caution:** The preference manager does not currently store a strong reference to the listener. You must store a strong reference to the listener, or it will be susceptible to garbage collection. We recommend you keep a reference to the listener in the instance data of an object that will exist as long as you need the listener.

| Parameters ||
|---|---|
| `listener` | [SharedPreferences.OnSharedPreferenceChangeListener](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.OnSharedPreferenceChangeListener)!: The callback that will run. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/SharedPreferences#unregisterOnSharedPreferenceChangeListener(android.content.SharedPreferences.OnSharedPreferenceChangeListener)`

### unregisterOnSharedPreferenceChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun unregisterOnSharedPreferenceChangeListener(listener: SharedPreferences.OnSharedPreferenceChangeListener!): Unit
```

Unregisters a previous callback.

| Parameters ||
|---|---|
| `listener` | [SharedPreferences.OnSharedPreferenceChangeListener](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.OnSharedPreferenceChangeListener)!: The callback that should be unregistered. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/SharedPreferences#registerOnSharedPreferenceChangeListener(android.content.SharedPreferences.OnSharedPreferenceChangeListener)`
