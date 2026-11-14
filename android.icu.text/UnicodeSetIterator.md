# UnicodeSetIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnicodeSetIterator

Kotlin| [Java](UnicodeSetIterator.md) 
| --- | --- |

```
open class UnicodeSetIterator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.UnicodeSetIterator](UnicodeSetIterator.md) |

UnicodeSetIterator iterates over the contents of a UnicodeSet. It iterates over either code points or code point ranges. After all code points or ranges have been returned, it returns the multicharacter strings of the UnicodeSet, if any.

This class is not intended for public subclassing.

To iterate over code points and multicharacter strings, use a loop like this: 

```kotlin
for (UnicodeSetIterator it = new UnicodeSetIterator(set); it.next();) {
    processString(it.getString());
  }
  
```

To iterate over code point ranges, use a loop like this: 

```kotlin
for (UnicodeSetIterator it = new UnicodeSetIterator(set); it.nextRange();) {
    if (it.codepoint != UnicodeSetIterator.IS_STRING) {
      processCodepointRange(it.codepoint, it.codepointEnd);
    } else {
      processString(it.getString());
    }
  }
  
```

To iterate over only the strings, start with`new UnicodeSetIterator(set).skipToStrings()`.

**Warning:**For speed, UnicodeSet iteration does not check for concurrent modification. Do not alter the UnicodeSet while iterating.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnicodeSetIterator](UnicodeSetIterator.md))`()` Create an iterator over nothing. |
| [UnicodeSetIterator](UnicodeSetIterator.md))`(`set:` ` [UnicodeSet](UnicodeSet.md)!`)` Create an iterator over the given set. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](UnicodeSetIterator.md))`()` Gets the current string from the iterator. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [next](UnicodeSetIterator.md))`()` Returns the next element in the set, either a single code point or a string. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [nextRange](UnicodeSetIterator.md))`()` Returns the next element in the set, either a code point range or a string. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](UnicodeSetIterator.md))`()` Resets this iterator to the start of the set. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](UnicodeSetIterator.md))`(`uset:` ` [UnicodeSet](UnicodeSet.md)!`)` Sets this iterator to visit the elements of the given set and resets it to the start of that set. |
| open [UnicodeSetIterator](UnicodeSetIterator.md)! | [skipToStrings](UnicodeSetIterator.md))`()` Skips over the remaining code points/ranges, if any. |
| --- | --- |

| Properties ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IS_STRING](UnicodeSetIterator.md) Value of codepoint if the iterator points to a string. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [codepoint](UnicodeSetIterator.md) Current code point, or the special value IS_STRING, if the iterator points to a string. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [codepointEnd](UnicodeSetIterator.md) When iterating over ranges using nextRange(), codepointEnd contains the inclusive end of the iteration range, if codepoint != IS_STRING. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [string](UnicodeSetIterator.md) If codepoint == IS_STRING, then string points to the current string. |

## Public constructors

### UnicodeSetIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnicodeSetIterator()
```

Create an iterator over nothing. next() and nextRange() return false. This is a convenience constructor allowing the target to be set later. 

### UnicodeSetIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnicodeSetIterator(set: UnicodeSet!)
```

Create an iterator over the given set.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------|
| `set` | [UnicodeSet](UnicodeSet.md)!:set to iterate over |

## Public methods

### getString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getString(): String!
```

Gets the current string from the iterator. Only use after calling next(), not nextRange(). 

### next

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun next(): Boolean
```

Returns the next element in the set, either a single code point or a string. If there are no more elements in the set, return false. If codepoint == IS_STRING, the value is a string in the string field. Otherwise the value is a single code point in the codepoint field.

The order of iteration is all code points in sorted order, followed by all strings sorted order. codepointEnd is undefined after calling this method. string is undefined unless codepoint == IS_STRING. Do not mix calls to next() and nextRange() without calling reset() between them. The results of doing so are undefined.

**Warning:**For speed, UnicodeSet iteration does not check for concurrent modification. Do not alter the UnicodeSet while iterating.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if there was another element in the set and this object contains the element. |

### nextRange

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextRange(): Boolean
```

Returns the next element in the set, either a code point range or a string. If there are no more elements in the set, return false. If codepoint == IS_STRING, the value is a string in the string field. Otherwise the value is a range of one or more code points from codepoint to codepointeEnd inclusive.

The order of iteration is all code points ranges in sorted order, followed by all strings sorted order. Ranges are disjoint and non-contiguous. string is undefined unless codepoint == IS_STRING. Do not mix calls to next() and nextRange() without calling reset() between them. The results of doing so are undefined.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if there was another element in the set and this object contains the element. |

### reset

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Resets this iterator to the start of the set. 

### reset

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(uset: UnicodeSet!): Unit
```

Sets this iterator to visit the elements of the given set and resets it to the start of that set. The iterator is valid only so long as set is valid.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------|
| `uset` | [UnicodeSet](UnicodeSet.md)!:the set to iterate over. |

### skipToStrings

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun skipToStrings(): UnicodeSetIterator!
```

Skips over the remaining code points/ranges, if any. A following call to next() or nextRange() will yield a string, if there is one. No-op if next() would return false, or if it would yield a string anyway.

| Return ||
|------------------------------------------------------------------------------------------------------------|------|
| [UnicodeSetIterator](UnicodeSetIterator.md)! | this |

**See Also**

- [android.icu.text.UnicodeSet#strings()](UnicodeSet.md))

## Properties

### IS_STRING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static var IS_STRING: Int
```

Value of codepoint if the iterator points to a string. If codepoint == IS_STRING, then examine string for the current iteration result. 

### codepoint

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var codepoint: Int
```

Current code point, or the special value IS_STRING, if the iterator points to a string. 

### codepointEnd

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var codepointEnd: Int
```

When iterating over ranges using nextRange(), codepointEnd contains the inclusive end of the iteration range, if codepoint != IS_STRING. If iterating over code points using next(), or if codepoint == IS_STRING, then the value of codepointEnd is undefined. 

### string

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var string: String!
```

If codepoint == IS_STRING, then string points to the current string. If codepoint != IS_STRING, the value of string is undefined.
