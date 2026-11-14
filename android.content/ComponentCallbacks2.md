Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ComponentCallbacks2

```
interface ComponentCallbacks2 : ComponentCallbacks
```

| [android.content.ComponentCallbacks2](https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#) |

Known Direct Subclasses [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#), [Application](https://developer.android.com/reference/kotlin/android/app/Application.html#), [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider), [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment.html#), [Service](https://developer.android.com/reference/kotlin/android/app/Service.html#), [VoiceInteractionSession](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.html#) [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) An activity is a single, focused thing that the user can do.
[Application](https://developer.android.com/reference/kotlin/android/app/Application.html#) Base class for maintaining global application state.
[ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider) Content providers are one of the primary building blocks of Android applications, providing content to applications.
[Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment.html#) A Fragment is a piece of an application's user interface or behavior that can be placed in an `https://developer.android.com/reference/kotlin/android/app/Activity.html#`.
[Service](https://developer.android.com/reference/kotlin/android/app/Service.html#) A Service is an application component representing either an application's desire to perform a longer-running operation while not interacting with the user or to supply functionality for other applications to use.
[VoiceInteractionSession](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.html#) An active voice interaction session, providing a facility for the implementation to interact with the user in the voice interaction layer.
Known Indirect Subclasses [AbstractInputMethodService](https://developer.android.com/reference/kotlin/android/inputmethodservice/AbstractInputMethodService.html#), [AccessibilityService](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#), [AccountAuthenticatorActivity](https://developer.android.com/reference/kotlin/android/accounts/AccountAuthenticatorActivity.html#), [ActivityGroup](https://developer.android.com/reference/kotlin/android/app/ActivityGroup.html#), [AliasActivity](https://developer.android.com/reference/kotlin/android/app/AliasActivity.html#), [AlternativeMessageTransportService](https://developer.android.com/reference/kotlin/android/service/messaging/AlternativeMessageTransportService.html#), [AppContentProjectionService](https://developer.android.com/reference/kotlin/android/media/projection/AppContentProjectionService.html#), [AppFunctionService](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionService.html#), [AutofillService](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#), [CallRedirectionService](https://developer.android.com/reference/kotlin/android/telecom/CallRedirectionService.html#), [CallScreeningService](https://developer.android.com/reference/kotlin/android/telecom/CallScreeningService.html#), [CameraPrewarmService](https://developer.android.com/reference/kotlin/android/service/media/CameraPrewarmService.html#), and 63 others. [AbstractInputMethodService](https://developer.android.com/reference/kotlin/android/inputmethodservice/AbstractInputMethodService.html#) AbstractInputMethodService provides a abstract base class for input methods.
[AccessibilityService](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#) Accessibility services should only be used to assist users with disabilities in using Android devices and apps.
[AccountAuthenticatorActivity](https://developer.android.com/reference/kotlin/android/accounts/AccountAuthenticatorActivity.html#) Base class for implementing an Activity that is used to help implement an AbstractAccountAuthenticator.
[ActivityGroup](https://developer.android.com/reference/kotlin/android/app/ActivityGroup.html#) A screen that contains and runs multiple embedded activities.
[AliasActivity](https://developer.android.com/reference/kotlin/android/app/AliasActivity.html#) Stub activity that launches another activity (and then finishes itself) based on information in its component's manifest meta-data.
[AlternativeMessageTransportService](https://developer.android.com/reference/kotlin/android/service/messaging/AlternativeMessageTransportService.html#) AlternativeMessageTransportService (AMTS) allows the default SMS app to handle the sending of a message over a different transport (e.g. RCS etc.) other than the SMS or MMS.
[AppContentProjectionService](https://developer.android.com/reference/kotlin/android/media/projection/AppContentProjectionService.html#) Service to be implemented by the application providing the `https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionAppContent.html#`.
[AppFunctionService](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionService.html#) Extend this class to implement app functions, that can be executed by android.
[AutofillService](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#) An `AutofillService` is a service used to automatically fill the contents of the screen on behalf of a given user - for more information about autofill, read [Autofill Framework](https://developer.android.com/preview/features/autofill.html).
[CallRedirectionService](https://developer.android.com/reference/kotlin/android/telecom/CallRedirectionService.html#) This service can be implemented to interact between Telecom and its implementor for making outgoing call with optional redirection/cancellation purposes.
[CallScreeningService](https://developer.android.com/reference/kotlin/android/telecom/CallScreeningService.html#) This service can be implemented by the default dialer (see `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager.html#getDefaultDialerPackage()`) or a third party app to allow or disallow incoming calls before they are shown to a user.
[CameraPrewarmService](https://developer.android.com/reference/kotlin/android/service/media/CameraPrewarmService.html#) Extend this class to implement a camera prewarm service.
[CarrierMessagingClientService](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierMessagingClientService.html#) If the default SMS app has a service that extends this class, the system always tries to bind it so that the process is always running, which allows the app to have a persistent connection to the server.
[CarrierMessagingService](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierMessagingService.html#) A service that receives calls from the system when new SMS and MMS are sent or received.
[CarrierService](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierService.html#) A service that exposes carrier-specific functionality to the system.
[ChooserTargetService](https://developer.android.com/reference/kotlin/android/service/chooser/ChooserTargetService.html#) A service that receives calls from the system when the user is asked to choose a target for an intent explicitly by another app.
[CloudMediaProvider](https://developer.android.com/reference/kotlin/android/provider/CloudMediaProvider.html#) Base class for a cloud media provider.
[CompanionDeviceService](https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceService.html#) A service that receives calls from the system with device events.
[ConditionProviderService](https://developer.android.com/reference/kotlin/android/service/notification/ConditionProviderService.html#) A service that provides conditions about boolean state.
[ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService.html#) An abstract service that should be implemented by any apps which either:

1. Can make phone calls (VoIP or otherwise) and want those calls to be integrated into the built-in phone app. Referred to as a **system managed** `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService.html#`.
2. Are a standalone calling app and don't want their calls to be integrated into the built-in phone app. Referred to as a **self managed** `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService.html#`.

Once implemented, the needs to take the following steps so that Telecom will bind to it:

<br />

[ContentSafetyAppService](https://developer.android.com/reference/kotlin/android/service/contentsafety/ContentSafetyAppService.html#) Base class for a service that the `android.app.role.RoleManager.ROLE_CONTENT_SAFETY` role holder must implement.
[ControlsProviderService](https://developer.android.com/reference/kotlin/android/service/controls/ControlsProviderService.html#) Service implementation allowing applications to contribute controls to the System UI.
[CredentialProviderService](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialProviderService.html#) Service to be extended by credential providers, in order to return user credentials to the framework.
[DataMigrationToPccService](https://developer.android.com/reference/kotlin/android/app/privatecompute/DataMigrationToPccService.html#) Base class for a service that handles data migration to the Private Compute Core (PCC) storage of an application.
[DeviceAdminService](https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminService.html#) Base class for a service that device owner/profile owners can optionally have.
[DialogFragment](https://developer.android.com/reference/kotlin/android/app/DialogFragment.html#) A fragment that displays a dialog window, floating on top of its activity's window.
[DocumentsProvider](https://developer.android.com/reference/kotlin/android/provider/DocumentsProvider.html#) Base class for a document provider.
[DreamService](https://developer.android.com/reference/kotlin/android/service/dreams/DreamService.html#) Extend this class to implement a custom dream (available to the user as a "Daydream").
[EgressReceiverService](https://developer.android.com/reference/kotlin/android/app/privatecompute/EgressReceiverService.html#) Base Service to be implemented by the partner agent proxy process to receive egress queries from a client running inside the Private Compute Core (PCC) sandbox.
[ExpandableListActivity](https://developer.android.com/reference/kotlin/android/app/ExpandableListActivity.html#) An activity that displays an expandable list of items by binding to a data source implementing the ExpandableListAdapter, and exposes event handlers when the user selects an item.
[HostApduService](https://developer.android.com/reference/kotlin/android/nfc/cardemulation/HostApduService.html#) HostApduService is a convenience `https://developer.android.com/reference/kotlin/android/app/Service.html#` class that can be extended to emulate an NFC card inside an Android service component.
[HostNfcFService](https://developer.android.com/reference/kotlin/android/nfc/cardemulation/HostNfcFService.html#) HostNfcFService is a convenience `https://developer.android.com/reference/kotlin/android/app/Service.html#` class that can be extended to emulate an NFC-F card inside an Android service component.
[InCallService](https://developer.android.com/reference/kotlin/android/telecom/InCallService.html#) This service is implemented by an app that wishes to provide functionality for managing phone calls.
[InputMethodService](https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#) InputMethodService provides a standard implementation of an InputMethod, which final implementations can derive from and customize.
[IntentService](https://developer.android.com/reference/kotlin/android/app/IntentService.html#) IntentService is an extension of the `https://developer.android.com/reference/kotlin/android/app/Service.html#` component class that handles asynchronous requests (expressed as `https://developer.android.com/reference/kotlin/android/content/Intent`s) on demand.
[IsolatedService](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService.html#) Base class for services that are started by ODP on a call to `OnDevicePersonalizationManager#execute(ComponentName, PersistableBundle, java.util.concurrent.Executor, OutcomeReceiver)` and run in an [isolated process](https://developer.android.com/guide/topics/manifest/service-element#isolated).
[JobService](https://developer.android.com/reference/kotlin/android/app/job/JobService.html#) Entry point for the callback from the `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler.html#`.
[LauncherActivity](https://developer.android.com/reference/kotlin/android/app/LauncherActivity.html#) Displays a list of all activities which can be performed for a given intent.
[ListActivity](https://developer.android.com/reference/kotlin/android/app/ListActivity.html#) An activity that displays a list of items by binding to a data source such as an array or Cursor, and exposes event handlers when the user selects an item.
[ListFragment](https://developer.android.com/reference/kotlin/android/app/ListFragment.html#) A fragment that displays a list of items by binding to a data source such as an array or Cursor, and exposes event handlers when the user selects an item.
[MediaBrowserService](https://developer.android.com/reference/kotlin/android/service/media/MediaBrowserService.html#) Base class for media browser services.
[MediaRoute2ProviderService](https://developer.android.com/reference/kotlin/android/media/MediaRoute2ProviderService.html#) Base class for media route provider services.
[MediaSession2Service](https://developer.android.com/reference/kotlin/android/media/MediaSession2Service.html#) This API is not generally intended for third party application developers.
[MidiDeviceService](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceService.html#) A service that implements a virtual MIDI device.
[MidiUmpDeviceService](https://developer.android.com/reference/kotlin/android/media/midi/MidiUmpDeviceService.html#) A service that implements a virtual MIDI device for Universal MIDI Packets (UMP).
[MockApplication](https://developer.android.com/reference/kotlin/android/test/mock/MockApplication.html#) A mock `https://developer.android.com/reference/kotlin/android/app/Application.html#` class.
[MockContentProvider](https://developer.android.com/reference/kotlin/android/test/mock/MockContentProvider.html#) Mock implementation of ContentProvider.
[NativeActivity](https://developer.android.com/reference/kotlin/android/app/NativeActivity.html#) Convenience for implementing an activity that will be implemented purely in native code.
[NotificationListenerService](https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#) A service that receives calls from the system when new notifications are posted or removed, or their ranking changed.
[OffHostApduService](https://developer.android.com/reference/kotlin/android/nfc/cardemulation/OffHostApduService.html#) OffHostApduService is a convenience `https://developer.android.com/reference/kotlin/android/app/Service.html#` class that can be extended to describe one or more NFC applications that are residing off-host, for example on an embedded secure element or a UICC.
[PccService](https://developer.android.com/reference/kotlin/android/app/privatecompute/PccService.html#) Abstract base class for a PCC service that receives data from other components.
[PreferenceActivity](https://developer.android.com/reference/kotlin/android/preference/PreferenceActivity.html#) This is the base class for an activity to show a hierarchy of preferences to the user.
[PreferenceFragment](https://developer.android.com/reference/kotlin/android/preference/PreferenceFragment.html#) Shows a hierarchy of `https://developer.android.com/reference/kotlin/android/preference/Preference.html#` objects as lists.
[PrintService](https://developer.android.com/reference/kotlin/android/printservice/PrintService.html#) This is the base class for implementing print services.
[QuickAccessWalletService](https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/QuickAccessWalletService.html#) A `QuickAccessWalletService` provides a list of `WalletCard`s shown in the Quick Access Wallet.
[RecognitionService](https://developer.android.com/reference/kotlin/android/speech/RecognitionService.html#) This class provides a base class for recognition service implementations.
[RemoteViewsService](https://developer.android.com/reference/kotlin/android/widget/RemoteViewsService.html#) The service to be connected to for a remote adapter to request RemoteViews.
[SearchRecentSuggestionsProvider](https://developer.android.com/reference/kotlin/android/content/SearchRecentSuggestionsProvider) This superclass can be used to create a simple search suggestions provider for your application.
[SettingInjectorService](https://developer.android.com/reference/kotlin/android/location/SettingInjectorService.html#) Dynamically specifies the summary (subtitle) and enabled status of a preference injected into the list of app settings displayed by the system settings app
[SettingsPreferenceService](https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceService.html#) Base class for a service that exposes its settings preferences to external access.
[SliceProvider](https://developer.android.com/reference/kotlin/android/app/slice/SliceProvider.html#) A SliceProvider allows an app to provide content to be displayed in system spaces.
[SpellCheckerService](https://developer.android.com/reference/kotlin/android/service/textservice/SpellCheckerService.html#) SpellCheckerService provides an abstract base class for a spell checker.
[TabActivity](https://developer.android.com/reference/kotlin/android/app/TabActivity.html#) For apps developing against `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int` or later, tabs are typically presented in the UI using the new `https://developer.android.com/reference/kotlin/android/app/ActionBar.html#newTab()` and related APIs for placing tabs within their action bar area.
[TextToSpeechService](https://developer.android.com/reference/kotlin/android/speech/tts/TextToSpeechService.html#) Abstract base class for TTS engine implementations.
[TileService](https://developer.android.com/reference/kotlin/android/service/quicksettings/TileService.html#) A TileService provides the user a tile that can be added to Quick Settings.
[TvAdService](https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdService.html#) The TvAdService class represents a TV client-side advertisement service.
[TvInputService](https://developer.android.com/reference/kotlin/android/media/tv/TvInputService.html#) The TvInputService class represents a TV input or source such as HDMI or built-in tuner which provides pass-through video or broadcast TV programs.
[TvInteractiveAppService](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppService.html#) A TV interactive application service is a service that provides runtime environment and runs TV interactive applications.
[VisualVoicemailService](https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailService.html#) This service is implemented by dialer apps that wishes to handle OMTP or similar visual voicemails.
[VoiceInteractionService](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionService.html#) Top-level service of the current global voice interactor, which is providing support for hotwording, the back-end of a `https://developer.android.com/reference/kotlin/android/app/VoiceInteractor.html#`, etc.
[VoiceInteractionSessionService](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSessionService.html#) An active voice interaction session, initiated by a `https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionService.html#`.
[VpnService](https://developer.android.com/reference/kotlin/android/net/VpnService.html#) VpnService is a base class for applications to extend and build their own VPN solutions.
[VrListenerService](https://developer.android.com/reference/kotlin/android/service/vr/VrListenerService.html#) A service that is bound from the system while running in virtual reality (VR) mode.
[WallpaperService](https://developer.android.com/reference/kotlin/android/service/wallpaper/WallpaperService.html#) A wallpaper service is responsible for showing a live wallpaper behind applications that would like to sit on top of it.
[WebViewFragment](https://developer.android.com/reference/kotlin/android/webkit/WebViewFragment.html#) A fragment that displays a WebView.

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
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_RUNNING_CRITICAL:kotlin.Int` Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running extremely low on memory and is about to not be able to keep any background processes running. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_RUNNING_LOW:kotlin.Int` Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running low on memory. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#TRIM_MEMORY_RUNNING_MODERATE:kotlin.Int` Level for `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2#onTrimMemory(kotlin.Int)`: the process is not an expendable background process, but the device is running moderately low on memory. |
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
