# android.location

# android.location

Kotlin| [Java](../android/location/_package.md)
| --- | --- |

## Interfaces

| [GeocodeListener](../android/location/Geocoder.GeocodeListener.md) | A listener for asynchronous geocoding results. |
| --- | --- |
| [Listener](../android/location/GnssAntennaInfo.Listener.md) | Used for receiving GNSS antenna info from the GNSS engine. |
| [Listener](../android/location/GpsStatus.Listener.md) | Used for receiving notifications when GPS status has changed. |
| [NmeaListener](../android/location/GpsStatus.NmeaListener.md) | Used for receiving NMEA sentences from the GPS. |
| --- | --- |
| [LocationListener](../android/location/LocationListener.md) | Used for receiving notifications when the device location has changed. |
| [OnNmeaMessageListener](../android/location/OnNmeaMessageListener.md) | Used for receiving NMEA sentences from the GNSS. |

## Classes

| [Address](../android/location/Address.md) | A class representing an Address, that is, a set of Strings describing a location. |
| --- | --- |
| [Criteria](../android/location/Criteria.md) | A class indicating the application criteria for selecting a location provider. |
| [Geocoder](../android/location/Geocoder.md) | A class for handling geocoding and reverse geocoding. |
| [GnssAntennaInfo](../android/location/GnssAntennaInfo.md) | A class that contains information about a GNSS antenna. |
| --- | --- |
| [GnssAutomaticGainControl](../android/location/GnssAutomaticGainControl.md) | A class that contains GNSS Automatic Gain Control (AGC) information. |
| [GnssCapabilities](../android/location/GnssCapabilities.md) | GNSS chipset capabilities. |
| [GnssClock](../android/location/GnssClock.md) | A class containing a GNSS clock timestamp. |
| --- | --- |
| [GnssMeasurement](../android/location/GnssMeasurement.md) | A class representing a GNSS satellite measurement, containing raw and computed information. |
| [GnssMeasurementRequest](../android/location/GnssMeasurementRequest.md) | This class contains extra parameters to pass in a GNSS measurement request. |
| [GnssMeasurementsEvent](../android/location/GnssMeasurementsEvent.md) | A class implementing a container for data associated with a measurement event. |
| --- | --- |
| [GnssNavigationMessage](../android/location/GnssNavigationMessage.md) | A class containing a GNSS satellite Navigation Message. |
| [GnssSignalType](../android/location/GnssSignalType.md) | This class represents a GNSS signal type. |
| [GnssStatus](../android/location/GnssStatus.md) | This class represents the current state of the GNSS engine and is used in conjunction with [GnssStatus.Callback](../android/location/GnssStatus.Callback.md). |
| --- | --- |
| [GpsSatellite](../android/location/GpsSatellite.md) | This class represents the current state of a GPS satellite. |
| [GpsStatus](../android/location/GpsStatus.md) | This class represents the current state of the GPS engine and is used in conjunction with [GpsStatus.Listener](../android/location/GpsStatus.Listener.md). |
| [Location](../android/location/Location.md) | A data class representing a geographic location. |
| --- | --- |
| [LocationManager](../android/location/LocationManager.md) | This class provides access to the system location services. |
| [LocationProvider](../android/location/LocationProvider.md) | Information about the properties of a location provider. |
| [LocationRequest](../android/location/LocationRequest.md) | An encapsulation of various parameters for requesting location via [LocationManager](../android/location/LocationManager.md). |
| --- | --- |
| [SettingInjectorService](../android/location/SettingInjectorService.md) | Dynamically specifies the summary (subtitle) and enabled status of a preference injected into the list of app settings displayed by the system settings app |
