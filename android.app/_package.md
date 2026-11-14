# android.app

## Interfaces

| [OnMenuVisibilityListener](../android/app/ActionBar.OnMenuVisibilityListener.md) | Listener for receiving events when action bar menus are shown or hidden. |
| --- | --- |
| [OnNavigationListener](../android/app/ActionBar.OnNavigationListener.md) | Listener interface for ActionBar navigation events. |
| [TabListener](../android/app/ActionBar.TabListener.md) | Callback interface invoked when a tab is focused, unfocused, added, or removed. |
| [ScreenCaptureCallback](../android/app/Activity.ScreenCaptureCallback.md) | Interface for observing screen captures of an Activity. |
| --- | --- |
| [OnAlarmListener](../android/app/AlarmManager.OnAlarmListener.md) | Direct-notification alarms: the requester must be running continuously from the time the alarm is set to the time it is delivered, or delivery will fail. |
| [LifecycleListener](../android/app/AppInteractionSession.LifecycleListener.md) | Listener for session lifecycle events. |
| [ActivityLifecycleCallbacks](../android/app/Application.ActivityLifecycleCallbacks.md) | <br /> |
| --- | --- |
| [OnProvideAssistDataListener](../android/app/Application.OnProvideAssistDataListener.md) | Callback interface for use with registerOnProvideAssistDataListener and unregisterOnProvideAssistDataListener. |
| [OnOpActiveChangedListener](../android/app/AppOpsManager.OnOpActiveChangedListener.md) | Callback for notification of changes to operation active state. |
| [OnOpChangedListener](../android/app/AppOpsManager.OnOpChangedListener.md) | Callback for notification of changes to operation state. |
| --- | --- |
| [OnDateSetListener](../android/app/DatePickerDialog.OnDateSetListener.md) | The listener used to indicate the user has finished selecting a date. |
| [OnBreadCrumbClickListener](../android/app/FragmentBreadCrumbs.OnBreadCrumbClickListener.md) | Interface to intercept clicks on the bread crumbs. |
| [BackStackEntry](../android/app/FragmentManager.BackStackEntry.md) | Representation of an entry on the fragment back stack, as created with addToBackStack. |
| --- | --- |
| [OnBackStackChangedListener](../android/app/FragmentManager.OnBackStackChangedListener.md) | Interface to watch for changes to the back stack. |
| [DeviceLockedStateListener](../android/app/KeyguardManager.DeviceLockedStateListener.md) | Listener for device locked state changes. |
| [KeyguardLockedStateListener](../android/app/KeyguardManager.KeyguardLockedStateListener.md) | Listener for keyguard locked state changes. |
| --- | --- |
| [OnKeyguardExitResult](../android/app/KeyguardManager.OnKeyguardExitResult.md) | Callback passed to exitKeyguardSecurely to notify caller of result. |
| [LoaderCallbacks](../android/app/LoaderManager.LoaderCallbacks.md) | Callback interface for a client to interact with the manager. |
| [OnOverBudgetListener](../android/app/MemoryBudgetManager.OnOverBudgetListener.md) | The callback that is notified when a budget is exceeded. |
| --- | --- |
| [Extender](../android/app/Notification.Extender.md) | Extender interface for use with extend. |
| [OnFinished](../android/app/PendingIntent.OnFinished.md) | Callback interface for discovering when a send operation has completed. |
| [OnCancelListener](../android/app/SearchManager.OnCancelListener.md) | See setOnCancelListener for configuring your activity to monitor search UI state. |
| --- | --- |
| [OnDismissListener](../android/app/SearchManager.OnDismissListener.md) | See setOnDismissListener for configuring your activity to monitor search UI state. |
| [OnSharedElementsReadyListener](../android/app/SharedElementCallback.OnSharedElementsReadyListener.md) | Listener to be called after onSharedElementsArrived when the shared elements are ready to be hidden in the source Activity and shown in the destination Activity. |
| [OnTimeSetListener](../android/app/TimePickerDialog.OnTimeSetListener.md) | The callback interface used to indicate the user is done filling in the time (e.g. they clicked on the 'OK' button). |
| --- | --- |
| [AccessibilityEventFilter](../android/app/UiAutomation.AccessibilityEventFilter.md) | Listener for filtering accessibility events. |
| [OnAccessibilityEventListener](../android/app/UiAutomation.OnAccessibilityEventListener.md) | Listener for observing the `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#` stream. |
| [ContrastChangeListener](../android/app/UiModeManager.ContrastChangeListener.md) | Listener for the UI contrast. |
| --- | --- |
| [OnColorsChangedListener](../android/app/WallpaperManager.OnColorsChangedListener.md) | Interface definition for a callback to be invoked when colors change on a wallpaper. |
| [ZygotePreload](ZygotePreload.md) | This is the interface to be implemented for the class that is specified by the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestApplication_zygotePreloadName:kotlin.Int` of the \<application\> tag. |

## Classes

| [ActionBar](ActionBar.md) | A primary toolbar within the activity that may display the activity title, application-level navigation affordances, and other interactive items. |
| --- | --- |
| [Activity](Activity.md) | An activity is a single, focused thing that the user can do. |
| [ActivityGroup](ActivityGroup.md) | A screen that contains and runs multiple embedded activities. |
| [ActivityManager](ActivityManager.md) | This class gives information about, and interacts with, activities, services, and the containing process. |
| --- | --- |
| [ActivityOptions](ActivityOptions.md) | Helper class for building an options Bundle that can be used with startActivity and related methods. |
| [AlarmManager](AlarmManager.md) | This class provides access to the system alarm services. |
| [AlertDialog](AlertDialog.md) | A subclass of Dialog that can display one, two or three buttons. |
| --- | --- |
| [AliasActivity](AliasActivity.md) | Stub activity that launches another activity (and then finishes itself) based on information in its component's manifest meta-data. |
| [AnrTypes](AnrTypes.md) | Defines the types of Application Not Responding (ANR) errors. |
| [AnrWarningResult](AnrWarningResult.md) | Describes the information about a potential ANR before the timeout is reached. |
| --- | --- |
| [AppComponentFactory](AppComponentFactory.md) | Interface used to control the instantiation of manifest elements. |
| [AppInteractionAttribution](../android/app/AppInteractionAttribution.md) | Represents attribution information for an app interaction, detailing the context and nature of the interaction that triggered it. |
| [AppInteractionContract](../android/app/AppInteractionContract.md) | The contract between the App Interaction history provider and applications with read permission. |
| --- | --- |
| [AppInteractionManager](AppInteractionManager.md) | Provides access to App Interaction access control APIs. |
| [AppInteractionSession](AppInteractionSession.md) | Represents an app interaction session. |
| [Application](Application.md) | Base class for maintaining global application state. |
| --- | --- |
| [ApplicationErrorReport](ApplicationErrorReport.md) | Describes an application error. |
| [ApplicationExitInfo](ApplicationExitInfo.md) | Describes the information of an application process's death. |
| [ApplicationStartInfo](ApplicationStartInfo.md) | Describes information related to an application process's startup. |
| --- | --- |
| [AppOpsManager](AppOpsManager.md) | App-ops are used for two purposes: Access control and tracking. |
| [AsyncNotedAppOp](AsyncNotedAppOp.md) | When an noteOp and the app the app-op is noted for has a `https://developer.android.com/reference/kotlin/android/app/AppOpsManager.OnOpNotedCallback` registered the note-event needs to be delivered to the callback. |
| [AutomaticZenRule](AutomaticZenRule.md) | Rule instance information for a zen (aka DND or Attention Management) mode. |
| --- | --- |
| [BroadcastOptions](BroadcastOptions.md) | Helper class for building an options Bundle that can be used with sendBroadcast and related methods. |
| [ComponentCaller](ComponentCaller.md) | Represents the app that launched the component. |
| [DatePickerDialog](DatePickerDialog.md) | A simple dialog containing an `https://developer.android.com/reference/kotlin/android/widget/DatePicker.html#`. |
| --- | --- |
| [Dialog](Dialog.md) | Base class for Dialogs. |
| [DialogFragment](DialogFragment.md) | A fragment that displays a dialog window, floating on top of its activity's window. |
| [DirectAction](DirectAction.md) | Represents an abstract action that can be perform on this app. |
| --- | --- |
| [DownloadManager](DownloadManager.md) | The download manager is a system service that handles long-running HTTP downloads. |
| [ExpandableListActivity](ExpandableListActivity.md) | An activity that displays an expandable list of items by binding to a data source implementing the ExpandableListAdapter, and exposes event handlers when the user selects an item. |
| [Fragment](Fragment.md) | A Fragment is a piece of an application's user interface or behavior that can be placed in an Activity. |
| --- | --- |
| [FragmentBreadCrumbs](FragmentBreadCrumbs.md) | Helper class for showing "bread crumbs" representing the fragment stack in an activity. |
| [FragmentContainer](FragmentContainer.md) | Callbacks to a Fragment's container. |
| [FragmentController](FragmentController.md) | Provides integration points with a FragmentManager for a fragment host. |
| --- | --- |
| [FragmentHostCallback](FragmentHostCallback.md) | Integration points with the Fragment host. |
| [FragmentManager](FragmentManager.md) | Interface for interacting with Fragment objects inside of an Activity > [!NOTE] > ### Developer Guides > For more information about using fragments, read the [Fragments](https://developer.android.com/guide/components/fragments.html) developer guide. While the FragmentManager API was introduced in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int`, a version of the API at is also available for use on older platforms through androidx. <br /> |
| [FragmentManagerNonConfig](FragmentManagerNonConfig.md) | FragmentManagerNonConfig stores the retained instance fragments across activity recreation events. |
| --- | --- |
| [FragmentTransaction](FragmentTransaction.md) | API for performing a set of Fragment operations. |
| [GameManager](GameManager.md) | The GameManager allows system apps to modify and query the game mode of apps. |
| [GameState](GameState.md) | State of the game passed to the GameManager. |
| --- | --- |
| [GrammaticalInflectionManager](GrammaticalInflectionManager.md) | This class allow applications to control granular grammatical inflection settings (such as per-app grammatical gender). |
| [HandoffActivityData](../android/app/HandoffActivityData.md) | Represents information needed to recreate an activity on a remote device owned by the user. |
| [HandoffActivityDataRequestInfo](../android/app/HandoffActivityDataRequestInfo.md) | Represents a request made by the platform to hand off an activity. |
| --- | --- |
| [HandoffActivityParams](../android/app/HandoffActivityParams.md) | Represents options specifying how an activity will be handed off to other devices. |
| [Instrumentation](Instrumentation.md) | Base class for implementing application instrumentation code. |
| [IntentService](IntentService.md) | IntentService is an extension of the Service component class that handles asynchronous requests (expressed as `https://developer.android.com/reference/kotlin/android/content/Intent.html#`s) on demand. |
| --- | --- |
| [KeyguardManager](KeyguardManager.md) | Class to manage and query the state of the lock screen (also known as Keyguard). |
| [LauncherActivity](LauncherActivity.md) | Displays a list of all activities which can be performed for a given intent. |
| [ListActivity](ListActivity.md) | An activity that displays a list of items by binding to a data source such as an array or Cursor, and exposes event handlers when the user selects an item. |
| --- | --- |
| [ListFragment](ListFragment.md) | A fragment that displays a list of items by binding to a data source such as an array or Cursor, and exposes event handlers when the user selects an item. |
| [LoaderManager](LoaderManager.md) | Interface associated with an Activity or Fragment for managing one or more `https://developer.android.com/reference/kotlin/android/content/Loader.html#` instances associated with it. |
| [LocalActivityManager](LocalActivityManager.md) | Helper class for managing multiple running embedded activities in the same process. |
| --- | --- |
| [LocaleConfig](LocaleConfig.md) | The LocaleConfig of an application. |
| [LocaleManager](LocaleManager.md) | This class gives access to system locale services. |
| [MediaRouteActionProvider](MediaRouteActionProvider.md) | The media route action provider displays a MediaRouteButton in the application's ActionBar to allow the user to select routes and to control the currently selected route. |
| --- | --- |
| [MediaRouteButton](MediaRouteButton.md) | <br /> |
| [MemoryBudgetManager](MemoryBudgetManager.md) | This class is the client interface to memory budgets for applications and processes. |
| [NativeActivity](NativeActivity.md) | Convenience for implementing an activity that will be implemented purely in native code. |
| --- | --- |
| [Notification](Notification.md) | A class that represents how a persistent notification is to be presented to the user using the NotificationManager. |
| [NotificationChannel](NotificationChannel.md) | A representation of settings that apply to a collection of similarly themed notifications. |
| [NotificationChannelGroup](NotificationChannelGroup.md) | A grouping of related notification channels. |
| --- | --- |
| [NotificationManager](NotificationManager.md) | Class to notify the user of events that happen. |
| [PendingIntent](PendingIntent.md) | A description of an Intent and target action to perform with it. |
| [Person](Person.md) | Provides an immutable reference to an entity that appears repeatedly on different surfaces of the platform. |
| --- | --- |
| [PictureInPictureParams](PictureInPictureParams.md) | Represents a set of parameters used to initialize and update an Activity in picture-in-picture mode. |
| [PictureInPictureUiState](PictureInPictureUiState.md) | Used by onPictureInPictureUiStateChanged. |
| [Presentation](Presentation.md) | Base class for presentations. |
| --- | --- |
| [ProgressDialog](ProgressDialog.md) | A dialog showing a progress indicator and an optional text message or view. |
| [RemoteAction](RemoteAction.md) | Represents a remote action that can be called from another process. |
| [RemoteInput](RemoteInput.md) | A `RemoteInput` object specifies input to be collected from a user to be passed along with an intent inside a PendingIntent that is sent. |
| --- | --- |
| [SearchableInfo](SearchableInfo.md) | Searchability meta-data for an activity. |
| [SearchManager](SearchManager.md) | This class provides access to the system search services. |
| [Service](Service.md) | A Service is an application component representing either an application's desire to perform a longer-running operation while not interacting with the user or to supply functionality for other applications to use. |
| --- | --- |
| [SharedElementCallback](SharedElementCallback.md) | Listener provided in setEnterSharedElementCallback and setExitSharedElementCallback as well as setEnterSharedElementCallback and setExitSharedElementCallback to monitor the Shared element transitions. |
| [StatusBarManager](StatusBarManager.md) | Allows an app to control the status bar. |
| [SyncNotedAppOp](SyncNotedAppOp.md) | Description of an app-op that was noted for the current process. |
| --- | --- |
| [TabActivity](TabActivity.md) | For apps developing against `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int` or later, tabs are typically presented in the UI using the new newTab and related APIs for placing tabs within their action bar area. |
| [TaskInfo](TaskInfo.md) | Stores information about a particular Task. |
| [TaskLocation](../android/app/TaskLocation.md) | Represents location of an `https://developer.android.com/reference/kotlin/android/app/ActivityManager.AppTask` that consists of the host display identifier and rectangular bounds in the pixel-based coordinate system relative to host display. |
| --- | --- |
| [TaskStackBuilder](TaskStackBuilder.md) | Utility class for constructing synthetic back stacks for cross-task navigation on Android 3. |
| [TimePickerDialog](TimePickerDialog.md) | A dialog that prompts the user for the time of day using a `https://developer.android.com/reference/kotlin/android/widget/TimePicker.html#`. |
| [UiAutomation](UiAutomation.md) | Class for interacting with the device's UI by simulation user actions and introspection of the screen content. |
| --- | --- |
| [UiModeManager](UiModeManager.md) | This class provides access to the system uimode services. |
| [VoiceInteractor](VoiceInteractor.md) | Interface for an Activity to interact with the user through voice. |
| [WallpaperColors](WallpaperColors.md) | Provides information about the colors of a wallpaper. |
| --- | --- |
| [WallpaperInfo](WallpaperInfo.md) | This class is used to specify meta information of a wallpaper service. |
| [WallpaperManager](WallpaperManager.md) | Provides access to the system wallpaper. |

## Exceptions

| [AppInteractionDeniedException](AppInteractionDeniedException.md) | Exception thrown when an app interaction is denied. |
| --- | --- |
| [AppInteractionException](AppInteractionException.md) | Exception thrown when an app interaction operation fails. |
| [AuthenticationRequiredException](AuthenticationRequiredException.md) | Specialization of `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` that is thrown when authentication is needed from the end user before viewing the content. |
| [BackgroundServiceStartNotAllowedException](BackgroundServiceStartNotAllowedException.md) | Exception thrown when an app tries to start a background Service when it's not allowed to do so. |
| --- | --- |
| [ForegroundServiceStartNotAllowedException](ForegroundServiceStartNotAllowedException.md) | Exception thrown when an app tries to start a foreground Service when it's not allowed to do so. |
| [ForegroundServiceTypeException](ForegroundServiceTypeException.md) | Base exception thrown when an app tries to start a foreground Service without a valid type. |
| [InfeasibleActivityOptionsException](InfeasibleActivityOptionsException.md) | This exception is thrown when a call to android. |
| --- | --- |
| [InvalidForegroundServiceTypeException](InvalidForegroundServiceTypeException.md) | Exception thrown when an app tries to start a foreground Service with an invalid type. |
| [MissingForegroundServiceTypeException](MissingForegroundServiceTypeException.md) | Exception thrown when an app tries to start a foreground Service without a type. |
| [RecoverableSecurityException](RecoverableSecurityException.md) | Specialization of `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` that contains additional information about how to involve the end user to recover from the exception. |
| --- | --- |
| [ServiceStartNotAllowedException](ServiceStartNotAllowedException.md) | Exception thrown when an app tries to start a Service when it's not allowed to do so. |
| [StartForegroundCalledOnStoppedServiceException](StartForegroundCalledOnStoppedServiceException.md) | Exception thrown when android. |
