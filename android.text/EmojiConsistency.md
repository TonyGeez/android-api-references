# EmojiConsistency

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EmojiConsistency

Kotlin| [Java](../android/text/EmojiConsistency.md) 
| --- | --- |

```
class EmojiConsistency
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.EmojiConsistency](../android/text/EmojiConsistency.md) |

The set of emoji that should be drawn by the system with the default font for device consistency. This is intended to be used only by applications that do custom emoji rendering using tools like [android.text.style.ReplacementSpan](../android/text/style/ReplacementSpan.md) or custom emoji fonts. An example of how this should be used:

<br />

1. Match emoji for third party custom rendering
2. For each match, check against NonStandardEmoji before displaying custom glyph
3. If in NonStandardEmojiSet, do not display custom glyph (render with android.graphics.Typeface.DEFAULT instead)
4. Otherwise, do custom rendering like normal

<br />

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\> | [getEmojiConsistencySet](../android/text/EmojiConsistency.md))`()` The set of emoji that should be drawn by the system with the default font for device consistency. |

## Public methods

### getEmojiConsistencySet

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getEmojiConsistencySet(): MutableSet<IntArray!>
```

The set of emoji that should be drawn by the system with the default font for device consistency. Apps SHOULD attempt to avoid overwriting system emoji rendering with custom emoji glyphs for these codepoint sequences. Apps that display custom emoji glyphs via matching code may filter against this set. On match, the application SHOULD prefer Typeface.Default instead of a custom glyph Apps that use fonts may use this set to add [android.text.style.TypefaceSpan](../android/text/style/TypefaceSpan.md) for android.graphics.Typeface.DEFAULT for matched codepoint sequences. Codepoint sequences returned MUST match exactly to be considered a match with the exception of Variation Selectors. All codepoint sequences returned MUST be a complete emoji codepoint sequence as defined by unicode.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!> | set of codepoint sequences representing codepoints that should be rendered by the system using the default font. This value cannot be`null`. |
