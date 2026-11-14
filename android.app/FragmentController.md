# FragmentController

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FragmentController

Kotlin| [Java](https://developer.android.com/reference/android/app/FragmentController "View this page in Java") 

```
open class FragmentController
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.FragmentController](https://developer.android.com/reference/kotlin/android/app/FragmentController#) |

| **This class was deprecated in API level 28.**
|
| Use the [Support Library](https://developer.android.com/tools/extras/support-library.html) androidx.fragment.app.FragmentController

Provides integration points with a [FragmentManager](https://developer.android.com/reference/kotlin/android/app/FragmentManager) for a fragment host.

It is the responsibility of the host to take care of the Fragment's lifecycle. The methods provided by [FragmentController](https://developer.android.com/reference/kotlin/android/app/FragmentController#) are for that purpose.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [attachHost](https://developer.android.com/reference/kotlin/android/app/FragmentController#attachHost(android.app.Fragment))`(`parent:` ` [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!`)` Attaches the host to the FragmentManager for this controller. |
| static [FragmentController](https://developer.android.com/reference/kotlin/android/app/FragmentController#)! | [createController](https://developer.android.com/reference/kotlin/android/app/FragmentController#createController(android.app.FragmentHostCallback))`(`callbacks:` ` [FragmentHostCallback](https://developer.android.com/reference/kotlin/android/app/FragmentHostCallback)<*>!`)` Returns a [FragmentController](https://developer.android.com/reference/kotlin/android/app/FragmentController#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchActivityCreated](https://developer.android.com/reference/kotlin/android/app/FragmentController#dispatchActivityCreated())`()` Moves all Fragments managed by the controller's FragmentManager into the activity created state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchConfigurationChanged](https://developer.android.com/reference/kotlin/android/app/FragmentController#dispatchConfigurationChanged(android.content.res.Configuration))`(`newConfig:` ` [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)!`)` Lets all Fragments managed by the controller's FragmentManager know a configuration change occurred. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchContextItemSelected](https://developer.android.com/reference/kotlin/android/app/FragmentController#dispatchContextItemSelected(android.view.MenuItem))`(`item:` ` [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem.html#)!`)` Sends a context item selection event to the Fragments managed by the controller's FragmentManager. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchCreate](https://developer.android.com/reference/kotlin/android/app/FragmentController#dispatchCreate())`()` Moves all Fragments managed by the controller's FragmentManager into the create state. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchCreateOptionsMenu](https://developer.android.com/reference/kotlin/android/app/FragmentController#dispatchCreateOptionsMenu(android.view.Menu,%20android.view.MenuInflater))`(`menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)!`, `inflater:` ` [MenuInflater](https://developer.android.com/reference/kotlin/android/view/MenuInflater.html#)!`)` Lets all Fragments managed by the controller's FragmentManager know they should create an options menu. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchDestroy](https://developer.android.com/reference/kotlin/android/app/FragmentController#dispatchDestroy())`()` Moves all Fragments managed by the controller's FragmentManager into the destroy state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchDestroyView](https://developer.android.com/reference/kotlin/android/app/FragmentController#dispatchDestroyView())`()` Moves all Fragments managed by the controller's FragmentManager into the destroy view state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchLowMemory](https://developer.android.com/reference/kotlin/android/app/FragmentController#dispatchLowMemory())`()` Lets all Fragments managed by the controller's FragmentManager know the device is in a low memory condition. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchMultiWindowModeChanged](https://developer.android.com/reference/kotlin/android/app/FragmentController#dispatchMultiWindowModeChanged(kotlin.Boolean))`(`isInMultiWindowMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Lets all Fragments managed by the controller's FragmentManager know the multi-window mode of the activity changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchMultiWindowModeChanged](https://developer.android.com/reference/kotlin/android/app/FragmentController#dispatchMultiWindowModeChanged(kotlin.Boolean,%20android.content.res.Configuration))`(`isInMultiWindowMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `newConfig:` ` [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)!`)` Lets all Fragments managed by the controller's FragmentManager know the multi-window mode of the activity changed. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchOptionsItemSelected](https://developer.android.com/reference/kotlin/android/app/FragmentController#dispatchOptionsItemSelected(android.view.MenuItem))`(`item:` ` [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem.html#)!`)` Sends an option item selection event to the Fragments managed by the controller's FragmentManager. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchOptionsMenuClosed](https://developer.android.com/reference/kotlin/android/app/FragmentController#dispatchOptionsMenuClosed(android.view.Menu))`(`menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)!`)` Lets all Fragments managed by the controller's FragmentManager know their options menu has closed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchPause](https://developer.android.com/reference/kotlin/android/app/FragmentController#dispatchPause())`()` Moves all Fragments managed by the controller's FragmentManager into the pause state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchPictureInPictureModeChanged](https://developer.android.com/reference/kotlin/android/app/FragmentController#dispatchPictureInPictureModeChanged(kotlin.Boolean))`(`isInPictureInPictureMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Lets all Fragments managed by the controller's FragmentManager know the picture-in-picture mode of the activity changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchPictureInPictureModeChanged](https://developer.android.com/reference/kotlin/android/app/FragmentController#dispatchPictureInPictureModeChanged(kotlin.Boolean,%20android.content.res.Configuration))`(`isInPictureInPictureMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `newConfig:` ` [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)!`)` Lets all Fragments managed by the controller's FragmentManager know the picture-in-picture mode of the activity changed. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchPrepareOptionsMenu](https://developer.android.com/reference/kotlin/android/app/FragmentController#dispatchPrepareOptionsMenu(android.view.Menu))`(`menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)!`)` Lets all Fragments managed by the controller's FragmentManager know they should prepare their options menu for display. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchResume](https://developer.android.com/reference/kotlin/android/app/FragmentController#dispatchResume())`()` Moves all Fragments managed by the controller's FragmentManager into the resume state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchStart](https://developer.android.com/reference/kotlin/android/app/FragmentController#dispatchStart())`()` Moves all Fragments managed by the controller's FragmentManager into the start state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchStop](https://developer.android.com/reference/kotlin/android/app/FragmentController#dispatchStop())`()` Moves all Fragments managed by the controller's FragmentManager into the stop state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchTrimMemory](https://developer.android.com/reference/kotlin/android/app/FragmentController#dispatchTrimMemory(kotlin.Int))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Lets all Fragments managed by the controller's FragmentManager know they should trim their memory usage. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [doLoaderDestroy](https://developer.android.com/reference/kotlin/android/app/FragmentController#doLoaderDestroy())`()` Destroys the loaders and, if their state is not being retained, removes them. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [doLoaderStart](https://developer.android.com/reference/kotlin/android/app/FragmentController#doLoaderStart())`()` Starts the loaders. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [doLoaderStop](https://developer.android.com/reference/kotlin/android/app/FragmentController#doLoaderStop(kotlin.Boolean))`(`retain:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Stops the loaders, optionally retaining their state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dumpLoaders](https://developer.android.com/reference/kotlin/android/app/FragmentController#dumpLoaders(kotlin.String,%20java.io.FileDescriptor,%20java.io.PrintWriter,%20kotlin.Array))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!`, `writer:` ` [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)!`, `args:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Dumps the current state of the loaders. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [execPendingActions](https://developer.android.com/reference/kotlin/android/app/FragmentController#execPendingActions())`()` Execute any pending actions for the Fragments managed by the controller's FragmentManager. |
| open [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)? | [findFragmentByWho](https://developer.android.com/reference/kotlin/android/app/FragmentController#findFragmentByWho(kotlin.String))`(`who:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a fragment with the given identifier. |
| open [FragmentManager](https://developer.android.com/reference/kotlin/android/app/FragmentManager)! | [getFragmentManager](https://developer.android.com/reference/kotlin/android/app/FragmentController#getFragmentManager())`()` Returns a [FragmentManager](https://developer.android.com/reference/kotlin/android/app/FragmentManager) for this controller. |
| open [LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager)! | [getLoaderManager](https://developer.android.com/reference/kotlin/android/app/FragmentController#getLoaderManager())`()` Returns a [LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [noteStateNotSaved](https://developer.android.com/reference/kotlin/android/app/FragmentController#noteStateNotSaved())`()` Marks the fragment state as unsaved. |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [onCreateView](https://developer.android.com/reference/kotlin/android/app/FragmentController#onCreateView(android.view.View,%20kotlin.String,%20android.content.Context,%20android.util.AttributeSet))`(`parent:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`)` Instantiates a Fragment's view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reportLoaderStart](https://developer.android.com/reference/kotlin/android/app/FragmentController#reportLoaderStart())`()` Lets the loaders know the host is ready to receive notifications. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreAllState](https://developer.android.com/reference/kotlin/android/app/FragmentController#restoreAllState(android.os.Parcelable,%20android.app.FragmentManagerNonConfig))`(`state:` ` [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#)!`, `nonConfig:` ` [FragmentManagerNonConfig](https://developer.android.com/reference/kotlin/android/app/FragmentManagerNonConfig)!`)` Restores the saved state for all Fragments. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreAllState](https://developer.android.com/reference/kotlin/android/app/FragmentController#restoreAllState(android.os.Parcelable,%20kotlin.collections.MutableList))`(`state:` ` [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#)!`, `nonConfigList:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!>!`)` Restores the saved state for all Fragments. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreLoaderNonConfig](https://developer.android.com/reference/kotlin/android/app/FragmentController#restoreLoaderNonConfig(android.util.ArrayMap))`(`loaderManagers:` ` [ArrayMap](https://developer.android.com/reference/kotlin/android/util/ArrayMap.html#)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager)!>!`)` Restores the saved state for all LoaderManagers. |
| open [ArrayMap](https://developer.android.com/reference/kotlin/android/util/ArrayMap.html#)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager)!\>! | [retainLoaderNonConfig](https://developer.android.com/reference/kotlin/android/app/FragmentController#retainLoaderNonConfig())`()` Returns a list of LoaderManagers that have opted to retain their instance across configuration changes. |
| open [FragmentManagerNonConfig](https://developer.android.com/reference/kotlin/android/app/FragmentManagerNonConfig)! | [retainNestedNonConfig](https://developer.android.com/reference/kotlin/android/app/FragmentController#retainNestedNonConfig())`()` Returns a nested tree of Fragments that have opted to retain their instance across configuration changes. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!\>! | [retainNonConfig](https://developer.android.com/reference/kotlin/android/app/FragmentController#retainNonConfig())`()` Returns a list of Fragments that have opted to retain their instance across configuration changes. |
| open [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#)! | [saveAllState](https://developer.android.com/reference/kotlin/android/app/FragmentController#saveAllState())`()` Saves the state for all Fragments. |

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

Returns a [FragmentController](https://developer.android.com/reference/kotlin/android/app/FragmentController#). 

### dispatchActivityCreated

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchActivityCreated(): Unit
```

**Deprecated:** *Deprecated in Java.*

Moves all Fragments managed by the controller's FragmentManager into the activity created state.

Call when Fragments should be informed their host has been created. 
**See Also**

- [android.app.Fragment#onActivityCreated(Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onActivityCreated(android.os.Bundle)) 

### dispatchConfigurationChanged

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchConfigurationChanged(newConfig: Configuration!): Unit
```

**Deprecated:** *Deprecated in Java.*

Lets all Fragments managed by the controller's FragmentManager know a configuration change occurred.

Call when there is a configuration change. 
**See Also**

- [android.app.Fragment#onConfigurationChanged(Configuration)](https://developer.android.com/reference/kotlin/android/app/Fragment#onConfigurationChanged(android.content.res.Configuration)) 

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

- [android.app.Fragment#onContextItemSelected(MenuItem)](https://developer.android.com/reference/kotlin/android/app/Fragment#onContextItemSelected(android.view.MenuItem)) 

### dispatchCreate

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchCreate(): Unit
```

**Deprecated:** *Deprecated in Java.*

Moves all Fragments managed by the controller's FragmentManager into the create state.

Call when Fragments should be created. 
**See Also**

- [android.app.Fragment#onCreate(Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreate(android.os.Bundle)) 

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

- [android.app.Fragment#onCreateOptionsMenu(Menu, MenuInflater)](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateOptionsMenu(android.view.Menu,%20android.view.MenuInflater)) 

### dispatchDestroy

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchDestroy(): Unit
```

**Deprecated:** *Deprecated in Java.*

Moves all Fragments managed by the controller's FragmentManager into the destroy state.

Call when Fragments should be destroyed. 
**See Also**

- [android.app.Fragment#onDestroy()](https://developer.android.com/reference/kotlin/android/app/Fragment#onDestroy()) 

### dispatchDestroyView

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchDestroyView(): Unit
```

**Deprecated:** *Deprecated in Java.*

Moves all Fragments managed by the controller's FragmentManager into the destroy view state.

Call when the Fragment's views should be destroyed. 
**See Also**

- [android.app.Fragment#onDestroyView()](https://developer.android.com/reference/kotlin/android/app/Fragment#onDestroyView()) 

### dispatchLowMemory

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchLowMemory(): Unit
```

**Deprecated:** *Deprecated in Java.*

Lets all Fragments managed by the controller's FragmentManager know the device is in a low memory condition.

Call when the device is low on memory and Fragment's should trim their memory usage. 
**See Also**

- [android.app.Fragment#onLowMemory()](https://developer.android.com/reference/kotlin/android/app/Fragment#onLowMemory()) 

### dispatchMultiWindowModeChanged

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchMultiWindowModeChanged(isInMultiWindowMode: Boolean): Unit
```

**Deprecated:** *use [dispatchMultiWindowModeChanged(boolean,android.content.res.Configuration)](https://developer.android.com/reference/kotlin/android/app/FragmentController#dispatchMultiWindowModeChanged(kotlin.Boolean,%20android.content.res.Configuration))*

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

- [android.app.Fragment#onOptionsItemSelected(MenuItem)](https://developer.android.com/reference/kotlin/android/app/Fragment#onOptionsItemSelected(android.view.MenuItem)) 

### dispatchOptionsMenuClosed

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchOptionsMenuClosed(menu: Menu!): Unit
```

**Deprecated:** *Deprecated in Java.*

Lets all Fragments managed by the controller's FragmentManager know their options menu has closed.

Call immediately after closing the Fragment's options menu. 
**See Also**

- [android.app.Fragment#onOptionsMenuClosed(Menu)](https://developer.android.com/reference/kotlin/android/app/Fragment#onOptionsMenuClosed(android.view.Menu)) 

### dispatchPause

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchPause(): Unit
```

**Deprecated:** *Deprecated in Java.*

Moves all Fragments managed by the controller's FragmentManager into the pause state.

Call when Fragments should be paused. 
**See Also**

- [android.app.Fragment#onPause()](https://developer.android.com/reference/kotlin/android/app/Fragment#onPause()) 

### dispatchPictureInPictureModeChanged

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchPictureInPictureModeChanged(isInPictureInPictureMode: Boolean): Unit
```

**Deprecated:** *use [dispatchPictureInPictureModeChanged(boolean,android.content.res.Configuration)](https://developer.android.com/reference/kotlin/android/app/FragmentController#dispatchPictureInPictureModeChanged(kotlin.Boolean,%20android.content.res.Configuration))*

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

- [android.app.Fragment#onPrepareOptionsMenu(Menu)](https://developer.android.com/reference/kotlin/android/app/Fragment#onPrepareOptionsMenu(android.view.Menu)) 

### dispatchResume

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchResume(): Unit
```

**Deprecated:** *Deprecated in Java.*

Moves all Fragments managed by the controller's FragmentManager into the resume state.

Call when Fragments should be resumed. 
**See Also**

- [android.app.Fragment#onResume()](https://developer.android.com/reference/kotlin/android/app/Fragment#onResume()) 

### dispatchStart

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchStart(): Unit
```

**Deprecated:** *Deprecated in Java.*

Moves all Fragments managed by the controller's FragmentManager into the start state.

Call when Fragments should be started. 
**See Also**

- [android.app.Fragment#onStart()](https://developer.android.com/reference/kotlin/android/app/Fragment#onStart()) 

### dispatchStop

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchStop(): Unit
```

**Deprecated:** *Deprecated in Java.*

Moves all Fragments managed by the controller's FragmentManager into the stop state.

Call when Fragments should be stopped. 
**See Also**

- [android.app.Fragment#onStop()](https://developer.android.com/reference/kotlin/android/app/Fragment#onStop()) 

### dispatchTrimMemory

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dispatchTrimMemory(level: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Lets all Fragments managed by the controller's FragmentManager know they should trim their memory usage.

Call when the Fragment can release allocated memory \[such as if the Fragment is in the background\]. 
**See Also**

- [android.app.Fragment#onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/app/Fragment#onTrimMemory(kotlin.Int)) 

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
| [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)? | This value may be`null`. |

### getFragmentManager

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFragmentManager(): FragmentManager!
```

**Deprecated:** *Deprecated in Java.*

Returns a [FragmentManager](https://developer.android.com/reference/kotlin/android/app/FragmentManager) for this controller. 

### getLoaderManager

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLoaderManager(): LoaderManager!
```

**Deprecated:** *Deprecated in Java.*

Returns a [LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager). 

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
| `parent` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The parent that the created view will be placed in;*note that this may be null*. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Tag name to be inflated. |
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The context the view is being created in. |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!:Inflation attributes as specified in XML file. |

| Return ||
|---------------------------------------------------------------------------------|-----------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | view the newly created view |

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

**Deprecated:** *use [restoreAllState(android.os.Parcelable,android.app.FragmentManagerNonConfig)](https://developer.android.com/reference/kotlin/android/app/FragmentController#restoreAllState(android.os.Parcelable,%20android.app.FragmentManagerNonConfig))*

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

**Deprecated:** *use [retainNestedNonConfig()](https://developer.android.com/reference/kotlin/android/app/FragmentController#retainNestedNonConfig())to also track retained nested child fragments*

Returns a list of Fragments that have opted to retain their instance across configuration changes. 

### saveAllState

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun saveAllState(): Parcelable!
```

**Deprecated:** *Deprecated in Java.*

Saves the state for all Fragments.
