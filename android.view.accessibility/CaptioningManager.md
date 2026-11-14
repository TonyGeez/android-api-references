# CaptioningManager

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CaptioningManager

Kotlin| [Java](CaptioningManager.md) 
| --- | --- |

```
open class CaptioningManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.accessibility.CaptioningManager](CaptioningManager.md) |

Contains methods for accessing and monitoring preferred video captioning state and visual properties.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [CaptionStyle](../android/view/accessibility/CaptioningManager.CaptionStyle.md) Specifies visual properties for video captions, including foreground and background colors, edge properties, and typeface. |
| abstract | [CaptioningChangeListener](../android/view/accessibility/CaptioningManager.CaptioningChangeListener.md) Listener for changes in captioning properties, including enabled state and user style preferences. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addCaptioningChangeListener](CaptioningManager.md))`(`listener:` ` [CaptioningManager.CaptioningChangeListener](../android/view/accessibility/CaptioningManager.CaptioningChangeListener.md)`)` Adds a listener for changes in the user's preferred captioning enabled state and visual properties. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFontScale](CaptioningManager.md))`()` <br /> |
| [Locale](../java.util/Locale.md)? | [getLocale](CaptioningManager.md))`()` <br /> |
| --- | --- |
| open [CaptioningManager.CaptionStyle](../android/view/accessibility/CaptioningManager.CaptionStyle.md) | [getUserStyle](CaptioningManager.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCallCaptioningEnabled](CaptioningManager.md))`()` Returns true if system wide call captioning is enabled for this device. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](CaptioningManager.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSystemAudioCaptioningEnabled](CaptioningManager.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSystemAudioCaptioningUiEnabled](CaptioningManager.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeCaptioningChangeListener](CaptioningManager.md))`(`listener:` ` [CaptioningManager.CaptioningChangeListener](../android/view/accessibility/CaptioningManager.CaptioningChangeListener.md)`)` Removes a listener previously added using [addCaptioningChangeListener](CaptioningManager.md)). |
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
| `listener` | [CaptioningManager.CaptioningChangeListener](../android/view/accessibility/CaptioningManager.CaptioningChangeListener.md):the listener to add This value cannot be`null`. |

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
| [Locale](../java.util/Locale.md)? | the locale for the user's preferred captioning language, or null if not specified |

### getUserStyle

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUserStyle(): CaptioningManager.CaptionStyle
```

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CaptioningManager.CaptionStyle](../android/view/accessibility/CaptioningManager.CaptionStyle.md) | the user's preferred visual properties for captions as a [CaptionStyle](../android/view/accessibility/CaptioningManager.CaptionStyle.md), or the default style if not specified This value cannot be`null`. |

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

Removes a listener previously added using [addCaptioningChangeListener](CaptioningManager.md)).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [CaptioningManager.CaptioningChangeListener](../android/view/accessibility/CaptioningManager.CaptioningChangeListener.md):the listener to remove This value cannot be`null`. |
