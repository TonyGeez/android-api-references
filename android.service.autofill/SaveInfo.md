# SaveInfo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SaveInfo

Kotlin| [Java](https://developer.android.com/reference/android/service/autofill/SaveInfo "View this page in Java") 

```
class SaveInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.service.autofill.SaveInfo](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#) |

Information used to indicate that an [AutofillService](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService) is interested on saving the user-inputed data for future use, through a [AutofillService.onSaveRequest(SaveRequest, SaveCallback)](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onSaveRequest(android.service.autofill.SaveRequest,%20android.service.autofill.SaveCallback))call.

A [SaveInfo](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#) is always associated with a [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse), and it contains at least two pieces of information:

1. The type(s) of user data (like password or credit card info) that would be saved.
2. The minimum set of views (represented by their [AutofillId](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#)) that need to be changed to trigger a save request.

Typically, the [SaveInfo](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#) contains the same`id`s as the [Dataset](https://developer.android.com/reference/kotlin/android/service/autofill/Dataset): 

```kotlin
new FillResponse.Builder()
        .addDataset(new Dataset.Builder()
            .setValue(id1, AutofillValue.forText("homer"), createPresentation("homer")) // username
            .setValue(id2, AutofillValue.forText("D'OH!"), createPresentation("password for homer")) // password
            .build())
        .setSaveInfo(new SaveInfo.Builder(
            SaveInfo.SAVE_DATA_TYPE_USERNAME | SaveInfo.SAVE_DATA_TYPE_PASSWORD,
            new AutofillId[] { id1, id2 }).build())
        .build();
  
```

The save type flags are used to display the appropriate strings in the autofill save UI. You can pass multiple values, but try to keep it short if possible. In the above example, just`SaveInfo.SAVE_DATA_TYPE_PASSWORD`would be enough.

There might be cases where the [AutofillService](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService) knows how to fill the screen, but the user has no data for it. In that case, the [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse) should contain just the [SaveInfo](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#), but no [Datasets](https://developer.android.com/reference/kotlin/android/service/autofill/Dataset): 

```kotlin
new FillResponse.Builder()
        .setSaveInfo(new SaveInfo.Builder(SaveInfo.SAVE_DATA_TYPE_PASSWORD,
            new AutofillId[] { id1, id2 }).build())
        .build();
  
```

There might be cases where the user data in the [AutofillService](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService) is enough to populate some fields but not all, and the service would still be interested on saving the other fields. In that case, the service could set the[SaveInfo.Builder.setOptionalIds(AutofillId[])](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo.Builder#setOptionalIds(kotlin.Array))as well: 

```kotlin
new FillResponse.Builder()
        .addDataset(new Dataset.Builder()
            .setValue(id1, AutofillValue.forText("742 Evergreen Terrace"),
                createPresentation("742 Evergreen Terrace")) // street
            .setValue(id2, AutofillValue.forText("Springfield"),
                createPresentation("Springfield")) // city
            .build())
        .setSaveInfo(new SaveInfo.Builder(SaveInfo.SAVE_DATA_TYPE_ADDRESS,
            new AutofillId[] { id1, id2 }) // street and  city
            .setOptionalIds(new AutofillId[] { id3, id4 }) // state and zipcode
            .build())
        .build();
  
```

### Triggering a save request

The [AutofillService.onSaveRequest(SaveRequest, SaveCallback)](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onSaveRequest(android.service.autofill.SaveRequest,%20android.service.autofill.SaveCallback))can be triggered after any of the following events:

- The [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) finishes.
- The app explicitly calls [AutofillManager.commit()](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager.html#commit()).
- All required views become invisible (if the [SaveInfo](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#) was created with the [FLAG_SAVE_ON_ALL_VIEWS_INVISIBLE](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#FLAG_SAVE_ON_ALL_VIEWS_INVISIBLE:kotlin.Int) flag).
- The user clicks a specific view (defined by [Builder.setTriggerId(AutofillId)](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo.Builder#setTriggerId(android.view.autofill.AutofillId)).

But it is only triggered when all conditions below are met:

- The [SaveInfo](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#) associated with the [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse) is not`null`neither has the [FLAG_DELAY_SAVE](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#FLAG_DELAY_SAVE:kotlin.Int) flag.
- The [AutofillValue](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue.html#) s of all required views (as set by the`requiredIds`passed to the [SaveInfo.Builder](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo.Builder) constructor are not empty.
- The [AutofillValue](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue.html#) of at least one view (be it required or optional) has changed (i.e., it's neither the same value passed in a [Dataset](https://developer.android.com/reference/kotlin/android/service/autofill/Dataset), nor the initial value presented in the view).
- There is no [Dataset](https://developer.android.com/reference/kotlin/android/service/autofill/Dataset) in the last [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse) that completely matches the screen state (i.e., all required and optional fields in the dataset have the same value as the fields in the screen).
- The user explicitly tapped the autofill save UI asking to save data for autofill.

### Customizing the autofill save UI

The service can also customize some aspects of the autofill save UI:

- Add a simple subtitle by calling [Builder.setDescription(CharSequence)](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo.Builder#setDescription(kotlin.CharSequence)).
- Add a customized subtitle by calling [Builder.setCustomDescription(CustomDescription)](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo.Builder#setCustomDescription(android.service.autofill.CustomDescription)).
- Customize the button used to reject the save request by calling [Builder.setNegativeAction(int, IntentSender)](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo.Builder#setNegativeAction(kotlin.Int,%20android.content.IntentSender)).
- Decide whether the UI should be shown based on the user input validation by calling [Builder.setValidator(Validator)](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo.Builder#setValidator(android.service.autofill.Validator)).

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo.Builder) A builder for [SaveInfo](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#) objects. |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_DELAY_SAVE](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#FLAG_DELAY_SAVE:kotlin.Int) Postpone the autofill save UI. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_DONT_SAVE_ON_FINISH](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#FLAG_DONT_SAVE_ON_FINISH:kotlin.Int) By default, a save request is automatically [triggered](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#TriggeringSaveRequest) once the [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) finishes. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_SAVE_ON_ALL_VIEWS_INVISIBLE](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#FLAG_SAVE_ON_ALL_VIEWS_INVISIBLE:kotlin.Int) Usually, a save request is only automatically [triggered](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#TriggeringSaveRequest) once the [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) finishes. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NEGATIVE_BUTTON_STYLE_CANCEL](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#NEGATIVE_BUTTON_STYLE_CANCEL:kotlin.Int) Style for the negative button of the save UI to cancel the save operation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NEGATIVE_BUTTON_STYLE_NEVER](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#NEGATIVE_BUTTON_STYLE_NEVER:kotlin.Int) Style for the negative button of the save UI to never do the save operation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NEGATIVE_BUTTON_STYLE_REJECT](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#NEGATIVE_BUTTON_STYLE_REJECT:kotlin.Int) Style for the negative button of the save UI to reject the save operation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POSITIVE_BUTTON_STYLE_CONTINUE](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#POSITIVE_BUTTON_STYLE_CONTINUE:kotlin.Int) Style for the positive button of save UI to have next action before the save operation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POSITIVE_BUTTON_STYLE_SAVE](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#POSITIVE_BUTTON_STYLE_SAVE:kotlin.Int) Style for the positive button of save UI to request the save operation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAVE_DATA_TYPE_ADDRESS](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#SAVE_DATA_TYPE_ADDRESS:kotlin.Int) Type used on when the [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse) represents a physical address (such as street, city, state, etc). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAVE_DATA_TYPE_CREDIT_CARD](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#SAVE_DATA_TYPE_CREDIT_CARD:kotlin.Int) Type used when the [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse) represents a credit card. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAVE_DATA_TYPE_DEBIT_CARD](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#SAVE_DATA_TYPE_DEBIT_CARD:kotlin.Int) Type used when the [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse) represents a debit card. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAVE_DATA_TYPE_EMAIL_ADDRESS](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#SAVE_DATA_TYPE_EMAIL_ADDRESS:kotlin.Int) Type used when the [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse) represents just an email address, without a password. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAVE_DATA_TYPE_GENERIC](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#SAVE_DATA_TYPE_GENERIC:kotlin.Int) Type used when the service can save the contents of a screen, but cannot describe what the content is for. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAVE_DATA_TYPE_GENERIC_CARD](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#SAVE_DATA_TYPE_GENERIC_CARD:kotlin.Int) Type used when the [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse) represents a card that does not a specified card or cannot identify what the card is for. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAVE_DATA_TYPE_PASSWORD](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#SAVE_DATA_TYPE_PASSWORD:kotlin.Int) Type used when the [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse) represents user credentials that have a password. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAVE_DATA_TYPE_PAYMENT_CARD](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#SAVE_DATA_TYPE_PAYMENT_CARD:kotlin.Int) Type used when the [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse) represents a payment card except for credit and debit cards. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAVE_DATA_TYPE_USERNAME](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#SAVE_DATA_TYPE_USERNAME:kotlin.Int) Type used when the [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse) represents just an username, without a password. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#describeContents())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [SaveInfo](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### FLAG_DELAY_SAVE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_DELAY_SAVE: Int
```

Postpone the autofill save UI.

If flag is set, the autofill save UI is not triggered when the autofill context associated with the response associated with this [SaveInfo](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#) is committed (with [AutofillManager.commit()](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager.html#commit())). Instead, the [FillContext](https://developer.android.com/reference/kotlin/android/service/autofill/FillContext) is delivered in future fill requests (with [android.service.autofill.AutofillService#onFillRequest(android.service.autofill.FillRequest,android.os.CancellationSignal,android.service.autofill.FillCallback)](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onFillRequest(android.service.autofill.FillRequest,%20android.os.CancellationSignal,%20android.service.autofill.FillCallback))) and save request (with [AutofillService.onSaveRequest(SaveRequest, SaveCallback)](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onSaveRequest(android.service.autofill.SaveRequest,%20android.service.autofill.SaveCallback))) of an activity belonging to the same task.

This flag should be used when the service detects that the application uses multiple screens to implement an autofillable workflow (for example, one screen for the username field, another for password). 

 Value: 4

### FLAG_DONT_SAVE_ON_FINISH

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_DONT_SAVE_ON_FINISH: Int
```

By default, a save request is automatically [triggered](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#TriggeringSaveRequest) once the [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) finishes. If this flag is set, finishing the activity doesn't trigger a save request.

This flag is typically used in conjunction with [Builder.setTriggerId(AutofillId)](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo.Builder#setTriggerId(android.view.autofill.AutofillId)). 

 Value: 2

### FLAG_SAVE_ON_ALL_VIEWS_INVISIBLE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_SAVE_ON_ALL_VIEWS_INVISIBLE: Int
```

Usually, a save request is only automatically [triggered](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#TriggeringSaveRequest) once the [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) finishes. If this flag is set, it is triggered once all saved views become invisible. 

 Value: 1

### NEGATIVE_BUTTON_STYLE_CANCEL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NEGATIVE_BUTTON_STYLE_CANCEL: Int
```

Style for the negative button of the save UI to cancel the save operation. In this case, the user tapping the negative button signals that they would prefer to not save the filled content. 

 Value: 0

### NEGATIVE_BUTTON_STYLE_NEVER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NEGATIVE_BUTTON_STYLE_NEVER: Int
```

Style for the negative button of the save UI to never do the save operation. This means that the user does not need to save any data on this activity or application. Once the user tapping the negative button, the service should never trigger the save UI again. In addition to this, must consider providing restore options for the user. 

 Value: 2

### NEGATIVE_BUTTON_STYLE_REJECT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NEGATIVE_BUTTON_STYLE_REJECT: Int
```

Style for the negative button of the save UI to reject the save operation. This could be useful if the user needs to opt-in your service and the save prompt is an advertisement of the potential value you can add to the user. In this case, the user tapping the negative button sends a strong signal that the feature may not be useful and you may consider some backoff strategy. 

 Value: 1

### POSITIVE_BUTTON_STYLE_CONTINUE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POSITIVE_BUTTON_STYLE_CONTINUE: Int
```

Style for the positive button of save UI to have next action before the save operation. This could be useful if the filled content contains sensitive personally identifiable information and then requires user confirmation or verification. In this case, the user tapping the positive button signals that they would complete the next required action to save the filled content. 

 Value: 1

### POSITIVE_BUTTON_STYLE_SAVE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POSITIVE_BUTTON_STYLE_SAVE: Int
```

Style for the positive button of save UI to request the save operation. In this case, the user tapping the positive button signals that they agrees to save the filled content. 

 Value: 0

### SAVE_DATA_TYPE_ADDRESS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAVE_DATA_TYPE_ADDRESS: Int
```

Type used on when the [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse) represents a physical address (such as street, city, state, etc). 

 Value: 2

### SAVE_DATA_TYPE_CREDIT_CARD

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAVE_DATA_TYPE_CREDIT_CARD: Int
```

Type used when the [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse) represents a credit card. 

 Value: 4

### SAVE_DATA_TYPE_DEBIT_CARD

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAVE_DATA_TYPE_DEBIT_CARD: Int
```

Type used when the [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse) represents a debit card. 

 Value: 32

### SAVE_DATA_TYPE_EMAIL_ADDRESS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAVE_DATA_TYPE_EMAIL_ADDRESS: Int
```

Type used when the [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse) represents just an email address, without a password. 

 Value: 16

### SAVE_DATA_TYPE_GENERIC

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAVE_DATA_TYPE_GENERIC: Int
```

Type used when the service can save the contents of a screen, but cannot describe what the content is for. 

 Value: 0

### SAVE_DATA_TYPE_GENERIC_CARD

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAVE_DATA_TYPE_GENERIC_CARD: Int
```

Type used when the [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse) represents a card that does not a specified card or cannot identify what the card is for. 

 Value: 128

### SAVE_DATA_TYPE_PASSWORD

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAVE_DATA_TYPE_PASSWORD: Int
```

Type used when the [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse) represents user credentials that have a password. 

 Value: 1

### SAVE_DATA_TYPE_PAYMENT_CARD

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAVE_DATA_TYPE_PAYMENT_CARD: Int
```

Type used when the [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse) represents a payment card except for credit and debit cards. 

 Value: 64

### SAVE_DATA_TYPE_USERNAME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAVE_DATA_TYPE_USERNAME: Int
```

Type used when the [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse) represents just an username, without a password. 

 Value: 8

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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
    parcel: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SaveInfo!>
```
