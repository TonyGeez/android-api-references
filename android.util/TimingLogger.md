# TimingLogger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TimingLogger

Kotlin| [Java](https://developer.android.com/reference/android/util/TimingLogger "View this page in Java") 
| --- | --- |

```
open class TimingLogger
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.TimingLogger](https://developer.android.com/reference/kotlin/android/util/TimingLogger#) |

| **This class was deprecated in API level 30.**
|
| Use [android.os.Trace](https://developer.android.com/reference/kotlin/android/os/Trace.html#), or [Android Studio](https://developer.android.com/studio/profile/benchmark). In general, milliseconds is the wrong granularity for method-level tracing. Rounding errors can overemphasize cheap operations, or underemphasize repeated operations. This timing system also does not take CPU scheduling or frequency into account.

A utility class to help log timings splits throughout a method call. Typical usage is: 

```kotlin
TimingLogger timings = new TimingLogger(TAG, "methodA");
      // ... do some work A ...
      timings.addSplit("work A");
      // ... do some work B ...
      timings.addSplit("work B");
      // ... do some work C ...
      timings.addSplit("work C");
      timings.dumpToLog();
  
```

<br />

The dumpToLog call would add the following to the log: 

```kotlin
D/TAG     ( 3459): methodA: begin
      D/TAG     ( 3459): methodA:      9 ms, work A
      D/TAG     ( 3459): methodA:      1 ms, work B
      D/TAG     ( 3459): methodA:      6 ms, work C
      D/TAG     ( 3459): methodA: end, 16 ms
  
```

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TimingLogger](https://developer.android.com/reference/kotlin/android/util/TimingLogger#TimingLogger(kotlin.String,%20kotlin.String))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `label:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create and initialize a TimingLogger object that will log using the specific tag. |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addSplit](https://developer.android.com/reference/kotlin/android/util/TimingLogger#addSplit(kotlin.String))`(`splitLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Add a split for the current time, labeled with splitLabel. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dumpToLog](https://developer.android.com/reference/kotlin/android/util/TimingLogger#dumpToLog())`()` Dumps the timings to the log using Log. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/android/util/TimingLogger#reset())`()` Clear and initialize a TimingLogger object that will log using the tag and label that was specified previously, either via the constructor or a call to reset(tag, label). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/android/util/TimingLogger#reset(kotlin.String,%20kotlin.String))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `label:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Clear and initialize a TimingLogger object that will log using the specific tag. |

## Public constructors

### TimingLogger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TimingLogger(
    tag: String!, 
    label: String!)
```

Create and initialize a TimingLogger object that will log using the specific tag. If the Log.isLoggable is not enabled to at least the Log.VERBOSE level for that tag at creation time then the addSplit and dumpToLog call will do nothing.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the log tag to use while logging the timings |
| `label` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a string to be displayed with each log |

## Public methods

### addSplit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addSplit(splitLabel: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Add a split for the current time, labeled with splitLabel. If Log.isLoggable was not enabled to at least the Log.VERBOSE for the specified tag at construction or reset() time then this call does nothing.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------|
| `splitLabel` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a label to associate with this split. |

### dumpToLog

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dumpToLog(): Unit
```

**Deprecated:** *Deprecated in Java.*

Dumps the timings to the log using Log.d(). If Log.isLoggable was not enabled to at least the Log.VERBOSE for the specified tag at construction or reset() time then this call does nothing. 

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

**Deprecated:** *Deprecated in Java.*

Clear and initialize a TimingLogger object that will log using the tag and label that was specified previously, either via the constructor or a call to reset(tag, label). If the Log.isLoggable is not enabled to at least the Log.VERBOSE level for that tag at creation time then the addSplit and dumpToLog call will do nothing. 

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(
    tag: String!, 
    label: String!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Clear and initialize a TimingLogger object that will log using the specific tag. If the Log.isLoggable is not enabled to at least the Log.VERBOSE level for that tag at creation time then the addSplit and dumpToLog call will do nothing.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the log tag to use while logging the timings |
| `label` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a string to be displayed with each log |
