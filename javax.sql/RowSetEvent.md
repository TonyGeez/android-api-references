# RowSetEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RowSetEvent

```
open class RowSetEvent : EventObject
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.EventObject](../java.util/EventObject.md) ||
| | ↳ | [javax.sql.RowSetEvent](RowSetEvent.md) |

An`Event`object generated when an event occurs to a`RowSet`object. A`RowSetEvent`object is generated when a single row in a rowset is changed, the whole rowset is changed, or the rowset cursor moves.

When an event occurs on a`RowSet`object, one of the`RowSetListener`methods will be sent to all registered listeners to notify them of the event. An`Event`object is supplied to the`RowSetListener`method so that the listener can use it to find out which`RowSet`object is the source of the event.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RowSetEvent](RowSetEvent.md))`(`source:` ` [RowSet](RowSet.md)!`)` Constructs a`RowSetEvent`object initialized with the given`RowSet`object. |

| Inherited functions ||
|---|---|
| From class [EventObject](../java.util/EventObject.md) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getSource](../java.util/EventObject.md))`()` <br /> The object on which the Event initially occurred. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java.util/EventObject.md))`()` <br /> Returns a String representation of this EventObject. <br /> | ||

| Inherited properties ||
|---|---|
| From class [EventObject](../java.util/EventObject.md) |-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [source](../java.util/EventObject.md) <br /> The object on which the Event initially occurred. <br /> | ||

## Public constructors

### RowSetEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RowSetEvent(source: RowSet!)
```

Constructs a`RowSetEvent`object initialized with the given`RowSet`object.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [RowSet](RowSet.md)!:the`RowSet`object whose data has changed or whose cursor has moved |

| Exceptions ||
|--------------------------------------|--------------------|
| `java.lang.IllegalArgumentException` | if`source`is null. |
