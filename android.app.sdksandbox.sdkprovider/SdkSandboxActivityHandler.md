Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 7](https://developer.android.com/sdkExtensions)

# SdkSandboxActivityHandler

Kotlin | [Java](SdkSandboxActivityHandler.md)
| --- | --- |

```
interface SdkSandboxActivityHandler
```

| [android.app.sdksandbox.sdkprovider.SdkSandboxActivityHandler](SdkSandboxActivityHandler.md) |

This is used to notify the SDK when an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` is created for it.

When an SDK wants to start an `https://developer.android.com/reference/kotlin/android/app/Activity.html#`, it should register an implementation of this class by calling `https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxController#registerSdkSandboxActivityHandler(android.app.sdksandbox.sdkprovider.SdkSandboxActivityHandler)` that will return an `https://developer.android.com/reference/kotlin/android/os/IBinder.html#` identifier for the registered `https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxActivityHandler#` to The SDK.

The SDK should be notified about the `https://developer.android.com/reference/kotlin/android/app/Activity.html#` creation by calling `https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxActivityHandler#onActivityCreated(android.app.Activity)` which happens when the caller app calls `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager.html#startSdkSandboxActivity(android.app.Activity,%20android.os.IBinder)` using the same `https://developer.android.com/reference/kotlin/android/os/IBinder.html#` identifier for the registered `https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxActivityHandler#`.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxActivityHandler#onActivityCreated(android.app.Activity)(activity: https://developer.android.com/reference/kotlin/android/app/Activity.html#)` Notifies SDK when an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` gets created. |

## Public methods

### onActivityCreated

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun onActivityCreated(activity: Activity): Unit
```

**Deprecated:** *Deprecated in Java.*

Notifies SDK when an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` gets created.

This function is called synchronously from the main thread of the `https://developer.android.com/reference/kotlin/android/app/Activity.html#` that is getting created.

SDK is expected to call `https://developer.android.com/reference/kotlin/android/app/Activity.html#setContentView(android.view.View)` to the passed `https://developer.android.com/reference/kotlin/android/app/Activity.html#` object to populate the view.

If SDK registers lifecycle callbacks over the passed `https://developer.android.com/reference/kotlin/android/app/Activity.html#` object using `https://developer.android.com/reference/kotlin/android/app/Activity.html#registerActivityLifecycleCallbacks(android.app.Application.ActivityLifecycleCallbacks)`, it is important to note that `https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks.html#onActivityPreCreated(android.app.Activity,%20android.os.Bundle)` and `https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks.html#onActivityCreated(android.app.Activity,%20android.os.Bundle)` will not be triggered as `https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxActivityHandler#onActivityCreated(android.app.Activity)` is called at the `https://developer.android.com/reference/kotlin/android/app/Activity.html#` creation stage. Then to know about the Activity state, SDKs should override `https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks.html#onActivityPostCreated(android.app.Activity,%20android.os.Bundle)`.

| Parameters ||
|---|---|
| `activity` | [Activity](../android.app/Activity.md): the `https://developer.android.com/reference/kotlin/android/app/Activity.html#` gets created. This value cannot be `null`. |
