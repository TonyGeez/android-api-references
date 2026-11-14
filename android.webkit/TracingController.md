# TracingController

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TracingController

Kotlin| [Java](TracingController.md) 
| --- | --- |

```
abstract class TracingController
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.TracingController](TracingController.md) |

Manages tracing of WebViews. In particular provides functionality for the app to enable/disable tracing of parts of code and to collect tracing data. This is useful for profiling performance issues, debugging and memory usage analysis in production and real life scenarios.

The resulting trace data is sent back as a byte sequence in json format. This file can be loaded in "chrome://tracing" for further analysis.

Example usage: 

```kotlin
TracingController tracingController = TracingController.getInstance();
  tracingController.start(new TracingConfig.Builder()
                   .addCategories(TracingConfig.CATEGORIES_WEB_DEVELOPER).build());
  ...
  tracingController.stop(new FileOutputStream("trace.json"),
                         Executors.newSingleThreadExecutor());
  
```

<br />

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------|---|
| [TracingController](TracingController.md))`()` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [TracingController](TracingController.md) | [getInstance](TracingController.md))`()` Returns the default TracingController instance. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTracing](TracingController.md))`()` Returns whether the WebView framework is tracing. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](TracingController.md))`(`tracingConfig:` ` [TracingConfig](TracingConfig.md)`)` Starts tracing all webviews. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [stop](TracingController.md))`(`outputStream:` ` [OutputStream](../java.io/OutputStream.md)?`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`)` Stops tracing and flushes tracing data to the specified outputStream. |

## Public constructors

### TracingController

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TracingController()
```

**Deprecated:** *This class should not be constructed by applications, use [getInstance](TracingController.md))instead to fetch the singleton instance.*

## Public methods

### getInstance

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(): TracingController
```

Returns the default TracingController instance. At present there is only one TracingController instance for all WebView instances, however this restriction may be relaxed in a future Android release.

| Return ||
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [TracingController](TracingController.md) | The default TracingController instance. This value cannot be`null`. |

### isTracing

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isTracing(): Boolean
```

Returns whether the WebView framework is tracing.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if tracing is enabled. |

### start

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun start(tracingConfig: TracingConfig): Unit
```

Starts tracing all webviews. Depending on the trace mode in traceConfig specifies how the trace events are recorded. For tracing modes [TracingConfig.RECORD_UNTIL_FULL](TracingConfig.md) and [TracingConfig.RECORD_CONTINUOUSLY](TracingConfig.md) the events are recorded using an internal buffer and flushed to the outputStream when [stop(java.io.OutputStream,java.util.concurrent.Executor)](TracingController.md))is called.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tracingConfig` | [TracingConfig](TracingConfig.md):Configuration options to use for tracing. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If the system is already tracing. |
| `java.lang.IllegalArgumentException` | If the configuration is invalid (e.g. invalid category pattern or invalid tracing mode). |

### stop

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun stop(
    outputStream: OutputStream?, 
    executor: Executor
): Boolean
```

Stops tracing and flushes tracing data to the specified outputStream. The data is sent to the specified output stream in json format typically in chunks by invoking[java.io.OutputStream#write(byte[])](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#write(kotlin.ByteArray)). On completion the java.io.OutputStream#close() method is called.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `outputStream` | [OutputStream](../java.io/OutputStream.md)?:The output stream the tracing data will be sent to. If null the tracing data will be discarded. |
| `executor` | [Executor](../java.util.concurrent/Executor.md):The [java.util.concurrent.Executor](../java.util.concurrent/Executor.md) on which the outputStream[java.io.OutputStream#write(byte[])](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#write(kotlin.ByteArray))and java.io.OutputStream#close() methods will be invoked. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | False if the WebView framework was not tracing at the time of the call, true otherwise. |
