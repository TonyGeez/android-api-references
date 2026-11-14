Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EmbeddedBiometricPrompt

```
class EmbeddedBiometricPrompt
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.biometrics.EmbeddedBiometricPrompt](EmbeddedBiometricPrompt.md) |

The embedded version of BiometricPrompt that allows client apps to pass in content to display above the biometric prompt as a connected sheet.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/EmbeddedBiometricPrompt.AuthenticationCallback` Callback structure provided to startAuthenticationSession. |
| | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/EmbeddedBiometricPrompt.Builder` A builder for the embedded version of BiometricPrompt that collects arguments to be shown on the system-provided biometric dialog. |
| abstract | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/EmbeddedBiometricPrompt.EmbeddedContentFactory` A factory that produces the custom embedded content view for the biometric prompt. |
| --- | --- |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/EmbeddedBiometricPrompt#START_MODE_DEFERRED:kotlin.Int` The prompt should be collapsed and display in the deferred/paused state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/EmbeddedBiometricPrompt#START_MODE_IMMEDIATE:kotlin.Int` Start authentication immediately with the full prompt displayed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/biometrics/EmbeddedBiometricPrompt#START_MODE_IMMEDIATE_UNLESS_OCCLUDED:kotlin.Int` Start authentication immediately unless the embedded content height exceeds the maximum allowed dimensions. |
| --- | --- |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getAllowedAuthenticators Gets the type(s) of authenticators that may be invoked by the prompt. |
| [EmbeddedBiometricPrompt.AuthenticationCallback](../android/hardware/biometrics/EmbeddedBiometricPrompt.AuthenticationCallback.md)? | getAuthenticationCallback Gets the authentication callback used for the prompt. |
| [Executor](../java.util.concurrent/Executor.md)? | getAuthenticationExecutor Gets the executor used for the authentication callback. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getAuthenticationPurpose Gets the authentication purpose for the prompt. |
| [PromptContentView](PromptContentView.md)? | getContentView Gets the content view, as set by setContentView. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | getDescription Gets the description, as set by setDescription. |
| --- | --- |
| [EmbeddedBiometricPrompt.EmbeddedContentFactory](../android/hardware/biometrics/EmbeddedBiometricPrompt.EmbeddedContentFactory.md) | getEmbeddedContentFactory Gets the factory that will create the content to display above the biometric prompt as a connected sheet. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getExistingAuthSessionId Returns the existing auth session id for BiometricPrompt. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [FallbackOption](FallbackOption.md)!\> | getFallbackOptions Gets the fallback options for the prompt. |
| --- | --- |
| [Bitmap](../android.graphics/Bitmap.md)? | getLogoBitmap Gets the logo bitmap, as set by setLogoBitmap. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getLogoDescription Gets the logo description, as set by setLogoDescription. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getLogoRes Gets the drawable resource of the logo, as set by setLogoRes. |
| --- | --- |
| [DialogInterface.OnClickListener](../android/content/DialogInterface.OnClickListener.md)? | getNegativeButton Gets the negative button listener, as set by setNegativeButton. |
| [Executor](../java.util.concurrent/Executor.md)? | getNegativeButtonExecutor Gets the executor used for the negative button listener, as set by setNegativeButton. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | getNegativeButtonText Gets the negative button text, as set by setNegativeButton. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getNextTranslationOffset Gets the ending target layout translation offset in pixels (px) for the disappear (exit) animation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPreviousTranslationOffset Gets the starting layout translation offset in pixels (px) for the appear (entry) animation. |
| [BiometricPromptStyleSpec](BiometricPromptStyleSpec.md)? | getStyleSpec Returns a BiometricPromptStyleSpec containing the style specifications of BiometricPrompt |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | getSubtitle Gets the subtitle, as set by setSubtitle. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | getTitle Gets the title, as set by setTitle. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isConfirmationRequired Determines if explicit user confirmation is required by the prompt. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | pauseAuthentication Pauses biometric authentication and collapses the biometric prompt to the delayed state, displaying a button in its place. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | resumeAuthentication Activates biometric authentication and starts the biometric sensor scanning if delayed authentication was configured. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setNextTranslationOffset Sets the ending target layout translation offset in pixels (px) for the disappear (exit) animation. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | startAuthenticationSession Starts an authentication session for embedded BiometricPrompt. |

## Constants

### START_MODE_DEFERRED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_MODE_DEFERRED: Int
```

The prompt should be collapsed and display in the deferred/paused state. A shorter bottom sheet with a down arrow button is shown in place of the full prompt, and biometric sensors are not activated. Apps can call resumeAuthentication when ready to expand the bottom sheet to the full prompt and activate biometric sensors to begin authenticating.

 Value: 2

### START_MODE_IMMEDIATE

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_MODE_IMMEDIATE: Int
```

Start authentication immediately with the full prompt displayed.

 Value: 0

### START_MODE_IMMEDIATE_UNLESS_OCCLUDED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_MODE_IMMEDIATE_UNLESS_OCCLUDED: Int
```

Start authentication immediately unless the embedded content height exceeds the maximum allowed dimensions. If authentication is started and the provided embedded content exceeds the maximum available space, the prompt displays in the deferred/paused state, where it shows a shorter bottom sheet with a down arrow button in place of the full prompt, and biometric sensors are not activated. Apps can listen for onAuthenticationPaused in this case, and respond by calling resumeAuthentication when ready to expand the bottom sheet to the full prompt and activate biometric sensors to begin authenticating.

 Value: 1

## Public methods

### getAllowedAuthenticators

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAllowedAuthenticators(): Int
```

Gets the type(s) of authenticators that may be invoked by the prompt.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A bit field representing the type(s) of authenticators that may be invoked by the prompt. |

### getAuthenticationCallback

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAuthenticationCallback(): EmbeddedBiometricPrompt.AuthenticationCallback?
```

Gets the authentication callback used for the prompt.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/biometrics/EmbeddedBiometricPrompt.AuthenticationCallback?` | The authentication callback used for the prompt, or null if not set. |

### getAuthenticationExecutor

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAuthenticationExecutor(): Executor?
```

Gets the executor used for the authentication callback.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#?` | The executor used for the authentication callback, or null if not set. |

### getAuthenticationPurpose

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAuthenticationPurpose(): Int
```

Gets the authentication purpose for the prompt.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The authentication purpose. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#AUTHENTICATION_PURPOSE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#AUTHENTICATION_PURPOSE_PAYMENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager#AUTHENTICATION_PURPOSE_LOGIN:kotlin.Int` |

### getContentView

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getContentView(): PromptContentView?
```

Gets the content view, as set by setContentView. This is only applicable to the device credential fallback page (when the user is authenticating with PIN/pattern/password).

| Return ||
|---|---|
| PromptContentView | The content view for the prompt, or null if the prompt has no content view. |

### getDescription

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDescription(): CharSequence?
```

Gets the description, as set by setDescription. This is only applicable to the device credential fallback page (when the user is authenticating with PIN/pattern/password).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | The description for the prompt, or null if the prompt has no description. |

### getEmbeddedContentFactory

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEmbeddedContentFactory(): EmbeddedBiometricPrompt.EmbeddedContentFactory
```

Gets the factory that will create the content to display above the biometric prompt as a connected sheet.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/biometrics/EmbeddedBiometricPrompt.EmbeddedContentFactory` | The factory used to create the content view. This value cannot be `null`. |

### getExistingAuthSessionId

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExistingAuthSessionId(): Long
```

Returns the existing auth session id for BiometricPrompt.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The existing auth session id, or EmbeddedBiometricPrompt if none has been set. |

### getFallbackOptions

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFallbackOptions(): MutableList<FallbackOption!>
```

Gets the fallback options for the prompt.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/hardware/biometrics/FallbackOption!>` | The fallback options for the prompt. This value cannot be `null`. |

### getLogoBitmap

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLogoBitmap(): Bitmap?
```

Gets the logo bitmap, as set by setLogoBitmap. This is only applicable to the device credential fallback page (when the user is authenticating with PIN/pattern/password). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_BIOMETRIC_DIALOG_ADVANCED:kotlin.String`

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#?` | The logo bitmap of the prompt, or null if the prompt has no logo bitmap set. |

### getLogoDescription

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLogoDescription(): String?
```

Gets the logo description, as set by setLogoDescription. This is only applicable to the device credential fallback page (when the user is authenticating with PIN/pattern/password). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_BIOMETRIC_DIALOG_ADVANCED:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | The logo description of the prompt, or null if the prompt has no logo description set. |

### getLogoRes

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLogoRes(): Int
```

Gets the drawable resource of the logo, as set by setLogoRes. This is only applicable to the device credential fallback page (when the user is authenticating with PIN/pattern/password). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_BIOMETRIC_DIALOG_ADVANCED:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The drawable resource of the logo, or 0 if the prompt has no logo resource set. |

### getNegativeButton

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNegativeButton(): DialogInterface.OnClickListener?
```

Gets the negative button listener, as set by setNegativeButton.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnClickListener.html#?` | The negative button listener, or null if not set. |

### getNegativeButtonExecutor

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNegativeButtonExecutor(): Executor?
```

Gets the executor used for the negative button listener, as set by setNegativeButton.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#?` | The executor used for the negative button listener, or null if not set. |

### getNegativeButtonText

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNegativeButtonText(): CharSequence?
```

Gets the negative button text, as set by setNegativeButton.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | The negative button text, or null if not set. |

### getNextTranslationOffset

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNextTranslationOffset(): Int
```

Gets the ending target layout translation offset in pixels (px) for the disappear (exit) animation.

In portrait mode, this target offset is applied vertically along the Y-axis.

In landscape mode, this target offset is applied horizontally along the X-axis.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The ending target translation offset in pixels (px). |

### getPreviousTranslationOffset

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPreviousTranslationOffset(): Int
```

Gets the starting layout translation offset in pixels (px) for the appear (entry) animation.

In portrait mode, this offset is applied vertically along the Y-axis.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The starting translation offset in pixels (px), or -1 if the system default is used. |

### getStyleSpec

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStyleSpec(): BiometricPromptStyleSpec?
```

Returns a BiometricPromptStyleSpec containing the style specifications of BiometricPrompt

| Return ||
|---|---|
| BiometricPromptStyleSpec | the style specifications of BiometricPrompt. This value may be `null`. |

### getSubtitle

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSubtitle(): CharSequence?
```

Gets the subtitle, as set by setSubtitle. This is only applicable to the device credential fallback page (when the user is authenticating with PIN/pattern/password).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | The subtitle for the prompt, or null if the prompt has no subtitle. |

### getTitle

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTitle(): CharSequence?
```

Gets the title, as set by setTitle. This is only applicable to the device credential fallback page (when the user is authenticating with PIN/pattern/password).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | The title of the prompt, or null if not set. |

### isConfirmationRequired

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isConfirmationRequired(): Boolean
```

Determines if explicit user confirmation is required by the prompt.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if explicit user confirmation is required, or false otherwise. |

### pauseAuthentication

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun pauseAuthentication(): Unit
```

Pauses biometric authentication and collapses the biometric prompt to the delayed state, displaying a button in its place.

### resumeAuthentication

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun resumeAuthentication(): Unit
```

Activates biometric authentication and starts the biometric sensor scanning if delayed authentication was configured. If authentication was started with `https://developer.android.com/reference/kotlin/android/hardware/biometrics/EmbeddedBiometricPrompt#START_MODE_IMMEDIATE_UNLESS_OCCLUDED:kotlin.Int` and the embedded content exceeds the allowed dimensions, or authentication was started with `https://developer.android.com/reference/kotlin/android/hardware/biometrics/EmbeddedBiometricPrompt#START_MODE_DEFERRED:kotlin.Int`, the prompt is initially hidden and in a paused state, instead displaying a downward arrow button. Calling this method transitions the layout to show the sensor and biometric prompt content, and activates the biometric sensor to actively start authenticating.

### setNextTranslationOffset

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setNextTranslationOffset(offset: Int): Unit
```

Sets the ending target layout translation offset in pixels (px) for the disappear (exit) animation.

When the prompt is dismissed, it animates from its resting position to this target layout offset.

In portrait mode, the target offset is applied vertically along the Y-axis.

In landscape mode, the target offset is applied horizontally along the X-axis.

| Parameters ||
|---|---|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The target translation offset in pixels (px). |

### startAuthenticationSession

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun startAuthenticationSession(
    cancel: CancellationSignal, 
    startMode: Int, 
    executor: Executor, 
    callback: EmbeddedBiometricPrompt.AuthenticationCallback
): Unit
```

Starts an authentication session for embedded BiometricPrompt. This call warms up the biometric hardware, displays a system-provided dialog, and starts scanning for a biometric. Authentication starts when onSessionStarted is called, terminates when onAuthenticationError is called, when onAuthenticationSucceeded is called, or when the user dismisses the system-provided dialog. This operation can be canceled by using the provided cancel object. The application will receive authentication errors through `https://developer.android.com/reference/kotlin/android/hardware/biometrics/EmbeddedBiometricPrompt.AuthenticationCallback`, and button events through the corresponding callback set in addFallbackOption.

| Parameters ||
|---|---|
| `cancel` | [CancellationSignal](../android.os/CancellationSignal.md): An object that can be used to cancel authentication. This value cannot be `null`. |
| `startMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The mode determining when authentication starts (e.g. `https://developer.android.com/reference/kotlin/android/hardware/biometrics/EmbeddedBiometricPrompt#START_MODE_IMMEDIATE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/hardware/biometrics/EmbeddedBiometricPrompt#START_MODE_IMMEDIATE_UNLESS_OCCLUDED:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/hardware/biometrics/EmbeddedBiometricPrompt#START_MODE_DEFERRED:kotlin.Int`). Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/EmbeddedBiometricPrompt#START_MODE_IMMEDIATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/EmbeddedBiometricPrompt#START_MODE_IMMEDIATE_UNLESS_OCCLUDED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/biometrics/EmbeddedBiometricPrompt#START_MODE_DEFERRED:kotlin.Int` |
| `executor` | [Executor](../java.util.concurrent/Executor.md): An executor to handle callback events. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| --- | --- |
| `callback` | [EmbeddedBiometricPrompt.AuthenticationCallback](../android/hardware/biometrics/EmbeddedBiometricPrompt.AuthenticationCallback.md): An object to receive authentication events. This value cannot be `null`. |
