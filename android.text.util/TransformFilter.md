# Linkify.TransformFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransformFilter

Kotlin| [Java](https://developer.android.com/reference/android/text/util/Linkify.TransformFilter "View this page in Java") 
| --- | --- |

```
interface TransformFilter
```

| [android.text.util.Linkify.TransformFilter](https://developer.android.com/reference/kotlin/android/text/util/Linkify.TransformFilter#) |

TransformFilter enables client code to have more control over how matched patterns are represented as URLs. For example: when converting a phone number such as (919) 555-1212 into a tel: URL the parentheses, white space, and hyphen need to be removed to produce tel:9195551212.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [transformUrl](https://developer.android.com/reference/kotlin/android/text/util/Linkify.TransformFilter#transformUrl(java.util.regex.Matcher,%20kotlin.String))`(`match:` ` [Matcher](https://developer.android.com/reference/kotlin/java/util/regex/Matcher.html#)!`, `url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Examines the matched text and either passes it through or uses the data in the Matcher state to produce a replacement. |

## Public methods

### transformUrl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun transformUrl(
    match: Matcher!, 
    url: String!
): String!
```

Examines the matched text and either passes it through or uses the data in the Matcher state to produce a replacement.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `match` | [Matcher](https://developer.android.com/reference/kotlin/java/util/regex/Matcher.html#)!:The regex matcher state that found this URL text |
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The text that was matched |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The transformed form of the URL |
