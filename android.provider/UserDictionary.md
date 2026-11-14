# UserDictionary

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UserDictionary

Kotlin| [Java](https://developer.android.com/reference/android/provider/UserDictionary "View this page in Java") 

```
open class UserDictionary
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.provider.UserDictionary](https://developer.android.com/reference/kotlin/android/provider/UserDictionary#) |

A provider of user defined words for input methods to use for predictive text input. Applications and input methods may add words into the dictionary. Words can have associated frequency information and locale information.

**NOTE:**Starting on API 23, the user dictionary is only accessible through IME and spellchecker.

## Summary

| Nested classes ||
|------|--------------------------------------------------------------------------------------------------------------------------------|
| open | [Words](https://developer.android.com/reference/kotlin/android/provider/UserDictionary.Words) Contains the user defined words. |

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [AUTHORITY](https://developer.android.com/reference/kotlin/android/provider/UserDictionary#AUTHORITY:kotlin.String) Authority string for this provider. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------|---|
| [UserDictionary](https://developer.android.com/reference/kotlin/android/provider/UserDictionary#UserDictionary())`()` <br /> |

| Properties ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | [CONTENT_URI](https://developer.android.com/reference/kotlin/android/provider/UserDictionary#CONTENT_URI:android.net.Uri) The content:// style URL for this provider |

## Constants

### AUTHORITY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUTHORITY: String
```

Authority string for this provider. 

 Value: "user_dictionary"

## Public constructors

### UserDictionary

```
UserDictionary()
```

## Properties

### CONTENT_URI

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_URI: Uri!
```

The content:// style URL for this provider
