# android.companion

## Interfaces

| [DeviceFilter](DeviceFilter.md) | A filter for companion devices of type `D` |
| --- | --- |

## Classes

| [ActionRequest](../android/companion/ActionRequest.md) | Represents a request for a companion app to perform a specific action. |
| --- | --- |
| [ActionResult](ActionResult.md) | A result reported by a companion app in response to an `https://developer.android.com/reference/kotlin/android/companion/ActionRequest`. |
| [AssociatedDevice](AssociatedDevice.md) | Container for device info from an association that is not self-managed. |
| [AssociationInfo](AssociationInfo.md) | Details for a specific "association" that has been established between an app and companion device. |
| --- | --- |
| [AssociationRequest](AssociationRequest.md) | A request for the user to select a companion device to associate with. |
| [BluetoothDeviceFilter](BluetoothDeviceFilter.md) | A filter for Bluetooth(non-LE) devices |
| [BluetoothLeDeviceFilter](BluetoothLeDeviceFilter.md) | A filter for Bluetooth LE devices |
| --- | --- |
| [CompanionDeviceManager](CompanionDeviceManager.md) | Public interfaces for managing companion devices. |
| [CompanionDeviceService](CompanionDeviceService.md) | A service that receives calls from the system with device events. |
| [DeviceId](DeviceId.md) | A device id represents a device identifier managed by the companion app. |
| --- | --- |
| [DevicePresenceEvent](DevicePresenceEvent.md) | Event for observing device presence. |
| [ObservingDevicePresenceRequest](ObservingDevicePresenceRequest.md) | A request for setting the types of device for observing device presence. |
| [OutOfBandPairingRequest](OutOfBandPairingRequest.md) | Represents a request for out-of-band pairing. |
| --- | --- |
| [WifiDeviceFilter](WifiDeviceFilter.md) | A filter for Wifi devices |

## Exceptions

| [CompanionException](CompanionException.md) | `CompanionException` can be thrown during the companion system data transfer process. |
| --- | --- |
| [DeviceNotAssociatedException](DeviceNotAssociatedException.md) | An exception for a case when a given device was not android. |
