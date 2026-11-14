Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyguardManager

Kotlin | [Java](KeyguardManager.md)
| --- | --- |

```
open class KeyguardManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.KeyguardManager](KeyguardManager.md) |

Class to manage and query the state of the lock screen (also known as Keyguard).

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.DeviceLockedStateListener` Listener for device locked state changes. |
| abstract | `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.KeyguardDismissCallback` Callback passed to `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#requestDismissKeyguard(android.app.Activity,%20android.app.KeyguardManager.KeyguardDismissCallback)` to notify caller of result. |
| open | `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.KeyguardLock` Handle returned by `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#newKeyguardLock(kotlin.String)` that allows you to temporarily disable / reenable the keyguard (lock screen). |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.KeyguardLockedStateListener` Listener for keyguard locked state changes. |
| abstract | `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.OnKeyguardExitResult` Callback passed to `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#exitKeyguardSecurely(android.app.KeyguardManager.OnKeyguardExitResult)` to notify caller of result. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#addDeviceLockedStateListener(java.util.concurrent.Executor,%20android.app.KeyguardManager.DeviceLockedStateListener)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/app/KeyguardManager.DeviceLockedStateListener)` Registers a listener to execute when the device locked state changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#addKeyguardLockedStateListener(java.util.concurrent.Executor,%20android.app.KeyguardManager.KeyguardLockedStateListener)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/app/KeyguardManager.KeyguardLockedStateListener)` Registers a listener to execute when the keyguard locked state changes. |
| open [Intent](../android.content/Intent.md)! | `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#createConfirmDeviceCredentialIntent(kotlin.CharSequence,%20kotlin.CharSequence)(title: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, description: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Get an intent to prompt the user to confirm credentials (pin, pattern, password or biometrics if enrolled) for the current user of the device. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#exitKeyguardSecurely(android.app.KeyguardManager.OnKeyguardExitResult)(callback: https://developer.android.com/reference/kotlin/android/app/KeyguardManager.OnKeyguardExitResult!)` Exit the keyguard securely. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#inKeyguardRestrictedInputMode()()` Returns whether the lock screen is showing. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#isDeviceLocked()()` Returns whether the device is currently locked for the user. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#isDeviceSecure()()` Returns whether the user has a secure lock screen. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#isKeyguardLocked()()` Returns whether the lock screen (also known as Keyguard) is showing. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#isKeyguardSecure()()` Returns whether the user has a secure lock screen or there is a locked SIM card. |
| --- | --- |
| open [KeyguardManager.KeyguardLock](../android/app/KeyguardManager.KeyguardLock.md)! | `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#newKeyguardLock(kotlin.String)(tag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Enables you to temporarily disable / reenable the keyguard (lock screen). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#removeDeviceLockedStateListener(android.app.KeyguardManager.DeviceLockedStateListener)(listener: https://developer.android.com/reference/kotlin/android/app/KeyguardManager.DeviceLockedStateListener)` Unregisters a listener that executes when the device locked state changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#removeKeyguardLockedStateListener(android.app.KeyguardManager.KeyguardLockedStateListener)(listener: https://developer.android.com/reference/kotlin/android/app/KeyguardManager.KeyguardLockedStateListener)` Unregisters a listener that executes when the keyguard locked state changes. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#requestDismissKeyguard(android.app.Activity,%20android.app.KeyguardManager.KeyguardDismissCallback)(activity: https://developer.android.com/reference/kotlin/android/app/Activity, callback: https://developer.android.com/reference/kotlin/android/app/KeyguardManager.KeyguardDismissCallback?)` Requests that the Keyguard (lock screen) be dismissed if it is currently showing. |

## Public methods

### addDeviceLockedStateListener

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addDeviceLockedStateListener(
    executor: Executor, 
    listener: KeyguardManager.DeviceLockedStateListener
): Unit
```

Registers a listener to execute when the device locked state changes. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SUBSCRIBE_TO_KEYGUARD_LOCKED_STATE:kotlin.String`

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): The `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` where the `listener` will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [KeyguardManager.DeviceLockedStateListener](../android/app/KeyguardManager.DeviceLockedStateListener.md): The listener to add to receive device locked state changes. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#isDeviceLocked()`
- `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#removeDeviceLockedStateListener(android.app.KeyguardManager.DeviceLockedStateListener)`

### addKeyguardLockedStateListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addKeyguardLockedStateListener(
    executor: Executor, 
    listener: KeyguardManager.KeyguardLockedStateListener
): Unit
```

Registers a listener to execute when the keyguard locked state changes. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SUBSCRIBE_TO_KEYGUARD_LOCKED_STATE:kotlin.String`

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [KeyguardManager.KeyguardLockedStateListener](../android/app/KeyguardManager.KeyguardLockedStateListener.md): The listener to add to receive keyguard locked state changes. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#isKeyguardLocked()`
- `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#removeKeyguardLockedStateListener(android.app.KeyguardManager.KeyguardLockedStateListener)`

### createConfirmDeviceCredentialIntent

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createConfirmDeviceCredentialIntent(
    title: CharSequence!, 
    description: CharSequence!
): Intent!
```

**Deprecated:** *see `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricPrompt.Builder.html#setAllowedAuthenticators(kotlin.Int)`*

Get an intent to prompt the user to confirm credentials (pin, pattern, password or biometrics if enrolled) for the current user of the device. The caller is expected to launch this activity using `https://developer.android.com/reference/kotlin/android/app/Activity#startActivityForResult(android.content.Intent,%20kotlin.Int)` and check for `https://developer.android.com/reference/kotlin/android/app/Activity#RESULT_OK:kotlin.Int` if the user successfully completes the challenge. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_SECURE_LOCK_SCREEN:kotlin.String` feature which can be detected using `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Intent.html#!` | the intent for launching the activity or null if no password is required. |

### exitKeyguardSecurely

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun exitKeyguardSecurely(callback: KeyguardManager.OnKeyguardExitResult!): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/R.attr.html#showWhenLocked:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/app/Activity#setShowWhenLocked(kotlin.Boolean)` to seamlessly occlude and unocclude the keyguard as your application moves in and out of the foreground, without requiring any special permissions. Use `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#requestDismissKeyguard(android.app.Activity,%20android.app.KeyguardManager.KeyguardDismissCallback)` to request dismissal of the keyguard.*

Exit the keyguard securely. The use case for this api is that, after disabling the keyguard, your app, which was granted permission to disable the keyguard and show a limited amount of information deemed safe without the user getting past the keyguard, needs to navigate to something that is not safe to view without getting past the keyguard. This will, if the keyguard is secure, bring up the unlock screen of the keyguard. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#DISABLE_KEYGUARD:kotlin.String`

| Parameters ||
|---|---|
| `callback` | [KeyguardManager.OnKeyguardExitResult](../android/app/KeyguardManager.OnKeyguardExitResult.md)!: Lets you know whether the operation was successful and it is safe to launch anything that would normally be considered safe once the user has gotten past the keyguard. |

### inKeyguardRestrictedInputMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun inKeyguardRestrictedInputMode(): Boolean
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#isKeyguardLocked()` instead.*

Returns whether the lock screen is showing.

This is exactly the same as `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#isKeyguardLocked()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the value of `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#isKeyguardLocked()` |

### isDeviceLocked

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDeviceLocked(): Boolean
```

Returns whether the device is currently locked for the user.

This method returns the device locked state for the `https://developer.android.com/reference/kotlin/android/content/Context.html#`'s user. The device is considered to be locked for a user when the user's apps are currently inaccessible and some form of lock screen authentication is required to regain access to them. The lock screen authentication typically uses PIN, pattern, password, or biometric. Some devices may support additional methods, such as unlock using a paired smartwatch. "Swipe" does not count as authentication; if the lock screen is dismissible with swipe, for example due to the lock screen being set to Swipe or due to the device being kept unlocked by being near a trusted bluetooth device or in a trusted location, the device is considered unlocked.

> [!NOTE]
> **Note:** In the case of multiple full users, each user can have their own lock screen authentication configured. The device-locked state may differ between different users. For example, the device may be unlocked for the current user, but locked for a non-current user if lock screen authentication would be required to access that user's apps after switching to that user.
>
> In the case of a profile, when the device goes to the main lock screen, up to two layers of authentication may be required to regain access to the profile's apps: one to unlock the main lock screen, and one to unlock the profile (when a separate profile challenge is required). For a profile, the device is considered to be locked as long as any challenge remains, either the parent user's challenge (when applicable) or the profile's challenge (when applicable).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the device is currently locked for the user |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#isKeyguardLocked()`

### isDeviceSecure

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDeviceSecure(): Boolean
```

Returns whether the user has a secure lock screen.

This returns `true` if the `https://developer.android.com/reference/kotlin/android/content/Context.html#`'s user has a secure lock screen. A full user or a profile that uses a separate challenge has a secure lock screen if its lock screen is set to PIN, pattern, or password, as opposed to swipe or none. A profile that uses a unified challenge is considered to have a secure lock screen if and only if its parent user has a secure lock screen.

This method does not consider whether the lock screen is currently showing or not.

See also `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#isKeyguardSecure()` which includes locked SIM cards.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the user has a secure lock screen |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#isKeyguardSecure()`

### isKeyguardLocked

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isKeyguardLocked(): Boolean
```

Returns whether the lock screen (also known as Keyguard) is showing.

Specifically, this returns `true` in the following cases:

- The lock screen is showing in the foreground.
- The lock screen is showing, but it is occluded by an activity that is showing on top of it. A common example is the phone app receiving a call or making an emergency call.
- The lock screen was showing but is temporarily disabled as a result of [lock task mode](https://developer.android.com/work/dpc/dedicated-devices/lock-task-mode) or an app using the deprecated `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.KeyguardLock` API.

"Showing" refers to a logical state of the UI, regardless of whether the screen happens to be on. When the power button is pressed on an unlocked device, the lock screen starts "showing" immediately when the screen turns off.

This method does not distinguish a lock screen that is requiring authentication (e.g. with PIN, pattern, password, or biometric) from a lock screen that is trivially dismissible (e.g. with swipe). It also does not distinguish a lock screen requesting a SIM card PIN from a normal device lock screen. Finally, it always returns the global lock screen state and does not consider the `https://developer.android.com/reference/kotlin/android/content/Context.html#`'s user specifically.

Note that `isKeyguardLocked()` is confusingly named and probably should be called `isKeyguardShowing()`. On many devices, the lock screen displays an *unlocked* padlock icon when it is trivially dismissible. As mentioned above, `isKeyguardLocked()` actually returns `true` in this case, not `false` as might be expected. `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#isDeviceLocked()` is an alternative API that has slightly different semantics.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the lock screen is showing |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#isDeviceLocked()`

### isKeyguardSecure

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isKeyguardSecure(): Boolean
```

Returns whether the user has a secure lock screen or there is a locked SIM card.

Specifically, this returns `true` if at least one of the following is true:

- The `https://developer.android.com/reference/kotlin/android/content/Context.html#`'s user has a secure lock screen. A full user or a profile that uses a separate challenge has a secure lock screen if its lock screen is set to PIN, pattern, or password, as opposed to swipe or none. A profile that uses a unified challenge is considered to have a secure lock screen if and only if its parent user has a secure lock screen.
- At least one SIM card is currently locked and requires a PIN.

This method does not consider whether the lock screen is currently showing or not.

See also `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#isDeviceSecure()` which excludes locked SIM cards.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the user has a secure lock screen or there is a locked SIM card |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#isDeviceSecure()`

### newKeyguardLock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun newKeyguardLock(tag: String!): KeyguardManager.KeyguardLock!
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/R.attr.html#showWhenLocked:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/app/Activity#setShowWhenLocked(kotlin.Boolean)` instead. This allows you to seamlessly occlude and unocclude the keyguard as your application moves in and out of the foreground and does not require that any special permissions be requested.*

Enables you to temporarily disable / reenable the keyguard (lock screen).

| Parameters ||
|---|---|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A tag that informally identifies who you are (for debugging who is disabling the keyguard). |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.KeyguardLock!` | A `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.KeyguardLock` handle to use to disable and reenable the keyguard. |

### removeDeviceLockedStateListener

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeDeviceLockedStateListener(listener: KeyguardManager.DeviceLockedStateListener): Unit
```

Unregisters a listener that executes when the device locked state changes. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SUBSCRIBE_TO_KEYGUARD_LOCKED_STATE:kotlin.String`

| Parameters ||
|---|---|
| `listener` | [KeyguardManager.DeviceLockedStateListener](../android/app/KeyguardManager.DeviceLockedStateListener.md): The listener to remove. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#isDeviceLocked()`
- `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#addDeviceLockedStateListener(java.util.concurrent.Executor,%20android.app.KeyguardManager.DeviceLockedStateListener)`

### removeKeyguardLockedStateListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeKeyguardLockedStateListener(listener: KeyguardManager.KeyguardLockedStateListener): Unit
```

Unregisters a listener that executes when the keyguard locked state changes. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SUBSCRIBE_TO_KEYGUARD_LOCKED_STATE:kotlin.String`

| Parameters ||
|---|---|
| `listener` | [KeyguardManager.KeyguardLockedStateListener](../android/app/KeyguardManager.KeyguardLockedStateListener.md): The listener to remove. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#isKeyguardLocked()`
- `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#addKeyguardLockedStateListener(java.util.concurrent.Executor,%20android.app.KeyguardManager.KeyguardLockedStateListener)`

### requestDismissKeyguard

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestDismissKeyguard(
    activity: Activity, 
    callback: KeyguardManager.KeyguardDismissCallback?
): Unit
```

Requests that the Keyguard (lock screen) be dismissed if it is currently showing.

If the Keyguard is not secure or the device is currently in a trusted state, calling this method will immediately dismiss the Keyguard without any user interaction.

If the Keyguard is secure and the device is not in a trusted state, this will bring up the UI so the user can enter their credentials.

If the value set for the `https://developer.android.com/reference/kotlin/android/app/Activity` attr `https://developer.android.com/reference/kotlin/android/R.attr.html#turnScreenOn:kotlin.Int` is true, the screen will turn on when the keyguard is dismissed.

| Parameters ||
|---|---|
| `activity` | [Activity](Activity.md): The activity requesting the dismissal. The activity must either be visible by using `https://developer.android.com/reference/kotlin/android/R.attr.html#showWhenLocked:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/app/Activity#setShowWhenLocked(kotlin.Boolean)`, or must be in a state in which it would be visible if Keyguard would not be hiding it. If that's not the case, the request will fail immediately and `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.KeyguardDismissCallback#onDismissError()` will be invoked. This value cannot be `null`. |
| `callback` | [KeyguardManager.KeyguardDismissCallback](../android/app/KeyguardManager.KeyguardDismissCallback.md)?: The callback to be called if the request to dismiss Keyguard was successful or `null` if the caller isn't interested in knowing the result. The callback will not be invoked if the activity was destroyed before the callback was received. |
