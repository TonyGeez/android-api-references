Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PreferenceDataStore

Kotlin | [Java](https://developer.android.com/reference/android/preference/PreferenceDataStore "View this page in Java")
| --- | --- |

```
interface PreferenceDataStore
```

| [android.preference.PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#) |

| **This interface was deprecated in API level 29.**
|
| Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Preference Library](https://developer.android.com/reference/androidx/preference/package-summary.html) for consistent behavior across all devices. For more information on using the AndroidX Preference Library see [Settings](https://developer.android.com/guide/topics/ui/settings.html).

A data store interface to be implemented and provided to the Preferences framework. This can be used to replace the default `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#`, if needed.

In most cases you want to use `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` as it is automatically backed up and migrated to new devices. However, providing custom data store to preferences can be useful if your app stores its preferences in a local db, cloud or they are device specific like "Developer settings". It might be also useful when you want to use the preferences UI but the data are not supposed to be stored at all because they are valid per session only.

Once a put method is called it is full responsibility of the data store implementation to safely store the given values. Time expensive operations need to be done in the background to prevent from blocking the UI. You also need to have a plan on how to serialize the data in case the activity holding this object gets destroyed.

By default, all "put" methods throw `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

## Summary

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#getBoolean(kotlin.String,%20kotlin.Boolean)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Retrieve a boolean value from the data store. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#getFloat(kotlin.String,%20kotlin.Float)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Retrieve a float value from the data store. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#getInt(kotlin.String,%20kotlin.Int)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve an int value from the data store. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#getLong(kotlin.String,%20kotlin.Long)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Retrieve a long value from the data store. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#getString(kotlin.String,%20kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Retrieve a String value from the data store. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#getStringSet(kotlin.String,%20kotlin.collections.MutableSet)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, defValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?)` Retrieve a set of String values from the data store. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#putBoolean(kotlin.String,%20kotlin.Boolean)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set a boolean value to the data store. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#putFloat(kotlin.String,%20kotlin.Float)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Set a float value to the data store. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#putInt(kotlin.String,%20kotlin.Int)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set an int value to the data store. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#putLong(kotlin.String,%20kotlin.Long)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Set a long value to the data store. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#putString(kotlin.String,%20kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Set a String value to the data store. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#putStringSet(kotlin.String,%20kotlin.collections.MutableSet)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, values: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?)` Set a set of String value to the data store. |
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

- `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#getBoolean(kotlin.String,%20kotlin.Boolean)`

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

- `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#putFloat(kotlin.String,%20kotlin.Float)`

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

- `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#putInt(kotlin.String,%20kotlin.Int)`

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

- `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#putLong(kotlin.String,%20kotlin.Long)`

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

- `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#putString(kotlin.String,%20kotlin.String)`

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

- `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#putStringSet(kotlin.String,%20kotlin.collections.MutableSet)`

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

- `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#getBoolean(kotlin.String,%20kotlin.Boolean)`

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

- `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#getFloat(kotlin.String,%20kotlin.Float)`

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

- `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#getInt(kotlin.String,%20kotlin.Int)`

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

- `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#getLong(kotlin.String,%20kotlin.Long)`

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

- `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#getString(kotlin.String,%20kotlin.String)`

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

- `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore#getStringSet(kotlin.String,%20kotlin.collections.MutableSet)`
