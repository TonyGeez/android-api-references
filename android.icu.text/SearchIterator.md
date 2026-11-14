Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SearchIterator

Kotlin | [Java](SearchIterator.md)
| --- | --- |

```
abstract class SearchIterator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.SearchIterator](SearchIterator.md) |

| Known Direct Subclasses [StringSearch](StringSearch.md) |---|---| | [StringSearch](StringSearch.md) | `StringSearch` is a `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#` that provides language-sensitive text searching based on the comparison rules defined in a `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator` object. | |
| --- | --- | --- | --- | --- | --- | --- |

`SearchIterator` is an abstract base class that provides methods to search for a pattern within a text string. Instances of `SearchIterator` maintain a current position and scan over the target text, returning the indices the pattern is matched and the length of each match.

`SearchIterator` defines a protocol for text searching. Subclasses provide concrete implementations of various search algorithms. For example, `StringSearch` implements language-sensitive pattern matching based on the comparison rules defined in a `RuleBasedCollator` object.

Other options for searching include using a BreakIterator to restrict the points at which matches are detected.

`SearchIterator` provides an API that is similar to that of other text iteration classes such as `BreakIterator`. Using this class, it is easy to scan through text looking for all occurrences of a given pattern. The following example uses a `StringSearch` object to find all instances of "fox" in the target string. Any other subclass of `SearchIterator` can be used in an identical manner.

```kotlin
<code>
  String target = "The quick brown fox jumped over the lazy fox";
  String pattern = "fox";
  SearchIterator iter = new StringSearch(pattern, target);
  for (int pos = iter.first(); pos != SearchIterator.DONE;
          pos = iter.next()) {
      System.out.println("Found match at " + pos +
              ", length is " + iter.getMatchLength());
  }
  </code>
```

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator.ElementComparisonType` Option to control how collation elements are compared. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int` DONE is returned by previous() and next() after all valid matches have been returned, and by first() and last() if there are no matches at all. |

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#SearchIterator(java.text.CharacterIterator,%20android.icu.text.BreakIterator)(target: https://developer.android.com/reference/kotlin/java/text/CharacterIterator.html#!, breaker: https://developer.android.com/reference/kotlin/android/icu/text/BreakIterator!)` Protected constructor for use by subclasses. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#first()()` Returns the first index at which the string text matches the search pattern. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#following(kotlin.Int)(position: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the first index equal or greater than `position` at which the string text matches the search pattern. |
| open [BreakIterator](BreakIterator.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getBreakIterator()()` Returns the BreakIterator that is used to restrict the indexes at which matches are detected. |
| --- | --- |
| open [SearchIterator.ElementComparisonType](../android/icu/text/SearchIterator.ElementComparisonType.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getElementComparisonType()()` Returns the collation element comparison type. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getIndex()()` Return the current index in the text being searched. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getMatchLength()()` Returns the length of text in the string which matches the search pattern. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getMatchStart()()` Returns the index to the match in the text string that was searched. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getMatchedText()()` Returns the text that was matched by the most recent call to `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#first()`, `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#next()`, `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#previous()`, or `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#last()`. |
| open [CharacterIterator](../java.text/CharacterIterator.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getTarget()()` Return the string text to be searched. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#isOverlapping()()` Return true if the overlapping property has been set. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#last()()` Returns the last index in the target text at which it matches the search pattern. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#next()()` Returns the index of the next point at which the text matches the search pattern, starting from the current position The iterator is adjusted so that its current index (as returned by `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getIndex()`) is the match position if one was found. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#preceding(kotlin.Int)(position: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the first index less than `position` at which the string text matches the search pattern. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#previous()()` Returns the index of the previous point at which the string text matches the search pattern, starting at the current position. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#reset()()` Resets the iteration. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#setBreakIterator(android.icu.text.BreakIterator)(breakiter: https://developer.android.com/reference/kotlin/android/icu/text/BreakIterator!)` Set the BreakIterator that will be used to restrict the points at which matches are detected. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#setElementComparisonType(android.icu.text.SearchIterator.ElementComparisonType)(type: https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator.ElementComparisonType!)` Sets the collation element comparison type. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#setIndex(kotlin.Int)(position: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the position in the target text at which the next search will start. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#setOverlapping(kotlin.Boolean)(allowOverlap: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Determines whether overlapping matches are returned. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#setTarget(java.text.CharacterIterator)(text: https://developer.android.com/reference/kotlin/java/text/CharacterIterator.html#!)` Set the target text to be searched. |

| Protected methods ||
|---|---|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#handleNext(kotlin.Int)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Abstract method which subclasses override to provide the mechanism for finding the next match in the target text. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#handlePrevious(kotlin.Int)(startAt: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Abstract method which subclasses override to provide the mechanism for finding the previous match in the target text. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#setMatchLength(kotlin.Int)(length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the length of the most recent match in the target text. |
| --- | --- |

| Properties ||
|---|---|
| [BreakIterator](BreakIterator.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#breakIterator:android.icu.text.BreakIterator` The BreakIterator to define the boundaries of a logical match. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#matchLength:kotlin.Int` Length of the most current match in target text. |
| [CharacterIterator](../java.text/CharacterIterator.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#targetText:java.text.CharacterIterator` Target text for searching. |
| --- | --- |

## Constants

### DONE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DONE: Int
```

DONE is returned by previous() and next() after all valid matches have been returned, and by first() and last() if there are no matches at all.

 Value: -1

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#previous()`
- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#next()`

## Protected constructors

### SearchIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected SearchIterator(
    target: CharacterIterator!, 
    breaker: BreakIterator!)
```

Protected constructor for use by subclasses. Initializes the iterator with the argument target text for searching and sets the BreakIterator. See class documentation for more details on the use of the target text and `https://developer.android.com/reference/kotlin/android/icu/text/BreakIterator`.

| Parameters ||
|---|---|
| `target` | [CharacterIterator](../java.text/CharacterIterator.md)!: The target text to be searched. |
| `breaker` | [BreakIterator](BreakIterator.md)!: A `https://developer.android.com/reference/kotlin/android/icu/text/BreakIterator` that is used to determine the boundaries of a logical match. This argument can be null. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | thrown when argument target is null, or of length 0 |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/BreakIterator`

## Public methods

### first

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun first(): Int
```

Returns the first index at which the string text matches the search pattern. The iterator is adjusted so that its current index (as returned by `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getIndex()`) is the match position if one was found. If a match is not found, `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int` will be returned and the iterator will be adjusted to the index `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The character index of the first match, or `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int` if there are no matches. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getIndex()`

### following

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun following(position: Int): Int
```

Returns the first index equal or greater than `position` at which the string text matches the search pattern. The iterator is adjusted so that its current index (as returned by `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getIndex()`) is the match position if one was found. If a match is not found, `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int` will be returned and the iterator will be adjusted to the index `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int`.

| Parameters ||
|---|---|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): where search if to start from. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The character index of the first match following `position`, or `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int` if there are no matches. |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If position is less than or greater than the text range for searching. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getIndex()`

### getBreakIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBreakIterator(): BreakIterator!
```

Returns the BreakIterator that is used to restrict the indexes at which matches are detected. This will be the same object that was passed to the constructor or to `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#setBreakIterator(android.icu.text.BreakIterator)`. If the `https://developer.android.com/reference/kotlin/android/icu/text/BreakIterator` has not been set, `null` will be returned. See `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#setBreakIterator(android.icu.text.BreakIterator)` for more information.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/BreakIterator!` | the BreakIterator set to restrict logic matches |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#setBreakIterator(android.icu.text.BreakIterator)`
- `https://developer.android.com/reference/kotlin/android/icu/text/BreakIterator`

### getElementComparisonType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getElementComparisonType(): SearchIterator.ElementComparisonType!
```

Returns the collation element comparison type.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator.ElementComparisonType`
- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#setElementComparisonType(android.icu.text.SearchIterator.ElementComparisonType)`

### getIndex

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getIndex(): Int
```

Return the current index in the text being searched. If the iteration has gone past the end of the text (or past the beginning for a backwards search), `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int` is returned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | current index in the text being searched. |

### getMatchLength

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMatchLength(): Int
```

Returns the length of text in the string which matches the search pattern. This call returns a valid result only after a successful call to `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#first()`, `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#next()`, `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#previous()`, or `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#last()`. Just after construction, or after a searching method returns `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int`, this method will return 0.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The length of the match in the target text, or 0 if there is no match currently. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#first()`
- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#next()`
- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#previous()`
- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#last()`

### getMatchStart

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMatchStart(): Int
```

Returns the index to the match in the text string that was searched. This call returns a valid result only after a successful call to `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#first()`, `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#next()`, `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#previous()`, or `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#last()`. Just after construction, or after a searching method returns `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int`, this method will return `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int`.

Use `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getMatchLength()` to get the matched string length.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | index of a substring within the text string that is being searched. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#first()`
- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#next()`
- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#previous()`
- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#last()`

### getMatchedText

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMatchedText(): String!
```

Returns the text that was matched by the most recent call to `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#first()`, `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#next()`, `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#previous()`, or `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#last()`. If the iterator is not pointing at a valid match (e.g. just after construction or after `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int` has been returned, returns an empty string.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the substring in the target test of the most recent match, or null if there is no match currently. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#first()`
- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#next()`
- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#previous()`
- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#last()`

### getTarget

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTarget(): CharacterIterator!
```

Return the string text to be searched.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/text/CharacterIterator.html#!` | text string to be searched. |

### isOverlapping

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isOverlapping(): Boolean
```

Return true if the overlapping property has been set. See `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#setOverlapping(kotlin.Boolean)` for more information.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the overlapping property has been set, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#setOverlapping(kotlin.Boolean)`

### last

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun last(): Int
```

Returns the last index in the target text at which it matches the search pattern. The iterator is adjusted so that its current index (as returned by `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getIndex()`) is the match position if one was found. If a match is not found, `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int` will be returned and the iterator will be adjusted to the index `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The index of the first match, or `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int` if there are no matches. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getIndex()`

### next

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun next(): Int
```

Returns the index of the next point at which the text matches the search pattern, starting from the current position The iterator is adjusted so that its current index (as returned by `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getIndex()`) is the match position if one was found. If a match is not found, `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int` will be returned and the iterator will be adjusted to a position after the end of the text string.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The index of the next match after the current position, or `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int` if there are no more matches. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getIndex()`

### preceding

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun preceding(position: Int): Int
```

Returns the first index less than `position` at which the string text matches the search pattern. The iterator is adjusted so that its current index (as returned by `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getIndex()`) is the match position if one was found. If a match is not found, `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int` will be returned and the iterator will be adjusted to the index `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int`

When the overlapping option (`https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#isOverlapping()`) is off, the last index of the result match is always less than `position`. When the overlapping option is on, the result match may span across `position`.

| Parameters ||
|---|---|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): where search is to start from. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The character index of the first match preceding `position`, or `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int` if there are no matches. |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If position is less than or greater than the text range for searching |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getIndex()`

### previous

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun previous(): Int
```

Returns the index of the previous point at which the string text matches the search pattern, starting at the current position. The iterator is adjusted so that its current index (as returned by `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getIndex()`) is the match position if one was found. If a match is not found, `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int` will be returned and the iterator will be adjusted to the index `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The index of the previous match before the current position, or `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int` if there are no more matches. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getIndex()`

### reset

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reset(): Unit
```

Resets the iteration. Search will begin at the start of the text string if a forward iteration is initiated before a backwards iteration. Otherwise if a backwards iteration is initiated before a forwards iteration, the search will begin at the end of the text string.

### setBreakIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBreakIterator(breakiter: BreakIterator!): Unit
```

Set the BreakIterator that will be used to restrict the points at which matches are detected.

| Parameters ||
|---|---|
| `breakiter` | [BreakIterator](BreakIterator.md)!: A BreakIterator that will be used to restrict the points at which matches are detected. If a match is found, but the match's start or end index is not a boundary as determined by the `https://developer.android.com/reference/kotlin/android/icu/text/BreakIterator`, the match will be rejected and another will be searched for. If this parameter is `null`, no break detection is attempted. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/BreakIterator`

### setElementComparisonType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setElementComparisonType(type: SearchIterator.ElementComparisonType!): Unit
```

Sets the collation element comparison type.

The default comparison type is `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator.ElementComparisonType`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator.ElementComparisonType`
- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getElementComparisonType()`

### setIndex

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIndex(position: Int): Unit
```

Sets the position in the target text at which the next search will start. This method clears any previous match.

| Parameters ||
|---|---|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): position from which to start the next search |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | thrown if argument position is out of the target text range. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getIndex()`

### setOverlapping

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOverlapping(allowOverlap: Boolean): Unit
```

Determines whether overlapping matches are returned. See the class documentation for more information about overlapping matches.

The default setting of this property is false

| Parameters ||
|---|---|
| `allowOverlap` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): flag indicator if overlapping matches are allowed |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#isOverlapping()`

### setTarget

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTarget(text: CharacterIterator!): Unit
```

Set the target text to be searched. Text iteration will then begin at the start of the text string. This method is useful if you want to reuse an iterator to search within a different body of text.

| Parameters ||
|---|---|
| `text` | [CharacterIterator](../java.text/CharacterIterator.md)!: new text iterator to look for match, |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | thrown when text is null or has 0 length |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getTarget()`

## Protected methods

### handleNext

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun handleNext(start: Int): Int
```

Abstract method which subclasses override to provide the mechanism for finding the next match in the target text. This allows different subclasses to provide different search algorithms.

If a match is found, the implementation should return the index at which the match starts and should call `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#setMatchLength(kotlin.Int)` with the number of characters in the target text that make up the match. If no match is found, the method should return `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int`.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index in the target text at which the search should start. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | index at which the match starts, else if match is not found `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int` is returned |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#setMatchLength(kotlin.Int)`

### handlePrevious

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun handlePrevious(startAt: Int): Int
```

Abstract method which subclasses override to provide the mechanism for finding the previous match in the target text. This allows different subclasses to provide different search algorithms.

If a match is found, the implementation should return the index at which the match starts and should call `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#setMatchLength(kotlin.Int)` with the number of characters in the target text that make up the match. If no match is found, the method should return `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int`.

| Parameters ||
|---|---|
| `startAt` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index in the target text at which the search should start. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | index at which the match starts, else if match is not found `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#DONE:kotlin.Int` is returned |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#setMatchLength(kotlin.Int)`

### setMatchLength

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun setMatchLength(length: Int): Unit
```

Sets the length of the most recent match in the target text. Subclasses' handleNext() and handlePrevious() methods should call this after they find a match in the target text.

| Parameters ||
|---|---|
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): new length to set |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#handleNext(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#handlePrevious(kotlin.Int)`

## Properties

### breakIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var breakIterator: BreakIterator!
```

The BreakIterator to define the boundaries of a logical match. This value can be a null. See class documentation for more information.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#setBreakIterator(android.icu.text.BreakIterator)`
- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getBreakIterator()`
- `https://developer.android.com/reference/kotlin/android/icu/text/BreakIterator`

### matchLength

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var matchLength: Int
```

Length of the most current match in target text. Value 0 is the default value.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#setMatchLength(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getMatchLength()`

### targetText

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var targetText: CharacterIterator!
```

Target text for searching.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#setTarget(java.text.CharacterIterator)`
- `https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator#getTarget()`
