# UrlQuerySanitizer.ValueSanitizer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ValueSanitizer

Kotlin| [Java](https://developer.android.com/reference/android/net/UrlQuerySanitizer.ValueSanitizer "View this page in Java") 
| --- | --- |

```
interface ValueSanitizer
```

| [android.net.UrlQuerySanitizer.ValueSanitizer](https://developer.android.com/reference/kotlin/android/net/UrlQuerySanitizer.ValueSanitizer#) |

| Known Direct Subclasses [UrlQuerySanitizer.IllegalCharacterValueSanitizer](https://developer.android.com/reference/kotlin/android/net/UrlQuerySanitizer.IllegalCharacterValueSanitizer) |-----------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------| | [UrlQuerySanitizer.IllegalCharacterValueSanitizer](https://developer.android.com/reference/kotlin/android/net/UrlQuerySanitizer.IllegalCharacterValueSanitizer) | Sanitize values based on which characters they contain. | |
| --- | --- | --- | --- | --- | --- | --- |

A functor used to sanitize a single query value.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [sanitize](https://developer.android.com/reference/kotlin/android/net/UrlQuerySanitizer.ValueSanitizer#sanitize(kotlin.String))`(`value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sanitize an unencoded value. |

## Public methods

### sanitize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun sanitize(value: String!): String!
```

Sanitize an unencoded value.

| Parameters ||
|---------|------------------------------------------------------------------------------------|
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the sanitized unencoded value |
