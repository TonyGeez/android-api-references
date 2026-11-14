Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Parcelable

```
interface Parcelable
```

| [android.os.Parcelable](Parcelable.md) |

Known Direct Subclasses [AbsSavedState](../android.view/AbsSavedState.md), [AccessibilityEvent](../android.view.accessibility/AccessibilityEvent.md), [AccessibilityGestureEvent](../android.accessibilityservice/AccessibilityGestureEvent.md), [AccessibilityNodeInfo](../android.view.accessibility/AccessibilityNodeInfo.md), [AccessibilityNodeInfo.AccessibilityAction](../android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction.md), [AccessibilityNodeInfo.ExtraRenderingInfo](../android/view/accessibility/AccessibilityNodeInfo.ExtraRenderingInfo.md), [AccessibilityNodeInfo.MathInfo](../android/view/accessibility/AccessibilityNodeInfo.MathInfo.md), [AccessibilityNodeInfo.Selection](../android/view/accessibility/AccessibilityNodeInfo.Selection.md), [AccessibilityNodeInfo.SelectionPosition](../android/view/accessibility/AccessibilityNodeInfo.SelectionPosition.md), [AccessibilityNodeInfo.TouchDelegateInfo](../android/view/accessibility/AccessibilityNodeInfo.TouchDelegateInfo.md), [AccessibilityServiceInfo](../android.accessibilityservice/AccessibilityServiceInfo.md), [AccessibilityWindowInfo](../android.view.accessibility/AccessibilityWindowInfo.md), and 873 others. [AbsSavedState](../android.view/AbsSavedState.md) A Parcelable implementation that should be used by inheritance hierarchies to ensure the state of all classes along the chain is saved.
[AccessibilityEvent](../android.view.accessibility/AccessibilityEvent.md) This class represents accessibility events that are sent by the system when something notable happens in the user interface.
[AccessibilityGestureEvent](../android.accessibilityservice/AccessibilityGestureEvent.md) This class describes the gesture event including gesture id and which display it happens on.
[AccessibilityNodeInfo](../android.view.accessibility/AccessibilityNodeInfo.md) This class represents a node of the window content as well as actions that can be requested from its source.
[AccessibilityNodeInfo.AccessibilityAction](../android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction.md) A class defining an action that can be performed on an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.html#`.
[AccessibilityNodeInfo.ExtraRenderingInfo](../android/view/accessibility/AccessibilityNodeInfo.ExtraRenderingInfo.md) Class with information of a view useful to evaluate accessibility needs.
[AccessibilityNodeInfo.MathInfo](../android/view/accessibility/AccessibilityNodeInfo.MathInfo.md) A class that holds information about a node that represents a mathematical expression.
[AccessibilityNodeInfo.Selection](../android/view/accessibility/AccessibilityNodeInfo.Selection.md) Represents a selection of content that may extend across more than one `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.html#` instance.
[AccessibilityNodeInfo.SelectionPosition](../android/view/accessibility/AccessibilityNodeInfo.SelectionPosition.md) A class which defines either the start or end of a selection that can span across multiple AccessibilityNodeInfo objects.
[AccessibilityNodeInfo.TouchDelegateInfo](../android/view/accessibility/AccessibilityNodeInfo.TouchDelegateInfo.md) Class with information of touch delegated views and regions from `https://developer.android.com/reference/kotlin/android/view/TouchDelegate.html#` for the `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.html#`.
[AccessibilityServiceInfo](../android.accessibilityservice/AccessibilityServiceInfo.md) This class describes an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`.
[AccessibilityWindowInfo](../android.view.accessibility/AccessibilityWindowInfo.md) This class represents a state snapshot of a window for accessibility purposes.
[Account](../android.accounts/Account.md) Value type that represents an Account in the `https://developer.android.com/reference/kotlin/android/accounts/AccountManager.html#`.
[AccountAuthenticatorResponse](../android.accounts/AccountAuthenticatorResponse.md) Object used to communicate responses back to the AccountManager
[Action](../android.service.credentials/Action.md) An action defined by the provider that intents into the provider's app for specific user actions.
[ActionRequest](../android/companion/ActionRequest.md) Represents a request for a companion app to perform a specific action.
[ActionResult](../android.companion/ActionResult.md) A result reported by a companion app in response to an `https://developer.android.com/reference/kotlin/android/companion/ActionRequest.html#`.
[ActiveProcessingPicture](../android.media.quality/ActiveProcessingPicture.md) Active picture represents an image or video undergoing picture processing which uses a picture profile.
[ActivityInfo](../android.content.pm/ActivityInfo.md) Information you can retrieve about a particular application activity or receiver.
[ActivityManager.MemoryInfo](../android/app/ActivityManager.MemoryInfo.md) Information you can retrieve about the available memory through getMemoryInfo.
[ActivityManager.ProcessErrorStateInfo](../android/app/ActivityManager.ProcessErrorStateInfo.md) Information you can retrieve about any processes that are in an error condition.
[ActivityManager.RecentTaskInfo](../android/app/ActivityManager.RecentTaskInfo.md) Information you can retrieve about tasks that the user has most recently started or visited.
[ActivityManager.RunningAppProcessInfo](../android/app/ActivityManager.RunningAppProcessInfo.md) Information you can retrieve about a running process.
[ActivityManager.RunningServiceInfo](../android/app/ActivityManager.RunningServiceInfo.md) Information you can retrieve about a particular Service that is currently running in the system.
[ActivityManager.RunningTaskInfo](../android/app/ActivityManager.RunningTaskInfo.md) Information you can retrieve about a particular task that is currently "running" in the system.
[ActivityManager.TaskDescription](../android/app/ActivityManager.TaskDescription.md) Information you can set and retrieve about the current activity within the recent task list.
[ActivityOptions.LaunchCookie](../android/app/ActivityOptions.LaunchCookie.md) An opaque token used to track and identify a specific activity launch request.
[AdBuffer](../android.media.tv/AdBuffer.md) Buffer for advertisement data.
[AdData](../android.adservices.common/AdData.md) Represents data specific to an ad that is necessary for ad selection and rendering.
[AdFilters](../android.adservices.common/AdFilters.md) A container class for filters which are associated with an ad.
[AdRequest](../android.media.tv/AdRequest.md) An advertisement request which can be sent to TV input to request AD operations.
[AdResponse](../android.media.tv/AdResponse.md) An advertisement response which can be sent to TV interactive App service to inform AD status.
[AdSelectionConfig](../android.adservices.adselection/AdSelectionConfig.md) Contains the configuration of the ad selection process.
[AdSelectionFromOutcomesConfig](../android.adservices.adselection/AdSelectionFromOutcomesConfig.md) Contains the configuration of the ad selection process that select a winner from a given list of ad selection ids.
[AdSelectionSignals](../android.adservices.common/AdSelectionSignals.md) This class holds JSON that will be passed into a JavaScript function during ad selection.
[AdTechIdentifier](../android.adservices.common/AdTechIdentifier.md) An Identifier representing an ad buyer or seller.
[AdWithBid](../android.adservices.adselection/AdWithBid.md) Represents an ad and its corresponding bid value after the bid generation step in the ad selection process.
[Address](../android.location/Address.md) A class representing an Address, that is, a set of Strings describing a location.
[AdvertiseData](../android.bluetooth.le/AdvertiseData.md) Advertise data packet container for Bluetooth LE advertising.
[AdvertiseSettings](../android.bluetooth.le/AdvertiseSettings.md) The `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseSettings.html#` provide a way to adjust advertising preferences for each Bluetooth LE advertisement instance.
[AdvertisingRequest](../android.net.nsd/AdvertisingRequest.md) Encapsulates parameters for android.
[AdvertisingSetParameters](../android.bluetooth.le/AdvertisingSetParameters.md) The `https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters.html#` provide a way to adjust advertising preferences for each Bluetooth LE advertising set.
[AitInfo](../android.media.tv/AitInfo.md) AIT (Application Information Table) info.
[AlarmManager.AlarmClockInfo](../android/app/AlarmManager.AlarmClockInfo.md) An immutable description of a scheduled "alarm clock" event.
[AlternativeSpan](../android.speech/AlternativeSpan.md) List of alternative hypotheses for a specific span of a speech recognition result string.
[AlternativeSpans](../android.speech/AlternativeSpans.md) List of `https://developer.android.com/reference/kotlin/android/speech/AlternativeSpan.html#` for a specific speech recognition result.
[AmbientBacklightEvent](../android.media.quality/AmbientBacklightEvent.md) Ambient backlight event
[AmbientBacklightMetadata](../android.media.quality/AmbientBacklightMetadata.md) Metadata of ambient backlight.
[AmbientBacklightSettings](../android.media.quality/AmbientBacklightSettings.md) Settings to configure ambient backlight hardware.
[AnrWarningResult](../android.app/AnrWarningResult.md) Describes the information about a potential ANR before the timeout is reached.
[ApkChecksum](../android.content.pm/ApkChecksum.md) A typed checksum of an APK.
[ApnSetting](../android.telephony.data/ApnSetting.md) An Access Point Name (APN) configuration for a carrier data connection.
[AppFunctionActivityId](../android/app/appfunctions/AppFunctionActivityId.md) An identifier of an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` an app function can be associated with.
[AppFunctionActivityState](../android.app.appfunctions/AppFunctionActivityState.md) The state of an activity from the perspective of app functions, retrieved using getAppFunctionActivityStates.
[AppFunctionException](../android.app.appfunctions/AppFunctionException.md) App function related error.
[AppFunctionMetadata](../android.app.appfunctions/AppFunctionMetadata.md) Contains an app function's metadata, essential for its invocation and discovery, retrieved using searchAppFunctions.
[AppFunctionName](../android/app/appfunctions/AppFunctionName.md) Globally unique identifier for an app function.
[AppFunctionPackageMetadata](../android/app/appfunctions/AppFunctionPackageMetadata.md) Contains metadata about a package providing app functions.
[AppFunctionSchemaMetadata](../android.app.appfunctions/AppFunctionSchemaMetadata.md) Contains identifying metadata for a predefined schema, which can describe well-known function signatures.
[AppFunctionSearchSpec](../android.app.appfunctions/AppFunctionSearchSpec.md) Filter criteria for searchAppFunctions.
[AppFunctionState](../android/app/appfunctions/AppFunctionState.md) Runtime state of an app function, retrieved using getAppFunctionStates.
[AppFunctionUriGrant](../android.app.appfunctions/AppFunctionUriGrant.md) `https://developer.android.com/reference/kotlin/android/net/Uri.html#` for which access permission is to be granted to the caller of android.
[AppInfo](../android.adservices.ondevicepersonalization/AppInfo.md) Information about apps.
[AppInstallFilters](../android.adservices.common/AppInstallFilters.md) A container for the ad filters that are based on app install state.
[AppInteractionAttribution](../android/app/AppInteractionAttribution.md) Represents attribution information for an app interaction, detailing the context and nature of the interaction that triggered it.
[AppLinkInfo](../android.media.tv.interactive/AppLinkInfo.md) App link information used by TV interactive app to launch Android apps.
[AppOwnedSdkSandboxInterface](../android.app.sdksandbox/AppOwnedSdkSandboxInterface.md) Represents a channel for an SDK in the sandbox process to interact with the app.
[AppSearchBlobHandle](../android.app.appsearch/AppSearchBlobHandle.md) An identifier to represent a blob in AppSearch.
[AppSearchSchema](../android.app.appsearch/AppSearchSchema.md) The AppSearch Schema for a particular type of document.
[AppUriAuthenticationPolicy](../android.security/AppUriAuthenticationPolicy.md) The app-URI authentication policy is set by the credential management app.
[AppUsageDuration](../android/app/usage/AppUsageDuration.md) Contains usage statistics for a single app package.
[AppUsageDurationQuery](../android/app/usage/AppUsageDurationQuery.md) Represents a query for application usage duration statistics.
[AppWidgetEvent](../android.appwidget/AppWidgetEvent.md) An immutable class that describes the event data for an app widget interaction event.
[AppWidgetProviderInfo](../android.appwidget/AppWidgetProviderInfo.md) Describes the meta data for an installed AppWidget provider.
[ApplicationErrorReport](../android.app/ApplicationErrorReport.md) Describes an application error.
[ApplicationExitInfo](../android.app/ApplicationExitInfo.md) Describes the information of an application process's death.
[ApplicationExitInfo.AnrInfo](../android/app/ApplicationExitInfo.AnrInfo.md) <br />

[ApplicationInfo](../android.content.pm/ApplicationInfo.md) Information you can retrieve about a particular application.
[ApplicationMediaCapabilities](../android.media/ApplicationMediaCapabilities.md) ApplicationMediaCapabilities is an immutable class that encapsulates an application's capabilities for handling newer video codec format and media features.
[ApplicationStartInfo](../android.app/ApplicationStartInfo.md) Describes information related to an application process's startup.
[AssetFileDescriptor](../android.content.res/AssetFileDescriptor.md) File descriptor of an entry in the AssetManager.
[AssistContent](../android.app.assist/AssistContent.md) Holds information about the content an application is viewing, to hand to an assistant at the user's request.
[AssistStructure](../android.app.assist/AssistStructure.md) This API automatically creates assist data from the platform's implementation of assist and autofill.
[AssistantQueryRequest](../android.app.privatecompute/AssistantQueryRequest.md) Request object specifically for Assistant Query Egress operations.
[AssistantQueryRequest.Query](../android/app/privatecompute/AssistantQueryRequest.Query.md) Payload containing the raw query details to be routed to the non-PCC assistant process.
[AssistantQueryResponse](../android.app.privatecompute/AssistantQueryResponse.md) Specialized response for Assistant Query use-cases.
[AssociatedDevice](../android.companion/AssociatedDevice.md) Container for device info from an association that is not self-managed.
[AssociationInfo](../android.companion/AssociationInfo.md) Details for a specific "association" that has been established between an app and companion device.
[AssociationRequest](../android.companion/AssociationRequest.md) A request for the user to select a companion device to associate with.
[AsyncNotedAppOp](../android.app/AsyncNotedAppOp.md) When an noteOp and the app the app-op is noted for has a `https://developer.android.com/reference/kotlin/android/app/AppOpsManager.OnOpNotedCallback.html#` registered the note-event needs to be delivered to the callback.
[Attribution](../android.content.pm/Attribution.md) Information about an attribution declared by a package.
[AttributionSource](../android.content/AttributionSource.md) This class represents a source to which access to permission protected data should be attributed.
[AudioAttributes](../android.media/AudioAttributes.md) A class to encapsulate a collection of attributes describing information about an audio stream.
[AudioDescriptor](../android.media/AudioDescriptor.md) The AudioDescriptor contains the information to describe the audio playback/capture capabilities.
[AudioFormat](../android.media/AudioFormat.md) The `https://developer.android.com/reference/kotlin/android/media/AudioFormat.html#` class is used to access a number of audio format and channel configuration constants.
[AudioMixerAttributes](../android.media/AudioMixerAttributes.md) Class to represent the attributes of the audio mixer: its format, which represents by an `https://developer.android.com/reference/kotlin/android/media/AudioFormat.html#` object and mixer behavior.
[AudioPlaybackConfiguration](../android.media/AudioPlaybackConfiguration.md) The AudioPlaybackConfiguration class collects the information describing an audio playback session.
[AudioPresentation](../android.media/AudioPresentation.md) The AudioPresentation class encapsulates the information that describes an audio presentation which is available in next generation audio content.
[AudioProfile](../android.media/AudioProfile.md) An AudioProfile is specific to an audio format and lists supported sampling rates and channel masks for that format.
[AudioRecordingConfiguration](../android.media/AudioRecordingConfiguration.md) The AudioRecordingConfiguration class collects the information describing an audio recording session.
[AudioTimestamp](../android.media/AudioTimestamp.md) Structure that groups a position in frame units relative to an assumed audio stream, together with the estimated time when that frame enters or leaves the audio processing pipeline on that device.
[AuthenticationRequiredException](../android.app/AuthenticationRequiredException.md) Specialization of `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` that is thrown when authentication is needed from the end user before viewing the content.
[AuthenticatorDescription](../android.accounts/AuthenticatorDescription.md) A Parcelable value type that contains information about an account authenticator.
[AutofillId](../android.view.autofill/AutofillId.md) A unique identifier for an autofill node inside an `https://developer.android.com/reference/kotlin/android/app/Activity.html#`.
[AutofillNoiseInjectedData](../android/view/autofill/AutofillNoiseInjectedData.md) Represents the noise-injected version of a text field's content, generated using a differential privacy algorithm.
[AutofillValue](../android.view.autofill/AutofillValue.md) Abstracts how a `https://developer.android.com/reference/kotlin/android/view/View.html#` can be autofilled by an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#`.
[AutomaticZenRule](../android.app/AutomaticZenRule.md) Rule instance information for a zen (aka DND or Attention Management) mode.
[AvailableNetworkInfo](../android.telephony/AvailableNetworkInfo.md) Defines available network information which includes corresponding subscription id, network plmns and corresponding priority to be used for network selection by Opportunistic Network Service when passed through updateAvailableNetworks
[AvailableNfcAntenna](../android.nfc/AvailableNfcAntenna.md) Represents a single available Nfc antenna on an Android device.
[AwareDataPathRequest](../android/net/wifi/aware/AwareDataPathRequest.md) A request to set up a data path for a Wi-Fi Aware network.
[AwarePairingConfig](../android.net.wifi.aware/AwarePairingConfig.md) The config for the Aware Pairing.
[AwareResources](../android.net.wifi.aware/AwareResources.md) The resources of the Aware service.
[BackgroundServiceStartNotAllowedException](../android.app/BackgroundServiceStartNotAllowedException.md) Exception thrown when an app tries to start a background `https://developer.android.com/reference/kotlin/android/app/Service.html#` when it's not allowed to do so.
[BarringInfo](../android.telephony/BarringInfo.md) Provides the barring configuration for a particular service type.
[BarringInfo.BarringServiceInfo](../android/telephony/BarringInfo.BarringServiceInfo.md) Describe the current barring configuration of a cell
[BatchUpdates](../android.service.autofill/BatchUpdates.md) Defines actions to be applied to a `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#`.
[BeginCreateCredentialRequest](../android.service.credentials/BeginCreateCredentialRequest.md) Request for beginning a create credential request.
[BeginCreateCredentialResponse](../android.service.credentials/BeginCreateCredentialResponse.md) Response to a `https://developer.android.com/reference/kotlin/android/service/credentials/BeginCreateCredentialRequest.html#`.
[BeginGetCredentialOption](../android.service.credentials/BeginGetCredentialOption.md) A specific type of credential request to be sent to the provider during the query phase of a get flow.
[BeginGetCredentialRequest](../android.service.credentials/BeginGetCredentialRequest.md) Query stage request for getting user's credentials from a given credential provider.
[BeginGetCredentialResponse](../android.service.credentials/BeginGetCredentialResponse.md) Response from a credential provider, containing credential entries and other associated data to be shown on the account selector UI.
[BiometricPromptStyleSpec](../android.hardware.biometrics/BiometricPromptStyleSpec.md) A class that describes the visual styles of the embedded BiometricPrompt UI to allow client applications to maintain visual consistency.
[Bitmap](../android.graphics/Bitmap.md) <br />

[BleCsRangingCapabilities](../android.ranging.ble.cs/BleCsRangingCapabilities.md) Represents the capabilities of the Bluetooth-based Channel Sounding (CS) ranging.
[BleCsRangingParams](../android.ranging.ble.cs/BleCsRangingParams.md) BleCsRangingParams encapsulates the parameters required for a bluetooth channel sounding ranging session.
[BleRssiRangingParams](../android.ranging.ble.rssi/BleRssiRangingParams.md) BleRssiRangingParams encapsulates the parameters required for a bluetooth rssi based ranging session.
[BleSpecificData](../android.ranging.ble/BleSpecificData.md) Represents the `https://developer.android.com/reference/kotlin/android/ranging/RangingManager.html#BLE_CS:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/ranging/RangingManager.html#BLE_RSSI:kotlin.Int` specific data.
[BlobHandle](../android.app.blob/BlobHandle.md) An identifier to represent a blob.
[BlockingOption](../android.net.wifi/BlockingOption.md) Options for blocking a network through disallowCurrentSuggestedNetwork
[BluetoothClass](../android.bluetooth/BluetoothClass.md) Represents a Bluetooth class, which describes general characteristics and capabilities of a device.
[BluetoothCodecConfig](../android.bluetooth/BluetoothCodecConfig.md) Represents the codec configuration for a Bluetooth A2DP source device.
[BluetoothCodecStatus](../android.bluetooth/BluetoothCodecStatus.md) Represents the codec status (configuration and capability) for a Bluetooth A2DP source device.
[BluetoothCodecType](../android.bluetooth/BluetoothCodecType.md) Represents a supported source codec type for a Bluetooth A2DP device.
[BluetoothDevice](../android.bluetooth/BluetoothDevice.md) Represents a remote Bluetooth device.
[BluetoothDevice.BluetoothAddress](../android/bluetooth/BluetoothDevice.BluetoothAddress.md) A data class for Bluetooth address and address type.
[BluetoothGattCharacteristic](../android.bluetooth/BluetoothGattCharacteristic.md) Represents a Bluetooth GATT Characteristic
[BluetoothGattDescriptor](../android.bluetooth/BluetoothGattDescriptor.md) Represents a Bluetooth GATT Descriptor
[BluetoothGattService](../android.bluetooth/BluetoothGattService.md) Represents a Bluetooth GATT Service
[BluetoothHealthAppConfiguration](../android.bluetooth/BluetoothHealthAppConfiguration.md) The Bluetooth Health Application Configuration that is used in conjunction with the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth.html#` class.
[BluetoothHidDeviceAppQosSettings](../android.bluetooth/BluetoothHidDeviceAppQosSettings.md) Represents the Quality of Service (QoS) settings for a Bluetooth HID Device application.
[BluetoothHidDeviceAppSdpSettings](../android.bluetooth/BluetoothHidDeviceAppSdpSettings.md) Represents the Service Discovery Protocol (SDP) settings for a Bluetooth HID Device application.
[BluetoothLeAudioCodecConfig](../android.bluetooth/BluetoothLeAudioCodecConfig.md) Represents the codec configuration for a Bluetooth LE Audio source device.
[BluetoothLeAudioCodecStatus](../android.bluetooth/BluetoothLeAudioCodecStatus.md) Represents the codec status (configuration and capability) for a Bluetooth Le Audio source device.
[BroadcastInfoRequest](../android.media.tv/BroadcastInfoRequest.md) A request for the information retrieved from broadcast signal.
[BroadcastInfoResponse](../android.media.tv/BroadcastInfoResponse.md) A response of `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest.html#` for information retrieved from broadcast signal.
[Bundle](Bundle.md) A mapping from String keys to various Parcelable values.
[CallAttributes](../android.telecom/CallAttributes.md) CallAttributes represents a set of properties that define a new Call.
[CallAudioState](../android.telecom/CallAudioState.md) Encapsulates the telecom audio state, including the current audio routing, supported audio routing and mute.
[CallEndpoint](../android.telecom/CallEndpoint.md) Encapsulates the endpoint where call media can flow
[CallEndpointException](../android.telecom/CallEndpointException.md) This class represents a set of exceptions that can occur when requesting a `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint.html#` change.
[CallException](../android.telecom/CallException.md) This class defines exceptions that can be thrown when using Telecom APIs with OutcomeReceivers.
[CallingAppInfo](../android.service.credentials/CallingAppInfo.md) Information pertaining to the calling application, including the package name and a list of app signatures.
[Capability](../android.content.pm/Capability.md) Represents a capability that can be performed by an app, also known as App Action.
[CapabilityParams](../android.content.pm/CapabilityParams.md) Represents the parameters and its matching names which can be associated with a `https://developer.android.com/reference/kotlin/android/content/pm/Capability.html#`.
[CaptivePortal](../android.net/CaptivePortal.md) A class allowing apps handling the `https://developer.android.com/reference/kotlin/android/net/ConnectivityManager.html#ACTION_CAPTIVE_PORTAL_SIGN_IN:kotlin.String` activity to indicate to the system different outcomes of captive portal sign in.
[CaptureRequest](../android.hardware.camera2/CaptureRequest.md) An immutable package of settings and outputs needed to capture a single image from the camera device.
[CarrierIdentifier](../android.service.carrier/CarrierIdentifier.md) Used to pass info to CarrierConfigService implementations so they can decide what values to return.
[CellIdentity](../android.telephony/CellIdentity.md) CellIdentity represents the identity of a unique cell.
[CellInfo](../android.telephony/CellInfo.md) Immutable cell information from a point in time.
[CellInfoCdma](../android.telephony/CellInfoCdma.md) A `https://developer.android.com/reference/kotlin/android/telephony/CellInfo.html#` representing a CDMA cell that provides identity and measurement info.
[CellInfoGsm](../android.telephony/CellInfoGsm.md) A `https://developer.android.com/reference/kotlin/android/telephony/CellInfo.html#` representing a GSM cell that provides identity and measurement info.
[CellInfoLte](../android.telephony/CellInfoLte.md) A `https://developer.android.com/reference/kotlin/android/telephony/CellInfo.html#` representing an LTE cell that provides identity and measurement info.
[CellInfoTdscdma](../android.telephony/CellInfoTdscdma.md) A `https://developer.android.com/reference/kotlin/android/telephony/CellInfo.html#` representing a TD-SCDMA cell that provides identity and measurement info.
[CellInfoWcdma](../android.telephony/CellInfoWcdma.md) A `https://developer.android.com/reference/kotlin/android/telephony/CellInfo.html#` representing a WCDMA cell that provides identity and measurement info.
[CellSignalStrengthCdma](../android.telephony/CellSignalStrengthCdma.md) Signal strength related information.
[CellSignalStrengthGsm](../android.telephony/CellSignalStrengthGsm.md) GSM signal strength related information.
[CellSignalStrengthLte](../android.telephony/CellSignalStrengthLte.md) LTE signal strength related information.
[CellSignalStrengthNr](../android.telephony/CellSignalStrengthNr.md) 5G NR signal strength related information.
[CellSignalStrengthTdscdma](../android.telephony/CellSignalStrengthTdscdma.md) Tdscdma signal strength related information.
[CellSignalStrengthWcdma](../android.telephony/CellSignalStrengthWcdma.md) Wcdma signal strength related information.
[ChangeLogTokenRequest](../android.health.connect.changelog/ChangeLogTokenRequest.md) A class to request changelog token using getChangeLogToken
[ChangeLogTokenResponse](../android.health.connect.changelog/ChangeLogTokenResponse.md) Response class for getChangeLogToken}
[ChangeLogsRequest](../android.health.connect.changelog/ChangeLogsRequest.md) Request class for getChangeLogs
[ChangeLogsResponse](../android.health.connect.changelog/ChangeLogsResponse.md) Response class for getChangeLogs This is the response to clients fetching changes.
[ChangedPackages](../android.content.pm/ChangedPackages.md) Packages that have been changed since the last time they were requested.
[CharSequenceTransformation](../android.service.autofill/CharSequenceTransformation.md) Replaces a `https://developer.android.com/reference/kotlin/android/widget/TextView.html#` child of a `https://developer.android.com/reference/kotlin/android/service/autofill/CustomDescription.html#` with the contents of one or more regular expressions (regexs).
[Characteristics](../android.net.wifi.aware/Characteristics.md) The characteristics of the Wi-Fi Aware implementation.
[Checksum](../android.content.pm/Checksum.md) A typed checksum.
[ChooserAction](../android.service.chooser/ChooserAction.md) A ChooserAction is an app-defined action that can be provided to the Android Sharesheet to be shown to the user when `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CHOOSER:kotlin.String` is invoked.
[ChooserResult](../android.service.chooser/ChooserResult.md) An event reported to a supplied \[IntentSender\] by the system chooser when an activity is selected or other actions are taken to complete the session.
[ChooserSessionToken](../android.service.chooser/ChooserSessionToken.md) An opaque token that serves as a Chooser session identifier.
[ChooserTarget](../android.service.chooser/ChooserTarget.md) A ChooserTarget represents a deep-link into an application as returned by a `https://developer.android.com/reference/kotlin/android/service/chooser/ChooserTargetService.html#`.
[ClassifiableContent](../android.app.contentsafety/ClassifiableContent.md) A class representing content to be classified.
[ClearCredentialStateRequest](../android.service.credentials/ClearCredentialStateRequest.md) A request class for clearing a user's credential state.
[ClearCredentialStateRequest](../android.credentials/ClearCredentialStateRequest.md) A request class for clearing a user's credential state from the credential providers.
[ClipData](../android.content/ClipData.md) Representation of a clipped data on the clipboard.
[ClipDescription](../android.content/ClipDescription.md) Meta-data describing the contents of a `https://developer.android.com/reference/kotlin/android/content/ClipData.html#`.
[ClosedSubscriberGroupInfo](../android.telephony/ClosedSubscriberGroupInfo.md) Information to represent a closed subscriber group.
[CloudMediaProviderContract.Capabilities](../android/provider/CloudMediaProviderContract.Capabilities.md) Information about what capabilities a CloudMediaProvider can support.
[ColorSequence](../android/hardware/lights/ColorSequence.md) Models a sequence of colors and their relative timing to create a light effect.
[ColorStateList](../android.content.res/ColorStateList.md) Lets you map `https://developer.android.com/reference/kotlin/android/view/View.html#` state sets to colors.
[CombinedVibration](CombinedVibration.md) A CombinedVibration describes a combination of haptic effects to be performed by one or more Vibrator.
[CommandRequest](../android.media.tv/CommandRequest.md) A request for command from broadcast signal.
[CommandResponse](../android.media.tv/CommandResponse.md) A response for command from broadcast signal.
[CommitBlobResponse](../android.app.appsearch/CommitBlobResponse.md) The response to provide batch operation results of commitBlob.
[CompletionInfo](../android.view.inputmethod/CompletionInfo.md) Information about a single text completion that an editor has reported to an input method.
[ComponentAdData](../android.adservices.common/ComponentAdData.md) Represents data specific to a component ad that is necessary for ad selection and rendering.
[ComponentName](../android.content/ComponentName.md) Identifier for a specific application component (`https://developer.android.com/reference/kotlin/android/app/Activity.html#`, `https://developer.android.com/reference/kotlin/android/app/Service.html#`, `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#`, or `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#`) that is available.
[Condition](../android.service.notification/Condition.md) The current condition of an `https://developer.android.com/reference/kotlin/android/app/AutomaticZenRule.html#`, provided by the app that owns the rule.
[Configuration](../android.content.res/Configuration.md) This class describes all device configuration information that can impact the resources the application retrieves.
[ConfigurationInfo](../android.content.pm/ConfigurationInfo.md) Information you can retrieve about hardware configuration preferences declared by an application.
[ConfigurationStats](../android.app.usage/ConfigurationStats.md) Represents the usage statistics of a device `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#` for a specific time range.
[ConnectEvent](../android.app.admin/ConnectEvent.md) A class that represents a TCP connect event initiated through the standard network stack.
[ConnectionRequest](../android.telecom/ConnectionRequest.md) Simple data container encapsulating a request to some entity to create a new `https://developer.android.com/reference/kotlin/android/telecom/Connection.html#`.
[ConnectivityDiagnosticsManager.ConnectivityReport](../android/net/ConnectivityDiagnosticsManager.ConnectivityReport.md) Class that includes connectivity information for a specific Network at a specific time.
[ConnectivityDiagnosticsManager.DataStallReport](../android/net/ConnectivityDiagnosticsManager.DataStallReport.md) Class that includes information for a suspected data stall on a specific Network
[ContactsContract.SimAccount](../android/provider/ContactsContract.SimAccount.md) A parcelable class encapsulating account data for contacts that originate from a SIM card.
[ContentCaptureCondition](../android.view.contentcapture/ContentCaptureCondition.md) Defines a condition for when content capture should be allowed.
[ContentCaptureContext](../android.view.contentcapture/ContentCaptureContext.md) Context associated with a `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession.html#` - see `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureManager.html#` for more info.
[ContentCaptureSessionId](../android.view.contentcapture/ContentCaptureSessionId.md) Identifier for a Content Capture session.
[ContentClassificationResult](../android.app.contentsafety/ContentClassificationResult.md) A result reported by a Content Safety app in response to a content classification request.
[ContentInfo](../android.view/ContentInfo.md) Holds all the relevant data for a request to performReceiveContent.
[ContentProviderOperation](../android.content/ContentProviderOperation.md) Represents a single operation to be performed as part of a batch of operations.
[ContentProviderResult](../android.content/ContentProviderResult.md) Contains the result of the application of a `https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation.html#`.
[ContentValues](../android.content/ContentValues.md) This class is used to store a set of values that the `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#` can process.
[Control](../android.service.controls/Control.md) Represents a physical object that can be represented by a `https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate.html#` and whose properties may be modified through a `https://developer.android.com/reference/kotlin/android/service/controls/actions/ControlAction.html#`.
[ControlButton](../android.service.controls.templates/ControlButton.md) Button element for `https://developer.android.com/reference/kotlin/android/service/controls/templates/ControlTemplate.html#`.
[ConversationAction](../android.view.textclassifier/ConversationAction.md) Represents the action suggested by a `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier.html#` on a given conversation.
[ConversationActions](../android.view.textclassifier/ConversationActions.md) Represents a list of actions suggested by a `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier.html#` on a given conversation.
[ConversationActions.Message](../android/view/textclassifier/ConversationActions.Message.md) Represents a message in the conversation.
[ConversationActions.Request](../android/view/textclassifier/ConversationActions.Request.md) A request object for generating conversation action suggestions.
[ConversationStatus](../android.app.people/ConversationStatus.md) <br />

[CorrectionInfo](../android.view.inputmethod/CorrectionInfo.md) Information about a single text correction that an editor has reported to an input method.
[CpuUsageInfo](CpuUsageInfo.md) CPU usage information per core.
[CreateCredentialRequest](../android.service.credentials/CreateCredentialRequest.md) Request for creating a credential.
[CreateCredentialRequest](../android.credentials/CreateCredentialRequest.md) A request to register a specific type of user credential, potentially launching UI flows to collect user consent and any other operation needed.
[CreateCredentialResponse](../android.credentials/CreateCredentialResponse.md) A response object that encapsulates the result of a successful credential creation execution.
[CreateEntry](../android.service.credentials/CreateEntry.md) An entry to be shown on the UI.
[CreateMedicalDataSourceRequest](../android.health.connect/CreateMedicalDataSourceRequest.md) A create request for createMedicalDataSource.
[Credential](../android.net.wifi.hotspot2.pps/Credential.md) Class representing Credential subtree in the PerProviderSubscription (PPS) Management Object (MO) tree.
[Credential](../android.credentials/Credential.md) Represents a user credential that can be used to authenticate to your app.
[Credential.CertificateCredential](../android/net/wifi/hotspot2/pps/Credential.CertificateCredential.md) Certificate based credential.
[Credential.SimCredential](../android/net/wifi/hotspot2/pps/Credential.SimCredential.md) SIM (Subscriber Identify Module) based credential.
[Credential.UserCredential](../android/net/wifi/hotspot2/pps/Credential.UserCredential.md) Username-password based credential.
[CredentialDescription](../android.credentials/CredentialDescription.md) Represents the type and contained data fields of a `https://developer.android.com/reference/kotlin/android/credentials/Credential.html#`.
[CredentialEntry](../android.service.credentials/CredentialEntry.md) A credential entry that is to be displayed on the account selector that is presented to the user.
[CredentialOption](../android.credentials/CredentialOption.md) Information about a specific type of credential to be requested during a android.
[Criteria](../android.location/Criteria.md) A class indicating the application criteria for selecting a location provider.
[CursorAnchorInfo](../android.view.inputmethod/CursorAnchorInfo.md) Positional information about the text insertion point and characters in the composition string.
[CursorWindow](../android.database/CursorWindow.md) A buffer containing multiple cursor rows.
[CustomAudience](../android.adservices.customaudience/CustomAudience.md) Represents the information necessary for a custom audience to participate in ad selection.
[CustomDescription](../android.service.autofill/CustomDescription.md) Defines a custom description for the autofill save UI.
[DataNotificationConfig](../android.ranging/DataNotificationConfig.md) Represents the configuration for data notifications in ranging operations.
[DataRemovalRequest](../android.view.contentcapture/DataRemovalRequest.md) Class used by apps to request the content capture service to remove data associated with `https://developer.android.com/reference/kotlin/android/content/LocusId.html#`.
[DataShareRequest](../android.view.contentcapture/DataShareRequest.md) Container class representing a request to share data with Content Capture service.
[Dataset](../android.service.autofill/Dataset.md) A `Dataset` object represents a group of fields (key / value pairs) used to autofill parts of a screen.
[DateTransformation](../android.service.autofill/DateTransformation.md) Replaces a `https://developer.android.com/reference/kotlin/android/widget/TextView.html#` child of a `https://developer.android.com/reference/kotlin/android/service/autofill/CustomDescription.html#` with the contents of a field that is expected to have a forDate.
[DateValueSanitizer](../android.service.autofill/DateValueSanitizer.md) Sanitizes a date `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue.html#` using a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.html#`.
[Debug.MemoryInfo](../android/os/Debug.MemoryInfo.md) This class is used to retrieved various statistics about the memory mappings for this process.
[DecisionLogic](../android.adservices.adselection/DecisionLogic.md) Generic Decision logic that could be provided by the buyer or seller.
[DeleteGesture](../android.view.inputmethod/DeleteGesture.md) A sub-class of `https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture.html#` for deleting an area of text using single rectangle.
[DeleteMedicalResourcesRequest](../android.health.connect/DeleteMedicalResourcesRequest.md) A delete request for android.
[DeleteRangeGesture](../android.view.inputmethod/DeleteRangeGesture.md) A subclass of `https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture.html#` for deleting a range of text by defining start and end rectangles.
[DeviceAdminInfo](../android.app.admin/DeviceAdminInfo.md) This class is used to specify meta information of a device administrator component.
[DeviceDataSource](../android.health.connect/DeviceDataSource.md) Represents a device that acts as a source of health and fitness data.
[DeviceDataTypeSource](../android/health/connect/DeviceDataTypeSource.md) A data type provided by a device.
[DeviceFilter](../android.companion/DeviceFilter.md) A filter for companion devices of type `D`
[DeviceHandle](../android.ranging.oob/DeviceHandle.md) Represents a handle to a ranging device, containing information about the device and a transport handle for out-of-band communication.
[DeviceId](../android.companion/DeviceId.md) A device id represents a device identifier managed by the companion app.
[DevicePresenceEvent](../android.companion/DevicePresenceEvent.md) Event for observing device presence.
[DeviceProductInfo](../android.hardware.display/DeviceProductInfo.md) Product-specific information about the display or the directly connected device on the display chain.
[DeviceProductInfo.EdidStructureMetadata](../android/hardware/display/DeviceProductInfo.EdidStructureMetadata.md) Encapsulates the EDID version, parsed from bytes 18 (version) and 19 (revision).
[DhcpInfo](../android.net/DhcpInfo.md) A simple object for retrieving the results of a DHCP request.
[DirectAction](../android.app/DirectAction.md) Represents an abstract action that can be perform on this app.
[DisconnectCause](../android.telecom/DisconnectCause.md) Describes the cause of a disconnected call.
[DiscoveryRequest](../android.net.nsd/DiscoveryRequest.md) Encapsulates parameters for android.
[Display.HdrCapabilities](../android/view/Display.HdrCapabilities.md) Encapsulates the HDR capabilities of a given display.
[Display.Mode](../android/view/Display.Mode.md) A mode supported by a given display.
[DisplayHash](../android.view.displayhash/DisplayHash.md) The DisplayHash used to validate information about what was present on screen.
[DisplayShape](../android.view/DisplayShape.md) A class representing the shape of a display.
[DisplayTopology](../android.hardware.display/DisplayTopology.md) Represents the relative placement of extended displays.
[DlTdoaMeasurement](../android/ranging/DlTdoaMeasurement.md) Represents a single measurement from a Downlink Time Difference of Arrival (DL-TDoA) ranging session.
[DlTdoaMeasurement.AnchorLocation](../android/ranging/DlTdoaMeasurement.AnchorLocation.md) Class to represent the anchor location.
[DlTdoaMeasurement.RelativeLocation](../android/ranging/DlTdoaMeasurement.RelativeLocation.md) Represents a location in a relative coordinate system.
[DlTdoaMeasurement.Wgs84Location](../android/ranging/DlTdoaMeasurement.Wgs84Location.md) Represents a location in the WGS-84 coordinate system.
[DlTdoaMeasurement.ZElementExtension](../android/ranging/DlTdoaMeasurement.ZElementExtension.md) Represents a Z-element extension regarding the height of a anchor.
[DlTdoaRangingParams](../android/ranging/uwb/DlTdoaRangingParams.md) Class to represent UWB Downlink TDoA ranging parameters.
[DnsEvent](../android.app.admin/DnsEvent.md) A class that represents a DNS lookup event initiated through the standard network stack.
[DocumentsContract.Path](../android/provider/DocumentsContract.Path.md) Holds a path from a document to a particular document under it.
[DomainVerificationUserState](../android.content.pm.verify.domain/DomainVerificationUserState.md) Contains the user selection state for a package.
[DownloadRequest](../android.telephony.mbms/DownloadRequest.md) Describes a request to download files over cell-broadcast.
[DownloadableSubscription](../android.telephony.euicc/DownloadableSubscription.md) Information about a subscription which is downloadable to an eUICC using downloadSubscription.
[DragAndDropPermissions](../android.view/DragAndDropPermissions.md) `https://developer.android.com/reference/kotlin/android/view/DragAndDropPermissions.html#` controls the access permissions for the content URIs associated with a `https://developer.android.com/reference/kotlin/android/view/DragEvent.html#`.
[DragEvent](../android.view/DragEvent.md) Represents an event that is sent out by the system at various times during a drag and drop operation.
[DropBoxManager.Entry](../android/os/DropBoxManager.Entry.md) A single entry retrieved from the drop box.
[DsmccRequest](../android.media.tv/DsmccRequest.md) A request for DSM-CC from broadcast signal.
[DsmccResponse](../android.media.tv/DsmccResponse.md) A response for DSM-CC from broadcast signal.
[E2eeContactKeysManager.E2eeContactKey](../android/provider/E2eeContactKeysManager.E2eeContactKey.md) A parcelable class encapsulating other users' end to end encrypted contact key.
[E2eeContactKeysManager.E2eeSelfKey](../android/provider/E2eeContactKeysManager.E2eeSelfKey.md) A parcelable class encapsulating self end to end encrypted contact key.
[EditingEndedEvent](../android.media.metrics/EditingEndedEvent.md) Event for an editing operation having ended.
[EditorBoundsInfo](../android.view.inputmethod/EditorBoundsInfo.md) Container of rectangular position related info for the Editor.
[EditorInfo](../android.view.inputmethod/EditorInfo.md) An EditorInfo describes several attributes of a text editing object that an input method is communicating with (typically an EditText), most importantly the type of text content it contains and the current cursor position.
[EgressRequest](../android.app.privatecompute/EgressRequest.md) Abstract base request class for PccSandboxManager.
[EgressResponse](../android.app.privatecompute/EgressResponse.md) Abstract base response class for PccSandboxManager.
[EmbeddedPhotoPickerFeatureInfo](../android.widget.photopicker/EmbeddedPhotoPickerFeatureInfo.md) An immutable parcel to carry information regarding desired features of caller for a given session.
[EmbeddedPhotoPickerUiCustomizationParams](../android.widget.photopicker/EmbeddedPhotoPickerUiCustomizationParams.md) Defines UI customization options specific to the embedded Photo Picker interface.
[EmbeddingVector](../android.app.appsearch/EmbeddingVector.md) Embeddings are vector representations of data, such as text, images, and audio, which can be generated by machine learning models and used for semantic search.
[EmergencyNumber](../android.telephony.emergency/EmergencyNumber.md) A parcelable class that wraps and retrieves the information of number, service category(s) and country code for a specific emergency number.
[EqualizerBand](../android/media/quality/EqualizerBand.md) Represents a single band in an equalizer.
[EqualizerCapabilities](../android/media/quality/EqualizerCapabilities.md) A class to represent the static capabilities of an equalizer.
[EqualizerSettings](../android/media/quality/EqualizerSettings.md) A class to represent the current settings of an equalizer.
[EthernetNetworkSpecifier](../android.net/EthernetNetworkSpecifier.md) A `https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier.html#` used to identify ethernet interfaces.
[EuiccInfo](../android.telephony.euicc/EuiccInfo.md) Information about an eUICC chip/device.
[EventLogRecord](../android.adservices.ondevicepersonalization/EventLogRecord.md) Data to be logged in the EVENTS table.
[EventStats](../android.app.usage/EventStats.md) Contains usage statistics for an event type for a specific time range.
[ExecuteAppFunctionRequest](../android.app.appfunctions/ExecuteAppFunctionRequest.md) A request to execute an app function, provided to android.
[ExecuteAppFunctionResponse](../android.app.appfunctions/ExecuteAppFunctionResponse.md) The response to an app function execution, returned by android.
[ExerciseRoute](../android.health.connect.datatypes/ExerciseRoute.md) Route of the exercise session.
[ExerciseRoute.Location](../android/health/connect/datatypes/ExerciseRoute.Location.md) Point in the time and space.
[ExternalStorageStats](../android.app.usage/ExternalStorageStats.md) Shared/external storage statistics for a UserHandle on a single storage volume.
[ExtractedText](../android.view.inputmethod/ExtractedText.md) Information about text that has been extracted for use by an input method.
[ExtractedTextRequest](../android.view.inputmethod/ExtractedTextRequest.md) Description of what an input method would like from an application when extract text from its input editor.
[FactoryResetProtectionPolicy](../android.app.admin/FactoryResetProtectionPolicy.md) The factory reset protection policy determines which accounts can unlock a device that has gone through untrusted factory reset.
[FallbackOption](../android.hardware.biometrics/FallbackOption.md) Contains the information for a fallback option to be displayed within Biometric Prompt.
[FeatureGroupInfo](../android.content.pm/FeatureGroupInfo.md) A set of features that can be requested by an application.
[FeatureInfo](../android.content.pm/FeatureInfo.md) Definition of a single optional hardware or software feature of an Android device.
[FhirResource](../android.health.connect.datatypes/FhirResource.md) A class to capture the FHIR resource data.
[FhirVersion](../android.health.connect.datatypes/FhirVersion.md) Represents the FHIR version.
[FieldClassification](../android.service.assist.classification/FieldClassification.md) Represents a classified field from the detection service.
[FileInfo](../android.telephony.mbms/FileInfo.md) Describes a single file that is available over MBMS.
[FileOperationEnqueueResult](../android/os/storage/operations/FileOperationEnqueueResult.md) Result of an operation enqueue request.
[FileOperationRequest](../android/os/storage/operations/FileOperationRequest.md) Encapsulates a request to Move, or Copy files.
[FileOperationResult](../android/os/storage/operations/FileOperationResult.md) Represents the result of a file operation.
[FileServiceInfo](../android.telephony.mbms/FileServiceInfo.md) Describes a file service available from the carrier from which files can be downloaded via cell-broadcast.
[FillContext](../android.service.autofill/FillContext.md) This class represents a context for each fill request made via onFillRequest.
[FillEventHistory](../android.service.autofill/FillEventHistory.md) Describes what happened after the last onFillRequest call.
[FillRequest](../android.service.autofill/FillRequest.md) This class represents a request to an autofill service to interpret the screen and provide information to the system which views are interesting for saving and what are the possible ways to fill the inputs on the screen if applicable.
[FillResponse](../android.service.autofill/FillResponse.md) Response for an onFillRequest.
[ForegroundServiceStartNotAllowedException](../android.app/ForegroundServiceStartNotAllowedException.md) Exception thrown when an app tries to start a foreground `https://developer.android.com/reference/kotlin/android/app/Service.html#` when it's not allowed to do so.
[FormEditRecord](../android.graphics.pdf.models/FormEditRecord.md) Record of a form filling operation that has been executed on a single form field in a PDF.
[FormWidgetInfo](../android.graphics.pdf.models/FormWidgetInfo.md) Information about a form widget of a PDF document.
[Fragment.SavedState](../android/app/Fragment.SavedState.md) State information that has been retrieved from a fragment instance through saveFragmentInstanceState.
[FrameRateVelocityPoint](../android/view/FrameRateVelocityPoint.md) Contains the frame rate / velocity values.
[FrequencyCapFilters](../android.adservices.common/FrequencyCapFilters.md) A container for the ad filters that are based on frequency caps.
[Gainmap](../android.graphics/Gainmap.md) Gainmap represents a mechanism for augmenting an SDR image to produce an HDR one with variable display adjustment capability.
[GameState](../android.app/GameState.md) State of the game passed to the GameManager.
[GatewayInfo](../android.telecom/GatewayInfo.md) Encapsulated gateway address information for outgoing call.
[Gesture](../android.gesture/Gesture.md) A gesture is a hand-drawn shape on a touch screen.
[GetByDocumentIdRequest](../android.app.appsearch/GetByDocumentIdRequest.md) Encapsulates a request to retrieve documents by namespace and IDs from the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession.html#` database.
[GetCredentialRequest](../android.service.credentials/GetCredentialRequest.md) Request for getting user's credential from a given credential provider.
[GetCredentialRequest](../android.credentials/GetCredentialRequest.md) A request to retrieve the user credential, potentially launching UI flows to let the user pick from different credential sources.
[GetCredentialResponse](../android.credentials/GetCredentialResponse.md) A response object that encapsulates the credential successfully retrieved from the user.
[GetDeviceDataSourcesResponse](../android/health/connect/GetDeviceDataSourcesResponse.md) Response containing the list of `https://developer.android.com/reference/kotlin/android/health/connect/DeviceDataSource.html#`.
[GetMedicalDataSourcesRequest](../android.health.connect/GetMedicalDataSourcesRequest.md) A create request for android.
[GetSchemaResponse](../android.app.appsearch/GetSchemaResponse.md) The response class of getSchema
[GetValueRequest](../android.service.settings.preferences/GetValueRequest.md) Request parameters to retrieve the current value of a Settings Preference.
[GetValueResult](../android.service.settings.preferences/GetValueResult.md) Result object given a corresponding `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueRequest.html#`.
[GetWalletCardsError](../android.service.quickaccesswallet/GetWalletCardsError.md) Error response for an `https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsRequest.html#`.
[GetWalletCardsRequest](../android.service.quickaccesswallet/GetWalletCardsRequest.md) Represents a request to a `https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/QuickAccessWalletService.html#` for `https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard.html#`.
[GetWalletCardsResponse](../android.service.quickaccesswallet/GetWalletCardsResponse.md) The response for an `https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/GetWalletCardsRequest.html#` contains a list of wallet cards and the index of the card that should initially be displayed in the 'selected' position.
[GnssAntennaInfo](../android.location/GnssAntennaInfo.md) A class that contains information about a GNSS antenna.
[GnssAntennaInfo.PhaseCenterOffset](../android/location/GnssAntennaInfo.PhaseCenterOffset.md) Class containing information about the antenna phase center offset (PCO).
[GnssAntennaInfo.SphericalCorrections](../android/location/GnssAntennaInfo.SphericalCorrections.md) Represents corrections on a spherical mapping.
[GnssAutomaticGainControl](../android.location/GnssAutomaticGainControl.md) A class that contains GNSS Automatic Gain Control (AGC) information.
[GnssCapabilities](../android.location/GnssCapabilities.md) GNSS chipset capabilities.
[GnssClock](../android.location/GnssClock.md) A class containing a GNSS clock timestamp.
[GnssMeasurement](../android.location/GnssMeasurement.md) A class representing a GNSS satellite measurement, containing raw and computed information.
[GnssMeasurementRequest](../android.location/GnssMeasurementRequest.md) This class contains extra parameters to pass in a GNSS measurement request.
[GnssMeasurementsEvent](../android.location/GnssMeasurementsEvent.md) A class implementing a container for data associated with a measurement event.
[GnssNavigationMessage](../android.location/GnssNavigationMessage.md) A class containing a GNSS satellite Navigation Message.
[GnssSignalType](../android.location/GnssSignalType.md) This class represents a GNSS signal type.
[GnssStatus](../android.location/GnssStatus.md) This class represents the current state of the GNSS engine and is used in conjunction with `https://developer.android.com/reference/kotlin/android/location/GnssStatus.Callback.html#`.
[GrantedKeyInfo](../android.security/GrantedKeyInfo.md) Information about a key pair granted to an application via KeyChain.
[HandoffActivityData](../android/app/HandoffActivityData.md) Represents information needed to recreate an activity on a remote device owned by the user.
[HandoffActivityParams](../android/app/HandoffActivityParams.md) Represents options specifying how an activity will be handed off to other devices.
[HardwareBuffer](../android.hardware/HardwareBuffer.md) HardwareBuffer wraps a native `AHardwareBuffer` object, which is a low-level object representing a memory buffer accessible by various hardware units.
[HdrConversionMode](../android.hardware.display/HdrConversionMode.md) Describes the HDR conversion mode for a device.
[HomeSp](../android.net.wifi.hotspot2.pps/HomeSp.md) Class representing HomeSP subtree in PerProviderSubscription (PPS) Management Object (MO) tree.
[HostUsiVersion](../android.hardware.input/HostUsiVersion.md) Provides information about the supported Universal Stylus Initiative (USI) version of the host device.
[IccOpenLogicalChannelResponse](../android.telephony/IccOpenLogicalChannelResponse.md) Response to the android.
[Icon](../android.graphics.drawable/Icon.md) An umbrella container for several serializable graphics representations, including Bitmaps, compressed bitmap images (e.g. JPG or PNG), and drawable resources (including vectors).
[ImageTransformation](../android.service.autofill/ImageTransformation.md) Replaces the content of a child `https://developer.android.com/reference/kotlin/android/widget/ImageView.html#` of a `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#` with the first image that matches a regular expression (regex).
[ImsReasonInfo](../android.telephony.ims/ImsReasonInfo.md) Provides details on why an IMS call failed.
[ImsRegistrationAttributes](../android.telephony.ims/ImsRegistrationAttributes.md) Contains the attributes associated with the current IMS registration.
[InlinePresentation](../android.service.autofill/InlinePresentation.md) Wrapper class holding a `https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#` and an `https://developer.android.com/reference/kotlin/android/widget/inline/InlinePresentationSpec.html#` for rendering UI for an Inline Suggestion.
[InlinePresentationSpec](../android.widget.inline/InlinePresentationSpec.md) This class represents the presentation specification by which an inline suggestion should abide when constructing its UI.
[InlineSuggestion](../android.view.inputmethod/InlineSuggestion.md) This class represents an inline suggestion which is made by one app and can be embedded into the UI of another.
[InlineSuggestionInfo](../android.view.inputmethod/InlineSuggestionInfo.md) This class represents the description of an inline suggestion.
[InlineSuggestionsRequest](../android.view.inputmethod/InlineSuggestionsRequest.md) This class represents an inline suggestion request made by one app to get suggestions from the other source.
[InlineSuggestionsResponse](../android.view.inputmethod/InlineSuggestionsResponse.md) This class represents an inline suggestion response.
[InputBinding](../android.view.inputmethod/InputBinding.md) Information given to an `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod.html#` about a client connecting to it.
[InputContentInfo](../android.view.inputmethod/InputContentInfo.md) A container object with which input methods can send content files to the target application.
[InputDevice](../android.view/InputDevice.md) Describes the capabilities of a particular input device.
[InputEvent](../android.view/InputEvent.md) Common base class for input events.
[InputMethodInfo](../android.view.inputmethod/InputMethodInfo.md) This class is used to specify meta information of an input method.
[InputMethodSubtype](../android.view.inputmethod/InputMethodSubtype.md) This class is used to specify meta information of a subtype contained in an input method editor (IME).
[InputTransferToken](../android.window/InputTransferToken.md) A token that can be used to request focus on or to transfer touch gesture to a `https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.html#` or `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.html#` that has an input channel.
[InsertGesture](../android.view.inputmethod/InsertGesture.md) A sub-class of `https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture.html#` for inserting text at the defined insertion point.
[InsertModeGesture](../android.view.inputmethod/InsertModeGesture.md) A sub-class of `https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture.html#` for starting an insert mode which inserts a space in the editor to let users hand write freely at the designated insertion point.
[Insets](../android.graphics/Insets.md) An Insets instance holds four integer offsets which describe changes to the four edges of a Rectangle.
[InstallSourceInfo](../android.content.pm/InstallSourceInfo.md) Information about how an app was installed.
[InstrumentationInfo](../android.content.pm/InstrumentationInfo.md) Information you can retrieve about a particular piece of test instrumentation.
[Intent](../android.content/Intent.md) An intent is an abstract description of an operation to be performed.
[Intent.ShortcutIconResource](../android/content/Intent.ShortcutIconResource.md) Represents a shortcut/live folder icon resource.
[IntentFilter](../android.content/IntentFilter.md) Structured description of Intent values to be matched.
[IntentSender](../android.content/IntentSender.md) A description of an Intent and target action to perform with it.
[InvalidForegroundServiceTypeException](../android.app/InvalidForegroundServiceTypeException.md) Exception thrown when an app tries to start a foreground `https://developer.android.com/reference/kotlin/android/app/Service.html#` with an invalid type.
[IpConfiguration](../android.net/IpConfiguration.md) A class representing the IP configuration of a network.
[IpPrefix](../android.net/IpPrefix.md) This class represents an IP prefix, i.
[IpSecAlgorithm](../android.net/IpSecAlgorithm.md) This class represents a single algorithm that can be used by an `https://developer.android.com/reference/kotlin/android/net/IpSecTransform.html#`.
[IpSecTransformState](../android.net/IpSecTransformState.md) This class represents a snapshot of the state of an IpSecTransform
[JobInfo](../android.app.job/JobInfo.md) Container of data passed to the `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler.html#` fully encapsulating the parameters required to schedule work against the calling application.
[JobInfo.TriggerContentUri](../android/app/job/JobInfo.TriggerContentUri.md) Information about a content URI modification that a job would like to trigger on.
[JobParameters](../android.app.job/JobParameters.md) Contains the parameters used to configure/identify your job.
[JobWorkItem](../android.app.job/JobWorkItem.md) A unit of work that can be enqueued for a job using enqueue.
[JoinOrSplitGesture](../android.view.inputmethod/JoinOrSplitGesture.md) A subclass of `https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture.html#` for deleting or inserting whitespace in text.
[JoinSpec](../android.app.appsearch/JoinSpec.md) This class represents the specifications for the joining operation in search.
[KeyCharacterMap](../android.view/KeyCharacterMap.md) Describes the keys provided by a keyboard device and their associated labels.
[KeyEvent](../android.view/KeyEvent.md) Object used to report key and button events.
[KeyboardShortcutGroup](../android.view/KeyboardShortcutGroup.md) A group of `https://developer.android.com/reference/kotlin/android/view/KeyboardShortcutInfo.html#`.
[KeyboardShortcutInfo](../android.view/KeyboardShortcutInfo.md) Information about a Keyboard Shortcut.
[KeyedFrequencyCap](../android.adservices.common/KeyedFrequencyCap.md) A frequency cap for a specific ad counter key.
[L2capNetworkSpecifier](../android.net/L2capNetworkSpecifier.md) A `https://developer.android.com/reference/kotlin/android/net/NetworkSpecifier.html#` used to identify an L2CAP network over BLE.
[LauncherApps.PinItemRequest](../android/content/pm/LauncherApps.PinItemRequest.md) Represents a "pin shortcut" or a "pin appwidget" request made by an app, which is sent with an `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.html#ACTION_CONFIRM_PIN_SHORTCUT:kotlin.String` or `https://developer.android.com/reference/kotlin/android/content/pm/LauncherApps.html#ACTION_CONFIRM_PIN_APPWIDGET:kotlin.String` intent respectively to the default launcher app.
[LauncherUserInfo](../android.content.pm/LauncherUserInfo.md) The LauncherUserInfo object holds information about an Android user that is required to display the Launcher related UI elements specific to the user (like badges).
[Light](../android.hardware.lights/Light.md) Represents a logical light on the device.
[LightState](../android.hardware.lights/LightState.md) Represents the state of a device light.
[LineBreakConfig](../android.graphics.text/LineBreakConfig.md) Specifies the line-break strategies for text wrapping.
[LinkAddress](../android.net/LinkAddress.md) Identifies an IP address on a network link.
[LinkProperties](../android.net/LinkProperties.md) Describes the properties of a network link.
[ListItem](../android.graphics.pdf.models/ListItem.md) Represents a single option in a combo box or list box PDF form widget.
[LoadSdkException](../android.app.sdksandbox/LoadSdkException.md) Exception thrown by loadSdk
[LocaleConfig](../android.app/LocaleConfig.md) The LocaleConfig of an application.
[LocaleList](LocaleList.md) LocaleList is an immutable list of Locales, typically used to keep an ordered list of user preferences for locales.
[Location](../android.location/Location.md) A data class representing a geographic location.
[LocationButtonRequest](../android/app/permissionui/LocationButtonRequest.md) Defines the requested visual properties for a location button.
[LocationRequest](../android.location/LocationRequest.md) An encapsulation of various parameters for requesting location via `https://developer.android.com/reference/kotlin/android/location/LocationManager.html#`.
[LocusId](../android.content/LocusId.md) An identifier for an unique state (locus) in the application.
[LuhnChecksumValidator](../android.service.autofill/LuhnChecksumValidator.md) Validator that returns `true` if the number created by concatenating all given fields pass a Luhn algorithm checksum.
[MacAddress](../android.net/MacAddress.md) Representation of a MAC address.
[MagnificationConfig](../android.accessibilityservice/MagnificationConfig.md) This class describes the magnification config for `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#` to control the magnification.
[ManagedSubscriptionsPolicy](../android.app.admin/ManagedSubscriptionsPolicy.md) A policy class that describes how managed SIM subscriptions should behave on the device.
[MatchmakingRequest](../android.health.connect/MatchmakingRequest.md) Represents a request to determine if there are matching data sources for a given set of record types.
[MatchmakingResponse](../android/health/connect/MatchmakingResponse.md) A response for isMatchmakingPossible.
[MediaBrowser.MediaItem](../android/media/browse/MediaBrowser.MediaItem.md) A class with information on a single media item for use in browsing/searching media.
[MediaController.PlaybackInfo](../android/media/session/MediaController.PlaybackInfo.md) Holds information about the current playback and how audio is handled for this session.
[MediaDescription](../android.media/MediaDescription.md) A simple set of metadata for a media item suitable for display.
[MediaItemInfo](../android.media.metrics/MediaItemInfo.md) Represents information about a piece of media (for example, an audio or video file).
[MediaMetadata](../android.media/MediaMetadata.md) Contains metadata about an item, such as the title, artist, etc.
[MediaPlayer.TrackInfo](../android/media/MediaPlayer.TrackInfo.md) Class for MediaPlayer to return each audio/video/subtitle track's metadata.
[MediaProjectionAppContent](../android/media/projection/MediaProjectionAppContent.md) Holds information about content an app can share via the MediaProjection APIs.
[MediaProjectionConfig](../android.media.projection/MediaProjectionConfig.md) Configure the `https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection.html#` session requested from createScreenCaptureIntent.
[MediaQualityManager.ProfileQueryParams](../android/media/quality/MediaQualityManager.ProfileQueryParams.md) Options for profile queries.
[MediaRoute2Info](../android.media/MediaRoute2Info.md) Describes the properties of a route.
[MediaSession.QueueItem](../android/media/session/MediaSession.QueueItem.md) A single item that is part of the play queue.
[MediaSession.Token](../android/media/session/MediaSession.Token.md) Represents an ongoing session.
[MediaSyncEvent](../android.media/MediaSyncEvent.md) The MediaSyncEvent class defines events that can be used to synchronize playback or capture actions between different players and recorders.
[MedicalDataSource](../android.health.connect.datatypes/MedicalDataSource.md) Captures the data source information of medical data.
[MedicalResource](../android.health.connect.datatypes/MedicalResource.md) A class to capture the user's medical data.
[MedicalResourceId](../android.health.connect/MedicalResourceId.md) A class to represent a unique identifier of a medical resource.
[MemoryBudgetInfo](../android.content.pm/MemoryBudgetInfo.md) Memory budget information for an application.
[Message](Message.md) Defines a message containing a description and arbitrary data object that can be sent to a Handler.
[MessagePdu](../android.service.carrier/MessagePdu.md) A parcelable list of PDUs representing contents of a possibly multi-part SMS.
[Messenger](Messenger.md) Reference to a Handler, which others can use to send messages to it.
[MetadataRequest](../android.service.settings.preferences/MetadataRequest.md) Request parameters to retrieve all metadata for all available settings preferences within this application.
[MetadataResult](../android.service.settings.preferences/MetadataResult.md) Result object given a corresponding `https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataRequest.html#`.
[MidiDeviceInfo](../android.media.midi/MidiDeviceInfo.md) This class contains information to describe a MIDI device.
[MidiDeviceStatus](../android.media.midi/MidiDeviceStatus.md) This is an immutable class that describes the current status of a MIDI device's ports.
[MigrationRequestResult](../android.app.privatecompute/MigrationRequestResult.md) Result of a migration request initiated by a PCC component.
[MissingForegroundServiceTypeException](../android.app/MissingForegroundServiceTypeException.md) Exception thrown when an app tries to start a foreground `https://developer.android.com/reference/kotlin/android/app/Service.html#` without a type.
[MloLink](../android.net.wifi/MloLink.md) Data structure class representing a Wi-Fi Multi-Link Operation (MLO) link This is only used by 802.
[ModuleInfo](../android.content.pm/ModuleInfo.md) Information you can retrieve about a particular system module.
[MotionEvent](../android.view/MotionEvent.md) Object used to report movement (mouse, pen, finger, trackball) events.
[MotionState](../android/ranging/MotionState.md) Represents the motion state of a ranging device.
[MultiLightEffect](../android/hardware/lights/MultiLightEffect.md) Models an effect that will be shown in one or more lights.
[NdefMessage](../android.nfc/NdefMessage.md) Represents an immutable NDEF Message.
[NdefRecord](../android.nfc/NdefRecord.md) Represents an immutable NDEF Record.
[NeighboringCellInfo](../android.telephony/NeighboringCellInfo.md) Represents the neighboring cell information, including Received Signal Strength and Cell ID location.
[Network](../android.net/Network.md) Identifies a `Network`.
[NetworkCapabilities](../android.net/NetworkCapabilities.md) Representation of the capabilities of an active network.
[NetworkEvent](../android.app.admin/NetworkEvent.md) An abstract class that represents a network event.
[NetworkEvent](../android.media.metrics/NetworkEvent.md) Media network event.
[NetworkInfo](../android.net/NetworkInfo.md) Describes the status of a network interface.
[NetworkRegistrationInfo](../android.telephony/NetworkRegistrationInfo.md) Description of a mobile network registration info
[NetworkRequest](../android.net/NetworkRequest.md) An object describing a network that the application is interested in.
[NetworkScanRequest](../android.telephony/NetworkScanRequest.md) Defines a request to perform a network scan.
[NetworkSliceInfo](../android.telephony.data/NetworkSliceInfo.md) Represents a S-NSSAI as defined in 3GPP TS 24.
[NetworkSlicingConfig](../android.telephony.data/NetworkSlicingConfig.md) Represents a slicing configuration
[NfcAntennaInfo](../android.nfc/NfcAntennaInfo.md) Contains information on all available Nfc antennas on an Android device as well as information on the device itself in relation positioning of the antennas.
[Notification](../android.app/Notification.md) A class that represents how a persistent notification is to be presented to the user using the `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#`.
[Notification.Action](../android/app/Notification.Action.md) Structure to encapsulate a named action that can be shown as part of this notification.
[Notification.BridgedNotificationMetadata](../android/app/Notification.BridgedNotificationMetadata.md) Encapsulates the information needed to display a notification as a bridged notification.
[Notification.BubbleMetadata](../android/app/Notification.BubbleMetadata.md) Encapsulates the information needed to display a notification as a bubble.
[NotificationChannel](../android.app/NotificationChannel.md) A representation of settings that apply to a collection of similarly themed notifications.
[NotificationChannelGroup](../android.app/NotificationChannelGroup.md) A grouping of related notification channels.
[NotificationListenerService.RankingMap](../android/service/notification/NotificationListenerService.RankingMap.md) Provides access to ranking information on currently active notifications.
[NotificationManager.Policy](../android/app/NotificationManager.Policy.md) Notification policy configuration.
[NsdServiceInfo](../android.net.nsd/NsdServiceInfo.md) A class representing service information for network service discovery
[NtnSignalStrength](../android/telephony/satellite/NtnSignalStrength.md) NTN signal strength related information.
[ObbInfo](../android.content.res/ObbInfo.md) Basic information about a Opaque Binary Blob (OBB) that reflects the info from the footer on the OBB file.
[ObserverSpec](../android.app.appsearch.observer/ObserverSpec.md) Configures the types, namespaces and other properties that `https://developer.android.com/reference/kotlin/android/app/appsearch/observer/ObserverCallback.html#` instances match against.
[ObservingDevicePresenceRequest](../android.companion/ObservingDevicePresenceRequest.md) A request for setting the types of device for observing device presence.
[OobInitiatorRangingConfig](../android.ranging.oob/OobInitiatorRangingConfig.md) Represents the configuration for an Out-of-Band (OOB) initiator in a ranging session.
[OobResponderRangingConfig](../android.ranging.oob/OobResponderRangingConfig.md) Represents the configuration for an Out-of-Band (OOB) responder in a ranging session.
[OpenBlobForReadResponse](../android.app.appsearch/OpenBlobForReadResponse.md) The response to provide batch operation results of openBlobForRead.
[OpenBlobForWriteResponse](../android.app.appsearch/OpenBlobForWriteResponse.md) The response to provide batch operation results of openBlobForWrite.
[OutOfBandPairingRequest](../android.companion/OutOfBandPairingRequest.md) Represents a request for out-of-band pairing.
[OutputConfiguration](../android.hardware.camera2.params/OutputConfiguration.md) A class for describing camera output, which contains a `https://developer.android.com/reference/kotlin/android/view/Surface.html#` and its specific configuration for creating capture session.
[OverlayIdentifier](../android.content.om/OverlayIdentifier.md) A key used to uniquely identify a Runtime Resource Overlay (RRO).
[OverlayInfo](../android.content.om/OverlayInfo.md) An immutable information about an overlay.
[OverlayManagerTransaction](../android.content.om/OverlayManagerTransaction.md) A container for a batch of requests to the OverlayManager.
[OverlayProperties](../android.hardware/OverlayProperties.md) Provides supported overlay properties of the device.
[PackageInfo](../android.content.pm/PackageInfo.md) Overall information about the contents of a package.
[PackageInstaller.InstallConstraints](../android/content/pm/PackageInstaller.InstallConstraints.md) A class to encapsulate constraints for installation.
[PackageInstaller.InstallConstraintsResult](../android/content/pm/PackageInstaller.InstallConstraintsResult.md) The callback result of checkInstallConstraints.
[PackageInstaller.PreapprovalDetails](../android/content/pm/PackageInstaller.PreapprovalDetails.md) Details for requesting the pre-commit install approval.
[PackageInstaller.SessionInfo](../android/content/pm/PackageInstaller.SessionInfo.md) Details for an active install session.
[PackageInstaller.SessionParams](../android/content/pm/PackageInstaller.SessionParams.md) Parameters for creating a new `https://developer.android.com/reference/kotlin/android/content/pm/PackageInstaller.Session.html#`.
[PackageManager.ComponentEnabledSetting](../android/content/pm/PackageManager.ComponentEnabledSetting.md) The class containing the enabled setting of a package component.
[PackageManager.Property](../android/content/pm/PackageManager.Property.md) A property value set within the manifest.
[PackagePolicy](../android.app.admin/PackagePolicy.md) A generic class that defines which APK packages are in scope for some device policy.
[PackageStats](../android.content.pm/PackageStats.md) implementation of PackageStats associated with a application package.
[PageMatchBounds](../android.graphics.pdf.models/PageMatchBounds.md) Represents the bounds of a single search match on a page of the PDF document.
[PageRange](../android.print/PageRange.md) Represents a range of pages.
[PageSelection](../android.graphics.pdf.models.selection/PageSelection.md) Represents the list of selected content on a particular page of the PDF document.
[ParameterCapability](../android.media.quality/ParameterCapability.md) Capability info of media quality parameters
[ParcelFileDescriptor](ParcelFileDescriptor.md) The FileDescriptor returned by readFileDescriptor, allowing you to close it when done with it.
[ParcelUuid](ParcelUuid.md) This class is a Parcelable wrapper around `https://developer.android.com/reference/kotlin/java/util/UUID.html#` which is an immutable representation of a 128-bit universally unique identifier.
[ParcelableColorSpace](../android.graphics/ParcelableColorSpace.md) A Parcelable wrapper for a `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.html#`.
[ParcelablePeerHandle](../android.net.wifi.aware/ParcelablePeerHandle.md) A Parcelable `https://developer.android.com/reference/kotlin/android/net/wifi/aware/PeerHandle.html#`.
[ParcelableSpan](../android.text/ParcelableSpan.md) A special kind of Parcelable for objects that will serve as text spans.
[ParsedPhoneNumber](../android.telephony/ParsedPhoneNumber.md) Handles the results from PhoneNumberManager by providing Phone number, error code, and is valid number.
[PartialCustomAudience](../android.adservices.customaudience/PartialCustomAudience.md) Represents a partial custom audience that is passed along to the buyer ad tech, when scheduling a delayed update for Custom Audience.
[PasnConfig](../android.net.wifi.rtt/PasnConfig.md) Pre-association security negotiation (PASN) configuration.
[PasspointConfiguration](../android.net.wifi.hotspot2/PasspointConfiguration.md) Class representing Passpoint configuration.
[PatternMatcher](PatternMatcher.md) A simple pattern matcher, which is safe to use on untrusted data: it does not provide full reg-exp support, only simple globbing that can not be used maliciously.
[PccEgressException](../android.app.privatecompute/PccEgressException.md) Exception thrown when an egress request fails inside the PCC sandbox.
[PccEgressException.SensitiveCategoryInfo](../android/app/privatecompute/PccEgressException.SensitiveCategoryInfo.md) Details about the detected sensitive content that caused an egress request to be rejected.
[PdfPageGotoLinkContent](../android.graphics.pdf.content/PdfPageGotoLinkContent.md) Represents the content associated with a goto link on a page in the PDF document.
[PdfPageGotoLinkContent.Destination](../android/graphics/pdf/content/PdfPageGotoLinkContent.Destination.md) Represents the content associated with the destination where a goto link is directing
[PdfPageImageContent](../android.graphics.pdf.content/PdfPageImageContent.md) Represents the content associated with an image type in a page of a PDF document.
[PdfPageLinkContent](../android.graphics.pdf.content/PdfPageLinkContent.md) Represents the bounds and link on a page of the PDF document.
[PdfPageTextContent](../android.graphics.pdf.content/PdfPageTextContent.md) Represents a continuous stream of text in a page of a PDF document in the order of viewing.
[PendingIntent](../android.app/PendingIntent.md) A description of an Intent and target action to perform with it.
[PendingJobReasonsInfo](../android.app.job/PendingJobReasonsInfo.md) A simple wrapper which includes a timestamp (in millis since epoch) and an array of android.
[PerBuyerConfiguration](../android.adservices.adselection/PerBuyerConfiguration.md) Contains a per buyer configuration which will be used as part of a `https://developer.android.com/reference/kotlin/android/adservices/adselection/SellerConfiguration.html#` in a `https://developer.android.com/reference/kotlin/android/adservices/adselection/GetAdSelectionDataRequest.html#`.
[PerBuyerDecisionLogic](../android.adservices.adselection/PerBuyerDecisionLogic.md) The override object for decision logic JS per buyer for `https://developer.android.com/reference/kotlin/android/adservices/adselection/SignedContextualAds.html#`.
[PeriodicAdvertisingParameters](../android.bluetooth.le/PeriodicAdvertisingParameters.md) The `https://developer.android.com/reference/kotlin/android/bluetooth/le/PeriodicAdvertisingParameters.html#` provide a way to adjust periodic advertising preferences for each Bluetooth LE advertising set.
[PeriodicSync](../android.content/PeriodicSync.md) Value type that contains information about a periodic sync.
[PermissionGroupInfo](../android.content.pm/PermissionGroupInfo.md) Information you can retrieve about a particular security permission group known to the system.
[PermissionInfo](../android.content.pm/PermissionInfo.md) Information you can retrieve about a particular security permission known to the system.
[PersistableBundle](PersistableBundle.md) A mapping from String keys to values of various types.
[Person](../android.app/Person.md) Provides an immutable reference to an entity that appears repeatedly on different surfaces of the platform.
[PesRequest](../android.media.tv/PesRequest.md) A request for PES from broadcast signal.
[PesResponse](../android.media.tv/PesResponse.md) A response for PES from broadcast signal.
[PhoneAccount](../android.telecom/PhoneAccount.md) Represents a distinct method to place or receive a phone call.
[PhoneAccountHandle](../android.telecom/PhoneAccountHandle.md) The unique identifier for a `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount.html#`.
[PhoneAccountSuggestion](../android.telecom/PhoneAccountSuggestion.md) <br />

[PhotoPickerSelectionParams](../android/widget/photopicker/PhotoPickerSelectionParams.md) An immutable parcel that carries constraints to be applied to media items displayed in the Photo Picker.
[PhotoPickerUiCustomizationParams](../android.widget.photopicker/PhotoPickerUiCustomizationParams.md) Defines UI customization options for the system's Photo Picker interface.
[PhysicalChannelConfig](../android.telephony/PhysicalChannelConfig.md) Information describing the physical channel configuration.
[PictureInPictureParams](../android.app/PictureInPictureParams.md) Represents a set of parameters used to initialize and update an Activity in picture-in-picture mode.
[PictureInPictureUiState](../android.app/PictureInPictureUiState.md) Used by onPictureInPictureUiStateChanged.
[PictureProfile](../android.media.quality/PictureProfile.md) Profile for picture quality.
[PlaybackErrorEvent](../android.media.metrics/PlaybackErrorEvent.md) Playback error event.
[PlaybackMetrics](../android.media.metrics/PlaybackMetrics.md) This class is used to store playback data.
[PlaybackParams](../android.media/PlaybackParams.md) Structure for common playback params.
[PlaybackState](../android.media.session/PlaybackState.md) Playback state for a `https://developer.android.com/reference/kotlin/android/media/session/MediaSession.html#`.
[PlaybackState.CustomAction](../android/media/session/PlaybackState.CustomAction.md) `https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.CustomAction.html#` can be used to extend the capabilities of the standard transport controls by exposing app specific actions to `https://developer.android.com/reference/kotlin/android/media/session/MediaController.html#`.
[PlaybackStateEvent](../android.media.metrics/PlaybackStateEvent.md) Playback state event.
[Point](../android.graphics/Point.md) Point holds two integer coordinates
[PointF](../android.graphics/PointF.md) PointF holds two float coordinates
[PointerIcon](../android.view/PointerIcon.md) Represents an icon that can be used as a mouse pointer.
[PollingFrame](../android.nfc.cardemulation/PollingFrame.md) Polling Frames represent data about individual frames of an NFC polling loop.
[PowerMonitor](PowerMonitor.md) A PowerMonitor represents either an ODPM rail (on-device power rail monitor) or a modeled energy consumer.
[PreciseDataConnectionState](../android.telephony/PreciseDataConnectionState.md) Contains precise data connection state.
[PreferenceActivity.Header](../android/preference/PreferenceActivity.Header.md) Description of a single Header item that the user can select.
[PreferentialNetworkServiceConfig](../android.app.admin/PreferentialNetworkServiceConfig.md) Network configuration to be set for the user profile.
[PrintAttributes](../android.print/PrintAttributes.md) This class represents the attributes of a print job.
[PrintDocumentInfo](../android.print/PrintDocumentInfo.md) This class encapsulates information about a document for printing purposes.
[PrintJobId](../android.print/PrintJobId.md) This class represents the id of a print job.
[PrintJobInfo](../android.print/PrintJobInfo.md) This class represents the description of a print job.
[PrinterCapabilitiesInfo](../android.print/PrinterCapabilitiesInfo.md) This class represents the capabilities of a printer.
[PrinterId](../android.print/PrinterId.md) This class represents the unique id of a printer.
[PrinterInfo](../android.print/PrinterInfo.md) This class represents the description of a printer.
[ProfilingResult](ProfilingResult.md) Encapsulates results of a single profiling request operation.
[PromptContentItemBulletedText](../android.hardware.biometrics/PromptContentItemBulletedText.md) A list item with bulleted text shown on `https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptVerticalListContentView.html#`.
[PromptContentItemPlainText](../android.hardware.biometrics/PromptContentItemPlainText.md) A list item with plain text shown on `https://developer.android.com/reference/kotlin/android/hardware/biometrics/PromptVerticalListContentView.html#`.
[PromptContentViewWithMoreOptionsButton](../android.hardware.biometrics/PromptContentViewWithMoreOptionsButton.md) Contains the information of the template of content view with a more options button for Biometric Prompt.
[PromptVerticalListContentView](../android.hardware.biometrics/PromptVerticalListContentView.md) Contains the information of the template of vertical list content view for Biometric Prompt.
[ProviderInfo](../android.content.pm/ProviderInfo.md) Holds information about a specific `https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#`.
[ProviderProperties](../android.location.provider/ProviderProperties.md) Location provider properties.
[ProxyInfo](../android.net/ProxyInfo.md) Describes a proxy configuration.
[PublishConfig](../android.net.wifi.aware/PublishConfig.md) Defines the configuration of an Aware publish session.
[QueryLocationException](../android.telecom/QueryLocationException.md) This class represents a set of exceptions that can occur when requesting a queryLocationForEmergency
[RadioAccessSpecifier](../android.telephony/RadioAccessSpecifier.md) Describes a particular radio access network to be scanned.
[RangingCapabilities](../android.ranging/RangingCapabilities.md) Represents the capabilities and availability of various ranging technologies.
[RangingConfig](../android.ranging/RangingConfig.md) Abstract class to represent type of ranging configuration.
[RangingData](../android.ranging/RangingData.md) Represents ranging data, including distance, azimuth, elevation, and RSSI measurements, along with the ranging technology used and a timestamp.
[RangingDataExtras](../android/ranging/RangingDataExtras.md) Represents extra ranging data from various technologies.
[RangingDevice](../android.ranging/RangingDevice.md) Represents a ranging device identified by a unique UUID.
[RangingMeasurement](../android.ranging/RangingMeasurement.md) Represents a ranging measurement.
[RangingPreference](../android.ranging/RangingPreference.md) Represents the configuration preferences for a ranging session.
[RangingRequest](../android.net.wifi.rtt/RangingRequest.md) Defines the ranging request to other devices.
[RangingResult](../android.net.wifi.rtt/RangingResult.md) Ranging result for a request started by startRanging.
[Rating](../android.media/Rating.md) A class to encapsulate rating information used as content metadata.
[RawDtTagRangingConfig](../android/ranging/raw/RawDtTagRangingConfig.md) <br />

[RawInitiatorRangingConfig](../android.ranging.raw/RawInitiatorRangingConfig.md) Represents the configuration for initiating a raw ranging session.
[RawRangingDevice](../android.ranging.raw/RawRangingDevice.md) Represents a device participating in ranging operations.
[RawResponderRangingConfig](../android.ranging.raw/RawResponderRangingConfig.md) Represents the configuration for a raw ranging session initiated by a responder device.
[ReadMedicalResourcesResponse](../android.health.connect/ReadMedicalResourcesResponse.md) A read response for android.
[RecognitionPart](../android.speech/RecognitionPart.md) Info about a single recognition part.
[RecognitionSupport](../android.speech/RecognitionSupport.md) Encodes the level of support for a given speech recognition request
[RecoverableSecurityException](../android.app/RecoverableSecurityException.md) Specialization of `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` that contains additional information about how to involve the end user to recover from the exception.
[Rect](../android.graphics/Rect.md) Rect holds four integer coordinates for a rectangle.
[RectF](../android.graphics/RectF.md) RectF holds four float coordinates for a rectangle.
[RegexValidator](../android.service.autofill/RegexValidator.md) Defines if a field is valid based on a regular expression (regex).
[Region](../android.graphics/Region.md) <br />

[RegisterCredentialDescriptionRequest](../android.credentials/RegisterCredentialDescriptionRequest.md) A request to register a `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` that contains an actively provisioned `https://developer.android.com/reference/kotlin/android/credentials/Credential.html#` represented by a `https://developer.android.com/reference/kotlin/android/credentials/CredentialDescription.html#`.
[RemoteAction](../android.app/RemoteAction.md) Represents a remote action that can be called from another process.
[RemoteEntry](../android.service.credentials/RemoteEntry.md) An entry to be shown on the UI.
[RemoteInput](../android.app/RemoteInput.md) A `RemoteInput` object specifies input to be collected from a user to be passed along with an intent inside a `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` that is sent.
[RemoteViews](../android.widget/RemoteViews.md) A class that describes a view hierarchy that can be displayed in another process.
[RemoteViews.RemoteCollectionItems](../android/widget/RemoteViews.RemoteCollectionItems.md) Representation of a fixed list of items to be displayed in a RemoteViews collection.
[RemoveBlobResponse](../android.app.appsearch/RemoveBlobResponse.md) Results of removeBlob, containing the outcome of the removal of each handles.
[RemoveByDocumentIdRequest](../android.app.appsearch/RemoveByDocumentIdRequest.md) Encapsulates a request to remove documents by namespace and IDs from the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession.html#` database.
[RemoveSpaceGesture](../android.view.inputmethod/RemoveSpaceGesture.md) A subclass of `https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture.html#` for removing whitespace from text.
[RenderingConfig](../android.adservices.ondevicepersonalization/RenderingConfig.md) Information returned by onExecute that is used in a subesequent call to onRender to identify the content to be displayed in a single `https://developer.android.com/reference/kotlin/android/view/View.html#`.
[ReportUsageRequest](../android.app.appsearch/ReportUsageRequest.md) A request to report usage of a document.
[RequestLogRecord](../android.adservices.ondevicepersonalization/RequestLogRecord.md) Contains data that will be written to the REQUESTS table at the end of a call to onExecute.
[ResolveInfo](../android.content.pm/ResolveInfo.md) Information that is returned from resolving an intent against an IntentFilter.
[ResponderConfig](../android.net.wifi.rtt/ResponderConfig.md) Defines the configuration of an IEEE 802.
[ResponderLocation](../android.net.wifi.rtt/ResponderLocation.md) ResponderLocation is both a Location Configuration Information (LCI) decoder and a Location Civic Report (LCR) decoder for information received from a Wi-Fi Access Point (AP) during Wi-Fi RTT ranging process.
[RestrictionEntry](../android.content/RestrictionEntry.md) Applications can expose restrictions for a restricted user on a multiuser device.
[ResultReceiver](ResultReceiver.md) Generic interface for receiving a callback result from someone.
[RoundedCorner](../android.view/RoundedCorner.md) Represents a rounded corner of the display.
[RouteDiscoveryPreference](../android.media/RouteDiscoveryPreference.md) A media route discovery preference describing the features of routes that media router would like to discover and whether to perform active scanning.
[RouteInfo](../android.net/RouteInfo.md) Represents a network route.
[RouteListingPreference](../android.media/RouteListingPreference.md) Allows applications to customize the list of routes used for media routing (for example, in the System UI Output Switcher).
[RouteListingPreference.Item](../android/media/RouteListingPreference.Item.md) Holds preference information for a specific route in a `https://developer.android.com/reference/kotlin/android/media/RouteListingPreference.html#`.
[RouteSelectionDescriptor](../android.telephony.data/RouteSelectionDescriptor.md) Represents a single route selection descriptor as defined in 3GPP TS 24.
[RoutingSessionInfo](../android.media/RoutingSessionInfo.md) Describes a routing session which is created when a media route is selected.
[RttRangingCapabilities](../android.ranging.wifi.rtt/RttRangingCapabilities.md) Represents the capabilities of the WiFi Neighbor Awareness Networking Round Trip Time (NAN-RTT) ranging.
[RttRangingParams](../android.ranging.wifi.rtt/RttRangingParams.md) Represents the parameters required to perform Wi-Fi Round Trip Time (RTT) ranging.
[RttStationRangingParams](../android.ranging.wifi.rtt/RttStationRangingParams.md) Represents the parameters required to perform Wi-Fi Station-AP Round Trip Time (RTT) ranging.
[SandboxedSdk](../android.app.sdksandbox/SandboxedSdk.md) Represents an SDK loaded in the sandbox process.
[SaveInfo](../android.service.autofill/SaveInfo.md) Information used to indicate that an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#` is interested on saving the user-inputed data for future use, through a onSaveRequest call.
[SaveRequest](../android.service.autofill/SaveRequest.md) This class represents a request to an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService.html#` to save applicable data entered by the user.
[ScanFilter](../android.bluetooth.le/ScanFilter.md) Criteria for filtering result from Bluetooth LE scans.
[ScanResult](../android.net.wifi/ScanResult.md) Describes information about a detected access point.
[ScanResult](../android.bluetooth.le/ScanResult.md) ScanResult for Bluetooth LE scan.
[ScanResult.InformationElement](../android/net/wifi/ScanResult.InformationElement.md) information elements from beacon.
[ScanSettings](../android.bluetooth.le/ScanSettings.md) Bluetooth LE scan settings are passed to android.
[SchemaVisibilityConfig](../android.app.appsearch/SchemaVisibilityConfig.md) A class to hold a all necessary Visibility information corresponding to the same schema.
[SearchResult](../android.app.appsearch/SearchResult.md) This class represents one of the results obtained from an AppSearch query.
[SearchResult.EmbeddingMatchInfo](../android/app/appsearch/SearchResult.EmbeddingMatchInfo.md) This class represents match objects for any snippets that might be present in `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResults.html#` from an embedding query.
[SearchResult.MatchInfo](../android/app/appsearch/SearchResult.MatchInfo.md) This class represents match objects for any snippets that might be present in `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResults.html#` from a query.
[SearchResult.MatchRange](../android/app/appsearch/SearchResult.MatchRange.md) Class providing the position range of a text match information.
[SearchResult.TextMatchInfo](../android/app/appsearch/SearchResult.TextMatchInfo.md) This class represents match objects for any text match snippets that might be present in `https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResults.html#` from a string query.
[SearchSpec](../android.app.appsearch/SearchSpec.md) This class represents the specification logic for AppSearch.
[SearchSuggestionResult](../android.app.appsearch/SearchSuggestionResult.md) The result class of the searchSuggestion.
[SearchSuggestionSpec](../android.app.appsearch/SearchSuggestionSpec.md) This class represents the specification logic for AppSearch.
[SearchableInfo](../android.app/SearchableInfo.md) Searchability meta-data for an activity.
[SectionRequest](../android.media.tv/SectionRequest.md) A request for Section from broadcast signal.
[SectionResponse](../android.media.tv/SectionResponse.md) A response for Section from broadcast signal.
[SecureRangingConfig](../android.net.wifi.rtt/SecureRangingConfig.md) Secure ranging configuration.
[SecurityLog.SecurityEvent](../android/app/admin/SecurityLog.SecurityEvent.md) A class representing a security event log entry.
[SelectGesture](../android.view.inputmethod/SelectGesture.md) A sub-class of `https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture.html#` for selecting an area of text using single rectangle.
[SelectRangeGesture](../android.view.inputmethod/SelectRangeGesture.md) A subclass of `https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture.html#` for selecting a range of text by defining start and end rectangles.
[SelectWalletCardRequest](../android.service.quickaccesswallet/SelectWalletCardRequest.md) Represents a request to a `https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/QuickAccessWalletService.html#` to select a particular `https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard.html#`.
[SelectionBoundary](../android.graphics.pdf.models.selection/SelectionBoundary.md) Represents one edge of the selected content.
[SelectionEvent](../android.view.textclassifier/SelectionEvent.md) A selection event.
[SellerConfiguration](../android.adservices.adselection/SellerConfiguration.md) This object will be part of the `https://developer.android.com/reference/kotlin/android/adservices/adselection/GetAdSelectionDataRequest.html#` and will be constructed and used by the SDK to influence the size of the response of getAdSelectionData
[SensorFusionParams](../android.ranging/SensorFusionParams.md) Configuration for the sensor fusion algorithm to use in a ranging session.
[SentenceSuggestionsInfo](../android.view.textservice/SentenceSuggestionsInfo.md) This class contains a metadata of suggestions returned from a text service (e.g.
[ServiceInfo](../android.content.pm/ServiceInfo.md) Information you can retrieve about a particular application service.
[ServiceState](../android.telephony/ServiceState.md) Contains phone state and service related information.
[Session2Command](../android.media/Session2Command.md) This API is not generally intended for third party application developers.
[Session2CommandGroup](../android.media/Session2CommandGroup.md) This API is not generally intended for third party application developers.
[Session2Token](../android.media/Session2Token.md) This API is not generally intended for third party application developers.
[SessionConfig](../android.ranging/SessionConfig.md) Defines the ranging session configurations.
[SessionConfiguration](../android.hardware.camera2.params/SessionConfiguration.md) A helper class that aggregates all supported arguments for capture session initialization.
[SetSchemaResponse](../android.app.appsearch/SetSchemaResponse.md) The response class of setSchema
[SetSchemaResponse.MigrationFailure](../android/app/appsearch/SetSchemaResponse.MigrationFailure.md) The class represents a post-migrated `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.html#` that failed to be saved by setSchema.
[SetValueRequest](../android.service.settings.preferences/SetValueRequest.md) Request parameters to set the current value to a Settings Preference.
[SetValueResult](../android.service.settings.preferences/SetValueResult.md) Result object given a corresponding `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueRequest.html#`.
[SettingsPreferenceMetadata](../android.service.settings.preferences/SettingsPreferenceMetadata.md) Data object representation of a Settings Preference definition and state.
[SettingsPreferenceValue](../android.service.settings.preferences/SettingsPreferenceValue.md) This objects represents a value that can be used for a particular settings preference.
[SharedLibraryInfo](../android.content.pm/SharedLibraryInfo.md) This class provides information for a shared library.
[SharedMemory](SharedMemory.md) SharedMemory enables the creation, mapping, and protection control over anonymous shared memory.
[ShortcutInfo](../android.content.pm/ShortcutInfo.md) Represents a shortcut that can be published via `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager.html#`.
[SignalStrength](../android.telephony/SignalStrength.md) Contains phone signal strength related information.
[SignalStrengthUpdateRequest](../android.telephony/SignalStrengthUpdateRequest.md) Request used to register `https://developer.android.com/reference/kotlin/android/telephony/SignalThresholdInfo.html#` to be notified when the signal strength breach the specified thresholds.
[SignalThresholdInfo](../android.telephony/SignalThresholdInfo.md) Defines the threshold value of the signal strength.
[SignalingDataInfo](../android.media.tv/SignalingDataInfo.md) Describes a metadata object of a `https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataResponse.html#`.
[SignalingDataRequest](../android.media.tv/SignalingDataRequest.md) Request to retrieve the Low-level Signalling Tables (LLS) and Service-layer Signalling (SLS) metadata.
[SignalingDataResponse](../android.media.tv/SignalingDataResponse.md) A response for the signaling data from the broadcast signal.
[Signature](../android.content.pm/Signature.md) Opaque, immutable representation of a signing certificate associated with an application package.
[SignedContextualAds](../android.adservices.adselection/SignedContextualAds.md) Contains a list of buyer supplied `https://developer.android.com/reference/kotlin/android/adservices/adselection/AdWithBid.html#` bundle and its signature.
[SigningInfo](../android.content.pm/SigningInfo.md) Information pertaining to the signing certificates used to sign a package.
[SipDetails](../android.telephony.ims/SipDetails.md) Contains the information for SIP.
[SipProfile](../android.net.sip/SipProfile.md) Defines a SIP profile, including a SIP account, domain and server information.
[SizeF](../android.util/SizeF.md) Immutable class for describing width and height dimensions in some arbitrary unit.
[Slice](../android.app.slice/Slice.md) A slice is a piece of app content and actions that can be surfaced outside of the app.
[SliceItem](../android.app.slice/SliceItem.md) A SliceItem is a single unit in the tree structure of a `https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#`.
[SliceSpec](../android.app.slice/SliceSpec.md) Class describing the structure of the data contained within a slice.
[SoftApConfiguration](../android.net.wifi/SoftApConfiguration.md) Configuration for a soft access point (a.k.a. Soft AP, SAP, Hotspot).
[SoundProfile](../android.media.quality/SoundProfile.md) Profile for sound quality.
[SourceRegistrationRequest](../android.adservices.measurement/SourceRegistrationRequest.md) Class to hold input to measurement source registration calls.
[SpellCheckerInfo](../android.view.textservice/SpellCheckerInfo.md) This class is used to specify meta information of a spell checker.
[SpellCheckerSubtype](../android.view.textservice/SpellCheckerSubtype.md) This class is used to specify meta information of a subtype contained in a spell checker.
[StartForegroundCalledOnStoppedServiceException](../android.app/StartForegroundCalledOnStoppedServiceException.md) Exception thrown when android.
[StaticIpConfiguration](../android.net/StaticIpConfiguration.md) Class that describes static IP configuration.
[StatusBarNotification](../android.service.notification/StatusBarNotification.md) Class encapsulating a Notification.
[StatusHints](../android.telecom/StatusHints.md) Contains status label and icon displayed in the in-call UI.
[StorageInfo](../android.app.appsearch/StorageInfo.md) The response class of `AppSearchSession#getStorageInfo`.
[StorageStats](../android.app.usage/StorageStats.md) Storage statistics for a UID, package, or UserHandle on a single storage volume.
[StorageVolume](../android.os.storage/StorageVolume.md) Information about a shared/external storage volume for a specific user.
[StreamEventRequest](../android.media.tv/StreamEventRequest.md) A request for Stream Event from broadcast signal.
[StreamEventResponse](../android.media.tv/StreamEventResponse.md) A response for Stream Event from broadcast signal.
[StreamingServiceInfo](../android.telephony.mbms/StreamingServiceInfo.md) Describes a single MBMS streaming service.
[SubscribeConfig](../android.net.wifi.aware/SubscribeConfig.md) Defines the configuration of an Aware subscribe session.
[SubscriptionInfo](../android.telephony/SubscriptionInfo.md) A Parcelable class for Subscription Information.
[SubscriptionPlan](../android.telephony/SubscriptionPlan.md) Description of a billing relationship plan between a carrier and a specific subscriber.
[SuggestedDeviceInfo](../android.media/SuggestedDeviceInfo.md) Allows applications to suggest routes to the system UI (for example, in the System UI Output Switcher).
[SuggestionsInfo](../android.view.textservice/SuggestionsInfo.md) This class contains a metadata of suggestions from the text service
[SupplicantState](../android.net.wifi/SupplicantState.md) From
[Surface](../android.view/Surface.md) Handle onto a raw buffer that is being managed by the screen compositor.
[SurfaceControl](../android.view/SurfaceControl.md) Handle to an on-screen Surface managed by the system compositor.
[SurfaceControl.Transaction](../android/view/SurfaceControl.Transaction.md) An atomic set of changes to a set of SurfaceControl.
[SurfaceControlViewHost.SurfacePackage](../android/view/SurfaceControlViewHost.SurfacePackage.md) Package encapsulating a Surface hierarchy which contains interactive view elements.
[SurroundingText](../android.view.inputmethod/SurroundingText.md) Information about the surrounding text around the cursor for use by an input method.
[SyncAdapterType](../android.content/SyncAdapterType.md) Value type that represents a SyncAdapterType.
[SyncFence](../android.hardware/SyncFence.md) A SyncFence represents a synchronization primitive which signals when hardware units have completed work on a particular resource.
[SyncInfo](../android.content/SyncInfo.md) Information about the sync operation that is currently underway.
[SyncNotedAppOp](../android.app/SyncNotedAppOp.md) Description of an app-op that was noted for the current process.
[SyncRequest](../android.content/SyncRequest.md) Convenience class to construct sync requests.
[SyncResult](../android.content/SyncResult.md) This class is used to communicate the results of a sync operation to the SyncManager.
[SyncStats](../android.content/SyncStats.md) Used to record various statistics about the result of a sync operation.
[SystemUpdateInfo](../android.app.admin/SystemUpdateInfo.md) A class containing information about a pending system update.
[SystemUpdatePolicy](../android.app.admin/SystemUpdatePolicy.md) Determines when over-the-air system updates are installed on a device.
[SystemUpdatePolicy.ValidationFailedException](../android/app/admin/SystemUpdatePolicy.ValidationFailedException.md) An exception class that represents various validation errors thrown from setFreezePeriods and setSystemUpdatePolicy
[TableRequest](../android.media.tv/TableRequest.md) A request for Table from broadcast signal.
[TableResponse](../android.media.tv/TableResponse.md) A response for Table from broadcast signal.
[Tag](../android.nfc/Tag.md) Represents an NFC tag that has been discovered.
[TelephonyDisplayInfo](../android.telephony/TelephonyDisplayInfo.md) TelephonyDisplayInfo contains telephony-related information used for display purposes only.
[TelephonyNetworkSpecifier](../android.net/TelephonyNetworkSpecifier.md) NetworkSpecifier object for cellular network request.
[TetheringInterface](../android.net/TetheringInterface.md) The mapping of tethering interface and type.
[TetheringManager.TetheringRequest](../android/net/TetheringManager.TetheringRequest.md) Use with startTethering to specify additional parameters when starting tethering.
[TextAppearanceInfo](../android.view.inputmethod/TextAppearanceInfo.md) Information about text appearance in an editor, passed through `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo.html#` for use by `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#`.
[TextAttribute](../android.view.inputmethod/TextAttribute.md) The data class that IME can take extra information to applications when setting the text.
[TextBoundsInfo](../android.view.inputmethod/TextBoundsInfo.md) The text bounds information of a slice of text in the editor.
[TextClassification](../android.view.textclassifier/TextClassification.md) Information for generating a widget to handle classified text.
[TextClassification.Request](../android/view/textclassifier/TextClassification.Request.md) A request object for generating TextClassification.
[TextClassificationContext](../android.view.textclassifier/TextClassificationContext.md) A representation of the context in which text classification would be performed.
[TextClassificationSessionId](../android.view.textclassifier/TextClassificationSessionId.md) This class represents the id of a text classification session.
[TextClassifier.EntityConfig](../android/view/textclassifier/TextClassifier.EntityConfig.md) Configuration object for specifying what entity types to identify.
[TextClassifierEvent](../android.view.textclassifier/TextClassifierEvent.md) This class represents events that are sent by components to the `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier.html#` to report something of note that relates to a feature powered by the TextClassifier.
[TextClassifierEvent.ConversationActionsEvent](../android/view/textclassifier/TextClassifierEvent.ConversationActionsEvent.md) This class represents events that are related to the conversation actions feature.
[TextClassifierEvent.LanguageDetectionEvent](../android/view/textclassifier/TextClassifierEvent.LanguageDetectionEvent.md) This class represents events that are related to the language detection feature.
[TextClassifierEvent.TextLinkifyEvent](../android/view/textclassifier/TextClassifierEvent.TextLinkifyEvent.md) This class represents events that are related to the smart linkify feature.
[TextClassifierEvent.TextSelectionEvent](../android/view/textclassifier/TextClassifierEvent.TextSelectionEvent.md) This class represents events that are related to the smart text selection feature.
[TextInfo](../android.view.textservice/TextInfo.md) This class contains a metadata of the input of TextService
[TextLanguage](../android.view.textclassifier/TextLanguage.md) Represents the result of language detection of a piece of text.
[TextLanguage.Request](../android/view/textclassifier/TextLanguage.Request.md) A request object for detecting the language of a piece of text.
[TextLinks](../android.view.textclassifier/TextLinks.md) A collection of links, representing subsequences of text and the entity types (phone number, address, url, etc) they may be.
[TextLinks.Request](../android/view/textclassifier/TextLinks.Request.md) A request object for generating TextLinks.
[TextLinks.TextLink](../android/view/textclassifier/TextLinks.TextLink.md) A link, identifying a substring of text and possible entity types for it.
[TextSelection](../android.view.textclassifier/TextSelection.md) Information about where text selection should be.
[TextSelection.Request](../android/view/textclassifier/TextSelection.Request.md) A request object for generating TextSelection.
[TextValueSanitizer](../android.service.autofill/TextValueSanitizer.md) Sanitizes a text `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue.html#` using a regular expression (regex) substitution.
[Tile](../android.service.quicksettings/Tile.md) A Tile holds the state of a tile that will be displayed in Quick Settings.
[TimelineRequest](../android.media.tv/TimelineRequest.md) A request for Timeline from broadcast signal.
[TimelineResponse](../android.media.tv/TimelineResponse.md) A response for Timeline from broadcast signal.
[TimerStat](../android.os.health/TimerStat.md) A TimerStat object stores a count and a time.
[TrackChangeEvent](../android.media.metrics/TrackChangeEvent.md) Playback track change event.
[TrafficDescriptor](../android.telephony.data/TrafficDescriptor.md) A traffic descriptor, as defined in 3GPP TS 24.
[TrainingExampleRecord](../android.adservices.ondevicepersonalization/TrainingExampleRecord.md) One record of `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/TrainingExamplesOutput.html#`.
[TranslationCapability](../android.view.translation/TranslationCapability.md) Capability class holding information for a pair of `https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec.html#`s.
[TranslationContext](../android.view.translation/TranslationContext.md) Info class holding information for `https://developer.android.com/reference/kotlin/android/view/translation/Translator.html#`s and used by createOnDeviceTranslator.
[TranslationRequest](../android.view.translation/TranslationRequest.md) Translation request sent to the translation service by the `https://developer.android.com/reference/kotlin/android/view/translation/Translator.html#` which contains the text to be translated.
[TranslationRequestValue](../android.view.translation/TranslationRequestValue.md) A value to be translated via `https://developer.android.com/reference/kotlin/android/view/translation/Translator.html#`.
[TranslationResponse](../android.view.translation/TranslationResponse.md) Response from the translation service, which contains the translated result.
[TranslationResponseValue](../android.view.translation/TranslationResponseValue.md) A translated response value from translation service.
[TranslationSpec](../android.view.translation/TranslationSpec.md) Specs and additional info for the translation data.
[TransportBlock](../android.bluetooth.le/TransportBlock.md) Wrapper for Transport Discovery Data Transport Blocks.
[TransportDiscoveryData](../android.bluetooth.le/TransportDiscoveryData.md) Wrapper for Transport Discovery Data AD Type.
[TrustedBiddingData](../android.adservices.customaudience/TrustedBiddingData.md) Represents data used during the ad selection process to fetch buyer bidding signals from a trusted key/value server.
[TrustedPresentationThresholds](../android.window/TrustedPresentationThresholds.md) Threshold values that are sent with android.
[TsRequest](../android.media.tv/TsRequest.md) A request for TS (transport stream) from broadcast signal.
[TsResponse](../android.media.tv/TsResponse.md) A response for TS (transport stream) from broadcast signal.
[TvAdServiceInfo](../android.media.tv.ad/TvAdServiceInfo.md) This class is used to specify meta information of a TV AD service.
[TvInputInfo](../android.media.tv/TvInputInfo.md) This class is used to specify meta information of a TV input.
[TvInteractiveAppServiceInfo](../android.media.tv.interactive/TvInteractiveAppServiceInfo.md) This class is used to specify meta information of a TV interactive app.
[TvRecordingInfo](../android.media.tv/TvRecordingInfo.md) This class is used to describe the meta information for a TV recording.
[TvTrackInfo](../android.media.tv/TvTrackInfo.md) Encapsulates the format of tracks played in `https://developer.android.com/reference/kotlin/android/media/tv/TvInputService.html#`.
[UiccCardInfo](../android.telephony/UiccCardInfo.md) The UiccCardInfo represents information about a currently inserted UICC or embedded eUICC.
[UiccPortInfo](../android.telephony/UiccPortInfo.md) UiccPortInfo class represents information about a single port contained on `https://developer.android.com/reference/kotlin/android/telephony/UiccCardInfo.html#`.
[UnregisterCredentialDescriptionRequest](../android.credentials/UnregisterCredentialDescriptionRequest.md) A request to unregister a `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` that contains an actively provisioned `https://developer.android.com/reference/kotlin/android/credentials/Credential.html#` represented by a `https://developer.android.com/reference/kotlin/android/credentials/CredentialDescription.html#`.
[UnsafeStateException](../android.app.admin/UnsafeStateException.md) Exception thrown when a `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.html#` operation failed because it was not safe to be executed at that moment.
[UpsertMedicalResourceRequest](../android.health.connect/UpsertMedicalResourceRequest.md) An upsert request for upsertMedicalResources.
[Uri](../android.net/Uri.md) Immutable URI reference.
[UriPermission](../android.content/UriPermission.md) Description of a single Uri permission grant.
[UrspRule](../android.telephony.data/UrspRule.md) Represents a single URSP rule as defined in 3GPP TS 24.
[UsageEvents](../android.app.usage/UsageEvents.md) A result returned from queryEvents from which to read `https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.Event.html#` objects.
[UsageEventsQuery](../android.app.usage/UsageEventsQuery.md) An Object-Oriented representation for a `https://developer.android.com/reference/kotlin/android/app/usage/UsageEvents.html#` query.
[UsageStats](../android.app.usage/UsageStats.md) Contains usage statistics for an app package for a specific time range.
[UsbAccessory](../android.hardware.usb/UsbAccessory.md) A class representing a USB accessory, which is an external hardware component that communicates with an android application over USB.
[UsbConfiguration](../android.hardware.usb/UsbConfiguration.md) A class representing a configuration on a `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice.html#`.
[UsbDevice](../android.hardware.usb/UsbDevice.md) This class represents a USB device attached to the android device with the android device acting as the USB host.
[UsbEndpoint](../android.hardware.usb/UsbEndpoint.md) A class representing an endpoint on a `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbInterface.html#`.
[UsbInterface](../android.hardware.usb/UsbInterface.md) A class representing an interface on a `https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice.html#`.
[UserData](../android.service.autofill/UserData.md) Defines the user data used for [field classification](../android.service.autofill/AutofillService.md).
[UserData](../android.adservices.ondevicepersonalization/UserData.md) User data provided by the platform to an `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService.html#`.
[UserHandle](UserHandle.md) Representation of a user on the device.
[UwbAddress](../android.ranging.uwb/UwbAddress.md) A class representing a UWB address
[UwbComplexChannel](../android.ranging.uwb/UwbComplexChannel.md) A Class representing the complex channel for UWB which comprises channel and preamble index negotiated between peer devices out of band before ranging.
[UwbRangingCapabilities](../android.ranging.uwb/UwbRangingCapabilities.md) Represents the capabilities of Ultra-Wideband (UWB) ranging technology.
[UwbRangingParams](../android.ranging.uwb/UwbRangingParams.md) UwbRangingParams encapsulates the parameters required for a UWB ranging session.
[UwbSpecificData](../android/ranging/uwb/UwbSpecificData.md) Represents the android.
[VcnConfig](../android.net.vcn/VcnConfig.md) This class represents a configuration for a Virtual Carrier Network.
[VerifiedDisplayHash](../android.view.displayhash/VerifiedDisplayHash.md) The verified display hash used to validate information about what was present on screen.
[VerifiedInputEvent](../android.view/VerifiedInputEvent.md) Base class for verified events.
[VerifiedKeyEvent](../android.view/VerifiedKeyEvent.md) KeyEvent that has been verified by the system.
[VerifiedMotionEvent](../android.view/VerifiedMotionEvent.md) MotionEvent that has been verified by the system.
[VersionedPackage](../android.content.pm/VersionedPackage.md) Encapsulates a package and its version code.
[VibrationAttributes](VibrationAttributes.md) Encapsulates a collection of attributes describing information about a vibration.
[VibrationEffect](VibrationEffect.md) A VibrationEffect describes a haptic effect to be performed by a Vibrator.
[VibratorEnvelopeEffectInfo](../android.os.vibrator/VibratorEnvelopeEffectInfo.md) Provides information about the vibrator hardware capabilities and limitations regarding waveform envelope effects.
[VideoProfile](../android.telecom/VideoProfile.md) Represents attributes of video calls.
[VideoProfile.CameraCapabilities](../android/telecom/VideoProfile.CameraCapabilities.md) Represents the camera capabilities important to a Video Telephony provider.
[ViewTranslationRequest](../android.view.translation/ViewTranslationRequest.md) Wrapper class representing a translation request associated with a `https://developer.android.com/reference/kotlin/android/view/View.html#` to be used by translation service.
[ViewTranslationResponse](../android.view.translation/ViewTranslationResponse.md) Wrapper class representing a translation response associated with a `https://developer.android.com/reference/kotlin/android/view/View.html#` to be used by translation service.
[VirtualDevice](../android.companion.virtual/VirtualDevice.md) Details of a particular virtual device.
[VirtualDisplayConfig](../android.hardware.display/VirtualDisplayConfig.md) Holds configuration used to create `https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay.html#` instances.
[VisibilitySetterAction](../android.service.autofill/VisibilitySetterAction.md) Action used to change the visibility of other child view in a `https://developer.android.com/reference/kotlin/android/service/autofill/CustomDescription.html#` `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#`.
[VisibleActivityInfo](../android.service.voice/VisibleActivityInfo.md) The class is used to represent a visible activity information.
[VisualVoicemailSms](../android.telephony/VisualVoicemailSms.md) Represents the content of a visual voicemail SMS.
[VisualVoicemailSmsFilterSettings](../android.telephony/VisualVoicemailSmsFilterSettings.md) Class to represent various settings for the visual voicemail SMS filter.
[Voice](../android.speech.tts/Voice.md) Characteristics and features of a Text-To-Speech Voice.
[VoiceInteractor.PickOptionRequest.Option](../android/app/VoiceInteractor.PickOptionRequest.Option.md) Represents a single option that the user may select using their voice.
[VoiceInteractor.Prompt](../android/app/VoiceInteractor.Prompt.md) A set of voice prompts to use with the voice interaction system to confirm an action, select an option, or do similar operations.
[VolumeShaper.Configuration](../android/media/VolumeShaper.Configuration.md) The `VolumeShaper.Configuration` class contains curve and duration information.
[VolumeShaper.Operation](../android/media/VolumeShaper.Operation.md) The `VolumeShaper.Operation` class is used to specify operations to the `VolumeShaper` that affect the volume change.
[VpnProfileState](../android.net/VpnProfileState.md) Describe the state of VPN.
[WalletCard](../android.service.quickaccesswallet/WalletCard.md) A `https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/WalletCard.html#` can represent anything that a user might carry in their wallet -- a credit card, library card, transit pass, etc.
[WalletServiceEvent](../android.service.quickaccesswallet/WalletServiceEvent.md) Represents a request from the `https://developer.android.com/reference/kotlin/android/service/quickaccesswallet/QuickAccessWalletService.html#` to the Quick Access Wallet in System UI.
[WallpaperColors](../android.app/WallpaperColors.md) Provides information about the colors of a wallpaper.
[WallpaperDescription](../android.app.wallpaper/WallpaperDescription.md) Describes a wallpaper, including associated metadata and optional content to be used by its `https://developer.android.com/reference/kotlin/android/service/wallpaper/WallpaperService.Engine.html#`, the `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` to be used by `https://developer.android.com/reference/kotlin/android/app/WallpaperManager.html#`, and an optional id to differentiate between different distinct wallpapers rendered by the same wallpaper service.
[WallpaperInfo](../android.app/WallpaperInfo.md) This class is used to specify meta information of a wallpaper service.
[WallpaperInstance](../android.app.wallpaper/WallpaperInstance.md) Describes a wallpaper that has been set as a current wallpaper.
[WebSourceParams](../android.adservices.measurement/WebSourceParams.md) Class holding source registration parameters.
[WebSourceRegistrationRequest](../android.adservices.measurement/WebSourceRegistrationRequest.md) Class to hold input to measurement source registration calls from web context.
[WebTriggerParams](../android.adservices.measurement/WebTriggerParams.md) Class holding trigger registration parameters.
[WebTriggerRegistrationRequest](../android.adservices.measurement/WebTriggerRegistrationRequest.md) Class to hold input to measurement trigger registration calls from web context.
[WifiAvailableChannel](../android.net.wifi/WifiAvailableChannel.md) Contains information about a Wifi channel and bitmask of Wifi operational modes allowed on that channel.
[WifiAwareChannelInfo](../android.net.wifi.aware/WifiAwareChannelInfo.md) Wi-Fi Aware data-path channel information.
[WifiAwareDataPathSecurityConfig](../android.net.wifi.aware/WifiAwareDataPathSecurityConfig.md) Wi-Fi Aware data-path security config.
[WifiAwareNetworkInfo](../android.net.wifi.aware/WifiAwareNetworkInfo.md) Wi-Fi Aware-specific network information.
[WifiAwareNetworkSpecifier](../android.net.wifi.aware/WifiAwareNetworkSpecifier.md) Network specifier object used to request a Wi-Fi Aware network.
[WifiConfiguration](../android.net.wifi/WifiConfiguration.md) A class representing a configured Wi-Fi network, including the security configuration.
[WifiEnterpriseConfig](../android.net.wifi/WifiEnterpriseConfig.md) Enterprise configuration details for Wi-Fi.
[WifiInfo](../android.net.wifi/WifiInfo.md) Describes the state of any Wi-Fi connection that is active or is in the process of being set up.
[WifiManager.AddNetworkResult](../android/net/wifi/WifiManager.AddNetworkResult.md) Provides the results of a call to addNetworkPrivileged
[WifiNetworkSpecifier](../android.net.wifi/WifiNetworkSpecifier.md) Network specifier object used to request a Wi-Fi network.
[WifiNetworkSuggestion](../android.net.wifi/WifiNetworkSuggestion.md) The Network Suggestion object is used to provide a Wi-Fi network for consideration when auto-connecting to networks.
[WifiP2pConfig](../android.net.wifi.p2p/WifiP2pConfig.md) A class representing a Wi-Fi P2p configuration for setting up a connection
[WifiP2pConnectionInfo](../android.net.wifi.p2p/WifiP2pConnectionInfo.md) A class representing the connection capabilities of a Wi-Fi P2P link.
[WifiP2pDevice](../android.net.wifi.p2p/WifiP2pDevice.md) A class representing a Wi-Fi p2p device Note that the operations are not thread safe
[WifiP2pDeviceList](../android.net.wifi.p2p/WifiP2pDeviceList.md) A class representing a Wi-Fi P2p device list.
[WifiP2pDirInfo](../android.net.wifi.p2p/WifiP2pDirInfo.md) This object contains the Device Identity Resolution (DIR) Info to check if the device is a previously paired device.
[WifiP2pDiscoveryConfig](../android.net.wifi.p2p/WifiP2pDiscoveryConfig.md) A class representing a Wi-Fi P2P scan configuration for setting up discovery.
[WifiP2pGroup](../android.net.wifi.p2p/WifiP2pGroup.md) A class representing a Wi-Fi P2p group.
[WifiP2pInfo](../android.net.wifi.p2p/WifiP2pInfo.md) A class representing connection information about a Wi-Fi p2p group
[WifiP2pPairingBootstrappingConfig](../android.net.wifi.p2p/WifiP2pPairingBootstrappingConfig.md) A class representing Wi-Fi Direct pairing bootstrapping configuration.
[WifiP2pServiceInfo](../android.net.wifi.p2p.nsd/WifiP2pServiceInfo.md) A class for storing service information that is advertised over a Wi-Fi peer-to-peer setup
[WifiP2pServiceRequest](../android.net.wifi.p2p.nsd/WifiP2pServiceRequest.md) A class for creating a service discovery request for use with addServiceRequest and removeServiceRequest
[WifiP2pUsdBasedLocalServiceAdvertisementConfig](../android.net.wifi.p2p/WifiP2pUsdBasedLocalServiceAdvertisementConfig.md) A class representing a Wi-Fi P2P USD based service advertisement configuration for advertising the services.
[WifiP2pUsdBasedServiceConfig](../android.net.wifi.p2p.nsd/WifiP2pUsdBasedServiceConfig.md) A class for creating a USD based service discovery configuration for use with `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceInfo.html#`.
[WifiP2pUsdBasedServiceDiscoveryConfig](../android.net.wifi.p2p/WifiP2pUsdBasedServiceDiscoveryConfig.md) A class representing a Wi-Fi P2P USD based service discovery configuration for discovering the services.
[WifiP2pUsdBasedServiceResponse](../android.net.wifi.p2p.nsd/WifiP2pUsdBasedServiceResponse.md) A class for a response for USD based service discovery.
[WifiP2pWfdInfo](../android.net.wifi.p2p/WifiP2pWfdInfo.md) A class representing Wifi Display information for a device.
[WifiPdRangingCapabilities](../android/ranging/wifi/pd/WifiPdRangingCapabilities.md) The ranging capabilities for Wi-Fi Proximity Detection (PD).
[WifiPdRangingParams](../android/ranging/wifi/pd/WifiPdRangingParams.md) Defines the parameters for Wi-Fi Proximity Detection (PD) ranging.
[WifiRttSpecificData](../android/ranging/wifi/rtt/WifiRttSpecificData.md) Represents the android.
[WifiSsid](../android.net.wifi/WifiSsid.md) Representation of a Wi-Fi Service Set Identifier (SSID).
[WifiSsidPolicy](../android.app.admin/WifiSsidPolicy.md) Used to indicate the Wi-Fi SSID restriction policy the network must satisfy in order to be eligible for a connection.
[WindowAnimationFrameStats](../android.view/WindowAnimationFrameStats.md) This class contains window animation frame statistics.
[WindowContentFrameStats](../android.view/WindowContentFrameStats.md) This class contains window content frame statistics.
[WindowId](../android.view/WindowId.md) Safe identifier for a window.
[WindowManager.LayoutParams](../android/view/WindowManager.LayoutParams.md) <br />

[WorkSource](WorkSource.md) Describes the source of some work that may be done by someone else.
[WpsInfo](../android.net.wifi/WpsInfo.md) A class representing Wi-Fi Protected Setup
[ZenDeviceEffects](../android.service.notification/ZenDeviceEffects.md) Represents the set of device effects (affecting display and device behavior in general) that are applied whenever an `https://developer.android.com/reference/kotlin/android/app/AutomaticZenRule.html#` is active.
[ZenPolicy](../android.service.notification/ZenPolicy.md) ZenPolicy determines whether to allow certain notifications and their corresponding sounds to play when a device is in Do Not Disturb mode.
Known Indirect Subclasses [AbsoluteSizeSpan](../android.text.style/AbsoluteSizeSpan.md), [AlignmentSpan.Standard](../android/text/style/AlignmentSpan.Standard.md), [Annotation](../android.text/Annotation.md), [AssistantQueryRequest](../android.app.privatecompute/AssistantQueryRequest.md), [AssistantQueryResponse](../android.app.privatecompute/AssistantQueryResponse.md), [BackgroundColorSpan](../android.text.style/BackgroundColorSpan.md), [BluetoothDeviceFilter](../android.companion/BluetoothDeviceFilter.md), [BluetoothLeDeviceFilter](../android.companion/BluetoothLeDeviceFilter.md), [BulletSpan](../android.text.style/BulletSpan.md), [CellIdentityCdma](../android.telephony/CellIdentityCdma.md), [CellIdentityGsm](../android.telephony/CellIdentityGsm.md), [CellIdentityLte](../android.telephony/CellIdentityLte.md), and 87 others. [AbsoluteSizeSpan](../android.text.style/AbsoluteSizeSpan.md) A span that changes the size of the text it's attached to.
[AlignmentSpan.Standard](../android/text/style/AlignmentSpan.Standard.md) Default implementation of the `https://developer.android.com/reference/kotlin/android/text/style/AlignmentSpan.html#`.
[Annotation](../android.text/Annotation.md) Annotations are simple key-value pairs that are preserved across TextView save/restore cycles and can be used to keep application-specific data that needs to be maintained for regions of text.
[AssistantQueryRequest](../android.app.privatecompute/AssistantQueryRequest.md) Request object specifically for Assistant Query Egress operations.
[AssistantQueryResponse](../android.app.privatecompute/AssistantQueryResponse.md) Specialized response for Assistant Query use-cases.
[BackgroundColorSpan](../android.text.style/BackgroundColorSpan.md) Changes the background color of the text to which the span is attached.
[BluetoothDeviceFilter](../android.companion/BluetoothDeviceFilter.md) A filter for Bluetooth(non-LE) devices
[BluetoothLeDeviceFilter](../android.companion/BluetoothLeDeviceFilter.md) A filter for Bluetooth LE devices
[BulletSpan](../android.text.style/BulletSpan.md) A span which styles paragraphs as bullet points (respecting layout direction).
[CellIdentityCdma](../android.telephony/CellIdentityCdma.md) CellIdentity is to represent a unique CDMA cell
[CellIdentityGsm](../android.telephony/CellIdentityGsm.md) CellIdentity to represent a unique GSM cell
[CellIdentityLte](../android.telephony/CellIdentityLte.md) CellIdentity is to represent a unique LTE cell
[CellIdentityNr](../android.telephony/CellIdentityNr.md) Information to represent a unique NR(New Radio 5G) cell.
[CellIdentityTdscdma](../android.telephony/CellIdentityTdscdma.md) CellIdentity is to represent a unique TD-SCDMA cell
[CellIdentityWcdma](../android.telephony/CellIdentityWcdma.md) CellIdentity to represent a unique UMTS cell
[CellInfoCdma](../android.telephony/CellInfoCdma.md) A `https://developer.android.com/reference/kotlin/android/telephony/CellInfo.html#` representing a CDMA cell that provides identity and measurement info.
[CellInfoGsm](../android.telephony/CellInfoGsm.md) A `https://developer.android.com/reference/kotlin/android/telephony/CellInfo.html#` representing a GSM cell that provides identity and measurement info.
[CellInfoLte](../android.telephony/CellInfoLte.md) A `https://developer.android.com/reference/kotlin/android/telephony/CellInfo.html#` representing an LTE cell that provides identity and measurement info.
[CellInfoNr](../android.telephony/CellInfoNr.md) A `https://developer.android.com/reference/kotlin/android/telephony/CellInfo.html#` representing an 5G NR cell that provides identity and measurement info.
[CellInfoTdscdma](../android.telephony/CellInfoTdscdma.md) A `https://developer.android.com/reference/kotlin/android/telephony/CellInfo.html#` representing a TD-SCDMA cell that provides identity and measurement info.
[CellInfoWcdma](../android.telephony/CellInfoWcdma.md) A `https://developer.android.com/reference/kotlin/android/telephony/CellInfo.html#` representing a WCDMA cell that provides identity and measurement info.
[CommandRequest](../android.media.tv/CommandRequest.md) A request for command from broadcast signal.
[CommandResponse](../android.media.tv/CommandResponse.md) A response for command from broadcast signal.
[ConnectEvent](../android.app.admin/ConnectEvent.md) A class that represents a TCP connect event initiated through the standard network stack.
[DnsEvent](../android.app.admin/DnsEvent.md) A class that represents a DNS lookup event initiated through the standard network stack.
[DsmccRequest](../android.media.tv/DsmccRequest.md) A request for DSM-CC from broadcast signal.
[DsmccResponse](../android.media.tv/DsmccResponse.md) A response for DSM-CC from broadcast signal.
[EasyEditSpan](../android.text.style/EasyEditSpan.md) Provides an easy way to edit a portion of text.
[ForegroundColorSpan](../android.text.style/ForegroundColorSpan.md) Changes the color of the text to which the span is attached.
[KeyEvent](../android.view/KeyEvent.md) Object used to report key and button events.
[LabeledIntent](../android.content.pm/LabeledIntent.md) A special subclass of Intent that can have a custom label/icon associated with it.
[LeadingMarginSpan.Standard](../android/text/style/LeadingMarginSpan.Standard.md) The standard implementation of LeadingMarginSpan, which adjusts the margin but does not do any rendering.
[LineBackgroundSpan.Standard](../android/text/style/LineBackgroundSpan.Standard.md) Default implementation of the `https://developer.android.com/reference/kotlin/android/text/style/LineBackgroundSpan.html#`, which changes the background color of the lines to which the span is attached.
[LineBreakConfigSpan](../android.text.style/LineBreakConfigSpan.md) LineBreakSpan for changing line break style of the specific region of the text.
[LineHeightSpan.Standard](../android/text/style/LineHeightSpan.Standard.md) Default implementation of the `https://developer.android.com/reference/kotlin/android/text/style/LineHeightSpan.html#`, which changes the line height of the attached paragraph.
[LocaleSpan](../android.text.style/LocaleSpan.md) Changes the `https://developer.android.com/reference/kotlin/java/util/Locale.html#` of the text to which the span is attached.
[MotionEvent](../android.view/MotionEvent.md) Object used to report movement (mouse, pen, finger, trackball) events.
[NoWritingToolsSpan](../android.text.style/NoWritingToolsSpan.md) A span that signals to IMEs that writing tools should not modify the text.
[OobInitiatorRangingConfig](../android.ranging.oob/OobInitiatorRangingConfig.md) Represents the configuration for an Out-of-Band (OOB) initiator in a ranging session.
[OobResponderRangingConfig](../android.ranging.oob/OobResponderRangingConfig.md) Represents the configuration for an Out-of-Band (OOB) responder in a ranging session.
[PathPermission](../android.content.pm/PathPermission.md) Description of permissions needed to access a particular path in a `https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo.html#`.
[PesRequest](../android.media.tv/PesRequest.md) A request for PES from broadcast signal.
[PesResponse](../android.media.tv/PesResponse.md) A response for PES from broadcast signal.
[Preference.BaseSavedState](../android/preference/Preference.BaseSavedState.md) A base class for managing the instance state of a `https://developer.android.com/reference/kotlin/android/preference/Preference.html#`.
[QuoteSpan](../android.text.style/QuoteSpan.md) A span which styles paragraphs by adding a vertical stripe at the beginning of the text (respecting layout direction).
[RawDtTagRangingConfig](../android/ranging/raw/RawDtTagRangingConfig.md) <br />

[RawInitiatorRangingConfig](../android.ranging.raw/RawInitiatorRangingConfig.md) Represents the configuration for initiating a raw ranging session.
[RawResponderRangingConfig](../android.ranging.raw/RawResponderRangingConfig.md) Represents the configuration for a raw ranging session initiated by a responder device.
[RelativeSizeSpan](../android.text.style/RelativeSizeSpan.md) Uniformly scales the size of the text to which it's attached by a certain proportion.
[ScaleXSpan](../android.text.style/ScaleXSpan.md) Scales horizontally the size of the text to which it's attached by a certain factor.
[SectionRequest](../android.media.tv/SectionRequest.md) A request for Section from broadcast signal.
[SectionResponse](../android.media.tv/SectionResponse.md) A response for Section from broadcast signal.
[SignalingDataRequest](../android.media.tv/SignalingDataRequest.md) Request to retrieve the Low-level Signalling Tables (LLS) and Service-layer Signalling (SLS) metadata.
[SignalingDataResponse](../android.media.tv/SignalingDataResponse.md) A response for the signaling data from the broadcast signal.
[StreamEventRequest](../android.media.tv/StreamEventRequest.md) A request for Stream Event from broadcast signal.
[StreamEventResponse](../android.media.tv/StreamEventResponse.md) A response for Stream Event from broadcast signal.
[StrikethroughSpan](../android.text.style/StrikethroughSpan.md) A span that strikes through the text it's attached to.
[StyleSpan](../android.text.style/StyleSpan.md) Span that allows setting the style of the text it's attached to.
[SubscriptSpan](../android.text.style/SubscriptSpan.md) The span that moves the position of the text baseline lower.
[SuggestionRangeSpan](../android.text.style/SuggestionRangeSpan.md) A SuggestionRangeSpan is used to show which part of an EditText is affected by a suggestion popup window.
[SuggestionSpan](../android.text.style/SuggestionSpan.md) Holds suggestion candidates for the text enclosed in this span.
[SuperscriptSpan](../android.text.style/SuperscriptSpan.md) The span that moves the position of the text baseline higher.
[SupplicantState.ASSOCIATED](../android.net.wifi/SupplicantState.md) Association completed.
[SupplicantState.ASSOCIATING](../android.net.wifi/SupplicantState.md) Trying to associate with a BSS/SSID.
[SupplicantState.AUTHENTICATING](../android.net.wifi/SupplicantState.md) Trying to authenticate with a BSS/SSID
[SupplicantState.COMPLETED](../android.net.wifi/SupplicantState.md) All authentication completed.
[SupplicantState.DISCONNECTED](../android.net.wifi/SupplicantState.md) This state indicates that client is not associated, but is likely to start looking for an access point.
[SupplicantState.DORMANT](../android.net.wifi/SupplicantState.md) An Android-added state that is reported when a client issues an explicit DISCONNECT command.
[SupplicantState.FOUR_WAY_HANDSHAKE](../android.net.wifi/SupplicantState.md) WPA 4-Way Key Handshake in progress.
[SupplicantState.GROUP_HANDSHAKE](../android.net.wifi/SupplicantState.md) WPA Group Key Handshake in progress.
[SupplicantState.INACTIVE](../android.net.wifi/SupplicantState.md) Inactive state (wpa_supplicant disabled).
[SupplicantState.INTERFACE_DISABLED](../android.net.wifi/SupplicantState.md) Interface is disabled
[SupplicantState.INVALID](../android.net.wifi/SupplicantState.md) A pseudo-state that should normally never be seen.
[SupplicantState.SCANNING](../android.net.wifi/SupplicantState.md) Scanning for a network.
[SupplicantState.UNINITIALIZED](../android.net.wifi/SupplicantState.md) No connection to wpa_supplicant.
[TableRequest](../android.media.tv/TableRequest.md) A request for Table from broadcast signal.
[TableResponse](../android.media.tv/TableResponse.md) A response for Table from broadcast signal.
[TextAppearanceSpan](../android.text.style/TextAppearanceSpan.md) Sets the text appearance using the given `https://developer.android.com/reference/kotlin/android/R.styleable.html#TextAppearance:kotlin.IntArray` attributes.
[TextClassifierEvent.ConversationActionsEvent](../android/view/textclassifier/TextClassifierEvent.ConversationActionsEvent.md) This class represents events that are related to the conversation actions feature.
[TextClassifierEvent.LanguageDetectionEvent](../android/view/textclassifier/TextClassifierEvent.LanguageDetectionEvent.md) This class represents events that are related to the language detection feature.
[TextClassifierEvent.TextLinkifyEvent](../android/view/textclassifier/TextClassifierEvent.TextLinkifyEvent.md) This class represents events that are related to the smart linkify feature.
[TextClassifierEvent.TextSelectionEvent](../android/view/textclassifier/TextClassifierEvent.TextSelectionEvent.md) This class represents events that are related to the smart text selection feature.
[TextView.SavedState](../android/widget/TextView.SavedState.md) User interface state that is stored by TextView for implementing onSaveInstanceState.
[TimelineRequest](../android.media.tv/TimelineRequest.md) A request for Timeline from broadcast signal.
[TimelineResponse](../android.media.tv/TimelineResponse.md) A response for Timeline from broadcast signal.
[TsRequest](../android.media.tv/TsRequest.md) A request for TS (transport stream) from broadcast signal.
[TsResponse](../android.media.tv/TsResponse.md) A response for TS (transport stream) from broadcast signal.
[TtsSpan](../android.text.style/TtsSpan.md) A span that supplies additional meta-data for the associated text intended for text-to-speech engines.
[TypefaceSpan](../android.text.style/TypefaceSpan.md) Span that updates the typeface of the text it's attached to.
[URLSpan](../android.text.style/URLSpan.md) Implementation of the `https://developer.android.com/reference/kotlin/android/text/style/ClickableSpan.html#` that allows setting a url string.
[UnderlineSpan](../android.text.style/UnderlineSpan.md) A span that underlines the text it's attached to.
[VerifiedKeyEvent](../android.view/VerifiedKeyEvent.md) KeyEvent that has been verified by the system.
[VerifiedMotionEvent](../android.view/VerifiedMotionEvent.md) MotionEvent that has been verified by the system.
[View.BaseSavedState](../android/view/View.BaseSavedState.md) Base class for derived classes that want to save and restore their own state in onSaveInstanceState.
[WifiDeviceFilter](../android.companion/WifiDeviceFilter.md) A filter for Wifi devices
[WifiP2pDnsSdServiceInfo](../android.net.wifi.p2p.nsd/WifiP2pDnsSdServiceInfo.md) A class for storing Bonjour service information that is advertised over a Wi-Fi peer-to-peer setup.
[WifiP2pDnsSdServiceRequest](../android.net.wifi.p2p.nsd/WifiP2pDnsSdServiceRequest.md) A class for creating a Bonjour service discovery request for use with addServiceRequest and removeServiceRequest
[WifiP2pUpnpServiceInfo](../android.net.wifi.p2p.nsd/WifiP2pUpnpServiceInfo.md) A class for storing Upnp service information that is advertised over a Wi-Fi peer-to-peer setup.
[WifiP2pUpnpServiceRequest](../android.net.wifi.p2p.nsd/WifiP2pUpnpServiceRequest.md) A class for creating a Upnp service discovery request for use with addServiceRequest and removeServiceRequest

Interface for classes whose instances can be written to and restored from a Parcel. Classes implementing the Parcelable interface must also have a non-null public static field called `CREATOR` of a type that implements the `https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator` interface.

A typical implementation of Parcelable is:

### Kotlin

```kotlin
class MyParcelable private constructor(`in`: Parcel) : Parcelable {
      private val mData: Int = `in`.readInt()
 
      override fun describeContents(): Int {
          return 0
      }
 
      override fun writeToParcel(out: Parcel, flags: Int) {
          out.writeInt(mData)
      }
 
      companion object CREATOR: Parcelable.Creator<MyParcelable?> {
          override fun createFromParcel(`in`: Parcel): MyParcelable? {
              return MyParcelable(`in`)
          }
 
          override fun newArray(size: Int): Array<MyParcelable?> {
              return arrayOfNulls(size)
          }
      }
  }
  
```

### Java

```kotlin
public class MyParcelable implements Parcelable {
      private int mData;
 
      public int describeContents() {
          return 0;
      }
 
      public void writeToParcel(Parcel out, int flags) {
          out.writeInt(mData);
      }
 
      public static final Parcelable.Creator<MyParcelable> CREATOR
              = new Parcelable.Creator<MyParcelable>() {
          public MyParcelable createFromParcel(Parcel in) {
              return new MyParcelable(in);
          }
 
          public MyParcelable[] newArray(int size) {
              return new MyParcelable[size];
          }
      };
 
      private MyParcelable(Parcel in) {
          mData = in.readInt();
      }
  }
```

<br />

<br />

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/os/Parcelable.ClassLoaderCreator` Specialization of `https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator` that allows you to receive the ClassLoader the object is being created in. |
| abstract | `https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator` Interface that must be implemented and provided as a public CREATOR field that generates instances of your Parcelable class from a Parcel. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". |

| Public methods ||
|---|---|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

## Constants

### CONTENTS_FILE_DESCRIPTOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTENTS_FILE_DESCRIPTOR: Int
```

Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor.

 Value: 1

**See Also**

- describeContents

### PARCELABLE_WRITE_RETURN_VALUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARCELABLE_WRITE_RETURN_VALUE: Int
```

Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

 Value: 1

## Public methods

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |
