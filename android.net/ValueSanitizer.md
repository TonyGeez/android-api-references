# UrlQuerySanitizer.ValueSanitizer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ValueSanitizer

Kotlin| [Java](../android/net/UrlQuerySanitizer.ValueSanitizer.md) 
| --- | --- |

```
interface ValueSanitizer
```

| [android.net.UrlQuerySanitizer.ValueSanitizer](../android/net/UrlQuerySanitizer.ValueSanitizer.md) |

| Known Direct Subclasses [UrlQuerySanitizer.IllegalCharacterValueSanitizer](../android/net/UrlQuerySanitizer.IllegalCharacterValueSanitizer.md) |-----------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------| | [UrlQuerySanitizer.IllegalCharacterValueSanitizer](../android/net/UrlQuerySanitizer.IllegalCharacterValueSanitizer.md) | Sanitize values based on which characters they contain. | |
| --- | --- | --- | --- | --- | --- | --- |

A functor used to sanitize a single query value.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [sanitize](../android/net/UrlQuerySanitizer.ValueSanitizer.md))`(`value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sanitize an unencoded value. |

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
