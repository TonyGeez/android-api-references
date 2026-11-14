# android.app

## Interfaces

| [OnMenuVisibilityListener](https://developer.android.com/reference/kotlin/android/app/ActionBar.OnMenuVisibilityListener) | Listener for receiving events when action bar menus are shown or hidden. |
| --- | --- |
| [OnNavigationListener](https://developer.android.com/reference/kotlin/android/app/ActionBar.OnNavigationListener) | Listener interface for ActionBar navigation events. |
| [TabListener](https://developer.android.com/reference/kotlin/android/app/ActionBar.TabListener) | Callback interface invoked when a tab is focused, unfocused, added, or removed. |
| [ScreenCaptureCallback](https://developer.android.com/reference/kotlin/android/app/Activity.ScreenCaptureCallback) | Interface for observing screen captures of an `https://developer.android.com/reference/kotlin/android/app/Activity`. |
| --- | --- |
| [OnAlarmListener](https://developer.android.com/reference/kotlin/android/app/AlarmManager.OnAlarmListener) | Direct-notification alarms: the requester must be running continuously from the time the alarm is set to the time it is delivered, or delivery will fail. |
| [LifecycleListener](https://developer.android.com/reference/kotlin/android/app/AppInteractionSession.LifecycleListener) | Listener for session lifecycle events. |
| [ActivityLifecycleCallbacks](https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks) | <br /> |
| --- | --- |
| [OnProvideAssistDataListener](https://developer.android.com/reference/kotlin/android/app/Application.OnProvideAssistDataListener) | Callback interface for use with `https://developer.android.com/reference/kotlin/android/app/Application#registerOnProvideAssistDataListener(android.app.Application.OnProvideAssistDataListener)` and `https://developer.android.com/reference/kotlin/android/app/Application#unregisterOnProvideAssistDataListener(android.app.Application.OnProvideAssistDataListener)`. |
| [OnOpActiveChangedListener](https://developer.android.com/reference/kotlin/android/app/AppOpsManager.OnOpActiveChangedListener) | Callback for notification of changes to operation active state. |
| [OnOpChangedListener](https://developer.android.com/reference/kotlin/android/app/AppOpsManager.OnOpChangedListener) | Callback for notification of changes to operation state. |
| --- | --- |
| [OnDateSetListener](https://developer.android.com/reference/kotlin/android/app/DatePickerDialog.OnDateSetListener) | The listener used to indicate the user has finished selecting a date. |
| [OnBreadCrumbClickListener](https://developer.android.com/reference/kotlin/android/app/FragmentBreadCrumbs.OnBreadCrumbClickListener) | Interface to intercept clicks on the bread crumbs. |
| [BackStackEntry](https://developer.android.com/reference/kotlin/android/app/FragmentManager.BackStackEntry) | Representation of an entry on the fragment back stack, as created with `https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#addToBackStack(kotlin.String)`. |
| --- | --- |
| [OnBackStackChangedListener](https://developer.android.com/reference/kotlin/android/app/FragmentManager.OnBackStackChangedListener) | Interface to watch for changes to the back stack. |
| [DeviceLockedStateListener](https://developer.android.com/reference/kotlin/android/app/KeyguardManager.DeviceLockedStateListener) | Listener for device locked state changes. |
| [KeyguardLockedStateListener](https://developer.android.com/reference/kotlin/android/app/KeyguardManager.KeyguardLockedStateListener) | Listener for keyguard locked state changes. |
| --- | --- |
| [OnKeyguardExitResult](https://developer.android.com/reference/kotlin/android/app/KeyguardManager.OnKeyguardExitResult) | Callback passed to `https://developer.android.com/reference/kotlin/android/app/KeyguardManager#exitKeyguardSecurely(android.app.KeyguardManager.OnKeyguardExitResult)` to notify caller of result. |
| [LoaderCallbacks](https://developer.android.com/reference/kotlin/android/app/LoaderManager.LoaderCallbacks) | Callback interface for a client to interact with the manager. |
| [OnOverBudgetListener](https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager.OnOverBudgetListener) | The callback that is notified when a budget is exceeded. |
| --- | --- |
| [Extender](https://developer.android.com/reference/kotlin/android/app/Notification.Extender) | Extender interface for use with `https://developer.android.com/reference/kotlin/android/app/Notification.Builder#extend(android.app.Notification.Extender)`. |
| [OnFinished](https://developer.android.com/reference/kotlin/android/app/PendingIntent.OnFinished) | Callback interface for discovering when a send operation has completed. |
| [OnCancelListener](https://developer.android.com/reference/kotlin/android/app/SearchManager.OnCancelListener) | See `https://developer.android.com/reference/kotlin/android/app/SearchManager#setOnCancelListener(android.app.SearchManager.OnCancelListener)` for configuring your activity to monitor search UI state. |
| --- | --- |
| [OnDismissListener](https://developer.android.com/reference/kotlin/android/app/SearchManager.OnDismissListener) | See `https://developer.android.com/reference/kotlin/android/app/SearchManager#setOnDismissListener(android.app.SearchManager.OnDismissListener)` for configuring your activity to monitor search UI state. |
| [OnSharedElementsReadyListener](https://developer.android.com/reference/kotlin/android/app/SharedElementCallback.OnSharedElementsReadyListener) | Listener to be called after `https://developer.android.com/reference/kotlin/android/app/SharedElementCallback#onSharedElementsArrived(kotlin.collections.MutableList,%20kotlin.collections.MutableList,%20android.app.SharedElementCallback.OnSharedElementsReadyListener)` when the shared elements are ready to be hidden in the source Activity and shown in the destination Activity. |
| [OnTimeSetListener](https://developer.android.com/reference/kotlin/android/app/TimePickerDialog.OnTimeSetListener) | The callback interface used to indicate the user is done filling in the time (e.g. they clicked on the 'OK' button). |
| --- | --- |
| [AccessibilityEventFilter](https://developer.android.com/reference/kotlin/android/app/UiAutomation.AccessibilityEventFilter) | Listener for filtering accessibility events. |
| [OnAccessibilityEventListener](https://developer.android.com/reference/kotlin/android/app/UiAutomation.OnAccessibilityEventListener) | Listener for observing the `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#` stream. |
| [ContrastChangeListener](https://developer.android.com/reference/kotlin/android/app/UiModeManager.ContrastChangeListener) | Listener for the UI contrast. |
| --- | --- |
| [OnColorsChangedListener](https://developer.android.com/reference/kotlin/android/app/WallpaperManager.OnColorsChangedListener) | Interface definition for a callback to be invoked when colors change on a wallpaper. |
| [ZygotePreload](https://developer.android.com/reference/kotlin/android/app/ZygotePreload) | This is the interface to be implemented for the class that is specified by the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_zygotePreloadName:kotlin.Int` of the \<application\> tag. |

## Classes

| [ActionBar](https://developer.android.com/reference/kotlin/android/app/ActionBar) | A primary toolbar within the activity that may display the activity title, application-level navigation affordances, and other interactive items. |
| --- | --- |
| [Activity](https://developer.android.com/reference/kotlin/android/app/Activity) | An activity is a single, focused thing that the user can do. |
| [ActivityGroup](https://developer.android.com/reference/kotlin/android/app/ActivityGroup) | A screen that contains and runs multiple embedded activities. |
| [ActivityManager](https://developer.android.com/reference/kotlin/android/app/ActivityManager) | This class gives information about, and interacts with, activities, services, and the containing process. |
| --- | --- |
| [ActivityOptions](https://developer.android.com/reference/kotlin/android/app/ActivityOptions) | Helper class for building an options Bundle that can be used with `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent,%20android.os.Bundle)` and related methods. |
| [AlarmManager](https://developer.android.com/reference/kotlin/android/app/AlarmManager) | This class provides access to the system alarm services. |
| [AlertDialog](https://developer.android.com/reference/kotlin/android/app/AlertDialog) | A subclass of Dialog that can display one, two or three buttons. |
| --- | --- |
| [AliasActivity](https://developer.android.com/reference/kotlin/android/app/AliasActivity) | Stub activity that launches another activity (and then finishes itself) based on information in its component's manifest meta-data. |
| [AnrTypes](https://developer.android.com/reference/kotlin/android/app/AnrTypes) | Defines the types of Application Not Responding (ANR) errors. |
| [AnrWarningResult](https://developer.android.com/reference/kotlin/android/app/AnrWarningResult) | Describes the information about a potential ANR before the timeout is reached. |
| --- | --- |
| [AppComponentFactory](https://developer.android.com/reference/kotlin/android/app/AppComponentFactory) | Interface used to control the instantiation of manifest elements. |
| [AppInteractionAttribution](https://developer.android.com/reference/kotlin/android/app/AppInteractionAttribution) | Represents attribution information for an app interaction, detailing the context and nature of the interaction that triggered it. |
| [AppInteractionContract](https://developer.android.com/reference/kotlin/android/app/AppInteractionContract) | The contract between the App Interaction history provider and applications with read permission. |
| --- | --- |
| [AppInteractionManager](https://developer.android.com/reference/kotlin/android/app/AppInteractionManager) | Provides access to App Interaction access control APIs. |
| [AppInteractionSession](https://developer.android.com/reference/kotlin/android/app/AppInteractionSession) | Represents an app interaction session. |
| [Application](https://developer.android.com/reference/kotlin/android/app/Application) | Base class for maintaining global application state. |
| --- | --- |
| [ApplicationErrorReport](https://developer.android.com/reference/kotlin/android/app/ApplicationErrorReport) | Describes an application error. |
| [ApplicationExitInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationExitInfo) | Describes the information of an application process's death. |
| [ApplicationStartInfo](https://developer.android.com/reference/kotlin/android/app/ApplicationStartInfo) | Describes information related to an application process's startup. |
| --- | --- |
| [AppOpsManager](https://developer.android.com/reference/kotlin/android/app/AppOpsManager) | App-ops are used for two purposes: Access control and tracking. |
| [AsyncNotedAppOp](https://developer.android.com/reference/kotlin/android/app/AsyncNotedAppOp) | When an `https://developer.android.com/reference/kotlin/android/app/AppOpsManager#noteOp(kotlin.String,%20kotlin.Int,%20kotlin.String,%20kotlin.String,%20kotlin.String)` and the app the app-op is noted for has a `https://developer.android.com/reference/kotlin/android/app/AppOpsManager.OnOpNotedCallback` registered the note-event needs to be delivered to the callback. |
| [AutomaticZenRule](https://developer.android.com/reference/kotlin/android/app/AutomaticZenRule) | Rule instance information for a zen (aka DND or Attention Management) mode. |
| --- | --- |
| [BroadcastOptions](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions) | Helper class for building an options Bundle that can be used with `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)` and related methods. |
| [ComponentCaller](https://developer.android.com/reference/kotlin/android/app/ComponentCaller) | Represents the app that launched the component. |
| [DatePickerDialog](https://developer.android.com/reference/kotlin/android/app/DatePickerDialog) | A simple dialog containing an `https://developer.android.com/reference/kotlin/android/widget/DatePicker.html#`. |
| --- | --- |
| [Dialog](https://developer.android.com/reference/kotlin/android/app/Dialog) | Base class for Dialogs. |
| [DialogFragment](https://developer.android.com/reference/kotlin/android/app/DialogFragment) | A fragment that displays a dialog window, floating on top of its activity's window. |
| [DirectAction](https://developer.android.com/reference/kotlin/android/app/DirectAction) | Represents an abstract action that can be perform on this app. |
| --- | --- |
| [DownloadManager](https://developer.android.com/reference/kotlin/android/app/DownloadManager) | The download manager is a system service that handles long-running HTTP downloads. |
| [ExpandableListActivity](https://developer.android.com/reference/kotlin/android/app/ExpandableListActivity) | An activity that displays an expandable list of items by binding to a data source implementing the ExpandableListAdapter, and exposes event handlers when the user selects an item. |
| [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment) | A Fragment is a piece of an application's user interface or behavior that can be placed in an `https://developer.android.com/reference/kotlin/android/app/Activity`. |
| --- | --- |
| [FragmentBreadCrumbs](https://developer.android.com/reference/kotlin/android/app/FragmentBreadCrumbs) | Helper class for showing "bread crumbs" representing the fragment stack in an activity. |
| [FragmentContainer](https://developer.android.com/reference/kotlin/android/app/FragmentContainer) | Callbacks to a `https://developer.android.com/reference/kotlin/android/app/Fragment`'s container. |
| [FragmentController](https://developer.android.com/reference/kotlin/android/app/FragmentController) | Provides integration points with a `https://developer.android.com/reference/kotlin/android/app/FragmentManager` for a fragment host. |
| --- | --- |
| [FragmentHostCallback](https://developer.android.com/reference/kotlin/android/app/FragmentHostCallback) | Integration points with the Fragment host. |
| [FragmentManager](https://developer.android.com/reference/kotlin/android/app/FragmentManager) | Interface for interacting with `https://developer.android.com/reference/kotlin/android/app/Fragment` objects inside of an `https://developer.android.com/reference/kotlin/android/app/Activity` > [!NOTE] > ### Developer Guides > For more information about using fragments, read the [Fragments](https://developer.android.com/guide/components/fragments.html) developer guide. While the FragmentManager API was introduced in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int`, a version of the API at is also available for use on older platforms through androidx. <br /> |
| [FragmentManagerNonConfig](https://developer.android.com/reference/kotlin/android/app/FragmentManagerNonConfig) | FragmentManagerNonConfig stores the retained instance fragments across activity recreation events. |
| --- | --- |
| [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction) | API for performing a set of Fragment operations. |
| [GameManager](https://developer.android.com/reference/kotlin/android/app/GameManager) | The GameManager allows system apps to modify and query the game mode of apps. |
| [GameState](https://developer.android.com/reference/kotlin/android/app/GameState) | State of the game passed to the GameManager. |
| --- | --- |
| [GrammaticalInflectionManager](https://developer.android.com/reference/kotlin/android/app/GrammaticalInflectionManager) | This class allow applications to control granular grammatical inflection settings (such as per-app grammatical gender). |
| [HandoffActivityData](https://developer.android.com/reference/kotlin/android/app/HandoffActivityData) | Represents information needed to recreate an activity on a remote device owned by the user. |
| [HandoffActivityDataRequestInfo](https://developer.android.com/reference/kotlin/android/app/HandoffActivityDataRequestInfo) | Represents a request made by the platform to hand off an activity. |
| --- | --- |
| [HandoffActivityParams](https://developer.android.com/reference/kotlin/android/app/HandoffActivityParams) | Represents options specifying how an activity will be handed off to other devices. |
| [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation) | Base class for implementing application instrumentation code. |
| [IntentService](https://developer.android.com/reference/kotlin/android/app/IntentService) | IntentService is an extension of the `https://developer.android.com/reference/kotlin/android/app/Service` component class that handles asynchronous requests (expressed as `https://developer.android.com/reference/kotlin/android/content/Intent.html#`s) on demand. |
| --- | --- |
| [KeyguardManager](https://developer.android.com/reference/kotlin/android/app/KeyguardManager) | Class to manage and query the state of the lock screen (also known as Keyguard). |
| [LauncherActivity](https://developer.android.com/reference/kotlin/android/app/LauncherActivity) | Displays a list of all activities which can be performed for a given intent. |
| [ListActivity](https://developer.android.com/reference/kotlin/android/app/ListActivity) | An activity that displays a list of items by binding to a data source such as an array or Cursor, and exposes event handlers when the user selects an item. |
| --- | --- |
| [ListFragment](https://developer.android.com/reference/kotlin/android/app/ListFragment) | A fragment that displays a list of items by binding to a data source such as an array or Cursor, and exposes event handlers when the user selects an item. |
| [LoaderManager](https://developer.android.com/reference/kotlin/android/app/LoaderManager) | Interface associated with an `https://developer.android.com/reference/kotlin/android/app/Activity` or `https://developer.android.com/reference/kotlin/android/app/Fragment` for managing one or more `https://developer.android.com/reference/kotlin/android/content/Loader.html#` instances associated with it. |
| [LocalActivityManager](https://developer.android.com/reference/kotlin/android/app/LocalActivityManager) | Helper class for managing multiple running embedded activities in the same process. |
| --- | --- |
| [LocaleConfig](https://developer.android.com/reference/kotlin/android/app/LocaleConfig) | The LocaleConfig of an application. |
| [LocaleManager](https://developer.android.com/reference/kotlin/android/app/LocaleManager) | This class gives access to system locale services. |
| [MediaRouteActionProvider](https://developer.android.com/reference/kotlin/android/app/MediaRouteActionProvider) | The media route action provider displays a `https://developer.android.com/reference/kotlin/android/app/MediaRouteButton` in the application's `https://developer.android.com/reference/kotlin/android/app/ActionBar` to allow the user to select routes and to control the currently selected route. |
| --- | --- |
| [MediaRouteButton](https://developer.android.com/reference/kotlin/android/app/MediaRouteButton) | <br /> |
| [MemoryBudgetManager](https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager) | This class is the client interface to memory budgets for applications and processes. |
| [NativeActivity](https://developer.android.com/reference/kotlin/android/app/NativeActivity) | Convenience for implementing an activity that will be implemented purely in native code. |
| --- | --- |
| [Notification](https://developer.android.com/reference/kotlin/android/app/Notification) | A class that represents how a persistent notification is to be presented to the user using the `https://developer.android.com/reference/kotlin/android/app/NotificationManager`. |
| [NotificationChannel](https://developer.android.com/reference/kotlin/android/app/NotificationChannel) | A representation of settings that apply to a collection of similarly themed notifications. |
| [NotificationChannelGroup](https://developer.android.com/reference/kotlin/android/app/NotificationChannelGroup) | A grouping of related notification channels. |
| --- | --- |
| [NotificationManager](https://developer.android.com/reference/kotlin/android/app/NotificationManager) | Class to notify the user of events that happen. |
| [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent) | A description of an Intent and target action to perform with it. |
| [Person](https://developer.android.com/reference/kotlin/android/app/Person) | Provides an immutable reference to an entity that appears repeatedly on different surfaces of the platform. |
| --- | --- |
| [PictureInPictureParams](https://developer.android.com/reference/kotlin/android/app/PictureInPictureParams) | Represents a set of parameters used to initialize and update an Activity in picture-in-picture mode. |
| [PictureInPictureUiState](https://developer.android.com/reference/kotlin/android/app/PictureInPictureUiState) | Used by `https://developer.android.com/reference/kotlin/android/app/Activity#onPictureInPictureUiStateChanged(android.app.PictureInPictureUiState)`. |
| [Presentation](https://developer.android.com/reference/kotlin/android/app/Presentation) | Base class for presentations. |
| --- | --- |
| [ProgressDialog](https://developer.android.com/reference/kotlin/android/app/ProgressDialog) | A dialog showing a progress indicator and an optional text message or view. |
| [RemoteAction](https://developer.android.com/reference/kotlin/android/app/RemoteAction) | Represents a remote action that can be called from another process. |
| [RemoteInput](https://developer.android.com/reference/kotlin/android/app/RemoteInput) | A `RemoteInput` object specifies input to be collected from a user to be passed along with an intent inside a `https://developer.android.com/reference/kotlin/android/app/PendingIntent` that is sent. |
| --- | --- |
| [SearchableInfo](https://developer.android.com/reference/kotlin/android/app/SearchableInfo) | Searchability meta-data for an activity. |
| [SearchManager](https://developer.android.com/reference/kotlin/android/app/SearchManager) | This class provides access to the system search services. |
| [Service](https://developer.android.com/reference/kotlin/android/app/Service) | A Service is an application component representing either an application's desire to perform a longer-running operation while not interacting with the user or to supply functionality for other applications to use. |
| --- | --- |
| [SharedElementCallback](https://developer.android.com/reference/kotlin/android/app/SharedElementCallback) | Listener provided in `https://developer.android.com/reference/kotlin/android/app/Activity#setEnterSharedElementCallback(android.app.SharedElementCallback)` and `https://developer.android.com/reference/kotlin/android/app/Activity#setExitSharedElementCallback(android.app.SharedElementCallback)` as well as `https://developer.android.com/reference/kotlin/android/app/Fragment#setEnterSharedElementCallback(android.app.SharedElementCallback)` and `https://developer.android.com/reference/kotlin/android/app/Fragment#setExitSharedElementCallback(android.app.SharedElementCallback)` to monitor the Shared element transitions. |
| [StatusBarManager](https://developer.android.com/reference/kotlin/android/app/StatusBarManager) | Allows an app to control the status bar. |
| [SyncNotedAppOp](https://developer.android.com/reference/kotlin/android/app/SyncNotedAppOp) | Description of an app-op that was noted for the current process. |
| --- | --- |
| [TabActivity](https://developer.android.com/reference/kotlin/android/app/TabActivity) | For apps developing against `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int` or later, tabs are typically presented in the UI using the new `https://developer.android.com/reference/kotlin/android/app/ActionBar#newTab()` and related APIs for placing tabs within their action bar area. |
| [TaskInfo](https://developer.android.com/reference/kotlin/android/app/TaskInfo) | Stores information about a particular Task. |
| [TaskLocation](https://developer.android.com/reference/kotlin/android/app/TaskLocation) | Represents location of an `https://developer.android.com/reference/kotlin/android/app/ActivityManager.AppTask` that consists of the host display identifier and rectangular bounds in the pixel-based coordinate system relative to host display. |
| --- | --- |
| [TaskStackBuilder](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder) | Utility class for constructing synthetic back stacks for cross-task navigation on Android 3. |
| [TimePickerDialog](https://developer.android.com/reference/kotlin/android/app/TimePickerDialog) | A dialog that prompts the user for the time of day using a `https://developer.android.com/reference/kotlin/android/widget/TimePicker.html#`. |
| [UiAutomation](https://developer.android.com/reference/kotlin/android/app/UiAutomation) | Class for interacting with the device's UI by simulation user actions and introspection of the screen content. |
| --- | --- |
| [UiModeManager](https://developer.android.com/reference/kotlin/android/app/UiModeManager) | This class provides access to the system uimode services. |
| [VoiceInteractor](https://developer.android.com/reference/kotlin/android/app/VoiceInteractor) | Interface for an `https://developer.android.com/reference/kotlin/android/app/Activity` to interact with the user through voice. |
| [WallpaperColors](https://developer.android.com/reference/kotlin/android/app/WallpaperColors) | Provides information about the colors of a wallpaper. |
| --- | --- |
| [WallpaperInfo](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo) | This class is used to specify meta information of a wallpaper service. |
| [WallpaperManager](https://developer.android.com/reference/kotlin/android/app/WallpaperManager) | Provides access to the system wallpaper. |

## Exceptions

| [AppInteractionDeniedException](https://developer.android.com/reference/kotlin/android/app/AppInteractionDeniedException) | Exception thrown when an app interaction is denied. |
| --- | --- |
| [AppInteractionException](https://developer.android.com/reference/kotlin/android/app/AppInteractionException) | Exception thrown when an app interaction operation fails. |
| [AuthenticationRequiredException](https://developer.android.com/reference/kotlin/android/app/AuthenticationRequiredException) | Specialization of `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` that is thrown when authentication is needed from the end user before viewing the content. |
| [BackgroundServiceStartNotAllowedException](https://developer.android.com/reference/kotlin/android/app/BackgroundServiceStartNotAllowedException) | Exception thrown when an app tries to start a background `https://developer.android.com/reference/kotlin/android/app/Service` when it's not allowed to do so. |
| --- | --- |
| [ForegroundServiceStartNotAllowedException](https://developer.android.com/reference/kotlin/android/app/ForegroundServiceStartNotAllowedException) | Exception thrown when an app tries to start a foreground `https://developer.android.com/reference/kotlin/android/app/Service` when it's not allowed to do so. |
| [ForegroundServiceTypeException](https://developer.android.com/reference/kotlin/android/app/ForegroundServiceTypeException) | Base exception thrown when an app tries to start a foreground `https://developer.android.com/reference/kotlin/android/app/Service` without a valid type. |
| [InfeasibleActivityOptionsException](https://developer.android.com/reference/kotlin/android/app/InfeasibleActivityOptionsException) | This exception is thrown when a call to android. |
| --- | --- |
| [InvalidForegroundServiceTypeException](https://developer.android.com/reference/kotlin/android/app/InvalidForegroundServiceTypeException) | Exception thrown when an app tries to start a foreground `https://developer.android.com/reference/kotlin/android/app/Service` with an invalid type. |
| [MissingForegroundServiceTypeException](https://developer.android.com/reference/kotlin/android/app/MissingForegroundServiceTypeException) | Exception thrown when an app tries to start a foreground `https://developer.android.com/reference/kotlin/android/app/Service` without a type. |
| [RecoverableSecurityException](https://developer.android.com/reference/kotlin/android/app/RecoverableSecurityException) | Specialization of `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` that contains additional information about how to involve the end user to recover from the exception. |
| --- | --- |
| [ServiceStartNotAllowedException](https://developer.android.com/reference/kotlin/android/app/ServiceStartNotAllowedException) | Exception thrown when an app tries to start a `https://developer.android.com/reference/kotlin/android/app/Service` when it's not allowed to do so. |
| [StartForegroundCalledOnStoppedServiceException](https://developer.android.com/reference/kotlin/android/app/StartForegroundCalledOnStoppedServiceException) | Exception thrown when android. |
