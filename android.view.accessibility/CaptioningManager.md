# CaptioningManager

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CaptioningManager

Kotlin| [Java](https://developer.android.com/reference/android/view/accessibility/CaptioningManager "View this page in Java") 
| --- | --- |

```
open class CaptioningManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.accessibility.CaptioningManager](https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager#) |

Contains methods for accessing and monitoring preferred video captioning state and visual properties.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [CaptionStyle](https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager.CaptionStyle) Specifies visual properties for video captions, including foreground and background colors, edge properties, and typeface. |
| abstract | [CaptioningChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager.CaptioningChangeListener) Listener for changes in captioning properties, including enabled state and user style preferences. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addCaptioningChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager#addCaptioningChangeListener(android.view.accessibility.CaptioningManager.CaptioningChangeListener))`(`listener:` ` [CaptioningManager.CaptioningChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager.CaptioningChangeListener)`)` Adds a listener for changes in the user's preferred captioning enabled state and visual properties. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFontScale](https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager#getFontScale())`()` <br /> |
| [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)? | [getLocale](https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager#getLocale())`()` <br /> |
| --- | --- |
| open [CaptioningManager.CaptionStyle](https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager.CaptionStyle) | [getUserStyle](https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager#getUserStyle())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCallCaptioningEnabled](https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager#isCallCaptioningEnabled())`()` Returns true if system wide call captioning is enabled for this device. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager#isEnabled())`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSystemAudioCaptioningEnabled](https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager#isSystemAudioCaptioningEnabled())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSystemAudioCaptioningUiEnabled](https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager#isSystemAudioCaptioningUiEnabled())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeCaptioningChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager#removeCaptioningChangeListener(android.view.accessibility.CaptioningManager.CaptioningChangeListener))`(`listener:` ` [CaptioningManager.CaptioningChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager.CaptioningChangeListener)`)` Removes a listener previously added using [addCaptioningChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager#addCaptioningChangeListener(android.view.accessibility.CaptioningManager.CaptioningChangeListener)). |
| --- | --- |

## Public methods

### addCaptioningChangeListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addCaptioningChangeListener(listener: CaptioningManager.CaptioningChangeListener): Unit
```

Adds a listener for changes in the user's preferred captioning enabled state and visual properties.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [CaptioningManager.CaptioningChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager.CaptioningChangeListener):the listener to add This value cannot be`null`. |

### getFontScale

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFontScale(): Float
```

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the user's preferred font scaling factor for video captions, or 1 if not specified |

### getLocale

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLocale(): Locale?
```

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)? | the locale for the user's preferred captioning language, or null if not specified |

### getUserStyle

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUserStyle(): CaptioningManager.CaptionStyle
```

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CaptioningManager.CaptionStyle](https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager.CaptionStyle) | the user's preferred visual properties for captions as a [CaptionStyle](https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager.CaptionStyle), or the default style if not specified This value cannot be`null`. |

### isCallCaptioningEnabled

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isCallCaptioningEnabled(): Boolean
```

Returns true if system wide call captioning is enabled for this device. 

### isEnabled

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isEnabled(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the user's preferred captioning enabled state |

### isSystemAudioCaptioningEnabled

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSystemAudioCaptioningEnabled(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the system audio caption enabled state. |

### isSystemAudioCaptioningUiEnabled

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSystemAudioCaptioningUiEnabled(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the system audio caption UI enabled state. |

### removeCaptioningChangeListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeCaptioningChangeListener(listener: CaptioningManager.CaptioningChangeListener): Unit
```

Removes a listener previously added using [addCaptioningChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager#addCaptioningChangeListener(android.view.accessibility.CaptioningManager.CaptioningChangeListener)).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [CaptioningManager.CaptioningChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager.CaptioningChangeListener):the listener to remove This value cannot be`null`. |
