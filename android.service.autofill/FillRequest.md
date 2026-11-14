# FillRequest

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FillRequest

Kotlin| [Java](../android/service/autofill/FillRequest.md) 
| --- | --- |

```
class FillRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.autofill.FillRequest](../android/service/autofill/FillRequest.md) |

This class represents a request to an autofill service to interpret the screen and provide information to the system which views are interesting for saving and what are the possible ways to fill the inputs on the screen if applicable.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_COMPATIBILITY_MODE_REQUEST](../android/service/autofill/FillRequest.md) Indicates this request was made using [compatibility mode](../android/service/autofill/AutofillService.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_MANUAL_REQUEST](../android/service/autofill/FillRequest.md) Indicates autofill was explicitly requested by the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_SUPPORTS_FILL_DIALOG](../android/service/autofill/FillRequest.md) Indicates the request supports fill dialog presentation for the fields, the system will send the request when the activity just started. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/service/autofill/FillRequest.md))`()` <br /> |
| [Bundle](../android/os/Bundle.md)? | [getClientState](../android/service/autofill/FillRequest.md))`()` Gets the latest client state bundle set by the service in a [fill response](../android/service/autofill/FillResponse.Builder.md)). |
| [IntentSender](../android/content/IntentSender.md)? | [getDelayedFillIntentSender](../android/service/autofill/FillRequest.md))`()` Gets the [IntentSender](../android/content/IntentSender.md) to send a delayed fill response. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [FillContext](../android/service/autofill/FillContext.md)!\> | [getFillContexts](../android/service/autofill/FillRequest.md))`()` Gets the contexts associated with each previous fill request. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFlags](../android/service/autofill/FillRequest.md))`()` Gets the flags associated with this request. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getHints](../android/service/autofill/FillRequest.md))`()` Sends a list of datatypes for the Autofill Provider. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](../android/service/autofill/FillRequest.md))`()` Gets the unique id of this request. |
| [InlineSuggestionsRequest](../android/view/inputmethod/InlineSuggestionsRequest.md)? | [getInlineSuggestionsRequest](../android/service/autofill/FillRequest.md))`()` Gets the [InlineSuggestionsRequest](../android/view/inputmethod/InlineSuggestionsRequest.md) associated with this request. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/service/autofill/FillRequest.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/service/autofill/FillRequest.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [FillRequest](../android/service/autofill/FillRequest.md)!\> | [CREATOR](../android/service/autofill/FillRequest.md) <br /> |

## Constants

### FLAG_COMPATIBILITY_MODE_REQUEST

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_COMPATIBILITY_MODE_REQUEST: Int
```

Indicates this request was made using [compatibility mode](../android/service/autofill/AutofillService.md). 
Value is either`0`or a combination of [android.service.autofill.FillRequest#FLAG_MANUAL_REQUEST](../android/service/autofill/FillRequest.md), [android.service.autofill.FillRequest#FLAG_COMPATIBILITY_MODE_REQUEST](../android/service/autofill/FillRequest.md), android.service.autofill.FillRequest.FLAG_PASSWORD_INPUT_TYPE, android.service.autofill.FillRequest.FLAG_VIEW_NOT_FOCUSED, [android.service.autofill.FillRequest#FLAG_SUPPORTS_FILL_DIALOG](../android/service/autofill/FillRequest.md), android.service.autofill.FillRequest.FLAG_IME_SHOWING, android.service.autofill.FillRequest.FLAG_RESET_FILL_DIALOG_STATE, android.service.autofill.FillRequest.FLAG_PCC_DETECTION, android.service.autofill.FillRequest.FLAG_SCREEN_HAS_CREDMAN_FIELD, and android.service.autofill.FillRequest.FLAG_VIEW_REQUESTS_CREDMAN_SERVICE 

 Value: 2

### FLAG_MANUAL_REQUEST

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_MANUAL_REQUEST: Int
```

Indicates autofill was explicitly requested by the user.

Users typically make an explicit request to autofill a screen in two situations:

- The app disabled autofill (using [View.setImportantForAutofill(int)](../android/view/View.md)).
- The service could not figure out how to autofill a screen (but the user knows the service has data for that app).

This flag is particularly useful for the second case. For example, the service could offer a complex UI where the user can map which screen views belong to each user data, or it could offer a simpler UI where the user picks the data for just the view used to trigger the request (that would be the view whose [android.app.assist.AssistStructure.ViewNode#isFocused()](../android/app/assist/AssistStructure.ViewNode.md))method returns`true`).

An explicit autofill request is triggered when the [android.view.autofill.AutofillManager#requestAutofill(View)](../android/view/autofill/AutofillManager.md))or [android.view.autofill.AutofillManager#requestAutofill(View, int, android.graphics.Rect)](../android/view/autofill/AutofillManager.md))is called. For example, standard [android.widget.TextView](../android/widget/TextView.md) views show an`AUTOFILL`option in the overflow menu that triggers such request. 
Value is either`0`or a combination of [android.service.autofill.FillRequest#FLAG_MANUAL_REQUEST](../android/service/autofill/FillRequest.md), [android.service.autofill.FillRequest#FLAG_COMPATIBILITY_MODE_REQUEST](../android/service/autofill/FillRequest.md), android.service.autofill.FillRequest.FLAG_PASSWORD_INPUT_TYPE, android.service.autofill.FillRequest.FLAG_VIEW_NOT_FOCUSED, [android.service.autofill.FillRequest#FLAG_SUPPORTS_FILL_DIALOG](../android/service/autofill/FillRequest.md), android.service.autofill.FillRequest.FLAG_IME_SHOWING, android.service.autofill.FillRequest.FLAG_RESET_FILL_DIALOG_STATE, android.service.autofill.FillRequest.FLAG_PCC_DETECTION, android.service.autofill.FillRequest.FLAG_SCREEN_HAS_CREDMAN_FIELD, and android.service.autofill.FillRequest.FLAG_VIEW_REQUESTS_CREDMAN_SERVICE 

 Value: 1

### FLAG_SUPPORTS_FILL_DIALOG

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_SUPPORTS_FILL_DIALOG: Int
```

**Deprecated:** *All requests would support fill dialog by default. Presence of this flag isn't needed.*

Indicates the request supports fill dialog presentation for the fields, the system will send the request when the activity just started. 
Value is either`0`or a combination of [android.service.autofill.FillRequest#FLAG_MANUAL_REQUEST](../android/service/autofill/FillRequest.md), [android.service.autofill.FillRequest#FLAG_COMPATIBILITY_MODE_REQUEST](../android/service/autofill/FillRequest.md), android.service.autofill.FillRequest.FLAG_PASSWORD_INPUT_TYPE, android.service.autofill.FillRequest.FLAG_VIEW_NOT_FOCUSED, [android.service.autofill.FillRequest#FLAG_SUPPORTS_FILL_DIALOG](../android/service/autofill/FillRequest.md), android.service.autofill.FillRequest.FLAG_IME_SHOWING, android.service.autofill.FillRequest.FLAG_RESET_FILL_DIALOG_STATE, android.service.autofill.FillRequest.FLAG_PCC_DETECTION, android.service.autofill.FillRequest.FLAG_SCREEN_HAS_CREDMAN_FIELD, and android.service.autofill.FillRequest.FLAG_VIEW_REQUESTS_CREDMAN_SERVICE 

 Value: 64

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getClientState

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClientState(): Bundle?
```

Gets the latest client state bundle set by the service in a [fill response](../android/service/autofill/FillResponse.Builder.md)).

**Note:** Prior to Android [android.os.Build.VERSION_CODES#P](../android/os/Build.VERSION_CODES.md), only client state bundles set by [FillResponse.Builder.setClientState(Bundle)](../android/service/autofill/FillResponse.Builder.md))were considered. On Android [android.os.Build.VERSION_CODES#P](../android/os/Build.VERSION_CODES.md) and higher, bundles set in the result of an authenticated request through the [android.view.autofill.AutofillManager#EXTRA_CLIENT_STATE](../android/view/autofill/AutofillManager.md) extra are also considered (and take precedence when set).

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------|
| [Bundle](../android/os/Bundle.md)? | The client state. This value may be`null`. |

### getDelayedFillIntentSender

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDelayedFillIntentSender(): IntentSender?
```

Gets the [IntentSender](../android/content/IntentSender.md) to send a delayed fill response.

The autofill service must first indicate that it wants to return a delayed [FillResponse](../android/service/autofill/FillResponse.md) by setting [FillResponse.FLAG_DELAY_FILL](../android/service/autofill/FillResponse.md) in a successful fill response. Then it can use this IntentSender to send an Intent with extra [AutofillService.EXTRA_FILL_RESPONSE](../android/service/autofill/AutofillService.md) with the delayed response.

Note that this may be null if a delayed fill response is not supported for this fill request. 

### getFillContexts

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFillContexts(): MutableList<FillContext!>
```

Gets the contexts associated with each previous fill request.

**Note:** Starting on Android [android.os.Build.VERSION_CODES#Q](../android/os/Build.VERSION_CODES.md), it could also include contexts from requests whose [SaveInfo](../android/service/autofill/SaveInfo.md) had the [SaveInfo.FLAG_DELAY_SAVE](../android/service/autofill/SaveInfo.md) flag.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [FillContext](../android/service/autofill/FillContext.md)!> | This value cannot be`null`. |

### getFlags

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFlags(): Int
```

Gets the flags associated with this request.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | any combination of [FLAG_MANUAL_REQUEST](../android/service/autofill/FillRequest.md), [FLAG_SUPPORTS_FILL_DIALOG](../android/service/autofill/FillRequest.md) and [FLAG_COMPATIBILITY_MODE_REQUEST](../android/service/autofill/FillRequest.md). Value is either`0`or a combination of [android.service.autofill.FillRequest#FLAG_MANUAL_REQUEST](../android/service/autofill/FillRequest.md), [android.service.autofill.FillRequest#FLAG_COMPATIBILITY_MODE_REQUEST](../android/service/autofill/FillRequest.md), android.service.autofill.FillRequest.FLAG_PASSWORD_INPUT_TYPE, android.service.autofill.FillRequest.FLAG_VIEW_NOT_FOCUSED, [android.service.autofill.FillRequest#FLAG_SUPPORTS_FILL_DIALOG](../android/service/autofill/FillRequest.md), android.service.autofill.FillRequest.FLAG_IME_SHOWING, android.service.autofill.FillRequest.FLAG_RESET_FILL_DIALOG_STATE, android.service.autofill.FillRequest.FLAG_PCC_DETECTION, android.service.autofill.FillRequest.FLAG_SCREEN_HAS_CREDMAN_FIELD, and android.service.autofill.FillRequest.FLAG_VIEW_REQUESTS_CREDMAN_SERVICE |

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

Gets the [InlineSuggestionsRequest](../android/view/inputmethod/InlineSuggestionsRequest.md) associated with this request.

Autofill Framework will send a`@non-null` [InlineSuggestionsRequest](../android/view/inputmethod/InlineSuggestionsRequest.md) if currently inline suggestions are supported and can be displayed. If the Autofill service wants to show inline suggestions, they may return [Dataset](../android/service/autofill/Dataset.md) with valid [InlinePresentation](../android/service/autofill/InlinePresentation.md).

The Autofill Service must set supportsInlineSuggestions in its XML to enable support for inline suggestions.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------|--------------------|
| [InlineSuggestionsRequest](../android/view/inputmethod/InlineSuggestionsRequest.md)? | the suggestionspec |

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
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<FillRequest!>
```
