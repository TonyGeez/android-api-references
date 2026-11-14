# FreezePeriod

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FreezePeriod

Kotlin| [Java](../android/app/admin/FreezePeriod.md) 
| --- | --- |

```
open class FreezePeriod
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.admin.FreezePeriod](../android/app/admin/FreezePeriod.md) |

A class that represents one freeze period which repeats*annually*. A freeze period has two java.time#MonthDay values that define the start and end dates of the period, both inclusive. If the end date is earlier than the start date, the period is considered wrapped around the year-end. As far as freeze period is concerned, leap year is disregarded and February 29th should be treated as if it were February 28th: so a freeze starting or ending on February 28th is identical to a freeze starting or ending on February 29th. When calulating the length of a freeze or the distance bewteen two freee periods, February 29th is also ignored.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FreezePeriod](../android/app/admin/FreezePeriod.md))`(`start:` ` [MonthDay](../java/time/MonthDay.md)!`, `end:` ` [MonthDay](../java/time/MonthDay.md)!`)` Creates a freeze period by its start and end dates. |

| Public methods ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MonthDay](../java/time/MonthDay.md)! | [getEnd](../android/app/admin/FreezePeriod.md))`()` Returns the end date (inclusive) of this freeze period. |
| open [MonthDay](../java/time/MonthDay.md)! | [getStart](../android/app/admin/FreezePeriod.md))`()` Returns the start date (inclusive) of this freeze period. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/app/admin/FreezePeriod.md))`()` <br /> |
| --- | --- |

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
