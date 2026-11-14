Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContextWrapper

```
open class ContextWrapper : Context
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.content.Context](../android/content/Context.md) ||
| | ↳ | [android.content.ContextWrapper](../android/content/ContextWrapper.md) |

Known Direct Subclasses [Application](../android/app/Application.md), [BackupAgent](../android/app/backup/BackupAgent.md), [ContextThemeWrapper](../android/view/ContextThemeWrapper.md), [IsolatedContext](../android/test/IsolatedContext.md), [MutableContextWrapper](../android/content/MutableContextWrapper.md), [RenamingDelegatingContext](../android/test/RenamingDelegatingContext.md), [Service](../android/app/Service.md) [Application](../android/app/Application.md) Base class for maintaining global application state.
[BackupAgent](../android/app/backup/BackupAgent.md) Provides the central interface between an application and Android's data backup infrastructure.
[ContextThemeWrapper](../android/view/ContextThemeWrapper.md) A context wrapper that allows you to modify or replace the theme of the wrapped context.
[IsolatedContext](../android/test/IsolatedContext.md) A mock context which prevents its users from talking to the rest of the device while stubbing enough methods to satify code that tries to talk to other packages.
[MutableContextWrapper](../android/content/MutableContextWrapper.md) Special version of `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#` that allows the base context to be modified after it is initially set.
[RenamingDelegatingContext](../android/test/RenamingDelegatingContext.md) This is a class which delegates to the given context, but performs database and file operations with a renamed database/file name (prefixes default names with a given prefix).
[Service](../android/app/Service.md) A Service is an application component representing either an application's desire to perform a longer-running operation while not interacting with the user or to supply functionality for other applications to use.
Known Indirect Subclasses [AbstractInputMethodService](../android/inputmethodservice/AbstractInputMethodService.md), [AccessibilityService](../android/accessibilityservice/AccessibilityService.md), [AccountAuthenticatorActivity](../android/accounts/AccountAuthenticatorActivity.md), [Activity](../android/app/Activity.md), [ActivityGroup](../android/app/ActivityGroup.md), [AliasActivity](../android/app/AliasActivity.md), [AlternativeMessageTransportService](../android/service/messaging/AlternativeMessageTransportService.md), [AppContentProjectionService](../android/media/projection/AppContentProjectionService.md), [AppFunctionService](../android/app/appfunctions/AppFunctionService.md), [AutofillService](../android/service/autofill/AutofillService.md), [BackupAgentHelper](../android/app/backup/BackupAgentHelper.md), [CallRedirectionService](../android/telecom/CallRedirectionService.md), and 56 others. [AbstractInputMethodService](../android/inputmethodservice/AbstractInputMethodService.md) AbstractInputMethodService provides a abstract base class for input methods.
[AccessibilityService](../android/accessibilityservice/AccessibilityService.md) Accessibility services should only be used to assist users with disabilities in using Android devices and apps.
[AccountAuthenticatorActivity](../android/accounts/AccountAuthenticatorActivity.md) Base class for implementing an Activity that is used to help implement an AbstractAccountAuthenticator.
[Activity](../android/app/Activity.md) An activity is a single, focused thing that the user can do.
[ActivityGroup](../android/app/ActivityGroup.md) A screen that contains and runs multiple embedded activities.
[AliasActivity](../android/app/AliasActivity.md) Stub activity that launches another activity (and then finishes itself) based on information in its component's manifest meta-data.
[AlternativeMessageTransportService](../android/service/messaging/AlternativeMessageTransportService.md) AlternativeMessageTransportService (AMTS) allows the default SMS app to handle the sending of a message over a different transport (e.g. RCS etc.) other than the SMS or MMS.
[AppContentProjectionService](../android/media/projection/AppContentProjectionService.md) Service to be implemented by the application providing the `https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionAppContent.html#`.
[AppFunctionService](../android/app/appfunctions/AppFunctionService.md) Extend this class to implement app functions, that can be executed by android.
[AutofillService](../android/service/autofill/AutofillService.md) An `AutofillService` is a service used to automatically fill the contents of the screen on behalf of a given user - for more information about autofill, read [Autofill Framework](https://developer.android.com/preview/features/autofill.html).
[BackupAgentHelper](../android/app/backup/BackupAgentHelper.md) A convenient `https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent.html#` wrapper class that automatically manages heterogeneous data sets within the backup data, each identified by a unique key prefix.
[CallRedirectionService](../android/telecom/CallRedirectionService.md) This service can be implemented to interact between Telecom and its implementor for making outgoing call with optional redirection/cancellation purposes.
[CallScreeningService](../android/telecom/CallScreeningService.md) This service can be implemented by the default dialer (see `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager.html#getDefaultDialerPackage()`) or a third party app to allow or disallow incoming calls before they are shown to a user.
[CameraPrewarmService](../android/service/media/CameraPrewarmService.md) Extend this class to implement a camera prewarm service.
[CarrierMessagingClientService](../android/service/carrier/CarrierMessagingClientService.md) If the default SMS app has a service that extends this class, the system always tries to bind it so that the process is always running, which allows the app to have a persistent connection to the server.
[CarrierMessagingService](../android/service/carrier/CarrierMessagingService.md) A service that receives calls from the system when new SMS and MMS are sent or received.
[CarrierService](../android/service/carrier/CarrierService.md) A service that exposes carrier-specific functionality to the system.
[ChooserTargetService](../android/service/chooser/ChooserTargetService.md) A service that receives calls from the system when the user is asked to choose a target for an intent explicitly by another app.
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
[MediaBrowserService](../android/service/media/MediaBrowserService.md) Base class for media browser services.
[MediaRoute2ProviderService](../android/media/MediaRoute2ProviderService.md) Base class for media route provider services.
[MediaSession2Service](../android/media/MediaSession2Service.md) This API is not generally intended for third party application developers.
[MidiDeviceService](../android/media/midi/MidiDeviceService.md) A service that implements a virtual MIDI device.
[MidiUmpDeviceService](../android/media/midi/MidiUmpDeviceService.md) A service that implements a virtual MIDI device for Universal MIDI Packets (UMP).
[MockApplication](../android/test/mock/MockApplication.md) A mock `https://developer.android.com/reference/kotlin/android/app/Application.html#` class.
[NativeActivity](../android/app/NativeActivity.md) Convenience for implementing an activity that will be implemented purely in native code.
[NotificationListenerService](../android/service/notification/NotificationListenerService.md) A service that receives calls from the system when new notifications are posted or removed, or their ranking changed.
[OffHostApduService](../android/nfc/cardemulation/OffHostApduService.md) OffHostApduService is a convenience `https://developer.android.com/reference/kotlin/android/app/Service.html#` class that can be extended to describe one or more NFC applications that are residing off-host, for example on an embedded secure element or a UICC.
[PccService](../android/app/privatecompute/PccService.md) Abstract base class for a PCC service that receives data from other components.
[PreferenceActivity](../android/preference/PreferenceActivity.md) This is the base class for an activity to show a hierarchy of preferences to the user.
[PrintService](../android/printservice/PrintService.md) This is the base class for implementing print services.
[QuickAccessWalletService](../android/service/quickaccesswallet/QuickAccessWalletService.md) A `QuickAccessWalletService` provides a list of `WalletCard`s shown in the Quick Access Wallet.
[RecognitionService](../android/speech/RecognitionService.md) This class provides a base class for recognition service implementations.
[RemoteViewsService](../android/widget/RemoteViewsService.md) The service to be connected to for a remote adapter to request RemoteViews.
[SettingInjectorService](../android/location/SettingInjectorService.md) Dynamically specifies the summary (subtitle) and enabled status of a preference injected into the list of app settings displayed by the system settings app
[SettingsPreferenceService](../android/service/settings/preferences/SettingsPreferenceService.md) Base class for a service that exposes its settings preferences to external access.
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

Proxying implementation of Context that simply delegates all of its calls to another Context. Can be subclassed to modify behavior without changing the original Context.

## Summary

Inherited constants From class `https://developer.android.com/reference/kotlin/android/content/Context` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#ACCESSIBILITY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.html#` for giving the user feedback for UI events through the registered event listeners.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#ACCOUNT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/accounts/AccountManager.html#` for receiving intents at a time of your choosing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#ACTIVITY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#` for interacting with the global system state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#ADVANCED_PROTECTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/security/advancedprotection/AdvancedProtectionManager.html#`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#ALARM_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/AlarmManager.html#` for receiving intents at a time of your choosing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#APPWIDGET_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager.html#` for accessing AppWidgets.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#APP_FUNCTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager.html#` for executing app functions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#APP_INTERACTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/app/AppInteractionManager.html#` for managing app interactions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#APP_OPS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#` for tracking application operations on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#APP_SEARCH_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchManager.html#` for indexing and querying app data managed by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#AUDIO_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/AudioManager.html#` for handling management of volume, ringer modes and audio routing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#AUTHENTICATION_POLICY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/AuthenticationPolicyManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#AUTOFILL_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#BATTERY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/BatteryManager.html#` for managing battery state.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#BIND_ABOVE_CLIENT:kotlin.Int`

Flag for #bindService: indicates that the client application binding to this service considers the service to be more important than the app itself. When set, the platform will try to have the out of memory killer kill the app before it kills the service it is bound to, though this is not guaranteed to be the case.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#BIND_ADJUST_WITH_ACTIVITY:kotlin.Int`

Flag for #bindService: If binding from an activity, allow the target service's process importance to be raised based on whether the activity is visible to the user, regardless whether another flag is used to reduce the amount that the client process's overall importance is used to impact it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#BIND_ALLOW_ACTIVITY_STARTS:kotlin.Int`

Flag for #bindService: If binding from an app that is visible, the bound service is allowed to start an activity from background. This was the default behavior before SDK version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`. Since then, the default behavior changed to disallow the bound service to start a background activity even if the app bound to it is in foreground, unless this flag is specified when binding.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#BIND_ALLOW_OOM_MANAGEMENT:kotlin.Int`

Flag for #bindService: allow the process hosting the bound service to go through its normal memory management. It will be treated more like a running service, allowing the system to (temporarily) expunge the process if low on memory or for some other whim it may have, and being more aggressive about making it a candidate to be killed (and restarted) if running for a long time.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#BIND_AUTO_CREATE:kotlin.Int`

Flag for #bindService: automatically create the service as long as the binding exists. Note that while this will create the service, its `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` method will still only be called due to an explicit call to `https://developer.android.com/reference/kotlin/android/content/Context#startService(android.content.Intent)`. Even without that, though, this still provides you with access to the service object while the service is created.

Note that prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, not supplying this flag would also impact how important the system consider's the target service's process to be. When set, the only way for it to be raised was by binding from a service in which case it will only be important when that activity is in the foreground. Now to achieve this behavior you must explicitly supply the new flag `https://developer.android.com/reference/kotlin/android/content/Context#BIND_ADJUST_WITH_ACTIVITY:kotlin.Int`. For compatibility, old applications that don't specify `https://developer.android.com/reference/kotlin/android/content/Context#BIND_AUTO_CREATE:kotlin.Int` will automatically have the flags `https://developer.android.com/reference/kotlin/android/content/Context#BIND_WAIVE_PRIORITY:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/content/Context#BIND_ADJUST_WITH_ACTIVITY:kotlin.Int` set for them in order to achieve the same result.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#BIND_DEBUG_UNBIND:kotlin.Int`

Flag for #bindService: include debugging help for mismatched calls to unbind. When this flag is set, the callstack of the following `https://developer.android.com/reference/kotlin/android/content/Context#unbindService(android.content.ServiceConnection)` call is retained, to be printed if a later incorrect unbind call is made. Note that doing this requires retaining information about the binding that was made for the lifetime of the app, resulting in a leak -- this should only be used for debugging.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#BIND_EXTERNAL_SERVICE:kotlin.Int`

Flag for #bindService: The service being bound is an `https://developer.android.com/reference/kotlin/android/R.attr.html#isolatedProcess:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/R.attr.html#externalService:kotlin.Int` service. This binds the service into the calling application's package, rather than the package in which the service is declared.

When using this flag, the code for the service being bound will execute under the calling application's package name and user ID. Because the service must be an isolated process, it will not have direct access to the application's data, though. The purpose of this flag is to allow applications to provide services that are attributed to the app using the service, rather than the application providing the service.
*This flag is NOT compatible with `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags`. If you need to use `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags`, you must use `https://developer.android.com/reference/kotlin/android/content/Context#BIND_EXTERNAL_SERVICE_LONG:kotlin.Long` instead.*

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#BIND_EXTERNAL_SERVICE_LONG:kotlin.Long`

Works in the same way as `https://developer.android.com/reference/kotlin/android/content/Context#BIND_EXTERNAL_SERVICE:kotlin.Int`, but it's defined as a `long` value that is compatible to `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#BIND_IMPORTANT:kotlin.Int`

Flag for #bindService: this service is very important to the client, so should be brought to the foreground process level when the client is. Normally a process can only be raised to the visibility level by a client, even if that client is in the foreground.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#BIND_INCLUDE_CAPABILITIES:kotlin.Int`

Flag for #bindService: If binding from an app that has specific capabilities due to its foreground state such as an activity or foreground service, then this flag will allow the bound app to get the same capabilities, as long as it has the required permissions as well. If binding from a top app and its target SDK version is at or above `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`, the app needs to explicitly use BIND_INCLUDE_CAPABILITIES flag to pass all capabilities to the service so the other app can have while-in-use access such as location, camera, microphone from background. If binding from a top app and its target SDK version is below `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`, BIND_INCLUDE_CAPABILITIES is implicit.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#BIND_NOT_FOREGROUND:kotlin.Int`

Flag for #bindService: don't allow this binding to raise the target service's process to the foreground scheduling priority. It will still be raised to at least the same memory priority as the client (so that its process will not be killable in any situation where the client is not killable), but for CPU scheduling purposes it may be left in the background. This only has an impact in the situation where the binding client is a foreground process and the target service is in a background process.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#BIND_NOT_PERCEPTIBLE:kotlin.Int`

Flag for #bindService: If binding from an app that is visible or user-perceptible, lower the target service's importance to below the perceptible level. This allows the system to (temporarily) expunge the bound process from memory to make room for more important user-perceptible processes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#BIND_PACKAGE_ISOLATED_PROCESS:kotlin.Int`

Flag for #bindIsolatedService: Bind the service into a shared isolated process, but only with other isolated services from the same package that declare the same process name.

Specifying this flag allows multiple isolated services defined in the same package to be running in a single shared isolated process. This shared isolated process must be specified since this flag will not work with the default application process.

This flag is different from `https://developer.android.com/reference/kotlin/android/content/Context#BIND_SHARED_ISOLATED_PROCESS:kotlin.Int` since it only allows binding services from the same package in the same shared isolated process. This also means the shared package isolated process is global, and not scoped to each potential calling app.

The shared isolated process instance is identified by the "android:process" attribute defined by the service. This flag cannot be used without this attribute set.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#BIND_SHARED_ISOLATED_PROCESS:kotlin.Int`

Flag for #bindIsolatedService: Bind the service into a shared isolated process. Specifying this flag allows multiple isolated services to be running in a single shared isolated process. The shared isolated process instance is identified by the instanceName parameter in `https://developer.android.com/reference/kotlin/android/content/Context#bindIsolatedService(android.content.Intent,%20kotlin.Int,%20kotlin.String,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)`. Subsequent calls to #bindIsolatedService with the same instanceName will cause the isolated service to be co-located in the same shared isolated process. Note that the shared isolated process is scoped to the calling app; once created, only the calling app can bind additional isolated services into the shared process. However, the services themselves can come from different APKs and therefore different vendors. Only services that set the `https://developer.android.com/reference/kotlin/android/R.attr.html#allowSharedIsolatedProcess:kotlin.Int` attribute to `true` are allowed to be bound into a shared isolated process.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#BIND_WAIVE_PRIORITY:kotlin.Int`

Flag for #bindService: don't impact the scheduling or memory management priority of the target service's hosting process. Allows the service's process to be managed on the background LRU list just like a regular application process in the background.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#BIOMETRIC_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/biometrics/BiometricManager.html#` for handling biometric and PIN/pattern/password authentication.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#BLOB_STORE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager.html#` for contributing and accessing data blobs from the blob store maintained by the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#BLUETOOTH_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager.html#` for using Bluetooth.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#BUGREPORT_SERVICE:kotlin.String`

Service to capture a bugreport.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#CAMERA_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.html#` for interacting with camera devices.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#CAPTIONING_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager.html#` for obtaining captioning properties and listening for changes in captioning preferences.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#CARRIER_CONFIG_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.html#` for reading carrier configuration values.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#CHOOSER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/service/chooser/ChooserManager.html#`.

**Note:** This service is not available on Wear OS, Android TV, or Android Auto devices. On these form factors, calls to `getSystemService` for this service will return `null`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#CLIPBOARD_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/ClipboardManager` for accessing and modifying the contents of the global clipboard.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#COMPANION_DEVICE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.html#` for managing companion devices

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#CONNECTIVITY_DIAGNOSTICS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/ConnectivityDiagnosticsManager.html#` for performing network connectivity diagnostics as well as receiving network connectivity information from the system.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#CONNECTIVITY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#` for handling management of network connections.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#CONSUMER_IR_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/ConsumerIrManager.html#` for transmitting infrared signals from the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#CONTACT_KEYS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/provider/E2eeContactKeysManager.html#` to managing contact keys.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#CONTENT_RESTRICTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentSafetyManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#CONTEXT_IGNORE_SECURITY:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/content/Context#createPackageContext(kotlin.String,%20kotlin.Int)`: ignore any security restrictions on the Context being requested, allowing it to always be loaded. For use with `https://developer.android.com/reference/kotlin/android/content/Context#CONTEXT_INCLUDE_CODE:kotlin.Int` to allow code to be loaded into a process even when it isn't safe to do so. Use with extreme care!

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#CONTEXT_INCLUDE_CODE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/content/Context#createPackageContext(kotlin.String,%20kotlin.Int)`: include the application code with the context. This means loading code into the caller's process, so that `https://developer.android.com/reference/kotlin/android/content/Context#getClassLoader()` can be used to instantiate the application's classes. Setting this flags imposes security restrictions on what application context you can access; if the requested application can not be safely loaded into your process, java.lang.SecurityException will be thrown. If this flag is not set, there will be no restrictions on the packages that can be loaded, but `https://developer.android.com/reference/kotlin/android/content/Context#getClassLoader()` will always return the default system class loader.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#CONTEXT_RESTRICTED:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/content/Context#createPackageContext(kotlin.String,%20kotlin.Int)`: a restricted context may disable specific features. For instance, a View associated with a restricted context would ignore particular XML attributes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#CREDENTIAL_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager.html#` to authenticate a user to your app.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#CROSS_PROFILE_APPS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/pm/CrossProfileApps` for cross profile operations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#DEVICE_ID_DEFAULT:kotlin.Int`

The default device ID, which is the ID of the primary (non-virtual) device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#DEVICE_ID_INVALID:kotlin.Int`

Invalid device ID.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#DEVICE_LOCK_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#DEVICE_POLICY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#` for working with global device policy management.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#DISPLAY_HASH_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to access `https://developer.android.com/reference/kotlin/android/view/displayhash/DisplayHashManager.html#` to handle display hashes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#DISPLAY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#` for interacting with display devices.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#DOMAIN_VERIFICATION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to access `https://developer.android.com/reference/kotlin/android/content/pm/verify/domain/DomainVerificationManager` to retrieve approval and user state for declared web domains.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#DOWNLOAD_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/DownloadManager.html#` for requesting HTTP downloads.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#DROPBOX_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/DropBoxManager.html#` instance for recording diagnostic logs.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#EUICC_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/euicc/EuiccManager.html#` to manage the device eUICC (embedded SIM).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#FILE_INTEGRITY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/security/FileIntegrityManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#FILE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/storage/FileManager.html#` for handling file operations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#GAME_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/GameManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#GRAMMATICAL_INFLECTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/GrammaticalInflectionManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#HARDWARE_PROPERTIES_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager.html#` for accessing the hardware properties service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#HEALTHCONNECT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#HID_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/hid/HidManager.html#` for interacting with HID devices.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#INPUT_METHOD_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#` for accessing input methods.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#INPUT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/input/InputManager.html#` for interacting with input devices.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#IPSEC_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/IpSecManager.html#` for encrypting Sockets or Networks with IPSec.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#JOB_SCHEDULER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler.html#` instance for managing occasional background tasks.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#KEYCHAIN_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/security/KeyChainManager.html#` for managing KeyChain certificates and grants.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#KEYGUARD_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.html#` for controlling keyguard.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#KEYSTORE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/security/keystore/KeyStoreManager.html#` for accessing [Android Keystore](../privacy-and-security/keystore.md) functions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#LAUNCHER_APPS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps` for querying and monitoring launchable apps across profiles of a user.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#LAYOUT_INFLATER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` for inflating layout resources in this context.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#LOCALE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/LocaleManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#LOCATION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/location/LocationManager.html#` for controlling location updates.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#MEDIA_COMMUNICATION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/MediaCommunicationManager.html#` for managing `https://developer.android.com/reference/kotlin/android/media/MediaSession2.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#MEDIA_METRICS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/metrics/MediaMetricsManager.html#` for interacting with media metrics on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#MEDIA_PROJECTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionManager.html#` instance for managing media projection sessions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#MEDIA_QUALITY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityManager.html#` for standardize picture and audio API parameters.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#MEDIA_ROUTER_SERVICE:kotlin.String`

Use with #getSystemService to retrieve a `https://developer.android.com/reference/kotlin/android/media/MediaRouter.html#` for controlling and managing routing of media.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#MEDIA_SESSION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.html#` for managing media Sessions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#MEMORY_BUDGET_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/MemoryBudgetManager.html#` for monitoring memory budgets.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#MIDI_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.html#` for accessing the MIDI service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#MODE_APPEND:kotlin.Int`

File creation mode: for use with `https://developer.android.com/reference/kotlin/android/content/Context#openFileOutput(kotlin.String,%20kotlin.Int)`, if the file already exists then write data to the end of the existing file instead of erasing it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#MODE_ENABLE_WRITE_AHEAD_LOGGING:kotlin.Int`

Database open flag: when set, the database is opened with write-ahead logging enabled by default.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#MODE_MULTI_PROCESS:kotlin.Int`

SharedPreference loading flag: when set, the file on disk will be checked for modification even if the shared preferences instance is already loaded in this process. This behavior is sometimes desired in cases where the application has multiple processes, all writing to the same SharedPreferences file. Generally there are better forms of communication between processes, though.

This was the legacy (but undocumented) behavior in and before Gingerbread (Android 2.3) and this flag is implied when targeting such releases. For applications targeting SDK versions *greater than* Android 2.3, this flag must be explicitly set if desired.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#MODE_NO_LOCALIZED_COLLATORS:kotlin.Int`

Database open flag: when set, the database is opened without support for localized collators.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#MODE_PRIVATE:kotlin.Int`

File creation mode: the default mode, where the created file can only be accessed by the calling application (or all applications sharing the same user ID).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#MODE_WORLD_READABLE:kotlin.Int`

File creation mode: allow all other applications to have read access to the created file.

Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int`, attempting to use this mode throws a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#MODE_WORLD_WRITEABLE:kotlin.Int`

File creation mode: allow all other applications to have write access to the created file.

Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int`, attempting to use this mode will throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#MULTISENSORY_MANAGER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve the service that plays multisensory feedback.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#NETWORK_STATS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager.html#` for querying network usage stats.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#NFC_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/nfc/NfcManager.html#` for using NFC.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#NOTIFICATION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#` for informing the user of background events.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#NPU_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#NSD_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.html#` for handling management of network service discovery

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#OVERLAY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/om/OverlayManager` for managing overlay packages.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#PCC_SANDBOX_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccSandboxManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#PEOPLE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to access a `https://developer.android.com/reference/kotlin/android/app/people/PeopleManager.html#` to interact with your published conversations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#PERFORMANCE_HINT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/PerformanceHintManager.html#` for accessing the performance hinting service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#PERSISTENT_DATA_BLOCK_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/service/persistentdata/PersistentDataBlockManager.html#` instance for interacting with a storage device that lives across factory resets.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#POWER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/PowerManager.html#` for controlling power management, including "wake locks," which let you keep the device on while you're running long tasks.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#PRINT_SERVICE:kotlin.String`

`https://developer.android.com/reference/kotlin/android/print/PrintManager.html#` for printing and managing printers and print tasks.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#PROFILING_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/os/ProfilingManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_EXPORTED:kotlin.Int`

Flag for #registerReceiver: The receiver can receive broadcasts from other Apps. Has the same behavior as marking a statically registered receiver with "exported=true"

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_NOT_EXPORTED:kotlin.Int`

Flag for #registerReceiver: The receiver cannot receive broadcasts from other Apps. Has the same behavior as marking a statically registered receiver with "exported=false"

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_VISIBLE_TO_INSTANT_APPS:kotlin.Int`

Flag for #registerReceiver: The receiver can receive broadcasts from Instant Apps.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#RESTRICTIONS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/RestrictionsManager` for retrieving application restrictions and requesting permissions for restricted operations.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#ROLE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#` for managing roles.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#SATELLITE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/satellite/SatelliteManager.html#` for accessing satellite functionality.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#SEARCH_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#` for handling searches.

`https://developer.android.com/reference/kotlin/android/content/res/Configuration#UI_MODE_TYPE_WATCH:kotlin.Int` does not support `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#SECURITY_STATE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/SecurityStateManager.html#` for accessing the security state manager service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#SENSOR_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/SensorManager.html#` for accessing sensors.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#SERIAL_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/serial/SerialManager.html#` for access to serial ports.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#SHORTCUT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager` for accessing the launcher shortcut service.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#STATUS_BAR_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/StatusBarManager.html#` for interacting with the status bar and quick settings.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#STORAGE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.html#` for accessing system storage functions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#STORAGE_STATS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/usage/StorageStatsManager.html#` for accessing system storage statistics.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#SYSTEM_HEALTH_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager.html#` for accessing system health (battery, power, memory, etc) metrics.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#TELECOM_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager.html#` to manage telecom-related features of the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#TELEPHONY_IMS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/telephony/ims/ImsManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#TELEPHONY_PHONE_NUMBER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberManager.html#` for parsing phone numbers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#TELEPHONY_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#` for handling management the telephony features of the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#TELEPHONY_SUBSCRIPTION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.html#` for handling management the telephony subscriptions of the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#TETHERING_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/TetheringManager.html#` for managing tethering functions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#TEXT_CLASSIFICATION_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassificationManager.html#` for text classification services.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#TEXT_SERVICES_MANAGER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/textservice/TextServicesManager.html#` for accessing text services.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#TIME_MANAGER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/time/TimeManager.html#`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#TV_AD_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager.html#` for interacting with TV client-side advertisement services on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#TV_INPUT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/tv/TvInputManager.html#` for interacting with TV inputs on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#TV_INTERACTIVE_APP_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager.html#` for interacting with TV interactive applications on the device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#UI_MODE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/UiModeManager.html#` for controlling UI modes.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#USAGE_STATS_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/app/usage/UsageStatsManager.html#` for querying device usage stats.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#USB_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager.html#` for access to USB devices (as a USB host) and for controlling this device's behavior as a USB device.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#USER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/UserManager.html#` for managing users on devices that support multiple users.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#VIBRATOR_MANAGER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/VibratorManager.html#` for accessing the device vibrators, interacting with individual ones and playing synchronized effects on multiple vibrators.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#VIBRATOR_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/os/Vibrator.html#` for interacting with the vibration hardware.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#VIRTUAL_DEVICE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager.html#` for managing virtual devices. On devices without `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#FEATURE_COMPANION_DEVICE_SETUP:kotlin.String` system feature the `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` will return `null`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#VPN_MANAGEMENT_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/VpnManager.html#` to manage profiles for the platform built-in VPN.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#WALLPAPER_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a com.android.server.WallpaperService for accessing wallpapers.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#WEB_APP_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/content/pm/webapp/WebAppManager`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#WIFI_AWARE_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager.html#` for handling management of Wi-Fi Aware.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#WIFI_P2P_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.html#` for handling management of Wi-Fi peer-to-peer connections.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#WIFI_RTT_RANGING_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/wifi/rtt/WifiRttManager.html#` for ranging devices with wifi.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#WIFI_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#` for handling management of Wi-Fi access.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#WINDOW_SERVICE:kotlin.String`

Use with `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` to retrieve a `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#` for accessing the system's window manager.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#ContextWrapper(android.content.Context)(base: https://developer.android.com/reference/kotlin/android/content/Context!)` <br /> |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#bindIsolatedService(android.content.Intent,%20kotlin.Int,%20kotlin.String,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)(service: https://developer.android.com/reference/kotlin/android/content/Intent, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, instanceName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection)` Variation of #bindService that, in the specific case of isolated services, allows the caller to generate multiple instances of a service from a single component declaration. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#bindService(android.content.Intent,%20android.content.Context.BindServiceFlags,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)(service: https://developer.android.com/reference/kotlin/android/content/Intent, flags: https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection)` See `https://developer.android.com/reference/kotlin/android/content/Context#bindService(android.content.Intent,%20kotlin.Int,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)` Call `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags#of(kotlin.Long)` to obtain a BindServiceFlags object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#bindService(android.content.Intent,%20android.content.ServiceConnection,%20android.content.Context.BindServiceFlags)(service: https://developer.android.com/reference/kotlin/android/content/Intent, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection, flags: https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags)` See `https://developer.android.com/reference/kotlin/android/content/Context#bindService(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int)` Call `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags#of(kotlin.Long)` to obtain a BindServiceFlags object. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#bindService(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int)(service: https://developer.android.com/reference/kotlin/android/content/Intent, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Connects to an application service, creating it if needed. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#bindService(android.content.Intent,%20kotlin.Int,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)(service: https://developer.android.com/reference/kotlin/android/content/Intent, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection)` Same as `https://developer.android.com/reference/kotlin/android/content/Context#bindService(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int)` with executor to control ServiceConnection callbacks. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#bindServiceAsUser(android.content.Intent,%20android.content.ServiceConnection,%20android.content.Context.BindServiceFlags,%20android.os.UserHandle)(service: https://developer.android.com/reference/kotlin/android/content/Intent, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection, flags: https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)` See `https://developer.android.com/reference/kotlin/android/content/Context#bindServiceAsUser(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int,%20android.os.UserHandle)` Call `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags#of(kotlin.Long)` to obtain a BindServiceFlags object. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#bindServiceAsUser(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int,%20android.os.UserHandle)(service: https://developer.android.com/reference/kotlin/android/content/Intent, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)` Binds to a service in the given `user` in the same manner as #bindService. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#checkCallingOrSelfPermission(kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Determine whether the calling process of an IPC *or you* have been granted a particular permission. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#checkCallingOrSelfUriPermission(android.net.Uri,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determine whether the calling process of an IPC *or you* has been granted permission to access a specific URI. |
| --- | --- |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#checkCallingOrSelfUriPermissions(kotlin.collections.MutableList,%20kotlin.Int)(uris: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determine whether the calling process of an IPC *or you* has been granted permission to access a list of URIs. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#checkCallingPermission(kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Determine whether the calling process of an IPC you are handling has been granted a particular permission. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#checkCallingUriPermission(android.net.Uri,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determine whether the calling process and uid has been granted permission to access a specific URI. |
| --- | --- |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#checkCallingUriPermissions(kotlin.collections.MutableList,%20kotlin.Int)(uris: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determine whether the calling process and uid has been granted permission to access a list of URIs. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#checkContentUriPermissionFull(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determine whether a particular process and uid has been granted permission to access a specific content URI. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#checkPermission(kotlin.String,%20kotlin.Int,%20kotlin.Int)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determine whether the given permission is allowed for a particular process and user ID running in the system. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#checkSelfPermission(kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Determine whether *you* have been granted a particular permission. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#checkUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determine whether a particular process and uid has been granted permission to access a specific URI. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#checkUriPermission(android.net.Uri,%20kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#?, readPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, writePermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Check both a Uri and normal permission. |
| --- | --- |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#checkUriPermissions(kotlin.collections.MutableList,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(uris: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determine whether a particular process and uid has been granted permission to access a list of URIs. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#clearWallpaper()()` <br /> |
| open [Context](../android/content/Context.md) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#createAttributionContext(kotlin.String)(attributionTag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Return a new Context object for the current Context but attribute to a different tag. |
| --- | --- |
| open [Context](../android/content/Context.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#createConfigurationContext(android.content.res.Configuration)(overrideConfiguration: https://developer.android.com/reference/kotlin/android/content/res/Configuration)` Return a new Context object for the current Context but whose resources are adjusted to match the given Configuration. |
| open [Context](../android/content/Context.md) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#createContext(android.content.ContextParams)(contextParams: https://developer.android.com/reference/kotlin/android/content/ContextParams)` Creates a context with specific properties and behaviors. |
| open [Context](../android/content/Context.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#createContextForSplit(kotlin.String)(splitName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Return a new Context object for the given split name. |
| --- | --- |
| open [Context](../android/content/Context.md) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#createDeviceContext(kotlin.Int)(deviceId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a new `Context` object from the current context but with device association given by the `deviceId`. |
| open [Context](../android/content/Context.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#createDeviceProtectedStorageContext()()` Return a new Context object for the current Context but whose storage APIs are backed by device-protected storage. |
| open [Context](../android/content/Context.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#createDisplayContext(android.view.Display)(display: https://developer.android.com/reference/kotlin/android/view/Display.html#)` Returns a new `Context` object from the current context but with resources adjusted to match the metrics of `display`. |
| --- | --- |
| open [Context](../android/content/Context.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#createPackageContext(kotlin.String,%20kotlin.Int)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return a new Context object for the given application name. |
| open [Context](../android/content/Context.md) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#createWindowContext(android.view.Display,%20kotlin.Int,%20android.os.Bundle)(display: https://developer.android.com/reference/kotlin/android/view/Display.html#, type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Creates a `Context` for a non-`https://developer.android.com/reference/kotlin/android/app/Activity.html#` window on the given `https://developer.android.com/reference/kotlin/android/view/Display.html#`. |
| open [Context](../android/content/Context.md) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#createWindowContext(kotlin.Int,%20android.os.Bundle)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Creates a Context for a non-activity window. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#databaseList()()` Returns an array of strings naming the private databases associated with this Context's application package. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#deleteDatabase(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Delete an existing private SQLiteDatabase associated with this Context's application package. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#deleteFile(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Delete the given private file associated with this Context's application package. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#deleteSharedPreferences(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Delete an existing shared preferences file. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#enforceCallingOrSelfPermission(kotlin.String,%20kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` If neither you nor the calling process of an IPC you are handling has been granted a particular permission, throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#enforceCallingOrSelfUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` If the calling process of an IPC *or you* has not been granted permission to access a specific URI, throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#enforceCallingPermission(kotlin.String,%20kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` If the calling process of an IPC you are handling has not been granted a particular permission, throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#enforceCallingUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` If the calling process and uid has not been granted permission to access a specific URI, throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#enforcePermission(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` If the given permission is not allowed for a particular process and user ID running in the system, throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#enforceUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` If a particular process and uid has not been granted permission to access a specific URI, throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#enforceUriPermission(android.net.Uri,%20kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#?, readPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, writePermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, pid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Enforce both a Uri and normal permission. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#fileList()()` Returns an array of strings naming the private files associated with this Context's application package. |
| --- | --- |
| open [Context](../android/content/Context.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getApplicationContext()()` Return the context of the single, global Application object of the current process. |
| open [ApplicationInfo](../android/content/pm/ApplicationInfo.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getApplicationInfo()()` Return the full application info for this context's package. |
| open [AssetManager](../android/content/res/AssetManager.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getAssets()()` Returns an AssetManager instance for the application's package. |
| --- | --- |
| open [AttributionSource](../android/content/AttributionSource.md) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getAttributionSource()()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getAttributionTag()()` Attribution can be used in complex apps to logically separate parts of the app. |
| open [Context](../android/content/Context.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getBaseContext()()` <br /> |
| --- | --- |
| open [File](../java/io/File.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getCacheDir()()` Returns the absolute path to the application specific cache directory on the filesystem. |
| open [ClassLoader](../java/lang/ClassLoader.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getClassLoader()()` Return a class loader you can use to retrieve classes in this package. |
| open [File](../java/io/File.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getCodeCacheDir()()` Returns the absolute path to the application specific cache directory on the filesystem designed for storing cached code. |
| --- | --- |
| open [ContentResolver](../android/content/ContentResolver.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getContentResolver()()` Return a ContentResolver instance for your application's package. |
| open [File](../java/io/File.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getDataDir()()` Returns the absolute path to the directory on the filesystem where all private files belonging to this app are stored. |
| open [File](../java/io/File.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getDatabasePath(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the absolute path on the filesystem where a database created with #openOrCreateDatabase is stored. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getDeviceId()()` Gets the device ID this context is associated with. |
| open [File](../java/io/File.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getDir(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve, creating if needed, a new directory in which the application can place its own custom data files. |
| open [Display](../android/view/Display.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getDisplay()()` Get the display this context is associated with. |
| --- | --- |
| open [File](../java/io/File.md)? | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getExternalCacheDir()()` Returns absolute path to application-specific directory on the primary shared/external storage device where the application can place cache files it owns. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [File](../java/io/File.md)!\>! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getExternalCacheDirs()()` Returns absolute paths to application-specific directories on all shared/external storage devices where the application can place cache files it owns. |
| open [File](../java/io/File.md)? | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getExternalFilesDir(kotlin.String)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns the absolute path to the directory on the primary shared/external storage device where the application can place persistent files it owns. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [File](../java/io/File.md)!\>! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getExternalFilesDirs(kotlin.String)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns absolute paths to application-specific directories on all shared/external storage devices where the application can place persistent files it owns. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [File](../java/io/File.md)!\>! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getExternalMediaDirs()()` Returns absolute paths to application-specific directories on all shared/external storage devices where the application can place media files. |
| open [File](../java/io/File.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getFileStreamPath(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the absolute path on the filesystem where a file created with `https://developer.android.com/reference/kotlin/android/content/Context#openFileOutput(kotlin.String,%20kotlin.Int)` is stored. |
| --- | --- |
| open [File](../java/io/File.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getFilesDir()()` Returns the absolute path to the directory on the filesystem where files created with `https://developer.android.com/reference/kotlin/android/content/Context#openFileOutput(kotlin.String,%20kotlin.Int)` are stored. |
| open [Executor](../java/util/concurrent/Executor.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getMainExecutor()()` Return an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that will run enqueued tasks on the main thread associated with this context. |
| open [Looper](../android/os/Looper.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getMainLooper()()` Return the Looper for the main thread of the current process. |
| --- | --- |
| open [File](../java/io/File.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getNoBackupFilesDir()()` Returns the absolute path to the directory on the filesystem similar to `https://developer.android.com/reference/kotlin/android/content/Context#getFilesDir()`. |
| open [File](../java/io/File.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getObbDir()()` Return the primary shared/external storage directory where this application's OBB files (if there are any) can be found. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [File](../java/io/File.md)!\>! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getObbDirs()()` Returns absolute paths to application-specific directories on all shared/external storage devices where the application's OBB files (if there are any) can be found. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getOpPackageName()()` Return the package name that should be used for `https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#` calls from this context, so that app ops manager's uid verification will work with the name. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getPackageCodePath()()` Return the full path to this context's primary Android package. |
| open [PackageManager](../android/content/pm/PackageManager.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getPackageManager()()` Return PackageManager instance to find global package information. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getPackageName()()` Return the name of this application's package. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getPackageResourcePath()()` Return the full path to this context's primary Android package. |
| open [ContextParams](../android/content/ContextParams.md)? | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getParams()()` Return the set of parameters which this Context was created with, if it was created via `https://developer.android.com/reference/kotlin/android/content/Context#createContext(android.content.ContextParams)`. |
| --- | --- |
| open [Resources](../android/content/res/Resources.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getResources()()` Returns a Resources instance for the application's package. |
| open [SharedPreferences](../android/content/SharedPreferences.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getSharedPreferences(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve and hold the contents of the preferences file 'name', returning a SharedPreferences through which you can retrieve and modify its values. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getSystemService(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Return the handle to a system-level service by name. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getSystemServiceName(java.lang.Class)(serviceClass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<*>)` Gets the name of the system-level service that is represented by the specified class. |
| open [Resources.Theme](../android/content/res/Resources.Theme.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getTheme()()` Return the Theme object associated with this Context. |
| open [Drawable](../android/graphics/drawable/Drawable.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getWallpaper()()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getWallpaperDesiredMinimumHeight()()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getWallpaperDesiredMinimumWidth()()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#grantUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)(toPackage: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Grant permission to access a specific Uri to another package, regardless of whether that package has general permission to access the Uri's content provider. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#isDeviceProtectedStorage()()` Indicates if the storage APIs of this Context are backed by device-protected storage. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#isRestricted()()` Indicates whether this Context is restricted. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#isUiContext()()` Returns `true` if the context is a UI context which can access UI components such as `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#`, `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` or `https://developer.android.com/reference/kotlin/android/app/WallpaperManager.html#`. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#moveDatabaseFrom(android.content.Context,%20kotlin.String)(sourceContext: https://developer.android.com/reference/kotlin/android/content/Context!, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Move an existing database file from the given source storage context to this context. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#moveSharedPreferencesFrom(android.content.Context,%20kotlin.String)(sourceContext: https://developer.android.com/reference/kotlin/android/content/Context!, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Move an existing shared preferences file from the given source storage context to this context. |
| open [FileInputStream](../java/io/FileInputStream.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#openFileInput(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Open a private file associated with this Context's application package for reading. |
| --- | --- |
| open [FileOutputStream](../java/io/FileOutputStream.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#openFileOutput(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Open a private file associated with this Context's application package for writing. |
| open [SQLiteDatabase](../android/database/sqlite/SQLiteDatabase.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#openOrCreateDatabase(kotlin.String,%20kotlin.Int,%20android.database.sqlite.SQLiteDatabase.CursorFactory)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, factory: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory.html#!)` Open a new private SQLiteDatabase associated with this Context's application package. |
| open [SQLiteDatabase](../android/database/sqlite/SQLiteDatabase.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#openOrCreateDatabase(kotlin.String,%20kotlin.Int,%20android.database.sqlite.SQLiteDatabase.CursorFactory,%20android.database.DatabaseErrorHandler)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, factory: https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.CursorFactory.html#!, errorHandler: https://developer.android.com/reference/kotlin/android/database/DatabaseErrorHandler.html#?)` Open a new private SQLiteDatabase associated with this Context's application package. |
| --- | --- |
| open [Drawable](../android/graphics/drawable/Drawable.md)! | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#peekWallpaper()()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#rebindService(android.content.ServiceConnection,%20android.content.Context.BindServiceFlags)(conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection, flags: https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags)` Rebind an application service with updated bind service flags |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#registerComponentCallbacks(android.content.ComponentCallbacks)(callback: https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks!)` Add a new `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks` to the base application of the Context, which will be called at the same times as the ComponentCallbacks methods of activities and other components are called. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#registerDeviceIdChangeListener(java.util.concurrent.Executor,%20java.util.function.IntConsumer)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/java/util/function/IntConsumer.html#)` Adds a new device ID changed listener to the `Context`, which will be called when the device association is changed by the system. |
| open [Intent](../android/content/Intent.md)? | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)(receiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver?, filter: https://developer.android.com/reference/kotlin/android/content/IntentFilter!)` Register a BroadcastReceiver to be run in the main activity thread. |
| open [Intent](../android/content/Intent.md)? | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.Int)(receiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver?, filter: https://developer.android.com/reference/kotlin/android/content/IntentFilter!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Register to receive intent broadcasts, with the receiver optionally being exposed to Instant Apps. |
| --- | --- |
| open [Intent](../android/content/Intent.md)? | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.String,%20android.os.Handler)(receiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver?, filter: https://developer.android.com/reference/kotlin/android/content/IntentFilter!, broadcastPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?)` Register to receive intent broadcasts, to run in the context of scheduler. |
| open [Intent](../android/content/Intent.md)? | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.String,%20android.os.Handler,%20kotlin.Int)(receiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver?, filter: https://developer.android.com/reference/kotlin/android/content/IntentFilter!, broadcastPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Register to receive intent broadcasts, to run in the context of scheduler. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#removeStickyBroadcast(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent!)` Remove the data previously sent with #sendStickyBroadcast, so that it is as if the sticky broadcast had never happened. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#removeStickyBroadcastAsUser(android.content.Intent,%20android.os.UserHandle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!)` Version of `https://developer.android.com/reference/kotlin/android/content/Context#removeStickyBroadcast(android.content.Intent)` that allows you to specify the user the broadcast will be sent to. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#revokeSelfPermissionsOnKill(kotlin.collections.MutableCollection)(permissions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)` Triggers the revocation of one or more permissions for the calling package. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#revokeUriPermission(android.net.Uri,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Remove all permissions to access a particular content provider Uri that were previously added with `https://developer.android.com/reference/kotlin/android/content/Context#grantUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)` or *any other* mechanism. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#revokeUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)(targetPackage: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Remove permissions to access a particular content provider Uri that were previously added with `https://developer.android.com/reference/kotlin/android/content/Context#grantUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)` for a specific target package. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#sendBroadcast(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent!)` Broadcast the given intent to all interested BroadcastReceivers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#sendBroadcast(android.content.Intent,%20kotlin.String)(intent: https://developer.android.com/reference/kotlin/android/content/Intent!, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Broadcast the given intent to all interested BroadcastReceivers, allowing an optional required permission to be enforced. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#sendBroadcast(android.content.Intent,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Broadcast the given intent to all interested BroadcastReceivers, allowing an optional required permission to be enforced. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#sendBroadcastAsUser(android.content.Intent,%20android.os.UserHandle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!)` Version of `https://developer.android.com/reference/kotlin/android/content/Context#sendBroadcast(android.content.Intent)` that allows you to specify the user the broadcast will be sent to. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#sendBroadcastAsUser(android.content.Intent,%20android.os.UserHandle,%20kotlin.String)(intent: https://developer.android.com/reference/kotlin/android/content/Intent!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Version of `https://developer.android.com/reference/kotlin/android/content/Context#sendBroadcast(android.content.Intent,%20kotlin.String)` that allows you to specify the user the broadcast will be sent to. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#sendOrderedBroadcast(android.content.Intent,%20kotlin.Int,%20kotlin.String,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.String,%20android.os.Bundle,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, receiverAppOp: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)(intent: https://developer.android.com/reference/kotlin/android/content/Intent!, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Broadcast the given intent to all interested BroadcastReceivers, delivering them one at a time to allow more preferred receivers to consume the broadcast before it is delivered to less preferred receivers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Version of `https://developer.android.com/reference/kotlin/android/content/Context#sendBroadcast(android.content.Intent)` that allows you to receive data back from the broadcast. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Broadcast the given intent to all interested BroadcastReceivers, delivering them one at a time to allow more preferred receivers to consume the broadcast before it is delivered to less preferred receivers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20android.os.Bundle,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Version of `https://developer.android.com/reference/kotlin/android/content/Context#sendBroadcast(android.content.Intent)` that allows you to receive data back from the broadcast. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, receiverAppOp: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Version of `https://developer.android.com/reference/kotlin/android/content/Context#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)` that allows you to specify the App Op to enforce restrictions on which receivers the broadcast will be sent to. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#sendOrderedBroadcastAsUser(android.content.Intent,%20android.os.UserHandle,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!, receiverPermission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Version of `https://developer.android.com/reference/kotlin/android/content/Context#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)` that allows you to specify the user the broadcast will be sent to. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#sendStickyBroadcast(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent!)` Perform a `https://developer.android.com/reference/kotlin/android/content/Context#sendBroadcast(android.content.Intent)` that is "sticky," meaning the Intent you are sending stays around after the broadcast is complete, so that others can quickly retrieve that data through the return value of `https://developer.android.com/reference/kotlin/android/content/Context#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#sendStickyBroadcast(android.content.Intent,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Perform a `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#sendBroadcast(android.content.Intent)` that is "sticky," meaning the Intent you are sending stays around after the broadcast is complete, so that others can quickly retrieve that data through the return value of `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#sendStickyBroadcastAsUser(android.content.Intent,%20android.os.UserHandle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!)` Version of `https://developer.android.com/reference/kotlin/android/content/Context#sendStickyBroadcast(android.content.Intent)` that allows you to specify the user the broadcast will be sent to. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#sendStickyOrderedBroadcast(android.content.Intent,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent!, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Version of #sendStickyBroadcast that allows you to receive data back from the broadcast. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#sendStickyOrderedBroadcastAsUser(android.content.Intent,%20android.os.UserHandle,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent!, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!, resultReceiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver?, scheduler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?, initialCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, initialData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, initialExtras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Version of `https://developer.android.com/reference/kotlin/android/content/Context#sendStickyOrderedBroadcast(android.content.Intent,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)` that allows you to specify the user the broadcast will be sent to. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#setTheme(kotlin.Int)(resid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the base theme for this context. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#setWallpaper(android.graphics.Bitmap)(bitmap: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#!)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#setWallpaper(java.io.InputStream)(data: https://developer.android.com/reference/kotlin/java/io/InputStream.html#!)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#shouldShowRequestPermissionRationale(kotlin.String)(permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Gets whether you should show UI with rationale before requesting a permission. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#startActivities(kotlin.Array)(intents: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/Intent!>!)` Same as `https://developer.android.com/reference/kotlin/android/content/Context#startActivities(kotlin.Array,%20android.os.Bundle)` with no options specified. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#startActivities(kotlin.Array,%20android.os.Bundle)(intents: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/content/Intent!>!, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Launch multiple new activities. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#startActivity(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent!)` Same as `https://developer.android.com/reference/kotlin/android/content/Context#startActivity(android.content.Intent,%20android.os.Bundle)` with no options specified. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#startActivity(android.content.Intent,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/Intent!, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Launch a new activity. |
| open [ComponentName](../android/content/ComponentName.md)? | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#startForegroundService(android.content.Intent)(service: https://developer.android.com/reference/kotlin/android/content/Intent!)` Similar to `https://developer.android.com/reference/kotlin/android/content/Context#startService(android.content.Intent)`, but with an implicit promise that the Service will call `https://developer.android.com/reference/kotlin/android/app/Service.html#startForeground(kotlin.Int,%20android.app.Notification)` once it begins running. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#startInstrumentation(android.content.ComponentName,%20kotlin.String,%20android.os.Bundle)(className: https://developer.android.com/reference/kotlin/android/content/ComponentName, profileFile: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, arguments: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Start executing an `https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#` class. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#startIntentSender(android.content.IntentSender,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(intent: https://developer.android.com/reference/kotlin/android/content/IntentSender!, fillInIntent: https://developer.android.com/reference/kotlin/android/content/Intent?, flagsMask: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flagsValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, extraFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Same as `https://developer.android.com/reference/kotlin/android/content/Context#startIntentSender(android.content.IntentSender,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)` with no options specified. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#startIntentSender(android.content.IntentSender,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)(intent: https://developer.android.com/reference/kotlin/android/content/IntentSender!, fillInIntent: https://developer.android.com/reference/kotlin/android/content/Intent?, flagsMask: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flagsValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, extraFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?)` Like `https://developer.android.com/reference/kotlin/android/content/Context#startActivity(android.content.Intent,%20android.os.Bundle)`, but taking a IntentSender to start. |
| --- | --- |
| open [ComponentName](../android/content/ComponentName.md)? | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#startService(android.content.Intent)(service: https://developer.android.com/reference/kotlin/android/content/Intent!)` Request that a given application service be started. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#stopService(android.content.Intent)(name: https://developer.android.com/reference/kotlin/android/content/Intent!)` Request that a given application service be stopped. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#unbindService(android.content.ServiceConnection)(conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection)` Disconnect from an application service. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#unregisterComponentCallbacks(android.content.ComponentCallbacks)(callback: https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks!)` Remove a `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks` object that was previously registered with `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#registerComponentCallbacks(android.content.ComponentCallbacks)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#unregisterDeviceIdChangeListener(java.util.function.IntConsumer)(listener: https://developer.android.com/reference/kotlin/java/util/function/IntConsumer.html#)` Removes a device ID changed listener from the Context. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#unregisterReceiver(android.content.BroadcastReceiver)(receiver: https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver!)` Unregister a previously registered BroadcastReceiver. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#updateServiceBindings(kotlin.collections.MutableCollection)(params: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/android/content/Context.UpdateBindingParams!>)` Perform a batch update of existing bindings. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#updateServiceGroup(android.content.ServiceConnection,%20kotlin.Int,%20kotlin.Int)(conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection, group: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, importance: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` For a service previously bound with #bindService or a related method, change how the system manages that service's process in relation to other processes. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#attachBaseContext(android.content.Context)(base: https://developer.android.com/reference/kotlin/android/content/Context!)` Set the base context for this ContextWrapper. |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/content/Context` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#bindIsolatedService(android.content.Intent,%20android.content.Context.BindServiceFlags,%20kotlin.String,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)(service: https://developer.android.com/reference/kotlin/android/content/Intent, flags: https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags, instanceName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, conn: https://developer.android.com/reference/kotlin/android/content/ServiceConnection)`

See `https://developer.android.com/reference/kotlin/android/content/Context#bindIsolatedService(android.content.Intent,%20kotlin.Int,%20kotlin.String,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)` Call `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags#of(kotlin.Long)` to obtain a BindServiceFlags object.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#getColor(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns a color associated with a particular resource ID and styled for the current theme.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/ColorStateList` `https://developer.android.com/reference/kotlin/android/content/Context#getColorStateList(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns a color state list associated with a particular resource ID and styled for the current theme.

<br />

`https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` `https://developer.android.com/reference/kotlin/android/content/Context#getDrawable(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns a drawable object associated with a particular resource ID and styled for the current theme.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#getString(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Returns a localized string from the application's package's default string table.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#getString(kotlin.Int,%20kotlin.Any)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, vararg formatArgs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)`

Returns a localized formatted string from the application's package's default string table, substituting the format arguments as defined in `https://developer.android.com/reference/kotlin/java/util/Formatter.html#` and java.lang.String#format.

<br />

`T` `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(java.lang.Class)(serviceClass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>)`

Return the handle to a system-level service by class.

Currently available classes are: `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#`, `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#`, `https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#`, `https://developer.android.com/reference/kotlin/android/os/PowerManager.html#`, `https://developer.android.com/reference/kotlin/android/app/AlarmManager.html#`, `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#`, `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.html#`, `https://developer.android.com/reference/kotlin/android/location/LocationManager.html#`, `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#`, `https://developer.android.com/reference/kotlin/android/os/Vibrator.html#`, `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#`, `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#`, `https://developer.android.com/reference/kotlin/android/media/AudioManager.html#`, `https://developer.android.com/reference/kotlin/android/media/MediaRouter.html#`, `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#`, `https://developer.android.com/reference/kotlin/android/telephony/SubscriptionManager.html#`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#`, `https://developer.android.com/reference/kotlin/android/app/UiModeManager.html#`, `https://developer.android.com/reference/kotlin/android/app/DownloadManager.html#`, `https://developer.android.com/reference/kotlin/android/os/BatteryManager.html#`, `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler.html#`, `https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager.html#`, `https://developer.android.com/reference/kotlin/android/content/pm/verify/domain/DomainVerificationManager`, `https://developer.android.com/reference/kotlin/android/view/displayhash/DisplayHashManager.html#` `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/AuthenticationPolicyManager.html#`.

Note: System services obtained via this API may be closely associated with the Context in which they are obtained from. In general, do not share the service objects between various different contexts (Activities, Applications, Services, Providers, etc.)

Note: Instant apps, for which `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#isInstantApp()` returns true, don't have access to the following system services: `https://developer.android.com/reference/kotlin/android/content/Context#DEVICE_POLICY_SERVICE:kotlin.String`, #FINGERPRINT_SERVICE, `https://developer.android.com/reference/kotlin/android/content/Context#KEYGUARD_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context#SHORTCUT_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context#USB_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context#WALLPAPER_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context#WIFI_P2P_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context#WIFI_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context#WIFI_AWARE_SERVICE:kotlin.String`. For these services this method will return `null`. Generally, if you are running as an instant app you should always check whether the result of this method is `null`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#getText(kotlin.Int)(resId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Return a localized, styled CharSequence from the application's package's default string table.

<br />

`https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags` `https://developer.android.com/reference/kotlin/android/content/Context#getUpdateableFlags()()`

Gets the list of bind flags that may be updated (i.e. added or removed) for an existing connection. Includes:

- `https://developer.android.com/reference/kotlin/android/content/Context#BIND_NOT_FOREGROUND:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Context#BIND_ABOVE_CLIENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Context#BIND_ALLOW_OOM_MANAGEMENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Context#BIND_WAIVE_PRIORITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Context#BIND_IMPORTANT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Context#BIND_ADJUST_WITH_ACTIVITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/Context#BIND_NOT_PERCEPTIBLE:kotlin.Int`

<br />

<br />

`https://developer.android.com/reference/kotlin/android/content/res/TypedArray` `https://developer.android.com/reference/kotlin/android/content/Context#obtainStyledAttributes(android.util.AttributeSet,%20kotlin.IntArray)(set: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#?, attrs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`

Retrieve styled attribute information in this Context's theme. See `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme#obtainStyledAttributes(android.util.AttributeSet,%20kotlin.IntArray,%20kotlin.Int,%20kotlin.Int)` for more information.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/TypedArray` `https://developer.android.com/reference/kotlin/android/content/Context#obtainStyledAttributes(android.util.AttributeSet,%20kotlin.IntArray,%20kotlin.Int,%20kotlin.Int)(set: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#?, attrs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html, defStyleAttr: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, defStyleRes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Retrieve styled attribute information in this Context's theme. See `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme#obtainStyledAttributes(android.util.AttributeSet,%20kotlin.IntArray,%20kotlin.Int,%20kotlin.Int)` for more information.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/TypedArray` `https://developer.android.com/reference/kotlin/android/content/Context#obtainStyledAttributes(kotlin.Int,%20kotlin.IntArray)(resid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, attrs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`

Retrieve styled attribute information in this Context's theme. See `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme#obtainStyledAttributes(kotlin.Int,%20kotlin.IntArray)` for more information.

<br />

`https://developer.android.com/reference/kotlin/android/content/res/TypedArray` `https://developer.android.com/reference/kotlin/android/content/Context#obtainStyledAttributes(kotlin.IntArray)(attrs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)`

Retrieve styled attribute information in this Context's theme. See `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme#obtainStyledAttributes(kotlin.IntArray)` for more information.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#revokeSelfPermissionOnKill(kotlin.String)(permName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`

Triggers the asynchronous revocation of a runtime permission. If the permission is not currently granted, nothing happens (even if later granted by the user).

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/Context#sendBroadcastWithMultiplePermissions(android.content.Intent,%20kotlin.Array)(intent: https://developer.android.com/reference/kotlin/android/content/Intent, receiverPermissions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)`

Broadcast the given intent to all interested BroadcastReceivers, allowing an array of required permissions to be enforced. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run. No results are propagated from receivers and receivers can not abort the broadcast. If you want to allow receivers to propagate results or abort the broadcast, you must send an ordered broadcast using `https://developer.android.com/reference/kotlin/android/content/Context#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver` for more information on Intent broadcasts.

<br />

## Public constructors

### ContextWrapper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ContextWrapper(base: Context!)
```

## Public methods

### bindIsolatedService

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun bindIsolatedService(
    service: Intent, 
    flags: Int, 
    instanceName: String, 
    executor: Executor, 
    conn: ServiceConnection
): Boolean
```

Variation of #bindService that, in the specific case of isolated services, allows the caller to generate multiple instances of a service from a single component declaration. In other words, you can use this to bind to a service that has specified `https://developer.android.com/reference/kotlin/android/R.attr.html#isolatedProcess:kotlin.Int` and, in addition to the existing behavior of running in an isolated process, you can also through the arguments here have the system bring up multiple concurrent processes hosting their own instances of that service. The instanceName you provide here identifies the different instances, and you can use `https://developer.android.com/reference/kotlin/android/content/Context#updateServiceGroup(android.content.ServiceConnection,%20kotlin.Int,%20kotlin.Int)` to tell the system how it should manage each of these instances.

| Parameters ||
|---|---|
| `service` | [Intent](../android/content/Intent.md): Identifies the service to connect to. The Intent must specify an explicit component name. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Operation options for the binding as per #bindService. |
| `instanceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Unique identifier for the service instance. Each unique name here will result in a different service instance being created. Identifiers must only contain ASCII letters, digits, underscores, and periods. This value cannot be `null`. |
| --- | --- |
| `executor` | [Executor](../java/util/concurrent/Executor.md): Callbacks on ServiceConnection will be called on executor. Must use same instance for the same instance of ServiceConnection. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `conn` | [ServiceConnection](../android/content/ServiceConnection.md): Receives information as the service is started and stopped. This must be a valid ServiceConnection object; it must not be null. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns success of binding as per #bindService. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the instanceName is invalid. |
| `java.lang.SecurityException` | If the caller does not have permission to access the service |

### bindService

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun bindService(
    service: Intent, 
    flags: Context.BindServiceFlags, 
    executor: Executor, 
    conn: ServiceConnection
): Boolean
```

See `https://developer.android.com/reference/kotlin/android/content/Context#bindService(android.content.Intent,%20kotlin.Int,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)` Call `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags#of(kotlin.Long)` to obtain a BindServiceFlags object.

| Parameters ||
|---|---|
| `service` | [Intent](../android/content/Intent.md): This value cannot be `null`. |
| `flags` | [Context.BindServiceFlags](../android/content/Context.BindServiceFlags.md): This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md): This value cannot be `null`. |
| --- | --- |
| `conn` | [ServiceConnection](../android/content/ServiceConnection.md): This value cannot be `null`. |

### bindService

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun bindService(
    service: Intent, 
    conn: ServiceConnection, 
    flags: Context.BindServiceFlags
): Boolean
```

See `https://developer.android.com/reference/kotlin/android/content/Context#bindService(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int)` Call `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags#of(kotlin.Long)` to obtain a BindServiceFlags object.

| Parameters ||
|---|---|
| `service` | [Intent](../android/content/Intent.md): This value cannot be `null`. |
| `conn` | [ServiceConnection](../android/content/ServiceConnection.md): This value cannot be `null`. |
| `flags` | [Context.BindServiceFlags](../android/content/Context.BindServiceFlags.md): This value cannot be `null`. |
| --- | --- |

### bindService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun bindService(
    service: Intent, 
    conn: ServiceConnection, 
    flags: Int
): Boolean
```

Connects to an application service, creating it if needed. This defines a dependency between your application and the service. The given conn will receive the service object when it is created and be told if it dies and restarts. The service will be considered required by the system only for as long as the calling context exists. For example, if this Context is an Activity that is stopped, the service will not be required to continue running until the Activity is resumed.

If the service does not support binding, it may return `null` from its `https://developer.android.com/reference/kotlin/android/app/Service.html#onBind(android.content.Intent)` method. If it does, then the ServiceConnection's `https://developer.android.com/reference/kotlin/android/content/ServiceConnection#onNullBinding(android.content.ComponentName)` method will be invoked instead of `https://developer.android.com/reference/kotlin/android/content/ServiceConnection#onServiceConnected(android.content.ComponentName,%20android.os.IBinder)`.

**Note:** This method *cannot* be called from a `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver` component. A pattern you can use to communicate from a BroadcastReceiver to a Service is to call `https://developer.android.com/reference/kotlin/android/content/Context#startService(android.content.Intent)` with the arguments containing the command to be sent, with the service calling its `https://developer.android.com/reference/kotlin/android/app/Service.html#stopSelf(kotlin.Int)` method when done executing that command. See the API demo App/Service/Service Start Arguments Controller for an illustration of this. It is okay, however, to use this method from a BroadcastReceiver that has been registered with #registerReceiver, since the lifetime of this BroadcastReceiver is tied to another object (the one that registered it).

This method only accepts a int type flag, to pass in a long type flag, call `https://developer.android.com/reference/kotlin/android/content/Context#bindService(android.content.Intent,%20android.content.ServiceConnection,%20android.content.Context.BindServiceFlags)` instead.

| Parameters ||
|---|---|
| `service` | [Intent](../android/content/Intent.md): Identifies the service to connect to. The Intent must specify an explicit component name. This value cannot be `null`. |
| `conn` | [ServiceConnection](../android/content/ServiceConnection.md): Receives information as the service is started and stopped. This must be a valid ServiceConnection object; it must not be null. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Operation options for the binding. Can be: - 0 - `https://developer.android.com/reference/kotlin/android/content/Context#BIND_AUTO_CREATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#BIND_DEBUG_UNBIND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#BIND_NOT_FOREGROUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#BIND_ABOVE_CLIENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#BIND_ALLOW_OOM_MANAGEMENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#BIND_WAIVE_PRIORITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#BIND_IMPORTANT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#BIND_ADJUST_WITH_ACTIVITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#BIND_NOT_PERCEPTIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#BIND_INCLUDE_CAPABILITIES:kotlin.Int` |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the system is in the process of bringing up a service that your client has permission to bind to; `false` if the system couldn't find the service or if your client doesn't have permission to bind to it. Regardless of the return value, you should later call `https://developer.android.com/reference/kotlin/android/content/Context#unbindService(android.content.ServiceConnection)` to release the connection. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If the caller does not have permission to access the service or the service cannot be found. Call `https://developer.android.com/reference/kotlin/android/content/Context#unbindService(android.content.ServiceConnection)` to release the connection when this exception is thrown. |

### bindService

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun bindService(
    service: Intent, 
    flags: Int, 
    executor: Executor, 
    conn: ServiceConnection
): Boolean
```

Same as `https://developer.android.com/reference/kotlin/android/content/Context#bindService(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int)` with executor to control ServiceConnection callbacks.

This method only accepts a 32 bits flag, to pass in a 64 bits flag, call `https://developer.android.com/reference/kotlin/android/content/Context#bindService(android.content.Intent,%20android.content.Context.BindServiceFlags,%20java.util.concurrent.Executor,%20android.content.ServiceConnection)` instead.

| Parameters ||
|---|---|
| `service` | [Intent](../android/content/Intent.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Context#BIND_AUTO_CREATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#BIND_DEBUG_UNBIND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#BIND_NOT_FOREGROUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#BIND_ABOVE_CLIENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#BIND_ALLOW_OOM_MANAGEMENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#BIND_WAIVE_PRIORITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#BIND_IMPORTANT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#BIND_ADJUST_WITH_ACTIVITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#BIND_NOT_PERCEPTIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#BIND_ALLOW_ACTIVITY_STARTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#BIND_INCLUDE_CAPABILITIES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#BIND_SHARED_ISOLATED_PROCESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#BIND_PACKAGE_ISOLATED_PROCESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#BIND_EXTERNAL_SERVICE:kotlin.Int` |
| `executor` | [Executor](../java/util/concurrent/Executor.md): Callbacks on ServiceConnection will be called on executor. Must use same instance for the same instance of ServiceConnection. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| --- | --- |
| `conn` | [ServiceConnection](../android/content/ServiceConnection.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | The result of the binding as described in `https://developer.android.com/reference/kotlin/android/content/Context#bindService(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int)`. |

### bindServiceAsUser

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun bindServiceAsUser(
    service: Intent, 
    conn: ServiceConnection, 
    flags: Context.BindServiceFlags, 
    user: UserHandle
): Boolean
```

See `https://developer.android.com/reference/kotlin/android/content/Context#bindServiceAsUser(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int,%20android.os.UserHandle)` Call `https://developer.android.com/reference/kotlin/android/content/Context.BindServiceFlags#of(kotlin.Long)` to obtain a BindServiceFlags object.

| Parameters ||
|---|---|
| `service` | [Intent](../android/content/Intent.md): This value cannot be `null`. |
| `conn` | [ServiceConnection](../android/content/ServiceConnection.md): This value cannot be `null`. |
| `flags` | [Context.BindServiceFlags](../android/content/Context.BindServiceFlags.md): This value cannot be `null`. |
| --- | --- |
| `user` | [UserHandle](../android/os/UserHandle.md): This value cannot be `null`. |

### bindServiceAsUser

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun bindServiceAsUser(
    service: Intent, 
    conn: ServiceConnection, 
    flags: Int, 
    user: UserHandle
): Boolean
```

Binds to a service in the given `user` in the same manner as #bindService.

Requires that one of the following conditions are met:

- caller has `android.Manifest.permission.INTERACT_ACROSS_USERS_FULL`
- caller has `android.Manifest.permission.INTERACT_ACROSS_USERS` and is the same package as the `service` (determined by its component's package) and the Android version is at least `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`
- caller has `android.Manifest.permission.INTERACT_ACROSS_USERS` and is in same profile group as the given `user`
- caller has `android.Manifest.permission.INTERACT_ACROSS_PROFILES` and is in same profile group as the given `user` and is the same package as the `service`

| Parameters ||
|---|---|
| `service` | [Intent](../android/content/Intent.md): Identifies the service to connect to. The Intent must specify an explicit component name. This value cannot be `null`. |
| `conn` | [ServiceConnection](../android/content/ServiceConnection.md): Receives information as the service is started and stopped. This must be a valid ServiceConnection object; it must not be null. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Operation options for the binding. May be 0, `https://developer.android.com/reference/kotlin/android/content/Context#BIND_AUTO_CREATE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/Context#BIND_DEBUG_UNBIND:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/Context#BIND_NOT_FOREGROUND:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/Context#BIND_ABOVE_CLIENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/Context#BIND_ALLOW_OOM_MANAGEMENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/Context#BIND_WAIVE_PRIORITY:kotlin.Int`. `https://developer.android.com/reference/kotlin/android/content/Context#BIND_IMPORTANT:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/content/Context#BIND_ADJUST_WITH_ACTIVITY:kotlin.Int`. |
| --- | --- |
| `user` | [UserHandle](../android/os/UserHandle.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the system is in the process of bringing up a service that your client has permission to bind to; `false` if the system couldn't find the service. You should call `https://developer.android.com/reference/kotlin/android/content/Context#unbindService(android.content.ServiceConnection)` to release the connection even if this method returned `false`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the client does not have the required permission to bind. |

### checkCallingOrSelfPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkCallingOrSelfPermission(permission: String): Int
```

Determine whether the calling process of an IPC *or you* have been granted a particular permission. This is the same as `https://developer.android.com/reference/kotlin/android/content/Context#checkCallingPermission(kotlin.String)`, except it grants your own permissions if you are not currently processing an IPC. Use with care!

| Parameters ||
|---|---|
| `permission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the permission being checked. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_GRANTED:kotlin.Int` if the calling pid/uid is allowed that permission, or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_DENIED:kotlin.Int` if it is not. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_GRANTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_DENIED:kotlin.Int` |

### checkCallingOrSelfUriPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkCallingOrSelfUriPermission(
    uri: Uri!, 
    modeFlags: Int
): Int
```

Determine whether the calling process of an IPC *or you* has been granted permission to access a specific URI. This is the same as `https://developer.android.com/reference/kotlin/android/content/Context#checkCallingUriPermission(android.net.Uri,%20kotlin.Int)`, except it grants your own permissions if you are not currently processing an IPC. Use with care!

| Parameters ||
|---|---|
| `uri` | [Uri](../android/net/Uri.md)!: The uri that is being checked. |
| `modeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The access modes to check. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_GRANTED:kotlin.Int` if the caller is allowed to access that uri, or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_DENIED:kotlin.Int` if it is not. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_GRANTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_DENIED:kotlin.Int` |

### checkCallingOrSelfUriPermissions

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkCallingOrSelfUriPermissions(
    uris: MutableList<Uri!>, 
    modeFlags: Int
): IntArray
```

Determine whether the calling process of an IPC *or you* has been granted permission to access a list of URIs. This is the same as `https://developer.android.com/reference/kotlin/android/content/Context#checkCallingUriPermission(android.net.Uri,%20kotlin.Int)`, except it grants your own permissions if you are not currently processing an IPC. Use with care!

| Parameters ||
|---|---|
| `uris` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](../android/net/Uri.md)!\>: This value cannot be `null`. |
| `modeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The access modes to check. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | This value cannot be `null`. |

### checkCallingPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkCallingPermission(permission: String): Int
```

Determine whether the calling process of an IPC you are handling has been granted a particular permission. This is basically the same as calling `https://developer.android.com/reference/kotlin/android/content/Context#checkPermission(kotlin.String,%20kotlin.Int,%20kotlin.Int)` with the pid and uid returned by `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingPid()` and `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingUid()`. One important difference is that if you are not currently processing an IPC, this function will always fail. This is done to protect against accidentally leaking permissions; you can use `https://developer.android.com/reference/kotlin/android/content/Context#checkCallingOrSelfPermission(kotlin.String)` to avoid this protection.

| Parameters ||
|---|---|
| `permission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the permission being checked. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_GRANTED:kotlin.Int` if the calling pid/uid is allowed that permission, or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_DENIED:kotlin.Int` if it is not. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_GRANTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_DENIED:kotlin.Int` |

### checkCallingUriPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkCallingUriPermission(
    uri: Uri!, 
    modeFlags: Int
): Int
```

Determine whether the calling process and uid has been granted permission to access a specific URI. This is basically the same as calling `https://developer.android.com/reference/kotlin/android/content/Context#checkUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` with the pid and uid returned by `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingPid()` and `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingUid()`. One important difference is that if you are not currently processing an IPC, this function will always fail.

| Parameters ||
|---|---|
| `uri` | [Uri](../android/net/Uri.md)!: The uri that is being checked. |
| `modeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The access modes to check. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_GRANTED:kotlin.Int` if the caller is allowed to access that uri, or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_DENIED:kotlin.Int` if it is not. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_GRANTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_DENIED:kotlin.Int` |

### checkCallingUriPermissions

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkCallingUriPermissions(
    uris: MutableList<Uri!>, 
    modeFlags: Int
): IntArray
```

Determine whether the calling process and uid has been granted permission to access a list of URIs. This is basically the same as calling `https://developer.android.com/reference/kotlin/android/content/Context#checkUriPermissions(kotlin.collections.MutableList,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` with the pid and uid returned by `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingPid()` and `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingUid()`. One important difference is that if you are not currently processing an IPC, this function will always fail.

| Parameters ||
|---|---|
| `uris` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](../android/net/Uri.md)!\>: This value cannot be `null`. |
| `modeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The access modes to check. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | This value cannot be `null`. |

### checkContentUriPermissionFull

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkContentUriPermissionFull(
    uri: Uri, 
    pid: Int, 
    uid: Int, 
    modeFlags: Int
): Int
```

Determine whether a particular process and uid has been granted permission to access a specific content URI.

Unlike `https://developer.android.com/reference/kotlin/android/content/Context#checkUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`, this method checks for general access to the URI's content provider, as well as explicitly granted permissions.

Note, this check will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` for non-content URIs.

| Parameters ||
|---|---|
| `uri` | [Uri](../android/net/Uri.md): This value cannot be `null`. |
| `pid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): (Optional) The process ID being checked against. If the pid is unknown, pass -1. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The UID being checked against. A uid of 0 is the root user, which will pass every permission check. |
| --- | --- |
| `modeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The access modes to check. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_GRANTED:kotlin.Int` if the given pid/uid is allowed to access that uri, or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_DENIED:kotlin.Int` if it is not. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_GRANTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_DENIED:kotlin.Int` |

### checkPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkPermission(
    permission: String, 
    pid: Int, 
    uid: Int
): Int
```

Determine whether the given permission is allowed for a particular process and user ID running in the system.

| Parameters ||
|---|---|
| `permission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the permission being checked. This value cannot be `null`. |
| `pid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The process ID being checked against. Must be \> 0. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The UID being checked against. A uid of 0 is the root user, which will pass every permission check. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_GRANTED:kotlin.Int` if the given pid/uid is allowed that permission, or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_DENIED:kotlin.Int` if it is not. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_GRANTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_DENIED:kotlin.Int` |

### checkSelfPermission

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkSelfPermission(permission: String): Int
```

Determine whether *you* have been granted a particular permission.

| Parameters ||
|---|---|
| `permission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the permission being checked. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_GRANTED:kotlin.Int` if you have the permission, or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_DENIED:kotlin.Int` if not. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_GRANTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_DENIED:kotlin.Int` |

### checkUriPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkUriPermission(
    uri: Uri!, 
    pid: Int, 
    uid: Int, 
    modeFlags: Int
): Int
```

Determine whether a particular process and uid has been granted permission to access a specific URI. This only checks for permissions that have been explicitly granted -- if the given process/uid has more general access to the URI's content provider then this check will always fail.

| Parameters ||
|---|---|
| `uri` | [Uri](../android/net/Uri.md)!: The uri that is being checked. |
| `pid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The process ID being checked against. Must be \> 0. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The UID being checked against. A uid of 0 is the root user, which will pass every permission check. |
| --- | --- |
| `modeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The access modes to check. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_GRANTED:kotlin.Int` if the given pid/uid is allowed to access that uri, or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_DENIED:kotlin.Int` if it is not. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_GRANTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_DENIED:kotlin.Int` |

### checkUriPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkUriPermission(
    uri: Uri?, 
    readPermission: String?, 
    writePermission: String?, 
    pid: Int, 
    uid: Int, 
    modeFlags: Int
): Int
```

Check both a Uri and normal permission. This allows you to perform both `https://developer.android.com/reference/kotlin/android/content/Context#checkPermission(kotlin.String,%20kotlin.Int,%20kotlin.Int)` and #checkUriPermission in one call.

| Parameters ||
|---|---|
| `uri` | [Uri](../android/net/Uri.md)?: This value may be `null`. |
| `readPermission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `writePermission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| --- | --- |
| `pid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The process ID being checked against. Must be \> 0. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The UID being checked against. A uid of 0 is the root user, which will pass every permission check. |
| `modeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The access modes to check. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_GRANTED:kotlin.Int` if the caller is allowed to access that uri or holds one of the given permissions, or `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_DENIED:kotlin.Int` if it is not. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_GRANTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_DENIED:kotlin.Int` |

### checkUriPermissions

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkUriPermissions(
    uris: MutableList<Uri!>, 
    pid: Int, 
    uid: Int, 
    modeFlags: Int
): IntArray
```

Determine whether a particular process and uid has been granted permission to access a list of URIs. This only checks for permissions that have been explicitly granted -- if the given process/uid has more general access to the URI's content provider then this check will always fail. **Note:** On SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, calling this method from a secondary-user's context will incorrectly return `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#PERMISSION_DENIED:kotlin.Int` for all {code uris}.

| Parameters ||
|---|---|
| `uris` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](../android/net/Uri.md)!\>: This value cannot be `null`. |
| `pid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The process ID being checked against. Must be \> 0. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The UID being checked against. A uid of 0 is the root user, which will pass every permission check. |
| --- | --- |
| `modeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The access modes to check for the list of uris. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | This value cannot be `null`. |

### clearWallpaper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearWallpaper(): Unit
```

**Deprecated:** *Deprecated in Java.*

### createAttributionContext

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createAttributionContext(attributionTag: String?): Context
```

Return a new Context object for the current Context but attribute to a different tag. In complex apps attribution tagging can be used to distinguish between separate logical parts.

| Parameters ||
|---|---|
| `attributionTag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Context` | This value cannot be `null`. |

### createConfigurationContext

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createConfigurationContext(overrideConfiguration: Configuration): Context!
```

Return a new Context object for the current Context but whose resources are adjusted to match the given Configuration. Each call to this method returns a new instance of a Context object; Context objects are not shared, however common state (ClassLoader, other Resources for the same configuration) may be so the Context itself can be fairly lightweight.

| Parameters ||
|---|---|
| `overrideConfiguration` | [Configuration](../android/content/res/Configuration.md): A `https://developer.android.com/reference/kotlin/android/content/res/Configuration` specifying what values to modify in the base Configuration of the original Context's resources. If the base configuration changes (such as due to an orientation change), the resources of this context will also change except for those that have been explicitly overridden with a value here. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Context!` | A `https://developer.android.com/reference/kotlin/android/content/Context` with the given configuration override. |

### createContext

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createContext(contextParams: ContextParams): Context
```

Creates a context with specific properties and behaviors.

| Parameters ||
|---|---|
| `contextParams` | [ContextParams](../android/content/ContextParams.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Context` | This value cannot be `null`. |

### createContextForSplit

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createContextForSplit(splitName: String!): Context!
```

Return a new Context object for the given split name. The new Context has a ClassLoader and Resources object that can access the split's and all of its dependencies' code/resources. Each call to this method returns a new instance of a Context object; Context objects are not shared, however common state (ClassLoader, other Resources for the same split) may be so the Context itself can be fairly lightweight.

| Parameters ||
|---|---|
| `splitName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the split to include, as declared in the split's `AndroidManifest.xml`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Context!` | A `https://developer.android.com/reference/kotlin/android/content/Context` with the given split's code and/or resources loaded. |

### createDeviceContext

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createDeviceContext(deviceId: Int): Context
```

Returns a new `Context` object from the current context but with device association given by the `deviceId`. Each call to this method returns a new instance of a context object. Context objects are not shared; however, common state (such as the `https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#` and other resources for the same configuration) can be shared, so the `Context` itself is lightweight.

Applications that run on virtual devices may use this method to access the default device capabilities and functionality (by passing `https://developer.android.com/reference/kotlin/android/content/Context#DEVICE_ID_DEFAULT:kotlin.Int`. Similarly, applications running on the default device may access the functionality of virtual devices.

Note that the newly created instance will be associated with the same display as the parent Context, regardless of the device ID passed here.

| Parameters ||
|---|---|
| `deviceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The ID of the device to associate with this context. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Context` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the given device ID is not a valid ID of the default device or a virtual device. |

### createDeviceProtectedStorageContext

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createDeviceProtectedStorageContext(): Context!
```

Return a new Context object for the current Context but whose storage APIs are backed by device-protected storage.

On devices with direct boot, data stored in this location is encrypted with a key tied to the physical device, and it can be accessed immediately after the device has booted successfully, both *before and after* the user has authenticated with their credentials (such as a lock pattern or PIN).

Because device-protected data is available without user authentication, you should carefully limit the data you store using this Context. For example, storing sensitive authentication tokens or passwords in the device-protected area is strongly discouraged.

If the underlying device does not have the ability to store device-protected and credential-protected data using different keys, then both storage areas will become available at the same time. They remain as two distinct storage locations on disk, and only the window of availability changes.

Each call to this method returns a new instance of a Context object; Context objects are not shared, however common state (ClassLoader, other Resources for the same configuration) may be so the Context itself can be fairly lightweight.

### createDisplayContext

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createDisplayContext(display: Display): Context!
```

Returns a new `Context` object from the current context but with resources adjusted to match the metrics of `display`. Each call to this method returns a new instance of a context object. Context objects are not shared; however, common state (such as the `https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#` and other resources for the same configuration) can be shared, so the `Context` itself is lightweight.

**Note:** This `Context` is **not** expected to be updated with new configuration if the underlying display configuration changes and the cached `Resources` it returns could be stale. It is suggested to use `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.DisplayListener.html#` to listen for changes and re-create an instance if necessary.

This `Context` is **not** a UI context, do not use it to access UI components or obtain a `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#` instance.

To obtain an instance of `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#` configured to show windows on the given display, call `https://developer.android.com/reference/kotlin/android/content/Context#createWindowContext(kotlin.Int,%20android.os.Bundle)` on the returned display context, then call `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(kotlin.String)` or `https://developer.android.com/reference/kotlin/android/content/Context#getSystemService(java.lang.Class)` on the returned window context.

| Parameters ||
|---|---|
| `display` | [Display](../android/view/Display.md): The display to which the current context's resources are adjusted. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Context!` | A context for the display. |

### createPackageContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createPackageContext(
    packageName: String!, 
    flags: Int
): Context!
```

Return a new Context object for the given application name. This Context is the same as what the named application gets when it is launched, containing the same resources and class loader. Each call to this method returns a new instance of a Context object; Context objects are not shared, however they share common state (Resources, ClassLoader, etc) so the Context instance itself is fairly lightweight.

Throws `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.NameNotFoundException` if there is no application with the given package name.

Throws `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` if the Context requested can not be loaded into the caller's process for security reasons (see `https://developer.android.com/reference/kotlin/android/content/Context#CONTEXT_INCLUDE_CODE:kotlin.Int` for more information}.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Name of the application's package. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Option flags. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Context#CONTEXT_INCLUDE_CODE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#CONTEXT_IGNORE_SECURITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#CONTEXT_RESTRICTED:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Context!` | A `https://developer.android.com/reference/kotlin/android/content/Context` for the application. |

| Exceptions ||
|---|---|
| `android.content.pm.PackageManager.NameNotFoundException` | if there is no application with the given package name. |
| `java.lang.SecurityException` | |

### createWindowContext

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createWindowContext(
    display: Display, 
    type: Int, 
    options: Bundle?
): Context
```

Creates a `Context` for a non-`https://developer.android.com/reference/kotlin/android/app/Activity.html#` window on the given `https://developer.android.com/reference/kotlin/android/view/Display.html#`.

Similar to `https://developer.android.com/reference/kotlin/android/content/Context#createWindowContext(kotlin.Int,%20android.os.Bundle)`, but the `display` is passed in, instead of implicitly using the `https://developer.android.com/reference/kotlin/android/content/Context#getDisplay()`.

| Parameters ||
|---|---|
| `display` | [Display](../android/view/Display.md): This value cannot be `null`. |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_BASE_APPLICATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_APPLICATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_APPLICATION_STARTING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_DRAWN_APPLICATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_APPLICATION_PANEL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_APPLICATION_MEDIA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_APPLICATION_SUB_PANEL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_APPLICATION_ATTACHED_DIALOG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_STATUS_BAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_SEARCH_BAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_PHONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_SYSTEM_ALERT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_TOAST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_SYSTEM_OVERLAY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_PRIORITY_PHONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_SYSTEM_DIALOG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_KEYGUARD_DIALOG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_SYSTEM_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_INPUT_METHOD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_INPUT_METHOD_DIALOG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_WALLPAPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_PRIVATE_PRESENTATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_ACCESSIBILITY_OVERLAY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_APPLICATION_OVERLAY:kotlin.Int` |
| `options` | [Bundle](../android/os/Bundle.md)?: This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Context` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the `https://developer.android.com/reference/kotlin/android/view/Display.html#` is `null`. |

### createWindowContext

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createWindowContext(
    type: Int, 
    options: Bundle?
): Context
```

Creates a Context for a non-activity window.

A window context is a context that can be used to add non-activity windows, such as `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_APPLICATION_OVERLAY:kotlin.Int`. A window context must be created from a context that has an associated `https://developer.android.com/reference/kotlin/android/view/Display.html#`, such as `https://developer.android.com/reference/kotlin/android/app/Activity.html#` or a context created with `https://developer.android.com/reference/kotlin/android/content/Context#createDisplayContext(android.view.Display)`.

The window context is created with the appropriate `https://developer.android.com/reference/kotlin/android/content/res/Configuration` for the area of the display that the windows created with it can occupy; it must be used when `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` views, such that they can be inflated with proper `https://developer.android.com/reference/kotlin/android/content/res/Resources`. Below is a sample code to **add an application overlay window on the primary display:**

```kotlin
...
  final DisplayManager dm = anyContext.getSystemService(DisplayManager.class);
  final Display primaryDisplay = dm.getDisplay(DEFAULT_DISPLAY);
  final Context windowContext = anyContext.createDisplayContext(primaryDisplay)
          .createWindowContext(TYPE_APPLICATION_OVERLAY, null);
  final View overlayView = Inflater.from(windowContext).inflate(someLayoutXml, null);
 
  // WindowManager.LayoutParams initialization
  ...
  // The types used in addView and createWindowContext must match.
  mParams.type = TYPE_APPLICATION_OVERLAY;
  ...
 
  windowContext.getSystemService(WindowManager.class).addView(overlayView, mParams);
  
```

This context's configuration and resources are adjusted to an area of the display where the windows with provided type will be added. **Note that all windows associated with the same context will have an affinity and can only be moved together between different displays or areas on a display.** If there is a need to add different window types, or non-associated windows, separate Contexts should be used.

Creating a window context is an expensive operation. Misuse of this API may lead to a huge performance drop. The best practice is to use the same window context when possible. An approach is to create one window context with specific window type and display and use it everywhere it's needed.

After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, window context provides the capability to receive configuration changes for existing token by overriding the `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#token:android.os.IBinder` of the `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#` passed in `https://developer.android.com/reference/kotlin/android/view/ViewManager.html#addView(android.view.View,%20android.view.ViewGroup.LayoutParams)`. This is useful when an application needs to attach its window to an existing activity for window token sharing use-case.

Note that the window context in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` didn't have this capability. This is a no-op for the window context in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`.
Below is sample code to **attach an existing token to a window context:**

```kotlin
final DisplayManager dm = anyContext.getSystemService(DisplayManager.class);
  final Display primaryDisplay = dm.getDisplay(DEFAULT_DISPLAY);
  final Context windowContext = anyContext.createWindowContext(primaryDisplay,
          TYPE_APPLICATION, null);
 
  // Get an existing token.
  final IBinder existingToken = activity.getWindow().getAttributes().token;
 
  // The types used in addView() and createWindowContext() must match.
  final WindowManager.LayoutParams params = new WindowManager.LayoutParams(TYPE_APPLICATION);
  params.token = existingToken;
 
  // After WindowManager#addView(), the server side will extract the provided token from
  // LayoutParams#token (existingToken in the sample code), and switch to propagate
  // configuration changes from the node associated with the provided token.
  windowContext.getSystemService(WindowManager.class).addView(overlayView, mParams);
  
```

After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, window context provides the capability to listen to its `https://developer.android.com/reference/kotlin/android/content/res/Configuration` changes by calling `https://developer.android.com/reference/kotlin/android/content/Context#registerComponentCallbacks(android.content.ComponentCallbacks)`, while other kinds of `https://developer.android.com/reference/kotlin/android/content/Context` will register the `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks` to `https://developer.android.com/reference/kotlin/android/content/Context#getApplicationContext()`. Note that window context only propagate `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks#onConfigurationChanged(android.content.res.Configuration)` callback. `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks#onLowMemory()` or other callbacks in `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2` won't be invoked.

Note that using `https://developer.android.com/reference/kotlin/android/app/Application.html#` or `https://developer.android.com/reference/kotlin/android/app/Service.html#` context for UI-related queries may result in layout or continuity issues on devices with variable screen sizes (e.g. foldables) or in multi-window modes, since these non-UI contexts may not reflect the `https://developer.android.com/reference/kotlin/android/content/res/Configuration` changes for the visual container.

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_BASE_APPLICATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_APPLICATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_APPLICATION_STARTING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_DRAWN_APPLICATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_APPLICATION_PANEL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_APPLICATION_MEDIA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_APPLICATION_SUB_PANEL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_APPLICATION_ATTACHED_DIALOG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_STATUS_BAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_SEARCH_BAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_PHONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_SYSTEM_ALERT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_TOAST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_SYSTEM_OVERLAY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_PRIORITY_PHONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_SYSTEM_DIALOG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_KEYGUARD_DIALOG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_SYSTEM_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_INPUT_METHOD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_INPUT_METHOD_DIALOG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_WALLPAPER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_PRIVATE_PRESENTATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_ACCESSIBILITY_OVERLAY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#TYPE_APPLICATION_OVERLAY:kotlin.Int` |
| `options` | [Bundle](../android/os/Bundle.md)?: This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Context` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if this `https://developer.android.com/reference/kotlin/android/content/Context` does not attach to a display, such as `https://developer.android.com/reference/kotlin/android/app/Application.html#` or `https://developer.android.com/reference/kotlin/android/app/Service.html#`. |

### databaseList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun databaseList(): Array<String!>!
```

Returns an array of strings naming the private databases associated with this Context's application package.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | Array of strings naming the private databases. |

### deleteDatabase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun deleteDatabase(name: String!): Boolean
```

Delete an existing private SQLiteDatabase associated with this Context's application package.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name (unique in the application package) of the database. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the database was successfully deleted; else `false`. |

### deleteFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun deleteFile(name: String!): Boolean
```

Delete the given private file associated with this Context's application package.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the file to delete; can not contain path separators. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the file was successfully deleted; else `false`. |

### deleteSharedPreferences

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun deleteSharedPreferences(name: String!): Boolean
```

Delete an existing shared preferences file.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name (unique in the application package) of the shared preferences file. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the shared preferences file was successfully deleted; else `false`. |

### enforceCallingOrSelfPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun enforceCallingOrSelfPermission(
    permission: String, 
    message: String?
): Unit
```

If neither you nor the calling process of an IPC you are handling has been granted a particular permission, throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This is the same as `https://developer.android.com/reference/kotlin/android/content/Context#enforceCallingPermission(kotlin.String,%20kotlin.String)`, except it grants your own permissions if you are not currently processing an IPC. Use with care!

| Parameters ||
|---|---|
| `permission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the permission being checked. This value cannot be `null`. |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

### enforceCallingOrSelfUriPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun enforceCallingOrSelfUriPermission(
    uri: Uri!, 
    modeFlags: Int, 
    message: String!
): Unit
```

If the calling process of an IPC *or you* has not been granted permission to access a specific URI, throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This is the same as `https://developer.android.com/reference/kotlin/android/content/Context#enforceCallingUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.String)`, except it grants your own permissions if you are not currently processing an IPC. Use with care!

| Parameters ||
|---|---|
| `uri` | [Uri](../android/net/Uri.md)!: The uri that is being checked. |
| `modeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The access modes to enforce. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A message to include in the exception if it is thrown. |
| --- | --- |

### enforceCallingPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun enforceCallingPermission(
    permission: String, 
    message: String?
): Unit
```

If the calling process of an IPC you are handling has not been granted a particular permission, throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This is basically the same as calling `https://developer.android.com/reference/kotlin/android/content/Context#enforcePermission(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)` with the pid and uid returned by `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingPid()` and `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingUid()`. One important difference is that if you are not currently processing an IPC, this function will always throw the SecurityException. This is done to protect against accidentally leaking permissions; you can use `https://developer.android.com/reference/kotlin/android/content/Context#enforceCallingOrSelfPermission(kotlin.String,%20kotlin.String)` to avoid this protection.

| Parameters ||
|---|---|
| `permission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the permission being checked. This value cannot be `null`. |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

### enforceCallingUriPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun enforceCallingUriPermission(
    uri: Uri!, 
    modeFlags: Int, 
    message: String!
): Unit
```

If the calling process and uid has not been granted permission to access a specific URI, throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This is basically the same as calling `https://developer.android.com/reference/kotlin/android/content/Context#enforceUriPermission(android.net.Uri,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)` with the pid and uid returned by `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingPid()` and `https://developer.android.com/reference/kotlin/android/os/Binder.html#getCallingUid()`. One important difference is that if you are not currently processing an IPC, this function will always throw a SecurityException.

| Parameters ||
|---|---|
| `uri` | [Uri](../android/net/Uri.md)!: The uri that is being checked. |
| `modeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The access modes to enforce. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A message to include in the exception if it is thrown. |
| --- | --- |

### enforcePermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun enforcePermission(
    permission: String, 
    pid: Int, 
    uid: Int, 
    message: String?
): Unit
```

If the given permission is not allowed for a particular process and user ID running in the system, throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

| Parameters ||
|---|---|
| `permission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the permission being checked. This value cannot be `null`. |
| `pid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The process ID being checked against. Must be \> 0. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The UID being checked against. A uid of 0 is the root user, which will pass every permission check. |
| --- | --- |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

### enforceUriPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun enforceUriPermission(
    uri: Uri!, 
    pid: Int, 
    uid: Int, 
    modeFlags: Int, 
    message: String!
): Unit
```

If a particular process and uid has not been granted permission to access a specific URI, throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`. This only checks for permissions that have been explicitly granted -- if the given process/uid has more general access to the URI's content provider then this check will always fail.

| Parameters ||
|---|---|
| `uri` | [Uri](../android/net/Uri.md)!: The uri that is being checked. |
| `pid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The process ID being checked against. Must be \> 0. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The UID being checked against. A uid of 0 is the root user, which will pass every permission check. |
| --- | --- |
| `modeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The access modes to enforce. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A message to include in the exception if it is thrown. |

### enforceUriPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun enforceUriPermission(
    uri: Uri?, 
    readPermission: String?, 
    writePermission: String?, 
    pid: Int, 
    uid: Int, 
    modeFlags: Int, 
    message: String?
): Unit
```

Enforce both a Uri and normal permission. This allows you to perform both `https://developer.android.com/reference/kotlin/android/content/Context#enforcePermission(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)` and #enforceUriPermission in one call.

| Parameters ||
|---|---|
| `uri` | [Uri](../android/net/Uri.md)?: This value may be `null`. |
| `readPermission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `writePermission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| --- | --- |
| `pid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The process ID being checked against. Must be \> 0. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The UID being checked against. A uid of 0 is the root user, which will pass every permission check. |
| `modeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The access modes to enforce. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` |
| --- | --- |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

### fileList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun fileList(): Array<String!>!
```

Returns an array of strings naming the private files associated with this Context's application package.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | Array of strings naming the private files. |

### getApplicationContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getApplicationContext(): Context!
```

Return the context of the single, global Application object of the current process. This generally should only be used if you need a Context whose lifecycle is separate from the current context, that is tied to the lifetime of the process rather than the current component.

Consider for example how this interacts with `https://developer.android.com/reference/kotlin/android/content/Context#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)`:

- If used from an Activity context, the receiver is being registered within that activity. This means that you are expected to unregister before the activity is done being destroyed; in fact if you do not do so, the framework will clean up your leaked registration as it removes the activity and log an error. Thus, if you use the Activity context to register a receiver that is static (global to the process, not associated with an Activity instance) then that registration will be removed on you at whatever point the activity you used is destroyed.

- If used from the Context returned here, the receiver is being registered with the global state associated with your application. Thus it will never be unregistered for you. This is necessary if the receiver is associated with static data, not a particular component. However using the ApplicationContext elsewhere can easily lead to serious leaks if you forget to unregister, unbind, etc.

### getApplicationInfo

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getApplicationInfo(): ApplicationInfo!
```

Return the full application info for this context's package.

### getAssets

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAssets(): AssetManager!
```

Returns an AssetManager instance for the application's package.

**Note:** Implementations of this method should return an AssetManager instance that is consistent with the Resources instance returned by `https://developer.android.com/reference/kotlin/android/content/Context#getResources()`. For example, they should share the same `https://developer.android.com/reference/kotlin/android/content/res/Configuration` object.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/AssetManager!` | an AssetManager instance for the application's package |

### getAttributionSource

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAttributionSource(): AttributionSource
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/AttributionSource` | This value cannot be `null`. |

### getAttributionTag

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAttributionTag(): String?
```

Attribution can be used in complex apps to logically separate parts of the app. E.g. a blogging app might also have a instant messaging app built in. In this case two separate tags can for used each sub-feature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

### getBaseContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBaseContext(): Context!
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Context!` | the base context as set by the constructor or setBaseContext |

### getCacheDir

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCacheDir(): File!
```

Returns the absolute path to the application specific cache directory on the filesystem.

The system will automatically delete files in this directory as disk space is needed elsewhere on the device. The system will always delete older files first, as reported by `https://developer.android.com/reference/kotlin/java/io/File.html#lastModified()`. If desired, you can exert more control over how files are deleted using `https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.html#setCacheBehaviorGroup(java.io.File,%20kotlin.Boolean)` and `https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.html#setCacheBehaviorTombstone(java.io.File,%20kotlin.Boolean)`.

Apps are strongly encouraged to keep their usage of cache space below the quota returned by `https://developer.android.com/reference/kotlin/android/os/storage/StorageManager.html#getCacheQuotaBytes(java.util.UUID)`. If your app goes above this quota, your cached files will be some of the first to be deleted when additional disk space is needed. Conversely, if your app stays under this quota, your cached files will be some of the last to be deleted when additional disk space is needed.

Note that your cache quota will change over time depending on how frequently the user interacts with your app, and depending on how much system-wide disk space is used.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

Apps require no extra permissions to read or write to the returned path, since this path lives in their private storage.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/File.html#!` | The path of the directory holding application cache files. |

### getClassLoader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getClassLoader(): ClassLoader!
```

Return a class loader you can use to retrieve classes in this package.

### getCodeCacheDir

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCodeCacheDir(): File!
```

Returns the absolute path to the application specific cache directory on the filesystem designed for storing cached code.

The system will delete any files stored in this location both when your specific application is upgraded, and when the entire platform is upgraded.

This location is optimal for storing compiled or optimized code generated by your application at runtime.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

Apps require no extra permissions to read or write to the returned path, since this path lives in their private storage.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/File.html#!` | The path of the directory holding application code cache files. |

### getContentResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getContentResolver(): ContentResolver!
```

Return a ContentResolver instance for your application's package.

### getDataDir

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDataDir(): File!
```

Returns the absolute path to the directory on the filesystem where all private files belonging to this app are stored. Apps should not use this path directly; they should instead use `https://developer.android.com/reference/kotlin/android/content/Context#getFilesDir()`, `https://developer.android.com/reference/kotlin/android/content/Context#getCacheDir()`, `https://developer.android.com/reference/kotlin/android/content/Context#getDir(kotlin.String,%20kotlin.Int)`, or other storage APIs on this class.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

No additional permissions are required for the calling app to read or write files under the returned path.

### getDatabasePath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDatabasePath(name: String!): File!
```

Returns the absolute path on the filesystem where a database created with #openOrCreateDatabase is stored.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the database for which you would like to get its path. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/File.html#!` | An absolute path to the given database. |

### getDeviceId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDeviceId(): Int
```

Gets the device ID this context is associated with. Applications can use this method to determine whether they are running on a virtual device and identify that device. The device ID of the host device is `https://developer.android.com/reference/kotlin/android/content/Context#DEVICE_ID_DEFAULT:kotlin.Int`

If the underlying device ID is changed by the system, for example, when an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` is moved to a different virtual device, applications can register to listen to changes by calling `https://developer.android.com/reference/kotlin/android/content/Context#registerDeviceIdChangeListener(java.util.concurrent.Executor,%20java.util.function.IntConsumer)`.

This method will only return a reliable value for this instance if it was created with `https://developer.android.com/reference/kotlin/android/content/Context#createDeviceContext(kotlin.Int)`, or if this instance is a UI or Display Context. Contexts created with `https://developer.android.com/reference/kotlin/android/content/Context#createDeviceContext(kotlin.Int)` will have an explicit device association, which will never change, even if the underlying device is closed or is removed. UI Contexts and Display Contexts are already associated with a display, so if the device association is not explicitly given, `https://developer.android.com/reference/kotlin/android/content/Context#getDeviceId()` will return the ID of the device associated with the associated display. The system can assign an arbitrary device id value for Contexts not logically associated with a device.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the ID of the device this context is associated with. |

### getDir

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDir(
    name: String!, 
    mode: Int
): File!
```

Retrieve, creating if needed, a new directory in which the application can place its own custom data files. You can use the returned File object to create and access files in this directory. Note that files created through a File object will only be accessible by your own application; you can only set the mode of the entire directory, not of individual files.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

Apps require no extra permissions to read or write to the returned path, since this path lives in their private storage.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Name of the directory to retrieve. This is a directory that is created as part of your application data. |
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Operating mode. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Context#MODE_PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#MODE_WORLD_READABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#MODE_WORLD_WRITEABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#MODE_APPEND:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/File.html#!` | A `https://developer.android.com/reference/kotlin/java/io/File.html#` object for the requested directory. The directory will have been created if it does not already exist. |

### getDisplay

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDisplay(): Display!
```

Get the display this context is associated with. Applications should use this method with `https://developer.android.com/reference/kotlin/android/app/Activity.html#` or a context associated with a `https://developer.android.com/reference/kotlin/android/view/Display.html#` via `https://developer.android.com/reference/kotlin/android/content/Context#createDisplayContext(android.view.Display)` to get a display object associated with a Context, or `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#getDisplay(kotlin.Int)` to get a display object by id.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/Display.html#!` | This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the method is called on an instance that is not associated with any display. |

### getExternalCacheDir

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getExternalCacheDir(): File?
```

Returns absolute path to application-specific directory on the primary shared/external storage device where the application can place cache files it owns. These files are internal to the application, and not typically visible to the user as media.

This is like `https://developer.android.com/reference/kotlin/android/content/Context#getCacheDir()` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- The platform does not always monitor the space available in shared storage, and thus may not automatically delete these files. Apps should always manage the maximum space used in this location. Currently the only time files here will be deleted by the platform is when running on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR1:kotlin.Int` or later and `https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)` returns true.
- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

If a shared storage device is emulated (as determined by `https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)`), its contents are backed by a private user data partition, which means there is little benefit to storing data here instead of the private directory returned by `https://developer.android.com/reference/kotlin/android/content/Context#getCacheDir()`.

Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int`, no permissions are required to read or write to the returned path; it's always accessible to the calling app. This only applies to paths generated for package name of the calling application. To access paths belonging to other packages, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` and/or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` are required.

On devices with multiple users (as described by `https://developer.android.com/reference/kotlin/android/os/UserManager.html#`), each user has their own isolated shared storage. Applications only have access to the shared storage for the user they're running as.

The returned path may change over time if different shared storage media is inserted, so only relative paths should be persisted.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/File.html#?` | This value may be `null`. |

### getExternalCacheDirs

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getExternalCacheDirs(): Array<File!>!
```

Returns absolute paths to application-specific directories on all shared/external storage devices where the application can place cache files it owns. These files are internal to the application, and not typically visible to the user as media.

This is like `https://developer.android.com/reference/kotlin/android/content/Context#getCacheDir()` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- The platform does not always monitor the space available in shared storage, and thus may not automatically delete these files. Apps should always manage the maximum space used in this location. Currently the only time files here will be deleted by the platform is when running on `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR1:kotlin.Int` or later and `https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)` returns true.
- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

If a shared storage device is emulated (as determined by `https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)`), its contents are backed by a private user data partition, which means there is little benefit to storing data here instead of the private directory returned by `https://developer.android.com/reference/kotlin/android/content/Context#getCacheDir()`.

Shared storage devices returned here are considered a stable part of the device, including physical media slots under a protective cover. The returned paths do not include transient devices, such as USB flash drives connected to handheld devices.

An application may store data on any or all of the returned devices. For example, an app may choose to store large files on the device with the most available space, as measured by `https://developer.android.com/reference/kotlin/android/os/StatFs.html#`.

No additional permissions are required for the calling app to read or write files under the returned path. Write access outside of these paths on secondary external storage devices is not available.

The returned paths may change over time if different shared storage media is inserted, so only relative paths should be persisted.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/io/File.html#!>!` | the absolute paths to application-specific directories. Some individual paths may be `null` if that shared storage is not currently available. The first path returned is the same as `https://developer.android.com/reference/kotlin/android/content/Context#getExternalCacheDir()`. |

### getExternalFilesDir

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getExternalFilesDir(type: String?): File?
```

Returns the absolute path to the directory on the primary shared/external storage device where the application can place persistent files it owns. These files are internal to the applications, and not typically visible to the user as media.

This is like `https://developer.android.com/reference/kotlin/android/content/Context#getFilesDir()` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

If a shared storage device is emulated (as determined by `https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)`), its contents are backed by a private user data partition, which means there is little benefit to storing data here instead of the private directories returned by `https://developer.android.com/reference/kotlin/android/content/Context#getFilesDir()`, etc.

Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int`, no permissions are required to read or write to the returned path; it's always accessible to the calling app. This only applies to paths generated for package name of the calling application. To access paths belonging to other packages, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` and/or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` are required.

On devices with multiple users (as described by `https://developer.android.com/reference/kotlin/android/os/UserManager.html#`), each user has their own isolated shared storage. Applications only have access to the shared storage for the user they're running as.

The returned path may change over time if different shared storage media is inserted, so only relative paths should be persisted.

Here is an example of typical code to manipulate a file in an application's shared storage:

If you supply a non-null type to this function, the returned file will be a path to a sub-directory of the given type. Though these files are not automatically scanned by the media scanner, you can explicitly add them to the media database with `https://developer.android.com/reference/kotlin/android/media/MediaScannerConnection.html#scanFile(android.content.Context,%20kotlin.Array,%20kotlin.Array,%20android.media.MediaScannerConnection.OnScanCompletedListener)`. Note that this is not the same as `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStoragePublicDirectory(kotlin.String)`, which provides directories of media shared by all applications. The directories returned here are owned by the application, and their contents will be removed when the application is uninstalled. Unlike `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStoragePublicDirectory(kotlin.String)`, the directory returned here will be automatically created for you.

Here is an example of typical code to manipulate a picture in an application's shared storage and add it to the media database:

| Parameters ||
|---|---|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/File.html#?` | This value may be `null`. |

### getExternalFilesDirs

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getExternalFilesDirs(type: String!): Array<File!>!
```

Returns absolute paths to application-specific directories on all shared/external storage devices where the application can place persistent files it owns. These files are internal to the application, and not typically visible to the user as media.

This is like `https://developer.android.com/reference/kotlin/android/content/Context#getFilesDir()` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

If a shared storage device is emulated (as determined by `https://developer.android.com/reference/kotlin/android/os/Environment.html#isExternalStorageEmulated(java.io.File)`), its contents are backed by a private user data partition, which means there is little benefit to storing data here instead of the private directories returned by `https://developer.android.com/reference/kotlin/android/content/Context#getFilesDir()`, etc.

Shared storage devices returned here are considered a stable part of the device, including physical media slots under a protective cover. The returned paths do not include transient devices, such as USB flash drives connected to handheld devices.

An application may store data on any or all of the returned devices. For example, an app may choose to store large files on the device with the most available space, as measured by `https://developer.android.com/reference/kotlin/android/os/StatFs.html#`.

No additional permissions are required for the calling app to read or write files under the returned path. Write access outside of these paths on secondary external storage devices is not available.

The returned path may change over time if different shared storage media is inserted, so only relative paths should be persisted.

| Parameters ||
|---|---|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The type of files directory to return. May be `null` for the root of the files directory or one of the following constants for a subdirectory: `https://developer.android.com/reference/kotlin/android/os/Environment.html#DIRECTORY_MUSIC:kotlin.String`, `https://developer.android.com/reference/kotlin/android/os/Environment.html#DIRECTORY_PODCASTS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/os/Environment.html#DIRECTORY_RINGTONES:kotlin.String`, `https://developer.android.com/reference/kotlin/android/os/Environment.html#DIRECTORY_ALARMS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/os/Environment.html#DIRECTORY_NOTIFICATIONS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/os/Environment.html#DIRECTORY_PICTURES:kotlin.String`, or `https://developer.android.com/reference/kotlin/android/os/Environment.html#DIRECTORY_MOVIES:kotlin.String`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/io/File.html#!>!` | the absolute paths to application-specific directories. Some individual paths may be `null` if that shared storage is not currently available. The first path returned is the same as `https://developer.android.com/reference/kotlin/android/content/Context#getExternalFilesDir(kotlin.String)`. |

### getExternalMediaDirs

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getExternalMediaDirs(): Array<File!>!
```

Returns absolute paths to application-specific directories on all shared/external storage devices where the application can place media files. These files are scanned and made available to other apps through `https://developer.android.com/reference/kotlin/android/provider/MediaStore.html#`.

This is like `https://developer.android.com/reference/kotlin/android/content/Context#getExternalFilesDirs(kotlin.String)` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

Shared storage devices returned here are considered a stable part of the device, including physical media slots under a protective cover. The returned paths do not include transient devices, such as USB flash drives connected to handheld devices.

An application may store data on any or all of the returned devices. For example, an app may choose to store large files on the device with the most available space, as measured by `https://developer.android.com/reference/kotlin/android/os/StatFs.html#`.

No additional permissions are required for the calling app to read or write files under the returned path. Write access outside of these paths on secondary external storage devices is not available.

The returned paths may change over time if different shared storage media is inserted, so only relative paths should be persisted.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/io/File.html#!>!` | the absolute paths to application-specific directories. Some individual paths may be `null` if that shared storage is not currently available. |

### getFileStreamPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFileStreamPath(name: String!): File!
```

Returns the absolute path on the filesystem where a file created with `https://developer.android.com/reference/kotlin/android/content/Context#openFileOutput(kotlin.String,%20kotlin.Int)` is stored.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the file for which you would like to get its path. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/File.html#!` | An absolute path to the given file. |

### getFilesDir

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFilesDir(): File!
```

Returns the absolute path to the directory on the filesystem where files created with `https://developer.android.com/reference/kotlin/android/content/Context#openFileOutput(kotlin.String,%20kotlin.Int)` are stored.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

No additional permissions are required for the calling app to read or write files under the returned path.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/File.html#!` | The path of the directory holding application files. |

### getMainExecutor

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMainExecutor(): Executor!
```

Return an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that will run enqueued tasks on the main thread associated with this context. This is the thread used to dispatch calls to application components (activities, services, etc).

### getMainLooper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMainLooper(): Looper!
```

Return the Looper for the main thread of the current process. This is the thread used to dispatch calls to application components (activities, services, etc).

By definition, this method returns the same result as would be obtained by calling `https://developer.android.com/reference/kotlin/android/os/Looper.html#getMainLooper()`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Looper.html#!` | The main looper. |

### getNoBackupFilesDir

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNoBackupFilesDir(): File!
```

Returns the absolute path to the directory on the filesystem similar to `https://developer.android.com/reference/kotlin/android/content/Context#getFilesDir()`. The difference is that files placed under this directory will be excluded from automatic backup to remote storage. See `https://developer.android.com/reference/kotlin/android/app/backup/BackupAgent.html#` for a full discussion of the automatic backup mechanism in Android.

The returned path may change over time if the calling app is moved to an adopted storage device, so only relative paths should be persisted.

No additional permissions are required for the calling app to read or write files under the returned path.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/File.html#!` | The path of the directory holding application files that will not be automatically backed up to remote storage. |

### getObbDir

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getObbDir(): File!
```

Return the primary shared/external storage directory where this application's OBB files (if there are any) can be found. Note if the application does not have any OBB files, this directory may not exist.

This is like `https://developer.android.com/reference/kotlin/android/content/Context#getFilesDir()` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

Starting in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int`, no permissions are required to read or write to the path that this method returns. However, starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, to read the OBB expansion files, you must declare the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` permission in the app manifest and ask for permission at runtime as follows:

`<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" android:maxSdkVersion="23" />`

Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` permission is not required, so don't ask for this permission at runtime. To handle both cases, your app must first try to read the OBB file, and if it fails, you must request `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` permission at runtime.

The following code snippet shows how to do this:

```kotlin
File obb = new File(obb_filename);
  boolean open_failed = false;
 
  try {
      BufferedReader br = new BufferedReader(new FileReader(obb));
      open_failed = false;
      ReadObbFile(br);
  } catch (IOException e) {
      open_failed = true;
  }
 
  if (open_failed) {
      // request READ_EXTERNAL_STORAGE permission before reading OBB file
      ReadObbFileWithPermission();
  }
  
```
On devices with multiple users (as described by `https://developer.android.com/reference/kotlin/android/os/UserManager.html#`), multiple users may share the same OBB storage location. Applications should ensure that multiple instances running under different users don't interfere with each other.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/File.html#!` | the absolute path to application-specific directory. May return `null` if shared storage is not currently available. |

### getObbDirs

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getObbDirs(): Array<File!>!
```

Returns absolute paths to application-specific directories on all shared/external storage devices where the application's OBB files (if there are any) can be found. Note if the application does not have any OBB files, these directories may not exist.

This is like `https://developer.android.com/reference/kotlin/android/content/Context#getFilesDir()` in that these files will be deleted when the application is uninstalled, however there are some important differences:

- Shared storage may not always be available, since removable media can be ejected by the user. Media state can be checked using `https://developer.android.com/reference/kotlin/android/os/Environment.html#getExternalStorageState(java.io.File)`.
- There is no security enforced with these files. For example, any application holding `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#WRITE_EXTERNAL_STORAGE:kotlin.String` can write to these files.

Shared storage devices returned here are considered a stable part of the device, including physical media slots under a protective cover. The returned paths do not include transient devices, such as USB flash drives connected to handheld devices.

An application may store data on any or all of the returned devices. For example, an app may choose to store large files on the device with the most available space, as measured by `https://developer.android.com/reference/kotlin/android/os/StatFs.html#`.

No additional permissions are required for the calling app to read or write files under the returned path. Write access outside of these paths on secondary external storage devices is not available.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/io/File.html#!>!` | the absolute paths to application-specific directories. Some individual paths may be `null` if that shared storage is not currently available. The first path returned is the same as `https://developer.android.com/reference/kotlin/android/content/Context#getObbDir()` |

### getOpPackageName

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOpPackageName(): String
```

Return the package name that should be used for `https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#` calls from this context, so that app ops manager's uid verification will work with the name.

This is not generally intended for third party application developers.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getPackageCodePath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPackageCodePath(): String!
```

Return the full path to this context's primary Android package. The Android package is a ZIP file which contains application's primary code and assets.

Note: this is not generally useful for applications, since they should not be directly accessing the file system.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | String Path to the code and assets. |

### getPackageManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPackageManager(): PackageManager!
```

Return PackageManager instance to find global package information.

### getPackageName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPackageName(): String!
```

Return the name of this application's package.

### getPackageResourcePath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPackageResourcePath(): String!
```

Return the full path to this context's primary Android package. The Android package is a ZIP file which contains the application's primary resources.

Note: this is not generally useful for applications, since they should not be directly accessing the file system.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | String Path to the resources. |

### getParams

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getParams(): ContextParams?
```

Return the set of parameters which this Context was created with, if it was created via `https://developer.android.com/reference/kotlin/android/content/Context#createContext(android.content.ContextParams)`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/ContextParams?` | This value may be `null`. |

### getResources

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getResources(): Resources!
```

Returns a Resources instance for the application's package.

**Note:** Implementations of this method should return a Resources instance that is consistent with the AssetManager instance returned by `https://developer.android.com/reference/kotlin/android/content/Context#getAssets()`. For example, they should share the same `https://developer.android.com/reference/kotlin/android/content/res/Configuration` object.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/Resources!` | a Resources instance for the application's package |

### getSharedPreferences

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSharedPreferences(
    name: String!, 
    mode: Int
): SharedPreferences!
```

Retrieve and hold the contents of the preferences file 'name', returning a SharedPreferences through which you can retrieve and modify its values. Only one instance of the SharedPreferences object is returned to any callers for the same name, meaning they will see each other's edits as soon as they are made.

This method is thread-safe.

If the preferences directory does not already exist, it will be created when this method is called.

If a preferences file by this name does not exist, it will be created when you retrieve an editor (`https://developer.android.com/reference/kotlin/android/content/SharedPreferences#edit()`) and then commit changes (`https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor#commit()` or `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor#apply()`).

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Desired preferences file. |
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Operating mode. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Context#MODE_PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#MODE_WORLD_READABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#MODE_WORLD_WRITEABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#MODE_MULTI_PROCESS:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/SharedPreferences!` | The single `https://developer.android.com/reference/kotlin/android/content/SharedPreferences` instance that can be used to retrieve and modify the preference values. |

### getSystemService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSystemService(name: String): Any!
```

Return the handle to a system-level service by name. The class of the returned object varies by the requested name. Currently available names are:

`https://developer.android.com/reference/kotlin/android/content/Context#WINDOW_SERVICE:kotlin.String` ("window")
: The top-level window manager in which you can place custom windows. The returned object is a `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#`. Must only be obtained from a visual context such as Activity or a Context created with `https://developer.android.com/reference/kotlin/android/content/Context#createWindowContext(kotlin.Int,%20android.os.Bundle)`, which are adjusted to the configuration and visual bounds of an area on screen.

`https://developer.android.com/reference/kotlin/android/content/Context#LAYOUT_INFLATER_SERVICE:kotlin.String` ("layout_inflater")
: A `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` for inflating layout resources in this context. Must only be obtained from a visual context such as Activity or a Context created with `https://developer.android.com/reference/kotlin/android/content/Context#createWindowContext(kotlin.Int,%20android.os.Bundle)`, which are adjusted to the configuration and visual bounds of an area on screen.

`https://developer.android.com/reference/kotlin/android/content/Context#ACTIVITY_SERVICE:kotlin.String` ("activity")
: A `https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#` for interacting with the global activity state of the system.

`https://developer.android.com/reference/kotlin/android/content/Context#WALLPAPER_SERVICE:kotlin.String` ("wallpaper")
: A `https://developer.android.com/reference/kotlin/android/service/wallpaper/WallpaperService.html#` for accessing wallpapers in this context. Must only be obtained from a visual context such as Activity or a Context created with `https://developer.android.com/reference/kotlin/android/content/Context#createWindowContext(kotlin.Int,%20android.os.Bundle)`, which are adjusted to the configuration and visual bounds of an area on screen.

`https://developer.android.com/reference/kotlin/android/content/Context#POWER_SERVICE:kotlin.String` ("power")
: A `https://developer.android.com/reference/kotlin/android/os/PowerManager.html#` for controlling power management.

`https://developer.android.com/reference/kotlin/android/content/Context#ALARM_SERVICE:kotlin.String` ("alarm")
: A `https://developer.android.com/reference/kotlin/android/app/AlarmManager.html#` for receiving intents at the time of your choosing.

`https://developer.android.com/reference/kotlin/android/content/Context#NOTIFICATION_SERVICE:kotlin.String` ("notification")
: A `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#` for informing the user of background events.

`https://developer.android.com/reference/kotlin/android/content/Context#KEYGUARD_SERVICE:kotlin.String` ("keyguard")
: A `https://developer.android.com/reference/kotlin/android/app/KeyguardManager.html#` for controlling keyguard.

`https://developer.android.com/reference/kotlin/android/content/Context#LOCATION_SERVICE:kotlin.String` ("location")
: A `https://developer.android.com/reference/kotlin/android/location/LocationManager.html#` for controlling location (e.g., GPS) updates.

`https://developer.android.com/reference/kotlin/android/content/Context#SEARCH_SERVICE:kotlin.String` ("search")
: A `https://developer.android.com/reference/kotlin/android/app/SearchManager.html#` for handling search.

`https://developer.android.com/reference/kotlin/android/content/Context#VIBRATOR_MANAGER_SERVICE:kotlin.String` ("vibrator_manager")
: A `https://developer.android.com/reference/kotlin/android/os/VibratorManager.html#` for accessing the device vibrators, interacting with individual ones and playing synchronized effects on multiple vibrators.

`https://developer.android.com/reference/kotlin/android/content/Context#MULTISENSORY_MANAGER_SERVICE:kotlin.String` ("multisensory_manager")
: A `https://developer.android.com/reference/kotlin/android/os/multisensory/MultisensoryManager.html#` for delivering audio-haptic feedback in the Multisensory Design System

`https://developer.android.com/reference/kotlin/android/content/Context#VIBRATOR_SERVICE:kotlin.String` ("vibrator")
: A `https://developer.android.com/reference/kotlin/android/os/Vibrator.html#` for interacting with the vibrator hardware.

`https://developer.android.com/reference/kotlin/android/content/Context#CONNECTIVITY_SERVICE:kotlin.String` ("connectivity")
: A `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#` for handling management of network connections.

`https://developer.android.com/reference/kotlin/android/content/Context#IPSEC_SERVICE:kotlin.String` ("ipsec")
: A `https://developer.android.com/reference/kotlin/android/net/IpSecManager.html#` for managing IPSec on sockets and networks.

`https://developer.android.com/reference/kotlin/android/content/Context#WIFI_SERVICE:kotlin.String` ("wifi")
: A `https://developer.android.com/reference/kotlin/android/net/wifi/WifiManager.html#` for management of Wi-Fi connectivity. On releases before Android 7, it should only be obtained from an application context, and not from any other derived context to avoid memory leaks within the calling process.

`https://developer.android.com/reference/kotlin/android/content/Context#WIFI_AWARE_SERVICE:kotlin.String` ("wifiaware")
: A `https://developer.android.com/reference/kotlin/android/net/wifi/aware/WifiAwareManager.html#` for management of Wi-Fi Aware discovery and connectivity.

`https://developer.android.com/reference/kotlin/android/content/Context#WIFI_P2P_SERVICE:kotlin.String` ("wifip2p")
: A `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.html#` for management of Wi-Fi Direct connectivity.

`https://developer.android.com/reference/kotlin/android/content/Context#INPUT_METHOD_SERVICE:kotlin.String` ("input_method")
: An `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#` for management of input methods.

`https://developer.android.com/reference/kotlin/android/content/Context#UI_MODE_SERVICE:kotlin.String` ("uimode")
: An `https://developer.android.com/reference/kotlin/android/app/UiModeManager.html#` for controlling UI modes.

`https://developer.android.com/reference/kotlin/android/content/Context#DOWNLOAD_SERVICE:kotlin.String` ("download")
: A `https://developer.android.com/reference/kotlin/android/app/DownloadManager.html#` for requesting HTTP downloads

`https://developer.android.com/reference/kotlin/android/content/Context#BATTERY_SERVICE:kotlin.String` ("batterymanager")
: A `https://developer.android.com/reference/kotlin/android/os/BatteryManager.html#` for managing battery state

`https://developer.android.com/reference/kotlin/android/content/Context#JOB_SCHEDULER_SERVICE:kotlin.String` ("taskmanager")
: A `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler.html#` for managing scheduled tasks

`https://developer.android.com/reference/kotlin/android/content/Context#NETWORK_STATS_SERVICE:kotlin.String` ("netstats")
: A `https://developer.android.com/reference/kotlin/android/app/usage/NetworkStatsManager.html#` for querying network usage statistics.

`https://developer.android.com/reference/kotlin/android/content/Context#HARDWARE_PROPERTIES_SERVICE:kotlin.String` ("hardware_properties")
: A `https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager.html#` for accessing hardware properties.

`https://developer.android.com/reference/kotlin/android/content/Context#DOMAIN_VERIFICATION_SERVICE:kotlin.String` ("domain_verification")
: A `https://developer.android.com/reference/kotlin/android/content/pm/verify/domain/DomainVerificationManager` for accessing web domain approval state.

`https://developer.android.com/reference/kotlin/android/content/Context#DISPLAY_HASH_SERVICE:kotlin.String` ("display_hash")
: A `https://developer.android.com/reference/kotlin/android/view/displayhash/DisplayHashManager.html#` for management of display hashes.

`https://developer.android.com/reference/kotlin/android/content/Context#AUTHENTICATION_POLICY_SERVICE:kotlin.String` ("authentication_policy")
: A `https://developer.android.com/reference/kotlin/android/security/authenticationpolicy/AuthenticationPolicyManager.html#` for managing authentication related policies on the device.

<br />

Note: System services obtained via this API may be closely associated with the Context in which they are obtained from. In general, do not share the service objects between various different contexts (Activities, Applications, Services, Providers, etc.)

Note: Instant apps, for which `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#isInstantApp()` returns true, don't have access to the following system services: `https://developer.android.com/reference/kotlin/android/content/Context#DEVICE_POLICY_SERVICE:kotlin.String`, #FINGERPRINT_SERVICE, `https://developer.android.com/reference/kotlin/android/content/Context#KEYGUARD_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context#SHORTCUT_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context#USB_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context#WALLPAPER_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context#WIFI_P2P_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context#WIFI_SERVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/content/Context#WIFI_AWARE_SERVICE:kotlin.String`. For these services this method will return `null`. Generally, if you are running as an instant app you should always check whether the result of this method is `null`.

Note: When implementing this method, keep in mind that new services can be added on newer Android releases, so if you're looking for just the explicit names mentioned above, make sure to return `null` when you don't recognize the name --- if you throw a `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` exception instead, your app might break on new Android releases.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the desired service. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/Context#POWER_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#WINDOW_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#LAYOUT_INFLATER_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#ACCOUNT_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#ACTIVITY_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#ALARM_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#NOTIFICATION_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#ACCESSIBILITY_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#CAPTIONING_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#KEYGUARD_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#LOCATION_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#HEALTHCONNECT_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#SEARCH_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#SENSOR_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#STORAGE_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#STORAGE_STATS_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#WALLPAPER_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#VIBRATOR_MANAGER_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#MULTISENSORY_MANAGER_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#VIBRATOR_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#CONNECTIVITY_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#TETHERING_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#IPSEC_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#VPN_MANAGEMENT_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#NETWORK_STATS_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#WIFI_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#WIFI_AWARE_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#WIFI_P2P_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#WIFI_RTT_RANGING_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#NSD_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#AUDIO_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#BIOMETRIC_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#AUTHENTICATION_POLICY_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#MEDIA_ROUTER_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#TELEPHONY_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#TELEPHONY_SUBSCRIPTION_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#TELEPHONY_PHONE_NUMBER_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#CARRIER_CONFIG_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#EUICC_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#TELECOM_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#CLIPBOARD_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#INPUT_METHOD_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#TEXT_SERVICES_MANAGER_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#TEXT_CLASSIFICATION_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#APPWIDGET_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#DROPBOX_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#DEVICE_POLICY_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#UI_MODE_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#DOWNLOAD_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#NFC_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#BLUETOOTH_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#USB_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#LAUNCHER_APPS_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#SERIAL_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#INPUT_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#DISPLAY_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#USER_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#RESTRICTIONS_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#APP_OPS_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#ROLE_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#CAMERA_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#PRINT_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#CONSUMER_IR_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#TV_INTERACTIVE_APP_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#TV_INPUT_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#USAGE_STATS_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#MEDIA_SESSION_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#MEDIA_COMMUNICATION_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#BATTERY_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#JOB_SCHEDULER_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#PERSISTENT_DATA_BLOCK_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#MEDIA_PROJECTION_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#MIDI_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#HARDWARE_PROPERTIES_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#SHORTCUT_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#SYSTEM_HEALTH_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#COMPANION_DEVICE_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#VIRTUAL_DEVICE_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#CROSS_PROFILE_APPS_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#LOCALE_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#MEDIA_METRICS_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#DISPLAY_HASH_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#CREDENTIAL_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#DEVICE_LOCK_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#GRAMMATICAL_INFLECTION_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#SECURITY_STATE_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#CONTACT_KEYS_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#MEDIA_QUALITY_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#ADVANCED_PROTECTION_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#NPU_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#WEB_APP_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#HID_SERVICE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/content/Context#MEMORY_BUDGET_SERVICE:kotlin.String` . This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | The service or `null` if the name does not exist. |

### getSystemServiceName

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSystemServiceName(serviceClass: Class<*>): String?
```

Gets the name of the system-level service that is represented by the specified class.

| Parameters ||
|---|---|
| `serviceClass` | [Class](../java/lang/Class.md)\<\*\>: The class of the desired service. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | The service name or null if the class is not a supported system service. |

### getTheme

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTheme(): Resources.Theme!
```

Return the Theme object associated with this Context.

### getWallpaper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWallpaper(): Drawable!
```

**Deprecated:** *Deprecated in Java.*

### getWallpaperDesiredMinimumHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWallpaperDesiredMinimumHeight(): Int
```

**Deprecated:** *Deprecated in Java.*

### getWallpaperDesiredMinimumWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWallpaperDesiredMinimumWidth(): Int
```

**Deprecated:** *Deprecated in Java.*

### grantUriPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun grantUriPermission(
    toPackage: String!, 
    uri: Uri!, 
    modeFlags: Int
): Unit
```

Grant permission to access a specific Uri to another package, regardless of whether that package has general permission to access the Uri's content provider. This can be used to grant specific, temporary permissions, typically in response to user interaction (such as the user opening an attachment that you would like someone else to display).

Normally you should use `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` with the Intent being used to start an activity instead of this function directly. If you use this function directly, you should be sure to call #revokeUriPermission when the target should no longer be allowed to access it.

To succeed, the content provider owning the Uri must have set the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestProvider_grantUriPermissions:kotlin.Int` attribute in its manifest or included the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestGrantUriPermission:kotlin.IntArray` tag.

| Parameters ||
|---|---|
| `toPackage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The package you would like to allow to access the Uri. |
| `uri` | [Uri](../android/net/Uri.md)!: The Uri you would like to grant access to. |
| `modeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired access modes. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_PERSISTABLE_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_PREFIX_URI_PERMISSION:kotlin.Int` |
| --- | --- |

### isDeviceProtectedStorage

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDeviceProtectedStorage(): Boolean
```

Indicates if the storage APIs of this Context are backed by device-protected storage.

### isRestricted

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isRestricted(): Boolean
```

Indicates whether this Context is restricted.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this Context is restricted, `false` otherwise. |

### isUiContext

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isUiContext(): Boolean
```

Returns `true` if the context is a UI context which can access UI components such as `https://developer.android.com/reference/kotlin/android/view/WindowManager.html#`, `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#` or `https://developer.android.com/reference/kotlin/android/app/WallpaperManager.html#`. Accessing UI components from non-UI contexts throws `https://developer.android.com/reference/kotlin/android/os/strictmode/Violation.html#` if `https://developer.android.com/reference/kotlin/android/os/StrictMode.VmPolicy.Builder.html#detectIncorrectContextUse()` is enabled.

Examples of UI contexts are an `https://developer.android.com/reference/kotlin/android/app/Activity.html#`, a context created from `https://developer.android.com/reference/kotlin/android/content/Context#createWindowContext(kotlin.Int,%20android.os.Bundle)` or `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#`

Note that even if it is allowed programmatically, it is not suggested to override this method to bypass `https://developer.android.com/reference/kotlin/android/os/strictmode/IncorrectContextUseViolation.html#` verification.

### moveDatabaseFrom

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun moveDatabaseFrom(
    sourceContext: Context!, 
    name: String!
): Boolean
```

Move an existing database file from the given source storage context to this context. This is typically used to migrate data between storage locations after an upgrade, such as migrating to device protected storage.

The database must be closed before being moved.

| Parameters ||
|---|---|
| `sourceContext` | [Context](../android/content/Context.md)!: The source context which contains the existing database to move. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the database file. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the move was successful or if the database didn't exist in the source context, otherwise `false`. |

### moveSharedPreferencesFrom

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun moveSharedPreferencesFrom(
    sourceContext: Context!, 
    name: String!
): Boolean
```

Move an existing shared preferences file from the given source storage context to this context. This is typically used to migrate data between storage locations after an upgrade, such as moving to device protected storage.

| Parameters ||
|---|---|
| `sourceContext` | [Context](../android/content/Context.md)!: The source context which contains the existing shared preferences to move. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the shared preferences file. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the move was successful or if the shared preferences didn't exist in the source context, otherwise `false`. |

### openFileInput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun openFileInput(name: String!): FileInputStream!
```

Open a private file associated with this Context's application package for reading.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the file to open; can not contain path separators. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/FileInputStream.html#!` | The resulting `https://developer.android.com/reference/kotlin/java/io/FileInputStream.html#`. |

### openFileOutput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun openFileOutput(
    name: String!, 
    mode: Int
): FileOutputStream!
```

Open a private file associated with this Context's application package for writing. Creates the file if it doesn't already exist.

No additional permissions are required for the calling app to read or write the returned file.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the file to open; can not contain path separators. |
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Operating mode. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Context#MODE_PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#MODE_WORLD_READABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#MODE_WORLD_WRITEABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#MODE_APPEND:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/FileOutputStream.html#!` | The resulting `https://developer.android.com/reference/kotlin/java/io/FileOutputStream.html#`. |

### openOrCreateDatabase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun openOrCreateDatabase(
    name: String!, 
    mode: Int, 
    factory: SQLiteDatabase.CursorFactory!
): SQLiteDatabase!
```

Open a new private SQLiteDatabase associated with this Context's application package. Create the database file if it doesn't exist.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name (unique in the application package) of the database. |
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Operating mode. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Context#MODE_PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#MODE_WORLD_READABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#MODE_WORLD_WRITEABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#MODE_ENABLE_WRITE_AHEAD_LOGGING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#MODE_NO_LOCALIZED_COLLATORS:kotlin.Int` |
| `factory` | [SQLiteDatabase.CursorFactory](../android/database/sqlite/SQLiteDatabase.CursorFactory.md)!: An optional factory class that is called to instantiate a cursor when query is called. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.html#!` | The contents of a newly created database with the given name. |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteException` | if the database file could not be opened. |

### openOrCreateDatabase

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun openOrCreateDatabase(
    name: String!, 
    mode: Int, 
    factory: SQLiteDatabase.CursorFactory!, 
    errorHandler: DatabaseErrorHandler?
): SQLiteDatabase!
```

Open a new private SQLiteDatabase associated with this Context's application package. Creates the database file if it doesn't exist.

Accepts input param: a concrete instance of `https://developer.android.com/reference/kotlin/android/database/DatabaseErrorHandler.html#` to be used to handle corruption when sqlite reports database corruption.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name (unique in the application package) of the database. |
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Operating mode. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Context#MODE_PRIVATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#MODE_WORLD_READABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#MODE_WORLD_WRITEABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#MODE_ENABLE_WRITE_AHEAD_LOGGING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#MODE_NO_LOCALIZED_COLLATORS:kotlin.Int` |
| `factory` | [SQLiteDatabase.CursorFactory](../android/database/sqlite/SQLiteDatabase.CursorFactory.md)!: An optional factory class that is called to instantiate a cursor when query is called. |
| --- | --- |
| `errorHandler` | [DatabaseErrorHandler](../android/database/DatabaseErrorHandler.md)?: This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteDatabase.html#!` | The contents of a newly created database with the given name. |

| Exceptions ||
|---|---|
| `android.database.sqlite.SQLiteException` | if the database file could not be opened. |

### peekWallpaper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun peekWallpaper(): Drawable!
```

**Deprecated:** *Deprecated in Java.*

### rebindService

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun rebindService(
    conn: ServiceConnection, 
    flags: Context.BindServiceFlags
): Unit
```

Rebind an application service with updated bind service flags

| Parameters ||
|---|---|
| `conn` | [ServiceConnection](../android/content/ServiceConnection.md): This value cannot be `null`. |
| `flags` | [Context.BindServiceFlags](../android/content/Context.BindServiceFlags.md): This value cannot be `null`. |

### registerComponentCallbacks

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerComponentCallbacks(callback: ComponentCallbacks!): Unit
```

Add a new `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks` to the base application of the Context, which will be called at the same times as the ComponentCallbacks methods of activities and other components are called. Note that you *must* be sure to use `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#unregisterComponentCallbacks(android.content.ComponentCallbacks)` when appropriate in the future; this will not be removed for you.

After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks` will be registered to `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getBaseContext()`, and can be only used after `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#attachBaseContext(android.content.Context)`. Users can still call to `getApplicationContext().registerComponentCallbacks(ComponentCallbacks)` to add `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks` to the base application.

| Parameters ||
|---|---|
| `callback` | [ComponentCallbacks](../android/content/ComponentCallbacks.md)!: The interface to call. This can be either a `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks` or `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2` interface. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this method calls before `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#attachBaseContext(android.content.Context)` |

### registerDeviceIdChangeListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerDeviceIdChangeListener(
    executor: Executor, 
    listener: IntConsumer
): Unit
```

Adds a new device ID changed listener to the `Context`, which will be called when the device association is changed by the system.

The callback can be called when an app is moved to a different device and the `Context` is not explicitly associated with a specific device.

When an application receives a device id update callback, this Context is guaranteed to also have an updated display ID(if any) and `https://developer.android.com/reference/kotlin/android/content/res/Configuration`.

<br />

| Parameters ||
|---|---|
| `executor` | [Executor](../java/util/concurrent/Executor.md): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [IntConsumer](../java/util/function/IntConsumer.md): This value cannot be `null`. |

### registerReceiver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerReceiver(
    receiver: BroadcastReceiver?, 
    filter: IntentFilter!
): Intent?
```

Register a BroadcastReceiver to be run in the main activity thread. The receiver will be called with any broadcast Intent that matches filter, in the main application thread.

The system may broadcast Intents that are "sticky" -- these stay around after the broadcast has finished, to be sent to any later registrations. If your IntentFilter matches one of these sticky Intents, that Intent will be returned by this function **and** sent to your receiver as if it had just been broadcast.

There may be multiple sticky Intents that match filter, in which case each of these will be sent to receiver. In this case, only one of these can be returned directly by the function; which of these that is returned is arbitrarily decided by the system.

If you know the Intent you are registering for is sticky, you can supply null for your receiver. In this case, no receiver is registered -- the function simply returns the sticky Intent that matches filter. In the case of multiple matches, the same rules as described above apply.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver` for more information on Intent broadcasts.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, the system can [place context-registered broadcasts in a queue while the app is in the](https://developer.android.com/develop/background-work/background-tasks/broadcasts#android-14) [cached state](https://developer.android.com/guide/components/activities/process-lifecycle). When the app leaves the cached state, such as returning to the foreground, the system delivers any queued broadcasts. Multiple instances of certain broadcasts might be merged into one broadcast.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, receivers registered with this method will correctly respect the `https://developer.android.com/reference/kotlin/android/content/Intent#setPackage(kotlin.String)` specified for an Intent being broadcast. Prior to that, it would be ignored and delivered to all matching registered receivers. Be careful if using this for security.

For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, either `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_EXPORTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_NOT_EXPORTED:kotlin.Int` must be specified if the receiver is not being registered for [system broadcasts](https://developer.android.com/guide/components/broadcasts#system-broadcasts) or a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown. See `https://developer.android.com/reference/kotlin/android/content/Context#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.Int)` to register a receiver with flags.

Note: this method *cannot be called from a `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver` component;* that is, from a BroadcastReceiver that is declared in an application's manifest. It is okay, however, to call this method from another BroadcastReceiver that has itself been registered at run time with #registerReceiver, since the lifetime of such a registered BroadcastReceiver is tied to the object that registered it.

| Parameters ||
|---|---|
| `receiver` | [BroadcastReceiver](../android/content/BroadcastReceiver.md)?: This value may be `null`. |
| `filter` | [IntentFilter](../android/content/IntentFilter.md)!: Selects the Intent broadcasts to be received. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Intent?` | The first sticky intent found that matches filter, or null if there are none. |

### registerReceiver

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerReceiver(
    receiver: BroadcastReceiver?, 
    filter: IntentFilter!, 
    flags: Int
): Intent?
```

Register to receive intent broadcasts, with the receiver optionally being exposed to Instant Apps. See `https://developer.android.com/reference/kotlin/android/content/Context#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)` for more information. By default Instant Apps cannot interact with receivers in other applications, this allows you to expose a receiver that Instant Apps can interact with.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver` for more information on Intent broadcasts.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, the system can [place context-registered broadcasts in a queue while the app is in the](https://developer.android.com/develop/background-work/background-tasks/broadcasts#android-14) [cached state](https://developer.android.com/guide/components/activities/process-lifecycle). When the app leaves the cached state, such as returning to the foreground, the system delivers any queued broadcasts. Multiple instances of certain broadcasts might be merged into one broadcast.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, receivers registered with this method will correctly respect the `https://developer.android.com/reference/kotlin/android/content/Intent#setPackage(kotlin.String)` specified for an Intent being broadcast. Prior to that, it would be ignored and delivered to all matching registered receivers. Be careful if using this for security.

| Parameters ||
|---|---|
| `receiver` | [BroadcastReceiver](../android/content/BroadcastReceiver.md)?: This value may be `null`. |
| `filter` | [IntentFilter](../android/content/IntentFilter.md)!: Selects the Intent broadcasts to be received. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional options for the receiver. For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` either `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_EXPORTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_NOT_EXPORTED:kotlin.Int` must be specified if the receiver isn't being registered for [system broadcasts](https://developer.android.com/guide/components/broadcasts#system-broadcasts) or a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown. If `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_EXPORTED:kotlin.Int` is specified, a receiver may additionally specify `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_VISIBLE_TO_INSTANT_APPS:kotlin.Int`. For a complete list of system broadcast actions, see the BROADCAST_ACTIONS.TXT file in the Android SDK. If both `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_EXPORTED:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_NOT_EXPORTED:kotlin.Int` are specified, an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_VISIBLE_TO_INSTANT_APPS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_EXPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_NOT_EXPORTED:kotlin.Int` |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Intent?` | The first sticky intent found that matches filter, or null if there are none. |

### registerReceiver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerReceiver(
    receiver: BroadcastReceiver?, 
    filter: IntentFilter!, 
    broadcastPermission: String?, 
    scheduler: Handler?
): Intent?
```

Register to receive intent broadcasts, to run in the context of scheduler. See `https://developer.android.com/reference/kotlin/android/content/Context#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)` for more information. This allows you to enforce permissions on who can broadcast intents to your receiver, or have the receiver run in a different thread than the main application thread.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver` for more information on Intent broadcasts.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, the system can [place context-registered broadcasts in a queue while the app is in the](https://developer.android.com/develop/background-work/background-tasks/broadcasts#android-14) [cached state](https://developer.android.com/guide/components/activities/process-lifecycle). When the app leaves the cached state, such as returning to the foreground, the system delivers any queued broadcasts. Multiple instances of certain broadcasts might be merged into one broadcast.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, receivers registered with this method will correctly respect the `https://developer.android.com/reference/kotlin/android/content/Intent#setPackage(kotlin.String)` specified for an Intent being broadcast. Prior to that, it would be ignored and delivered to all matching registered receivers. Be careful if using this for security.

For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, either `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_EXPORTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_NOT_EXPORTED:kotlin.Int` must be specified if the receiver is not being registered for [system broadcasts](https://developer.android.com/guide/components/broadcasts#system-broadcasts) or a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown. See `https://developer.android.com/reference/kotlin/android/content/Context#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.String,%20android.os.Handler,%20kotlin.Int)` to register a receiver with flags.

| Parameters ||
|---|---|
| `receiver` | [BroadcastReceiver](../android/content/BroadcastReceiver.md)?: This value may be `null`. |
| `filter` | [IntentFilter](../android/content/IntentFilter.md)!: Selects the Intent broadcasts to be received. |
| `broadcastPermission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| --- | --- |
| `scheduler` | [Handler](../android/os/Handler.md)?: This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Intent?` | The first sticky intent found that matches filter, or null if there are none. |

### registerReceiver

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerReceiver(
    receiver: BroadcastReceiver?, 
    filter: IntentFilter!, 
    broadcastPermission: String?, 
    scheduler: Handler?, 
    flags: Int
): Intent?
```

Register to receive intent broadcasts, to run in the context of scheduler. See `https://developer.android.com/reference/kotlin/android/content/Context#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/content/Context#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter,%20kotlin.String,%20android.os.Handler)` for more information.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver` for more information on Intent broadcasts.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int`, the system can [place context-registered broadcasts in a queue while the app is in the](https://developer.android.com/develop/background-work/background-tasks/broadcasts#android-14) [cached state](https://developer.android.com/guide/components/activities/process-lifecycle). When the app leaves the cached state, such as returning to the foreground, the system delivers any queued broadcasts. Multiple instances of certain broadcasts might be merged into one broadcast.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#ICE_CREAM_SANDWICH:kotlin.Int`, receivers registered with this method will correctly respect the `https://developer.android.com/reference/kotlin/android/content/Intent#setPackage(kotlin.String)` specified for an Intent being broadcast. Prior to that, it would be ignored and delivered to all matching registered receivers. Be careful if using this for security.

| Parameters ||
|---|---|
| `receiver` | [BroadcastReceiver](../android/content/BroadcastReceiver.md)?: This value may be `null`. |
| `filter` | [IntentFilter](../android/content/IntentFilter.md)!: Selects the Intent broadcasts to be received. |
| `broadcastPermission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| --- | --- |
| `scheduler` | [Handler](../android/os/Handler.md)?: This value may be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional options for the receiver. For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` either `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_EXPORTED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_NOT_EXPORTED:kotlin.Int` must be specified if the receiver isn't being registered for [system broadcasts](https://developer.android.com/guide/components/broadcasts#system-broadcasts) or a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown. If `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_EXPORTED:kotlin.Int` is specified, a receiver may additionally specify `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_VISIBLE_TO_INSTANT_APPS:kotlin.Int`. For a complete list of system broadcast actions, see the BROADCAST_ACTIONS.TXT file in the Android SDK. If both `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_EXPORTED:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_NOT_EXPORTED:kotlin.Int` are specified, an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_VISIBLE_TO_INSTANT_APPS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_EXPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Context#RECEIVER_NOT_EXPORTED:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Intent?` | The first sticky intent found that matches filter, or null if there are none. |

### removeStickyBroadcast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeStickyBroadcast(intent: Intent!): Unit
```

**Deprecated:** *Deprecated in Java.*

Remove the data previously sent with #sendStickyBroadcast, so that it is as if the sticky broadcast had never happened. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

| Parameters ||
|---|---|
| `intent` | [Intent](../android/content/Intent.md)!: The Intent that was previously broadcast. |

### removeStickyBroadcastAsUser

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeStickyBroadcastAsUser(
    intent: Intent!, 
    user: UserHandle!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Version of `https://developer.android.com/reference/kotlin/android/content/Context#removeStickyBroadcast(android.content.Intent)` that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image.

You must hold the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String` permission in order to use this API. If you do not hold that permission, `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` will be thrown. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

| Parameters ||
|---|---|
| `intent` | [Intent](../android/content/Intent.md)!: The Intent that was previously broadcast. |
| `user` | [UserHandle](../android/os/UserHandle.md)!: UserHandle to remove the sticky broadcast from. |

### revokeSelfPermissionsOnKill

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun revokeSelfPermissionsOnKill(permissions: MutableCollection<String!>): Unit
```

Triggers the revocation of one or more permissions for the calling package. A package is only able to revoke runtime permissions. If a permission is not currently granted, it is ignored and will not get revoked (even if later granted by the user). Ultimately, you should never make assumptions about a permission status as users may grant or revoke them at any time.

Background permissions which have no corresponding foreground permission still granted once the revocation is effective will also be revoked.

The revocation happens asynchronously and kills all processes running in the calling UID. It will be triggered once it is safe to do so. In particular, it will not be triggered as long as the package remains in the foreground, or has any active manifest components (e.g. when another app is accessing a content provider in the package).

If you want to revoke the permissions right away, you could call `System.exit()` in `Handler.postDelayed` with a delay to allow completion of async IPC, But `System.exit()` could affect other apps that are accessing your app at the moment. For example, apps accessing a content provider in your app will all crash.

Note that the settings UI shows a permission group as granted as long as at least one permission in the group is granted. If you want the user to observe the revocation in the settings, you should revoke every permission in the target group. To learn the current list of permissions in a group, you may use `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getGroupOfPlatformPermission(kotlin.String,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` and `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getPlatformPermissionsForGroup(kotlin.String,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`. This list of permissions may evolve over time, so it is recommended to check whether it contains any permission you wish to retain before trying to revoke an entire group.

| Parameters ||
|---|---|
| `permissions` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if any of the permissions is not a runtime permission |

### revokeUriPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun revokeUriPermission(
    uri: Uri!, 
    modeFlags: Int
): Unit
```

Remove all permissions to access a particular content provider Uri that were previously added with `https://developer.android.com/reference/kotlin/android/content/Context#grantUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)` or *any other* mechanism. The given Uri will match all previously granted Uris that are the same or a sub-path of the given Uri. That is, revoking "content://foo/target" will revoke both "content://foo/target" and "content://foo/target/sub", but not "content://foo". It will not remove any prefix grants that exist at a higher level.

Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int`, if you did not have regular permission access to a Uri, but had received access to it through a specific Uri permission grant, you could not revoke that grant with this function and a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` would be thrown. As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int`, this function will not throw a security exception, but will remove whatever permission grants to the Uri had been given to the app (or none).

Unlike `https://developer.android.com/reference/kotlin/android/content/Context#revokeUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)`, this method impacts all permission grants matching the given Uri, for any package they had been granted to, through any mechanism this had happened (such as indirectly through the clipboard, activity launch, service start, etc). That means this can be potentially dangerous to use, as it can revoke grants that another app could be strongly expecting to stick around.

| Parameters ||
|---|---|
| `uri` | [Uri](../android/net/Uri.md)!: The Uri you would like to revoke access to. |
| `modeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The access modes to revoke. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` |

### revokeUriPermission

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun revokeUriPermission(
    targetPackage: String!, 
    uri: Uri!, 
    modeFlags: Int
): Unit
```

Remove permissions to access a particular content provider Uri that were previously added with `https://developer.android.com/reference/kotlin/android/content/Context#grantUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)` for a specific target package. The given Uri will match all previously granted Uris that are the same or a sub-path of the given Uri. That is, revoking "content://foo/target" will revoke both "content://foo/target" and "content://foo/target/sub", but not "content://foo". It will not remove any prefix grants that exist at a higher level.

Unlike `https://developer.android.com/reference/kotlin/android/content/Context#revokeUriPermission(android.net.Uri,%20kotlin.Int)`, this method will *only* revoke permissions that had been explicitly granted through `https://developer.android.com/reference/kotlin/android/content/Context#grantUriPermission(kotlin.String,%20android.net.Uri,%20kotlin.Int)` and only for the package specified. Any matching grants that have happened through other mechanisms (clipboard, activity launching, service starting, etc) will not be removed.

| Parameters ||
|---|---|
| `toPackage` | The package you had previously granted access to. |
| `uri` | [Uri](../android/net/Uri.md)!: The Uri you would like to revoke access to. |
| `modeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The access modes to revoke. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` |
| --- | --- |

### sendBroadcast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendBroadcast(intent: Intent!): Unit
```

Broadcast the given intent to all interested BroadcastReceivers. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run. No results are propagated from receivers and receivers can not abort the broadcast. If you want to allow receivers to propagate results or abort the broadcast, you must send an ordered broadcast using `https://developer.android.com/reference/kotlin/android/content/Context#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver` for more information on Intent broadcasts.

| Parameters ||
|---|---|
| `intent` | [Intent](../android/content/Intent.md)!: The Intent to broadcast; all receivers matching this Intent will receive the broadcast. |

### sendBroadcast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendBroadcast(
    intent: Intent!, 
    receiverPermission: String?
): Unit
```

Broadcast the given intent to all interested BroadcastReceivers, allowing an optional required permission to be enforced. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run. No results are propagated from receivers and receivers can not abort the broadcast. If you want to allow receivers to propagate results or abort the broadcast, you must send an ordered broadcast using `https://developer.android.com/reference/kotlin/android/content/Context#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver` for more information on Intent broadcasts.

| Parameters ||
|---|---|
| `intent` | [Intent](../android/content/Intent.md)!: The Intent to broadcast; all receivers matching this Intent will receive the broadcast. |
| `receiverPermission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

### sendBroadcast

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendBroadcast(
    intent: Intent, 
    receiverPermission: String?, 
    options: Bundle?
): Unit
```

Broadcast the given intent to all interested BroadcastReceivers, allowing an optional required permission to be enforced. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run. No results are propagated from receivers and receivers can not abort the broadcast. If you want to allow receivers to propagate results or abort the broadcast, you must send an ordered broadcast using `https://developer.android.com/reference/kotlin/android/content/Context#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver` for more information on Intent broadcasts.

| Parameters ||
|---|---|
| `intent` | [Intent](../android/content/Intent.md): This value cannot be `null`. |
| `receiverPermission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `options` | [Bundle](../android/os/Bundle.md)?: This value may be `null`. |
| --- | --- |

### sendBroadcastAsUser

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendBroadcastAsUser(
    intent: Intent!, 
    user: UserHandle!
): Unit
```

Version of `https://developer.android.com/reference/kotlin/android/content/Context#sendBroadcast(android.content.Intent)` that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS

| Parameters ||
|---|---|
| `intent` | [Intent](../android/content/Intent.md)!: The intent to broadcast |
| `user` | [UserHandle](../android/os/UserHandle.md)!: UserHandle to send the intent to. |

### sendBroadcastAsUser

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendBroadcastAsUser(
    intent: Intent!, 
    user: UserHandle!, 
    receiverPermission: String?
): Unit
```

Version of `https://developer.android.com/reference/kotlin/android/content/Context#sendBroadcast(android.content.Intent,%20kotlin.String)` that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS

| Parameters ||
|---|---|
| `intent` | [Intent](../android/content/Intent.md)!: The Intent to broadcast; all receivers matching this Intent will receive the broadcast. |
| `user` | [UserHandle](../android/os/UserHandle.md)!: UserHandle to send the intent to. |
| `receiverPermission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: (optional) String naming a permission that a receiver must hold in order to receive your broadcast. If null, no permission is required. |
| --- | --- |

### sendOrderedBroadcast

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendOrderedBroadcast(
    intent: Intent, 
    initialCode: Int, 
    receiverPermission: String?, 
    receiverAppOp: String?, 
    resultReceiver: BroadcastReceiver?, 
    scheduler: Handler?, 
    initialData: String?, 
    initialExtras: Bundle?, 
    options: Bundle?
): Unit
```

| Parameters ||
|---|---|
| `intent` | [Intent](../android/content/Intent.md): This value cannot be `null`. |
| `receiverPermission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `receiverAppOp` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| --- | --- |
| `resultReceiver` | [BroadcastReceiver](../android/content/BroadcastReceiver.md)?: This value may be `null`. |
| `scheduler` | [Handler](../android/os/Handler.md)?: This value may be `null`. |
| `initialData` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| --- | --- |
| `initialExtras` | [Bundle](../android/os/Bundle.md)?: This value may be `null`. |
| `options` | [Bundle](../android/os/Bundle.md)?: This value may be `null`. |

### sendOrderedBroadcast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendOrderedBroadcast(
    intent: Intent!, 
    receiverPermission: String?
): Unit
```

Broadcast the given intent to all interested BroadcastReceivers, delivering them one at a time to allow more preferred receivers to consume the broadcast before it is delivered to less preferred receivers. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver` for more information on Intent broadcasts.

| Parameters ||
|---|---|
| `intent` | [Intent](../android/content/Intent.md)!: The Intent to broadcast; all receivers matching this Intent will receive the broadcast. |
| `receiverPermission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

### sendOrderedBroadcast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendOrderedBroadcast(
    intent: Intent, 
    receiverPermission: String?, 
    resultReceiver: BroadcastReceiver?, 
    scheduler: Handler?, 
    initialCode: Int, 
    initialData: String?, 
    initialExtras: Bundle?
): Unit
```

Version of `https://developer.android.com/reference/kotlin/android/content/Context#sendBroadcast(android.content.Intent)` that allows you to receive data back from the broadcast. This is accomplished by supplying your own BroadcastReceiver when calling, which will be treated as a final receiver at the end of the broadcast -- its `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver#onReceive(android.content.Context,%20android.content.Intent)` method will be called with the result values collected from the other receivers. The broadcast will be serialized in the same way as calling `https://developer.android.com/reference/kotlin/android/content/Context#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

Like `https://developer.android.com/reference/kotlin/android/content/Context#sendBroadcast(android.content.Intent)`, this method is asynchronous; it will return before resultReceiver.onReceive() is called.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver` for more information on Intent broadcasts.

| Parameters ||
|---|---|
| `intent` | [Intent](../android/content/Intent.md): The Intent to broadcast; all receivers matching this Intent will receive the broadcast. This value cannot be `null`. |
| `receiverPermission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `resultReceiver` | [BroadcastReceiver](../android/content/BroadcastReceiver.md)?: This value may be `null`. |
| --- | --- |
| `scheduler` | [Handler](../android/os/Handler.md)?: This value may be `null`. |
| `initialCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An initial value for the result code. Often Activity.RESULT_OK. |
| `initialData` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| --- | --- |
| `initialExtras` | [Bundle](../android/os/Bundle.md)?: This value may be `null`. |

### sendOrderedBroadcast

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendOrderedBroadcast(
    intent: Intent, 
    receiverPermission: String?, 
    options: Bundle?
): Unit
```

Broadcast the given intent to all interested BroadcastReceivers, delivering them one at a time to allow more preferred receivers to consume the broadcast before it is delivered to less preferred receivers. This call is asynchronous; it returns immediately, and you will continue executing while the receivers are run.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver` for more information on Intent broadcasts.

| Parameters ||
|---|---|
| `intent` | [Intent](../android/content/Intent.md): This value cannot be `null`. |
| `receiverPermission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `options` | [Bundle](../android/os/Bundle.md)?: This value may be `null`. |
| --- | --- |

### sendOrderedBroadcast

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendOrderedBroadcast(
    intent: Intent, 
    receiverPermission: String?, 
    options: Bundle?, 
    resultReceiver: BroadcastReceiver?, 
    scheduler: Handler?, 
    initialCode: Int, 
    initialData: String?, 
    initialExtras: Bundle?
): Unit
```

Version of `https://developer.android.com/reference/kotlin/android/content/Context#sendBroadcast(android.content.Intent)` that allows you to receive data back from the broadcast. This is accomplished by supplying your own BroadcastReceiver when calling, which will be treated as a final receiver at the end of the broadcast -- its `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver#onReceive(android.content.Context,%20android.content.Intent)` method will be called with the result values collected from the other receivers. The broadcast will be serialized in the same way as calling `https://developer.android.com/reference/kotlin/android/content/Context#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

Like `https://developer.android.com/reference/kotlin/android/content/Context#sendBroadcast(android.content.Intent)`, this method is asynchronous; it will return before resultReceiver.onReceive() is called.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver` for more information on Intent broadcasts.

| Parameters ||
|---|---|
| `intent` | [Intent](../android/content/Intent.md): This value cannot be `null`. |
| `receiverPermission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `options` | [Bundle](../android/os/Bundle.md)?: This value may be `null`. |
| --- | --- |
| `resultReceiver` | [BroadcastReceiver](../android/content/BroadcastReceiver.md)?: This value may be `null`. |
| `scheduler` | [Handler](../android/os/Handler.md)?: This value may be `null`. |
| `initialCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An initial value for the result code. Often Activity.RESULT_OK. |
| --- | --- |
| `initialData` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `initialExtras` | [Bundle](../android/os/Bundle.md)?: This value may be `null`. |

### sendOrderedBroadcast

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendOrderedBroadcast(
    intent: Intent, 
    receiverPermission: String?, 
    receiverAppOp: String?, 
    resultReceiver: BroadcastReceiver?, 
    scheduler: Handler?, 
    initialCode: Int, 
    initialData: String?, 
    initialExtras: Bundle?
): Unit
```

Version of `https://developer.android.com/reference/kotlin/android/content/Context#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)` that allows you to specify the App Op to enforce restrictions on which receivers the broadcast will be sent to.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver` for more information on Intent broadcasts.

| Parameters ||
|---|---|
| `intent` | [Intent](../android/content/Intent.md): This value cannot be `null`. |
| `receiverPermission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `receiverAppOp` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| --- | --- |
| `resultReceiver` | [BroadcastReceiver](../android/content/BroadcastReceiver.md)?: This value may be `null`. |
| `scheduler` | [Handler](../android/os/Handler.md)?: This value may be `null`. |
| `initialCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An initial value for the result code. Often Activity.RESULT_OK. |
| --- | --- |
| `initialData` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `initialExtras` | [Bundle](../android/os/Bundle.md)?: This value may be `null`. |

### sendOrderedBroadcastAsUser

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendOrderedBroadcastAsUser(
    intent: Intent!, 
    user: UserHandle!, 
    receiverPermission: String?, 
    resultReceiver: BroadcastReceiver?, 
    scheduler: Handler?, 
    initialCode: Int, 
    initialData: String?, 
    initialExtras: Bundle?
): Unit
```

Version of `https://developer.android.com/reference/kotlin/android/content/Context#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)` that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver` for more information on Intent broadcasts. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS

| Parameters ||
|---|---|
| `intent` | [Intent](../android/content/Intent.md)!: The Intent to broadcast; all receivers matching this Intent will receive the broadcast. |
| `user` | [UserHandle](../android/os/UserHandle.md)!: UserHandle to send the intent to. |
| `receiverPermission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| --- | --- |
| `resultReceiver` | [BroadcastReceiver](../android/content/BroadcastReceiver.md)?: This value may be `null`. |
| `scheduler` | [Handler](../android/os/Handler.md)?: This value may be `null`. |
| `initialCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An initial value for the result code. Often Activity.RESULT_OK. |
| --- | --- |
| `initialData` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `initialExtras` | [Bundle](../android/os/Bundle.md)?: This value may be `null`. |

### sendStickyBroadcast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendStickyBroadcast(intent: Intent!): Unit
```

**Deprecated:** *Deprecated in Java.*

Perform a `https://developer.android.com/reference/kotlin/android/content/Context#sendBroadcast(android.content.Intent)` that is "sticky," meaning the Intent you are sending stays around after the broadcast is complete, so that others can quickly retrieve that data through the return value of `https://developer.android.com/reference/kotlin/android/content/Context#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)`. In all other ways, this behaves the same as `https://developer.android.com/reference/kotlin/android/content/Context#sendBroadcast(android.content.Intent)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

| Parameters ||
|---|---|
| `intent` | [Intent](../android/content/Intent.md)!: The Intent to broadcast; all receivers matching this Intent will receive the broadcast, and the Intent will be held to be re-broadcast to future receivers. |

### sendStickyBroadcast

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendStickyBroadcast(
    intent: Intent, 
    options: Bundle?
): Unit
```

**Deprecated:** *Sticky broadcasts should not be used. They provide no security (anyone can access them), no protection (anyone can modify them), and many other problems. The recommended pattern is to use a non-sticky broadcast to report that *something* has changed, with another mechanism for apps to retrieve the current value whenever desired.*

Perform a `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#sendBroadcast(android.content.Intent)` that is "sticky," meaning the Intent you are sending stays around after the broadcast is complete, so that others can quickly retrieve that data through the return value of `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)`. In all other ways, this behaves the same as `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#sendBroadcast(android.content.Intent)`.

| Parameters ||
|---|---|
| `intent` | [Intent](../android/content/Intent.md): The Intent to broadcast; all receivers matching this Intent will receive the broadcast, and the Intent will be held to be re-broadcast to future receivers. This value cannot be `null`. |
| `options` | [Bundle](../android/os/Bundle.md)?: (optional) Additional sending options, generated from a `https://developer.android.com/reference/kotlin/android/app/BroadcastOptions.html#`. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#sendBroadcast(android.content.Intent)`
- `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#sendStickyOrderedBroadcast(android.content.Intent,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)`

### sendStickyBroadcastAsUser

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendStickyBroadcastAsUser(
    intent: Intent!, 
    user: UserHandle!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Version of `https://developer.android.com/reference/kotlin/android/content/Context#sendStickyBroadcast(android.content.Intent)` that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

| Parameters ||
|---|---|
| `intent` | [Intent](../android/content/Intent.md)!: The Intent to broadcast; all receivers matching this Intent will receive the broadcast, and the Intent will be held to be re-broadcast to future receivers. |
| `user` | [UserHandle](../android/os/UserHandle.md)!: UserHandle to send the intent to. |

### sendStickyOrderedBroadcast

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendStickyOrderedBroadcast(
    intent: Intent!, 
    resultReceiver: BroadcastReceiver?, 
    scheduler: Handler?, 
    initialCode: Int, 
    initialData: String?, 
    initialExtras: Bundle?
): Unit
```

**Deprecated:** *Deprecated in Java.*

Version of #sendStickyBroadcast that allows you to receive data back from the broadcast. This is accomplished by supplying your own BroadcastReceiver when calling, which will be treated as a final receiver at the end of the broadcast -- its `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver#onReceive(android.content.Context,%20android.content.Intent)` method will be called with the result values collected from the other receivers. The broadcast will be serialized in the same way as calling `https://developer.android.com/reference/kotlin/android/content/Context#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`.

Like `https://developer.android.com/reference/kotlin/android/content/Context#sendBroadcast(android.content.Intent)`, this method is asynchronous; it will return before resultReceiver.onReceive() is called. Note that the sticky data stored is only the data you initially supply to the broadcast, not the result of any changes made by the receivers.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver` for more information on Intent broadcasts. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

| Parameters ||
|---|---|
| `intent` | [Intent](../android/content/Intent.md)!: The Intent to broadcast; all receivers matching this Intent will receive the broadcast. |
| `resultReceiver` | [BroadcastReceiver](../android/content/BroadcastReceiver.md)?: This value may be `null`. |
| `scheduler` | [Handler](../android/os/Handler.md)?: This value may be `null`. |
| --- | --- |
| `initialCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An initial value for the result code. Often Activity.RESULT_OK. |
| `initialData` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `initialExtras` | [Bundle](../android/os/Bundle.md)?: This value may be `null`. |
| --- | --- |

### sendStickyOrderedBroadcastAsUser

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendStickyOrderedBroadcastAsUser(
    intent: Intent!, 
    user: UserHandle!, 
    resultReceiver: BroadcastReceiver?, 
    scheduler: Handler?, 
    initialCode: Int, 
    initialData: String?, 
    initialExtras: Bundle?
): Unit
```

**Deprecated:** *Deprecated in Java.*

Version of `https://developer.android.com/reference/kotlin/android/content/Context#sendStickyOrderedBroadcast(android.content.Intent,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)` that allows you to specify the user the broadcast will be sent to. This is not available to applications that are not pre-installed on the system image.

See `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver` for more information on Intent broadcasts. 
Requires android.Manifest.permission.INTERACT_ACROSS_USERS and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BROADCAST_STICKY:kotlin.String`

| Parameters ||
|---|---|
| `intent` | [Intent](../android/content/Intent.md)!: The Intent to broadcast; all receivers matching this Intent will receive the broadcast. |
| `user` | [UserHandle](../android/os/UserHandle.md)!: UserHandle to send the intent to. |
| `resultReceiver` | [BroadcastReceiver](../android/content/BroadcastReceiver.md)?: This value may be `null`. |
| --- | --- |
| `scheduler` | [Handler](../android/os/Handler.md)?: This value may be `null`. |
| `initialCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An initial value for the result code. Often Activity.RESULT_OK. |
| `initialData` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| --- | --- |
| `initialExtras` | [Bundle](../android/os/Bundle.md)?: This value may be `null`. |

### setTheme

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTheme(resid: Int): Unit
```

Set the base theme for this context. Note that this should be called before any views are instantiated in the Context (for example before calling android.app.Activity#setContentView or android.view.LayoutInflater#inflate).

| Parameters ||
|---|---|
| `resid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The style resource describing the theme. |

### setWallpaper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWallpaper(bitmap: Bitmap!): Unit
```

**Deprecated:** *Deprecated in Java.*

### setWallpaper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWallpaper(data: InputStream!): Unit
```

**Deprecated:** *Deprecated in Java.*

### shouldShowRequestPermissionRationale

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun shouldShowRequestPermissionRationale(permission: String): Boolean
```

Gets whether you should show UI with rationale before requesting a permission. If the permission does not exist on this SDK level or is not visible to this app, the method will return `false`.

| Parameters ||
|---|---|
| `permission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether you should show permission rationale UI. |

### startActivities

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startActivities(intents: Array<Intent!>!): Unit
```

Same as `https://developer.android.com/reference/kotlin/android/content/Context#startActivities(kotlin.Array,%20android.os.Bundle)` with no options specified.

| Parameters ||
|---|---|
| `intents` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Intent](../android/content/Intent.md)!\>!: An array of Intents to be started. |

| Exceptions ||
|---|---|
| `android.content.ActivityNotFoundException` | |

### startActivities

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startActivities(
    intents: Array<Intent!>!, 
    options: Bundle?
): Unit
```

Launch multiple new activities. This is generally the same as calling `https://developer.android.com/reference/kotlin/android/content/Context#startActivity(android.content.Intent)` for the first Intent in the array, that activity during its creation calling `https://developer.android.com/reference/kotlin/android/content/Context#startActivity(android.content.Intent)` for the second entry, etc. Note that unlike that approach, generally none of the activities except the last in the array will be created at this point, but rather will be created when the user first visits them (due to pressing back from the activity on top).

This method throws `https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException` if there was no Activity found for *any* given Intent. In this case the state of the activity stack is undefined (some Intents in the list may be on it, some not), so you probably want to avoid such situations.

| Parameters ||
|---|---|
| `intents` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Intent](../android/content/Intent.md)!\>!: An array of Intents to be started. |
| `options` | [Bundle](../android/os/Bundle.md)?: This value may be `null`. |

| Exceptions ||
|---|---|
| `android.content.ActivityNotFoundException` | |

### startActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startActivity(intent: Intent!): Unit
```

Same as `https://developer.android.com/reference/kotlin/android/content/Context#startActivity(android.content.Intent,%20android.os.Bundle)` with no options specified.

| Parameters ||
|---|---|
| `intent` | [Intent](../android/content/Intent.md)!: The description of the activity to start. |

| Exceptions ||
|---|---|
| `android.content.ActivityNotFoundException` | \` |

### startActivity

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startActivity(
    intent: Intent!, 
    options: Bundle?
): Unit
```

Launch a new activity. You will not receive any information about when the activity exits.

Note that if this method is being called from outside of an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` Context, then the Intent must include the `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_NEW_TASK:kotlin.Int` launch flag. This is because, without being started from an existing Activity, there is no existing task in which to place the new activity and thus it needs to be placed in its own separate task.

This method throws `https://developer.android.com/reference/kotlin/android/content/ActivityNotFoundException` if there was no Activity found to run the given Intent.

| Parameters ||
|---|---|
| `intent` | [Intent](../android/content/Intent.md)!: The description of the activity to start. |
| `options` | [Bundle](../android/os/Bundle.md)?: This value may be `null`. |

| Exceptions ||
|---|---|
| `android.content.ActivityNotFoundException` | |

### startForegroundService

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startForegroundService(service: Intent!): ComponentName?
```

Similar to `https://developer.android.com/reference/kotlin/android/content/Context#startService(android.content.Intent)`, but with an implicit promise that the Service will call `https://developer.android.com/reference/kotlin/android/app/Service.html#startForeground(kotlin.Int,%20android.app.Notification)` once it begins running. The service is given an amount of time comparable to the ANR interval to do this, otherwise the system will automatically crash the process, in which case an internal exception `ForegroundServiceDidNotStartInTimeException` is logged on logcat on devices running SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or later. On older Android versions, an internal exception `RemoteServiceException` is logged instead, with a corresponding message.

Unlike the ordinary `https://developer.android.com/reference/kotlin/android/content/Context#startService(android.content.Intent)`, this method can be used at any time, regardless of whether the app hosting the service is in a foreground state.

**Note:** Beginning with SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, apps targeting SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or higher are not allowed to start foreground services from the background. See [Behavior changes: Apps targeting Android 12](../about/versions/12/behavior-changes-12.md) for more details.

<br />

| Parameters ||
|---|---|
| `service` | [Intent](../android/content/Intent.md)!: Identifies the service to be started. The Intent must be fully explicit (supplying a component name). Additional values may be included in the Intent extras to supply arguments along with this specific start call. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/ComponentName?` | This value may be `null`. |

| Exceptions ||
|---|---|
| `android.app.ForegroundServiceStartNotAllowedException` | If the caller app's targeting API is `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or later, and the foreground service is restricted from start due to background restriction. |
| `java.lang.SecurityException` | If the caller does not have permission to access the service or the service can not be found. |

### startInstrumentation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startInstrumentation(
    className: ComponentName, 
    profileFile: String?, 
    arguments: Bundle?
): Boolean
```

Start executing an `https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#` class. The given Instrumentation component will be run by killing its target application (if currently running), starting the target process, instantiating the instrumentation component, and then letting it drive the application.

This function is not synchronous -- it returns as soon as the instrumentation has started and while it is running.

Instrumentation is normally only allowed to run against a package that is either unsigned or signed with a signature that the the instrumentation package is also signed with (ensuring the target trusts the instrumentation).

| Parameters ||
|---|---|
| `className` | [ComponentName](../android/content/ComponentName.md): Name of the Instrumentation component to be run. This value cannot be `null`. |
| `profileFile` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `arguments` | [Bundle](../android/os/Bundle.md)?: This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the instrumentation was successfully started, else `false` if it could not be found. |

### startIntentSender

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startIntentSender(
    intent: IntentSender!, 
    fillInIntent: Intent?, 
    flagsMask: Int, 
    flagsValues: Int, 
    extraFlags: Int
): Unit
```

Same as `https://developer.android.com/reference/kotlin/android/content/Context#startIntentSender(android.content.IntentSender,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)` with no options specified.

| Parameters ||
|---|---|
| `intent` | [IntentSender](../android/content/IntentSender.md)!: The IntentSender to launch. |
| `fillInIntent` | [Intent](../android/content/Intent.md)?: This value may be `null`. |
| `flagsMask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Intent flags in the original IntentSender that you would like to change. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_FROM_BACKGROUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_DEBUG_LOG_RESOLUTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_EXCLUDE_STOPPED_PACKAGES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_INCLUDE_STOPPED_PACKAGES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_MATCH_EXTERNAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_NO_HISTORY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_SINGLE_TOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_NEW_TASK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_MULTIPLE_TASK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_CLEAR_TOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_FORWARD_RESULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_PREVIOUS_IS_TOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_EXCLUDE_FROM_RECENTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_BROUGHT_TO_FRONT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_RESET_TASK_IF_NEEDED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_LAUNCHED_FROM_HISTORY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_CLEAR_WHEN_TASK_RESET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_NEW_DOCUMENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_CLEAR_WHEN_TASK_RESET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_NO_USER_ACTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_REORDER_TO_FRONT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_NO_ANIMATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_CLEAR_TASK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_TASK_ON_HOME:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_RETAIN_IN_RECENTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_LAUNCH_ADJACENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_RECEIVER_REGISTERED_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_RECEIVER_REPLACE_PENDING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_RECEIVER_FOREGROUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_RECEIVER_NO_ABORT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_RECEIVER_VISIBLE_TO_INSTANT_APPS:kotlin.Int` |
| --- | --- |
| `flagsValues` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Desired values for any bits set in flagsMask. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_FROM_BACKGROUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_DEBUG_LOG_RESOLUTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_EXCLUDE_STOPPED_PACKAGES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_INCLUDE_STOPPED_PACKAGES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_MATCH_EXTERNAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_NO_HISTORY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_SINGLE_TOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_NEW_TASK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_MULTIPLE_TASK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_CLEAR_TOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_FORWARD_RESULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_PREVIOUS_IS_TOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_EXCLUDE_FROM_RECENTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_BROUGHT_TO_FRONT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_RESET_TASK_IF_NEEDED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_LAUNCHED_FROM_HISTORY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_CLEAR_WHEN_TASK_RESET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_NEW_DOCUMENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_CLEAR_WHEN_TASK_RESET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_NO_USER_ACTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_REORDER_TO_FRONT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_NO_ANIMATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_CLEAR_TASK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_TASK_ON_HOME:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_RETAIN_IN_RECENTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_LAUNCH_ADJACENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_RECEIVER_REGISTERED_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_RECEIVER_REPLACE_PENDING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_RECEIVER_FOREGROUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_RECEIVER_NO_ABORT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_RECEIVER_VISIBLE_TO_INSTANT_APPS:kotlin.Int` |
| `extraFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Always set to 0. |

### startIntentSender

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startIntentSender(
    intent: IntentSender!, 
    fillInIntent: Intent?, 
    flagsMask: Int, 
    flagsValues: Int, 
    extraFlags: Int, 
    options: Bundle?
): Unit
```

Like `https://developer.android.com/reference/kotlin/android/content/Context#startActivity(android.content.Intent,%20android.os.Bundle)`, but taking a IntentSender to start. If the IntentSender is for an activity, that activity will be started as if you had called the regular `https://developer.android.com/reference/kotlin/android/content/Context#startActivity(android.content.Intent)` here; otherwise, its associated action will be executed (such as sending a broadcast) as if you had called android.content.IntentSender#sendIntent on it.

| Parameters ||
|---|---|
| `intent` | [IntentSender](../android/content/IntentSender.md)!: The IntentSender to launch. |
| `fillInIntent` | [Intent](../android/content/Intent.md)?: This value may be `null`. |
| `flagsMask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Intent flags in the original IntentSender that you would like to change. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_FROM_BACKGROUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_DEBUG_LOG_RESOLUTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_EXCLUDE_STOPPED_PACKAGES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_INCLUDE_STOPPED_PACKAGES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_MATCH_EXTERNAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_NO_HISTORY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_SINGLE_TOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_NEW_TASK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_MULTIPLE_TASK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_CLEAR_TOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_FORWARD_RESULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_PREVIOUS_IS_TOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_EXCLUDE_FROM_RECENTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_BROUGHT_TO_FRONT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_RESET_TASK_IF_NEEDED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_LAUNCHED_FROM_HISTORY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_CLEAR_WHEN_TASK_RESET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_NEW_DOCUMENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_CLEAR_WHEN_TASK_RESET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_NO_USER_ACTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_REORDER_TO_FRONT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_NO_ANIMATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_CLEAR_TASK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_TASK_ON_HOME:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_RETAIN_IN_RECENTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_LAUNCH_ADJACENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_RECEIVER_REGISTERED_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_RECEIVER_REPLACE_PENDING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_RECEIVER_FOREGROUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_RECEIVER_NO_ABORT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_RECEIVER_VISIBLE_TO_INSTANT_APPS:kotlin.Int` |
| --- | --- |
| `flagsValues` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Desired values for any bits set in flagsMask. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_FROM_BACKGROUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_DEBUG_LOG_RESOLUTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_EXCLUDE_STOPPED_PACKAGES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_INCLUDE_STOPPED_PACKAGES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_MATCH_EXTERNAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_NO_HISTORY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_SINGLE_TOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_NEW_TASK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_MULTIPLE_TASK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_CLEAR_TOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_FORWARD_RESULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_PREVIOUS_IS_TOP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_EXCLUDE_FROM_RECENTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_BROUGHT_TO_FRONT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_RESET_TASK_IF_NEEDED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_LAUNCHED_FROM_HISTORY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_CLEAR_WHEN_TASK_RESET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_NEW_DOCUMENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_CLEAR_WHEN_TASK_RESET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_NO_USER_ACTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_REORDER_TO_FRONT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_NO_ANIMATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_CLEAR_TASK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_TASK_ON_HOME:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_RETAIN_IN_RECENTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_ACTIVITY_LAUNCH_ADJACENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_RECEIVER_REGISTERED_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_RECEIVER_REPLACE_PENDING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_RECEIVER_FOREGROUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_RECEIVER_NO_ABORT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent#FLAG_RECEIVER_VISIBLE_TO_INSTANT_APPS:kotlin.Int` |
| `extraFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Always set to 0. |
| `options` | [Bundle](../android/os/Bundle.md)?: This value may be `null`. |
| --- | --- |

### startService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startService(service: Intent!): ComponentName?
```

Request that a given application service be started. The Intent should either contain the complete class name of a specific service implementation to start, or a specific package name to target. If the Intent is less specified, it logs a warning about this. In this case any of the multiple matching services may be used. If this service is not already running, it will be instantiated and started (creating a process for it if needed); if it is running then it remains running.

Every call to this method will result in a corresponding call to the target service's `https://developer.android.com/reference/kotlin/android/app/Service.html#onStartCommand(android.content.Intent,%20kotlin.Int,%20kotlin.Int)` method, with the intent given here. This provides a convenient way to submit jobs to a service without having to bind and call on to its interface.

Using startService() overrides the default service lifetime that is managed by #bindService: it requires the service to remain running until `https://developer.android.com/reference/kotlin/android/content/Context#stopService(android.content.Intent)` is called, regardless of whether any clients are connected to it. Note that calls to startService() do not nest: no matter how many times you call startService(), a single call to `https://developer.android.com/reference/kotlin/android/content/Context#stopService(android.content.Intent)` will stop it.

The system attempts to keep running services around as much as possible. The only time they should be stopped is if the current foreground application is using so many resources that the service needs to be killed. If any errors happen in the service's process, it will automatically be restarted.

This function will throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` if you do not have permission to start the given service.

**Note:** Each call to startService() results in significant work done by the system to manage service lifecycle surrounding the processing of the intent, which can take multiple milliseconds of CPU time. Due to this cost, startService() should not be used for frequent intent delivery to a service, and only for scheduling significant work. Use #bindService for high frequency calls.
Beginning with SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int`, apps targeting SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` or higher are not allowed to start background services from the background. See [Background Execution Limits](../about/versions/oreo/background.md) for more details.

**Note:** Beginning with SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, apps targeting SDK Version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or higher are not allowed to start foreground services from the background. See [Behavior changes: Apps targeting Android 12](../about/versions/12/behavior-changes-12.md) for more details.

<br />

| Parameters ||
|---|---|
| `service` | [Intent](../android/content/Intent.md)!: Identifies the service to be started. The Intent must be fully explicit (supplying a component name). Additional values may be included in the Intent extras to supply arguments along with this specific start call. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/ComponentName?` | This value may be `null`. |

| Exceptions ||
|---|---|
| `android.app.BackgroundServiceStartNotAllowedException` | On Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` and later, if the application is in a state where the service can not be started (such as not in the foreground in a state when services are allowed), `https://developer.android.com/reference/kotlin/android/app/BackgroundServiceStartNotAllowedException.html#` is thrown. This exception extends `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`, so apps can use `catch (IllegalStateException)` to catch both. |
| `java.lang.IllegalStateException` | Before Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, if the application is in a state where the service can not be started (such as not in the foreground in a state when services are allowed), `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` was thrown. |
| `java.lang.SecurityException` | If the caller does not have permission to access the service or the service can not be found. |
| --- | --- |

### stopService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun stopService(name: Intent!): Boolean
```

Request that a given application service be stopped. If the service is not running, nothing happens. Otherwise it is stopped. Note that calls to startService() are not counted -- this stops the service no matter how many times it was started.

If the service is running as a foreground service when it is stopped, its associated notification will be removed. To avoid this, apps can use `https://developer.android.com/reference/kotlin/android/app/Service.html#stopForeground(kotlin.Int)` to decouple the notification from the service's lifecycle before stopping it.

Note that if a stopped service still has `https://developer.android.com/reference/kotlin/android/content/ServiceConnection` objects bound to it with the `https://developer.android.com/reference/kotlin/android/content/Context#BIND_AUTO_CREATE:kotlin.Int` set, it will not be destroyed until all of these bindings are removed. See the `https://developer.android.com/reference/kotlin/android/app/Service.html#` documentation for more details on a service's lifecycle.

This function will throw `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` if you do not have permission to stop the given service.

| Parameters ||
|---|---|
| `service` | Description of the service to be stopped. The Intent must be either fully explicit (supplying a component name) or specify a specific package name it is targeted to. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | If there is a service matching the given Intent that is already running, then it is stopped and `true` is returned; else `false` is returned. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If the application is in a state where the service can not be started (such as not in the foreground in a state when services are allowed). |
| `java.lang.SecurityException` | If the caller does not have permission to access the service or the service can not be found. |

### unbindService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unbindService(conn: ServiceConnection): Unit
```

Disconnect from an application service. You will no longer receive calls as the service is restarted, and the service is now allowed to stop at any time.

| Parameters ||
|---|---|
| `conn` | [ServiceConnection](../android/content/ServiceConnection.md): The connection interface previously supplied to bindService(). This parameter must not be null. |

### unregisterComponentCallbacks

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterComponentCallbacks(callback: ComponentCallbacks!): Unit
```

Remove a `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks` object that was previously registered with `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#registerComponentCallbacks(android.content.ComponentCallbacks)`.

After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, the `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks` will be unregistered to `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#getBaseContext()`, and can be only used after `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#attachBaseContext(android.content.Context)`

| Parameters ||
|---|---|
| `callback` | [ComponentCallbacks](../android/content/ComponentCallbacks.md)!: The interface to call. This can be either a `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks` or `https://developer.android.com/reference/kotlin/android/content/ComponentCallbacks2` interface. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this method calls before `https://developer.android.com/reference/kotlin/android/content/ContextWrapper#attachBaseContext(android.content.Context)` |

### unregisterDeviceIdChangeListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterDeviceIdChangeListener(listener: IntConsumer): Unit
```

Removes a device ID changed listener from the Context. It's a no-op if the listener is not already registered.

| Parameters ||
|---|---|
| `listener` | [IntConsumer](../java/util/function/IntConsumer.md): This value cannot be `null`. |

### unregisterReceiver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterReceiver(receiver: BroadcastReceiver!): Unit
```

Unregister a previously registered BroadcastReceiver. *All* filters that have been registered for this BroadcastReceiver will be removed.

| Parameters ||
|---|---|
| `receiver` | [BroadcastReceiver](../android/content/BroadcastReceiver.md)!: The BroadcastReceiver to unregister. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the `receiver` was not previously registered or already unregistered. |

### updateServiceBindings

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateServiceBindings(params: MutableCollection<Context.UpdateBindingParams!>): Unit
```

Perform a batch update of existing bindings. Existing bindings can be rebound with an updated set of flags, or unbound. Only flags returned from `https://developer.android.com/reference/kotlin/android/content/Context#getUpdateableFlags()` may be added or removed.

This API behaves as if the `https://developer.android.com/reference/kotlin/android/content/Context#rebindService(android.content.ServiceConnection,%20android.content.Context.BindServiceFlags)` and `https://developer.android.com/reference/kotlin/android/content/Context#unbindService(android.content.ServiceConnection)` API are called in the same order as the params are iterated.

| Parameters ||
|---|---|
| `params` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Context.UpdateBindingParams](../android/content/Context.UpdateBindingParams.md)!\>: This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | Any invalid additions or removals will trigger an exception. |

### updateServiceGroup

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateServiceGroup(
    conn: ServiceConnection, 
    group: Int, 
    importance: Int
): Unit
```

For a service previously bound with #bindService or a related method, change how the system manages that service's process in relation to other processes. This doesn't modify the original bind flags that were passed in when binding, but adjusts how the process will be managed in some cases based on those flags. Currently only works on isolated processes (will be ignored for non-isolated processes).

Note that this call does not take immediate effect, but will be applied the next time the impacted process is adjusted for some other reason. Typically you would call this before then calling a new #bindIsolatedService on the service of interest, with that binding causing the process to be shuffled accordingly.

| Parameters ||
|---|---|
| `conn` | [ServiceConnection](../android/content/ServiceConnection.md): The connection interface previously supplied to bindService(). This parameter must not be null. |
| `group` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A group to put this connection's process in. Upon calling here, this will override any previous group that was set for that process. The group tells the system about processes that are logically grouped together, so should be managed as one unit of importance (such as when being considered a recently used app). All processes in the same app with the same group are considered to be related. Supplying 0 reverts to the default behavior of not grouping. |
| `importance` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional importance of the processes within a group. Upon calling here, this will override any previous importance that was set for that process. The most important process is 0, and higher values are successively less important. You can view this as describing how to order the processes in an array, with the processes at the end of the array being the least important. This value has no meaning besides indicating how processes should be ordered in that array one after the other. This provides a way to fine-tune the system's process killing, guiding it to kill processes at the end of the array first. |
| --- | --- |

## Protected methods

### attachBaseContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun attachBaseContext(base: Context!): Unit
```

Set the base context for this ContextWrapper. All calls will then be delegated to the base context. Throws IllegalStateException if a base context has already been set.

| Parameters ||
|---|---|
| `base` | [Context](../android/content/Context.md)!: The new base context for this wrapper. |
