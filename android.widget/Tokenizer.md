# MultiAutoCompleteTextView.Tokenizer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Tokenizer

Kotlin| [Java](https://developer.android.com/reference/android/widget/MultiAutoCompleteTextView.Tokenizer "View this page in Java") 
| --- | --- |

```
interface Tokenizer
```

| [android.widget.MultiAutoCompleteTextView.Tokenizer](https://developer.android.com/reference/kotlin/android/widget/MultiAutoCompleteTextView.Tokenizer#) |

| Known Direct Subclasses [MultiAutoCompleteTextView.CommaTokenizer](https://developer.android.com/reference/kotlin/android/widget/MultiAutoCompleteTextView.CommaTokenizer), [Rfc822Tokenizer](https://developer.android.com/reference/kotlin/android/text/util/Rfc822Tokenizer.html#) |----------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MultiAutoCompleteTextView.CommaTokenizer](https://developer.android.com/reference/kotlin/android/widget/MultiAutoCompleteTextView.CommaTokenizer) | This simple Tokenizer can be used for lists where the items are separated by a comma and one or more spaces. | | [Rfc822Tokenizer](https://developer.android.com/reference/kotlin/android/text/util/Rfc822Tokenizer.html#) | This class works as a Tokenizer for MultiAutoCompleteTextView for address list fields, and also provides a method for converting a string of addresses (such as might be typed into such a field) into a series of Rfc822Tokens. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [findTokenEnd](https://developer.android.com/reference/kotlin/android/widget/MultiAutoCompleteTextView.Tokenizer#findTokenEnd(kotlin.CharSequence,%20kotlin.Int))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `cursor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the end of the token (minus trailing punctuation) that begins at offset`cursor`within`text`. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [findTokenStart](https://developer.android.com/reference/kotlin/android/widget/MultiAutoCompleteTextView.Tokenizer#findTokenStart(kotlin.CharSequence,%20kotlin.Int))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `cursor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the start of the token that ends at offset`cursor`within`text`. |
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [terminateToken](https://developer.android.com/reference/kotlin/android/widget/MultiAutoCompleteTextView.Tokenizer#terminateToken(kotlin.CharSequence))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Returns`text`, modified, if necessary, to ensure that it ends with a token terminator (for example a space or comma). |
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
