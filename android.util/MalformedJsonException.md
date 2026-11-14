# MalformedJsonException

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MalformedJsonException

Kotlin| [Java](https://developer.android.com/reference/android/util/MalformedJsonException "View this page in Java") 
| --- | --- |

```
class MalformedJsonException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.util.MalformedJsonException](https://developer.android.com/reference/kotlin/android/util/MalformedJsonException#) |

Thrown when a reader encounters malformed JSON. Some syntax errors can be ignored by calling [JsonReader.setLenient(boolean)](https://developer.android.com/reference/kotlin/android/util/JsonReader#setLenient(kotlin.Boolean)).

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MalformedJsonException](https://developer.android.com/reference/kotlin/android/util/MalformedJsonException#MalformedJsonException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### MalformedJsonException

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MalformedJsonException(message: String!)
```
