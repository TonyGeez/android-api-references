Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CollationElementIterator

```
class CollationElementIterator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.icu.text.CollationElementIterator](https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator#) |

`CollationElementIterator` is an iterator created by a RuleBasedCollator to walk through a string. The return result of each iteration is a 32-bit collation element (CE) that defines the ordering priority of the next character or sequence of characters in the source string.

For illustration, consider the following in Slovak and in traditional Spanish collation:

```kotlin
"ca" -> the first collation element is CE('c') and the second
          collation element is CE('a').
  "cha" -> the first collation element is CE('ch') and the second
           collation element is CE('a').
  
```
And in German phonebook collation,

```kotlin
Since the character 'æ' is a composed character of 'a' and 'e', the
  iterator returns two collation elements for the single character 'æ'
 
  "æb" -> the first collation element is collation_element('a'), the
               second collation element is collation_element('e'), and the
               third collation element is collation_element('b').
  
```

For collation ordering comparison, the collation element results can not be compared simply by using basic arithmetic operators, e.g. \<, == or \>, further processing has to be done. Details can be found in the ICU [User Guide](https://unicode-org.github.io/icu/userguide/collation/architecture). An example of using the CollationElementIterator for collation ordering comparison is the class `https://developer.android.com/reference/kotlin/android/icu/text/StringSearch`.

To construct a CollationElementIterator object, users call the method getCollationElementIterator() on a RuleBasedCollator that defines the desired sorting order.

Example:

```kotlin
String testString = "This is a test";
   RuleBasedCollator rbc = new RuleBasedCollator("&a<b");
   CollationElementIterator iterator = rbc.getCollationElementIterator(testString);
   int primaryOrder = iterator.IGNORABLE;
   while (primaryOrder != iterator.NULLORDER) {
       int order = iterator.next();
       if (order != iterator.IGNORABLE &&
           order != iterator.NULLORDER) {
           // order is valid, not ignorable and we have not passed the end
           // of the iteration, we do something
           primaryOrder = CollationElementIterator.primaryOrder(order);
           System.out.println("Next primary order 0x" +
                              Integer.toHexString(primaryOrder));
       }
   }
  
```

The method next() returns the collation order of the next character based on the comparison level of the collator. The method previous() returns the collation order of the previous character based on the comparison level of the collator. The Collation Element Iterator moves only in one direction between calls to reset(), setOffset(), or setText(). That is, next() and previous() can not be inter-used. Whenever previous() is to be called after next() or vice versa, reset(), setOffset() or setText() has to be called first to reset the status, shifting current position to either the end or the start of the string (reset() or setText()), or the specified position (setOffset()). Hence at the next call of next() or previous(), the first or last collation order, or collation order at the specified position will be returned. If a change of direction is done without one of these calls, the result is undefined.

This class is not subclassable.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator#IGNORABLE:kotlin.Int` This constant is returned by the iterator in the methods next() and previous() when a collation element result is to be ignored. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator#NULLORDER:kotlin.Int` This constant is returned by the iterator in the methods next() and previous() when the end or the beginning of the source string has been reached, and there are no more valid collation elements to return. |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Tests that argument object is equals to this CollationElementIterator. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator#getMaxExpansion(kotlin.Int)(ce: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the maximum length of any expansion sequence that ends with the specified collation element. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator#getOffset()()` Returns the character offset in the source string corresponding to the next collation element. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator#hashCode()()` Mock implementation of hashCode(). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator#next()()` Get the next collation element in the source string. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator#previous()()` Get the previous collation element in the source string. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator#primaryOrder(kotlin.Int)(ce: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the primary order of the specified collation element, i. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator#reset()()` Resets the cursor to the beginning of the string. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator#secondaryOrder(kotlin.Int)(ce: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the secondary order of the specified collation element, i. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator#setOffset(kotlin.Int)(newOffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the iterator to point to the collation element corresponding to the character at the specified offset. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator#setText(android.icu.text.UCharacterIterator)(source: https://developer.android.com/reference/kotlin/android/icu/text/UCharacterIterator!)` Set a new source string iterator for iteration, and reset the offset to the beginning of the text. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator#setText(kotlin.String)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Set a new source string for iteration, and reset the offset to the beginning of the text. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator#setText(java.text.CharacterIterator)(source: https://developer.android.com/reference/kotlin/java/text/CharacterIterator.html#!)` Set a new source string iterator for iteration, and reset the offset to the beginning of the text. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator#tertiaryOrder(kotlin.Int)(ce: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the tertiary order of the specified collation element, i. |

## Constants

### IGNORABLE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IGNORABLE: Int
```

This constant is returned by the iterator in the methods next() and previous() when a collation element result is to be ignored.

See class documentation for an example of use.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator#next()`
- `https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator#previous()`

### NULLORDER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NULLORDER: Int
```

This constant is returned by the iterator in the methods next() and previous() when the end or the beginning of the source string has been reached, and there are no more valid collation elements to return.

See class documentation for an example of use.

 Value: -1

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator#next()`
- `https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator#previous()`

## Public methods

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Tests that argument object is equals to this CollationElementIterator. Iterators are equal if the objects uses the same RuleBasedCollator, the same source text and have the same current position in iteration.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `that` | object to test if it is equals to this CollationElementIterator |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getMaxExpansion

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMaxExpansion(ce: Int): Int
```

Returns the maximum length of any expansion sequence that ends with the specified collation element. If there is no expansion with this collation element as the last element, returns 1.

| Parameters ||
|---|---|
| `ce` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a collation element returned by previous() or next(). |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the maximum length of any expansion sequence ending with the specified collation element. |

### getOffset

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOffset(): Int
```

Returns the character offset in the source string corresponding to the next collation element. I.e., getOffset() returns the position in the source string corresponding to the collation element that will be returned by the next call to next() or previous(). This value could be any of:

- The index of the **first** character corresponding to the next collation element. (This means that if `setOffset(offset)` sets the index in the middle of a contraction, `getOffset()` returns the index of the first character in the contraction, which may not be equal to the original offset that was set. Hence calling getOffset() immediately after setOffset(offset) does not guarantee that the original offset set will be returned.)
- If normalization is on, the index of the **immediate** subsequent character, or composite character with the first character, having a combining class of 0.
- The length of the source string, if iteration has reached the end.

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The character offset in the source string corresponding to the collation element that will be returned by the next call to next() or previous(). |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Mock implementation of hashCode(). This implementation always returns a constant value. When Java assertion is enabled, this method triggers an assertion failure.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### next

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun next(): Int
```

Get the next collation element in the source string.

This iterator iterates over a sequence of collation elements that were built from the string. Because there isn't necessarily a one-to-one mapping from characters to collation elements, this doesn't mean the same thing as "return the collation element \[or ordering priority\] of the next character in the string".

This function returns the collation element that the iterator is currently pointing to, and then updates the internal pointer to point to the next element.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the next collation element or NULLORDER if the end of the iteration has been reached. |

### previous

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun previous(): Int
```

Get the previous collation element in the source string.

This iterator iterates over a sequence of collation elements that were built from the string. Because there isn't necessarily a one-to-one mapping from characters to collation elements, this doesn't mean the same thing as "return the collation element \[or ordering priority\] of the previous character in the string".

This function updates the iterator's internal pointer to point to the collation element preceding the one it's currently pointing to and then returns that element, while next() returns the current element and then updates the pointer.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the previous collation element, or NULLORDER when the start of the iteration has been reached. |

### primaryOrder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun primaryOrder(ce: Int): Int
```

Return the primary order of the specified collation element, i.e. the first 16 bits. This value is unsigned.

| Parameters ||
|---|---|
| `ce` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the collation element |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the element's 16 bits primary order. |

### reset

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun reset(): Unit
```

Resets the cursor to the beginning of the string. The next call to next() or previous() will return the first and last collation element in the string, respectively.

If the RuleBasedCollator used by this iterator has had its attributes changed, calling reset() will reinitialize the iterator to use the new attributes.

### secondaryOrder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun secondaryOrder(ce: Int): Int
```

Return the secondary order of the specified collation element, i.e. the 16th to 23th bits, inclusive. This value is unsigned.

| Parameters ||
|---|---|
| `ce` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the collation element |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the element's 8 bits secondary order |

### setOffset

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setOffset(newOffset: Int): Unit
```

Sets the iterator to point to the collation element corresponding to the character at the specified offset. The value returned by the next call to next() will be the collation element corresponding to the characters at offset.

If offset is in the middle of a contracting character sequence, the iterator is adjusted to the start of the contracting sequence. This means that getOffset() is not guaranteed to return the same value set by this method.

If the decomposition mode is on, and offset is in the middle of a decomposible range of source text, the iterator may not return a correct result for the next forwards or backwards iteration. The user must ensure that the offset is not in the middle of a decomposible range.

| Parameters ||
|---|---|
| `newOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character offset into the original source string to set. Note that this is not an offset into the corresponding sequence of collation elements. |

### setText

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setText(source: UCharacterIterator!): Unit
```

Set a new source string iterator for iteration, and reset the offset to the beginning of the text.

The source iterator's integrity will be preserved since a new copy will be created for use.

| Parameters ||
|---|---|
| `source` | [UCharacterIterator](https://developer.android.com/reference/kotlin/android/icu/text/UCharacterIterator)!: the new source string iterator for iteration. |

### setText

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setText(source: String!): Unit
```

Set a new source string for iteration, and reset the offset to the beginning of the text.

| Parameters ||
|---|---|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the new source string for iteration. |

### setText

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setText(source: CharacterIterator!): Unit
```

Set a new source string iterator for iteration, and reset the offset to the beginning of the text.

| Parameters ||
|---|---|
| `source` | [CharacterIterator](https://developer.android.com/reference/kotlin/java/text/CharacterIterator.html#)!: the new source string iterator for iteration. |

### tertiaryOrder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun tertiaryOrder(ce: Int): Int
```

Return the tertiary order of the specified collation element, i.e. the last 8 bits. This value is unsigned.

| Parameters ||
|---|---|
| `ce` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the collation element |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the element's 8 bits tertiary order |
