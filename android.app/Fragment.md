# Fragment

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Fragment

Kotlin| [Java](../android/app/Fragment.md) 
| --- | --- |

```
open class Fragment : ComponentCallbacks2, View.OnCreateContextMenuListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.Fragment](../android/app/Fragment.md) |

| Known Direct Subclasses [DialogFragment](../android/app/DialogFragment.md), [ListFragment](../android/app/ListFragment.md), [PreferenceFragment](../android/preference/PreferenceFragment.md), [WebViewFragment](../android/webkit/WebViewFragment.md) |------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DialogFragment](../android/app/DialogFragment.md) | A fragment that displays a dialog window, floating on top of its activity's window. | | [ListFragment](../android/app/ListFragment.md) | A fragment that displays a list of items by binding to a data source such as an array or Cursor, and exposes event handlers when the user selects an item. | | [PreferenceFragment](../android/preference/PreferenceFragment.md) | Shows a hierarchy of [Preference](../android/preference/Preference.md) objects as lists. | | [WebViewFragment](../android/webkit/WebViewFragment.md) | A fragment that displays a WebView. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| **This class was deprecated in API level 28.**
|
| Use the [Jetpack Fragment Library](https://developer.android.com/jetpack) androidx.fragment.app.Fragment for consistent behavior across all devices and access to [Lifecycle](https://developer.android.com/topic/libraries/architecture/lifecycle.html).

A Fragment is a piece of an application's user interface or behavior that can be placed in an [Activity](../android/app/Activity.md). Interaction with fragments is done through [FragmentManager](../android/app/FragmentManager.md), which can be obtained via [Activity.getFragmentManager()](../android/app/Activity.md))and [Fragment.getFragmentManager()](../android/app/Fragment.md)).

The Fragment class can be used many ways to achieve a wide variety of results. In its core, it represents a particular operation or interface that is running within a larger [Activity](../android/app/Activity.md). A Fragment is closely tied to the Activity it is in, and can not be used apart from one. Though Fragment defines its own lifecycle, that lifecycle is dependent on its activity: if the activity is stopped, no fragments inside of it can be started; when the activity is destroyed, all fragments will be destroyed.

All subclasses of Fragment must include a public no-argument constructor. The framework will often re-instantiate a fragment class when needed, in particular during state restore, and needs to be able to find this constructor to instantiate it. If the no-argument constructor is not available, a runtime exception will occur in some cases during state restore.

Topics covered here:

1. [Older Platforms](../android/app/Fragment.md)
2. [Lifecycle](../android/app/Fragment.md)
3. [Layout](../android/app/Fragment.md)
4. [Back Stack](../android/app/Fragment.md)

| ### Developer Guides
|
| For more information about using fragments, read the [Fragments](https://developer.android.com/guide/components/fragments.html) developer guide.

### Older Platforms

While the Fragment API was introduced in [android.os.Build.VERSION_CODES#HONEYCOMB](../android/os/Build.VERSION_CODES.md), a version of the API at is also available for use on older platforms through androidx.fragment.app.FragmentActivity. See the blog post [Fragments For All](http://android-developers.blogspot.com/2011/03/fragments-for-all.html) for more details.

### Lifecycle

Though a Fragment's lifecycle is tied to its owning activity, it has its own wrinkle on the standard activity lifecycle. It includes basic activity lifecycle methods such as [onResume](../android/app/Fragment.md)), but also important are methods related to interactions with the activity and UI generation.

The core series of lifecycle methods that are called to bring a fragment up to resumed state (interacting with the user) are:

1. #onAttach called once the fragment is associated with its activity.
2. [onCreate](../android/app/Fragment.md))called to do initial creation of the fragment.
3. [onCreateView](../android/app/Fragment.md))creates and returns the view hierarchy associated with the fragment.
4. [onActivityCreated](../android/app/Fragment.md))tells the fragment that its activity has completed its own android.app.Activity#onCreate.
5. [onViewStateRestored](../android/app/Fragment.md))tells the fragment that all of the saved state of its view hierarchy has been restored.
6. [onStart](../android/app/Fragment.md))makes the fragment visible to the user (based on its containing activity being started).
7. [onResume](../android/app/Fragment.md))makes the fragment begin interacting with the user (based on its containing activity being resumed).

As a fragment is no longer being used, it goes through a reverse series of callbacks:

1. [onPause](../android/app/Fragment.md))fragment is no longer interacting with the user either because its activity is being paused or a fragment operation is modifying it in the activity.
2. [onStop](../android/app/Fragment.md))fragment is no longer visible to the user either because its activity is being stopped or a fragment operation is modifying it in the activity.
3. [onDestroyView](../android/app/Fragment.md))allows the fragment to clean up resources associated with its View.
4. [onDestroy](../android/app/Fragment.md))called to do final cleanup of the fragment's state.
5. [onDetach](../android/app/Fragment.md))called immediately prior to the fragment no longer being associated with its activity.

### Layout

Fragments can be used as part of your application's layout, allowing you to better modularize your code and more easily adjust your user interface to the screen it is running on. As an example, we can look at a simple program consisting of a list of items, and display of the details of each item.

An activity's layout XML can include`<fragment>`tags to embed fragment instances inside of the layout. For example, here is a simple layout that embeds one fragment:

The layout is installed in the activity in the normal way:

The titles fragment, showing a list of titles, is fairly simple, relying on [ListFragment](../android/app/ListFragment.md) for most of its work. Note the implementation of clicking an item: depending on the current activity's layout, it can either create and display a new fragment to show the details in-place (more about this later), or start a new activity to show the details.

The details fragment showing the contents of a selected item just displays a string of text based on an index of a string array built in to the app:

In this case when the user clicks on a title, there is no details container in the current activity, so the titles fragment's click code will launch a new activity to display the details fragment:

However the screen may be large enough to show both the list of titles and details about the currently selected title. To use such a layout on a landscape screen, this alternative layout can be placed under layout-land:

Note how the prior code will adjust to this alternative UI flow: the titles fragment will now embed the details fragment inside of this activity, and the details activity will finish itself if it is running in a configuration where the details can be shown in-place.

When a configuration change causes the activity hosting these fragments to restart, its new instance may use a different layout that doesn't include the same fragments as the previous layout. In this case all of the previous fragments will still be instantiated and running in the new instance. However, any that are no longer associated with a \<fragment\> tag in the view hierarchy will not have their content view created and will return false from [isInLayout](../android/app/Fragment.md)). (The code here also shows how you can determine if a fragment placed in a container is no longer running in a layout with that container and avoid creating its view hierarchy in that case.)

The attributes of the \<fragment\> tag are used to control the LayoutParams provided when attaching the fragment's view to the parent container. They can also be parsed by the fragment in #onInflate as parameters.

The fragment being instantiated must have some kind of unique identifier so that it can be re-associated with a previous instance if the parent activity needs to be destroyed and recreated. This can be provided these ways:

- If nothing is explicitly supplied, the view ID of the container will be used.
- `android:tag`can be used in \<fragment\> to provide a specific tag name for the fragment.
- `android:id`can be used in \<fragment\> to provide a specific identifier for the fragment.

### Back Stack

The transaction in which fragments are modified can be placed on an internal back-stack of the owning activity. When the user presses back in the activity, any transactions on the back stack are popped off before the activity itself is finished.

For example, consider this simple fragment that is instantiated with an integer argument and displays that in a TextView in its UI:

A function that creates a new instance of the fragment, replacing whatever current fragment instance is being shown and pushing that change on to the back stack could be written as:

After each call to this function, a new entry is on the stack, and pressing back will pop it to return the user to whatever previous state the activity UI was in.

Fragments appearing or disappearing do not generate system events for accessibility, so set a title on your fragments with [View.setAccessibilityPaneTitle(CharSequence)](../android/view/View.md))to notify accessibility users of these UI transitions.

## Summary

| Nested classes ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [InstantiationException](../android/app/Fragment.InstantiationException.md) Thrown by [Fragment.instantiate(Context, String, Bundle)](../android/app/Fragment.md))when there is an instantiation failure. |
| open | [SavedState](../android/app/Fragment.SavedState.md) State information that has been retrieved from a fragment instance through [FragmentManager.saveFragmentInstanceState](../android/app/FragmentManager.md)). |

| Inherited constants ||
|---|---|
| From class [ComponentCallbacks2](../android/content/ComponentCallbacks2.md) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_BACKGROUND](../android/content/ComponentCallbacks2.md) <br /> Level for [onTrimMemory(int)](../android/content/ComponentCallbacks2.md)): the process has gone on to the LRU list. This is a good opportunity to clean up resources that can efficiently and quickly be re-built if the user returns to the app. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_COMPLETE](../android/content/ComponentCallbacks2.md) <br /> Level for [onTrimMemory(int)](../android/content/ComponentCallbacks2.md)): the process is nearing the end of the background LRU list, and if more memory isn't found soon it will be killed. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_MODERATE](../android/content/ComponentCallbacks2.md) <br /> Level for [onTrimMemory(int)](../android/content/ComponentCallbacks2.md)): the process is around the middle of the background LRU list; freeing memory can help the system keep other processes running later in the list for better overall performance. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_RUNNING_CRITICAL](../android/content/ComponentCallbacks2.md) <br /> Level for [onTrimMemory(int)](../android/content/ComponentCallbacks2.md)): the process is not an expendable background process, but the device is running extremely low on memory and is about to not be able to keep any background processes running. Your running process should free up as many non-critical resources as it can to allow that memory to be used elsewhere. The next thing that will happen after this is [onLowMemory()](../android/content/ComponentCallbacks.md))called to report that nothing at all can be kept in the background, a situation that can start to notably impact the user. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_RUNNING_LOW](../android/content/ComponentCallbacks2.md) <br /> Level for [onTrimMemory(int)](../android/content/ComponentCallbacks2.md)): the process is not an expendable background process, but the device is running low on memory. Your running process should free up unneeded resources to allow that memory to be used elsewhere. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_RUNNING_MODERATE](../android/content/ComponentCallbacks2.md) <br /> Level for [onTrimMemory(int)](../android/content/ComponentCallbacks2.md)): the process is not an expendable background process, but the device is running moderately low on memory. Your running process may want to release some unneeded resources for use elsewhere. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_UI_HIDDEN](../android/content/ComponentCallbacks2.md) <br /> Level for [onTrimMemory(int)](../android/content/ComponentCallbacks2.md)): the process had been showing a user interface, and is no longer doing so. Large allocations with the UI should be released at this point to allow memory to be better managed. <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------|---|
| [Fragment](../android/app/Fragment.md))`()` Default constructor. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](../android/app/Fragment.md))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `fd:` ` [FileDescriptor](../java/io/FileDescriptor.md)!`, `writer:` ` [PrintWriter](../java/io/PrintWriter.md)!`, `args:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Print the Fragments's state into the given stream. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/app/Fragment.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Subclasses can not override equals(). |
| [Activity](../android/app/Activity.md)! | [getActivity](../android/app/Fragment.md))`()` Return the Activity this fragment is currently associated with. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAllowEnterTransitionOverlap](../android/app/Fragment.md))`()` Returns whether the exit transition and enter transition overlap or not. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAllowReturnTransitionOverlap](../android/app/Fragment.md))`()` Returns whether the return transition and reenter transition overlap or not. |
| [Bundle](../android/os/Bundle.md)! | [getArguments](../android/app/Fragment.md))`()` Return the arguments supplied to [setArguments](../android/app/Fragment.md)), if any. |
| --- | --- |
| [FragmentManager](../android/app/FragmentManager.md)! | [getChildFragmentManager](../android/app/Fragment.md))`()` Return a private FragmentManager for placing and managing Fragments inside of this Fragment. |
| open [Context](../android/content/Context.md)! | [getContext](../android/app/Fragment.md))`()` Return the [Context](../android/content/Context.md) this fragment is currently associated with. |
| open [Transition](../android/transition/Transition.md)! | [getEnterTransition](../android/app/Fragment.md))`()` Returns the Transition that will be used to move Views into the initial scene. |
| --- | --- |
| open [Transition](../android/transition/Transition.md)! | [getExitTransition](../android/app/Fragment.md))`()` Returns the Transition that will be used to move Views out of the scene when the fragment is removed, hidden, or detached when not popping the back stack. |
| [FragmentManager](../android/app/FragmentManager.md)! | [getFragmentManager](../android/app/Fragment.md))`()` Return the FragmentManager for interacting with fragments associated with this fragment's activity. |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | [getHost](../android/app/Fragment.md))`()` Return the host object of this fragment. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](../android/app/Fragment.md))`()` Return the identifier this fragment is known by. |
| [LayoutInflater](../android/view/LayoutInflater.md)! | [getLayoutInflater](../android/app/Fragment.md))`()` Returns the cached LayoutInflater used to inflate Views of this Fragment. |
| open [LoaderManager](../android/app/LoaderManager.md)! | [getLoaderManager](../android/app/Fragment.md))`()` Return the LoaderManager for this fragment, creating it if needed. |
| --- | --- |
| [Fragment](../android/app/Fragment.md)! | [getParentFragment](../android/app/Fragment.md))`()` Returns the parent Fragment containing this Fragment. |
| open [Transition](../android/transition/Transition.md)! | [getReenterTransition](../android/app/Fragment.md))`()` Returns the Transition that will be used to move Views in to the scene when returning due to popping a back stack. |
| [Resources](../android/content/res/Resources.md)! | [getResources](../android/app/Fragment.md))`()` Return`getActivity().getResources()`. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getRetainInstance](../android/app/Fragment.md))`()` <br /> |
| open [Transition](../android/transition/Transition.md)! | [getReturnTransition](../android/app/Fragment.md))`()` Returns the Transition that will be used to move Views out of the scene when the Fragment is preparing to be removed, hidden, or detached because of popping the back stack. |
| open [Transition](../android/transition/Transition.md)! | [getSharedElementEnterTransition](../android/app/Fragment.md))`()` Returns the Transition that will be used for shared elements transferred into the content Scene. |
| --- | --- |
| open [Transition](../android/transition/Transition.md)! | [getSharedElementReturnTransition](../android/app/Fragment.md))`()` Return the Transition that will be used for shared elements transferred back during a pop of the back stack. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](../android/app/Fragment.md))`(`resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return a localized string from the application's package's default string table. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](../android/app/Fragment.md))`(`resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `vararg` `formatArgs:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Return a localized formatted string from the application's package's default string table, substituting the format arguments as defined in [java.util.Formatter](../java/util/Formatter.md) and java. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTag](../android/app/Fragment.md))`()` Get the tag name of the fragment, if specified. |
| [Fragment](../android/app/Fragment.md)! | [getTargetFragment](../android/app/Fragment.md))`()` Return the target fragment set by [setTargetFragment](../android/app/Fragment.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTargetRequestCode](../android/app/Fragment.md))`()` Return the target request code set by [setTargetFragment](../android/app/Fragment.md)). |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getText](../android/app/Fragment.md))`(`resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return a localized, styled CharSequence from the application's package's default string table. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getUserVisibleHint](../android/app/Fragment.md))`()` <br /> |
| open [View](../android/view/View.md)? | [getView](../android/app/Fragment.md))`()` Get the root view for the fragment's layout (the one returned by [onCreateView](../android/app/Fragment.md))), if provided. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/app/Fragment.md))`()` Subclasses can not override hashCode(). |
| openstatic [Fragment](../android/app/Fragment.md)! | [instantiate](../android/app/Fragment.md))`(`context:` ` [Context](../android/content/Context.md)!`, `fname:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Like [instantiate(android.content.Context,java.lang.String,android.os.Bundle)](../android/app/Fragment.md))but with a null argument Bundle. |
| openstatic [Fragment](../android/app/Fragment.md)! | [instantiate](../android/app/Fragment.md))`(`context:` ` [Context](../android/content/Context.md)!`, `fname:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `args:` ` [Bundle](../android/os/Bundle.md)?`)` Create a new instance of a Fragment with the given class name. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAdded](../android/app/Fragment.md))`()` Return true if the fragment is currently added to its activity. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDetached](../android/app/Fragment.md))`()` Return true if the fragment has been explicitly detached from the UI. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHidden](../android/app/Fragment.md))`()` Return true if the fragment has been hidden. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInLayout](../android/app/Fragment.md))`()` Return true if the layout is included as part of an activity view hierarchy via the \<fragment\> tag. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRemoving](../android/app/Fragment.md))`()` Return true if this fragment is currently being removed from its activity. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isResumed](../android/app/Fragment.md))`()` Return true if the fragment is in the resumed state. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStateSaved](../android/app/Fragment.md))`()` Returns true if this fragment is added and its state has already been saved by its host. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVisible](../android/app/Fragment.md))`()` Return true if the fragment is currently visible to the user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityCreated](../android/app/Fragment.md))`(`savedInstanceState:` ` [Bundle](../android/os/Bundle.md)?`)` Called when the fragment's activity has been created and this fragment's view hierarchy instantiated. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityResult](../android/app/Fragment.md))`(`requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [Intent](../android/content/Intent.md)!`)` Receive the result from a previous call to [startActivityForResult(android.content.Intent,int)](../android/app/Fragment.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttach](../android/app/Fragment.md))`(`activity:` ` [Activity](../android/app/Activity.md)!`)` <br /> If you override this method you*must*call through to the superclass implementation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttach](../android/app/Fragment.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Called when a fragment is first attached to its context. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttachFragment](../android/app/Fragment.md))`(`childFragment:` ` [Fragment](../android/app/Fragment.md)!`)` Called when a fragment is attached as a child of this fragment. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConfigurationChanged](../android/app/Fragment.md))`(`newConfig:` ` [Configuration](../android/content/res/Configuration.md)`)` Called by the system when the device configuration changes while your component is running. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onContextItemSelected](../android/app/Fragment.md))`(`item:` ` [MenuItem](../android/view/MenuItem.md)!`)` This hook is called whenever an item in a context menu is selected. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCreate](../android/app/Fragment.md))`(`savedInstanceState:` ` [Bundle](../android/os/Bundle.md)?`)` Called to do initial creation of a fragment. |
| open [Animator](../android/animation/Animator.md)! | [onCreateAnimator](../android/app/Fragment.md))`(`transit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `enter:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `nextAnim:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when a fragment loads an animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCreateContextMenu](../android/app/Fragment.md))`(`menu:` ` [ContextMenu](../android/view/ContextMenu.md)!`, `v:` ` [View](../android/view/View.md)!`, `menuInfo:` ` [ContextMenu.ContextMenuInfo](../android/view/ContextMenu.ContextMenuInfo.md)!`)` Called when a context menu for the`view`is about to be shown. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCreateOptionsMenu](../android/app/Fragment.md))`(`menu:` ` [Menu](../android/view/Menu.md)!`, `inflater:` ` [MenuInflater](../android/view/MenuInflater.md)!`)` Initialize the contents of the Activity's standard options menu. |
| open [View](../android/view/View.md)? | [onCreateView](../android/app/Fragment.md))`(`inflater:` ` [LayoutInflater](../android/view/LayoutInflater.md)!`, `container:` ` [ViewGroup](../android/view/ViewGroup.md)?`, `savedInstanceState:` ` [Bundle](../android/os/Bundle.md)!`)` Called to have the fragment instantiate its user interface view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDestroy](../android/app/Fragment.md))`()` Called when the fragment is no longer in use. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDestroyOptionsMenu](../android/app/Fragment.md))`()` Called when this fragment's option menu items are no longer being included in the overall options menu. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDestroyView](../android/app/Fragment.md))`()` Called when the view previously created by [onCreateView](../android/app/Fragment.md))has been detached from the fragment. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDetach](../android/app/Fragment.md))`()` Called when the fragment is no longer attached to its activity. |
| --- | --- |
| open [LayoutInflater](../android/view/LayoutInflater.md)! | [onGetLayoutInflater](../android/app/Fragment.md))`(`savedInstanceState:` ` [Bundle](../android/os/Bundle.md)!`)` Returns the LayoutInflater used to inflate Views of this Fragment. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onHiddenChanged](../android/app/Fragment.md))`(`hidden:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the hidden state (as returned by [isHidden()](../android/app/Fragment.md))of the fragment has changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInflate](../android/app/Fragment.md))`(`activity:` ` [Activity](../android/app/Activity.md)!`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)!`, `savedInstanceState:` ` [Bundle](../android/os/Bundle.md)!`)` <br /> If you override this method you*must*call through to the superclass implementation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInflate](../android/app/Fragment.md))`(`context:` ` [Context](../android/content/Context.md)!`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)!`, `savedInstanceState:` ` [Bundle](../android/os/Bundle.md)!`)` Called when a fragment is being created as part of a view layout inflation, typically from setting the content view of an activity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInflate](../android/app/Fragment.md))`(`attrs:` ` [AttributeSet](../android/util/AttributeSet.md)!`, `savedInstanceState:` ` [Bundle](../android/os/Bundle.md)!`)` <br /> If you override this method you*must*call through to the superclass implementation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLowMemory](../android/app/Fragment.md))`()` This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMultiWindowModeChanged](../android/app/Fragment.md))`(`isInMultiWindowMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the Fragment's activity changes from fullscreen mode to multi-window mode and visa-versa. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMultiWindowModeChanged](../android/app/Fragment.md))`(`isInMultiWindowMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `newConfig:` ` [Configuration](../android/content/res/Configuration.md)!`)` Called when the Fragment's activity changes from fullscreen mode to multi-window mode and visa-versa. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onOptionsItemSelected](../android/app/Fragment.md))`(`item:` ` [MenuItem](../android/view/MenuItem.md)!`)` This hook is called whenever an item in your options menu is selected. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onOptionsMenuClosed](../android/app/Fragment.md))`(`menu:` ` [Menu](../android/view/Menu.md)!`)` This hook is called whenever the options menu is being closed (either by the user canceling the menu with the back/menu button, or when an item is selected). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPause](../android/app/Fragment.md))`()` Called when the Fragment is no longer resumed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPictureInPictureModeChanged](../android/app/Fragment.md))`(`isInPictureInPictureMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called by the system when the activity changes to and from picture-in-picture mode. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPictureInPictureModeChanged](../android/app/Fragment.md))`(`isInPictureInPictureMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `newConfig:` ` [Configuration](../android/content/res/Configuration.md)!`)` Called by the system when the activity changes to and from picture-in-picture mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPrepareOptionsMenu](../android/app/Fragment.md))`(`menu:` ` [Menu](../android/view/Menu.md)!`)` Prepare the Screen's standard options menu to be displayed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRequestPermissionsResult](../android/app/Fragment.md))`(`requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `permissions:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`, `grantResults:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` Callback for the result from requesting permissions. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResume](../android/app/Fragment.md))`()` Called when the fragment is visible to the user and actively running. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSaveInstanceState](../android/app/Fragment.md))`(`outState:` ` [Bundle](../android/os/Bundle.md)!`)` Called to ask the fragment to save its current dynamic state, so it can later be reconstructed in a new instance of its process is restarted. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStart](../android/app/Fragment.md))`()` Called when the Fragment is visible to the user. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStop](../android/app/Fragment.md))`()` Called when the Fragment is no longer started. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTrimMemory](../android/app/Fragment.md))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the operating system has determined that it is a good time for a process to trim unneeded memory from its process. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onViewCreated](../android/app/Fragment.md))`(`view:` ` [View](../android/view/View.md)!`, `savedInstanceState:` ` [Bundle](../android/os/Bundle.md)?`)` Called immediately after [onCreateView(android.view.LayoutInflater,android.view.ViewGroup,android.os.Bundle)](../android/app/Fragment.md))has returned, but before any saved state has been restored in to the view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onViewStateRestored](../android/app/Fragment.md))`(`savedInstanceState:` ` [Bundle](../android/os/Bundle.md)!`)` Called when all saved state has been restored into the view hierarchy of the fragment. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [postponeEnterTransition](../android/app/Fragment.md))`()` Postpone the entering Fragment transition until [startPostponedEnterTransition()](../android/app/Fragment.md))or [FragmentManager.executePendingTransactions()](../android/app/FragmentManager.md))has been called. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerForContextMenu](../android/app/Fragment.md))`(`view:` ` [View](../android/view/View.md)!`)` Registers a context menu to be shown for the given view (multiple views can show the context menu). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestPermissions](../android/app/Fragment.md))`(`permissions:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`, `requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Requests permissions to be granted to this application. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAllowEnterTransitionOverlap](../android/app/Fragment.md))`(`allow:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the exit transition and enter transition overlap or not. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAllowReturnTransitionOverlap](../android/app/Fragment.md))`(`allow:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the return transition and reenter transition overlap or not. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setArguments](../android/app/Fragment.md))`(`args:` ` [Bundle](../android/os/Bundle.md)!`)` Supply the construction arguments for this fragment. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnterSharedElementCallback](../android/app/Fragment.md))`(`callback:` ` [SharedElementCallback](../android/app/SharedElementCallback.md)!`)` When custom transitions are used with Fragments, the enter transition callback is called when this Fragment is attached or detached when not popping the back stack. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnterTransition](../android/app/Fragment.md))`(`transition:` ` [Transition](../android/transition/Transition.md)!`)` Sets the Transition that will be used to move Views into the initial scene. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExitSharedElementCallback](../android/app/Fragment.md))`(`callback:` ` [SharedElementCallback](../android/app/SharedElementCallback.md)!`)` When custom transitions are used with Fragments, the exit transition callback is called when this Fragment is attached or detached when popping the back stack. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExitTransition](../android/app/Fragment.md))`(`transition:` ` [Transition](../android/transition/Transition.md)!`)` Sets the Transition that will be used to move Views out of the scene when the fragment is removed, hidden, or detached when not popping the back stack. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHasOptionsMenu](../android/app/Fragment.md))`(`hasMenu:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Report that this fragment would like to participate in populating the options menu by receiving a call to [onCreateOptionsMenu](../android/app/Fragment.md))and related methods. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInitialSavedState](../android/app/Fragment.md))`(`state:` ` [Fragment.SavedState](../android/app/Fragment.SavedState.md)!`)` Set the initial saved state that this Fragment should restore itself from when first being constructed, as returned by [FragmentManager.saveFragmentInstanceState](../android/app/FragmentManager.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMenuVisibility](../android/app/Fragment.md))`(`menuVisible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set a hint for whether this fragment's menu should be visible. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReenterTransition](../android/app/Fragment.md))`(`transition:` ` [Transition](../android/transition/Transition.md)!`)` Sets the Transition that will be used to move Views in to the scene when returning due to popping a back stack. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRetainInstance](../android/app/Fragment.md))`(`retain:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Control whether a fragment instance is retained across Activity re-creation (such as from a configuration change). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReturnTransition](../android/app/Fragment.md))`(`transition:` ` [Transition](../android/transition/Transition.md)!`)` Sets the Transition that will be used to move Views out of the scene when the Fragment is preparing to be removed, hidden, or detached because of popping the back stack. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSharedElementEnterTransition](../android/app/Fragment.md))`(`transition:` ` [Transition](../android/transition/Transition.md)!`)` Sets the Transition that will be used for shared elements transferred into the content Scene. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSharedElementReturnTransition](../android/app/Fragment.md))`(`transition:` ` [Transition](../android/transition/Transition.md)!`)` Sets the Transition that will be used for shared elements transferred back during a pop of the back stack. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTargetFragment](../android/app/Fragment.md))`(`fragment:` ` [Fragment](../android/app/Fragment.md)!`, `requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Optional target for this fragment. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUserVisibleHint](../android/app/Fragment.md))`(`isVisibleToUser:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set a hint to the system about whether this fragment's UI is currently visible to the user. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldShowRequestPermissionRationale](../android/app/Fragment.md))`(`permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Gets whether you should show UI with rationale before requesting a permission. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startActivity](../android/app/Fragment.md))`(`intent:` ` [Intent](../android/content/Intent.md)!`)` Call android. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startActivity](../android/app/Fragment.md))`(`intent:` ` [Intent](../android/content/Intent.md)!`, `options:` ` [Bundle](../android/os/Bundle.md)!`)` Call android. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startActivityForResult](../android/app/Fragment.md))`(`intent:` ` [Intent](../android/content/Intent.md)!`, `requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Call [Activity.startActivityForResult(Intent, int)](../android/app/Activity.md))from the fragment's containing Activity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startActivityForResult](../android/app/Fragment.md))`(`intent:` ` [Intent](../android/content/Intent.md)!`, `requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `options:` ` [Bundle](../android/os/Bundle.md)!`)` Call [Activity.startActivityForResult(Intent, int, Bundle)](../android/app/Activity.md))from the fragment's containing Activity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startIntentSenderForResult](../android/app/Fragment.md))`(`intent:` ` [IntentSender](../android/content/IntentSender.md)!`, `requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fillInIntent:` ` [Intent](../android/content/Intent.md)?`, `flagsMask:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flagsValues:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `extraFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `options:` ` [Bundle](../android/os/Bundle.md)!`)` Call [Activity.startIntentSenderForResult(IntentSender, int, Intent, int, int, int,](../android/app/Activity.md))from the fragment's containing Activity. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startPostponedEnterTransition](../android/app/Fragment.md))`()` Begin postponed transitions after [postponeEnterTransition()](../android/app/Fragment.md))was called. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/app/Fragment.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterForContextMenu](../android/app/Fragment.md))`(`view:` ` [View](../android/view/View.md)!`)` Prevents a context menu to be shown for the given view. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [ComponentCallbacks](../android/content/ComponentCallbacks.md) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConfigurationChanged](../android/content/ComponentCallbacks.md))`(`newConfig:` ` [Configuration](../android/content/res/Configuration.md)`)` <br /> Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources. At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration. For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLowMemory](../android/content/ComponentCallbacks.md))`()` <br /> This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing. <br /> | ||

## Public constructors

### Fragment

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Fragment()
```

Default constructor.**Every** fragment must have an empty constructor, so it can be instantiated when restoring its activity's state. It is strongly recommended that subclasses do not have other constructors with parameters, since these constructors will not be called when the fragment is re-instantiated; instead, arguments can be supplied by the caller with [setArguments](../android/app/Fragment.md))and later retrieved by the Fragment with [getArguments](../android/app/Fragment.md)).

Applications should generally not implement a constructor. Prefer [onAttach(android.content.Context)](../android/app/Fragment.md))instead. It is the first place application code can run where the fragment is ready to be used - the point where the fragment is actually associated with its context. Some applications may also want to implement #onInflate to retrieve attributes from a layout resource, although note this happens when the fragment is attached.

## Public methods

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
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Text to print at the front of each line. |
| `fd` | [FileDescriptor](../java/io/FileDescriptor.md)!:The raw file descriptor that the dump is being sent to. |
| `writer` | [PrintWriter](../java/io/PrintWriter.md)!:The PrintWriter to which you should dump your state. This will be closed for you after you return. |
| --- | --- |
| `args` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:additional arguments to the dump request. |

### equals

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

**Deprecated:** *Deprecated in Java.*

Subclasses can not override equals().

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getActivity

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActivity(): Activity!
```

**Deprecated:** *Deprecated in Java.*

Return the Activity this fragment is currently associated with. 

### getAllowEnterTransitionOverlap

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAllowEnterTransitionOverlap(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns whether the exit transition and enter transition overlap or not. When true, the enter transition will start as soon as possible. When false, the enter transition will wait until the exit transition completes before starting.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true when the enter transition should start as soon as possible or false to when it should wait until the exiting transition completes. |

### getAllowReturnTransitionOverlap

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAllowReturnTransitionOverlap(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns whether the return transition and reenter transition overlap or not. When true, the reenter transition will start as soon as possible. When false, the reenter transition will wait until the return transition completes before starting.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true to start the reenter transition when possible or false to wait until the return transition completes. |

### getArguments

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getArguments(): Bundle!
```

**Deprecated:** *Deprecated in Java.*

Return the arguments supplied to [setArguments](../android/app/Fragment.md)), if any. 

### getChildFragmentManager

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getChildFragmentManager(): FragmentManager!
```

**Deprecated:** *Deprecated in Java.*

Return a private FragmentManager for placing and managing Fragments inside of this Fragment. 

### getContext

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContext(): Context!
```

**Deprecated:** *Deprecated in Java.*

Return the [Context](../android/content/Context.md) this fragment is currently associated with. 

### getEnterTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEnterTransition(): Transition!
```

**Deprecated:** *Deprecated in Java.*

Returns the Transition that will be used to move Views into the initial scene. The entering Views will be those that are regular Views or ViewGroups that have [ViewGroup.isTransitionGroup](../android/view/ViewGroup.md))return true. Typical Transitions will extend [android.transition.Visibility](../android/transition/Visibility.md) as entering is governed by changing visibility from [View.INVISIBLE](../android/view/View.md) to [View.VISIBLE](../android/view/View.md).

| Return ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Transition](../android/transition/Transition.md)! | the Transition to use to move Views into the initial Scene. |

### getExitTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExitTransition(): Transition!
```

**Deprecated:** *Deprecated in Java.*

Returns the Transition that will be used to move Views out of the scene when the fragment is removed, hidden, or detached when not popping the back stack. The exiting Views will be those that are regular Views or ViewGroups that have [ViewGroup.isTransitionGroup](../android/view/ViewGroup.md))return true. Typical Transitions will extend [android.transition.Visibility](../android/transition/Visibility.md) as exiting is governed by changing visibility from [View.VISIBLE](../android/view/View.md) to [View.INVISIBLE](../android/view/View.md). If transition is null, the views will remain unaffected.

| Return ||
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Transition](../android/transition/Transition.md)! | the Transition to use to move Views out of the Scene when the Fragment is being closed not due to popping the back stack. |

### getFragmentManager

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFragmentManager(): FragmentManager!
```

**Deprecated:** *Deprecated in Java.*

Return the FragmentManager for interacting with fragments associated with this fragment's activity. Note that this will be non-null slightly before [getActivity()](../android/app/Fragment.md)), during the time from when the fragment is placed in a [FragmentTransaction](../android/app/FragmentTransaction.md) until it is committed and attached to its activity.

If this Fragment is a child of another Fragment, the FragmentManager returned here will be the parent's [getChildFragmentManager()](../android/app/Fragment.md)). 

### getHost

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHost(): Any?
```

**Deprecated:** *Deprecated in Java.*

Return the host object of this fragment. May return`null`if the fragment isn't currently being hosted. 

### getId

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): Int
```

**Deprecated:** *Deprecated in Java.*

Return the identifier this fragment is known by. This is either the android:id value supplied in a layout or the container view ID supplied when adding the fragment. 

### getLayoutInflater

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLayoutInflater(): LayoutInflater!
```

**Deprecated:** *Deprecated in Java.*

Returns the cached LayoutInflater used to inflate Views of this Fragment. If [onGetLayoutInflater(android.os.Bundle)](../android/app/Fragment.md))has not been called [onGetLayoutInflater(android.os.Bundle)](../android/app/Fragment.md))will be called with a`null`argument and that value will be cached.

The cached LayoutInflater will be replaced immediately prior to [onCreateView(android.view.LayoutInflater,android.view.ViewGroup,android.os.Bundle)](../android/app/Fragment.md))and cleared immediately after [onDetach()](../android/app/Fragment.md)).

| Return ||
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [LayoutInflater](../android/view/LayoutInflater.md)! | The LayoutInflater used to inflate Views of this Fragment. |

### getLoaderManager

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLoaderManager(): LoaderManager!
```

**Deprecated:** *Use androidx.fragment.app.Fragment#getLoaderManager()*

Return the LoaderManager for this fragment, creating it if needed. 

### getParentFragment

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParentFragment(): Fragment!
```

**Deprecated:** *Deprecated in Java.*

Returns the parent Fragment containing this Fragment. If this Fragment is attached directly to an Activity, returns null. 

### getReenterTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReenterTransition(): Transition!
```

**Deprecated:** *Deprecated in Java.*

Returns the Transition that will be used to move Views in to the scene when returning due to popping a back stack. The entering Views will be those that are regular Views or ViewGroups that have [ViewGroup.isTransitionGroup](../android/view/ViewGroup.md))return true. Typical Transitions will extend [android.transition.Visibility](../android/transition/Visibility.md) as exiting is governed by changing visibility from [View.VISIBLE](../android/view/View.md) to [View.INVISIBLE](../android/view/View.md). If transition is null, the views will remain unaffected. If nothing is set, the default will be to use the same transition as [setExitTransition(android.transition.Transition)](../android/app/Fragment.md)).

| Return ||
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Transition](../android/transition/Transition.md)! | the Transition to use to move Views into the scene when reentering from a previously-started Activity. |

### getResources

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getResources(): Resources!
```

**Deprecated:** *Deprecated in Java.*

Return`getActivity().getResources()`. 

### getRetainInstance

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRetainInstance(): Boolean
```

**Deprecated:** *Deprecated in Java.* 

### getReturnTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReturnTransition(): Transition!
```

**Deprecated:** *Deprecated in Java.*

Returns the Transition that will be used to move Views out of the scene when the Fragment is preparing to be removed, hidden, or detached because of popping the back stack. The exiting Views will be those that are regular Views or ViewGroups that have [ViewGroup.isTransitionGroup](../android/view/ViewGroup.md))return true. Typical Transitions will extend [android.transition.Visibility](../android/transition/Visibility.md) as entering is governed by changing visibility from [View.VISIBLE](../android/view/View.md) to [View.INVISIBLE](../android/view/View.md). If`transition`is null, entering Views will remain unaffected.

| Return ||
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Transition](../android/transition/Transition.md)! | the Transition to use to move Views out of the Scene when the Fragment is preparing to close. |

### getSharedElementEnterTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSharedElementEnterTransition(): Transition!
```

**Deprecated:** *Deprecated in Java.*

Returns the Transition that will be used for shared elements transferred into the content Scene. Typical Transitions will affect size and location, such as [android.transition.ChangeBounds](../android/transition/ChangeBounds.md). A null value will cause transferred shared elements to blink to the final position.

| Return ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Transition](../android/transition/Transition.md)! | The Transition to use for shared elements transferred into the content Scene. |

### getSharedElementReturnTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSharedElementReturnTransition(): Transition!
```

**Deprecated:** *Deprecated in Java.*

Return the Transition that will be used for shared elements transferred back during a pop of the back stack. This Transition acts in the leaving Fragment. Typical Transitions will affect size and location, such as [android.transition.ChangeBounds](../android/transition/ChangeBounds.md). A null value will cause transferred shared elements to blink to the final position. If no value is set, the default will be to use the same value as [setSharedElementEnterTransition(android.transition.Transition)](../android/app/Fragment.md)).

| Return ||
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Transition](../android/transition/Transition.md)! | The Transition to use for shared elements transferred out of the content Scene. |

### getString

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getString(resId: Int): String!
```

**Deprecated:** *Deprecated in Java.*

Return a localized string from the application's package's default string table.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------|
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Resource id for the string |

### getString

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getString(
    resId: Int, 
    vararg formatArgs: Any!
): String!
```

**Deprecated:** *Deprecated in Java.*

Return a localized formatted string from the application's package's default string table, substituting the format arguments as defined in [java.util.Formatter](../java/util/Formatter.md) and java.lang.String#format.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Resource id for the format string |
| `formatArgs` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The format arguments that will be used for substitution. |

### getTag

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTag(): String!
```

**Deprecated:** *Deprecated in Java.*

Get the tag name of the fragment, if specified. 

### getTargetFragment

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTargetFragment(): Fragment!
```

**Deprecated:** *Deprecated in Java.*

Return the target fragment set by [setTargetFragment](../android/app/Fragment.md)). 

### getTargetRequestCode

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTargetRequestCode(): Int
```

**Deprecated:** *Deprecated in Java.*

Return the target request code set by [setTargetFragment](../android/app/Fragment.md)). 

### getText

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getText(resId: Int): CharSequence!
```

**Deprecated:** *Deprecated in Java.*

Return a localized, styled CharSequence from the application's package's default string table.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------|
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Resource id for the CharSequence text |

### getUserVisibleHint

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUserVisibleHint(): Boolean
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | The current value of the user-visible hint on this fragment. |

**See Also**

- [#setUserVisibleHint(boolean)](../android/app/Fragment.md)) 

### getView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getView(): View?
```

**Deprecated:** *Deprecated in Java.*

Get the root view for the fragment's layout (the one returned by [onCreateView](../android/app/Fragment.md))), if provided.

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------|
| [View](../android/view/View.md)? | The fragment's root view, or null if it has no layout. |

### hashCode

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

**Deprecated:** *Deprecated in Java.*

Subclasses can not override hashCode().

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### instantiate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun instantiate(
    context: Context!, 
    fname: String!
): Fragment!
```

**Deprecated:** *Deprecated in Java.*

Like [instantiate(android.content.Context,java.lang.String,android.os.Bundle)](../android/app/Fragment.md))but with a null argument Bundle. 

### instantiate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun instantiate(
    context: Context!, 
    fname: String!, 
    args: Bundle?
): Fragment!
```

**Deprecated:** *Deprecated in Java.*

Create a new instance of a Fragment with the given class name. This is the same as calling its empty constructor.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:The calling context being used to instantiate the fragment. This is currently just used to get its ClassLoader. |
| `fname` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The class name of the fragment to instantiate. |
| `args` | [Bundle](../android/os/Bundle.md)?:Bundle of arguments to supply to the fragment, which it can retrieve with [getArguments()](../android/app/Fragment.md)). May be null. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------|
| [Fragment](../android/app/Fragment.md)! | Returns a new fragment instance. |

| Exceptions ||
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `android.app.Fragment.InstantiationException` | If there is a failure in instantiating the given fragment class. This is a runtime exception; it is not normally expected to happen. |

### isAdded

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAdded(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Return true if the fragment is currently added to its activity. 

### isDetached

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isDetached(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Return true if the fragment has been explicitly detached from the UI. That is, [FragmentTransaction.detach(Fragment)](../android/app/FragmentTransaction.md))has been used on it. 

### isHidden

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isHidden(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Return true if the fragment has been hidden. By default fragments are shown. You can find out about changes to this state with [onHiddenChanged](../android/app/Fragment.md)). Note that the hidden state is orthogonal to other states -- that is, to be visible to the user, a fragment must be both started and not hidden. 

### isInLayout

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isInLayout(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Return true if the layout is included as part of an activity view hierarchy via the \<fragment\> tag. This will always be true when fragments are created through the \<fragment\> tag,*except*in the case where an old fragment is restored from a previous state and it does not appear in the layout of the current state. 

### isRemoving

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isRemoving(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Return true if this fragment is currently being removed from its activity. This is*not*whether its activity is finishing, but rather whether it is in the process of being removed from its activity. 

### isResumed

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isResumed(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Return true if the fragment is in the resumed state. This is true for the duration of [onResume()](../android/app/Fragment.md))and [onPause()](../android/app/Fragment.md))as well. 

### isStateSaved

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isStateSaved(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if this fragment is added and its state has already been saved by its host. Any operations that would change saved state should not be performed if this method returns true, and some operations such as [setArguments(android.os.Bundle)](../android/app/Fragment.md))will fail.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this fragment's state has already been saved by its host |

### isVisible

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isVisible(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Return true if the fragment is currently visible to the user. This means it: (1) has been added, (2) has its view attached to the window, and (3) is not hidden. 

### onActivityCreated

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityCreated(savedInstanceState: Bundle?): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the fragment's activity has been created and this fragment's view hierarchy instantiated. It can be used to do final initialization once these pieces are in place, such as retrieving views or restoring state. It is also useful for fragments that use [setRetainInstance(boolean)](../android/app/Fragment.md))to retain their instance, as this callback tells the fragment when it is fully associated with the new activity instance. This is called after [onCreateView](../android/app/Fragment.md))and before [onViewStateRestored(android.os.Bundle)](../android/app/Fragment.md)). 
If you override this method you*must*call through to the superclass implementation.

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `savedInstanceState` | [Bundle](../android/os/Bundle.md)?:If the fragment is being re-created from a previous saved state, this is the state. This value may be`null`. |

### onActivityResult

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityResult(
    requestCode: Int, 
    resultCode: Int, 
    data: Intent!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Receive the result from a previous call to [startActivityForResult(android.content.Intent,int)](../android/app/Fragment.md)). This follows the related Activity API as described there in [Activity.onActivityResult(int, int, Intent)](../android/app/Activity.md)).

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The integer request code originally supplied to startActivityForResult(), allowing you to identify who this result came from. |
| `resultCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The integer result code returned by the child activity through its setResult(). |
| `data` | [Intent](../android/content/Intent.md)!:An Intent, which can return result data to the caller (various data can be attached to Intent "extras"). |
| --- | --- |

### onAttach

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAttach(activity: Activity!): Unit
```

**Deprecated:** *Use [onAttach(android.content.Context)](../android/app/Fragment.md))instead.*

<br />

If you override this method you*must*call through to the superclass implementation. 

### onAttach

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAttach(context: Context!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when a fragment is first attached to its context. [onCreate(android.os.Bundle)](../android/app/Fragment.md))will be called after this. 
If you override this method you*must*call through to the superclass implementation. 

### onAttachFragment

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAttachFragment(childFragment: Fragment!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when a fragment is attached as a child of this fragment.

This is called after the attached fragment's`onAttach`and before the attached fragment's`onCreate`if the fragment has not yet had a previous call to`onCreate`.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------|
| `childFragment` | [Fragment](../android/app/Fragment.md)!:child fragment being attached |

### onConfigurationChanged

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onConfigurationChanged(newConfig: Configuration): Unit
```

**Deprecated:** *Deprecated in Java.*

Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources.

At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration.

For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html). If you override this method you*must*call through to the superclass implementation.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newConfig` | [Configuration](../android/content/res/Configuration.md):The new device configuration. This value cannot be`null`. |

### onContextItemSelected

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onContextItemSelected(item: MenuItem!): Boolean
```

**Deprecated:** *Deprecated in Java.*

This hook is called whenever an item in a context menu is selected. The default implementation simply returns false to have the normal processing happen (calling the item's Runnable or sending a message to its Handler as appropriate). You can use this method for any items for which you would like to do processing without those other facilities.

Use [MenuItem.getMenuInfo()](../android/view/MenuItem.md))to get extra information set by the View that added this menu item.

Derived classes should call through to the base class for it to perform the default menu handling.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------|
| `item` | [MenuItem](../android/view/MenuItem.md)!:The context menu item that was selected. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean Return false to allow normal context menu processing to proceed, true to consume it here. |

### onCreate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCreate(savedInstanceState: Bundle?): Unit
```

**Deprecated:** *Deprecated in Java.*

Called to do initial creation of a fragment. This is called after [onAttach(android.app.Activity)](../android/app/Fragment.md))and before [onCreateView(android.view.LayoutInflater,android.view.ViewGroup,android.os.Bundle)](../android/app/Fragment.md)), but is not called if the fragment instance is retained across Activity re-creation (see [setRetainInstance(boolean)](../android/app/Fragment.md))).

Note that this can be called while the fragment's activity is still in the process of being created. As such, you can not rely on things like the activity's content view hierarchy being initialized at this point. If you want to do work once the activity itself is created, see [onActivityCreated(android.os.Bundle)](../android/app/Fragment.md)).

If your app's`targetSdkVersion`is [android.os.Build.VERSION_CODES#M](../android/os/Build.VERSION_CODES.md) or lower, child fragments being restored from the savedInstanceState are restored after`onCreate`returns. When targeting [android.os.Build.VERSION_CODES#N](../android/os/Build.VERSION_CODES.md) or above and running on an N or newer platform version they are restored by`Fragment.onCreate`.

If you override this method you*must* call through to the superclass implementation.

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `savedInstanceState` | [Bundle](../android/os/Bundle.md)?:If the fragment is being re-created from a previous saved state, this is the state. This value may be`null`. |

### onCreateAnimator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCreateAnimator(
    transit: Int, 
    enter: Boolean, 
    nextAnim: Int
): Animator!
```

**Deprecated:** *Deprecated in Java.*

Called when a fragment loads an animation. 

### onCreateContextMenu

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCreateContextMenu(
    menu: ContextMenu!, 
    v: View!, 
    menuInfo: ContextMenu.ContextMenuInfo!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when a context menu for the`view`is about to be shown. Unlike [onCreateOptionsMenu](../android/app/Fragment.md)), this will be called every time the context menu is about to be shown and should be populated for the view (or item inside the view for [AdapterView](../android/widget/AdapterView.md) subclasses, this can be found in the`menuInfo`)).

Use [onContextItemSelected(android.view.MenuItem)](../android/app/Fragment.md))to know when an item has been selected.

The default implementation calls up to [Activity.onCreateContextMenu](../android/app/Activity.md)), though you can not call this implementation if you don't want that behavior.

It is not safe to hold onto the context menu after this method returns. Called when the context menu for this view is being built. It is not safe to hold onto the menu after this method returns.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `menu` | [ContextMenu](../android/view/ContextMenu.md)!:The context menu that is being built |
| `v` | [View](../android/view/View.md)!:The view for which the context menu is being built |
| `menuInfo` | [ContextMenu.ContextMenuInfo](../android/view/ContextMenu.ContextMenuInfo.md)!:Extra information about the item for which the context menu should be shown. This information will vary depending on the class of v. |
| --- | --- |

### onCreateOptionsMenu

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCreateOptionsMenu(
    menu: Menu!, 
    inflater: MenuInflater!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Initialize the contents of the Activity's standard options menu. You should place your menu items in to menu. For this method to be called, you must have first called [setHasOptionsMenu](../android/app/Fragment.md)). See [Activity.onCreateOptionsMenu](../android/app/Activity.md))for more information.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------|
| `menu` | [Menu](../android/view/Menu.md)!:The options menu in which you place your items. |

**See Also**

- [#setHasOptionsMenu](../android/app/Fragment.md))
- [#onPrepareOptionsMenu](../android/app/Fragment.md))
- [#onOptionsItemSelected](../android/app/Fragment.md)) 

### onCreateView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCreateView(
    inflater: LayoutInflater!, 
    container: ViewGroup?, 
    savedInstanceState: Bundle!
): View?
```

**Deprecated:** *Deprecated in Java.*

Called to have the fragment instantiate its user interface view. This is optional, and non-graphical fragments can return null (which is the default implementation). This will be called between [onCreate(android.os.Bundle)](../android/app/Fragment.md))and [onActivityCreated(android.os.Bundle)](../android/app/Fragment.md)).

If you return a View from here, you will later be called in [onDestroyView](../android/app/Fragment.md))when the view is being released.

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inflater` | [LayoutInflater](../android/view/LayoutInflater.md)!:The LayoutInflater object that can be used to inflate any views in the fragment, |
| `container` | [ViewGroup](../android/view/ViewGroup.md)?:If non-null, this is the parent view that the fragment's UI should be attached to. The fragment should not add the view itself, but this can be used to generate the LayoutParams of the view. |
| `savedInstanceState` | [Bundle](../android/os/Bundle.md)!:If non-null, this fragment is being re-constructed from a previous saved state as given here. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------|
| [View](../android/view/View.md)? | Return the View for the fragment's UI, or null. |

### onDestroy

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDestroy(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the fragment is no longer in use. This is called after [onStop()](../android/app/Fragment.md))and before [onDetach()](../android/app/Fragment.md)). 
If you override this method you*must*call through to the superclass implementation. 

### onDestroyOptionsMenu

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDestroyOptionsMenu(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when this fragment's option menu items are no longer being included in the overall options menu. Receiving this call means that the menu needed to be rebuilt, but this fragment's items were not included in the newly built menu (its [onCreateOptionsMenu(android.view.Menu,android.view.MenuInflater)](../android/app/Fragment.md))was not called). 

### onDestroyView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDestroyView(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the view previously created by [onCreateView](../android/app/Fragment.md))has been detached from the fragment. The next time the fragment needs to be displayed, a new view will be created. This is called after [onStop()](../android/app/Fragment.md))and before [onDestroy()](../android/app/Fragment.md)). It is called*regardless* of whether [onCreateView](../android/app/Fragment.md))returned a non-null view. Internally it is called after the view's state has been saved but before it has been removed from its parent. 
If you override this method you*must*call through to the superclass implementation. 

### onDetach

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDetach(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the fragment is no longer attached to its activity. This is called after [onDestroy()](../android/app/Fragment.md)), except in the cases where the fragment instance is retained across Activity re-creation (see [setRetainInstance(boolean)](../android/app/Fragment.md))), in which case it is called after [onStop()](../android/app/Fragment.md)). 
If you override this method you*must*call through to the superclass implementation. 

### onGetLayoutInflater

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onGetLayoutInflater(savedInstanceState: Bundle!): LayoutInflater!
```

**Deprecated:** *Deprecated in Java.*

Returns the LayoutInflater used to inflate Views of this Fragment. The default implementation will throw an exception if the Fragment is not attached.

| Return ||
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [LayoutInflater](../android/view/LayoutInflater.md)! | The LayoutInflater used to inflate Views of this Fragment. |

### onHiddenChanged

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onHiddenChanged(hidden: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the hidden state (as returned by [isHidden()](../android/app/Fragment.md))of the fragment has changed. Fragments start out not hidden; this will be called whenever the fragment changes state from that.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `hidden` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the fragment is now hidden, false otherwise. |

### onInflate

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onInflate(
    activity: Activity!, 
    attrs: AttributeSet!, 
    savedInstanceState: Bundle!
): Unit
```

**Deprecated:** *Use [onInflate(android.content.Context,android.util.AttributeSet,android.os.Bundle)](../android/app/Fragment.md))instead.*

<br />

If you override this method you*must*call through to the superclass implementation. 

### onInflate

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onInflate(
    context: Context!, 
    attrs: AttributeSet!, 
    savedInstanceState: Bundle!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when a fragment is being created as part of a view layout inflation, typically from setting the content view of an activity. This may be called immediately after the fragment is created from a tag in a layout file. Note this is*before* the fragment's [onAttach(android.app.Activity)](../android/app/Fragment.md))has been called; all you should do here is parse the attributes and save them away.

This is called every time the fragment is inflated, even if it is being inflated into a new instance with saved state. It typically makes sense to re-parse the parameters each time, to allow them to change with different configurations.

Here is a typical implementation of a fragment that can take parameters both through attributes supplied here as well from [getArguments()](../android/app/Fragment.md)):

Note that parsing the XML attributes uses a "styleable" resource. The declaration for the styleable used here is:

The fragment can then be declared within its activity's content layout through a tag like this:

This fragment can also be created dynamically from arguments given at runtime in the arguments Bundle; here is an example of doing so at creation of the containing activity:

If you override this method you*must* call through to the superclass implementation.

<br />

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:The Context that is inflating this fragment. |
| `attrs` | [AttributeSet](../android/util/AttributeSet.md)!:The attributes at the tag where the fragment is being created. |
| `savedInstanceState` | [Bundle](../android/os/Bundle.md)!:If the fragment is being re-created from a previous saved state, this is the state. |
| --- | --- |

### onInflate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onInflate(
    attrs: AttributeSet!, 
    savedInstanceState: Bundle!
): Unit
```

**Deprecated:** *Use [onInflate(android.content.Context,android.util.AttributeSet,android.os.Bundle)](../android/app/Fragment.md))instead.*

<br />

If you override this method you*must*call through to the superclass implementation. 

### onLowMemory

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onLowMemory(): Unit
```

**Deprecated:** *Deprecated in Java.*

This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing. If you override this method you*must*call through to the superclass implementation. 

### onMultiWindowModeChanged

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onMultiWindowModeChanged(isInMultiWindowMode: Boolean): Unit
```

**Deprecated:** *Use [onMultiWindowModeChanged(boolean,android.content.res.Configuration)](../android/app/Fragment.md))instead.*

Called when the Fragment's activity changes from fullscreen mode to multi-window mode and visa-versa. This is generally tied to android.app.Activity#onMultiWindowModeChanged of the containing Activity.

| Parameters ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------|
| `isInMultiWindowMode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the activity is in multi-window mode. |

### onMultiWindowModeChanged

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onMultiWindowModeChanged(
    isInMultiWindowMode: Boolean, 
    newConfig: Configuration!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the Fragment's activity changes from fullscreen mode to multi-window mode and visa-versa. This is generally tied to android.app.Activity#onMultiWindowModeChanged of the containing Activity. This method provides the same configuration that will be sent in the following [onConfigurationChanged(android.content.res.Configuration)](../android/app/Fragment.md))call after the activity enters this mode.

| Parameters ||
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `isInMultiWindowMode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the activity is in multi-window mode. |
| `newConfig` | [Configuration](../android/content/res/Configuration.md)!:The new configuration of the activity with the state {@param isInMultiWindowMode}. |

### onOptionsItemSelected

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onOptionsItemSelected(item: MenuItem!): Boolean
```

**Deprecated:** *Deprecated in Java.*

This hook is called whenever an item in your options menu is selected. The default implementation simply returns false to have the normal processing happen (calling the item's Runnable or sending a message to its Handler as appropriate). You can use this method for any items for which you would like to do processing without those other facilities.

Derived classes should call through to the base class for it to perform the default menu handling.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------|
| `item` | [MenuItem](../android/view/MenuItem.md)!:The menu item that was selected. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean Return false to allow normal menu processing to proceed, true to consume it here. |

**See Also**

- [#onCreateOptionsMenu](../android/app/Fragment.md)) 

### onOptionsMenuClosed

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onOptionsMenuClosed(menu: Menu!): Unit
```

**Deprecated:** *Deprecated in Java.*

This hook is called whenever the options menu is being closed (either by the user canceling the menu with the back/menu button, or when an item is selected).

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `menu` | [Menu](../android/view/Menu.md)!:The options menu as last shown or first initialized by onCreateOptionsMenu(). |

### onPause

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPause(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the Fragment is no longer resumed. This is generally tied to [Activity.onPause](../android/app/Activity.md))of the containing Activity's lifecycle. 
If you override this method you*must*call through to the superclass implementation. 

### onPictureInPictureModeChanged

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPictureInPictureModeChanged(isInPictureInPictureMode: Boolean): Unit
```

**Deprecated:** *Use [onPictureInPictureModeChanged(boolean,android.content.res.Configuration)](../android/app/Fragment.md))instead.*

Called by the system when the activity changes to and from picture-in-picture mode. This is generally tied to android.app.Activity#onPictureInPictureModeChanged of the containing Activity.

| Parameters ||
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `isInPictureInPictureMode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the activity is in picture-in-picture mode. |

### onPictureInPictureModeChanged

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPictureInPictureModeChanged(
    isInPictureInPictureMode: Boolean, 
    newConfig: Configuration!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called by the system when the activity changes to and from picture-in-picture mode. This is generally tied to android.app.Activity#onPictureInPictureModeChanged of the containing Activity. This method provides the same configuration that will be sent in the following [onConfigurationChanged(android.content.res.Configuration)](../android/app/Fragment.md))call after the activity enters this mode.

| Parameters ||
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `isInPictureInPictureMode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the activity is in picture-in-picture mode. |
| `newConfig` | [Configuration](../android/content/res/Configuration.md)!:The new configuration of the activity with the state {@param isInPictureInPictureMode}. |

### onPrepareOptionsMenu

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPrepareOptionsMenu(menu: Menu!): Unit
```

**Deprecated:** *Deprecated in Java.*

Prepare the Screen's standard options menu to be displayed. This is called right before the menu is shown, every time it is shown. You can use this method to efficiently enable/disable items or otherwise dynamically modify the contents. See [Activity.onPrepareOptionsMenu](../android/app/Activity.md))for more information.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `menu` | [Menu](../android/view/Menu.md)!:The options menu as last shown or first initialized by onCreateOptionsMenu(). |

**See Also**

- [#setHasOptionsMenu](../android/app/Fragment.md))
- [#onCreateOptionsMenu](../android/app/Fragment.md)) 

### onRequestPermissionsResult

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onRequestPermissionsResult(
    requestCode: Int, 
    permissions: Array<String!>, 
    grantResults: IntArray
): Unit
```

**Deprecated:** *Deprecated in Java.*

Callback for the result from requesting permissions. This method is invoked for every call on[requestPermissions(java.lang.String[],int)](https://developer.android.com/reference/kotlin/android/app/Fragment#requestPermissions(kotlin.Array,%20kotlin.Int)).

**Note:**It is possible that the permissions request interaction with the user is interrupted. In this case you will receive empty permissions and results arrays which should be treated as a cancellation.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The request code passed in[requestPermissions(java.lang.String[],int)](https://developer.android.com/reference/kotlin/android/app/Fragment#requestPermissions(kotlin.Array,%20kotlin.Int)). |
| `permissions` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:The requested permissions. Never null. |
| `grantResults` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html):The grant results for the corresponding permissions which is either [android.content.pm.PackageManager#PERMISSION_GRANTED](../android/content/pm/PackageManager.md) or [android.content.pm.PackageManager#PERMISSION_DENIED](../android/content/pm/PackageManager.md). Never null. |
| --- | --- |

**See Also**

- [#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Fragment#requestPermissions(kotlin.Array,%20kotlin.Int)) 

### onResume

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onResume(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the fragment is visible to the user and actively running. This is generally tied to [Activity.onResume](../android/app/Activity.md))of the containing Activity's lifecycle. 
If you override this method you*must*call through to the superclass implementation. 

### onSaveInstanceState

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSaveInstanceState(outState: Bundle!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called to ask the fragment to save its current dynamic state, so it can later be reconstructed in a new instance of its process is restarted. If a new instance of the fragment later needs to be created, the data you place in the Bundle here will be available in the Bundle given to [onCreate(android.os.Bundle)](../android/app/Fragment.md)), [onCreateView(android.view.LayoutInflater,android.view.ViewGroup,android.os.Bundle)](../android/app/Fragment.md)), and [onActivityCreated(android.os.Bundle)](../android/app/Fragment.md)).

This corresponds to [Activity.onSaveInstanceState(Bundle)](../android/app/Activity.md))and most of the discussion there applies here as well. Note however:*this method may be called at any time before [onDestroy()](../android/app/Fragment.md))*. There are many situations where a fragment may be mostly torn down (such as when placed on the back stack with no UI showing), but its state will not be saved until its owning activity actually needs to save its state.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------|
| `outState` | [Bundle](../android/os/Bundle.md)!:Bundle in which to place your saved state. |

### onStart

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onStart(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the Fragment is visible to the user. This is generally tied to [Activity.onStart](../android/app/Activity.md))of the containing Activity's lifecycle. 
If you override this method you*must*call through to the superclass implementation. 

### onStop

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onStop(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the Fragment is no longer started. This is generally tied to [Activity.onStop](../android/app/Activity.md))of the containing Activity's lifecycle. 
If you override this method you*must*call through to the superclass implementation. 

### onTrimMemory

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTrimMemory(level: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the operating system has determined that it is a good time for a process to trim unneeded memory from its process. You should never compare to exact values of the level, since new intermediate values may be added -- you will typically want to compare if the value is greater or equal to a level you are interested in.

To retrieve the processes current trim level at any point, you can use [ActivityManager.getMyMemoryState(RunningAppProcessInfo)](../android/app/ActivityManager.md)). If you override this method you*must*call through to the superclass implementation.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The context of the trim, giving a hint of the amount of trimming the application may like to perform. Value is [android.content.ComponentCallbacks2#TRIM_MEMORY_COMPLETE](../android/content/ComponentCallbacks2.md), [android.content.ComponentCallbacks2#TRIM_MEMORY_MODERATE](../android/content/ComponentCallbacks2.md), [android.content.ComponentCallbacks2#TRIM_MEMORY_BACKGROUND](../android/content/ComponentCallbacks2.md), [android.content.ComponentCallbacks2#TRIM_MEMORY_UI_HIDDEN](../android/content/ComponentCallbacks2.md), [android.content.ComponentCallbacks2#TRIM_MEMORY_RUNNING_CRITICAL](../android/content/ComponentCallbacks2.md), [android.content.ComponentCallbacks2#TRIM_MEMORY_RUNNING_LOW](../android/content/ComponentCallbacks2.md), or [android.content.ComponentCallbacks2#TRIM_MEMORY_RUNNING_MODERATE](../android/content/ComponentCallbacks2.md) |

### onViewCreated

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onViewCreated(
    view: View!, 
    savedInstanceState: Bundle?
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called immediately after [onCreateView(android.view.LayoutInflater,android.view.ViewGroup,android.os.Bundle)](../android/app/Fragment.md))has returned, but before any saved state has been restored in to the view. This gives subclasses a chance to initialize themselves once they know their view hierarchy has been completely created. The fragment's view hierarchy is not however attached to its parent at this point.

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md)!:The View returned by [onCreateView(android.view.LayoutInflater,android.view.ViewGroup,android.os.Bundle)](../android/app/Fragment.md)). |
| `savedInstanceState` | [Bundle](../android/os/Bundle.md)?:If non-null, this fragment is being re-constructed from a previous saved state as given here. |

### onViewStateRestored

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onViewStateRestored(savedInstanceState: Bundle!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when all saved state has been restored into the view hierarchy of the fragment. This can be used to do initialization based on saved state that you are letting the view hierarchy track itself, such as whether check box widgets are currently checked. This is called after [onActivityCreated(android.os.Bundle)](../android/app/Fragment.md))and before [onStart()](../android/app/Fragment.md)). 
If you override this method you*must*call through to the superclass implementation.

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `savedInstanceState` | [Bundle](../android/os/Bundle.md)!:If the fragment is being re-created from a previous saved state, this is the state. |

### postponeEnterTransition

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun postponeEnterTransition(): Unit
```

**Deprecated:** *Deprecated in Java.*

Postpone the entering Fragment transition until [startPostponedEnterTransition()](../android/app/Fragment.md))or [FragmentManager.executePendingTransactions()](../android/app/FragmentManager.md))has been called.

This method gives the Fragment the ability to delay Fragment animations until all data is loaded. Until then, the added, shown, and attached Fragments will be INVISIBLE and removed, hidden, and detached Fragments won't be have their Views removed. The transaction runs when all postponed added Fragments in the transaction have called [startPostponedEnterTransition()](../android/app/Fragment.md)).

This method should be called before being added to the FragmentTransaction or in [onCreate(android.os.Bundle)](../android/app/Fragment.md)), [onAttach(android.content.Context)](../android/app/Fragment.md)), or [onCreateView(android.view.LayoutInflater,android.view.ViewGroup,android.os.Bundle)](../android/app/Fragment.md))}. [startPostponedEnterTransition()](../android/app/Fragment.md))must be called to allow the Fragment to start the transitions.

When a FragmentTransaction is started that may affect a postponed FragmentTransaction, based on which containers are in their operations, the postponed FragmentTransaction will have its start triggered. The early triggering may result in faulty or nonexistent animations in the postponed transaction. FragmentTransactions that operate only on independent containers will not interfere with each other's postponement.

Calling postponeEnterTransition on Fragments with a null View will not postpone the transition. Likewise, postponement only works if FragmentTransaction optimizations are enabled. 
**See Also**

- [android.app.Activity#postponeEnterTransition()](../android/app/Activity.md))
- [android.app.FragmentTransaction#setReorderingAllowed(boolean)](../android/app/FragmentTransaction.md)) 

### registerForContextMenu

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerForContextMenu(view: View!): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers a context menu to be shown for the given view (multiple views can show the context menu). This method will set the [OnCreateContextMenuListener](../android/view/View.OnCreateContextMenuListener.md) on the view to this fragment, so [onCreateContextMenu(android.view.ContextMenu,android.view.View,android.view.ContextMenu.ContextMenuInfo)](../android/app/Fragment.md))will be called when it is time to show the context menu.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md)!:The view that should show a context menu. |

**See Also**

- [#unregisterForContextMenu(View)](../android/app/Fragment.md)) 

### requestPermissions

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun requestPermissions(
    permissions: Array<String!>, 
    requestCode: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Requests permissions to be granted to this application. These permissions must be requested in your manifest, they should not be granted to your app, and they should have protection level [#PROTECTION_DANGEROUS dangerous](../android/content/pm/PermissionInfo.md), regardless whether they are declared by the platform or a third-party app.

Normal permissions [android.content.pm.PermissionInfo#PROTECTION_NORMAL](../android/content/pm/PermissionInfo.md) are granted at install time if requested in the manifest. Signature permissions [android.content.pm.PermissionInfo#PROTECTION_SIGNATURE](../android/content/pm/PermissionInfo.md) are granted at install time if requested in the manifest and the signature of your app matches the signature of the app declaring the permissions.

Call [shouldShowRequestPermissionRationale(java.lang.String)](../android/app/Fragment.md))before calling this API to check if the system recommends to show a rationale UI before asking for a permission.

If your app does not have the requested permissions the user will be presented with UI for accepting them. After the user has accepted or rejected the requested permissions you will receive a callback on[onRequestPermissionsResult(int,java.lang.String[],int[])](https://developer.android.com/reference/kotlin/android/app/Fragment#onRequestPermissionsResult(kotlin.Int,%20kotlin.Array,%20kotlin.IntArray))reporting whether the permissions were granted or not.

Note that requesting a permission does not guarantee it will be granted and your app should be able to run without having this permission.

This method may start an activity allowing the user to choose which permissions to grant and which to reject. Hence, you should be prepared that your activity may be paused and resumed. Further, granting some permissions may require a restart of you application. In such a case, the system will recreate the activity stack before delivering the result to[onRequestPermissionsResult(int,java.lang.String[],int[])](https://developer.android.com/reference/kotlin/android/app/Fragment#onRequestPermissionsResult(kotlin.Int,%20kotlin.Array,%20kotlin.IntArray)).

When checking whether you have a permission you should use [android.content.Context#checkSelfPermission(String)](../android/content/Context.md)).

Calling this API for permissions already granted to your app would show UI to the user to decide whether the app can still hold these permissions. This can be useful if the way your app uses data guarded by the permissions changes significantly.

You cannot request a permission if your activity sets [noHistory](../android/R.styleable.md) to`true`because in this case the activity would not receive result callbacks including[onRequestPermissionsResult(int,java.lang.String[],int[])](https://developer.android.com/reference/kotlin/android/app/Fragment#onRequestPermissionsResult(kotlin.Int,%20kotlin.Array,%20kotlin.IntArray)).

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `permissions` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:The requested permissions. Must me non-null and not empty. |
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Application specific request code to match with a result reported to[onRequestPermissionsResult(int,java.lang.String[],int[])](https://developer.android.com/reference/kotlin/android/app/Fragment#onRequestPermissionsResult(kotlin.Int,%20kotlin.Array,%20kotlin.IntArray)). Should be \>= 0. |

**See Also**

- [#onRequestPermissionsResult(int, String[], int[])](https://developer.android.com/reference/kotlin/android/app/Fragment#onRequestPermissionsResult(kotlin.Int,%20kotlin.Array,%20kotlin.IntArray))
- [android.content.Context#checkSelfPermission(String)](../android/content/Context.md)) 

### setAllowEnterTransitionOverlap

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAllowEnterTransitionOverlap(allow: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets whether the exit transition and enter transition overlap or not. When true, the enter transition will start as soon as possible. When false, the enter transition will wait until the exit transition completes before starting.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `allow` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true to start the enter transition when possible or false to wait until the exiting transition completes. |

### setAllowReturnTransitionOverlap

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAllowReturnTransitionOverlap(allow: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets whether the return transition and reenter transition overlap or not. When true, the reenter transition will start as soon as possible. When false, the reenter transition will wait until the return transition completes before starting.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `allow` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true to start the reenter transition when possible or false to wait until the return transition completes. |

### setArguments

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setArguments(args: Bundle!): Unit
```

**Deprecated:** *Deprecated in Java.*

Supply the construction arguments for this fragment. The arguments supplied here will be retained across fragment destroy and creation.

This method cannot be called if the fragment is added to a FragmentManager and if [isStateSaved()](../android/app/Fragment.md))would return true. Prior to [Build.VERSION_CODES.O](../android/os/Build.VERSION_CODES.md), this method may only be called if the fragment has not yet been added to a FragmentManager. 

### setEnterSharedElementCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEnterSharedElementCallback(callback: SharedElementCallback!): Unit
```

**Deprecated:** *Deprecated in Java.*

When custom transitions are used with Fragments, the enter transition callback is called when this Fragment is attached or detached when not popping the back stack.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [SharedElementCallback](../android/app/SharedElementCallback.md)!:Used to manipulate the shared element transitions on this Fragment when added not as a pop from the back stack. |

### setEnterTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEnterTransition(transition: Transition!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the Transition that will be used to move Views into the initial scene. The entering Views will be those that are regular Views or ViewGroups that have [ViewGroup.isTransitionGroup](../android/view/ViewGroup.md))return true. Typical Transitions will extend [android.transition.Visibility](../android/transition/Visibility.md) as entering is governed by changing visibility from [View.INVISIBLE](../android/view/View.md) to [View.VISIBLE](../android/view/View.md). If`transition`is null, entering Views will remain unaffected.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transition` | [Transition](../android/transition/Transition.md)!:The Transition to use to move Views into the initial Scene. |

### setExitSharedElementCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setExitSharedElementCallback(callback: SharedElementCallback!): Unit
```

**Deprecated:** *Deprecated in Java.*

When custom transitions are used with Fragments, the exit transition callback is called when this Fragment is attached or detached when popping the back stack.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [SharedElementCallback](../android/app/SharedElementCallback.md)!:Used to manipulate the shared element transitions on this Fragment when added as a pop from the back stack. |

### setExitTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setExitTransition(transition: Transition!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the Transition that will be used to move Views out of the scene when the fragment is removed, hidden, or detached when not popping the back stack. The exiting Views will be those that are regular Views or ViewGroups that have [ViewGroup.isTransitionGroup](../android/view/ViewGroup.md))return true. Typical Transitions will extend [android.transition.Visibility](../android/transition/Visibility.md) as exiting is governed by changing visibility from [View.VISIBLE](../android/view/View.md) to [View.INVISIBLE](../android/view/View.md). If transition is null, the views will remain unaffected.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transition` | [Transition](../android/transition/Transition.md)!:The Transition to use to move Views out of the Scene when the Fragment is being closed not due to popping the back stack. |

### setHasOptionsMenu

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setHasOptionsMenu(hasMenu: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Report that this fragment would like to participate in populating the options menu by receiving a call to [onCreateOptionsMenu](../android/app/Fragment.md))and related methods.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `hasMenu` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true, the fragment has menu items to contribute. |

### setInitialSavedState

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInitialSavedState(state: Fragment.SavedState!): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the initial saved state that this Fragment should restore itself from when first being constructed, as returned by [FragmentManager.saveFragmentInstanceState](../android/app/FragmentManager.md)).

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Fragment.SavedState](../android/app/Fragment.SavedState.md)!:The state the fragment should be restored from. |

### setMenuVisibility

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMenuVisibility(menuVisible: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Set a hint for whether this fragment's menu should be visible. This is useful if you know that a fragment has been placed in your view hierarchy so that the user can not currently seen it, so any menu items it has should also not be shown.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `menuVisible` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):The default is true, meaning the fragment's menu will be shown as usual. If false, the user will not see the menu. |

### setReenterTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setReenterTransition(transition: Transition!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the Transition that will be used to move Views in to the scene when returning due to popping a back stack. The entering Views will be those that are regular Views or ViewGroups that have [ViewGroup.isTransitionGroup](../android/view/ViewGroup.md))return true. Typical Transitions will extend [android.transition.Visibility](../android/transition/Visibility.md) as exiting is governed by changing visibility from [View.VISIBLE](../android/view/View.md) to [View.INVISIBLE](../android/view/View.md). If transition is null, the views will remain unaffected. If nothing is set, the default will be to use the same transition as [setExitTransition(android.transition.Transition)](../android/app/Fragment.md)).

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transition` | [Transition](../android/transition/Transition.md)!:The Transition to use to move Views into the scene when reentering from a previously-started Activity. |

### setRetainInstance

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRetainInstance(retain: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Control whether a fragment instance is retained across Activity re-creation (such as from a configuration change). This can only be used with fragments not in the back stack. If set, the fragment lifecycle will be slightly different when an activity is recreated:

- [onDestroy()](../android/app/Fragment.md))will not be called (but [onDetach()](../android/app/Fragment.md))still will be, because the fragment is being detached from its current activity).
- [onCreate(android.os.Bundle)](../android/app/Fragment.md))will not be called since the fragment is not being re-created.
- [onAttach(android.app.Activity)](../android/app/Fragment.md))and [onActivityCreated(android.os.Bundle)](../android/app/Fragment.md))**will**still be called.

<br />

### setReturnTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setReturnTransition(transition: Transition!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the Transition that will be used to move Views out of the scene when the Fragment is preparing to be removed, hidden, or detached because of popping the back stack. The exiting Views will be those that are regular Views or ViewGroups that have [ViewGroup.isTransitionGroup](../android/view/ViewGroup.md))return true. Typical Transitions will extend [android.transition.Visibility](../android/transition/Visibility.md) as entering is governed by changing visibility from [View.VISIBLE](../android/view/View.md) to [View.INVISIBLE](../android/view/View.md). If`transition`is null, entering Views will remain unaffected. If nothing is set, the default will be to use the same value as set in [setEnterTransition(android.transition.Transition)](../android/app/Fragment.md)).

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transition` | [Transition](../android/transition/Transition.md)!:The Transition to use to move Views out of the Scene when the Fragment is preparing to close. |

### setSharedElementEnterTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSharedElementEnterTransition(transition: Transition!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the Transition that will be used for shared elements transferred into the content Scene. Typical Transitions will affect size and location, such as [android.transition.ChangeBounds](../android/transition/ChangeBounds.md). A null value will cause transferred shared elements to blink to the final position.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transition` | [Transition](../android/transition/Transition.md)!:The Transition to use for shared elements transferred into the content Scene. |

### setSharedElementReturnTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSharedElementReturnTransition(transition: Transition!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the Transition that will be used for shared elements transferred back during a pop of the back stack. This Transition acts in the leaving Fragment. Typical Transitions will affect size and location, such as [android.transition.ChangeBounds](../android/transition/ChangeBounds.md). A null value will cause transferred shared elements to blink to the final position. If no value is set, the default will be to use the same value as [setSharedElementEnterTransition(android.transition.Transition)](../android/app/Fragment.md)).

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transition` | [Transition](../android/transition/Transition.md)!:The Transition to use for shared elements transferred out of the content Scene. |

### setTargetFragment

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTargetFragment(
    fragment: Fragment!, 
    requestCode: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Optional target for this fragment. This may be used, for example, if this fragment is being started by another, and when done wants to give a result back to the first. The target set here is retained across instances via [FragmentManager.putFragment()](../android/app/FragmentManager.md)).

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fragment` | [Fragment](../android/app/Fragment.md)!:The fragment that is the target of this one. |
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Optional request code, for convenience if you are going to call back with [onActivityResult(int,int,android.content.Intent)](../android/app/Fragment.md)). |

### setUserVisibleHint

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setUserVisibleHint(isVisibleToUser: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Set a hint to the system about whether this fragment's UI is currently visible to the user. This hint defaults to true and is persistent across fragment instance state save and restore.

An app may set this to false to indicate that the fragment's UI is scrolled out of visibility or is otherwise not directly visible to the user. This may be used by the system to prioritize operations such as fragment lifecycle updates or loader ordering behavior.

**Note:**This method may be called outside of the fragment lifecycle and thus has no ordering guarantees with regard to fragment lifecycle method calls.

**Note:** Prior to Android N there was a platform bug that could cause`setUserVisibleHint`to bring a fragment up to the started state before its`FragmentTransaction`had been committed. As some apps relied on this behavior, it is preserved for apps that declare a`targetSdkVersion`of 23 or lower.

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `isVisibleToUser` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if this fragment's UI is currently visible to the user (default), false if it is not. |

### shouldShowRequestPermissionRationale

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shouldShowRequestPermissionRationale(permission: String): Boolean
```

**Deprecated:** *Deprecated in Java.*

Gets whether you should show UI with rationale before requesting a permission.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `permission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):A permission your app wants to request. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether you should show permission rationale UI. |

**See Also**

- [android.content.Context#checkSelfPermission(String)](../android/content/Context.md))
- [#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Fragment#requestPermissions(kotlin.Array,%20kotlin.Int))
- [#onRequestPermissionsResult(int, String[], int[])](https://developer.android.com/reference/kotlin/android/app/Fragment#onRequestPermissionsResult(kotlin.Int,%20kotlin.Array,%20kotlin.IntArray)) 

### startActivity

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startActivity(intent: Intent!): Unit
```

**Deprecated:** *Deprecated in Java.*

Call android.app.Activity#startActivity(android.content.Intent) from the fragment's containing Activity.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](../android/content/Intent.md)!:The intent to start. |

### startActivity

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startActivity(
    intent: Intent!, 
    options: Bundle!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Call android.app.Activity#startActivity(android.content.Intent,android.os.Bundle) from the fragment's containing Activity.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](../android/content/Intent.md)!:The intent to start. |
| `options` | [Bundle](../android/os/Bundle.md)!:Additional options for how the Activity should be started. See [android.content.Context#startActivity(Intent, Bundle)](../android/content/Context.md))Context.startActivity(Intent, Bundle)} for more details. |

### startActivityForResult

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startActivityForResult(
    intent: Intent!, 
    requestCode: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Call [Activity.startActivityForResult(Intent, int)](../android/app/Activity.md))from the fragment's containing Activity. 

### startActivityForResult

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startActivityForResult(
    intent: Intent!, 
    requestCode: Int, 
    options: Bundle!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Call [Activity.startActivityForResult(Intent, int, Bundle)](../android/app/Activity.md))from the fragment's containing Activity. 

### startIntentSenderForResult

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startIntentSenderForResult(
    intent: IntentSender!, 
    requestCode: Int, 
    fillInIntent: Intent?, 
    flagsMask: Int, 
    flagsValues: Int, 
    extraFlags: Int, 
    options: Bundle!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Call [Activity.startIntentSenderForResult(IntentSender, int, Intent, int, int, int,](../android/app/Activity.md))from the fragment's containing Activity.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------|
| `fillInIntent` | [Intent](../android/content/Intent.md)?:This value may be`null`. |

### startPostponedEnterTransition

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startPostponedEnterTransition(): Unit
```

**Deprecated:** *Deprecated in Java.*

Begin postponed transitions after [postponeEnterTransition()](../android/app/Fragment.md))was called. If postponeEnterTransition() was called, you must call startPostponedEnterTransition() or [FragmentManager.executePendingTransactions()](../android/app/FragmentManager.md))to complete the FragmentTransaction. If postponement was interrupted with [FragmentManager.executePendingTransactions()](../android/app/FragmentManager.md)), before`startPostponedEnterTransition()`, animations may not run or may execute improperly. 
**See Also**

- [android.app.Activity#startPostponedEnterTransition()](../android/app/Activity.md)) 

### toString

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### unregisterForContextMenu

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterForContextMenu(view: View!): Unit
```

**Deprecated:** *Deprecated in Java.*

Prevents a context menu to be shown for the given view. This method will remove the [OnCreateContextMenuListener](../android/view/View.OnCreateContextMenuListener.md) on the view.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md)!:The view that should stop showing a context menu. |

**See Also**

- [#registerForContextMenu(View)](../android/app/Fragment.md))
