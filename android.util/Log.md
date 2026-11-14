# Log

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Log

Kotlin| [Java](https://developer.android.com/reference/android/util/Log "View this page in Java") 

```
class Log
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.util.Log](https://developer.android.com/reference/kotlin/android/util/Log#) |

API for sending log output.

Generally, you should use the #v, #d, #i, #w, and #e methods to write logs. You can then [view the logs in logcat](https://developer.android.com/studio/debug/am-logcat.html).

The order in terms of verbosity, from least to most is ERROR, WARN, INFO, DEBUG, VERBOSE.

**Tip:** A good convention is to declare a`TAG`constant in your class: 

```kotlin
private static final String TAG = "MyActivity";
```
and use that in subsequent calls to the log methods.

<br />

**Tip:**Don't forget that when you make a call like 

```kotlin
Log.v(TAG, "index=" + i);
```
that when you're building the string to pass into Log.d, the compiler uses a StringBuilder and at least three allocations occur: the StringBuilder itself, the buffer, and the String object. Realistically, there is also another buffer allocation and copy, and even more pressure on the gc. That means that if your log message is filtered out, you might be doing significant work and incurring significant overhead.

When calling the log methods that take a Throwable parameter, if any of the throwables in the cause chain is an`UnknownHostException`, then the stack trace is not logged.

Note: The return value from the logging functions in this class may vary between Android releases due to changes in the logging implementation. For the methods that return an integer, a positive value may be considered as a successful invocation.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ASSERT](https://developer.android.com/reference/kotlin/android/util/Log#ASSERT:kotlin.Int) Priority constant for the println method. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEBUG](https://developer.android.com/reference/kotlin/android/util/Log#DEBUG:kotlin.Int) Priority constant for the println method; use Log. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](https://developer.android.com/reference/kotlin/android/util/Log#ERROR:kotlin.Int) Priority constant for the println method; use Log. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INFO](https://developer.android.com/reference/kotlin/android/util/Log#INFO:kotlin.Int) Priority constant for the println method; use Log. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VERBOSE](https://developer.android.com/reference/kotlin/android/util/Log#VERBOSE:kotlin.Int) Priority constant for the println method; use Log. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WARN](https://developer.android.com/reference/kotlin/android/util/Log#WARN:kotlin.Int) Priority constant for the println method; use Log. |

| Public methods ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [d](https://developer.android.com/reference/kotlin/android/util/Log#d(kotlin.String,%20kotlin.String))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Send a [DEBUG](https://developer.android.com/reference/kotlin/android/util/Log#DEBUG:kotlin.Int) log message. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [d](https://developer.android.com/reference/kotlin/android/util/Log#d(kotlin.String,%20kotlin.String,%20kotlin.Throwable))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `tr:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Send a [DEBUG](https://developer.android.com/reference/kotlin/android/util/Log#DEBUG:kotlin.Int) log message and log the exception. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [e](https://developer.android.com/reference/kotlin/android/util/Log#e(kotlin.String,%20kotlin.String))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Send an [ERROR](https://developer.android.com/reference/kotlin/android/util/Log#ERROR:kotlin.Int) log message. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [e](https://developer.android.com/reference/kotlin/android/util/Log#e(kotlin.String,%20kotlin.String,%20kotlin.Throwable))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `tr:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Send a [ERROR](https://developer.android.com/reference/kotlin/android/util/Log#ERROR:kotlin.Int) log message and log the exception. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getStackTraceString](https://developer.android.com/reference/kotlin/android/util/Log#getStackTraceString(kotlin.Throwable))`(`tr:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Handy function to get a loggable stack trace from a Throwable |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [i](https://developer.android.com/reference/kotlin/android/util/Log#i(kotlin.String,%20kotlin.String))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Send an [INFO](https://developer.android.com/reference/kotlin/android/util/Log#INFO:kotlin.Int) log message. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [i](https://developer.android.com/reference/kotlin/android/util/Log#i(kotlin.String,%20kotlin.String,%20kotlin.Throwable))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `tr:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Send a [INFO](https://developer.android.com/reference/kotlin/android/util/Log#INFO:kotlin.Int) log message and log the exception. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLoggable](https://developer.android.com/reference/kotlin/android/util/Log#isLoggable(kotlin.String,%20kotlin.Int))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Checks to see whether or not a log for the specified tag is loggable at the specified level. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [println](https://developer.android.com/reference/kotlin/android/util/Log#println(kotlin.Int,%20kotlin.String,%20kotlin.String))`(`priority:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Low-level logging call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [v](https://developer.android.com/reference/kotlin/android/util/Log#v(kotlin.String,%20kotlin.String))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Send a [VERBOSE](https://developer.android.com/reference/kotlin/android/util/Log#VERBOSE:kotlin.Int) log message. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [v](https://developer.android.com/reference/kotlin/android/util/Log#v(kotlin.String,%20kotlin.String,%20kotlin.Throwable))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `tr:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Send a [VERBOSE](https://developer.android.com/reference/kotlin/android/util/Log#VERBOSE:kotlin.Int) log message and log the exception. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [w](https://developer.android.com/reference/kotlin/android/util/Log#w(kotlin.String,%20kotlin.String))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Send a [WARN](https://developer.android.com/reference/kotlin/android/util/Log#WARN:kotlin.Int) log message. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [w](https://developer.android.com/reference/kotlin/android/util/Log#w(kotlin.String,%20kotlin.String,%20kotlin.Throwable))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `tr:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Send a [WARN](https://developer.android.com/reference/kotlin/android/util/Log#WARN:kotlin.Int) log message and log the exception. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [w](https://developer.android.com/reference/kotlin/android/util/Log#w(kotlin.String,%20kotlin.Throwable))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `tr:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Send a [WARN](https://developer.android.com/reference/kotlin/android/util/Log#WARN:kotlin.Int) log message and log the exception. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [wtf](https://developer.android.com/reference/kotlin/android/util/Log#wtf(kotlin.String,%20kotlin.String))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` What a Terrible Failure: Report a condition that should never happen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [wtf](https://developer.android.com/reference/kotlin/android/util/Log#wtf(kotlin.String,%20kotlin.String,%20kotlin.Throwable))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `tr:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` What a Terrible Failure: Report an exception that should never happen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [wtf](https://developer.android.com/reference/kotlin/android/util/Log#wtf(kotlin.String,%20kotlin.Throwable))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `tr:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`)` What a Terrible Failure: Report an exception that should never happen. |

## Constants

### ASSERT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ASSERT: Int
```

Priority constant for the println method. 

 Value: 7

### DEBUG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEBUG: Int
```

Priority constant for the println method; use Log.d. 

 Value: 3

### ERROR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR: Int
```

Priority constant for the println method; use Log.e. 

 Value: 6

### INFO

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INFO: Int
```

Priority constant for the println method; use Log.i. 

 Value: 4

### VERBOSE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VERBOSE: Int
```

Priority constant for the println method; use Log.v. 

 Value: 2

### WARN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WARN: Int
```

Priority constant for the println method; use Log.w. 

 Value: 5

## Public methods

### d

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun d(
    tag: String?, 
    msg: String
): Int
```

Send a [DEBUG](https://developer.android.com/reference/kotlin/android/util/Log#DEBUG:kotlin.Int) log message.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Used to identify the source of a log message. It usually identifies the class or activity where the log call occurs. This value may be`null`. |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The message you would like logged. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A positive value if the message was loggable (see [isLoggable](https://developer.android.com/reference/kotlin/android/util/Log#isLoggable(kotlin.String,%20kotlin.Int))). |

### d

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun d(
    tag: String?, 
    msg: String?, 
    tr: Throwable?
): Int
```

Send a [DEBUG](https://developer.android.com/reference/kotlin/android/util/Log#DEBUG:kotlin.Int) log message and log the exception.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Used to identify the source of a log message. It usually identifies the class or activity where the log call occurs. This value may be`null`. |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The message you would like logged. This value may be`null`. |
| `tr` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:An exception to log. This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A positive value if the message was loggable (see [isLoggable](https://developer.android.com/reference/kotlin/android/util/Log#isLoggable(kotlin.String,%20kotlin.Int))). |

### e

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun e(
    tag: String?, 
    msg: String
): Int
```

Send an [ERROR](https://developer.android.com/reference/kotlin/android/util/Log#ERROR:kotlin.Int) log message.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Used to identify the source of a log message. It usually identifies the class or activity where the log call occurs. This value may be`null`. |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The message you would like logged. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A positive value if the message was loggable (see [isLoggable](https://developer.android.com/reference/kotlin/android/util/Log#isLoggable(kotlin.String,%20kotlin.Int))). |

### e

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun e(
    tag: String?, 
    msg: String?, 
    tr: Throwable?
): Int
```

Send a [ERROR](https://developer.android.com/reference/kotlin/android/util/Log#ERROR:kotlin.Int) log message and log the exception.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Used to identify the source of a log message. It usually identifies the class or activity where the log call occurs. This value may be`null`. |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The message you would like logged. This value may be`null`. |
| `tr` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:An exception to log. This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A positive value if the message was loggable (see [isLoggable](https://developer.android.com/reference/kotlin/android/util/Log#isLoggable(kotlin.String,%20kotlin.Int))). |

### getStackTraceString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getStackTraceString(tr: Throwable?): String
```

Handy function to get a loggable stack trace from a Throwable

If any of the throwables in the cause chain is an`UnknownHostException`, this returns an empty string.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------|
| `tr` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:An exception to log. This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### i

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun i(
    tag: String?, 
    msg: String
): Int
```

Send an [INFO](https://developer.android.com/reference/kotlin/android/util/Log#INFO:kotlin.Int) log message.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Used to identify the source of a log message. It usually identifies the class or activity where the log call occurs. This value may be`null`. |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The message you would like logged. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A positive value if the message was loggable (see [isLoggable](https://developer.android.com/reference/kotlin/android/util/Log#isLoggable(kotlin.String,%20kotlin.Int))). |

### i

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun i(
    tag: String?, 
    msg: String?, 
    tr: Throwable?
): Int
```

Send a [INFO](https://developer.android.com/reference/kotlin/android/util/Log#INFO:kotlin.Int) log message and log the exception.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Used to identify the source of a log message. It usually identifies the class or activity where the log call occurs. This value may be`null`. |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The message you would like logged. This value may be`null`. |
| `tr` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:An exception to log. This value may be`null`. |

### isLoggable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isLoggable(
    tag: String?, 
    level: Int
): Boolean
```

Checks to see whether or not a log for the specified tag is loggable at the specified level. The default level of any tag is set to INFO. This means that any level above and including INFO will be logged. Before you make any calls to a logging method you should check to see if your tag should be logged. You can change the default level by setting a system property: 'setprop log.tag.\<YOUR_LOG_TAG\> \<LEVEL\>' Where level is either VERBOSE, DEBUG, INFO, WARN, ERROR, or ASSERT. You can also create a local.prop file that with the following in it: 'log.tag.\<YOUR_LOG_TAG\>=\<LEVEL\>' and place that in /data/local.prop.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The tag to check. This value may be`null`. |
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The level to check. Value is [android.util.Log#ASSERT](https://developer.android.com/reference/kotlin/android/util/Log#ASSERT:kotlin.Int), [android.util.Log#ERROR](https://developer.android.com/reference/kotlin/android/util/Log#ERROR:kotlin.Int), [android.util.Log#WARN](https://developer.android.com/reference/kotlin/android/util/Log#WARN:kotlin.Int), [android.util.Log#INFO](https://developer.android.com/reference/kotlin/android/util/Log#INFO:kotlin.Int), [android.util.Log#DEBUG](https://developer.android.com/reference/kotlin/android/util/Log#DEBUG:kotlin.Int), or [android.util.Log#VERBOSE](https://developer.android.com/reference/kotlin/android/util/Log#VERBOSE:kotlin.Int) |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether or not that this is allowed to be logged. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | is thrown if the tag.length() \> 23 for Nougat (7.0) and prior releases (API \<= 25), there is no tag limit of concern after this API level. |

### println

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun println(
    priority: Int, 
    tag: String?, 
    msg: String
): Int
```

Low-level logging call.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `priority` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The priority/type of this log message Value is [android.util.Log#ASSERT](https://developer.android.com/reference/kotlin/android/util/Log#ASSERT:kotlin.Int), [android.util.Log#ERROR](https://developer.android.com/reference/kotlin/android/util/Log#ERROR:kotlin.Int), [android.util.Log#WARN](https://developer.android.com/reference/kotlin/android/util/Log#WARN:kotlin.Int), [android.util.Log#INFO](https://developer.android.com/reference/kotlin/android/util/Log#INFO:kotlin.Int), [android.util.Log#DEBUG](https://developer.android.com/reference/kotlin/android/util/Log#DEBUG:kotlin.Int), or [android.util.Log#VERBOSE](https://developer.android.com/reference/kotlin/android/util/Log#VERBOSE:kotlin.Int) |
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Used to identify the source of a log message. It usually identifies the class or activity where the log call occurs. This value may be`null`. |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The message you would like logged. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A positive value if the message was loggable (see [isLoggable](https://developer.android.com/reference/kotlin/android/util/Log#isLoggable(kotlin.String,%20kotlin.Int))). |

### v

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun v(
    tag: String?, 
    msg: String
): Int
```

Send a [VERBOSE](https://developer.android.com/reference/kotlin/android/util/Log#VERBOSE:kotlin.Int) log message.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Used to identify the source of a log message. It usually identifies the class or activity where the log call occurs. This value may be`null`. |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The message you would like logged. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A positive value if the message was loggable (see [isLoggable](https://developer.android.com/reference/kotlin/android/util/Log#isLoggable(kotlin.String,%20kotlin.Int))). |

### v

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun v(
    tag: String?, 
    msg: String?, 
    tr: Throwable?
): Int
```

Send a [VERBOSE](https://developer.android.com/reference/kotlin/android/util/Log#VERBOSE:kotlin.Int) log message and log the exception.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Used to identify the source of a log message. It usually identifies the class or activity where the log call occurs. This value may be`null`. |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The message you would like logged. This value may be`null`. |
| `tr` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:An exception to log. This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A positive value if the message was loggable (see [isLoggable](https://developer.android.com/reference/kotlin/android/util/Log#isLoggable(kotlin.String,%20kotlin.Int))). |

### w

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun w(
    tag: String?, 
    msg: String
): Int
```

Send a [WARN](https://developer.android.com/reference/kotlin/android/util/Log#WARN:kotlin.Int) log message.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Used to identify the source of a log message. It usually identifies the class or activity where the log call occurs. This value may be`null`. |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The message you would like logged. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A positive value if the message was loggable (see [isLoggable](https://developer.android.com/reference/kotlin/android/util/Log#isLoggable(kotlin.String,%20kotlin.Int))). |

### w

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun w(
    tag: String?, 
    msg: String?, 
    tr: Throwable?
): Int
```

Send a [WARN](https://developer.android.com/reference/kotlin/android/util/Log#WARN:kotlin.Int) log message and log the exception.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Used to identify the source of a log message. It usually identifies the class or activity where the log call occurs. This value may be`null`. |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The message you would like logged. This value may be`null`. |
| `tr` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:An exception to log. This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A positive value if the message was loggable (see [isLoggable](https://developer.android.com/reference/kotlin/android/util/Log#isLoggable(kotlin.String,%20kotlin.Int))). |

### w

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun w(
    tag: String?, 
    tr: Throwable?
): Int
```

Send a [WARN](https://developer.android.com/reference/kotlin/android/util/Log#WARN:kotlin.Int) log message and log the exception.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Used to identify the source of a log message. It usually identifies the class or activity where the log call occurs. This value may be`null`. |
| `tr` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:An exception to log. This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A positive value if the message was loggable (see [isLoggable](https://developer.android.com/reference/kotlin/android/util/Log#isLoggable(kotlin.String,%20kotlin.Int))). |

### wtf

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun wtf(
    tag: String?, 
    msg: String?
): Int
```

What a Terrible Failure: Report a condition that should never happen. The error will always be logged at level ASSERT with the call stack. Depending on system configuration, a report may be added to the [android.os.DropBoxManager](https://developer.android.com/reference/kotlin/android/os/DropBoxManager.html#) and/or the process may be terminated immediately with an error dialog.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Used to identify the source of a log message. This value may be`null`. |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The message you would like logged. This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A positive value if the message was loggable (see [isLoggable](https://developer.android.com/reference/kotlin/android/util/Log#isLoggable(kotlin.String,%20kotlin.Int))). |

### wtf

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun wtf(
    tag: String?, 
    msg: String?, 
    tr: Throwable?
): Int
```

What a Terrible Failure: Report an exception that should never happen. Similar to [wtf(java.lang.String,java.lang.Throwable)](https://developer.android.com/reference/kotlin/android/util/Log#wtf(kotlin.String,%20kotlin.Throwable)), with a message as well.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Used to identify the source of a log message. This value may be`null`. |
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The message you would like logged. This value may be`null`. |
| `tr` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:An exception to log. May be null. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A positive value if the message was loggable (see [isLoggable](https://developer.android.com/reference/kotlin/android/util/Log#isLoggable(kotlin.String,%20kotlin.Int))). |

### wtf

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun wtf(
    tag: String?, 
    tr: Throwable
): Int
```

What a Terrible Failure: Report an exception that should never happen. Similar to [wtf(java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/util/Log#wtf(kotlin.String,%20kotlin.String)), with an exception to log.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Used to identify the source of a log message. This value may be`null`. |
| `tr` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html):An exception to log. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A positive value if the message was loggable (see [isLoggable](https://developer.android.com/reference/kotlin/android/util/Log#isLoggable(kotlin.String,%20kotlin.Int))). |
