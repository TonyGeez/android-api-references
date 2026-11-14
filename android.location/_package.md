# android.location

# android.location

Kotlin| [Java](https://developer.android.com/reference/android/location/package-summary "View this page in Java")
| --- | --- |

## Interfaces

| [GeocodeListener](https://developer.android.com/reference/kotlin/android/location/Geocoder.GeocodeListener) | A listener for asynchronous geocoding results. |
| --- | --- |
| [Listener](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.Listener) | Used for receiving GNSS antenna info from the GNSS engine. |
| [Listener](https://developer.android.com/reference/kotlin/android/location/GpsStatus.Listener) | Used for receiving notifications when GPS status has changed. |
| [NmeaListener](https://developer.android.com/reference/kotlin/android/location/GpsStatus.NmeaListener) | Used for receiving NMEA sentences from the GPS. |
| --- | --- |
| [LocationListener](https://developer.android.com/reference/kotlin/android/location/LocationListener) | Used for receiving notifications when the device location has changed. |
| [OnNmeaMessageListener](https://developer.android.com/reference/kotlin/android/location/OnNmeaMessageListener) | Used for receiving NMEA sentences from the GNSS. |

## Classes

| [Address](https://developer.android.com/reference/kotlin/android/location/Address) | A class representing an Address, that is, a set of Strings describing a location. |
| --- | --- |
| [Criteria](https://developer.android.com/reference/kotlin/android/location/Criteria) | A class indicating the application criteria for selecting a location provider. |
| [Geocoder](https://developer.android.com/reference/kotlin/android/location/Geocoder) | A class for handling geocoding and reverse geocoding. |
| [GnssAntennaInfo](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo) | A class that contains information about a GNSS antenna. |
| --- | --- |
| [GnssAutomaticGainControl](https://developer.android.com/reference/kotlin/android/location/GnssAutomaticGainControl) | A class that contains GNSS Automatic Gain Control (AGC) information. |
| [GnssCapabilities](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities) | GNSS chipset capabilities. |
| [GnssClock](https://developer.android.com/reference/kotlin/android/location/GnssClock) | A class containing a GNSS clock timestamp. |
| --- | --- |
| [GnssMeasurement](https://developer.android.com/reference/kotlin/android/location/GnssMeasurement) | A class representing a GNSS satellite measurement, containing raw and computed information. |
| [GnssMeasurementRequest](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementRequest) | This class contains extra parameters to pass in a GNSS measurement request. |
| [GnssMeasurementsEvent](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent) | A class implementing a container for data associated with a measurement event. |
| --- | --- |
| [GnssNavigationMessage](https://developer.android.com/reference/kotlin/android/location/GnssNavigationMessage) | A class containing a GNSS satellite Navigation Message. |
| [GnssSignalType](https://developer.android.com/reference/kotlin/android/location/GnssSignalType) | This class represents a GNSS signal type. |
| [GnssStatus](https://developer.android.com/reference/kotlin/android/location/GnssStatus) | This class represents the current state of the GNSS engine and is used in conjunction with [GnssStatus.Callback](https://developer.android.com/reference/kotlin/android/location/GnssStatus.Callback). |
| --- | --- |
| [GpsSatellite](https://developer.android.com/reference/kotlin/android/location/GpsSatellite) | This class represents the current state of a GPS satellite. |
| [GpsStatus](https://developer.android.com/reference/kotlin/android/location/GpsStatus) | This class represents the current state of the GPS engine and is used in conjunction with [GpsStatus.Listener](https://developer.android.com/reference/kotlin/android/location/GpsStatus.Listener). |
| [Location](https://developer.android.com/reference/kotlin/android/location/Location) | A data class representing a geographic location. |
| --- | --- |
| [LocationManager](https://developer.android.com/reference/kotlin/android/location/LocationManager) | This class provides access to the system location services. |
| [LocationProvider](https://developer.android.com/reference/kotlin/android/location/LocationProvider) | Information about the properties of a location provider. |
| [LocationRequest](https://developer.android.com/reference/kotlin/android/location/LocationRequest) | An encapsulation of various parameters for requesting location via [LocationManager](https://developer.android.com/reference/kotlin/android/location/LocationManager). |
| --- | --- |
| [SettingInjectorService](https://developer.android.com/reference/kotlin/android/location/SettingInjectorService) | Dynamically specifies the summary (subtitle) and enabled status of a preference injected into the list of app settings displayed by the system settings app |
