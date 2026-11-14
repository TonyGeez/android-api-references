# ViewTranslationCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ViewTranslationCallback

Kotlin| [Java](https://developer.android.com/reference/android/view/translation/ViewTranslationCallback "View this page in Java") 

```
interface ViewTranslationCallback
```

| [android.view.translation.ViewTranslationCallback](https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationCallback#) |

Callback for handling the translated information show or hide in the [View](https://developer.android.com/reference/kotlin/android/view/View.html#).

When the platform intelligence starts translation of an app's ui, the system will call [View.dispatchCreateViewTranslationRequest](https://developer.android.com/reference/kotlin/android/view/View.html#dispatchCreateViewTranslationRequest(kotlin.collections.MutableMap,%20kotlin.IntArray,%20android.view.translation.TranslationCapability,%20kotlin.collections.MutableList))to collect the [ViewTranslationRequest](https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationRequest) s for translation purpose by traversing the hierarchy then send to translation service. After receiving the [ViewTranslationResponse](https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationResponse), the system will call [ViewTranslationCallback.onShowTranslation(View)](https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationCallback#onShowTranslation(android.view.View))to show the translated information for the [View](https://developer.android.com/reference/kotlin/android/view/View.html#).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onClearTranslation](https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationCallback#onClearTranslation(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`)` Called when the translation state is no longer needed. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onHideTranslation](https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationCallback#onHideTranslation(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`)` Called when user wants to view the original content instead of the translated content. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onShowTranslation](https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationCallback#onShowTranslation(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`)` Called when the translated text is ready to show or if the user has requested to reshow the translated content after hiding it. |

## Public methods

### onClearTranslation

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClearTranslation(view: View): Boolean
```

Called when the translation state is no longer needed. It should restore the original content and clear all saved states.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the View handles clearing the translation. |

### onHideTranslation

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onHideTranslation(view: View): Boolean
```

Called when user wants to view the original content instead of the translated content. This method will not be called before [View.onViewTranslationResponse](https://developer.android.com/reference/kotlin/android/view/View.html#onViewTranslationResponse(android.view.translation.ViewTranslationResponse))or [View.onVirtualViewTranslationResponses](https://developer.android.com/reference/kotlin/android/view/View.html#onVirtualViewTranslationResponses(android.util.LongSparseArray)).

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the View handles hiding the translation. |

### onShowTranslation

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onShowTranslation(view: View): Boolean
```

Called when the translated text is ready to show or if the user has requested to reshow the translated content after hiding it.

The translated content can be obtained from [View.getViewTranslationResponse](https://developer.android.com/reference/kotlin/android/view/View.html#getViewTranslationResponse()). This method will not be called before [View.onViewTranslationResponse](https://developer.android.com/reference/kotlin/android/view/View.html#onViewTranslationResponse(android.view.translation.ViewTranslationResponse))or [View.onVirtualViewTranslationResponses](https://developer.android.com/reference/kotlin/android/view/View.html#onVirtualViewTranslationResponses(android.util.LongSparseArray)).

NOTE: It is possible the user changes text that causes a new [ViewTranslationResponse](https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationResponse) returns to show the new translation. If you cache the [ViewTranslationResponse](https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationResponse) here, you should remember to keep the cached value up to date.

NOTE: For TextView implementation, [ContentCaptureSession.notifyViewTextChanged](https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession.html#notifyViewTextChanged(android.view.autofill.AutofillId,%20kotlin.CharSequence))shouldn't be called with the translated text, simply calling setText() here will trigger the method. You should either override`View#onProvideContentCaptureStructure()`to report the original text instead of the translated text or use a different approach to display the translated text.

NOTE: In Android version [android.os.Build.VERSION_CODES#TIRAMISU](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int) and later, the implementation must be able to handle a selectable [android.widget.TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)(i.e., [android.widget.TextView#isTextSelectable()](https://developer.android.com/reference/kotlin/android/widget/TextView.html#isTextSelectable())returns`true`. The default callback implementation for TextView uses a [android.text.method.TransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/TransformationMethod.html#) to show the translated text, which will cause a crash when the translated text is selected. Therefore, the default callback temporarily makes the TextView non-selectable while the translation text is shown. This is one approach for handling selectable TextViews a TransformationMethod is used. See [View.onViewTranslationResponse](https://developer.android.com/reference/kotlin/android/view/View.html#onViewTranslationResponse(android.view.translation.ViewTranslationResponse))for how to get the translated information.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the View handles showing the translation. |
