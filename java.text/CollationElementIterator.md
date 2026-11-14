# CollationElementIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CollationElementIterator

```
class CollationElementIterator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.text.CollationElementIterator](CollationElementIterator.md) |

The`CollationElementIterator`class is used as an iterator to walk through each character of an international string. Use the iterator to return the ordering priority of the positioned character. The ordering priority of a character, which we refer to as a key, defines how a character is collated in the given collation object.

For example, consider the following in Spanish: 

```kotlin
"ca" → the first key is key('c') and second key is key('a').
  "cha" → the first key is key('ch') and second key is key('a').
  
```
And in German, 

```kotlin
"\u00e4b" → the first key is key('a'), the second key is key('e'), and
  the third key is key('b').
  
```
The key of a character is an integer composed of primary order(short), secondary order(byte), and tertiary order(byte). Java strictly defines the size and signedness of its primitive data types. Therefore, the static functions`primaryOrder`,`secondaryOrder`, and`tertiaryOrder`return`int`,`short`, and`short`respectively to ensure the correctness of the key value.

Example of the iterator usage, 

```kotlin
String testString = "This is a test";
   Collator col = Collator.getInstance();
   if (col instanceof RuleBasedCollator) {
       RuleBasedCollator ruleBasedCollator = (RuleBasedCollator)col;
       CollationElementIterator collationElementIterator = ruleBasedCollator.getCollationElementIterator(testString);
       int primaryOrder = CollationElementIterator.primaryOrder(collationElementIterator.next());
           :
   }
  
```

`CollationElementIterator.next`returns the collation order of the next character. A collation order consists of primary order, secondary order and tertiary order. The data type of the collation order is**int**. The first 16 bits of a collation order is its primary order; the next 8 bits is the secondary order and the last 8 bits is the tertiary order.

**Note:** `CollationElementIterator`is a part of`RuleBasedCollator`implementation. It is only usable with`RuleBasedCollator`instances.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NULLORDER](CollationElementIterator.md) Null order which indicates the end of string is reached by the cursor. |

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxExpansion](CollationElementIterator.md))`(`order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the maximum length of any expansion sequences that end with the specified comparison order. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOffset](CollationElementIterator.md))`()` Returns the character offset in the original text corresponding to the next collation element. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [next](CollationElementIterator.md))`()` Get the next collation element in the string. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [previous](CollationElementIterator.md))`()` Get the previous collation element in the string. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [primaryOrder](CollationElementIterator.md))`(`order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the primary component of a collation element. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](CollationElementIterator.md))`()` Resets the cursor to the beginning of the string. |
| --- | --- |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [secondaryOrder](CollationElementIterator.md))`(`order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the secondary component of a collation element. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOffset](CollationElementIterator.md))`(`newOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the iterator to point to the collation element corresponding to the specified character (the parameter is a CHARACTER offset in the original string, not an offset into its corresponding sequence of collation elements). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setText](CollationElementIterator.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set a new string over which to iterate. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setText](CollationElementIterator.md))`(`source:` ` [CharacterIterator](CharacterIterator.md)!`)` Set a new string over which to iterate. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [tertiaryOrder](CollationElementIterator.md))`(`order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the tertiary component of a collation element. |

## Constants

### NULLORDER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NULLORDER: Int
```

Null order which indicates the end of string is reached by the cursor. 

 Value: -1

## Public methods

### getMaxExpansion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxExpansion(order: Int): Int
```

Return the maximum length of any expansion sequences that end with the specified comparison order.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------|
| `order` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a collation order returned by previous or next. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum length of any expansion sequences ending with the specified order. |

### getOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOffset(): Int
```

Returns the character offset in the original text corresponding to the next collation element. (That is, getOffset() returns the position in the text corresponding to the collation element that will be returned by the next call to next().) This value will always be the index of the FIRST character corresponding to the collation element (a contracting character sequence is when two or more characters all correspond to the same collation element). This means if you do setOffset(x) followed immediately by getOffset(), getOffset() won't necessarily return x.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The character offset in the original text corresponding to the collation element that will be returned by the next call to next(). |

### next

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun next(): Int
```

Get the next collation element in the string.

This iterator iterates over a sequence of collation elements that were built from the string. Because there isn't necessarily a one-to-one mapping from characters to collation elements, this doesn't mean the same thing as "return the collation element \[or ordering priority\] of the next character in the string".

This function returns the collation element that the iterator is currently pointing to and then updates the internal pointer to point to the next element. previous() updates the pointer first and then returns the element. This means that when you change direction while iterating (i.e., call next() and then call previous(), or call previous() and then call next()), you'll get back the same element twice.

| Return ||
|----------------------------------------------------------------------------|----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the next collation element |

### previous

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun previous(): Int
```

Get the previous collation element in the string.

This iterator iterates over a sequence of collation elements that were built from the string. Because there isn't necessarily a one-to-one mapping from characters to collation elements, this doesn't mean the same thing as "return the collation element \[or ordering priority\] of the previous character in the string".

This function updates the iterator's internal pointer to point to the collation element preceding the one it's currently pointing to and then returns that element, while next() returns the current element and then updates the pointer. This means that when you change direction while iterating (i.e., call next() and then call previous(), or call previous() and then call next()), you'll get back the same element twice.

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous collation element |

### primaryOrder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun primaryOrder(order: Int): Int
```

Return the primary component of a collation element.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------|
| `order` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the collation element |

| Return ||
|----------------------------------------------------------------------------|---------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the element's primary component |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun reset(): Unit
```

Resets the cursor to the beginning of the string. The next call to next() will return the first collation element in the string. 

### secondaryOrder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun secondaryOrder(order: Int): Short
```

Return the secondary component of a collation element.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------|
| `order` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the collation element |

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the element's secondary component |

### setOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOffset(newOffset: Int): Unit
```

Sets the iterator to point to the collation element corresponding to the specified character (the parameter is a CHARACTER offset in the original string, not an offset into its corresponding sequence of collation elements). The value returned by the next call to next() will be the collation element corresponding to the specified position in the text. If that position is in the middle of a contracting character sequence, the result of the next call to next() is the collation element for that sequence. This means that getOffset() is not guaranteed to return the same value as was passed to a preceding call to setOffset().

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------|
| `newOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new character offset into the original text. |

### setText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setText(source: String!): Unit
```

Set a new string over which to iterate.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the new source text |

### setText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setText(source: CharacterIterator!): Unit
```

Set a new string over which to iterate.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------|
| `source` | [CharacterIterator](CharacterIterator.md)!:the new source text. |

### tertiaryOrder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun tertiaryOrder(order: Int): Short
```

Return the tertiary component of a collation element.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------|
| `order` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the collation element |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the element's tertiary component |
