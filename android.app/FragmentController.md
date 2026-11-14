# FragmentController

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FragmentController

Kotlin| [Java](../android/app/FragmentController.md) 
| --- | --- |

```
open class FragmentController
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.FragmentController](../android/app/FragmentController.md) |

| **This class was deprecated in API level 28.**
|
| Use the [Support Library](https://developer.android.com/tools/extras/support-library.html) androidx.fragment.app.FragmentController

Provides integration points with a [FragmentManager](../android/app/FragmentManager.md) for a fragment host.

It is the responsibility of the host to take care of the Fragment's lifecycle. The methods provided by [FragmentController](../android/app/FragmentController.md) are for that purpose.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [attachHost](../android/app/FragmentController.md))`(`parent:` ` [Fragment](../android/app/Fragment.md)!`)` Attaches the host to the FragmentManager for this controller. |
| static [FragmentController](../android/app/FragmentController.md)! | [createController](../android/app/FragmentController.md))`(`callbacks:` ` [FragmentHostCallback](../android/app/FragmentHostCallback.md)<*>!`)` Returns a [FragmentController](../android/app/FragmentController.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchActivityCreated](../android/app/FragmentController.md))`()` Moves all Fragments managed by the controller's FragmentManager into the activity created state. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchConfigurationChanged](../android/app/FragmentController.md))`(`newConfig:` ` [Configuration](../android/content/res/Configuration.md)!`)` Lets all Fragments managed by the controller's FragmentManager know a configuration change occurred. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchContextItemSelected](../android/app/FragmentController.md))`(`item:` ` [MenuItem](../android/view/MenuItem.md)!`)` Sends a context item selection event to the Fragments managed by the controller's FragmentManager. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchCreate](../android/app/FragmentController.md))`()` Moves all Fragments managed by the controller's FragmentManager into the create state. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchCreateOptionsMenu](../android/app/FragmentController.md))`(`menu:` ` [Menu](../android/view/Menu.md)!`, `inflater:` ` [MenuInflater](../android/view/MenuInflater.md)!`)` Lets all Fragments managed by the controller's FragmentManager know they should create an options menu. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchDestroy](../android/app/FragmentController.md))`()` Moves all Fragments managed by the controller's FragmentManager into the destroy state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchDestroyView](../android/app/FragmentController.md))`()` Moves all Fragments managed by the controller's FragmentManager into the destroy view state. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchLowMemory](../android/app/FragmentController.md))`()` Lets all Fragments managed by the controller's FragmentManager know the device is in a low memory condition. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchMultiWindowModeChanged](../android/app/FragmentController.md))`(`isInMultiWindowMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Lets all Fragments managed by the controller's FragmentManager know the multi-window mode of the activity changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchMultiWindowModeChanged](../android/app/FragmentController.md))`(`isInMultiWindowMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `newConfig:` ` [Configuration](../android/content/res/Configuration.md)!`)` Lets all Fragments managed by the controller's FragmentManager know the multi-window mode of the activity changed. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchOptionsItemSelected](../android/app/FragmentController.md))`(`item:` ` [MenuItem](../android/view/MenuItem.md)!`)` Sends an option item selection event to the Fragments managed by the controller's FragmentManager. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchOptionsMenuClosed](../android/app/FragmentController.md))`(`menu:` ` [Menu](../android/view/Menu.md)!`)` Lets all Fragments managed by the controller's FragmentManager know their options menu has closed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchPause](../android/app/FragmentController.md))`()` Moves all Fragments managed by the controller's FragmentManager into the pause state. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchPictureInPictureModeChanged](../android/app/FragmentController.md))`(`isInPictureInPictureMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Lets all Fragments managed by the controller's FragmentManager know the picture-in-picture mode of the activity changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchPictureInPictureModeChanged](../android/app/FragmentController.md))`(`isInPictureInPictureMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `newConfig:` ` [Configuration](../android/content/res/Configuration.md)!`)` Lets all Fragments managed by the controller's FragmentManager know the picture-in-picture mode of the activity changed. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchPrepareOptionsMenu](../android/app/FragmentController.md))`(`menu:` ` [Menu](../android/view/Menu.md)!`)` Lets all Fragments managed by the controller's FragmentManager know they should prepare their options menu for display. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchResume](../android/app/FragmentController.md))`()` Moves all Fragments managed by the controller's FragmentManager into the resume state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchStart](../android/app/FragmentController.md))`()` Moves all Fragments managed by the controller's FragmentManager into the start state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchStop](../android/app/FragmentController.md))`()` Moves all Fragments managed by the controller's FragmentManager into the stop state. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchTrimMemory](../android/app/FragmentController.md))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Lets all Fragments managed by the controller's FragmentManager know they should trim their memory usage. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [doLoaderDestroy](../android/app/FragmentController.md))`()` Destroys the loaders and, if their state is not being retained, removes them. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [doLoaderStart](../android/app/FragmentController.md))`()` Starts the loaders. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [doLoaderStop](../android/app/FragmentController.md))`(`retain:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Stops the loaders, optionally retaining their state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dumpLoaders](../android/app/FragmentController.md))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `fd:` ` [FileDescriptor](../java/io/FileDescriptor.md)!`, `writer:` ` [PrintWriter](../java/io/PrintWriter.md)!`, `args:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Dumps the current state of the loaders. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [execPendingActions](../android/app/FragmentController.md))`()` Execute any pending actions for the Fragments managed by the controller's FragmentManager. |
| --- | --- |
| open [Fragment](../android/app/Fragment.md)? | [findFragmentByWho](../android/app/FragmentController.md))`(`who:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a fragment with the given identifier. |
| open [FragmentManager](../android/app/FragmentManager.md)! | [getFragmentManager](../android/app/FragmentController.md))`()` Returns a [FragmentManager](../android/app/FragmentManager.md) for this controller. |
| open [LoaderManager](../android/app/LoaderManager.md)! | [getLoaderManager](../android/app/FragmentController.md))`()` Returns a [LoaderManager](../android/app/LoaderManager.md). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [noteStateNotSaved](../android/app/FragmentController.md))`()` Marks the fragment state as unsaved. |
| open [View](../android/view/View.md)! | [onCreateView](../android/app/FragmentController.md))`(`parent:` ` [View](../android/view/View.md)!`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `context:` ` [Context](../android/content/Context.md)!`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)!`)` Instantiates a Fragment's view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reportLoaderStart](../android/app/FragmentController.md))`()` Lets the loaders know the host is ready to receive notifications. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreAllState](../android/app/FragmentController.md))`(`state:` ` [Parcelable](../android/os/Parcelable.md)!`, `nonConfig:` ` [FragmentManagerNonConfig](../android/app/FragmentManagerNonConfig.md)!`)` Restores the saved state for all Fragments. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreAllState](../android/app/FragmentController.md))`(`state:` ` [Parcelable](../android/os/Parcelable.md)!`, `nonConfigList:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Fragment](../android/app/Fragment.md)!>!`)` Restores the saved state for all Fragments. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreLoaderNonConfig](../android/app/FragmentController.md))`(`loaderManagers:` ` [ArrayMap](../android/util/ArrayMap.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [LoaderManager](../android/app/LoaderManager.md)!>!`)` Restores the saved state for all LoaderManagers. |
| --- | --- |
| open [ArrayMap](../android/util/ArrayMap.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [LoaderManager](../android/app/LoaderManager.md)!\>! | [retainLoaderNonConfig](../android/app/FragmentController.md))`()` Returns a list of LoaderManagers that have opted to retain their instance across configuration changes. |
| open [FragmentManagerNonConfig](../android/app/FragmentManagerNonConfig.md)! | [retainNestedNonConfig](../android/app/FragmentController.md))`()` Returns a nested tree of Fragments that have opted to retain their instance across configuration changes. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Fragment](../android/app/Fragment.md)!\>! | [retainNonConfig](../android/app/FragmentController.md))`()` Returns a list of Fragments that have opted to retain their instance across configuration changes. |
| --- | --- |
| open [Parcelable](../android/os/Parcelable.md)! | [saveAllState](../android/app/FragmentController.md))`()` Saves the state for all Fragments. |

## Public methods

### attachHost

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun attachHost(parent: Fragment!): Unit
```

**Deprecated:** *Deprecated in Java.*

Attaches the host to the FragmentManager for this controller. The host must be attached before the FragmentManager can be used to manage Fragments. 

### createController

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createController(callbacks: FragmentHostCallback<*>!): FragmentController!
```

**Deprecated:** *Deprecated in Java.*

Returns a [FragmentController](../android/app/FragmentController.md). 

### dispatchActivityCreated

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchActivityCreated(): Unit
```

**Deprecated:** *Deprecated in Java.*

Moves all Fragments managed by the controller's FragmentManager into the activity created state.

Call when Fragments should be informed their host has been created. 
**See Also**

- [android.app.Fragment#onActivityCreated(Bundle)](../android/app/Fragment.md)) 

### dispatchConfigurationChanged

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchConfigurationChanged(newConfig: Configuration!): Unit
```

**Deprecated:** *Deprecated in Java.*

Lets all Fragments managed by the controller's FragmentManager know a configuration change occurred.

Call when there is a configuration change. 
**See Also**

- [android.app.Fragment#onConfigurationChanged(Configuration)](../android/app/Fragment.md)) 

### dispatchContextItemSelected

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchContextItemSelected(item: MenuItem!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Sends a context item selection event to the Fragments managed by the controller's FragmentManager. Once the event has been consumed, no additional handling will be performed.

Call immediately after an options menu item has been selected

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the context menu selection event was consumed |

**See Also**

- [android.app.Fragment#onContextItemSelected(MenuItem)](../android/app/Fragment.md)) 

### dispatchCreate

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchCreate(): Unit
```

**Deprecated:** *Deprecated in Java.*

Moves all Fragments managed by the controller's FragmentManager into the create state.

Call when Fragments should be created. 
**See Also**

- [android.app.Fragment#onCreate(Bundle)](../android/app/Fragment.md)) 

### dispatchCreateOptionsMenu

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchCreateOptionsMenu(
    menu: Menu!, 
    inflater: MenuInflater!
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Lets all Fragments managed by the controller's FragmentManager know they should create an options menu.

Call when the Fragment should create an options menu.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the options menu contains items to display |

**See Also**

- [android.app.Fragment#onCreateOptionsMenu(Menu, MenuInflater)](../android/app/Fragment.md)) 

### dispatchDestroy

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchDestroy(): Unit
```

**Deprecated:** *Deprecated in Java.*

Moves all Fragments managed by the controller's FragmentManager into the destroy state.

Call when Fragments should be destroyed. 
**See Also**

- [android.app.Fragment#onDestroy()](../android/app/Fragment.md)) 

### dispatchDestroyView

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchDestroyView(): Unit
```

**Deprecated:** *Deprecated in Java.*

Moves all Fragments managed by the controller's FragmentManager into the destroy view state.

Call when the Fragment's views should be destroyed. 
**See Also**

- [android.app.Fragment#onDestroyView()](../android/app/Fragment.md)) 

### dispatchLowMemory

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchLowMemory(): Unit
```

**Deprecated:** *Deprecated in Java.*

Lets all Fragments managed by the controller's FragmentManager know the device is in a low memory condition.

Call when the device is low on memory and Fragment's should trim their memory usage. 
**See Also**

- [android.app.Fragment#onLowMemory()](../android/app/Fragment.md)) 

### dispatchMultiWindowModeChanged

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchMultiWindowModeChanged(isInMultiWindowMode: Boolean): Unit
```

**Deprecated:** *use [dispatchMultiWindowModeChanged(boolean,android.content.res.Configuration)](../android/app/FragmentController.md))*

Lets all Fragments managed by the controller's FragmentManager know the multi-window mode of the activity changed.

Call when the multi-window mode of the activity changed. 
**See Also**

### dispatchMultiWindowModeChanged

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchMultiWindowModeChanged(
    isInMultiWindowMode: Boolean, 
    newConfig: Configuration!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Lets all Fragments managed by the controller's FragmentManager know the multi-window mode of the activity changed.

Call when the multi-window mode of the activity changed. 
**See Also**

### dispatchOptionsItemSelected

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchOptionsItemSelected(item: MenuItem!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Sends an option item selection event to the Fragments managed by the controller's FragmentManager. Once the event has been consumed, no additional handling will be performed.

Call immediately after an options menu item has been selected

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the options menu selection event was consumed |

**See Also**

- [android.app.Fragment#onOptionsItemSelected(MenuItem)](../android/app/Fragment.md)) 

### dispatchOptionsMenuClosed

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchOptionsMenuClosed(menu: Menu!): Unit
```

**Deprecated:** *Deprecated in Java.*

Lets all Fragments managed by the controller's FragmentManager know their options menu has closed.

Call immediately after closing the Fragment's options menu. 
**See Also**

- [android.app.Fragment#onOptionsMenuClosed(Menu)](../android/app/Fragment.md)) 

### dispatchPause

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchPause(): Unit
```

**Deprecated:** *Deprecated in Java.*

Moves all Fragments managed by the controller's FragmentManager into the pause state.

Call when Fragments should be paused. 
**See Also**

- [android.app.Fragment#onPause()](../android/app/Fragment.md)) 

### dispatchPictureInPictureModeChanged

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchPictureInPictureModeChanged(isInPictureInPictureMode: Boolean): Unit
```

**Deprecated:** *use [dispatchPictureInPictureModeChanged(boolean,android.content.res.Configuration)](../android/app/FragmentController.md))*

Lets all Fragments managed by the controller's FragmentManager know the picture-in-picture mode of the activity changed.

Call when the picture-in-picture mode of the activity changed. 
**See Also**

### dispatchPictureInPictureModeChanged

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchPictureInPictureModeChanged(
    isInPictureInPictureMode: Boolean, 
    newConfig: Configuration!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Lets all Fragments managed by the controller's FragmentManager know the picture-in-picture mode of the activity changed.

Call when the picture-in-picture mode of the activity changed. 
**See Also**

### dispatchPrepareOptionsMenu

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchPrepareOptionsMenu(menu: Menu!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Lets all Fragments managed by the controller's FragmentManager know they should prepare their options menu for display.

Call immediately before displaying the Fragment's options menu.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the options menu contains items to display |

**See Also**

- [android.app.Fragment#onPrepareOptionsMenu(Menu)](../android/app/Fragment.md)) 

### dispatchResume

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchResume(): Unit
```

**Deprecated:** *Deprecated in Java.*

Moves all Fragments managed by the controller's FragmentManager into the resume state.

Call when Fragments should be resumed. 
**See Also**

- [android.app.Fragment#onResume()](../android/app/Fragment.md)) 

### dispatchStart

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchStart(): Unit
```

**Deprecated:** *Deprecated in Java.*

Moves all Fragments managed by the controller's FragmentManager into the start state.

Call when Fragments should be started. 
**See Also**

- [android.app.Fragment#onStart()](../android/app/Fragment.md)) 

### dispatchStop

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchStop(): Unit
```

**Deprecated:** *Deprecated in Java.*

Moves all Fragments managed by the controller's FragmentManager into the stop state.

Call when Fragments should be stopped. 
**See Also**

- [android.app.Fragment#onStop()](../android/app/Fragment.md)) 

### dispatchTrimMemory

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchTrimMemory(level: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Lets all Fragments managed by the controller's FragmentManager know they should trim their memory usage.

Call when the Fragment can release allocated memory \[such as if the Fragment is in the background\]. 
**See Also**

- [android.app.Fragment#onTrimMemory(int)](../android/app/Fragment.md)) 

### doLoaderDestroy

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun doLoaderDestroy(): Unit
```

**Deprecated:** *Deprecated in Java.*

Destroys the loaders and, if their state is not being retained, removes them. 

### doLoaderStart

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun doLoaderStart(): Unit
```

**Deprecated:** *Deprecated in Java.*

Starts the loaders. 

### doLoaderStop

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun doLoaderStop(retain: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Stops the loaders, optionally retaining their state. This is useful for keeping the loader state across configuration changes.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `retain` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):When`true`, the loaders aren't stopped, but, their instances are retained in a started state |

### dumpLoaders

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dumpLoaders(
    prefix: String!, 
    fd: FileDescriptor!, 
    writer: PrintWriter!, 
    args: Array<String!>!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Dumps the current state of the loaders. 

### execPendingActions

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun execPendingActions(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Execute any pending actions for the Fragments managed by the controller's FragmentManager.

Call when queued actions can be performed \[eg when the Fragment moves into a start or resume state\].

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if queued actions were performed |

### findFragmentByWho

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun findFragmentByWho(who: String!): Fragment?
```

**Deprecated:** *Deprecated in Java.*

Returns a fragment with the given identifier.

| Return ||
|----------------------------------------------------------------------------------|--------------------------|
| [Fragment](../android/app/Fragment.md)? | This value may be`null`. |

### getFragmentManager

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFragmentManager(): FragmentManager!
```

**Deprecated:** *Deprecated in Java.*

Returns a [FragmentManager](../android/app/FragmentManager.md) for this controller. 

### getLoaderManager

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLoaderManager(): LoaderManager!
```

**Deprecated:** *Deprecated in Java.*

Returns a [LoaderManager](../android/app/LoaderManager.md). 

### noteStateNotSaved

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun noteStateNotSaved(): Unit
```

**Deprecated:** *Deprecated in Java.*

Marks the fragment state as unsaved. This allows for "state loss" detection. 

### onCreateView

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCreateView(
    parent: View!, 
    name: String!, 
    context: Context!, 
    attrs: AttributeSet!
): View!
```

**Deprecated:** *Deprecated in Java.*

Instantiates a Fragment's view.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [View](../android/view/View.md)!:The parent that the created view will be placed in;*note that this may be null*. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Tag name to be inflated. |
| `context` | [Context](../android/content/Context.md)!:The context the view is being created in. |
| --- | --- |
| `attrs` | [AttributeSet](../android/util/AttributeSet.md)!:Inflation attributes as specified in XML file. |

| Return ||
|---------------------------------------------------------------------------------|-----------------------------|
| [View](../android/view/View.md)! | view the newly created view |

### reportLoaderStart

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reportLoaderStart(): Unit
```

**Deprecated:** *Deprecated in Java.*

Lets the loaders know the host is ready to receive notifications. 

### restoreAllState

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun restoreAllState(
    state: Parcelable!, 
    nonConfig: FragmentManagerNonConfig!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Restores the saved state for all Fragments. The given FragmentManagerNonConfig are Fragment instances retained across configuration changes, including nested fragments 
**See Also**

- <https://developer.android.com/reference/kotlin/android/app/FragmentController#retainNestedNonConfig()> 

### restoreAllState

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun restoreAllState(
    state: Parcelable!, 
    nonConfigList: MutableList<Fragment!>!
): Unit
```

**Deprecated:** *use [restoreAllState(android.os.Parcelable,android.app.FragmentManagerNonConfig)](../android/app/FragmentController.md))*

Restores the saved state for all Fragments. The given Fragment list are Fragment instances retained across configuration changes. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/app/FragmentController#retainNonConfig()> 

### restoreLoaderNonConfig

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun restoreLoaderNonConfig(loaderManagers: ArrayMap<String!, LoaderManager!>!): Unit
```

**Deprecated:** *Deprecated in Java.*

Restores the saved state for all LoaderManagers. The given LoaderManager list are LoaderManager instances retained across configuration changes. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/app/FragmentController#retainLoaderNonConfig()> 

### retainLoaderNonConfig

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun retainLoaderNonConfig(): ArrayMap<String!, LoaderManager!>!
```

**Deprecated:** *Deprecated in Java.*

Returns a list of LoaderManagers that have opted to retain their instance across configuration changes. 

### retainNestedNonConfig

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun retainNestedNonConfig(): FragmentManagerNonConfig!
```

**Deprecated:** *Deprecated in Java.*

Returns a nested tree of Fragments that have opted to retain their instance across configuration changes. 

### retainNonConfig

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun retainNonConfig(): MutableList<Fragment!>!
```

**Deprecated:** *use [retainNestedNonConfig()](../android/app/FragmentController.md))to also track retained nested child fragments*

Returns a list of Fragments that have opted to retain their instance across configuration changes. 

### saveAllState

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun saveAllState(): Parcelable!
```

**Deprecated:** *Deprecated in Java.*

Saves the state for all Fragments.
