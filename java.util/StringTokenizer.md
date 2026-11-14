# StringTokenizer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StringTokenizer

```
open class StringTokenizer : Enumeration<Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.util.StringTokenizer](https://developer.android.com/reference/kotlin/java/util/StringTokenizer#) |

The string tokenizer class allows an application to break a string into tokens. The tokenization method is much simpler than the one used by the`StreamTokenizer`class. The`StringTokenizer`methods do not distinguish among identifiers, numbers, and quoted strings, nor do they recognize and skip comments.

The set of delimiters (the characters that separate tokens) may be specified either at creation time or on a per-token basis.

An instance of`StringTokenizer`behaves in one of two ways, depending on whether it was created with the`returnDelims`flag having the value`true`or`false`:

- If the flag is`false`, delimiter characters serve to separate tokens. A token is a maximal sequence of consecutive characters that are not delimiters.
- If the flag is`true`, delimiter characters are themselves considered to be tokens. A token is thus either one delimiter character, or a maximal sequence of consecutive characters that are not delimiters.

A`StringTokenizer`object internally maintains a current position within the string to be tokenized. Some operations advance this current position past the characters processed.

A token is returned by taking a substring of the string that was used to create the`StringTokenizer`object.

The following is one example of the use of the tokenizer. The code: 

```kotlin
StringTokenizer st = new StringTokenizer("this is a test");
      while (st.hasMoreTokens()) {
          System.out.println(st.nextToken());
      }
  
```

prints the following output: 

```kotlin
this
      is
      a
      test
  
```

`StringTokenizer`is a legacy class that is retained for compatibility reasons although its use is discouraged in new code. It is recommended that anyone seeking this functionality use the`split`method of`String`or the java.util.regex package instead.

The following example illustrates how the`String.split`method can be used to break up a string into its basic tokens: 

```kotlin
String[] result = "this is a test".split("\\s");
      for (int x=0; x<result.length; x++)
          System.out.println(result[x]);
  
```

prints the following output: 

```kotlin
this
      is
      a
      test
  
```

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StringTokenizer](https://developer.android.com/reference/kotlin/java/util/StringTokenizer#StringTokenizer(kotlin.String))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a string tokenizer for the specified string. |
| [StringTokenizer](https://developer.android.com/reference/kotlin/java/util/StringTokenizer#StringTokenizer(kotlin.String,%20kotlin.String))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `delim:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a string tokenizer for the specified string. |
| [StringTokenizer](https://developer.android.com/reference/kotlin/java/util/StringTokenizer#StringTokenizer(kotlin.String,%20kotlin.String,%20kotlin.Boolean))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `delim:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `returnDelims:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Constructs a string tokenizer for the specified string. |

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [countTokens](https://developer.android.com/reference/kotlin/java/util/StringTokenizer#countTokens())`()` Calculates the number of times that this tokenizer's`nextToken`method can be called before it generates an exception. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMoreElements](https://developer.android.com/reference/kotlin/java/util/StringTokenizer#hasMoreElements())`()` Returns the same value as the`hasMoreTokens`method. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMoreTokens](https://developer.android.com/reference/kotlin/java/util/StringTokenizer#hasMoreTokens())`()` Tests if there are more tokens available from this tokenizer's string. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [nextElement](https://developer.android.com/reference/kotlin/java/util/StringTokenizer#nextElement())`()` Returns the same value as the`nextToken`method, except that its declared return value is`Object`rather than`String`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [nextToken](https://developer.android.com/reference/kotlin/java/util/StringTokenizer#nextToken())`()` Returns the next token from this string tokenizer. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [nextToken](https://developer.android.com/reference/kotlin/java/util/StringTokenizer#nextToken(kotlin.String))`(`delim:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the next token in this string tokenizer's string. |

| Inherited functions ||
|---|---|
| From class [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration) |---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E>! | [asIterator](https://developer.android.com/reference/kotlin/java/util/Enumeration#asIterator())`()` <br /> Returns an [Iterator](https://developer.android.com/reference/kotlin/java/util/Iterator) that traverses the remaining elements covered by this enumeration. Traversal is undefined if any methods are called on this enumeration after the call to`asIterator`. <br /> | ||

## Public constructors

### StringTokenizer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StringTokenizer(str: String!)
```

Constructs a string tokenizer for the specified string. The tokenizer uses the default delimiter set, which is`" \t\n\r\f"`: the space character, the tab character, the newline character, the carriage-return character, and the form-feed character. Delimiter characters themselves will not be treated as tokens.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a string to be parsed. |

| Exceptions ||
|----------------------------------|-----------------|
| `java.lang.NullPointerException` | if str is`null` |

### StringTokenizer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StringTokenizer(
    str: String!, 
    delim: String!)
```

Constructs a string tokenizer for the specified string. The characters in the`delim`argument are the delimiters for separating tokens. Delimiter characters themselves will not be treated as tokens.

Note that if`delim`is`null`, this constructor does not throw an exception. However, trying to invoke other methods on the resulting`StringTokenizer`may result in a`NullPointerException`.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a string to be parsed. |
| `delim` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the delimiters. |

| Exceptions ||
|----------------------------------|-----------------|
| `java.lang.NullPointerException` | if str is`null` |

### StringTokenizer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StringTokenizer(
    str: String!, 
    delim: String!, 
    returnDelims: Boolean)
```

Constructs a string tokenizer for the specified string. All characters in the`delim`argument are the delimiters for separating tokens.

If the`returnDelims`flag is`true`, then the delimiter characters are also returned as tokens. Each delimiter is returned as a string of length one. If the flag is`false`, the delimiter characters are skipped and only serve as separators between tokens.

Note that if`delim`is`null`, this constructor does not throw an exception. However, trying to invoke other methods on the resulting`StringTokenizer`may result in a`NullPointerException`.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a string to be parsed. |
| `delim` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the delimiters. |
| `returnDelims` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):flag indicating whether to return the delimiters as tokens. |

| Exceptions ||
|----------------------------------|-----------------|
| `java.lang.NullPointerException` | if str is`null` |

## Public methods

### countTokens

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun countTokens(): Int
```

Calculates the number of times that this tokenizer's`nextToken`method can be called before it generates an exception. The current position is not advanced.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of tokens remaining in the string using the current delimiter set. |

**See Also**

- [java.util.StringTokenizer#nextToken()](https://developer.android.com/reference/kotlin/java/util/StringTokenizer#nextToken()) 

### hasMoreElements

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasMoreElements(): Boolean
```

Returns the same value as the`hasMoreTokens`method. It exists so that this class can implement the`Enumeration`interface.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if there are more tokens;`false`otherwise. |

**See Also**

- [java.util.Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration)
- [java.util.StringTokenizer#hasMoreTokens()](https://developer.android.com/reference/kotlin/java/util/StringTokenizer#hasMoreTokens()) 

### hasMoreTokens

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasMoreTokens(): Boolean
```

Tests if there are more tokens available from this tokenizer's string. If this method returns`true`, then a subsequent call to`nextToken`with no argument will successfully return a token.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if and only if there is at least one token in the string after the current position;`false`otherwise. |

### nextElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextElement(): Any!
```

Returns the same value as the`nextToken`method, except that its declared return value is`Object`rather than`String`. It exists so that this class can implement the`Enumeration`interface.

| Return ||
|-----------------------------------------------------------------------------|-------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the next token in the string. |

| Exceptions ||
|------------------------------------|---------------------------------------------------------|
| `java.util.NoSuchElementException` | if there are no more tokens in this tokenizer's string. |

**See Also**

- [java.util.Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration)
- [java.util.StringTokenizer#nextToken()](https://developer.android.com/reference/kotlin/java/util/StringTokenizer#nextToken()) 

### nextToken

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextToken(): String!
```

Returns the next token from this string tokenizer.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the next token from this string tokenizer. |

| Exceptions ||
|------------------------------------|---------------------------------------------------------|
| `java.util.NoSuchElementException` | if there are no more tokens in this tokenizer's string. |

### nextToken

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextToken(delim: String!): String!
```

Returns the next token in this string tokenizer's string. First, the set of characters considered to be delimiters by this`StringTokenizer`object is changed to be the characters in the string`delim`. Then the next token in the string after the current position is returned. The current position is advanced beyond the recognized token. The new delimiter set remains the default after this call.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------|
| `delim` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the new delimiters. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the next token, after switching to the new delimiter set. |

| Exceptions ||
|------------------------------------|---------------------------------------------------------|
| `java.util.NoSuchElementException` | if there are no more tokens in this tokenizer's string. |
| `java.lang.NullPointerException` | if delim is`null` |
