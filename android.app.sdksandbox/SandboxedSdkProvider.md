Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SandboxedSdkProvider

```
abstract class SandboxedSdkProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.sdksandbox.SandboxedSdkProvider](SandboxedSdkProvider.md) |

> [!CAUTION]
> **This class was deprecated in API level 37.**
>
> The SDK sandbox is no longer supported.

Encapsulates API which SDK sandbox can use to interact with SDKs loaded into it.

SDK has to implement this abstract class to generate an entry point for SDK sandbox to be able to call it through.

## Summary

| Public constructors ||
|---|---|
| SandboxedSdkProvider <br /> |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | attachContext Sets the SDK `https://developer.android.com/reference/kotlin/android/content/Context.html#` which can then be received using getContext. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | beforeUnloadSdk Does the work needed for the SDK to free its resources before being unloaded. |
| [Context](../android.content/Context.md)? | getContext Return the `https://developer.android.com/reference/kotlin/android/content/Context.html#` previously set through attachContext. |
| --- | --- |
| abstract [View](../android.view/View.md) | getView Requests a view to be remotely rendered to the client app process. |
| abstract [SandboxedSdk](SandboxedSdk.md) | onLoadSdk Does the work needed for the SDK to start handling requests. |

## Public constructors

### SandboxedSdkProvider

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

```
SandboxedSdkProvider()
```

## Public methods

### attachContext

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun attachContext(context: Context): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the SDK `https://developer.android.com/reference/kotlin/android/content/Context.html#` which can then be received using getContext. This is called before onLoadSdk is invoked. No operations requiring a `https://developer.android.com/reference/kotlin/android/content/Context.html#` should be performed before then, as getContext will return null until this method has been called.

Throws IllegalStateException if a base context has already been set.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The new base context. This value cannot be `null`. |

### beforeUnloadSdk

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun beforeUnloadSdk(): Unit
```

**Deprecated:** *Deprecated in Java.*

Does the work needed for the SDK to free its resources before being unloaded.

This function is called by the SDK sandbox manager before it unloads the SDK. The SDK should fail any invocations on the Binder previously returned to the client through getInterface.

The SDK should not do any long-running tasks here, like I/O and network calls.

### getContext

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getContext(): Context?
```

**Deprecated:** *Deprecated in Java.*

Return the `https://developer.android.com/reference/kotlin/android/content/Context.html#` previously set through attachContext. This will return null if no context has been previously set.

### getView

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getView(
    windowContext: Context, 
    params: Bundle, 
    width: Int, 
    height: Int
): View
```

**Deprecated:** *This method will no longer be supported as it is being used by requestSurfacePackage which is getting deprecated.*

Requests a view to be remotely rendered to the client app process.

Returns `https://developer.android.com/reference/kotlin/android/view/View.html#` will be wrapped into `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.SurfacePackage.html#`. the resulting `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.SurfacePackage.html#` will be sent back to the client application.

The SDK should not do any long-running tasks here, like I/O and network calls. Doing so can prevent the SDK from receiving requests from the client.

| Parameters ||
|---|---|
| `windowContext` | [Context](../android.content/Context.md): the `https://developer.android.com/reference/kotlin/android/content/Context.html#` of the display which meant to show the view. This value cannot be `null`. |
| `params` | [Bundle](../android.os/Bundle.md): list of params passed from the client application requesting the view. This value cannot be `null`. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The view returned will be laid as if in a window of this width, in pixels. |
| --- | --- |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The view returned will be laid as if in a window of this height, in pixels. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View.html#` | a `https://developer.android.com/reference/kotlin/android/view/View.html#` which SDK sandbox pass to the client application requesting the view. This value cannot be `null`. |

### onLoadSdk

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onLoadSdk(params: Bundle): SandboxedSdk
```

**Deprecated:** *Deprecated in Java.*

Does the work needed for the SDK to start handling requests.

This function is called by the SDK sandbox after it loads the SDK.

SDK should do any work to be ready to handle upcoming requests. It should not do any long-running tasks here, like I/O and network calls. Doing so can prevent the SDK from receiving requests from the client. Additionally, it should not do initialization that depends on other SDKs being loaded into the SDK sandbox.

The SDK should not do any operations requiring a `https://developer.android.com/reference/kotlin/android/content/Context.html#` object before this method has been called.

| Parameters ||
|---|---|
| `params` | [Bundle](../android.os/Bundle.md): list of params passed from the client when it loads the SDK. This can be empty. This value cannot be `null`. |

| Return ||
|---|---|
| SandboxedSdk | Returns a SandboxedSdk, passed back to the client. The IBinder used to create the SandboxedSdk object will be used by the client to call into the SDK. This value cannot be `null`. |
