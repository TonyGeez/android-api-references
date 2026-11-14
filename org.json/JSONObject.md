# JSONObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JSONObject

```
open class JSONObject
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [org.json.JSONObject](../org/json/JSONObject.md) |

A modifiable set of name/value mappings. Names are unique, non-null strings. Values may be any mix of [JSONObjects](../org/json/JSONObject.md), [JSONArrays](../org/json/JSONArray.md), Strings, Booleans, Integers, Longs, Doubles or [NULL](../org/json/JSONObject.md). Values may not be`null`, [NaNs](../java/lang/Double.md)), [infinities](../java/lang/Double.md)), or of any type not listed here.

This class can coerce values to another type when requested.

- When the requested type is a boolean, strings will be coerced using a case-insensitive comparison to "true" and "false".
- When the requested type is a double, other [Number](../java/lang/Number.md) types will be coerced using [doubleValue](../java/lang/Number.md)). Strings that can be coerced using [Double.valueOf(String)](../java/lang/Double.md))will be.
- When the requested type is an int, other [Number](../java/lang/Number.md) types will be coerced using [intValue](../java/lang/Number.md)). Strings that can be coerced using [Double.valueOf(String)](../java/lang/Double.md))will be, and then cast to int.
- When the requested type is a long, other [Number](../java/lang/Number.md) types will be coerced using [longValue](../java/lang/Number.md)). Strings that can be coerced using [Double.valueOf(String)](../java/lang/Double.md))will be, and then cast to long. This two-step conversion is lossy for very large values. For example, the string "9223372036854775806" yields the long 9223372036854775807.
- When the requested type is a String, other non-null values will be coerced using [String.valueOf(Object)](../java/lang/String.md)). Although null cannot be coerced, the sentinel value [JSONObject.NULL](../org/json/JSONObject.md) is coerced to the string "null".

This class can look up both mandatory and optional values:

- Use`get`*Type*`()`to retrieve a mandatory value. This fails with a`JSONException`if the requested name has no value or if the value cannot be coerced to the requested type.
- Use`opt`*Type*`()`to retrieve an optional value. This returns a system- or user-supplied default if the requested name has no value or if the value cannot be coerced to the requested type.

**Warning:** this class represents null in two incompatible ways: the standard Java`null`reference, and the sentinel value [org.json.JSONObject#NULL](../org/json/JSONObject.md). In particular, calling`put(name, null)`removes the named entry from the object but`put(name, JSONObject.NULL)`stores an entry whose value is`JSONObject.NULL`.

Instances of this class are not thread safe. Although this class is nonfinal, it was not designed for inheritance and should not be subclassed. In particular, self-use by overrideable methods is not specified. See*Effective Java, 3rd edition*Item 19, "Design and Document for inheritance or else prohibit it" for further information.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [JSONObject](../org/json/JSONObject.md))`()` Creates a`JSONObject`with no name/value mappings. |
| [JSONObject](../org/json/JSONObject.md))`(`json:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Creates a new`JSONObject`with name/value mappings from the JSON string. |
| [JSONObject](../org/json/JSONObject.md))`(`copyFrom:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?,` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?>`)` Creates a new`JSONObject`by copying all name/value mappings from the given map. |
| [JSONObject](../org/json/JSONObject.md))`(`copyFrom:` ` [JSONObject](../org/json/JSONObject.md)`, `names:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Creates a new`JSONObject`by copying mappings for the listed names from the given object. |
| [JSONObject](../org/json/JSONObject.md))`(`readFrom:` ` [JSONTokener](../org/json/JSONTokener.md)`)` Creates a new`JSONObject`with name/value mappings from the next object in the tokener. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [JSONObject](../org/json/JSONObject.md) | [accumulate](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Appends`value`to the array already mapped to`name`. |
| open [JSONObject](../org/json/JSONObject.md) | [append](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Appends values to the array mapped to`name`. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [get](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the value mapped by`name`, or throws if no such mapping exists. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBoolean](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the value mapped by`name`if it exists and is a boolean or can be coerced to a boolean, or throws otherwise. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the value mapped by`name`if it exists and is a double or can be coerced to a double, or throws otherwise. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the value mapped by`name`if it exists and is an int or can be coerced to an int, or throws otherwise. |
| --- | --- |
| open [JSONArray](../org/json/JSONArray.md) | [getJSONArray](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the value mapped by`name`if it exists and is a`JSONArray`, or throws otherwise. |
| open [JSONObject](../org/json/JSONObject.md) | [getJSONObject](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the value mapped by`name`if it exists and is a`JSONObject`, or throws otherwise. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the value mapped by`name`if it exists and is a long or can be coerced to a long, or throws otherwise. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getString](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the value mapped by`name`if it exists, coercing it if necessary, or throws if no such mapping exists. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [has](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns true if this object has a mapping for`name`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNull](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns true if this object has no mapping for`name`or if it has a mapping whose value is [NULL](../org/json/JSONObject.md). |
| --- | --- |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [keys](../org/json/JSONObject.md))`()` Returns an iterator of the`String`names in this object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [length](../org/json/JSONObject.md))`()` Returns the number of name/value mappings in this object. |
| open [JSONArray](../org/json/JSONArray.md)? | [names](../org/json/JSONObject.md))`()` Returns an array containing the string names in this object. |
| --- | --- |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [numberToString](../org/json/JSONObject.md))`(`number:` ` [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)`)` Encodes the number as a JSON string. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | [opt](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns the value mapped by`name`, or null if no such mapping exists. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [optBoolean](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns the value mapped by`name`if it exists and is a boolean or can be coerced to a boolean, or false otherwise. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [optBoolean](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `fallback:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns the value mapped by`name`if it exists and is a boolean or can be coerced to a boolean, or`fallback`otherwise. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [optDouble](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns the value mapped by`name`if it exists and is a double or can be coerced to a double, or`NaN`otherwise. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [optDouble](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `fallback:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns the value mapped by`name`if it exists and is a double or can be coerced to a double, or`fallback`otherwise. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [optInt](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns the value mapped by`name`if it exists and is an int or can be coerced to an int, or 0 otherwise. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [optInt](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `fallback:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value mapped by`name`if it exists and is an int or can be coerced to an int, or`fallback`otherwise. |
| open [JSONArray](../org/json/JSONArray.md)? | [optJSONArray](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns the value mapped by`name`if it exists and is a`JSONArray`, or null otherwise. |
| --- | --- |
| open [JSONObject](../org/json/JSONObject.md)? | [optJSONObject](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns the value mapped by`name`if it exists and is a`JSONObject`, or null otherwise. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [optLong](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns the value mapped by`name`if it exists and is a long or can be coerced to a long, or 0 otherwise. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [optLong](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `fallback:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the value mapped by`name`if it exists and is a long or can be coerced to a long, or`fallback`otherwise. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [optString](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns the value mapped by`name`if it exists, coercing it if necessary, or the empty string if no such mapping exists. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [optString](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `fallback:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the value mapped by`name`if it exists, coercing it if necessary, or`fallback`if no such mapping exists. |
| open [JSONObject](../org/json/JSONObject.md) | [put](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Maps`name`to`value`, clobbering any existing name/value mapping with the same name. |
| --- | --- |
| open [JSONObject](../org/json/JSONObject.md) | [put](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Maps`name`to`value`, clobbering any existing name/value mapping with the same name. |
| open [JSONObject](../org/json/JSONObject.md) | [put](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Maps`name`to`value`, clobbering any existing name/value mapping with the same name. |
| open [JSONObject](../org/json/JSONObject.md) | [put](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Maps`name`to`value`, clobbering any existing name/value mapping with the same name. |
| --- | --- |
| open [JSONObject](../org/json/JSONObject.md) | [put](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Maps`name`to`value`, clobbering any existing name/value mapping with the same name. |
| open [JSONObject](../org/json/JSONObject.md) | [putOpt](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Equivalent to`put(name, value)`when both parameters are non-null; does nothing otherwise. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [quote](../org/json/JSONObject.md))`(`data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Encodes`data`as a JSON string. |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | [remove](../org/json/JSONObject.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Removes the named mapping if it exists; does nothing otherwise. |
| open [JSONArray](../org/json/JSONArray.md)? | [toJSONArray](../org/json/JSONObject.md))`(`names:` ` [JSONArray](../org/json/JSONArray.md)?`)` Returns an array with the values corresponding to`names`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../org/json/JSONObject.md))`()` Encodes this object as a compact JSON string, such as: ```kotlin {"query":"Pizza","locations":[94043,90210]} ``` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../org/json/JSONObject.md))`(`indentSpaces:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Encodes this object as a human readable JSON string for debugging, such as: ```kotlin { "query": "Pizza", "locations": [ 94043, 90210 ] } ``` <br /> |
| openstatic [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | [wrap](../org/json/JSONObject.md))`(`o:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Wraps the given object if necessary. |

| Properties ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [NULL](../org/json/JSONObject.md) A sentinel value used to explicitly define a name with no value. |

## Public constructors

### JSONObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JSONObject()
```

Creates a`JSONObject`with no name/value mappings. 

### JSONObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JSONObject(json: String)
```

Creates a new`JSONObject`with name/value mappings from the JSON string.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------|
| `json` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a JSON-encoded string containing an object. |

| Exceptions ||
|--------------------------|----------------------------------------------------|
| `org.json.JSONException` | if the parse fails or doesn't yield a`JSONObject`. |

### JSONObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JSONObject(copyFrom: MutableMap<Any?, Any?>)
```

Creates a new`JSONObject`by copying all name/value mappings from the given map.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `copyFrom` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?\>:a map whose keys are of type [String](../java/lang/String.md) and whose values are of supported types. |

| Exceptions ||
|----------------------------------|------------------------------------|
| `java.lang.NullPointerException` | if any of the map's keys are null. |

### JSONObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JSONObject(
    copyFrom: JSONObject, 
    names: Array<String!>)
```

Creates a new`JSONObject`by copying mappings for the listed names from the given object. Names that aren't present in`copyFrom`will be skipped. 

### JSONObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JSONObject(readFrom: JSONTokener)
```

Creates a new`JSONObject`with name/value mappings from the next object in the tokener.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `readFrom` | [JSONTokener](../org/json/JSONTokener.md):a tokener whose nextValue() method will yield a`JSONObject`. |

| Exceptions ||
|--------------------------|----------------------------------------------------|
| `org.json.JSONException` | if the parse fails or doesn't yield a`JSONObject`. |

## Public methods

### accumulate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun accumulate(
    name: String, 
    value: Any?
): JSONObject
```

Appends`value`to the array already mapped to`name`. If this object has no mapping for`name`, this inserts a new mapping. If the mapping exists but its value is not an array, the existing and new values are inserted in order into a new array which is itself mapped to`name`. In aggregate, this allows values to be added to a mapping one at a time.

Note that [append(java.lang.String,java.lang.Object)](../org/json/JSONObject.md))provides better semantics. In particular, the mapping for`name`will**always** be a [JSONArray](../org/json/JSONArray.md). Using`accumulate`will result in either a [JSONArray](../org/json/JSONArray.md) or a mapping whose type is the type of`value`depending on the number of calls to it.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:a [JSONObject](../org/json/JSONObject.md), [JSONArray](../org/json/JSONArray.md), String, Boolean, Integer, Long, Double, [NULL](../org/json/JSONObject.md) or null. May not be [NaNs](../java/lang/Double.md))or [infinities](../java/lang/Double.md)). |

### append

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun append(
    name: String, 
    value: Any?
): JSONObject
```

Appends values to the array mapped to`name`. A new [JSONArray](../org/json/JSONArray.md) mapping for`name`will be inserted if no mapping exists. If the existing mapping for`name`is not a [JSONArray](../org/json/JSONArray.md), a [JSONException](../org/json/JSONException.md) will be thrown.

| Exceptions ||
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.json.JSONException` | if`name`is`null`or if the mapping for`name`is non-null and is not a [JSONArray](../org/json/JSONArray.md). |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(name: String): Any
```

Returns the value mapped by`name`, or throws if no such mapping exists.

| Exceptions ||
|--------------------------|----------------------------|
| `org.json.JSONException` | if no such mapping exists. |

### getBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBoolean(name: String): Boolean
```

Returns the value mapped by`name`if it exists and is a boolean or can be coerced to a boolean, or throws otherwise.

| Exceptions ||
|--------------------------|-----------------------------------------------------------------|
| `org.json.JSONException` | if the mapping doesn't exist or cannot be coerced to a boolean. |

### getDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDouble(name: String): Double
```

Returns the value mapped by`name`if it exists and is a double or can be coerced to a double, or throws otherwise.

| Exceptions ||
|--------------------------|----------------------------------------------------------------|
| `org.json.JSONException` | if the mapping doesn't exist or cannot be coerced to a double. |

### getInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInt(name: String): Int
```

Returns the value mapped by`name`if it exists and is an int or can be coerced to an int, or throws otherwise.

| Exceptions ||
|--------------------------|--------------------------------------------------------------|
| `org.json.JSONException` | if the mapping doesn't exist or cannot be coerced to an int. |

### getJSONArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getJSONArray(name: String): JSONArray
```

Returns the value mapped by`name`if it exists and is a`JSONArray`, or throws otherwise.

| Exceptions ||
|--------------------------|------------------------------------------------------|
| `org.json.JSONException` | if the mapping doesn't exist or is not a`JSONArray`. |

### getJSONObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getJSONObject(name: String): JSONObject
```

Returns the value mapped by`name`if it exists and is a`JSONObject`, or throws otherwise.

| Exceptions ||
|--------------------------|-------------------------------------------------------|
| `org.json.JSONException` | if the mapping doesn't exist or is not a`JSONObject`. |

### getLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLong(name: String): Long
```

Returns the value mapped by`name`if it exists and is a long or can be coerced to a long, or throws otherwise. Note that JSON represents numbers as doubles, so this is [lossy](../org/json/JSONObject.md); use strings to transfer numbers via JSON.

| Exceptions ||
|--------------------------|--------------------------------------------------------------|
| `org.json.JSONException` | if the mapping doesn't exist or cannot be coerced to a long. |

### getString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getString(name: String): String
```

Returns the value mapped by`name`if it exists, coercing it if necessary, or throws if no such mapping exists.

| Exceptions ||
|--------------------------|----------------------------|
| `org.json.JSONException` | if no such mapping exists. |

### has

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun has(name: String?): Boolean
```

Returns true if this object has a mapping for`name`. The mapping may be [NULL](../org/json/JSONObject.md). 

### isNull

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isNull(name: String?): Boolean
```

Returns true if this object has no mapping for`name`or if it has a mapping whose value is [NULL](../org/json/JSONObject.md). 

### keys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun keys(): MutableIterator<String!>
```

Returns an iterator of the`String`names in this object. The returned iterator supports [remove](../java/util/Iterator.md)), which will remove the corresponding mapping from this object. If this object is modified after the iterator is returned, the iterator's behavior is undefined. The order of the keys is undefined. 

### length

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun length(): Int
```

Returns the number of name/value mappings in this object. 

### names

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun names(): JSONArray?
```

Returns an array containing the string names in this object. This method returns null if this object contains no mappings. 

### numberToString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun numberToString(number: Number): String
```

Encodes the number as a JSON string.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `number` | [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html):a finite value. May not be [NaNs](../java/lang/Double.md))or [infinities](../java/lang/Double.md)). |

### opt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun opt(name: String?): Any?
```

Returns the value mapped by`name`, or null if no such mapping exists. 

### optBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optBoolean(name: String?): Boolean
```

Returns the value mapped by`name`if it exists and is a boolean or can be coerced to a boolean, or false otherwise. 

### optBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optBoolean(
    name: String?, 
    fallback: Boolean
): Boolean
```

Returns the value mapped by`name`if it exists and is a boolean or can be coerced to a boolean, or`fallback`otherwise. 

### optDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optDouble(name: String?): Double
```

Returns the value mapped by`name`if it exists and is a double or can be coerced to a double, or`NaN`otherwise. 

### optDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optDouble(
    name: String?, 
    fallback: Double
): Double
```

Returns the value mapped by`name`if it exists and is a double or can be coerced to a double, or`fallback`otherwise. 

### optInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optInt(name: String?): Int
```

Returns the value mapped by`name`if it exists and is an int or can be coerced to an int, or 0 otherwise. 

### optInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optInt(
    name: String?, 
    fallback: Int
): Int
```

Returns the value mapped by`name`if it exists and is an int or can be coerced to an int, or`fallback`otherwise. 

### optJSONArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optJSONArray(name: String?): JSONArray?
```

Returns the value mapped by`name`if it exists and is a`JSONArray`, or null otherwise. 

### optJSONObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optJSONObject(name: String?): JSONObject?
```

Returns the value mapped by`name`if it exists and is a`JSONObject`, or null otherwise. 

### optLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optLong(name: String?): Long
```

Returns the value mapped by`name`if it exists and is a long or can be coerced to a long, or 0 otherwise. Note that JSON represents numbers as doubles, so this is [lossy](../org/json/JSONObject.md); use strings to transfer numbers via JSON. 

### optLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optLong(
    name: String?, 
    fallback: Long
): Long
```

Returns the value mapped by`name`if it exists and is a long or can be coerced to a long, or`fallback`otherwise. Note that JSON represents numbers as doubles, so this is [lossy](../org/json/JSONObject.md); use strings to transfer numbers via JSON. 

### optString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optString(name: String?): String
```

Returns the value mapped by`name`if it exists, coercing it if necessary, or the empty string if no such mapping exists. 

### optString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optString(
    name: String?, 
    fallback: String
): String
```

Returns the value mapped by`name`if it exists, coercing it if necessary, or`fallback`if no such mapping exists. 

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    name: String, 
    value: Boolean
): JSONObject
```

Maps`name`to`value`, clobbering any existing name/value mapping with the same name.

| Return ||
|-----------------------------------------------------------------------------------|--------------|
| [JSONObject](../org/json/JSONObject.md) | this object. |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    name: String, 
    value: Double
): JSONObject
```

Maps`name`to`value`, clobbering any existing name/value mapping with the same name.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):a finite value. May not be [NaNs](../java/lang/Double.md))or [infinities](../java/lang/Double.md)). |

| Return ||
|-----------------------------------------------------------------------------------|--------------|
| [JSONObject](../org/json/JSONObject.md) | this object. |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    name: String, 
    value: Int
): JSONObject
```

Maps`name`to`value`, clobbering any existing name/value mapping with the same name.

| Return ||
|-----------------------------------------------------------------------------------|--------------|
| [JSONObject](../org/json/JSONObject.md) | this object. |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    name: String, 
    value: Any?
): JSONObject
```

Maps`name`to`value`, clobbering any existing name/value mapping with the same name. If the value is`null`, any existing mapping for`name`is removed.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:a [JSONObject](../org/json/JSONObject.md), [JSONArray](../org/json/JSONArray.md), String, Boolean, Integer, Long, Double, [NULL](../org/json/JSONObject.md), or`null`. May not be [NaNs](../java/lang/Double.md))or [infinities](../java/lang/Double.md)). |

| Return ||
|-----------------------------------------------------------------------------------|--------------|
| [JSONObject](../org/json/JSONObject.md) | this object. |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    name: String, 
    value: Long
): JSONObject
```

Maps`name`to`value`, clobbering any existing name/value mapping with the same name.

| Return ||
|-----------------------------------------------------------------------------------|--------------|
| [JSONObject](../org/json/JSONObject.md) | this object. |

### putOpt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun putOpt(
    name: String?, 
    value: Any?
): JSONObject
```

Equivalent to`put(name, value)`when both parameters are non-null; does nothing otherwise. 

### quote

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun quote(data: String?): String
```

Encodes`data`as a JSON string. This applies quotes and any necessary character escaping.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:the string to encode. Null will be interpreted as an empty string. |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(name: String?): Any?
```

Removes the named mapping if it exists; does nothing otherwise.

| Return ||
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | the value previously mapped by`name`, or null if there was no such mapping. |

### toJSONArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toJSONArray(names: JSONArray?): JSONArray?
```

Returns an array with the values corresponding to`names`. The array contains null for names that aren't mapped. This method returns null if`names`is either null or empty. 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Encodes this object as a compact JSON string, such as: 

```kotlin
{"query":"Pizza","locations":[94043,90210]}
```

<br />

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(indentSpaces: Int): String
```

Encodes this object as a human readable JSON string for debugging, such as: 

```kotlin
{
      "query": "Pizza",
      "locations": [
          94043,
          90210
      ]
  }
```

<br />

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `indentSpaces` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of spaces to indent for each level of nesting. |

### wrap

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun wrap(o: Any?): Any?
```

Wraps the given object if necessary.

If the object is null or , returns [NULL](../org/json/JSONObject.md). If the object is a`JSONArray`or`JSONObject`, no wrapping is necessary. If the object is`NULL`, no wrapping is necessary. If the object is an array or`Collection`, returns an equivalent`JSONArray`. If the object is a`Map`, returns an equivalent`JSONObject`. If the object is a primitive wrapper type or`String`, returns the object. Otherwise if the object is from a`java`package, returns the result of`toString`. If wrapping fails, returns null.

## Properties

### NULL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NULL: Any
```

A sentinel value used to explicitly define a name with no value. Unlike`null`, names with this value:

- show up in the [names](../org/json/JSONObject.md))array
- show up in the [keys](../org/json/JSONObject.md))iterator
- return`true`for [has(java.lang.String)](../org/json/JSONObject.md))
- do not throw on [get(java.lang.String)](../org/json/JSONObject.md))
- are included in the encoded JSON string.

<br />

This value violates the general contract of [Object.equals](../java/lang/Object.md))by returning true when compared to`null`. Its #toString method returns "null".
