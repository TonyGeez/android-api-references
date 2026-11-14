# RangeValueIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RangeValueIterator

Kotlin | [Java](https://developer.android.com/reference/android/icu/util/RangeValueIterator "View this page in Java") 

```
interface RangeValueIterator
```

| [android.icu.util.RangeValueIterator](https://developer.android.com/reference/kotlin/android/icu/util/RangeValueIterator#) |

Interface for enabling iteration over sets of \<int index, int value\>, where index is the sorted integer index in ascending order and value, its associated integer value.

The result for each iteration is the consecutive range of \<int index, int value\> with the same value. Result is represented by \<start, limit, value\> where

- start is the starting integer of the result range
- limit is 1 after the maximum integer that follows start, such that all integers between start and (limit - 1), inclusive, have the same associated integer value.
- value is the integer value that all integers from start to (limit - 1) share in common.

Hence value(start) = value(start + 1) = .... = value(start + n) = .... = value(limit - 1). However value(start -1) != value(start) and value(limit) != value(start).

Most implementations will be created by factory methods, such as the character type iterator in UCharacter.getTypeIterator. See example below.

Example of use: 

```kotlin
RangeValueIterator iterator = UCharacter.getTypeIterator();
  RangeValueIterator.Element result = new RangeValueIterator.Element();
  while (iterator.next(result)) {
      System.out.println("Codepoint \\u" +
                         Integer.toHexString(result.start) +
                         " to codepoint \\u" +
                         Integer.toHexString(result.limit - 1) +
                         " has the character type " + result.value);
  }
  
```

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Element](https://developer.android.com/reference/kotlin/android/icu/util/RangeValueIterator.Element) Return result wrapper for android. |

| Public methods ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [next](https://developer.android.com/reference/kotlin/android/icu/util/RangeValueIterator#next(android.icu.util.RangeValueIterator.Element))`(`element:` ` [RangeValueIterator.Element](https://developer.android.com/reference/kotlin/android/icu/util/RangeValueIterator.Element)!`)` Returns the next maximal result range with a common value and returns true if we are not at the end of the iteration, false otherwise. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/android/icu/util/RangeValueIterator#reset())`()` Resets the iterator to the beginning of the iteration. |

## Public methods

### next

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun next(element: RangeValueIterator.Element!): Boolean
```

Returns the next maximal result range with a common value and returns true if we are not at the end of the iteration, false otherwise.

If this returns a false, the contents of elements will not be updated.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `element` | [RangeValueIterator.Element](https://developer.android.com/reference/kotlin/android/icu/util/RangeValueIterator.Element)!: for storing the result range and value |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if we are not at the end of the iteration, false otherwise. |

**See Also**

- [android.icu.util.RangeValueIterator.Element](https://developer.android.com/reference/kotlin/android/icu/util/RangeValueIterator.Element) 

### reset

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun reset(): Unit
```

Resets the iterator to the beginning of the iteration.
