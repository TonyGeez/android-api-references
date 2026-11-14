# android.service.carrier

# android.service.carrier

Kotlin| [Java](https://developer.android.com/reference/android/service/carrier/package-summary "View this page in Java")
| --- | --- |

## Interfaces

| [ResultCallback](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierMessagingService.ResultCallback) | A callback interface used to provide results asynchronously. |
| --- | --- |

## Classes

| [CarrierIdentifier](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierIdentifier) | Used to pass info to CarrierConfigService implementations so they can decide what values to return. |
| --- | --- |
| [CarrierMessagingClientService](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierMessagingClientService) | If the default SMS app has a service that extends this class, the system always tries to bind it so that the process is always running, which allows the app to have a persistent connection to the server. |
| [CarrierMessagingService](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierMessagingService) | A service that receives calls from the system when new SMS and MMS are sent or received. |
| [CarrierService](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierService) | A service that exposes carrier-specific functionality to the system. |
| --- | --- |
| [MessagePdu](https://developer.android.com/reference/kotlin/android/service/carrier/MessagePdu) | A parcelable list of PDUs representing contents of a possibly multi-part SMS. |
