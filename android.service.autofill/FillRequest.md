# FillRequest

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FillRequest

Kotlin| [Java](https://developer.android.com/reference/android/service/autofill/FillRequest "View this page in Java") 
| --- | --- |

```
class FillRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.autofill.FillRequest](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#) |

This class represents a request to an autofill service to interpret the screen and provide information to the system which views are interesting for saving and what are the possible ways to fill the inputs on the screen if applicable.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_COMPATIBILITY_MODE_REQUEST](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#FLAG_COMPATIBILITY_MODE_REQUEST:kotlin.Int) Indicates this request was made using [compatibility mode](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#CompatibilityMode). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_MANUAL_REQUEST](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#FLAG_MANUAL_REQUEST:kotlin.Int) Indicates autofill was explicitly requested by the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_SUPPORTS_FILL_DIALOG](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#FLAG_SUPPORTS_FILL_DIALOG:kotlin.Int) Indicates the request supports fill dialog presentation for the fields, the system will send the request when the activity just started. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#describeContents())`()` <br /> |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | [getClientState](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#getClientState())`()` Gets the latest client state bundle set by the service in a [fill response](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse.Builder#setClientState(android.os.Bundle)). |
| [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#)? | [getDelayedFillIntentSender](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#getDelayedFillIntentSender())`()` Gets the [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#) to send a delayed fill response. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [FillContext](https://developer.android.com/reference/kotlin/android/service/autofill/FillContext)!\> | [getFillContexts](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#getFillContexts())`()` Gets the contexts associated with each previous fill request. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFlags](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#getFlags())`()` Gets the flags associated with this request. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getHints](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#getHints())`()` Sends a list of datatypes for the Autofill Provider. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#getId())`()` Gets the unique id of this request. |
| [InlineSuggestionsRequest](https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestionsRequest.html#)? | [getInlineSuggestionsRequest](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#getInlineSuggestionsRequest())`()` Gets the [InlineSuggestionsRequest](https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestionsRequest.html#) associated with this request. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#toString())`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [FillRequest](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### FLAG_COMPATIBILITY_MODE_REQUEST

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_COMPATIBILITY_MODE_REQUEST: Int
```

Indicates this request was made using [compatibility mode](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#CompatibilityMode). 
Value is either`0`or a combination of [android.service.autofill.FillRequest#FLAG_MANUAL_REQUEST](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#FLAG_MANUAL_REQUEST:kotlin.Int), [android.service.autofill.FillRequest#FLAG_COMPATIBILITY_MODE_REQUEST](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#FLAG_COMPATIBILITY_MODE_REQUEST:kotlin.Int), android.service.autofill.FillRequest.FLAG_PASSWORD_INPUT_TYPE, android.service.autofill.FillRequest.FLAG_VIEW_NOT_FOCUSED, [android.service.autofill.FillRequest#FLAG_SUPPORTS_FILL_DIALOG](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#FLAG_SUPPORTS_FILL_DIALOG:kotlin.Int), android.service.autofill.FillRequest.FLAG_IME_SHOWING, android.service.autofill.FillRequest.FLAG_RESET_FILL_DIALOG_STATE, android.service.autofill.FillRequest.FLAG_PCC_DETECTION, android.service.autofill.FillRequest.FLAG_SCREEN_HAS_CREDMAN_FIELD, and android.service.autofill.FillRequest.FLAG_VIEW_REQUESTS_CREDMAN_SERVICE 

 Value: 2

### FLAG_MANUAL_REQUEST

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_MANUAL_REQUEST: Int
```

Indicates autofill was explicitly requested by the user.

Users typically make an explicit request to autofill a screen in two situations:

- The app disabled autofill (using [View.setImportantForAutofill(int)](https://developer.android.com/reference/kotlin/android/view/View.html#setImportantForAutofill(kotlin.Int)).
- The service could not figure out how to autofill a screen (but the user knows the service has data for that app).

This flag is particularly useful for the second case. For example, the service could offer a complex UI where the user can map which screen views belong to each user data, or it could offer a simpler UI where the user picks the data for just the view used to trigger the request (that would be the view whose [android.app.assist.AssistStructure.ViewNode#isFocused()](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure.ViewNode.html#isFocused())method returns`true`).

An explicit autofill request is triggered when the [android.view.autofill.AutofillManager#requestAutofill(View)](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager.html#requestAutofill(android.view.View))or [android.view.autofill.AutofillManager#requestAutofill(View, int, android.graphics.Rect)](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager.html#requestAutofill(android.view.View,%20kotlin.Int,%20android.graphics.Rect))is called. For example, standard [android.widget.TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#) views show an`AUTOFILL`option in the overflow menu that triggers such request. 
Value is either`0`or a combination of [android.service.autofill.FillRequest#FLAG_MANUAL_REQUEST](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#FLAG_MANUAL_REQUEST:kotlin.Int), [android.service.autofill.FillRequest#FLAG_COMPATIBILITY_MODE_REQUEST](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#FLAG_COMPATIBILITY_MODE_REQUEST:kotlin.Int), android.service.autofill.FillRequest.FLAG_PASSWORD_INPUT_TYPE, android.service.autofill.FillRequest.FLAG_VIEW_NOT_FOCUSED, [android.service.autofill.FillRequest#FLAG_SUPPORTS_FILL_DIALOG](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#FLAG_SUPPORTS_FILL_DIALOG:kotlin.Int), android.service.autofill.FillRequest.FLAG_IME_SHOWING, android.service.autofill.FillRequest.FLAG_RESET_FILL_DIALOG_STATE, android.service.autofill.FillRequest.FLAG_PCC_DETECTION, android.service.autofill.FillRequest.FLAG_SCREEN_HAS_CREDMAN_FIELD, and android.service.autofill.FillRequest.FLAG_VIEW_REQUESTS_CREDMAN_SERVICE 

 Value: 1

### FLAG_SUPPORTS_FILL_DIALOG

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_SUPPORTS_FILL_DIALOG: Int
```

**Deprecated:** *All requests would support fill dialog by default. Presence of this flag isn't needed.*

Indicates the request supports fill dialog presentation for the fields, the system will send the request when the activity just started. 
Value is either`0`or a combination of [android.service.autofill.FillRequest#FLAG_MANUAL_REQUEST](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#FLAG_MANUAL_REQUEST:kotlin.Int), [android.service.autofill.FillRequest#FLAG_COMPATIBILITY_MODE_REQUEST](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#FLAG_COMPATIBILITY_MODE_REQUEST:kotlin.Int), android.service.autofill.FillRequest.FLAG_PASSWORD_INPUT_TYPE, android.service.autofill.FillRequest.FLAG_VIEW_NOT_FOCUSED, [android.service.autofill.FillRequest#FLAG_SUPPORTS_FILL_DIALOG](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#FLAG_SUPPORTS_FILL_DIALOG:kotlin.Int), android.service.autofill.FillRequest.FLAG_IME_SHOWING, android.service.autofill.FillRequest.FLAG_RESET_FILL_DIALOG_STATE, android.service.autofill.FillRequest.FLAG_PCC_DETECTION, android.service.autofill.FillRequest.FLAG_SCREEN_HAS_CREDMAN_FIELD, and android.service.autofill.FillRequest.FLAG_VIEW_REQUESTS_CREDMAN_SERVICE 

 Value: 64

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getClientState

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClientState(): Bundle?
```

Gets the latest client state bundle set by the service in a [fill response](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse.Builder#setClientState(android.os.Bundle)).

**Note:** Prior to Android [android.os.Build.VERSION_CODES#P](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int), only client state bundles set by [FillResponse.Builder.setClientState(Bundle)](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse.Builder#setClientState(android.os.Bundle))were considered. On Android [android.os.Build.VERSION_CODES#P](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int) and higher, bundles set in the result of an authenticated request through the [android.view.autofill.AutofillManager#EXTRA_CLIENT_STATE](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager.html#EXTRA_CLIENT_STATE:kotlin.String) extra are also considered (and take precedence when set).

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | The client state. This value may be`null`. |

### getDelayedFillIntentSender

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDelayedFillIntentSender(): IntentSender?
```

Gets the [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#) to send a delayed fill response.

The autofill service must first indicate that it wants to return a delayed [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse) by setting [FillResponse.FLAG_DELAY_FILL](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse#FLAG_DELAY_FILL:kotlin.Int) in a successful fill response. Then it can use this IntentSender to send an Intent with extra [AutofillService.EXTRA_FILL_RESPONSE](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#EXTRA_FILL_RESPONSE:kotlin.String) with the delayed response.

Note that this may be null if a delayed fill response is not supported for this fill request. 

### getFillContexts

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFillContexts(): MutableList<FillContext!>
```

Gets the contexts associated with each previous fill request.

**Note:** Starting on Android [android.os.Build.VERSION_CODES#Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int), it could also include contexts from requests whose [SaveInfo](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo) had the [SaveInfo.FLAG_DELAY_SAVE](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#FLAG_DELAY_SAVE:kotlin.Int) flag.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [FillContext](https://developer.android.com/reference/kotlin/android/service/autofill/FillContext)!> | This value cannot be`null`. |

### getFlags

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFlags(): Int
```

Gets the flags associated with this request.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | any combination of [FLAG_MANUAL_REQUEST](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#FLAG_MANUAL_REQUEST:kotlin.Int), [FLAG_SUPPORTS_FILL_DIALOG](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#FLAG_SUPPORTS_FILL_DIALOG:kotlin.Int) and [FLAG_COMPATIBILITY_MODE_REQUEST](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#FLAG_COMPATIBILITY_MODE_REQUEST:kotlin.Int). Value is either`0`or a combination of [android.service.autofill.FillRequest#FLAG_MANUAL_REQUEST](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#FLAG_MANUAL_REQUEST:kotlin.Int), [android.service.autofill.FillRequest#FLAG_COMPATIBILITY_MODE_REQUEST](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#FLAG_COMPATIBILITY_MODE_REQUEST:kotlin.Int), android.service.autofill.FillRequest.FLAG_PASSWORD_INPUT_TYPE, android.service.autofill.FillRequest.FLAG_VIEW_NOT_FOCUSED, [android.service.autofill.FillRequest#FLAG_SUPPORTS_FILL_DIALOG](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#FLAG_SUPPORTS_FILL_DIALOG:kotlin.Int), android.service.autofill.FillRequest.FLAG_IME_SHOWING, android.service.autofill.FillRequest.FLAG_RESET_FILL_DIALOG_STATE, android.service.autofill.FillRequest.FLAG_PCC_DETECTION, android.service.autofill.FillRequest.FLAG_SCREEN_HAS_CREDMAN_FIELD, and android.service.autofill.FillRequest.FLAG_VIEW_REQUESTS_CREDMAN_SERVICE |

### getHints

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHints(): MutableList<String!>
```

Sends a list of datatypes for the Autofill Provider. If this is populated, Autofill Provider should return data for the autofill hints requested here, even though the Autofill Provider may not have detected these types. The hints would be part of HintConstants: https://developer.android.com/reference/androidx/autofill/HintConstants This is populated if the platform's field detection is enabled.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. |

### getId

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): Int
```

Gets the unique id of this request. 

### getInlineSuggestionsRequest

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInlineSuggestionsRequest(): InlineSuggestionsRequest?
```

Gets the [InlineSuggestionsRequest](https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestionsRequest.html#) associated with this request.

Autofill Framework will send a`@non-null` [InlineSuggestionsRequest](https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestionsRequest.html#) if currently inline suggestions are supported and can be displayed. If the Autofill service wants to show inline suggestions, they may return [Dataset](https://developer.android.com/reference/kotlin/android/service/autofill/Dataset) with valid [InlinePresentation](https://developer.android.com/reference/kotlin/android/service/autofill/InlinePresentation).

The Autofill Service must set supportsInlineSuggestions in its XML to enable support for inline suggestions.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------|--------------------|
| [InlineSuggestionsRequest](https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestionsRequest.html#)? | the suggestionspec |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<FillRequest!>
```
