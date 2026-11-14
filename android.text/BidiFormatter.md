# BidiFormatter

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BidiFormatter

Kotlin| [Java](https://developer.android.com/reference/android/text/BidiFormatter "View this page in Java") 
| --- | --- |

```
class BidiFormatter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.BidiFormatter](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#) |

Utility class for formatting text for display in a potentially opposite-directionality context without garbling. The directionality of the context is set at formatter creation and the directionality of the text can be either estimated or passed in when known.

To support versions lower than [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int), you can use the support library's androidx.core.text.BidiFormatter class.

These APIs provides the following functionality:

1. Bidi Wrapping When text in one language is mixed into a document in another, opposite-directionality language, e.g. when an English business name is embedded in some Hebrew text, both the inserted string and the text surrounding it may be displayed incorrectly unless the inserted string is explicitly separated from the surrounding text in a "wrapper" that:

- Declares its directionality so that the string is displayed correctly. This can be done in Unicode bidi formatting codes by #unicodeWrap and similar methods.

- Isolates the string's directionality, so it does not unduly affect the surrounding content. Currently, this can only be done using invisible Unicode characters of the same direction as the context (LRM or RLM) in addition to the directionality declaration above, thus "resetting" the directionality to that of the context. The "reset" may need to be done at both ends of the string. Without "reset" after the string, the string will "stick" to a number or logically separate opposite-direction text that happens to follow it in-line (even if separated by neutral content like spaces and punctuation). Without "reset" before the string, the same can happen there, but only with more opposite-direction text, not a number. One approach is to "reset" the direction only after each string, on the theory that if the preceding opposite- direction text is itself bidi-wrapped, the "reset" after it will prevent the sticking. (Doing the "reset" only before each string definitely does not work because we do not want to require bidi-wrapping numbers, and a bidi-wrapped opposite-direction string could be followed by a number.) Still, the safest policy is to do the "reset" on both ends of each string, since RTL message translations often contain untranslated Latin-script brand names and technical terms, and one of these can be followed by a bidi-wrapped inserted value. On the other hand, when one has such a message, it is best to do the "reset" manually in the message translation itself, since the message's opposite-direction text could be followed by an inserted number, which we would not bidi-wrap anyway. Thus, "reset" only after the string is the current default. In an alternative to "reset", recent additions to the HTML, CSS, and Unicode standards allow the isolation to be part of the directionality declaration. This form of isolation is better than "reset" because it takes less space, does not require knowing the context directionality, has a gentler effect than "reset", and protects both ends of the string. However, we do not yet allow using it because required platforms do not yet support it.

Providing these wrapping services is the basic purpose of the bidi formatter.

2. Directionality estimation How does one know whether a string about to be inserted into surrounding text has the same directionality? Well, in many cases, one knows that this must be the case when writing the code doing the insertion, e.g. when a localized message is inserted into a localized page. In such cases there is no need to involve the bidi formatter at all. In some other cases, it need not be the same as the context, but is either constant (e.g. urls are always LTR) or otherwise known. In the remaining cases, e.g. when the string is user-entered or comes from a database, the language of the string (and thus its directionality) is not known a priori, and must be estimated at run-time. The bidi formatter can do this automatically using the default first-strong estimation algorithm. It can also be configured to use a custom directionality estimation object.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/text/BidiFormatter.Builder) A class for building a BidiFormatter with non-default options. |

| Public methods ||
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [BidiFormatter](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#)! | [getInstance](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#getInstance())`()` Factory for creating an instance of BidiFormatter for the default locale directionality. |
| static [BidiFormatter](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#)! | [getInstance](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#getInstance(kotlin.Boolean))`(`rtlContext:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Factory for creating an instance of BidiFormatter given the context directionality. |
| static [BidiFormatter](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#)! | [getInstance](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#getInstance(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Factory for creating an instance of BidiFormatter given the context locale. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getStereoReset](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#getStereoReset())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRtl](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#isRtl(kotlin.CharSequence))`(`str:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Operates like [isRtl(java.lang.String)](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#isRtl(kotlin.String)), but takes a CharSequence instead of a string |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRtl](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#isRtl(kotlin.String))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Estimates the directionality of a string using the default text direction heuristic. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRtlContext](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#isRtlContext())`()` <br /> |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [unicodeWrap](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#unicodeWrap(kotlin.CharSequence))`(`str:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Operates like [unicodeWrap(java.lang.CharSequence,android.text.TextDirectionHeuristic,boolean)](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#unicodeWrap(kotlin.CharSequence,%20android.text.TextDirectionHeuristic,%20kotlin.Boolean)), but uses the formatter's default direction estimation algorithm and assumes`isolate`is true. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [unicodeWrap](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#unicodeWrap(kotlin.CharSequence,%20android.text.TextDirectionHeuristic))`(`str:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `heuristic:` ` [TextDirectionHeuristic](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristic)!`)` Operates like [unicodeWrap(java.lang.CharSequence,android.text.TextDirectionHeuristic,boolean)](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#unicodeWrap(kotlin.CharSequence,%20android.text.TextDirectionHeuristic,%20kotlin.Boolean)), but assumes`isolate`is true. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [unicodeWrap](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#unicodeWrap(kotlin.CharSequence,%20android.text.TextDirectionHeuristic,%20kotlin.Boolean))`(`str:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`, `heuristic:` ` [TextDirectionHeuristic](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristic)!`, `isolate:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Operates like [unicodeWrap(java.lang.String,android.text.TextDirectionHeuristic,boolean)](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#unicodeWrap(kotlin.String,%20android.text.TextDirectionHeuristic,%20kotlin.Boolean)), but takes a CharSequence instead of a string |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [unicodeWrap](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#unicodeWrap(kotlin.CharSequence,%20kotlin.Boolean))`(`str:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `isolate:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Operates like [unicodeWrap(java.lang.CharSequence,android.text.TextDirectionHeuristic,boolean)](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#unicodeWrap(kotlin.CharSequence,%20android.text.TextDirectionHeuristic,%20kotlin.Boolean)), but uses the formatter's default direction estimation algorithm. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [unicodeWrap](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#unicodeWrap(kotlin.String))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Operates like [unicodeWrap(java.lang.String,android.text.TextDirectionHeuristic,boolean)](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#unicodeWrap(kotlin.String,%20android.text.TextDirectionHeuristic,%20kotlin.Boolean)), but uses the formatter's default direction estimation algorithm and assumes`isolate`is true. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [unicodeWrap](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#unicodeWrap(kotlin.String,%20android.text.TextDirectionHeuristic))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `heuristic:` ` [TextDirectionHeuristic](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristic)!`)` Operates like [unicodeWrap(java.lang.String,android.text.TextDirectionHeuristic,boolean)](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#unicodeWrap(kotlin.String,%20android.text.TextDirectionHeuristic,%20kotlin.Boolean)), but assumes`isolate`is true. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [unicodeWrap](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#unicodeWrap(kotlin.String,%20android.text.TextDirectionHeuristic,%20kotlin.Boolean))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `heuristic:` ` [TextDirectionHeuristic](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristic)!`, `isolate:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Formats a string of given directionality for use in plain-text output of the context directionality, so an opposite-directionality string is neither garbled nor garbles its surroundings. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [unicodeWrap](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#unicodeWrap(kotlin.String,%20kotlin.Boolean))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `isolate:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Operates like [unicodeWrap(java.lang.String,android.text.TextDirectionHeuristic,boolean)](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#unicodeWrap(kotlin.String,%20android.text.TextDirectionHeuristic,%20kotlin.Boolean)), but uses the formatter's default direction estimation algorithm. |
| --- | --- |

## Public methods

### getInstance

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(): BidiFormatter!
```

Factory for creating an instance of BidiFormatter for the default locale directionality. This does not create any new objects, and returns already existing static instances. 

### getInstance

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(rtlContext: Boolean): BidiFormatter!
```

Factory for creating an instance of BidiFormatter given the context directionality. This does not create any new objects, and returns already existing static instances.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------|
| `rtlContext` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the context directionality is RTL. |

### getInstance

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(locale: Locale!): BidiFormatter!
```

Factory for creating an instance of BidiFormatter given the context locale. This does not create any new objects, and returns already existing static instances.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:The context locale. |

### getStereoReset

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStereoReset(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether directionality "reset" should also be done before a string being bidi-wrapped, not just after it. |

### isRtl

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isRtl(str: CharSequence!): Boolean
```

Operates like [isRtl(java.lang.String)](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#isRtl(kotlin.String)), but takes a CharSequence instead of a string

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `str` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:CharSequence whose directionality is to be estimated. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if`str`'s estimated overall directionality is RTL. Otherwise returns false. |

### isRtl

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isRtl(str: String!): Boolean
```

Estimates the directionality of a string using the default text direction heuristic.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:String whose directionality is to be estimated. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if`str`'s estimated overall directionality is RTL. Otherwise returns false. |

### isRtlContext

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isRtlContext(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the context directionality is RTL |

### unicodeWrap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unicodeWrap(str: CharSequence!): CharSequence!
```

Operates like [unicodeWrap(java.lang.CharSequence,android.text.TextDirectionHeuristic,boolean)](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#unicodeWrap(kotlin.CharSequence,%20android.text.TextDirectionHeuristic,%20kotlin.Boolean)), but uses the formatter's default direction estimation algorithm and assumes`isolate`is true.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------|
| `str` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The input CharSequence. |

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | Input CharSequence after applying the above processing. |

### unicodeWrap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unicodeWrap(
    str: CharSequence!, 
    heuristic: TextDirectionHeuristic!
): CharSequence!
```

Operates like [unicodeWrap(java.lang.CharSequence,android.text.TextDirectionHeuristic,boolean)](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#unicodeWrap(kotlin.CharSequence,%20android.text.TextDirectionHeuristic,%20kotlin.Boolean)), but assumes`isolate`is true.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `str` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The input CharSequence. |
| `heuristic` | [TextDirectionHeuristic](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristic)!:The algorithm to be used to estimate the CharSequence's overall direction. See [TextDirectionHeuristics](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristics) for pre-defined heuristics. |

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | Input CharSequence after applying the above processing. |

### unicodeWrap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unicodeWrap(
    str: CharSequence?, 
    heuristic: TextDirectionHeuristic!, 
    isolate: Boolean
): CharSequence?
```

Operates like [unicodeWrap(java.lang.String,android.text.TextDirectionHeuristic,boolean)](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#unicodeWrap(kotlin.String,%20android.text.TextDirectionHeuristic,%20kotlin.Boolean)), but takes a CharSequence instead of a string

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `str` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:The input CharSequence. This value may be`null`. |
| `heuristic` | [TextDirectionHeuristic](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristic)!:The algorithm to be used to estimate the CharSequence's overall direction. See [TextDirectionHeuristics](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristics) for pre-defined heuristics. |
| `isolate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether to directionally isolate the CharSequence to prevent it from garbling the content around it |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | Input CharSequence after applying the above processing.`null`if`str`is`null`. |

### unicodeWrap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unicodeWrap(
    str: CharSequence!, 
    isolate: Boolean
): CharSequence!
```

Operates like [unicodeWrap(java.lang.CharSequence,android.text.TextDirectionHeuristic,boolean)](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#unicodeWrap(kotlin.CharSequence,%20android.text.TextDirectionHeuristic,%20kotlin.Boolean)), but uses the formatter's default direction estimation algorithm.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `str` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The input CharSequence. |
| `isolate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether to directionally isolate the CharSequence to prevent it from garbling the content around it |

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | Input CharSequence after applying the above processing. |

### unicodeWrap

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unicodeWrap(str: String!): String!
```

Operates like [unicodeWrap(java.lang.String,android.text.TextDirectionHeuristic,boolean)](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#unicodeWrap(kotlin.String,%20android.text.TextDirectionHeuristic,%20kotlin.Boolean)), but uses the formatter's default direction estimation algorithm and assumes`isolate`is true.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The input string. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | Input string after applying the above processing. |

### unicodeWrap

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unicodeWrap(
    str: String!, 
    heuristic: TextDirectionHeuristic!
): String!
```

Operates like [unicodeWrap(java.lang.String,android.text.TextDirectionHeuristic,boolean)](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#unicodeWrap(kotlin.String,%20android.text.TextDirectionHeuristic,%20kotlin.Boolean)), but assumes`isolate`is true.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The input string. |
| `heuristic` | [TextDirectionHeuristic](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristic)!:The algorithm to be used to estimate the string's overall direction. See [TextDirectionHeuristics](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristics) for pre-defined heuristics. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | Input string after applying the above processing. |

### unicodeWrap

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unicodeWrap(
    str: String?, 
    heuristic: TextDirectionHeuristic!, 
    isolate: Boolean
): String?
```

Formats a string of given directionality for use in plain-text output of the context directionality, so an opposite-directionality string is neither garbled nor garbles its surroundings. This makes use of Unicode bidi formatting characters.

The algorithm: In case the given directionality doesn't match the context directionality, wraps the string with Unicode bidi formatting characters: RLE+`str`+PDF for RTL text, or LRE+`str`+PDF for LTR text.

If`isolate`, directionally isolates the string so that it does not garble its surroundings. Currently, this is done by "resetting" the directionality after the string by appending a trailing Unicode bidi mark matching the context directionality (LRM or RLM) when either the overall directionality or the exit directionality of the string is opposite to that of the context. Unless the formatter was built using [Builder.stereoReset(boolean)](https://developer.android.com/reference/kotlin/android/text/BidiFormatter.Builder#stereoReset(kotlin.Boolean))with a`false`argument, also prepends a Unicode bidi mark matching the context directionality when either the overall directionality or the entry directionality of the string is opposite to that of the context. Note that as opposed to the overall directionality, the entry and exit directionalities are determined from the string itself.

Does \*not\* do HTML-escaping.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The input string. This value may be`null`. |
| `heuristic` | [TextDirectionHeuristic](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristic)!:The algorithm to be used to estimate the string's overall direction. See [TextDirectionHeuristics](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristics) for pre-defined heuristics. |
| `isolate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether to directionally isolate the string to prevent it from garbling the content around it |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | Input string after applying the above processing.`null`if`str`is`null`. |

### unicodeWrap

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unicodeWrap(
    str: String!, 
    isolate: Boolean
): String!
```

Operates like [unicodeWrap(java.lang.String,android.text.TextDirectionHeuristic,boolean)](https://developer.android.com/reference/kotlin/android/text/BidiFormatter#unicodeWrap(kotlin.String,%20android.text.TextDirectionHeuristic,%20kotlin.Boolean)), but uses the formatter's default direction estimation algorithm.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The input string. |
| `isolate` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether to directionally isolate the string to prevent it from garbling the content around it |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | Input string after applying the above processing. |
