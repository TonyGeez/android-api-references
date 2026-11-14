# android.telecom

## Interfaces

| [CallControlCallback](https://developer.android.com/reference/kotlin/android/telecom/CallControlCallback) | CallControlCallback relays call updates (that require a response) from the Telecom framework out to the application. |
| [CallEventCallback](https://developer.android.com/reference/kotlin/android/telecom/CallEventCallback) | CallEventCallback relays call updates (that do not require any action) from the Telecom framework out to the application. |

## Classes

| [Call](https://developer.android.com/reference/kotlin/android/telecom/Call) | Represents an ongoing phone call that the in-call app should present to the user. |
| [CallAttributes](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes) | CallAttributes represents a set of properties that define a new Call. |
| [CallAudioState](https://developer.android.com/reference/kotlin/android/telecom/CallAudioState) | Encapsulates the telecom audio state, including the current audio routing, supported audio routing and mute. |
| [CallControl](https://developer.android.com/reference/kotlin/android/telecom/CallControl) | CallControl provides client side control of a call. |
| [CallEndpoint](https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint) | Encapsulates the endpoint where call media can flow |
| [CallRedirectionService](https://developer.android.com/reference/kotlin/android/telecom/CallRedirectionService) | This service can be implemented to interact between Telecom and its implementor for making outgoing call with optional redirection/cancellation purposes. |
| [CallScreeningService](https://developer.android.com/reference/kotlin/android/telecom/CallScreeningService) | This service can be implemented by the default dialer (see `https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#getDefaultDialerPackage()`) or a third party app to allow or disallow incoming calls before they are shown to a user. |
| [Conference](https://developer.android.com/reference/kotlin/android/telecom/Conference) | Represents a conference call which can contain any number of `https://developer.android.com/reference/kotlin/android/telecom/Connection` objects. |
| [Conferenceable](https://developer.android.com/reference/kotlin/android/telecom/Conferenceable) | Interface used to identify entities with which another entity can participate in a conference call with. |
| [Connection](https://developer.android.com/reference/kotlin/android/telecom/Connection) | Represents a phone call or connection to a remote endpoint that carries voice and/or video traffic. |
| [ConnectionRequest](https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest) | Simple data container encapsulating a request to some entity to create a new `https://developer.android.com/reference/kotlin/android/telecom/Connection`. |
| [ConnectionService](https://developer.android.com/reference/kotlin/android/telecom/ConnectionService) | An abstract service that should be implemented by any apps which either: 1. Can make phone calls (VoIP or otherwise) and want those calls to be integrated into the built-in phone app. Referred to as a **system managed** `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`. 2. Are a standalone calling app and don't want their calls to be integrated into the built-in phone app. Referred to as a **self managed** `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService`. Once implemented, the needs to take the following steps so that Telecom will bind to it: <br /> |
| [DisconnectCause](https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause) | Describes the cause of a disconnected call. |
| [GatewayInfo](https://developer.android.com/reference/kotlin/android/telecom/GatewayInfo) | Encapsulated gateway address information for outgoing call. |
| [InCallService](https://developer.android.com/reference/kotlin/android/telecom/InCallService) | This service is implemented by an app that wishes to provide functionality for managing phone calls. |
| [PhoneAccount](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount) | Represents a distinct method to place or receive a phone call. |
| [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle) | The unique identifier for a `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount`. |
| [PhoneAccountSuggestion](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountSuggestion) | <br /> |
| [RemoteConference](https://developer.android.com/reference/kotlin/android/telecom/RemoteConference) | A conference provided to a `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` by another `ConnectionService` through `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService#conferenceRemoteConnections(android.telecom.RemoteConnection,%20android.telecom.RemoteConnection)`. |
| [RemoteConnection](https://developer.android.com/reference/kotlin/android/telecom/RemoteConnection) | A connection provided to a `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` by another `ConnectionService` running in a different process. |
| [StatusHints](https://developer.android.com/reference/kotlin/android/telecom/StatusHints) | Contains status label and icon displayed in the in-call UI. |
| [TelecomManager](https://developer.android.com/reference/kotlin/android/telecom/TelecomManager) | The Android Telecom framework manages audio and video calls on an Android device. |
| [VideoProfile](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile) | Represents attributes of video calls. |

## Exceptions

| [CallEndpointException](https://developer.android.com/reference/kotlin/android/telecom/CallEndpointException) | This class represents a set of exceptions that can occur when requesting a `https://developer.android.com/reference/kotlin/android/telecom/CallEndpoint` change. |
| [CallException](https://developer.android.com/reference/kotlin/android/telecom/CallException) | This class defines exceptions that can be thrown when using Telecom APIs with `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#`s. |
| [QueryLocationException](https://developer.android.com/reference/kotlin/android/telecom/QueryLocationException) | This class represents a set of exceptions that can occur when requesting a `https://developer.android.com/reference/kotlin/android/telecom/Connection#queryLocationForEmergency(kotlin.Long,%20kotlin.String,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` |
