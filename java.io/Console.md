# Console

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Console

```
class Console : Flushable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.io.Console](https://developer.android.com/reference/kotlin/java/io/Console#) |

Methods to access the character-based console device, if any, associated with the current Java virtual machine.

Whether a virtual machine has a console is dependent upon the underlying platform and also upon the manner in which the virtual machine is invoked. If the virtual machine is started from an interactive command line without redirecting the standard input and output streams then its console will exist and will typically be connected to the keyboard and display from which the virtual machine was launched. If the virtual machine is started automatically, for example by a background job scheduler, then it will typically not have a console.

If this virtual machine has a console then it is represented by a unique instance of this class which can be obtained by invoking the [java.lang.System#console()](https://developer.android.com/reference/kotlin/java/lang/System.html#console())method. If no console device is available then an invocation of that method will return`null`.

Read and write operations are synchronized to guarantee the atomic completion of critical operations; therefore invoking methods [readLine()](https://developer.android.com/reference/kotlin/java/io/Console#readLine()), [readPassword()](https://developer.android.com/reference/kotlin/java/io/Console#readPassword()), [format()](https://developer.android.com/reference/kotlin/java/io/Console#format(kotlin.String,%20kotlin.Any)), [printf()](https://developer.android.com/reference/kotlin/java/io/Console#printf(kotlin.String,%20kotlin.Any))as well as the read, format and write operations on the objects returned by [reader()](https://developer.android.com/reference/kotlin/java/io/Console#reader())and [writer()](https://developer.android.com/reference/kotlin/java/io/Console#writer())may block in multithreaded scenarios.

Invoking`close()`on the objects returned by the [reader()](https://developer.android.com/reference/kotlin/java/io/Console#reader())and the [writer()](https://developer.android.com/reference/kotlin/java/io/Console#writer())will not close the underlying stream of those objects.

The console-read methods return`null`when the end of the console input stream is reached, for example by typing control-D on Unix or control-Z on Windows. Subsequent read operations will succeed if additional characters are later entered on the console's input device.

Unless otherwise specified, passing a`null`argument to any method in this class will cause a [NullPointerException](https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#) to be thrown.

**Security note:** If an application needs to read a password or other secure data, it should use [readPassword()](https://developer.android.com/reference/kotlin/java/io/Console#readPassword())or [readPassword(java.lang.String,java.lang.Object...)](https://developer.android.com/reference/kotlin/java/io/Console#readPassword(kotlin.String,%20kotlin.Any))and manually zero the returned character array after processing to minimize the lifetime of sensitive data in memory. 

```kotlin
<code>Console cons;
  char[] passwd;
  if ((cons = System.console()) != null &amp;&amp;
      (passwd = cons.readPassword("[%s]", "Password:")) != null) {
      ...
      java.util.Arrays.fill(passwd, ' ');
  }
  </code>
```

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)! | [charset](https://developer.android.com/reference/kotlin/java/io/Console#charset())`()` Returns the [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) object used for the`Console`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](https://developer.android.com/reference/kotlin/java/io/Console#flush())`()` Flushes the console and forces any buffered output to be written immediately . |
| [Console](https://developer.android.com/reference/kotlin/java/io/Console#)! | [format](https://developer.android.com/reference/kotlin/java/io/Console#format(kotlin.String,%20kotlin.Any))`(`fmt:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Writes a formatted string to this console's output stream using the specified format string and arguments. |
| --- | --- |
| [Console](https://developer.android.com/reference/kotlin/java/io/Console#)! | [printf](https://developer.android.com/reference/kotlin/java/io/Console#printf(kotlin.String,%20kotlin.Any))`(`format:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` A convenience method to write a formatted string to this console's output stream using the specified format string and arguments. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [readLine](https://developer.android.com/reference/kotlin/java/io/Console#readLine())`()` Reads a single line of text from the console. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [readLine](https://developer.android.com/reference/kotlin/java/io/Console#readLine(kotlin.String,%20kotlin.Any))`(`fmt:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Provides a formatted prompt, then reads a single line of text from the console. |
| --- | --- |
| [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | [readPassword](https://developer.android.com/reference/kotlin/java/io/Console#readPassword())`()` Reads a password or passphrase from the console with echoing disabled |
| [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | [readPassword](https://developer.android.com/reference/kotlin/java/io/Console#readPassword(kotlin.String,%20kotlin.Any))`(`fmt:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Provides a formatted prompt, then reads a password or passphrase from the console with echoing disabled. |
| [Reader](https://developer.android.com/reference/kotlin/java/io/Reader)! | [reader](https://developer.android.com/reference/kotlin/java/io/Console#reader())`()` Retrieves the unique [Reader](https://developer.android.com/reference/kotlin/java/io/Reader) object associated with this console. |
| --- | --- |
| [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter)! | [writer](https://developer.android.com/reference/kotlin/java/io/Console#writer())`()` Retrieves the unique [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter) object associated with this console. |

## Public methods

### charset

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun charset(): Charset!
```

Returns the [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) object used for the`Console`.

The returned charset corresponds to the input and output source (e.g., keyboard and/or display) specified by the host environment or user. It may not necessarily be the same as the default charset returned from [Charset.defaultCharset()](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#defaultCharset()).

| Return ||
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)! | a [Charset](https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#) object used for the`Console` |

### flush

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun flush(): Unit
```

Flushes the console and forces any buffered output to be written immediately .

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### format

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(
    fmt: String!, 
    vararg args: Any!
): Console!
```

Writes a formatted string to this console's output stream using the specified format string and arguments.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fmt` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A format string as described in [Format string syntax](https://developer.android.com/reference/kotlin/java/util/Formatter.html#syntax) |
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:Arguments referenced by the format specifiers in the format string. If there are more arguments than format specifiers, the extra arguments are ignored. The number of arguments is variable and may be zero. The maximum number of arguments is limited by the maximum dimension of a Java array as defined by The Java Virtual Machine Specification. The behaviour on a`null`argument depends on the [conversion](https://developer.android.com/reference/kotlin/java/util/Formatter.html#syntax). |

| Return ||
|-----------------------------------------------------------------------------|--------------|
| [Console](https://developer.android.com/reference/kotlin/java/io/Console#)! | This console |

| Exceptions ||
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.util.IllegalFormatException` | If a format string contains an illegal syntax, a format specifier that is incompatible with the given arguments, insufficient arguments given the format string, or other illegal conditions. For specification of all possible formatting errors, see the [Details](https://developer.android.com/reference/kotlin/java/util/Formatter.html#detail) section of the formatter class specification. |

### printf

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun printf(
    format: String!, 
    vararg args: Any!
): Console!
```

A convenience method to write a formatted string to this console's output stream using the specified format string and arguments.

An invocation of this method of the form`con.printf(format, args)`behaves in exactly the same way as the invocation of 

```kotlin
con.format(format, args)
```
.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `format` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A format string as described in [Format string syntax](https://developer.android.com/reference/kotlin/java/util/Formatter.html#syntax). |
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:Arguments referenced by the format specifiers in the format string. If there are more arguments than format specifiers, the extra arguments are ignored. The number of arguments is variable and may be zero. The maximum number of arguments is limited by the maximum dimension of a Java array as defined by The Java Virtual Machine Specification. The behaviour on a`null`argument depends on the [conversion](https://developer.android.com/reference/kotlin/java/util/Formatter.html#syntax). |

| Return ||
|-----------------------------------------------------------------------------|--------------|
| [Console](https://developer.android.com/reference/kotlin/java/io/Console#)! | This console |

| Exceptions ||
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.util.IllegalFormatException` | If a format string contains an illegal syntax, a format specifier that is incompatible with the given arguments, insufficient arguments given the format string, or other illegal conditions. For specification of all possible formatting errors, see the [Details](https://developer.android.com/reference/kotlin/java/util/Formatter.html#detail) section of the formatter class specification. |

### readLine

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readLine(): String!
```

Reads a single line of text from the console.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | A string containing the line read from the console, not including any line-termination characters, or`null`if an end of stream has been reached. |

| Exceptions ||
|-------------------|-------------------------|
| `java.io.IOError` | If an I/O error occurs. |

### readLine

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readLine(
    fmt: String!, 
    vararg args: Any!
): String!
```

Provides a formatted prompt, then reads a single line of text from the console.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fmt` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A format string as described in [Format string syntax](https://developer.android.com/reference/kotlin/java/util/Formatter.html#syntax). |
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:Arguments referenced by the format specifiers in the format string. If there are more arguments than format specifiers, the extra arguments are ignored. The maximum number of arguments is limited by the maximum dimension of a Java array as defined by The Java Virtual Machine Specification. |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | A string containing the line read from the console, not including any line-termination characters, or`null`if an end of stream has been reached. |

| Exceptions ||
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.util.IllegalFormatException` | If a format string contains an illegal syntax, a format specifier that is incompatible with the given arguments, insufficient arguments given the format string, or other illegal conditions. For specification of all possible formatting errors, see the [Details](https://developer.android.com/reference/kotlin/java/util/Formatter.html#detail) section of the formatter class specification. |
| `java.io.IOError` | If an I/O error occurs. |

### readPassword

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readPassword(): CharArray!
```

Reads a password or passphrase from the console with echoing disabled

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | A character array containing the password or passphrase read from the console, not including any line-termination characters, or`null`if an end of stream has been reached. |

| Exceptions ||
|-------------------|-------------------------|
| `java.io.IOError` | If an I/O error occurs. |

### readPassword

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readPassword(
    fmt: String!, 
    vararg args: Any!
): CharArray!
```

Provides a formatted prompt, then reads a password or passphrase from the console with echoing disabled.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fmt` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A format string as described in [Format string syntax](https://developer.android.com/reference/kotlin/java/util/Formatter.html#syntax) for the prompt text. |
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:Arguments referenced by the format specifiers in the format string. If there are more arguments than format specifiers, the extra arguments are ignored. The maximum number of arguments is limited by the maximum dimension of a Java array as defined by The Java Virtual Machine Specification. |

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | A character array containing the password or passphrase read from the console, not including any line-termination characters, or`null`if an end of stream has been reached. |

| Exceptions ||
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.util.IllegalFormatException` | If a format string contains an illegal syntax, a format specifier that is incompatible with the given arguments, insufficient arguments given the format string, or other illegal conditions. For specification of all possible formatting errors, see the [Details](https://developer.android.com/reference/kotlin/java/util/Formatter.html#detail) section of the formatter class specification. |
| `java.io.IOError` | If an I/O error occurs. |

### reader

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun reader(): Reader!
```

Retrieves the unique [Reader](https://developer.android.com/reference/kotlin/java/io/Reader) object associated with this console.

This method is intended to be used by sophisticated applications, for example, a [java.util.Scanner](https://developer.android.com/reference/kotlin/java/util/Scanner.html#) object which utilizes the rich parsing/scanning functionality provided by the`Scanner`: 

```kotlin
Console con = System.console();
  if (con != null) {
      Scanner sc = new Scanner(con.reader());
      ...
  }
  
```

For simple applications requiring only line-oriented reading, use #readLine.

The bulk read operations[read(char[])](https://developer.android.com/reference/kotlin/java/io/Reader#read(kotlin.CharArray)),[read(char[], int, int)](https://developer.android.com/reference/kotlin/java/io/Reader#read(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))and [read(java.nio.CharBuffer)](https://developer.android.com/reference/kotlin/java/io/Reader#read(java.nio.CharBuffer))on the returned object will not read in characters beyond the line bound for each invocation, even if the destination buffer has space for more characters. The`Reader`'s`read`methods may block if a line bound has not been entered or reached on the console's input device. A line bound is considered to be any one of a line feed (`'\n'`), a carriage return (`'\r'`), a carriage return followed immediately by a linefeed, or an end of stream.

| Return ||
|--------------------------------------------------------------------------|-----------------------------------------|
| [Reader](https://developer.android.com/reference/kotlin/java/io/Reader)! | The reader associated with this console |

### writer

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writer(): PrintWriter!
```

Retrieves the unique [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter) object associated with this console.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter)! | The printwriter associated with this console |
