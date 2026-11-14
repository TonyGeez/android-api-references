# Rfc822Tokenizer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Rfc822Tokenizer

Kotlin| [Java](Rfc822Tokenizer.md) 
| --- | --- |

```
open class Rfc822Tokenizer : MultiAutoCompleteTextView.Tokenizer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.util.Rfc822Tokenizer](Rfc822Tokenizer.md) |

This class works as a Tokenizer for MultiAutoCompleteTextView for address list fields, and also provides a method for converting a string of addresses (such as might be typed into such a field) into a series of Rfc822Tokens.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------|---|
| [Rfc822Tokenizer](Rfc822Tokenizer.md))`()` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [findTokenEnd](Rfc822Tokenizer.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `cursor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the end of the token (minus trailing punctuation) that begins at offset`cursor`within`text`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [findTokenStart](Rfc822Tokenizer.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `cursor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the start of the token that ends at offset`cursor`within`text`. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [terminateToken](Rfc822Tokenizer.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Terminates the specified address with a comma and space. |
| --- | --- |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Rfc822Token](Rfc822Token.md)!\>! | [tokenize](Rfc822Tokenizer.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` This method will try to take a string like "Foo Bar (something) \<foo\\@google. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tokenize](Rfc822Tokenizer.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `out:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [Rfc822Token](Rfc822Token.md)!>!`)` This constructor will try to take a string like "Foo Bar (something) \<foo\\@google. |

## Public constructors

### Rfc822Tokenizer

```
Rfc822Tokenizer()
```

## Public methods

### findTokenEnd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun findTokenEnd(
    text: CharSequence!, 
    cursor: Int
): Int
```

Returns the end of the token (minus trailing punctuation) that begins at offset`cursor`within`text`. 

### findTokenStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun findTokenStart(
    text: CharSequence!, 
    cursor: Int
): Int
```

Returns the start of the token that ends at offset`cursor`within`text`. 

### terminateToken

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun terminateToken(text: CharSequence!): CharSequence!
```

Terminates the specified address with a comma and space. This assumes that the specified text already has valid syntax. The Adapter subclass's convertToString() method must make that guarantee. 

### tokenize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun tokenize(text: CharSequence!): Array<Rfc822Token!>!
```

This method will try to take a string like "Foo Bar (something) \<foo\\@google.com\>, blah\\@google.com (something)" and convert it into one or more Rfc822Tokens. It does \*not\* decode MIME encoded-words; charset conversion must already have taken place if necessary. It will try to be tolerant of broken syntax instead of returning an error. 

### tokenize

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun tokenize(
    text: CharSequence!, 
    out: MutableCollection<Rfc822Token!>!
): Unit
```

This constructor will try to take a string like "Foo Bar (something) \<foo\\@google.com\>, blah\\@google.com (something)" and convert it into one or more Rfc822Tokens, output into the supplied collection. It does \*not\* decode MIME encoded-words; charset conversion must already have taken place if necessary. It will try to be tolerant of broken syntax instead of returning an error.
