# Filter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Filter

```
@FunctionalInterface interface Filter
```

| [java.util.logging.Filter](Filter.md) |

A Filter can be used to provide fine grain control over what is logged, beyond the control provided by log levels.

Each Logger and each Handler can have a filter associated with it. The Logger or Handler will call the isLoggable method to check if a given LogRecord should be published. If isLoggable returns false, the LogRecord will be discarded.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLoggable](Filter.md))`(`record:` ` [LogRecord](LogRecord.md)!`)` Check if a given log record should be published. |

## Public methods

### isLoggable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isLoggable(record: LogRecord!): Boolean
```

Check if a given log record should be published.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------|
| `record` | [LogRecord](LogRecord.md)!:a LogRecord |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the log record should be published. |
