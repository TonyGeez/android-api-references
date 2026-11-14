# AccessibilityService.TakeScreenshotCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TakeScreenshotCallback

Kotlin| [Java](../android/accessibilityservice/AccessibilityService.TakeScreenshotCallback.md) 
| --- | --- |

```
interface TakeScreenshotCallback
```

| [android.accessibilityservice.AccessibilityService.TakeScreenshotCallback](../android/accessibilityservice/AccessibilityService.TakeScreenshotCallback.md) |

Interface used to report status of taking screenshot.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFailure](../android/accessibilityservice/AccessibilityService.TakeScreenshotCallback.md))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when taking screenshot has failed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSuccess](../android/accessibilityservice/AccessibilityService.TakeScreenshotCallback.md))`(`screenshot:` ` [AccessibilityService.ScreenshotResult](../android/accessibilityservice/AccessibilityService.ScreenshotResult.md)`)` Called when taking screenshot has completed successfully. |

## Public methods

### onFailure

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFailure(errorCode: Int): Unit
```

Called when taking screenshot has failed.`errorCode`will identify the reason of failure.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The error code of this operation. Value is [android.accessibilityservice.AccessibilityService#ERROR_TAKE_SCREENSHOT_INTERNAL_ERROR](AccessibilityService.md), [android.accessibilityservice.AccessibilityService#ERROR_TAKE_SCREENSHOT_NO_ACCESSIBILITY_ACCESS](AccessibilityService.md), [android.accessibilityservice.AccessibilityService#ERROR_TAKE_SCREENSHOT_INTERVAL_TIME_SHORT](AccessibilityService.md), [android.accessibilityservice.AccessibilityService#ERROR_TAKE_SCREENSHOT_INVALID_DISPLAY](AccessibilityService.md), or [android.accessibilityservice.AccessibilityService#ERROR_TAKE_SCREENSHOT_INVALID_WINDOW](AccessibilityService.md) |

### onSuccess

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSuccess(screenshot: AccessibilityService.ScreenshotResult): Unit
```

Called when taking screenshot has completed successfully.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `screenshot` | [AccessibilityService.ScreenshotResult](../android/accessibilityservice/AccessibilityService.ScreenshotResult.md):The content of screenshot. This value cannot be`null`. |
