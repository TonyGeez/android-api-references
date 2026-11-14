Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PreferenceDataStore

Kotlin | [Java](PreferenceDataStore.md)
| --- | --- |

```
interface PreferenceDataStore
```

| [android.preference.PreferenceDataStore](PreferenceDataStore.md) |

| **This interface was deprecated in API level 29.**
|
| Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Preference Library](../androidx/preference/_package.md) for consistent behavior across all devices. For more information on using the AndroidX Preference Library see [Settings](https://developer.android.com/guide/topics/ui/settings.html).

A data store interface to be implemented and provided to the Preferences framework. This can be used to replace the default `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#`, if needed.

In most cases you want to use `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` as it is automatically backed up and migrated to new devices. However, providing custom data store to preferences can be useful if your app stores its preferences in a local db, cloud or they are device specific like "Developer settings". It might be also useful when you want to use the preferences UI but the data are not supposed to be stored at all because they are valid per session only.

Once a put method is called it is full responsibility of the data store implementation to safely store the given values. Time expensive operations need to be done in the background to prevent from blocking the UI. You also need to have a plan on how to serialize the data in case the activity holding this object gets destroyed.

By default, all "put" methods throw `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

## Summary

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | getBoolean Retrieve a boolean value from the data store. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getFloat Retrieve a float value from the data store. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getInt Retrieve an int value from the data store. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getLong Retrieve a long value from the data store. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getString Retrieve a String value from the data store. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | getStringSet Retrieve a set of String values from the data store. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | putBoolean Set a boolean value to the data store. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | putFloat Set a float value to the data store. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | putInt Set an int value to the data store. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | putLong Set a long value to the data store. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | putString Set a String value to the data store. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | putStringSet Set a set of String value to the data store. |
| --- | --- |

## Public methods

### getBoolean

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBoolean(
    key: String!, 
    defValue: Boolean
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Retrieve a boolean value from the data store.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the preference to retrieve. |
| `defValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Value to return if this preference does not exist. |

**See Also**

- getBoolean

### getFloat

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFloat(
    key: String!, 
    defValue: Float
): Float
```

**Deprecated:** *Deprecated in Java.*

Retrieve a float value from the data store.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the preference to retrieve. |
| `defValue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Value to return if this preference does not exist. |

**See Also**

- putFloat

### getInt

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInt(
    key: String!, 
    defValue: Int
): Int
```

**Deprecated:** *Deprecated in Java.*

Retrieve an int value from the data store.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the preference to retrieve. |
| `defValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value to return if this preference does not exist. |

**See Also**

- putInt

### getLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLong(
    key: String!, 
    defValue: Long
): Long
```

**Deprecated:** *Deprecated in Java.*

Retrieve a long value from the data store.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the preference to retrieve. |
| `defValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Value to return if this preference does not exist. |

**See Also**

- putLong

### getString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getString(
    key: String!, 
    defValue: String?
): String?
```

**Deprecated:** *Deprecated in Java.*

Retrieve a String value from the data store.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the preference to retrieve. |
| `defValue` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: Value to return if this preference does not exist. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

**See Also**

- putString

### getStringSet

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStringSet(
    key: String!, 
    defValues: MutableSet<String!>?
): MutableSet<String!>?
```

**Deprecated:** *Deprecated in Java.*

Retrieve a set of String values from the data store.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the preference to retrieve. |
| `defValues` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: Values to return if this preference does not exist. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` | This value may be `null`. |

**See Also**

- putStringSet

### putBoolean

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun putBoolean(
    key: String!, 
    value: Boolean
): Unit
```

**Deprecated:** *Deprecated in Java.*

Set a boolean value to the data store.

Once the value is set the data store is responsible for holding it.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the preference to modify. |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The new value for the preference. |

**See Also**

- getBoolean

### putFloat

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun putFloat(
    key: String!, 
    value: Float
): Unit
```

**Deprecated:** *Deprecated in Java.*

Set a float value to the data store.

Once the value is set the data store is responsible for holding it.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the preference to modify. |
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The new value for the preference. |

**See Also**

- getFloat

### putInt

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun putInt(
    key: String!, 
    value: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Set an int value to the data store.

Once the value is set the data store is responsible for holding it.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the preference to modify. |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new value for the preference. |

**See Also**

- getInt

### putLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun putLong(
    key: String!, 
    value: Long
): Unit
```

**Deprecated:** *Deprecated in Java.*

Set a long value to the data store.

Once the value is set the data store is responsible for holding it.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the preference to modify. |
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The new value for the preference. |

**See Also**

- getLong

### putString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun putString(
    key: String!, 
    value: String?
): Unit
```

**Deprecated:** *Deprecated in Java.*

Set a String value to the data store.

Once the value is set the data store is responsible for holding it.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the preference to modify. |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The new value for the preference. This value may be `null`. |

**See Also**

- getString

### putStringSet

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun putStringSet(
    key: String!, 
    values: MutableSet<String!>?
): Unit
```

**Deprecated:** *Deprecated in Java.*

Set a set of String value to the data store.

Once the value is set the data store is responsible for holding it.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the preference to modify. |
| `values` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: The set of new values for the preference. This value may be `null`. |

**See Also**

- getStringSet
