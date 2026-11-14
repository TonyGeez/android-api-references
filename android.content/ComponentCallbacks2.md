Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ComponentCallbacks2

```
interface ComponentCallbacks2 : ComponentCallbacks
```

| [android.content.ComponentCallbacks2](../android/content/ComponentCallbacks2.md) |

Known Direct Subclasses [Activity](../android/app/Activity.md), [Application](../android/app/Application.md), [ContentProvider](../android/content/ContentProvider.md), [Fragment](../android/app/Fragment.md), [Service](../android/app/Service.md), [VoiceInteractionSession](../android/service/voice/VoiceInteractionSession.md) [Activity](../android/app/Activity.md) An activity is a single, focused thing that the user can do.
[Application](../android/app/Application.md) Base class for maintaining global application state.
[ContentProvider](../android/content/ContentProvider.md) Content providers are one of the primary building blocks of Android applications, providing content to applications.
[Fragment](../android/app/Fragment.md) A Fragment is a piece of an application's user interface or behavior that can be placed in an `https://developer.android.com/reference/kotlin/android/app/Activity.html#`.
[Service](../android/app/Service.md) A Service is an application component representing either an application's desire to perform a longer-running operation while not interacting with the user or to supply functionality for other applications to use.
[VoiceInteractionSession](../android/service/voice/VoiceInteractionSession.md) An active voice interaction session, providing a facility for the implementation to interact with the user in the voice interaction layer.
Known Indirect Subclasses [AbstractInputMethodService](../android/inputmethodservice/AbstractInputMethodService.md), [AccessibilityService](../android/accessibilityservice/AccessibilityService.md), [AccountAuthenticatorActivity](../android/accounts/AccountAuthenticatorActivity.md), [ActivityGroup](../android/app/ActivityGroup.md), [AliasActivity](../android/app/AliasActivity.md), [AlternativeMessageTransportService](../android/service/messaging/AlternativeMessageTransportService.md), [AppContentProjectionService](../android/media/projection/AppContentProjectionService.md), [AppFunctionService](../android/app/appfunctions/AppFunctionService.md), [AutofillService](../android/service/autofill/AutofillService.md), [CallRedirectionService](../android/telecom/CallRedirectionService.md), [CallScreeningService](../android/telecom/CallScreeningService.md), [CameraPrewarmService](../android/service/media/CameraPrewarmService.md), and 63 others. [AbstractInputMethodService](../android/inputmethodservice/AbstractInputMethodService.md) AbstractInputMethodService provides a abstract base class for input methods.
[AccessibilityService](../android/accessibilityservice/AccessibilityService.md) Accessibility services should only be used to assist users with disabilities in using Android devices and apps.
[AccountAuthenticatorActivity](../android/accounts/AccountAuthenticatorActivity.md) Base class for implementing an Activity that is used to help implement an AbstractAccountAuthenticator.
[ActivityGroup](../android/app/ActivityGroup.md) A screen that contains and runs multiple embedded activities.
[AliasActivity](../android/app/AliasActivity.md) Stub activity that launches another activity (and then finishes itself) based on information in its component's manifest meta-data.
[AlternativeMessageTransportService](../android/service/messaging/AlternativeMessageTransportService.md) AlternativeMessageTransportService (AMTS) allows the default SMS app to handle the sending of a message over a different transport (e.g. RCS etc.) other than the SMS or MMS.
[AppContentProjectionService](../android/media/projection/AppContentProjectionService.md) Service to be implemented by the application providing the `https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionAppContent.html#`.
[AppFunctionService](../android/app/appfunctions/AppFunctionService.md) Extend this class to implement app functions, that can be executed by android.
[AutofillService](../android/service/autofill/AutofillService.md) An `AutofillService` is a service used to automatically fill the contents of the screen on behalf of a given user - for more information about autofill, read [Autofill Framework](https://developer.android.com/preview/features/autofill.html).
[CallRedirectionService](../android/telecom/CallRedirectionService.md) This service can be implemented to interact between Telecom and its implementor for making outgoing call with optional redirection/cancellation purposes.
[CallScreeningService](../android/telecom/CallScreeningService.md) This service can be implemented by the default dialer (see `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager.html#getDefaultDialerPackage()`) or a third party app to allow or disallow incoming calls before they are shown to a user.
[CameraPrewarmService](../android/service/media/CameraPrewarmService.md) Extend this class to implement a camera prewarm service.
[CarrierMessagingClientService](../android/service/carrier/CarrierMessagingClientService.md) If the default SMS app has a service that extends this class, the system always tries to bind it so that the process is always running, which allows the app to have a persistent connection to the server.
[CarrierMessagingService](../android/service/carrier/CarrierMessagingService.md) A service that receives calls from the system when new SMS and MMS are sent or received.
[CarrierService](../android/service/carrier/CarrierService.md) A service that exposes carrier-specific functionality to the system.
[ChooserTargetService](../android/service/chooser/ChooserTargetService.md) A service that receives calls from the system when the user is asked to choose a target for an intent explicitly by another app.
[CloudMediaProvider](../android/provider/CloudMediaProvider.md) Base class for a cloud media provider.
[CompanionDeviceService](../android/companion/CompanionDeviceService.md) A service that receives calls from the system with device events.
[ConditionProviderService](../android/service/notification/ConditionProviderService.md) A service that provides conditions about boolean state.
[ConnectionService](../android/telecom/ConnectionService.md) An abstract service that should be implemented by any apps which either:

1. Can make phone calls (VoIP or otherwise) and want those calls to be integrated into the built-in phone app. Referred to as a **system managed** `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService.html#`.
2. Are a standalone calling app and don't want their calls to be integrated into the built-in phone app. Referred to as a **self managed** `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService.html#`.

Once implemented, the needs to take the following steps so that Telecom will bind to it:

<br />

[ContentSafetyAppService](../android/service/contentsafety/ContentSafetyAppService.md) Base class for a service that the `android.app.role.RoleManager.ROLE_CONTENT_SAFETY` role holder must implement.
[ControlsProviderService](../android/service/controls/ControlsProviderService.md) Service implementation allowing applications to contribute controls to the System UI.
[CredentialProviderService](../android/service/credentials/CredentialProviderService.md) Service to be extended by credential providers, in order to return user credentials to the framework.
[DataMigrationToPccService](../android/app/privatecompute/DataMigrationToPccService.md) Base class for a service that handles data migration to the Private Compute Core (PCC) storage of an application.
[DeviceAdminService](../android/app/admin/DeviceAdminService.md) Base class for a service that device owner/profile owners can optionally have.
[DialogFragment](../android/app/DialogFragment.md) A fragment that displays a dialog window, floating on top of its activity's window.
[DocumentsProvider](../android/provider/DocumentsProvider.md) Base class for a document provider.
[DreamService](../android/service/dreams/DreamService.md) Extend this class to implement a custom dream (available to the user as a "Daydream").
[EgressReceiverService](../android/app/privatecompute/EgressReceiverService.md) Base Service to be implemented by the partner agent proxy process to receive egress queries from a client running inside the Private Compute Core (PCC) sandbox.
[ExpandableListActivity](../android/app/ExpandableListActivity.md) An activity that displays an expandable list of items by binding to a data source implementing the ExpandableListAdapter, and exposes event handlers when the user selects an item.
[HostApduService](../android/nfc/cardemulation/HostApduService.md) HostApduService is a convenience `https://developer.android.com/reference/kotlin/android/app/Service.html#` class that can be extended to emulate an NFC card inside an Android service component.
[HostNfcFService](../android/nfc/cardemulation/HostNfcFService.md) HostNfcFService is a convenience `https://developer.android.com/reference/kotlin/android/app/Service.html#` class that can be extended to emulate an NFC-F card inside an Android service component.
[InCallService](../android/telecom/InCallService.md) This service is implemented by an app that wishes to provide functionality for managing phone calls.
[InputMethodService](../android/inputmethodservice/InputMethodService.md) InputMethodService provides a standard implementation of an InputMethod, which final implementations can derive from and customize.
[IntentService](../android/app/IntentService.md) IntentService is an extension of the `https://developer.android.com/reference/kotlin/android/app/Service.html#` component class that handles asynchronous requests (expressed as `https://developer.android.com/reference/kotlin/android/content/Intent`s) on demand.
[IsolatedService](../android/adservices/ondevicepersonalization/IsolatedService.md) Base class for services that are started by ODP on a call to `OnDevicePersonalizationManager#execute(ComponentName, PersistableBundle, java.util.concurrent.Executor, OutcomeReceiver)` and run in an [isolated process](https://developer.android.com/guide/topics/manifest/service-element#isolated).
[JobService](../android/app/job/JobService.md) Entry point for the callback from the `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler.html#`.
[LauncherActivity](../android/app/LauncherActivity.md) Displays a list of all activities which can be performed for a given intent.
[ListActivity](../android/app/ListActivity.md) An activity that displays a list of items by binding to a data source such as an array or Cursor, and exposes event handlers when the user selects an item.
[ListFragment](../android/app/ListFragment.md) A fragment that displays a list of items by binding to a data source such as an array or Cursor, and exposes event handlers when the user selects an item.
[MediaBrowserService](../android/service/media/MediaBrowserService.md) Base class for media browser services.
[MediaRoute2ProviderService](../android/media/MediaRoute2ProviderService.md) Base class for media route provider services.
[MediaSession2Service](../android/media/MediaSession2Service.md) This API is not generally intended for third party application developers.
[MidiDeviceService](../android/media/midi/MidiDeviceService.md) A service that implements a virtual MIDI device.
[MidiUmpDeviceService](../android/media/midi/MidiUmpDeviceService.md) A service that implements a virtual MIDI device for Universal MIDI Packets (UMP).
[MockApplication](../android/test/mock/MockApplication.md) A mock `https://developer.android.com/reference/kotlin/android/app/Application.html#` class.
[MockContentProvider](../android/test/mock/MockContentProvider.md) Mock implementation of ContentProvider.
[NativeActivity](../android/app/NativeActivity.md) Convenience for implementing an activity that will be implemented purely in native code.
[NotificationListenerService](../android/service/notification/NotificationListenerService.md) A service that receives calls from the system when new notifications are posted or removed, or their ranking changed.
[OffHostApduService](../android/nfc/cardemulation/OffHostApduService.md) OffHostApduService is a convenience `https://developer.android.com/reference/kotlin/android/app/Service.html#` class that can be extended to describe one or more NFC applications that are residing off-host, for example on an embedded secure element or a UICC.
[PccService](../android/app/privatecompute/PccService.md) Abstract base class for a PCC service that receives data from other components.
[PreferenceActivity](../android/preference/PreferenceActivity.md) This is the base class for an activity to show a hierarchy of preferences to the user.
[PreferenceFragment](../android/preference/PreferenceFragment.md) Shows a hierarchy of `https://developer.android.com/reference/kotlin/android/preference/Preference.html#` objects as lists.
[PrintService](../android/printservice/PrintService.md) This is the base class for implementing print services.
[QuickAccessWalletService](../android/service/quickaccesswallet/QuickAccessWalletService.md) A `QuickAccessWalletService` provides a list of `WalletCard`s shown in the Quick Access Wallet.
[RecognitionService](../android/speech/RecognitionService.md) This class provides a base class for recognition service implementations.
[RemoteViewsService](../android/widget/RemoteViewsService.md) The service to be connected to for a remote adapter to request RemoteViews.
[SearchRecentSuggestionsProvider](../android/content/SearchRecentSuggestionsProvider.md) This superclass can be used to create a simple search suggestions provider for your application.
[SettingInjectorService](../android/location/SettingInjectorService.md) Dynamically specifies the summary (subtitle) and enabled status of a preference injected into the list of app settings displayed by the system settings app
[SettingsPreferenceService](../android/service/settings/preferences/SettingsPreferenceService.md) Base class for a service that exposes its settings preferences to external access.
[SliceProvider](../android/app/slice/SliceProvider.md) A SliceProvider allows an app to provide content to be displayed in system spaces.
[SpellCheckerService](../android/service/textservice/SpellCheckerService.md) SpellCheckerService provides an abstract base class for a spell checker.
[TabActivity](../android/app/TabActivity.md) For apps developing against `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int` or later, tabs are typically presented in the UI using the new `https://developer.android.com/reference/kotlin/android/app/ActionBar.html#newTab()` and related APIs for placing tabs within their action bar area.
[TextToSpeechService](../android/speech/tts/TextToSpeechService.md) Abstract base class for TTS engine implementations.
[TileService](../android/service/quicksettings/TileService.md) A TileService provides the user a tile that can be added to Quick Settings.
[TvAdService](../android/media/tv/ad/TvAdService.md) The TvAdService class represents a TV client-side advertisement service.
[TvInputService](../android/media/tv/TvInputService.md) The TvInputService class represents a TV input or source such as HDMI or built-in tuner which provides pass-through video or broadcast TV programs.
[TvInteractiveAppService](../android/media/tv/interactive/TvInteractiveAppService.md) A TV interactive application service is a service that provides runtime environment and runs TV interactive applications.
[VisualVoicemailService](../android/telephony/VisualVoicemailService.md) This service is implemented by dialer apps that wishes to handle OMTP or similar visual voicemails.
[VoiceInteractionService](../android/service/voice/VoiceInteractionService.md) Top-level service of the current global voice interactor, which is providing support for hotwording, the back-end of a `https://developer.android.com/reference/kotlin/android/app/VoiceInteractor.html#`, etc.
[VoiceInteractionSessionService](../android/service/voice/VoiceInteractionSessionService.md) An active voice interaction session, initiated by a `https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionService.html#`.
[VpnService](../android/net/VpnService.md) VpnService is a base class for applications to extend and build their own VPN solutions.
[VrListenerService](../android/service/vr/VrListenerService.md) A service that is bound from the system while running in virtual reality (VR) mode.
[WallpaperService](../android/service/wallpaper/WallpaperService.md) A wallpaper service is responsible for showing a live wallpaper behind applications that would like to sit on top of it.
[WebViewFragment](../android/webkit/WebViewFragment.md) A fragment that displays a WebView.

Callbacks for app state transitions that can be used to improve background memory management. This interface is available in all application components (`https://developer.android.com/reference/kotlin/android/app/Activity.html#`, `https://developer.android.com/reference/kotlin/android/app/Service.html#`, `https://developer.android.com/reference/kotlin/android/content/ContentProvider`, and `https://developer.android.com/reference/kotlin/android/app/Application.html#`).

You should implement `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)` to release memory when your app goes to background states. Doing so helps the system keep your app's process cached in memory for longer, such that the next time that the user brings your app to the foreground, the app will perform a [warm or hot start](https://developer.android.com/topic/performance/vitals/launch-time), resuming faster and retaining state.

## Trim memory levels and how to handle them

- `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_UI_HIDDEN:kotlin.Int` 
 Your app's UI is no longer visible. This is a good time to release large memory allocations that are used only by your UI, such as `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#`, or resources related to video playback or animations.
- `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_BACKGROUND:kotlin.Int` 
 Your app's process is considered to be in the background, and has become eligible to be killed in order to free memory for other processes. Releasing more memory will prolong the time that your process can remain cached in memory. An effective strategy is to release resources that can be re-built when the user returns to your app.

Apps that continue to do work for the user when they're not visible can respond to the `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_UI_HIDDEN:kotlin.Int` callback by changing their behavior to favor lower memory usage. For example, a music player may keep full-sized album art for all tracks in the currently playing playlist as Bitmaps cached in memory. When the app is backgrounded but music playback continues, the app can change the caching behavior to cache fewer, or smaller, Bitmaps in memory.

The ordinal values for trim levels represent an escalating series of memory pressure events, with incrementing values accordingly. More states may be added in the future. As such, it's important not to check for specific values, but rather check if the level passed to `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)` is greater than or equal to the levels that your application handles. For example:

```kotlin
<code>public void onTrimMemory(int level) {
      if (level &gt;= TRIM_MEMORY_BACKGROUND) {
          // Release any resources that can be rebuilt
          // quickly when the app returns to the foreground
          releaseResources();
      } else if (level &gt;= TRIM_MEMORY_UI_HIDDEN) {
          // Release UI-related resources
          releaseUiResources();
      }
  }
  </code>
```

**Note:** the runtime may invoke Garbage Collection (GC) in response to application state changes. There is no need to explicitly invoke GC from your app.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_BACKGROUND:kotlin.Int` Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)`: the process has gone on to the LRU list. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_COMPLETE:kotlin.Int` Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)`: the process is nearing the end of the background LRU list, and if more memory isn't found soon it will be killed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_MODERATE:kotlin.Int` Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)`: the process is around the middle of the background LRU list; freeing memory can help the system keep other processes running later in the list for better overall performance. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_RUNNING_CRITICAL:kotlin.Int` Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running extremely low on memory and is about to not be able to keep any background processes running. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_RUNNING_LOW:kotlin.Int` Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running low on memory. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_RUNNING_MODERATE:kotlin.Int` Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running moderately low on memory. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_UI_HIDDEN:kotlin.Int` Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)`: the process had been showing a user interface, and is no longer doing so. |

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)(level: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Called when the operating system has determined that it is a good time for a process to trim unneeded memory from its process. |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks#onConfigurationChanged(android.content.res.Configuration)(newConfig: https://developer.android.com/reference/kotlin/android/content/res/Configuration)`

Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources.

At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration.

For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks#onLowMemory()()`

This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing.

<br />

## Constants

### TRIM_MEMORY_BACKGROUND

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRIM_MEMORY_BACKGROUND: Int
```

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)`: the process has gone on to the LRU list. This is a good opportunity to clean up resources that can efficiently and quickly be re-built if the user returns to the app.

 Value: 40

### TRIM_MEMORY_COMPLETE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRIM_MEMORY_COMPLETE: Int
```

**Deprecated:** *Apps are not notified of this level since API level 34*

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)`: the process is nearing the end of the background LRU list, and if more memory isn't found soon it will be killed.

 Value: 80

### TRIM_MEMORY_MODERATE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRIM_MEMORY_MODERATE: Int
```

**Deprecated:** *Apps are not notified of this level since API level 34*

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)`: the process is around the middle of the background LRU list; freeing memory can help the system keep other processes running later in the list for better overall performance.

 Value: 60

### TRIM_MEMORY_RUNNING_CRITICAL

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRIM_MEMORY_RUNNING_CRITICAL: Int
```

**Deprecated:** *Apps are not notified of this level since API level 34*

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running extremely low on memory and is about to not be able to keep any background processes running. Your running process should free up as many non-critical resources as it can to allow that memory to be used elsewhere. The next thing that will happen after this is `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks#onLowMemory()` called to report that nothing at all can be kept in the background, a situation that can start to notably impact the user.

 Value: 15

### TRIM_MEMORY_RUNNING_LOW

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRIM_MEMORY_RUNNING_LOW: Int
```

**Deprecated:** *Apps are not notified of this level since API level 34*

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running low on memory. Your running process should free up unneeded resources to allow that memory to be used elsewhere.

 Value: 10

### TRIM_MEMORY_RUNNING_MODERATE

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRIM_MEMORY_RUNNING_MODERATE: Int
```

**Deprecated:** *Apps are not notified of this level since API level 34*

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running moderately low on memory. Your running process may want to release some unneeded resources for use elsewhere.

 Value: 5

### TRIM_MEMORY_UI_HIDDEN

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRIM_MEMORY_UI_HIDDEN: Int
```

Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)`: the process had been showing a user interface, and is no longer doing so. Large allocations with the UI should be released at this point to allow memory to be better managed.

 Value: 20

## Public methods

### onTrimMemory

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onTrimMemory(level: Int): Unit
```

Called when the operating system has determined that it is a good time for a process to trim unneeded memory from its process. You should never compare to exact values of the level, since new intermediate values may be added -- you will typically want to compare if the value is greater or equal to a level you are interested in.

To retrieve the processes current trim level at any point, you can use `https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#getMyMemoryState(android.app.ActivityManager.RunningAppProcessInfo)`.

| Parameters ||
|---|---|
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The context of the trim, giving a hint of the amount of trimming the application may like to perform. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_COMPLETE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_MODERATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_BACKGROUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_UI_HIDDEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_RUNNING_CRITICAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_RUNNING_LOW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_RUNNING_MODERATE:kotlin.Int` |
