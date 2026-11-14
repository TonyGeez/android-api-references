# StatementEventListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StatementEventListener

```
interface StatementEventListener : EventListener
```

| [javax.sql.StatementEventListener](StatementEventListener.md) |

An object that registers to be notified of events that occur on PreparedStatements that are in the Statement pool.

The JDBC 3.0 specification added the maxStatements`ConnectionPooledDataSource`property to provide a standard mechanism for enabling the pooling of`PreparedStatements`and to specify the size of the statement pool. However, there was no way for a driver to notify an external statement pool when a`PreparedStatement`becomes invalid. For some databases, a statement becomes invalid if a DDL operation is performed that affects the table. For example an application may create a temporary table to do some work on the table and then destroy it. It may later recreate the same table when it is needed again. Some databases will invalidate any prepared statements that reference the temporary table when the table is dropped.

Similar to the methods defined in the`ConnectionEventListener`interface, the driver will call the`StatementEventListener.statementErrorOccurred`method prior to throwing any exceptions when it detects a statement is invalid. The driver will also call the`StatementEventListener.statementClosed`method when a`PreparedStatement`is closed.

Methods which allow a component to register a StatementEventListener with a`PooledConnection`have been added to the`PooledConnection`interface.

<br />

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [statementClosed](StatementEventListener.md))`(`event:` ` [StatementEvent](StatementEvent.md)!`)` The driver calls this method on all`StatementEventListener`s registered on the connection when it detects that a`PreparedStatement`is closed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [statementErrorOccurred](StatementEventListener.md))`(`event:` ` [StatementEvent](StatementEvent.md)!`)` The driver calls this method on all`StatementEventListener`s registered on the connection when it detects that a`PreparedStatement`is invalid. |

## Public methods

### statementClosed

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun statementClosed(event: StatementEvent!): Unit
```

The driver calls this method on all`StatementEventListener`s registered on the connection when it detects that a`PreparedStatement`is closed.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [StatementEvent](StatementEvent.md)!:an event object describing the source of the event and that the`PreparedStatement`was closed. |

### statementErrorOccurred

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun statementErrorOccurred(event: StatementEvent!): Unit
```

The driver calls this method on all`StatementEventListener`s registered on the connection when it detects that a`PreparedStatement`is invalid. The driver calls this method just before it throws the`SQLException`, contained in the given event, to the application.

<br />

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [StatementEvent](StatementEvent.md)!:an event object describing the source of the event, the statement that is invalid and the exception the driver is about to throw. The source of the event is the`PooledConnection`which the invalid`PreparedStatement`is associated with. <br /> |
