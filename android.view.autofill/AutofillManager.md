# AutofillManager

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AutofillManager

Kotlin| [Java](../android/view/autofill/AutofillManager.md) 
| --- | --- |

```
class AutofillManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.autofill.AutofillManager](../android/view/autofill/AutofillManager.md) |

The [AutofillManager](../android/view/autofill/AutofillManager.md) class provides ways for apps and custom views to integrate with the Autofill Framework lifecycle.

To learn about using Autofill in your app, read the [Autofill Framework](../guide/topics/text/autofill.md) guides.

### Autofill lifecycle

The autofill lifecycle starts with the creation of an autofill context associated with an activity context. The autofill context is created when one of the following methods is called for the first time in an activity context, and the current user has an enabled autofill service:

- [notifyViewEntered(android.view.View)](../android/view/autofill/AutofillManager.md))
- [notifyViewEntered(android.view.View,int,android.graphics.Rect)](../android/view/autofill/AutofillManager.md))
- [requestAutofill(android.view.View)](../android/view/autofill/AutofillManager.md))

Typically, the context is automatically created when the first view of the activity is focused because`View.onFocusChanged()`indirectly calls [notifyViewEntered(android.view.View)](../android/view/autofill/AutofillManager.md)). App developers can call [requestAutofill(android.view.View)](../android/view/autofill/AutofillManager.md))to explicitly create it (for example, a custom view developer could offer a contextual menu action in a text-field view to let users manually request autofill).

After the context is created, the Android System creates a [android.view.ViewStructure](../android/view/ViewStructure.md) that represents the view hierarchy by calling [View.dispatchProvideAutofillStructure(android.view.ViewStructure, int)](../android/view/View.md))in the root views of all application windows. By default,`dispatchProvideAutofillStructure()`results in subsequent calls to [View.onProvideAutofillStructure(android.view.ViewStructure, int)](../android/view/View.md))and [View.onProvideAutofillVirtualStructure(android.view.ViewStructure, int)](../android/view/View.md))for each view in the hierarchy.

The resulting [android.view.ViewStructure](../android/view/ViewStructure.md) is then passed to the autofill service, which parses it looking for views that can be autofilled. If the service finds such views, it returns a data structure to the Android System containing the following optional info:

- Datasets used to autofill subsets of views in the activity.
- Id of views that the service can save their values for future autofilling.

When the service returns datasets, the Android System displays an autofill dataset picker UI associated with the view, when the view is focused on and is part of a dataset. The application can be notified when the UI is shown by registering an [AutofillCallback](../android/view/autofill/AutofillManager.AutofillCallback.md) through [registerCallback(android.view.autofill.AutofillManager.AutofillCallback)](../android/view/autofill/AutofillManager.md)). When the user selects a dataset from the UI, all views present in the dataset are autofilled, through calls to [View.autofill(AutofillValue)](../android/view/View.md))or [View.autofill(SparseArray)](../android/view/View.md)).

When the service returns ids of savable views, the Android System keeps track of changes made to these views, so they can be used to determine if the autofill save UI is shown later.

The context is then finished when one of the following occurs:

- [commit()](../android/view/autofill/AutofillManager.md))is called or all savable views are gone.
- [cancel()](../android/view/autofill/AutofillManager.md))is called.

Finally, after the autofill context is commited (i.e., not cancelled), the Android System shows an autofill save UI if the value of savable views have changed. If the user selects the option to Save, the current value of the views is then sent to the autofill service.

### Additional notes

It is safe to call`AutofillManager`methods from any thread. 
Requires the [PackageManager#FEATURE_AUTOFILL](../android/content/pm/PackageManager.md) feature which can be detected using [PackageManager.hasSystemFeature(String)](../android/content/pm/PackageManager.md)).

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [AutofillCallback](../android/view/autofill/AutofillManager.AutofillCallback.md) Callback for autofill related events. |

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_ASSIST_STRUCTURE](../android/view/autofill/AutofillManager.md) Intent extra: The assist structure which captures the filled screen. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_AUTHENTICATION_RESULT](../android/view/autofill/AutofillManager.md) Intent extra: The result of an authentication operation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_AUTHENTICATION_RESULT_EPHEMERAL_DATASET](../android/view/autofill/AutofillManager.md) Intent extra: The optional boolean extra field provided by the [android.service.autofill.AutofillService](../android/service/autofill/AutofillService.md) accompanying the result of an authentication operation. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_CLIENT_STATE](../android/view/autofill/AutofillManager.md) Intent extra: The optional extras provided by the [android.service.autofill.AutofillService](../android/service/autofill/AutofillService.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_INLINE_SUGGESTIONS_REQUEST](../android/view/autofill/AutofillManager.md) Intent extra: the [android.view.inputmethod.InlineSuggestionsRequest](../android/view/inputmethod/InlineSuggestionsRequest.md) in the autofill request. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](../android/view/autofill/AutofillManager.md))`()` Called to indicate the current autofill context should be cancelled. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [commit](../android/view/autofill/AutofillManager.md))`()` Called to indicate the current autofill context should be commited. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disableAutofillServices](../android/view/autofill/AutofillManager.md))`()` If the app calling this API has enabled autofill services they will be disabled. |
| --- | --- |
| [ComponentName](../android/content/ComponentName.md)? | [getAutofillServiceComponentName](../android/view/autofill/AutofillManager.md))`()` Returns the component name of the [AutofillService](../android/service/autofill/AutofillService.md) that is enabled for the current user. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getAvailableFieldClassificationAlgorithms](../android/view/autofill/AutofillManager.md))`()` Gets the name of all algorithms currently available for [field classification](../android/view/autofill/AutofillService.md). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getDefaultFieldClassificationAlgorithm](../android/view/autofill/AutofillManager.md))`()` Gets the name of the default algorithm used for [field classification](../android/view/autofill/AutofillService.md). |
| --- | --- |
| [AutofillId](../android/view/autofill/AutofillId.md)? | [getNextAutofillId](../android/view/autofill/AutofillManager.md))`()` Gets the next unique autofill ID for the activity context. |
| [UserData](../android/service/autofill/UserData.md)? | [getUserData](../android/view/autofill/AutofillManager.md))`()` Gets the user data used for [field classification](../android/view/autofill/AutofillService.md). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getUserDataId](../android/view/autofill/AutofillManager.md))`()` Gets the id of the [UserData](../android/service/autofill/UserData.md) used for [field classification](../android/view/autofill/AutofillService.md). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasEnabledAutofillServices](../android/view/autofill/AutofillManager.md))`()` Returns`true`if the calling application provides a [AutofillService](../android/service/autofill/AutofillService.md) that is enabled for the current user, or`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAutofillSupported](../android/view/autofill/AutofillManager.md))`()` Returns`true`if autofill is supported by the current device and is supported for this user. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](../android/view/autofill/AutofillManager.md))`()` Checks whether autofill is enabled for the current user. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFieldClassificationEnabled](../android/view/autofill/AutofillManager.md))`()` Checks if [field classification](../android/view/autofill/AutofillService.md) is enabled. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyValueChanged](../android/view/autofill/AutofillManager.md))`(`view:` ` [View](../android/view/View.md)!`)` Called to indicate the value of an autofillable [View](../android/view/View.md) changed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyValueChanged](../android/view/autofill/AutofillManager.md))`(`view:` ` [View](../android/view/View.md)!`, `virtualId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [AutofillValue](../android/view/autofill/AutofillValue.md)!`)` Called to indicate the value of an autofillable virtual view has changed. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyViewClicked](../android/view/autofill/AutofillManager.md))`(`view:` ` [View](../android/view/View.md)`)` Called to indicate a [View](../android/view/View.md) is clicked. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyViewClicked](../android/view/autofill/AutofillManager.md))`(`view:` ` [View](../android/view/View.md)`, `virtualId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called to indicate a virtual view has been clicked. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyViewEntered](../android/view/autofill/AutofillManager.md))`(`view:` ` [View](../android/view/View.md)`)` Called when a [View](../android/view/View.md) that supports autofill is entered. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyViewEntered](../android/view/autofill/AutofillManager.md))`(`view:` ` [View](../android/view/View.md)`, `virtualId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `absBounds:` ` [Rect](../android/graphics/Rect.md)`)` Called when a virtual view that supports autofill is entered. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyViewExited](../android/view/autofill/AutofillManager.md))`(`view:` ` [View](../android/view/View.md)`)` Called when a [View](../android/view/View.md) that supports autofill is exited. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyViewExited](../android/view/autofill/AutofillManager.md))`(`view:` ` [View](../android/view/View.md)`, `virtualId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when a virtual view that supports autofill is exited. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyViewVisibilityChanged](../android/view/autofill/AutofillManager.md))`(`view:` ` [View](../android/view/View.md)`, `isVisible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when a [view's](../android/view/View.md) visibility changed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyViewVisibilityChanged](../android/view/autofill/AutofillManager.md))`(`view:` ` [View](../android/view/View.md)`, `virtualId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isVisible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when a virtual view's visibility changed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyVirtualViewsReady](../android/view/autofill/AutofillManager.md))`(`view:` ` [View](../android/view/View.md)`, `infos:` ` [SparseArray](../android/util/SparseArray.md)< [VirtualViewFillInfo](../android/view/autofill/VirtualViewFillInfo.md)!>`)` Called when the virtual views are ready to the user for autofill. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerCallback](../android/view/autofill/AutofillManager.md))`(`callback:` ` [AutofillManager.AutofillCallback](../android/view/autofill/AutofillManager.AutofillCallback.md)?`)` Registers a [AutofillCallback](../android/view/autofill/AutofillManager.AutofillCallback.md) to receive autofill events. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestAutofill](../android/view/autofill/AutofillManager.md))`(`view:` ` [View](../android/view/View.md)`)` Explicitly requests a new autofill context. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestAutofill](../android/view/autofill/AutofillManager.md))`(`view:` ` [View](../android/view/View.md)`, `virtualId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `absBounds:` ` [Rect](../android/graphics/Rect.md)`)` Explicitly requests a new autofill context for virtual views. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUserData](../android/view/autofill/AutofillManager.md))`(`userData:` ` [UserData](../android/service/autofill/UserData.md)?`)` Sets the [UserData](../android/service/autofill/UserData.md) used for [field classification](../android/view/autofill/AutofillService.md) |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [showAutofillDialog](../android/view/autofill/AutofillManager.md))`(`view:` ` [View](../android/view/View.md)`)` If autofill suggestions for a [dialog-style UI](../android/service/autofill/Dataset.md) are available for`view`, shows a dialog allowing the user to select a suggestion and returns`true`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [showAutofillDialog](../android/view/autofill/AutofillManager.md))`(`view:` ` [View](../android/view/View.md)`, `virtualId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` If autofill suggestions for a [dialog-style UI](../android/service/autofill/Dataset.md) are available for virtual`view`, shows a dialog allowing the user to select a suggestion and returns`true`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterCallback](../android/view/autofill/AutofillManager.md))`(`callback:` ` [AutofillManager.AutofillCallback](../android/view/autofill/AutofillManager.AutofillCallback.md)?`)` Unregisters a [AutofillCallback](../android/view/autofill/AutofillManager.AutofillCallback.md) to receive autofill events. |

## Constants

### EXTRA_ASSIST_STRUCTURE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_ASSIST_STRUCTURE: String
```

Intent extra: The assist structure which captures the filled screen.

Type: [android.app.assist.AssistStructure](../android/app/assist/AssistStructure.md) 

 Value: "android.view.autofill.extra.ASSIST_STRUCTURE"

### EXTRA_AUTHENTICATION_RESULT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_AUTHENTICATION_RESULT: String
```

Intent extra: The result of an authentication operation. It is either a fully populated [android.service.autofill.FillResponse](../android/service/autofill/FillResponse.md) or a fully populated [android.service.autofill.Dataset](../android/service/autofill/Dataset.md) if a response or a dataset is being authenticated respectively.

Type: [android.service.autofill.FillResponse](../android/service/autofill/FillResponse.md) or a [android.service.autofill.Dataset](../android/service/autofill/Dataset.md) 

 Value: "android.view.autofill.extra.AUTHENTICATION_RESULT"

### EXTRA_AUTHENTICATION_RESULT_EPHEMERAL_DATASET

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_AUTHENTICATION_RESULT_EPHEMERAL_DATASET: String
```

Intent extra: The optional boolean extra field provided by the [android.service.autofill.AutofillService](../android/service/autofill/AutofillService.md) accompanying the result of an authentication operation.

Before [android.os.Build.VERSION_CODES#R](../android/os/Build.VERSION_CODES.md), if the authentication result is a [android.service.autofill.Dataset](../android/service/autofill/Dataset.md), it'll be used to autofill the fields, and also replace the existing dataset in the cached [android.service.autofill.FillResponse](../android/service/autofill/FillResponse.md). That means if the user clears the field values, the autofill suggestion will show up again with the new authenticated Dataset.

In [android.os.Build.VERSION_CODES#R](../android/os/Build.VERSION_CODES.md), we added an exception to this behavior that if the Dataset being authenticated is a pinned dataset (see [android.service.autofill.InlinePresentation#isPinned()](../android/service/autofill/InlinePresentation.md))), the old Dataset will not be replaced.

In [android.os.Build.VERSION_CODES#S](../android/os/Build.VERSION_CODES.md), we added this boolean extra field to allow the [android.service.autofill.AutofillService](../android/service/autofill/AutofillService.md) to explicitly specify whether the returned authenticated Dataset is ephemeral. An ephemeral Dataset will be used to autofill once and then thrown away. Therefore, when the boolean extra is set to true, the returned Dataset will not replace the old dataset from the existing [android.service.autofill.FillResponse](../android/service/autofill/FillResponse.md). When it's set to false, it will. When it's not set, the old dataset will be replaced, unless it is a pinned inline suggestion, which is consistent with the behavior in [android.os.Build.VERSION_CODES#R](../android/os/Build.VERSION_CODES.md). 

 Value: "android.view.autofill.extra.AUTHENTICATION_RESULT_EPHEMERAL_DATASET"

### EXTRA_CLIENT_STATE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_CLIENT_STATE: String
```

Intent extra: The optional extras provided by the [android.service.autofill.AutofillService](../android/service/autofill/AutofillService.md).

For example, when the service responds to a [android.service.autofill.FillCallback#onSuccess(android.service.autofill.FillResponse)](../android/service/autofill/FillCallback.md))with a`FillResponse`that requires authentication, the Intent that launches the service authentication will contain the Bundle set by [android.service.autofill.FillResponse.Builder#setClientState(Bundle)](../android/service/autofill/FillResponse.Builder.md))on this extra.

On Android [android.os.Build.VERSION_CODES#P](../android/os/Build.VERSION_CODES.md) and higher, the autofill service can also add this bundle to the [Intent](../android/content/Intent.md) set as the [result](../android/app/Activity.md))for an authentication request, so the bundle can be recovered later on [android.service.autofill.SaveRequest#getClientState()](../android/service/autofill/SaveRequest.md)).

Type: [android.os.Bundle](../android/os/Bundle.md) 

 Value: "android.view.autofill.extra.CLIENT_STATE"

### EXTRA_INLINE_SUGGESTIONS_REQUEST

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_INLINE_SUGGESTIONS_REQUEST: String
```

Intent extra: the [android.view.inputmethod.InlineSuggestionsRequest](../android/view/inputmethod/InlineSuggestionsRequest.md) in the autofill request.

This is filled in the authentication intent so the [android.service.autofill.AutofillService](../android/service/autofill/AutofillService.md) can use it to create the inline suggestion [android.service.autofill.Dataset](../android/service/autofill/Dataset.md) in the response, if the original autofill request contains the [android.view.inputmethod.InlineSuggestionsRequest](../android/view/inputmethod/InlineSuggestionsRequest.md). 

 Value: "android.view.autofill.extra.INLINE_SUGGESTIONS_REQUEST"

## Public methods

### cancel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun cancel(): Unit
```

Called to indicate the current autofill context should be cancelled.

This method is typically called by [Views](../android/view/View.md) that manage virtual views; for example, when the view is rendering an`HTML`page with a form and virtual views that represent the HTML elements, it should call this method if the user does not post the form but moves to another form in this page.

**Note:** This method does not need to be called on regular application lifecycle methods such as [android.app.Activity#finish()](../android/app/Activity.md)). 

### commit

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun commit(): Unit
```

Called to indicate the current autofill context should be commited.

This method is typically called by [Views](../android/view/View.md) that manage virtual views; for example, when the view is rendering an`HTML`page with a form and virtual views that represent the HTML elements, it should call this method after the form is submitted and another page is rendered.

**Note:** This method does not need to be called on regular application lifecycle methods such as [android.app.Activity#finish()](../android/app/Activity.md)). 

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

Returns the component name of the [AutofillService](../android/service/autofill/AutofillService.md) that is enabled for the current user.

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------|
| [ComponentName](../android/content/ComponentName.md)? | This value may be`null`. |

### getAvailableFieldClassificationAlgorithms

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAvailableFieldClassificationAlgorithms(): MutableList<String!>
```

Gets the name of all algorithms currently available for [field classification](../android/view/autofill/AutofillService.md).

**Note:**This method should only be called by an app providing an autofill service, and it returns an empty list if the caller currently doesn't have an enabled autofill service for the user.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. |

### getDefaultFieldClassificationAlgorithm

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDefaultFieldClassificationAlgorithm(): String?
```

Gets the name of the default algorithm used for [field classification](../android/view/autofill/AutofillService.md).

The default algorithm is used when the algorithm on [UserData](../android/service/autofill/UserData.md) is invalid or not set.

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

Typically used to manage views whose content is recycled - see [View.setAutofillId(AutofillId)](../android/view/View.md))for more info.

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AutofillId](../android/view/autofill/AutofillId.md)? | An ID that is unique in the activity, or`null`if autofill is not supported in the [Context](../android/content/Context.md) associated with this [AutofillManager](../android/view/autofill/AutofillManager.md). |

### getUserData

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUserData(): UserData?
```

Gets the user data used for [field classification](../android/view/autofill/AutofillService.md).

**Note:**This method should only be called by an app providing an autofill service, and it's ignored if the caller currently doesn't have an enabled autofill service for the user.

| Return ||
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [UserData](../android/service/autofill/UserData.md)? | value previously set by [setUserData(android.service.autofill.UserData)](../android/view/autofill/AutofillManager.md))or`null`if it was reset or if the caller currently does not have an enabled autofill service for the user. |

### getUserDataId

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUserDataId(): String?
```

Gets the id of the [UserData](../android/service/autofill/UserData.md) used for [field classification](../android/view/autofill/AutofillService.md).

This method is useful when the service must check the status of the [UserData](../android/service/autofill/UserData.md) in the device without fetching the whole object.

**Note:**This method should only be called by an app providing an autofill service, and it's ignored if the caller currently doesn't have an enabled autofill service for the user.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | id of the [UserData](../android/service/autofill/UserData.md) previously set by [setUserData(android.service.autofill.UserData)](../android/view/autofill/AutofillManager.md))or`null`if it was reset or if the caller currently does not have an enabled autofill service for the user. |

### hasEnabledAutofillServices

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasEnabledAutofillServices(): Boolean
```

Returns`true`if the calling application provides a [AutofillService](../android/service/autofill/AutofillService.md) that is enabled for the current user, or`false`otherwise. 

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

Typically used to determine whether the option to explicitly request autofill should be offered - see [requestAutofill(android.view.View)](../android/view/autofill/AutofillManager.md)).

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether autofill is enabled for the current user. |

### isFieldClassificationEnabled

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isFieldClassificationEnabled(): Boolean
```

Checks if [field classification](../android/view/autofill/AutofillService.md) is enabled.

As field classification is an expensive operation, it could be disabled, either temporarily (for example, because the service exceeded a rate-limit threshold) or permanently (for example, because the device is a low-level device).

**Note:**This method should only be called by an app providing an autofill service, and it's ignored if the caller currently doesn't have an enabled autofill service for the user. 

### notifyValueChanged

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun notifyValueChanged(view: View!): Unit
```

Called to indicate the value of an autofillable [View](../android/view/View.md) changed.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md)!:view whose value changed. |

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
| `view` | [View](../android/view/View.md)!:the virtual view parent. |
| `virtualId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):id identifying the virtual child inside the parent view. |
| `value` | [AutofillValue](../android/view/autofill/AutofillValue.md)!:new value of the child. |
| --- | --- |

### notifyViewClicked

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun notifyViewClicked(view: View): Unit
```

Called to indicate a [View](../android/view/View.md) is clicked.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md):view that has been clicked. This value cannot be`null`. |

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
| `view` | [View](../android/view/View.md):the virtual view parent. This value cannot be`null`. |
| `virtualId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):id identifying the virtual child inside the parent view. |

### notifyViewEntered

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun notifyViewEntered(view: View): Unit
```

Called when a [View](../android/view/View.md) that supports autofill is entered.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md): [View](../android/view/View.md) that was entered. This value cannot be`null`. |

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
| `view` | [View](../android/view/View.md):the virtual view parent. This value cannot be`null`. |
| `virtualId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):id identifying the virtual child inside the parent view. |
| `absBounds` | [Rect](../android/graphics/Rect.md):absolute boundaries of the virtual view in the screen. This value cannot be`null`. |
| --- | --- |

### notifyViewExited

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun notifyViewExited(view: View): Unit
```

Called when a [View](../android/view/View.md) that supports autofill is exited.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md): [View](../android/view/View.md) that was exited. This value cannot be`null`. |

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
| `view` | [View](../android/view/View.md):the virtual view parent. This value cannot be`null`. |
| `virtualId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):id identifying the virtual child inside the parent view. |

### notifyViewVisibilityChanged

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun notifyViewVisibilityChanged(
    view: View, 
    isVisible: Boolean
): Unit
```

Called when a [view's](../android/view/View.md) visibility changed.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md): [View](../android/view/View.md) that was exited. This value cannot be`null`. |
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
| `view` | [View](../android/view/View.md): [View](../android/view/View.md) that was exited. This value cannot be`null`. |
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

Called when the virtual views are ready to the user for autofill. This method is used to notify autofill system the views are ready to the user. And then Autofill can do initialization if needed before the user starts to input. For example, do a pre-fill request for the [fill dialog](../reference/android/service/autofill/Dataset.md).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md):the host view that holds a virtual view hierarchy. This value cannot be`null`. |
| `infos` | [SparseArray](../android/util/SparseArray.md)\< [VirtualViewFillInfo](../android/view/autofill/VirtualViewFillInfo.md)!\>:extra information for the virtual views. The key is virtual id which represents the virtual view in the host view. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|------------------------|
| `java.lang.IllegalArgumentException` | if the`infos`was empty |

### registerCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerCallback(callback: AutofillManager.AutofillCallback?): Unit
```

Registers a [AutofillCallback](../android/view/autofill/AutofillManager.AutofillCallback.md) to receive autofill events.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [AutofillManager.AutofillCallback](../android/view/autofill/AutofillManager.AutofillCallback.md)?:callback to receive events. This value may be`null`. |

### requestAutofill

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun requestAutofill(view: View): Unit
```

Explicitly requests a new autofill context.

Normally, the autofill context is automatically started if necessary when [notifyViewEntered(android.view.View)](../android/view/autofill/AutofillManager.md))is called, but this method should be used in the cases where it must be explicitly started. For example, when the view offers an AUTOFILL option on its contextual overflow menu, and the user selects it.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md):view requesting the new autofill context. This value cannot be`null`. |

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

Normally, the autofill context is automatically started if necessary when [notifyViewEntered(android.view.View,int,android.graphics.Rect)](../android/view/autofill/AutofillManager.md))is called, but this method should be used in the cases where it must be explicitly started. For example, when the virtual view offers an AUTOFILL option on its contextual overflow menu, and the user selects it.

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
| `view` | [View](../android/view/View.md):the virtual view parent. This value cannot be`null`. |
| `virtualId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):id identifying the virtual child inside the parent view. |
| `absBounds` | [Rect](../android/graphics/Rect.md):absolute boundaries of the virtual view in the screen. This value cannot be`null`. |
| --- | --- |

### setUserData

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setUserData(userData: UserData?): Unit
```

Sets the [UserData](../android/service/autofill/UserData.md) used for [field classification](../android/view/autofill/AutofillService.md)

**Note:**This method should only be called by an app providing an autofill service, and it's ignored if the caller currently doesn't have an enabled autofill service for the user.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------|
| `userData` | [UserData](../android/service/autofill/UserData.md)?:This value may be`null`. |

### showAutofillDialog

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun showAutofillDialog(view: View): Boolean
```

**Deprecated:** *This function will not do anything. Showing fill dialog is now fully controlled by the framework and the autofill provider.*

If autofill suggestions for a [dialog-style UI](../android/service/autofill/Dataset.md) are available for`view`, shows a dialog allowing the user to select a suggestion and returns`true`.

The dialog may not be shown if the autofill service does not support it, if the autofill request has not returned a response yet, if the dialog was shown previously, or if the input method is already shown.

It is recommended apps to call this method the first time a user focuses on an autofill-able form, and to avoid showing the input method if the dialog is shown. If this method returns`false`, you should then instead show the input method (assuming that is how the view normally handles the focus event). If the user re-focuses on the view, you should not call this method again so as to not disrupt usage of the input method.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md):the view for which to show autofill suggestions. This is typically a view receiving a focus event. The autofill suggestions shown will include content for related views as well. This value cannot be`null`. |

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

If autofill suggestions for a [dialog-style UI](../android/service/autofill/Dataset.md) are available for virtual`view`, shows a dialog allowing the user to select a suggestion and returns`true`.

The dialog may not be shown if the autofill service does not support it, if the autofill request has not returned a response yet, if the dialog was shown previously, or if the input method is already shown.

It is recommended apps to call this method the first time a user focuses on an autofill-able form, and to avoid showing the input method if the dialog is shown. If this method returns`false`, you should then instead show the input method (assuming that is how the view normally handles the focus event). If the user re-focuses on the view, you should not call this method again so as to not disrupt usage of the input method.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md):the view hosting the virtual view hierarchy which is used to show autofill suggestions. This value cannot be`null`. |
| `virtualId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):id identifying the virtual view inside the host view. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the autofill dialog is being shown |

### unregisterCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterCallback(callback: AutofillManager.AutofillCallback?): Unit
```

Unregisters a [AutofillCallback](../android/view/autofill/AutofillManager.AutofillCallback.md) to receive autofill events.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [AutofillManager.AutofillCallback](../android/view/autofill/AutofillManager.AutofillCallback.md)?:callback to stop receiving events. This value may be`null`. |
