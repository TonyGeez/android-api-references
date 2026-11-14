# ConnectionlessHandwritingCallback

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConnectionlessHandwritingCallback

Kotlin| [Java](https://developer.android.com/reference/android/view/inputmethod/ConnectionlessHandwritingCallback "View this page in Java") 
| --- | --- |

```
interface ConnectionlessHandwritingCallback
```

| [android.view.inputmethod.ConnectionlessHandwritingCallback](https://developer.android.com/reference/kotlin/android/view/inputmethod/ConnectionlessHandwritingCallback#) |

Interface to receive the result of starting a connectionless stylus handwriting session using one of [InputMethodManager.startConnectionlessStylusHandwriting(View, CursorAnchorInfo,](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startConnectionlessStylusHandwriting(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)), [android.view.inputmethod.InputMethodManager#startConnectionlessStylusHandwritingForDelegation(android.view.View,android.view.inputmethod.CursorAnchorInfo,java.util.concurrent.Executor,android.view.inputmethod.ConnectionlessHandwritingCallback)](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startConnectionlessStylusHandwritingForDelegation(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)), or [android.view.inputmethod.InputMethodManager#startConnectionlessStylusHandwritingForDelegation(android.view.View,android.view.inputmethod.CursorAnchorInfo,java.lang.String,java.util.concurrent.Executor,android.view.inputmethod.ConnectionlessHandwritingCallback)](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startConnectionlessStylusHandwritingForDelegation(android.view.View,%20android.view.inputmethod.CursorAnchorInfo,%20kotlin.String,%20java.util.concurrent.Executor,%20android.view.inputmethod.ConnectionlessHandwritingCallback)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONNECTIONLESS_HANDWRITING_ERROR_NO_TEXT_RECOGNIZED](https://developer.android.com/reference/kotlin/android/view/inputmethod/ConnectionlessHandwritingCallback#CONNECTIONLESS_HANDWRITING_ERROR_NO_TEXT_RECOGNIZED:kotlin.Int) Error code indicating that the connectionless handwriting session started and completed but no text was recognized. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONNECTIONLESS_HANDWRITING_ERROR_OTHER](https://developer.android.com/reference/kotlin/android/view/inputmethod/ConnectionlessHandwritingCallback#CONNECTIONLESS_HANDWRITING_ERROR_OTHER:kotlin.Int) Error code for any other reason that the connectionless handwriting session did not complete successfully. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONNECTIONLESS_HANDWRITING_ERROR_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/view/inputmethod/ConnectionlessHandwritingCallback#CONNECTIONLESS_HANDWRITING_ERROR_UNSUPPORTED:kotlin.Int) Error code indicating that the connectionless handwriting session was not started as the current IME does not support it. |
| --- | --- |

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](https://developer.android.com/reference/kotlin/android/view/inputmethod/ConnectionlessHandwritingCallback#onError(kotlin.Int))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback when the connectionless handwriting session did not complete successfully. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResult](https://developer.android.com/reference/kotlin/android/view/inputmethod/ConnectionlessHandwritingCallback#onResult(kotlin.CharSequence))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`)` Callback when the connectionless handwriting session completed successfully and recognized text. |

## Constants

### CONNECTIONLESS_HANDWRITING_ERROR_NO_TEXT_RECOGNIZED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONNECTIONLESS_HANDWRITING_ERROR_NO_TEXT_RECOGNIZED: Int
```

Error code indicating that the connectionless handwriting session started and completed but no text was recognized. 

 Value: 0

### CONNECTIONLESS_HANDWRITING_ERROR_OTHER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONNECTIONLESS_HANDWRITING_ERROR_OTHER: Int
```

Error code for any other reason that the connectionless handwriting session did not complete successfully. Either the session could not start, or the session started but did not complete successfully. 

 Value: 2

### CONNECTIONLESS_HANDWRITING_ERROR_UNSUPPORTED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONNECTIONLESS_HANDWRITING_ERROR_UNSUPPORTED: Int
```

Error code indicating that the connectionless handwriting session was not started as the current IME does not support it. 

 Value: 1

## Public methods

### onError

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onError(errorCode: Int): Unit
```

Callback when the connectionless handwriting session did not complete successfully.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.view.inputmethod.ConnectionlessHandwritingCallback#CONNECTIONLESS_HANDWRITING_ERROR_NO_TEXT_RECOGNIZED](https://developer.android.com/reference/kotlin/android/view/inputmethod/ConnectionlessHandwritingCallback#CONNECTIONLESS_HANDWRITING_ERROR_NO_TEXT_RECOGNIZED:kotlin.Int), [android.view.inputmethod.ConnectionlessHandwritingCallback#CONNECTIONLESS_HANDWRITING_ERROR_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/view/inputmethod/ConnectionlessHandwritingCallback#CONNECTIONLESS_HANDWRITING_ERROR_UNSUPPORTED:kotlin.Int), or [android.view.inputmethod.ConnectionlessHandwritingCallback#CONNECTIONLESS_HANDWRITING_ERROR_OTHER](https://developer.android.com/reference/kotlin/android/view/inputmethod/ConnectionlessHandwritingCallback#CONNECTIONLESS_HANDWRITING_ERROR_OTHER:kotlin.Int) |

### onResult

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onResult(text: CharSequence): Unit
```

Callback when the connectionless handwriting session completed successfully and recognized text.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):This value cannot be`null`. |
