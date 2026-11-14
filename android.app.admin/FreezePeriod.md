# FreezePeriod

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FreezePeriod

Kotlin| [Java](https://developer.android.com/reference/android/app/admin/FreezePeriod "View this page in Java") 

```
open class FreezePeriod
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.admin.FreezePeriod](https://developer.android.com/reference/kotlin/android/app/admin/FreezePeriod#) |

A class that represents one freeze period which repeats*annually*. A freeze period has two java.time#MonthDay values that define the start and end dates of the period, both inclusive. If the end date is earlier than the start date, the period is considered wrapped around the year-end. As far as freeze period is concerned, leap year is disregarded and February 29th should be treated as if it were February 28th: so a freeze starting or ending on February 28th is identical to a freeze starting or ending on February 29th. When calulating the length of a freeze or the distance bewteen two freee periods, February 29th is also ignored.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FreezePeriod](https://developer.android.com/reference/kotlin/android/app/admin/FreezePeriod#FreezePeriod(java.time.MonthDay,%20java.time.MonthDay))`(`start:` ` [MonthDay](https://developer.android.com/reference/kotlin/java/time/MonthDay.html#)!`, `end:` ` [MonthDay](https://developer.android.com/reference/kotlin/java/time/MonthDay.html#)!`)` Creates a freeze period by its start and end dates. |

| Public methods ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MonthDay](https://developer.android.com/reference/kotlin/java/time/MonthDay.html#)! | [getEnd](https://developer.android.com/reference/kotlin/android/app/admin/FreezePeriod#getEnd())`()` Returns the end date (inclusive) of this freeze period. |
| open [MonthDay](https://developer.android.com/reference/kotlin/java/time/MonthDay.html#)! | [getStart](https://developer.android.com/reference/kotlin/android/app/admin/FreezePeriod#getStart())`()` Returns the start date (inclusive) of this freeze period. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/app/admin/FreezePeriod#toString())`()` <br /> |

## Public constructors

### FreezePeriod

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FreezePeriod(
    start: MonthDay!, 
    end: MonthDay!)
```

Creates a freeze period by its start and end dates. If the end date is earlier than the start date, the freeze period is considered wrapping year-end.

## Public methods

### getEnd

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEnd(): MonthDay!
```

Returns the end date (inclusive) of this freeze period. 

### getStart

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStart(): MonthDay!
```

Returns the start date (inclusive) of this freeze period. 

### toString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
