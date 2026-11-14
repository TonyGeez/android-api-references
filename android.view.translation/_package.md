# android.view.translation

# android.view.translation

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [UiTranslationStateCallback](UiTranslationStateCallback.md) | Callback for listening to UI Translation state changes. |
| --- | --- |
| [ViewTranslationCallback](ViewTranslationCallback.md) | Callback for handling the translated information show or hide in the [View](../android.view/View.md). |

## Classes

| [TranslationCapability](TranslationCapability.md) | Capability class holding information for a pair of [TranslationSpec](TranslationSpec.md) s. |
| --- | --- |
| [TranslationContext](TranslationContext.md) | Info class holding information for [Translator](Translator.md) s and used by [TranslationManager.createOnDeviceTranslator(TranslationContext, Executor, Consumer)](TranslationManager.md)). |
| [TranslationManager](TranslationManager.md) | The [TranslationManager](TranslationManager.md) class provides ways for apps to integrate and use the translation framework. |
| [TranslationRequest](TranslationRequest.md) | Translation request sent to the translation service by the [android.view.translation.Translator](Translator.md) which contains the text to be translated. |
| --- | --- |
| [TranslationRequestValue](TranslationRequestValue.md) | A value to be translated via [android.view.translation.Translator](Translator.md). |
| [TranslationResponse](TranslationResponse.md) | Response from the translation service, which contains the translated result. |
| [TranslationResponseValue](TranslationResponseValue.md) | A translated response value from translation service. |
| --- | --- |
| [TranslationSpec](TranslationSpec.md) | Specs and additional info for the translation data. |
| [Translator](Translator.md) | The [Translator](Translator.md) for translation, defined by a [TranslationContext](TranslationContext.md). |
| [UiTranslationManager](UiTranslationManager.md) | The [UiTranslationManager](UiTranslationManager.md) class provides ways for apps to use the ui translation function in framework. |
| --- | --- |
| [ViewTranslationRequest](ViewTranslationRequest.md) | Wrapper class representing a translation request associated with a [android.view.View](../android.view/View.md) to be used by translation service. |
| [ViewTranslationResponse](ViewTranslationResponse.md) | Wrapper class representing a translation response associated with a [android.view.View](../android.view/View.md) to be used by translation service. |
