# StructPollfd

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StructPollfd

Kotlin| [Java](https://developer.android.com/reference/android/system/StructPollfd "View this page in Java") 
| --- | --- |

```
class StructPollfd
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.system.StructPollfd](https://developer.android.com/reference/kotlin/android/system/StructPollfd#) |

Used as an in/out parameter to [Os.poll](https://developer.android.com/reference/kotlin/android/system/Os#poll(kotlin.Array,%20kotlin.Int)). Corresponds to C's`struct pollfd`from`<poll.h>`.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------|---|
| [StructPollfd](https://developer.android.com/reference/kotlin/android/system/StructPollfd#StructPollfd())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/system/StructPollfd#toString())`()` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [events](https://developer.android.com/reference/kotlin/android/system/StructPollfd#events:kotlin.Short) The events we're interested in. |
| [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)! | [fd](https://developer.android.com/reference/kotlin/android/system/StructPollfd#fd:java.io.FileDescriptor) The file descriptor to poll. |
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [revents](https://developer.android.com/reference/kotlin/android/system/StructPollfd#revents:kotlin.Short) The events that actually happened. |
| --- | --- |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [userData](https://developer.android.com/reference/kotlin/android/system/StructPollfd#userData:kotlin.Any) A non-standard extension that lets callers conveniently map back to the object their fd belongs to. |

## Public constructors

### StructPollfd

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StructPollfd()
```

## Public methods

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

## Properties

### events

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var events: Short
```

The events we're interested in. POLLIN corresponds to being in select(2)'s read fd set, POLLOUT to the write fd set. 

### fd

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var fd: FileDescriptor!
```

The file descriptor to poll. 

### revents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var revents: Short
```

The events that actually happened. 

### userData

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var userData: Any!
```

A non-standard extension that lets callers conveniently map back to the object their fd belongs to. This is used by Selector, for example, to associate each FileDescriptor with the corresponding SelectionKey.
