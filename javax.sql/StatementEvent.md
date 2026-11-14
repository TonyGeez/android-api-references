# StatementEvent

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StatementEvent

```
open class StatementEvent : EventObject
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.util.EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) ||
| | ↳ | [javax.sql.StatementEvent](https://developer.android.com/reference/kotlin/javax/sql/StatementEvent#) |

A`StatementEvent`is sent to all`StatementEventListener`s which were registered with a`PooledConnection`. This occurs when the driver determines that a`PreparedStatement`that is associated with the`PooledConnection`has been closed or the driver determines is invalid.

<br />

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StatementEvent](https://developer.android.com/reference/kotlin/javax/sql/StatementEvent#StatementEvent(javax.sql.PooledConnection,%20java.sql.PreparedStatement))`(`con:` ` [PooledConnection](https://developer.android.com/reference/kotlin/javax/sql/PooledConnection)!`, `statement:` ` [PreparedStatement](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement.html#)!`)` Constructs a`StatementEvent`with the specified`PooledConnection`and`PreparedStatement`. |
| [StatementEvent](https://developer.android.com/reference/kotlin/javax/sql/StatementEvent#StatementEvent(javax.sql.PooledConnection,%20java.sql.PreparedStatement,%20java.sql.SQLException))`(`con:` ` [PooledConnection](https://developer.android.com/reference/kotlin/javax/sql/PooledConnection)!`, `statement:` ` [PreparedStatement](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement.html#)!`, `exception:` ` [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException.html#)!`)` Constructs a`StatementEvent`with the specified`PooledConnection`,`PreparedStatement`and`SQLException` |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException.html#)! | [getSQLException](https://developer.android.com/reference/kotlin/javax/sql/StatementEvent#getSQLException())`()` Returns the`SQLException`the driver is about to throw |
| open [PreparedStatement](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement.html#)! | [getStatement](https://developer.android.com/reference/kotlin/javax/sql/StatementEvent#getStatement())`()` Returns the`PreparedStatement`that is being closed or is invalid |

| Inherited functions ||
|---|---|
| From class [EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getSource](https://developer.android.com/reference/kotlin/java/util/EventObject.html#getSource())`()` <br /> The object on which the Event initially occurred. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/EventObject.html#toString())`()` <br /> Returns a String representation of this EventObject. <br /> | ||

| Inherited properties ||
|---|---|
| From class [EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) |-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [source](https://developer.android.com/reference/kotlin/java/util/EventObject.html#source:kotlin.Any) <br /> The object on which the Event initially occurred. <br /> | ||

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
| `con` | [PooledConnection](https://developer.android.com/reference/kotlin/javax/sql/PooledConnection)!:The`PooledConnection`that the closed or invalid`PreparedStatement`is associated with. |
| `statement` | [PreparedStatement](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement.html#)!:The`PreparedStatement`that is bieng closed or is invalid <br /> |

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
| `con` | [PooledConnection](https://developer.android.com/reference/kotlin/javax/sql/PooledConnection)!:The`PooledConnection`that the closed or invalid`PreparedStatement`is associated with. |
| `statement` | [PreparedStatement](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement.html#)!:The`PreparedStatement`that is being closed or is invalid |
| `exception` | [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException.html#)!:The`SQLException `the driver is about to throw to the application |

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
| [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException.html#)! | The`SQLException`the driver is about to throw <br /> |

### getStatement

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStatement(): PreparedStatement!
```

Returns the`PreparedStatement`that is being closed or is invalid

<br />

| Return ||
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [PreparedStatement](https://developer.android.com/reference/kotlin/java/sql/PreparedStatement.html#)! | The`PreparedStatement`that is being closed or is invalid <br /> |
