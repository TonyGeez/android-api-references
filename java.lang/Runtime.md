# Runtime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Runtime

```
open class Runtime
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.Runtime](Runtime.md) |

Every Java application has a single instance of class `Runtime` that allows the application to interface with the environment in which the application is running. The current runtime can be obtained from the `getRuntime` method.

An application cannot create its own instance of this class.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addShutdownHook](Runtime.md))`(`hook:` ` [Thread](Thread.md)!`)` Registers a new virtual-machine shutdown hook. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [availableProcessors](Runtime.md))`()` Returns the number of processors available to the Java virtual machine. |
| open [Process](Process.md)! | [exec](Runtime.md))`(`command:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Executes the specified string command in a separate process. |
| --- | --- |
| open [Process](Process.md)! | [exec](Runtime.md))`(`command:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `envp:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Executes the specified string command in a separate process with the specified environment. |
| open [Process](Process.md)! | [exec](Runtime.md))`(`command:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `envp:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `dir:` ` [File](../java.io/File.md)!`)` Executes the specified string command in a separate process with the specified environment and working directory. |
| open [Process](Process.md)! | [exec](Runtime.md))`(`cmdarray:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Executes the specified command and arguments in a separate process. |
| --- | --- |
| open [Process](Process.md)! | [exec](Runtime.md))`(`cmdarray:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `envp:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Executes the specified command and arguments in a separate process with the specified environment. |
| open [Process](Process.md)! | [exec](Runtime.md))`(`cmdarray:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `envp:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `dir:` ` [File](../java.io/File.md)!`)` Executes the specified command and arguments in a separate process with the specified environment and working directory. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [exit](Runtime.md))`(`status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Terminates the currently running Java virtual machine by initiating its shutdown sequence. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [freeMemory](Runtime.md))`()` Returns the amount of free memory in the Java Virtual Machine. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [gc](Runtime.md))`()` Runs the garbage collector. |
| open static [Runtime](Runtime.md)! | [getRuntime](Runtime.md))`()` Returns the runtime object associated with the current Java application. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [halt](Runtime.md))`(`status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Forcibly terminates the currently running Java virtual machine. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [load](Runtime.md))`(`filename:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Loads the native library specified by the filename argument. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadLibrary](Runtime.md))`(`libname:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Loads the native library specified by the `libname` argument. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [maxMemory](Runtime.md))`()` Returns the maximum amount of memory that the Java virtual machine will attempt to use. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeShutdownHook](Runtime.md))`(`hook:` ` [Thread](Thread.md)!`)` De-registers a previously-registered virtual-machine shutdown hook. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runFinalization](Runtime.md))`()` Runs the finalization methods of any objects pending finalization. |
| --- | --- |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runFinalizersOnExit](Runtime.md))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enable or disable finalization on exit; doing so specifies that the finalizers of all objects that have finalizers that have not yet been automatically invoked are to be run before the Java runtime exits. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [totalMemory](Runtime.md))`()` Returns the total amount of memory in the Java virtual machine. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [traceInstructions](Runtime.md))`(`on:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Not implemented, does nothing. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [traceMethodCalls](Runtime.md))`(`on:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Not implemented, does nothing. |

## Public methods

### addShutdownHook

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addShutdownHook(hook: Thread!): Unit
```

Registers a new virtual-machine shutdown hook.

The Java virtual machine *shuts down* in response to two kinds of events:

- The program *exits* normally, when the last non-daemon thread exits or when the [exit](Runtime.md)) (equivalently, [System.exit](System.md))) method is invoked, or
- The virtual machine is *terminated* in response to a user interrupt, such as typing `^C`, or a system-wide event, such as user logoff or system shutdown.

A *shutdown hook* is simply an initialized but unstarted thread. When the virtual machine begins its shutdown sequence it will start all registered shutdown hooks in some unspecified order and let them run concurrently. When all the hooks have finished it will then halt. Note that daemon threads will continue to run during the shutdown sequence, as will non-daemon threads if shutdown was initiated by invoking the [exit](Runtime.md)) method.

Once the shutdown sequence has begun it can be stopped only by invoking the [halt](Runtime.md)) method, which forcibly terminates the virtual machine.

Once the shutdown sequence has begun it is impossible to register a new shutdown hook or de-register a previously-registered hook. Attempting either of these operations will cause an [IllegalStateException](IllegalStateException.md) to be thrown.

Shutdown hooks run at a delicate time in the life cycle of a virtual machine and should therefore be coded defensively. They should, in particular, be written to be thread-safe and to avoid deadlocks insofar as possible. They should also not rely blindly upon services that may have registered their own shutdown hooks and therefore may themselves in the process of shutting down. Attempts to use other thread-based services such as the AWT event-dispatch thread, for example, may lead to deadlocks.

Shutdown hooks should also finish their work quickly. When a program invokes [exit](Runtime.md)) the expectation is that the virtual machine will promptly shut down and exit. When the virtual machine is terminated due to user logoff or system shutdown the underlying operating system may only allow a fixed amount of time in which to shut down and exit. It is therefore inadvisable to attempt any user interaction or to perform a long-running computation in a shutdown hook.

Uncaught exceptions are handled in shutdown hooks just as in any other thread, by invoking the [uncaughtException](ThreadGroup.md)) method of the thread's [ThreadGroup](ThreadGroup.md) object. The default implementation of this method prints the exception's stack trace to [System.err](System.md) and terminates the thread; it does not cause the virtual machine to exit or halt.

In rare circumstances the virtual machine may *abort* , that is, stop running without shutting down cleanly. This occurs when the virtual machine is terminated externally, for example with the `SIGKILL` signal on Unix or the `TerminateProcess` call on Microsoft Windows. The virtual machine may also abort if a native method goes awry by, for example, corrupting internal data structures or attempting to access nonexistent memory. If the virtual machine aborts then no guarantee can be made about whether or not any shutdown hooks will be run.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `hook` | [Thread](Thread.md)!: An initialized but unstarted [Thread](Thread.md) object |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the specified hook has already been registered, or if it can be determined that the hook is already running or has already been run |
| `java.lang.IllegalStateException` | If the virtual machine is already in the process of shutting down |
| `java.lang.SecurityException` | If a security manager is present and it denies [RuntimePermission](RuntimePermission.md)("shutdownHooks") |
| --- | --- |

**See Also**

- [#removeShutdownHook](Runtime.md))
- [#halt(int)](Runtime.md))
- [#exit(int)](Runtime.md)) 

### availableProcessors

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun availableProcessors(): Int
```

Returns the number of processors available to the Java virtual machine.

This value may change during a particular invocation of the virtual machine. Applications that are sensitive to the number of available processors should therefore occasionally poll this property and adjust their resource usage appropriately.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of processors available to the virtual machine; never smaller than one |

### exec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun exec(command: String!): Process!
```

Executes the specified string command in a separate process.

This is a convenience method. An invocation of the form `exec(command)` behaves in exactly the same way as the invocation [exec](Runtime.md))`(command, null, null)`.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------|
| `command` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a specified system command. |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Process](Process.md)! | A new [Process](Process.md) object for managing the subprocess |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | If a security manager exists and its [checkExec](SecurityManager.md)) method doesn't allow creation of the subprocess |
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.NullPointerException` | If `command` is `null` |
| --- | --- |
| `java.lang.IllegalArgumentException` | If `command` is empty |

**See Also**

- [#exec(String[], String[], File)](https://developer.android.com/reference/kotlin/java/lang/Runtime#exec(kotlin.Array,%20kotlin.Array,%20java.io.File))
- [java.lang.ProcessBuilder](ProcessBuilder.md) 

### exec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun exec(
    command: String!, 
    envp: Array<String!>!
): Process!
```

Executes the specified string command in a separate process with the specified environment.

This is a convenience method. An invocation of the form `exec(command, envp)` behaves in exactly the same way as the invocation [exec](Runtime.md))`(command, envp, null)`.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `command` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a specified system command. |
| `envp` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: array of strings, each element of which has environment variable settings in the format *name* =*value* , or `null` if the subprocess should inherit the environment of the current process. |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Process](Process.md)! | A new [Process](Process.md) object for managing the subprocess |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | If a security manager exists and its [checkExec](SecurityManager.md)) method doesn't allow creation of the subprocess |
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.NullPointerException` | If `command` is `null`, or one of the elements of `envp` is `null` |
| --- | --- |
| `java.lang.IllegalArgumentException` | If `command` is empty |

**See Also**

- [#exec(String[], String[], File)](https://developer.android.com/reference/kotlin/java/lang/Runtime#exec(kotlin.Array,%20kotlin.Array,%20java.io.File))
- [java.lang.ProcessBuilder](ProcessBuilder.md) 

### exec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun exec(
    command: String!, 
    envp: Array<String!>!, 
    dir: File!
): Process!
```

Executes the specified string command in a separate process with the specified environment and working directory.

This is a convenience method. An invocation of the form `exec(command, envp, dir)` behaves in exactly the same way as the invocation [exec](Runtime.md))`(cmdarray, envp, dir)`, where `cmdarray` is an array of all the tokens in `command`.

More precisely, the `command` string is broken into tokens using a [StringTokenizer](../java.util/StringTokenizer.md) created by the call `new { StringTokenizer}(command)` with no further modification of the character categories. The tokens produced by the tokenizer are then placed in the new string array `cmdarray`, in the same order.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `command` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a specified system command. |
| `envp` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: array of strings, each element of which has environment variable settings in the format *name* =*value* , or `null` if the subprocess should inherit the environment of the current process. |
| `dir` | [File](../java.io/File.md)!: the working directory of the subprocess, or `null` if the subprocess should inherit the working directory of the current process. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Process](Process.md)! | A new [Process](Process.md) object for managing the subprocess |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | If a security manager exists and its [checkExec](SecurityManager.md)) method doesn't allow creation of the subprocess |
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.NullPointerException` | If `command` is `null`, or one of the elements of `envp` is `null` |
| --- | --- |
| `java.lang.IllegalArgumentException` | If `command` is empty |

**See Also**

- [java.lang.ProcessBuilder](ProcessBuilder.md) 

### exec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun exec(cmdarray: Array<String!>!): Process!
```

Executes the specified command and arguments in a separate process.

This is a convenience method. An invocation of the form `exec(cmdarray)` behaves in exactly the same way as the invocation [exec](Runtime.md))`(cmdarray, null, null)`.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cmdarray` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: array containing the command to call and its arguments. |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Process](Process.md)! | A new [Process](Process.md) object for managing the subprocess |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | If a security manager exists and its [checkExec](SecurityManager.md)) method doesn't allow creation of the subprocess |
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.NullPointerException` | If `cmdarray` is `null`, or one of the elements of `cmdarray` is `null` |
| --- | --- |
| `java.lang.IndexOutOfBoundsException` | If `cmdarray` is an empty array (has length `0`) |

**See Also**

- [java.lang.ProcessBuilder](ProcessBuilder.md) 

### exec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun exec(
    cmdarray: Array<String!>!, 
    envp: Array<String!>!
): Process!
```

Executes the specified command and arguments in a separate process with the specified environment.

This is a convenience method. An invocation of the form `exec(cmdarray, envp)` behaves in exactly the same way as the invocation [exec](Runtime.md))`(cmdarray, envp, null)`.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cmdarray` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: array containing the command to call and its arguments. |
| `envp` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: array of strings, each element of which has environment variable settings in the format *name* =*value* , or `null` if the subprocess should inherit the environment of the current process. |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Process](Process.md)! | A new [Process](Process.md) object for managing the subprocess |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | If a security manager exists and its [checkExec](SecurityManager.md)) method doesn't allow creation of the subprocess |
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.NullPointerException` | If `cmdarray` is `null`, or one of the elements of `cmdarray` is `null`, or one of the elements of `envp` is `null` |
| --- | --- |
| `java.lang.IndexOutOfBoundsException` | If `cmdarray` is an empty array (has length `0`) |

**See Also**

- [java.lang.ProcessBuilder](ProcessBuilder.md) 

### exec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun exec(
    cmdarray: Array<String!>!, 
    envp: Array<String!>!, 
    dir: File!
): Process!
```

Executes the specified command and arguments in a separate process with the specified environment and working directory.

Given an array of strings `cmdarray`, representing the tokens of a command line, and an array of strings `envp`, representing "environment" variable settings, this method creates a new process in which to execute the specified command.

This method checks that `cmdarray` is a valid operating system command. Which commands are valid is system-dependent, but at the very least the command must be a non-empty list of non-null strings.

If `envp` is `null`, the subprocess inherits the environment settings of the current process.

A minimal set of system dependent environment variables may be required to start a process on some operating systems. As a result, the subprocess may inherit additional environment variable settings beyond those in the specified environment.

[ProcessBuilder.start()](ProcessBuilder.md)) is now the preferred way to start a process with a modified environment.

The working directory of the new subprocess is specified by `dir`. If `dir` is `null`, the subprocess inherits the current working directory of the current process.

If a security manager exists, its [checkExec](SecurityManager.md)) method is invoked with the first component of the array `cmdarray` as its argument. This may result in a [SecurityException](SecurityException.md) being thrown.

Starting an operating system process is highly system-dependent. Among the many things that can go wrong are:

- The operating system program file was not found.
- Access to the program file was denied.
- The working directory does not exist.

In such cases an exception will be thrown. The exact nature of the exception is system-dependent, but it will always be a subclass of [IOException](../java.io/IOException.md).

If the operating system does not support the creation of processes, an [UnsupportedOperationException](UnsupportedOperationException.md) will be thrown.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cmdarray` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: array containing the command to call and its arguments. |
| `envp` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: array of strings, each element of which has environment variable settings in the format *name* =*value* , or `null` if the subprocess should inherit the environment of the current process. |
| `dir` | [File](../java.io/File.md)!: the working directory of the subprocess, or `null` if the subprocess should inherit the working directory of the current process. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Process](Process.md)! | A new [Process](Process.md) object for managing the subprocess |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | If a security manager exists and its [checkExec](SecurityManager.md)) method doesn't allow creation of the subprocess |
| `java.lang.UnsupportedOperationException` | If the operating system does not support the creation of processes. |
| `java.io.IOException` | If an I/O error occurs |
| --- | --- |
| `java.lang.NullPointerException` | If `cmdarray` is `null`, or one of the elements of `cmdarray` is `null`, or one of the elements of `envp` is `null` |
| `java.lang.IndexOutOfBoundsException` | If `cmdarray` is an empty array (has length `0`) |

**See Also**

- [java.lang.ProcessBuilder](ProcessBuilder.md) 

### exit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun exit(status: Int): Unit
```

Terminates the currently running Java virtual machine by initiating its shutdown sequence. This method never returns normally. The argument serves as a status code; by convention, a nonzero status code indicates abnormal termination.

All registered [shutdown hooks](Runtime.md)), if any, are started in some unspecified order and allowed to run concurrently until they finish. Once this is done the virtual machine [halts](Runtime.md)).

If this method is invoked after all shutdown hooks have already been run and the status is nonzero then this method halts the virtual machine with the given status code. Otherwise, this method blocks indefinitely.

The [System.exit](System.md)) method is the conventional and convenient means of invoking this method.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Termination status. By convention, a nonzero status code indicates abnormal termination. |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | If a security manager is present and its [checkExit](SecurityManager.md)) method does not permit exiting with the specified status |

**See Also**

- [java.lang.SecurityException](SecurityException.md)
- [java.lang.SecurityManager#checkExit(int)](SecurityManager.md))
- [#addShutdownHook](Runtime.md))
- [#removeShutdownHook](Runtime.md))
- [#halt(int)](Runtime.md)) 

### freeMemory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun freeMemory(): Long
```

Returns the amount of free memory in the Java Virtual Machine. Calling the `gc` method may result in increasing the value returned by `freeMemory.`

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | an approximation to the total amount of memory currently available for future allocated objects, measured in bytes. |

### gc

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun gc(): Unit
```

Runs the garbage collector. Calling this method suggests that the Java virtual machine expend effort toward recycling unused objects in order to make the memory they currently occupy available for quick reuse. When control returns from the method call, the virtual machine has made its best effort to recycle all discarded objects.

The name `gc` stands for "garbage collector". The virtual machine performs this recycling process automatically as needed, in a separate thread, even if the `gc` method is not invoked explicitly.

The method [System.gc()](System.md)) is the conventional and convenient means of invoking this method. 

### getRuntime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getRuntime(): Runtime!
```

Returns the runtime object associated with the current Java application. Most of the methods of class `Runtime` are instance methods and must be invoked with respect to the current runtime object.

| Return ||
|-------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Runtime](Runtime.md)! | the `Runtime` object associated with the current Java application. |

### halt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun halt(status: Int): Unit
```

Forcibly terminates the currently running Java virtual machine. This method never returns normally.

This method should be used with extreme caution. Unlike the [exit](Runtime.md)) method, this method does not cause shutdown hooks to be started. If the shutdown sequence has already been initiated then this method does not wait for any running shutdown hooks to finish their work.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Termination status. By convention, a nonzero status code indicates abnormal termination. If the [exit](Runtime.md)) (equivalently, [System.exit](System.md))) method has already been invoked then this status code will override the status code passed to that method. |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | If a security manager is present and its [checkExit](SecurityManager.md)) method does not permit an exit with the specified status |

**See Also**

- [#exit](Runtime.md))
- [#addShutdownHook](Runtime.md))
- [#removeShutdownHook](Runtime.md)) 

### load

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun load(filename: String!): Unit
```

Loads the native library specified by the filename argument. The filename argument must be an absolute path name. (for example `Runtime.getRuntime().load("/home/avh/lib/libX11.so");`). If the filename argument, when stripped of any platform-specific library prefix, path, and file extension, indicates a library whose name is, for example, L, and a native library called L is statically linked with the VM, then the JNI_OnLoad_L function exported by the library is invoked rather than attempting to load a dynamic library. A filename matching the argument does not have to exist in the file system. See the [JNI Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/jni/index.html) for more details. Otherwise, the filename argument is mapped to a native library image in an implementation-dependent manner.

First, if there is a security manager, its `checkLink` method is called with the `filename` as its argument. This may result in a security exception.

This is similar to the method [loadLibrary(java.lang.String)](Runtime.md)), but it accepts a general file name as an argument rather than just a library name, allowing any file of native code to be loaded.

The method [System.load(String)](System.md)) is the conventional and convenient means of invoking this method.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------|
| `filename` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the file to load. |

| Exceptions ||
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its `checkLink` method doesn't allow loading of the specified dynamic library |
| `java.lang.UnsatisfiedLinkError` | if either the filename is not an absolute path name, the native library is not statically linked with the VM, or the library cannot be mapped to a native library image by the host system. |
| `java.lang.NullPointerException` | if `filename` is `null` |
| --- | --- |

**See Also**

- [java.lang.Runtime#getRuntime()](Runtime.md))
- [java.lang.SecurityException](SecurityException.md)
- [java.lang.SecurityManager#checkLink(java.lang.String)](SecurityManager.md)) 

### loadLibrary

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun loadLibrary(libname: String!): Unit
```

Loads the native library specified by the `libname` argument. The `libname` argument must not contain any platform specific prefix, file extension or path. If a native library called `libname` is statically linked with the VM, then the JNI_OnLoad_`libname` function exported by the library is invoked. See the [JNI Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/jni/index.html) for more details. Otherwise, the libname argument is loaded from a system library location and mapped to a native library image in an implementation- dependent manner.

First, if there is a security manager, its `checkLink` method is called with the `libname` as its argument. This may result in a security exception.

The method [System.loadLibrary(String)](System.md)) is the conventional and convenient means of invoking this method. If native methods are to be used in the implementation of a class, a standard strategy is to put the native code in a library file (call it `LibFile`) and then to put a static initializer: 

```kotlin
static { System.loadLibrary("LibFile"); }
  
```
within the class declaration. When the class is loaded and initialized, the necessary native code implementation for the native methods will then be loaded as well.

If this method is called more than once with the same library name, the second and subsequent calls are ignored.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------|
| `libname` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the library. |

| Exceptions ||
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its `checkLink` method doesn't allow loading of the specified dynamic library |
| `java.lang.UnsatisfiedLinkError` | if either the libname argument contains a file path, the native library is not statically linked with the VM, or the library cannot be mapped to a native library image by the host system. |
| `java.lang.NullPointerException` | if `libname` is `null` |
| --- | --- |

**See Also**

- [java.lang.SecurityException](SecurityException.md)
- [java.lang.SecurityManager#checkLink(java.lang.String)](SecurityManager.md)) 

### maxMemory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun maxMemory(): Long
```

Returns the maximum amount of memory that the Java virtual machine will attempt to use. If there is no inherent limit then the value [java.lang.Long#MAX_VALUE](Long.md) will be returned.

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the maximum amount of memory that the virtual machine will attempt to use, measured in bytes |

### removeShutdownHook

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeShutdownHook(hook: Thread!): Boolean
```

De-registers a previously-registered virtual-machine shutdown hook.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------|
| `hook` | [Thread](Thread.md)!: the hook to remove |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if the specified hook had previously been registered and was successfully de-registered, `false` otherwise. |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If the virtual machine is already in the process of shutting down |
| `java.lang.SecurityException` | If a security manager is present and it denies [RuntimePermission](RuntimePermission.md)("shutdownHooks") |

**See Also**

- [#addShutdownHook](Runtime.md))
- [#exit(int)](Runtime.md)) 

### runFinalization

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun runFinalization(): Unit
```

Runs the finalization methods of any objects pending finalization. Calling this method suggests that the Java virtual machine expend effort toward running the `finalize` methods of objects that have been found to be discarded but whose `finalize` methods have not yet been run. When control returns from the method call, the virtual machine has made a best effort to complete all outstanding finalizations.

The virtual machine performs the finalization process automatically as needed, in a separate thread, if the `runFinalization` method is not invoked explicitly.

The method [System.runFinalization()](System.md)) is the conventional and convenient means of invoking this method. 
**See Also**

- [java.lang.Object#finalize()](Object.md)) 

### runFinalizersOnExit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun runFinalizersOnExit(value: Boolean): Unit
```

**Deprecated:** *This method is inherently unsafe. It may result in finalizers being called on live objects while other threads are concurrently manipulating those objects, resulting in erratic behavior or deadlock.*

Enable or disable finalization on exit; doing so specifies that the finalizers of all objects that have finalizers that have not yet been automatically invoked are to be run before the Java runtime exits. By default, finalization on exit is disabled.

If there is a security manager, its `checkExit` method is first called with 0 as its argument to ensure the exit is allowed. This could result in a SecurityException.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to enable finalization on exit, false to disable |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its `checkExit` method doesn't allow the exit. |

**See Also**

- [java.lang.Runtime#exit(int)](Runtime.md))
- [java.lang.Runtime#gc()](Runtime.md))
- [java.lang.SecurityManager#checkExit(int)](SecurityManager.md)) 

### totalMemory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun totalMemory(): Long
```

Returns the total amount of memory in the Java virtual machine. The value returned by this method may vary over time, depending on the host environment.

Note that the amount of memory required to hold an object of any given type may be implementation-dependent.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the total amount of memory currently available for current and future objects, measured in bytes. |

### traceInstructions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun traceInstructions(on: Boolean): Unit
```

**Deprecated:** *This method was intended to control instruction tracing. It has been superseded by ART-specific tracing mechanisms.*

Not implemented, does nothing.

| Parameters ||
|------|---------------------------------------------------------------------------------------------|
| `on` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): ignored |

### traceMethodCalls

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun traceMethodCalls(on: Boolean): Unit
```

**Deprecated:** *This method was intended to control method call tracing. It has been superseded by ART-specific tracing mechanisms.*

Not implemented, does nothing.

Calling this method on Android Lollipop or later (API level \>= 21) with `true` argument will cause it to throw an `UnsupportedOperationException`.

| Parameters ||
|------|---------------------------------------------------------------------------------------------|
| `on` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): ignored |
