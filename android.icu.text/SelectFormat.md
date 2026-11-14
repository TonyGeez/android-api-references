# SelectFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SelectFormat

Kotlin | [Java](https://developer.android.com/reference/android/icu/text/SelectFormat "View this page in Java") 

```
open class SelectFormat : Format
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.text.Format](https://developer.android.com/reference/kotlin/java/text/Format.html#) ||
| | ↳ | [android.icu.text.SelectFormat](https://developer.android.com/reference/kotlin/android/icu/text/SelectFormat#) |

`SelectFormat` supports the creation of internationalized messages by selecting phrases based on keywords. The pattern specifies how to map keywords to phrases and provides a default phrase. The object provided to the format method is a string that's matched against the keywords. If there is a match, the corresponding phrase is selected; otherwise, the default phrase is used.

### Using `SelectFormat` for Gender Agreement

Note: Typically, select formatting is done via `MessageFormat` with a `select` argument type, rather than using a stand-alone `SelectFormat`.

The main use case for the select format is gender based inflection. When names or nouns are inserted into sentences, their gender can affect pronouns, verb forms, articles, and adjectives. Special care needs to be taken for the case where the gender cannot be determined. The impact varies between languages:

- English has three genders, and unknown gender is handled as a special case. Names use the gender of the named person (if known), nouns referring to people use natural gender, and inanimate objects are usually neutral. The gender only affects pronouns: "he", "she", "it", "they".
- German differs from English in that the gender of nouns is rather arbitrary, even for nouns referring to people ("Mädchen", girl, is neutral). The gender affects pronouns ("er", "sie", "es"), articles ("der", "die", "das"), and adjective forms ("guter Mann", "gute Frau", "gutes Mädchen").
- French has only two genders; as in German the gender of nouns is rather arbitrary - for sun and moon, the genders are the opposite of those in German. The gender affects pronouns ("il", "elle"), articles ("le", "la"), adjective forms ("bon", "bonne"), and sometimes verb forms ("allé", "allée").
- Polish distinguishes five genders (or noun classes), human masculine, animate non-human masculine, inanimate masculine, feminine, and neuter.

Some other languages have noun classes that are not related to gender, but similar in grammatical use. Some African languages have around 20 noun classes.

**Note:** For the gender of a *person* in a given sentence, we usually need to distinguish only between female, male and other/unknown.

To enable localizers to create sentence patterns that take their language's gender dependencies into consideration, software has to provide information about the gender associated with a noun or name to `MessageFormat`. Two main cases can be distinguished:

- For people, natural gender information should be maintained for each person. Keywords like "male", "female", "mixed" (for groups of people) and "unknown" could be used.
- For nouns, grammatical gender information should be maintained for each noun and per language, e.g., in resource bundles. The keywords "masculine", "feminine", and "neuter" are commonly used, but some languages may require other keywords.

The resulting keyword is provided to `MessageFormat` as a parameter separate from the name or noun it's associated with. For example, to generate a message such as "Jean went to Paris", three separate arguments would be provided: The name of the person as argument 0, the gender of the person as argument 1, and the name of the city as argument 2. The sentence pattern for English, where the gender of the person has no impact on this simple sentence, would not refer to argument 1 at all: 

```kotlin
{0} went to {2}.
```

**Note:** The entire sentence should be included (and partially repeated) inside each phrase. Otherwise translators would have to be trained on how to move bits of the sentence in and out of the select argument of a message. (The examples below do not follow this recommendation!)

The sentence pattern for French, where the gender of the person affects the form of the participle, uses a select format based on argument 1: 

```kotlin
{0} est {1, select, female {allée} other {allé}} à {2}.
```

Patterns can be nested, so that it's possible to handle interactions of number and gender where necessary. For example, if the above sentence should allow for the names of several people to be inserted, the following sentence pattern can be used (with argument 0 the list of people's names, argument 1 the number of people, argument 2 their combined gender, and argument 3 the city name): 

```kotlin
{0} {1, plural,
  one {est {2, select, female {allée} other  {allé}}}
  other {sont {2, select, female {allées} other {allés}}}
  }à {3}.
```

#### Patterns and Their Interpretation

The `SelectFormat` pattern string defines the phrase output for each user-defined keyword. The pattern is a sequence of (keyword, message) pairs. A keyword is a "pattern identifier": \[\^\[\[:Pattern_Syntax:\]\[:Pattern_White_Space:\]\]\]+

Each message is a MessageFormat pattern string enclosed in {curly braces}.

You always have to define a phrase for the default keyword `other`; this phrase is returned when the keyword provided to the `format` method matches no other keyword. If a pattern does not provide a phrase for `other`, the method it's provided to returns the error `U_DEFAULT_KEYWORD_MISSING`. 
Pattern_White_Space between keywords and messages is ignored. Pattern_White_Space within a message is preserved and output. 

```kotlin
Example:
  MessageFormat msgFmt = new MessageFormat("{0} est " +
      "{1, select, female {allée} other {allé}} à Paris.",
      new ULocale("fr"));
  Object args[] = {"Kirti","female"};
  System.out.println(msgFmt.format(args));
  
```

Produces the output: 
`Kirti est allée à Paris.`

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SelectFormat](https://developer.android.com/reference/kotlin/android/icu/text/SelectFormat#SelectFormat(kotlin.String))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new `SelectFormat` for a given pattern string. |

| Public methods ||
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyPattern](https://developer.android.com/reference/kotlin/android/icu/text/SelectFormat#applyPattern(kotlin.String))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the pattern used by this select format. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/icu/text/SelectFormat#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| open [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | [format](https://developer.android.com/reference/kotlin/android/icu/text/SelectFormat#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(`keyword:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `toAppendTo:` ` [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!`, `pos:` ` [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#)!`)` Selects the phrase for the given keyword. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](https://developer.android.com/reference/kotlin/android/icu/text/SelectFormat#format(kotlin.String))`(`keyword:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Selects the phrase for the given keyword. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/icu/text/SelectFormat#hashCode())`()` Returns a hash code value for the object. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [parseObject](https://developer.android.com/reference/kotlin/android/icu/text/SelectFormat#parseObject(kotlin.String,%20java.text.ParsePosition))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `pos:` ` [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#)!`)` This method is not supported by `SelectFormat`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toPattern](https://developer.android.com/reference/kotlin/android/icu/text/SelectFormat#toPattern())`()` Returns the pattern for this `SelectFormat` |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/icu/text/SelectFormat#toString())`()` Returns a string representation of the object. |

| Inherited functions ||
|---|---|
| From class [Format](https://developer.android.com/reference/kotlin/java/text/Format.html#) |----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/text/Format.html#clone())`()` Creates and returns a copy of this object. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](https://developer.android.com/reference/kotlin/java/text/Format.html#format(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Formats an object to produce a string. This is equivalent to [format](https://developer.android.com/reference/kotlin/java/text/Format.html#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(obj, new StringBuffer(), new FieldPosition(0)).toString();` <br /> | | [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.html#)! | [formatToCharacterIterator](https://developer.android.com/reference/kotlin/java/text/Format.html#formatToCharacterIterator(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Formats an Object producing an `AttributedCharacterIterator`. You can use the returned `AttributedCharacterIterator` to build the resulting String, as well as to determine information about the resulting String. Each attribute key of the AttributedCharacterIterator will be of type `Field`. It is up to each `Format` implementation to define what the legal values are for each attribute in the `AttributedCharacterIterator`, but typically the attribute key is also used as the attribute value. The default implementation creates an `AttributedCharacterIterator` with no attributes. Subclasses that support fields should override this and create an `AttributedCharacterIterator` with meaningful attributes. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [parseObject](https://developer.android.com/reference/kotlin/java/text/Format.html#parseObject(kotlin.String))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parses text from the beginning of the given string to produce an object. The method may not use the entire text of the given string. <br /> | ||

## Public constructors

### SelectFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SelectFormat(pattern: String!)
```

Creates a new `SelectFormat` for a given pattern string.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the pattern for this `SelectFormat`. |

## Public methods

### applyPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyPattern(pattern: String!): Unit
```

Sets the pattern used by this select format. Patterns and their interpretation are specified in the class description.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the pattern for this select format. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------|
| `java.lang.IllegalArgumentException` | when the pattern is not a valid select format pattern. |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if this object is the same as the obj argument; `false` otherwise. |

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun format(
    keyword: Any!, 
    toAppendTo: StringBuffer!, 
    pos: FieldPosition!
): StringBuffer!
```

Selects the phrase for the given keyword. and appends the formatted message to the given `StringBuffer`.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | The object to format |
| `toAppendTo` | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!: the selected phrase will be appended to this `StringBuffer`. |
| `pos` | [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#)!: will be ignored by this method. |
| `keyword` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: a phrase selection keyword. |

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | the string buffer passed in as toAppendTo, with formatted text appended. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------|
| `java.lang.NullPointerException` | if `toAppendTo` or `pos` is null |
| `java.lang.IllegalArgumentException` | when the given keyword is not a String or not a "pattern identifier" |

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(keyword: String!): String!
```

Selects the phrase for the given keyword.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------|
| `keyword` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a phrase selection keyword. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the string containing the formatted select message. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------|
| `java.lang.IllegalArgumentException` | when the given keyword is not a "pattern identifier" |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by [java.util.HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#).

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the [equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)) method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the [equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)) method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### parseObject

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parseObject(
    source: String!, 
    pos: ParsePosition!
): Any!
```

This method is not supported by `SelectFormat`.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the string to be parsed. |
| `pos` | [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#)!: defines the position where parsing is to begin, and upon return, the position where parsing left off. If the position has not changed upon return, then parsing failed. |

| Return ||
|-----------------------------------------------------------------------------|-----------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | nothing because this method is not supported. |

| Exceptions ||
|-------------------------------------------|-------------------------------|
| `java.lang.NullPointerException` | if `source` or `pos` is null. |
| `java.lang.UnsupportedOperationException` | thrown always. |

### toPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toPattern(): String!
```

Returns the pattern for this `SelectFormat`

| Return ||
|-----------------------------------------------------------------------------------|--------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the pattern string |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
