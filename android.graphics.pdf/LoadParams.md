# LoadParams

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

# LoadParams

Kotlin| [Java](https://developer.android.com/reference/android/graphics/pdf/LoadParams "View this page in Java") 
| --- | --- |

```
class LoadParams
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.pdf.LoadParams](https://developer.android.com/reference/kotlin/android/graphics/pdf/LoadParams#) |

Represents a set of parameters to load the PDF document.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/graphics/pdf/LoadParams.Builder) Builder for constructing [LoadParams](https://developer.android.com/reference/kotlin/android/graphics/pdf/LoadParams#). |

| Public methods ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPassword](https://developer.android.com/reference/kotlin/android/graphics/pdf/LoadParams#getPassword())`()` Gets the password for the loaded document. |

## Public methods

### getPassword

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getPassword(): String?
```

Gets the password for the loaded document. Returns`null`if not set.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the password for the document. |
