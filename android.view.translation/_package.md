# android.view.translation

# android.view.translation

Kotlin| [Java](../android/view/translation/_package.md)
| --- | --- |

## Interfaces

| [UiTranslationStateCallback](../android/view/translation/UiTranslationStateCallback.md) | Callback for listening to UI Translation state changes. |
| --- | --- |
| [ViewTranslationCallback](../android/view/translation/ViewTranslationCallback.md) | Callback for handling the translated information show or hide in the [View](../android/view/View.md). |

## Classes

| [TranslationCapability](../android/view/translation/TranslationCapability.md) | Capability class holding information for a pair of [TranslationSpec](../android/view/translation/TranslationSpec.md) s. |
| --- | --- |
| [TranslationContext](../android/view/translation/TranslationContext.md) | Info class holding information for [Translator](../android/view/translation/Translator.md) s and used by [TranslationManager.createOnDeviceTranslator(TranslationContext, Executor, Consumer)](../android/view/translation/TranslationManager.md)). |
| [TranslationManager](../android/view/translation/TranslationManager.md) | The [TranslationManager](../android/view/translation/TranslationManager.md) class provides ways for apps to integrate and use the translation framework. |
| [TranslationRequest](../android/view/translation/TranslationRequest.md) | Translation request sent to the translation service by the [android.view.translation.Translator](../android/view/translation/Translator.md) which contains the text to be translated. |
| --- | --- |
| [TranslationRequestValue](../android/view/translation/TranslationRequestValue.md) | A value to be translated via [android.view.translation.Translator](../android/view/translation/Translator.md). |
| [TranslationResponse](../android/view/translation/TranslationResponse.md) | Response from the translation service, which contains the translated result. |
| [TranslationResponseValue](../android/view/translation/TranslationResponseValue.md) | A translated response value from translation service. |
| --- | --- |
| [TranslationSpec](../android/view/translation/TranslationSpec.md) | Specs and additional info for the translation data. |
| [Translator](../android/view/translation/Translator.md) | The [Translator](../android/view/translation/Translator.md) for translation, defined by a [TranslationContext](../android/view/translation/TranslationContext.md). |
| [UiTranslationManager](../android/view/translation/UiTranslationManager.md) | The [UiTranslationManager](../android/view/translation/UiTranslationManager.md) class provides ways for apps to use the ui translation function in framework. |
| --- | --- |
| [ViewTranslationRequest](../android/view/translation/ViewTranslationRequest.md) | Wrapper class representing a translation request associated with a [android.view.View](../android/view/View.md) to be used by translation service. |
| [ViewTranslationResponse](../android/view/translation/ViewTranslationResponse.md) | Wrapper class representing a translation response associated with a [android.view.View](../android/view/View.md) to be used by translation service. |
