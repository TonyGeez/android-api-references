# DateSorter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DateSorter

Kotlin| [Java](https://developer.android.com/reference/android/webkit/DateSorter "View this page in Java") 
| --- | --- |

```
open class DateSorter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.DateSorter](https://developer.android.com/reference/kotlin/android/webkit/DateSorter#) |

Sorts dates into the following groups: Today Yesterday seven days ago one month ago older than a month ago

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DAY_COUNT](https://developer.android.com/reference/kotlin/android/webkit/DateSorter#DAY_COUNT:kotlin.Int) must be \>= 3 |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DateSorter](https://developer.android.com/reference/kotlin/android/webkit/DateSorter#DateSorter(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getBoundary](https://developer.android.com/reference/kotlin/android/webkit/DateSorter#getBoundary(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](https://developer.android.com/reference/kotlin/android/webkit/DateSorter#getIndex(kotlin.Long))`(`time:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLabel](https://developer.android.com/reference/kotlin/android/webkit/DateSorter#getLabel(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

## Constants

### DAY_COUNT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DAY_COUNT: Int
```

must be \>= 3 

 Value: 5

## Public constructors

### DateSorter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DateSorter(context: Context!)
```

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:Application context |

## Public methods

### getBoundary

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBoundary(index: Int): Long
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):date bin index as returned by getIndex() |

| Return ||
|------------------------------------------------------------------------------|------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | date boundary at given index |

### getIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIndex(time: Long): Int
```

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `time` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):time since the Epoch in milliseconds, such as that returned by Calendar.getTimeInMillis() |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an index from 0 to (DAY_COUNT - 1) that identifies which date bin this date belongs to |

### getLabel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLabel(index: Int): String!
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):date bin index as returned by getIndex() |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | string label suitable for display to user |
