# java.util.logging

# java.util.logging

## Interfaces

| [Filter](https://developer.android.com/reference/kotlin/java/util/logging/Filter) | A Filter can be used to provide fine grain control over what is logged, beyond the control provided by log levels. |
| --- | --- |
| [LoggingMXBean](https://developer.android.com/reference/kotlin/java/util/logging/LoggingMXBean) | The management interface for the logging facility. |

## Classes

| [ConsoleHandler](https://developer.android.com/reference/kotlin/java/util/logging/ConsoleHandler) | This Handler publishes log records to System.err. |
| --- | --- |
| [ErrorManager](https://developer.android.com/reference/kotlin/java/util/logging/ErrorManager) | ErrorManager objects can be attached to Handlers to process any error that occurs on a Handler during Logging. |
| [FileHandler](https://developer.android.com/reference/kotlin/java/util/logging/FileHandler) | Simple file logging Handler. |
| [Formatter](https://developer.android.com/reference/kotlin/java/util/logging/Formatter) | A Formatter provides support for formatting LogRecords. |
| --- | --- |
| [Handler](https://developer.android.com/reference/kotlin/java/util/logging/Handler) | A Handler object takes log messages from a Logger and exports them. |
| [Level](https://developer.android.com/reference/kotlin/java/util/logging/Level) | The Level class defines a set of standard logging levels that can be used to control logging output. |
| [Logger](https://developer.android.com/reference/kotlin/java/util/logging/Logger) | A Logger object is used to log messages for a specific system or application component. |
| --- | --- |
| [LoggingPermission](https://developer.android.com/reference/kotlin/java/util/logging/LoggingPermission) | Legacy security code; do not use. |
| [LogManager](https://developer.android.com/reference/kotlin/java/util/logging/LogManager) | There is a single global LogManager object that is used to maintain a set of shared state about Loggers and log services. |
| [LogRecord](https://developer.android.com/reference/kotlin/java/util/logging/LogRecord) | LogRecord objects are used to pass logging requests between the logging framework and individual log Handlers. |
| --- | --- |
| [MemoryHandler](https://developer.android.com/reference/kotlin/java/util/logging/MemoryHandler) | Handler that buffers requests in a circular buffer in memory. |
| [SimpleFormatter](https://developer.android.com/reference/kotlin/java/util/logging/SimpleFormatter) | Print a brief summary of the`LogRecord`in a human readable format. |
| [SocketHandler](https://developer.android.com/reference/kotlin/java/util/logging/SocketHandler) | Simple network logging Handler. |
| --- | --- |
| [StreamHandler](https://developer.android.com/reference/kotlin/java/util/logging/StreamHandler) | Stream based logging Handler. |
| [XMLFormatter](https://developer.android.com/reference/kotlin/java/util/logging/XMLFormatter) | Format a LogRecord into a standard XML format. |
