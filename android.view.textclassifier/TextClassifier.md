Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextClassifier

```
interface TextClassifier
```

| [android.view.textclassifier.TextClassifier](TextClassifier.md) |

Interface for providing text classification related features.

The TextClassifier may be used to understand the meaning of text, as well as generating predicted next actions based on the text.

**NOTE:**Unless otherwise stated, methods of this interface are blocking operations. Call on a worker thread.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier.EntityConfig` Configuration object for specifying what entity types to identify. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#EXTRA_CLASSIFICATION_TIMEOUT_MS:kotlin.String` Extra indicating the classification timeout in milliseconds (as a `long`) allowed for this text classification request. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#EXTRA_FROM_TEXT_CLASSIFIER:kotlin.String` Extra that is included on activity intents coming from a TextClassifier when it suggests actions to its caller. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#EXTRA_OTP_TRUSTED_PACKAGES:kotlin.String` Extra specifying a list of trusted packages which can receive or view the OTP. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#EXTRA_TEXT_ORIGIN_PACKAGE:kotlin.String` Extra specifying the package name of the app from which the text to be classified originated. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#HINT_TEXT_IS_EDITABLE:kotlin.String` Designates that the text in question is editable. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#HINT_TEXT_IS_NOT_EDITABLE:kotlin.String` Designates that the text in question is not editable. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TIMEOUT_NO_TIMEOUT:kotlin.Long` Sentinel value for `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#EXTRA_CLASSIFICATION_TIMEOUT_MS:kotlin.String` indicating that there is no strict classification timeout (e.g. the UI renders suggestions asynchronously). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_ADDRESS:kotlin.String` Physical address. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_DATE:kotlin.String` Time reference that is no more specific than a date. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_DATE_TIME:kotlin.String` Time reference that includes a specific time. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_EMAIL:kotlin.String` E-mail address (e.g. "noreply@android.com"). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_FLIGHT_NUMBER:kotlin.String` Flight number in IATA format. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_OTHER:kotlin.String` The classifier ran, but didn't recognize a known entity. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_OTP:kotlin.String` Onetime password. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_PHONE:kotlin.String` Phone number (e.g. "555-123 456"). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_SMS_RETRIEVER_OTP:kotlin.String` SMS retriever OTP. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_SMS_WEB_OTP:kotlin.String` WebOTP SMS. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_UNKNOWN:kotlin.String` The TextClassifier failed to run. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_URL:kotlin.String` Web URL. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_CLIPBOARD:kotlin.String` The text classification context is for use with the system clipboard. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_CUSTOM_EDITTEXT:kotlin.String` The widget involved in the text classification context is a custom editable text widget. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_CUSTOM_TEXTVIEW:kotlin.String` The widget involved in the text classification context is a custom text widget. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_CUSTOM_UNSELECTABLE_TEXTVIEW:kotlin.String` The widget involved in the text classification context is a custom non-selectable text widget. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_EDITTEXT:kotlin.String` The widget involved in the text classification context is a standard `https://developer.android.com/reference/kotlin/android/widget/EditText.html#`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_EDIT_WEBVIEW:kotlin.String` The widget involved in the text classification context is a standard editable `https://developer.android.com/reference/kotlin/android/webkit/WebView.html#`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_NOTIFICATION:kotlin.String` The widget involved in the text classification context is a notification |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_TEXTVIEW:kotlin.String` The widget involved in the text classification context is a standard `https://developer.android.com/reference/kotlin/android/widget/TextView.html#`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_UNKNOWN:kotlin.String` The widget involved in the text classification context is of an unknown/unspecified type. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_UNSELECTABLE_TEXTVIEW:kotlin.String` The widget involved in the text classification context is a standard non-selectable `https://developer.android.com/reference/kotlin/android/widget/TextView.html#`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#WIDGET_TYPE_WEBVIEW:kotlin.String` The widget involved in the text classification context is a standard `https://developer.android.com/reference/kotlin/android/webkit/WebView.html#`. |
| --- | --- |

| Public methods ||
|---|---|
| open [TextClassification](TextClassification.md) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#classifyText(android.view.textclassifier.TextClassification.Request)(request: https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification.Request)` Classifies the specified text and returns a `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification` object that can be used to generate a widget for handling the classified text. |
| open [TextClassification](TextClassification.md) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#classifyText(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20android.os.LocaleList)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, startIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, endIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, defaultLocales: https://developer.android.com/reference/kotlin/android/os/LocaleList.html#?)` Classifies the specified text and returns a `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification` object that can be used to generate a widget for handling the classified text. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#destroy()()` Destroys this TextClassifier. |
| --- | --- |
| open [TextLanguage](TextLanguage.md) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#detectLanguage(android.view.textclassifier.TextLanguage.Request)(request: https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLanguage.Request)` Detects the language of the text in the given request. |
| open [TextLinks](TextLinks.md) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#generateLinks(android.view.textclassifier.TextLinks.Request)(request: https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks.Request)` Generates and returns a `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks` that may be applied to the text to annotate it with links information. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#getMaxGenerateLinksTextLength()()` Returns the maximal length of text that can be processed by generateLinks. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#isDestroyed()()` Returns whether or not this TextClassifier has been destroyed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#onSelectionEvent(android.view.textclassifier.SelectionEvent)(event: https://developer.android.com/reference/kotlin/android/view/textclassifier/SelectionEvent)` **NOTE:** Use `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#onTextClassifierEvent(android.view.textclassifier.TextClassifierEvent)` instead. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#onTextClassifierEvent(android.view.textclassifier.TextClassifierEvent)(event: https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifierEvent)` Reports a text classifier event. |
| --- | --- |
| open [ConversationActions](ConversationActions.md) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#suggestConversationActions(android.view.textclassifier.ConversationActions.Request)(request: https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationActions.Request)` Suggests and returns a list of actions according to the given conversation. |
| open [TextSelection](TextSelection.md) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#suggestSelection(android.view.textclassifier.TextSelection.Request)(request: https://developer.android.com/reference/kotlin/android/view/textclassifier/TextSelection.Request)` Returns suggested text selection start and end indices, recognized entity types, and their associated confidence scores. |
| open [TextSelection](TextSelection.md) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#suggestSelection(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20android.os.LocaleList)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, selectionStartIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, selectionEndIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, defaultLocales: https://developer.android.com/reference/kotlin/android/os/LocaleList.html#?)` Returns suggested text selection start and end indices, recognized entity types, and their associated confidence scores. |
| --- | --- |

| Properties ||
|---|---|
| static [TextClassifier](TextClassifier.md)! | `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#NO_OP:android.view.textclassifier.TextClassifier` No-op TextClassifier. |

## Constants

### EXTRA_CLASSIFICATION_TIMEOUT_MS

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CLASSIFICATION_TIMEOUT_MS: String
```

Extra indicating the classification timeout in milliseconds (as a `long`) allowed for this text classification request.

If this extra is missing, the timeout is unknown (legacy caller). If this extra is set to `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TIMEOUT_NO_TIMEOUT:kotlin.Long` (0L), there is no strict timeout and results may arrive asynchronously without causing UI blocking or layout shifts. If set to a positive number, it indicates the timeout budget in milliseconds.

 Value: "android.view.textclassifier.extra.CLASSIFICATION_TIMEOUT_MS"

### EXTRA_FROM_TEXT_CLASSIFIER

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_FROM_TEXT_CLASSIFIER: String
```

Extra that is included on activity intents coming from a TextClassifier when it suggests actions to its caller.

All `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#` implementations should make sure this extra exists in their generated intents.

 Value: "android.view.textclassifier.extra.FROM_TEXT_CLASSIFIER"

### EXTRA_OTP_TRUSTED_PACKAGES

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_OTP_TRUSTED_PACKAGES: String
```

Extra specifying a list of trusted packages which can receive or view the OTP.

 Value: "android.view.textclassifier.extra.OTP_TRUSTED_PACKAGES"

### EXTRA_TEXT_ORIGIN_PACKAGE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_TEXT_ORIGIN_PACKAGE: String
```

Extra specifying the package name of the app from which the text to be classified originated. For example, a notification assistant might use TextClassifier, but the notification content could originate from a different app. This key allows you to provide the package name of that source app.

 Value: "android.view.textclassifier.extra.TEXT_ORIGIN_PACKAGE"

### HINT_TEXT_IS_EDITABLE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HINT_TEXT_IS_EDITABLE: String
```

Designates that the text in question is editable. \*

 Value: "android.text_is_editable"

### HINT_TEXT_IS_NOT_EDITABLE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HINT_TEXT_IS_NOT_EDITABLE: String
```

Designates that the text in question is not editable. \*

 Value: "android.text_is_not_editable"

### TIMEOUT_NO_TIMEOUT

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TIMEOUT_NO_TIMEOUT: Long
```

Sentinel value for `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#EXTRA_CLASSIFICATION_TIMEOUT_MS:kotlin.String` indicating that there is no strict classification timeout (e.g. the UI renders suggestions asynchronously).

 Value: 0L

### TYPE_ADDRESS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_ADDRESS: String
```

Physical address.

 Value: "address"

### TYPE_DATE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_DATE: String
```

Time reference that is no more specific than a date. May be absolute such as "01/01/2000" or relative like "tomorrow". \*

 Value: "date"

### TYPE_DATE_TIME

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_DATE_TIME: String
```

Time reference that includes a specific time. May be absolute such as "01/01/2000 5:30pm" or relative like "tomorrow at 5:30pm". \*

 Value: "datetime"

### TYPE_EMAIL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_EMAIL: String
```

E-mail address (e.g. "noreply@android.com").

 Value: "email"

### TYPE_FLIGHT_NUMBER

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_FLIGHT_NUMBER: String
```

Flight number in IATA format.

 Value: "flight"

### TYPE_OTHER

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_OTHER: String
```

The classifier ran, but didn't recognize a known entity.

 Value: "other"

### TYPE_OTP

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_OTP: String
```

Onetime password.

 Value: "otp"

### TYPE_PHONE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_PHONE: String
```

Phone number (e.g. "555-123 456").

 Value: "phone"

### TYPE_SMS_RETRIEVER_OTP

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_SMS_RETRIEVER_OTP: String
```

SMS retriever OTP.

 Value: "sms_retriever_otp"

### TYPE_SMS_WEB_OTP

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_SMS_WEB_OTP: String
```

WebOTP SMS.

 Value: "sms_web_otp"

### TYPE_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_UNKNOWN: String
```

The TextClassifier failed to run.

 Value: ""

### TYPE_URL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_URL: String
```

Web URL.

 Value: "url"

### WIDGET_TYPE_CLIPBOARD

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIDGET_TYPE_CLIPBOARD: String
```

The text classification context is for use with the system clipboard.

 Value: "clipboard"

### WIDGET_TYPE_CUSTOM_EDITTEXT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIDGET_TYPE_CUSTOM_EDITTEXT: String
```

The widget involved in the text classification context is a custom editable text widget.

 Value: "customedit"

### WIDGET_TYPE_CUSTOM_TEXTVIEW

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIDGET_TYPE_CUSTOM_TEXTVIEW: String
```

The widget involved in the text classification context is a custom text widget.

 Value: "customview"

### WIDGET_TYPE_CUSTOM_UNSELECTABLE_TEXTVIEW

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIDGET_TYPE_CUSTOM_UNSELECTABLE_TEXTVIEW: String
```

The widget involved in the text classification context is a custom non-selectable text widget.

 Value: "nosel-customview"

### WIDGET_TYPE_EDITTEXT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIDGET_TYPE_EDITTEXT: String
```

The widget involved in the text classification context is a standard `https://developer.android.com/reference/kotlin/android/widget/EditText.html#`.

 Value: "edittext"

### WIDGET_TYPE_EDIT_WEBVIEW

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIDGET_TYPE_EDIT_WEBVIEW: String
```

The widget involved in the text classification context is a standard editable `https://developer.android.com/reference/kotlin/android/webkit/WebView.html#`.

 Value: "edit-webview"

### WIDGET_TYPE_NOTIFICATION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIDGET_TYPE_NOTIFICATION: String
```

The widget involved in the text classification context is a notification

 Value: "notification"

### WIDGET_TYPE_TEXTVIEW

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIDGET_TYPE_TEXTVIEW: String
```

The widget involved in the text classification context is a standard `https://developer.android.com/reference/kotlin/android/widget/TextView.html#`.

 Value: "textview"

### WIDGET_TYPE_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIDGET_TYPE_UNKNOWN: String
```

The widget involved in the text classification context is of an unknown/unspecified type.

 Value: "unknown"

### WIDGET_TYPE_UNSELECTABLE_TEXTVIEW

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIDGET_TYPE_UNSELECTABLE_TEXTVIEW: String
```

The widget involved in the text classification context is a standard non-selectable `https://developer.android.com/reference/kotlin/android/widget/TextView.html#`.

 Value: "nosel-textview"

### WIDGET_TYPE_WEBVIEW

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WIDGET_TYPE_WEBVIEW: String
```

The widget involved in the text classification context is a standard `https://developer.android.com/reference/kotlin/android/webkit/WebView.html#`.

 Value: "webview"

## Public methods

### classifyText

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun classifyText(request: TextClassification.Request): TextClassification
```

Classifies the specified text and returns a `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification` object that can be used to generate a widget for handling the classified text.

**NOTE:**Call on a worker thread.

**NOTE:** If a TextClassifier has been destroyed, calls to this method should throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`. See `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#isDestroyed()`. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `request` | [TextClassification.Request](../android/view/textclassifier/TextClassification.Request.md): the text classification request. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification` | This value cannot be `null`. |

### classifyText

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun classifyText(
    text: CharSequence, 
    startIndex: Int, 
    endIndex: Int, 
    defaultLocales: LocaleList?
): TextClassification
```

Classifies the specified text and returns a `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification` object that can be used to generate a widget for handling the classified text.

**NOTE:**Call on a worker thread.

**NOTE:** Do not implement. The default implementation of this method calls `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#classifyText(android.view.textclassifier.TextClassification.Request)`. If that method calls this method, a stack overflow error will happen.

**NOTE:** If a TextClassifier has been destroyed, calls to this method should throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`. See `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#isDestroyed()`. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): text providing context for the text to classify (which is specified by the sub sequence starting at startIndex and ending at endIndex). This value cannot be `null`. |
| `startIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): start index of the text to classify. Value is 0 or greater |
| `endIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): end index of the text to classify. Value is 0 or greater |
| --- | --- |
| `defaultLocales` | [LocaleList](../android.os/LocaleList.md)?: ordered list of locale preferences that may be used to disambiguate the provided text. If no locale preferences exist, set this to null or an empty locale list. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if text is null; startIndex is negative; endIndex is greater than text.length() or not greater than startIndex |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#classifyText(android.view.textclassifier.TextClassification.Request)`

### destroy

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun destroy(): Unit
```

Destroys this TextClassifier.

**NOTE:** If a TextClassifier has been destroyed, calls to its methods should throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`. See `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#isDestroyed()`.

Subsequent calls to this method are no-ops.

### detectLanguage

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun detectLanguage(request: TextLanguage.Request): TextLanguage
```

Detects the language of the text in the given request.

**NOTE:**Call on a worker thread.

**NOTE:** If a TextClassifier has been destroyed, calls to this method should throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`. See `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#isDestroyed()`. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `request` | [TextLanguage.Request](../android/view/textclassifier/TextLanguage.Request.md): the `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLanguage` request. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLanguage` | the `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLanguage` result. This value cannot be `null`. |

### generateLinks

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun generateLinks(request: TextLinks.Request): TextLinks
```

Generates and returns a `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks` that may be applied to the text to annotate it with links information.

**NOTE:**Call on a worker thread.

**NOTE:** If a TextClassifier has been destroyed, calls to this method should throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`. See `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#isDestroyed()`. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `request` | [TextLinks.Request](../android/view/textclassifier/TextLinks.Request.md): the text links request. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#getMaxGenerateLinksTextLength()`

### getMaxGenerateLinksTextLength

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMaxGenerateLinksTextLength(): Int
```

Returns the maximal length of text that can be processed by generateLinks.

**NOTE:** If a TextClassifier has been destroyed, calls to this method should throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`. See `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#isDestroyed()`. 
This method may take several seconds to complete, so it should only be called from a worker thread.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#generateLinks(android.view.textclassifier.TextLinks.Request)`

### isDestroyed

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDestroyed(): Boolean
```

Returns whether or not this TextClassifier has been destroyed.

**NOTE:** If a TextClassifier has been destroyed, caller should not interact with the classifier and an attempt to do so would throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`. However, this method should never throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#destroy()`

### onSelectionEvent

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onSelectionEvent(event: SelectionEvent): Unit
```

**NOTE:** Use `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#onTextClassifierEvent(android.view.textclassifier.TextClassifierEvent)` instead.

Reports a selection event.

**NOTE:** If a TextClassifier has been destroyed, calls to this method should throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`. See `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#isDestroyed()`.

| Parameters ||
|---|---|
| `event` | [SelectionEvent](SelectionEvent.md): This value cannot be `null`. |

### onTextClassifierEvent

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onTextClassifierEvent(event: TextClassifierEvent): Unit
```

Reports a text classifier event.

**NOTE:**Call on a worker thread.

| Parameters ||
|---|---|
| `event` | [TextClassifierEvent](TextClassifierEvent.md): This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this TextClassifier has been destroyed. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#isDestroyed()`

### suggestConversationActions

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun suggestConversationActions(request: ConversationActions.Request): ConversationActions
```

Suggests and returns a list of actions according to the given conversation. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `request` | [ConversationActions.Request](../android/view/textclassifier/ConversationActions.Request.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationActions` | This value cannot be `null`. |

### suggestSelection

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun suggestSelection(request: TextSelection.Request): TextSelection
```

Returns suggested text selection start and end indices, recognized entity types, and their associated confidence scores. The entity types are ordered from highest to lowest scoring.

**NOTE:**Call on a worker thread.

**NOTE:** If a TextClassifier has been destroyed, calls to this method should throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`. See `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#isDestroyed()`. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `request` | [TextSelection.Request](../android/view/textclassifier/TextSelection.Request.md): the text selection request. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextSelection` | This value cannot be `null`. |

### suggestSelection

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun suggestSelection(
    text: CharSequence, 
    selectionStartIndex: Int, 
    selectionEndIndex: Int, 
    defaultLocales: LocaleList?
): TextSelection
```

Returns suggested text selection start and end indices, recognized entity types, and their associated confidence scores. The entity types are ordered from highest to lowest scoring.

**NOTE:**Call on a worker thread.

**NOTE:** If a TextClassifier has been destroyed, calls to this method should throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`. See `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#isDestroyed()`.

**NOTE:** Do not implement. The default implementation of this method calls `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#suggestSelection(android.view.textclassifier.TextSelection.Request)`. If that method calls this method, a stack overflow error will happen. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): text providing context for the selected text (which is specified by the sub sequence starting at selectionStartIndex and ending at selectionEndIndex). This value cannot be `null`. |
| `selectionStartIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): start index of the selected part of text. Value is 0 or greater |
| `selectionEndIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): end index of the selected part of text. Value is 0 or greater |
| --- | --- |
| `defaultLocales` | [LocaleList](../android.os/LocaleList.md)?: ordered list of locale preferences that may be used to disambiguate the provided text. If no locale preferences exist, set this to null or an empty locale list. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextSelection` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if text is null; selectionStartIndex is negative; selectionEndIndex is greater than text.length() or not greater than selectionStartIndex |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#suggestSelection(android.view.textclassifier.TextSelection.Request)`

## Properties

### NO_OP

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NO_OP: TextClassifier!
```

No-op TextClassifier. This may be used to turn off TextClassifier features.
