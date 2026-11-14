# ValueIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ValueIterator

Kotlin| [Java](https://developer.android.com/reference/android/icu/util/ValueIterator "View this page in Java") 

```
interface ValueIterator
```

| [android.icu.util.ValueIterator](https://developer.android.com/reference/kotlin/android/icu/util/ValueIterator#) |

Interface for enabling iteration over sets of \<int, Object\>, where int is the sorted integer index in ascending order, and Object its associated value.

The ValueIterator allows iterations over integer indexes in the range of Integer.MIN_VALUE to Integer.MAX_VALUE inclusive. Implementations of ValueIterator should specify their own maximum subrange within the above range that is meaningful to its applications.

Most implementations will be created by factory methods, such as the character name iterator in UCharacter.getNameIterator. See example below. Example of use: 

```kotlin
ValueIterator iterator = UCharacter.getNameIterator();
  ValueIterator.Element result = new ValueIterator.Element();
  iterator.setRange(UCharacter.MIN_VALUE, UCharacter.MAX_VALUE);
  while (iterator.next(result)) {
      System.out.println("Codepoint \\u" +
                         Integer.toHexString(result.integer) +
                         " has the character name " + (String)result.value);
  }
  
```

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Element](https://developer.android.com/reference/kotlin/android/icu/util/ValueIterator.Element) The return result container of each iteration. |

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [next](https://developer.android.com/reference/kotlin/android/icu/util/ValueIterator#next(android.icu.util.ValueIterator.Element))`(`element:` ` [ValueIterator.Element](https://developer.android.com/reference/kotlin/android/icu/util/ValueIterator.Element)!`)` Returns the next result for this iteration and returns true if we are not at the end of the iteration, false otherwise. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/android/icu/util/ValueIterator#reset())`()` Resets the iterator to start iterating from the integer index Integer. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRange](https://developer.android.com/reference/kotlin/android/icu/util/ValueIterator#setRange(kotlin.Int,%20kotlin.Int))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Restricts the range of integers to iterate and resets the iteration to begin at the index argument start. |

## Public methods

### next

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun next(element: ValueIterator.Element!): Boolean
```

Returns the next result for this iteration and returns true if we are not at the end of the iteration, false otherwise.

If this returns a false, the contents of elements will not be updated.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `element` | [ValueIterator.Element](https://developer.android.com/reference/kotlin/android/icu/util/ValueIterator.Element)!:for storing the result index and value |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if we are not at the end of the iteration, false otherwise. |

**See Also**

- [android.icu.util.ValueIterator.Element](https://developer.android.com/reference/kotlin/android/icu/util/ValueIterator.Element) 

### reset

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun reset(): Unit
```

Resets the iterator to start iterating from the integer index Integer.MIN_VALUE or X if a setRange(X, Y) has been called previously. 

### setRange

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setRange(
    start: Int, 
    limit: Int
): Unit
```

Restricts the range of integers to iterate and resets the iteration to begin at the index argument start.

If setRange(start, end) is not performed before next(element) is called, the iteration will start from the integer index Integer.MIN_VALUE and end at Integer.MAX_VALUE.

If this range is set outside the meaningful range specified by the implementation, next(element) will always return false.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):first integer in the range to iterate |
| `limit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one more than the last integer in the range |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | thrown when attempting to set an illegal range. E.g limit \<= start |
