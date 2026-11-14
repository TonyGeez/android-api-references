# ProcessBuilder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProcessBuilder

```
class ProcessBuilder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#) |

This class is used to create operating system processes.

Each`ProcessBuilder`instance manages a collection of process attributes. The [start()](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#start())method creates a new [Process](https://developer.android.com/reference/kotlin/java/lang/Process) instance with those attributes. The [start()](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#start())method can be invoked repeatedly from the same instance to create new subprocesses with identical or related attributes.

Each process builder manages these process attributes:

- a*command*, a list of strings which signifies the external program file to be invoked and its arguments, if any. Which string lists represent a valid operating system command is system-dependent. For example, it is common for each conceptual argument to be an element in this list, but there are operating systems where programs are expected to tokenize command line strings themselves - on such a system a Java implementation might require commands to contain exactly two elements.
- an*environment* , which is a system-dependent mapping from*variables* to*values* . The initial value is a copy of the environment of the current process (see [System.getenv()](https://developer.android.com/reference/kotlin/java/lang/System#getenv())).
- a*working directory* . The default value is the current working directory of the current process, usually the directory named by the system property`user.dir`.
- a source of*standard input*. By default, the subprocess reads input from a pipe. Java code can access this pipe via the output stream returned by [Process.getOutputStream()](https://developer.android.com/reference/kotlin/java/lang/Process#getOutputStream()). However, standard input may be redirected to another source using [redirectInput](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirectInput(java.lang.ProcessBuilder.Redirect)). In this case, [Process.getOutputStream()](https://developer.android.com/reference/kotlin/java/lang/Process#getOutputStream())will return a*null output stream* , for which:
 - the [write](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#write(kotlin.Int))methods always throw`IOException`
 - the java.io.OutputStream#close() method does nothing
- a destination for*standard output* and*standard error*. By default, the subprocess writes standard output and standard error to pipes. Java code can access these pipes via the input streams returned by [Process.getInputStream()](https://developer.android.com/reference/kotlin/java/lang/Process#getInputStream())and [Process.getErrorStream()](https://developer.android.com/reference/kotlin/java/lang/Process#getErrorStream()). However, standard output and standard error may be redirected to other destinations using [redirectOutput](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirectOutput(java.lang.ProcessBuilder.Redirect))and [redirectError](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirectError(java.lang.ProcessBuilder.Redirect)). In this case, [Process.getInputStream()](https://developer.android.com/reference/kotlin/java/lang/Process#getInputStream())and/or [Process.getErrorStream()](https://developer.android.com/reference/kotlin/java/lang/Process#getErrorStream())will return a*null input stream* , for which:
 - the [read](https://developer.android.com/reference/kotlin/java/io/InputStream.html#read())methods always return`-1`
 - the [available](https://developer.android.com/reference/kotlin/java/io/InputStream.html#available())method always returns`0`
 - the java.io.InputStream#close() method does nothing
- a*redirectErrorStream* property. Initially, this property is`false`, meaning that the standard output and error output of a subprocess are sent to two separate streams, which can be accessed using the [Process.getInputStream()](https://developer.android.com/reference/kotlin/java/lang/Process#getInputStream())and [java.lang.Process#getErrorStream()](https://developer.android.com/reference/kotlin/java/lang/Process#getErrorStream())methods.

 If the value is set to`true`, then:
 - standard error is merged with the standard output and always sent to the same destination (this makes it easier to correlate error messages with the corresponding output)
 - the common destination of standard error and standard output can be redirected using [redirectOutput](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirectOutput(java.lang.ProcessBuilder.Redirect))
 - any redirection set by the [redirectError](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirectError(java.lang.ProcessBuilder.Redirect))method is ignored when creating a subprocess
 - the stream returned from [Process.getErrorStream()](https://developer.android.com/reference/kotlin/java/lang/Process#getErrorStream())will always be a [null input stream](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirect-output)

Modifying a process builder's attributes will affect processes subsequently started by that object's [start()](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#start())method, but will never affect previously started processes or the Java process itself.

Most error checking is performed by the [start()](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#start())method. It is possible to modify the state of an object so that [start()](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#start())will fail. For example, setting the command attribute to an empty list will not throw an exception unless [start()](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#start())is invoked.

**Note that this class is not synchronized.** If multiple threads access a`ProcessBuilder`instance concurrently, and at least one of the threads modifies one of the attributes structurally, it*must*be synchronized externally.

Starting a new process which uses the default working directory and environment is easy: 

```kotlin
<code>Process p = new ProcessBuilder("myCommand", "myArg").start();
  </code>
```

Here is an example that starts a process with a modified working directory and environment, and redirects standard output and error to be appended to a log file: 

```kotlin
<code>ProcessBuilder pb =
    new ProcessBuilder("myCommand", "myArg1", "myArg2");
  Map&lt;String, String&gt; env = pb.environment();
  env.put("VAR1", "myValue");
  env.remove("OTHERVAR");
  env.put("VAR2", env.get("VAR1") + "suffix");
  pb.directory(new File("myDir"));
  File log = new File("log");
  pb.redirectErrorStream(true);
  pb.redirectOutput(Redirect.appendTo(log));
  Process p = pb.start();
  assert pb.redirectInput() == Redirect.PIPE;
  assert pb.redirectOutput().file() == log;
  assert p.getInputStream().read() == -1;
  </code>
```

To start a process with an explicit set of environment variables, first call [Map.clear()](https://developer.android.com/reference/kotlin/java/util/Map.html#clear())before adding environment variables.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Redirect](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder.Redirect) Represents a source of subprocess input or a destination of subprocess output. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#ProcessBuilder(kotlin.String))`(`vararg` `command:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a process builder with the specified operating system program and arguments. |
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#ProcessBuilder(kotlin.collections.MutableList))`(`command:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Constructs a process builder with the specified operating system program and arguments. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [command](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#command())`()` Returns this process builder's operating system program and arguments. |
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#)! | [command](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#command(kotlin.String))`(`vararg` `command:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets this process builder's operating system program and arguments. |
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#)! | [command](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#command(kotlin.collections.MutableList))`(`command:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Sets this process builder's operating system program and arguments. |
| --- | --- |
| [File](https://developer.android.com/reference/kotlin/java/io/File.html#)! | [directory](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#directory())`()` Returns this process builder's working directory. |
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#)! | [directory](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#directory(java.io.File))`(`directory:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`)` Sets this process builder's working directory. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [environment](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#environment())`()` Returns a string map view of this process builder's environment. |
| --- | --- |
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#)! | [inheritIO](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#inheritIO())`()` Sets the source and destination for subprocess standard I/O to be the same as those of the current Java process. |
| [ProcessBuilder.Redirect](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder.Redirect)! | [redirectError](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirectError())`()` Returns this process builder's standard error destination. |
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#)! | [redirectError](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirectError(java.io.File))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`)` Sets this process builder's standard error destination to a file. |
| --- | --- |
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#)! | [redirectError](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirectError(java.lang.ProcessBuilder.Redirect))`(`destination:` ` [ProcessBuilder.Redirect](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder.Redirect)!`)` Sets this process builder's standard error destination. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [redirectErrorStream](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirectErrorStream())`()` Tells whether this process builder merges standard error and standard output. |
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#)! | [redirectErrorStream](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirectErrorStream(kotlin.Boolean))`(`redirectErrorStream:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets this process builder's`redirectErrorStream`property. |
| --- | --- |
| [ProcessBuilder.Redirect](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder.Redirect)! | [redirectInput](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirectInput())`()` Returns this process builder's standard input source. |
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#)! | [redirectInput](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirectInput(java.io.File))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`)` Sets this process builder's standard input source to a file. |
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#)! | [redirectInput](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirectInput(java.lang.ProcessBuilder.Redirect))`(`source:` ` [ProcessBuilder.Redirect](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder.Redirect)!`)` Sets this process builder's standard input source. |
| --- | --- |
| [ProcessBuilder.Redirect](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder.Redirect)! | [redirectOutput](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirectOutput())`()` Returns this process builder's standard output destination. |
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#)! | [redirectOutput](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirectOutput(java.io.File))`(`file:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`)` Sets this process builder's standard output destination to a file. |
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#)! | [redirectOutput](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirectOutput(java.lang.ProcessBuilder.Redirect))`(`destination:` ` [ProcessBuilder.Redirect](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder.Redirect)!`)` Sets this process builder's standard output destination. |
| --- | --- |
| [Process](https://developer.android.com/reference/kotlin/java/lang/Process)! | [start](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#start())`()` Starts a new process using the attributes of this process builder. |

## Public constructors

### ProcessBuilder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ProcessBuilder(vararg command: String!)
```

Constructs a process builder with the specified operating system program and arguments. This is a convenience constructor that sets the process builder's command to a string list containing the same strings as the`command`array, in the same order. It is not checked whether`command`corresponds to a valid operating system command.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `command` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a string array containing the program and its arguments |

### ProcessBuilder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ProcessBuilder(command: MutableList<String!>!)
```

Constructs a process builder with the specified operating system program and arguments. This constructor does*not* make a copy of the`command`list. Subsequent updates to the list will be reflected in the state of the process builder. It is not checked whether`command`corresponds to a valid operating system command.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `command` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the list containing the program and its arguments |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.lang.NullPointerException` | if the argument is null |

## Public methods

### command

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun command(): MutableList<String!>!
```

Returns this process builder's operating system program and arguments. The returned list is*not*a copy. Subsequent updates to the list will be reflected in the state of this process builder.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | this process builder's program and its arguments |

### command

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun command(vararg command: String!): ProcessBuilder!
```

Sets this process builder's operating system program and arguments. This is a convenience method that sets the command to a string list containing the same strings as the`command`array, in the same order. It is not checked whether`command`corresponds to a valid operating system command.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `command` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a string array containing the program and its arguments |

| Return ||
|---------------------------------------------------------------------------------------------|----------------------|
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#)! | this process builder |

### command

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun command(command: MutableList<String!>!): ProcessBuilder!
```

Sets this process builder's operating system program and arguments. This method does*not* make a copy of the`command`list. Subsequent updates to the list will be reflected in the state of the process builder. It is not checked whether`command`corresponds to a valid operating system command.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `command` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the list containing the program and its arguments |

| Return ||
|---------------------------------------------------------------------------------------------|----------------------|
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#)! | this process builder |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.lang.NullPointerException` | if the argument is null |

### directory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun directory(): File!
```

Returns this process builder's working directory. Subprocesses subsequently started by this object's [start()](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#start())method will use this as their working directory. The returned value may be`null`-- this means to use the working directory of the current Java process, usually the directory named by the system property`user.dir`, as the working directory of the child process.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [File](https://developer.android.com/reference/kotlin/java/io/File.html#)! | this process builder's working directory |

### directory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun directory(directory: File!): ProcessBuilder!
```

Sets this process builder's working directory. Subprocesses subsequently started by this object's [start()](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#start())method will use this as their working directory. The argument may be`null`-- this means to use the working directory of the current Java process, usually the directory named by the system property`user.dir`, as the working directory of the child process.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------|
| `directory` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!:the new working directory |

| Return ||
|---------------------------------------------------------------------------------------------|----------------------|
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#)! | this process builder |

### environment

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun environment(): MutableMap<String!, String!>!
```

Returns a string map view of this process builder's environment. Whenever a process builder is created, the environment is initialized to a copy of the current process environment (see [System.getenv()](https://developer.android.com/reference/kotlin/java/lang/System#getenv())). Subprocesses subsequently started by this object's [start()](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#start())method will use this map as their environment.

The returned object may be modified using ordinary operations. These modifications will be visible to subprocesses started via the [start()](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#start())method. Two`ProcessBuilder`instances always contain independent process environments, so changes to the returned map will never be reflected in any other`ProcessBuilder`instance or the values returned by java.lang.System#getenv.

If the system does not support environment variables, an empty map is returned.

The returned map does not permit null keys or values. Attempting to insert or query the presence of a null key or value will throw a [NullPointerException](https://developer.android.com/reference/kotlin/java/lang/NullPointerException). Attempting to query the presence of a key or value which is not of type [String](https://developer.android.com/reference/kotlin/java/lang/String) will throw a [ClassCastException](https://developer.android.com/reference/kotlin/java/lang/ClassCastException).

The behavior of the returned map is system-dependent. A system may not allow modifications to environment variables or may forbid certain variable names or values. For this reason, attempts to modify the map may fail with [UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException) or [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException) if the modification is not permitted by the operating system.

Since the external format of environment variable names and values is system-dependent, there may not be a one-to-one mapping between them and Java's Unicode strings. Nevertheless, the map is implemented in such a way that environment variables which are not modified by Java code will have an unmodified native representation in the subprocess.

The returned map and its collection views may not obey the general contract of the [Object.equals](https://developer.android.com/reference/kotlin/java/lang/Object#equals(kotlin.Any))and [Object.hashCode](https://developer.android.com/reference/kotlin/java/lang/Object#hashCode())methods.

The returned map is typically case-sensitive on all platforms.

If a security manager exists, its java.lang.SecurityManager#checkPermission method is called with a [RuntimePermission](https://developer.android.com/reference/kotlin/java/lang/RuntimePermission)`("getenv.*")`permission. This may result in a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException) being thrown.

When passing information to a Java subprocess, [system properties](https://developer.android.com/reference/kotlin/java/lang/System#EnvironmentVSSystemProperties) are generally preferred over environment variables.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | this process builder's environment |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its java.lang.SecurityManager#checkPermission method doesn't allow access to the process environment |

**See Also**

- [java.lang.Runtime#exec(String[],String[],java.io.File)](https://developer.android.com/reference/kotlin/java/lang/Runtime#exec(kotlin.Array,%20kotlin.Array,%20java.io.File))
- [java.lang.System#getenv()](https://developer.android.com/reference/kotlin/java/lang/System#getenv()) 

### inheritIO

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun inheritIO(): ProcessBuilder!
```

Sets the source and destination for subprocess standard I/O to be the same as those of the current Java process.

This is a convenience method. An invocation of the form 

```kotlin
<code>pb.inheritIO()
  </code>
```
behaves in exactly the same way as the invocation 

```kotlin
<code>pb.redirectInput(Redirect.INHERIT)
    .redirectOutput(Redirect.INHERIT)
    .redirectError(Redirect.INHERIT)
  </code>
```
This gives behavior equivalent to most operating system command interpreters, or the standard C library function`system()`.

| Return ||
|---------------------------------------------------------------------------------------------|----------------------|
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#)! | this process builder |

### redirectError

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun redirectError(): ProcessBuilder.Redirect!
```

Returns this process builder's standard error destination. Subprocesses subsequently started by this object's [start()](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#start())method redirect their standard error to this destination. The initial value is [Redirect.PIPE](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder.Redirect#PIPE:java.lang.ProcessBuilder.Redirect).

| Return ||
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [ProcessBuilder.Redirect](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder.Redirect)! | this process builder's standard error destination |

### redirectError

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun redirectError(file: File!): ProcessBuilder!
```

Sets this process builder's standard error destination to a file.

This is a convenience method. An invocation of the form`redirectError(file)`behaves in exactly the same way as the invocation [redirectError](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirectError(java.lang.ProcessBuilder.Redirect))`(Redirect.to(file))`.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!:the new standard error destination |

| Return ||
|---------------------------------------------------------------------------------------------|----------------------|
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#)! | this process builder |

### redirectError

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun redirectError(destination: ProcessBuilder.Redirect!): ProcessBuilder!
```

Sets this process builder's standard error destination. Subprocesses subsequently started by this object's [start()](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#start())method send their standard error to this destination.

If the destination is [Redirect.PIPE](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder.Redirect#PIPE:java.lang.ProcessBuilder.Redirect)(the initial value), then the error output of a subprocess can be read using the input stream returned by [java.lang.Process#getErrorStream()](https://developer.android.com/reference/kotlin/java/lang/Process#getErrorStream()). If the destination is set to any other value, then [Process.getErrorStream()](https://developer.android.com/reference/kotlin/java/lang/Process#getErrorStream())will return a [null input stream](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirect-output).

If the #redirectErrorStream attribute has been set`true`, then the redirection set by this method has no effect.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `destination` | [ProcessBuilder.Redirect](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder.Redirect)!:the new standard error destination |

| Return ||
|---------------------------------------------------------------------------------------------|----------------------|
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#)! | this process builder |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the redirect does not correspond to a valid destination of data, that is, has type [READ](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder.Redirect.Type) |

### redirectErrorStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun redirectErrorStream(): Boolean
```

Tells whether this process builder merges standard error and standard output.

If this property is`true`, then any error output generated by subprocesses subsequently started by this object's [start()](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#start())method will be merged with the standard output, so that both can be read using the [Process.getInputStream()](https://developer.android.com/reference/kotlin/java/lang/Process#getInputStream())method. This makes it easier to correlate error messages with the corresponding output. The initial value is`false`.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | this process builder's`redirectErrorStream`property |

### redirectErrorStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun redirectErrorStream(redirectErrorStream: Boolean): ProcessBuilder!
```

Sets this process builder's`redirectErrorStream`property.

If this property is`true`, then any error output generated by subprocesses subsequently started by this object's [start()](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#start())method will be merged with the standard output, so that both can be read using the [Process.getInputStream()](https://developer.android.com/reference/kotlin/java/lang/Process#getInputStream())method. This makes it easier to correlate error messages with the corresponding output. The initial value is`false`.

| Parameters ||
|-----------------------|-----------------------------------------------------------------------------------------------------------|
| `redirectErrorStream` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new property value |

| Return ||
|---------------------------------------------------------------------------------------------|----------------------|
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#)! | this process builder |

### redirectInput

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun redirectInput(): ProcessBuilder.Redirect!
```

Returns this process builder's standard input source. Subprocesses subsequently started by this object's [start()](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#start())method obtain their standard input from this source. The initial value is [Redirect.PIPE](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder.Redirect#PIPE:java.lang.ProcessBuilder.Redirect).

| Return ||
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| [ProcessBuilder.Redirect](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder.Redirect)! | this process builder's standard input source |

### redirectInput

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun redirectInput(file: File!): ProcessBuilder!
```

Sets this process builder's standard input source to a file.

This is a convenience method. An invocation of the form`redirectInput(file)`behaves in exactly the same way as the invocation [redirectInput](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirectInput(java.lang.ProcessBuilder.Redirect))`(Redirect.from(file))`.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!:the new standard input source |

| Return ||
|---------------------------------------------------------------------------------------------|----------------------|
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#)! | this process builder |

### redirectInput

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun redirectInput(source: ProcessBuilder.Redirect!): ProcessBuilder!
```

Sets this process builder's standard input source. Subprocesses subsequently started by this object's [start()](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#start())method obtain their standard input from this source.

If the source is [Redirect.PIPE](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder.Redirect#PIPE:java.lang.ProcessBuilder.Redirect)(the initial value), then the standard input of a subprocess can be written to using the output stream returned by [Process.getOutputStream()](https://developer.android.com/reference/kotlin/java/lang/Process#getOutputStream()). If the source is set to any other value, then [Process.getOutputStream()](https://developer.android.com/reference/kotlin/java/lang/Process#getOutputStream())will return a [null output stream](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirect-input).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [ProcessBuilder.Redirect](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder.Redirect)!:the new standard input source |

| Return ||
|---------------------------------------------------------------------------------------------|----------------------|
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#)! | this process builder |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the redirect does not correspond to a valid source of data, that is, has type [WRITE](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder.Redirect.Type) or [APPEND](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder.Redirect.Type) |

### redirectOutput

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun redirectOutput(): ProcessBuilder.Redirect!
```

Returns this process builder's standard output destination. Subprocesses subsequently started by this object's [start()](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#start())method redirect their standard output to this destination. The initial value is [Redirect.PIPE](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder.Redirect#PIPE:java.lang.ProcessBuilder.Redirect).

| Return ||
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [ProcessBuilder.Redirect](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder.Redirect)! | this process builder's standard output destination |

### redirectOutput

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun redirectOutput(file: File!): ProcessBuilder!
```

Sets this process builder's standard output destination to a file.

This is a convenience method. An invocation of the form`redirectOutput(file)`behaves in exactly the same way as the invocation [redirectOutput](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirectOutput(java.lang.ProcessBuilder.Redirect))`(Redirect.to(file))`.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------|
| `file` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!:the new standard output destination |

| Return ||
|---------------------------------------------------------------------------------------------|----------------------|
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#)! | this process builder |

### redirectOutput

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun redirectOutput(destination: ProcessBuilder.Redirect!): ProcessBuilder!
```

Sets this process builder's standard output destination. Subprocesses subsequently started by this object's [start()](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#start())method send their standard output to this destination.

If the destination is [Redirect.PIPE](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder.Redirect#PIPE:java.lang.ProcessBuilder.Redirect)(the initial value), then the standard output of a subprocess can be read using the input stream returned by [java.lang.Process#getInputStream()](https://developer.android.com/reference/kotlin/java/lang/Process#getInputStream()). If the destination is set to any other value, then [Process.getInputStream()](https://developer.android.com/reference/kotlin/java/lang/Process#getInputStream())will return a [null input stream](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#redirect-output).

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `destination` | [ProcessBuilder.Redirect](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder.Redirect)!:the new standard output destination |

| Return ||
|---------------------------------------------------------------------------------------------|----------------------|
| [ProcessBuilder](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#)! | this process builder |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the redirect does not correspond to a valid destination of data, that is, has type [READ](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder.Redirect.Type) |

### start

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun start(): Process!
```

Starts a new process using the attributes of this process builder.

The new process will invoke the command and arguments given by [command()](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#command()), in a working directory as given by [directory()](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#directory()), with a process environment as given by [environment()](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#environment()).

This method checks that the command is a valid operating system command. Which commands are valid is system-dependent, but at the very least the command must be a non-empty list of non-null strings.

A minimal set of system dependent environment variables may be required to start a process on some operating systems. As a result, the subprocess may inherit additional environment variable settings beyond those in the process builder's [environment()](https://developer.android.com/reference/kotlin/java/lang/ProcessBuilder#environment()).

If there is a security manager, its [checkExec](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkExec(kotlin.String))method is called with the first component of this object's`command`array as its argument. This may result in a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException) being thrown.

Starting an operating system process is highly system-dependent. Among the many things that can go wrong are:

- The operating system program file was not found.
- Access to the program file was denied.
- The working directory does not exist.

In such cases an exception will be thrown. The exact nature of the exception is system-dependent, but it will always be a subclass of [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#).

Subsequent modifications to this process builder will not affect the returned [Process](https://developer.android.com/reference/kotlin/java/lang/Process).

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Process](https://developer.android.com/reference/kotlin/java/lang/Process)! | a new [Process](https://developer.android.com/reference/kotlin/java/lang/Process) object for managing the subprocess |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if an element of the command list is null |
| `java.lang.IndexOutOfBoundsException` | if the command is an empty list (has size`0`) |
| `java.lang.SecurityException` | if a security manager exists and - its [checkExec](https://developer.android.com/reference/kotlin/java/lang/SecurityManager#checkExec(kotlin.String))method doesn't allow creation of the subprocess, or - the standard input to the subprocess was #redirectInput and the security manager's java.lang.SecurityManager#checkRead method denies read access to the file, or - the standard output or standard error of the subprocess was #redirectOutput and the security manager's java.lang.SecurityManager#checkWrite method denies write access to the file |
| --- | --- |
| `java.io.IOException` | if an I/O error occurs |

**See Also**

- [java.lang.Runtime#exec(String[], String[], java.io.File)](https://developer.android.com/reference/kotlin/java/lang/Runtime#exec(kotlin.Array,%20kotlin.Array,%20java.io.File))
