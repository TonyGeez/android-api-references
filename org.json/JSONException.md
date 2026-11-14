# JSONException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JSONException

```
open class JSONException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [org.json.JSONException](https://developer.android.com/reference/kotlin/org/json/JSONException#) |

Thrown to indicate a problem with the JSON API. Such problems include:

- Attempts to parse or construct malformed documents
- Use of null as a name
- Use of numeric types not available to JSON, such as [NaNs](https://developer.android.com/reference/kotlin/java/lang/Double.html#isNaN())or [infinities](https://developer.android.com/reference/kotlin/java/lang/Double.html#isInfinite()).
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
| [JSONException](https://developer.android.com/reference/kotlin/org/json/JSONException#JSONException(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [JSONException](https://developer.android.com/reference/kotlin/org/json/JSONException#JSONException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |
| [JSONException](https://developer.android.com/reference/kotlin/org/json/JSONException#JSONException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |

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
