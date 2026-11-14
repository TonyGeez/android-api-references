# SaveInfo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SaveInfo

Kotlin| [Java](SaveInfo.md) 
| --- | --- |

```
class SaveInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.autofill.SaveInfo](SaveInfo.md) |

Information used to indicate that an [AutofillService](AutofillService.md) is interested on saving the user-inputed data for future use, through a [AutofillService.onSaveRequest(SaveRequest, SaveCallback)](AutofillService.md))call.

A [SaveInfo](SaveInfo.md) is always associated with a [FillResponse](FillResponse.md), and it contains at least two pieces of information:

1. The type(s) of user data (like password or credit card info) that would be saved.
2. The minimum set of views (represented by their [AutofillId](../android.view.autofill/AutofillId.md)) that need to be changed to trigger a save request.

Typically, the [SaveInfo](SaveInfo.md) contains the same`id`s as the [Dataset](Dataset.md): 

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

There might be cases where the [AutofillService](AutofillService.md) knows how to fill the screen, but the user has no data for it. In that case, the [FillResponse](FillResponse.md) should contain just the [SaveInfo](SaveInfo.md), but no [Datasets](Dataset.md): 

```kotlin
new FillResponse.Builder()
        .setSaveInfo(new SaveInfo.Builder(SaveInfo.SAVE_DATA_TYPE_PASSWORD,
            new AutofillId[] { id1, id2 }).build())
        .build();
  
```

There might be cases where the user data in the [AutofillService](AutofillService.md) is enough to populate some fields but not all, and the service would still be interested on saving the other fields. In that case, the service could set the[SaveInfo.Builder.setOptionalIds(AutofillId[])](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo.Builder#setOptionalIds(kotlin.Array))as well: 

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

The [AutofillService.onSaveRequest(SaveRequest, SaveCallback)](AutofillService.md))can be triggered after any of the following events:

- The [Activity](../android.app/Activity.md) finishes.
- The app explicitly calls [AutofillManager.commit()](../android.view.autofill/AutofillManager.md)).
- All required views become invisible (if the [SaveInfo](SaveInfo.md) was created with the [FLAG_SAVE_ON_ALL_VIEWS_INVISIBLE](SaveInfo.md) flag).
- The user clicks a specific view (defined by [Builder.setTriggerId(AutofillId)](../android/service/autofill/SaveInfo.Builder.md)).

But it is only triggered when all conditions below are met:

- The [SaveInfo](SaveInfo.md) associated with the [FillResponse](FillResponse.md) is not`null`neither has the [FLAG_DELAY_SAVE](SaveInfo.md) flag.
- The [AutofillValue](../android.view.autofill/AutofillValue.md) s of all required views (as set by the`requiredIds`passed to the [SaveInfo.Builder](../android/service/autofill/SaveInfo.Builder.md) constructor are not empty.
- The [AutofillValue](../android.view.autofill/AutofillValue.md) of at least one view (be it required or optional) has changed (i.e., it's neither the same value passed in a [Dataset](Dataset.md), nor the initial value presented in the view).
- There is no [Dataset](Dataset.md) in the last [FillResponse](FillResponse.md) that completely matches the screen state (i.e., all required and optional fields in the dataset have the same value as the fields in the screen).
- The user explicitly tapped the autofill save UI asking to save data for autofill.

### Customizing the autofill save UI

The service can also customize some aspects of the autofill save UI:

- Add a simple subtitle by calling [Builder.setDescription(CharSequence)](../android/service/autofill/SaveInfo.Builder.md)).
- Add a customized subtitle by calling [Builder.setCustomDescription(CustomDescription)](../android/service/autofill/SaveInfo.Builder.md)).
- Customize the button used to reject the save request by calling [Builder.setNegativeAction(int, IntentSender)](../android/service/autofill/SaveInfo.Builder.md)).
- Decide whether the UI should be shown based on the user input validation by calling [Builder.setValidator(Validator)](../android/service/autofill/SaveInfo.Builder.md)).

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/service/autofill/SaveInfo.Builder.md) A builder for [SaveInfo](SaveInfo.md) objects. |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_DELAY_SAVE](SaveInfo.md) Postpone the autofill save UI. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_DONT_SAVE_ON_FINISH](SaveInfo.md) By default, a save request is automatically [triggered](SaveInfo.md) once the [Activity](../android.app/Activity.md) finishes. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_SAVE_ON_ALL_VIEWS_INVISIBLE](SaveInfo.md) Usually, a save request is only automatically [triggered](SaveInfo.md) once the [Activity](../android.app/Activity.md) finishes. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NEGATIVE_BUTTON_STYLE_CANCEL](SaveInfo.md) Style for the negative button of the save UI to cancel the save operation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NEGATIVE_BUTTON_STYLE_NEVER](SaveInfo.md) Style for the negative button of the save UI to never do the save operation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NEGATIVE_BUTTON_STYLE_REJECT](SaveInfo.md) Style for the negative button of the save UI to reject the save operation. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POSITIVE_BUTTON_STYLE_CONTINUE](SaveInfo.md) Style for the positive button of save UI to have next action before the save operation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POSITIVE_BUTTON_STYLE_SAVE](SaveInfo.md) Style for the positive button of save UI to request the save operation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAVE_DATA_TYPE_ADDRESS](SaveInfo.md) Type used on when the [FillResponse](FillResponse.md) represents a physical address (such as street, city, state, etc). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAVE_DATA_TYPE_CREDIT_CARD](SaveInfo.md) Type used when the [FillResponse](FillResponse.md) represents a credit card. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAVE_DATA_TYPE_DEBIT_CARD](SaveInfo.md) Type used when the [FillResponse](FillResponse.md) represents a debit card. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAVE_DATA_TYPE_EMAIL_ADDRESS](SaveInfo.md) Type used when the [FillResponse](FillResponse.md) represents just an email address, without a password. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAVE_DATA_TYPE_GENERIC](SaveInfo.md) Type used when the service can save the contents of a screen, but cannot describe what the content is for. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAVE_DATA_TYPE_GENERIC_CARD](SaveInfo.md) Type used when the [FillResponse](FillResponse.md) represents a card that does not a specified card or cannot identify what the card is for. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAVE_DATA_TYPE_PASSWORD](SaveInfo.md) Type used when the [FillResponse](FillResponse.md) represents user credentials that have a password. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAVE_DATA_TYPE_PAYMENT_CARD](SaveInfo.md) Type used when the [FillResponse](FillResponse.md) represents a payment card except for credit and debit cards. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAVE_DATA_TYPE_USERNAME](SaveInfo.md) Type used when the [FillResponse](FillResponse.md) represents just an username, without a password. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](SaveInfo.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](SaveInfo.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](SaveInfo.md))`(`parcel:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SaveInfo](SaveInfo.md)!\> | [CREATOR](SaveInfo.md) <br /> |

## Constants

### FLAG_DELAY_SAVE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_DELAY_SAVE: Int
```

Postpone the autofill save UI.

If flag is set, the autofill save UI is not triggered when the autofill context associated with the response associated with this [SaveInfo](SaveInfo.md) is committed (with [AutofillManager.commit()](../android.view.autofill/AutofillManager.md))). Instead, the [FillContext](FillContext.md) is delivered in future fill requests (with [android.service.autofill.AutofillService#onFillRequest(android.service.autofill.FillRequest,android.os.CancellationSignal,android.service.autofill.FillCallback)](AutofillService.md))) and save request (with [AutofillService.onSaveRequest(SaveRequest, SaveCallback)](AutofillService.md))) of an activity belonging to the same task.

This flag should be used when the service detects that the application uses multiple screens to implement an autofillable workflow (for example, one screen for the username field, another for password). 

 Value: 4

### FLAG_DONT_SAVE_ON_FINISH

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_DONT_SAVE_ON_FINISH: Int
```

By default, a save request is automatically [triggered](SaveInfo.md) once the [Activity](../android.app/Activity.md) finishes. If this flag is set, finishing the activity doesn't trigger a save request.

This flag is typically used in conjunction with [Builder.setTriggerId(AutofillId)](../android/service/autofill/SaveInfo.Builder.md)). 

 Value: 2

### FLAG_SAVE_ON_ALL_VIEWS_INVISIBLE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_SAVE_ON_ALL_VIEWS_INVISIBLE: Int
```

Usually, a save request is only automatically [triggered](SaveInfo.md) once the [Activity](../android.app/Activity.md) finishes. If this flag is set, it is triggered once all saved views become invisible. 

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

Type used on when the [FillResponse](FillResponse.md) represents a physical address (such as street, city, state, etc). 

 Value: 2

### SAVE_DATA_TYPE_CREDIT_CARD

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAVE_DATA_TYPE_CREDIT_CARD: Int
```

Type used when the [FillResponse](FillResponse.md) represents a credit card. 

 Value: 4

### SAVE_DATA_TYPE_DEBIT_CARD

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAVE_DATA_TYPE_DEBIT_CARD: Int
```

Type used when the [FillResponse](FillResponse.md) represents a debit card. 

 Value: 32

### SAVE_DATA_TYPE_EMAIL_ADDRESS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAVE_DATA_TYPE_EMAIL_ADDRESS: Int
```

Type used when the [FillResponse](FillResponse.md) represents just an email address, without a password. 

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

Type used when the [FillResponse](FillResponse.md) represents a card that does not a specified card or cannot identify what the card is for. 

 Value: 128

### SAVE_DATA_TYPE_PASSWORD

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAVE_DATA_TYPE_PASSWORD: Int
```

Type used when the [FillResponse](FillResponse.md) represents user credentials that have a password. 

 Value: 1

### SAVE_DATA_TYPE_PAYMENT_CARD

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAVE_DATA_TYPE_PAYMENT_CARD: Int
```

Type used when the [FillResponse](FillResponse.md) represents a payment card except for credit and debit cards. 

 Value: 64

### SAVE_DATA_TYPE_USERNAME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAVE_DATA_TYPE_USERNAME: Int
```

Type used when the [FillResponse](FillResponse.md) represents just an username, without a password. 

 Value: 8

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SaveInfo!>
```
