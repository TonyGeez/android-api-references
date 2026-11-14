# MonthDisplayHelper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MonthDisplayHelper

Kotlin| [Java](MonthDisplayHelper.md) 
| --- | --- |

```
open class MonthDisplayHelper
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.MonthDisplayHelper](MonthDisplayHelper.md) |

Helps answer common questions that come up when displaying a month in a 6 row calendar grid format. Not thread safe.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MonthDisplayHelper](MonthDisplayHelper.md))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [MonthDisplayHelper](MonthDisplayHelper.md))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `weekStartDay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnOf](MonthDisplayHelper.md))`(`day:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDayAt](MonthDisplayHelper.md))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [getDigitsForRow](MonthDisplayHelper.md))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFirstDayOfMonth](MonthDisplayHelper.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMonth](MonthDisplayHelper.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNumberOfDaysInMonth](MonthDisplayHelper.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOffset](MonthDisplayHelper.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRowOf](MonthDisplayHelper.md))`(`day:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWeekStartDay](MonthDisplayHelper.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getYear](MonthDisplayHelper.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWithinCurrentMonth](MonthDisplayHelper.md))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [nextMonth](MonthDisplayHelper.md))`()` Increment the month. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [previousMonth](MonthDisplayHelper.md))`()` Decrement the month. |

## Public constructors

### MonthDisplayHelper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MonthDisplayHelper(
    year: Int, 
    month: Int)
```  

### MonthDisplayHelper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MonthDisplayHelper(
    year: Int, 
    month: Int, 
    weekStartDay: Int)
```

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The year. |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The month. |
| `weekStartDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):What day of the week the week should start. |
| --- | --- |

## Public methods

### getColumnOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColumnOf(day: Int): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Which column day is in. |

### getDayAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDayAt(
    row: Int, 
    column: Int
): Int
```

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The row, 0-5, starting from the top. |
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The column, 0-6, starting from the left. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The day at a particular row, column |

### getDigitsForRow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDigitsForRow(row: Int): IntArray!
```

| Parameters ||
|-------|---------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which row (0-5). |

| Return ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | the digits of the month to display in one of the 6 rows of a calendar month display. |

### getFirstDayOfMonth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFirstDayOfMonth(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The first day of the month using a constants such as [java.util.Calendar#SUNDAY](../java.util/Calendar.md). |

### getMonth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMonth(): Int
```  

### getNumberOfDaysInMonth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNumberOfDaysInMonth(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of days in the month. |

### getOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOffset(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The offset from displaying everything starting on the very first box. For example, if the calendar is set to display the first day of the week as Sunday, and the month starts on a Wednesday, the offset is 3. |

### getRowOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRowOf(day: Int): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Which row day is in. |

### getWeekStartDay

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWeekStartDay(): Int
```  

### getYear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getYear(): Int
```  

### isWithinCurrentMonth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isWithinCurrentMonth(
    row: Int, 
    column: Int
): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the row and column fall within the month. |

### nextMonth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextMonth(): Unit
```

Increment the month. 

### previousMonth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun previousMonth(): Unit
```

Decrement the month.
