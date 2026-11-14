# JSONStringer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JSONStringer

```
open class JSONStringer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [org.json.JSONStringer](../org/json/JSONStringer.md) |

Implements org.json.JSONObject#toString and org.json.JSONArray#toString. Most application developers should use those methods directly and disregard this API. For example: 

```kotlin
JSONObject object = ...
  String json = object.toString();
```

<br />

Stringers only encode well-formed JSON strings. In particular:

- The stringer must have exactly one top-level array or object.
- Lexical scopes must be balanced: every call to [array](../org/json/JSONStringer.md))must have a matching call to [endArray](../org/json/JSONStringer.md))and every call to [object](../org/json/JSONStringer.md))must have a matching call to [endObject](../org/json/JSONStringer.md)).
- Arrays may not contain keys (property names).
- Objects must alternate keys (property names) and values.
- Values are inserted with either literal [value](../org/json/JSONStringer.md))calls, or by nesting arrays or objects.

Calls that would result in a malformed JSON string will fail with a [JSONException](../org/json/JSONException.md).

This class provides no facility for pretty-printing (ie. indenting) output. To encode indented output, use [JSONObject.toString(int)](../org/json/JSONObject.md))or [JSONArray.toString(int)](../org/json/JSONArray.md)).

Some implementations of the API support at most 20 levels of nesting. Attempts to create more than 20 levels of nesting may fail with a [JSONException](../org/json/JSONException.md).

Each stringer may be used to encode a single top level value. Instances of this class are not thread safe. Although this class is nonfinal, it was not designed for inheritance and should not be subclassed. In particular, self-use by overrideable methods is not specified. See*Effective Java*Item 17, "Design and Document or inheritance or else prohibit it" for further information.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------|---|
| [JSONStringer](../org/json/JSONStringer.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [JSONStringer](../org/json/JSONStringer.md)! | [array](../org/json/JSONStringer.md))`()` Begins encoding a new array. |
| open [JSONStringer](../org/json/JSONStringer.md)! | [endArray](../org/json/JSONStringer.md))`()` Ends encoding the current array. |
| open [JSONStringer](../org/json/JSONStringer.md)! | [endObject](../org/json/JSONStringer.md))`()` Ends encoding the current object. |
| --- | --- |
| open [JSONStringer](../org/json/JSONStringer.md)! | [key](../org/json/JSONStringer.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Encodes the key (property name) to this stringer. |
| open [JSONStringer](../org/json/JSONStringer.md)! | [object](../org/json/JSONStringer.md))`()` Begins encoding a new object. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../org/json/JSONStringer.md))`()` Returns the encoded JSON string. |
| --- | --- |
| open [JSONStringer](../org/json/JSONStringer.md)! | [value](../org/json/JSONStringer.md))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Encodes`value`to this stringer. |
| open [JSONStringer](../org/json/JSONStringer.md)! | [value](../org/json/JSONStringer.md))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Encodes`value`to this stringer. |
| open [JSONStringer](../org/json/JSONStringer.md)! | [value](../org/json/JSONStringer.md))`(`value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Encodes`value`. |
| --- | --- |
| open [JSONStringer](../org/json/JSONStringer.md)! | [value](../org/json/JSONStringer.md))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Encodes`value`to this stringer. |

## Public constructors

### JSONStringer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JSONStringer()
```

## Public methods

### array

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun array(): JSONStringer!
```

Begins encoding a new array. Each call to this method must be paired with a call to [endArray](../org/json/JSONStringer.md)).

| Return ||
|----------------------------------------------------------------------------------------|----------------|
| [JSONStringer](../org/json/JSONStringer.md)! | this stringer. |

### endArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun endArray(): JSONStringer!
```

Ends encoding the current array.

| Return ||
|----------------------------------------------------------------------------------------|----------------|
| [JSONStringer](../org/json/JSONStringer.md)! | this stringer. |

### endObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun endObject(): JSONStringer!
```

Ends encoding the current object.

| Return ||
|----------------------------------------------------------------------------------------|----------------|
| [JSONStringer](../org/json/JSONStringer.md)! | this stringer. |

### key

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun key(name: String!): JSONStringer!
```

Encodes the key (property name) to this stringer.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the forthcoming value. May not be null. |

| Return ||
|----------------------------------------------------------------------------------------|----------------|
| [JSONStringer](../org/json/JSONStringer.md)! | this stringer. |

### object

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun object(): JSONStringer!
```

Begins encoding a new object. Each call to this method must be paired with a call to [endObject](../org/json/JSONStringer.md)).

| Return ||
|----------------------------------------------------------------------------------------|----------------|
| [JSONStringer](../org/json/JSONStringer.md)! | this stringer. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns the encoded JSON string.

If invoked with unterminated arrays or unclosed objects, this method's return value is undefined.

**Warning:** although it contradicts the general contract of [Object.toString](../java/lang/Object.md)), this method returns null if the stringer contains no data.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### value

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun value(value: Boolean): JSONStringer!
```

Encodes`value`to this stringer.

| Return ||
|----------------------------------------------------------------------------------------|----------------|
| [JSONStringer](../org/json/JSONStringer.md)! | this stringer. |

### value

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun value(value: Double): JSONStringer!
```

Encodes`value`to this stringer.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):a finite value. May not be [NaNs](../java/lang/Double.md))or [infinities](../java/lang/Double.md)). |

| Return ||
|----------------------------------------------------------------------------------------|----------------|
| [JSONStringer](../org/json/JSONStringer.md)! | this stringer. |

### value

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun value(value: Any!): JSONStringer!
```

Encodes`value`.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:a [JSONObject](../org/json/JSONObject.md), [JSONArray](../org/json/JSONArray.md), String, Boolean, Integer, Long, Double or null. May not be [NaNs](../java/lang/Double.md))or [infinities](../java/lang/Double.md)). |

| Return ||
|----------------------------------------------------------------------------------------|----------------|
| [JSONStringer](../org/json/JSONStringer.md)! | this stringer. |

### value

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun value(value: Long): JSONStringer!
```

Encodes`value`to this stringer.

| Return ||
|----------------------------------------------------------------------------------------|----------------|
| [JSONStringer](../org/json/JSONStringer.md)! | this stringer. |
