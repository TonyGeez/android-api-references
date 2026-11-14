Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Process

```
abstract class Process
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.Process](../java/lang/Process.md) |

The `https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#start()` and `https://developer.android.com/reference/kotlin/java/lang/Runtime#exec(kotlin.Array,%20kotlin.Array,%20java.io.File)` methods create a native process and return an instance of a subclass of `Process` that can be used to control the process and obtain information about it. The class `Process` provides methods for performing input from the process, performing output to the process, waiting for the process to complete, checking the exit status of the process, and destroying (killing) the process.

The methods that create processes may not work well for special processes on certain native platforms, such as native windowing processes, daemon processes, Win16/DOS processes on Microsoft Windows, or shell scripts.

By default, the created subprocess does not have its own terminal or console. All its standard I/O (i.e. stdin, stdout, stderr) operations will be redirected to the parent process, where they can be accessed via the streams obtained using the methods `https://developer.android.com/reference/kotlin/java/lang/Process#getOutputStream()`, `https://developer.android.com/reference/kotlin/java/lang/Process#getInputStream()`, and `https://developer.android.com/reference/kotlin/java/lang/Process#getErrorStream()`. The parent process uses these streams to feed input to and get output from the subprocess. Because some native platforms only provide limited buffer size for standard input and output streams, failure to promptly write the input stream or read the output stream of the subprocess may cause the subprocess to block, or even deadlock.

Where desired, [subprocess I/O can also be redirected](../java/lang/ProcessBuilder.md) using methods of the `https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder` class.

The subprocess is not killed when there are no more references to the `Process` object, but rather the subprocess continues executing asynchronously.

There is no requirement that a process represented by a `Process` object execute asynchronously or concurrently with respect to the Java process that owns the `Process` object.

As of 1.5, `https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#start()` is the preferred way to create a `Process`.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Process#Process()()` <br /> |

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Process#destroy()()` Kills the subprocess. |
| open [Process](../java/lang/Process.md)! | `https://developer.android.com/reference/kotlin/java/lang/Process#destroyForcibly()()` Kills the subprocess. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Process#exitValue()()` Returns the exit value for the subprocess. |
| --- | --- |
| abstract [InputStream](../java/io/InputStream.md)! | `https://developer.android.com/reference/kotlin/java/lang/Process#getErrorStream()()` Returns the input stream connected to the error output of the subprocess. |
| abstract [InputStream](../java/io/InputStream.md)! | `https://developer.android.com/reference/kotlin/java/lang/Process#getInputStream()()` Returns the input stream connected to the normal output of the subprocess. |
| abstract [OutputStream](../java/io/OutputStream.md)! | `https://developer.android.com/reference/kotlin/java/lang/Process#getOutputStream()()` Returns the output stream connected to the normal input of the subprocess. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Process#isAlive()()` Tests whether the subprocess represented by this `Process` is alive. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Process#pid()()` Returns the native process ID of the process. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Process#waitFor()()` Causes the current thread to wait, if necessary, until the process represented by this `Process` object has terminated. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Process#waitFor(kotlin.Long,%20java.util.concurrent.TimeUnit)(timeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit.html#!)` Causes the current thread to wait, if necessary, until the subprocess represented by this `Process` object has terminated, or the specified waiting time elapses. |

## Public constructors

### Process

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Process()
```

## Public methods

### destroy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun destroy(): Unit
```

Kills the subprocess. Whether the subprocess represented by this `Process` object is forcibly terminated or not is implementation dependent.

### destroyForcibly

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun destroyForcibly(): Process!
```

Kills the subprocess. The subprocess represented by this `Process` object is forcibly terminated.

The default implementation of this method invokes `https://developer.android.com/reference/kotlin/java/lang/Process#destroy()` and so may not forcibly terminate the process. Concrete implementations of this class are strongly encouraged to override this method with a compliant implementation. Invoking this method on `Process` objects returned by `https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#start()` and java.lang.Runtime#exec will forcibly terminate the process.

Note: The subprocess may not terminate immediately. i.e. `isAlive()` may return true for a brief period after `destroyForcibly()` is called. This method may be chained to `waitFor()` if needed.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Process#!` | the `Process` object representing the subprocess to be forcibly destroyed. |

### exitValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun exitValue(): Int
```

Returns the exit value for the subprocess.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the exit value of the subprocess represented by this `Process` object. By convention, the value `0` indicates normal termination. |

| Exceptions ||
|---|---|
| `java.lang.IllegalThreadStateException` | if the subprocess represented by this `Process` object has not yet terminated |

### getErrorStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getErrorStream(): InputStream!
```

Returns the input stream connected to the error output of the subprocess. The stream obtains data piped from the error output of the process represented by this `Process` object.

If the standard error of the subprocess has been redirected using java.lang.ProcessBuilder#redirectError(Redirect) or `https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirectErrorStream(kotlin.Boolean)` then this method will return a [null input stream](../java/lang/ProcessBuilder.md).

Implementation note: It is a good idea for the returned input stream to be buffered.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/InputStream.html#!` | the input stream connected to the error output of the subprocess |

### getInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getInputStream(): InputStream!
```

Returns the input stream connected to the normal output of the subprocess. The stream obtains data piped from the standard output of the process represented by this `Process` object.

If the standard output of the subprocess has been redirected using java.lang.ProcessBuilder#redirectOutput(Redirect) then this method will return a [null input stream](../java/lang/ProcessBuilder.md).

Otherwise, if the standard error of the subprocess has been redirected using `https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirectErrorStream(kotlin.Boolean)` then the input stream returned by this method will receive the merged standard output and the standard error of the subprocess.

Implementation note: It is a good idea for the returned input stream to be buffered.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/InputStream.html#!` | the input stream connected to the normal output of the subprocess |

### getOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getOutputStream(): OutputStream!
```

Returns the output stream connected to the normal input of the subprocess. Output to the stream is piped into the standard input of the process represented by this `Process` object.

If the standard input of the subprocess has been redirected using java.lang.ProcessBuilder#redirectInput(Redirect) then this method will return a [null output stream](../java/lang/ProcessBuilder.md).

Implementation note: It is a good idea for the returned output stream to be buffered.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/OutputStream.html#!` | the output stream connected to the normal input of the subprocess |

### isAlive

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAlive(): Boolean
```

Tests whether the subprocess represented by this `Process` is alive.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the subprocess represented by this `Process` object has not yet terminated. |

### pid

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun pid(): Long
```

Returns the native process ID of the process. The native process ID is an identification number that the operating system assigns to the process.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the native process id of the process |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the Process implementation does not support this operation |

### waitFor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun waitFor(): Int
```

Causes the current thread to wait, if necessary, until the process represented by this `Process` object has terminated. This method returns immediately if the subprocess has already terminated. If the subprocess has not yet terminated, the calling thread will be blocked until the subprocess exits.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the exit value of the subprocess represented by this `Process` object. By convention, the value `0` indicates normal termination. |

| Exceptions ||
|---|---|
| `java.lang.InterruptedException` | if the current thread is [interrupted](../java/lang/Thread.md)) by another thread while it is waiting, then the wait is ended and an `https://developer.android.com/reference/kotlin/java/lang/InterruptedException` is thrown. |

### waitFor

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun waitFor(
    timeout: Long, 
    unit: TimeUnit!
): Boolean
```

Causes the current thread to wait, if necessary, until the subprocess represented by this `Process` object has terminated, or the specified waiting time elapses.

If the subprocess has already terminated then this method returns immediately with the value `true`. If the process has not terminated and the timeout value is less than, or equal to, zero, then this method returns immediately with the value `false`.

The default implementation of this methods polls the `exitValue` to check if the process has terminated. Concrete implementations of this class are strongly encouraged to override this method with a more efficient implementation.

| Parameters ||
|---|---|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the maximum time to wait |
| `unit` | [TimeUnit](../java/util/concurrent/TimeUnit.md)!: the time unit of the `timeout` argument |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the subprocess has exited and `false` if the waiting time elapsed before the subprocess has exited. |

| Exceptions ||
|---|---|
| `java.lang.InterruptedException` | if the current thread is interrupted while waiting. |
| `java.lang.NullPointerException` | if unit is null |
