Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputMethod

```
interface InputMethod
```

| [android.view.inputmethod.InputMethod](../android/view/inputmethod/InputMethod.md) |

Known Direct Subclasses [AbstractInputMethodService.AbstractInputMethodImpl](../android/inputmethodservice/AbstractInputMethodService.AbstractInputMethodImpl.md) [AbstractInputMethodService.AbstractInputMethodImpl](../android/inputmethodservice/AbstractInputMethodService.AbstractInputMethodImpl.md) Base class for derived classes to implement their `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#` interface.
Known Indirect Subclasses [InputMethodService.InputMethodImpl](../android/inputmethodservice/InputMethodService.InputMethodImpl.md) [InputMethodService.InputMethodImpl](../android/inputmethodservice/InputMethodService.InputMethodImpl.md) Concrete implementation of `https://developer.android.com/reference/kotlin/android/inputmethodservice/AbstractInputMethodService.AbstractInputMethodImpl.html#` that provides all of the standard behavior for an input method.

The InputMethod interface represents an input method which can generate key events and text, such as digital, email addresses, CJK characters, other language characters, and etc., while handling various input events, and send the text back to the application that requests text input. See `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager` for more general information about the architecture.

Applications will not normally use this interface themselves, instead relying on the standard interaction provided by `https://developer.android.com/reference/kotlin/android/widget/TextView.html#` and `https://developer.android.com/reference/kotlin/android/widget/EditText.html#`.

Those implementing input methods should normally do so by deriving from `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#` or one of its subclasses. When implementing an input method, the service component containing it must also supply a `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#SERVICE_META_DATA:kotlin.String` meta-data field, referencing an XML resource providing details about the input method. All input methods also must require that clients hold the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BIND_INPUT_METHOD:kotlin.String` in order to interact with the service; if this is not required, the system will not use that input method, because it can not trust that it is not compromised.

The InputMethod interface is actually split into two parts: the interface here is the top-level interface to the input method, providing all access to it, which only the system can access (due to the BIND_INPUT_METHOD permission requirement). In addition its method `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#createSession(android.view.inputmethod.InputMethod.SessionCallback)` can be called to instantate a secondary `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession` interface which is what clients use to communicate with the input method.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod.SessionCallback` <br /> |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#SERVICE_INTERFACE:kotlin.String` This is the interface name that a service implementing an input method should say that it supports -- that is, this is the action it uses for its intent filter. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#SERVICE_META_DATA:kotlin.String` Name under which an InputMethod service component publishes information about itself. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#SHOW_EXPLICIT:kotlin.Int` Flag for `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#showSoftInput(kotlin.Int,%20android.os.ResultReceiver)`: this show has been explicitly requested by the user. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#SHOW_FORCED:kotlin.Int` Flag for `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#showSoftInput(kotlin.Int,%20android.os.ResultReceiver)`: this show has been forced to happen by the user. |

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#attachToken(android.os.IBinder)(token: https://developer.android.com/reference/kotlin/android/os/IBinder.html#!)` Called first thing after an input method is created, this supplies a unique token for the session it has with the system service. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#bindInput(android.view.inputmethod.InputBinding)(binding: https://developer.android.com/reference/kotlin/android/view/inputmethod/InputBinding!)` Bind a new application environment in to the input method, so that it can later start and stop input processing. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#changeInputMethodSubtype(android.view.inputmethod.InputMethodSubtype)(subtype: https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSubtype!)` Notify that the input method subtype is being changed in the same input method. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#createSession(android.view.inputmethod.InputMethod.SessionCallback)(callback: https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod.SessionCallback!)` Create a new `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession` that can be handed to client applications for interacting with the input method. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#hideSoftInput(kotlin.Int,%20android.os.ResultReceiver)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, resultReceiver: https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#!)` Request that any soft input part of the input method be hidden from the user. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#restartInput(android.view.inputmethod.InputConnection,%20android.view.inputmethod.EditorInfo)(inputConnection: https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection!, editorInfo: https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo!)` This method is called when the state of this input method needs to be reset. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#revokeSession(android.view.inputmethod.InputMethodSession)(session: https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession!)` Disable and destroy a session that was previously created with `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#createSession(android.view.inputmethod.InputMethod.SessionCallback)`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#setSessionEnabled(android.view.inputmethod.InputMethodSession,%20kotlin.Boolean)(session: https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession!, enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Control whether a particular input method session is active. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#showSoftInput(kotlin.Int,%20android.os.ResultReceiver)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, resultReceiver: https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#!)` Request that any soft input part of the input method be shown to the user. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#startInput(android.view.inputmethod.InputConnection,%20android.view.inputmethod.EditorInfo)(inputConnection: https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection!, editorInfo: https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo!)` This method is called when the application starts to receive text and it is ready for this input method to process received events and send result text back to the application. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#unbindInput()()` Unbind an application environment, called when the information previously set by `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#bindInput(android.view.inputmethod.InputBinding)` is no longer valid for this input method. |

## Constants

### SERVICE_INTERFACE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SERVICE_INTERFACE: String
```

This is the interface name that a service implementing an input method should say that it supports -- that is, this is the action it uses for its intent filter. To be supported, the service must also require the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BIND_INPUT_METHOD:kotlin.String` permission so that other applications can not abuse it.

 Value: "android.view.InputMethod"

### SERVICE_META_DATA

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SERVICE_META_DATA: String
```

Name under which an InputMethod service component publishes information about itself. This meta-data must reference an XML resource containing an ``<`https://developer.android.com/reference/kotlin/android/R.attr.html#inputMethod:kotlin.Int`>`` tag.

 Value: "android.view.im"

### SHOW_EXPLICIT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SHOW_EXPLICIT: Int
```

**Deprecated:** *`https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#SHOW_IMPLICIT:kotlin.Int` is deprecated therefore this flag becomes the default. There is no need to pass it anymore.*

Flag for `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#showSoftInput(kotlin.Int,%20android.os.ResultReceiver)`: this show has been explicitly requested by the user. If not set, the system has decided it may be a good idea to show the input method based on a navigation operation in the UI.

 Value: 1

### SHOW_FORCED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SHOW_FORCED: Int
```

**Deprecated:** *Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#SHOW_IMPLICIT:kotlin.Int` is deprecated and has no effect, therefore all requests will have this flag set. IMEs should no longer react to this flag.*

Flag for `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#showSoftInput(kotlin.Int,%20android.os.ResultReceiver)`: this show has been forced to happen by the user. If set, the input method should remain visible until deliberated dismissed by the user in its UI.

 Value: 2

## Public methods

### attachToken

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun attachToken(token: IBinder!): Unit
```

Called first thing after an input method is created, this supplies a unique token for the session it has with the system service. It is needed to identify itself with the service to validate its operations. This token **must not** be passed to applications, since it grants special priviledges that should not be given to applications.

The system guarantees that this method is called back between `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#onCreate()` and android.inputmethodservice.InputMethodService#onDestroy() at most once. 
This method must be called from the main thread of your app.

### bindInput

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun bindInput(binding: InputBinding!): Unit
```

Bind a new application environment in to the input method, so that it can later start and stop input processing. Typically this method is called when this input method is enabled in an application for the first time. 
This method must be called from the main thread of your app.

| Parameters ||
|---|---|
| `binding` | [InputBinding](../android/view/inputmethod/InputBinding.md)!: Information about the application window that is binding to the input method. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputBinding`
- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#unbindInput()`

### changeInputMethodSubtype

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun changeInputMethodSubtype(subtype: InputMethodSubtype!): Unit
```

Notify that the input method subtype is being changed in the same input method. 
This method must be called from the main thread of your app.

| Parameters ||
|---|---|
| `subtype` | [InputMethodSubtype](../android/view/inputmethod/InputMethodSubtype.md)!: New subtype of the notified input method |

### createSession

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun createSession(callback: InputMethod.SessionCallback!): Unit
```

Create a new `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession` that can be handed to client applications for interacting with the input method. You can later use `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#revokeSession(android.view.inputmethod.InputMethodSession)` to destroy the session so that it can no longer be used by any clients. 
This method must be called from the main thread of your app.

| Parameters ||
|---|---|
| `callback` | [InputMethod.SessionCallback](../android/view/inputmethod/InputMethod.SessionCallback.md)!: Interface that is called with the newly created session. |

### hideSoftInput

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun hideSoftInput(
    flags: Int, 
    resultReceiver: ResultReceiver!
): Unit
```

Request that any soft input part of the input method be hidden from the user. 
This method must be called from the main thread of your app.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Provides additional information about the hide request. Currently always 0. |
| `resultReceiver` | [ResultReceiver](../android/os/ResultReceiver.md)!: The client requesting the show may wish to be told the impact of their request, which should be supplied here. The result code should be `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#RESULT_UNCHANGED_SHOWN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#RESULT_UNCHANGED_HIDDEN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#RESULT_SHOWN:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#RESULT_HIDDEN:kotlin.Int`. |

### restartInput

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun restartInput(
    inputConnection: InputConnection!, 
    editorInfo: EditorInfo!
): Unit
```

This method is called when the state of this input method needs to be reset.

Typically, this method is called when the input focus is moved from one text box to another. 
This method must be called from the main thread of your app.

| Parameters ||
|---|---|
| `inputConnection` | [InputConnection](../android/view/inputmethod/InputConnection.md)!: Optional specific input connection for communicating with the text box; if null, you should use the generic bound input connection. |
| `editorInfo` | [EditorInfo](../android/view/inputmethod/EditorInfo.md)!: The attribute of the text box (typically, a EditText) that requests input. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo`

### revokeSession

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun revokeSession(session: InputMethodSession!): Unit
```

Disable and destroy a session that was previously created with `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#createSession(android.view.inputmethod.InputMethod.SessionCallback)`. After this call, the given session interface is no longer active and calls on it will fail. 
This method must be called from the main thread of your app.

| Parameters ||
|---|---|
| `session` | [InputMethodSession](../android/view/inputmethod/InputMethodSession.md)!: The `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession` previously provided through SessionCallback.sessionCreated() that is to be revoked. |

### setSessionEnabled

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setSessionEnabled(
    session: InputMethodSession!, 
    enabled: Boolean
): Unit
```

Control whether a particular input method session is active. 
This method must be called from the main thread of your app.

| Parameters ||
|---|---|
| `session` | [InputMethodSession](../android/view/inputmethod/InputMethodSession.md)!: The `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession` previously provided through SessionCallback.sessionCreated() that is to be changed. |

### showSoftInput

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun showSoftInput(
    flags: Int, 
    resultReceiver: ResultReceiver!
): Unit
```

Request that any soft input part of the input method be shown to the user. 
This method must be called from the main thread of your app.

| Parameters ||
|---|---|
| `resultReceiver` | [ResultReceiver](../android/os/ResultReceiver.md)!: The client requesting the show may wish to be told the impact of their request, which should be supplied here. The result code should be `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#RESULT_UNCHANGED_SHOWN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#RESULT_UNCHANGED_HIDDEN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#RESULT_SHOWN:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#RESULT_HIDDEN:kotlin.Int`. |

### startInput

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun startInput(
    inputConnection: InputConnection!, 
    editorInfo: EditorInfo!
): Unit
```

This method is called when the application starts to receive text and it is ready for this input method to process received events and send result text back to the application. 
This method must be called from the main thread of your app.

| Parameters ||
|---|---|
| `inputConnection` | [InputConnection](../android/view/inputmethod/InputConnection.md)!: Optional specific input connection for communicating with the text box; if null, you should use the generic bound input connection. |
| `editorInfo` | [EditorInfo](../android/view/inputmethod/EditorInfo.md)!: Information about the text box (typically, an EditText) that requests input. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo`

### unbindInput

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun unbindInput(): Unit
```

Unbind an application environment, called when the information previously set by `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod#bindInput(android.view.inputmethod.InputBinding)` is no longer valid for this input method.

Typically this method is called when the application changes to be non-foreground. 
This method must be called from the main thread of your app.
