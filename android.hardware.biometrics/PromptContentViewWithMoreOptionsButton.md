# PromptContentViewWithMoreOptionsButton

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PromptContentViewWithMoreOptionsButton

Kotlin| [Java](https://developer.android.com/reference/android/hardware/biometrics/PromptContentViewWithMoreOptionsButton "View this page in Java") 

```
class PromptContentViewWithMoreOptionsButton : Parcelable, PromptContentView
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.hardware.biometrics.PromptContentViewWithMoreOptionsButton](https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptContentViewWithMoreOptionsButton#) |

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
| | [Builder](https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptContentViewWithMoreOptionsButton.Builder) A builder that collects arguments to be shown on the content view with more options button. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptContentViewWithMoreOptionsButton#describeContents())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getDescription](https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptContentViewWithMoreOptionsButton#getDescription())`()` Gets the description for the content view, as set by [PromptContentViewWithMoreOptionsButton.Builder.setDescription(String)](https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptContentViewWithMoreOptionsButton.Builder#setDescription(kotlin.String)). |
| [DialogInterface.OnClickListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnClickListener.html#) | [getMoreOptionsButtonListener](https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptContentViewWithMoreOptionsButton#getMoreOptionsButtonListener())`()` Gets the click listener for the more options button on the content view, as set by [PromptContentViewWithMoreOptionsButton.Builder.setMoreOptionsButtonListener(Executor,](https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptContentViewWithMoreOptionsButton.Builder#setMoreOptionsButtonListener(java.util.concurrent.Executor,%20android.content.DialogInterface.OnClickListener)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptContentViewWithMoreOptionsButton#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [PromptContentViewWithMoreOptionsButton](https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptContentViewWithMoreOptionsButton#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptContentViewWithMoreOptionsButton#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getDescription

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDescription(): String?
```

Gets the description for the content view, as set by [PromptContentViewWithMoreOptionsButton.Builder.setDescription(String)](https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptContentViewWithMoreOptionsButton.Builder#setDescription(kotlin.String)). 
Requires [android.Manifest.permission#SET_BIOMETRIC_DIALOG_ADVANCED](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_BIOMETRIC_DIALOG_ADVANCED:kotlin.String)

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | The description for the content view, or null if the content view has no description. |

### getMoreOptionsButtonListener

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMoreOptionsButtonListener(): DialogInterface.OnClickListener
```

Gets the click listener for the more options button on the content view, as set by [PromptContentViewWithMoreOptionsButton.Builder.setMoreOptionsButtonListener(Executor,](https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptContentViewWithMoreOptionsButton.Builder#setMoreOptionsButtonListener(java.util.concurrent.Executor,%20android.content.DialogInterface.OnClickListener)). 
Requires [android.Manifest.permission#SET_BIOMETRIC_DIALOG_ADVANCED](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_BIOMETRIC_DIALOG_ADVANCED:kotlin.String)

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [DialogInterface.OnClickListener](https://developer.android.com/reference/kotlin/android/content/DialogInterface.OnClickListener.html#) | The click listener for the more options button on the content view. This value cannot be`null`. |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<PromptContentViewWithMoreOptionsButton!>
```  
**See Also**

- [android.os.Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)
