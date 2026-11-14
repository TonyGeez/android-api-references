# Dataset

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Dataset

Kotlin| [Java](../android/service/autofill/Dataset.md) 
| --- | --- |

```
class Dataset : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.autofill.Dataset](../android/service/autofill/Dataset.md) |

A`Dataset`object represents a group of fields (key / value pairs) used to autofill parts of a screen.

For more information about the role of datasets in the autofill workflow, read [Build autofill services](../guide/topics/text/autofill-services.md) and the [AutofillService](../reference/android/service/autofill/AutofillService.md) documentation.

### Basic usage

In its simplest form, a dataset contains one or more fields (comprised of an [id](../android/view/autofill/AutofillId.md), a [value](../android/view/autofill/AutofillValue.md), and an optional filter [regex](../java/util/regex/Pattern.md)); and one or more [presentations](../android/widget/RemoteViews.md) for these fields (each field could have its own [presentation](../android/widget/RemoteViews.md), or use the default [presentation](../android/widget/RemoteViews.md) associated with the whole dataset).

When an autofill service returns datasets in a [FillResponse](../android/service/autofill/FillResponse.md) and the screen input is focused in a view that is present in at least one of these datasets, the Android System displays a UI containing the [presentation](../android/widget/RemoteViews.md) of all datasets pairs that have that view's [AutofillId](../android/view/autofill/AutofillId.md). Then, when the user selects a dataset from the UI, all views in that dataset are autofilled.

If both the current Input Method and autofill service supports inline suggestions, the Dataset can be shown by the keyboard as a suggestion. To use this feature, the Dataset should contain an [InlinePresentation](../android/service/autofill/InlinePresentation.md) representing how the inline suggestion UI will be rendered.

### Fill Dialog UI

The fill dialog UI is a more conspicuous and efficient interface than dropdown UI. If autofill suggestions are available when the user clicks on a field that supports filling the dialog UI, Autofill will pop up a fill dialog. The dialog will take up a larger area to display the datasets, so it is easy for users to pay attention to the datasets and selecting a dataset. If the user focuses on the view before suggestions are available, will fall back to dropdown UI or inline suggestions.

### Dataset authentication

In a more sophisticated form, the dataset values can be protected until the user authenticates the dataset---in that case, when a dataset is selected by the user, the Android System launches an intent set by the service to "unlock" the dataset.

For example, when a data set contains credit card information (such as number, expiration date, and verification code), you could provide a dataset presentation saying "Tap to authenticate". Then when the user taps that option, you would launch an activity asking the user to enter the credit card code, and if the user enters a valid code, you could then "unlock" the dataset.

You can also use authenticated datasets to offer an interactive UI for the user. For example, if the activity being autofilled is an account creation screen, you could use an authenticated dataset to automatically generate a random password for the user.

See [Dataset.Builder.setAuthentication(IntentSender)](../android/service/autofill/Dataset.Builder.md))for more details about the dataset authentication mechanism.

### Filtering

The autofill UI automatically changes which values are shown based on value of the view anchoring it, following the rules below:

1. If the view's [autofill value](../android/view/View.md))is not [text](../android/view/autofill/AutofillValue.md))or is empty, all datasets are shown.
2. Datasets that have a filter regex (set through [Field.Builder.setFilter(Pattern)](../android/service/autofill/Field.Builder.md))and [Dataset.Builder.setField(AutofillId, Field)](../android/service/autofill/Dataset.Builder.md))) and whose regex matches the view's text value converted to lower case are shown.
3. Datasets that do not require authentication, have a field value that is [text](../android/view/autofill/AutofillValue.md))and whose [value](../android/view/autofill/AutofillValue.md))starts with the lower case value of the view's text are shown.
4. All other datasets are hidden.

Note: If user enters four or more characters, all datasets will be hidden

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/service/autofill/Dataset.Builder.md) A builder for [Dataset](../android/service/autofill/Dataset.md) objects. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/service/autofill/Dataset.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/service/autofill/Dataset.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/service/autofill/Dataset.md))`(`parcel:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Dataset](../android/service/autofill/Dataset.md)!\> | [CREATOR](../android/service/autofill/Dataset.md) <br /> |

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Dataset!>
```
