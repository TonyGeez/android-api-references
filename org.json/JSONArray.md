# JSONArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JSONArray

```
open class JSONArray
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [org.json.JSONArray](../org/json/JSONArray.md) |

A dense indexed sequence of values. Values may be any mix of [JSONObjects](../org/json/JSONObject.md), other [JSONArrays](../org/json/JSONArray.md), Strings, Booleans, Integers, Longs, Doubles,`null`or [JSONObject.NULL](../org/json/JSONObject.md). Values may not be [NaNs](../java/lang/Double.md)), [infinities](../java/lang/Double.md)), or of any type not listed here.

`JSONArray`has the same type coercion behavior and optional/mandatory accessors as [JSONObject](../org/json/JSONObject.md). See that class' documentation for details.

**Warning:** this class represents null in two incompatible ways: the standard Java`null`reference, and the sentinel value [org.json.JSONObject#NULL](../org/json/JSONObject.md). In particular,`get`fails if the requested index holds the null reference, but succeeds if it holds`JSONObject.NULL`.

Instances of this class are not thread safe. Although this class is nonfinal, it was not designed for inheritance and should not be subclassed. In particular, self-use by overridable methods is not specified. See*Effective Java*Item 17, "Design and Document or inheritance or else prohibit it" for further information.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [JSONArray](../org/json/JSONArray.md))`()` Creates a`JSONArray`with no values. |
| [JSONArray](../org/json/JSONArray.md))`(`array:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Creates a new`JSONArray`with values from the given primitive array. |
| [JSONArray](../org/json/JSONArray.md))`(`json:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new`JSONArray`with values from the JSON string. |
| [JSONArray](../org/json/JSONArray.md))`(`copyFrom:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?>!`)` Creates a new`JSONArray`by copying all values from the given collection. |
| [JSONArray](../org/json/JSONArray.md))`(`readFrom:` ` [JSONTokener](../org/json/JSONTokener.md)!`)` Creates a new`JSONArray`with values from the next array in the tokener. |

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../org/json/JSONArray.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [get](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBoolean](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is a boolean or can be coerced to a boolean. |
| --- | --- |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is a double or can be coerced to a double. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is an int or can be coerced to an int. |
| open [JSONArray](../org/json/JSONArray.md)! | [getJSONArray](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is a`JSONArray`. |
| --- | --- |
| open [JSONObject](../org/json/JSONObject.md)! | [getJSONObject](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is a`JSONObject`. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is a long or can be coerced to a long. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists, coercing it if necessary. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../org/json/JSONArray.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNull](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if this array has no value at`index`, or if its value is the`null`reference or [JSONObject.NULL](../org/json/JSONObject.md). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [join](../org/json/JSONArray.md))`(`separator:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a new string by alternating this array's values with`separator`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [length](../org/json/JSONArray.md))`()` Returns the number of values in this array. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [opt](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`, or null if the array has no value at`index`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [optBoolean](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is a boolean or can be coerced to a boolean. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [optBoolean](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fallback:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns the value at`index`if it exists and is a boolean or can be coerced to a boolean. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [optDouble](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is a double or can be coerced to a double. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [optDouble](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fallback:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns the value at`index`if it exists and is a double or can be coerced to a double. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [optInt](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is an int or can be coerced to an int. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [optInt](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fallback:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is an int or can be coerced to an int. |
| open [JSONArray](../org/json/JSONArray.md)! | [optJSONArray](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is a`JSONArray`. |
| --- | --- |
| open [JSONObject](../org/json/JSONObject.md)! | [optJSONObject](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is a`JSONObject`. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [optLong](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is a long or can be coerced to a long. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [optLong](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fallback:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the value at`index`if it exists and is a long or can be coerced to a long. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [optString](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists, coercing it if necessary. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [optString](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fallback:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the value at`index`if it exists, coercing it if necessary. |
| open [JSONArray](../org/json/JSONArray.md)! | [put](../org/json/JSONArray.md))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Appends`value`to the end of this array. |
| --- | --- |
| open [JSONArray](../org/json/JSONArray.md)! | [put](../org/json/JSONArray.md))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Appends`value`to the end of this array. |
| open [JSONArray](../org/json/JSONArray.md)! | [put](../org/json/JSONArray.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Appends`value`to the end of this array. |
| open [JSONArray](../org/json/JSONArray.md)! | [put](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the value at`index`to`value`, null padding this array to the required length if necessary. |
| --- | --- |
| open [JSONArray](../org/json/JSONArray.md)! | [put](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Sets the value at`index`to`value`, null padding this array to the required length if necessary. |
| open [JSONArray](../org/json/JSONArray.md)! | [put](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the value at`index`to`value`, null padding this array to the required length if necessary. |
| open [JSONArray](../org/json/JSONArray.md)! | [put](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Sets the value at`index`to`value`, null padding this array to the required length if necessary. |
| --- | --- |
| open [JSONArray](../org/json/JSONArray.md)! | [put](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the value at`index`to`value`, null padding this array to the required length if necessary. |
| open [JSONArray](../org/json/JSONArray.md)! | [put](../org/json/JSONArray.md))`(`value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Appends`value`to the end of this array. |
| open [JSONArray](../org/json/JSONArray.md)! | [put](../org/json/JSONArray.md))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Appends`value`to the end of this array. |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [remove](../org/json/JSONArray.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Removes and returns the value at`index`, or null if the array has no value at`index`. |
| open [JSONObject](../org/json/JSONObject.md)! | [toJSONObject](../org/json/JSONArray.md))`(`names:` ` [JSONArray](../org/json/JSONArray.md)!`)` Returns a new object whose values are the values in this array, and whose names are the values in`names`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../org/json/JSONArray.md))`()` Encodes this array as a compact JSON string, such as: ```kotlin [94043,90210] ``` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toString](../org/json/JSONArray.md))`(`indentSpaces:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Encodes this array as a human readable JSON string for debugging, such as: ```kotlin [ 94043, 90210 ] ``` <br /> |

## Public constructors

### JSONArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JSONArray()
```

Creates a`JSONArray`with no values. 

### JSONArray

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JSONArray(array: Any!)
```

Creates a new`JSONArray`with values from the given primitive array. 

### JSONArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JSONArray(json: String!)
```

Creates a new`JSONArray`with values from the JSON string.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------|
| `json` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a JSON-encoded string containing an array. |

| Exceptions ||
|--------------------------|---------------------------------------------------|
| `org.json.JSONException` | if the parse fails or doesn't yield a`JSONArray`. |

### JSONArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JSONArray(copyFrom: MutableCollection<Any?>!)
```

Creates a new`JSONArray`by copying all values from the given collection.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `copyFrom` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?\>!:a collection whose values are of supported types. Unsupported values are not permitted and will yield an array in an inconsistent state. |

### JSONArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JSONArray(readFrom: JSONTokener!)
```

Creates a new`JSONArray`with values from the next array in the tokener.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `readFrom` | [JSONTokener](../org/json/JSONTokener.md)!:a tokener whose nextValue() method will yield a`JSONArray`. |

| Exceptions ||
|--------------------------|---------------------------------------------------|
| `org.json.JSONException` | if the parse fails or doesn't yield a`JSONArray`. |

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(index: Int): Any!
```

Returns the value at`index`.

| Exceptions ||
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `org.json.JSONException` | if this array has no value at`index`, or if that value is the`null`reference. This method returns normally if the value is`JSONObject#NULL`. |

### getBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBoolean(index: Int): Boolean
```

Returns the value at`index`if it exists and is a boolean or can be coerced to a boolean.

| Exceptions ||
|--------------------------|------------------------------------------------------------------------|
| `org.json.JSONException` | if the value at`index`doesn't exist or cannot be coerced to a boolean. |

### getDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDouble(index: Int): Double
```

Returns the value at`index`if it exists and is a double or can be coerced to a double.

| Exceptions ||
|--------------------------|-----------------------------------------------------------------------|
| `org.json.JSONException` | if the value at`index`doesn't exist or cannot be coerced to a double. |

### getInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInt(index: Int): Int
```

Returns the value at`index`if it exists and is an int or can be coerced to an int.

| Exceptions ||
|--------------------------|--------------------------------------------------------------------|
| `org.json.JSONException` | if the value at`index`doesn't exist or cannot be coerced to a int. |

### getJSONArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getJSONArray(index: Int): JSONArray!
```

Returns the value at`index`if it exists and is a`JSONArray`.

| Exceptions ||
|--------------------------|----------------------------------------------------|
| `org.json.JSONException` | if the value doesn't exist or is not a`JSONArray`. |

### getJSONObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getJSONObject(index: Int): JSONObject!
```

Returns the value at`index`if it exists and is a`JSONObject`.

| Exceptions ||
|--------------------------|-----------------------------------------------------|
| `org.json.JSONException` | if the value doesn't exist or is not a`JSONObject`. |

### getLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLong(index: Int): Long
```

Returns the value at`index`if it exists and is a long or can be coerced to a long.

| Exceptions ||
|--------------------------|---------------------------------------------------------------------|
| `org.json.JSONException` | if the value at`index`doesn't exist or cannot be coerced to a long. |

### getString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getString(index: Int): String!
```

Returns the value at`index`if it exists, coercing it if necessary.

| Exceptions ||
|--------------------------|--------------------------|
| `org.json.JSONException` | if no such value exists. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isNull

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isNull(index: Int): Boolean
```

Returns true if this array has no value at`index`, or if its value is the`null`reference or [JSONObject.NULL](../org/json/JSONObject.md). 

### join

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun join(separator: String!): String!
```

Returns a new string by alternating this array's values with`separator`. This array's string values are quoted and have their special characters escaped. For example, the array containing the strings '12" pizza', 'taco' and 'soda' joined on '+' returns this: 

```kotlin
"12\" pizza"+"taco"+"soda"
```

<br />

### length

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun length(): Int
```

Returns the number of values in this array. 

### opt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun opt(index: Int): Any!
```

Returns the value at`index`, or null if the array has no value at`index`. 

### optBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optBoolean(index: Int): Boolean
```

Returns the value at`index`if it exists and is a boolean or can be coerced to a boolean. Returns false otherwise. 

### optBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optBoolean(
    index: Int, 
    fallback: Boolean
): Boolean
```

Returns the value at`index`if it exists and is a boolean or can be coerced to a boolean. Returns`fallback`otherwise. 

### optDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optDouble(index: Int): Double
```

Returns the value at`index`if it exists and is a double or can be coerced to a double. Returns`NaN`otherwise. 

### optDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optDouble(
    index: Int, 
    fallback: Double
): Double
```

Returns the value at`index`if it exists and is a double or can be coerced to a double. Returns`fallback`otherwise. 

### optInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optInt(index: Int): Int
```

Returns the value at`index`if it exists and is an int or can be coerced to an int. Returns 0 otherwise. 

### optInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optInt(
    index: Int, 
    fallback: Int
): Int
```

Returns the value at`index`if it exists and is an int or can be coerced to an int. Returns`fallback`otherwise. 

### optJSONArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optJSONArray(index: Int): JSONArray!
```

Returns the value at`index`if it exists and is a`JSONArray`. Returns null otherwise. 

### optJSONObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optJSONObject(index: Int): JSONObject!
```

Returns the value at`index`if it exists and is a`JSONObject`. Returns null otherwise. 

### optLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optLong(index: Int): Long
```

Returns the value at`index`if it exists and is a long or can be coerced to a long. Returns 0 otherwise. 

### optLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optLong(
    index: Int, 
    fallback: Long
): Long
```

Returns the value at`index`if it exists and is a long or can be coerced to a long. Returns`fallback`otherwise. 

### optString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optString(index: Int): String!
```

Returns the value at`index`if it exists, coercing it if necessary. Returns the empty string if no such value exists. 

### optString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optString(
    index: Int, 
    fallback: String!
): String!
```

Returns the value at`index`if it exists, coercing it if necessary. Returns`fallback`if no such value exists. 

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(value: Boolean): JSONArray!
```

Appends`value`to the end of this array.

| Return ||
|----------------------------------------------------------------------------------|-------------|
| [JSONArray](../org/json/JSONArray.md)! | this array. |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(value: Double): JSONArray!
```

Appends`value`to the end of this array.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):a finite value. May not be [NaNs](../java/lang/Double.md))or [infinities](../java/lang/Double.md)). |

| Return ||
|----------------------------------------------------------------------------------|-------------|
| [JSONArray](../org/json/JSONArray.md)! | this array. |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(value: Int): JSONArray!
```

Appends`value`to the end of this array.

| Return ||
|----------------------------------------------------------------------------------|-------------|
| [JSONArray](../org/json/JSONArray.md)! | this array. |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    index: Int, 
    value: Boolean
): JSONArray!
```

Sets the value at`index`to`value`, null padding this array to the required length if necessary. If a value already exists at`index`, it will be replaced.

| Return ||
|----------------------------------------------------------------------------------|-------------|
| [JSONArray](../org/json/JSONArray.md)! | this array. |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    index: Int, 
    value: Double
): JSONArray!
```

Sets the value at`index`to`value`, null padding this array to the required length if necessary. If a value already exists at`index`, it will be replaced.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):a finite value. May not be [NaNs](../java/lang/Double.md))or [infinities](../java/lang/Double.md)). |

| Return ||
|----------------------------------------------------------------------------------|-------------|
| [JSONArray](../org/json/JSONArray.md)! | this array. |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    index: Int, 
    value: Int
): JSONArray!
```

Sets the value at`index`to`value`, null padding this array to the required length if necessary. If a value already exists at`index`, it will be replaced.

| Return ||
|----------------------------------------------------------------------------------|-------------|
| [JSONArray](../org/json/JSONArray.md)! | this array. |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    index: Int, 
    value: Any!
): JSONArray!
```

Sets the value at`index`to`value`, null padding this array to the required length if necessary. If a value already exists at`index`, it will be replaced.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:a [JSONObject](../org/json/JSONObject.md), [JSONArray](../org/json/JSONArray.md), String, Boolean, Integer, Long, Double, [JSONObject.NULL](../org/json/JSONObject.md), or`null`. May not be [NaNs](../java/lang/Double.md))or [infinities](../java/lang/Double.md)). |

| Return ||
|----------------------------------------------------------------------------------|-------------|
| [JSONArray](../org/json/JSONArray.md)! | this array. |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    index: Int, 
    value: Long
): JSONArray!
```

Sets the value at`index`to`value`, null padding this array to the required length if necessary. If a value already exists at`index`, it will be replaced.

| Return ||
|----------------------------------------------------------------------------------|-------------|
| [JSONArray](../org/json/JSONArray.md)! | this array. |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(value: Any!): JSONArray!
```

Appends`value`to the end of this array.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:a [JSONObject](../org/json/JSONObject.md), [JSONArray](../org/json/JSONArray.md), String, Boolean, Integer, Long, Double, [JSONObject.NULL](../org/json/JSONObject.md), or`null`. May not be [NaNs](../java/lang/Double.md))or [infinities](../java/lang/Double.md)). Unsupported values are not permitted and will cause the array to be in an inconsistent state. |

| Return ||
|----------------------------------------------------------------------------------|-------------|
| [JSONArray](../org/json/JSONArray.md)! | this array. |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(value: Long): JSONArray!
```

Appends`value`to the end of this array.

| Return ||
|----------------------------------------------------------------------------------|-------------|
| [JSONArray](../org/json/JSONArray.md)! | this array. |

### remove

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(index: Int): Any!
```

Removes and returns the value at`index`, or null if the array has no value at`index`. 

### toJSONObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toJSONObject(names: JSONArray!): JSONObject!
```

Returns a new object whose values are the values in this array, and whose names are the values in`names`. Names and values are paired up by index from 0 through to the shorter array's length. Names that are not strings will be coerced to strings. This method returns null if either array is empty. 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Encodes this array as a compact JSON string, such as: 

```kotlin
[94043,90210]
```

<br />

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(indentSpaces: Int): String!
```

Encodes this array as a human readable JSON string for debugging, such as: 

```kotlin
[
      94043,
      90210
  ]
```

<br />

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `indentSpaces` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of spaces to indent for each level of nesting. |
