# UCharacterIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UCharacterIterator

Kotlin| [Java](../android/icu/text/UCharacterIterator.md) 
| --- | --- |

```
abstract class UCharacterIterator : Cloneable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.UCharacterIterator](../android/icu/text/UCharacterIterator.md) |

Abstract class that defines an API for iteration on text objects.This is an interface for forward and backward iteration and random access into a text object. Forward iteration is done with post-increment and backward iteration is done with pre-decrement semantics, while the`java.text.CharacterIterator`interface methods provided forward iteration with "pre-increment" and backward iteration with pre-decrement semantics. This API is more efficient for forward iteration over code points. The other major difference is that this API can do both code unit and code point iteration,`java.text.CharacterIterator`can only iterate over code units and is limited to BMP (0 - 0xFFFF)

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DONE](../android/icu/text/UCharacterIterator.md) Indicator that we have reached the ends of the UTF16 text. |

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UCharacterIterator](../android/icu/text/UCharacterIterator.md))`()` Protected default constructor for the subclasses |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../android/icu/text/UCharacterIterator.md))`()` Creates a copy of this iterator, independent from other iterators. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [current](../android/icu/text/UCharacterIterator.md))`()` Returns the code unit at the current index. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [currentCodePoint](../android/icu/text/UCharacterIterator.md))`()` Returns the codepoint at the current index. |
| --- | --- |
| open [CharacterIterator](../java/text/CharacterIterator.md)! | [getCharacterIterator](../android/icu/text/UCharacterIterator.md))`()` Returns a`java.text.CharacterIterator`object for the underlying text of this iterator. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](../android/icu/text/UCharacterIterator.md))`()` Gets the current index in text. |
| static [UCharacterIterator](../android/icu/text/UCharacterIterator.md)! | [getInstance](../android/icu/text/UCharacterIterator.md))`(`source:` ` [Replaceable](../android/icu/text/Replaceable.md)!`)` Returns a`UCharacterIterator`object given a`Replaceable`object. |
| --- | --- |
| static [UCharacterIterator](../android/icu/text/UCharacterIterator.md)! | [getInstance](../android/icu/text/UCharacterIterator.md))`(`source:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` Returns a`UCharacterIterator`object given a source character array. |
| static [UCharacterIterator](../android/icu/text/UCharacterIterator.md)! | [getInstance](../android/icu/text/UCharacterIterator.md))`(`source:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a`UCharacterIterator`object given a source character array. |
| static [UCharacterIterator](../android/icu/text/UCharacterIterator.md)! | [getInstance](../android/icu/text/UCharacterIterator.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a`UCharacterIterator`object given a source string. |
| --- | --- |
| static [UCharacterIterator](../android/icu/text/UCharacterIterator.md)! | [getInstance](../android/icu/text/UCharacterIterator.md))`(`source:` ` [StringBuffer](../java/lang/StringBuffer.md)!`)` Returns a`UCharacterIterator`object given a source StringBuffer. |
| static [UCharacterIterator](../android/icu/text/UCharacterIterator.md)! | [getInstance](../android/icu/text/UCharacterIterator.md))`(`source:` ` [CharacterIterator](../java/text/CharacterIterator.md)!`)` Returns a`UCharacterIterator`object given a CharacterIterator. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLength](../android/icu/text/UCharacterIterator.md))`()` Returns the length of the text |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getText](../android/icu/text/UCharacterIterator.md))`()` Convenience method for returning the underlying text storage as as string |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getText](../android/icu/text/UCharacterIterator.md))`(`fillIn:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` Convenience override for`getText(char[], int)`that provides an offset of 0. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getText](../android/icu/text/UCharacterIterator.md))`(`fillIn:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Fills the buffer with the underlying text storage of the iterator If the buffer capacity is not enough a exception is thrown. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [moveCodePointIndex](../android/icu/text/UCharacterIterator.md))`(`delta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Moves the current position by the number of code points specified, either forward or backward depending on the sign of delta (positive or negative respectively). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [moveIndex](../android/icu/text/UCharacterIterator.md))`(`delta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Moves the current position by the number of code units specified, either forward or backward depending on the sign of delta (positive or negative respectively). |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [next](../android/icu/text/UCharacterIterator.md))`()` Returns the UTF16 code unit at index, and increments to the next code unit (post-increment semantics). |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextCodePoint](../android/icu/text/UCharacterIterator.md))`()` Returns the code point at index, and increments to the next code point (post-increment semantics). |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [previous](../android/icu/text/UCharacterIterator.md))`()` Decrement to the position of the previous code unit in the text, and return it (pre-decrement semantics). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [previousCodePoint](../android/icu/text/UCharacterIterator.md))`()` Retreat to the start of the previous code point in the text, and return it (pre-decrement semantics). |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIndex](../android/icu/text/UCharacterIterator.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the index to the specified index in the text. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setToLimit](../android/icu/text/UCharacterIterator.md))`()` Sets the current index to the limit. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setToStart](../android/icu/text/UCharacterIterator.md))`()` Sets the current index to the start. |
| --- | --- |

## Constants

### DONE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DONE: Int
```

Indicator that we have reached the ends of the UTF16 text. 

 Value: -1

## Protected constructors

### UCharacterIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected UCharacterIterator()
```

Protected default constructor for the subclasses

## Public methods

### clone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Creates a copy of this iterator, independent from other iterators. If it is not possible to clone the iterator, returns null.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | copy of this iterator |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### current

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun current(): Int
```

Returns the code unit at the current index. If index is out of range, returns DONE. Index is not changed.

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | current code unit |

### currentCodePoint

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun currentCodePoint(): Int
```

Returns the codepoint at the current index. If the current index is invalid, DONE is returned. If the current index points to a lead surrogate, and there is a following trail surrogate, then the code point is returned. Otherwise, the code unit at index is returned. Index is not changed.

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | current codepoint |

### getCharacterIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCharacterIterator(): CharacterIterator!
```

Returns a`java.text.CharacterIterator`object for the underlying text of this iterator. The returned iterator is independent of this iterator.

| Return ||
|--------------------------------------------------------------------------------------------------------|------------------------------------|
| [CharacterIterator](../java/text/CharacterIterator.md)! | java.text.CharacterIterator object |

### getIndex

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getIndex(): Int
```

Gets the current index in text.

| Return ||
|----------------------------------------------------------------------------|------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | current index in text. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(source: Replaceable!): UCharacterIterator!
```

Returns a`UCharacterIterator`object given a`Replaceable`object.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Replaceable](../android/icu/text/Replaceable.md)!:a valid source as a`Replaceable`object |

| Return ||
|------------------------------------------------------------------------------------------------------------|---------------------------|
| [UCharacterIterator](../android/icu/text/UCharacterIterator.md)! | UCharacterIterator object |

| Exceptions ||
|--------------------------------------|-------------------------|
| `java.lang.IllegalArgumentException` | if the argument is null |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(source: CharArray!): UCharacterIterator!
```

Returns a`UCharacterIterator`object given a source character array.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `source` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:an array of UTF-16 code units |

| Return ||
|------------------------------------------------------------------------------------------------------------|---------------------------|
| [UCharacterIterator](../android/icu/text/UCharacterIterator.md)! | UCharacterIterator object |

| Exceptions ||
|--------------------------------------|-------------------------|
| `java.lang.IllegalArgumentException` | if the argument is null |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(
    source: CharArray!, 
    start: Int, 
    limit: Int
): UCharacterIterator!
```

Returns a`UCharacterIterator`object given a source character array.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `source` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:an array of UTF-16 code units |

| Return ||
|------------------------------------------------------------------------------------------------------------|---------------------------|
| [UCharacterIterator](../android/icu/text/UCharacterIterator.md)! | UCharacterIterator object |

| Exceptions ||
|--------------------------------------|-------------------------|
| `java.lang.IllegalArgumentException` | if the argument is null |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(source: String!): UCharacterIterator!
```

Returns a`UCharacterIterator`object given a source string.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a string |

| Return ||
|------------------------------------------------------------------------------------------------------------|---------------------------|
| [UCharacterIterator](../android/icu/text/UCharacterIterator.md)! | UCharacterIterator object |

| Exceptions ||
|--------------------------------------|-------------------------|
| `java.lang.IllegalArgumentException` | if the argument is null |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(source: StringBuffer!): UCharacterIterator!
```

Returns a`UCharacterIterator`object given a source StringBuffer.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [StringBuffer](../java/lang/StringBuffer.md)!:an string buffer of UTF-16 code units |

| Return ||
|------------------------------------------------------------------------------------------------------------|---------------------------|
| [UCharacterIterator](../android/icu/text/UCharacterIterator.md)! | UCharacterIterator object |

| Exceptions ||
|--------------------------------------|-------------------------|
| `java.lang.IllegalArgumentException` | if the argument is null |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(source: CharacterIterator!): UCharacterIterator!
```

Returns a`UCharacterIterator`object given a CharacterIterator.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [CharacterIterator](../java/text/CharacterIterator.md)!:a valid CharacterIterator object. |

| Return ||
|------------------------------------------------------------------------------------------------------------|---------------------------|
| [UCharacterIterator](../android/icu/text/UCharacterIterator.md)! | UCharacterIterator object |

| Exceptions ||
|--------------------------------------|-------------------------|
| `java.lang.IllegalArgumentException` | if the argument is null |

### getLength

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLength(): Int
```

Returns the length of the text

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | length of the text |

### getText

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getText(): String!
```

Convenience method for returning the underlying text storage as as string

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the underlying text storage in the iterator as a string |

### getText

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getText(fillIn: CharArray!): Int
```

Convenience override for`getText(char[], int)`that provides an offset of 0.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fillIn` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:an array of chars to fill with the underlying UTF-16 code units. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of code units added to fillIn, as a convenience |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | exception if there is not enough room in the array. |

### getText

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getText(
    fillIn: CharArray!, 
    offset: Int
): Int
```

Fills the buffer with the underlying text storage of the iterator If the buffer capacity is not enough a exception is thrown. The capacity of the fill in buffer should at least be equal to length of text in the iterator obtained by calling`getLength()`).**Usage:** 

```kotlin
UChacterIterator iter = new UCharacterIterator.getInstance(text);
          char[] buf = new char[iter.getLength()];
          iter.getText(buf);
 
          OR
          char[] buf= new char[1];
          int len = 0;
          for(;;){
              try{
                  len = iter.getText(buf);
                  break;
              }catch(IndexOutOfBoundsException e){
                  buf = new char[iter.getLength()];
              }
          }
  
```

<br />

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fillIn` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:an array of chars to fill with the underlying UTF-16 code units. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position within the array to start putting the data. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of code units added to fillIn, as a convenience |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | exception if there is not enough room after offset in the array, or if offset \< 0. |

### moveCodePointIndex

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun moveCodePointIndex(delta: Int): Int
```

Moves the current position by the number of code points specified, either forward or backward depending on the sign of delta (positive or negative respectively). If the current index is at a trail surrogate then the first adjustment is by code unit, and the remaining adjustments are by code points. If the resulting index would be less than zero, the index is set to zero, and if the resulting index would be greater than limit, the index is set to limit.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------|
| `delta` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of code units to move the current index. |

| Return ||
|----------------------------------------------------------------------------|---------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the new index |

| Exceptions ||
|---------------------------------------|-------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | is thrown if an invalid delta is supplied |

### moveIndex

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun moveIndex(delta: Int): Int
```

Moves the current position by the number of code units specified, either forward or backward depending on the sign of delta (positive or negative respectively). If the resulting index would be less than zero, the index is set to zero, and if the resulting index would be greater than limit, the index is set to limit.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------|
| `delta` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of code units to move the current index. |

| Return ||
|----------------------------------------------------------------------------|----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the new index. |

| Exceptions ||
|---------------------------------------|-------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | is thrown if an invalid index is supplied |

### next

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun next(): Int
```

Returns the UTF16 code unit at index, and increments to the next code unit (post-increment semantics). If index is out of range, DONE is returned, and the iterator is reset to the limit of the text.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the next UTF16 code unit, or DONE if the index is at the limit of the text. |

### nextCodePoint

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextCodePoint(): Int
```

Returns the code point at index, and increments to the next code point (post-increment semantics). If index does not point to a valid surrogate pair, the behavior is the same as`next()`. Otherwise the iterator is incremented past the surrogate pair, and the code point represented by the pair is returned.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the next codepoint in text, or DONE if the index is at the limit of the text. |

### previous

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun previous(): Int
```

Decrement to the position of the previous code unit in the text, and return it (pre-decrement semantics). If the resulting index is less than 0, the index is reset to 0 and DONE is returned.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous code unit in the text, or DONE if the new index is before the start of the text. |

### previousCodePoint

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun previousCodePoint(): Int
```

Retreat to the start of the previous code point in the text, and return it (pre-decrement semantics). If the index is not preceded by a valid surrogate pair, the behavior is the same as`previous()`. Otherwise the iterator is decremented to the start of the surrogate pair, and the code point represented by the pair is returned.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous code point in the text, or DONE if the new index is before the start of the text. |

### setIndex

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setIndex(index: Int): Unit
```

Sets the index to the specified index in the text.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index within the text. |

| Exceptions ||
|---------------------------------------|-------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | is thrown if an invalid index is supplied |

### setToLimit

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setToLimit(): Unit
```

Sets the current index to the limit. 

### setToStart

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setToStart(): Unit
```

Sets the current index to the start.
