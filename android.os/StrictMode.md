Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StrictMode

Kotlin | [Java](../android/os/StrictMode.md)
| --- | --- |

```
class StrictMode
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.StrictMode](../android/os/StrictMode.md) |

StrictMode is a developer tool which detects things you might be doing by accident and brings them to your attention so you can fix them.

StrictMode is most commonly used to catch accidental disk or network access on the application's main thread, where UI operations are received and animations take place. Keeping disk and network operations off the main thread makes for much smoother, more responsive applications. By keeping your application's main thread responsive, you also prevent [ANR dialogs](https://developer.android.com/guide/practices/design/responsiveness.html) from being shown to users.

Note that even though an Android device's disk is often on flash memory, many devices run a filesystem on top of that memory with very limited concurrency. It's often the case that almost all disk accesses are fast, but may in individual cases be dramatically slower when certain I/O is happening in the background from other processes. If possible, it's best to assume that such things are not fast.

Example code to enable from early in your `https://developer.android.com/reference/kotlin/android/app/Application.html#`, `https://developer.android.com/reference/kotlin/android/app/Activity.html#`, or other application component's `https://developer.android.com/reference/kotlin/android/app/Application.html#onCreate()` method:

```kotlin
override fun onCreate(savedInstanceState: Bundle?) {
      super.onCreate(savedInstanceState)
      StrictMode.setThreadPolicy(
          StrictMode.ThreadPolicy.Builder()
          .detectAll()
          .build()
      )
      StrictMode.setVmPolicy(
          StrictMode.VmPolicy.Builder()
          .detectAll()
          .build()
      )
  }
  
```

You can decide what should happen when a violation is detected. For example, using `https://developer.android.com/reference/kotlin/android/os/StrictMode.ThreadPolicy.Builder#penaltyLog()` you can watch the output of `adb logcat` while you use your application to see the violations as they happen.

If you find violations that you feel are problematic, there are a variety of tools to help solve them: threads, `https://developer.android.com/reference/kotlin/android/os/Handler`, `https://developer.android.com/reference/kotlin/android/os/AsyncTask`, `https://developer.android.com/reference/kotlin/android/app/IntentService.html#`, etc. But don't feel compelled to fix everything that StrictMode finds. In particular, many cases of disk access are often necessary during the normal activity lifecycle. Use StrictMode to find things you did by accident. Network requests on the UI thread are almost always a problem, though.

StrictMode is not a security mechanism and is not guaranteed to find all disk or network accesses. While it does propagate its state across process boundaries when doing `https://developer.android.com/reference/kotlin/android/os/Binder` calls, it's still ultimately a best effort mechanism. Notably, disk or network access from JNI calls won't necessarily trigger it.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/os/StrictMode.OnThreadViolationListener` When #`https://developer.android.com/reference/kotlin/android/os/StrictMode.ThreadPolicy.Builder#penaltyListener(java.util.concurrent.Executor,%20android.os.StrictMode.OnThreadViolationListener)` is enabled, the listener is called on the provided executor when a Thread violation occurs. |
| abstract | `https://developer.android.com/reference/kotlin/android/os/StrictMode.OnVmViolationListener` When #`https://developer.android.com/reference/kotlin/android/os/StrictMode.VmPolicy.Builder#penaltyListener(java.util.concurrent.Executor,%20android.os.StrictMode.OnVmViolationListener)` is enabled, the listener is called on the provided executor when a VM violation occurs. |
| | `https://developer.android.com/reference/kotlin/android/os/StrictMode.ThreadPolicy` `https://developer.android.com/reference/kotlin/android/os/StrictMode#` policy applied to a certain thread. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/os/StrictMode.VmPolicy` `https://developer.android.com/reference/kotlin/android/os/StrictMode#` policy applied to all threads in the virtual machine's process. |

| Public methods ||
|---|---|
| static [StrictMode.ThreadPolicy](../android/os/StrictMode.ThreadPolicy.md)! | `https://developer.android.com/reference/kotlin/android/os/StrictMode#allowThreadDiskReads()()` A convenience wrapper that takes the current `https://developer.android.com/reference/kotlin/android/os/StrictMode.ThreadPolicy` from `https://developer.android.com/reference/kotlin/android/os/StrictMode#getThreadPolicy()`, modifies it to permit disk reads, and sets the new policy with `https://developer.android.com/reference/kotlin/android/os/StrictMode#setThreadPolicy(android.os.StrictMode.ThreadPolicy)`, returning the old policy so you can restore it at the end of a block. |
| static [StrictMode.ThreadPolicy](../android/os/StrictMode.ThreadPolicy.md)! | `https://developer.android.com/reference/kotlin/android/os/StrictMode#allowThreadDiskWrites()()` A convenience wrapper that takes the current `https://developer.android.com/reference/kotlin/android/os/StrictMode.ThreadPolicy` from `https://developer.android.com/reference/kotlin/android/os/StrictMode#getThreadPolicy()`, modifies it to permit both disk reads \& writes, and sets the new policy with `https://developer.android.com/reference/kotlin/android/os/StrictMode#setThreadPolicy(android.os.StrictMode.ThreadPolicy)`, returning the old policy so you can restore it at the end of a block. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/StrictMode#enableDefaults()()` Enables the recommended StrictMode defaults, with violations just being logged. |
| --- | --- |
| static [StrictMode.ThreadPolicy](../android/os/StrictMode.ThreadPolicy.md)! | `https://developer.android.com/reference/kotlin/android/os/StrictMode#getThreadPolicy()()` Returns the current thread's policy. |
| static [StrictMode.VmPolicy](../android/os/StrictMode.VmPolicy.md)! | `https://developer.android.com/reference/kotlin/android/os/StrictMode#getVmPolicy()()` Gets the current VM policy. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/StrictMode#noteSlowCall(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` For code to note that it's slow. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/StrictMode#setThreadPolicy(android.os.StrictMode.ThreadPolicy)(policy: https://developer.android.com/reference/kotlin/android/os/StrictMode.ThreadPolicy!)` Sets the policy for what actions on the current thread should be detected, as well as the penalty if such actions occur. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/StrictMode#setVmPolicy(android.os.StrictMode.VmPolicy)(policy: https://developer.android.com/reference/kotlin/android/os/StrictMode.VmPolicy!)` Sets the policy for what actions in the VM process (on any thread) should be detected, as well as the penalty if such actions occur. |

## Public methods

### allowThreadDiskReads

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun allowThreadDiskReads(): StrictMode.ThreadPolicy!
```

A convenience wrapper that takes the current `https://developer.android.com/reference/kotlin/android/os/StrictMode.ThreadPolicy` from `https://developer.android.com/reference/kotlin/android/os/StrictMode#getThreadPolicy()`, modifies it to permit disk reads, and sets the new policy with `https://developer.android.com/reference/kotlin/android/os/StrictMode#setThreadPolicy(android.os.StrictMode.ThreadPolicy)`, returning the old policy so you can restore it at the end of a block.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/StrictMode.ThreadPolicy!` | the old policy, to be passed to setThreadPolicy to restore the policy. |

### allowThreadDiskWrites

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun allowThreadDiskWrites(): StrictMode.ThreadPolicy!
```

A convenience wrapper that takes the current `https://developer.android.com/reference/kotlin/android/os/StrictMode.ThreadPolicy` from `https://developer.android.com/reference/kotlin/android/os/StrictMode#getThreadPolicy()`, modifies it to permit both disk reads \& writes, and sets the new policy with `https://developer.android.com/reference/kotlin/android/os/StrictMode#setThreadPolicy(android.os.StrictMode.ThreadPolicy)`, returning the old policy so you can restore it at the end of a block.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/StrictMode.ThreadPolicy!` | the old policy, to be passed to `https://developer.android.com/reference/kotlin/android/os/StrictMode#setThreadPolicy(android.os.StrictMode.ThreadPolicy)` to restore the policy at the end of a block |

### enableDefaults

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun enableDefaults(): Unit
```

Enables the recommended StrictMode defaults, with violations just being logged.

This catches disk and network access on the main thread, as well as leaked SQLite cursors and unclosed resources. This is simply a wrapper around `https://developer.android.com/reference/kotlin/android/os/StrictMode#setVmPolicy(android.os.StrictMode.VmPolicy)` and `https://developer.android.com/reference/kotlin/android/os/StrictMode#setThreadPolicy(android.os.StrictMode.ThreadPolicy)`.

### getThreadPolicy

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getThreadPolicy(): StrictMode.ThreadPolicy!
```

Returns the current thread's policy.

### getVmPolicy

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getVmPolicy(): StrictMode.VmPolicy!
```

Gets the current VM policy.

### noteSlowCall

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun noteSlowCall(name: String!): Unit
```

For code to note that it's slow. This is a no-op unless the current thread's `https://developer.android.com/reference/kotlin/android/os/StrictMode.ThreadPolicy` has `https://developer.android.com/reference/kotlin/android/os/StrictMode.ThreadPolicy.Builder#detectCustomSlowCalls()` enabled.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a short string for the exception stack trace that's built if when this fires. |

### setThreadPolicy

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setThreadPolicy(policy: StrictMode.ThreadPolicy!): Unit
```

Sets the policy for what actions on the current thread should be detected, as well as the penalty if such actions occur.

Internally this sets a thread-local variable which is propagated across cross-process IPC calls, meaning you can catch violations when a system service or another process accesses the disk or network on your behalf.

| Parameters ||
|---|---|
| `policy` | [StrictMode.ThreadPolicy](../android/os/StrictMode.ThreadPolicy.md)!: the policy to put into place |

### setVmPolicy

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setVmPolicy(policy: StrictMode.VmPolicy!): Unit
```

Sets the policy for what actions in the VM process (on any thread) should be detected, as well as the penalty if such actions occur.

| Parameters ||
|---|---|
| `policy` | [StrictMode.VmPolicy](../android/os/StrictMode.VmPolicy.md)!: the policy to put into place |
