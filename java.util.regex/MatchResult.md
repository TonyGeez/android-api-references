# MatchResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MatchResult

```
interface MatchResult
```

| [java.util.regex.MatchResult](MatchResult.md) |

| Known Direct Subclasses [Matcher](Matcher.md) |-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------| | [Matcher](Matcher.md) | An engine that performs match operations on a by interpreting a [Pattern](Pattern.md). | |
| --- | --- | --- | --- | --- | --- | --- |

The result of a match operation.

This interface contains query methods used to determine the results of a match against a regular expression. The match boundaries, groups and group boundaries can be seen but not modified through a`MatchResult`.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [end](MatchResult.md))`()` Returns the offset after the last character matched. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [end](MatchResult.md))`(`group:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the offset after the last character of the subsequence captured by the given group during this match. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [group](MatchResult.md))`()` Returns the input subsequence matched by the previous match. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [group](MatchResult.md))`(`group:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the input subsequence captured by the given group during the previous match operation. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [groupCount](MatchResult.md))`()` Returns the number of capturing groups in this match result's pattern. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [start](MatchResult.md))`()` Returns the start index of the match. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [start](MatchResult.md))`(`group:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the start index of the subsequence captured by the given group during this match. |

## Public methods

### end

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun end(): Int
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
abstract fun end(group: Int): Int
```

Returns the offset after the last character of the subsequence captured by the given group during this match.

[Capturing groups](Pattern.md) are indexed from left to right, starting at one. Group zero denotes the entire pattern, so the expression*m.* `end(0)`is equivalent to*m.* `end()`.

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

### group

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun group(): String!
```

Returns the input subsequence matched by the previous match.

For a matcher*m* with input sequence*s* , the expressions*m.* `group()`and*s.* `substring(`*m.* `start(),`*m.* `end())`are equivalent.

Note that some patterns, for example`a*`, match the empty string. This method will return the empty string when the pattern successfully matches the empty string in the input.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The (possibly empty) subsequence matched by the previous match, in string form |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If no match has yet been attempted, or if the previous match operation failed |

### group

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun group(group: Int): String!
```

Returns the input subsequence captured by the given group during the previous match operation.

For a matcher*m* , input sequence*s* , and group index*g* , the expressions*m.* `group(`*g* `)`and*s.* `substring(`*m.* `start(`*g* `),`*m.* `end(`*g* `))`are equivalent.

[Capturing groups](Pattern.md) are indexed from left to right, starting at one. Group zero denotes the entire pattern, so the expression`m.group(0)`is equivalent to`m.group()`.

If the match was successful but the group specified failed to match any part of the input sequence, then`null`is returned. Note that some groups, for example`(a*)`, match the empty string. This method will return the empty string when such a group successfully matches the empty string in the input.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------|
| `group` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of a capturing group in this matcher's pattern |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The (possibly empty) subsequence captured by the group during the previous match, or`null`if the group failed to match part of the input |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If no match has yet been attempted, or if the previous match operation failed |
| `java.lang.IndexOutOfBoundsException` | If there is no capturing group in the pattern with the given index |

### groupCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun groupCount(): Int
```

Returns the number of capturing groups in this match result's pattern.

Group zero denotes the entire pattern by convention. It is not included in this count.

Any non-negative integer smaller than or equal to the value returned by this method is guaranteed to be a valid group index for this matcher.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of capturing groups in this matcher's pattern |

### start

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun start(): Int
```

Returns the start index of the match.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The index of the first character matched |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If no match has yet been attempted, or if the previous match operation failed |

### start

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun start(group: Int): Int
```

Returns the start index of the subsequence captured by the given group during this match.

[Capturing groups](Pattern.md) are indexed from left to right, starting at one. Group zero denotes the entire pattern, so the expression*m.* `start(0)`is equivalent to*m.* `start()`.

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
