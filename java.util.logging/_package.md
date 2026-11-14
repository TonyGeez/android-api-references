# java.util.logging

# java.util.logging

## Interfaces

| [Filter](Filter.md) | A Filter can be used to provide fine grain control over what is logged, beyond the control provided by log levels. |
| --- | --- |
| [LoggingMXBean](LoggingMXBean.md) | The management interface for the logging facility. |

## Classes

| [ConsoleHandler](ConsoleHandler.md) | This Handler publishes log records to System.err. |
| --- | --- |
| [ErrorManager](ErrorManager.md) | ErrorManager objects can be attached to Handlers to process any error that occurs on a Handler during Logging. |
| [FileHandler](FileHandler.md) | Simple file logging Handler. |
| [Formatter](Formatter.md) | A Formatter provides support for formatting LogRecords. |
| --- | --- |
| [Handler](Handler.md) | A Handler object takes log messages from a Logger and exports them. |
| [Level](Level.md) | The Level class defines a set of standard logging levels that can be used to control logging output. |
| [Logger](Logger.md) | A Logger object is used to log messages for a specific system or application component. |
| --- | --- |
| [LoggingPermission](LoggingPermission.md) | Legacy security code; do not use. |
| [LogManager](LogManager.md) | There is a single global LogManager object that is used to maintain a set of shared state about Loggers and log services. |
| [LogRecord](LogRecord.md) | LogRecord objects are used to pass logging requests between the logging framework and individual log Handlers. |
| --- | --- |
| [MemoryHandler](MemoryHandler.md) | Handler that buffers requests in a circular buffer in memory. |
| [SimpleFormatter](SimpleFormatter.md) | Print a brief summary of the`LogRecord`in a human readable format. |
| [SocketHandler](SocketHandler.md) | Simple network logging Handler. |
| --- | --- |
| [StreamHandler](StreamHandler.md) | Stream based logging Handler. |
| [XMLFormatter](XMLFormatter.md) | Format a LogRecord into a standard XML format. |
