# RowSetEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RowSetEvent

```
open class RowSetEvent : EventObject
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) ||
| | ↳ | [javax.sql.RowSetEvent](https://developer.android.com/reference/kotlin/javax/sql/RowSetEvent#) |

An`Event`object generated when an event occurs to a`RowSet`object. A`RowSetEvent`object is generated when a single row in a rowset is changed, the whole rowset is changed, or the rowset cursor moves.

When an event occurs on a`RowSet`object, one of the`RowSetListener`methods will be sent to all registered listeners to notify them of the event. An`Event`object is supplied to the`RowSetListener`method so that the listener can use it to find out which`RowSet`object is the source of the event.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RowSetEvent](https://developer.android.com/reference/kotlin/javax/sql/RowSetEvent#RowSetEvent(javax.sql.RowSet))`(`source:` ` [RowSet](https://developer.android.com/reference/kotlin/javax/sql/RowSet)!`)` Constructs a`RowSetEvent`object initialized with the given`RowSet`object. |

| Inherited functions ||
|---|---|
| From class [EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getSource](https://developer.android.com/reference/kotlin/java/util/EventObject.html#getSource())`()` <br /> The object on which the Event initially occurred. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/EventObject.html#toString())`()` <br /> Returns a String representation of this EventObject. <br /> | ||

| Inherited properties ||
|---|---|
| From class [EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) |-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [source](https://developer.android.com/reference/kotlin/java/util/EventObject.html#source:kotlin.Any) <br /> The object on which the Event initially occurred. <br /> | ||

## Public constructors

### RowSetEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RowSetEvent(source: RowSet!)
```

Constructs a`RowSetEvent`object initialized with the given`RowSet`object.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [RowSet](https://developer.android.com/reference/kotlin/javax/sql/RowSet)!:the`RowSet`object whose data has changed or whose cursor has moved |

| Exceptions ||
|--------------------------------------|--------------------|
| `java.lang.IllegalArgumentException` | if`source`is null. |
