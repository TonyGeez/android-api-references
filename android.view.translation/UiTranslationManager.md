Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UiTranslationManager

Kotlin | [Java](UiTranslationManager.md)
| --- | --- |

```
class UiTranslationManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.translation.UiTranslationManager](UiTranslationManager.md) |

The UiTranslationManager class provides ways for apps to use the ui translation function in framework.

The UI translation provides ways for apps to support inline translation for the views. For example the system supports text translation for `https://developer.android.com/reference/kotlin/android/widget/TextView.html#`. To support UI translation for your views, you should override the following methods to provide the content to be translated and deal with the translated result. Here is an example for `https://developer.android.com/reference/kotlin/android/widget/TextView.html#`-like views:

```kotlin
<code>
  public class MyTextView extends View {
      public MyTextView(...) {
          // implements how to show the translated result in your View in
          // ViewTranslationCallback and set it by setViewTranslationCallback()
          setViewTranslationCallback(new MyViewTranslationCallback());
      }
 
      public void onCreateViewTranslationRequest(int[] supportedFormats,
              Consumer
 <viewtranslationrequest>
   requestsCollector) { // collect the information that needs to be translated ViewTranslationRequest.Builder requestBuilder = new ViewTranslationRequest.Builder(getAutofillId()); requestBuilder.setValue(ViewTranslationRequest.ID_TEXT, TranslationRequestValue.forText(etText())); requestsCollector.accept(requestBuilder.build()); } public void onProvideContentCaptureStructure( ViewStructure structure, int flags) { // set ViewTranslationResponse super.onViewTranslationResponse(response); } } 
 </viewtranslationrequest></code>
```

If your view provides its own virtual hierarchy (for example, if it's a browser that draws the HTML using `https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#` or native libraries in a different render process), you must override onCreateVirtualViewTranslationRequests to provide the content to be translated and implement onVirtualViewTranslationResponses for the translated result. You also need to implement ViewTranslationCallback to handle the translated information show or hide in your `https://developer.android.com/reference/kotlin/android/view/View.html#`.

## Summary

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerUiTranslationStateCallback Register for notifications of UI Translation state changes on the foreground Activity. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterUiTranslationStateCallback Unregister `callback`. |

## Public methods

### registerUiTranslationStateCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerUiTranslationStateCallback(
    executor: Executor, 
    callback: UiTranslationStateCallback
): Unit
```

Register for notifications of UI Translation state changes on the foreground Activity. This is available to the owning application itself and also the current input method.

The application whose UI is being translated can use this to customize the UI Translation behavior in ways that aren't made easy by methods like onCreateViewTranslationRequest.

Input methods can use this to offer complementary features to UI Translation; for example, enabling outgoing message translation when the system is translating incoming messages in a communication app.

Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, if Activities are already being translated when a callback is registered, methods on the callback will be invoked for each translated activity, depending on the state of translation:

- If translation is *not* paused, android.view.translation.UiTranslationStateCallback#onStarted will be invoked.
- If translation *is* paused, android.view.translation.UiTranslationStateCallback#onStarted will first be invoked, followed by android.view.translation.UiTranslationStateCallback#onPaused.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [UiTranslationStateCallback](UiTranslationStateCallback.md): the callback to register for receiving the state change notifications. This value cannot be `null`. |

### unregisterUiTranslationStateCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterUiTranslationStateCallback(callback: UiTranslationStateCallback): Unit
```

Unregister `callback`.

| Parameters ||
|---|---|
| `callback` | [UiTranslationStateCallback](UiTranslationStateCallback.md): This value cannot be `null`. |

**See Also**

- registerUiTranslationStateCallback
