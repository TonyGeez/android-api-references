# RowSetListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RowSetListener

```
interface RowSetListener : EventListener
```

| [javax.sql.RowSetListener](https://developer.android.com/reference/kotlin/javax/sql/RowSetListener#) |

An interface that must be implemented by a component that wants to be notified when a significant event happens in the life of a`RowSet`object. A component becomes a listener by being registered with a`RowSet`object via the method`RowSet.addRowSetListener`. How a registered component implements this interface determines what it does when it is notified of an event.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cursorMoved](https://developer.android.com/reference/kotlin/javax/sql/RowSetListener#cursorMoved(javax.sql.RowSetEvent))`(`event:` ` [RowSetEvent](https://developer.android.com/reference/kotlin/javax/sql/RowSetEvent)!`)` Notifies registered listeners that a`RowSet`object's cursor has moved. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rowChanged](https://developer.android.com/reference/kotlin/javax/sql/RowSetListener#rowChanged(javax.sql.RowSetEvent))`(`event:` ` [RowSetEvent](https://developer.android.com/reference/kotlin/javax/sql/RowSetEvent)!`)` Notifies registered listeners that a`RowSet`object has had a change in one of its rows. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rowSetChanged](https://developer.android.com/reference/kotlin/javax/sql/RowSetListener#rowSetChanged(javax.sql.RowSetEvent))`(`event:` ` [RowSetEvent](https://developer.android.com/reference/kotlin/javax/sql/RowSetEvent)!`)` Notifies registered listeners that a`RowSet`object in the given`RowSetEvent`object has changed its entire contents. |
| --- | --- |

## Public methods

### cursorMoved

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun cursorMoved(event: RowSetEvent!): Unit
```

Notifies registered listeners that a`RowSet`object's cursor has moved.

The source of the event can be retrieved with the method`event.getSource`.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [RowSetEvent](https://developer.android.com/reference/kotlin/javax/sql/RowSetEvent)!:a`RowSetEvent`object that contains the`RowSet`object that is the source of the event |

### rowChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun rowChanged(event: RowSetEvent!): Unit
```

Notifies registered listeners that a`RowSet`object has had a change in one of its rows.

The source of the event can be retrieved with the method`event.getSource`.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [RowSetEvent](https://developer.android.com/reference/kotlin/javax/sql/RowSetEvent)!:a`RowSetEvent`object that contains the`RowSet`object that is the source of the event |

### rowSetChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun rowSetChanged(event: RowSetEvent!): Unit
```

Notifies registered listeners that a`RowSet`object in the given`RowSetEvent`object has changed its entire contents.

The source of the event can be retrieved with the method`event.getSource`.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [RowSetEvent](https://developer.android.com/reference/kotlin/javax/sql/RowSetEvent)!:a`RowSetEvent`object that contains the`RowSet`object that is the source of the event |
