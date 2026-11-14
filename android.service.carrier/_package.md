# android.service.carrier

# android.service.carrier

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [ResultCallback](../android/service/carrier/CarrierMessagingService.ResultCallback.md) | A callback interface used to provide results asynchronously. |
| --- | --- |

## Classes

| [CarrierIdentifier](CarrierIdentifier.md) | Used to pass info to CarrierConfigService implementations so they can decide what values to return. |
| --- | --- |
| [CarrierMessagingClientService](CarrierMessagingClientService.md) | If the default SMS app has a service that extends this class, the system always tries to bind it so that the process is always running, which allows the app to have a persistent connection to the server. |
| [CarrierMessagingService](CarrierMessagingService.md) | A service that receives calls from the system when new SMS and MMS are sent or received. |
| [CarrierService](CarrierService.md) | A service that exposes carrier-specific functionality to the system. |
| --- | --- |
| [MessagePdu](MessagePdu.md) | A parcelable list of PDUs representing contents of a possibly multi-part SMS. |
