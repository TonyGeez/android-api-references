# android.companion

## Interfaces

| [DeviceFilter](https://developer.android.com/reference/kotlin/android/companion/DeviceFilter) | A filter for companion devices of type `D` |
| --- | --- |

## Classes

| [ActionRequest](https://developer.android.com/reference/kotlin/android/companion/ActionRequest) | Represents a request for a companion app to perform a specific action. |
| --- | --- |
| [ActionResult](https://developer.android.com/reference/kotlin/android/companion/ActionResult) | A result reported by a companion app in response to an `https://developer.android.com/reference/kotlin/android/companion/ActionRequest`. |
| [AssociatedDevice](https://developer.android.com/reference/kotlin/android/companion/AssociatedDevice) | Container for device info from an association that is not self-managed. |
| [AssociationInfo](https://developer.android.com/reference/kotlin/android/companion/AssociationInfo) | Details for a specific "association" that has been established between an app and companion device. |
| --- | --- |
| [AssociationRequest](https://developer.android.com/reference/kotlin/android/companion/AssociationRequest) | A request for the user to select a companion device to associate with. |
| [BluetoothDeviceFilter](https://developer.android.com/reference/kotlin/android/companion/BluetoothDeviceFilter) | A filter for Bluetooth(non-LE) devices |
| [BluetoothLeDeviceFilter](https://developer.android.com/reference/kotlin/android/companion/BluetoothLeDeviceFilter) | A filter for Bluetooth LE devices |
| --- | --- |
| [CompanionDeviceManager](https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager) | Public interfaces for managing companion devices. |
| [CompanionDeviceService](https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceService) | A service that receives calls from the system with device events. |
| [DeviceId](https://developer.android.com/reference/kotlin/android/companion/DeviceId) | A device id represents a device identifier managed by the companion app. |
| --- | --- |
| [DevicePresenceEvent](https://developer.android.com/reference/kotlin/android/companion/DevicePresenceEvent) | Event for observing device presence. |
| [ObservingDevicePresenceRequest](https://developer.android.com/reference/kotlin/android/companion/ObservingDevicePresenceRequest) | A request for setting the types of device for observing device presence. |
| [OutOfBandPairingRequest](https://developer.android.com/reference/kotlin/android/companion/OutOfBandPairingRequest) | Represents a request for out-of-band pairing. |
| --- | --- |
| [WifiDeviceFilter](https://developer.android.com/reference/kotlin/android/companion/WifiDeviceFilter) | A filter for Wifi devices |

## Exceptions

| [CompanionException](https://developer.android.com/reference/kotlin/android/companion/CompanionException) | `CompanionException` can be thrown during the companion system data transfer process. |
| --- | --- |
| [DeviceNotAssociatedException](https://developer.android.com/reference/kotlin/android/companion/DeviceNotAssociatedException) | An exception for a case when a given device was not android. |
