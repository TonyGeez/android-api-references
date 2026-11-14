# MultiAutoCompleteTextView.Tokenizer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Tokenizer

Kotlin| [Java](../android/widget/MultiAutoCompleteTextView.Tokenizer.md) 
| --- | --- |

```
interface Tokenizer
```

| [android.widget.MultiAutoCompleteTextView.Tokenizer](../android/widget/MultiAutoCompleteTextView.Tokenizer.md) |

| Known Direct Subclasses [MultiAutoCompleteTextView.CommaTokenizer](../android/widget/MultiAutoCompleteTextView.CommaTokenizer.md), [Rfc822Tokenizer](../android.text.util/Rfc822Tokenizer.md) |----------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MultiAutoCompleteTextView.CommaTokenizer](../android/widget/MultiAutoCompleteTextView.CommaTokenizer.md) | This simple Tokenizer can be used for lists where the items are separated by a comma and one or more spaces. | | [Rfc822Tokenizer](../android.text.util/Rfc822Tokenizer.md) | This class works as a Tokenizer for MultiAutoCompleteTextView for address list fields, and also provides a method for converting a string of addresses (such as might be typed into such a field) into a series of Rfc822Tokens. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [findTokenEnd](../android/widget/MultiAutoCompleteTextView.Tokenizer.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `cursor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the end of the token (minus trailing punctuation) that begins at offset`cursor`within`text`. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [findTokenStart](../android/widget/MultiAutoCompleteTextView.Tokenizer.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `cursor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the start of the token that ends at offset`cursor`within`text`. |
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [terminateToken](../android/widget/MultiAutoCompleteTextView.Tokenizer.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Returns`text`, modified, if necessary, to ensure that it ends with a token terminator (for example a space or comma). |
| --- | --- |

## Public methods

### findTokenEnd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun findTokenEnd(
    text: CharSequence!, 
    cursor: Int
): Int
```

Returns the end of the token (minus trailing punctuation) that begins at offset`cursor`within`text`. 

### findTokenStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun findTokenStart(
    text: CharSequence!, 
    cursor: Int
): Int
```

Returns the start of the token that ends at offset`cursor`within`text`. 

### terminateToken

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun terminateToken(text: CharSequence!): CharSequence!
```

Returns`text`, modified, if necessary, to ensure that it ends with a token terminator (for example a space or comma).
