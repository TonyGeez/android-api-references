# android.view.translation

# android.view.translation

Kotlin| [Java](https://developer.android.com/reference/android/view/translation/package-summary "View this page in Java")

## Interfaces

| [UiTranslationStateCallback](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationStateCallback) | Callback for listening to UI Translation state changes. |
| [ViewTranslationCallback](https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationCallback) | Callback for handling the translated information show or hide in the [View](https://developer.android.com/reference/kotlin/android/view/View.html#). |

## Classes

| [TranslationCapability](https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability) | Capability class holding information for a pair of [TranslationSpec](https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec) s. |
| [TranslationContext](https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext) | Info class holding information for [Translator](https://developer.android.com/reference/kotlin/android/view/translation/Translator) s and used by [TranslationManager.createOnDeviceTranslator(TranslationContext, Executor, Consumer)](https://developer.android.com/reference/kotlin/android/view/translation/TranslationManager#createOnDeviceTranslator(android.view.translation.TranslationContext,%20java.util.concurrent.Executor,%20java.util.function.Consumer)). |
| [TranslationManager](https://developer.android.com/reference/kotlin/android/view/translation/TranslationManager) | The [TranslationManager](https://developer.android.com/reference/kotlin/android/view/translation/TranslationManager) class provides ways for apps to integrate and use the translation framework. |
| [TranslationRequest](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest) | Translation request sent to the translation service by the [android.view.translation.Translator](https://developer.android.com/reference/kotlin/android/view/translation/Translator) which contains the text to be translated. |
| [TranslationRequestValue](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequestValue) | A value to be translated via [android.view.translation.Translator](https://developer.android.com/reference/kotlin/android/view/translation/Translator). |
| [TranslationResponse](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse) | Response from the translation service, which contains the translated result. |
| [TranslationResponseValue](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue) | A translated response value from translation service. |
| [TranslationSpec](https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec) | Specs and additional info for the translation data. |
| [Translator](https://developer.android.com/reference/kotlin/android/view/translation/Translator) | The [Translator](https://developer.android.com/reference/kotlin/android/view/translation/Translator) for translation, defined by a [TranslationContext](https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext). |
| [UiTranslationManager](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationManager) | The [UiTranslationManager](https://developer.android.com/reference/kotlin/android/view/translation/UiTranslationManager) class provides ways for apps to use the ui translation function in framework. |
| [ViewTranslationRequest](https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationRequest) | Wrapper class representing a translation request associated with a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#) to be used by translation service. |
| [ViewTranslationResponse](https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationResponse) | Wrapper class representing a translation response associated with a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#) to be used by translation service. |
