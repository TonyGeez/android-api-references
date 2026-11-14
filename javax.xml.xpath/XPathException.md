Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XPathException

```
open class XPathException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||
| | | ↳ | [javax.xml.xpath.XPathException](../javax/xml/xpath/XPathException.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [XPathExpressionException](../javax/xml/xpath/XPathExpressionException.md), [XPathFactoryConfigurationException](../javax/xml/xpath/XPathFactoryConfigurationException.md) |---|---| | [XPathExpressionException](../javax/xml/xpath/XPathExpressionException.md) | `XPathExpressionException` represents an error in an XPath expression. | | [XPathFactoryConfigurationException](../javax/xml/xpath/XPathFactoryConfigurationException.md) | `XPathFactoryConfigurationException` represents a configuration error in a `XPathFactory` environment. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [XPathFunctionException](../javax/xml/xpath/XPathFunctionException.md) |---|---| | [XPathFunctionException](../javax/xml/xpath/XPathFunctionException.md) | `XPathFunctionException` represents an error with an XPath function. | |
| --- | --- | --- | --- | --- | --- | --- |

`XPathException` represents a generic XPath exception.

<br />

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathException#XPathException(kotlin.String)(message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Constructs a new `XPathException` with the specified detail `message`. |
| `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathException#XPathException(kotlin.Throwable)(cause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!)` Constructs a new `XPathException` with the specified `cause`. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathException#printStackTrace()()` Prints this throwable and its backtrace to the standard error stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathException#printStackTrace(java.io.PrintStream)(s: https://developer.android.com/reference/kotlin/java/io/PrintStream.html#)` Prints this throwable and its backtrace to the specified print stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathException#printStackTrace(java.io.PrintWriter)(s: https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)` Prints this throwable and its backtrace to the specified print writer. |
| --- | --- |

| Properties ||
|---|---|
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)? | `https://developer.android.com/reference/kotlin/javax/xml/xpath/XPathException#cause:kotlin.Throwable` Returns the cause of this throwable or `null` if the cause is nonexistent or unknown. |

## Public constructors

### XPathException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
XPathException(message: String!)
```

Constructs a new `XPathException` with the specified detail `message`.

The `cause` is not initialized.

If `message` is `null`, then a `NullPointerException` is thrown.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The detail message. |

### XPathException

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
XPathException(cause: Throwable!)
```

Constructs a new `XPathException` with the specified `cause`.

If `cause` is `null`, then a `NullPointerException` is thrown.

| Parameters ||
|---|---|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: The cause. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `cause` is `null`. |

## Public methods

### printStackTrace

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun printStackTrace(): Unit
```

Prints this throwable and its backtrace to the standard error stream. This method prints a stack trace for this `Throwable` object on the error output stream that is the value of the field `System.err`. The first line of output contains the result of the `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#toString()` method for this object. Remaining lines represent data previously recorded by the method `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#fillInStackTrace()`. The format of this information depends on the implementation, but the following example may be regarded as typical:

```kotlin
java.lang.NullPointerException
          at MyClass.mash(MyClass.java:9)
          at MyClass.crunch(MyClass.java:6)
          at MyClass.main(MyClass.java:3)
  
```
This example was produced by running the program:

```kotlin
class MyClass {
      public static void main(String[] args) {
          crunch(null);
      }
      static void crunch(int[] a) {
          mash(a);
      }
      static void mash(int[] b) {
          System.out.println(b[0]);
      }
  }
  
```
The backtrace for a throwable with an initialized, non-null cause should generally include the backtrace for the cause. The format of this information depends on the implementation, but the following example may be regarded as typical:

```kotlin
HighLevelException: MidLevelException: LowLevelException
          at Junk.a(Junk.java:13)
          at Junk.main(Junk.java:4)
  Caused by: MidLevelException: LowLevelException
          at Junk.c(Junk.java:23)
          at Junk.b(Junk.java:17)
          at Junk.a(Junk.java:11)
          ... 1 more
  Caused by: LowLevelException
          at Junk.e(Junk.java:30)
          at Junk.d(Junk.java:27)
          at Junk.c(Junk.java:21)
          ... 3 more
  
```
Note the presence of lines containing the characters `"..."`. These lines indicate that the remainder of the stack trace for this exception matches the indicated number of frames from the bottom of the stack trace of the exception that was caused by this exception (the "enclosing" exception). This shorthand can greatly reduce the length of the output in the common case where a wrapped exception is thrown from same method as the "causative exception" is caught. The above example was produced by running the program:

```kotlin
public class Junk {
      public static void main(String args[]) {
          try {
              a();
          } catch(HighLevelException e) {
              e.printStackTrace();
          }
      }
      static void a() throws HighLevelException {
          try {
              b();
          } catch(MidLevelException e) {
              throw new HighLevelException(e);
          }
      }
      static void b() throws MidLevelException {
          c();
      }
      static void c() throws MidLevelException {
          try {
              d();
          } catch(LowLevelException e) {
              throw new MidLevelException(e);
          }
      }
      static void d() throws LowLevelException {
         e();
      }
      static void e() throws LowLevelException {
          throw new LowLevelException();
      }
  }
 
  class HighLevelException extends Exception {
      HighLevelException(Throwable cause) { super(cause); }
  }
 
  class MidLevelException extends Exception {
      MidLevelException(Throwable cause)  { super(cause); }
  }
 
  class LowLevelException extends Exception {
  }
  
```
As of release 7, the platform supports the notion of *suppressed exceptions* (in conjunction with the `try`-with-resources statement). Any exceptions that were suppressed in order to deliver an exception are printed out beneath the stack trace. The format of this information depends on the implementation, but the following example may be regarded as typical:

```kotlin
Exception in thread "main" java.lang.Exception: Something happened
   at Foo.bar(Foo.java:10)
   at Foo.main(Foo.java:5)
   Suppressed: Resource$CloseFailException: Resource ID = 0
           at Resource.close(Resource.java:26)
           at Foo.bar(Foo.java:9)
           ... 1 more
  
```
Note that the "... n more" notation is used on suppressed exceptions just as it is used on causes. Unlike causes, suppressed exceptions are indented beyond their "containing exceptions."

<br />

An exception can have both a cause and one or more suppressed exceptions:

```kotlin
Exception in thread "main" java.lang.Exception: Main block
   at Foo3.main(Foo3.java:7)
   Suppressed: Resource$CloseFailException: Resource ID = 2
           at Resource.close(Resource.java:26)
           at Foo3.main(Foo3.java:5)
   Suppressed: Resource$CloseFailException: Resource ID = 1
           at Resource.close(Resource.java:26)
           at Foo3.main(Foo3.java:5)
  Caused by: java.lang.Exception: I did it
   at Foo3.main(Foo3.java:8)
  
```
Likewise, a suppressed exception can have a cause:

```kotlin
Exception in thread "main" java.lang.Exception: Main block
   at Foo4.main(Foo4.java:6)
   Suppressed: Resource2$CloseFailException: Resource ID = 1
           at Resource2.close(Resource2.java:20)
           at Foo4.main(Foo4.java:5)
   Caused by: java.lang.Exception: Rats, you caught me
           at Resource2$CloseFailException.<init>(Resource2.java:45)
           ... 2 more
  
```

### printStackTrace

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun printStackTrace(s: PrintStream): Unit
```

Prints this throwable and its backtrace to the specified print stream.

| Parameters ||
|---|---|
| `s` | [PrintStream](../java/io/PrintStream.md): `PrintStream` to use for output |

### printStackTrace

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun printStackTrace(s: PrintWriter): Unit
```

Prints this throwable and its backtrace to the specified print writer.

| Parameters ||
|---|---|
| `s` | [PrintWriter](../java/io/PrintWriter.md): `PrintWriter` to use for output |

## Properties

### cause

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val cause: Throwable?
```

Returns the cause of this throwable or `null` if the cause is nonexistent or unknown. (The cause is the throwable that caused this throwable to get thrown.)

This implementation returns the cause that was supplied via one of the constructors requiring a `Throwable`, or that was set after creation with the `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable)` method. While it is typically unnecessary to override this method, a subclass can override it to return a cause set by some other means. This is appropriate for a "legacy chained throwable" that predates the addition of chained exceptions to `Throwable`. Note that it is *not* necessary to override any of the `PrintStackTrace` methods, all of which invoke the `getCause` method to determine the cause of a throwable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html?` | the cause of this throwable or `null` if the cause is nonexistent or unknown. |
