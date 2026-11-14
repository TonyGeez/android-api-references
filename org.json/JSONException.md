# JSONException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JSONException

```
open class JSONException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||
| | | ↳ | [org.json.JSONException](../org/json/JSONException.md) |
| --- | --- | --- | --- |

Thrown to indicate a problem with the JSON API. Such problems include:

- Attempts to parse or construct malformed documents
- Use of null as a name
- Use of numeric types not available to JSON, such as [NaNs](../java/lang/Double.md))or [infinities](../java/lang/Double.md)).
- Lookups using an out of range index or nonexistent name
- Type mismatches on lookups

<br />

Although this is a checked exception, it is rarely recoverable. Most callers should simply wrap this exception in an unchecked exception and rethrow: 

```kotlin
public JSONArray toJSONObject() {
      try {
          JSONObject result = new JSONObject();
          ...
      } catch (JSONException e) {
          throw new RuntimeException(e);
      }
  }
```

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [JSONException](../org/json/JSONException.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [JSONException](../org/json/JSONException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |
| [JSONException](../org/json/JSONException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |

## Public constructors

### JSONException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JSONException(s: String!)
```  

### JSONException

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JSONException(
    message: String!, 
    cause: Throwable!)
```  

### JSONException

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JSONException(cause: Throwable!)
```
