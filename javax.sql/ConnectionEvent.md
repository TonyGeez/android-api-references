# ConnectionEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConnectionEvent

```
open class ConnectionEvent : EventObject
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.EventObject](../java/util/EventObject.md) ||
| | ↳ | [javax.sql.ConnectionEvent](../javax/sql/ConnectionEvent.md) |

An`Event`object that provides information about the source of a connection-related event.`ConnectionEvent`objects are generated when an application closes a pooled connection and when an error occurs. The`ConnectionEvent`object contains two kinds of information:

- The pooled connection closed by the application
- In the case of an error event, the`SQLException`about to be thrown to the application

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ConnectionEvent](../javax/sql/ConnectionEvent.md))`(`con:` ` [PooledConnection](../javax/sql/PooledConnection.md)!`)` Constructs a`ConnectionEvent`object initialized with the given`PooledConnection`object. |
| [ConnectionEvent](../javax/sql/ConnectionEvent.md))`(`con:` ` [PooledConnection](../javax/sql/PooledConnection.md)!`, `ex:` ` [SQLException](../java/sql/SQLException.md)!`)` Constructs a`ConnectionEvent`object initialized with the given`PooledConnection`object and`SQLException`object. |

| Public methods ||
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [SQLException](../java/sql/SQLException.md)! | [getSQLException](../javax/sql/ConnectionEvent.md))`()` Retrieves the`SQLException`for this`ConnectionEvent`object. |

| Inherited functions ||
|---|---|
| From class [EventObject](../java/util/EventObject.md) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getSource](../java/util/EventObject.md))`()` <br /> The object on which the Event initially occurred. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/util/EventObject.md))`()` <br /> Returns a String representation of this EventObject. <br /> | ||

| Inherited properties ||
|---|---|
| From class [EventObject](../java/util/EventObject.md) |-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [source](../java/util/EventObject.md) <br /> The object on which the Event initially occurred. <br /> | ||

## Public constructors

### ConnectionEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ConnectionEvent(con: PooledConnection!)
```

Constructs a`ConnectionEvent`object initialized with the given`PooledConnection`object.`SQLException`defaults to`null`.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `con` | [PooledConnection](../javax/sql/PooledConnection.md)!:the pooled connection that is the source of the event |

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
| `con` | [PooledConnection](../javax/sql/PooledConnection.md)!:the pooled connection that is the source of the event |
| `ex` | [SQLException](../java/sql/SQLException.md)!:the SQLException about to be thrown to the application |

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
| [SQLException](../java/sql/SQLException.md)! | the SQLException about to be thrown or`null` |
