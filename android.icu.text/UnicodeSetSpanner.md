# UnicodeSetSpanner

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnicodeSetSpanner

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/UnicodeSetSpanner "View this page in Java") 
| --- | --- |

```
open class UnicodeSetSpanner
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.UnicodeSetSpanner](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner#) |

A helper class used to count, replace, and trim CharSequences based on UnicodeSet matches. An instance is immutable (and thus thread-safe) iff the source UnicodeSet is frozen.

**Note:** The counting, deletion, and replacement depend on alternating a [SpanCondition](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.SpanCondition) with its inverse. That is, the code spans, then spans for the inverse, then spans, and so on. For the inverse, the following mapping is used:

- [UnicodeSet.SpanCondition.SIMPLE](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.SpanCondition)→ [UnicodeSet.SpanCondition.NOT_CONTAINED](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.SpanCondition)
- [UnicodeSet.SpanCondition.CONTAINED](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.SpanCondition)→ [UnicodeSet.SpanCondition.NOT_CONTAINED](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.SpanCondition)
- [UnicodeSet.SpanCondition.NOT_CONTAINED](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.SpanCondition)→ [UnicodeSet.SpanCondition.SIMPLE](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.SpanCondition)

These are actually not complete inverses. However, the alternating works because there are no gaps. For example, with \[a{ab}{bc}\], you get the following behavior when scanning forward:

| SIMPLE | xxx\[ab\]cyyy |
| --- | --- |
| CONTAINED | xxx\[abc\]yyy |
| NOT_CONTAINED | \[xxx\]ab\[cyyy\] |
|---------------|-------------------|

So here is what happens when you alternate:

| start | |xxxabcyyy |
| --- | --- | --- |
| NOT_CONTAINED | xxx|abcyyy |
| CONTAINED | xxxabc|yyy |
| NOT_CONTAINED | xxxabcyyy| |
|---------------|-------------|

The entire string is traversed.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [CountMethod](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner.CountMethod) Options for replaceFrom and countIn to control how to treat each matched span. |
| | [TrimOption](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner.TrimOption) Options for the trim() method |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnicodeSetSpanner](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner#UnicodeSetSpanner(android.icu.text.UnicodeSet))`(`source:` ` [UnicodeSet](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet)!`)` Create a spanner from a UnicodeSet. |

| Public methods ||
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [countIn](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner#countIn(kotlin.CharSequence))`(`sequence:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Returns the number of matching characters found in a character sequence, counting by CountMethod. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [countIn](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner#countIn(kotlin.CharSequence,%20android.icu.text.UnicodeSetSpanner.CountMethod))`(`sequence:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `countMethod:` ` [UnicodeSetSpanner.CountMethod](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner.CountMethod)!`)` Returns the number of matching characters found in a character sequence, using SpanCondition. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [countIn](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner#countIn(kotlin.CharSequence,%20android.icu.text.UnicodeSetSpanner.CountMethod,%20android.icu.text.UnicodeSet.SpanCondition))`(`sequence:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `countMethod:` ` [UnicodeSetSpanner.CountMethod](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner.CountMethod)!`, `spanCondition:` ` [UnicodeSet.SpanCondition](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.SpanCondition)!`)` Returns the number of matching characters found in a character sequence. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [deleteFrom](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner#deleteFrom(kotlin.CharSequence))`(`sequence:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Delete all the matching spans in sequence, using SpanCondition. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [deleteFrom](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner#deleteFrom(kotlin.CharSequence,%20android.icu.text.UnicodeSet.SpanCondition))`(`sequence:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `spanCondition:` ` [UnicodeSet.SpanCondition](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.SpanCondition)!`)` Delete all matching spans in sequence, according to the spanCondition. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| --- | --- |
| open [UnicodeSet](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet)! | [getUnicodeSet](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner#getUnicodeSet())`()` Returns the UnicodeSet used for processing. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner#hashCode())`()` Returns a hash code value for the object. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [replaceFrom](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner#replaceFrom(kotlin.CharSequence,%20kotlin.CharSequence))`(`sequence:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `replacement:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Replace all matching spans in sequence by the replacement, counting by CountMethod. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [replaceFrom](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner#replaceFrom(kotlin.CharSequence,%20kotlin.CharSequence,%20android.icu.text.UnicodeSetSpanner.CountMethod))`(`sequence:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `replacement:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `countMethod:` ` [UnicodeSetSpanner.CountMethod](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner.CountMethod)!`)` Replace all matching spans in sequence by replacement, according to the CountMethod, using SpanCondition. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [replaceFrom](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner#replaceFrom(kotlin.CharSequence,%20kotlin.CharSequence,%20android.icu.text.UnicodeSetSpanner.CountMethod,%20android.icu.text.UnicodeSet.SpanCondition))`(`sequence:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `replacement:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `countMethod:` ` [UnicodeSetSpanner.CountMethod](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner.CountMethod)!`, `spanCondition:` ` [UnicodeSet.SpanCondition](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.SpanCondition)!`)` Replace all matching spans in sequence by replacement, according to the countMethod and spanCondition. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [trim](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner#trim(kotlin.CharSequence))`(`sequence:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Returns a trimmed sequence (using CharSequence.subsequence()), that omits matching elements at the start and end of the string, using TrimOption. |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [trim](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner#trim(kotlin.CharSequence,%20android.icu.text.UnicodeSetSpanner.TrimOption))`(`sequence:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `trimOption:` ` [UnicodeSetSpanner.TrimOption](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner.TrimOption)!`)` Returns a trimmed sequence (using CharSequence.subsequence()), that omits matching elements at the start or end of the string, using the trimOption and SpanCondition. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [trim](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner#trim(kotlin.CharSequence,%20android.icu.text.UnicodeSetSpanner.TrimOption,%20android.icu.text.UnicodeSet.SpanCondition))`(`sequence:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `trimOption:` ` [UnicodeSetSpanner.TrimOption](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner.TrimOption)!`, `spanCondition:` ` [UnicodeSet.SpanCondition](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.SpanCondition)!`)` Returns a trimmed sequence (using CharSequence.subsequence()), that omits matching elements at the start or end of the string, depending on the trimOption and spanCondition. |

## Public constructors

### UnicodeSetSpanner

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnicodeSetSpanner(source: UnicodeSet!)
```

Create a spanner from a UnicodeSet. For speed and safety, the UnicodeSet should be frozen. However, this class can be used with a non-frozen version to avoid the cost of freezing.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------|
| `source` | [UnicodeSet](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet)!:the original UnicodeSet |

## Public methods

### countIn

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun countIn(sequence: CharSequence!): Int
```

Returns the number of matching characters found in a character sequence, counting by CountMethod.MIN_ELEMENTS using SpanCondition.SIMPLE. The code alternates spans; see the class doc for [UnicodeSetSpanner](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner#) for a note about boundary conditions.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------|
| `sequence` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the sequence to count characters in |

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the count. Zero if there are none. |

### countIn

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun countIn(
    sequence: CharSequence!, 
    countMethod: UnicodeSetSpanner.CountMethod!
): Int
```

Returns the number of matching characters found in a character sequence, using SpanCondition.SIMPLE. The code alternates spans; see the class doc for [UnicodeSetSpanner](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner#) for a note about boundary conditions.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sequence` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the sequence to count characters in |
| `countMethod` | [UnicodeSetSpanner.CountMethod](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner.CountMethod)!:whether to treat an entire span as a match, or individual elements as matches |

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the count. Zero if there are none. |

### countIn

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun countIn(
    sequence: CharSequence!, 
    countMethod: UnicodeSetSpanner.CountMethod!, 
    spanCondition: UnicodeSet.SpanCondition!
): Int
```

Returns the number of matching characters found in a character sequence. The code alternates spans; see the class doc for [UnicodeSetSpanner](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner#) for a note about boundary conditions.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sequence` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the sequence to count characters in |
| `countMethod` | [UnicodeSetSpanner.CountMethod](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner.CountMethod)!:whether to treat an entire span as a match, or individual elements as matches |
| `spanCondition` | [UnicodeSet.SpanCondition](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.SpanCondition)!:the spanCondition to use. SIMPLE or CONTAINED means only count the elements in the span; NOT_CONTAINED is the reverse. **WARNING:**when a UnicodeSet contains strings, there may be unexpected behavior in edge cases. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the count. Zero if there are none. |

### deleteFrom

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun deleteFrom(sequence: CharSequence!): String!
```

Delete all the matching spans in sequence, using SpanCondition.SIMPLE The code alternates spans; see the class doc for [UnicodeSetSpanner](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner#) for a note about boundary conditions.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `sequence` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:charsequence to replace matching spans in. |

| Return ||
|-----------------------------------------------------------------------------------|------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | modified string. |

### deleteFrom

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun deleteFrom(
    sequence: CharSequence!, 
    spanCondition: UnicodeSet.SpanCondition!
): String!
```

Delete all matching spans in sequence, according to the spanCondition. The code alternates spans; see the class doc for [UnicodeSetSpanner](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner#) for a note about boundary conditions.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sequence` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:charsequence to replace matching spans in. |
| `spanCondition` | [UnicodeSet.SpanCondition](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.SpanCondition)!:specify whether to modify the matching spans (CONTAINED or SIMPLE) or the non-matching (NOT_CONTAINED) |

| Return ||
|-----------------------------------------------------------------------------------|------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | modified string. |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getUnicodeSet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUnicodeSet(): UnicodeSet!
```

Returns the UnicodeSet used for processing. It is frozen iff the original was.

| Return ||
|-------------------------------------------------------------------------------------------|-----------------------|
| [UnicodeSet](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet)! | the construction set. |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by [java.util.HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#).

The general contract of`hashCode`is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the`hashCode`method must consistently return the same integer, provided no information used in`equals`comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the [equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any))method, then calling the`hashCode`method on each of the two objects must produce the same integer result.
- It is*not* required that if two objects are unequal according to the [equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any))method, then calling the`hashCode`method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### replaceFrom

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun replaceFrom(
    sequence: CharSequence!, 
    replacement: CharSequence!
): String!
```

Replace all matching spans in sequence by the replacement, counting by CountMethod.MIN_ELEMENTS using SpanCondition.SIMPLE. The code alternates spans; see the class doc for [UnicodeSetSpanner](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner#) for a note about boundary conditions.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `sequence` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:charsequence to replace matching spans in. |
| `replacement` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:replacement sequence. To delete, use "" |

| Return ||
|-----------------------------------------------------------------------------------|------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | modified string. |

### replaceFrom

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun replaceFrom(
    sequence: CharSequence!, 
    replacement: CharSequence!, 
    countMethod: UnicodeSetSpanner.CountMethod!
): String!
```

Replace all matching spans in sequence by replacement, according to the CountMethod, using SpanCondition.SIMPLE. The code alternates spans; see the class doc for [UnicodeSetSpanner](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner#) for a note about boundary conditions.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sequence` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:charsequence to replace matching spans in. |
| `replacement` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:replacement sequence. To delete, use "" |
| `countMethod` | [UnicodeSetSpanner.CountMethod](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner.CountMethod)!:whether to treat an entire span as a match, or individual elements as matches |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------|------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | modified string. |

### replaceFrom

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun replaceFrom(
    sequence: CharSequence!, 
    replacement: CharSequence!, 
    countMethod: UnicodeSetSpanner.CountMethod!, 
    spanCondition: UnicodeSet.SpanCondition!
): String!
```

Replace all matching spans in sequence by replacement, according to the countMethod and spanCondition. The code alternates spans; see the class doc for [UnicodeSetSpanner](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner#) for a note about boundary conditions.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sequence` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:charsequence to replace matching spans in. |
| `replacement` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:replacement sequence. To delete, use "" |
| `countMethod` | [UnicodeSetSpanner.CountMethod](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner.CountMethod)!:whether to treat an entire span as a match, or individual elements as matches |
| --- | --- |
| `spanCondition` | [UnicodeSet.SpanCondition](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.SpanCondition)!:specify whether to modify the matching spans (CONTAINED or SIMPLE) or the non-matching (NOT_CONTAINED) |

| Return ||
|-----------------------------------------------------------------------------------|------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | modified string. |

### trim

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun trim(sequence: CharSequence!): CharSequence!
```

Returns a trimmed sequence (using CharSequence.subsequence()), that omits matching elements at the start and end of the string, using TrimOption.BOTH and SpanCondition.SIMPLE. For example: 

```kotlin
<code>new UnicodeSet("[ab]").trim("abacatbab")</code>
```
... returns`"cat"`.

<br />

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------|
| `sequence` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the sequence to trim |

| Return ||
|------------------------------------------------------------------------------------------------|---------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | a subsequence |

### trim

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun trim(
    sequence: CharSequence!, 
    trimOption: UnicodeSetSpanner.TrimOption!
): CharSequence!
```

Returns a trimmed sequence (using CharSequence.subsequence()), that omits matching elements at the start or end of the string, using the trimOption and SpanCondition.SIMPLE. For example: 

```kotlin
<code>new UnicodeSet("[ab]").trim("abacatbab", TrimOption.LEADING)</code>
```
... returns`"catbab"`.

<br />

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sequence` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the sequence to trim |
| `trimOption` | [UnicodeSetSpanner.TrimOption](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner.TrimOption)!:LEADING, TRAILING, or BOTH |

| Return ||
|------------------------------------------------------------------------------------------------|---------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | a subsequence |

### trim

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun trim(
    sequence: CharSequence!, 
    trimOption: UnicodeSetSpanner.TrimOption!, 
    spanCondition: UnicodeSet.SpanCondition!
): CharSequence!
```

Returns a trimmed sequence (using CharSequence.subsequence()), that omits matching elements at the start or end of the string, depending on the trimOption and spanCondition. For example: 

```kotlin
<code>new UnicodeSet("[ab]").trim("abacatbab", TrimOption.LEADING, SpanCondition.SIMPLE)</code>
```
... returns`"catbab"`.

<br />

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sequence` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the sequence to trim |
| `trimOption` | [UnicodeSetSpanner.TrimOption](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner.TrimOption)!:LEADING, TRAILING, or BOTH |
| `spanCondition` | [UnicodeSet.SpanCondition](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.SpanCondition)!:SIMPLE, CONTAINED or NOT_CONTAINED |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------------|---------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | a subsequence |
