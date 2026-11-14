# AutofillManager

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AutofillManager

Kotlin| [Java](https://developer.android.com/reference/android/view/autofill/AutofillManager "View this page in Java") 
| --- | --- |

```
class AutofillManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.autofill.AutofillManager](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#) |

The [AutofillManager](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#) class provides ways for apps and custom views to integrate with the Autofill Framework lifecycle.

To learn about using Autofill in your app, read the [Autofill Framework](https://developer.android.com/reference/kotlin/guide/topics/text/autofill) guides.

### Autofill lifecycle

The autofill lifecycle starts with the creation of an autofill context associated with an activity context. The autofill context is created when one of the following methods is called for the first time in an activity context, and the current user has an enabled autofill service:

- [notifyViewEntered(android.view.View)](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#notifyViewEntered(android.view.View))
- [notifyViewEntered(android.view.View,int,android.graphics.Rect)](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#notifyViewEntered(android.view.View,%20kotlin.Int,%20android.graphics.Rect))
- [requestAutofill(android.view.View)](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#requestAutofill(android.view.View))

Typically, the context is automatically created when the first view of the activity is focused because`View.onFocusChanged()`indirectly calls [notifyViewEntered(android.view.View)](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#notifyViewEntered(android.view.View)). App developers can call [requestAutofill(android.view.View)](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#requestAutofill(android.view.View))to explicitly create it (for example, a custom view developer could offer a contextual menu action in a text-field view to let users manually request autofill).

After the context is created, the Android System creates a [android.view.ViewStructure](https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#) that represents the view hierarchy by calling [View.dispatchProvideAutofillStructure(android.view.ViewStructure, int)](https://developer.android.com/reference/kotlin/android/view/View.html#dispatchProvideAutofillStructure(android.view.ViewStructure,%20kotlin.Int))in the root views of all application windows. By default,`dispatchProvideAutofillStructure()`results in subsequent calls to [View.onProvideAutofillStructure(android.view.ViewStructure, int)](https://developer.android.com/reference/kotlin/android/view/View.html#onProvideAutofillStructure(android.view.ViewStructure,%20kotlin.Int))and [View.onProvideAutofillVirtualStructure(android.view.ViewStructure, int)](https://developer.android.com/reference/kotlin/android/view/View.html#onProvideAutofillVirtualStructure(android.view.ViewStructure,%20kotlin.Int))for each view in the hierarchy.

The resulting [android.view.ViewStructure](https://developer.android.com/reference/kotlin/android/view/ViewStructure.html#) is then passed to the autofill service, which parses it looking for views that can be autofilled. If the service finds such views, it returns a data structure to the Android System containing the following optional info:

- Datasets used to autofill subsets of views in the activity.
- Id of views that the service can save their values for future autofilling.

When the service returns datasets, the Android System displays an autofill dataset picker UI associated with the view, when the view is focused on and is part of a dataset. The application can be notified when the UI is shown by registering an [AutofillCallback](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager.AutofillCallback) through [registerCallback(android.view.autofill.AutofillManager.AutofillCallback)](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#registerCallback(android.view.autofill.AutofillManager.AutofillCallback)). When the user selects a dataset from the UI, all views present in the dataset are autofilled, through calls to [View.autofill(AutofillValue)](https://developer.android.com/reference/kotlin/android/view/View.html#autofill(android.view.autofill.AutofillValue))or [View.autofill(SparseArray)](https://developer.android.com/reference/kotlin/android/view/View.html#autofill(android.util.SparseArray)).

When the service returns ids of savable views, the Android System keeps track of changes made to these views, so they can be used to determine if the autofill save UI is shown later.

The context is then finished when one of the following occurs:

- [commit()](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#commit())is called or all savable views are gone.
- [cancel()](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#cancel())is called.

Finally, after the autofill context is commited (i.e., not cancelled), the Android System shows an autofill save UI if the value of savable views have changed. If the user selects the option to Save, the current value of the views is then sent to the autofill service.

### Additional notes

It is safe to call`AutofillManager`methods from any thread. 
Requires the [PackageManager#FEATURE_AUTOFILL](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_AUTOFILL:kotlin.String) feature which can be detected using [PackageManager.hasSystemFeature(String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)).

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [AutofillCallback](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager.AutofillCallback) Callback for autofill related events. |

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_ASSIST_STRUCTURE](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#EXTRA_ASSIST_STRUCTURE:kotlin.String) Intent extra: The assist structure which captures the filled screen. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_AUTHENTICATION_RESULT](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#EXTRA_AUTHENTICATION_RESULT:kotlin.String) Intent extra: The result of an authentication operation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_AUTHENTICATION_RESULT_EPHEMERAL_DATASET](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#EXTRA_AUTHENTICATION_RESULT_EPHEMERAL_DATASET:kotlin.String) Intent extra: The optional boolean extra field provided by the [android.service.autofill.AutofillService](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#) accompanying the result of an authentication operation. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_CLIENT_STATE](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#EXTRA_CLIENT_STATE:kotlin.String) Intent extra: The optional extras provided by the [android.service.autofill.AutofillService](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_INLINE_SUGGESTIONS_REQUEST](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#EXTRA_INLINE_SUGGESTIONS_REQUEST:kotlin.String) Intent extra: the [android.view.inputmethod.InlineSuggestionsRequest](https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestionsRequest.html#) in the autofill request. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#cancel())`()` Called to indicate the current autofill context should be cancelled. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [commit](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#commit())`()` Called to indicate the current autofill context should be commited. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disableAutofillServices](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#disableAutofillServices())`()` If the app calling this API has enabled autofill services they will be disabled. |
| --- | --- |
| [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)? | [getAutofillServiceComponentName](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#getAutofillServiceComponentName())`()` Returns the component name of the [AutofillService](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#) that is enabled for the current user. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getAvailableFieldClassificationAlgorithms](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#getAvailableFieldClassificationAlgorithms())`()` Gets the name of all algorithms currently available for [field classification](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillService#FieldClassification). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getDefaultFieldClassificationAlgorithm](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#getDefaultFieldClassificationAlgorithm())`()` Gets the name of the default algorithm used for [field classification](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillService#FieldClassification). |
| --- | --- |
| [AutofillId](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId)? | [getNextAutofillId](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#getNextAutofillId())`()` Gets the next unique autofill ID for the activity context. |
| [UserData](https://developer.android.com/reference/kotlin/android/service/autofill/UserData.html#)? | [getUserData](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#getUserData())`()` Gets the user data used for [field classification](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillService#FieldClassification). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getUserDataId](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#getUserDataId())`()` Gets the id of the [UserData](https://developer.android.com/reference/kotlin/android/service/autofill/UserData.html#) used for [field classification](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillService#FieldClassification). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasEnabledAutofillServices](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#hasEnabledAutofillServices())`()` Returns`true`if the calling application provides a [AutofillService](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#) that is enabled for the current user, or`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAutofillSupported](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#isAutofillSupported())`()` Returns`true`if autofill is supported by the current device and is supported for this user. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#isEnabled())`()` Checks whether autofill is enabled for the current user. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFieldClassificationEnabled](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#isFieldClassificationEnabled())`()` Checks if [field classification](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillService#FieldClassification) is enabled. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyValueChanged](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#notifyValueChanged(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Called to indicate the value of an autofillable [View](https://developer.android.com/reference/kotlin/android/view/View.html#) changed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyValueChanged](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#notifyValueChanged(android.view.View,%20kotlin.Int,%20android.view.autofill.AutofillValue))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `virtualId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [AutofillValue](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue)!`)` Called to indicate the value of an autofillable virtual view has changed. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyViewClicked](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#notifyViewClicked(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`)` Called to indicate a [View](https://developer.android.com/reference/kotlin/android/view/View.html#) is clicked. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyViewClicked](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#notifyViewClicked(android.view.View,%20kotlin.Int))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`, `virtualId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called to indicate a virtual view has been clicked. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyViewEntered](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#notifyViewEntered(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`)` Called when a [View](https://developer.android.com/reference/kotlin/android/view/View.html#) that supports autofill is entered. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyViewEntered](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#notifyViewEntered(android.view.View,%20kotlin.Int,%20android.graphics.Rect))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`, `virtualId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `absBounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` Called when a virtual view that supports autofill is entered. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyViewExited](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#notifyViewExited(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`)` Called when a [View](https://developer.android.com/reference/kotlin/android/view/View.html#) that supports autofill is exited. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyViewExited](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#notifyViewExited(android.view.View,%20kotlin.Int))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`, `virtualId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when a virtual view that supports autofill is exited. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyViewVisibilityChanged](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#notifyViewVisibilityChanged(android.view.View,%20kotlin.Boolean))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`, `isVisible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when a [view's](https://developer.android.com/reference/kotlin/android/view/View.html#) visibility changed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyViewVisibilityChanged](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#notifyViewVisibilityChanged(android.view.View,%20kotlin.Int,%20kotlin.Boolean))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`, `virtualId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isVisible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when a virtual view's visibility changed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyVirtualViewsReady](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#notifyVirtualViewsReady(android.view.View,%20android.util.SparseArray))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`, `infos:` ` [SparseArray](https://developer.android.com/reference/kotlin/android/util/SparseArray.html#)< [VirtualViewFillInfo](https://developer.android.com/reference/kotlin/android/view/autofill/VirtualViewFillInfo)!>`)` Called when the virtual views are ready to the user for autofill. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerCallback](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#registerCallback(android.view.autofill.AutofillManager.AutofillCallback))`(`callback:` ` [AutofillManager.AutofillCallback](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager.AutofillCallback)?`)` Registers a [AutofillCallback](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager.AutofillCallback) to receive autofill events. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestAutofill](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#requestAutofill(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`)` Explicitly requests a new autofill context. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestAutofill](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#requestAutofill(android.view.View,%20kotlin.Int,%20android.graphics.Rect))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`, `virtualId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `absBounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`)` Explicitly requests a new autofill context for virtual views. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUserData](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#setUserData(android.service.autofill.UserData))`(`userData:` ` [UserData](https://developer.android.com/reference/kotlin/android/service/autofill/UserData.html#)?`)` Sets the [UserData](https://developer.android.com/reference/kotlin/android/service/autofill/UserData.html#) used for [field classification](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillService#FieldClassification) |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [showAutofillDialog](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#showAutofillDialog(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`)` If autofill suggestions for a [dialog-style UI](https://developer.android.com/reference/android/service/autofill/Dataset.html#FillDialogUI) are available for`view`, shows a dialog allowing the user to select a suggestion and returns`true`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [showAutofillDialog](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#showAutofillDialog(android.view.View,%20kotlin.Int))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`, `virtualId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` If autofill suggestions for a [dialog-style UI](https://developer.android.com/reference/android/service/autofill/Dataset.html#FillDialogUI) are available for virtual`view`, shows a dialog allowing the user to select a suggestion and returns`true`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterCallback](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#unregisterCallback(android.view.autofill.AutofillManager.AutofillCallback))`(`callback:` ` [AutofillManager.AutofillCallback](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager.AutofillCallback)?`)` Unregisters a [AutofillCallback](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager.AutofillCallback) to receive autofill events. |

## Constants

### EXTRA_ASSIST_STRUCTURE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_ASSIST_STRUCTURE: String
```

Intent extra: The assist structure which captures the filled screen.

Type: [android.app.assist.AssistStructure](https://developer.android.com/reference/kotlin/android/app/assist/AssistStructure.html#) 

 Value: "android.view.autofill.extra.ASSIST_STRUCTURE"

### EXTRA_AUTHENTICATION_RESULT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_AUTHENTICATION_RESULT: String
```

Intent extra: The result of an authentication operation. It is either a fully populated [android.service.autofill.FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse.html#) or a fully populated [android.service.autofill.Dataset](https://developer.android.com/reference/kotlin/android/service/autofill/Dataset.html#) if a response or a dataset is being authenticated respectively.

Type: [android.service.autofill.FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse.html#) or a [android.service.autofill.Dataset](https://developer.android.com/reference/kotlin/android/service/autofill/Dataset.html#) 

 Value: "android.view.autofill.extra.AUTHENTICATION_RESULT"

### EXTRA_AUTHENTICATION_RESULT_EPHEMERAL_DATASET

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_AUTHENTICATION_RESULT_EPHEMERAL_DATASET: String
```

Intent extra: The optional boolean extra field provided by the [android.service.autofill.AutofillService](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#) accompanying the result of an authentication operation.

Before [android.os.Build.VERSION_CODES#R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int), if the authentication result is a [android.service.autofill.Dataset](https://developer.android.com/reference/kotlin/android/service/autofill/Dataset.html#), it'll be used to autofill the fields, and also replace the existing dataset in the cached [android.service.autofill.FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse.html#). That means if the user clears the field values, the autofill suggestion will show up again with the new authenticated Dataset.

In [android.os.Build.VERSION_CODES#R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int), we added an exception to this behavior that if the Dataset being authenticated is a pinned dataset (see [android.service.autofill.InlinePresentation#isPinned()](https://developer.android.com/reference/kotlin/android/service/autofill/InlinePresentation.html#isPinned())), the old Dataset will not be replaced.

In [android.os.Build.VERSION_CODES#S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int), we added this boolean extra field to allow the [android.service.autofill.AutofillService](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#) to explicitly specify whether the returned authenticated Dataset is ephemeral. An ephemeral Dataset will be used to autofill once and then thrown away. Therefore, when the boolean extra is set to true, the returned Dataset will not replace the old dataset from the existing [android.service.autofill.FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse.html#). When it's set to false, it will. When it's not set, the old dataset will be replaced, unless it is a pinned inline suggestion, which is consistent with the behavior in [android.os.Build.VERSION_CODES#R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int). 

 Value: "android.view.autofill.extra.AUTHENTICATION_RESULT_EPHEMERAL_DATASET"

### EXTRA_CLIENT_STATE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_CLIENT_STATE: String
```

Intent extra: The optional extras provided by the [android.service.autofill.AutofillService](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#).

For example, when the service responds to a [android.service.autofill.FillCallback#onSuccess(android.service.autofill.FillResponse)](https://developer.android.com/reference/kotlin/android/service/autofill/FillCallback.html#onSuccess(android.service.autofill.FillResponse))with a`FillResponse`that requires authentication, the Intent that launches the service authentication will contain the Bundle set by [android.service.autofill.FillResponse.Builder#setClientState(Bundle)](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse.Builder.html#setClientState(android.os.Bundle))on this extra.

On Android [android.os.Build.VERSION_CODES#P](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int) and higher, the autofill service can also add this bundle to the [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) set as the [result](https://developer.android.com/reference/kotlin/android/app/Activity.html#setResult(kotlin.Int,%20android.content.Intent))for an authentication request, so the bundle can be recovered later on [android.service.autofill.SaveRequest#getClientState()](https://developer.android.com/reference/kotlin/android/service/autofill/SaveRequest.html#getClientState()).

Type: [android.os.Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) 

 Value: "android.view.autofill.extra.CLIENT_STATE"

### EXTRA_INLINE_SUGGESTIONS_REQUEST

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_INLINE_SUGGESTIONS_REQUEST: String
```

Intent extra: the [android.view.inputmethod.InlineSuggestionsRequest](https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestionsRequest.html#) in the autofill request.

This is filled in the authentication intent so the [android.service.autofill.AutofillService](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#) can use it to create the inline suggestion [android.service.autofill.Dataset](https://developer.android.com/reference/kotlin/android/service/autofill/Dataset.html#) in the response, if the original autofill request contains the [android.view.inputmethod.InlineSuggestionsRequest](https://developer.android.com/reference/kotlin/android/view/inputmethod/InlineSuggestionsRequest.html#). 

 Value: "android.view.autofill.extra.INLINE_SUGGESTIONS_REQUEST"

## Public methods

### cancel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun cancel(): Unit
```

Called to indicate the current autofill context should be cancelled.

This method is typically called by [Views](https://developer.android.com/reference/kotlin/android/view/View.html#) that manage virtual views; for example, when the view is rendering an`HTML`page with a form and virtual views that represent the HTML elements, it should call this method if the user does not post the form but moves to another form in this page.

**Note:** This method does not need to be called on regular application lifecycle methods such as [android.app.Activity#finish()](https://developer.android.com/reference/kotlin/android/app/Activity.html#finish()). 

### commit

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun commit(): Unit
```

Called to indicate the current autofill context should be commited.

This method is typically called by [Views](https://developer.android.com/reference/kotlin/android/view/View.html#) that manage virtual views; for example, when the view is rendering an`HTML`page with a form and virtual views that represent the HTML elements, it should call this method after the form is submitted and another page is rendered.

**Note:** This method does not need to be called on regular application lifecycle methods such as [android.app.Activity#finish()](https://developer.android.com/reference/kotlin/android/app/Activity.html#finish()). 

### disableAutofillServices

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun disableAutofillServices(): Unit
```

If the app calling this API has enabled autofill services they will be disabled. 

### getAutofillServiceComponentName

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAutofillServiceComponentName(): ComponentName?
```

Returns the component name of the [AutofillService](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#) that is enabled for the current user.

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------|
| [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)? | This value may be`null`. |

### getAvailableFieldClassificationAlgorithms

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAvailableFieldClassificationAlgorithms(): MutableList<String!>
```

Gets the name of all algorithms currently available for [field classification](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillService#FieldClassification).

**Note:**This method should only be called by an app providing an autofill service, and it returns an empty list if the caller currently doesn't have an enabled autofill service for the user.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. |

### getDefaultFieldClassificationAlgorithm

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDefaultFieldClassificationAlgorithm(): String?
```

Gets the name of the default algorithm used for [field classification](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillService#FieldClassification).

The default algorithm is used when the algorithm on [UserData](https://developer.android.com/reference/kotlin/android/service/autofill/UserData.html#) is invalid or not set.

**Note:**This method should only be called by an app providing an autofill service, and it's ignored if the caller currently doesn't have an enabled autofill service for the user.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getNextAutofillId

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNextAutofillId(): AutofillId?
```

Gets the next unique autofill ID for the activity context.

Typically used to manage views whose content is recycled - see [View.setAutofillId(AutofillId)](https://developer.android.com/reference/kotlin/android/view/View.html#setAutofillId(android.view.autofill.AutofillId))for more info.

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AutofillId](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId)? | An ID that is unique in the activity, or`null`if autofill is not supported in the [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) associated with this [AutofillManager](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#). |

### getUserData

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUserData(): UserData?
```

Gets the user data used for [field classification](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillService#FieldClassification).

**Note:**This method should only be called by an app providing an autofill service, and it's ignored if the caller currently doesn't have an enabled autofill service for the user.

| Return ||
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [UserData](https://developer.android.com/reference/kotlin/android/service/autofill/UserData.html#)? | value previously set by [setUserData(android.service.autofill.UserData)](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#setUserData(android.service.autofill.UserData))or`null`if it was reset or if the caller currently does not have an enabled autofill service for the user. |

### getUserDataId

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUserDataId(): String?
```

Gets the id of the [UserData](https://developer.android.com/reference/kotlin/android/service/autofill/UserData.html#) used for [field classification](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillService#FieldClassification).

This method is useful when the service must check the status of the [UserData](https://developer.android.com/reference/kotlin/android/service/autofill/UserData.html#) in the device without fetching the whole object.

**Note:**This method should only be called by an app providing an autofill service, and it's ignored if the caller currently doesn't have an enabled autofill service for the user.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | id of the [UserData](https://developer.android.com/reference/kotlin/android/service/autofill/UserData.html#) previously set by [setUserData(android.service.autofill.UserData)](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#setUserData(android.service.autofill.UserData))or`null`if it was reset or if the caller currently does not have an enabled autofill service for the user. |

### hasEnabledAutofillServices

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasEnabledAutofillServices(): Boolean
```

Returns`true`if the calling application provides a [AutofillService](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#) that is enabled for the current user, or`false`otherwise. 

### isAutofillSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAutofillSupported(): Boolean
```

Returns`true`if autofill is supported by the current device and is supported for this user.

Autofill is typically supported, but it could be unsupported in cases like:

1. Low-end devices.
2. Device policy rules that forbid its usage. 

### isEnabled

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isEnabled(): Boolean
```

Checks whether autofill is enabled for the current user.

Typically used to determine whether the option to explicitly request autofill should be offered - see [requestAutofill(android.view.View)](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#requestAutofill(android.view.View)).

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether autofill is enabled for the current user. |

### isFieldClassificationEnabled

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isFieldClassificationEnabled(): Boolean
```

Checks if [field classification](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillService#FieldClassification) is enabled.

As field classification is an expensive operation, it could be disabled, either temporarily (for example, because the service exceeded a rate-limit threshold) or permanently (for example, because the device is a low-level device).

**Note:**This method should only be called by an app providing an autofill service, and it's ignored if the caller currently doesn't have an enabled autofill service for the user. 

### notifyValueChanged

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun notifyValueChanged(view: View!): Unit
```

Called to indicate the value of an autofillable [View](https://developer.android.com/reference/kotlin/android/view/View.html#) changed.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:view whose value changed. |

### notifyValueChanged

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun notifyValueChanged(
    view: View!, 
    virtualId: Int, 
    value: AutofillValue!
): Unit
```

Called to indicate the value of an autofillable virtual view has changed.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:the virtual view parent. |
| `virtualId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):id identifying the virtual child inside the parent view. |
| `value` | [AutofillValue](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue)!:new value of the child. |
| --- | --- |

### notifyViewClicked

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun notifyViewClicked(view: View): Unit
```

Called to indicate a [View](https://developer.android.com/reference/kotlin/android/view/View.html#) is clicked.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#):view that has been clicked. This value cannot be`null`. |

### notifyViewClicked

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun notifyViewClicked(
    view: View, 
    virtualId: Int
): Unit
```

Called to indicate a virtual view has been clicked.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#):the virtual view parent. This value cannot be`null`. |
| `virtualId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):id identifying the virtual child inside the parent view. |

### notifyViewEntered

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun notifyViewEntered(view: View): Unit
```

Called when a [View](https://developer.android.com/reference/kotlin/android/view/View.html#) that supports autofill is entered.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): [View](https://developer.android.com/reference/kotlin/android/view/View.html#) that was entered. This value cannot be`null`. |

### notifyViewEntered

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun notifyViewEntered(
    view: View, 
    virtualId: Int, 
    absBounds: Rect
): Unit
```

Called when a virtual view that supports autofill is entered.

The virtual view boundaries must be absolute screen coordinates. For example, if the parent, non-virtual view uses`bounds`to draw the virtual view inside its Canvas, the absolute bounds could be calculated by: 

```kotlin
int offset[] = new int[2];
    getLocationOnScreen(offset);
    Rect absBounds = new Rect(bounds.left + offset[0],
        bounds.top + offset[1],
        bounds.right + offset[0], bounds.bottom + offset[1]);
  
```

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#):the virtual view parent. This value cannot be`null`. |
| `virtualId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):id identifying the virtual child inside the parent view. |
| `absBounds` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#):absolute boundaries of the virtual view in the screen. This value cannot be`null`. |
| --- | --- |

### notifyViewExited

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun notifyViewExited(view: View): Unit
```

Called when a [View](https://developer.android.com/reference/kotlin/android/view/View.html#) that supports autofill is exited.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): [View](https://developer.android.com/reference/kotlin/android/view/View.html#) that was exited. This value cannot be`null`. |

### notifyViewExited

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun notifyViewExited(
    view: View, 
    virtualId: Int
): Unit
```

Called when a virtual view that supports autofill is exited.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#):the virtual view parent. This value cannot be`null`. |
| `virtualId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):id identifying the virtual child inside the parent view. |

### notifyViewVisibilityChanged

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun notifyViewVisibilityChanged(
    view: View, 
    isVisible: Boolean
): Unit
```

Called when a [view's](https://developer.android.com/reference/kotlin/android/view/View.html#) visibility changed.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): [View](https://developer.android.com/reference/kotlin/android/view/View.html#) that was exited. This value cannot be`null`. |
| `isVisible` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):visible if the view is visible in the view hierarchy. |

### notifyViewVisibilityChanged

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun notifyViewVisibilityChanged(
    view: View, 
    virtualId: Int, 
    isVisible: Boolean
): Unit
```

Called when a virtual view's visibility changed.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): [View](https://developer.android.com/reference/kotlin/android/view/View.html#) that was exited. This value cannot be`null`. |
| `virtualId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):id identifying the virtual child inside the parent view. |
| `isVisible` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):visible if the view is visible in the view hierarchy. |
| --- | --- |

### notifyVirtualViewsReady

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun notifyVirtualViewsReady(
    view: View, 
    infos: SparseArray<VirtualViewFillInfo!>
): Unit
```

**Deprecated:** *This function will not do anything. Showing fill dialog is now fully controlled by the framework and the autofill provider.*

Called when the virtual views are ready to the user for autofill. This method is used to notify autofill system the views are ready to the user. And then Autofill can do initialization if needed before the user starts to input. For example, do a pre-fill request for the [fill dialog](https://developer.android.com/reference/kotlin/reference/android/service/autofill/Dataset.html#FillDialogUI).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#):the host view that holds a virtual view hierarchy. This value cannot be`null`. |
| `infos` | [SparseArray](https://developer.android.com/reference/kotlin/android/util/SparseArray.html#)\< [VirtualViewFillInfo](https://developer.android.com/reference/kotlin/android/view/autofill/VirtualViewFillInfo)!\>:extra information for the virtual views. The key is virtual id which represents the virtual view in the host view. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|------------------------|
| `java.lang.IllegalArgumentException` | if the`infos`was empty |

### registerCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerCallback(callback: AutofillManager.AutofillCallback?): Unit
```

Registers a [AutofillCallback](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager.AutofillCallback) to receive autofill events.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [AutofillManager.AutofillCallback](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager.AutofillCallback)?:callback to receive events. This value may be`null`. |

### requestAutofill

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun requestAutofill(view: View): Unit
```

Explicitly requests a new autofill context.

Normally, the autofill context is automatically started if necessary when [notifyViewEntered(android.view.View)](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#notifyViewEntered(android.view.View))is called, but this method should be used in the cases where it must be explicitly started. For example, when the view offers an AUTOFILL option on its contextual overflow menu, and the user selects it.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#):view requesting the new autofill context. This value cannot be`null`. |

### requestAutofill

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun requestAutofill(
    view: View, 
    virtualId: Int, 
    absBounds: Rect
): Unit
```

Explicitly requests a new autofill context for virtual views.

Normally, the autofill context is automatically started if necessary when [notifyViewEntered(android.view.View,int,android.graphics.Rect)](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager#notifyViewEntered(android.view.View,%20kotlin.Int,%20android.graphics.Rect))is called, but this method should be used in the cases where it must be explicitly started. For example, when the virtual view offers an AUTOFILL option on its contextual overflow menu, and the user selects it.

The virtual view boundaries must be absolute screen coordinates. For example, if the parent view uses`bounds`to draw the virtual view inside its Canvas, the absolute bounds could be calculated by: 

```kotlin
int offset[] = new int[2];
    getLocationOnScreen(offset);
    Rect absBounds = new Rect(bounds.left + offset[0],
        bounds.top + offset[1],
        bounds.right + offset[0], bounds.bottom + offset[1]);
  
```

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#):the virtual view parent. This value cannot be`null`. |
| `virtualId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):id identifying the virtual child inside the parent view. |
| `absBounds` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#):absolute boundaries of the virtual view in the screen. This value cannot be`null`. |
| --- | --- |

### setUserData

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setUserData(userData: UserData?): Unit
```

Sets the [UserData](https://developer.android.com/reference/kotlin/android/service/autofill/UserData.html#) used for [field classification](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillService#FieldClassification)

**Note:**This method should only be called by an app providing an autofill service, and it's ignored if the caller currently doesn't have an enabled autofill service for the user.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------|
| `userData` | [UserData](https://developer.android.com/reference/kotlin/android/service/autofill/UserData.html#)?:This value may be`null`. |

### showAutofillDialog

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun showAutofillDialog(view: View): Boolean
```

**Deprecated:** *This function will not do anything. Showing fill dialog is now fully controlled by the framework and the autofill provider.*

If autofill suggestions for a [dialog-style UI](https://developer.android.com/reference/android/service/autofill/Dataset.html#FillDialogUI) are available for`view`, shows a dialog allowing the user to select a suggestion and returns`true`.

The dialog may not be shown if the autofill service does not support it, if the autofill request has not returned a response yet, if the dialog was shown previously, or if the input method is already shown.

It is recommended apps to call this method the first time a user focuses on an autofill-able form, and to avoid showing the input method if the dialog is shown. If this method returns`false`, you should then instead show the input method (assuming that is how the view normally handles the focus event). If the user re-focuses on the view, you should not call this method again so as to not disrupt usage of the input method.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#):the view for which to show autofill suggestions. This is typically a view receiving a focus event. The autofill suggestions shown will include content for related views as well. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the autofill dialog is being shown |

### showAutofillDialog

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun showAutofillDialog(
    view: View, 
    virtualId: Int
): Boolean
```

**Deprecated:** *This function will not do anything. Showing fill dialog is now fully controlled by the framework and the autofill provider.*

If autofill suggestions for a [dialog-style UI](https://developer.android.com/reference/android/service/autofill/Dataset.html#FillDialogUI) are available for virtual`view`, shows a dialog allowing the user to select a suggestion and returns`true`.

The dialog may not be shown if the autofill service does not support it, if the autofill request has not returned a response yet, if the dialog was shown previously, or if the input method is already shown.

It is recommended apps to call this method the first time a user focuses on an autofill-able form, and to avoid showing the input method if the dialog is shown. If this method returns`false`, you should then instead show the input method (assuming that is how the view normally handles the focus event). If the user re-focuses on the view, you should not call this method again so as to not disrupt usage of the input method.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#):the view hosting the virtual view hierarchy which is used to show autofill suggestions. This value cannot be`null`. |
| `virtualId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):id identifying the virtual view inside the host view. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the autofill dialog is being shown |

### unregisterCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterCallback(callback: AutofillManager.AutofillCallback?): Unit
```

Unregisters a [AutofillCallback](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager.AutofillCallback) to receive autofill events.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [AutofillManager.AutofillCallback](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager.AutofillCallback)?:callback to stop receiving events. This value may be`null`. |
