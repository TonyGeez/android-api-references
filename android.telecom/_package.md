# android.telecom

## Interfaces

| [CallControlCallback](../android/telecom/CallControlCallback.md) | CallControlCallback relays call updates (that require a response) from the Telecom framework out to the application. |
| --- | --- |
| [CallEventCallback](../android/telecom/CallEventCallback.md) | CallEventCallback relays call updates (that do not require any action) from the Telecom framework out to the application. |

## Classes

| [Call](../android/telecom/Call.md) | Represents an ongoing phone call that the in-call app should present to the user. |
| --- | --- |
| [CallAttributes](../android/telecom/CallAttributes.md) | CallAttributes represents a set of properties that define a new Call. |
| [CallAudioState](../android/telecom/CallAudioState.md) | Encapsulates the telecom audio state, including the current audio routing, supported audio routing and mute. |
| [CallControl](../android/telecom/CallControl.md) | CallControl provides client side control of a call. |
| --- | --- |
| [CallEndpoint](../android/telecom/CallEndpoint.md) | Encapsulates the endpoint where call media can flow |
| [CallRedirectionService](../android/telecom/CallRedirectionService.md) | This service can be implemented to interact between Telecom and its implementor for making outgoing call with optional redirection/cancellation purposes. |
| [CallScreeningService](../android/telecom/CallScreeningService.md) | This service can be implemented by the default dialer (see `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getDefaultDialerPackage()`) or a third party app to allow or disallow incoming calls before they are shown to a user. |
| --- | --- |
| [Conference](../android/telecom/Conference.md) | Represents a conference call which can contain any number of `https://developer.android.com/reference/kotlin/android/telecom/Connection` objects. |
| [Conferenceable](../android/telecom/Conferenceable.md) | Interface used to identify entities with which another entity can participate in a conference call with. |
| [Connection](../android/telecom/Connection.md) | Represents a phone call or connection to a remote endpoint that carries voice and/or video traffic. |
| --- | --- |
| [ConnectionRequest](../android/telecom/ConnectionRequest.md) | Simple data container encapsulating a request to some entity to create a new `https://developer.android.com/reference/kotlin/android/telecom/Connection`. |
| [ConnectionService](../android/telecom/ConnectionService.md) | An abstract service that should be implemented by any apps which either: 1. Can make phone calls (VoIP or otherwise) and want those calls to be integrated into the built-in phone app. Referred to as a **system managed** `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`. 2. Are a standalone calling app and don't want their calls to be integrated into the built-in phone app. Referred to as a **self managed** `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`. Once implemented, the needs to take the following steps so that Telecom will bind to it: <br /> |
| [DisconnectCause](../android/telecom/DisconnectCause.md) | Describes the cause of a disconnected call. |
| --- | --- |
| [GatewayInfo](../android/telecom/GatewayInfo.md) | Encapsulated gateway address information for outgoing call. |
| [InCallService](../android/telecom/InCallService.md) | This service is implemented by an app that wishes to provide functionality for managing phone calls. |
| [PhoneAccount](../android/telecom/PhoneAccount.md) | Represents a distinct method to place or receive a phone call. |
| --- | --- |
| [PhoneAccountHandle](../android/telecom/PhoneAccountHandle.md) | The unique identifier for a `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount`. |
| [PhoneAccountSuggestion](../android/telecom/PhoneAccountSuggestion.md) | <br /> |
| [RemoteConference](../android/telecom/RemoteConference.md) | A conference provided to a `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` by another `ConnectionService` through `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#conferenceRemoteConnections(android.telecom.RemoteConnection,%20android.telecom.RemoteConnection)`. |
| --- | --- |
| [RemoteConnection](../android/telecom/RemoteConnection.md) | A connection provided to a `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` by another `ConnectionService` running in a different process. |
| [StatusHints](../android/telecom/StatusHints.md) | Contains status label and icon displayed in the in-call UI. |
| [TelecomManager](../android/telecom/TelecomManager.md) | The Android Telecom framework manages audio and video calls on an Android device. |
| --- | --- |
| [VideoProfile](../android/telecom/VideoProfile.md) | Represents attributes of video calls. |

## Exceptions

| [CallEndpointException](../android/telecom/CallEndpointException.md) | This class represents a set of exceptions that can occur when requesting a `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint` change. |
| --- | --- |
| [CallException](../android/telecom/CallException.md) | This class defines exceptions that can be thrown when using Telecom APIs with `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#`s. |
| [QueryLocationException](../android/telecom/QueryLocationException.md) | This class represents a set of exceptions that can occur when requesting a `https://developer.android.com/reference/kotlin/android/telecom/Connection#queryLocationForEmergency(kotlin.Long,%20kotlin.String,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` |
