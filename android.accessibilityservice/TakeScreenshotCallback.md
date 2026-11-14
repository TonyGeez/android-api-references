# AccessibilityService.TakeScreenshotCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TakeScreenshotCallback

Kotlin| [Java](https://developer.android.com/reference/android/accessibilityservice/AccessibilityService.TakeScreenshotCallback "View this page in Java") 

```
interface TakeScreenshotCallback
```

| [android.accessibilityservice.AccessibilityService.TakeScreenshotCallback](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.TakeScreenshotCallback#) |

Interface used to report status of taking screenshot.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFailure](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.TakeScreenshotCallback#onFailure(kotlin.Int))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when taking screenshot has failed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSuccess](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.TakeScreenshotCallback#onSuccess(android.accessibilityservice.AccessibilityService.ScreenshotResult))`(`screenshot:` ` [AccessibilityService.ScreenshotResult](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.ScreenshotResult)`)` Called when taking screenshot has completed successfully. |

## Public methods

### onFailure

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFailure(errorCode: Int): Unit
```

Called when taking screenshot has failed.`errorCode`will identify the reason of failure.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The error code of this operation. Value is [android.accessibilityservice.AccessibilityService#ERROR_TAKE_SCREENSHOT_INTERNAL_ERROR](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#ERROR_TAKE_SCREENSHOT_INTERNAL_ERROR:kotlin.Int), [android.accessibilityservice.AccessibilityService#ERROR_TAKE_SCREENSHOT_NO_ACCESSIBILITY_ACCESS](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#ERROR_TAKE_SCREENSHOT_NO_ACCESSIBILITY_ACCESS:kotlin.Int), [android.accessibilityservice.AccessibilityService#ERROR_TAKE_SCREENSHOT_INTERVAL_TIME_SHORT](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#ERROR_TAKE_SCREENSHOT_INTERVAL_TIME_SHORT:kotlin.Int), [android.accessibilityservice.AccessibilityService#ERROR_TAKE_SCREENSHOT_INVALID_DISPLAY](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#ERROR_TAKE_SCREENSHOT_INVALID_DISPLAY:kotlin.Int), or [android.accessibilityservice.AccessibilityService#ERROR_TAKE_SCREENSHOT_INVALID_WINDOW](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#ERROR_TAKE_SCREENSHOT_INVALID_WINDOW:kotlin.Int) |

### onSuccess

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSuccess(screenshot: AccessibilityService.ScreenshotResult): Unit
```

Called when taking screenshot has completed successfully.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `screenshot` | [AccessibilityService.ScreenshotResult](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.ScreenshotResult):The content of screenshot. This value cannot be`null`. |
