# InputMethod

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputMethod

Kotlin| [Java](../android/accessibilityservice/InputMethod.md) 
| --- | --- |

```
open class InputMethod
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.accessibilityservice.InputMethod](../android/accessibilityservice/InputMethod.md) |

This class provides input method APIs. Some public methods such as [onUpdateSelection(int,int,int,int,int,int)](../android/accessibilityservice/InputMethod.md))do nothing by default and service developers should override them as needed. Developers should also override [AccessibilityService.onCreateInputMethod()](../android/accessibilityservice/AccessibilityService.md))to return their custom InputMethod implementation. Accessibility services also need to set the [AccessibilityServiceInfo.FLAG_INPUT_METHOD_EDITOR](../android/accessibilityservice/AccessibilityServiceInfo.md) flag to use input method APIs.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [AccessibilityInputConnection](../android/accessibilityservice/InputMethod.AccessibilityInputConnection.md) This class provides the allowed list of [InputConnection](../android/view/inputmethod/InputConnection.md) APIs for accessibility services. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InputMethod](../android/accessibilityservice/InputMethod.md))`(`service:` ` [AccessibilityService](../android/accessibilityservice/AccessibilityService.md)`)` Creates a new InputMethod instance for the given`service`, so that the accessibility service can control editing. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [InputMethod.AccessibilityInputConnection](../android/accessibilityservice/InputMethod.AccessibilityInputConnection.md)? | [getCurrentInputConnection](../android/accessibilityservice/InputMethod.md))`()` Retrieve the currently active InputConnection that is bound to the input method, or null if there is none. |
| [EditorInfo](../android/view/inputmethod/EditorInfo.md)? | [getCurrentInputEditorInfo](../android/accessibilityservice/InputMethod.md))`()` Get the EditorInfo which describes several attributes of a text editing object that an accessibility service is communicating with (typically an EditText). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getCurrentInputStarted](../android/accessibilityservice/InputMethod.md))`()` Whether the input has started. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFinishInput](../android/accessibilityservice/InputMethod.md))`()` Called to inform the accessibility service that text input has finished in the last editor. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStartInput](../android/accessibilityservice/InputMethod.md))`(`attribute:` ` [EditorInfo](../android/view/inputmethod/EditorInfo.md)`, `restarting:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called to inform the accessibility service that text input has started in an editor. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onUpdateSelection](../android/accessibilityservice/InputMethod.md))`(`oldSelStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `oldSelEnd:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newSelStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newSelEnd:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `candidatesStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `candidatesEnd:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the application has reported a new selection region of the text. |
| --- | --- |

## Public constructors

### InputMethod

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InputMethod(service: AccessibilityService)
```

Creates a new InputMethod instance for the given`service`, so that the accessibility service can control editing.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `service` | [AccessibilityService](../android/accessibilityservice/AccessibilityService.md):This value cannot be`null`. |

## Public methods

### getCurrentInputConnection

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCurrentInputConnection(): InputMethod.AccessibilityInputConnection?
```

Retrieve the currently active InputConnection that is bound to the input method, or null if there is none. 

### getCurrentInputEditorInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCurrentInputEditorInfo(): EditorInfo?
```

Get the EditorInfo which describes several attributes of a text editing object that an accessibility service is communicating with (typically an EditText).

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------|
| [EditorInfo](../android/view/inputmethod/EditorInfo.md)? | This value may be`null`. |

### getCurrentInputStarted

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCurrentInputStarted(): Boolean
```

Whether the input has started. 

### onFinishInput

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onFinishInput(): Unit
```

Called to inform the accessibility service that text input has finished in the last editor. At this point there may be a call to [onStartInput(android.view.inputmethod.EditorInfo,boolean)](../android/accessibilityservice/InputMethod.md))to perform input in a new editor, or the accessibility service may be left idle. This method is*not*called when input restarts in the same editor.

The default implementation uses the InputConnection to clear any active composing text; you can override this (not calling the base class implementation) to perform whatever behavior you would like. 

### onStartInput

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onStartInput(
    attribute: EditorInfo, 
    restarting: Boolean
): Unit
```

Called to inform the accessibility service that text input has started in an editor. You should use this callback to initialize the state of your input to match the state of the editor given to it.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `attribute` | [EditorInfo](../android/view/inputmethod/EditorInfo.md):The attributes of the editor that input is starting in. This value cannot be`null`. |
| `restarting` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Set to true if input is restarting in the same editor such as because the application has changed the text in the editor. Otherwise will be false, indicating this is a new session with the editor. |

### onUpdateSelection

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onUpdateSelection(
    oldSelStart: Int, 
    oldSelEnd: Int, 
    newSelStart: Int, 
    newSelEnd: Int, 
    candidatesStart: Int, 
    candidatesEnd: Int
): Unit
```

Called when the application has reported a new selection region of the text. This is called whether or not the accessibility service has requested extracted text updates, although if so it will not receive this call if the extracted text has changed as well.

Be careful about changing the text in reaction to this call with methods such as setComposingText, commitText or deleteSurroundingText. If the cursor moves as a result, this method will be called again, which may result in an infinite loop.
