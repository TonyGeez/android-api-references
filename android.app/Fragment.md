# Fragment

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Fragment

Kotlin| [Java](https://developer.android.com/reference/android/app/Fragment "View this page in Java") 

```
open class Fragment : ComponentCallbacks2, View.OnCreateContextMenuListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment#) |

| Known Direct Subclasses [DialogFragment](https://developer.android.com/reference/kotlin/android/app/DialogFragment), [ListFragment](https://developer.android.com/reference/kotlin/android/app/ListFragment), [PreferenceFragment](https://developer.android.com/reference/kotlin/android/preference/PreferenceFragment.html#), [WebViewFragment](https://developer.android.com/reference/kotlin/android/webkit/WebViewFragment.html#) |------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DialogFragment](https://developer.android.com/reference/kotlin/android/app/DialogFragment) | A fragment that displays a dialog window, floating on top of its activity's window. | | [ListFragment](https://developer.android.com/reference/kotlin/android/app/ListFragment) | A fragment that displays a list of items by binding to a data source such as an array or Cursor, and exposes event handlers when the user selects an item. | | [PreferenceFragment](https://developer.android.com/reference/kotlin/android/preference/PreferenceFragment.html#) | Shows a hierarchy of [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference.html#) objects as lists. | | [WebViewFragment](https://developer.android.com/reference/kotlin/android/webkit/WebViewFragment.html#) | A fragment that displays a WebView. | |

| **This class was deprecated in API level 28.**
|
| Use the [Jetpack Fragment Library](https://developer.android.com/jetpack) androidx.fragment.app.Fragment for consistent behavior across all devices and access to [Lifecycle](https://developer.android.com/topic/libraries/architecture/lifecycle.html).

A Fragment is a piece of an application's user interface or behavior that can be placed in an [Activity](https://developer.android.com/reference/kotlin/android/app/Activity). Interaction with fragments is done through [FragmentManager](https://developer.android.com/reference/kotlin/android/app/FragmentManager), which can be obtained via [Activity.getFragmentManager()](https://developer.android.com/reference/kotlin/android/app/Activity#getFragmentManager())and [Fragment.getFragmentManager()](https://developer.android.com/reference/kotlin/android/app/Fragment#getFragmentManager()).

The Fragment class can be used many ways to achieve a wide variety of results. In its core, it represents a particular operation or interface that is running within a larger [Activity](https://developer.android.com/reference/kotlin/android/app/Activity). A Fragment is closely tied to the Activity it is in, and can not be used apart from one. Though Fragment defines its own lifecycle, that lifecycle is dependent on its activity: if the activity is stopped, no fragments inside of it can be started; when the activity is destroyed, all fragments will be destroyed.

All subclasses of Fragment must include a public no-argument constructor. The framework will often re-instantiate a fragment class when needed, in particular during state restore, and needs to be able to find this constructor to instantiate it. If the no-argument constructor is not available, a runtime exception will occur in some cases during state restore.

Topics covered here:

1. [Older Platforms](https://developer.android.com/reference/kotlin/android/app/Fragment#OlderPlatforms)
2. [Lifecycle](https://developer.android.com/reference/kotlin/android/app/Fragment#Lifecycle)
3. [Layout](https://developer.android.com/reference/kotlin/android/app/Fragment#Layout)
4. [Back Stack](https://developer.android.com/reference/kotlin/android/app/Fragment#BackStack)

| ### Developer Guides
|
| For more information about using fragments, read the [Fragments](https://developer.android.com/guide/components/fragments.html) developer guide.

### Older Platforms

While the Fragment API was introduced in [android.os.Build.VERSION_CODES#HONEYCOMB](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int), a version of the API at is also available for use on older platforms through androidx.fragment.app.FragmentActivity. See the blog post [Fragments For All](http://android-developers.blogspot.com/2011/03/fragments-for-all.html) for more details.

### Lifecycle

Though a Fragment's lifecycle is tied to its owning activity, it has its own wrinkle on the standard activity lifecycle. It includes basic activity lifecycle methods such as [onResume](https://developer.android.com/reference/kotlin/android/app/Fragment#onResume()), but also important are methods related to interactions with the activity and UI generation.

The core series of lifecycle methods that are called to bring a fragment up to resumed state (interacting with the user) are:

1. #onAttach called once the fragment is associated with its activity.
2. [onCreate](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreate(android.os.Bundle))called to do initial creation of the fragment.
3. [onCreateView](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle))creates and returns the view hierarchy associated with the fragment.
4. [onActivityCreated](https://developer.android.com/reference/kotlin/android/app/Fragment#onActivityCreated(android.os.Bundle))tells the fragment that its activity has completed its own android.app.Activity#onCreate.
5. [onViewStateRestored](https://developer.android.com/reference/kotlin/android/app/Fragment#onViewStateRestored(android.os.Bundle))tells the fragment that all of the saved state of its view hierarchy has been restored.
6. [onStart](https://developer.android.com/reference/kotlin/android/app/Fragment#onStart())makes the fragment visible to the user (based on its containing activity being started).
7. [onResume](https://developer.android.com/reference/kotlin/android/app/Fragment#onResume())makes the fragment begin interacting with the user (based on its containing activity being resumed).

As a fragment is no longer being used, it goes through a reverse series of callbacks:

1. [onPause](https://developer.android.com/reference/kotlin/android/app/Fragment#onPause())fragment is no longer interacting with the user either because its activity is being paused or a fragment operation is modifying it in the activity.
2. [onStop](https://developer.android.com/reference/kotlin/android/app/Fragment#onStop())fragment is no longer visible to the user either because its activity is being stopped or a fragment operation is modifying it in the activity.
3. [onDestroyView](https://developer.android.com/reference/kotlin/android/app/Fragment#onDestroyView())allows the fragment to clean up resources associated with its View.
4. [onDestroy](https://developer.android.com/reference/kotlin/android/app/Fragment#onDestroy())called to do final cleanup of the fragment's state.
5. [onDetach](https://developer.android.com/reference/kotlin/android/app/Fragment#onDetach())called immediately prior to the fragment no longer being associated with its activity.

### Layout

Fragments can be used as part of your application's layout, allowing you to better modularize your code and more easily adjust your user interface to the screen it is running on. As an example, we can look at a simple program consisting of a list of items, and display of the details of each item.

An activity's layout XML can include`<fragment>`tags to embed fragment instances inside of the layout. For example, here is a simple layout that embeds one fragment:

The layout is installed in the activity in the normal way:

The titles fragment, showing a list of titles, is fairly simple, relying on [ListFragment](https://developer.android.com/reference/kotlin/android/app/ListFragment) for most of its work. Note the implementation of clicking an item: depending on the current activity's layout, it can either create and display a new fragment to show the details in-place (more about this later), or start a new activity to show the details.

The details fragment showing the contents of a selected item just displays a string of text based on an index of a string array built in to the app:

In this case when the user clicks on a title, there is no details container in the current activity, so the titles fragment's click code will launch a new activity to display the details fragment:

However the screen may be large enough to show both the list of titles and details about the currently selected title. To use such a layout on a landscape screen, this alternative layout can be placed under layout-land:

Note how the prior code will adjust to this alternative UI flow: the titles fragment will now embed the details fragment inside of this activity, and the details activity will finish itself if it is running in a configuration where the details can be shown in-place.

When a configuration change causes the activity hosting these fragments to restart, its new instance may use a different layout that doesn't include the same fragments as the previous layout. In this case all of the previous fragments will still be instantiated and running in the new instance. However, any that are no longer associated with a \<fragment\> tag in the view hierarchy will not have their content view created and will return false from [isInLayout](https://developer.android.com/reference/kotlin/android/app/Fragment#isInLayout()). (The code here also shows how you can determine if a fragment placed in a container is no longer running in a layout with that container and avoid creating its view hierarchy in that case.)

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

Fragments appearing or disappearing do not generate system events for accessibility, so set a title on your fragments with [View.setAccessibilityPaneTitle(CharSequence)](https://developer.android.com/reference/kotlin/android/view/View.html#setAccessibilityPaneTitle(kotlin.CharSequence))to notify accessibility users of these UI transitions.

## Summary

| Nested classes ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [InstantiationException](https://developer.android.com/reference/kotlin/android/app/Fragment.InstantiationException) Thrown by [Fragment.instantiate(Context, String, Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#instantiate(android.content.Context,%20kotlin.String,%20android.os.Bundle))when there is an instantiation failure. |
| open | [SavedState](https://developer.android.com/reference/kotlin/android/app/Fragment.SavedState) State information that has been retrieved from a fragment instance through [FragmentManager.saveFragmentInstanceState](https://developer.android.com/reference/kotlin/android/app/FragmentManager#saveFragmentInstanceState(android.app.Fragment)). |

| Inherited constants ||
|---|---|
| From class [ComponentCallbacks2](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_BACKGROUND](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_BACKGROUND:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)): the process has gone on to the LRU list. This is a good opportunity to clean up resources that can efficiently and quickly be re-built if the user returns to the app. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_COMPLETE](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_COMPLETE:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)): the process is nearing the end of the background LRU list, and if more memory isn't found soon it will be killed. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_MODERATE](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_MODERATE:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)): the process is around the middle of the background LRU list; freeing memory can help the system keep other processes running later in the list for better overall performance. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_RUNNING_CRITICAL](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_CRITICAL:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)): the process is not an expendable background process, but the device is running extremely low on memory and is about to not be able to keep any background processes running. Your running process should free up as many non-critical resources as it can to allow that memory to be used elsewhere. The next thing that will happen after this is [onLowMemory()](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onLowMemory())called to report that nothing at all can be kept in the background, a situation that can start to notably impact the user. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_RUNNING_LOW](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_LOW:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)): the process is not an expendable background process, but the device is running low on memory. Your running process should free up unneeded resources to allow that memory to be used elsewhere. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_RUNNING_MODERATE](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_MODERATE:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)): the process is not an expendable background process, but the device is running moderately low on memory. Your running process may want to release some unneeded resources for use elsewhere. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRIM_MEMORY_UI_HIDDEN](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_UI_HIDDEN:kotlin.Int) <br /> Level for [onTrimMemory(int)](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#onTrimMemory(kotlin.Int)): the process had been showing a user interface, and is no longer doing so. Large allocations with the UI should be released at this point to allow memory to be better managed. <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------|---|
| [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment#Fragment())`()` Default constructor. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](https://developer.android.com/reference/kotlin/android/app/Fragment#dump(kotlin.String,%20java.io.FileDescriptor,%20java.io.PrintWriter,%20kotlin.Array))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!`, `writer:` ` [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)!`, `args:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Print the Fragments's state into the given stream. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/app/Fragment#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Subclasses can not override equals(). |
| [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)! | [getActivity](https://developer.android.com/reference/kotlin/android/app/Fragment#getActivity())`()` Return the Activity this fragment is currently associated with. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAllowEnterTransitionOverlap](https://developer.android.com/reference/kotlin/android/app/Fragment#getAllowEnterTransitionOverlap())`()` Returns whether the exit transition and enter transition overlap or not. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAllowReturnTransitionOverlap](https://developer.android.com/reference/kotlin/android/app/Fragment#getAllowReturnTransitionOverlap())`()` Returns whether the return transition and reenter transition overlap or not. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [getArguments](https://developer.android.com/reference/kotlin/android/app/Fragment#getArguments())`()` Return the arguments supplied to [setArguments](https://developer.android.com/reference/kotlin/android/app/Fragment#setArguments(android.os.Bundle)), if any. |
| [FragmentManager](https://developer.android.com/reference/kotlin/android/app/FragmentManager)! | [getChildFragmentManager](https://developer.android.com/reference/kotlin/android/app/Fragment#getChildFragmentManager())`()` Return a private FragmentManager for placing and managing Fragments inside of this Fragment. |
| open [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)! | [getContext](https://developer.android.com/reference/kotlin/android/app/Fragment#getContext())`()` Return the [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) this fragment is currently associated with. |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)! | [getEnterTransition](https://developer.android.com/reference/kotlin/android/app/Fragment#getEnterTransition())`()` Returns the Transition that will be used to move Views into the initial scene. |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)! | [getExitTransition](https://developer.android.com/reference/kotlin/android/app/Fragment#getExitTransition())`()` Returns the Transition that will be used to move Views out of the scene when the fragment is removed, hidden, or detached when not popping the back stack. |
| [FragmentManager](https://developer.android.com/reference/kotlin/android/app/FragmentManager)! | [getFragmentManager](https://developer.android.com/reference/kotlin/android/app/Fragment#getFragmentManager())`()` Return the FragmentManager for interacting with fragments associated with this fragment's activity. |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | [getHost](https://developer.android.com/reference/kotlin/android/app/Fragment#getHost())`()` Return the host object of this fragment. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](https://developer.android.com/reference/kotlin/android/app/Fragment#getId())`()` Return the identifier this fragment is known by. |
| [LayoutInflater](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#)! | [getLayoutInflater](https://developer.android.com/reference/kotlin/android/app/Fragment#getLayoutInflater())`()` Returns the cached LayoutInflater used to inflate Views of this Fragment. |
| open [LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager)! | [getLoaderManager](https://developer.android.com/reference/kotlin/android/app/Fragment#getLoaderManager())`()` Return the LoaderManager for this fragment, creating it if needed. |
| [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment#)! | [getParentFragment](https://developer.android.com/reference/kotlin/android/app/Fragment#getParentFragment())`()` Returns the parent Fragment containing this Fragment. |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)! | [getReenterTransition](https://developer.android.com/reference/kotlin/android/app/Fragment#getReenterTransition())`()` Returns the Transition that will be used to move Views in to the scene when returning due to popping a back stack. |
| [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)! | [getResources](https://developer.android.com/reference/kotlin/android/app/Fragment#getResources())`()` Return`getActivity().getResources()`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getRetainInstance](https://developer.android.com/reference/kotlin/android/app/Fragment#getRetainInstance())`()` <br /> |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)! | [getReturnTransition](https://developer.android.com/reference/kotlin/android/app/Fragment#getReturnTransition())`()` Returns the Transition that will be used to move Views out of the scene when the Fragment is preparing to be removed, hidden, or detached because of popping the back stack. |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)! | [getSharedElementEnterTransition](https://developer.android.com/reference/kotlin/android/app/Fragment#getSharedElementEnterTransition())`()` Returns the Transition that will be used for shared elements transferred into the content Scene. |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)! | [getSharedElementReturnTransition](https://developer.android.com/reference/kotlin/android/app/Fragment#getSharedElementReturnTransition())`()` Return the Transition that will be used for shared elements transferred back during a pop of the back stack. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](https://developer.android.com/reference/kotlin/android/app/Fragment#getString(kotlin.Int))`(`resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return a localized string from the application's package's default string table. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](https://developer.android.com/reference/kotlin/android/app/Fragment#getString(kotlin.Int,%20kotlin.Any))`(`resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `vararg` `formatArgs:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Return a localized formatted string from the application's package's default string table, substituting the format arguments as defined in [java.util.Formatter](https://developer.android.com/reference/kotlin/java/util/Formatter.html#) and java. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTag](https://developer.android.com/reference/kotlin/android/app/Fragment#getTag())`()` Get the tag name of the fragment, if specified. |
| [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment#)! | [getTargetFragment](https://developer.android.com/reference/kotlin/android/app/Fragment#getTargetFragment())`()` Return the target fragment set by [setTargetFragment](https://developer.android.com/reference/kotlin/android/app/Fragment#setTargetFragment(android.app.Fragment,%20kotlin.Int)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTargetRequestCode](https://developer.android.com/reference/kotlin/android/app/Fragment#getTargetRequestCode())`()` Return the target request code set by [setTargetFragment](https://developer.android.com/reference/kotlin/android/app/Fragment#setTargetFragment(android.app.Fragment,%20kotlin.Int)). |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getText](https://developer.android.com/reference/kotlin/android/app/Fragment#getText(kotlin.Int))`(`resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return a localized, styled CharSequence from the application's package's default string table. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getUserVisibleHint](https://developer.android.com/reference/kotlin/android/app/Fragment#getUserVisibleHint())`()` <br /> |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)? | [getView](https://developer.android.com/reference/kotlin/android/app/Fragment#getView())`()` Get the root view for the fragment's layout (the one returned by [onCreateView](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle))), if provided. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/app/Fragment#hashCode())`()` Subclasses can not override hashCode(). |
| openstatic [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment#)! | [instantiate](https://developer.android.com/reference/kotlin/android/app/Fragment#instantiate(android.content.Context,%20kotlin.String))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `fname:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Like [instantiate(android.content.Context,java.lang.String,android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#instantiate(android.content.Context,%20kotlin.String,%20android.os.Bundle))but with a null argument Bundle. |
| openstatic [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment#)! | [instantiate](https://developer.android.com/reference/kotlin/android/app/Fragment#instantiate(android.content.Context,%20kotlin.String,%20android.os.Bundle))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `fname:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `args:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` Create a new instance of a Fragment with the given class name. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAdded](https://developer.android.com/reference/kotlin/android/app/Fragment#isAdded())`()` Return true if the fragment is currently added to its activity. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDetached](https://developer.android.com/reference/kotlin/android/app/Fragment#isDetached())`()` Return true if the fragment has been explicitly detached from the UI. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHidden](https://developer.android.com/reference/kotlin/android/app/Fragment#isHidden())`()` Return true if the fragment has been hidden. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInLayout](https://developer.android.com/reference/kotlin/android/app/Fragment#isInLayout())`()` Return true if the layout is included as part of an activity view hierarchy via the \<fragment\> tag. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRemoving](https://developer.android.com/reference/kotlin/android/app/Fragment#isRemoving())`()` Return true if this fragment is currently being removed from its activity. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isResumed](https://developer.android.com/reference/kotlin/android/app/Fragment#isResumed())`()` Return true if the fragment is in the resumed state. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStateSaved](https://developer.android.com/reference/kotlin/android/app/Fragment#isStateSaved())`()` Returns true if this fragment is added and its state has already been saved by its host. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVisible](https://developer.android.com/reference/kotlin/android/app/Fragment#isVisible())`()` Return true if the fragment is currently visible to the user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityCreated](https://developer.android.com/reference/kotlin/android/app/Fragment#onActivityCreated(android.os.Bundle))`(`savedInstanceState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` Called when the fragment's activity has been created and this fragment's view hierarchy instantiated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityResult](https://developer.android.com/reference/kotlin/android/app/Fragment#onActivityResult(kotlin.Int,%20kotlin.Int,%20android.content.Intent))`(`requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` Receive the result from a previous call to [startActivityForResult(android.content.Intent,int)](https://developer.android.com/reference/kotlin/android/app/Fragment#startActivityForResult(android.content.Intent,%20kotlin.Int)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttach](https://developer.android.com/reference/kotlin/android/app/Fragment#onAttach(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)!`)` <br /> If you override this method you*must*call through to the superclass implementation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttach](https://developer.android.com/reference/kotlin/android/app/Fragment#onAttach(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Called when a fragment is first attached to its context. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttachFragment](https://developer.android.com/reference/kotlin/android/app/Fragment#onAttachFragment(android.app.Fragment))`(`childFragment:` ` [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment#)!`)` Called when a fragment is attached as a child of this fragment. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConfigurationChanged](https://developer.android.com/reference/kotlin/android/app/Fragment#onConfigurationChanged(android.content.res.Configuration))`(`newConfig:` ` [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)`)` Called by the system when the device configuration changes while your component is running. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onContextItemSelected](https://developer.android.com/reference/kotlin/android/app/Fragment#onContextItemSelected(android.view.MenuItem))`(`item:` ` [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem.html#)!`)` This hook is called whenever an item in a context menu is selected. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCreate](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreate(android.os.Bundle))`(`savedInstanceState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` Called to do initial creation of a fragment. |
| open [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator.html#)! | [onCreateAnimator](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateAnimator(kotlin.Int,%20kotlin.Boolean,%20kotlin.Int))`(`transit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `enter:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `nextAnim:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when a fragment loads an animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCreateContextMenu](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateContextMenu(android.view.ContextMenu,%20android.view.View,%20android.view.ContextMenu.ContextMenuInfo))`(`menu:` ` [ContextMenu](https://developer.android.com/reference/kotlin/android/view/ContextMenu.html#)!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `menuInfo:` ` [ContextMenu.ContextMenuInfo](https://developer.android.com/reference/kotlin/android/view/ContextMenu.ContextMenuInfo.html#)!`)` Called when a context menu for the`view`is about to be shown. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCreateOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateOptionsMenu(android.view.Menu,%20android.view.MenuInflater))`(`menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)!`, `inflater:` ` [MenuInflater](https://developer.android.com/reference/kotlin/android/view/MenuInflater.html#)!`)` Initialize the contents of the Activity's standard options menu. |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)? | [onCreateView](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle))`(`inflater:` ` [LayoutInflater](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#)!`, `container:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)?`, `savedInstanceState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Called to have the fragment instantiate its user interface view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDestroy](https://developer.android.com/reference/kotlin/android/app/Fragment#onDestroy())`()` Called when the fragment is no longer in use. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDestroyOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Fragment#onDestroyOptionsMenu())`()` Called when this fragment's option menu items are no longer being included in the overall options menu. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDestroyView](https://developer.android.com/reference/kotlin/android/app/Fragment#onDestroyView())`()` Called when the view previously created by [onCreateView](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle))has been detached from the fragment. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDetach](https://developer.android.com/reference/kotlin/android/app/Fragment#onDetach())`()` Called when the fragment is no longer attached to its activity. |
| open [LayoutInflater](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#)! | [onGetLayoutInflater](https://developer.android.com/reference/kotlin/android/app/Fragment#onGetLayoutInflater(android.os.Bundle))`(`savedInstanceState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Returns the LayoutInflater used to inflate Views of this Fragment. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onHiddenChanged](https://developer.android.com/reference/kotlin/android/app/Fragment#onHiddenChanged(kotlin.Boolean))`(`hidden:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the hidden state (as returned by [isHidden()](https://developer.android.com/reference/kotlin/android/app/Fragment#isHidden())of the fragment has changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInflate](https://developer.android.com/reference/kotlin/android/app/Fragment#onInflate(android.app.Activity,%20android.util.AttributeSet,%20android.os.Bundle))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)!`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`, `savedInstanceState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` <br /> If you override this method you*must*call through to the superclass implementation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInflate](https://developer.android.com/reference/kotlin/android/app/Fragment#onInflate(android.content.Context,%20android.util.AttributeSet,%20android.os.Bundle))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`, `savedInstanceState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Called when a fragment is being created as part of a view layout inflation, typically from setting the content view of an activity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInflate](https://developer.android.com/reference/kotlin/android/app/Fragment#onInflate(android.util.AttributeSet,%20android.os.Bundle))`(`attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`, `savedInstanceState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` <br /> If you override this method you*must*call through to the superclass implementation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLowMemory](https://developer.android.com/reference/kotlin/android/app/Fragment#onLowMemory())`()` This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMultiWindowModeChanged](https://developer.android.com/reference/kotlin/android/app/Fragment#onMultiWindowModeChanged(kotlin.Boolean))`(`isInMultiWindowMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the Fragment's activity changes from fullscreen mode to multi-window mode and visa-versa. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMultiWindowModeChanged](https://developer.android.com/reference/kotlin/android/app/Fragment#onMultiWindowModeChanged(kotlin.Boolean,%20android.content.res.Configuration))`(`isInMultiWindowMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `newConfig:` ` [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)!`)` Called when the Fragment's activity changes from fullscreen mode to multi-window mode and visa-versa. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onOptionsItemSelected](https://developer.android.com/reference/kotlin/android/app/Fragment#onOptionsItemSelected(android.view.MenuItem))`(`item:` ` [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem.html#)!`)` This hook is called whenever an item in your options menu is selected. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onOptionsMenuClosed](https://developer.android.com/reference/kotlin/android/app/Fragment#onOptionsMenuClosed(android.view.Menu))`(`menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)!`)` This hook is called whenever the options menu is being closed (either by the user canceling the menu with the back/menu button, or when an item is selected). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPause](https://developer.android.com/reference/kotlin/android/app/Fragment#onPause())`()` Called when the Fragment is no longer resumed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPictureInPictureModeChanged](https://developer.android.com/reference/kotlin/android/app/Fragment#onPictureInPictureModeChanged(kotlin.Boolean))`(`isInPictureInPictureMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called by the system when the activity changes to and from picture-in-picture mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPictureInPictureModeChanged](https://developer.android.com/reference/kotlin/android/app/Fragment#onPictureInPictureModeChanged(kotlin.Boolean,%20android.content.res.Configuration))`(`isInPictureInPictureMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `newConfig:` ` [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)!`)` Called by the system when the activity changes to and from picture-in-picture mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPrepareOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Fragment#onPrepareOptionsMenu(android.view.Menu))`(`menu:` ` [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)!`)` Prepare the Screen's standard options menu to be displayed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRequestPermissionsResult](https://developer.android.com/reference/kotlin/android/app/Fragment#onRequestPermissionsResult(kotlin.Int,%20kotlin.Array,%20kotlin.IntArray))`(`requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `permissions:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`, `grantResults:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`)` Callback for the result from requesting permissions. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResume](https://developer.android.com/reference/kotlin/android/app/Fragment#onResume())`()` Called when the fragment is visible to the user and actively running. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSaveInstanceState](https://developer.android.com/reference/kotlin/android/app/Fragment#onSaveInstanceState(android.os.Bundle))`(`outState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Called to ask the fragment to save its current dynamic state, so it can later be reconstructed in a new instance of its process is restarted. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStart](https://developer.android.com/reference/kotlin/android/app/Fragment#onStart())`()` Called when the Fragment is visible to the user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStop](https://developer.android.com/reference/kotlin/android/app/Fragment#onStop())`()` Called when the Fragment is no longer started. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTrimMemory](https://developer.android.com/reference/kotlin/android/app/Fragment#onTrimMemory(kotlin.Int))`(`level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the operating system has determined that it is a good time for a process to trim unneeded memory from its process. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onViewCreated](https://developer.android.com/reference/kotlin/android/app/Fragment#onViewCreated(android.view.View,%20android.os.Bundle))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `savedInstanceState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` Called immediately after [onCreateView(android.view.LayoutInflater,android.view.ViewGroup,android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle))has returned, but before any saved state has been restored in to the view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onViewStateRestored](https://developer.android.com/reference/kotlin/android/app/Fragment#onViewStateRestored(android.os.Bundle))`(`savedInstanceState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Called when all saved state has been restored into the view hierarchy of the fragment. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [postponeEnterTransition](https://developer.android.com/reference/kotlin/android/app/Fragment#postponeEnterTransition())`()` Postpone the entering Fragment transition until [startPostponedEnterTransition()](https://developer.android.com/reference/kotlin/android/app/Fragment#startPostponedEnterTransition())or [FragmentManager.executePendingTransactions()](https://developer.android.com/reference/kotlin/android/app/FragmentManager#executePendingTransactions())has been called. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerForContextMenu](https://developer.android.com/reference/kotlin/android/app/Fragment#registerForContextMenu(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Registers a context menu to be shown for the given view (multiple views can show the context menu). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestPermissions](https://developer.android.com/reference/kotlin/android/app/Fragment#requestPermissions(kotlin.Array,%20kotlin.Int))`(`permissions:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`, `requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Requests permissions to be granted to this application. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAllowEnterTransitionOverlap](https://developer.android.com/reference/kotlin/android/app/Fragment#setAllowEnterTransitionOverlap(kotlin.Boolean))`(`allow:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the exit transition and enter transition overlap or not. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAllowReturnTransitionOverlap](https://developer.android.com/reference/kotlin/android/app/Fragment#setAllowReturnTransitionOverlap(kotlin.Boolean))`(`allow:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the return transition and reenter transition overlap or not. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setArguments](https://developer.android.com/reference/kotlin/android/app/Fragment#setArguments(android.os.Bundle))`(`args:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Supply the construction arguments for this fragment. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnterSharedElementCallback](https://developer.android.com/reference/kotlin/android/app/Fragment#setEnterSharedElementCallback(android.app.SharedElementCallback))`(`callback:` ` [SharedElementCallback](https://developer.android.com/reference/kotlin/android/app/SharedElementCallback)!`)` When custom transitions are used with Fragments, the enter transition callback is called when this Fragment is attached or detached when not popping the back stack. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnterTransition](https://developer.android.com/reference/kotlin/android/app/Fragment#setEnterTransition(android.transition.Transition))`(`transition:` ` [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)!`)` Sets the Transition that will be used to move Views into the initial scene. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExitSharedElementCallback](https://developer.android.com/reference/kotlin/android/app/Fragment#setExitSharedElementCallback(android.app.SharedElementCallback))`(`callback:` ` [SharedElementCallback](https://developer.android.com/reference/kotlin/android/app/SharedElementCallback)!`)` When custom transitions are used with Fragments, the exit transition callback is called when this Fragment is attached or detached when popping the back stack. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExitTransition](https://developer.android.com/reference/kotlin/android/app/Fragment#setExitTransition(android.transition.Transition))`(`transition:` ` [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)!`)` Sets the Transition that will be used to move Views out of the scene when the fragment is removed, hidden, or detached when not popping the back stack. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHasOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Fragment#setHasOptionsMenu(kotlin.Boolean))`(`hasMenu:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Report that this fragment would like to participate in populating the options menu by receiving a call to [onCreateOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateOptionsMenu(android.view.Menu,%20android.view.MenuInflater))and related methods. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInitialSavedState](https://developer.android.com/reference/kotlin/android/app/Fragment#setInitialSavedState(android.app.Fragment.SavedState))`(`state:` ` [Fragment.SavedState](https://developer.android.com/reference/kotlin/android/app/Fragment.SavedState)!`)` Set the initial saved state that this Fragment should restore itself from when first being constructed, as returned by [FragmentManager.saveFragmentInstanceState](https://developer.android.com/reference/kotlin/android/app/FragmentManager#saveFragmentInstanceState(android.app.Fragment)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMenuVisibility](https://developer.android.com/reference/kotlin/android/app/Fragment#setMenuVisibility(kotlin.Boolean))`(`menuVisible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set a hint for whether this fragment's menu should be visible. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReenterTransition](https://developer.android.com/reference/kotlin/android/app/Fragment#setReenterTransition(android.transition.Transition))`(`transition:` ` [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)!`)` Sets the Transition that will be used to move Views in to the scene when returning due to popping a back stack. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRetainInstance](https://developer.android.com/reference/kotlin/android/app/Fragment#setRetainInstance(kotlin.Boolean))`(`retain:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Control whether a fragment instance is retained across Activity re-creation (such as from a configuration change). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReturnTransition](https://developer.android.com/reference/kotlin/android/app/Fragment#setReturnTransition(android.transition.Transition))`(`transition:` ` [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)!`)` Sets the Transition that will be used to move Views out of the scene when the Fragment is preparing to be removed, hidden, or detached because of popping the back stack. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSharedElementEnterTransition](https://developer.android.com/reference/kotlin/android/app/Fragment#setSharedElementEnterTransition(android.transition.Transition))`(`transition:` ` [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)!`)` Sets the Transition that will be used for shared elements transferred into the content Scene. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSharedElementReturnTransition](https://developer.android.com/reference/kotlin/android/app/Fragment#setSharedElementReturnTransition(android.transition.Transition))`(`transition:` ` [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)!`)` Sets the Transition that will be used for shared elements transferred back during a pop of the back stack. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTargetFragment](https://developer.android.com/reference/kotlin/android/app/Fragment#setTargetFragment(android.app.Fragment,%20kotlin.Int))`(`fragment:` ` [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment#)!`, `requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Optional target for this fragment. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUserVisibleHint](https://developer.android.com/reference/kotlin/android/app/Fragment#setUserVisibleHint(kotlin.Boolean))`(`isVisibleToUser:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set a hint to the system about whether this fragment's UI is currently visible to the user. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldShowRequestPermissionRationale](https://developer.android.com/reference/kotlin/android/app/Fragment#shouldShowRequestPermissionRationale(kotlin.String))`(`permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Gets whether you should show UI with rationale before requesting a permission. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startActivity](https://developer.android.com/reference/kotlin/android/app/Fragment#startActivity(android.content.Intent))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` Call android. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startActivity](https://developer.android.com/reference/kotlin/android/app/Fragment#startActivity(android.content.Intent,%20android.os.Bundle))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`, `options:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Call android. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startActivityForResult](https://developer.android.com/reference/kotlin/android/app/Fragment#startActivityForResult(android.content.Intent,%20kotlin.Int))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`, `requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Call [Activity.startActivityForResult(Intent, int)](https://developer.android.com/reference/kotlin/android/app/Activity#startActivityForResult(android.content.Intent,%20kotlin.Int))from the fragment's containing Activity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startActivityForResult](https://developer.android.com/reference/kotlin/android/app/Fragment#startActivityForResult(android.content.Intent,%20kotlin.Int,%20android.os.Bundle))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`, `requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `options:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Call [Activity.startActivityForResult(Intent, int, Bundle)](https://developer.android.com/reference/kotlin/android/app/Activity#startActivityForResult(android.content.Intent,%20kotlin.Int,%20android.os.Bundle))from the fragment's containing Activity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startIntentSenderForResult](https://developer.android.com/reference/kotlin/android/app/Fragment#startIntentSenderForResult(android.content.IntentSender,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle))`(`intent:` ` [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#)!`, `requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fillInIntent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)?`, `flagsMask:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flagsValues:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `extraFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `options:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Call [Activity.startIntentSenderForResult(IntentSender, int, Intent, int, int, int,](https://developer.android.com/reference/kotlin/android/app/Activity#startIntentSenderForResult(android.content.IntentSender,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle))from the fragment's containing Activity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startPostponedEnterTransition](https://developer.android.com/reference/kotlin/android/app/Fragment#startPostponedEnterTransition())`()` Begin postponed transitions after [postponeEnterTransition()](https://developer.android.com/reference/kotlin/android/app/Fragment#postponeEnterTransition())was called. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/app/Fragment#toString())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterForContextMenu](https://developer.android.com/reference/kotlin/android/app/Fragment#unregisterForContextMenu(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Prevents a context menu to be shown for the given view. |

| Inherited functions ||
|---|---|
| From class [ComponentCallbacks](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConfigurationChanged](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onConfigurationChanged(android.content.res.Configuration))`(`newConfig:` ` [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)`)` <br /> Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources. At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration. For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLowMemory](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#onLowMemory())`()` <br /> This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing. <br /> | ||

## Public constructors

### Fragment

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Fragment()
```

Default constructor.**Every** fragment must have an empty constructor, so it can be instantiated when restoring its activity's state. It is strongly recommended that subclasses do not have other constructors with parameters, since these constructors will not be called when the fragment is re-instantiated; instead, arguments can be supplied by the caller with [setArguments](https://developer.android.com/reference/kotlin/android/app/Fragment#setArguments(android.os.Bundle))and later retrieved by the Fragment with [getArguments](https://developer.android.com/reference/kotlin/android/app/Fragment#getArguments()).

Applications should generally not implement a constructor. Prefer [onAttach(android.content.Context)](https://developer.android.com/reference/kotlin/android/app/Fragment#onAttach(android.content.Context))instead. It is the first place application code can run where the fragment is ready to be used - the point where the fragment is actually associated with its context. Some applications may also want to implement #onInflate to retrieve attributes from a layout resource, although note this happens when the fragment is attached.

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
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!:The raw file descriptor that the dump is being sent to. |
| `writer` | [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)!:The PrintWriter to which you should dump your state. This will be closed for you after you return. |
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

Return the arguments supplied to [setArguments](https://developer.android.com/reference/kotlin/android/app/Fragment#setArguments(android.os.Bundle)), if any. 

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

Return the [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) this fragment is currently associated with. 

### getEnterTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEnterTransition(): Transition!
```

**Deprecated:** *Deprecated in Java.*

Returns the Transition that will be used to move Views into the initial scene. The entering Views will be those that are regular Views or ViewGroups that have [ViewGroup.isTransitionGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#isTransitionGroup())return true. Typical Transitions will extend [android.transition.Visibility](https://developer.android.com/reference/kotlin/android/transition/Visibility.html#) as entering is governed by changing visibility from [View.INVISIBLE](https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int) to [View.VISIBLE](https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int).

| Return ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)! | the Transition to use to move Views into the initial Scene. |

### getExitTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExitTransition(): Transition!
```

**Deprecated:** *Deprecated in Java.*

Returns the Transition that will be used to move Views out of the scene when the fragment is removed, hidden, or detached when not popping the back stack. The exiting Views will be those that are regular Views or ViewGroups that have [ViewGroup.isTransitionGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#isTransitionGroup())return true. Typical Transitions will extend [android.transition.Visibility](https://developer.android.com/reference/kotlin/android/transition/Visibility.html#) as exiting is governed by changing visibility from [View.VISIBLE](https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int) to [View.INVISIBLE](https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int). If transition is null, the views will remain unaffected.

| Return ||
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)! | the Transition to use to move Views out of the Scene when the Fragment is being closed not due to popping the back stack. |

### getFragmentManager

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFragmentManager(): FragmentManager!
```

**Deprecated:** *Deprecated in Java.*

Return the FragmentManager for interacting with fragments associated with this fragment's activity. Note that this will be non-null slightly before [getActivity()](https://developer.android.com/reference/kotlin/android/app/Fragment#getActivity()), during the time from when the fragment is placed in a [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction) until it is committed and attached to its activity.

If this Fragment is a child of another Fragment, the FragmentManager returned here will be the parent's [getChildFragmentManager()](https://developer.android.com/reference/kotlin/android/app/Fragment#getChildFragmentManager()). 

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

Returns the cached LayoutInflater used to inflate Views of this Fragment. If [onGetLayoutInflater(android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onGetLayoutInflater(android.os.Bundle))has not been called [onGetLayoutInflater(android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onGetLayoutInflater(android.os.Bundle))will be called with a`null`argument and that value will be cached.

The cached LayoutInflater will be replaced immediately prior to [onCreateView(android.view.LayoutInflater,android.view.ViewGroup,android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle))and cleared immediately after [onDetach()](https://developer.android.com/reference/kotlin/android/app/Fragment#onDetach()).

| Return ||
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [LayoutInflater](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#)! | The LayoutInflater used to inflate Views of this Fragment. |

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

Returns the Transition that will be used to move Views in to the scene when returning due to popping a back stack. The entering Views will be those that are regular Views or ViewGroups that have [ViewGroup.isTransitionGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#isTransitionGroup())return true. Typical Transitions will extend [android.transition.Visibility](https://developer.android.com/reference/kotlin/android/transition/Visibility.html#) as exiting is governed by changing visibility from [View.VISIBLE](https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int) to [View.INVISIBLE](https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int). If transition is null, the views will remain unaffected. If nothing is set, the default will be to use the same transition as [setExitTransition(android.transition.Transition)](https://developer.android.com/reference/kotlin/android/app/Fragment#setExitTransition(android.transition.Transition)).

| Return ||
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)! | the Transition to use to move Views into the scene when reentering from a previously-started Activity. |

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

Returns the Transition that will be used to move Views out of the scene when the Fragment is preparing to be removed, hidden, or detached because of popping the back stack. The exiting Views will be those that are regular Views or ViewGroups that have [ViewGroup.isTransitionGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#isTransitionGroup())return true. Typical Transitions will extend [android.transition.Visibility](https://developer.android.com/reference/kotlin/android/transition/Visibility.html#) as entering is governed by changing visibility from [View.VISIBLE](https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int) to [View.INVISIBLE](https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int). If`transition`is null, entering Views will remain unaffected.

| Return ||
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)! | the Transition to use to move Views out of the Scene when the Fragment is preparing to close. |

### getSharedElementEnterTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSharedElementEnterTransition(): Transition!
```

**Deprecated:** *Deprecated in Java.*

Returns the Transition that will be used for shared elements transferred into the content Scene. Typical Transitions will affect size and location, such as [android.transition.ChangeBounds](https://developer.android.com/reference/kotlin/android/transition/ChangeBounds.html#). A null value will cause transferred shared elements to blink to the final position.

| Return ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)! | The Transition to use for shared elements transferred into the content Scene. |

### getSharedElementReturnTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSharedElementReturnTransition(): Transition!
```

**Deprecated:** *Deprecated in Java.*

Return the Transition that will be used for shared elements transferred back during a pop of the back stack. This Transition acts in the leaving Fragment. Typical Transitions will affect size and location, such as [android.transition.ChangeBounds](https://developer.android.com/reference/kotlin/android/transition/ChangeBounds.html#). A null value will cause transferred shared elements to blink to the final position. If no value is set, the default will be to use the same value as [setSharedElementEnterTransition(android.transition.Transition)](https://developer.android.com/reference/kotlin/android/app/Fragment#setSharedElementEnterTransition(android.transition.Transition)).

| Return ||
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)! | The Transition to use for shared elements transferred out of the content Scene. |

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

Return a localized formatted string from the application's package's default string table, substituting the format arguments as defined in [java.util.Formatter](https://developer.android.com/reference/kotlin/java/util/Formatter.html#) and java.lang.String#format.

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

Return the target fragment set by [setTargetFragment](https://developer.android.com/reference/kotlin/android/app/Fragment#setTargetFragment(android.app.Fragment,%20kotlin.Int)). 

### getTargetRequestCode

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTargetRequestCode(): Int
```

**Deprecated:** *Deprecated in Java.*

Return the target request code set by [setTargetFragment](https://developer.android.com/reference/kotlin/android/app/Fragment#setTargetFragment(android.app.Fragment,%20kotlin.Int)). 

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

- [#setUserVisibleHint(boolean)](https://developer.android.com/reference/kotlin/android/app/Fragment#setUserVisibleHint(kotlin.Boolean)) 

### getView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getView(): View?
```

**Deprecated:** *Deprecated in Java.*

Get the root view for the fragment's layout (the one returned by [onCreateView](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle))), if provided.

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)? | The fragment's root view, or null if it has no layout. |

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

Like [instantiate(android.content.Context,java.lang.String,android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#instantiate(android.content.Context,%20kotlin.String,%20android.os.Bundle))but with a null argument Bundle. 

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The calling context being used to instantiate the fragment. This is currently just used to get its ClassLoader. |
| `fname` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The class name of the fragment to instantiate. |
| `args` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:Bundle of arguments to supply to the fragment, which it can retrieve with [getArguments()](https://developer.android.com/reference/kotlin/android/app/Fragment#getArguments()). May be null. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------|
| [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment#)! | Returns a new fragment instance. |

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

Return true if the fragment has been explicitly detached from the UI. That is, [FragmentTransaction.detach(Fragment)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#detach(android.app.Fragment))has been used on it. 

### isHidden

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isHidden(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Return true if the fragment has been hidden. By default fragments are shown. You can find out about changes to this state with [onHiddenChanged](https://developer.android.com/reference/kotlin/android/app/Fragment#onHiddenChanged(kotlin.Boolean)). Note that the hidden state is orthogonal to other states -- that is, to be visible to the user, a fragment must be both started and not hidden. 

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

Return true if the fragment is in the resumed state. This is true for the duration of [onResume()](https://developer.android.com/reference/kotlin/android/app/Fragment#onResume())and [onPause()](https://developer.android.com/reference/kotlin/android/app/Fragment#onPause())as well. 

### isStateSaved

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isStateSaved(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if this fragment is added and its state has already been saved by its host. Any operations that would change saved state should not be performed if this method returns true, and some operations such as [setArguments(android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#setArguments(android.os.Bundle))will fail.

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

Called when the fragment's activity has been created and this fragment's view hierarchy instantiated. It can be used to do final initialization once these pieces are in place, such as retrieving views or restoring state. It is also useful for fragments that use [setRetainInstance(boolean)](https://developer.android.com/reference/kotlin/android/app/Fragment#setRetainInstance(kotlin.Boolean))to retain their instance, as this callback tells the fragment when it is fully associated with the new activity instance. This is called after [onCreateView](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle))and before [onViewStateRestored(android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onViewStateRestored(android.os.Bundle)). 
If you override this method you*must*call through to the superclass implementation.

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `savedInstanceState` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:If the fragment is being re-created from a previous saved state, this is the state. This value may be`null`. |

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

Receive the result from a previous call to [startActivityForResult(android.content.Intent,int)](https://developer.android.com/reference/kotlin/android/app/Fragment#startActivityForResult(android.content.Intent,%20kotlin.Int)). This follows the related Activity API as described there in [Activity.onActivityResult(int, int, Intent)](https://developer.android.com/reference/kotlin/android/app/Activity#onActivityResult(kotlin.Int,%20kotlin.Int,%20android.content.Intent)).

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The integer request code originally supplied to startActivityForResult(), allowing you to identify who this result came from. |
| `resultCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The integer result code returned by the child activity through its setResult(). |
| `data` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:An Intent, which can return result data to the caller (various data can be attached to Intent "extras"). |

### onAttach

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAttach(activity: Activity!): Unit
```

**Deprecated:** *Use [onAttach(android.content.Context)](https://developer.android.com/reference/kotlin/android/app/Fragment#onAttach(android.content.Context))instead.*

<br />

If you override this method you*must*call through to the superclass implementation. 

### onAttach

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAttach(context: Context!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when a fragment is first attached to its context. [onCreate(android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreate(android.os.Bundle))will be called after this. 
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
| `childFragment` | [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment#)!:child fragment being attached |

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
| `newConfig` | [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#):The new device configuration. This value cannot be`null`. |

### onContextItemSelected

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onContextItemSelected(item: MenuItem!): Boolean
```

**Deprecated:** *Deprecated in Java.*

This hook is called whenever an item in a context menu is selected. The default implementation simply returns false to have the normal processing happen (calling the item's Runnable or sending a message to its Handler as appropriate). You can use this method for any items for which you would like to do processing without those other facilities.

Use [MenuItem.getMenuInfo()](https://developer.android.com/reference/kotlin/android/view/MenuItem.html#getMenuInfo())to get extra information set by the View that added this menu item.

Derived classes should call through to the base class for it to perform the default menu handling.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------|
| `item` | [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem.html#)!:The context menu item that was selected. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean Return false to allow normal context menu processing to proceed, true to consume it here. |

### onCreate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCreate(savedInstanceState: Bundle?): Unit
```

**Deprecated:** *Deprecated in Java.*

Called to do initial creation of a fragment. This is called after [onAttach(android.app.Activity)](https://developer.android.com/reference/kotlin/android/app/Fragment#onAttach(android.app.Activity))and before [onCreateView(android.view.LayoutInflater,android.view.ViewGroup,android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle)), but is not called if the fragment instance is retained across Activity re-creation (see [setRetainInstance(boolean)](https://developer.android.com/reference/kotlin/android/app/Fragment#setRetainInstance(kotlin.Boolean))).

Note that this can be called while the fragment's activity is still in the process of being created. As such, you can not rely on things like the activity's content view hierarchy being initialized at this point. If you want to do work once the activity itself is created, see [onActivityCreated(android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onActivityCreated(android.os.Bundle)).

If your app's`targetSdkVersion`is [android.os.Build.VERSION_CODES#M](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int) or lower, child fragments being restored from the savedInstanceState are restored after`onCreate`returns. When targeting [android.os.Build.VERSION_CODES#N](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int) or above and running on an N or newer platform version they are restored by`Fragment.onCreate`.

If you override this method you*must* call through to the superclass implementation.

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `savedInstanceState` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:If the fragment is being re-created from a previous saved state, this is the state. This value may be`null`. |

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

Called when a context menu for the`view`is about to be shown. Unlike [onCreateOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateOptionsMenu(android.view.Menu,%20android.view.MenuInflater)), this will be called every time the context menu is about to be shown and should be populated for the view (or item inside the view for [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView.html#) subclasses, this can be found in the`menuInfo`)).

Use [onContextItemSelected(android.view.MenuItem)](https://developer.android.com/reference/kotlin/android/app/Fragment#onContextItemSelected(android.view.MenuItem))to know when an item has been selected.

The default implementation calls up to [Activity.onCreateContextMenu](https://developer.android.com/reference/kotlin/android/app/Activity#onCreateContextMenu(android.view.ContextMenu,%20android.view.View,%20android.view.ContextMenu.ContextMenuInfo)), though you can not call this implementation if you don't want that behavior.

It is not safe to hold onto the context menu after this method returns. Called when the context menu for this view is being built. It is not safe to hold onto the menu after this method returns.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `menu` | [ContextMenu](https://developer.android.com/reference/kotlin/android/view/ContextMenu.html#)!:The context menu that is being built |
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view for which the context menu is being built |
| `menuInfo` | [ContextMenu.ContextMenuInfo](https://developer.android.com/reference/kotlin/android/view/ContextMenu.ContextMenuInfo.html#)!:Extra information about the item for which the context menu should be shown. This information will vary depending on the class of v. |

### onCreateOptionsMenu

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCreateOptionsMenu(
    menu: Menu!, 
    inflater: MenuInflater!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Initialize the contents of the Activity's standard options menu. You should place your menu items in to menu. For this method to be called, you must have first called [setHasOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Fragment#setHasOptionsMenu(kotlin.Boolean)). See [Activity.onCreateOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Activity#onCreateOptionsMenu(android.view.Menu))for more information.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------|
| `menu` | [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)!:The options menu in which you place your items. |

**See Also**

- [#setHasOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Fragment#setHasOptionsMenu(kotlin.Boolean))
- [#onPrepareOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Fragment#onPrepareOptionsMenu(android.view.Menu))
- [#onOptionsItemSelected](https://developer.android.com/reference/kotlin/android/app/Fragment#onOptionsItemSelected(android.view.MenuItem)) 

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

Called to have the fragment instantiate its user interface view. This is optional, and non-graphical fragments can return null (which is the default implementation). This will be called between [onCreate(android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreate(android.os.Bundle))and [onActivityCreated(android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onActivityCreated(android.os.Bundle)).

If you return a View from here, you will later be called in [onDestroyView](https://developer.android.com/reference/kotlin/android/app/Fragment#onDestroyView())when the view is being released.

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inflater` | [LayoutInflater](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#)!:The LayoutInflater object that can be used to inflate any views in the fragment, |
| `container` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)?:If non-null, this is the parent view that the fragment's UI should be attached to. The fragment should not add the view itself, but this can be used to generate the LayoutParams of the view. |
| `savedInstanceState` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:If non-null, this fragment is being re-constructed from a previous saved state as given here. |

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)? | Return the View for the fragment's UI, or null. |

### onDestroy

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDestroy(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the fragment is no longer in use. This is called after [onStop()](https://developer.android.com/reference/kotlin/android/app/Fragment#onStop())and before [onDetach()](https://developer.android.com/reference/kotlin/android/app/Fragment#onDetach()). 
If you override this method you*must*call through to the superclass implementation. 

### onDestroyOptionsMenu

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDestroyOptionsMenu(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when this fragment's option menu items are no longer being included in the overall options menu. Receiving this call means that the menu needed to be rebuilt, but this fragment's items were not included in the newly built menu (its [onCreateOptionsMenu(android.view.Menu,android.view.MenuInflater)](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateOptionsMenu(android.view.Menu,%20android.view.MenuInflater))was not called). 

### onDestroyView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDestroyView(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the view previously created by [onCreateView](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle))has been detached from the fragment. The next time the fragment needs to be displayed, a new view will be created. This is called after [onStop()](https://developer.android.com/reference/kotlin/android/app/Fragment#onStop())and before [onDestroy()](https://developer.android.com/reference/kotlin/android/app/Fragment#onDestroy()). It is called*regardless* of whether [onCreateView](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle))returned a non-null view. Internally it is called after the view's state has been saved but before it has been removed from its parent. 
If you override this method you*must*call through to the superclass implementation. 

### onDetach

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDetach(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the fragment is no longer attached to its activity. This is called after [onDestroy()](https://developer.android.com/reference/kotlin/android/app/Fragment#onDestroy()), except in the cases where the fragment instance is retained across Activity re-creation (see [setRetainInstance(boolean)](https://developer.android.com/reference/kotlin/android/app/Fragment#setRetainInstance(kotlin.Boolean))), in which case it is called after [onStop()](https://developer.android.com/reference/kotlin/android/app/Fragment#onStop()). 
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
| [LayoutInflater](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#)! | The LayoutInflater used to inflate Views of this Fragment. |

### onHiddenChanged

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onHiddenChanged(hidden: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the hidden state (as returned by [isHidden()](https://developer.android.com/reference/kotlin/android/app/Fragment#isHidden())of the fragment has changed. Fragments start out not hidden; this will be called whenever the fragment changes state from that.

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

**Deprecated:** *Use [onInflate(android.content.Context,android.util.AttributeSet,android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onInflate(android.content.Context,%20android.util.AttributeSet,%20android.os.Bundle))instead.*

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

Called when a fragment is being created as part of a view layout inflation, typically from setting the content view of an activity. This may be called immediately after the fragment is created from a tag in a layout file. Note this is*before* the fragment's [onAttach(android.app.Activity)](https://developer.android.com/reference/kotlin/android/app/Fragment#onAttach(android.app.Activity))has been called; all you should do here is parse the attributes and save them away.

This is called every time the fragment is inflated, even if it is being inflated into a new instance with saved state. It typically makes sense to re-parse the parameters each time, to allow them to change with different configurations.

Here is a typical implementation of a fragment that can take parameters both through attributes supplied here as well from [getArguments()](https://developer.android.com/reference/kotlin/android/app/Fragment#getArguments()):

Note that parsing the XML attributes uses a "styleable" resource. The declaration for the styleable used here is:

The fragment can then be declared within its activity's content layout through a tag like this:

This fragment can also be created dynamically from arguments given at runtime in the arguments Bundle; here is an example of doing so at creation of the containing activity:

If you override this method you*must* call through to the superclass implementation.

<br />

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The Context that is inflating this fragment. |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!:The attributes at the tag where the fragment is being created. |
| `savedInstanceState` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:If the fragment is being re-created from a previous saved state, this is the state. |

### onInflate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onInflate(
    attrs: AttributeSet!, 
    savedInstanceState: Bundle!
): Unit
```

**Deprecated:** *Use [onInflate(android.content.Context,android.util.AttributeSet,android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onInflate(android.content.Context,%20android.util.AttributeSet,%20android.os.Bundle))instead.*

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

**Deprecated:** *Use [onMultiWindowModeChanged(boolean,android.content.res.Configuration)](https://developer.android.com/reference/kotlin/android/app/Fragment#onMultiWindowModeChanged(kotlin.Boolean,%20android.content.res.Configuration))instead.*

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

Called when the Fragment's activity changes from fullscreen mode to multi-window mode and visa-versa. This is generally tied to android.app.Activity#onMultiWindowModeChanged of the containing Activity. This method provides the same configuration that will be sent in the following [onConfigurationChanged(android.content.res.Configuration)](https://developer.android.com/reference/kotlin/android/app/Fragment#onConfigurationChanged(android.content.res.Configuration))call after the activity enters this mode.

| Parameters ||
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `isInMultiWindowMode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the activity is in multi-window mode. |
| `newConfig` | [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)!:The new configuration of the activity with the state {@param isInMultiWindowMode}. |

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
| `item` | [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem.html#)!:The menu item that was selected. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean Return false to allow normal menu processing to proceed, true to consume it here. |

**See Also**

- [#onCreateOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateOptionsMenu(android.view.Menu,%20android.view.MenuInflater)) 

### onOptionsMenuClosed

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onOptionsMenuClosed(menu: Menu!): Unit
```

**Deprecated:** *Deprecated in Java.*

This hook is called whenever the options menu is being closed (either by the user canceling the menu with the back/menu button, or when an item is selected).

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `menu` | [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)!:The options menu as last shown or first initialized by onCreateOptionsMenu(). |

### onPause

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPause(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the Fragment is no longer resumed. This is generally tied to [Activity.onPause](https://developer.android.com/reference/kotlin/android/app/Activity#onPause())of the containing Activity's lifecycle. 
If you override this method you*must*call through to the superclass implementation. 

### onPictureInPictureModeChanged

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPictureInPictureModeChanged(isInPictureInPictureMode: Boolean): Unit
```

**Deprecated:** *Use [onPictureInPictureModeChanged(boolean,android.content.res.Configuration)](https://developer.android.com/reference/kotlin/android/app/Fragment#onPictureInPictureModeChanged(kotlin.Boolean,%20android.content.res.Configuration))instead.*

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

Called by the system when the activity changes to and from picture-in-picture mode. This is generally tied to android.app.Activity#onPictureInPictureModeChanged of the containing Activity. This method provides the same configuration that will be sent in the following [onConfigurationChanged(android.content.res.Configuration)](https://developer.android.com/reference/kotlin/android/app/Fragment#onConfigurationChanged(android.content.res.Configuration))call after the activity enters this mode.

| Parameters ||
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `isInPictureInPictureMode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the activity is in picture-in-picture mode. |
| `newConfig` | [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)!:The new configuration of the activity with the state {@param isInPictureInPictureMode}. |

### onPrepareOptionsMenu

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPrepareOptionsMenu(menu: Menu!): Unit
```

**Deprecated:** *Deprecated in Java.*

Prepare the Screen's standard options menu to be displayed. This is called right before the menu is shown, every time it is shown. You can use this method to efficiently enable/disable items or otherwise dynamically modify the contents. See [Activity.onPrepareOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Activity#onPrepareOptionsMenu(android.view.Menu))for more information.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `menu` | [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)!:The options menu as last shown or first initialized by onCreateOptionsMenu(). |

**See Also**

- [#setHasOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Fragment#setHasOptionsMenu(kotlin.Boolean))
- [#onCreateOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateOptionsMenu(android.view.Menu,%20android.view.MenuInflater)) 

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
| `grantResults` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html):The grant results for the corresponding permissions which is either [android.content.pm.PackageManager#PERMISSION_GRANTED](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PERMISSION_GRANTED:kotlin.Int) or [android.content.pm.PackageManager#PERMISSION_DENIED](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#PERMISSION_DENIED:kotlin.Int). Never null. |

**See Also**

- [#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Fragment#requestPermissions(kotlin.Array,%20kotlin.Int)) 

### onResume

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onResume(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the fragment is visible to the user and actively running. This is generally tied to [Activity.onResume](https://developer.android.com/reference/kotlin/android/app/Activity#onResume())of the containing Activity's lifecycle. 
If you override this method you*must*call through to the superclass implementation. 

### onSaveInstanceState

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSaveInstanceState(outState: Bundle!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called to ask the fragment to save its current dynamic state, so it can later be reconstructed in a new instance of its process is restarted. If a new instance of the fragment later needs to be created, the data you place in the Bundle here will be available in the Bundle given to [onCreate(android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreate(android.os.Bundle)), [onCreateView(android.view.LayoutInflater,android.view.ViewGroup,android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle)), and [onActivityCreated(android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onActivityCreated(android.os.Bundle)).

This corresponds to [Activity.onSaveInstanceState(Bundle)](https://developer.android.com/reference/kotlin/android/app/Activity#onSaveInstanceState(android.os.Bundle))and most of the discussion there applies here as well. Note however:*this method may be called at any time before [onDestroy()](https://developer.android.com/reference/kotlin/android/app/Fragment#onDestroy())*. There are many situations where a fragment may be mostly torn down (such as when placed on the back stack with no UI showing), but its state will not be saved until its owning activity actually needs to save its state.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------|
| `outState` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:Bundle in which to place your saved state. |

### onStart

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onStart(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the Fragment is visible to the user. This is generally tied to [Activity.onStart](https://developer.android.com/reference/kotlin/android/app/Activity#onStart())of the containing Activity's lifecycle. 
If you override this method you*must*call through to the superclass implementation. 

### onStop

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onStop(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the Fragment is no longer started. This is generally tied to [Activity.onStop](https://developer.android.com/reference/kotlin/android/app/Activity#onStop())of the containing Activity's lifecycle. 
If you override this method you*must*call through to the superclass implementation. 

### onTrimMemory

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTrimMemory(level: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the operating system has determined that it is a good time for a process to trim unneeded memory from its process. You should never compare to exact values of the level, since new intermediate values may be added -- you will typically want to compare if the value is greater or equal to a level you are interested in.

To retrieve the processes current trim level at any point, you can use [ActivityManager.getMyMemoryState(RunningAppProcessInfo)](https://developer.android.com/reference/kotlin/android/app/ActivityManager#getMyMemoryState(android.app.ActivityManager.RunningAppProcessInfo)). If you override this method you*must*call through to the superclass implementation.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The context of the trim, giving a hint of the amount of trimming the application may like to perform. Value is [android.content.ComponentCallbacks2#TRIM_MEMORY_COMPLETE](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_COMPLETE:kotlin.Int), [android.content.ComponentCallbacks2#TRIM_MEMORY_MODERATE](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_MODERATE:kotlin.Int), [android.content.ComponentCallbacks2#TRIM_MEMORY_BACKGROUND](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_BACKGROUND:kotlin.Int), [android.content.ComponentCallbacks2#TRIM_MEMORY_UI_HIDDEN](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_UI_HIDDEN:kotlin.Int), [android.content.ComponentCallbacks2#TRIM_MEMORY_RUNNING_CRITICAL](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_CRITICAL:kotlin.Int), [android.content.ComponentCallbacks2#TRIM_MEMORY_RUNNING_LOW](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_LOW:kotlin.Int), or [android.content.ComponentCallbacks2#TRIM_MEMORY_RUNNING_MODERATE](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_MODERATE:kotlin.Int) |

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

Called immediately after [onCreateView(android.view.LayoutInflater,android.view.ViewGroup,android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle))has returned, but before any saved state has been restored in to the view. This gives subclasses a chance to initialize themselves once they know their view hierarchy has been completely created. The fragment's view hierarchy is not however attached to its parent at this point.

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The View returned by [onCreateView(android.view.LayoutInflater,android.view.ViewGroup,android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle)). |
| `savedInstanceState` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:If non-null, this fragment is being re-constructed from a previous saved state as given here. |

### onViewStateRestored

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onViewStateRestored(savedInstanceState: Bundle!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when all saved state has been restored into the view hierarchy of the fragment. This can be used to do initialization based on saved state that you are letting the view hierarchy track itself, such as whether check box widgets are currently checked. This is called after [onActivityCreated(android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onActivityCreated(android.os.Bundle))and before [onStart()](https://developer.android.com/reference/kotlin/android/app/Fragment#onStart()). 
If you override this method you*must*call through to the superclass implementation.

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `savedInstanceState` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:If the fragment is being re-created from a previous saved state, this is the state. |

### postponeEnterTransition

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun postponeEnterTransition(): Unit
```

**Deprecated:** *Deprecated in Java.*

Postpone the entering Fragment transition until [startPostponedEnterTransition()](https://developer.android.com/reference/kotlin/android/app/Fragment#startPostponedEnterTransition())or [FragmentManager.executePendingTransactions()](https://developer.android.com/reference/kotlin/android/app/FragmentManager#executePendingTransactions())has been called.

This method gives the Fragment the ability to delay Fragment animations until all data is loaded. Until then, the added, shown, and attached Fragments will be INVISIBLE and removed, hidden, and detached Fragments won't be have their Views removed. The transaction runs when all postponed added Fragments in the transaction have called [startPostponedEnterTransition()](https://developer.android.com/reference/kotlin/android/app/Fragment#startPostponedEnterTransition()).

This method should be called before being added to the FragmentTransaction or in [onCreate(android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreate(android.os.Bundle)), [onAttach(android.content.Context)](https://developer.android.com/reference/kotlin/android/app/Fragment#onAttach(android.content.Context)), or [onCreateView(android.view.LayoutInflater,android.view.ViewGroup,android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle))}. [startPostponedEnterTransition()](https://developer.android.com/reference/kotlin/android/app/Fragment#startPostponedEnterTransition())must be called to allow the Fragment to start the transitions.

When a FragmentTransaction is started that may affect a postponed FragmentTransaction, based on which containers are in their operations, the postponed FragmentTransaction will have its start triggered. The early triggering may result in faulty or nonexistent animations in the postponed transaction. FragmentTransactions that operate only on independent containers will not interfere with each other's postponement.

Calling postponeEnterTransition on Fragments with a null View will not postpone the transition. Likewise, postponement only works if FragmentTransaction optimizations are enabled. 
**See Also**

- [android.app.Activity#postponeEnterTransition()](https://developer.android.com/reference/kotlin/android/app/Activity#postponeEnterTransition())
- [android.app.FragmentTransaction#setReorderingAllowed(boolean)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#setReorderingAllowed(kotlin.Boolean)) 

### registerForContextMenu

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerForContextMenu(view: View!): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers a context menu to be shown for the given view (multiple views can show the context menu). This method will set the [OnCreateContextMenuListener](https://developer.android.com/reference/kotlin/android/view/View.OnCreateContextMenuListener.html#) on the view to this fragment, so [onCreateContextMenu(android.view.ContextMenu,android.view.View,android.view.ContextMenu.ContextMenuInfo)](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateContextMenu(android.view.ContextMenu,%20android.view.View,%20android.view.ContextMenu.ContextMenuInfo))will be called when it is time to show the context menu.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should show a context menu. |

**See Also**

- [#unregisterForContextMenu(View)](https://developer.android.com/reference/kotlin/android/app/Fragment#unregisterForContextMenu(android.view.View)) 

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

Requests permissions to be granted to this application. These permissions must be requested in your manifest, they should not be granted to your app, and they should have protection level [#PROTECTION_DANGEROUS dangerous](https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#), regardless whether they are declared by the platform or a third-party app.

Normal permissions [android.content.pm.PermissionInfo#PROTECTION_NORMAL](https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#PROTECTION_NORMAL:kotlin.Int) are granted at install time if requested in the manifest. Signature permissions [android.content.pm.PermissionInfo#PROTECTION_SIGNATURE](https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#PROTECTION_SIGNATURE:kotlin.Int) are granted at install time if requested in the manifest and the signature of your app matches the signature of the app declaring the permissions.

Call [shouldShowRequestPermissionRationale(java.lang.String)](https://developer.android.com/reference/kotlin/android/app/Fragment#shouldShowRequestPermissionRationale(kotlin.String))before calling this API to check if the system recommends to show a rationale UI before asking for a permission.

If your app does not have the requested permissions the user will be presented with UI for accepting them. After the user has accepted or rejected the requested permissions you will receive a callback on[onRequestPermissionsResult(int,java.lang.String[],int[])](https://developer.android.com/reference/kotlin/android/app/Fragment#onRequestPermissionsResult(kotlin.Int,%20kotlin.Array,%20kotlin.IntArray))reporting whether the permissions were granted or not.

Note that requesting a permission does not guarantee it will be granted and your app should be able to run without having this permission.

This method may start an activity allowing the user to choose which permissions to grant and which to reject. Hence, you should be prepared that your activity may be paused and resumed. Further, granting some permissions may require a restart of you application. In such a case, the system will recreate the activity stack before delivering the result to[onRequestPermissionsResult(int,java.lang.String[],int[])](https://developer.android.com/reference/kotlin/android/app/Fragment#onRequestPermissionsResult(kotlin.Int,%20kotlin.Array,%20kotlin.IntArray)).

When checking whether you have a permission you should use [android.content.Context#checkSelfPermission(String)](https://developer.android.com/reference/kotlin/android/content/Context.html#checkSelfPermission(kotlin.String)).

Calling this API for permissions already granted to your app would show UI to the user to decide whether the app can still hold these permissions. This can be useful if the way your app uses data guarded by the permissions changes significantly.

You cannot request a permission if your activity sets [noHistory](https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestActivity_noHistory:kotlin.Int) to`true`because in this case the activity would not receive result callbacks including[onRequestPermissionsResult(int,java.lang.String[],int[])](https://developer.android.com/reference/kotlin/android/app/Fragment#onRequestPermissionsResult(kotlin.Int,%20kotlin.Array,%20kotlin.IntArray)).

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `permissions` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:The requested permissions. Must me non-null and not empty. |
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Application specific request code to match with a result reported to[onRequestPermissionsResult(int,java.lang.String[],int[])](https://developer.android.com/reference/kotlin/android/app/Fragment#onRequestPermissionsResult(kotlin.Int,%20kotlin.Array,%20kotlin.IntArray)). Should be \>= 0. |

**See Also**

- [#onRequestPermissionsResult(int, String[], int[])](https://developer.android.com/reference/kotlin/android/app/Fragment#onRequestPermissionsResult(kotlin.Int,%20kotlin.Array,%20kotlin.IntArray))
- [android.content.Context#checkSelfPermission(String)](https://developer.android.com/reference/kotlin/android/content/Context.html#checkSelfPermission(kotlin.String)) 

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

This method cannot be called if the fragment is added to a FragmentManager and if [isStateSaved()](https://developer.android.com/reference/kotlin/android/app/Fragment#isStateSaved())would return true. Prior to [Build.VERSION_CODES.O](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int), this method may only be called if the fragment has not yet been added to a FragmentManager. 

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
| `callback` | [SharedElementCallback](https://developer.android.com/reference/kotlin/android/app/SharedElementCallback)!:Used to manipulate the shared element transitions on this Fragment when added not as a pop from the back stack. |

### setEnterTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEnterTransition(transition: Transition!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the Transition that will be used to move Views into the initial scene. The entering Views will be those that are regular Views or ViewGroups that have [ViewGroup.isTransitionGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#isTransitionGroup())return true. Typical Transitions will extend [android.transition.Visibility](https://developer.android.com/reference/kotlin/android/transition/Visibility.html#) as entering is governed by changing visibility from [View.INVISIBLE](https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int) to [View.VISIBLE](https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int). If`transition`is null, entering Views will remain unaffected.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transition` | [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)!:The Transition to use to move Views into the initial Scene. |

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
| `callback` | [SharedElementCallback](https://developer.android.com/reference/kotlin/android/app/SharedElementCallback)!:Used to manipulate the shared element transitions on this Fragment when added as a pop from the back stack. |

### setExitTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setExitTransition(transition: Transition!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the Transition that will be used to move Views out of the scene when the fragment is removed, hidden, or detached when not popping the back stack. The exiting Views will be those that are regular Views or ViewGroups that have [ViewGroup.isTransitionGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#isTransitionGroup())return true. Typical Transitions will extend [android.transition.Visibility](https://developer.android.com/reference/kotlin/android/transition/Visibility.html#) as exiting is governed by changing visibility from [View.VISIBLE](https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int) to [View.INVISIBLE](https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int). If transition is null, the views will remain unaffected.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transition` | [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)!:The Transition to use to move Views out of the Scene when the Fragment is being closed not due to popping the back stack. |

### setHasOptionsMenu

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setHasOptionsMenu(hasMenu: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Report that this fragment would like to participate in populating the options menu by receiving a call to [onCreateOptionsMenu](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateOptionsMenu(android.view.Menu,%20android.view.MenuInflater))and related methods.

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

Set the initial saved state that this Fragment should restore itself from when first being constructed, as returned by [FragmentManager.saveFragmentInstanceState](https://developer.android.com/reference/kotlin/android/app/FragmentManager#saveFragmentInstanceState(android.app.Fragment)).

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Fragment.SavedState](https://developer.android.com/reference/kotlin/android/app/Fragment.SavedState)!:The state the fragment should be restored from. |

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

Sets the Transition that will be used to move Views in to the scene when returning due to popping a back stack. The entering Views will be those that are regular Views or ViewGroups that have [ViewGroup.isTransitionGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#isTransitionGroup())return true. Typical Transitions will extend [android.transition.Visibility](https://developer.android.com/reference/kotlin/android/transition/Visibility.html#) as exiting is governed by changing visibility from [View.VISIBLE](https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int) to [View.INVISIBLE](https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int). If transition is null, the views will remain unaffected. If nothing is set, the default will be to use the same transition as [setExitTransition(android.transition.Transition)](https://developer.android.com/reference/kotlin/android/app/Fragment#setExitTransition(android.transition.Transition)).

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transition` | [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)!:The Transition to use to move Views into the scene when reentering from a previously-started Activity. |

### setRetainInstance

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRetainInstance(retain: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Control whether a fragment instance is retained across Activity re-creation (such as from a configuration change). This can only be used with fragments not in the back stack. If set, the fragment lifecycle will be slightly different when an activity is recreated:

- [onDestroy()](https://developer.android.com/reference/kotlin/android/app/Fragment#onDestroy())will not be called (but [onDetach()](https://developer.android.com/reference/kotlin/android/app/Fragment#onDetach())still will be, because the fragment is being detached from its current activity).
- [onCreate(android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreate(android.os.Bundle))will not be called since the fragment is not being re-created.
- [onAttach(android.app.Activity)](https://developer.android.com/reference/kotlin/android/app/Fragment#onAttach(android.app.Activity))and [onActivityCreated(android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onActivityCreated(android.os.Bundle))**will**still be called.

<br />

### setReturnTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setReturnTransition(transition: Transition!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the Transition that will be used to move Views out of the scene when the Fragment is preparing to be removed, hidden, or detached because of popping the back stack. The exiting Views will be those that are regular Views or ViewGroups that have [ViewGroup.isTransitionGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#isTransitionGroup())return true. Typical Transitions will extend [android.transition.Visibility](https://developer.android.com/reference/kotlin/android/transition/Visibility.html#) as entering is governed by changing visibility from [View.VISIBLE](https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int) to [View.INVISIBLE](https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int). If`transition`is null, entering Views will remain unaffected. If nothing is set, the default will be to use the same value as set in [setEnterTransition(android.transition.Transition)](https://developer.android.com/reference/kotlin/android/app/Fragment#setEnterTransition(android.transition.Transition)).

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transition` | [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)!:The Transition to use to move Views out of the Scene when the Fragment is preparing to close. |

### setSharedElementEnterTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSharedElementEnterTransition(transition: Transition!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the Transition that will be used for shared elements transferred into the content Scene. Typical Transitions will affect size and location, such as [android.transition.ChangeBounds](https://developer.android.com/reference/kotlin/android/transition/ChangeBounds.html#). A null value will cause transferred shared elements to blink to the final position.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transition` | [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)!:The Transition to use for shared elements transferred into the content Scene. |

### setSharedElementReturnTransition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSharedElementReturnTransition(transition: Transition!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the Transition that will be used for shared elements transferred back during a pop of the back stack. This Transition acts in the leaving Fragment. Typical Transitions will affect size and location, such as [android.transition.ChangeBounds](https://developer.android.com/reference/kotlin/android/transition/ChangeBounds.html#). A null value will cause transferred shared elements to blink to the final position. If no value is set, the default will be to use the same value as [setSharedElementEnterTransition(android.transition.Transition)](https://developer.android.com/reference/kotlin/android/app/Fragment#setSharedElementEnterTransition(android.transition.Transition)).

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transition` | [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition.html#)!:The Transition to use for shared elements transferred out of the content Scene. |

### setTargetFragment

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTargetFragment(
    fragment: Fragment!, 
    requestCode: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Optional target for this fragment. This may be used, for example, if this fragment is being started by another, and when done wants to give a result back to the first. The target set here is retained across instances via [FragmentManager.putFragment()](https://developer.android.com/reference/kotlin/android/app/FragmentManager#putFragment(android.os.Bundle,%20kotlin.String,%20android.app.Fragment)).

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fragment` | [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment#)!:The fragment that is the target of this one. |
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Optional request code, for convenience if you are going to call back with [onActivityResult(int,int,android.content.Intent)](https://developer.android.com/reference/kotlin/android/app/Fragment#onActivityResult(kotlin.Int,%20kotlin.Int,%20android.content.Intent)). |

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

- [android.content.Context#checkSelfPermission(String)](https://developer.android.com/reference/kotlin/android/content/Context.html#checkSelfPermission(kotlin.String))
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
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:The intent to start. |

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
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:The intent to start. |
| `options` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:Additional options for how the Activity should be started. See [android.content.Context#startActivity(Intent, Bundle)](https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent,%20android.os.Bundle))Context.startActivity(Intent, Bundle)} for more details. |

### startActivityForResult

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startActivityForResult(
    intent: Intent!, 
    requestCode: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Call [Activity.startActivityForResult(Intent, int)](https://developer.android.com/reference/kotlin/android/app/Activity#startActivityForResult(android.content.Intent,%20kotlin.Int))from the fragment's containing Activity. 

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

Call [Activity.startActivityForResult(Intent, int, Bundle)](https://developer.android.com/reference/kotlin/android/app/Activity#startActivityForResult(android.content.Intent,%20kotlin.Int,%20android.os.Bundle))from the fragment's containing Activity. 

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

Call [Activity.startIntentSenderForResult(IntentSender, int, Intent, int, int, int,](https://developer.android.com/reference/kotlin/android/app/Activity#startIntentSenderForResult(android.content.IntentSender,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle))from the fragment's containing Activity.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------|
| `fillInIntent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)?:This value may be`null`. |

### startPostponedEnterTransition

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startPostponedEnterTransition(): Unit
```

**Deprecated:** *Deprecated in Java.*

Begin postponed transitions after [postponeEnterTransition()](https://developer.android.com/reference/kotlin/android/app/Fragment#postponeEnterTransition())was called. If postponeEnterTransition() was called, you must call startPostponedEnterTransition() or [FragmentManager.executePendingTransactions()](https://developer.android.com/reference/kotlin/android/app/FragmentManager#executePendingTransactions())to complete the FragmentTransaction. If postponement was interrupted with [FragmentManager.executePendingTransactions()](https://developer.android.com/reference/kotlin/android/app/FragmentManager#executePendingTransactions()), before`startPostponedEnterTransition()`, animations may not run or may execute improperly. 
**See Also**

- [android.app.Activity#startPostponedEnterTransition()](https://developer.android.com/reference/kotlin/android/app/Activity#startPostponedEnterTransition()) 

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

Prevents a context menu to be shown for the given view. This method will remove the [OnCreateContextMenuListener](https://developer.android.com/reference/kotlin/android/view/View.OnCreateContextMenuListener.html#) on the view.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should stop showing a context menu. |

**See Also**

- [#registerForContextMenu(View)](https://developer.android.com/reference/kotlin/android/app/Fragment#registerForContextMenu(android.view.View))
