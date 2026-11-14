# Matcher

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Matcher

```
class Matcher : MatchResult
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.regex.Matcher](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#) |

An engine that performs match operations on a by interpreting a [Pattern](https://developer.android.com/reference/kotlin/java/util/regex/Pattern).

A matcher is created from a pattern by invoking the pattern's [matcher](https://developer.android.com/reference/kotlin/java/util/regex/Pattern#matcher(kotlin.CharSequence))method. Once created, a matcher can be used to perform three different kinds of match operations:

- The [matches](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#matches())method attempts to match the entire input sequence against the pattern.
- The [lookingAt](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#lookingAt())method attempts to match the input sequence, starting at the beginning, against the pattern.
- The #find method scans the input sequence looking for the next subsequence that matches the pattern.

Each of these methods returns a boolean indicating success or failure. More information about a successful match can be obtained by querying the state of the matcher.

A matcher finds matches in a subset of its input called the*region* . By default, the region contains all of the matcher's input. The region can be modified via the [region](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#region(kotlin.Int,%20kotlin.Int))method and queried via the [regionStart](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#regionStart())and [regionEnd](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#regionEnd())methods. The way that the region boundaries interact with some pattern constructs can be changed. See [useAnchoringBounds](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#useAnchoringBounds(kotlin.Boolean))and [useTransparentBounds](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#useTransparentBounds(kotlin.Boolean))for more details.

This class also defines methods for replacing matched subsequences with new strings whose contents can, if desired, be computed from the match result. The #appendReplacement and #appendTail methods can be used in tandem in order to collect the result into an existing string buffer or string builder. Alternatively, the more convenient #replaceAll method can be used to create a string in which every matching subsequence in the input sequence is replaced.

The explicit state of a matcher includes the start and end indices of the most recent successful match. It also includes the start and end indices of the input subsequence captured by each [capturing group](https://developer.android.com/reference/kotlin/java/util/regex/Pattern#cg) in the pattern as well as a total count of such subsequences. As a convenience, methods are also provided for returning these captured subsequences in string form.

The explicit state of a matcher is initially undefined; attempting to query any part of it before a successful match will cause an [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) to be thrown. The explicit state of a matcher is recomputed by every match operation.

The implicit state of a matcher includes the input character sequence as well as the*append position*, which is initially zero and is updated by the #appendReplacement method.

A matcher may be reset explicitly by invoking its [reset()](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#reset())method or, if a new input sequence is desired, its [reset(CharSequence)](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#reset(kotlin.CharSequence))method. Resetting a matcher discards its explicit state information and sets the append position to zero.

Instances of this class are not safe for use by multiple concurrent threads.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Matcher](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#) | [appendReplacement](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#appendReplacement(java.lang.StringBuffer,%20kotlin.String))`(`sb:` ` [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)`, `replacement:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Implements a non-terminal append-and-replace step. |
| [Matcher](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#) | [appendReplacement](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#appendReplacement(java.lang.StringBuilder,%20kotlin.String))`(`sb:` ` [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)`, `replacement:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Implements a non-terminal append-and-replace step. |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#) | [appendTail](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#appendTail(java.lang.StringBuffer))`(`sb:` ` [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)`)` Implements a terminal append-and-replace step. |
| --- | --- |
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#) | [appendTail](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#appendTail(java.lang.StringBuilder))`(`sb:` ` [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)`)` Implements a terminal append-and-replace step. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [end](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#end())`()` Returns the offset after the last character matched. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [end](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#end(kotlin.Int))`(`group:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the offset after the last character of the subsequence captured by the given group during the previous match operation. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [end](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#end(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the offset after the last character of the subsequence captured by the given [named-capturing group](https://developer.android.com/reference/kotlin/java/util/regex/Pattern#groupname) during the previous match operation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [find](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#find())`()` Attempts to find the next subsequence of the input sequence that matches the pattern. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [find](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#find(kotlin.Int))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Resets this matcher and then attempts to find the next subsequence of the input sequence that matches the pattern, starting at the specified index. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [group](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#group())`()` Returns the input subsequence matched by the previous match. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [group](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#group(kotlin.Int))`(`group:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the input subsequence captured by the given group during the previous match operation. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [group](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#group(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the input subsequence captured by the given [named-capturing group](https://developer.android.com/reference/kotlin/java/util/regex/Pattern#groupname) during the previous match operation. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [groupCount](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#groupCount())`()` Returns the number of capturing groups in this matcher's pattern. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasAnchoringBounds](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#hasAnchoringBounds())`()` Queries the anchoring of region bounds for this matcher. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasTransparentBounds](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#hasTransparentBounds())`()` Queries the transparency of region bounds for this matcher. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hitEnd](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#hitEnd())`()` Returns true if the end of input was hit by the search engine in the last match operation performed by this matcher. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [lookingAt](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#lookingAt())`()` Attempts to match the input sequence, starting at the beginning of the region, against the pattern. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [matches](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#matches())`()` Attempts to match the entire region against the pattern. |
| --- | --- |
| [Pattern](https://developer.android.com/reference/kotlin/java/util/regex/Pattern) | [pattern](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#pattern())`()` Returns the pattern that is interpreted by this matcher. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [quoteReplacement](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#quoteReplacement(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns a literal replacement`String`for the specified`String`. |
| [Matcher](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#) | [region](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#region(kotlin.Int,%20kotlin.Int))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the limits of this matcher's region. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [regionEnd](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#regionEnd())`()` Reports the end index (exclusive) of this matcher's region. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [regionStart](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#regionStart())`()` Reports the start index of this matcher's region. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [replaceAll](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#replaceAll(kotlin.String))`(`replacement:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Replaces every subsequence of the input sequence that matches the pattern with the given replacement string. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [replaceAll](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#replaceAll(java.util.function.Function))`(`replacer:` ` [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)< [MatchResult](https://developer.android.com/reference/kotlin/java/util/regex/MatchResult)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Replaces every subsequence of the input sequence that matches the pattern with the result of applying the given replacer function to the match result of this matcher corresponding to that subsequence. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [replaceFirst](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#replaceFirst(kotlin.String))`(`replacement:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Replaces the first subsequence of the input sequence that matches the pattern with the given replacement string. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [replaceFirst](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#replaceFirst(java.util.function.Function))`(`replacer:` ` [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)< [MatchResult](https://developer.android.com/reference/kotlin/java/util/regex/MatchResult)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Replaces the first subsequence of the input sequence that matches the pattern with the result of applying the given replacer function to the match result of this matcher corresponding to that subsequence. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requireEnd](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#requireEnd())`()` Returns true if more input could change a positive match into a negative one. |
| [Matcher](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#) | [reset](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#reset())`()` Resets this matcher. |
| [Matcher](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#) | [reset](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#reset(kotlin.CharSequence))`(`input:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`)` Resets this matcher with a new input sequence. |
| --- | --- |
| [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#)\< [MatchResult](https://developer.android.com/reference/kotlin/java/util/regex/MatchResult)!\> | [results](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#results())`()` Returns a stream of match results for each subsequence of the input sequence that matches the pattern. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [start](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#start())`()` Returns the start index of the previous match. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [start](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#start(kotlin.Int))`(`group:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the start index of the subsequence captured by the given group during the previous match operation. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [start](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#start(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the start index of the subsequence captured by the given [named-capturing group](https://developer.android.com/reference/kotlin/java/util/regex/Pattern#groupname) during the previous match operation. |
| [MatchResult](https://developer.android.com/reference/kotlin/java/util/regex/MatchResult) | [toMatchResult](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#toMatchResult())`()` Returns the match state of this matcher as a [MatchResult](https://developer.android.com/reference/kotlin/java/util/regex/MatchResult). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#toString())`()` Returns the string representation of this matcher. |
| --- | --- |
| [Matcher](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#) | [useAnchoringBounds](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#useAnchoringBounds(kotlin.Boolean))`(`b:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the anchoring of region bounds for this matcher. |
| [Matcher](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#) | [usePattern](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#usePattern(java.util.regex.Pattern))`(`newPattern:` ` [Pattern](https://developer.android.com/reference/kotlin/java/util/regex/Pattern)`)` Changes the`Pattern`that this`Matcher`uses to find matches with. |
| [Matcher](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#) | [useTransparentBounds](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#useTransparentBounds(kotlin.Boolean))`(`b:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the transparency of region bounds for this matcher. |
| --- | --- |

## Public methods

### appendReplacement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun appendReplacement(
    sb: StringBuffer, 
    replacement: String
): Matcher
```

Implements a non-terminal append-and-replace step.

This method performs the following actions:

1. It reads characters from the input sequence, starting at the append position, and appends them to the given string buffer. It stops after reading the last character preceding the previous match, that is, the character at index [start()](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#start())`-``1`.
2. It appends the given replacement string to the string buffer.
3. It sets the append position of this matcher to the index of the last character matched, plus one, that is, to [end()](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#end()).

The replacement string may contain references to subsequences captured during the previous match: Each occurrence of`${`*name* `}`or`$`*g* will be replaced by the result of evaluating the corresponding [group(name)](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#group(kotlin.String))or [group(g)](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#group(kotlin.Int))respectively. For`$`*g* , the first number after the`$`is always treated as part of the group reference. Subsequent numbers are incorporated into g if they would form a legal group reference. Only the numerals '0' through '9' are considered as potential components of the group reference. If the second group matched the string`"foo"`, for example, then passing the replacement string`"$2bar"`would cause`"foobar"`to be appended to the string buffer. A dollar sign (`$`) may be included as a literal in the replacement string by preceding it with a backslash (`\$`).

Note that backslashes (`\`) and dollar signs (`$`) in the replacement string may cause the results to be different than if it were being treated as a literal replacement string. Dollar signs may be treated as references to captured subsequences as described above, and backslashes are used to escape literal characters in the replacement string.

This method is intended to be used in a loop together with the [appendTail](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#appendTail(java.lang.StringBuffer))and [find](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#find())methods. The following code, for example, writes`one dog two dogs in the yard`to the standard-output stream: 

```kotlin
Pattern p = Pattern.compile("cat");
  Matcher m = p.matcher("one cat two cats in the yard");
  StringBuffer sb = new StringBuffer();
  while (m.find()) {
      m.appendReplacement(sb, "dog");
  }
  m.appendTail(sb);
  System.out.println(sb.toString());
```

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------|
| `sb` | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#):The target string buffer |
| `replacement` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The replacement string |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [Matcher](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#) | This matcher |

| Exceptions ||
|---------------------------------------|------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If no match has yet been attempted, or if the previous match operation failed |
| `java.lang.IllegalArgumentException` | If the replacement string refers to a named-capturing group that does not exist in the pattern |
| `java.lang.IndexOutOfBoundsException` | If the replacement string refers to a capturing group that does not exist in the pattern |
| --- | --- |

### appendReplacement

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun appendReplacement(
    sb: StringBuilder, 
    replacement: String
): Matcher
```

Implements a non-terminal append-and-replace step.

This method performs the following actions:

1. It reads characters from the input sequence, starting at the append position, and appends them to the given string builder. It stops after reading the last character preceding the previous match, that is, the character at index [start()](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#start())`-``1`.
2. It appends the given replacement string to the string builder.
3. It sets the append position of this matcher to the index of the last character matched, plus one, that is, to [end()](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#end()).

The replacement string may contain references to subsequences captured during the previous match: Each occurrence of`$`*g* will be replaced by the result of evaluating [group](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#group(kotlin.Int))`(`*g* `)`. The first number after the`$`is always treated as part of the group reference. Subsequent numbers are incorporated into g if they would form a legal group reference. Only the numerals '0' through '9' are considered as potential components of the group reference. If the second group matched the string`"foo"`, for example, then passing the replacement string`"$2bar"`would cause`"foobar"`to be appended to the string builder. A dollar sign (`$`) may be included as a literal in the replacement string by preceding it with a backslash (`\$`).

Note that backslashes (`\`) and dollar signs (`$`) in the replacement string may cause the results to be different than if it were being treated as a literal replacement string. Dollar signs may be treated as references to captured subsequences as described above, and backslashes are used to escape literal characters in the replacement string.

This method is intended to be used in a loop together with the [appendTail](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#appendTail(java.lang.StringBuilder))and [find](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#find())methods. The following code, for example, writes`one dog two dogs in the yard`to the standard-output stream: 

```kotlin
Pattern p = Pattern.compile("cat");
  Matcher m = p.matcher("one cat two cats in the yard");
  StringBuilder sb = new StringBuilder();
  while (m.find()) {
      m.appendReplacement(sb, "dog");
  }
  m.appendTail(sb);
  System.out.println(sb.toString());
```

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------|
| `sb` | [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#):The target string builder |
| `replacement` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The replacement string |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [Matcher](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#) | This matcher |

| Exceptions ||
|---------------------------------------|------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If no match has yet been attempted, or if the previous match operation failed |
| `java.lang.IllegalArgumentException` | If the replacement string refers to a named-capturing group that does not exist in the pattern |
| `java.lang.IndexOutOfBoundsException` | If the replacement string refers to a capturing group that does not exist in the pattern |
| --- | --- |

### appendTail

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun appendTail(sb: StringBuffer): StringBuffer
```

Implements a terminal append-and-replace step.

This method reads characters from the input sequence, starting at the append position, and appends them to the given string buffer. It is intended to be invoked after one or more invocations of the [appendReplacement](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#appendReplacement(java.lang.StringBuffer,%20kotlin.String))method in order to copy the remainder of the input sequence.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------|
| `sb` | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#):The target string buffer |

| Return ||
|---------------------------------------------------------------------------------------------|--------------------------|
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#) | The target string buffer |

### appendTail

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun appendTail(sb: StringBuilder): StringBuilder
```

Implements a terminal append-and-replace step.

This method reads characters from the input sequence, starting at the append position, and appends them to the given string builder. It is intended to be invoked after one or more invocations of the [appendReplacement](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#appendReplacement(java.lang.StringBuilder,%20kotlin.String))method in order to copy the remainder of the input sequence.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------|
| `sb` | [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#):The target string builder |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------|
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#) | The target string builder |

### end

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun end(): Int
```

Returns the offset after the last character matched.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The offset after the last character matched |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If no match has yet been attempted, or if the previous match operation failed |

### end

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun end(group: Int): Int
```

Returns the offset after the last character of the subsequence captured by the given group during the previous match operation.

[Capturing groups](https://developer.android.com/reference/kotlin/java/util/regex/Pattern#cg) are indexed from left to right, starting at one. Group zero denotes the entire pattern, so the expression*m.* `end(0)`is equivalent to*m.* `end()`.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------|
| `group` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of a capturing group in this matcher's pattern |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The offset after the last character captured by the group, or`-1`if the match was successful but the group itself did not match anything |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If no match has yet been attempted, or if the previous match operation failed |
| `java.lang.IndexOutOfBoundsException` | If there is no capturing group in the pattern with the given index |

### end

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun end(name: String): Int
```

Returns the offset after the last character of the subsequence captured by the given [named-capturing group](https://developer.android.com/reference/kotlin/java/util/regex/Pattern#groupname) during the previous match operation.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of a named-capturing group in this matcher's pattern |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The offset after the last character captured by the group, or`-1`if the match was successful but the group itself did not match anything |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If no match has yet been attempted, or if the previous match operation failed |
| `java.lang.IllegalArgumentException` | If there is no capturing group in the pattern with the given name |

### find

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun find(): Boolean
```

Attempts to find the next subsequence of the input sequence that matches the pattern.

This method starts at the beginning of this matcher's region, or, if a previous invocation of the method was successful and the matcher has not since been reset, at the first character not matched by the previous match.

If the match succeeds then more information can be obtained via the`start`,`end`, and`group`methods.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, a subsequence of the input sequence matches this matcher's pattern |

### find

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun find(start: Int): Boolean
```

Resets this matcher and then attempts to find the next subsequence of the input sequence that matches the pattern, starting at the specified index.

If the match succeeds then more information can be obtained via the`start`,`end`, and`group`methods, and subsequent invocations of the [find()](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#find())method will start at the first character not matched by this match.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index to start searching for a match |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, a subsequence of the input sequence starting at the given index matches this matcher's pattern |

| Exceptions ||
|---------------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If start is less than zero or if start is greater than the length of the input sequence. |

### group

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun group(): String
```

Returns the input subsequence matched by the previous match.

For a matcher*m* with input sequence*s* , the expressions*m.* `group()`and*s.* `substring(`*m.* `start(),`*m.* `end())`are equivalent.

Note that some patterns, for example`a*`, match the empty string. This method will return the empty string when the pattern successfully matches the empty string in the input.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The (possibly empty) subsequence matched by the previous match, in string form |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If no match has yet been attempted, or if the previous match operation failed |

### group

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun group(group: Int): String?
```

Returns the input subsequence captured by the given group during the previous match operation.

For a matcher*m* , input sequence*s* , and group index*g* , the expressions*m.* `group(`*g* `)`and*s.* `substring(`*m.* `start(`*g* `),`*m.* `end(`*g* `))`are equivalent.

[Capturing groups](https://developer.android.com/reference/kotlin/java/util/regex/Pattern#cg) are indexed from left to right, starting at one. Group zero denotes the entire pattern, so the expression`m.group(0)`is equivalent to`m.group()`.

If the match was successful but the group specified failed to match any part of the input sequence, then`null`is returned. Note that some groups, for example`(a*)`, match the empty string. This method will return the empty string when such a group successfully matches the empty string in the input.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------|
| `group` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of a capturing group in this matcher's pattern |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | The (possibly empty) subsequence captured by the group during the previous match, or`null`if the group failed to match part of the input |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If no match has yet been attempted, or if the previous match operation failed |
| `java.lang.IndexOutOfBoundsException` | If there is no capturing group in the pattern with the given index |

### group

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun group(name: String): String?
```

Returns the input subsequence captured by the given [named-capturing group](https://developer.android.com/reference/kotlin/java/util/regex/Pattern#groupname) during the previous match operation.

If the match was successful but the group specified failed to match any part of the input sequence, then`null`is returned. Note that some groups, for example`(a*)`, match the empty string. This method will return the empty string when such a group successfully matches the empty string in the input.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of a named-capturing group in this matcher's pattern |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | The (possibly empty) subsequence captured by the named group during the previous match, or`null`if the group failed to match part of the input |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If no match has yet been attempted, or if the previous match operation failed |
| `java.lang.IllegalArgumentException` | If there is no capturing group in the pattern with the given name |

### groupCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun groupCount(): Int
```

Returns the number of capturing groups in this matcher's pattern.

Group zero denotes the entire pattern by convention. It is not included in this count.

Any non-negative integer smaller than or equal to the value returned by this method is guaranteed to be a valid group index for this matcher.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of capturing groups in this matcher's pattern |

### hasAnchoringBounds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasAnchoringBounds(): Boolean
```

Queries the anchoring of region bounds for this matcher.

This method returns`true`if this matcher uses*anchoring* bounds,`false`otherwise.

See [useAnchoringBounds](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#useAnchoringBounds(kotlin.Boolean))for a description of anchoring bounds.

By default, a matcher uses anchoring region boundaries.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`iff this matcher is using anchoring bounds,`false`otherwise. |

**See Also**

- [java.util.regex.Matcher#useAnchoringBounds(boolean)](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#useAnchoringBounds(kotlin.Boolean)) 

### hasTransparentBounds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasTransparentBounds(): Boolean
```

Queries the transparency of region bounds for this matcher.

This method returns`true`if this matcher uses*transparent* bounds,`false`if it uses*opaque*bounds.

See [useTransparentBounds](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#useTransparentBounds(kotlin.Boolean))for a description of transparent and opaque bounds.

By default, a matcher uses opaque region boundaries.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`iff this matcher is using transparent bounds,`false`otherwise. |

**See Also**

- [java.util.regex.Matcher#useTransparentBounds(boolean)](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#useTransparentBounds(kotlin.Boolean)) 

### hitEnd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hitEnd(): Boolean
```

Returns true if the end of input was hit by the search engine in the last match operation performed by this matcher.

When this method returns true, then it is possible that more input would have changed the result of the last search.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true iff the end of input was hit in the last match; false otherwise |

### lookingAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun lookingAt(): Boolean
```

Attempts to match the input sequence, starting at the beginning of the region, against the pattern.

Like the [matches](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#matches())method, this method always starts at the beginning of the region; unlike that method, it does not require that the entire region be matched.

If the match succeeds then more information can be obtained via the`start`,`end`, and`group`methods.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, a prefix of the input sequence matches this matcher's pattern |

### matches

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun matches(): Boolean
```

Attempts to match the entire region against the pattern.

If the match succeeds then more information can be obtained via the`start`,`end`, and`group`methods.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, the entire region sequence matches this matcher's pattern |

### pattern

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun pattern(): Pattern
```

Returns the pattern that is interpreted by this matcher.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [Pattern](https://developer.android.com/reference/kotlin/java/util/regex/Pattern) | The pattern for which this matcher was created |

### quoteReplacement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun quoteReplacement(s: String): String
```

Returns a literal replacement`String`for the specified`String`. This method produces a`String`that will work as a literal replacement`s`in the`appendReplacement`method of the [Matcher](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#) class. The`String`produced will match the sequence of characters in`s`treated as a literal sequence. Slashes ('\\') and dollar signs ('$') will be given no special meaning.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The string to be literalized |

| Return ||
|----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | A literal string replacement |

### region

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun region(
    start: Int, 
    end: Int
): Matcher
```

Sets the limits of this matcher's region. The region is the part of the input sequence that will be searched to find a match. Invoking this method resets the matcher, and then sets the region to start at the index specified by the`start`parameter and end at the index specified by the`end`parameter.

Depending on the transparency and anchoring being used (see [useTransparentBounds](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#useTransparentBounds(kotlin.Boolean))and [useAnchoringBounds](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#useAnchoringBounds(kotlin.Boolean))), certain constructs such as anchors may behave differently at or around the boundaries of the region.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index to start searching at (inclusive) |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index to end searching at (exclusive) |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [Matcher](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#) | this matcher |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If start or end is less than zero, if start is greater than the length of the input sequence, if end is greater than the length of the input sequence, or if start is greater than end. |

### regionEnd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun regionEnd(): Int
```

Reports the end index (exclusive) of this matcher's region. The searches this matcher conducts are limited to finding matches within [regionStart](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#regionStart())(inclusive) and [regionEnd](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#regionEnd())(exclusive).

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the ending point of this matcher's region |

### regionStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun regionStart(): Int
```

Reports the start index of this matcher's region. The searches this matcher conducts are limited to finding matches within [regionStart](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#regionStart())(inclusive) and [regionEnd](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#regionEnd())(exclusive).

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The starting point of this matcher's region |

### replaceAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun replaceAll(replacement: String): String
```

Replaces every subsequence of the input sequence that matches the pattern with the given replacement string.

This method first resets this matcher. It then scans the input sequence looking for matches of the pattern. Characters that are not part of any match are appended directly to the result string; each match is replaced in the result by the replacement string. The replacement string may contain references to captured subsequences as in the #appendReplacement method.

Note that backslashes (`\`) and dollar signs (`$`) in the replacement string may cause the results to be different than if it were being treated as a literal replacement string. Dollar signs may be treated as references to captured subsequences as described above, and backslashes are used to escape literal characters in the replacement string.

Given the regular expression`a*b`, the input`"aabfooaabfooabfoob"`, and the replacement string`"-"`, an invocation of this method on a matcher for that expression would yield the string`"-foo-foo-foo-"`.

Invoking this method changes this matcher's state. If the matcher is to be used in further matching operations then it should first be reset.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------|
| `replacement` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The replacement string |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The string constructed by replacing each matching subsequence by the replacement string, substituting captured subsequences as needed |

### replaceAll

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun replaceAll(replacer: Function<MatchResult!, String!>): String
```

Replaces every subsequence of the input sequence that matches the pattern with the result of applying the given replacer function to the match result of this matcher corresponding to that subsequence. Exceptions thrown by the function are relayed to the caller.

This method first resets this matcher. It then scans the input sequence looking for matches of the pattern. Characters that are not part of any match are appended directly to the result string; each match is replaced in the result by the applying the replacer function that returns a replacement string. Each replacement string may contain references to captured subsequences as in the #appendReplacement method.

Note that backslashes (`\`) and dollar signs (`$`) in a replacement string may cause the results to be different than if it were being treated as a literal replacement string. Dollar signs may be treated as references to captured subsequences as described above, and backslashes are used to escape literal characters in the replacement string.

Given the regular expression`dog`, the input`"zzzdogzzzdogzzz"`, and the function`mr -> mr.group().toUpperCase()`, an invocation of this method on a matcher for that expression would yield the string`"zzzDOGzzzDOGzzz"`.

Invoking this method changes this matcher's state. If the matcher is to be used in further matching operations then it should first be reset.

The replacer function should not modify this matcher's state during replacement. This method will, on a best-effort basis, throw a [java.util.ConcurrentModificationException](https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException.html#) if such modification is detected.

The state of each match result passed to the replacer function is guaranteed to be constant only for the duration of the replacer function call and only if the replacer function does not modify this matcher's state.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `replacer` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\< [MatchResult](https://developer.android.com/reference/kotlin/java/util/regex/MatchResult)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:The function to be applied to the match result of this matcher that returns a replacement string. |

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The string constructed by replacing each matching subsequence with the result of applying the replacer function to that matched subsequence, substituting captured subsequences as needed. |

| Exceptions ||
|---------------------------------------------|-----------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the replacer function is null |
| `java.util.ConcurrentModificationException` | if it is detected, on a best-effort basis, that the replacer function modified this matcher's state |

### replaceFirst

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun replaceFirst(replacement: String): String
```

Replaces the first subsequence of the input sequence that matches the pattern with the given replacement string.

This method first resets this matcher. It then scans the input sequence looking for a match of the pattern. Characters that are not part of the match are appended directly to the result string; the match is replaced in the result by the replacement string. The replacement string may contain references to captured subsequences as in the #appendReplacement method.

Note that backslashes (`\`) and dollar signs (`$`) in the replacement string may cause the results to be different than if it were being treated as a literal replacement string. Dollar signs may be treated as references to captured subsequences as described above, and backslashes are used to escape literal characters in the replacement string.

Given the regular expression`dog`, the input`"zzzdogzzzdogzzz"`, and the replacement string`"cat"`, an invocation of this method on a matcher for that expression would yield the string`"zzzcatzzzdogzzz"`.

Invoking this method changes this matcher's state. If the matcher is to be used in further matching operations then it should first be reset.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------|
| `replacement` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The replacement string |

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The string constructed by replacing the first matching subsequence by the replacement string, substituting captured subsequences as needed |

### replaceFirst

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun replaceFirst(replacer: Function<MatchResult!, String!>): String
```

Replaces the first subsequence of the input sequence that matches the pattern with the result of applying the given replacer function to the match result of this matcher corresponding to that subsequence. Exceptions thrown by the replace function are relayed to the caller.

This method first resets this matcher. It then scans the input sequence looking for a match of the pattern. Characters that are not part of the match are appended directly to the result string; the match is replaced in the result by the applying the replacer function that returns a replacement string. The replacement string may contain references to captured subsequences as in the #appendReplacement method.

Note that backslashes (`\`) and dollar signs (`$`) in the replacement string may cause the results to be different than if it were being treated as a literal replacement string. Dollar signs may be treated as references to captured subsequences as described above, and backslashes are used to escape literal characters in the replacement string.

Given the regular expression`dog`, the input`"zzzdogzzzdogzzz"`, and the function`mr -> mr.group().toUpperCase()`, an invocation of this method on a matcher for that expression would yield the string`"zzzDOGzzzdogzzz"`.

Invoking this method changes this matcher's state. If the matcher is to be used in further matching operations then it should first be reset.

The replacer function should not modify this matcher's state during replacement. This method will, on a best-effort basis, throw a [java.util.ConcurrentModificationException](https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException.html#) if such modification is detected.

The state of the match result passed to the replacer function is guaranteed to be constant only for the duration of the replacer function call and only if the replacer function does not modify this matcher's state.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `replacer` | [Function](https://developer.android.com/reference/kotlin/java/util/function/Function.html#)\< [MatchResult](https://developer.android.com/reference/kotlin/java/util/regex/MatchResult)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:The function to be applied to the match result of this matcher that returns a replacement string. |

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The string constructed by replacing the first matching subsequence with the result of applying the replacer function to the matched subsequence, substituting captured subsequences as needed. |

| Exceptions ||
|---------------------------------------------|-----------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the replacer function is null |
| `java.util.ConcurrentModificationException` | if it is detected, on a best-effort basis, that the replacer function modified this matcher's state |

### requireEnd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun requireEnd(): Boolean
```

Returns true if more input could change a positive match into a negative one.

If this method returns true, and a match was found, then more input could cause the match to be lost. If this method returns false and a match was found, then more input might change the match but the match won't be lost. If a match was not found, then requireEnd has no meaning.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true iff more input could change a positive match into a negative one. |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun reset(): Matcher
```

Resets this matcher.

Resetting a matcher discards all of its explicit state information and sets its append position to zero. The matcher's region is set to the default region, which is its entire character sequence. The anchoring and transparency of this matcher's region boundaries are unaffected.

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [Matcher](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#) | This matcher |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun reset(input: CharSequence): Matcher
```

Resets this matcher with a new input sequence.

Resetting a matcher discards all of its explicit state information and sets its append position to zero. The matcher's region is set to the default region, which is its entire character sequence. The anchoring and transparency of this matcher's region boundaries are unaffected.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------|
| `input` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):The new input character sequence |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [Matcher](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#) | This matcher |

### results

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun results(): Stream<MatchResult!>
```

Returns a stream of match results for each subsequence of the input sequence that matches the pattern. The match results occur in the same order as the matching subsequences in the input sequence.

Each match result is produced as if by [toMatchResult()](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#toMatchResult()).

This method does not reset this matcher. Matching starts on initiation of the terminal stream operation either at the beginning of this matcher's region, or, if the matcher has not since been reset, at the first character not matched by a previous match.

If the matcher is to be used for further matching operations after the terminal stream operation completes then it should be first reset.

This matcher's state should not be modified during execution of the returned stream's pipeline. The returned stream's source`Spliterator`is*fail-fast* and will, on a best-effort basis, throw a [java.util.ConcurrentModificationException](https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException.html#) if such modification is detected.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#)< [MatchResult](https://developer.android.com/reference/kotlin/java/util/regex/MatchResult)!> | a sequential stream of match results. |

### start

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun start(): Int
```

Returns the start index of the previous match.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The index of the first character matched |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If no match has yet been attempted, or if the previous match operation failed |

### start

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun start(group: Int): Int
```

Returns the start index of the subsequence captured by the given group during the previous match operation.

[Capturing groups](https://developer.android.com/reference/kotlin/java/util/regex/Pattern#cg) are indexed from left to right, starting at one. Group zero denotes the entire pattern, so the expression*m.* `start(0)`is equivalent to*m.* `start()`.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------|
| `group` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of a capturing group in this matcher's pattern |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The index of the first character captured by the group, or`-1`if the match was successful but the group itself did not match anything |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If no match has yet been attempted, or if the previous match operation failed |
| `java.lang.IndexOutOfBoundsException` | If there is no capturing group in the pattern with the given index |

### start

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun start(name: String): Int
```

Returns the start index of the subsequence captured by the given [named-capturing group](https://developer.android.com/reference/kotlin/java/util/regex/Pattern#groupname) during the previous match operation.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of a named-capturing group in this matcher's pattern |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The index of the first character captured by the group, or`-1`if the match was successful but the group itself did not match anything |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If no match has yet been attempted, or if the previous match operation failed |
| `java.lang.IllegalArgumentException` | If there is no capturing group in the pattern with the given name |

### toMatchResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toMatchResult(): MatchResult
```

Returns the match state of this matcher as a [MatchResult](https://developer.android.com/reference/kotlin/java/util/regex/MatchResult). The result is unaffected by subsequent operations performed upon this matcher.

| Return ||
|-------------------------------------------------------------------------------------------|----------------------------------------------|
| [MatchResult](https://developer.android.com/reference/kotlin/java/util/regex/MatchResult) | a`MatchResult`with the state of this matcher |

| Exceptions ||
|-----------------------------------|-----------------------|
| `java.lang.IllegalStateException` | if no match is found. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns the string representation of this matcher. The string representation of a`Matcher`contains information that may be useful for debugging. The exact format is unspecified.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The string representation of this matcher |

### useAnchoringBounds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun useAnchoringBounds(b: Boolean): Matcher
```

Sets the anchoring of region bounds for this matcher.

Invoking this method with an argument of`true`will set this matcher to use*anchoring* bounds. If the boolean argument is`false`, then*non-anchoring*bounds will be used.

Using anchoring bounds, the boundaries of this matcher's region match anchors such as \^ and $.

Without anchoring bounds, the boundaries of this matcher's region will not match anchors such as \^ and $.

By default, a matcher uses anchoring region boundaries.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `b` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):a boolean indicating whether or not to use anchoring bounds. |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [Matcher](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#) | this matcher |

**See Also**

- [java.util.regex.Matcher#hasAnchoringBounds](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#hasAnchoringBounds()) 

### usePattern

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun usePattern(newPattern: Pattern): Matcher
```

Changes the`Pattern`that this`Matcher`uses to find matches with.

This method causes this matcher to lose information about the groups of the last match that occurred. The matcher's position in the input is maintained and its last append position is unaffected.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------|
| `newPattern` | [Pattern](https://developer.android.com/reference/kotlin/java/util/regex/Pattern):The new pattern used by this matcher |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [Matcher](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#) | This matcher |

| Exceptions ||
|--------------------------------------|------------------------|
| `java.lang.IllegalArgumentException` | If newPattern is`null` |

### useTransparentBounds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun useTransparentBounds(b: Boolean): Matcher
```

Sets the transparency of region bounds for this matcher.

Invoking this method with an argument of`true`will set this matcher to use*transparent* bounds. If the boolean argument is`false`, then*opaque*bounds will be used.

Using transparent bounds, the boundaries of this matcher's region are transparent to lookahead, lookbehind, and boundary matching constructs. Those constructs can see beyond the boundaries of the region to see if a match is appropriate.

Using opaque bounds, the boundaries of this matcher's region are opaque to lookahead, lookbehind, and boundary matching constructs that may try to see beyond them. Those constructs cannot look past the boundaries so they will fail to match anything outside of the region.

By default, a matcher uses opaque bounds.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `b` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):a boolean indicating whether to use opaque or transparent regions |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [Matcher](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#) | this matcher |

**See Also**

- [java.util.regex.Matcher#hasTransparentBounds](https://developer.android.com/reference/kotlin/java/util/regex/Matcher#hasTransparentBounds())
