# PermissionRequest

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PermissionRequest

Kotlin| [Java](https://developer.android.com/reference/android/webkit/PermissionRequest "View this page in Java") 
| --- | --- |

```
abstract class PermissionRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.PermissionRequest](https://developer.android.com/reference/kotlin/android/webkit/PermissionRequest#) |

This class defines a permission request and is used when web content requests access to protected resources. The permission request related events are delivered via [WebChromeClient.onPermissionRequest](https://developer.android.com/reference/kotlin/android/webkit/WebChromeClient#onPermissionRequest(android.webkit.PermissionRequest))and [WebChromeClient.onPermissionRequestCanceled](https://developer.android.com/reference/kotlin/android/webkit/WebChromeClient#onPermissionRequestCanceled(android.webkit.PermissionRequest)). Either [grant()](https://developer.android.com/reference/kotlin/android/webkit/PermissionRequest#grant(kotlin.Array))or [deny()](https://developer.android.com/reference/kotlin/android/webkit/PermissionRequest#deny())must be called in UI thread to respond to the request. New protected resources whose names are not defined here may be requested in future versions of WebView, even when running on an older Android release. To avoid unintentionally granting requests for new permissions, you should pass the specific permissions you intend to grant to [grant()](https://developer.android.com/reference/kotlin/android/webkit/PermissionRequest#grant(kotlin.Array)), and avoid writing code like this example: 

```kotlin
permissionRequest.grant(permissionRequest.getResources())  // This is wrong!!!
  
```
See the WebView's release notes for information about new protected resources.

<br />

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RESOURCE_AUDIO_CAPTURE](https://developer.android.com/reference/kotlin/android/webkit/PermissionRequest#RESOURCE_AUDIO_CAPTURE:kotlin.String) Resource belongs to audio capture device, like microphone. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RESOURCE_MIDI_SYSEX](https://developer.android.com/reference/kotlin/android/webkit/PermissionRequest#RESOURCE_MIDI_SYSEX:kotlin.String) Resource will allow sysex messages to be sent to or received from MIDI devices. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RESOURCE_PROTECTED_MEDIA_ID](https://developer.android.com/reference/kotlin/android/webkit/PermissionRequest#RESOURCE_PROTECTED_MEDIA_ID:kotlin.String) Resource belongs to protected media identifier. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RESOURCE_VIDEO_CAPTURE](https://developer.android.com/reference/kotlin/android/webkit/PermissionRequest#RESOURCE_VIDEO_CAPTURE:kotlin.String) Resource belongs to video capture device, like camera. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------|---|
| [PermissionRequest](https://developer.android.com/reference/kotlin/android/webkit/PermissionRequest#PermissionRequest())`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deny](https://developer.android.com/reference/kotlin/android/webkit/PermissionRequest#deny())`()` Call this method to deny the request. |
| abstract [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | [getOrigin](https://developer.android.com/reference/kotlin/android/webkit/PermissionRequest#getOrigin())`()` Call this method to get the origin of the web page which is trying to access the restricted resources. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getResources](https://developer.android.com/reference/kotlin/android/webkit/PermissionRequest#getResources())`()` Call this method to get the resources the web page is trying to access. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [grant](https://developer.android.com/reference/kotlin/android/webkit/PermissionRequest#grant(kotlin.Array))`(`resources:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Call this method to grant origin the permission to access the given resources. |

## Constants

### RESOURCE_AUDIO_CAPTURE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESOURCE_AUDIO_CAPTURE: String
```

Resource belongs to audio capture device, like microphone. 

 Value: "android.webkit.resource.AUDIO_CAPTURE"

### RESOURCE_MIDI_SYSEX

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESOURCE_MIDI_SYSEX: String
```

Resource will allow sysex messages to be sent to or received from MIDI devices. These messages are privileged operations, e.g. modifying sound libraries and sampling data, or even updating the MIDI device's firmware. Permission may be requested for this resource in API levels 21 and above, if the Android device has been updated to WebView 45 or above. 

 Value: "android.webkit.resource.MIDI_SYSEX"

### RESOURCE_PROTECTED_MEDIA_ID

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESOURCE_PROTECTED_MEDIA_ID: String
```

Resource belongs to protected media identifier. After the user grants this resource, the origin can use EME APIs to generate the license requests. 

 Value: "android.webkit.resource.PROTECTED_MEDIA_ID"

### RESOURCE_VIDEO_CAPTURE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESOURCE_VIDEO_CAPTURE: String
```

Resource belongs to video capture device, like camera. 

 Value: "android.webkit.resource.VIDEO_CAPTURE"

## Public constructors

### PermissionRequest

```
PermissionRequest()
```

## Public methods

### deny

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun deny(): Unit
```

Call this method to deny the request. 

### getOrigin

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getOrigin(): Uri!
```

Call this method to get the origin of the web page which is trying to access the restricted resources.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | the origin of web content which attempt to access the restricted resources. |

### getResources

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getResources(): Array<String!>!
```

Call this method to get the resources the web page is trying to access.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the array of resources the web content wants to access. |

### grant

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun grant(resources: Array<String!>!): Unit
```

Call this method to grant origin the permission to access the given resources. The granted permission is only valid for this WebView.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resources` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the resources granted to be accessed by origin, to grant request, the requested resources returned by [getResources()](https://developer.android.com/reference/kotlin/android/webkit/PermissionRequest#getResources())must be equals or a subset of granted resources. This parameter is designed to avoid granting permission by accident especially when new resources are requested by web content. |
