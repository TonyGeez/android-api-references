# RemoteInput

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RemoteInput

Kotlin| [Java](RemoteInput.md) 
| --- | --- |

```
class RemoteInput : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.RemoteInput](RemoteInput.md) |

A`RemoteInput`object specifies input to be collected from a user to be passed along with an intent inside a [android.app.PendingIntent](PendingIntent.md) that is sent. Always use [RemoteInput.Builder](../android/app/RemoteInput.Builder.md) to create instances of this class.

See [Replying to notifications](https://developer.android.com/guide/topics/ui/notifiers/notifications.html#direct) for more information on how to use this class.

The following example adds a`RemoteInput`to a [Notification.Action](../android/app/Notification.Action.md), sets the result key as`quick_reply`, and sets the label as`Quick reply`. Users are prompted to input a response when they trigger the action. The results are sent along with the intent and can be retrieved with the result key (provided to the [Builder](../android/app/RemoteInput.Builder.md) constructor) from the Bundle returned by [getResultsFromIntent](RemoteInput.md)). 

```kotlin
public static final String KEY_QUICK_REPLY_TEXT = "quick_reply";
  Notification.Action action = new Notification.Action.Builder(
          R.drawable.reply, "Reply", actionIntent)
          <b>.addRemoteInput(new RemoteInput.Builder(KEY_QUICK_REPLY_TEXT)
                  .setLabel("Quick reply").build()</b>)
          .build();
```

When the [android.app.PendingIntent](PendingIntent.md) is fired, the intent inside will contain the input results if collected. To access these results, use the [getResultsFromIntent](RemoteInput.md))function. The result values will present under the result key passed to the [Builder](../android/app/RemoteInput.Builder.md) constructor. 

```kotlin
public static final String KEY_QUICK_REPLY_TEXT = "quick_reply";
  Bundle results = RemoteInput.getResultsFromIntent(intent);
  if (results != null) {
      CharSequence quickReplyResult = results.getCharSequence(KEY_QUICK_REPLY_TEXT);
  }
```

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/app/RemoteInput.Builder.md) Builder class for [RemoteInput](RemoteInput.md) objects. |

| Constants ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EDIT_CHOICES_BEFORE_SENDING_AUTO](RemoteInput.md) The platform will determine whether choices will be edited before being sent to the app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EDIT_CHOICES_BEFORE_SENDING_DISABLED](RemoteInput.md) Tapping on a choice should send the input immediately, without letting the user edit it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EDIT_CHOICES_BEFORE_SENDING_ENABLED](RemoteInput.md) Tapping on a choice should let the user edit the input before it is sent to the app. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_RESULTS_DATA](RemoteInput.md) Extra added to a clip data intent object to hold the text results bundle. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RESULTS_CLIP_LABEL](RemoteInput.md) Label used to denote the clip data type used for remote input transport |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_CHOICE](RemoteInput.md) The user selected one of the choices from [getChoices](RemoteInput.md)). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_FREE_FORM_INPUT](RemoteInput.md) The user manually entered the data. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addDataResultToIntent](RemoteInput.md))`(`remoteInput:` ` [RemoteInput](RemoteInput.md)!`, `intent:` ` [Intent](../android.content/Intent.md)!`, `results:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Uri](../android.net/Uri.md)!>!`)` Same as [addResultsToIntent](RemoteInput.md))but for setting data results. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addResultsToIntent](RemoteInput.md))`(`remoteInputs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [RemoteInput](RemoteInput.md)!>!`, `intent:` ` [Intent](../android.content/Intent.md)!`, `results:` ` [Bundle](../android.os/Bundle.md)!`)` Populate an intent object with the text results gathered from remote input. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](RemoteInput.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAllowFreeFormInput](RemoteInput.md))`()` Get whether or not users can provide an arbitrary value for input. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getAllowedDataTypes](RemoteInput.md))`()` Get possible non-textual inputs that are accepted. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\>! | [getChoices](RemoteInput.md))`()` Get possible input choices. |
| --- | --- |
| static [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Uri](../android.net/Uri.md)!\>! | [getDataResultsFromIntent](RemoteInput.md))`(`intent:` ` [Intent](../android.content/Intent.md)!`, `remoteInputResultKey:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Similar as [getResultsFromIntent](RemoteInput.md))but retrieves data results for a specific RemoteInput result. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEditChoicesBeforeSending](RemoteInput.md))`()` Gets whether tapping on a choice should let the user edit the input before it is sent to the app. |
| [Bundle](../android.os/Bundle.md)! | [getExtras](RemoteInput.md))`()` Get additional metadata carried around with this remote input. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getLabel](RemoteInput.md))`()` Get the label to display to users when collecting this input. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getResultKey](RemoteInput.md))`()` Get the key that the result of this input will be set in from the Bundle returned by [getResultsFromIntent](RemoteInput.md))when the [android.app.PendingIntent](PendingIntent.md) is sent. |
| static [Bundle](../android.os/Bundle.md)! | [getResultsFromIntent](RemoteInput.md))`(`intent:` ` [Intent](../android.content/Intent.md)!`)` Get the remote input text results bundle from an intent. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResultsSource](RemoteInput.md))`(`intent:` ` [Intent](../android.content/Intent.md)!`)` Get the source of the RemoteInput results. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDataOnly](RemoteInput.md))`()` Returns true if the input only accepts data, meaning [getAllowFreeFormInput](RemoteInput.md))is false, [getChoices](RemoteInput.md))is null or empty, and [getAllowedDataTypes](RemoteInput.md))is non-null and not empty. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResultsSource](RemoteInput.md))`(`intent:` ` [Intent](../android.content/Intent.md)!`, `source:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the source of the RemoteInput results. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](RemoteInput.md))`(`out:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [RemoteInput](RemoteInput.md)!\> | [CREATOR](RemoteInput.md) <br /> |

## Constants

### EDIT_CHOICES_BEFORE_SENDING_AUTO

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EDIT_CHOICES_BEFORE_SENDING_AUTO: Int
```

The platform will determine whether choices will be edited before being sent to the app. 

 Value: 0

### EDIT_CHOICES_BEFORE_SENDING_DISABLED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EDIT_CHOICES_BEFORE_SENDING_DISABLED: Int
```

Tapping on a choice should send the input immediately, without letting the user edit it. 

 Value: 1

### EDIT_CHOICES_BEFORE_SENDING_ENABLED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EDIT_CHOICES_BEFORE_SENDING_ENABLED: Int
```

Tapping on a choice should let the user edit the input before it is sent to the app. 

 Value: 2

### EXTRA_RESULTS_DATA

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_RESULTS_DATA: String
```

Extra added to a clip data intent object to hold the text results bundle. 

 Value: "android.remoteinput.resultsData"

### RESULTS_CLIP_LABEL

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULTS_CLIP_LABEL: String
```

Label used to denote the clip data type used for remote input transport 

 Value: "android.remoteinput.results"

### SOURCE_CHOICE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_CHOICE: Int
```

The user selected one of the choices from [getChoices](RemoteInput.md)). 

 Value: 1

### SOURCE_FREE_FORM_INPUT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_FREE_FORM_INPUT: Int
```

The user manually entered the data. 

 Value: 0

## Public methods

### addDataResultToIntent

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun addDataResultToIntent(
    remoteInput: RemoteInput!, 
    intent: Intent!, 
    results: MutableMap<String!, Uri!>!
): Unit
```

Same as [addResultsToIntent](RemoteInput.md))but for setting data results. This is used for inputs that accept non-textual results (see [Builder.setAllowDataType](../android/app/RemoteInput.Builder.md))). Only one result can be provided for every mime type accepted by the RemoteInput. If multiple inputs of the same mime type are expected then multiple RemoteInputs should be used.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `remoteInput` | [RemoteInput](RemoteInput.md)!:The remote input for which results are being provided |
| `intent` | [Intent](../android.content/Intent.md)!:The intent to add remote input results to. The [ClipData](../android.content/ClipData.md) field of the intent will be modified to contain the results. |
| `results` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Uri](../android.net/Uri.md)!\>!:A map of mime type to the Uri result for that mime type. |
| --- | --- |

### addResultsToIntent

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun addResultsToIntent(
    remoteInputs: Array<RemoteInput!>!, 
    intent: Intent!, 
    results: Bundle!
): Unit
```

Populate an intent object with the text results gathered from remote input. This method should only be called by remote input collection services when sending results to a pending intent.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `remoteInputs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [RemoteInput](RemoteInput.md)!\>!:The remote inputs for which results are being provided |
| `intent` | [Intent](../android.content/Intent.md)!:The intent to add remote inputs to. The [ClipData](../android.content/ClipData.md) field of the intent will be modified to contain the results. |
| `results` | [Bundle](../android.os/Bundle.md)!:A bundle holding the remote input results. This bundle should be populated with keys matching the result keys specified in`remoteInputs`with values being the CharSequence results per key. |
| --- | --- |

### describeContents

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getAllowFreeFormInput

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAllowFreeFormInput(): Boolean
```

Get whether or not users can provide an arbitrary value for input. If you set this to`false`, users must select one of the choices in [getChoices](RemoteInput.md)). An [IllegalArgumentException](../java.lang/IllegalArgumentException.md) is thrown if you set this to false and [getChoices](RemoteInput.md))returns`null`or empty. 

### getAllowedDataTypes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAllowedDataTypes(): MutableSet<String!>!
```

Get possible non-textual inputs that are accepted. This can be`null`if the input does not accept non-textual values. See [Builder.setAllowDataType](../android/app/RemoteInput.Builder.md)). 

### getChoices

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getChoices(): Array<CharSequence!>!
```

Get possible input choices. This can be`null`if there are no choices to present. 

### getDataResultsFromIntent

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDataResultsFromIntent(
    intent: Intent!, 
    remoteInputResultKey: String!
): MutableMap<String!, Uri!>!
```

Similar as [getResultsFromIntent](RemoteInput.md))but retrieves data results for a specific RemoteInput result. To retrieve a value use: 

```kotlin
<code>Map&lt;String, Uri&gt; results =
      RemoteInput.getDataResultsFromIntent(intent, REMOTE_INPUT_KEY);
  if (results != null) {
    Uri data = results.get(MIME_TYPE_OF_INTEREST);
  }
  </code>
```

<br />

| Parameters ||
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](../android.content/Intent.md)!:The intent object that fired in response to an action or content intent which also had one or more remote input requested. |
| `remoteInputResultKey` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The result key for the RemoteInput you want results for. |

### getEditChoicesBeforeSending

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEditChoicesBeforeSending(): Int
```

Gets whether tapping on a choice should let the user edit the input before it is sent to the app.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.app.RemoteInput#EDIT_CHOICES_BEFORE_SENDING_AUTO](RemoteInput.md), [android.app.RemoteInput#EDIT_CHOICES_BEFORE_SENDING_DISABLED](RemoteInput.md), or [android.app.RemoteInput#EDIT_CHOICES_BEFORE_SENDING_ENABLED](RemoteInput.md) |

### getExtras

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtras(): Bundle!
```

Get additional metadata carried around with this remote input. 

### getLabel

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLabel(): CharSequence!
```

Get the label to display to users when collecting this input. 

### getResultKey

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getResultKey(): String!
```

Get the key that the result of this input will be set in from the Bundle returned by [getResultsFromIntent](RemoteInput.md))when the [android.app.PendingIntent](PendingIntent.md) is sent. 

### getResultsFromIntent

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getResultsFromIntent(intent: Intent!): Bundle!
```

Get the remote input text results bundle from an intent. The returned Bundle will contain a key/value for every result key populated with text by remote input collector. Use the [Bundle.getCharSequence(String)](../android.os/Bundle.md))method to retrieve a value. For non-text results use [getDataResultsFromIntent](RemoteInput.md)).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](../android.content/Intent.md)!:The intent object that fired in response to an action or content intent which also had one or more remote input requested. |

### getResultsSource

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getResultsSource(intent: Intent!): Int
```

Get the source of the RemoteInput results.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](../android.content/Intent.md)!:The intent object that fired in response to an action or content intent which also had one or more remote input requested. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The source of the results. If no source was set, [SOURCE_FREE_FORM_INPUT](RemoteInput.md) will be returned. Value is [android.app.RemoteInput#SOURCE_FREE_FORM_INPUT](RemoteInput.md), or [android.app.RemoteInput#SOURCE_CHOICE](RemoteInput.md) |

**See Also**

- [#SOURCE_FREE_FORM_INPUT](RemoteInput.md)
- [#SOURCE_CHOICE](RemoteInput.md) 

### isDataOnly

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isDataOnly(): Boolean
```

Returns true if the input only accepts data, meaning [getAllowFreeFormInput](RemoteInput.md))is false, [getChoices](RemoteInput.md))is null or empty, and [getAllowedDataTypes](RemoteInput.md))is non-null and not empty. 

### setResultsSource

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setResultsSource(
    intent: Intent!, 
    source: Int
): Unit
```

Set the source of the RemoteInput results. This method should only be called by remote input collection services (e.g. [android.service.notification.NotificationListenerService](../android.service.notification/NotificationListenerService.md)) when sending results to a pending intent.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](../android.content/Intent.md)!:The intent to add remote input source to. The [ClipData](../android.content/ClipData.md) field of the intent will be modified to contain the source. |
| `source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The source of the results. Value is [android.app.RemoteInput#SOURCE_FREE_FORM_INPUT](RemoteInput.md), or [android.app.RemoteInput#SOURCE_CHOICE](RemoteInput.md) |

**See Also**

- [#SOURCE_FREE_FORM_INPUT](RemoteInput.md)
- [#SOURCE_CHOICE](RemoteInput.md) 

### writeToParcel

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<RemoteInput!>
```
