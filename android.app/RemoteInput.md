# RemoteInput

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RemoteInput

Kotlin| [Java](https://developer.android.com/reference/android/app/RemoteInput "View this page in Java") 

```
class RemoteInput : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.RemoteInput](https://developer.android.com/reference/kotlin/android/app/RemoteInput#) |

A`RemoteInput`object specifies input to be collected from a user to be passed along with an intent inside a [android.app.PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent) that is sent. Always use [RemoteInput.Builder](https://developer.android.com/reference/kotlin/android/app/RemoteInput.Builder) to create instances of this class.

See [Replying to notifications](https://developer.android.com/guide/topics/ui/notifiers/notifications.html#direct) for more information on how to use this class.

The following example adds a`RemoteInput`to a [Notification.Action](https://developer.android.com/reference/kotlin/android/app/Notification.Action), sets the result key as`quick_reply`, and sets the label as`Quick reply`. Users are prompted to input a response when they trigger the action. The results are sent along with the intent and can be retrieved with the result key (provided to the [Builder](https://developer.android.com/reference/kotlin/android/app/RemoteInput.Builder) constructor) from the Bundle returned by [getResultsFromIntent](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getResultsFromIntent(android.content.Intent)). 

```kotlin
public static final String KEY_QUICK_REPLY_TEXT = "quick_reply";
  Notification.Action action = new Notification.Action.Builder(
          R.drawable.reply, "Reply", actionIntent)
          <b>.addRemoteInput(new RemoteInput.Builder(KEY_QUICK_REPLY_TEXT)
                  .setLabel("Quick reply").build()</b>)
          .build();
```

When the [android.app.PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent) is fired, the intent inside will contain the input results if collected. To access these results, use the [getResultsFromIntent](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getResultsFromIntent(android.content.Intent))function. The result values will present under the result key passed to the [Builder](https://developer.android.com/reference/kotlin/android/app/RemoteInput.Builder) constructor. 

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
| | [Builder](https://developer.android.com/reference/kotlin/android/app/RemoteInput.Builder) Builder class for [RemoteInput](https://developer.android.com/reference/kotlin/android/app/RemoteInput#) objects. |

| Constants ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EDIT_CHOICES_BEFORE_SENDING_AUTO](https://developer.android.com/reference/kotlin/android/app/RemoteInput#EDIT_CHOICES_BEFORE_SENDING_AUTO:kotlin.Int) The platform will determine whether choices will be edited before being sent to the app. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EDIT_CHOICES_BEFORE_SENDING_DISABLED](https://developer.android.com/reference/kotlin/android/app/RemoteInput#EDIT_CHOICES_BEFORE_SENDING_DISABLED:kotlin.Int) Tapping on a choice should send the input immediately, without letting the user edit it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EDIT_CHOICES_BEFORE_SENDING_ENABLED](https://developer.android.com/reference/kotlin/android/app/RemoteInput#EDIT_CHOICES_BEFORE_SENDING_ENABLED:kotlin.Int) Tapping on a choice should let the user edit the input before it is sent to the app. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_RESULTS_DATA](https://developer.android.com/reference/kotlin/android/app/RemoteInput#EXTRA_RESULTS_DATA:kotlin.String) Extra added to a clip data intent object to hold the text results bundle. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RESULTS_CLIP_LABEL](https://developer.android.com/reference/kotlin/android/app/RemoteInput#RESULTS_CLIP_LABEL:kotlin.String) Label used to denote the clip data type used for remote input transport |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_CHOICE](https://developer.android.com/reference/kotlin/android/app/RemoteInput#SOURCE_CHOICE:kotlin.Int) The user selected one of the choices from [getChoices](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getChoices()). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_FREE_FORM_INPUT](https://developer.android.com/reference/kotlin/android/app/RemoteInput#SOURCE_FREE_FORM_INPUT:kotlin.Int) The user manually entered the data. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addDataResultToIntent](https://developer.android.com/reference/kotlin/android/app/RemoteInput#addDataResultToIntent(android.app.RemoteInput,%20android.content.Intent,%20kotlin.collections.MutableMap))`(`remoteInput:` ` [RemoteInput](https://developer.android.com/reference/kotlin/android/app/RemoteInput#)!`, `intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`, `results:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!>!`)` Same as [addResultsToIntent](https://developer.android.com/reference/kotlin/android/app/RemoteInput#addResultsToIntent(kotlin.Array,%20android.content.Intent,%20android.os.Bundle))but for setting data results. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addResultsToIntent](https://developer.android.com/reference/kotlin/android/app/RemoteInput#addResultsToIntent(kotlin.Array,%20android.content.Intent,%20android.os.Bundle))`(`remoteInputs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [RemoteInput](https://developer.android.com/reference/kotlin/android/app/RemoteInput#)!>!`, `intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`, `results:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Populate an intent object with the text results gathered from remote input. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/app/RemoteInput#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAllowFreeFormInput](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getAllowFreeFormInput())`()` Get whether or not users can provide an arbitrary value for input. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getAllowedDataTypes](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getAllowedDataTypes())`()` Get possible non-textual inputs that are accepted. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\>! | [getChoices](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getChoices())`()` Get possible input choices. |
| static [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>! | [getDataResultsFromIntent](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getDataResultsFromIntent(android.content.Intent,%20kotlin.String))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`, `remoteInputResultKey:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Similar as [getResultsFromIntent](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getResultsFromIntent(android.content.Intent))but retrieves data results for a specific RemoteInput result. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEditChoicesBeforeSending](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getEditChoicesBeforeSending())`()` Gets whether tapping on a choice should let the user edit the input before it is sent to the app. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [getExtras](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getExtras())`()` Get additional metadata carried around with this remote input. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getLabel](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getLabel())`()` Get the label to display to users when collecting this input. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getResultKey](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getResultKey())`()` Get the key that the result of this input will be set in from the Bundle returned by [getResultsFromIntent](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getResultsFromIntent(android.content.Intent))when the [android.app.PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent) is sent. |
| static [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [getResultsFromIntent](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getResultsFromIntent(android.content.Intent))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` Get the remote input text results bundle from an intent. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResultsSource](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getResultsSource(android.content.Intent))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` Get the source of the RemoteInput results. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDataOnly](https://developer.android.com/reference/kotlin/android/app/RemoteInput#isDataOnly())`()` Returns true if the input only accepts data, meaning [getAllowFreeFormInput](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getAllowFreeFormInput())is false, [getChoices](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getChoices())is null or empty, and [getAllowedDataTypes](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getAllowedDataTypes())is non-null and not empty. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResultsSource](https://developer.android.com/reference/kotlin/android/app/RemoteInput#setResultsSource(android.content.Intent,%20kotlin.Int))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`, `source:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the source of the RemoteInput results. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/app/RemoteInput#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [RemoteInput](https://developer.android.com/reference/kotlin/android/app/RemoteInput#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/app/RemoteInput#CREATOR:android.os.Parcelable.Creator) <br /> |

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

The user selected one of the choices from [getChoices](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getChoices()). 

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

Same as [addResultsToIntent](https://developer.android.com/reference/kotlin/android/app/RemoteInput#addResultsToIntent(kotlin.Array,%20android.content.Intent,%20android.os.Bundle))but for setting data results. This is used for inputs that accept non-textual results (see [Builder.setAllowDataType](https://developer.android.com/reference/kotlin/android/app/RemoteInput.Builder#setAllowDataType(kotlin.String,%20kotlin.Boolean))). Only one result can be provided for every mime type accepted by the RemoteInput. If multiple inputs of the same mime type are expected then multiple RemoteInputs should be used.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `remoteInput` | [RemoteInput](https://developer.android.com/reference/kotlin/android/app/RemoteInput#)!:The remote input for which results are being provided |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:The intent to add remote input results to. The [ClipData](https://developer.android.com/reference/kotlin/android/content/ClipData.html#) field of the intent will be modified to contain the results. |
| `results` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>!:A map of mime type to the Uri result for that mime type. |

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
| `remoteInputs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [RemoteInput](https://developer.android.com/reference/kotlin/android/app/RemoteInput#)!\>!:The remote inputs for which results are being provided |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:The intent to add remote inputs to. The [ClipData](https://developer.android.com/reference/kotlin/android/content/ClipData.html#) field of the intent will be modified to contain the results. |
| `results` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:A bundle holding the remote input results. This bundle should be populated with keys matching the result keys specified in`remoteInputs`with values being the CharSequence results per key. |

### describeContents

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getAllowFreeFormInput

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAllowFreeFormInput(): Boolean
```

Get whether or not users can provide an arbitrary value for input. If you set this to`false`, users must select one of the choices in [getChoices](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getChoices()). An [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) is thrown if you set this to false and [getChoices](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getChoices())returns`null`or empty. 

### getAllowedDataTypes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAllowedDataTypes(): MutableSet<String!>!
```

Get possible non-textual inputs that are accepted. This can be`null`if the input does not accept non-textual values. See [Builder.setAllowDataType](https://developer.android.com/reference/kotlin/android/app/RemoteInput.Builder#setAllowDataType(kotlin.String,%20kotlin.Boolean)). 

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

Similar as [getResultsFromIntent](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getResultsFromIntent(android.content.Intent))but retrieves data results for a specific RemoteInput result. To retrieve a value use: 

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
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:The intent object that fired in response to an action or content intent which also had one or more remote input requested. |
| `remoteInputResultKey` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The result key for the RemoteInput you want results for. |

### getEditChoicesBeforeSending

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEditChoicesBeforeSending(): Int
```

Gets whether tapping on a choice should let the user edit the input before it is sent to the app.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.app.RemoteInput#EDIT_CHOICES_BEFORE_SENDING_AUTO](https://developer.android.com/reference/kotlin/android/app/RemoteInput#EDIT_CHOICES_BEFORE_SENDING_AUTO:kotlin.Int), [android.app.RemoteInput#EDIT_CHOICES_BEFORE_SENDING_DISABLED](https://developer.android.com/reference/kotlin/android/app/RemoteInput#EDIT_CHOICES_BEFORE_SENDING_DISABLED:kotlin.Int), or [android.app.RemoteInput#EDIT_CHOICES_BEFORE_SENDING_ENABLED](https://developer.android.com/reference/kotlin/android/app/RemoteInput#EDIT_CHOICES_BEFORE_SENDING_ENABLED:kotlin.Int) |

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

Get the key that the result of this input will be set in from the Bundle returned by [getResultsFromIntent](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getResultsFromIntent(android.content.Intent))when the [android.app.PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent) is sent. 

### getResultsFromIntent

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getResultsFromIntent(intent: Intent!): Bundle!
```

Get the remote input text results bundle from an intent. The returned Bundle will contain a key/value for every result key populated with text by remote input collector. Use the [Bundle.getCharSequence(String)](https://developer.android.com/reference/kotlin/android/os/Bundle.html#getCharSequence(kotlin.String))method to retrieve a value. For non-text results use [getDataResultsFromIntent](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getDataResultsFromIntent(android.content.Intent,%20kotlin.String)).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:The intent object that fired in response to an action or content intent which also had one or more remote input requested. |

### getResultsSource

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getResultsSource(intent: Intent!): Int
```

Get the source of the RemoteInput results.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:The intent object that fired in response to an action or content intent which also had one or more remote input requested. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The source of the results. If no source was set, [SOURCE_FREE_FORM_INPUT](https://developer.android.com/reference/kotlin/android/app/RemoteInput#SOURCE_FREE_FORM_INPUT:kotlin.Int) will be returned. Value is [android.app.RemoteInput#SOURCE_FREE_FORM_INPUT](https://developer.android.com/reference/kotlin/android/app/RemoteInput#SOURCE_FREE_FORM_INPUT:kotlin.Int), or [android.app.RemoteInput#SOURCE_CHOICE](https://developer.android.com/reference/kotlin/android/app/RemoteInput#SOURCE_CHOICE:kotlin.Int) |

**See Also**

- [#SOURCE_FREE_FORM_INPUT](https://developer.android.com/reference/kotlin/android/app/RemoteInput#SOURCE_FREE_FORM_INPUT:kotlin.Int)
- [#SOURCE_CHOICE](https://developer.android.com/reference/kotlin/android/app/RemoteInput#SOURCE_CHOICE:kotlin.Int) 

### isDataOnly

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isDataOnly(): Boolean
```

Returns true if the input only accepts data, meaning [getAllowFreeFormInput](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getAllowFreeFormInput())is false, [getChoices](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getChoices())is null or empty, and [getAllowedDataTypes](https://developer.android.com/reference/kotlin/android/app/RemoteInput#getAllowedDataTypes())is non-null and not empty. 

### setResultsSource

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setResultsSource(
    intent: Intent!, 
    source: Int
): Unit
```

Set the source of the RemoteInput results. This method should only be called by remote input collection services (e.g. [android.service.notification.NotificationListenerService](https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#)) when sending results to a pending intent.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:The intent to add remote input source to. The [ClipData](https://developer.android.com/reference/kotlin/android/content/ClipData.html#) field of the intent will be modified to contain the source. |
| `source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The source of the results. Value is [android.app.RemoteInput#SOURCE_FREE_FORM_INPUT](https://developer.android.com/reference/kotlin/android/app/RemoteInput#SOURCE_FREE_FORM_INPUT:kotlin.Int), or [android.app.RemoteInput#SOURCE_CHOICE](https://developer.android.com/reference/kotlin/android/app/RemoteInput#SOURCE_CHOICE:kotlin.Int) |

**See Also**

- [#SOURCE_FREE_FORM_INPUT](https://developer.android.com/reference/kotlin/android/app/RemoteInput#SOURCE_FREE_FORM_INPUT:kotlin.Int)
- [#SOURCE_CHOICE](https://developer.android.com/reference/kotlin/android/app/RemoteInput#SOURCE_CHOICE:kotlin.Int) 

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<RemoteInput!>
```
