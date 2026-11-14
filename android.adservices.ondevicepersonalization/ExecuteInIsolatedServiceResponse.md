Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExecuteInIsolatedServiceResponse

```
open class ExecuteInIsolatedServiceResponse
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.adservices.ondevicepersonalization.ExecuteInIsolatedServiceResponse](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceResponse#) |

> [!CAUTION]
> **This class was deprecated in API level 37.**
>
> The ODP APIs are deprecated and will not be supported in future Android releases. There is no direct replacement API available. Developers currently integrated with these APIs must cease further integration efforts. For comprehensive details regarding this deprecation and the future roadmap of Privacy Sandbox on Android, please consult the official Privacy Sandbox developer documentation and announcements: <https://privacysandbox.google.com>

The response of `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationManager#executeInIsolatedService(android.adservices.ondevicepersonalization.ExecuteInIsolatedServiceRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceResponse#DEFAULT_BEST_VALUE:kotlin.Int` The default value of `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceResponse#getBestValue()` if `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService` didn't return any content. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceResponse#ExecuteInIsolatedServiceResponse(android.adservices.ondevicepersonalization.SurfacePackageToken,%20kotlin.Int)(surfacePackageToken: https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/SurfacePackageToken?, bestValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a new ExecuteInIsolatedServiceResponse. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceResponse#getBestValue()()` Returns the int value that was returned by the `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService` and applied noise. |
| open [SurfacePackageToken](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/SurfacePackageToken)? | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceResponse#getSurfacePackageToken()()` Returns a `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/SurfacePackageToken`, which is an opaque reference to content that can be displayed in a `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#`. |

## Constants

### DEFAULT_BEST_VALUE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEFAULT_BEST_VALUE: Int
```

**Deprecated:** *Deprecated in Java.*

The default value of `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceResponse#getBestValue()` if `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService` didn't return any content.

 Value: -1

## Public constructors

### ExecuteInIsolatedServiceResponse

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ExecuteInIsolatedServiceResponse(
    surfacePackageToken: SurfacePackageToken?, 
    bestValue: Int)
```

Creates a new ExecuteInIsolatedServiceResponse.

| Parameters ||
|---|---|
| `surfacePackageToken` | [SurfacePackageToken](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/SurfacePackageToken)?: an opaque reference to content that can be displayed in a `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#`. This may be `null` if the `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService` has not generated any content to be displayed within the calling app. |
| `bestValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an int value that was returned by the `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService` and applied noise.If `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest` output type is set to `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest.OutputSpec#OUTPUT_TYPE_NULL:kotlin.Int`, the platform ignores the data returned by `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService` and returns the default value `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceResponse#DEFAULT_BEST_VALUE:kotlin.Int`. If `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest` output type is set to `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest.OutputSpec#OUTPUT_TYPE_BEST_VALUE:kotlin.Int`, the platform validates `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteOutput#getBestValue()` between 0 and `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest.OutputSpec#getMaxIntValue()` and applies noise to result. Value is `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceResponse#DEFAULT_BEST_VALUE:kotlin.Int` or greater |

## Public methods

### getBestValue

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBestValue(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the int value that was returned by the `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService` and applied noise. If `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest` output type is set to `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest.OutputSpec#OUTPUT_TYPE_NULL:kotlin.Int`, the platform ignores the data returned by `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService` and returns the default value `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceResponse#DEFAULT_BEST_VALUE:kotlin.Int`. If `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest` output type is set to `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest.OutputSpec#OUTPUT_TYPE_BEST_VALUE:kotlin.Int`, the platform validates `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteOutput#getBestValue()` between 0 and `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest.OutputSpec#getMaxIntValue()` and applies noise to result.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceResponse#DEFAULT_BEST_VALUE:kotlin.Int` or greater |

### getSurfacePackageToken

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSurfacePackageToken(): SurfacePackageToken?
```

**Deprecated:** *Deprecated in Java.*

Returns a `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/SurfacePackageToken`, which is an opaque reference to content that can be displayed in a `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#`. This may be `null` if the `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService` has not generated any content to be displayed within the calling app.
