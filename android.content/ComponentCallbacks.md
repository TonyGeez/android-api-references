Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ComponentCallbacks

```
interface ComponentCallbacks
```

| [android.content.ComponentCallbacks](ComponentCallbacks.md) |

Known Direct Subclasses [ComponentCallbacks2](ComponentCallbacks2.md) [ComponentCallbacks2](ComponentCallbacks2.md) Callbacks for app state transitions that can be used to improve background memory management.
Known Indirect Subclasses [AbstractInputMethodService](../android.inputmethodservice/AbstractInputMethodService.md), [AccessibilityService](../android.accessibilityservice/AccessibilityService.md), [AccountAuthenticatorActivity](../android.accounts/AccountAuthenticatorActivity.md), [Activity](../android.app/Activity.md), [ActivityGroup](../android.app/ActivityGroup.md), [AliasActivity](../android.app/AliasActivity.md), [AlternativeMessageTransportService](../android/service/messaging/AlternativeMessageTransportService.md), [AppContentProjectionService](../android/media/projection/AppContentProjectionService.md), [AppFunctionService](../android.app.appfunctions/AppFunctionService.md), [Application](../android.app/Application.md), [AutofillService](../android.service.autofill/AutofillService.md), [CallRedirectionService](../android.telecom/CallRedirectionService.md), and 69 others. [AbstractInputMethodService](../android.inputmethodservice/AbstractInputMethodService.md) AbstractInputMethodService provides a abstract base class for input methods.
[AccessibilityService](../android.accessibilityservice/AccessibilityService.md) Accessibility services should only be used to assist users with disabilities in using Android devices and apps.
[AccountAuthenticatorActivity](../android.accounts/AccountAuthenticatorActivity.md) Base class for implementing an Activity that is used to help implement an AbstractAccountAuthenticator.
[Activity](../android.app/Activity.md) An activity is a single, focused thing that the user can do.
[ActivityGroup](../android.app/ActivityGroup.md) A screen that contains and runs multiple embedded activities.
[AliasActivity](../android.app/AliasActivity.md) Stub activity that launches another activity (and then finishes itself) based on information in its component's manifest meta-data.
[AlternativeMessageTransportService](../android/service/messaging/AlternativeMessageTransportService.md) AlternativeMessageTransportService (AMTS) allows the default SMS app to handle the sending of a message over a different transport (e.g. RCS etc.) other than the SMS or MMS.
[AppContentProjectionService](../android/media/projection/AppContentProjectionService.md) Service to be implemented by the application providing the `https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionAppContent.html#`.
[AppFunctionService](../android.app.appfunctions/AppFunctionService.md) Extend this class to implement app functions, that can be executed by android.
[Application](../android.app/Application.md) Base class for maintaining global application state.
[AutofillService](../android.service.autofill/AutofillService.md) An `AutofillService` is a service used to automatically fill the contents of the screen on behalf of a given user - for more information about autofill, read [Autofill Framework](https://developer.android.com/preview/features/autofill.html).
[CallRedirectionService](../android.telecom/CallRedirectionService.md) This service can be implemented to interact between Telecom and its implementor for making outgoing call with optional redirection/cancellation purposes.
[CallScreeningService](../android.telecom/CallScreeningService.md) This service can be implemented by the default dialer (see getDefaultDialerPackage) or a third party app to allow or disallow incoming calls before they are shown to a user.
[CameraPrewarmService](../android.service.media/CameraPrewarmService.md) Extend this class to implement a camera prewarm service.
[CarrierMessagingClientService](../android.service.carrier/CarrierMessagingClientService.md) If the default SMS app has a service that extends this class, the system always tries to bind it so that the process is always running, which allows the app to have a persistent connection to the server.
[CarrierMessagingService](../android.service.carrier/CarrierMessagingService.md) A service that receives calls from the system when new SMS and MMS are sent or received.
[CarrierService](../android.service.carrier/CarrierService.md) A service that exposes carrier-specific functionality to the system.
[ChooserTargetService](../android.service.chooser/ChooserTargetService.md) A service that receives calls from the system when the user is asked to choose a target for an intent explicitly by another app.
[CloudMediaProvider](../android.provider/CloudMediaProvider.md) Base class for a cloud media provider.
[CompanionDeviceService](../android.companion/CompanionDeviceService.md) A service that receives calls from the system with device events.
[ConditionProviderService](../android.service.notification/ConditionProviderService.md) A service that provides conditions about boolean state.
[ConnectionService](../android.telecom/ConnectionService.md) An abstract service that should be implemented by any apps which either:

1. Can make phone calls (VoIP or otherwise) and want those calls to be integrated into the built-in phone app. Referred to as a **system managed** `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService.html#`.
2. Are a standalone calling app and don't want their calls to be integrated into the built-in phone app. Referred to as a **self managed** `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService.html#`.

Once implemented, the needs to take the following steps so that Telecom will bind to it:

<br />

[ContentProvider](ContentProvider.md) Content providers are one of the primary building blocks of Android applications, providing content to applications.
[ContentSafetyAppService](../android.service.contentsafety/ContentSafetyAppService.md) Base class for a service that the `android.app.role.RoleManager.ROLE_CONTENT_SAFETY` role holder must implement.
[ControlsProviderService](../android.service.controls/ControlsProviderService.md) Service implementation allowing applications to contribute controls to the System UI.
[CredentialProviderService](../android.service.credentials/CredentialProviderService.md) Service to be extended by credential providers, in order to return user credentials to the framework.
[DataMigrationToPccService](../android.app.privatecompute/DataMigrationToPccService.md) Base class for a service that handles data migration to the Private Compute Core (PCC) storage of an application.
[DeviceAdminService](../android.app.admin/DeviceAdminService.md) Base class for a service that device owner/profile owners can optionally have.
[DialogFragment](../android.app/DialogFragment.md) A fragment that displays a dialog window, floating on top of its activity's window.
[DocumentsProvider](../android.provider/DocumentsProvider.md) Base class for a document provider.
[DreamService](../android.service.dreams/DreamService.md) Extend this class to implement a custom dream (available to the user as a "Daydream").
[EgressReceiverService](../android.app.privatecompute/EgressReceiverService.md) Base Service to be implemented by the partner agent proxy process to receive egress queries from a client running inside the Private Compute Core (PCC) sandbox.
[ExpandableListActivity](../android.app/ExpandableListActivity.md) An activity that displays an expandable list of items by binding to a data source implementing the ExpandableListAdapter, and exposes event handlers when the user selects an item.
[Fragment](../android.app/Fragment.md) A Fragment is a piece of an application's user interface or behavior that can be placed in an `https://developer.android.com/reference/kotlin/android/app/Activity.html#`.
[HostApduService](../android.nfc.cardemulation/HostApduService.md) HostApduService is a convenience `https://developer.android.com/reference/kotlin/android/app/Service.html#` class that can be extended to emulate an NFC card inside an Android service component.
[HostNfcFService](../android.nfc.cardemulation/HostNfcFService.md) HostNfcFService is a convenience `https://developer.android.com/reference/kotlin/android/app/Service.html#` class that can be extended to emulate an NFC-F card inside an Android service component.
[InCallService](../android.telecom/InCallService.md) This service is implemented by an app that wishes to provide functionality for managing phone calls.
[InputMethodService](../android.inputmethodservice/InputMethodService.md) InputMethodService provides a standard implementation of an InputMethod, which final implementations can derive from and customize.
[IntentService](../android.app/IntentService.md) IntentService is an extension of the `https://developer.android.com/reference/kotlin/android/app/Service.html#` component class that handles asynchronous requests (expressed as Intents) on demand.
[IsolatedService](../android.adservices.ondevicepersonalization/IsolatedService.md) Base class for services that are started by ODP on a call to `OnDevicePersonalizationManager#execute(ComponentName, PersistableBundle, java.util.concurrent.Executor, OutcomeReceiver)` and run in an [isolated process](https://developer.android.com/guide/topics/manifest/service-element#isolated).
[JobService](../android.app.job/JobService.md) Entry point for the callback from the `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler.html#`.
[LauncherActivity](../android.app/LauncherActivity.md) Displays a list of all activities which can be performed for a given intent.
[ListActivity](../android.app/ListActivity.md) An activity that displays a list of items by binding to a data source such as an array or Cursor, and exposes event handlers when the user selects an item.
[ListFragment](../android.app/ListFragment.md) A fragment that displays a list of items by binding to a data source such as an array or Cursor, and exposes event handlers when the user selects an item.
[MediaBrowserService](../android.service.media/MediaBrowserService.md) Base class for media browser services.
[MediaRoute2ProviderService](../android.media/MediaRoute2ProviderService.md) Base class for media route provider services.
[MediaSession2Service](../android.media/MediaSession2Service.md) This API is not generally intended for third party application developers.
[MidiDeviceService](../android.media.midi/MidiDeviceService.md) A service that implements a virtual MIDI device.
[MidiUmpDeviceService](../android.media.midi/MidiUmpDeviceService.md) A service that implements a virtual MIDI device for Universal MIDI Packets (UMP).
[MockApplication](../android.test.mock/MockApplication.md) A mock `https://developer.android.com/reference/kotlin/android/app/Application.html#` class.
[MockContentProvider](../android.test.mock/MockContentProvider.md) Mock implementation of ContentProvider.
[NativeActivity](../android.app/NativeActivity.md) Convenience for implementing an activity that will be implemented purely in native code.
[NotificationListenerService](../android.service.notification/NotificationListenerService.md) A service that receives calls from the system when new notifications are posted or removed, or their ranking changed.
[OffHostApduService](../android.nfc.cardemulation/OffHostApduService.md) OffHostApduService is a convenience `https://developer.android.com/reference/kotlin/android/app/Service.html#` class that can be extended to describe one or more NFC applications that are residing off-host, for example on an embedded secure element or a UICC.
[PccService](../android.app.privatecompute/PccService.md) Abstract base class for a PCC service that receives data from other components.
[PreferenceActivity](../android.preference/PreferenceActivity.md) This is the base class for an activity to show a hierarchy of preferences to the user.
[PreferenceFragment](../android.preference/PreferenceFragment.md) Shows a hierarchy of `https://developer.android.com/reference/kotlin/android/preference/Preference.html#` objects as lists.
[PrintService](../android.printservice/PrintService.md) This is the base class for implementing print services.
[QuickAccessWalletService](../android.service.quickaccesswallet/QuickAccessWalletService.md) A `QuickAccessWalletService` provides a list of `WalletCard`s shown in the Quick Access Wallet.
[RecognitionService](../android.speech/RecognitionService.md) This class provides a base class for recognition service implementations.
[RemoteViewsService](../android.widget/RemoteViewsService.md) The service to be connected to for a remote adapter to request RemoteViews.
[SearchRecentSuggestionsProvider](SearchRecentSuggestionsProvider.md) This superclass can be used to create a simple search suggestions provider for your application.
[Service](../android.app/Service.md) A Service is an application component representing either an application's desire to perform a longer-running operation while not interacting with the user or to supply functionality for other applications to use.
[SettingInjectorService](../android.location/SettingInjectorService.md) Dynamically specifies the summary (subtitle) and enabled status of a preference injected into the list of app settings displayed by the system settings app
[SettingsPreferenceService](../android.service.settings.preferences/SettingsPreferenceService.md) Base class for a service that exposes its settings preferences to external access.
[SliceProvider](../android.app.slice/SliceProvider.md) A SliceProvider allows an app to provide content to be displayed in system spaces.
[SpellCheckerService](../android.service.textservice/SpellCheckerService.md) SpellCheckerService provides an abstract base class for a spell checker.
[TabActivity](../android.app/TabActivity.md) For apps developing against `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int` or later, tabs are typically presented in the UI using the new newTab and related APIs for placing tabs within their action bar area.
[TextToSpeechService](../android.speech.tts/TextToSpeechService.md) Abstract base class for TTS engine implementations.
[TileService](../android.service.quicksettings/TileService.md) A TileService provides the user a tile that can be added to Quick Settings.
[TvAdService](../android.media.tv.ad/TvAdService.md) The TvAdService class represents a TV client-side advertisement service.
[TvInputService](../android.media.tv/TvInputService.md) The TvInputService class represents a TV input or source such as HDMI or built-in tuner which provides pass-through video or broadcast TV programs.
[TvInteractiveAppService](../android.media.tv.interactive/TvInteractiveAppService.md) A TV interactive application service is a service that provides runtime environment and runs TV interactive applications.
[VisualVoicemailService](../android.telephony/VisualVoicemailService.md) This service is implemented by dialer apps that wishes to handle OMTP or similar visual voicemails.
[VoiceInteractionService](../android.service.voice/VoiceInteractionService.md) Top-level service of the current global voice interactor, which is providing support for hotwording, the back-end of a `https://developer.android.com/reference/kotlin/android/app/VoiceInteractor.html#`, etc.
[VoiceInteractionSession](../android.service.voice/VoiceInteractionSession.md) An active voice interaction session, providing a facility for the implementation to interact with the user in the voice interaction layer.
[VoiceInteractionSessionService](../android.service.voice/VoiceInteractionSessionService.md) An active voice interaction session, initiated by a `https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionService.html#`.
[VpnService](../android.net/VpnService.md) VpnService is a base class for applications to extend and build their own VPN solutions.
[VrListenerService](../android.service.vr/VrListenerService.md) A service that is bound from the system while running in virtual reality (VR) mode.
[WallpaperService](../android.service.wallpaper/WallpaperService.md) A wallpaper service is responsible for showing a live wallpaper behind applications that would like to sit on top of it.
[WebViewFragment](../android.webkit/WebViewFragment.md) A fragment that displays a WebView.

The set of callback APIs that are common to all application components (`https://developer.android.com/reference/kotlin/android/app/Activity.html#`, `https://developer.android.com/reference/kotlin/android/app/Service.html#`, ContentProvider, and `https://developer.android.com/reference/kotlin/android/app/Application.html#`).

**Note:** You should also implement the ComponentCallbacks2 interface, which provides the onTrimMemory callback to help your app manage its memory usage more effectively.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onConfigurationChanged Called by the system when the device configuration changes while your component is running. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onLowMemory This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. |

## Public methods

### onConfigurationChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onConfigurationChanged(newConfig: Configuration): Unit
```

Called by the system when the device configuration changes while your component is running. Note that, unlike activities, other components are never restarted when a configuration changes: they must always deal with the results of the change, such as by re-retrieving resources.

At the time that this function has been called, your Resources object will have been updated to return resource values matching the new configuration.

For more information, read [Handling Runtime Changes](https://developer.android.com/guide/topics/resources/runtime-changes.html).

| Parameters ||
|---|---|
| `newConfig` | [Configuration](../android.content.res/Configuration.md): The new device configuration. This value cannot be `null`. |

### onLowMemory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onLowMemory(): Unit
```

**Deprecated:** *Since API level 14 this is superseded by onTrimMemory. Since API level 34 this is never called. If you're overriding ComponentCallbacks2#onTrimMemory and your minSdkVersion is greater than API 14, you can provide an empty implementation for this method.*

This is called when the overall system is running low on memory, and actively running processes should trim their memory usage. While the exact point at which this will be called is not defined, generally it will happen when all background process have been killed. That is, before reaching the point of killing processes hosting service and foreground UI that we would like to avoid killing.
