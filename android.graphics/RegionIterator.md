# RegionIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RegionIterator

Kotlin| [Java](https://developer.android.com/reference/android/graphics/RegionIterator "View this page in Java") 
| --- | --- |

```
open class RegionIterator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.RegionIterator](https://developer.android.com/reference/kotlin/android/graphics/RegionIterator#) |

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RegionIterator](https://developer.android.com/reference/kotlin/android/graphics/RegionIterator#RegionIterator(android.graphics.Region))`(`region:` ` [Region](https://developer.android.com/reference/kotlin/android/graphics/Region)!`)` Construct an iterator for all of the rectangles in a region. |

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [next](https://developer.android.com/reference/kotlin/android/graphics/RegionIterator#next(android.graphics.Rect))`(`r:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)!`)` Return the next rectangle in the region. |

| Protected methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/graphics/RegionIterator#finalize())`()` <br /> |

## Public constructors

### RegionIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RegionIterator(region: Region!)
```

Construct an iterator for all of the rectangles in a region. This effectively makes a private copy of the region, so any subsequent edits to region will not affect the iterator.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `region` | [Region](https://developer.android.com/reference/kotlin/android/graphics/Region)!:the region that will be iterated |

## Public methods

### next

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun next(r: Rect!): Boolean
```

Return the next rectangle in the region. If there are no more rectangles this returns false and r is unchanged. If there is at least one more, this returns true and r is set to that rectangle.

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
