# DateSorter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DateSorter

Kotlin| [Java](DateSorter.md) 
| --- | --- |

```
open class DateSorter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.DateSorter](DateSorter.md) |

Sorts dates into the following groups: Today Yesterday seven days ago one month ago older than a month ago

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DAY_COUNT](DateSorter.md) must be \>= 3 |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DateSorter](DateSorter.md))`(`context:` ` [Context](../android.content/Context.md)!`)` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getBoundary](DateSorter.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](DateSorter.md))`(`time:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLabel](DateSorter.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
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
| `context` | [Context](../android.content/Context.md)!:Application context |

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
