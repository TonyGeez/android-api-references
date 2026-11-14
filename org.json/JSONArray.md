# JSONArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JSONArray

```
open class JSONArray
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [org.json.JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#) |

A dense indexed sequence of values. Values may be any mix of [JSONObjects](https://developer.android.com/reference/kotlin/org/json/JSONObject), other [JSONArrays](https://developer.android.com/reference/kotlin/org/json/JSONArray#), Strings, Booleans, Integers, Longs, Doubles,`null`or [JSONObject.NULL](https://developer.android.com/reference/kotlin/org/json/JSONObject#NULL:kotlin.Any). Values may not be [NaNs](https://developer.android.com/reference/kotlin/java/lang/Double.html#isNaN()), [infinities](https://developer.android.com/reference/kotlin/java/lang/Double.html#isInfinite()), or of any type not listed here.

`JSONArray`has the same type coercion behavior and optional/mandatory accessors as [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject). See that class' documentation for details.

**Warning:** this class represents null in two incompatible ways: the standard Java`null`reference, and the sentinel value [org.json.JSONObject#NULL](https://developer.android.com/reference/kotlin/org/json/JSONObject#NULL:kotlin.Any). In particular,`get`fails if the requested index holds the null reference, but succeeds if it holds`JSONObject.NULL`.

Instances of this class are not thread safe. Although this class is nonfinal, it was not designed for inheritance and should not be subclassed. In particular, self-use by overridable methods is not specified. See*Effective Java*Item 17, "Design and Document or inheritance or else prohibit it" for further information.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#JSONArray())`()` Creates a`JSONArray`with no values. |
| [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#JSONArray(kotlin.Any))`(`array:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Creates a new`JSONArray`with values from the given primitive array. |
| [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#JSONArray(kotlin.String))`(`json:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new`JSONArray`with values from the JSON string. |
| [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#JSONArray(kotlin.collections.MutableCollection))`(`copyFrom:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?>!`)` Creates a new`JSONArray`by copying all values from the given collection. |
| [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#JSONArray(org.json.JSONTokener))`(`readFrom:` ` [JSONTokener](https://developer.android.com/reference/kotlin/org/json/JSONTokener)!`)` Creates a new`JSONArray`with values from the next array in the tokener. |

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/org/json/JSONArray#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [get](https://developer.android.com/reference/kotlin/org/json/JSONArray#get(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBoolean](https://developer.android.com/reference/kotlin/org/json/JSONArray#getBoolean(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is a boolean or can be coerced to a boolean. |
| --- | --- |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](https://developer.android.com/reference/kotlin/org/json/JSONArray#getDouble(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is a double or can be coerced to a double. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](https://developer.android.com/reference/kotlin/org/json/JSONArray#getInt(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is an int or can be coerced to an int. |
| open [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#)! | [getJSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#getJSONArray(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is a`JSONArray`. |
| --- | --- |
| open [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject)! | [getJSONObject](https://developer.android.com/reference/kotlin/org/json/JSONArray#getJSONObject(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is a`JSONObject`. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](https://developer.android.com/reference/kotlin/org/json/JSONArray#getLong(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is a long or can be coerced to a long. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](https://developer.android.com/reference/kotlin/org/json/JSONArray#getString(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists, coercing it if necessary. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/org/json/JSONArray#hashCode())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNull](https://developer.android.com/reference/kotlin/org/json/JSONArray#isNull(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if this array has no value at`index`, or if its value is the`null`reference or [JSONObject.NULL](https://developer.android.com/reference/kotlin/org/json/JSONObject#NULL:kotlin.Any). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [join](https://developer.android.com/reference/kotlin/org/json/JSONArray#join(kotlin.String))`(`separator:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a new string by alternating this array's values with`separator`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [length](https://developer.android.com/reference/kotlin/org/json/JSONArray#length())`()` Returns the number of values in this array. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [opt](https://developer.android.com/reference/kotlin/org/json/JSONArray#opt(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`, or null if the array has no value at`index`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [optBoolean](https://developer.android.com/reference/kotlin/org/json/JSONArray#optBoolean(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is a boolean or can be coerced to a boolean. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [optBoolean](https://developer.android.com/reference/kotlin/org/json/JSONArray#optBoolean(kotlin.Int,%20kotlin.Boolean))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fallback:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns the value at`index`if it exists and is a boolean or can be coerced to a boolean. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [optDouble](https://developer.android.com/reference/kotlin/org/json/JSONArray#optDouble(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is a double or can be coerced to a double. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [optDouble](https://developer.android.com/reference/kotlin/org/json/JSONArray#optDouble(kotlin.Int,%20kotlin.Double))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fallback:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns the value at`index`if it exists and is a double or can be coerced to a double. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [optInt](https://developer.android.com/reference/kotlin/org/json/JSONArray#optInt(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is an int or can be coerced to an int. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [optInt](https://developer.android.com/reference/kotlin/org/json/JSONArray#optInt(kotlin.Int,%20kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fallback:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is an int or can be coerced to an int. |
| open [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#)! | [optJSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#optJSONArray(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is a`JSONArray`. |
| --- | --- |
| open [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject)! | [optJSONObject](https://developer.android.com/reference/kotlin/org/json/JSONArray#optJSONObject(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is a`JSONObject`. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [optLong](https://developer.android.com/reference/kotlin/org/json/JSONArray#optLong(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists and is a long or can be coerced to a long. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [optLong](https://developer.android.com/reference/kotlin/org/json/JSONArray#optLong(kotlin.Int,%20kotlin.Long))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fallback:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the value at`index`if it exists and is a long or can be coerced to a long. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [optString](https://developer.android.com/reference/kotlin/org/json/JSONArray#optString(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value at`index`if it exists, coercing it if necessary. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [optString](https://developer.android.com/reference/kotlin/org/json/JSONArray#optString(kotlin.Int,%20kotlin.String))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fallback:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the value at`index`if it exists, coercing it if necessary. |
| open [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#)! | [put](https://developer.android.com/reference/kotlin/org/json/JSONArray#put(kotlin.Boolean))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Appends`value`to the end of this array. |
| --- | --- |
| open [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#)! | [put](https://developer.android.com/reference/kotlin/org/json/JSONArray#put(kotlin.Double))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Appends`value`to the end of this array. |
| open [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#)! | [put](https://developer.android.com/reference/kotlin/org/json/JSONArray#put(kotlin.Int))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Appends`value`to the end of this array. |
| open [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#)! | [put](https://developer.android.com/reference/kotlin/org/json/JSONArray#put(kotlin.Int,%20kotlin.Boolean))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the value at`index`to`value`, null padding this array to the required length if necessary. |
| --- | --- |
| open [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#)! | [put](https://developer.android.com/reference/kotlin/org/json/JSONArray#put(kotlin.Int,%20kotlin.Double))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Sets the value at`index`to`value`, null padding this array to the required length if necessary. |
| open [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#)! | [put](https://developer.android.com/reference/kotlin/org/json/JSONArray#put(kotlin.Int,%20kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the value at`index`to`value`, null padding this array to the required length if necessary. |
| open [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#)! | [put](https://developer.android.com/reference/kotlin/org/json/JSONArray#put(kotlin.Int,%20kotlin.Any))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Sets the value at`index`to`value`, null padding this array to the required length if necessary. |
| --- | --- |
| open [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#)! | [put](https://developer.android.com/reference/kotlin/org/json/JSONArray#put(kotlin.Int,%20kotlin.Long))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the value at`index`to`value`, null padding this array to the required length if necessary. |
| open [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#)! | [put](https://developer.android.com/reference/kotlin/org/json/JSONArray#put(kotlin.Any))`(`value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Appends`value`to the end of this array. |
| open [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#)! | [put](https://developer.android.com/reference/kotlin/org/json/JSONArray#put(kotlin.Long))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Appends`value`to the end of this array. |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [remove](https://developer.android.com/reference/kotlin/org/json/JSONArray#remove(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Removes and returns the value at`index`, or null if the array has no value at`index`. |
| open [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject)! | [toJSONObject](https://developer.android.com/reference/kotlin/org/json/JSONArray#toJSONObject(org.json.JSONArray))`(`names:` ` [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#)!`)` Returns a new object whose values are the values in this array, and whose names are the values in`names`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/org/json/JSONArray#toString())`()` Encodes this array as a compact JSON string, such as: ```kotlin [94043,90210] ``` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toString](https://developer.android.com/reference/kotlin/org/json/JSONArray#toString(kotlin.Int))`(`indentSpaces:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Encodes this array as a human readable JSON string for debugging, such as: ```kotlin [ 94043, 90210 ] ``` <br /> |

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
| `readFrom` | [JSONTokener](https://developer.android.com/reference/kotlin/org/json/JSONTokener)!:a tokener whose nextValue() method will yield a`JSONArray`. |

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

Returns true if this array has no value at`index`, or if its value is the`null`reference or [JSONObject.NULL](https://developer.android.com/reference/kotlin/org/json/JSONObject#NULL:kotlin.Any). 

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
| [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#)! | this array. |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(value: Double): JSONArray!
```

Appends`value`to the end of this array.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):a finite value. May not be [NaNs](https://developer.android.com/reference/kotlin/java/lang/Double.html#isNaN())or [infinities](https://developer.android.com/reference/kotlin/java/lang/Double.html#isInfinite()). |

| Return ||
|----------------------------------------------------------------------------------|-------------|
| [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#)! | this array. |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(value: Int): JSONArray!
```

Appends`value`to the end of this array.

| Return ||
|----------------------------------------------------------------------------------|-------------|
| [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#)! | this array. |

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
| [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#)! | this array. |

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
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):a finite value. May not be [NaNs](https://developer.android.com/reference/kotlin/java/lang/Double.html#isNaN())or [infinities](https://developer.android.com/reference/kotlin/java/lang/Double.html#isInfinite()). |

| Return ||
|----------------------------------------------------------------------------------|-------------|
| [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#)! | this array. |

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
| [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#)! | this array. |

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
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:a [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject), [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#), String, Boolean, Integer, Long, Double, [JSONObject.NULL](https://developer.android.com/reference/kotlin/org/json/JSONObject#NULL:kotlin.Any), or`null`. May not be [NaNs](https://developer.android.com/reference/kotlin/java/lang/Double.html#isNaN())or [infinities](https://developer.android.com/reference/kotlin/java/lang/Double.html#isInfinite()). |

| Return ||
|----------------------------------------------------------------------------------|-------------|
| [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#)! | this array. |

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
| [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#)! | this array. |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(value: Any!): JSONArray!
```

Appends`value`to the end of this array.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:a [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject), [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#), String, Boolean, Integer, Long, Double, [JSONObject.NULL](https://developer.android.com/reference/kotlin/org/json/JSONObject#NULL:kotlin.Any), or`null`. May not be [NaNs](https://developer.android.com/reference/kotlin/java/lang/Double.html#isNaN())or [infinities](https://developer.android.com/reference/kotlin/java/lang/Double.html#isInfinite()). Unsupported values are not permitted and will cause the array to be in an inconsistent state. |

| Return ||
|----------------------------------------------------------------------------------|-------------|
| [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#)! | this array. |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(value: Long): JSONArray!
```

Appends`value`to the end of this array.

| Return ||
|----------------------------------------------------------------------------------|-------------|
| [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray#)! | this array. |

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
