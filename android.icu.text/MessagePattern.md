# MessagePattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MessagePattern

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/MessagePattern "View this page in Java") 
| --- | --- |

```
class MessagePattern : Cloneable, Freezable<MessagePattern!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.MessagePattern](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#) |

Parses and represents ICU MessageFormat patterns. Also handles patterns for ChoiceFormat, PluralFormat and SelectFormat. Used in the implementations of those classes as well as in tools for message validation, translation and format conversion.

The parser handles all syntax relevant for identifying message arguments. This includes "complex" arguments whose style strings contain nested MessageFormat pattern substrings. For "simple" arguments (with no nested MessageFormat pattern substrings), the argument style is not parsed any further.

The parser handles named and numbered message arguments and allows both in one message.

Once a pattern has been parsed successfully, iterate through the parsed data with countParts(), getPart() and related methods.

The data logically represents a parse tree, but is stored and accessed as a list of "parts" for fast and simple parsing and to minimize object allocations. Arguments and nested messages are best handled via recursion. For every _START "part", [getLimitPartIndex(int)](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#getLimitPartIndex(kotlin.Int))efficiently returns the index of the corresponding _LIMIT "part".

List of "parts": 

```kotlin
message = MSG_START (SKIP_SYNTAX | INSERT_CHAR | REPLACE_NUMBER | argument)* MSG_LIMIT
  argument = noneArg | simpleArg | complexArg
  complexArg = choiceArg | pluralArg | selectArg
 
  noneArg = ARG_START.NONE (ARG_NAME | ARG_NUMBER) ARG_LIMIT.NONE
  simpleArg = ARG_START.SIMPLE (ARG_NAME | ARG_NUMBER) ARG_TYPE [ARG_STYLE] ARG_LIMIT.SIMPLE
  choiceArg = ARG_START.CHOICE (ARG_NAME | ARG_NUMBER) choiceStyle ARG_LIMIT.CHOICE
  pluralArg = ARG_START.PLURAL (ARG_NAME | ARG_NUMBER) pluralStyle ARG_LIMIT.PLURAL
  selectArg = ARG_START.SELECT (ARG_NAME | ARG_NUMBER) selectStyle ARG_LIMIT.SELECT
 
  choiceStyle = ((ARG_INT | ARG_DOUBLE) ARG_SELECTOR message)+
  pluralStyle = [ARG_INT | ARG_DOUBLE] (ARG_SELECTOR [ARG_INT | ARG_DOUBLE] message)+
  selectStyle = (ARG_SELECTOR message)+
  
```

- Literal output text is not represented directly by "parts" but accessed between parts of a message, from one part's getLimit() to the next part's getIndex().
- `ARG_START.CHOICE`stands for an ARG_START Part with ArgType CHOICE.
- In the choiceStyle, the ARG_SELECTOR has the '\<', the '#' or the less-than-or-equal-to sign (U+2264).
- In the pluralStyle, the first, optional numeric Part has the "offset:" value. The optional numeric Part between each (ARG_SELECTOR, message) pair is the value of an explicit-number selector like "=2", otherwise the selector is a non-numeric identifier.
- The REPLACE_NUMBER Part can occur only in an immediate sub-message of the pluralStyle.

This class is not intended for public subclassing.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [ApostropheMode](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern.ApostropheMode) Mode for when an apostrophe starts quoted literal text for MessageFormat output. |
| | [ArgType](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern.ArgType) Argument type constants. |
| | [Part](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern.Part) A message pattern "part", representing a pattern parsing event. |
| --- | --- |

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ARG_NAME_NOT_NUMBER](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#ARG_NAME_NOT_NUMBER:kotlin.Int) Return value from [validateArgumentName(java.lang.String)](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#validateArgumentName(kotlin.String))for when the string is a valid "pattern identifier" but not a number. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ARG_NAME_NOT_VALID](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#ARG_NAME_NOT_VALID:kotlin.Int) Return value from [validateArgumentName(java.lang.String)](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#validateArgumentName(kotlin.String))for when the string is invalid. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [NO_NUMERIC_VALUE](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#NO_NUMERIC_VALUE:kotlin.Double) Special value that is returned by getNumericValue(Part) when no numeric value is defined for a part. |
| --- | --- |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MessagePattern](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#MessagePattern())`()` Constructs an empty MessagePattern with default ApostropheMode. |
| [MessagePattern](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#MessagePattern(android.icu.text.MessagePattern.ApostropheMode))`(`mode:` ` [MessagePattern.ApostropheMode](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern.ApostropheMode)!`)` Constructs an empty MessagePattern. |
| [MessagePattern](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#MessagePattern(kotlin.String))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a MessagePattern with default ApostropheMode and parses the MessageFormat pattern string. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [autoQuoteApostropheDeep](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#autoQuoteApostropheDeep())`()` Returns a version of the parsed pattern string where each ASCII apostrophe is doubled (escaped) if it is not already, and if it is not interpreted as quoting syntax. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#clear())`()` Clears this MessagePattern. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearPatternAndSetApostropheMode](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#clearPatternAndSetApostropheMode(android.icu.text.MessagePattern.ApostropheMode))`(`mode:` ` [MessagePattern.ApostropheMode](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern.ApostropheMode)!`)` Clears this MessagePattern and sets the ApostropheMode. |
| --- | --- |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#clone())`()` Creates and returns a copy of this object. |
| [MessagePattern](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#)! | [cloneAsThawed](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#cloneAsThawed())`()` Creates and returns an unfrozen copy of this object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [countParts](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#countParts())`()` Returns the number of "parts" created by parsing the pattern string. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [MessagePattern](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#)! | [freeze](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#freeze())`()` Freezes this object, making it immutable and thread-safe. |
| [MessagePattern.ApostropheMode](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern.ApostropheMode)! | [getApostropheMode](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#getApostropheMode())`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLimitPartIndex](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#getLimitPartIndex(kotlin.Int))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the index of the ARG|MSG_LIMIT part corresponding to the ARG|MSG_START at start. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getNumericValue](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#getNumericValue(android.icu.text.MessagePattern.Part))`(`part:` ` [MessagePattern.Part](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern.Part)!`)` Returns the numeric value associated with an ARG_INT or ARG_DOUBLE. |
| [MessagePattern.Part](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern.Part)! | [getPart](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#getPart(kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the i-th pattern "part". |
| --- | --- |
| [MessagePattern.Part.Type](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern.Part.Type)! | [getPartType](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#getPartType(kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the Part. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPatternIndex](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#getPatternIndex(kotlin.Int))`(`partIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the pattern index of the specified pattern "part". |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPatternString](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#getPatternString())`()` <br /> |
| --- | --- |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getPluralOffset](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#getPluralOffset(kotlin.Int))`(`pluralStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the "offset:" value of a PluralFormat argument, or 0 if none is specified. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSubstring](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#getSubstring(android.icu.text.MessagePattern.Part))`(`part:` ` [MessagePattern.Part](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern.Part)!`)` Returns the substring of the pattern string indicated by the Part. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasNamedArguments](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#hasNamedArguments())`()` Does the parsed pattern have named arguments like {first_name}? |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasNumberedArguments](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#hasNumberedArguments())`()` Does the parsed pattern have numbered arguments like {2}? |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#hashCode())`()` Returns a hash code value for the object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFrozen](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#isFrozen())`()` Determines whether this object is frozen (immutable) or not. |
| --- | --- |
| [MessagePattern](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#)! | [parse](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#parse(kotlin.String))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parses a MessageFormat pattern string. |
| [MessagePattern](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#)! | [parseChoiceStyle](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#parseChoiceStyle(kotlin.String))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parses a ChoiceFormat pattern string. |
| [MessagePattern](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#)! | [parsePluralStyle](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#parsePluralStyle(kotlin.String))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parses a PluralFormat pattern string. |
| --- | --- |
| [MessagePattern](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#)! | [parseSelectStyle](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#parseSelectStyle(kotlin.String))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parses a SelectFormat pattern string. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [partSubstringMatches](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#partSubstringMatches(android.icu.text.MessagePattern.Part,%20kotlin.String))`(`part:` ` [MessagePattern.Part](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern.Part)!`, `s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Compares the part's substring with the input string s. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#toString())`()` Returns a string representation of the object. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [validateArgumentName](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#validateArgumentName(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Validates and parses an argument name or argument number string. |

## Constants

### ARG_NAME_NOT_NUMBER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ARG_NAME_NOT_NUMBER: Int
```

Return value from [validateArgumentName(java.lang.String)](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#validateArgumentName(kotlin.String))for when the string is a valid "pattern identifier" but not a number. 

 Value: -1

### ARG_NAME_NOT_VALID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ARG_NAME_NOT_VALID: Int
```

Return value from [validateArgumentName(java.lang.String)](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#validateArgumentName(kotlin.String))for when the string is invalid. It might not be a valid "pattern identifier", or it have only ASCII digits but there is a leading zero or the number is too large. 

 Value: -2

### NO_NUMERIC_VALUE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_NUMERIC_VALUE: Double
```

Special value that is returned by getNumericValue(Part) when no numeric value is defined for a part. 

 Value: -1.23456789E8

**See Also**

- [#getNumericValue](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#getNumericValue(android.icu.text.MessagePattern.Part))

## Public constructors

### MessagePattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MessagePattern()
```

Constructs an empty MessagePattern with default ApostropheMode. 

### MessagePattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MessagePattern(mode: MessagePattern.ApostropheMode!)
```

Constructs an empty MessagePattern.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [MessagePattern.ApostropheMode](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern.ApostropheMode)!:Explicit ApostropheMode. |

### MessagePattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MessagePattern(pattern: String!)
```

Constructs a MessagePattern with default ApostropheMode and parses the MessageFormat pattern string.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a MessageFormat pattern string |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | for syntax errors in the pattern string |
| `java.lang.IndexOutOfBoundsException` | if certain limits are exceeded (e.g., argument number too high, argument name too long, etc.) |
| `java.lang.NumberFormatException` | if a number could not be parsed |
| --- | --- |

## Public methods

### autoQuoteApostropheDeep

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun autoQuoteApostropheDeep(): String!
```

Returns a version of the parsed pattern string where each ASCII apostrophe is doubled (escaped) if it is not already, and if it is not interpreted as quoting syntax.

For example, this turns "I don't '{know}' {gender,select,female{h''er}other{h'im}}." into "I don''t '{know}' {gender,select,female{h''er}other{h''im}}."

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the deep-auto-quoted version of the parsed pattern string. |

**See Also**

- [android.icu.text.MessageFormat#autoQuoteApostrophe(String)](https://developer.android.com/reference/kotlin/android/icu/text/MessageFormat#autoQuoteApostrophe(kotlin.String)) 

### clear

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clear(): Unit
```

Clears this MessagePattern. countParts() will return 0. 

### clearPatternAndSetApostropheMode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clearPatternAndSetApostropheMode(mode: MessagePattern.ApostropheMode!): Unit
```

Clears this MessagePattern and sets the ApostropheMode. countParts() will return 0.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [MessagePattern.ApostropheMode](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern.ApostropheMode)!:The new ApostropheMode. |

### clone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clone(): Any
```

Creates and returns a copy of this object.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a copy of this object (or itself if frozen). |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### cloneAsThawed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun cloneAsThawed(): MessagePattern!
```

Creates and returns an unfrozen copy of this object.

| Return ||
|----------------------------------------------------------------------------------------------------|------------------------|
| [MessagePattern](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#)! | a copy of this object. |

### countParts

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun countParts(): Int
```

Returns the number of "parts" created by parsing the pattern string. Returns 0 if no pattern has been parsed or clear() was called.

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of pattern parts. |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `other` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:another object to compare with. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this object is equivalent to the other one. |

### freeze

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun freeze(): MessagePattern!
```

Freezes this object, making it immutable and thread-safe.

| Return ||
|----------------------------------------------------------------------------------------------------|------|
| [MessagePattern](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#)! | this |

### getApostropheMode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getApostropheMode(): MessagePattern.ApostropheMode!
```

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| [MessagePattern.ApostropheMode](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern.ApostropheMode)! | this instance's ApostropheMode. |

### getLimitPartIndex

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLimitPartIndex(start: Int): Int
```

Returns the index of the ARG|MSG_LIMIT part corresponding to the ARG|MSG_START at start.
| --- | --- | --- |

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of some Part data (0..countParts()-1); this Part should be of Type ARG_START or MSG_START. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The first i\>start where getPart(i).getType()==ARG|MSG_LIMIT at the same nesting level, or start itself if getPartType(msgStart)!=ARG|MSG_START. |

| Exceptions ||
|---------------------------------------|---------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if start is outside the (0..countParts()-1) range |

### getNumericValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNumericValue(part: MessagePattern.Part!): Double
```

Returns the numeric value associated with an ARG_INT or ARG_DOUBLE.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `part` | [MessagePattern.Part](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern.Part)!:a part of this MessagePattern. |

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the part's numeric value, or NO_NUMERIC_VALUE if this is not a numeric part. |

### getPart

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPart(i: Int): MessagePattern.Part!
```

Gets the i-th pattern "part".

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the Part data. (0..countParts()-1) |

| Return ||
|-------------------------------------------------------------------------------------------------------------|--------------------------|
| [MessagePattern.Part](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern.Part)! | the i-th pattern "part". |

| Exceptions ||
|---------------------------------------|-----------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if i is outside the (0..countParts()-1) range |

### getPartType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPartType(i: Int): MessagePattern.Part.Type!
```

Returns the Part.Type of the i-th pattern "part". Convenience method for getPart(i).getType().

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the Part data. (0..countParts()-1) |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------|
| [MessagePattern.Part.Type](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern.Part.Type)! | The Part.Type of the i-th Part. |

| Exceptions ||
|---------------------------------------|-----------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if i is outside the (0..countParts()-1) range |

### getPatternIndex

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPatternIndex(partIndex: Int): Int
```

Returns the pattern index of the specified pattern "part". Convenience method for getPart(partIndex).getIndex().

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------|
| `partIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the Part data. (0..countParts()-1) |

| Return ||
|----------------------------------------------------------------------------|---------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The pattern index of this Part. |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if partIndex is outside the (0..countParts()-1) range |

### getPatternString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPatternString(): String!
```

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the parsed pattern string (null if none was parsed). |

### getPluralOffset

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPluralOffset(pluralStart: Int): Double
```

Returns the "offset:" value of a PluralFormat argument, or 0 if none is specified.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pluralStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the first PluralFormat argument style part. (0..countParts()-1) |

| Return ||
|----------------------------------------------------------------------------------|----------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the "offset:" value. |

| Exceptions ||
|---------------------------------------|---------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if pluralStart is outside the (0..countParts()-1) range |

### getSubstring

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSubstring(part: MessagePattern.Part!): String!
```

Returns the substring of the pattern string indicated by the Part. Convenience method for getPatternString().substring(part.getIndex(), part.getLimit()).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `part` | [MessagePattern.Part](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern.Part)!:a part of this MessagePattern. |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the substring associated with part. |

### hasNamedArguments

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasNamedArguments(): Boolean
```

Does the parsed pattern have named arguments like {first_name}?

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the parsed pattern has at least one named argument. |

### hasNumberedArguments

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasNumberedArguments(): Boolean
```

Does the parsed pattern have numbered arguments like {2}?

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the parsed pattern has at least one numbered argument. |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by [java.util.HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#).

The general contract of`hashCode`is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the`hashCode`method must consistently return the same integer, provided no information used in`equals`comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the [equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any))method, then calling the`hashCode`method on each of the two objects must produce the same integer result.
- It is*not* required that if two objects are unequal according to the [equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any))method, then calling the`hashCode`method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isFrozen

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isFrozen(): Boolean
```

Determines whether this object is frozen (immutable) or not.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this object is frozen. |

### parse

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun parse(pattern: String!): MessagePattern!
```

Parses a MessageFormat pattern string.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a MessageFormat pattern string |

| Return ||
|----------------------------------------------------------------------------------------------------|------|
| [MessagePattern](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#)! | this |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | for syntax errors in the pattern string |
| `java.lang.IndexOutOfBoundsException` | if certain limits are exceeded (e.g., argument number too high, argument name too long, etc.) |
| `java.lang.NumberFormatException` | if a number could not be parsed |
| --- | --- |

### parseChoiceStyle

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun parseChoiceStyle(pattern: String!): MessagePattern!
```

Parses a ChoiceFormat pattern string.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a ChoiceFormat pattern string |

| Return ||
|----------------------------------------------------------------------------------------------------|------|
| [MessagePattern](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#)! | this |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | for syntax errors in the pattern string |
| `java.lang.IndexOutOfBoundsException` | if certain limits are exceeded (e.g., argument number too high, argument name too long, etc.) |
| `java.lang.NumberFormatException` | if a number could not be parsed |
| --- | --- |

### parsePluralStyle

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun parsePluralStyle(pattern: String!): MessagePattern!
```

Parses a PluralFormat pattern string.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a PluralFormat pattern string |

| Return ||
|----------------------------------------------------------------------------------------------------|------|
| [MessagePattern](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#)! | this |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | for syntax errors in the pattern string |
| `java.lang.IndexOutOfBoundsException` | if certain limits are exceeded (e.g., argument number too high, argument name too long, etc.) |
| `java.lang.NumberFormatException` | if a number could not be parsed |
| --- | --- |

### parseSelectStyle

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun parseSelectStyle(pattern: String!): MessagePattern!
```

Parses a SelectFormat pattern string.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a SelectFormat pattern string |

| Return ||
|----------------------------------------------------------------------------------------------------|------|
| [MessagePattern](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern#)! | this |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | for syntax errors in the pattern string |
| `java.lang.IndexOutOfBoundsException` | if certain limits are exceeded (e.g., argument number too high, argument name too long, etc.) |
| `java.lang.NumberFormatException` | if a number could not be parsed |
| --- | --- |

### partSubstringMatches

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun partSubstringMatches(
    part: MessagePattern.Part!, 
    s: String!
): Boolean
```

Compares the part's substring with the input string s.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `part` | [MessagePattern.Part](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern.Part)!:a part of this MessagePattern. |
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a string. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if getSubstring(part).equals(s). |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### validateArgumentName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun validateArgumentName(name: String!): Int
```

Validates and parses an argument name or argument number string. An argument name must be a "pattern identifier", that is, it must contain no Unicode Pattern_Syntax or Pattern_White_Space characters. If it only contains ASCII digits, then it must be a small integer with no leading zero.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Input string. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | \>=0 if the name is a valid number, ARG_NAME_NOT_NUMBER (-1) if it is a "pattern identifier" but not all ASCII digits, ARG_NAME_NOT_VALID (-2) if it is neither. |
