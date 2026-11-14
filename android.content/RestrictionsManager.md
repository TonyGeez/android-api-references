Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RestrictionsManager

```
open class RestrictionsManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.RestrictionsManager](https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#) |

Provides a mechanism for apps to query restrictions imposed by an entity that manages the user. Apps can also send permission requests to a local or remote device administrator to override default app-specific restrictions or any other operation that needs explicit authorization from the administrator.

Apps can expose a set of restrictions via an XML file specified in the manifest.

If the user has an active Restrictions Provider, dynamic requests can be made in addition to the statically imposed restrictions. Dynamic requests are app-specific and can be expressed via a predefined set of request types.

The RestrictionsManager forwards the dynamic requests to the active Restrictions Provider. The Restrictions Provider can respond back to requests by calling `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#notifyPermissionResponse(kotlin.String,%20android.os.PersistableBundle)`, when a response is received from the administrator of the device or user. The response is relayed back to the application via a protected broadcast, `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#ACTION_PERMISSION_RESPONSE_RECEIVED:kotlin.String`.

Static restrictions are specified by an XML file referenced by a meta-data attribute in the manifest. This enables applications as well as any web administration consoles to be able to read the list of available restrictions from the apk.

The syntax of the XML format is as follows:

```kotlin
<?xml version="1.0" encoding="utf-8"?>
  <restrictions xmlns:android="http://schemas.android.com/apk/res/android" >
      <restriction
          android:key="string"
          android:title="string resource"
          android:restrictionType=["bool" | "string" | "integer"
                                          | "choice" | "multi-select" | "hidden"
                                          | "bundle" | "bundle_array"]
          android:description="string resource"
          android:entries="string-array resource"
          android:entryValues="string-array resource"
          android:defaultValue="reference" >
              <restriction ... />
              ...
      </restriction>
      <restriction ... />
      ...
  </restrictions>
  
```

The attributes for each restriction depend on the restriction type.

- `key`, `title` and `restrictionType` are mandatory.
- `entries` and `entryValues` are required if `restrictionType ` is `choice` or `multi-select`.
- `defaultValue` is optional and its type depends on the `restrictionType`
- `hidden` type must have a `defaultValue` and will not be shown to the administrator. It can be used to pass along data that cannot be modified, such as a version code.
- `description` is meant to describe the restriction in more detail to the administrator controlling the values, if the title is not sufficient.

Only restrictions of type `bundle` and `bundle_array` can have one or multiple nested restriction elements.

In your manifest's `application` section, add the meta-data tag to point to the restrictions XML file as shown below:

```kotlin
<application ... >
      <meta-data android:name="android.content.APP_RESTRICTIONS"
                    android:resource="@xml/app_restrictions" />
      ...
  </application>
  
```

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#ACTION_PERMISSION_RESPONSE_RECEIVED:kotlin.String` Broadcast intent delivered when a response is received for a permission request. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#ACTION_REQUEST_LOCAL_APPROVAL:kotlin.String` Activity intent that is optionally implemented by the Restrictions Provider package to challenge for an administrator PIN or password locally on the device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#ACTION_REQUEST_PERMISSION:kotlin.String` Broadcast intent sent to the Restrictions Provider to handle a permission request from an app. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#EXTRA_PACKAGE_NAME:kotlin.String` The package name of the application making the request. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#EXTRA_REQUEST_BUNDLE:kotlin.String` The request bundle passed in the `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#ACTION_REQUEST_PERMISSION:kotlin.String` broadcast. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#EXTRA_REQUEST_ID:kotlin.String` The request ID passed in the `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#ACTION_REQUEST_PERMISSION:kotlin.String` broadcast. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#EXTRA_REQUEST_TYPE:kotlin.String` The request type passed in the `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#ACTION_REQUEST_PERMISSION:kotlin.String` broadcast. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#EXTRA_RESPONSE_BUNDLE:kotlin.String` Contains a response from the administrator for specific request. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#META_DATA_APP_RESTRICTIONS:kotlin.String` Name of the meta-data entry in the manifest that points to the XML file containing the application's available restrictions. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#REQUEST_KEY_APPROVE_LABEL:kotlin.String` Key for request approval button label contained in the request bundle. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#REQUEST_KEY_DATA:kotlin.String` Key for request data contained in the request bundle. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#REQUEST_KEY_DENY_LABEL:kotlin.String` Key for request rejection button label contained in the request bundle. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#REQUEST_KEY_ICON:kotlin.String` Key for request icon contained in the request bundle. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#REQUEST_KEY_ID:kotlin.String` Key for request ID contained in the request bundle. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#REQUEST_KEY_MESSAGE:kotlin.String` Key for request message contained in the request bundle. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#REQUEST_KEY_NEW_REQUEST:kotlin.String` Key for issuing a new request, contained in the request bundle. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#REQUEST_KEY_TITLE:kotlin.String` Key for request title contained in the request bundle. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#REQUEST_TYPE_APPROVAL:kotlin.String` Request type for a simple question, with a possible title and icon. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESPONSE_KEY_ERROR_CODE:kotlin.String` Key for the optional error code in the response bundle sent to the application. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESPONSE_KEY_MESSAGE:kotlin.String` Key for the optional message in the response bundle sent to the application. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESPONSE_KEY_RESPONSE_TIMESTAMP:kotlin.String` Key for the optional timestamp of when the administrator responded to the permission request. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESPONSE_KEY_RESULT:kotlin.String` Key for the response result in the response bundle sent to the application, for a permission request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESULT_APPROVED:kotlin.Int` Response result value indicating that the request was approved. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESULT_DENIED:kotlin.Int` Response result value indicating that the request was denied. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESULT_ERROR:kotlin.Int` Response result value indicating an error condition. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESULT_ERROR_BAD_REQUEST:kotlin.Int` Error code indicating that there was a problem with the request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESULT_ERROR_INTERNAL:kotlin.Int` Error code indicating that there was an internal error. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESULT_ERROR_NETWORK:kotlin.Int` Error code indicating that there was a problem with the network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESULT_NO_RESPONSE:kotlin.Int` Response result value indicating that the request has not received a response yet. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESULT_UNKNOWN_REQUEST:kotlin.Int` Response result value indicating that the request is unknown, when it's not a new request. |
| --- | --- |

| Public methods ||
|---|---|
| open static [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#convertRestrictionsToBundle(kotlin.collections.MutableList)(entries: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/RestrictionEntry!>!)` Converts a list of restrictions to the corresponding bundle, using the following mapping: | RestrictionEntry | Bundle | |---|---| | `https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_BOOLEAN:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle.html#putBoolean(kotlin.String,%20kotlin.Boolean)` | | `https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_CHOICE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_MULTI_SELECT:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle.html#putStringArray(kotlin.String,%20kotlin.Array)` | | `https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_INTEGER:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle.html#putInt(kotlin.String,%20kotlin.Int)` | | `https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_STRING:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle.html#putString(kotlin.String,%20kotlin.String)` | | `https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_BUNDLE:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/os/Bundle.html#putBundle(kotlin.String,%20android.os.Bundle)` | | `https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_BUNDLE_ARRAY:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/os/Bundle.html#putParcelableArray(kotlin.String,%20kotlin.Array)` | <br /> |
| open [Intent](https://developer.android.com/reference/kotlin/android/content/Intent)! | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#createLocalApprovalIntent()()` <br /> |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#getApplicationRestrictions()()` Returns any available set of application-specific restrictions applicable to this application. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!\> | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#getApplicationRestrictionsPerAdmin()()` Returns a `https://developer.android.com/reference/kotlin/java/util/List.html#` containing a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` for each managing agent that has set restrictions for the current application, the bundle contains any application restrictions set for the current package. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RestrictionEntry](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry)!\>! | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#getManifestRestrictions(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Parse and return the list of restrictions defined in the manifest for the specified package, if any. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#hasRestrictionsProvider()()` Called by an application to check if there is an active Restrictions Provider. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#notifyPermissionResponse(kotlin.String,%20android.os.PersistableBundle)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, response: https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#!)` Called by the Restrictions Provider to deliver a response to an application. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#requestPermission(kotlin.String,%20kotlin.String,%20android.os.PersistableBundle)(requestType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, requestId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, request: https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#!)` Called by an application to request permission for an operation. |

## Constants

### ACTION_PERMISSION_RESPONSE_RECEIVED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_PERMISSION_RESPONSE_RECEIVED: String
```

Broadcast intent delivered when a response is received for a permission request. The application should not interrupt the user by coming to the foreground if it isn't currently in the foreground. It can either post a notification informing the user of the response or wait until the next time the user launches the app.

For instance, if the user requested permission to make an in-app purchase, the app can post a notification that the request had been approved or denied.

The broadcast Intent carries the following extra: `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#EXTRA_RESPONSE_BUNDLE:kotlin.String`.

 Value: "android.content.action.PERMISSION_RESPONSE_RECEIVED"

### ACTION_REQUEST_LOCAL_APPROVAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_REQUEST_LOCAL_APPROVAL: String
```

Activity intent that is optionally implemented by the Restrictions Provider package to challenge for an administrator PIN or password locally on the device. Apps will call this intent using android.app.Activity#startActivityForResult. On a successful response, android.app.Activity#onActivityResult will return a resultCode of `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int`.

The intent must contain `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#EXTRA_REQUEST_BUNDLE:kotlin.String` as an extra and the bundle must contain at least `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#REQUEST_KEY_MESSAGE:kotlin.String` for the activity to display.

<br />

 Value: "android.content.action.REQUEST_LOCAL_APPROVAL"

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#createLocalApprovalIntent()`

### ACTION_REQUEST_PERMISSION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_REQUEST_PERMISSION: String
```

Broadcast intent sent to the Restrictions Provider to handle a permission request from an app. It will have the following extras: `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#EXTRA_PACKAGE_NAME:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#EXTRA_REQUEST_TYPE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#EXTRA_REQUEST_ID:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#EXTRA_REQUEST_BUNDLE:kotlin.String`. The Restrictions Provider will handle the request and respond back to the RestrictionsManager, when a response is available, by calling `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#notifyPermissionResponse(kotlin.String,%20android.os.PersistableBundle)`.

The BroadcastReceiver must require the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BIND_DEVICE_ADMIN:kotlin.String` permission to ensure that only the system can send the broadcast.

 Value: "android.content.action.REQUEST_PERMISSION"

### EXTRA_PACKAGE_NAME

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PACKAGE_NAME: String
```

The package name of the application making the request.

Type: String

 Value: "android.content.extra.PACKAGE_NAME"

### EXTRA_REQUEST_BUNDLE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_REQUEST_BUNDLE: String
```

The request bundle passed in the `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#ACTION_REQUEST_PERMISSION:kotlin.String` broadcast.

Type: `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#`

 Value: "android.content.extra.REQUEST_BUNDLE"

### EXTRA_REQUEST_ID

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_REQUEST_ID: String
```

The request ID passed in the `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#ACTION_REQUEST_PERMISSION:kotlin.String` broadcast.

Type: String

 Value: "android.content.extra.REQUEST_ID"

### EXTRA_REQUEST_TYPE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_REQUEST_TYPE: String
```

The request type passed in the `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#ACTION_REQUEST_PERMISSION:kotlin.String` broadcast.

Type: String

 Value: "android.content.extra.REQUEST_TYPE"

### EXTRA_RESPONSE_BUNDLE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_RESPONSE_BUNDLE: String
```

Contains a response from the administrator for specific request. The bundle contains the following information, at least:

- `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#REQUEST_KEY_ID:kotlin.String`: The request ID.
- `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESPONSE_KEY_RESULT:kotlin.String`: The response result.

<br />

Type: `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#`

 Value: "android.content.extra.RESPONSE_BUNDLE"

### META_DATA_APP_RESTRICTIONS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_DATA_APP_RESTRICTIONS: String
```

Name of the meta-data entry in the manifest that points to the XML file containing the application's available restrictions.

 Value: "android.content.APP_RESTRICTIONS"

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#getManifestRestrictions(kotlin.String)`

### REQUEST_KEY_APPROVE_LABEL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_KEY_APPROVE_LABEL: String
```

Key for request approval button label contained in the request bundle.

Optional, may be shown as a label on the positive button in a dialog or notification presented to the administrator who approves the request.

Type: String

 Value: "android.request.approve_label"

### REQUEST_KEY_DATA

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_KEY_DATA: String
```

Key for request data contained in the request bundle.

Optional, typically used to identify the specific data that is being referred to, such as the unique identifier for a movie or book. This is not used for display purposes and is more like a cookie. This value is returned in the `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#EXTRA_RESPONSE_BUNDLE:kotlin.String`.

Type: String

 Value: "android.request.data"

### REQUEST_KEY_DENY_LABEL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_KEY_DENY_LABEL: String
```

Key for request rejection button label contained in the request bundle.

Optional, may be shown as a label on the negative button in a dialog or notification presented to the administrator who approves the request.

Type: String

 Value: "android.request.deny_label"

### REQUEST_KEY_ICON

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_KEY_ICON: String
```

Key for request icon contained in the request bundle.

Optional, shown alongside the request message presented to the administrator who approves the request. The content must be a compressed image such as a PNG or JPEG, as a byte array.

Type: byte\[\]

 Value: "android.request.icon"

### REQUEST_KEY_ID

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_KEY_ID: String
```

Key for request ID contained in the request bundle.

App-generated request ID to identify the specific request when receiving a response. This value is returned in the `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#EXTRA_RESPONSE_BUNDLE:kotlin.String`.

Type: String

 Value: "android.request.id"

### REQUEST_KEY_MESSAGE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_KEY_MESSAGE: String
```

Key for request message contained in the request bundle.

Required, shown as the actual message in a notification or dialog presented to the administrator who approves the request.

Type: String

 Value: "android.request.mesg"

### REQUEST_KEY_NEW_REQUEST

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_KEY_NEW_REQUEST: String
```

Key for issuing a new request, contained in the request bundle. If this is set to true, the Restrictions Provider must make a new request. If it is false or not specified, then the Restrictions Provider can return a cached response that has the same requestId, if available. If there's no cached response, it will issue a new one to the administrator.

Type: boolean

 Value: "android.request.new_request"

### REQUEST_KEY_TITLE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_KEY_TITLE: String
```

Key for request title contained in the request bundle.

Optional, typically used as the title of any notification or dialog presented to the administrator who approves the request.

Type: String

 Value: "android.request.title"

### REQUEST_TYPE_APPROVAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_TYPE_APPROVAL: String
```

Request type for a simple question, with a possible title and icon.

Required keys are: `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#REQUEST_KEY_MESSAGE:kotlin.String`

Optional keys are `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#REQUEST_KEY_DATA:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#REQUEST_KEY_ICON:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#REQUEST_KEY_TITLE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#REQUEST_KEY_APPROVE_LABEL:kotlin.String` and `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#REQUEST_KEY_DENY_LABEL:kotlin.String`.

 Value: "android.request.type.approval"

### RESPONSE_KEY_ERROR_CODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESPONSE_KEY_ERROR_CODE: String
```

Key for the optional error code in the response bundle sent to the application.

Type: int

Possible values: `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESULT_ERROR_BAD_REQUEST:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESULT_ERROR_NETWORK:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESULT_ERROR_INTERNAL:kotlin.Int`.

 Value: "android.response.errorcode"

### RESPONSE_KEY_MESSAGE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESPONSE_KEY_MESSAGE: String
```

Key for the optional message in the response bundle sent to the application.

Type: String

 Value: "android.response.msg"

### RESPONSE_KEY_RESPONSE_TIMESTAMP

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESPONSE_KEY_RESPONSE_TIMESTAMP: String
```

Key for the optional timestamp of when the administrator responded to the permission request. It is an represented in milliseconds since January 1, 1970 00:00:00.0 UTC.

Type: long

 Value: "android.response.timestamp"

### RESPONSE_KEY_RESULT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESPONSE_KEY_RESULT: String
```

Key for the response result in the response bundle sent to the application, for a permission request. It indicates the status of the request. In some cases an additional message might be available in `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESPONSE_KEY_MESSAGE:kotlin.String`, to be displayed to the user.

Type: int

Possible values: `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESULT_APPROVED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESULT_DENIED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESULT_NO_RESPONSE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESULT_UNKNOWN_REQUEST:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESULT_ERROR:kotlin.Int`.

 Value: "android.response.result"

### RESULT_APPROVED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_APPROVED: Int
```

Response result value indicating that the request was approved.

 Value: 1

### RESULT_DENIED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_DENIED: Int
```

Response result value indicating that the request was denied.

 Value: 2

### RESULT_ERROR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_ERROR: Int
```

Response result value indicating an error condition. Additional error code might be available in the response bundle, for the key `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESPONSE_KEY_ERROR_CODE:kotlin.String`. There might also be an associated error message in the response bundle, for the key `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESPONSE_KEY_MESSAGE:kotlin.String`.

 Value: 5

### RESULT_ERROR_BAD_REQUEST

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_ERROR_BAD_REQUEST: Int
```

Error code indicating that there was a problem with the request.

Stored in `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESPONSE_KEY_ERROR_CODE:kotlin.String` field in the response bundle.

 Value: 1

### RESULT_ERROR_INTERNAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_ERROR_INTERNAL: Int
```

Error code indicating that there was an internal error.

Stored in `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESPONSE_KEY_ERROR_CODE:kotlin.String` field in the response bundle.

 Value: 3

### RESULT_ERROR_NETWORK

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_ERROR_NETWORK: Int
```

Error code indicating that there was a problem with the network.

Stored in `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#RESPONSE_KEY_ERROR_CODE:kotlin.String` field in the response bundle.

 Value: 2

### RESULT_NO_RESPONSE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_NO_RESPONSE: Int
```

Response result value indicating that the request has not received a response yet.

 Value: 3

### RESULT_UNKNOWN_REQUEST

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_UNKNOWN_REQUEST: Int
```

Response result value indicating that the request is unknown, when it's not a new request.

 Value: 4

## Public methods

### convertRestrictionsToBundle

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun convertRestrictionsToBundle(entries: MutableList<RestrictionEntry!>!): Bundle!
```

Converts a list of restrictions to the corresponding bundle, using the following mapping:

| RestrictionEntry | Bundle |
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_BOOLEAN:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle.html#putBoolean(kotlin.String,%20kotlin.Boolean)` |
| `https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_CHOICE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_MULTI_SELECT:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle.html#putStringArray(kotlin.String,%20kotlin.Array)` |
| `https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_INTEGER:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle.html#putInt(kotlin.String,%20kotlin.Int)` |
| --- | --- |
| `https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_STRING:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/os/BaseBundle.html#putString(kotlin.String,%20kotlin.String)` |
| `https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_BUNDLE:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/os/Bundle.html#putBundle(kotlin.String,%20android.os.Bundle)` |
| `https://developer.android.com/reference/kotlin/android/content/RestrictionEntry#TYPE_BUNDLE_ARRAY:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/os/Bundle.html#putParcelableArray(kotlin.String,%20kotlin.Array)` |
| --- | --- |

<br />

| Parameters ||
|---|---|
| `entries` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RestrictionEntry](https://developer.android.com/reference/kotlin/android/content/RestrictionEntry)!\>!: list of restrictions |

### createLocalApprovalIntent

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createLocalApprovalIntent(): Intent!
```

### getApplicationRestrictions

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getApplicationRestrictions(): Bundle!
```

Returns any available set of application-specific restrictions applicable to this application.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | the application restrictions as a Bundle. Returns null if there are no restrictions. Starting from Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, it is possible for there to be multiple managing apps on the device with the ability to set restrictions, e.g. a Device Policy Controller (DPC) and a Supervision admin. This API will only return the restrictions set by the DPCs. To retrieve restrictions set by all managing apps, use `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#getApplicationRestrictionsPerAdmin()` instead. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#`

### getApplicationRestrictionsPerAdmin

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getApplicationRestrictionsPerAdmin(): MutableList<Bundle!>
```

Returns a `https://developer.android.com/reference/kotlin/java/util/List.html#` containing a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` for each managing agent that has set restrictions for the current application, the bundle contains any application restrictions set for the current package. The order of the items in the list is not guaranteed to remain stable between multiple calls.

Starting from Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, it is possible for there to be multiple managing apps on the device with the ability to set restrictions, e.g. an Enterprise Device Policy Controller (DPC) and a Supervision admin.

Each `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` consists of key-value pairs, as defined by the application, where the types of values may be:

- `boolean`
- `int`
- `String` or `String[]`
- From `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, `Bundle` or `Bundle[]`

NOTE: The method performs disk I/O and shouldn't be called on the main thread. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!>` | a `https://developer.android.com/reference/kotlin/java/util/List.html#` of `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` containing the restrictions set by admins for that package. Returns an empty `https://developer.android.com/reference/kotlin/java/util/List.html#` if there are no saved restrictions. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/UserManager.html#KEY_RESTRICTIONS_PENDING:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#`

### getManifestRestrictions

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getManifestRestrictions(packageName: String!): MutableList<RestrictionEntry!>!
```

Parse and return the list of restrictions defined in the manifest for the specified package, if any.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The application for which to fetch the restrictions list. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/RestrictionEntry!>!` | The list of RestrictionEntry objects created from the XML file specified in the manifest, or null if none was specified. |

### hasRestrictionsProvider

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasRestrictionsProvider(): Boolean
```

Called by an application to check if there is an active Restrictions Provider. If there isn't, `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager#requestPermission(kotlin.String,%20kotlin.String,%20android.os.PersistableBundle)` is not available.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | whether there is an active Restrictions Provider. |

### notifyPermissionResponse

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun notifyPermissionResponse(
    packageName: String!, 
    response: PersistableBundle!
): Unit
```

Called by the Restrictions Provider to deliver a response to an application.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the application to deliver the response to. Cannot be null. |
| `response` | [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#)!: the bundle containing the response status, request ID and other information. Cannot be null. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if any of the required parameters are missing. |

### requestPermission

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestPermission(
    requestType: String!, 
    requestId: String!, 
    request: PersistableBundle!
): Unit
```

Called by an application to request permission for an operation. The contents of the request are passed in a Bundle that contains several pieces of data depending on the chosen request type.

| Parameters ||
|---|---|
| `requestType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The type of request. The type could be one of the predefined types specified here or a custom type that the specific Restrictions Provider might understand. For custom types, the type name should be namespaced to avoid collisions with predefined types and types specified by other Restrictions Providers. |
| `requestId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A unique id generated by the app that contains sufficient information to identify the parameters of the request when it receives the id in the response. |
| `request` | [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#)!: A PersistableBundle containing the data corresponding to the specified request type. The keys for the data in the bundle depend on the request type. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if any of the required parameters are missing. |
