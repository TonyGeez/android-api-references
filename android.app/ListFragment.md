Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ListFragment

Kotlin | [Java](ListFragment.md)
| --- | --- |

```
open class ListFragment : Fragment
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.app.Fragment](Fragment.md) ||
| | ↳ | [android.app.ListFragment](ListFragment.md) |

| **This class was deprecated in API level 28.**
|
| Use the [Support Library](https://developer.android.com/tools/extras/support-library.html) androidx.fragment.app.ListFragment for consistent behavior across all devices and access to [Lifecycle](https://developer.android.com/topic/libraries/architecture/lifecycle.html).

A fragment that displays a list of items by binding to a data source such as an array or Cursor, and exposes event handlers when the user selects an item.

ListFragment hosts a `https://developer.android.com/reference/kotlin/android/widget/ListView.html#` object that can be bound to different data sources, typically either an array or a Cursor holding query results. Binding, screen layout, and row layout are discussed in the following sections.

**Screen Layout**

ListFragment has a default layout that consists of a single list view. However, if you desire, you can customize the fragment layout by returning your own view hierarchy from onCreateView. To do this, your view hierarchy *must* contain a ListView object with the id "@android:id/list" (or `https://developer.android.com/reference/kotlin/android/R.id.html#list:kotlin.Int` if it's in code)

Optionally, your view hierarchy can contain another view object of any type to display when the list view is empty. This "empty list" notifier must have an id "android:empty". Note that when an empty view is present, the list view will be hidden when there is no data to display.

The following code demonstrates an (ugly) custom list layout. It has a list with a green background, and an alternate red "no data" message.

```kotlin
<?xml version="1.0" encoding="utf-8"?>
  <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
          android:orientation="vertical"
          android:layout_width="match_parent"
          android:layout_height="match_parent"
          android:paddingLeft="8dp"
          android:paddingRight="8dp">
 
      <ListView android:id="@id/android:list"
                android:layout_width="match_parent"
                android:layout_height="match_parent"
                android:background="#00FF00"
                android:layout_weight="1"
                android:drawSelectorOnTop="false"/>
 
      <TextView android:id="@id/android:empty"
                android:layout_width="match_parent"
                android:layout_height="match_parent"
                android:background="#FF0000"
                android:text="No data"/>
  </LinearLayout>
  
```

**Row Layout**

You can specify the layout of individual rows in the list. You do this by specifying a layout resource in the ListAdapter object hosted by the fragment (the ListAdapter binds the ListView to the data; more on this later).

A ListAdapter constructor takes a parameter that specifies a layout resource for each row. It also has two additional parameters that let you specify which data field to associate with which object in the row layout resource. These two parameters are typically parallel arrays.

Android provides some standard row layout resources. These are in the `https://developer.android.com/reference/kotlin/android/R.layout.html#` class, and have names such as simple_list_item_1, simple_list_item_2, and two_line_list_item. The following layout XML is the source for the resource two_line_list_item, which displays two data fields,one above the other, for each list row.

```kotlin
<?xml version="1.0" encoding="utf-8"?>
  <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
      android:layout_width="match_parent"
      android:layout_height="wrap_content"
      android:orientation="vertical">
 
      <TextView android:id="@+id/text1"
          android:textSize="16sp"
          android:textStyle="bold"
          android:layout_width="match_parent"
          android:layout_height="wrap_content"/>
 
      <TextView android:id="@+id/text2"
          android:textSize="16sp"
          android:layout_width="match_parent"
          android:layout_height="wrap_content"/>
  </LinearLayout>
  
```

You must identify the data bound to each TextView object in this layout. The syntax for this is discussed in the next section.

**Binding to Data**

You bind the ListFragment's ListView object to data using a class that implements the `https://developer.android.com/reference/kotlin/android/widget/ListAdapter.html#` interface. Android provides two standard list adapters: `https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter.html#` for static data (Maps), and `https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter.html#` for Cursor query results.

You **must** use setListAdapter to associate the list with an adapter. Do not directly call setAdapter or else important initialization will be skipped.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_BACKGROUND:kotlin.Int` Level for onTrimMemory: the process has gone on to the LRU list. This is a good opportunity to clean up resources that can efficiently and quickly be re-built if the user returns to the app. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_COMPLETE:kotlin.Int` Level for onTrimMemory: the process is nearing the end of the background LRU list, and if more memory isn't found soon it will be killed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_MODERATE:kotlin.Int` Level for onTrimMemory: the process is around the middle of the background LRU list; freeing memory can help the system keep other processes running later in the list for better overall performance. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_CRITICAL:kotlin.Int` Level for onTrimMemory: the process is not an expendable background process, but the device is running extremely low on memory and is about to not be able to keep any background processes running. Your running process should free up as many non-critical resources as it can to allow that memory to be used elsewhere. The next thing that will happen after this is onLowMemory called to report that nothing at all can be kept in the background, a situation that can start to notably impact the user. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_LOW:kotlin.Int` Level for onTrimMemory: the process is not an expendable background process, but the device is running low on memory. Your running process should free up unneeded resources to allow that memory to be used elsewhere. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_RUNNING_MODERATE:kotlin.Int` Level for onTrimMemory: the process is not an expendable background process, but the device is running moderately low on memory. Your running process may want to release some unneeded resources for use elsewhere. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2.html#TRIM_MEMORY_UI_HIDDEN:kotlin.Int` Level for onTrimMemory: the process had been showing a user interface, and is no longer doing so. Large allocations with the UI should be released at this point to allow memory to be better managed. <br /> | ||

| Public constructors ||
|---|---|
| ListFragment <br /> |

| Public methods ||
|---|---|
| open [ListAdapter](../android.widget/ListAdapter.md)! | getListAdapter Get the ListAdapter associated with this fragment's ListView. |
| open [ListView](../android.widget/ListView.md)! | getListView Get the fragment's list view widget. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getSelectedItemId Get the cursor row ID of the currently selected list item. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSelectedItemPosition Get the position of the currently selected list item. |
| open [View](../android.view/View.md)? | onCreateView Provide default implementation to return a simple list view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onDestroyView Detach from list view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onListItemClick This method will be called when an item in the list is selected. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onViewCreated Attach to list view once the view hierarchy has been created. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setEmptyText The default content for a ListFragment has a TextView that can be shown when the list is empty. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setListAdapter Provide the cursor for the list view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setListShown Control whether the list is being displayed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setListShownNoAnimation Like setListShown, but no animation is used when transitioning from the previous state. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setSelection Set the currently selected list item to the specified position with the adapter's data |

| Inherited functions ||
|---|---|
| From class Fragment |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | dump Print the Fragments's state into the given stream. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | equals Subclasses can not override equals(). <br /> | | `https://developer.android.com/reference/kotlin/android/app/Activity!` | getActivity Return the Activity this fragment is currently associated with. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getAllowEnterTransitionOverlap Returns whether the exit transition and enter transition overlap or not. When true, the enter transition will start as soon as possible. When false, the enter transition will wait until the exit transition completes before starting. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getAllowReturnTransitionOverlap Returns whether the return transition and reenter transition overlap or not. When true, the reenter transition will start as soon as possible. When false, the reenter transition will wait until the return transition completes before starting. <br /> | | `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | getArguments Return the arguments supplied to setArguments, if any. <br /> | | `https://developer.android.com/reference/kotlin/android/app/FragmentManager!` | getChildFragmentManager Return a private FragmentManager for placing and managing Fragments inside of this Fragment. <br /> | | `https://developer.android.com/reference/kotlin/android/content/Context.html#!` | getContext Return the `https://developer.android.com/reference/kotlin/android/content/Context.html#` this fragment is currently associated with. <br /> | | `https://developer.android.com/reference/kotlin/android/transition/Transition.html#!` | getEnterTransition Returns the Transition that will be used to move Views into the initial scene. The entering Views will be those that are regular Views or ViewGroups that have isTransitionGroup return true. Typical Transitions will extend `https://developer.android.com/reference/kotlin/android/transition/Visibility.html#` as entering is governed by changing visibility from `https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int`. <br /> | | `https://developer.android.com/reference/kotlin/android/transition/Transition.html#!` | getExitTransition Returns the Transition that will be used to move Views out of the scene when the fragment is removed, hidden, or detached when not popping the back stack. The exiting Views will be those that are regular Views or ViewGroups that have isTransitionGroup return true. Typical Transitions will extend `https://developer.android.com/reference/kotlin/android/transition/Visibility.html#` as exiting is governed by changing visibility from `https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int`. If transition is null, the views will remain unaffected. <br /> | | `https://developer.android.com/reference/kotlin/android/app/FragmentManager!` | getFragmentManager Return the FragmentManager for interacting with fragments associated with this fragment's activity. Note that this will be non-null slightly before getActivity, during the time from when the fragment is placed in a FragmentTransaction until it is committed and attached to its activity. If this Fragment is a child of another Fragment, the FragmentManager returned here will be the parent's getChildFragmentManager. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?` | getHost Return the host object of this fragment. May return `null` if the fragment isn't currently being hosted. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getId Return the identifier this fragment is known by. This is either the android:id value supplied in a layout or the container view ID supplied when adding the fragment. <br /> | | `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#!` | getLayoutInflater Returns the cached LayoutInflater used to inflate Views of this Fragment. If onGetLayoutInflater has not been called onGetLayoutInflater will be called with a `null` argument and that value will be cached. The cached LayoutInflater will be replaced immediately prior to onCreateView and cleared immediately after onDetach. <br /> | | `https://developer.android.com/reference/kotlin/android/app/LoaderManager!` | getLoaderManager Return the LoaderManager for this fragment, creating it if needed. <br /> | | `https://developer.android.com/reference/kotlin/android/app/Fragment!` | getParentFragment Returns the parent Fragment containing this Fragment. If this Fragment is attached directly to an Activity, returns null. <br /> | | `https://developer.android.com/reference/kotlin/android/transition/Transition.html#!` | getReenterTransition Returns the Transition that will be used to move Views in to the scene when returning due to popping a back stack. The entering Views will be those that are regular Views or ViewGroups that have isTransitionGroup return true. Typical Transitions will extend `https://developer.android.com/reference/kotlin/android/transition/Visibility.html#` as exiting is governed by changing visibility from `https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int`. If transition is null, the views will remain unaffected. If nothing is set, the default will be to use the same transition as setExitTransition. <br /> | | `https://developer.android.com/reference/kotlin/android/content/res/Resources.html#!` | getResources Return `getActivity().getResources()`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getRetainInstance <br /> | | `https://developer.android.com/reference/kotlin/android/transition/Transition.html#!` | getReturnTransition Returns the Transition that will be used to move Views out of the scene when the Fragment is preparing to be removed, hidden, or detached because of popping the back stack. The exiting Views will be those that are regular Views or ViewGroups that have isTransitionGroup return true. Typical Transitions will extend `https://developer.android.com/reference/kotlin/android/transition/Visibility.html#` as entering is governed by changing visibility from `https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int`. If `transition` is null, entering Views will remain unaffected. <br /> | | `https://developer.android.com/reference/kotlin/android/transition/Transition.html#!` | getSharedElementEnterTransition Returns the Transition that will be used for shared elements transferred into the content Scene. Typical Transitions will affect size and location, such as `https://developer.android.com/reference/kotlin/android/transition/ChangeBounds.html#`. A null value will cause transferred shared elements to blink to the final position. <br /> | | `https://developer.android.com/reference/kotlin/android/transition/Transition.html#!` | getSharedElementReturnTransition Return the Transition that will be used for shared elements transferred back during a pop of the back stack. This Transition acts in the leaving Fragment. Typical Transitions will affect size and location, such as `https://developer.android.com/reference/kotlin/android/transition/ChangeBounds.html#`. A null value will cause transferred shared elements to blink to the final position. If no value is set, the default will be to use the same value as setSharedElementEnterTransition. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getString Return a localized string from the application's package's default string table. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getString Return a localized formatted string from the application's package's default string table, substituting the format arguments as defined in `https://developer.android.com/reference/kotlin/java/util/Formatter.html#` and java.lang.String#format. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getTag Get the tag name of the fragment, if specified. <br /> | | `https://developer.android.com/reference/kotlin/android/app/Fragment!` | getTargetFragment Return the target fragment set by setTargetFragment. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getTargetRequestCode Return the target request code set by setTargetFragment. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | getText Return a localized, styled CharSequence from the application's package's default string table. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getUserVisibleHint <br /> | | `https://developer.android.com/reference/kotlin/android/view/View.html#?` | getView Get the root view for the fragment's layout (the one returned by onCreateView), if provided. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | hashCode Subclasses can not override hashCode(). <br /> | | `https://developer.android.com/reference/kotlin/android/app/Fragment!` | instantiate Like instantiate but with a null argument Bundle. <br /> | | `https://developer.android.com/reference/kotlin/android/app/Fragment!` | instantiate Create a new instance of a Fragment with the given class name. This is the same as calling its empty constructor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isAdded Return true if the fragment is currently added to its activity. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isDetached Return true if the fragment has been explicitly detached from the UI. That is, detach has been used on it. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isHidden Return true if the fragment has been hidden. By default fragments are shown. You can find out about changes to this state with onHiddenChanged. Note that the hidden state is orthogonal to other states -- that is, to be visible to the user, a fragment must be both started and not hidden. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isInLayout Return true if the layout is included as part of an activity view hierarchy via the \<fragment\> tag. This will always be true when fragments are created through the \<fragment\> tag, *except* in the case where an old fragment is restored from a previous state and it does not appear in the layout of the current state. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isRemoving Return true if this fragment is currently being removed from its activity. This is *not* whether its activity is finishing, but rather whether it is in the process of being removed from its activity. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isResumed Return true if the fragment is in the resumed state. This is true for the duration of onResume and onPause as well. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isStateSaved Returns true if this fragment is added and its state has already been saved by its host. Any operations that would change saved state should not be performed if this method returns true, and some operations such as setArguments will fail. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isVisible Return true if the fragment is currently visible to the user. This means it: (1) has been added, (2) has its view attached to the window, and (3) is not hidden. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onActivityCreated Called when the fragment's activity has been created and this fragment's view hierarchy instantiated. It can be used to do final initialization once these pieces are in place, such as retrieving views or restoring state. It is also useful for fragments that use setRetainInstance to retain their instance, as this callback tells the fragment when it is fully associated with the new activity instance. This is called after onCreateView and before onViewStateRestored. If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onActivityResult Receive the result from a previous call to startActivityForResult. This follows the related Activity API as described there in onActivityResult. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onAttach If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onAttach Called when a fragment is first attached to its context. onCreate will be called after this. If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onAttachFragment Called when a fragment is attached as a child of this fragment. This is called after the attached fragment's `onAttach` and before the attached fragment's `onCreate` if the fragment has not yet had a previous call to `onCreate`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onConfigurationChanged Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources. At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration. For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html). If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onContextItemSelected This hook is called whenever an item in a context menu is selected. The default implementation simply returns false to have the normal processing happen (calling the item's Runnable or sending a message to its Handler as appropriate). You can use this method for any items for which you would like to do processing without those other facilities. Use getMenuInfo to get extra information set by the View that added this menu item. Derived classes should call through to the base class for it to perform the default menu handling. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onCreate Called to do initial creation of a fragment. This is called after onAttach and before onCreateView, but is not called if the fragment instance is retained across Activity re-creation (see setRetainInstance). Note that this can be called while the fragment's activity is still in the process of being created. As such, you can not rely on things like the activity's content view hierarchy being initialized at this point. If you want to do work once the activity itself is created, see onActivityCreated. If your app's `targetSdkVersion` is `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int` or lower, child fragments being restored from the savedInstanceState are restored after `onCreate` returns. When targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int` or above and running on an N or newer platform version they are restored by `Fragment.onCreate`. . If you override this method you *must* call through to the superclass implementation. <br /> | | `https://developer.android.com/reference/kotlin/android/animation/Animator.html#!` | onCreateAnimator Called when a fragment loads an animation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onCreateContextMenu Called when a context menu for the `view` is about to be shown. Unlike onCreateOptionsMenu, this will be called every time the context menu is about to be shown and should be populated for the view (or item inside the view for `https://developer.android.com/reference/kotlin/android/widget/AdapterView.html#` subclasses, this can be found in the `menuInfo`)). Use onContextItemSelected to know when an item has been selected. The default implementation calls up to onCreateContextMenu, though you can not call this implementation if you don't want that behavior. It is not safe to hold onto the context menu after this method returns. Called when the context menu for this view is being built. It is not safe to hold onto the menu after this method returns. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onCreateOptionsMenu Initialize the contents of the Activity's standard options menu. You should place your menu items in to menu. For this method to be called, you must have first called setHasOptionsMenu. See onCreateOptionsMenu for more information. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onDestroy Called when the fragment is no longer in use. This is called after onStop and before onDetach. If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onDestroyOptionsMenu Called when this fragment's option menu items are no longer being included in the overall options menu. Receiving this call means that the menu needed to be rebuilt, but this fragment's items were not included in the newly built menu (its onCreateOptionsMenu was not called). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onDetach Called when the fragment is no longer attached to its activity. This is called after onDestroy, except in the cases where the fragment instance is retained across Activity re-creation (see setRetainInstance), in which case it is called after onStop. If you override this method you *must* call through to the superclass implementation. <br /> | | `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#!` | onGetLayoutInflater Returns the LayoutInflater used to inflate Views of this Fragment. The default implementation will throw an exception if the Fragment is not attached. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onHiddenChanged Called when the hidden state (as returned by isHidden of the fragment has changed. Fragments start out not hidden; this will be called whenever the fragment changes state from that. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onInflate If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onInflate Called when a fragment is being created as part of a view layout inflation, typically from setting the content view of an activity. This may be called immediately after the fragment is created from a tag in a layout file. Note this is *before* the fragment's onAttach has been called; all you should do here is parse the attributes and save them away. This is called every time the fragment is inflated, even if it is being inflated into a new instance with saved state. It typically makes sense to re-parse the parameters each time, to allow them to change with different configurations. Here is a typical implementation of a fragment that can take parameters both through attributes supplied here as well from getArguments: Note that parsing the XML attributes uses a "styleable" resource. The declaration for the styleable used here is: The fragment can then be declared within its activity's content layout through a tag like this: This fragment can also be created dynamically from arguments given at runtime in the arguments Bundle; here is an example of doing so at creation of the containing activity: <br /> If you override this method you *must* call through to the superclass implementation. <br /> <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onInflate If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onLowMemory This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing. If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onMultiWindowModeChanged Called when the Fragment's activity changes from fullscreen mode to multi-window mode and visa-versa. This is generally tied to android.app.Activity#onMultiWindowModeChanged of the containing Activity. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onMultiWindowModeChanged Called when the Fragment's activity changes from fullscreen mode to multi-window mode and visa-versa. This is generally tied to android.app.Activity#onMultiWindowModeChanged of the containing Activity. This method provides the same configuration that will be sent in the following onConfigurationChanged call after the activity enters this mode. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onOptionsItemSelected This hook is called whenever an item in your options menu is selected. The default implementation simply returns false to have the normal processing happen (calling the item's Runnable or sending a message to its Handler as appropriate). You can use this method for any items for which you would like to do processing without those other facilities. Derived classes should call through to the base class for it to perform the default menu handling. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onOptionsMenuClosed This hook is called whenever the options menu is being closed (either by the user canceling the menu with the back/menu button, or when an item is selected). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onPause Called when the Fragment is no longer resumed. This is generally tied to onPause of the containing Activity's lifecycle. If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onPictureInPictureModeChanged Called by the system when the activity changes to and from picture-in-picture mode. This is generally tied to android.app.Activity#onPictureInPictureModeChanged of the containing Activity. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onPictureInPictureModeChanged Called by the system when the activity changes to and from picture-in-picture mode. This is generally tied to android.app.Activity#onPictureInPictureModeChanged of the containing Activity. This method provides the same configuration that will be sent in the following onConfigurationChanged call after the activity enters this mode. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onPrepareOptionsMenu Prepare the Screen's standard options menu to be displayed. This is called right before the menu is shown, every time it is shown. You can use this method to efficiently enable/disable items or otherwise dynamically modify the contents. See onPrepareOptionsMenu for more information. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onRequestPermissionsResult Callback for the result from requesting permissions. This method is invoked for every call on requestPermissions. **Note:** It is possible that the permissions request interaction with the user is interrupted. In this case you will receive empty permissions and results arrays which should be treated as a cancellation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onResume Called when the fragment is visible to the user and actively running. This is generally tied to onResume of the containing Activity's lifecycle. If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onSaveInstanceState Called to ask the fragment to save its current dynamic state, so it can later be reconstructed in a new instance of its process is restarted. If a new instance of the fragment later needs to be created, the data you place in the Bundle here will be available in the Bundle given to onCreate, onCreateView, and onActivityCreated. This corresponds to onSaveInstanceState and most of the discussion there applies here as well. Note however: *this method may be called at any time before onDestroy*. There are many situations where a fragment may be mostly torn down (such as when placed on the back stack with no UI showing), but its state will not be saved until its owning activity actually needs to save its state. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onStart Called when the Fragment is visible to the user. This is generally tied to onStart of the containing Activity's lifecycle. If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onStop Called when the Fragment is no longer started. This is generally tied to onStop of the containing Activity's lifecycle. If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onTrimMemory Called when the operating system has determined that it is a good time for a process to trim unneeded memory from its process. You should never compare to exact values of the level, since new intermediate values may be added -- you will typically want to compare if the value is greater or equal to a level you are interested in. To retrieve the processes current trim level at any point, you can use getMyMemoryState. If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onViewStateRestored Called when all saved state has been restored into the view hierarchy of the fragment. This can be used to do initialization based on saved state that you are letting the view hierarchy track itself, such as whether check box widgets are currently checked. This is called after onActivityCreated and before onStart. If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | postponeEnterTransition Postpone the entering Fragment transition until startPostponedEnterTransition or executePendingTransactions has been called. This method gives the Fragment the ability to delay Fragment animations until all data is loaded. Until then, the added, shown, and attached Fragments will be INVISIBLE and removed, hidden, and detached Fragments won't be have their Views removed. The transaction runs when all postponed added Fragments in the transaction have called startPostponedEnterTransition. This method should be called before being added to the FragmentTransaction or in onCreate, onAttach, or onCreateView}. startPostponedEnterTransition must be called to allow the Fragment to start the transitions. When a FragmentTransaction is started that may affect a postponed FragmentTransaction, based on which containers are in their operations, the postponed FragmentTransaction will have its start triggered. The early triggering may result in faulty or nonexistent animations in the postponed transaction. FragmentTransactions that operate only on independent containers will not interfere with each other's postponement. Calling postponeEnterTransition on Fragments with a null View will not postpone the transition. Likewise, postponement only works if FragmentTransaction optimizations are enabled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | registerForContextMenu Registers a context menu to be shown for the given view (multiple views can show the context menu). This method will set the `https://developer.android.com/reference/kotlin/android/view/View.OnCreateContextMenuListener.html#` on the view to this fragment, so onCreateContextMenu will be called when it is time to show the context menu. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | requestPermissions Requests permissions to be granted to this application. These permissions must be requested in your manifest, they should not be granted to your app, and they should have protection level `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#`, regardless whether they are declared by the platform or a third-party app. Normal permissions `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#PROTECTION_NORMAL:kotlin.Int` are granted at install time if requested in the manifest. Signature permissions `https://developer.android.com/reference/kotlin/android/content/pm/PermissionInfo.html#PROTECTION_SIGNATURE:kotlin.Int` are granted at install time if requested in the manifest and the signature of your app matches the signature of the app declaring the permissions. Call shouldShowRequestPermissionRationale before calling this API to check if the system recommends to show a rationale UI before asking for a permission. If your app does not have the requested permissions the user will be presented with UI for accepting them. After the user has accepted or rejected the requested permissions you will receive a callback on onRequestPermissionsResult reporting whether the permissions were granted or not. Note that requesting a permission does not guarantee it will be granted and your app should be able to run without having this permission. This method may start an activity allowing the user to choose which permissions to grant and which to reject. Hence, you should be prepared that your activity may be paused and resumed. Further, granting some permissions may require a restart of you application. In such a case, the system will recreate the activity stack before delivering the result to onRequestPermissionsResult. When checking whether you have a permission you should use checkSelfPermission. Calling this API for permissions already granted to your app would show UI to the user to decide whether the app can still hold these permissions. This can be useful if the way your app uses data guarded by the permissions changes significantly. You cannot request a permission if your activity sets `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestActivity_noHistory:kotlin.Int` to `true` because in this case the activity would not receive result callbacks including onRequestPermissionsResult. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setAllowEnterTransitionOverlap Sets whether the exit transition and enter transition overlap or not. When true, the enter transition will start as soon as possible. When false, the enter transition will wait until the exit transition completes before starting. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setAllowReturnTransitionOverlap Sets whether the return transition and reenter transition overlap or not. When true, the reenter transition will start as soon as possible. When false, the reenter transition will wait until the return transition completes before starting. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setArguments Supply the construction arguments for this fragment. The arguments supplied here will be retained across fragment destroy and creation. This method cannot be called if the fragment is added to a FragmentManager and if isStateSaved would return true. Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int`, this method may only be called if the fragment has not yet been added to a FragmentManager. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setEnterSharedElementCallback When custom transitions are used with Fragments, the enter transition callback is called when this Fragment is attached or detached when not popping the back stack. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setEnterTransition Sets the Transition that will be used to move Views into the initial scene. The entering Views will be those that are regular Views or ViewGroups that have isTransitionGroup return true. Typical Transitions will extend `https://developer.android.com/reference/kotlin/android/transition/Visibility.html#` as entering is governed by changing visibility from `https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int`. If `transition` is null, entering Views will remain unaffected. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setExitSharedElementCallback When custom transitions are used with Fragments, the exit transition callback is called when this Fragment is attached or detached when popping the back stack. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setExitTransition Sets the Transition that will be used to move Views out of the scene when the fragment is removed, hidden, or detached when not popping the back stack. The exiting Views will be those that are regular Views or ViewGroups that have isTransitionGroup return true. Typical Transitions will extend `https://developer.android.com/reference/kotlin/android/transition/Visibility.html#` as exiting is governed by changing visibility from `https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int`. If transition is null, the views will remain unaffected. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setHasOptionsMenu Report that this fragment would like to participate in populating the options menu by receiving a call to onCreateOptionsMenu and related methods. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setInitialSavedState Set the initial saved state that this Fragment should restore itself from when first being constructed, as returned by saveFragmentInstanceState. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setMenuVisibility Set a hint for whether this fragment's menu should be visible. This is useful if you know that a fragment has been placed in your view hierarchy so that the user can not currently seen it, so any menu items it has should also not be shown. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setReenterTransition Sets the Transition that will be used to move Views in to the scene when returning due to popping a back stack. The entering Views will be those that are regular Views or ViewGroups that have isTransitionGroup return true. Typical Transitions will extend `https://developer.android.com/reference/kotlin/android/transition/Visibility.html#` as exiting is governed by changing visibility from `https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int`. If transition is null, the views will remain unaffected. If nothing is set, the default will be to use the same transition as setExitTransition. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setRetainInstance Control whether a fragment instance is retained across Activity re-creation (such as from a configuration change). This can only be used with fragments not in the back stack. If set, the fragment lifecycle will be slightly different when an activity is recreated: - onDestroy will not be called (but onDetach still will be, because the fragment is being detached from its current activity). - onCreate will not be called since the fragment is not being re-created. - onAttach and onActivityCreated **will** still be called. <br /> <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setReturnTransition Sets the Transition that will be used to move Views out of the scene when the Fragment is preparing to be removed, hidden, or detached because of popping the back stack. The exiting Views will be those that are regular Views or ViewGroups that have isTransitionGroup return true. Typical Transitions will extend `https://developer.android.com/reference/kotlin/android/transition/Visibility.html#` as entering is governed by changing visibility from `https://developer.android.com/reference/kotlin/android/view/View.html#VISIBLE:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int`. If `transition` is null, entering Views will remain unaffected. If nothing is set, the default will be to use the same value as set in setEnterTransition. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setSharedElementEnterTransition Sets the Transition that will be used for shared elements transferred into the content Scene. Typical Transitions will affect size and location, such as `https://developer.android.com/reference/kotlin/android/transition/ChangeBounds.html#`. A null value will cause transferred shared elements to blink to the final position. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setSharedElementReturnTransition Sets the Transition that will be used for shared elements transferred back during a pop of the back stack. This Transition acts in the leaving Fragment. Typical Transitions will affect size and location, such as `https://developer.android.com/reference/kotlin/android/transition/ChangeBounds.html#`. A null value will cause transferred shared elements to blink to the final position. If no value is set, the default will be to use the same value as setSharedElementEnterTransition. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setTargetFragment Optional target for this fragment. This may be used, for example, if this fragment is being started by another, and when done wants to give a result back to the first. The target set here is retained across instances via putFragment. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setUserVisibleHint Set a hint to the system about whether this fragment's UI is currently visible to the user. This hint defaults to true and is persistent across fragment instance state save and restore. An app may set this to false to indicate that the fragment's UI is scrolled out of visibility or is otherwise not directly visible to the user. This may be used by the system to prioritize operations such as fragment lifecycle updates or loader ordering behavior. **Note:** This method may be called outside of the fragment lifecycle and thus has no ordering guarantees with regard to fragment lifecycle method calls. **Note:** Prior to Android N there was a platform bug that could cause `setUserVisibleHint` to bring a fragment up to the started state before its `FragmentTransaction` had been committed. As some apps relied on this behavior, it is preserved for apps that declare a `targetSdkVersion` of 23 or lower. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | shouldShowRequestPermissionRationale Gets whether you should show UI with rationale before requesting a permission. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | startActivity Call android.app.Activity#startActivity(android.content.Intent) from the fragment's containing Activity. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | startActivity Call android.app.Activity#startActivity(android.content.Intent,android.os.Bundle) from the fragment's containing Activity. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | startActivityForResult Call startActivityForResult from the fragment's containing Activity. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | startActivityForResult Call startActivityForResult from the fragment's containing Activity. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | startIntentSenderForResult Call startIntentSenderForResult from the fragment's containing Activity. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | startPostponedEnterTransition Begin postponed transitions after postponeEnterTransition was called. If postponeEnterTransition() was called, you must call startPostponedEnterTransition() or executePendingTransactions to complete the FragmentTransaction. If postponement was interrupted with executePendingTransactions, before `startPostponedEnterTransition()`, animations may not run or may execute improperly. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | toString Returns a string representation of the object. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | unregisterForContextMenu Prevents a context menu to be shown for the given view. This method will remove the `https://developer.android.com/reference/kotlin/android/view/View.OnCreateContextMenuListener.html#` on the view. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onConfigurationChanged Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources. At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration. For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onLowMemory This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing. <br /> | ||

## Public constructors

### ListFragment

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ListFragment()
```

## Public methods

### getListAdapter

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getListAdapter(): ListAdapter!
```

**Deprecated:** *Deprecated in Java.*

Get the ListAdapter associated with this fragment's ListView.

### getListView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getListView(): ListView!
```

**Deprecated:** *Deprecated in Java.*

Get the fragment's list view widget.

### getSelectedItemId

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSelectedItemId(): Long
```

**Deprecated:** *Deprecated in Java.*

Get the cursor row ID of the currently selected list item.

### getSelectedItemPosition

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSelectedItemPosition(): Int
```

**Deprecated:** *Deprecated in Java.*

Get the position of the currently selected list item.

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

Provide default implementation to return a simple list view. Subclasses can override to replace with their own layout. If doing so, the returned view hierarchy *must* have a ListView whose id is `https://developer.android.com/reference/kotlin/android/R.id.html#list:kotlin.Int` and can optionally have a sibling view id `https://developer.android.com/reference/kotlin/android/R.id.html#empty:kotlin.Int` that is to be shown when the list is empty.

If you are overriding this method with your own custom content, consider including the standard layout `https://developer.android.com/reference/kotlin/android/R.layout.html#list_content:kotlin.Int` in your layout file, so that you continue to retain all of the standard behavior of ListFragment. In particular, this is currently the only way to have the built-in indeterminant progress state be shown.

| Parameters ||
|---|---|
| `inflater` | [LayoutInflater](../android.view/LayoutInflater.md)!: The LayoutInflater object that can be used to inflate any views in the fragment, |
| `container` | [ViewGroup](../android.view/ViewGroup.md)?: If non-null, this is the parent view that the fragment's UI should be attached to. The fragment should not add the view itself, but this can be used to generate the LayoutParams of the view. |
| `savedInstanceState` | [Bundle](../android.os/Bundle.md)!: If non-null, this fragment is being re-constructed from a previous saved state as given here. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View.html#?` | Return the View for the fragment's UI, or null. |

### onDestroyView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDestroyView(): Unit
```

**Deprecated:** *Deprecated in Java.*

Detach from list view.

### onListItemClick

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onListItemClick(
    l: ListView!, 
    v: View!, 
    position: Int, 
    id: Long
): Unit
```

**Deprecated:** *Deprecated in Java.*

This method will be called when an item in the list is selected. Subclasses should override. Subclasses can call getListView().getItemAtPosition(position) if they need to access the data associated with the selected item.

| Parameters ||
|---|---|
| `l` | [ListView](../android.widget/ListView.md)!: The ListView where the click happened |
| `v` | [View](../android.view/View.md)!: The view that was clicked within the ListView |
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The position of the view in the list |
| --- | --- |
| `id` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The row id of the item that was clicked |

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

Attach to list view once the view hierarchy has been created.

| Parameters ||
|---|---|
| `view` | [View](../android.view/View.md)!: The View returned by onCreateView. |
| `savedInstanceState` | [Bundle](../android.os/Bundle.md)?: If non-null, this fragment is being re-constructed from a previous saved state as given here. |

### setEmptyText

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setEmptyText(text: CharSequence!): Unit
```

**Deprecated:** *Deprecated in Java.*

The default content for a ListFragment has a TextView that can be shown when the list is empty. If you would like to have it shown, call this method to supply the text it should use.

### setListAdapter

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setListAdapter(adapter: ListAdapter!): Unit
```

**Deprecated:** *Deprecated in Java.*

Provide the cursor for the list view.

### setListShown

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setListShown(shown: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Control whether the list is being displayed. You can make it not displayed if you are waiting for the initial data to show in it. During this time an indeterminant progress indicator will be shown instead.

Applications do not normally need to use this themselves. The default behavior of ListFragment is to start with the list not being shown, only showing it once an adapter is given with setListAdapter. If the list at that point had not been shown, when it does get shown it will be do without the user ever seeing the hidden state.

| Parameters ||
|---|---|
| `shown` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, the list view is shown; if false, the progress indicator. The initial value is true. |

### setListShownNoAnimation

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setListShownNoAnimation(shown: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Like setListShown, but no animation is used when transitioning from the previous state.

### setSelection

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSelection(position: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the currently selected list item to the specified position with the adapter's data

| Parameters ||
|---|---|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
