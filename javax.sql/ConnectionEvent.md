# ConnectionEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConnectionEvent

```
open class ConnectionEvent : EventObject
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.util.EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) ||
| | ↳ | [javax.sql.ConnectionEvent](https://developer.android.com/reference/kotlin/javax/sql/ConnectionEvent#) |

An`Event`object that provides information about the source of a connection-related event.`ConnectionEvent`objects are generated when an application closes a pooled connection and when an error occurs. The`ConnectionEvent`object contains two kinds of information:

- The pooled connection closed by the application
- In the case of an error event, the`SQLException`about to be thrown to the application

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ConnectionEvent](https://developer.android.com/reference/kotlin/javax/sql/ConnectionEvent#ConnectionEvent(javax.sql.PooledConnection))`(`con:` ` [PooledConnection](https://developer.android.com/reference/kotlin/javax/sql/PooledConnection)!`)` Constructs a`ConnectionEvent`object initialized with the given`PooledConnection`object. |
| [ConnectionEvent](https://developer.android.com/reference/kotlin/javax/sql/ConnectionEvent#ConnectionEvent(javax.sql.PooledConnection,%20java.sql.SQLException))`(`con:` ` [PooledConnection](https://developer.android.com/reference/kotlin/javax/sql/PooledConnection)!`, `ex:` ` [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException.html#)!`)` Constructs a`ConnectionEvent`object initialized with the given`PooledConnection`object and`SQLException`object. |

| Public methods ||
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException.html#)! | [getSQLException](https://developer.android.com/reference/kotlin/javax/sql/ConnectionEvent#getSQLException())`()` Retrieves the`SQLException`for this`ConnectionEvent`object. |

| Inherited functions ||
|---|---|
| From class [EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getSource](https://developer.android.com/reference/kotlin/java/util/EventObject.html#getSource())`()` <br /> The object on which the Event initially occurred. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/EventObject.html#toString())`()` <br /> Returns a String representation of this EventObject. <br /> | ||

| Inherited properties ||
|---|---|
| From class [EventObject](https://developer.android.com/reference/kotlin/java/util/EventObject.html#) |-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [source](https://developer.android.com/reference/kotlin/java/util/EventObject.html#source:kotlin.Any) <br /> The object on which the Event initially occurred. <br /> | ||

## Public constructors

### ConnectionEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ConnectionEvent(con: PooledConnection!)
```

Constructs a`ConnectionEvent`object initialized with the given`PooledConnection`object.`SQLException`defaults to`null`.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `con` | [PooledConnection](https://developer.android.com/reference/kotlin/javax/sql/PooledConnection)!:the pooled connection that is the source of the event |

| Exceptions ||
|--------------------------------------|-----------------|
| `java.lang.IllegalArgumentException` | if`con`is null. |

### ConnectionEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ConnectionEvent(
    con: PooledConnection!, 
    ex: SQLException!)
```

Constructs a`ConnectionEvent`object initialized with the given`PooledConnection`object and`SQLException`object.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `con` | [PooledConnection](https://developer.android.com/reference/kotlin/javax/sql/PooledConnection)!:the pooled connection that is the source of the event |
| `ex` | [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException.html#)!:the SQLException about to be thrown to the application |

| Exceptions ||
|--------------------------------------|-----------------|
| `java.lang.IllegalArgumentException` | if`con`is null. |

## Public methods

### getSQLException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSQLException(): SQLException!
```

Retrieves the`SQLException`for this`ConnectionEvent`object. May be`null`.

| Return ||
|---------------------------------------------------------------------------------------------|----------------------------------------------|
| [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException.html#)! | the SQLException about to be thrown or`null` |
