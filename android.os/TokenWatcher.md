# TokenWatcher

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TokenWatcher

Kotlin| [Java](../android/os/TokenWatcher.md) 
| --- | --- |

```
abstract class TokenWatcher
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.TokenWatcher](../android/os/TokenWatcher.md) |

A TokenWatcher watches a collection of [IBinder](../android/os/IBinder.md) s. IBinders are added to the collection by calling [acquire](../android/os/TokenWatcher.md)), and removed by calling [release](../android/os/TokenWatcher.md)). IBinders are also implicitly removed when they become weakly reachable. Each IBinder may be added at most once. The [acquired](../android/os/TokenWatcher.md))method is invoked by posting to the specified handler whenever the size of the watched collection becomes nonzero. The [released](../android/os/TokenWatcher.md))method is invoked on the specified handler whenever the size of the watched collection becomes zero.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TokenWatcher](../android/os/TokenWatcher.md))`(`h:` ` [Handler](../android/os/Handler.md)!`, `tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Construct the TokenWatcher |

| Public methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [acquire](../android/os/TokenWatcher.md))`(`token:` ` [IBinder](../android/os/IBinder.md)!`, `tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Record that this token has been acquired. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [acquired](../android/os/TokenWatcher.md))`()` Called when the number of active tokens goes from 0 to 1. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cleanup](../android/os/TokenWatcher.md))`(`token:` ` [IBinder](../android/os/IBinder.md)!`, `unlink:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](../android/os/TokenWatcher.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](../android/os/TokenWatcher.md))`(`pw:` ` [PrintWriter](../java/io/PrintWriter.md)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAcquired](../android/os/TokenWatcher.md))`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](../android/os/TokenWatcher.md))`(`token:` ` [IBinder](../android/os/IBinder.md)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [released](../android/os/TokenWatcher.md))`()` Called when the number of active tokens goes from 1 to 0. |

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
| `h` | [Handler](../android/os/Handler.md)!:A handler to call [acquired](../android/os/TokenWatcher.md))and [released](../android/os/TokenWatcher.md))on. If you don't care, just call it like this, although your thread will have to be a Looper thread.`new TokenWatcher(new Handler())` |
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

Record that this token has been acquired. When acquire is called, and the current count is 0, the acquired method is called on the given handler. Note that the same`token`can only be acquired once. If this`token`has already been acquired, no action is taken. The first subsequent call to [release](../android/os/TokenWatcher.md))will release this`token`immediately.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `token` | [IBinder](../android/os/IBinder.md)!:An IBinder object. |
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
