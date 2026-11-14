# TokenWatcher

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TokenWatcher

Kotlin| [Java](https://developer.android.com/reference/android/os/TokenWatcher "View this page in Java") 
| --- | --- |

```
abstract class TokenWatcher
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.TokenWatcher](https://developer.android.com/reference/kotlin/android/os/TokenWatcher#) |

A TokenWatcher watches a collection of [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder) s. IBinders are added to the collection by calling [acquire](https://developer.android.com/reference/kotlin/android/os/TokenWatcher#acquire(android.os.IBinder,%20kotlin.String)), and removed by calling [release](https://developer.android.com/reference/kotlin/android/os/TokenWatcher#release(android.os.IBinder)). IBinders are also implicitly removed when they become weakly reachable. Each IBinder may be added at most once. The [acquired](https://developer.android.com/reference/kotlin/android/os/TokenWatcher#acquired())method is invoked by posting to the specified handler whenever the size of the watched collection becomes nonzero. The [released](https://developer.android.com/reference/kotlin/android/os/TokenWatcher#released())method is invoked on the specified handler whenever the size of the watched collection becomes zero.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TokenWatcher](https://developer.android.com/reference/kotlin/android/os/TokenWatcher#TokenWatcher(android.os.Handler,%20kotlin.String))`(`h:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)!`, `tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Construct the TokenWatcher |

| Public methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [acquire](https://developer.android.com/reference/kotlin/android/os/TokenWatcher#acquire(android.os.IBinder,%20kotlin.String))`(`token:` ` [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder)!`, `tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Record that this token has been acquired. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [acquired](https://developer.android.com/reference/kotlin/android/os/TokenWatcher#acquired())`()` Called when the number of active tokens goes from 0 to 1. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cleanup](https://developer.android.com/reference/kotlin/android/os/TokenWatcher#cleanup(android.os.IBinder,%20kotlin.Boolean))`(`token:` ` [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder)!`, `unlink:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](https://developer.android.com/reference/kotlin/android/os/TokenWatcher#dump())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](https://developer.android.com/reference/kotlin/android/os/TokenWatcher#dump(java.io.PrintWriter))`(`pw:` ` [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAcquired](https://developer.android.com/reference/kotlin/android/os/TokenWatcher#isAcquired())`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](https://developer.android.com/reference/kotlin/android/os/TokenWatcher#release(android.os.IBinder))`(`token:` ` [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [released](https://developer.android.com/reference/kotlin/android/os/TokenWatcher#released())`()` Called when the number of active tokens goes from 1 to 0. |

## Public constructors

### TokenWatcher

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TokenWatcher(
    h: Handler!, 
    tag: String!)
```

Construct the TokenWatcher

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `h` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)!:A handler to call [acquired](https://developer.android.com/reference/kotlin/android/os/TokenWatcher#acquired())and [released](https://developer.android.com/reference/kotlin/android/os/TokenWatcher#released())on. If you don't care, just call it like this, although your thread will have to be a Looper thread.`new TokenWatcher(new Handler())` |
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A debugging tag for this TokenWatcher |

## Public methods

### acquire

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun acquire(
    token: IBinder!, 
    tag: String!
): Unit
```

Record that this token has been acquired. When acquire is called, and the current count is 0, the acquired method is called on the given handler. Note that the same`token`can only be acquired once. If this`token`has already been acquired, no action is taken. The first subsequent call to [release](https://developer.android.com/reference/kotlin/android/os/TokenWatcher#release(android.os.IBinder))will release this`token`immediately.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `token` | [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder)!:An IBinder object. |
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A string used by the #dump method for debugging, to see who has references. |

### acquired

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun acquired(): Unit
```

Called when the number of active tokens goes from 0 to 1. 

### cleanup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun cleanup(
    token: IBinder!, 
    unlink: Boolean
): Unit
```  

### dump

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dump(): Unit
```  

### dump

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dump(pw: PrintWriter!): Unit
```  

### isAcquired

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAcquired(): Boolean
```  

### release

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun release(token: IBinder!): Unit
```  

### released

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun released(): Unit
```

Called when the number of active tokens goes from 1 to 0.
