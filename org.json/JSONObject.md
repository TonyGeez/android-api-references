# JSONObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JSONObject

```
open class JSONObject
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [org.json.JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#) |

A modifiable set of name/value mappings. Names are unique, non-null strings. Values may be any mix of [JSONObjects](https://developer.android.com/reference/kotlin/org/json/JSONObject#), [JSONArrays](https://developer.android.com/reference/kotlin/org/json/JSONArray), Strings, Booleans, Integers, Longs, Doubles or [NULL](https://developer.android.com/reference/kotlin/org/json/JSONObject#NULL:kotlin.Any). Values may not be`null`, [NaNs](https://developer.android.com/reference/kotlin/java/lang/Double.html#isNaN()), [infinities](https://developer.android.com/reference/kotlin/java/lang/Double.html#isInfinite()), or of any type not listed here.

This class can coerce values to another type when requested.

- When the requested type is a boolean, strings will be coerced using a case-insensitive comparison to "true" and "false".
- When the requested type is a double, other [Number](https://developer.android.com/reference/kotlin/java/lang/Number.html#) types will be coerced using [doubleValue](https://developer.android.com/reference/kotlin/java/lang/Number.html#doubleValue()). Strings that can be coerced using [Double.valueOf(String)](https://developer.android.com/reference/kotlin/java/lang/Double.html#valueOf(kotlin.String))will be.
- When the requested type is an int, other [Number](https://developer.android.com/reference/kotlin/java/lang/Number.html#) types will be coerced using [intValue](https://developer.android.com/reference/kotlin/java/lang/Number.html#intValue()). Strings that can be coerced using [Double.valueOf(String)](https://developer.android.com/reference/kotlin/java/lang/Double.html#valueOf(kotlin.String))will be, and then cast to int.
- When the requested type is a long, other [Number](https://developer.android.com/reference/kotlin/java/lang/Number.html#) types will be coerced using [longValue](https://developer.android.com/reference/kotlin/java/lang/Number.html#longValue()). Strings that can be coerced using [Double.valueOf(String)](https://developer.android.com/reference/kotlin/java/lang/Double.html#valueOf(kotlin.String))will be, and then cast to long. This two-step conversion is lossy for very large values. For example, the string "9223372036854775806" yields the long 9223372036854775807.
- When the requested type is a String, other non-null values will be coerced using [String.valueOf(Object)](https://developer.android.com/reference/kotlin/java/lang/String.html#valueOf(kotlin.Any)). Although null cannot be coerced, the sentinel value [JSONObject.NULL](https://developer.android.com/reference/kotlin/org/json/JSONObject#NULL:kotlin.Any) is coerced to the string "null".

This class can look up both mandatory and optional values:

- Use`get`*Type*`()`to retrieve a mandatory value. This fails with a`JSONException`if the requested name has no value or if the value cannot be coerced to the requested type.
- Use`opt`*Type*`()`to retrieve an optional value. This returns a system- or user-supplied default if the requested name has no value or if the value cannot be coerced to the requested type.

**Warning:** this class represents null in two incompatible ways: the standard Java`null`reference, and the sentinel value [org.json.JSONObject#NULL](https://developer.android.com/reference/kotlin/org/json/JSONObject#NULL:kotlin.Any). In particular, calling`put(name, null)`removes the named entry from the object but`put(name, JSONObject.NULL)`stores an entry whose value is`JSONObject.NULL`.

Instances of this class are not thread safe. Although this class is nonfinal, it was not designed for inheritance and should not be subclassed. In particular, self-use by overrideable methods is not specified. See*Effective Java, 3rd edition*Item 19, "Design and Document for inheritance or else prohibit it" for further information.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#JSONObject())`()` Creates a`JSONObject`with no name/value mappings. |
| [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#JSONObject(kotlin.String))`(`json:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Creates a new`JSONObject`with name/value mappings from the JSON string. |
| [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#JSONObject(kotlin.collections.MutableMap))`(`copyFrom:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?,` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?>`)` Creates a new`JSONObject`by copying all name/value mappings from the given map. |
| [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#JSONObject(org.json.JSONObject,%20kotlin.Array))`(`copyFrom:` ` [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#)`, `names:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Creates a new`JSONObject`by copying mappings for the listed names from the given object. |
| [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#JSONObject(org.json.JSONTokener))`(`readFrom:` ` [JSONTokener](https://developer.android.com/reference/kotlin/org/json/JSONTokener)`)` Creates a new`JSONObject`with name/value mappings from the next object in the tokener. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#) | [accumulate](https://developer.android.com/reference/kotlin/org/json/JSONObject#accumulate(kotlin.String,%20kotlin.Any))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Appends`value`to the array already mapped to`name`. |
| open [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#) | [append](https://developer.android.com/reference/kotlin/org/json/JSONObject#append(kotlin.String,%20kotlin.Any))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Appends values to the array mapped to`name`. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [get](https://developer.android.com/reference/kotlin/org/json/JSONObject#get(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the value mapped by`name`, or throws if no such mapping exists. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBoolean](https://developer.android.com/reference/kotlin/org/json/JSONObject#getBoolean(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the value mapped by`name`if it exists and is a boolean or can be coerced to a boolean, or throws otherwise. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](https://developer.android.com/reference/kotlin/org/json/JSONObject#getDouble(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the value mapped by`name`if it exists and is a double or can be coerced to a double, or throws otherwise. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](https://developer.android.com/reference/kotlin/org/json/JSONObject#getInt(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the value mapped by`name`if it exists and is an int or can be coerced to an int, or throws otherwise. |
| --- | --- |
| open [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray) | [getJSONArray](https://developer.android.com/reference/kotlin/org/json/JSONObject#getJSONArray(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the value mapped by`name`if it exists and is a`JSONArray`, or throws otherwise. |
| open [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#) | [getJSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#getJSONObject(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the value mapped by`name`if it exists and is a`JSONObject`, or throws otherwise. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](https://developer.android.com/reference/kotlin/org/json/JSONObject#getLong(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the value mapped by`name`if it exists and is a long or can be coerced to a long, or throws otherwise. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getString](https://developer.android.com/reference/kotlin/org/json/JSONObject#getString(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the value mapped by`name`if it exists, coercing it if necessary, or throws if no such mapping exists. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [has](https://developer.android.com/reference/kotlin/org/json/JSONObject#has(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns true if this object has a mapping for`name`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNull](https://developer.android.com/reference/kotlin/org/json/JSONObject#isNull(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns true if this object has no mapping for`name`or if it has a mapping whose value is [NULL](https://developer.android.com/reference/kotlin/org/json/JSONObject#NULL:kotlin.Any). |
| --- | --- |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [keys](https://developer.android.com/reference/kotlin/org/json/JSONObject#keys())`()` Returns an iterator of the`String`names in this object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [length](https://developer.android.com/reference/kotlin/org/json/JSONObject#length())`()` Returns the number of name/value mappings in this object. |
| open [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray)? | [names](https://developer.android.com/reference/kotlin/org/json/JSONObject#names())`()` Returns an array containing the string names in this object. |
| --- | --- |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [numberToString](https://developer.android.com/reference/kotlin/org/json/JSONObject#numberToString(kotlin.Number))`(`number:` ` [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)`)` Encodes the number as a JSON string. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | [opt](https://developer.android.com/reference/kotlin/org/json/JSONObject#opt(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns the value mapped by`name`, or null if no such mapping exists. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [optBoolean](https://developer.android.com/reference/kotlin/org/json/JSONObject#optBoolean(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns the value mapped by`name`if it exists and is a boolean or can be coerced to a boolean, or false otherwise. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [optBoolean](https://developer.android.com/reference/kotlin/org/json/JSONObject#optBoolean(kotlin.String,%20kotlin.Boolean))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `fallback:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns the value mapped by`name`if it exists and is a boolean or can be coerced to a boolean, or`fallback`otherwise. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [optDouble](https://developer.android.com/reference/kotlin/org/json/JSONObject#optDouble(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns the value mapped by`name`if it exists and is a double or can be coerced to a double, or`NaN`otherwise. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [optDouble](https://developer.android.com/reference/kotlin/org/json/JSONObject#optDouble(kotlin.String,%20kotlin.Double))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `fallback:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Returns the value mapped by`name`if it exists and is a double or can be coerced to a double, or`fallback`otherwise. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [optInt](https://developer.android.com/reference/kotlin/org/json/JSONObject#optInt(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns the value mapped by`name`if it exists and is an int or can be coerced to an int, or 0 otherwise. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [optInt](https://developer.android.com/reference/kotlin/org/json/JSONObject#optInt(kotlin.String,%20kotlin.Int))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `fallback:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value mapped by`name`if it exists and is an int or can be coerced to an int, or`fallback`otherwise. |
| open [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray)? | [optJSONArray](https://developer.android.com/reference/kotlin/org/json/JSONObject#optJSONArray(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns the value mapped by`name`if it exists and is a`JSONArray`, or null otherwise. |
| --- | --- |
| open [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#)? | [optJSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#optJSONObject(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns the value mapped by`name`if it exists and is a`JSONObject`, or null otherwise. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [optLong](https://developer.android.com/reference/kotlin/org/json/JSONObject#optLong(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns the value mapped by`name`if it exists and is a long or can be coerced to a long, or 0 otherwise. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [optLong](https://developer.android.com/reference/kotlin/org/json/JSONObject#optLong(kotlin.String,%20kotlin.Long))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `fallback:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the value mapped by`name`if it exists and is a long or can be coerced to a long, or`fallback`otherwise. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [optString](https://developer.android.com/reference/kotlin/org/json/JSONObject#optString(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns the value mapped by`name`if it exists, coercing it if necessary, or the empty string if no such mapping exists. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [optString](https://developer.android.com/reference/kotlin/org/json/JSONObject#optString(kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `fallback:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the value mapped by`name`if it exists, coercing it if necessary, or`fallback`if no such mapping exists. |
| open [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#) | [put](https://developer.android.com/reference/kotlin/org/json/JSONObject#put(kotlin.String,%20kotlin.Boolean))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Maps`name`to`value`, clobbering any existing name/value mapping with the same name. |
| --- | --- |
| open [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#) | [put](https://developer.android.com/reference/kotlin/org/json/JSONObject#put(kotlin.String,%20kotlin.Double))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Maps`name`to`value`, clobbering any existing name/value mapping with the same name. |
| open [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#) | [put](https://developer.android.com/reference/kotlin/org/json/JSONObject#put(kotlin.String,%20kotlin.Int))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Maps`name`to`value`, clobbering any existing name/value mapping with the same name. |
| open [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#) | [put](https://developer.android.com/reference/kotlin/org/json/JSONObject#put(kotlin.String,%20kotlin.Any))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Maps`name`to`value`, clobbering any existing name/value mapping with the same name. |
| --- | --- |
| open [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#) | [put](https://developer.android.com/reference/kotlin/org/json/JSONObject#put(kotlin.String,%20kotlin.Long))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Maps`name`to`value`, clobbering any existing name/value mapping with the same name. |
| open [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#) | [putOpt](https://developer.android.com/reference/kotlin/org/json/JSONObject#putOpt(kotlin.String,%20kotlin.Any))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Equivalent to`put(name, value)`when both parameters are non-null; does nothing otherwise. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [quote](https://developer.android.com/reference/kotlin/org/json/JSONObject#quote(kotlin.String))`(`data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Encodes`data`as a JSON string. |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | [remove](https://developer.android.com/reference/kotlin/org/json/JSONObject#remove(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Removes the named mapping if it exists; does nothing otherwise. |
| open [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray)? | [toJSONArray](https://developer.android.com/reference/kotlin/org/json/JSONObject#toJSONArray(org.json.JSONArray))`(`names:` ` [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray)?`)` Returns an array with the values corresponding to`names`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/org/json/JSONObject#toString())`()` Encodes this object as a compact JSON string, such as: ```kotlin {"query":"Pizza","locations":[94043,90210]} ``` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/org/json/JSONObject#toString(kotlin.Int))`(`indentSpaces:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Encodes this object as a human readable JSON string for debugging, such as: ```kotlin { "query": "Pizza", "locations": [ 94043, 90210 ] } ``` <br /> |
| openstatic [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | [wrap](https://developer.android.com/reference/kotlin/org/json/JSONObject#wrap(kotlin.Any))`(`o:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Wraps the given object if necessary. |

| Properties ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [NULL](https://developer.android.com/reference/kotlin/org/json/JSONObject#NULL:kotlin.Any) A sentinel value used to explicitly define a name with no value. |

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
| `copyFrom` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?\>:a map whose keys are of type [String](https://developer.android.com/reference/kotlin/java/lang/String.html#) and whose values are of supported types. |

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
| `readFrom` | [JSONTokener](https://developer.android.com/reference/kotlin/org/json/JSONTokener):a tokener whose nextValue() method will yield a`JSONObject`. |

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

Note that [append(java.lang.String,java.lang.Object)](https://developer.android.com/reference/kotlin/org/json/JSONObject#append(kotlin.String,%20kotlin.Any))provides better semantics. In particular, the mapping for`name`will**always** be a [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray). Using`accumulate`will result in either a [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray) or a mapping whose type is the type of`value`depending on the number of calls to it.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:a [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#), [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray), String, Boolean, Integer, Long, Double, [NULL](https://developer.android.com/reference/kotlin/org/json/JSONObject#NULL:kotlin.Any) or null. May not be [NaNs](https://developer.android.com/reference/kotlin/java/lang/Double.html#isNaN())or [infinities](https://developer.android.com/reference/kotlin/java/lang/Double.html#isInfinite()). |

### append

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun append(
    name: String, 
    value: Any?
): JSONObject
```

Appends values to the array mapped to`name`. A new [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray) mapping for`name`will be inserted if no mapping exists. If the existing mapping for`name`is not a [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray), a [JSONException](https://developer.android.com/reference/kotlin/org/json/JSONException) will be thrown.

| Exceptions ||
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.json.JSONException` | if`name`is`null`or if the mapping for`name`is non-null and is not a [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray). |

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

Returns the value mapped by`name`if it exists and is a long or can be coerced to a long, or throws otherwise. Note that JSON represents numbers as doubles, so this is [lossy](https://developer.android.com/reference/kotlin/org/json/JSONObject#lossy); use strings to transfer numbers via JSON.

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

Returns true if this object has a mapping for`name`. The mapping may be [NULL](https://developer.android.com/reference/kotlin/org/json/JSONObject#NULL:kotlin.Any). 

### isNull

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isNull(name: String?): Boolean
```

Returns true if this object has no mapping for`name`or if it has a mapping whose value is [NULL](https://developer.android.com/reference/kotlin/org/json/JSONObject#NULL:kotlin.Any). 

### keys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun keys(): MutableIterator<String!>
```

Returns an iterator of the`String`names in this object. The returned iterator supports [remove](https://developer.android.com/reference/kotlin/java/util/Iterator.html#remove()), which will remove the corresponding mapping from this object. If this object is modified after the iterator is returned, the iterator's behavior is undefined. The order of the keys is undefined. 

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
| `number` | [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html):a finite value. May not be [NaNs](https://developer.android.com/reference/kotlin/java/lang/Double.html#isNaN())or [infinities](https://developer.android.com/reference/kotlin/java/lang/Double.html#isInfinite()). |

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

Returns the value mapped by`name`if it exists and is a long or can be coerced to a long, or 0 otherwise. Note that JSON represents numbers as doubles, so this is [lossy](https://developer.android.com/reference/kotlin/org/json/JSONObject#lossy); use strings to transfer numbers via JSON. 

### optLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun optLong(
    name: String?, 
    fallback: Long
): Long
```

Returns the value mapped by`name`if it exists and is a long or can be coerced to a long, or`fallback`otherwise. Note that JSON represents numbers as doubles, so this is [lossy](https://developer.android.com/reference/kotlin/org/json/JSONObject#lossy); use strings to transfer numbers via JSON. 

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
| [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#) | this object. |

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
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):a finite value. May not be [NaNs](https://developer.android.com/reference/kotlin/java/lang/Double.html#isNaN())or [infinities](https://developer.android.com/reference/kotlin/java/lang/Double.html#isInfinite()). |

| Return ||
|-----------------------------------------------------------------------------------|--------------|
| [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#) | this object. |

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
| [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#) | this object. |

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
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:a [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#), [JSONArray](https://developer.android.com/reference/kotlin/org/json/JSONArray), String, Boolean, Integer, Long, Double, [NULL](https://developer.android.com/reference/kotlin/org/json/JSONObject#NULL:kotlin.Any), or`null`. May not be [NaNs](https://developer.android.com/reference/kotlin/java/lang/Double.html#isNaN())or [infinities](https://developer.android.com/reference/kotlin/java/lang/Double.html#isInfinite()). |

| Return ||
|-----------------------------------------------------------------------------------|--------------|
| [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#) | this object. |

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
| [JSONObject](https://developer.android.com/reference/kotlin/org/json/JSONObject#) | this object. |

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

If the object is null or , returns [NULL](https://developer.android.com/reference/kotlin/org/json/JSONObject#NULL:kotlin.Any). If the object is a`JSONArray`or`JSONObject`, no wrapping is necessary. If the object is`NULL`, no wrapping is necessary. If the object is an array or`Collection`, returns an equivalent`JSONArray`. If the object is a`Map`, returns an equivalent`JSONObject`. If the object is a primitive wrapper type or`String`, returns the object. Otherwise if the object is from a`java`package, returns the result of`toString`. If wrapping fails, returns null.

## Properties

### NULL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NULL: Any
```

A sentinel value used to explicitly define a name with no value. Unlike`null`, names with this value:

- show up in the [names](https://developer.android.com/reference/kotlin/org/json/JSONObject#names())array
- show up in the [keys](https://developer.android.com/reference/kotlin/org/json/JSONObject#keys())iterator
- return`true`for [has(java.lang.String)](https://developer.android.com/reference/kotlin/org/json/JSONObject#has(kotlin.String))
- do not throw on [get(java.lang.String)](https://developer.android.com/reference/kotlin/org/json/JSONObject#get(kotlin.String))
- are included in the encoded JSON string.

<br />

This value violates the general contract of [Object.equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any))by returning true when compared to`null`. Its #toString method returns "null".
