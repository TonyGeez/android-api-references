# Linkify.MatchFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MatchFilter

Kotlin| [Java](../android/text/util/Linkify.MatchFilter.md) 
| --- | --- |

```
interface MatchFilter
```

| [android.text.util.Linkify.MatchFilter](../android/text/util/Linkify.MatchFilter.md) |

MatchFilter enables client code to have more control over what is allowed to match and become a link, and what is not. For example: when matching web URLs you would like things like http://www.example.com to match, as well as just example.com itelf. However, you would not want to match against the domain in support@example.com. So, when matching against a web URL pattern you might also include a MatchFilter that disallows the match if it is immediately preceded by an at-sign (@).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [acceptMatch](../android/text/util/Linkify.MatchFilter.md))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Examines the character span matched by the pattern and determines if the match should be turned into an actionable link. |

## Public methods

### acceptMatch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun acceptMatch(
    s: CharSequence!, 
    start: Int, 
    end: Int
): Boolean
```

Examines the character span matched by the pattern and determines if the match should be turned into an actionable link.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The body of text against which the pattern was matched |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the first character in s that was matched by the pattern - inclusive |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the last character in s that was matched - exclusive |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether this match should be turned into a link |
