# TemporalQuery

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TemporalQuery

```
@FunctionalInterface interface TemporalQuery<R : Any!>
```

| [java.time.temporal.TemporalQuery](../java/time/temporal/TemporalQuery.md) |

Strategy for querying a temporal object.

Queries are a key tool for extracting information from temporal objects. They exist to externalize the process of querying, permitting different approaches, as per the strategy design pattern. Examples might be a query that checks if the date is the day before February 29th in a leap year, or calculates the number of days to your next birthday.

The [TemporalField](../java/time/temporal/TemporalField.md) interface provides another mechanism for querying temporal objects. That interface is limited to returning a`long`. By contrast, queries can return any type.

There are two equivalent ways of using a`TemporalQuery`. The first is to invoke the method on this interface directly. The second is to use [TemporalAccessor.query(TemporalQuery)](../java/time/temporal/TemporalAccessor.md)): 

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisQuery.queryFrom(temporal);
    temporal = temporal.query(thisQuery);
  
```
It is recommended to use the second approach,`query(TemporalQuery)`, as it is a lot clearer to read in code.

The most common implementations are method references, such as`LocalDate::from`and`ZoneId::from`. Additional common queries are provided as static methods in [TemporalQueries](../java/time/temporal/TemporalQueries.md).

## Summary

| Public methods ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstractR | [queryFrom](../java/time/temporal/TemporalQuery.md))`(`temporal:` ` [TemporalAccessor](../java/time/temporal/TemporalAccessor.md)!`)` Queries the specified temporal object. |

## Public methods

### queryFrom

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun queryFrom(temporal: TemporalAccessor!): R
```

Queries the specified temporal object.

This queries the specified temporal object to return an object using the logic encapsulated in the implementing class. Examples might be a query that checks if the date is the day before February 29th in a leap year, or calculates the number of days to your next birthday.

There are two equivalent ways of using this method. The first is to invoke this method directly. The second is to use [TemporalAccessor.query(TemporalQuery)](../java/time/temporal/TemporalAccessor.md)): 

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisQuery.queryFrom(temporal);
    temporal = temporal.query(thisQuery);
  
```
It is recommended to use the second approach,`query(TemporalQuery)`, as it is a lot clearer to read in code.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `temporal` | [TemporalAccessor](../java/time/temporal/TemporalAccessor.md)!:the temporal object to query, not null |

| Return ||
|---|----------------------------------------------------------|
| R | the queried value, may return null to indicate not found |

| Exceptions ||
|---------------------------------|----------------------------|
| `java.time.DateTimeException` | if unable to query |
| `java.lang.ArithmeticException` | if numeric overflow occurs |
