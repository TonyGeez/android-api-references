Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XmlPullParserException

```
open class XmlPullParserException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||
| | | ↳ | [org.xmlpull.v1.XmlPullParserException](XmlPullParserException.md) |
| --- | --- | --- | --- |

This exception is thrown to signal XML Pull Parser related faults.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserException#XmlPullParserException(kotlin.String)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` <br /> |
| `https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserException#XmlPullParserException(kotlin.String,%20org.xmlpull.v1.XmlPullParser,%20kotlin.Throwable)(msg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser!, chain: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!)` <br /> |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserException#getColumnNumber()()` <br /> |
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | `https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserException#getDetail()()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserException#getLineNumber()()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserException#printStackTrace()()` Prints this throwable and its backtrace to the standard error stream. |

| Properties ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserException#column:kotlin.Int` <br /> |
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | `https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserException#detail:kotlin.Throwable` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserException#row:kotlin.Int` <br /> |
| --- | --- |

## Public constructors

### XmlPullParserException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
XmlPullParserException(s: String!)
```

### XmlPullParserException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
XmlPullParserException(
    msg: String!, 
    parser: XmlPullParser!, 
    chain: Throwable!)
```

## Public methods

### getColumnNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getColumnNumber(): Int
```

### getDetail

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDetail(): Throwable!
```

### getLineNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLineNumber(): Int
```

### printStackTrace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

## Properties

### column

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var column: Int
```

### detail

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var detail: Throwable!
```

### row

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var row: Int
```
