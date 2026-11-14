# BaseBundle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BaseBundle

Kotlin| [Java](https://developer.android.com/reference/android/os/BaseBundle "View this page in Java") 

```
open class BaseBundle
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.os.BaseBundle](https://developer.android.com/reference/kotlin/android/os/BaseBundle#) |

| Known Direct Subclasses [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle), [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle) |--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------| | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle) | A mapping from String keys to various [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable) values. | | [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle) | A mapping from String keys to values of various types. | |

A mapping from String keys to values of various types. In most cases, you should work directly with either the [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle) or [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle) subclass.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/android/os/BaseBundle#clear())`()` Removes all elements from the mapping of this Bundle. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsKey](https://developer.android.com/reference/kotlin/android/os/BaseBundle#containsKey(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns true if the given key is contained in the mapping of this Bundle. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | [get](https://developer.android.com/reference/kotlin/android/os/BaseBundle#get(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the entry with the given key as an object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBoolean](https://developer.android.com/reference/kotlin/android/os/BaseBundle#getBoolean(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the value associated with the given key, or false if no mapping of the desired type exists for the given key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBoolean](https://developer.android.com/reference/kotlin/android/os/BaseBundle#getBoolean(kotlin.String,%20kotlin.Boolean))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `defaultValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key. |
| open [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)? | [getBooleanArray](https://developer.android.com/reference/kotlin/android/os/BaseBundle#getBooleanArray(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](https://developer.android.com/reference/kotlin/android/os/BaseBundle#getDouble(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the value associated with the given key, or 0. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](https://developer.android.com/reference/kotlin/android/os/BaseBundle#getDouble(kotlin.String,%20kotlin.Double))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `defaultValue:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key. |
| open [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)? | [getDoubleArray](https://developer.android.com/reference/kotlin/android/os/BaseBundle#getDoubleArray(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](https://developer.android.com/reference/kotlin/android/os/BaseBundle#getInt(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the value associated with the given key, or 0 if no mapping of the desired type exists for the given key. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](https://developer.android.com/reference/kotlin/android/os/BaseBundle#getInt(kotlin.String,%20kotlin.Int))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `defaultValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | [getIntArray](https://developer.android.com/reference/kotlin/android/os/BaseBundle#getIntArray(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](https://developer.android.com/reference/kotlin/android/os/BaseBundle#getLong(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the value associated with the given key, or 0L if no mapping of the desired type exists for the given key. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](https://developer.android.com/reference/kotlin/android/os/BaseBundle#getLong(kotlin.String,%20kotlin.Long))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `defaultValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key. |
| open [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)? | [getLongArray](https://developer.android.com/reference/kotlin/android/os/BaseBundle#getLongArray(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getString](https://developer.android.com/reference/kotlin/android/os/BaseBundle#getString(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](https://developer.android.com/reference/kotlin/android/os/BaseBundle#getString(kotlin.String,%20kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `defaultValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key or if a null value is explicitly associated with the given key. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | [getStringArray](https://developer.android.com/reference/kotlin/android/os/BaseBundle#getStringArray(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/android/os/BaseBundle#isEmpty())`()` Returns true if the mapping of this Bundle is empty, false otherwise. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [keySet](https://developer.android.com/reference/kotlin/android/os/BaseBundle#keySet())`()` Returns a Set containing the Strings used as keys in this Bundle. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putAll](https://developer.android.com/reference/kotlin/android/os/BaseBundle#putAll(android.os.PersistableBundle))`(`bundle:` ` [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle)!`)` Inserts all mappings from the given PersistableBundle into this BaseBundle. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putBoolean](https://developer.android.com/reference/kotlin/android/os/BaseBundle#putBoolean(kotlin.String,%20kotlin.Boolean))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Inserts a Boolean value into the mapping of this Bundle, replacing any existing value for the given key. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putBooleanArray](https://developer.android.com/reference/kotlin/android/os/BaseBundle#putBooleanArray(kotlin.String,%20kotlin.BooleanArray))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `value:` ` [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)?`)` Inserts a boolean array value into the mapping of this Bundle, replacing any existing value for the given key. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putDouble](https://developer.android.com/reference/kotlin/android/os/BaseBundle#putDouble(kotlin.String,%20kotlin.Double))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Inserts a double value into the mapping of this Bundle, replacing any existing value for the given key. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putDoubleArray](https://developer.android.com/reference/kotlin/android/os/BaseBundle#putDoubleArray(kotlin.String,%20kotlin.DoubleArray))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `value:` ` [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)?`)` Inserts a double array value into the mapping of this Bundle, replacing any existing value for the given key. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putInt](https://developer.android.com/reference/kotlin/android/os/BaseBundle#putInt(kotlin.String,%20kotlin.Int))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Inserts an int value into the mapping of this Bundle, replacing any existing value for the given key. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putIntArray](https://developer.android.com/reference/kotlin/android/os/BaseBundle#putIntArray(kotlin.String,%20kotlin.IntArray))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `value:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?`)` Inserts an int array value into the mapping of this Bundle, replacing any existing value for the given key. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putLong](https://developer.android.com/reference/kotlin/android/os/BaseBundle#putLong(kotlin.String,%20kotlin.Long))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Inserts a long value into the mapping of this Bundle, replacing any existing value for the given key. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putLongArray](https://developer.android.com/reference/kotlin/android/os/BaseBundle#putLongArray(kotlin.String,%20kotlin.LongArray))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `value:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)?`)` Inserts a long array value into the mapping of this Bundle, replacing any existing value for the given key. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putString](https://developer.android.com/reference/kotlin/android/os/BaseBundle#putString(kotlin.String,%20kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Inserts a String value into the mapping of this Bundle, replacing any existing value for the given key. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putStringArray](https://developer.android.com/reference/kotlin/android/os/BaseBundle#putStringArray(kotlin.String,%20kotlin.Array))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `value:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` Inserts a String array value into the mapping of this Bundle, replacing any existing value for the given key. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [remove](https://developer.android.com/reference/kotlin/android/os/BaseBundle#remove(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Removes any entry with the given key from the mapping of this Bundle. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](https://developer.android.com/reference/kotlin/android/os/BaseBundle#size())`()` Returns the number of mappings contained in this Bundle. |

## Public methods

### clear

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Removes all elements from the mapping of this Bundle. Recycles the underlying parcel if it is still present. 

### containsKey

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun containsKey(key: String!): Boolean
```

Returns true if the given key is contained in the mapping of this Bundle.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a String key |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the key is part of the mapping, false otherwise |

### get

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(key: String!): Any?
```

**Deprecated:** *Use the type-safe specific APIs depending on the type of the item to be retrieved, eg. [getString(java.lang.String)](https://developer.android.com/reference/kotlin/android/os/BaseBundle#getString(kotlin.String)).*

Returns the entry with the given key as an object.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a String key |

| Return ||
|-----------------------------------------------------------------------------|--------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | an Object, or null |

### getBoolean

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBoolean(key: String!): Boolean
```

Returns the value associated with the given key, or false if no mapping of the desired type exists for the given key.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a String |

| Return ||
|------------------------------------------------------------------------------------|-----------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a boolean value |

### getBoolean

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBoolean(
    key: String!, 
    defaultValue: Boolean
): Boolean
```

Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a String |
| `defaultValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Value to return if key does not exist |

| Return ||
|------------------------------------------------------------------------------------|-----------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a boolean value |

### getBooleanArray

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBooleanArray(key: String?): BooleanArray?
```

Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:a String, or null |

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------|
| [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)? | a boolean\[\] value, or null |

### getDouble

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDouble(key: String!): Double
```

Returns the value associated with the given key, or 0.0 if no mapping of the desired type exists for the given key.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a String |

| Return ||
|----------------------------------------------------------------------------------|----------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | a double value |

### getDouble

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDouble(
    key: String!, 
    defaultValue: Double
): Double
```

Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a String |
| `defaultValue` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):Value to return if key does not exist |

| Return ||
|----------------------------------------------------------------------------------|----------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | a double value |

### getDoubleArray

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDoubleArray(key: String?): DoubleArray?
```

Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:a String, or null |

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------|
| [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)? | a double\[\] value, or null |

### getInt

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInt(key: String!): Int
```

Returns the value associated with the given key, or 0 if no mapping of the desired type exists for the given key.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a String |

| Return ||
|----------------------------------------------------------------------------|--------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an int value |

### getInt

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInt(
    key: String!, 
    defaultValue: Int
): Int
```

Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a String |
| `defaultValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value to return if key does not exist |

| Return ||
|----------------------------------------------------------------------------|--------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an int value |

### getIntArray

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIntArray(key: String?): IntArray?
```

Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:a String, or null |

| Return ||
|----------------------------------------------------------------------------------------|---------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | an int\[\] value, or null |

### getLong

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLong(key: String!): Long
```

Returns the value associated with the given key, or 0L if no mapping of the desired type exists for the given key.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a String |

| Return ||
|------------------------------------------------------------------------------|--------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a long value |

### getLong

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLong(
    key: String!, 
    defaultValue: Long
): Long
```

Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a String |
| `defaultValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Value to return if key does not exist |

| Return ||
|------------------------------------------------------------------------------|--------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a long value |

### getLongArray

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLongArray(key: String?): LongArray?
```

Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:a String, or null |

| Return ||
|------------------------------------------------------------------------------------------|---------------------------|
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)? | a long\[\] value, or null |

### getString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getString(key: String?): String?
```

Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:a String, or null |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | a String value, or null |

### getString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getString(
    key: String?, 
    defaultValue: String!
): String!
```

Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key or if a null value is explicitly associated with the given key.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:a String, or null |
| `defaultValue` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Value to return if key does not exist or if a null value is associated with the given key. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the String value associated with the given key, or defaultValue if no valid String object is currently mapped to that key. |

### getStringArray

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStringArray(key: String?): Array<String!>?
```

Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:a String, or null |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>? | a String\[\] value, or null |

### isEmpty

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEmpty(): Boolean
```

Returns true if the mapping of this Bundle is empty, false otherwise. 

### keySet

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun keySet(): MutableSet<String!>!
```

Returns a Set containing the Strings used as keys in this Bundle.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | a Set of String keys |

### putAll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putAll(bundle: PersistableBundle!): Unit
```

Inserts all mappings from the given PersistableBundle into this BaseBundle.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------|
| `bundle` | [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle)!:a PersistableBundle |

### putBoolean

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putBoolean(
    key: String?, 
    value: Boolean
): Unit
```

Inserts a Boolean value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:a String, or null |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):a boolean |

### putBooleanArray

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putBooleanArray(
    key: String?, 
    value: BooleanArray?
): Unit
```

Inserts a boolean array value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:a String, or null |
| `value` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)?:a boolean array object, or null |

### putDouble

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putDouble(
    key: String?, 
    value: Double
): Unit
```

Inserts a double value into the mapping of this Bundle, replacing any existing value for the given key.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:a String, or null |
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):a double |

### putDoubleArray

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putDoubleArray(
    key: String?, 
    value: DoubleArray?
): Unit
```

Inserts a double array value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:a String, or null |
| `value` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)?:a double array object, or null |

### putInt

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putInt(
    key: String?, 
    value: Int
): Unit
```

Inserts an int value into the mapping of this Bundle, replacing any existing value for the given key.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:a String, or null |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an int |

### putIntArray

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putIntArray(
    key: String?, 
    value: IntArray?
): Unit
```

Inserts an int array value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:a String, or null |
| `value` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?:an int array object, or null |

### putLong

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putLong(
    key: String?, 
    value: Long
): Unit
```

Inserts a long value into the mapping of this Bundle, replacing any existing value for the given key.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:a String, or null |
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a long |

### putLongArray

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putLongArray(
    key: String?, 
    value: LongArray?
): Unit
```

Inserts a long array value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:a String, or null |
| `value` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)?:a long array object, or null |

### putString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putString(
    key: String?, 
    value: String?
): Unit
```

Inserts a String value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:a String, or null |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:a String, or null |

### putStringArray

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putStringArray(
    key: String?, 
    value: Array<String!>?
): Unit
```

Inserts a String array value into the mapping of this Bundle, replacing any existing value for the given key. Either key or value may be null.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:a String, or null |
| `value` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:a String array object, or null |

### remove

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(key: String!): Unit
```

Removes any entry with the given key from the mapping of this Bundle.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a String key |

### size

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun size(): Int
```

Returns the number of mappings contained in this Bundle.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of mappings as an int. |
