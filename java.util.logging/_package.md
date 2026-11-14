# java.util.logging

# java.util.logging

## Interfaces

| [Filter](../java/util/logging/Filter.md) | A Filter can be used to provide fine grain control over what is logged, beyond the control provided by log levels. |
| --- | --- |
| [LoggingMXBean](../java/util/logging/LoggingMXBean.md) | The management interface for the logging facility. |

## Classes

| [ConsoleHandler](../java/util/logging/ConsoleHandler.md) | This Handler publishes log records to System.err. |
| --- | --- |
| [ErrorManager](../java/util/logging/ErrorManager.md) | ErrorManager objects can be attached to Handlers to process any error that occurs on a Handler during Logging. |
| [FileHandler](../java/util/logging/FileHandler.md) | Simple file logging Handler. |
| [Formatter](../java/util/logging/Formatter.md) | A Formatter provides support for formatting LogRecords. |
| --- | --- |
| [Handler](../java/util/logging/Handler.md) | A Handler object takes log messages from a Logger and exports them. |
| [Level](../java/util/logging/Level.md) | The Level class defines a set of standard logging levels that can be used to control logging output. |
| [Logger](../java/util/logging/Logger.md) | A Logger object is used to log messages for a specific system or application component. |
| --- | --- |
| [LoggingPermission](../java/util/logging/LoggingPermission.md) | Legacy security code; do not use. |
| [LogManager](../java/util/logging/LogManager.md) | There is a single global LogManager object that is used to maintain a set of shared state about Loggers and log services. |
| [LogRecord](../java/util/logging/LogRecord.md) | LogRecord objects are used to pass logging requests between the logging framework and individual log Handlers. |
| --- | --- |
| [MemoryHandler](../java/util/logging/MemoryHandler.md) | Handler that buffers requests in a circular buffer in memory. |
| [SimpleFormatter](../java/util/logging/SimpleFormatter.md) | Print a brief summary of the`LogRecord`in a human readable format. |
| [SocketHandler](../java/util/logging/SocketHandler.md) | Simple network logging Handler. |
| --- | --- |
| [StreamHandler](../java/util/logging/StreamHandler.md) | Stream based logging Handler. |
| [XMLFormatter](../java/util/logging/XMLFormatter.md) | Format a LogRecord into a standard XML format. |
