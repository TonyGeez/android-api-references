Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CookieSyncManager

```
class CookieSyncManager : Runnable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.CookieSyncManager](https://developer.android.com/reference/kotlin/android/webkit/CookieSyncManager#) |

> [!CAUTION]
> **This class was deprecated in API level 21.**
>
> The WebView now automatically syncs cookies as necessary. You no longer need to create or use the CookieSyncManager. To manually force a sync you can use the CookieManager method `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#flush()` which is a synchronous replacement for `https://developer.android.com/reference/kotlin/android/webkit/CookieSyncManager#sync()`.

The CookieSyncManager is used to synchronize the browser cookie store between RAM and permanent storage. To get the best performance, browser cookies are saved in RAM. A separate thread saves the cookies between, driven by a timer.

To use the CookieSyncManager, the host application has to call the following when the application starts:

```kotlin
CookieSyncManager.createInstance(context)
```

To set up for sync, the host application has to call

```kotlin
CookieSyncManager.getInstance().startSync()
```

in Activity.onResume(), and call

```kotlin
CookieSyncManager.getInstance().stopSync()
  
```

in Activity.onPause().

To get instant sync instead of waiting for the timer to trigger, the host can call

```kotlin
CookieSyncManager.getInstance().sync()
```

The sync interval is 5 minutes, so you will want to force syncs manually anyway, for instance in `https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onPageFinished(android.webkit.WebView,%20kotlin.String)`. Note that even sync() happens asynchronously, so don't do it just as your activity is shutting down.

## Summary

| Public methods ||
|---|---|
| static [CookieSyncManager](https://developer.android.com/reference/kotlin/android/webkit/CookieSyncManager#)! | `https://developer.android.com/reference/kotlin/android/webkit/CookieSyncManager#createInstance(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` Create a singleton CookieSyncManager within a context |
| static [CookieSyncManager](https://developer.android.com/reference/kotlin/android/webkit/CookieSyncManager#)! | `https://developer.android.com/reference/kotlin/android/webkit/CookieSyncManager#getInstance()()` Singleton access to a `https://developer.android.com/reference/kotlin/android/webkit/CookieSyncManager#`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/webkit/CookieSyncManager#resetSync()()` resetSync() resets sync manager's timer. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/webkit/CookieSyncManager#run()()` When an object implementing interface `Runnable` is used to create a thread, starting the thread causes the object's `run` method to be called in that separately executing thread. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/webkit/CookieSyncManager#startSync()()` startSync() requests sync manager to start sync. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/webkit/CookieSyncManager#stopSync()()` stopSync() requests sync manager to stop sync. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/webkit/CookieSyncManager#sync()()` sync() forces sync manager to sync now |

| Protected methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/webkit/CookieSyncManager#syncFromRamToFlash()()` <br /> |

## Public methods

### createInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createInstance(context: Context!): CookieSyncManager!
```

**Deprecated:** *Deprecated in Java.*

Create a singleton CookieSyncManager within a context

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/webkit/CookieSyncManager#!` | CookieSyncManager |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(): CookieSyncManager!
```

**Deprecated:** *Deprecated in Java.*

Singleton access to a `https://developer.android.com/reference/kotlin/android/webkit/CookieSyncManager#`. An IllegalStateException will be thrown if `https://developer.android.com/reference/kotlin/android/webkit/CookieSyncManager#createInstance(android.content.Context)` is not called before.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/webkit/CookieSyncManager#!` | CookieSyncManager |

### resetSync

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun resetSync(): Unit
```

**Deprecated:** *Calling resetSync is no longer necessary as the WebView automatically syncs cookies.*

resetSync() resets sync manager's timer.

### run

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun run(): Unit
```

**Deprecated:** *Deprecated in Java.*

When an object implementing interface `Runnable` is used to create a thread, starting the thread causes the object's `run` method to be called in that separately executing thread.

The general contract of the method `run` is that it may take any action whatsoever.

### startSync

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun startSync(): Unit
```

**Deprecated:** *Calling startSync is no longer necessary as the WebView automatically syncs cookies.*

startSync() requests sync manager to start sync.

### stopSync

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun stopSync(): Unit
```

**Deprecated:** *Calling stopSync is no longer useful as the WebView automatically syncs cookies.*

stopSync() requests sync manager to stop sync. remove any SYNC_MESSAGE in the queue to break the sync loop

### sync

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sync(): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#flush()` instead.*

sync() forces sync manager to sync now

## Protected methods

### syncFromRamToFlash

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun syncFromRamToFlash(): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#flush()` instead.*
