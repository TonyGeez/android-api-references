Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DialogFragment

```
open class DialogFragment : Fragment, DialogInterface.OnCancelListener, DialogInterface.OnDismissListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.app.Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment) ||
| | ↳ | [android.app.DialogFragment](https://developer.android.com/reference/kotlin/android/app/DialogFragment#) |

> [!CAUTION]
> **This class was deprecated in API level 28.**
>
> Use the [Support Library](https://developer.android.com/tools/extras/support-library.html) androidx.fragment.app.DialogFragment for consistent behavior across all devices and access to [Lifecycle](https://developer.android.com/topic/libraries/architecture/lifecycle.html).

A fragment that displays a dialog window, floating on top of its activity's window. This fragment contains a Dialog object, which it displays as appropriate based on the fragment's state. Control of the dialog (deciding when to show, hide, dismiss it) should be done through the API here, not with direct calls on the dialog.

Implementations should override this class and implement `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle)` to supply the content of the dialog. Alternatively, they can override `https://developer.android.com/reference/kotlin/android/app/DialogFragment#onCreateDialog(android.os.Bundle)` to create an entirely custom dialog, such as an AlertDialog, with its own content.

Topics covered here:

1. [Lifecycle](https://developer.android.com/reference/kotlin/android/app/DialogFragment#Lifecycle)
2. [Basic Dialog](https://developer.android.com/reference/kotlin/android/app/DialogFragment#BasicDialog)
3. [Alert Dialog](https://developer.android.com/reference/kotlin/android/app/DialogFragment#AlertDialog)
4. [Selecting Between Dialog or Embedding](https://developer.android.com/reference/kotlin/android/app/DialogFragment#DialogOrEmbed)

### Lifecycle

DialogFragment does various things to keep the fragment's lifecycle driving it, instead of the Dialog. Note that dialogs are generally autonomous entities -- they are their own window, receiving their own input events, and often deciding on their own when to disappear (by receiving a back key event or the user clicking on a button).

DialogFragment needs to ensure that what is happening with the Fragment and Dialog states remains consistent. To do this, it watches for dismiss events from the dialog and takes care of removing its own state when they happen. This means you should use `https://developer.android.com/reference/kotlin/android/app/DialogFragment#show(android.app.FragmentManager,%20kotlin.String)` or `https://developer.android.com/reference/kotlin/android/app/DialogFragment#show(android.app.FragmentTransaction,%20kotlin.String)` to add an instance of DialogFragment to your UI, as these keep track of how DialogFragment should remove itself when the dialog is dismissed.

### Basic Dialog

The simplest use of DialogFragment is as a floating container for the fragment's view hierarchy. A simple implementation may look like this:

An example showDialog() method on the Activity could be:

This removes any currently shown dialog, creates a new DialogFragment with an argument, and shows it as a new state on the back stack. When the transaction is popped, the current DialogFragment and its Dialog will be destroyed, and the previous one (if any) re-shown. Note that in this case DialogFragment will take care of popping the transaction of the Dialog is dismissed separately from it.

### Alert Dialog

Instead of (or in addition to) implementing `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle)` to generate the view hierarchy inside of a dialog, you may implement `https://developer.android.com/reference/kotlin/android/app/DialogFragment#onCreateDialog(android.os.Bundle)` to create your own custom Dialog object.

This is most useful for creating an `https://developer.android.com/reference/kotlin/android/app/AlertDialog`, allowing you to display standard alerts to the user that are managed by a fragment. A simple example implementation of this is:

The activity creating this fragment may have the following methods to show the dialog and receive results from it:

Note that in this case the fragment is not placed on the back stack, it is just added as an indefinitely running fragment. Because dialogs normally are modal, this will still operate as a back stack, since the dialog will capture user input until it is dismissed. When it is dismissed, DialogFragment will take care of removing itself from its fragment manager.

### Selecting Between Dialog or Embedding

A DialogFragment can still optionally be used as a normal fragment, if desired. This is useful if you have a fragment that in some cases should be shown as a dialog and others embedded in a larger UI. This behavior will normally be automatically selected for you based on how you are using the fragment, but can be customized with `https://developer.android.com/reference/kotlin/android/app/DialogFragment#setShowsDialog(kotlin.Boolean)`.

For example, here is a simple dialog fragment:

An instance of this fragment can be created and shown as a dialog:

It can also be added as content in a view hierarchy:

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#STYLE_NORMAL:kotlin.Int` Style for `https://developer.android.com/reference/kotlin/android/app/DialogFragment#setStyle(kotlin.Int,%20kotlin.Int)`: a basic, normal dialog. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#STYLE_NO_FRAME:kotlin.Int` Style for `https://developer.android.com/reference/kotlin/android/app/DialogFragment#setStyle(kotlin.Int,%20kotlin.Int)`: don't draw any frame at all; the view hierarchy returned by `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle)` is entirely responsible for drawing the dialog. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#STYLE_NO_INPUT:kotlin.Int` Style for `https://developer.android.com/reference/kotlin/android/app/DialogFragment#setStyle(kotlin.Int,%20kotlin.Int)`: like `https://developer.android.com/reference/kotlin/android/app/DialogFragment#STYLE_NO_FRAME:kotlin.Int`, but also disables all input to the dialog. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#STYLE_NO_TITLE:kotlin.Int` Style for `https://developer.android.com/reference/kotlin/android/app/DialogFragment#setStyle(kotlin.Int,%20kotlin.Int)`: don't include a title area. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_BACKGROUND:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process has gone on to the LRU list. This is a good opportunity to clean up resources that can efficiently and quickly be re-built if the user returns to the app.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_COMPLETE:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is nearing the end of the background LRU list, and if more memory isn't found soon it will be killed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_MODERATE:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is around the middle of the background LRU list; freeing memory can help the system keep other processes running later in the list for better overall performance.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_CRITICAL:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running extremely low on memory and is about to not be able to keep any background processes running. Your running process should free up as many non-critical resources as it can to allow that memory to be used elsewhere. The next thing that will happen after this is `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onLowMemory()` called to report that nothing at all can be kept in the background, a situation that can start to notably impact the user.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_LOW:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running low on memory. Your running process should free up unneeded resources to allow that memory to be used elsewhere.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_MODERATE:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running moderately low on memory. Your running process may want to release some unneeded resources for use elsewhere.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_UI_HIDDEN:kotlin.Int`

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)`: the process had been showing a user interface, and is no longer doing so. Large allocations with the UI should be released at this point to allow memory to be better managed.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/DialogFragment#DialogFragment()()` <br /> |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#dismiss()()` Dismiss the fragment and its dialog. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#dismissAllowingStateLoss()()` Version of `https://developer.android.com/reference/kotlin/android/app/DialogFragment#dismiss()` that uses `https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#commitAllowingStateLoss()`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#dump(kotlin.String,%20java.io.FileDescriptor,%20java.io.PrintWriter,%20kotlin.Array)(prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, writer: https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#!, args: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Print the Fragments's state into the given stream. |
| open [Dialog](https://developer.android.com/reference/kotlin/android/app/Dialog)! | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#getDialog()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#getShowsDialog()()` Return the current value of `https://developer.android.com/reference/kotlin/android/app/DialogFragment#setShowsDialog(kotlin.Boolean)`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#getTheme()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#isCancelable()()` Return the current value of `https://developer.android.com/reference/kotlin/android/app/DialogFragment#setCancelable(kotlin.Boolean)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#onActivityCreated(android.os.Bundle)(savedInstanceState: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Called when the fragment's activity has been created and this fragment's view hierarchy instantiated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#onAttach(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` Called when a fragment is first attached to its context. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#onCancel(android.content.DialogInterface)(dialog: https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#!)` This method will be invoked when the dialog is canceled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#onCreate(android.os.Bundle)(savedInstanceState: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Called to do initial creation of a fragment. |
| open [Dialog](https://developer.android.com/reference/kotlin/android/app/Dialog)! | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#onCreateDialog(android.os.Bundle)(savedInstanceState: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Override to build your own custom Dialog container. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#onDestroyView()()` Remove dialog. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#onDetach()()` Called when the fragment is no longer attached to its activity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#onDismiss(android.content.DialogInterface)(dialog: https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#!)` This method will be invoked when the dialog is dismissed. |
| open [LayoutInflater](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#)! | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#onGetLayoutInflater(android.os.Bundle)(savedInstanceState: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Returns the LayoutInflater used to inflate Views of this Fragment. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#onSaveInstanceState(android.os.Bundle)(outState: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Called to ask the fragment to save its current dynamic state, so it can later be reconstructed in a new instance of its process is restarted. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#onStart()()` Called when the Fragment is visible to the user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#onStop()()` Called when the Fragment is no longer started. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#setCancelable(kotlin.Boolean)(cancelable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Control whether the shown Dialog is cancelable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#setShowsDialog(kotlin.Boolean)(showsDialog: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Controls whether this fragment should be shown in a dialog. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#setStyle(kotlin.Int,%20kotlin.Int)(style: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, theme: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Call to customize the basic appearance and behavior of the fragment's dialog. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#show(android.app.FragmentManager,%20kotlin.String)(manager: https://developer.android.com/reference/kotlin/android/app/FragmentManager!, tag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Display the dialog, adding the fragment to the given FragmentManager. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/DialogFragment#show(android.app.FragmentTransaction,%20kotlin.String)(transaction: https://developer.android.com/reference/kotlin/android/app/FragmentTransaction!, tag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Display the dialog, adding the fragment using an existing transaction and then committing the transaction. |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/app/Fragment` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)`

Subclasses can not override equals().

<br />

`https://developer.android.com/reference/kotlin/android/app/Activity!` `https://developer.android.com/reference/kotlin/android/app/Fragment#getActivity()()`

Return the Activity this fragment is currently associated with.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#getAllowEnterTransitionOverlap()()`

Returns whether the exit transition and enter transition overlap or not. When true, the enter transition will start as soon as possible. When false, the enter transition will wait until the exit transition completes before starting.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#getAllowReturnTransitionOverlap()()`

Returns whether the return transition and reenter transition overlap or not. When true, the reenter transition will start as soon as possible. When false, the reenter transition will wait until the return transition completes before starting.

<br />

`https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` `https://developer.android.com/reference/kotlin/android/app/Fragment#getArguments()()`

Return the arguments supplied to `https://developer.android.com/reference/kotlin/android/app/Fragment#setArguments(android.os.Bundle)`, if any.

<br />

`https://developer.android.com/reference/kotlin/android/app/FragmentManager!` `https://developer.android.com/reference/kotlin/android/app/Fragment#getChildFragmentManager()()`

Return a private FragmentManager for placing and managing Fragments inside of this Fragment.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.html#!` `https://developer.android.com/reference/kotlin/android/app/Fragment#getContext()()`

Return the `https://developer.android.com/reference/kotlin/android/content/Context.html#` this fragment is currently associated with.

<br />

`https://developer.android.com/reference/kotlin/android/transition/Transition.html#!` `https://developer.android.com/reference/kotlin/android/app/Fragment#getEnterTransition()()`

Returns the Transition that will be used to move Views into the initial scene. The entering Views will be those that are regular Views or ViewGroups that have `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#isTransitionGroup()` return true. Typical Transitions will extend `https://developer.android.com/reference/kotlin/android/transition/Visibility.html#` as entering is governed by changing visibility from `https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int`.

<br />

`https://developer.android.com/reference/kotlin/android/transition/Transition.html#!` `https://developer.android.com/reference/kotlin/android/app/Fragment#getExitTransition()()`

Returns the Transition that will be used to move Views out of the scene when the fragment is removed, hidden, or detached when not popping the back stack. The exiting Views will be those that are regular Views or ViewGroups that have `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#isTransitionGroup()` return true. Typical Transitions will extend `https://developer.android.com/reference/kotlin/android/transition/Visibility.html#` as exiting is governed by changing visibility from `https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int`. If transition is null, the views will remain unaffected.

<br />

`https://developer.android.com/reference/kotlin/android/app/FragmentManager!` `https://developer.android.com/reference/kotlin/android/app/Fragment#getFragmentManager()()`

Return the FragmentManager for interacting with fragments associated with this fragment's activity. Note that this will be non-null slightly before `https://developer.android.com/reference/kotlin/android/app/Fragment#getActivity()`, during the time from when the fragment is placed in a `https://developer.android.com/reference/kotlin/android/app/FragmentTransaction` until it is committed and attached to its activity.

If this Fragment is a child of another Fragment, the FragmentManager returned here will be the parent's `https://developer.android.com/reference/kotlin/android/app/Fragment#getChildFragmentManager()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?` `https://developer.android.com/reference/kotlin/android/app/Fragment#getHost()()`

Return the host object of this fragment. May return `null` if the fragment isn't currently being hosted.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#getId()()`

Return the identifier this fragment is known by. This is either the android:id value supplied in a layout or the container view ID supplied when adding the fragment.

<br />

`https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#!` `https://developer.android.com/reference/kotlin/android/app/Fragment#getLayoutInflater()()`

Returns the cached LayoutInflater used to inflate Views of this Fragment. If `https://developer.android.com/reference/kotlin/android/app/Fragment#onGetLayoutInflater(android.os.Bundle)` has not been called `https://developer.android.com/reference/kotlin/android/app/Fragment#onGetLayoutInflater(android.os.Bundle)` will be called with a `null` argument and that value will be cached.

The cached LayoutInflater will be replaced immediately prior to `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle)` and cleared immediately after `https://developer.android.com/reference/kotlin/android/app/Fragment#onDetach()`.

<br />

`https://developer.android.com/reference/kotlin/android/app/LoaderManager!` `https://developer.android.com/reference/kotlin/android/app/Fragment#getLoaderManager()()`

Return the LoaderManager for this fragment, creating it if needed.

<br />

`https://developer.android.com/reference/kotlin/android/app/Fragment!` `https://developer.android.com/reference/kotlin/android/app/Fragment#getParentFragment()()`

Returns the parent Fragment containing this Fragment. If this Fragment is attached directly to an Activity, returns null.

<br />

`https://developer.android.com/reference/kotlin/android/transition/Transition.html#!` `https://developer.android.com/reference/kotlin/android/app/Fragment#getReenterTransition()()`

Returns the Transition that will be used to move Views in to the scene when returning due to popping a back stack. The entering Views will be those that are regular Views or ViewGroups that have `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#isTransitionGroup()` return true. Typical Transitions will extend `https://developer.android.com/reference/kotlin/android/transition/Visibility.html#` as exiting is governed by changing visibility from `https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int`. If transition is null, the views will remain unaffected. If nothing is set, the default will be to use the same transition as `https://developer.android.com/reference/kotlin/android/app/Fragment#setExitTransition(android.transition.Transition)`.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/Resources.html#!` `https://developer.android.com/reference/kotlin/android/app/Fragment#getResources()()`

Return `getActivity().getResources()`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#getRetainInstance()()`

<br />

`https://developer.android.com/reference/kotlin/android/transition/Transition.html#!` `https://developer.android.com/reference/kotlin/android/app/Fragment#getReturnTransition()()`

Returns the Transition that will be used to move Views out of the scene when the Fragment is preparing to be removed, hidden, or detached because of popping the back stack. The exiting Views will be those that are regular Views or ViewGroups that have `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#isTransitionGroup()` return true. Typical Transitions will extend `https://developer.android.com/reference/kotlin/android/transition/Visibility.html#` as entering is governed by changing visibility from `https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int`. If `transition` is null, entering Views will remain unaffected.

<br />

`https://developer.android.com/reference/kotlin/android/transition/Transition.html#!` `https://developer.android.com/reference/kotlin/android/app/Fragment#getSharedElementEnterTransition()()`

Returns the Transition that will be used for shared elements transferred into the content Scene. Typical Transitions will affect size and location, such as `https://developer.android.com/reference/kotlin/android/transition/ChangeBounds.html#`. A null value will cause transferred shared elements to blink to the final position.

<br />

`https://developer.android.com/reference/kotlin/android/transition/Transition.html#!` `https://developer.android.com/reference/kotlin/android/app/Fragment#getSharedElementReturnTransition()()`

Return the Transition that will be used for shared elements transferred back during a pop of the back stack. This Transition acts in the leaving Fragment. Typical Transitions will affect size and location, such as `https://developer.android.com/reference/kotlin/android/transition/ChangeBounds.html#`. A null value will cause transferred shared elements to blink to the final position. If no value is set, the default will be to use the same value as `https://developer.android.com/reference/kotlin/android/app/Fragment#setSharedElementEnterTransition(android.transition.Transition)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/app/Fragment#getString(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Return a localized string from the application's package's default string table.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/app/Fragment#getString(kotlin.Int,%20kotlin.Any)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, vararg formatArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)`

Return a localized formatted string from the application's package's default string table, substituting the format arguments as defined in `https://developer.android.com/reference/kotlin/java/util/Formatter.html#` and java.lang.String#format.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/app/Fragment#getTag()()`

Get the tag name of the fragment, if specified.

<br />

`https://developer.android.com/reference/kotlin/android/app/Fragment!` `https://developer.android.com/reference/kotlin/android/app/Fragment#getTargetFragment()()`

Return the target fragment set by `https://developer.android.com/reference/kotlin/android/app/Fragment#setTargetFragment(android.app.Fragment,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#getTargetRequestCode()()`

Return the target request code set by `https://developer.android.com/reference/kotlin/android/app/Fragment#setTargetFragment(android.app.Fragment,%20kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` `https://developer.android.com/reference/kotlin/android/app/Fragment#getText(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Return a localized, styled CharSequence from the application's package's default string table.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#getUserVisibleHint()()`

<br />

`https://developer.android.com/reference/kotlin/android/view/View.html#?` `https://developer.android.com/reference/kotlin/android/app/Fragment#getView()()`

Get the root view for the fragment's layout (the one returned by `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle)`), if provided.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#hashCode()()`

Subclasses can not override hashCode().

<br />

`https://developer.android.com/reference/kotlin/android/app/Fragment!` `https://developer.android.com/reference/kotlin/android/app/Fragment#instantiate(android.content.Context,%20kotlin.String)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, fname: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Like `https://developer.android.com/reference/kotlin/android/app/Fragment#instantiate(android.content.Context,%20kotlin.String,%20android.os.Bundle)` but with a null argument Bundle.

<br />

`https://developer.android.com/reference/kotlin/android/app/Fragment!` `https://developer.android.com/reference/kotlin/android/app/Fragment#instantiate(android.content.Context,%20kotlin.String,%20android.os.Bundle)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, fname: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, args: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Create a new instance of a Fragment with the given class name. This is the same as calling its empty constructor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#isAdded()()`

Return true if the fragment is currently added to its activity.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#isDetached()()`

Return true if the fragment has been explicitly detached from the UI. That is, `https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#detach(android.app.Fragment)` has been used on it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#isHidden()()`

Return true if the fragment has been hidden. By default fragments are shown. You can find out about changes to this state with `https://developer.android.com/reference/kotlin/android/app/Fragment#onHiddenChanged(kotlin.Boolean)`. Note that the hidden state is orthogonal to other states -- that is, to be visible to the user, a fragment must be both started and not hidden.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#isInLayout()()`

Return true if the layout is included as part of an activity view hierarchy via the \<fragment\> tag. This will always be true when fragments are created through the \<fragment\> tag, *except* in the case where an old fragment is restored from a previous state and it does not appear in the layout of the current state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#isRemoving()()`

Return true if this fragment is currently being removed from its activity. This is *not* whether its activity is finishing, but rather whether it is in the process of being removed from its activity.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#isResumed()()`

Return true if the fragment is in the resumed state. This is true for the duration of `https://developer.android.com/reference/kotlin/android/app/Fragment#onResume()` and `https://developer.android.com/reference/kotlin/android/app/Fragment#onPause()` as well.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#isStateSaved()()`

Returns true if this fragment is added and its state has already been saved by its host. Any operations that would change saved state should not be performed if this method returns true, and some operations such as `https://developer.android.com/reference/kotlin/android/app/Fragment#setArguments(android.os.Bundle)` will fail.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#isVisible()()`

Return true if the fragment is currently visible to the user. This means it: (1) has been added, (2) has its view attached to the window, and (3) is not hidden.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onActivityResult(kotlin.Int,%20kotlin.Int,%20android.content.Intent)(requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, resultCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, data: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Receive the result from a previous call to `https://developer.android.com/reference/kotlin/android/app/Fragment#startActivityForResult(android.content.Intent,%20kotlin.Int)`. This follows the related Activity API as described there in `https://developer.android.com/reference/kotlin/android/app/Activity#onActivityResult(kotlin.Int,%20kotlin.Int,%20android.content.Intent)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onAttach(android.app.Activity)(activity: https://developer.android.com/reference/kotlin/android/app/Activity!)`

If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onAttachFragment(android.app.Fragment)(childFragment: https://developer.android.com/reference/kotlin/android/app/Fragment!)`

Called when a fragment is attached as a child of this fragment.

This is called after the attached fragment's `onAttach` and before the attached fragment's `onCreate` if the fragment has not yet had a previous call to `onCreate`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onConfigurationChanged(android.content.res.Configuration)(newConfig: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)`

Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources.

At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration.

For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html). If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onContextItemSelected(android.view.MenuItem)(item: https://developer.android.com/reference/kotlin/android/view/MenuItem.html#!)`

This hook is called whenever an item in a context menu is selected. The default implementation simply returns false to have the normal processing happen (calling the item's Runnable or sending a message to its Handler as appropriate). You can use this method for any items for which you would like to do processing without those other facilities.

Use `https://developer.android.com/reference/kotlin/android/view/MenuItem.html#getMenuInfo()` to get extra information set by the View that added this menu item.

Derived classes should call through to the base class for it to perform the default menu handling.

<br />

`https://developer.android.com/reference/kotlin/android/animation/Animator.html#!` `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateAnimator(kotlin.Int,%20kotlin.Boolean,%20kotlin.Int)(transit: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, enter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, nextAnim: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Called when a fragment loads an animation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateContextMenu(android.view.ContextMenu,%20android.view.View,%20android.view.ContextMenu.ContextMenuInfo)(menu: https://developer.android.com/reference/kotlin/android/view/ContextMenu.html#!, v: https://developer.android.com/reference/kotlin/android/view/View.html#!, menuInfo: https://developer.android.com/reference/kotlin/android/view/ContextMenu.ContextMenuInfo.html#!)`

Called when a context menu for the `view` is about to be shown. Unlike `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateOptionsMenu(android.view.Menu,%20android.view.MenuInflater)`, this will be called every time the context menu is about to be shown and should be populated for the view (or item inside the view for `https://developer.android.com/reference/kotlin/android/widget/AdapterView.html#` subclasses, this can be found in the `menuInfo`)).

Use `https://developer.android.com/reference/kotlin/android/app/Fragment#onContextItemSelected(android.view.MenuItem)` to know when an item has been selected.

The default implementation calls up to `https://developer.android.com/reference/kotlin/android/app/Activity#onCreateContextMenu(android.view.ContextMenu,%20android.view.View,%20android.view.ContextMenu.ContextMenuInfo)`, though you can not call this implementation if you don't want that behavior.

It is not safe to hold onto the context menu after this method returns. Called when the context menu for this view is being built. It is not safe to hold onto the menu after this method returns.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateOptionsMenu(android.view.Menu,%20android.view.MenuInflater)(menu: https://developer.android.com/reference/kotlin/android/view/Menu.html#!, inflater: https://developer.android.com/reference/kotlin/android/view/MenuInflater.html#!)`

Initialize the contents of the Activity's standard options menu. You should place your menu items in to menu. For this method to be called, you must have first called `https://developer.android.com/reference/kotlin/android/app/Fragment#setHasOptionsMenu(kotlin.Boolean)`. See `https://developer.android.com/reference/kotlin/android/app/Activity#onCreateOptionsMenu(android.view.Menu)` for more information.

<br />

`https://developer.android.com/reference/kotlin/android/view/View.html#?` `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle)(inflater: https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#!, container: https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#?, savedInstanceState: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)`

Called to have the fragment instantiate its user interface view. This is optional, and non-graphical fragments can return null (which is the default implementation). This will be called between `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreate(android.os.Bundle)` and `https://developer.android.com/reference/kotlin/android/app/Fragment#onActivityCreated(android.os.Bundle)`.

If you return a View from here, you will later be called in `https://developer.android.com/reference/kotlin/android/app/Fragment#onDestroyView()` when the view is being released.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onDestroy()()`

Called when the fragment is no longer in use. This is called after `https://developer.android.com/reference/kotlin/android/app/Fragment#onStop()` and before `https://developer.android.com/reference/kotlin/android/app/Fragment#onDetach()`. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onDestroyOptionsMenu()()`

Called when this fragment's option menu items are no longer being included in the overall options menu. Receiving this call means that the menu needed to be rebuilt, but this fragment's items were not included in the newly built menu (its `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateOptionsMenu(android.view.Menu,%20android.view.MenuInflater)` was not called).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onHiddenChanged(kotlin.Boolean)(hidden: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Called when the hidden state (as returned by `https://developer.android.com/reference/kotlin/android/app/Fragment#isHidden()` of the fragment has changed. Fragments start out not hidden; this will be called whenever the fragment changes state from that.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onInflate(android.app.Activity,%20android.util.AttributeSet,%20android.os.Bundle)(activity: https://developer.android.com/reference/kotlin/android/app/Activity!, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#!, savedInstanceState: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)`

If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onInflate(android.content.Context,%20android.util.AttributeSet,%20android.os.Bundle)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#!, savedInstanceState: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)`

Called when a fragment is being created as part of a view layout inflation, typically from setting the content view of an activity. This may be called immediately after the fragment is created from a tag in a layout file. Note this is *before* the fragment's `https://developer.android.com/reference/kotlin/android/app/Fragment#onAttach(android.app.Activity)` has been called; all you should do here is parse the attributes and save them away.

This is called every time the fragment is inflated, even if it is being inflated into a new instance with saved state. It typically makes sense to re-parse the parameters each time, to allow them to change with different configurations.

Here is a typical implementation of a fragment that can take parameters both through attributes supplied here as well from `https://developer.android.com/reference/kotlin/android/app/Fragment#getArguments()`:

Note that parsing the XML attributes uses a "styleable" resource. The declaration for the styleable used here is:

The fragment can then be declared within its activity's content layout through a tag like this:

This fragment can also be created dynamically from arguments given at runtime in the arguments Bundle; here is an example of doing so at creation of the containing activity:

If you override this method you *must* call through to the superclass implementation.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onInflate(android.util.AttributeSet,%20android.os.Bundle)(attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#!, savedInstanceState: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)`

If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onLowMemory()()`

This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing. If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onMultiWindowModeChanged(kotlin.Boolean)(isInMultiWindowMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Called when the Fragment's activity changes from fullscreen mode to multi-window mode and visa-versa. This is generally tied to android.app.Activity#onMultiWindowModeChanged of the containing Activity.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onMultiWindowModeChanged(kotlin.Boolean,%20android.content.res.Configuration)(isInMultiWindowMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, newConfig: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#!)`

Called when the Fragment's activity changes from fullscreen mode to multi-window mode and visa-versa. This is generally tied to android.app.Activity#onMultiWindowModeChanged of the containing Activity. This method provides the same configuration that will be sent in the following `https://developer.android.com/reference/kotlin/android/app/Fragment#onConfigurationChanged(android.content.res.Configuration)` call after the activity enters this mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onOptionsItemSelected(android.view.MenuItem)(item: https://developer.android.com/reference/kotlin/android/view/MenuItem.html#!)`

This hook is called whenever an item in your options menu is selected. The default implementation simply returns false to have the normal processing happen (calling the item's Runnable or sending a message to its Handler as appropriate). You can use this method for any items for which you would like to do processing without those other facilities.

Derived classes should call through to the base class for it to perform the default menu handling.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onOptionsMenuClosed(android.view.Menu)(menu: https://developer.android.com/reference/kotlin/android/view/Menu.html#!)`

This hook is called whenever the options menu is being closed (either by the user canceling the menu with the back/menu button, or when an item is selected).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onPause()()`

Called when the Fragment is no longer resumed. This is generally tied to `https://developer.android.com/reference/kotlin/android/app/Activity#onPause()` of the containing Activity's lifecycle. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onPictureInPictureModeChanged(kotlin.Boolean)(isInPictureInPictureMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Called by the system when the activity changes to and from picture-in-picture mode. This is generally tied to android.app.Activity#onPictureInPictureModeChanged of the containing Activity.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onPictureInPictureModeChanged(kotlin.Boolean,%20android.content.res.Configuration)(isInPictureInPictureMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, newConfig: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#!)`

Called by the system when the activity changes to and from picture-in-picture mode. This is generally tied to android.app.Activity#onPictureInPictureModeChanged of the containing Activity. This method provides the same configuration that will be sent in the following `https://developer.android.com/reference/kotlin/android/app/Fragment#onConfigurationChanged(android.content.res.Configuration)` call after the activity enters this mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onPrepareOptionsMenu(android.view.Menu)(menu: https://developer.android.com/reference/kotlin/android/view/Menu.html#!)`

Prepare the Screen's standard options menu to be displayed. This is called right before the menu is shown, every time it is shown. You can use this method to efficiently enable/disable items or otherwise dynamically modify the contents. See `https://developer.android.com/reference/kotlin/android/app/Activity#onPrepareOptionsMenu(android.view.Menu)` for more information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onRequestPermissionsResult(kotlin.Int,%20kotlin.Array,%20kotlin.IntArray)(requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, permissions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>, grantResults: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`

Callback for the result from requesting permissions. This method is invoked for every call on `https://developer.android.com/reference/kotlin/android/app/Fragment#requestPermissions(kotlin.Array,%20kotlin.Int)`.

**Note:** It is possible that the permissions request interaction with the user is interrupted. In this case you will receive empty permissions and results arrays which should be treated as a cancellation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onResume()()`

Called when the fragment is visible to the user and actively running. This is generally tied to `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()` of the containing Activity's lifecycle. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onTrimMemory(kotlin.Int)(level: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Called when the operating system has determined that it is a good time for a process to trim unneeded memory from its process. You should never compare to exact values of the level, since new intermediate values may be added -- you will typically want to compare if the value is greater or equal to a level you are interested in.

To retrieve the processes current trim level at any point, you can use `https://developer.android.com/reference/kotlin/android/app/ActivityManager#getMyMemoryState(android.app.ActivityManager.RunningAppProcessInfo)`. If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onViewCreated(android.view.View,%20android.os.Bundle)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!, savedInstanceState: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)`

Called immediately after `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle)` has returned, but before any saved state has been restored in to the view. This gives subclasses a chance to initialize themselves once they know their view hierarchy has been completely created. The fragment's view hierarchy is not however attached to its parent at this point.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#onViewStateRestored(android.os.Bundle)(savedInstanceState: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)`

Called when all saved state has been restored into the view hierarchy of the fragment. This can be used to do initialization based on saved state that you are letting the view hierarchy track itself, such as whether check box widgets are currently checked. This is called after `https://developer.android.com/reference/kotlin/android/app/Fragment#onActivityCreated(android.os.Bundle)` and before `https://developer.android.com/reference/kotlin/android/app/Fragment#onStart()`. 
If you override this method you *must* call through to the superclass implementation.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#postponeEnterTransition()()`

Postpone the entering Fragment transition until `https://developer.android.com/reference/kotlin/android/app/Fragment#startPostponedEnterTransition()` or `https://developer.android.com/reference/kotlin/android/app/FragmentManager#executePendingTransactions()` has been called.

This method gives the Fragment the ability to delay Fragment animations until all data is loaded. Until then, the added, shown, and attached Fragments will be INVISIBLE and removed, hidden, and detached Fragments won't be have their Views removed. The transaction runs when all postponed added Fragments in the transaction have called `https://developer.android.com/reference/kotlin/android/app/Fragment#startPostponedEnterTransition()`.

This method should be called before being added to the FragmentTransaction or in `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreate(android.os.Bundle)`, `https://developer.android.com/reference/kotlin/android/app/Fragment#onAttach(android.content.Context)`, or `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle)`}. `https://developer.android.com/reference/kotlin/android/app/Fragment#startPostponedEnterTransition()` must be called to allow the Fragment to start the transitions.

When a FragmentTransaction is started that may affect a postponed FragmentTransaction, based on which containers are in their operations, the postponed FragmentTransaction will have its start triggered. The early triggering may result in faulty or nonexistent animations in the postponed transaction. FragmentTransactions that operate only on independent containers will not interfere with each other's postponement.

Calling postponeEnterTransition on Fragments with a null View will not postpone the transition. Likewise, postponement only works if FragmentTransaction optimizations are enabled.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#registerForContextMenu(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!)`

Registers a context menu to be shown for the given view (multiple views can show the context menu). This method will set the `https://developer.android.com/reference/kotlin/android/view/View.OnCreateContextMenuListener.html#` on the view to this fragment, so `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateContextMenu(android.view.ContextMenu,%20android.view.View,%20android.view.ContextMenu.ContextMenuInfo)` will be called when it is time to show the context menu.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#requestPermissions(kotlin.Array,%20kotlin.Int)(permissions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Requests permissions to be granted to this application. These permissions must be requested in your manifest, they should not be granted to your app, and they should have protection level `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#`, regardless whether they are declared by the platform or a third-party app.

Normal permissions `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#PROTECTION_NORMAL:kotlin.Int` are granted at install time if requested in the manifest. Signature permissions `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#PROTECTION_SIGNATURE:kotlin.Int` are granted at install time if requested in the manifest and the signature of your app matches the signature of the app declaring the permissions.

Call `https://developer.android.com/reference/kotlin/android/app/Fragment#shouldShowRequestPermissionRationale(kotlin.String)` before calling this API to check if the system recommends to show a rationale UI before asking for a permission.

If your app does not have the requested permissions the user will be presented with UI for accepting them. After the user has accepted or rejected the requested permissions you will receive a callback on `https://developer.android.com/reference/kotlin/android/app/Fragment#onRequestPermissionsResult(kotlin.Int,%20kotlin.Array,%20kotlin.IntArray)` reporting whether the permissions were granted or not.

Note that requesting a permission does not guarantee it will be granted and your app should be able to run without having this permission.

This method may start an activity allowing the user to choose which permissions to grant and which to reject. Hence, you should be prepared that your activity may be paused and resumed. Further, granting some permissions may require a restart of you application. In such a case, the system will recreate the activity stack before delivering the result to `https://developer.android.com/reference/kotlin/android/app/Fragment#onRequestPermissionsResult(kotlin.Int,%20kotlin.Array,%20kotlin.IntArray)`.

When checking whether you have a permission you should use `https://developer.android.com/reference/kotlin/android/content/Context.html#checkSelfPermission(kotlin.String)`.

Calling this API for permissions already granted to your app would show UI to the user to decide whether the app can still hold these permissions. This can be useful if the way your app uses data guarded by the permissions changes significantly.

You cannot request a permission if your activity sets `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestActivity_noHistory:kotlin.Int` to `true` because in this case the activity would not receive result callbacks including `https://developer.android.com/reference/kotlin/android/app/Fragment#onRequestPermissionsResult(kotlin.Int,%20kotlin.Array,%20kotlin.IntArray)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#setAllowEnterTransitionOverlap(kotlin.Boolean)(allow: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Sets whether the exit transition and enter transition overlap or not. When true, the enter transition will start as soon as possible. When false, the enter transition will wait until the exit transition completes before starting.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#setAllowReturnTransitionOverlap(kotlin.Boolean)(allow: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Sets whether the return transition and reenter transition overlap or not. When true, the reenter transition will start as soon as possible. When false, the reenter transition will wait until the return transition completes before starting.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#setArguments(android.os.Bundle)(args: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)`

Supply the construction arguments for this fragment. The arguments supplied here will be retained across fragment destroy and creation.

This method cannot be called if the fragment is added to a FragmentManager and if `https://developer.android.com/reference/kotlin/android/app/Fragment#isStateSaved()` would return true. Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int`, this method may only be called if the fragment has not yet been added to a FragmentManager.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#setEnterSharedElementCallback(android.app.SharedElementCallback)(callback: https://developer.android.com/reference/kotlin/android/app/SharedElementCallback!)`

When custom transitions are used with Fragments, the enter transition callback is called when this Fragment is attached or detached when not popping the back stack.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#setEnterTransition(android.transition.Transition)(transition: https://developer.android.com/reference/kotlin/android/transition/Transition.html#!)`

Sets the Transition that will be used to move Views into the initial scene. The entering Views will be those that are regular Views or ViewGroups that have `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#isTransitionGroup()` return true. Typical Transitions will extend `https://developer.android.com/reference/kotlin/android/transition/Visibility.html#` as entering is governed by changing visibility from `https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int`. If `transition` is null, entering Views will remain unaffected.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#setExitSharedElementCallback(android.app.SharedElementCallback)(callback: https://developer.android.com/reference/kotlin/android/app/SharedElementCallback!)`

When custom transitions are used with Fragments, the exit transition callback is called when this Fragment is attached or detached when popping the back stack.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#setExitTransition(android.transition.Transition)(transition: https://developer.android.com/reference/kotlin/android/transition/Transition.html#!)`

Sets the Transition that will be used to move Views out of the scene when the fragment is removed, hidden, or detached when not popping the back stack. The exiting Views will be those that are regular Views or ViewGroups that have `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#isTransitionGroup()` return true. Typical Transitions will extend `https://developer.android.com/reference/kotlin/android/transition/Visibility.html#` as exiting is governed by changing visibility from `https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int`. If transition is null, the views will remain unaffected.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#setHasOptionsMenu(kotlin.Boolean)(hasMenu: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Report that this fragment would like to participate in populating the options menu by receiving a call to `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateOptionsMenu(android.view.Menu,%20android.view.MenuInflater)` and related methods.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#setInitialSavedState(android.app.Fragment.SavedState)(state: https://developer.android.com/reference/kotlin/android/app/Fragment.SavedState!)`

Set the initial saved state that this Fragment should restore itself from when first being constructed, as returned by `https://developer.android.com/reference/kotlin/android/app/FragmentManager#saveFragmentInstanceState(android.app.Fragment)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#setMenuVisibility(kotlin.Boolean)(menuVisible: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Set a hint for whether this fragment's menu should be visible. This is useful if you know that a fragment has been placed in your view hierarchy so that the user can not currently seen it, so any menu items it has should also not be shown.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#setReenterTransition(android.transition.Transition)(transition: https://developer.android.com/reference/kotlin/android/transition/Transition.html#!)`

Sets the Transition that will be used to move Views in to the scene when returning due to popping a back stack. The entering Views will be those that are regular Views or ViewGroups that have `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#isTransitionGroup()` return true. Typical Transitions will extend `https://developer.android.com/reference/kotlin/android/transition/Visibility.html#` as exiting is governed by changing visibility from `https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int`. If transition is null, the views will remain unaffected. If nothing is set, the default will be to use the same transition as `https://developer.android.com/reference/kotlin/android/app/Fragment#setExitTransition(android.transition.Transition)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#setRetainInstance(kotlin.Boolean)(retain: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Control whether a fragment instance is retained across Activity re-creation (such as from a configuration change). This can only be used with fragments not in the back stack. If set, the fragment lifecycle will be slightly different when an activity is recreated:

- `https://developer.android.com/reference/kotlin/android/app/Fragment#onDestroy()` will not be called (but `https://developer.android.com/reference/kotlin/android/app/Fragment#onDetach()` still will be, because the fragment is being detached from its current activity).
- `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreate(android.os.Bundle)` will not be called since the fragment is not being re-created.
- `https://developer.android.com/reference/kotlin/android/app/Fragment#onAttach(android.app.Activity)` and `https://developer.android.com/reference/kotlin/android/app/Fragment#onActivityCreated(android.os.Bundle)` **will** still be called.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#setReturnTransition(android.transition.Transition)(transition: https://developer.android.com/reference/kotlin/android/transition/Transition.html#!)`

Sets the Transition that will be used to move Views out of the scene when the Fragment is preparing to be removed, hidden, or detached because of popping the back stack. The exiting Views will be those that are regular Views or ViewGroups that have `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#isTransitionGroup()` return true. Typical Transitions will extend `https://developer.android.com/reference/kotlin/android/transition/Visibility.html#` as entering is governed by changing visibility from `https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int`. If `transition` is null, entering Views will remain unaffected. If nothing is set, the default will be to use the same value as set in `https://developer.android.com/reference/kotlin/android/app/Fragment#setEnterTransition(android.transition.Transition)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#setSharedElementEnterTransition(android.transition.Transition)(transition: https://developer.android.com/reference/kotlin/android/transition/Transition.html#!)`

Sets the Transition that will be used for shared elements transferred into the content Scene. Typical Transitions will affect size and location, such as `https://developer.android.com/reference/kotlin/android/transition/ChangeBounds.html#`. A null value will cause transferred shared elements to blink to the final position.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#setSharedElementReturnTransition(android.transition.Transition)(transition: https://developer.android.com/reference/kotlin/android/transition/Transition.html#!)`

Sets the Transition that will be used for shared elements transferred back during a pop of the back stack. This Transition acts in the leaving Fragment. Typical Transitions will affect size and location, such as `https://developer.android.com/reference/kotlin/android/transition/ChangeBounds.html#`. A null value will cause transferred shared elements to blink to the final position. If no value is set, the default will be to use the same value as `https://developer.android.com/reference/kotlin/android/app/Fragment#setSharedElementEnterTransition(android.transition.Transition)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#setTargetFragment(android.app.Fragment,%20kotlin.Int)(fragment: https://developer.android.com/reference/kotlin/android/app/Fragment!, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Optional target for this fragment. This may be used, for example, if this fragment is being started by another, and when done wants to give a result back to the first. The target set here is retained across instances via `https://developer.android.com/reference/kotlin/android/app/FragmentManager#putFragment(android.os.Bundle,%20kotlin.String,%20android.app.Fragment)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#setUserVisibleHint(kotlin.Boolean)(isVisibleToUser: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Set a hint to the system about whether this fragment's UI is currently visible to the user. This hint defaults to true and is persistent across fragment instance state save and restore.

An app may set this to false to indicate that the fragment's UI is scrolled out of visibility or is otherwise not directly visible to the user. This may be used by the system to prioritize operations such as fragment lifecycle updates or loader ordering behavior.

**Note:** This method may be called outside of the fragment lifecycle and thus has no ordering guarantees with regard to fragment lifecycle method calls.

**Note:** Prior to Android N there was a platform bug that could cause `setUserVisibleHint` to bring a fragment up to the started state before its `FragmentTransaction` had been committed. As some apps relied on this behavior, it is preserved for apps that declare a `targetSdkVersion` of 23 or lower.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#shouldShowRequestPermissionRationale(kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Gets whether you should show UI with rationale before requesting a permission.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#startActivity(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Call android.app.Activity#startActivity(android.content.Intent) from the fragment's containing Activity.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#startActivity(android.content.Intent,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)`

Call android.app.Activity#startActivity(android.content.Intent,android.os.Bundle) from the fragment's containing Activity.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#startActivityForResult(android.content.Intent,%20kotlin.Int)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Call `https://developer.android.com/reference/kotlin/android/app/Activity#startActivityForResult(android.content.Intent,%20kotlin.Int)` from the fragment's containing Activity.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#startActivityForResult(android.content.Intent,%20kotlin.Int,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)`

Call `https://developer.android.com/reference/kotlin/android/app/Activity#startActivityForResult(android.content.Intent,%20kotlin.Int,%20android.os.Bundle)` from the fragment's containing Activity.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#startIntentSenderForResult(android.content.IntentSender,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/IntentSender.html#!, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, fillInIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#?, flagsMask: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flagsValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, extraFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)`

Call `https://developer.android.com/reference/kotlin/android/app/Activity#startIntentSenderForResult(android.content.IntentSender,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)` from the fragment's containing Activity.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#startPostponedEnterTransition()()`

Begin postponed transitions after `https://developer.android.com/reference/kotlin/android/app/Fragment#postponeEnterTransition()` was called. If postponeEnterTransition() was called, you must call startPostponedEnterTransition() or `https://developer.android.com/reference/kotlin/android/app/FragmentManager#executePendingTransactions()` to complete the FragmentTransaction. If postponement was interrupted with `https://developer.android.com/reference/kotlin/android/app/FragmentManager#executePendingTransactions()`, before `startPostponedEnterTransition()`, animations may not run or may execute improperly.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#toString()()`

Returns a string representation of the object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/app/Fragment#unregisterForContextMenu(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!)`

Prevents a context menu to be shown for the given view. This method will remove the `https://developer.android.com/reference/kotlin/android/view/View.OnCreateContextMenuListener.html#` on the view.

<br />

From class `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onConfigurationChanged(android.content.res.Configuration)(newConfig: https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)`

Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources.

At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration.

For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onLowMemory()()`

This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing.

<br />

## Constants

### STYLE_NORMAL

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STYLE_NORMAL: Int
```

**Deprecated:** *Deprecated in Java.*

Style for `https://developer.android.com/reference/kotlin/android/app/DialogFragment#setStyle(kotlin.Int,%20kotlin.Int)`: a basic, normal dialog.

 Value: 0

### STYLE_NO_FRAME

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STYLE_NO_FRAME: Int
```

**Deprecated:** *Deprecated in Java.*

Style for `https://developer.android.com/reference/kotlin/android/app/DialogFragment#setStyle(kotlin.Int,%20kotlin.Int)`: don't draw any frame at all; the view hierarchy returned by `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle)` is entirely responsible for drawing the dialog.

 Value: 2

### STYLE_NO_INPUT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STYLE_NO_INPUT: Int
```

**Deprecated:** *Deprecated in Java.*

Style for `https://developer.android.com/reference/kotlin/android/app/DialogFragment#setStyle(kotlin.Int,%20kotlin.Int)`: like `https://developer.android.com/reference/kotlin/android/app/DialogFragment#STYLE_NO_FRAME:kotlin.Int`, but also disables all input to the dialog. The user can not touch it, and its window will not receive input focus.

 Value: 3

### STYLE_NO_TITLE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STYLE_NO_TITLE: Int
```

**Deprecated:** *Deprecated in Java.*

Style for `https://developer.android.com/reference/kotlin/android/app/DialogFragment#setStyle(kotlin.Int,%20kotlin.Int)`: don't include a title area.

 Value: 1

## Public constructors

### DialogFragment

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DialogFragment()
```

## Public methods

### dismiss

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dismiss(): Unit
```

**Deprecated:** *Deprecated in Java.*

Dismiss the fragment and its dialog. If the fragment was added to the back stack, all back stack state up to and including this entry will be popped. Otherwise, a new transaction will be committed to remove the fragment.

### dismissAllowingStateLoss

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dismissAllowingStateLoss(): Unit
```

**Deprecated:** *Deprecated in Java.*

Version of `https://developer.android.com/reference/kotlin/android/app/DialogFragment#dismiss()` that uses `https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#commitAllowingStateLoss()`. See linked documentation for further details.

### dump

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dump(
    prefix: String!, 
    fd: FileDescriptor!, 
    writer: PrintWriter!, 
    args: Array<String!>!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Print the Fragments's state into the given stream.

| Parameters ||
|---|---|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Text to print at the front of each line. |
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!: The raw file descriptor that the dump is being sent to. |
| `writer` | [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)!: The PrintWriter to which you should dump your state. This will be closed for you after you return. |
| `args` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: additional arguments to the dump request. |

### getDialog

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDialog(): Dialog!
```

**Deprecated:** *Deprecated in Java.*

### getShowsDialog

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getShowsDialog(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Return the current value of `https://developer.android.com/reference/kotlin/android/app/DialogFragment#setShowsDialog(kotlin.Boolean)`.

### getTheme

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTheme(): Int
```

**Deprecated:** *Deprecated in Java.*

### isCancelable

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isCancelable(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Return the current value of `https://developer.android.com/reference/kotlin/android/app/DialogFragment#setCancelable(kotlin.Boolean)`.

### onActivityCreated

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onActivityCreated(savedInstanceState: Bundle?): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the fragment's activity has been created and this fragment's view hierarchy instantiated. It can be used to do final initialization once these pieces are in place, such as retrieving views or restoring state. It is also useful for fragments that use `https://developer.android.com/reference/kotlin/android/app/Fragment#setRetainInstance(kotlin.Boolean)` to retain their instance, as this callback tells the fragment when it is fully associated with the new activity instance. This is called after `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle)` and before `https://developer.android.com/reference/kotlin/android/app/Fragment#onViewStateRestored(android.os.Bundle)`. 
If you override this method you *must* call through to the superclass implementation.

| Parameters ||
|---|---|
| `savedInstanceState` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?: If the fragment is being re-created from a previous saved state, this is the state. This value may be `null`. |

### onAttach

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onAttach(context: Context!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when a fragment is first attached to its context. `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreate(android.os.Bundle)` will be called after this. 
If you override this method you *must* call through to the superclass implementation.

### onCancel

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCancel(dialog: DialogInterface!): Unit
```

**Deprecated:** *Deprecated in Java.*

This method will be invoked when the dialog is canceled.

| Parameters ||
|---|---|
| `dialog` | [DialogInterface](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#)!: the dialog that was canceled will be passed into the method |

### onCreate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreate(savedInstanceState: Bundle?): Unit
```

**Deprecated:** *Deprecated in Java.*

Called to do initial creation of a fragment. This is called after `https://developer.android.com/reference/kotlin/android/app/Fragment#onAttach(android.app.Activity)` and before `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle)`, but is not called if the fragment instance is retained across Activity re-creation (see `https://developer.android.com/reference/kotlin/android/app/Fragment#setRetainInstance(kotlin.Boolean)`).

Note that this can be called while the fragment's activity is still in the process of being created. As such, you can not rely on things like the activity's content view hierarchy being initialized at this point. If you want to do work once the activity itself is created, see `https://developer.android.com/reference/kotlin/android/app/Fragment#onActivityCreated(android.os.Bundle)`.

If your app's `targetSdkVersion` is `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int` or lower, child fragments being restored from the savedInstanceState are restored after `onCreate` returns. When targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int` or above and running on an N or newer platform version they are restored by `Fragment.onCreate`.
. 
If you override this method you *must* call through to the superclass implementation.

| Parameters ||
|---|---|
| `savedInstanceState` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?: If the fragment is being re-created from a previous saved state, this is the state. This value may be `null`. |

### onCreateDialog

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateDialog(savedInstanceState: Bundle!): Dialog!
```

**Deprecated:** *Deprecated in Java.*

Override to build your own custom Dialog container. This is typically used to show an AlertDialog instead of a generic Dialog; when doing so, `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle)` does not need to be implemented since the AlertDialog takes care of its own content.

This method will be called after `https://developer.android.com/reference/kotlin/android/app/DialogFragment#onCreate(android.os.Bundle)` and before `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle)`. The default implementation simply instantiates and returns a `https://developer.android.com/reference/kotlin/android/app/Dialog` class.

*Note: DialogFragment own the `https://developer.android.com/reference/kotlin/android/app/Dialog#setOnCancelListener(android.content.DialogInterface.OnCancelListener)` and `https://developer.android.com/reference/kotlin/android/app/Dialog#setOnDismissListener(android.content.DialogInterface.OnDismissListener)` callbacks. You must not set them yourself.* To find out about these events, override `https://developer.android.com/reference/kotlin/android/app/DialogFragment#onCancel(android.content.DialogInterface)` and `https://developer.android.com/reference/kotlin/android/app/DialogFragment#onDismiss(android.content.DialogInterface)`.

| Parameters ||
|---|---|
| `savedInstanceState` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: The last saved instance state of the Fragment, or null if this is a freshly created Fragment. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/Dialog!` | Return a new Dialog instance to be displayed by the Fragment. |

### onDestroyView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDestroyView(): Unit
```

**Deprecated:** *Deprecated in Java.*

Remove dialog.

### onDetach

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDetach(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the fragment is no longer attached to its activity. This is called after `https://developer.android.com/reference/kotlin/android/app/Fragment#onDestroy()`, except in the cases where the fragment instance is retained across Activity re-creation (see `https://developer.android.com/reference/kotlin/android/app/Fragment#setRetainInstance(kotlin.Boolean)`), in which case it is called after `https://developer.android.com/reference/kotlin/android/app/Fragment#onStop()`. 
If you override this method you *must* call through to the superclass implementation.

### onDismiss

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDismiss(dialog: DialogInterface!): Unit
```

**Deprecated:** *Deprecated in Java.*

This method will be invoked when the dialog is dismissed.

| Parameters ||
|---|---|
| `dialog` | [DialogInterface](https://developer.android.com/reference/kotlin/android/content/DialogInterface.html#)!: the dialog that was dismissed will be passed into the method |

### onGetLayoutInflater

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onGetLayoutInflater(savedInstanceState: Bundle!): LayoutInflater!
```

**Deprecated:** *Deprecated in Java.*

Returns the LayoutInflater used to inflate Views of this Fragment. The default implementation will throw an exception if the Fragment is not attached.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#!` | The LayoutInflater used to inflate Views of this Fragment. |

### onSaveInstanceState

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onSaveInstanceState(outState: Bundle!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called to ask the fragment to save its current dynamic state, so it can later be reconstructed in a new instance of its process is restarted. If a new instance of the fragment later needs to be created, the data you place in the Bundle here will be available in the Bundle given to `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreate(android.os.Bundle)`, `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle)`, and `https://developer.android.com/reference/kotlin/android/app/Fragment#onActivityCreated(android.os.Bundle)`.

This corresponds to `https://developer.android.com/reference/kotlin/android/app/Activity#onSaveInstanceState(android.os.Bundle)` and most of the discussion there applies here as well. Note however: *this method may be called at any time before `https://developer.android.com/reference/kotlin/android/app/Fragment#onDestroy()`*. There are many situations where a fragment may be mostly torn down (such as when placed on the back stack with no UI showing), but its state will not be saved until its owning activity actually needs to save its state.

| Parameters ||
|---|---|
| `outState` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: Bundle in which to place your saved state. |

### onStart

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onStart(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the Fragment is visible to the user. This is generally tied to `https://developer.android.com/reference/kotlin/android/app/Activity#onStart()` of the containing Activity's lifecycle. 
If you override this method you *must* call through to the superclass implementation.

### onStop

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onStop(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the Fragment is no longer started. This is generally tied to `https://developer.android.com/reference/kotlin/android/app/Activity#onStop()` of the containing Activity's lifecycle. 
If you override this method you *must* call through to the superclass implementation.

### setCancelable

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCancelable(cancelable: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Control whether the shown Dialog is cancelable. Use this instead of directly calling `https://developer.android.com/reference/kotlin/android/app/Dialog#setCancelable(kotlin.Boolean)`, because DialogFragment needs to change its behavior based on this.

| Parameters ||
|---|---|
| `cancelable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, the dialog is cancelable. The default is true. |

### setShowsDialog

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setShowsDialog(showsDialog: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Controls whether this fragment should be shown in a dialog. If not set, no Dialog will be created in `https://developer.android.com/reference/kotlin/android/app/DialogFragment#onActivityCreated(android.os.Bundle)`, and the fragment's view hierarchy will thus not be added to it. This allows you to instead use it as a normal fragment (embedded inside of its activity).

This is normally set for you based on whether the fragment is associated with a container view ID passed to `https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#add(kotlin.Int,%20android.app.Fragment)`. If the fragment was added with a container, setShowsDialog will be initialized to false; otherwise, it will be true.

| Parameters ||
|---|---|
| `showsDialog` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, the fragment will be displayed in a Dialog. If false, no Dialog will be created and the fragment's view hierarchly left undisturbed. |

### setStyle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStyle(
    style: Int, 
    theme: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Call to customize the basic appearance and behavior of the fragment's dialog. This can be used for some common dialog behaviors, taking care of selecting flags, theme, and other options for you. The same effect can be achieve by manually setting Dialog and Window attributes yourself. Calling this after the fragment's Dialog is created will have no effect.

| Parameters ||
|---|---|
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Selects a standard style: may be `https://developer.android.com/reference/kotlin/android/app/DialogFragment#STYLE_NORMAL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/DialogFragment#STYLE_NO_TITLE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/DialogFragment#STYLE_NO_FRAME:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/app/DialogFragment#STYLE_NO_INPUT:kotlin.Int`. |
| `theme` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Optional custom theme. If 0, an appropriate theme (based on the style) will be selected for you. |

### show

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun show(
    manager: FragmentManager!, 
    tag: String!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Display the dialog, adding the fragment to the given FragmentManager. This is a convenience for explicitly creating a transaction, adding the fragment to it with the given tag, and committing it. This does *not* add the transaction to the back stack. When the fragment is dismissed, a new transaction will be executed to remove it from the activity.

| Parameters ||
|---|---|
| `manager` | [FragmentManager](https://developer.android.com/reference/kotlin/android/app/FragmentManager)!: The FragmentManager this fragment will be added to. |
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The tag for this fragment, as per `https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#add(android.app.Fragment,%20kotlin.String)`. |

### show

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun show(
    transaction: FragmentTransaction!, 
    tag: String!
): Int
```

**Deprecated:** *Deprecated in Java.*

Display the dialog, adding the fragment using an existing transaction and then committing the transaction.

| Parameters ||
|---|---|
| `transaction` | [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction)!: An existing transaction in which to add the fragment. |
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The tag for this fragment, as per `https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#add(android.app.Fragment,%20kotlin.String)`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns the identifier of the committed transaction, as per `https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#commit()`. |
