# ViewTranslationCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ViewTranslationCallback

Kotlin| [Java](ViewTranslationCallback.md) 
| --- | --- |

```
interface ViewTranslationCallback
```

| [android.view.translation.ViewTranslationCallback](ViewTranslationCallback.md) |

Callback for handling the translated information show or hide in the [View](../android.view/View.md).

When the platform intelligence starts translation of an app's ui, the system will call [View.dispatchCreateViewTranslationRequest](../android.view/View.md))to collect the [ViewTranslationRequest](ViewTranslationRequest.md) s for translation purpose by traversing the hierarchy then send to translation service. After receiving the [ViewTranslationResponse](ViewTranslationResponse.md), the system will call [ViewTranslationCallback.onShowTranslation(View)](ViewTranslationCallback.md))to show the translated information for the [View](../android.view/View.md).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onClearTranslation](ViewTranslationCallback.md))`(`view:` ` [View](../android.view/View.md)`)` Called when the translation state is no longer needed. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onHideTranslation](ViewTranslationCallback.md))`(`view:` ` [View](../android.view/View.md)`)` Called when user wants to view the original content instead of the translated content. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onShowTranslation](ViewTranslationCallback.md))`(`view:` ` [View](../android.view/View.md)`)` Called when the translated text is ready to show or if the user has requested to reshow the translated content after hiding it. |
| --- | --- |

## Public methods

### onClearTranslation

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClearTranslation(view: View): Boolean
```

Called when the translation state is no longer needed. It should restore the original content and clear all saved states.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android.view/View.md):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the View handles clearing the translation. |

### onHideTranslation

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onHideTranslation(view: View): Boolean
```

Called when user wants to view the original content instead of the translated content. This method will not be called before [View.onViewTranslationResponse](../android.view/View.md))or [View.onVirtualViewTranslationResponses](../android.view/View.md)).

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android.view/View.md):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the View handles hiding the translation. |

### onShowTranslation

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onShowTranslation(view: View): Boolean
```

Called when the translated text is ready to show or if the user has requested to reshow the translated content after hiding it.

The translated content can be obtained from [View.getViewTranslationResponse](../android.view/View.md)). This method will not be called before [View.onViewTranslationResponse](../android.view/View.md))or [View.onVirtualViewTranslationResponses](../android.view/View.md)).

NOTE: It is possible the user changes text that causes a new [ViewTranslationResponse](ViewTranslationResponse.md) returns to show the new translation. If you cache the [ViewTranslationResponse](ViewTranslationResponse.md) here, you should remember to keep the cached value up to date.

NOTE: For TextView implementation, [ContentCaptureSession.notifyViewTextChanged](../android.view.contentcapture/ContentCaptureSession.md))shouldn't be called with the translated text, simply calling setText() here will trigger the method. You should either override`View#onProvideContentCaptureStructure()`to report the original text instead of the translated text or use a different approach to display the translated text.

NOTE: In Android version [android.os.Build.VERSION_CODES#TIRAMISU](../android/os/Build.VERSION_CODES.md) and later, the implementation must be able to handle a selectable [android.widget.TextView](../android.widget/TextView.md)(i.e., [android.widget.TextView#isTextSelectable()](../android.widget/TextView.md))returns`true`. The default callback implementation for TextView uses a [android.text.method.TransformationMethod](../android.text.method/TransformationMethod.md) to show the translated text, which will cause a crash when the translated text is selected. Therefore, the default callback temporarily makes the TextView non-selectable while the translation text is shown. This is one approach for handling selectable TextViews a TransformationMethod is used. See [View.onViewTranslationResponse](../android.view/View.md))for how to get the translated information.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android.view/View.md):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the View handles showing the translation. |
