# StatementEvent

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StatementEvent

```
open class StatementEvent : EventObject
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.EventObject](../java.util/EventObject.md) ||
| | ↳ | [javax.sql.StatementEvent](StatementEvent.md) |

A`StatementEvent`is sent to all`StatementEventListener`s which were registered with a`PooledConnection`. This occurs when the driver determines that a`PreparedStatement`that is associated with the`PooledConnection`has been closed or the driver determines is invalid.

<br />

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StatementEvent](StatementEvent.md))`(`con:` ` [PooledConnection](PooledConnection.md)!`, `statement:` ` [PreparedStatement](../java.sql/PreparedStatement.md)!`)` Constructs a`StatementEvent`with the specified`PooledConnection`and`PreparedStatement`. |
| [StatementEvent](StatementEvent.md))`(`con:` ` [PooledConnection](PooledConnection.md)!`, `statement:` ` [PreparedStatement](../java.sql/PreparedStatement.md)!`, `exception:` ` [SQLException](../java.sql/SQLException.md)!`)` Constructs a`StatementEvent`with the specified`PooledConnection`,`PreparedStatement`and`SQLException` |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [SQLException](../java.sql/SQLException.md)! | [getSQLException](StatementEvent.md))`()` Returns the`SQLException`the driver is about to throw |
| open [PreparedStatement](../java.sql/PreparedStatement.md)! | [getStatement](StatementEvent.md))`()` Returns the`PreparedStatement`that is being closed or is invalid |

| Inherited functions ||
|---|---|
| From class [EventObject](../java.util/EventObject.md) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getSource](../java.util/EventObject.md))`()` <br /> The object on which the Event initially occurred. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java.util/EventObject.md))`()` <br /> Returns a String representation of this EventObject. <br /> | ||

| Inherited properties ||
|---|---|
| From class [EventObject](../java.util/EventObject.md) |-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [source](../java.util/EventObject.md) <br /> The object on which the Event initially occurred. <br /> | ||

## Public constructors

### StatementEvent

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StatementEvent(
    con: PooledConnection!, 
    statement: PreparedStatement!)
```

Constructs a`StatementEvent`with the specified`PooledConnection`and`PreparedStatement`. The`SQLException`contained in the event defaults to null.

<br />

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `con` | [PooledConnection](PooledConnection.md)!:The`PooledConnection`that the closed or invalid`PreparedStatement`is associated with. |
| `statement` | [PreparedStatement](../java.sql/PreparedStatement.md)!:The`PreparedStatement`that is bieng closed or is invalid <br /> |

| Exceptions ||
|--------------------------------------|-----------------|
| `java.lang.IllegalArgumentException` | if`con`is null. |

### StatementEvent

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StatementEvent(
    con: PooledConnection!, 
    statement: PreparedStatement!, 
    exception: SQLException!)
```

Constructs a`StatementEvent`with the specified`PooledConnection`,`PreparedStatement`and`SQLException`

<br />

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `con` | [PooledConnection](PooledConnection.md)!:The`PooledConnection`that the closed or invalid`PreparedStatement`is associated with. |
| `statement` | [PreparedStatement](../java.sql/PreparedStatement.md)!:The`PreparedStatement`that is being closed or is invalid |
| `exception` | [SQLException](../java.sql/SQLException.md)!:The`SQLException `the driver is about to throw to the application |
| --- | --- |

| Exceptions ||
|--------------------------------------|------------------------|
| `java.lang.IllegalArgumentException` | if`con`is null. <br /> |

## Public methods

### getSQLException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSQLException(): SQLException!
```

Returns the`SQLException`the driver is about to throw

<br />

| Return ||
|---------------------------------------------------------------------------------------------|------------------------------------------------------|
| [SQLException](../java.sql/SQLException.md)! | The`SQLException`the driver is about to throw <br /> |

### getStatement

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStatement(): PreparedStatement!
```

Returns the`PreparedStatement`that is being closed or is invalid

<br />

| Return ||
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [PreparedStatement](../java.sql/PreparedStatement.md)! | The`PreparedStatement`that is being closed or is invalid <br /> |
