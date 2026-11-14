# AssistContent

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AssistContent

Kotlin| [Java](https://developer.android.com/reference/android/app/assist/AssistContent "View this page in Java") 

```
open class AssistContent : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.assist.AssistContent](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#) |

Holds information about the content an application is viewing, to hand to an assistant at the user's request. This is filled in by [Activity.onProvideAssistContent](https://developer.android.com/reference/kotlin/android/app/Activity.html#onProvideAssistContent(android.app.assist.AssistContent)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_APP_FUNCTION_DATA](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#EXTRA_APP_FUNCTION_DATA:kotlin.String) Extra for a [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) that provides contextual AppFunction's information about the content currently being viewed in the application. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------|---|
| [AssistContent](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#AssistContent())`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#describeContents())`()` <br /> |
| open [ClipData](https://developer.android.com/reference/kotlin/android/content/ClipData.html#)! | [getClipData](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#getClipData())`()` Return the current [setClipData](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#setClipData(android.content.ClipData)), which you can modify in-place. |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [getExtras](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#getExtras())`()` Return Bundle for extra vendor-specific data that can be modified and examined. |
| open [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)! | [getIntent](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#getIntent())`()` Returns the current [setIntent](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#setIntent(android.content.Intent))if one is set, else the default Intent obtained from [Activity.getIntent](https://developer.android.com/reference/kotlin/android/app/Activity.html#getIntent()). |
| open [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [getSessionTransferUri](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#getSessionTransferUri())`()` Return the content's session transfer web URI as per [setSessionTransferUri(android.net.Uri)](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#setSessionTransferUri(android.net.Uri)), or null if there is none. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getStructuredData](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#getStructuredData())`()` Returns the current [setStructuredData](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#setStructuredData(kotlin.String)). |
| open [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | [getWebUri](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#getWebUri())`()` Return the content's web URI as per [setWebUri(android.net.Uri)](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#setWebUri(android.net.Uri)), or null if there is none. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAppProvidedIntent](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#isAppProvidedIntent())`()` Returns whether or not the current Intent was explicitly provided in [Activity.onProvideAssistContent](https://developer.android.com/reference/kotlin/android/app/Activity.html#onProvideAssistContent(android.app.assist.AssistContent)). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAppProvidedWebUri](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#isAppProvidedWebUri())`()` Returns whether or not the current [getWebUri](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#getWebUri())was explicitly provided in [Activity.onProvideAssistContent](https://developer.android.com/reference/kotlin/android/app/Activity.html#onProvideAssistContent(android.app.assist.AssistContent)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClipData](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#setClipData(android.content.ClipData))`(`clip:` ` [ClipData](https://developer.android.com/reference/kotlin/android/content/ClipData.html#)!`)` Optional additional content items that are involved with the current UI. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIntent](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#setIntent(android.content.Intent))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` Sets the Intent associated with the content, describing the current top-level context of the activity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSessionTransferUri](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#setSessionTransferUri(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?`)` This method can be used to provide a [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) which will be utilized when transitioning a user's session to another surface. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStructuredData](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#setStructuredData(kotlin.String))`(`structuredData:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets optional structured data regarding the content being viewed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWebUri](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#setWebUri(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`)` Set a web URI associated with the current data being shown to the user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AssistContent](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### EXTRA_APP_FUNCTION_DATA

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_APP_FUNCTION_DATA: String
```

Extra for a [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) that provides contextual AppFunction's information about the content currently being viewed in the application.

This extra can be optionally supplied in the [AssistContent.getExtras()](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#getExtras())bundle.

The schema of the [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) in this extra is defined in the AppFunction SDK. 

 Value: "android.app.assist.extra.APP_FUNCTION_DATA"

**See Also**

- [android.app.appfunctions.AppFunctionManager](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager.html#)

## Public constructors

### AssistContent

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AssistContent()
```

## Public methods

### describeContents

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getClipData

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getClipData(): ClipData!
```

Return the current [setClipData](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#setClipData(android.content.ClipData)), which you can modify in-place. 

### getExtras

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExtras(): Bundle!
```

Return Bundle for extra vendor-specific data that can be modified and examined. 

### getIntent

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIntent(): Intent!
```

Returns the current [setIntent](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#setIntent(android.content.Intent))if one is set, else the default Intent obtained from [Activity.getIntent](https://developer.android.com/reference/kotlin/android/app/Activity.html#getIntent()). Can be modified in-place. 

### getSessionTransferUri

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSessionTransferUri(): Uri?
```

Return the content's session transfer web URI as per [setSessionTransferUri(android.net.Uri)](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#setSessionTransferUri(android.net.Uri)), or null if there is none. 

### getStructuredData

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStructuredData(): String!
```

Returns the current [setStructuredData](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#setStructuredData(kotlin.String)). 

### getWebUri

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWebUri(): Uri!
```

Return the content's web URI as per [setWebUri(android.net.Uri)](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#setWebUri(android.net.Uri)), or null if there is none. 

### isAppProvidedIntent

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAppProvidedIntent(): Boolean
```

Returns whether or not the current Intent was explicitly provided in [Activity.onProvideAssistContent](https://developer.android.com/reference/kotlin/android/app/Activity.html#onProvideAssistContent(android.app.assist.AssistContent)). If not, the Intent was automatically set based on [Activity.getIntent](https://developer.android.com/reference/kotlin/android/app/Activity.html#getIntent()). 

### isAppProvidedWebUri

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAppProvidedWebUri(): Boolean
```

Returns whether or not the current [getWebUri](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#getWebUri())was explicitly provided in [Activity.onProvideAssistContent](https://developer.android.com/reference/kotlin/android/app/Activity.html#onProvideAssistContent(android.app.assist.AssistContent)). If not, the Intent was automatically set based on [Activity.getIntent](https://developer.android.com/reference/kotlin/android/app/Activity.html#getIntent()). 

### setClipData

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setClipData(clip: ClipData!): Unit
```

Optional additional content items that are involved with the current UI. Access to this content will be granted to the assistant as if you are sending it through an Intent with [Intent.FLAG_GRANT_READ_URI_PERMISSION](https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int). 

### setIntent

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIntent(intent: Intent!): Unit
```

Sets the Intent associated with the content, describing the current top-level context of the activity. If this contains a reference to a piece of data related to the activity, be sure to set [Intent.FLAG_GRANT_READ_URI_PERMISSION](https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int) so the accessibility service can access it. 

### setSessionTransferUri

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSessionTransferUri(uri: Uri?): Unit
```

This method can be used to provide a [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) which will be utilized when transitioning a user's session to another surface.

If provided, instead of using the URI provided in [setWebUri](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#setWebUri(android.net.Uri)), the "Open in browser" feature will use this URI to transition the current session from one surface to the other. Apps may choose to encode session or user information into this URI in order to provide a better session transfer experience. However, while this URI will only be available to the system and not other applications, developers should not encode authentication credentials into this URI, because it will be surfaced in the browser URL bar and may be copied and shared from there.

When providing this URI, developers should still continue to provide [setWebUri](https://developer.android.com/reference/kotlin/android/app/assist/AssistContent#setWebUri(android.net.Uri))for backwards compatibility with features such as [recents URL sharing](https://developer.android.com/guide/components/activities/recents#url-sharing) which facilitate link sharing with other users and would not benefit from a session-transfer URI.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?:This value may be`null`. |

**See Also**

- [android.app.Activity#requestOpenInBrowserEducation()](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestOpenInBrowserEducation()) 

### setStructuredData

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStructuredData(structuredData: String!): Unit
```

Sets optional structured data regarding the content being viewed. The provided data must be a string represented with [JSON-LD](http://json-ld.org/) using the [schema.org](http://schema.org/) vocabulary. 

### setWebUri

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setWebUri(uri: Uri!): Unit
```

Set a web URI associated with the current data being shown to the user. This URI could be opened in a web browser, or in the app as an [Intent.ACTION_VIEW](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_VIEW:kotlin.String) Intent, to show the same data that is currently being displayed by it. The URI here should be something that is transportable off the device into other environments to acesss the same data as is currently being shown in the app; if the app does not have such a representation, it should leave the null and only report the local intent and clip data. 

### writeToParcel

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AssistContent!>
```
