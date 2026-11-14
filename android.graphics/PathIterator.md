# PathIterator

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PathIterator

Kotlin | [Java](PathIterator.md) 
| --- | --- |

```
open class PathIterator : MutableIterator<PathIterator.Segment!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.PathIterator](PathIterator.md) |

`PathIterator` can be used to query a given [Path](Path.md) object, to discover its operations and point values.

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Segment](../android/graphics/PathIterator.Segment.md) This class holds the data for a given segment in a path, as returned by [next()](PathIterator.md)). |

| Constants ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VERB_CLOSE](PathIterator.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VERB_CONIC](PathIterator.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VERB_CUBIC](PathIterator.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VERB_DONE](PathIterator.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VERB_LINE](PathIterator.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VERB_MOVE](PathIterator.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VERB_QUAD](PathIterator.md) <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasNext](PathIterator.md))`()` Returns true if the there are more elements in this iterator to be returned. |
| open [PathIterator.Segment](../android/graphics/PathIterator.Segment.md) | [next](PathIterator.md))`()` Returns the next [Segment](../android/graphics/PathIterator.Segment.md) element in this iterator. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [next](PathIterator.md))`(`points:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the next verb in this iterator's [Path](Path.md), and fills entries in the `points` array with the point data (if any) for that operation. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [peek](PathIterator.md))`()` Returns the next verb in the iteration, or [VERB_DONE](PathIterator.md) if there are no more elements. |

## Constants

### VERB_CLOSE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VERB_CLOSE: Int
```  

 Value: 5

### VERB_CONIC

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VERB_CONIC: Int
```  

 Value: 3

### VERB_CUBIC

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VERB_CUBIC: Int
```  

 Value: 4

### VERB_DONE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VERB_DONE: Int
```  

 Value: 6

### VERB_LINE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VERB_LINE: Int
```  

 Value: 1

### VERB_MOVE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VERB_MOVE: Int
```  

 Value: 0

### VERB_QUAD

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VERB_QUAD: Int
```  

 Value: 2

## Public methods

### hasNext

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasNext(): Boolean
```

Returns true if the there are more elements in this iterator to be returned. A return value of `false` means there are no more elements, and an ensuing call to [next()](PathIterator.md)) or [next(float[],int)](https://developer.android.com/reference/kotlin/android/graphics/PathIterator#next(kotlin.FloatArray,%20kotlin.Int)) )} will return [VERB_DONE](PathIterator.md).

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if there are more elements to be iterated through, false otherwise |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------|
| `java.util.ConcurrentModificationException` | if the underlying path was modified since this iterator was created. |

### next

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun next(): PathIterator.Segment
```

Returns the next [Segment](../android/graphics/PathIterator.Segment.md) element in this iterator. There are two versions of `next()`. This version is slightly more expensive at runtime, since it allocates a new [Segment](../android/graphics/PathIterator.Segment.md) object with every call. The other version, [next(float[],int)](https://developer.android.com/reference/kotlin/android/graphics/PathIterator#next(kotlin.FloatArray,%20kotlin.Int)) requires no such allocation, but requires a little more manual effort to use.

| Return ||
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [PathIterator.Segment](../android/graphics/PathIterator.Segment.md) | the next segment in this iterator This value cannot be `null`. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------|
| `java.util.NoSuchElementException` | if the iteration has no more elements |
| `java.util.ConcurrentModificationException` | if the underlying path was modified since this iterator was created. |

### next

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun next(
    points: FloatArray, 
    offset: Int
): Int
```

Returns the next verb in this iterator's [Path](Path.md), and fills entries in the `points` array with the point data (if any) for that operation. Each two floats represent the data for a single point of that operation. The number of pairs of floats supplied in the resulting array depends on the verb:

- [VERB_MOVE](PathIterator.md): 1 pair (indices 0 to 1)
- [VERB_LINE](PathIterator.md): 2 pairs (indices 0 to 3)
- [VERB_QUAD](PathIterator.md): 3 pairs (indices 0 to 5)
- [VERB_CONIC](PathIterator.md): 3.5 pairs (indices 0 to 6), the seventh entry has the conic weight
- [VERB_CUBIC](PathIterator.md): 4 pairs (indices 0 to 7)
- [VERB_CLOSE](PathIterator.md): 0 pairs
- [VERB_DONE](PathIterator.md): 0 pairs

<br />

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `points` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): The point data for this operation, must have at least 8 items available to hold up to 4 pairs of point values This value cannot be `null`. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An offset into the `points` array where entries should be placed. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the operation for the next element in the iteration This value cannot be `null`. Value is [android.graphics.PathIterator#VERB_MOVE](PathIterator.md), [android.graphics.PathIterator#VERB_LINE](PathIterator.md), [android.graphics.PathIterator#VERB_QUAD](PathIterator.md), [android.graphics.PathIterator#VERB_CONIC](PathIterator.md), [android.graphics.PathIterator#VERB_CUBIC](PathIterator.md), [android.graphics.PathIterator#VERB_CLOSE](PathIterator.md), or [android.graphics.PathIterator#VERB_DONE](PathIterator.md) |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------|
| `java.lang.ArrayIndexOutOfBoundsException` | if the points array is too small |
| `java.util.ConcurrentModificationException` | if the underlying path was modified since this iterator was created. |

### peek

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun peek(): Int
```

Returns the next verb in the iteration, or [VERB_DONE](PathIterator.md) if there are no more elements.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the next verb in the iteration, or [VERB_DONE](PathIterator.md) if there are no more elements This value cannot be `null`. Value is [android.graphics.PathIterator#VERB_MOVE](PathIterator.md), [android.graphics.PathIterator#VERB_LINE](PathIterator.md), [android.graphics.PathIterator#VERB_QUAD](PathIterator.md), [android.graphics.PathIterator#VERB_CONIC](PathIterator.md), [android.graphics.PathIterator#VERB_CUBIC](PathIterator.md), [android.graphics.PathIterator#VERB_CLOSE](PathIterator.md), or [android.graphics.PathIterator#VERB_DONE](PathIterator.md) |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------|
| `java.util.ConcurrentModificationException` | if the underlying path was modified since this iterator was created. |
