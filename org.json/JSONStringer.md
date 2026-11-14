# JSONStringer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JSONStringer

```
open class JSONStringer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [org.json.JSONStringer](JSONStringer.md) |

Implements org.json.JSONObject#toString and org.json.JSONArray#toString. Most application developers should use those methods directly and disregard this API. For example: 

```kotlin
JSONObject object = ...
  String json = object.toString();
```

<br />

Stringers only encode well-formed JSON strings. In particular:

- The stringer must have exactly one top-level array or object.
- Lexical scopes must be balanced: every call to [array](JSONStringer.md))must have a matching call to [endArray](JSONStringer.md))and every call to [object](JSONStringer.md))must have a matching call to [endObject](JSONStringer.md)).
- Arrays may not contain keys (property names).
- Objects must alternate keys (property names) and values.
- Values are inserted with either literal [value](JSONStringer.md))calls, or by nesting arrays or objects.

Calls that would result in a malformed JSON string will fail with a [JSONException](JSONException.md).

This class provides no facility for pretty-printing (ie. indenting) output. To encode indented output, use [JSONObject.toString(int)](JSONObject.md))or [JSONArray.toString(int)](JSONArray.md)).

Some implementations of the API support at most 20 levels of nesting. Attempts to create more than 20 levels of nesting may fail with a [JSONException](JSONException.md).

Each stringer may be used to encode a single top level value. Instances of this class are not thread safe. Although this class is nonfinal, it was not designed for inheritance and should not be subclassed. In particular, self-use by overrideable methods is not specified. See*Effective Java*Item 17, "Design and Document or inheritance or else prohibit it" for further information.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------|---|
| [JSONStringer](JSONStringer.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [JSONStringer](JSONStringer.md)! | [array](JSONStringer.md))`()` Begins encoding a new array. |
| open [JSONStringer](JSONStringer.md)! | [endArray](JSONStringer.md))`()` Ends encoding the current array. |
| open [JSONStringer](JSONStringer.md)! | [endObject](JSONStringer.md))`()` Ends encoding the current object. |
| --- | --- |
| open [JSONStringer](JSONStringer.md)! | [key](JSONStringer.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Encodes the key (property name) to this stringer. |
| open [JSONStringer](JSONStringer.md)! | [object](JSONStringer.md))`()` Begins encoding a new object. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](JSONStringer.md))`()` Returns the encoded JSON string. |
| --- | --- |
| open [JSONStringer](JSONStringer.md)! | [value](JSONStringer.md))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Encodes`value`to this stringer. |
| open [JSONStringer](JSONStringer.md)! | [value](JSONStringer.md))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Encodes`value`to this stringer. |
| open [JSONStringer](JSONStringer.md)! | [value](JSONStringer.md))`(`value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Encodes`value`. |
| --- | --- |
| open [JSONStringer](JSONStringer.md)! | [value](JSONStringer.md))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Encodes`value`to this stringer. |

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

Begins encoding a new array. Each call to this method must be paired with a call to [endArray](JSONStringer.md)).

| Return ||
|----------------------------------------------------------------------------------------|----------------|
| [JSONStringer](JSONStringer.md)! | this stringer. |

### endArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun endArray(): JSONStringer!
```

Ends encoding the current array.

| Return ||
|----------------------------------------------------------------------------------------|----------------|
| [JSONStringer](JSONStringer.md)! | this stringer. |

### endObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun endObject(): JSONStringer!
```

Ends encoding the current object.

| Return ||
|----------------------------------------------------------------------------------------|----------------|
| [JSONStringer](JSONStringer.md)! | this stringer. |

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
| [JSONStringer](JSONStringer.md)! | this stringer. |

### object

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun object(): JSONStringer!
```

Begins encoding a new object. Each call to this method must be paired with a call to [endObject](JSONStringer.md)).

| Return ||
|----------------------------------------------------------------------------------------|----------------|
| [JSONStringer](JSONStringer.md)! | this stringer. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns the encoded JSON string.

If invoked with unterminated arrays or unclosed objects, this method's return value is undefined.

**Warning:** although it contradicts the general contract of [Object.toString](../java.lang/Object.md)), this method returns null if the stringer contains no data.

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
| [JSONStringer](JSONStringer.md)! | this stringer. |

### value

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun value(value: Double): JSONStringer!
```

Encodes`value`to this stringer.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):a finite value. May not be [NaNs](../java.lang/Double.md))or [infinities](../java.lang/Double.md)). |

| Return ||
|----------------------------------------------------------------------------------------|----------------|
| [JSONStringer](JSONStringer.md)! | this stringer. |

### value

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun value(value: Any!): JSONStringer!
```

Encodes`value`.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:a [JSONObject](JSONObject.md), [JSONArray](JSONArray.md), String, Boolean, Integer, Long, Double or null. May not be [NaNs](../java.lang/Double.md))or [infinities](../java.lang/Double.md)). |

| Return ||
|----------------------------------------------------------------------------------------|----------------|
| [JSONStringer](JSONStringer.md)! | this stringer. |

### value

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun value(value: Long): JSONStringer!
```

Encodes`value`to this stringer.

| Return ||
|----------------------------------------------------------------------------------------|----------------|
| [JSONStringer](JSONStringer.md)! | this stringer. |
