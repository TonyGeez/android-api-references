# PromptContentViewWithMoreOptionsButton

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PromptContentViewWithMoreOptionsButton

Kotlin| [Java](../android/hardware/biometrics/PromptContentViewWithMoreOptionsButton.md) 
| --- | --- |

```
class PromptContentViewWithMoreOptionsButton : Parcelable, PromptContentView
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.biometrics.PromptContentViewWithMoreOptionsButton](../android/hardware/biometrics/PromptContentViewWithMoreOptionsButton.md) |

Contains the information of the template of content view with a more options button for Biometric Prompt.

This button should be used to provide more options for sign in or other purposes, such as when a user needs to select between multiple app-specific accounts or profiles that are available for sign in.

Apps should avoid using this when possible because it will create additional steps that the user must navigate through - clicking the more options button will dismiss the prompt, provide the app an opportunity to ask the user for the correct option, and finally allow the app to decide how to proceed once selected.

Here's how you'd set a`PromptContentViewWithMoreOptionsButton`on a Biometric Prompt: 

```kotlin
BiometricPrompt biometricPrompt = new BiometricPrompt.Builder(...)
      .setTitle(...)
      .setSubTitle(...)
      .setContentView(new PromptContentViewWithMoreOptionsButton.Builder()
          .setDescription("test description")
          .setMoreOptionsButtonListener(executor, listener)
          .build())
      .build();
  
```

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/hardware/biometrics/PromptContentViewWithMoreOptionsButton.Builder.md) A builder that collects arguments to be shown on the content view with more options button. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/hardware/biometrics/PromptContentViewWithMoreOptionsButton.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getDescription](../android/hardware/biometrics/PromptContentViewWithMoreOptionsButton.md))`()` Gets the description for the content view, as set by [PromptContentViewWithMoreOptionsButton.Builder.setDescription(String)](../android/hardware/biometrics/PromptContentViewWithMoreOptionsButton.Builder.md)). |
| [DialogInterface.OnClickListener](../android/content/DialogInterface.OnClickListener.md) | [getMoreOptionsButtonListener](../android/hardware/biometrics/PromptContentViewWithMoreOptionsButton.md))`()` Gets the click listener for the more options button on the content view, as set by [PromptContentViewWithMoreOptionsButton.Builder.setMoreOptionsButtonListener(Executor,](../android/hardware/biometrics/PromptContentViewWithMoreOptionsButton.Builder.md)). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/hardware/biometrics/PromptContentViewWithMoreOptionsButton.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PromptContentViewWithMoreOptionsButton](../android/hardware/biometrics/PromptContentViewWithMoreOptionsButton.md)!\> | [CREATOR](../android/hardware/biometrics/PromptContentViewWithMoreOptionsButton.md) <br /> |

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getDescription

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDescription(): String?
```

Gets the description for the content view, as set by [PromptContentViewWithMoreOptionsButton.Builder.setDescription(String)](../android/hardware/biometrics/PromptContentViewWithMoreOptionsButton.Builder.md)). 
Requires [android.Manifest.permission#SET_BIOMETRIC_DIALOG_ADVANCED](../android/Manifest.permission.md)

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | The description for the content view, or null if the content view has no description. |

### getMoreOptionsButtonListener

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMoreOptionsButtonListener(): DialogInterface.OnClickListener
```

Gets the click listener for the more options button on the content view, as set by [PromptContentViewWithMoreOptionsButton.Builder.setMoreOptionsButtonListener(Executor,](../android/hardware/biometrics/PromptContentViewWithMoreOptionsButton.Builder.md)). 
Requires [android.Manifest.permission#SET_BIOMETRIC_DIALOG_ADVANCED](../android/Manifest.permission.md)

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [DialogInterface.OnClickListener](../android/content/DialogInterface.OnClickListener.md) | The click listener for the more options button on the content view. This value cannot be`null`. |

### writeToParcel

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<PromptContentViewWithMoreOptionsButton!>
```  
**See Also**

- [android.os.Parcelable.Creator](../android/os/Parcelable.Creator.md)
