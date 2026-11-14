# SymbolTable

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SymbolTable

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/SymbolTable "View this page in Java") 
| --- | --- |

```
interface SymbolTable
```

| [android.icu.text.SymbolTable](https://developer.android.com/reference/kotlin/android/icu/text/SymbolTable#) |

An interface that defines both lookup protocol and parsing of symbolic names.

This interface is used by UnicodeSet to resolve $Variable style references that appear in set patterns. RBBI and Transliteration both independently implement this interface.

A symbol table maintains two kinds of mappings. The first is between symbolic names and their values. For example, if the variable with the name "start" is set to the value "alpha" (perhaps, though not necessarily, through an expression such as "$start=alpha"), then the call lookup("start") will return the char\[\] array \['a', 'l', 'p', 'h', 'a'\].

The second kind of mapping is between character values and UnicodeMatcher objects. This is used by RuleBasedTransliterator, which uses characters in the private use area to represent objects such as UnicodeSets. If U+E015 is mapped to the UnicodeSet \[a-z\], then lookupMatcher(0xE015) will return the UnicodeSet \[a-z\].

Finally, a symbol table defines parsing behavior for symbolic names. All symbolic names start with the SYMBOL_REF character. When a parser encounters this character, it calls parseReference() with the position immediately following the SYMBOL_REF. The symbol table parses the name, if there is one, and returns it.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [SYMBOL_REF](https://developer.android.com/reference/kotlin/android/icu/text/SymbolTable#SYMBOL_REF:kotlin.Char) The character preceding a symbol reference name. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | [lookup](https://developer.android.com/reference/kotlin/android/icu/text/SymbolTable#lookup(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Lookup the characters associated with this string and return it. |
| abstract [UnicodeMatcher](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeMatcher)! | [lookupMatcher](https://developer.android.com/reference/kotlin/android/icu/text/SymbolTable#lookupMatcher(kotlin.Int))`(`ch:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Lookup the UnicodeMatcher associated with the given character, and return it. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [parseReference](https://developer.android.com/reference/kotlin/android/icu/text/SymbolTable#parseReference(kotlin.String,%20java.text.ParsePosition,%20kotlin.Int))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `pos:` ` [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#)!`, `limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Parse a symbol reference name from the given string, starting at the given position. |
| --- | --- |

## Constants

### SYMBOL_REF

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYMBOL_REF: Char
```

The character preceding a symbol reference name. 

 Value: '$'

## Public methods

### lookup

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun lookup(s: String!): CharArray!
```

Lookup the characters associated with this string and return it. Return null if no such name exists. The resultant array may have length zero.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the symbolic name to lookup |

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | a char array containing the name's value, or null if there is no mapping for s. |

### lookupMatcher

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun lookupMatcher(ch: Int): UnicodeMatcher!
```

Lookup the UnicodeMatcher associated with the given character, and return it. Return null if not found.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a 32-bit code point from 0 to 0x10FFFF inclusive. |

| Return ||
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [UnicodeMatcher](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeMatcher)! | the UnicodeMatcher object represented by the given character, or null if there is no mapping for ch. |

### parseReference

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun parseReference(
    text: String!, 
    pos: ParsePosition!, 
    limit: Int
): String!
```

Parse a symbol reference name from the given string, starting at the given position. If no valid symbol reference name is found, return null and leave pos unchanged. That is, if the character at pos cannot start a name, or if pos is at or after text.length(), then return null. This indicates an isolated SYMBOL_REF character.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the text to parse for the name |
| `pos` | [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#)!:on entry, the index of the first character to parse. This is the character following the SYMBOL_REF character. On exit, the index after the last parsed character. If the parse failed, pos is unchanged on exit. |
| `limit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index after the last character to be parsed. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the parsed name, or null if there is no valid symbolic name at the given position. |
