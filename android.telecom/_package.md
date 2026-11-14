# android.telecom

## Interfaces

| [CallControlCallback](CallControlCallback.md) | CallControlCallback relays call updates (that require a response) from the Telecom framework out to the application. |
| --- | --- |
| [CallEventCallback](CallEventCallback.md) | CallEventCallback relays call updates (that do not require any action) from the Telecom framework out to the application. |

## Classes

| [Call](Call.md) | Represents an ongoing phone call that the in-call app should present to the user. |
| --- | --- |
| [CallAttributes](CallAttributes.md) | CallAttributes represents a set of properties that define a new Call. |
| [CallAudioState](CallAudioState.md) | Encapsulates the telecom audio state, including the current audio routing, supported audio routing and mute. |
| [CallControl](CallControl.md) | CallControl provides client side control of a call. |
| --- | --- |
| [CallEndpoint](CallEndpoint.md) | Encapsulates the endpoint where call media can flow |
| [CallRedirectionService](CallRedirectionService.md) | This service can be implemented to interact between Telecom and its implementor for making outgoing call with optional redirection/cancellation purposes. |
| [CallScreeningService](CallScreeningService.md) | This service can be implemented by the default dialer (see getDefaultDialerPackage) or a third party app to allow or disallow incoming calls before they are shown to a user. |
| --- | --- |
| [Conference](Conference.md) | Represents a conference call which can contain any number of Connection objects. |
| [Conferenceable](Conferenceable.md) | Interface used to identify entities with which another entity can participate in a conference call with. |
| [Connection](Connection.md) | Represents a phone call or connection to a remote endpoint that carries voice and/or video traffic. |
| --- | --- |
| [ConnectionRequest](ConnectionRequest.md) | Simple data container encapsulating a request to some entity to create a new Connection. |
| [ConnectionService](ConnectionService.md) | An abstract service that should be implemented by any apps which either: 1. Can make phone calls (VoIP or otherwise) and want those calls to be integrated into the built-in phone app. Referred to as a **system managed** ConnectionService. 2. Are a standalone calling app and don't want their calls to be integrated into the built-in phone app. Referred to as a **self managed** ConnectionService. Once implemented, the needs to take the following steps so that Telecom will bind to it: <br /> |
| [DisconnectCause](DisconnectCause.md) | Describes the cause of a disconnected call. |
| --- | --- |
| [GatewayInfo](GatewayInfo.md) | Encapsulated gateway address information for outgoing call. |
| [InCallService](InCallService.md) | This service is implemented by an app that wishes to provide functionality for managing phone calls. |
| [PhoneAccount](PhoneAccount.md) | Represents a distinct method to place or receive a phone call. |
| --- | --- |
| [PhoneAccountHandle](PhoneAccountHandle.md) | The unique identifier for a PhoneAccount. |
| [PhoneAccountSuggestion](PhoneAccountSuggestion.md) | <br /> |
| [RemoteConference](RemoteConference.md) | A conference provided to a ConnectionService by another `ConnectionService` through conferenceRemoteConnections. |
| --- | --- |
| [RemoteConnection](RemoteConnection.md) | A connection provided to a ConnectionService by another `ConnectionService` running in a different process. |
| [StatusHints](StatusHints.md) | Contains status label and icon displayed in the in-call UI. |
| [TelecomManager](TelecomManager.md) | The Android Telecom framework manages audio and video calls on an Android device. |
| --- | --- |
| [VideoProfile](VideoProfile.md) | Represents attributes of video calls. |

## Exceptions

| [CallEndpointException](CallEndpointException.md) | This class represents a set of exceptions that can occur when requesting a CallEndpoint change. |
| --- | --- |
| [CallException](CallException.md) | This class defines exceptions that can be thrown when using Telecom APIs with `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#`s. |
| [QueryLocationException](QueryLocationException.md) | This class represents a set of exceptions that can occur when requesting a queryLocationForEmergency |
