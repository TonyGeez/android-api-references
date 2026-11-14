# LocationManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocationManager

Kotlin| [Java](https://developer.android.com/reference/android/location/LocationManager "View this page in Java") 

```
open class LocationManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.location.LocationManager](https://developer.android.com/reference/kotlin/android/location/LocationManager#) |

This class provides access to the system location services. These services allow applications to obtain periodic updates of the device's geographical location, or to be notified when the device enters the proximity of a given geographical location.

Unless otherwise noted, all Location API methods require the [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String) or [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String) permissions. If your application only has the coarse permission then providers will still return location results, but the exact location will be obfuscated to a coarse level of accuracy. 
Requires the [PackageManager#FEATURE_LOCATION](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_LOCATION:kotlin.String) feature which can be detected using [PackageManager.hasSystemFeature(String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_GNSS_CAPABILITIES_CHANGED](https://developer.android.com/reference/kotlin/android/location/LocationManager#ACTION_GNSS_CAPABILITIES_CHANGED:kotlin.String) Broadcast intent action when GNSS capabilities change. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_GNSS_CAPABILITIES](https://developer.android.com/reference/kotlin/android/location/LocationManager#EXTRA_GNSS_CAPABILITIES:kotlin.String) Intent extra included with [ACTION_GNSS_CAPABILITIES_CHANGED](https://developer.android.com/reference/kotlin/android/location/LocationManager#ACTION_GNSS_CAPABILITIES_CHANGED:kotlin.String) broadcasts, containing the new [GnssCapabilities](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_LOCATION_ENABLED](https://developer.android.com/reference/kotlin/android/location/LocationManager#EXTRA_LOCATION_ENABLED:kotlin.String) Intent extra included with [MODE_CHANGED_ACTION](https://developer.android.com/reference/kotlin/android/location/LocationManager#MODE_CHANGED_ACTION:kotlin.String) broadcasts, containing the boolean enabled state of location. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PROVIDER_ENABLED](https://developer.android.com/reference/kotlin/android/location/LocationManager#EXTRA_PROVIDER_ENABLED:kotlin.String) Intent extra included with [PROVIDERS_CHANGED_ACTION](https://developer.android.com/reference/kotlin/android/location/LocationManager#PROVIDERS_CHANGED_ACTION:kotlin.String) broadcasts, containing the boolean enabled state of the location provider that has changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PROVIDER_NAME](https://developer.android.com/reference/kotlin/android/location/LocationManager#EXTRA_PROVIDER_NAME:kotlin.String) Intent extra included with [PROVIDERS_CHANGED_ACTION](https://developer.android.com/reference/kotlin/android/location/LocationManager#PROVIDERS_CHANGED_ACTION:kotlin.String) broadcasts, containing the name of the location provider that has changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FUSED_PROVIDER](https://developer.android.com/reference/kotlin/android/location/LocationManager#FUSED_PROVIDER:kotlin.String) Standard name of the fused location provider. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [GPS_PROVIDER](https://developer.android.com/reference/kotlin/android/location/LocationManager#GPS_PROVIDER:kotlin.String) Standard name of the GNSS location provider. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_FLUSH_COMPLETE](https://developer.android.com/reference/kotlin/android/location/LocationManager#KEY_FLUSH_COMPLETE:kotlin.String) Key used for an extra holding an integer request code when location flush completion is sent using a PendingIntent. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_LOCATIONS](https://developer.android.com/reference/kotlin/android/location/LocationManager#KEY_LOCATIONS:kotlin.String) Key used for an extra holding a array of [Location](https://developer.android.com/reference/kotlin/android/location/Location) s when a location change is sent using a PendingIntent. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_LOCATION_CHANGED](https://developer.android.com/reference/kotlin/android/location/LocationManager#KEY_LOCATION_CHANGED:kotlin.String) Key used for an extra holding a [Location](https://developer.android.com/reference/kotlin/android/location/Location) value when a location change is sent using a PendingIntent. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_PROVIDER_ENABLED](https://developer.android.com/reference/kotlin/android/location/LocationManager#KEY_PROVIDER_ENABLED:kotlin.String) Key used for an extra holding a boolean enabled/disabled status value when a provider enabled/disabled event is broadcast using a PendingIntent. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_PROXIMITY_ENTERING](https://developer.android.com/reference/kotlin/android/location/LocationManager#KEY_PROXIMITY_ENTERING:kotlin.String) Key used for the Bundle extra holding a boolean indicating whether a proximity alert is entering (true) or exiting (false). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_STATUS_CHANGED](https://developer.android.com/reference/kotlin/android/location/LocationManager#KEY_STATUS_CHANGED:kotlin.String) This key is no longer in use. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MODE_CHANGED_ACTION](https://developer.android.com/reference/kotlin/android/location/LocationManager#MODE_CHANGED_ACTION:kotlin.String) Broadcast intent action when the device location enabled state changes. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NETWORK_PROVIDER](https://developer.android.com/reference/kotlin/android/location/LocationManager#NETWORK_PROVIDER:kotlin.String) Standard name of the network location provider. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PASSIVE_PROVIDER](https://developer.android.com/reference/kotlin/android/location/LocationManager#PASSIVE_PROVIDER:kotlin.String) A special location provider for receiving locations without actively initiating a location fix. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PROVIDERS_CHANGED_ACTION](https://developer.android.com/reference/kotlin/android/location/LocationManager#PROVIDERS_CHANGED_ACTION:kotlin.String) Broadcast intent action when the set of enabled location providers changes. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addGpsStatusListener](https://developer.android.com/reference/kotlin/android/location/LocationManager#addGpsStatusListener(android.location.GpsStatus.Listener))`(`listener:` ` [GpsStatus.Listener](https://developer.android.com/reference/kotlin/android/location/GpsStatus.Listener)!`)` Adds a GPS status listener. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addNmeaListener](https://developer.android.com/reference/kotlin/android/location/LocationManager#addNmeaListener(android.location.GpsStatus.NmeaListener))`(`listener:` ` [GpsStatus.NmeaListener](https://developer.android.com/reference/kotlin/android/location/GpsStatus.NmeaListener)`)` No-op method to keep backward-compatibility. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addNmeaListener](https://developer.android.com/reference/kotlin/android/location/LocationManager#addNmeaListener(android.location.OnNmeaMessageListener))`(`listener:` ` [OnNmeaMessageListener](https://developer.android.com/reference/kotlin/android/location/OnNmeaMessageListener)`)` Adds an NMEA listener. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addNmeaListener](https://developer.android.com/reference/kotlin/android/location/LocationManager#addNmeaListener(android.location.OnNmeaMessageListener,%20android.os.Handler))`(`listener:` ` [OnNmeaMessageListener](https://developer.android.com/reference/kotlin/android/location/OnNmeaMessageListener)`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?`)` Adds an NMEA listener. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addNmeaListener](https://developer.android.com/reference/kotlin/android/location/LocationManager#addNmeaListener(java.util.concurrent.Executor,%20android.location.OnNmeaMessageListener))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `listener:` ` [OnNmeaMessageListener](https://developer.android.com/reference/kotlin/android/location/OnNmeaMessageListener)`)` Adds an NMEA listener. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addProximityAlert](https://developer.android.com/reference/kotlin/android/location/LocationManager#addProximityAlert(kotlin.Double,%20kotlin.Double,%20kotlin.Float,%20kotlin.Long,%20android.app.PendingIntent))`(`latitude:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `longitude:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `radius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `expiration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `pendingIntent:` ` [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)`)` Sets a proximity alert for the location given by the position (latitude, longitude) and the given radius. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTestProvider](https://developer.android.com/reference/kotlin/android/location/LocationManager#addTestProvider(kotlin.String,%20android.location.provider.ProviderProperties))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `properties:` ` [ProviderProperties](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties)`)` Creates a test location provider and adds it to the set of active providers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTestProvider](https://developer.android.com/reference/kotlin/android/location/LocationManager#addTestProvider(kotlin.String,%20android.location.provider.ProviderProperties,%20kotlin.collections.MutableSet))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `properties:` ` [ProviderProperties](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties)`, `extraAttributionTags:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Creates a test location provider and adds it to the set of active providers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTestProvider](https://developer.android.com/reference/kotlin/android/location/LocationManager#addTestProvider(kotlin.String,%20kotlin.Boolean,%20kotlin.Boolean,%20kotlin.Boolean,%20kotlin.Boolean,%20kotlin.Boolean,%20kotlin.Boolean,%20kotlin.Boolean,%20kotlin.Int,%20kotlin.Int))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `requiresNetwork:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `requiresSatellite:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `requiresCell:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `hasMonetaryCost:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `supportsAltitude:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `supportsSpeed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `supportsBearing:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `powerUsage:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `accuracy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a test location provider and adds it to the set of active providers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearTestProviderEnabled](https://developer.android.com/reference/kotlin/android/location/LocationManager#clearTestProviderEnabled(kotlin.String))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Equivalent to calling [setTestProviderEnabled(java.lang.String,boolean)](https://developer.android.com/reference/kotlin/android/location/LocationManager#setTestProviderEnabled(kotlin.String,%20kotlin.Boolean))to disable a test provider. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearTestProviderLocation](https://developer.android.com/reference/kotlin/android/location/LocationManager#clearTestProviderLocation(kotlin.String))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Does nothing. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearTestProviderStatus](https://developer.android.com/reference/kotlin/android/location/LocationManager#clearTestProviderStatus(kotlin.String))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` This method has no effect as provider status has been deprecated and is no longer supported. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getAllProviders](https://developer.android.com/reference/kotlin/android/location/LocationManager#getAllProviders())`()` Returns a list of the names of all available location providers. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getBestProvider](https://developer.android.com/reference/kotlin/android/location/LocationManager#getBestProvider(android.location.Criteria,%20kotlin.Boolean))`(`criteria:` ` [Criteria](https://developer.android.com/reference/kotlin/android/location/Criteria)`, `enabledOnly:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns the name of the provider that best meets the given criteria. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getCurrentLocation](https://developer.android.com/reference/kotlin/android/location/LocationManager#getCurrentLocation(kotlin.String,%20android.location.LocationRequest,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `locationRequest:` ` [LocationRequest](https://developer.android.com/reference/kotlin/android/location/LocationRequest)`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `consumer:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [Location](https://developer.android.com/reference/kotlin/android/location/Location)!>`)` Asynchronously returns a single current location fix from the given provider based on the given [LocationRequest](https://developer.android.com/reference/kotlin/android/location/LocationRequest). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getCurrentLocation](https://developer.android.com/reference/kotlin/android/location/LocationManager#getCurrentLocation(kotlin.String,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `consumer:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [Location](https://developer.android.com/reference/kotlin/android/location/Location)!>`)` Asynchronously returns a single current location fix from the given provider. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [GnssAntennaInfo](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo)!\>? | [getGnssAntennaInfos](https://developer.android.com/reference/kotlin/android/location/LocationManager#getGnssAntennaInfos())`()` Returns the current list of GNSS antenna infos, or null if unknown or unsupported. |
| open [GnssCapabilities](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities) | [getGnssCapabilities](https://developer.android.com/reference/kotlin/android/location/LocationManager#getGnssCapabilities())`()` Returns the supported capabilities of the GNSS chipset. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getGnssHardwareModelName](https://developer.android.com/reference/kotlin/android/location/LocationManager#getGnssHardwareModelName())`()` Returns the model name (including vendor and hardware/software version) of the GNSS hardware driver, or null if this information is not available. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGnssYearOfHardware](https://developer.android.com/reference/kotlin/android/location/LocationManager#getGnssYearOfHardware())`()` Returns the model year of the GNSS hardware and software build, or 0 if the model year is before 2016. |
| open [GpsStatus](https://developer.android.com/reference/kotlin/android/location/GpsStatus)? | [getGpsStatus](https://developer.android.com/reference/kotlin/android/location/LocationManager#getGpsStatus(android.location.GpsStatus))`(`status:` ` [GpsStatus](https://developer.android.com/reference/kotlin/android/location/GpsStatus)?`)` Retrieves information about the current status of the GPS engine. |
| open [Location](https://developer.android.com/reference/kotlin/android/location/Location)? | [getLastKnownLocation](https://developer.android.com/reference/kotlin/android/location/LocationManager#getLastKnownLocation(kotlin.String))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Gets the last known location from the given provider, or null if there is no last known location. |
| open [LocationProvider](https://developer.android.com/reference/kotlin/android/location/LocationProvider)? | [getProvider](https://developer.android.com/reference/kotlin/android/location/LocationManager#getProvider(kotlin.String))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the information about the location provider with the given name, or null if no provider exists by that name. |
| open [ProviderProperties](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties)? | [getProviderProperties](https://developer.android.com/reference/kotlin/android/location/LocationManager#getProviderProperties(kotlin.String))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the properties of the given provider, or null if the properties are currently unknown. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getProviders](https://developer.android.com/reference/kotlin/android/location/LocationManager#getProviders(android.location.Criteria,%20kotlin.Boolean))`(`criteria:` ` [Criteria](https://developer.android.com/reference/kotlin/android/location/Criteria)`, `enabledOnly:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns a list of the names of available location providers that satisfy the given criteria. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getProviders](https://developer.android.com/reference/kotlin/android/location/LocationManager#getProviders(kotlin.Boolean))`(`enabledOnly:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns a list of the names of available location providers. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasProvider](https://developer.android.com/reference/kotlin/android/location/LocationManager#hasProvider(kotlin.String))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns true if the given location provider exists on this device, irrespective of whether it is currently enabled or not. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLocationEnabled](https://developer.android.com/reference/kotlin/android/location/LocationManager#isLocationEnabled())`()` Returns the current enabled/disabled state of location. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isProviderEnabled](https://developer.android.com/reference/kotlin/android/location/LocationManager#isProviderEnabled(kotlin.String))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the current enabled/disabled status of the given provider. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerAntennaInfoListener](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerAntennaInfoListener(java.util.concurrent.Executor,%20android.location.GnssAntennaInfo.Listener))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `listener:` ` [GnssAntennaInfo.Listener](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.Listener)`)` Registers a GNSS antenna info listener that will receive all changes to antenna info. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerGnssMeasurementsCallback](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerGnssMeasurementsCallback(android.location.GnssMeasurementRequest,%20java.util.concurrent.Executor,%20android.location.GnssMeasurementsEvent.Callback))`(`request:` ` [GnssMeasurementRequest](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementRequest)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [GnssMeasurementsEvent.Callback](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent.Callback)`)` Registers a GNSS measurement callback. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerGnssMeasurementsCallback](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerGnssMeasurementsCallback(android.location.GnssMeasurementsEvent.Callback))`(`callback:` ` [GnssMeasurementsEvent.Callback](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent.Callback)`)` Registers a GNSS measurements callback which will run on a binder thread. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerGnssMeasurementsCallback](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerGnssMeasurementsCallback(android.location.GnssMeasurementsEvent.Callback,%20android.os.Handler))`(`callback:` ` [GnssMeasurementsEvent.Callback](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent.Callback)`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?`)` Registers a GNSS measurements callback. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerGnssMeasurementsCallback](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerGnssMeasurementsCallback(java.util.concurrent.Executor,%20android.location.GnssMeasurementsEvent.Callback))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [GnssMeasurementsEvent.Callback](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent.Callback)`)` Registers a GNSS measurements callback. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerGnssNavigationMessageCallback](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerGnssNavigationMessageCallback(android.location.GnssNavigationMessage.Callback))`(`callback:` ` [GnssNavigationMessage.Callback](https://developer.android.com/reference/kotlin/android/location/GnssNavigationMessage.Callback)`)` Registers a GNSS navigation message callback which will run on a binder thread. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerGnssNavigationMessageCallback](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerGnssNavigationMessageCallback(android.location.GnssNavigationMessage.Callback,%20android.os.Handler))`(`callback:` ` [GnssNavigationMessage.Callback](https://developer.android.com/reference/kotlin/android/location/GnssNavigationMessage.Callback)`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?`)` Registers a GNSS navigation message callback. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerGnssNavigationMessageCallback](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerGnssNavigationMessageCallback(java.util.concurrent.Executor,%20android.location.GnssNavigationMessage.Callback))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [GnssNavigationMessage.Callback](https://developer.android.com/reference/kotlin/android/location/GnssNavigationMessage.Callback)`)` Registers a GNSS navigation message callback. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerGnssStatusCallback](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerGnssStatusCallback(android.location.GnssStatus.Callback))`(`callback:` ` [GnssStatus.Callback](https://developer.android.com/reference/kotlin/android/location/GnssStatus.Callback)`)` Registers a GNSS status callback. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerGnssStatusCallback](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerGnssStatusCallback(android.location.GnssStatus.Callback,%20android.os.Handler))`(`callback:` ` [GnssStatus.Callback](https://developer.android.com/reference/kotlin/android/location/GnssStatus.Callback)`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?`)` Registers a GNSS status callback. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerGnssStatusCallback](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerGnssStatusCallback(java.util.concurrent.Executor,%20android.location.GnssStatus.Callback))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [GnssStatus.Callback](https://developer.android.com/reference/kotlin/android/location/GnssStatus.Callback)`)` Registers a GNSS status callback. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeGpsStatusListener](https://developer.android.com/reference/kotlin/android/location/LocationManager#removeGpsStatusListener(android.location.GpsStatus.Listener))`(`listener:` ` [GpsStatus.Listener](https://developer.android.com/reference/kotlin/android/location/GpsStatus.Listener)!`)` Removes a GPS status listener. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeNmeaListener](https://developer.android.com/reference/kotlin/android/location/LocationManager#removeNmeaListener(android.location.GpsStatus.NmeaListener))`(`listener:` ` [GpsStatus.NmeaListener](https://developer.android.com/reference/kotlin/android/location/GpsStatus.NmeaListener)`)` No-op method to keep backward-compatibility. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeNmeaListener](https://developer.android.com/reference/kotlin/android/location/LocationManager#removeNmeaListener(android.location.OnNmeaMessageListener))`(`listener:` ` [OnNmeaMessageListener](https://developer.android.com/reference/kotlin/android/location/OnNmeaMessageListener)`)` Removes an NMEA listener. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeProximityAlert](https://developer.android.com/reference/kotlin/android/location/LocationManager#removeProximityAlert(android.app.PendingIntent))`(`intent:` ` [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)`)` Removes the proximity alert with the given PendingIntent. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeTestProvider](https://developer.android.com/reference/kotlin/android/location/LocationManager#removeTestProvider(kotlin.String))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Removes the test location provider with the given name or does nothing if no such test location provider exists. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeUpdates](https://developer.android.com/reference/kotlin/android/location/LocationManager#removeUpdates(android.app.PendingIntent))`(`pendingIntent:` ` [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)`)` Removes location updates for the specified [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeUpdates](https://developer.android.com/reference/kotlin/android/location/LocationManager#removeUpdates(android.location.LocationListener))`(`listener:` ` [LocationListener](https://developer.android.com/reference/kotlin/android/location/LocationListener)`)` Removes all location updates for the specified [LocationListener](https://developer.android.com/reference/kotlin/android/location/LocationListener). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestFlush](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestFlush(kotlin.String,%20android.app.PendingIntent,%20kotlin.Int))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `pendingIntent:` ` [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)`, `requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Requests that the given provider flush any batched locations to listeners. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestFlush](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestFlush(kotlin.String,%20android.location.LocationListener,%20kotlin.Int))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `listener:` ` [LocationListener](https://developer.android.com/reference/kotlin/android/location/LocationListener)`, `requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Requests that the given provider flush any batched locations to listeners. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestLocationUpdates](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.String,%20android.location.LocationRequest,%20android.app.PendingIntent))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `locationRequest:` ` [LocationRequest](https://developer.android.com/reference/kotlin/android/location/LocationRequest)`, `pendingIntent:` ` [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)`)` Register for location updates from the specified provider, using a [LocationRequest](https://developer.android.com/reference/kotlin/android/location/LocationRequest), and callbacks delivered via the provided [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestLocationUpdates](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.String,%20android.location.LocationRequest,%20java.util.concurrent.Executor,%20android.location.LocationListener))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `locationRequest:` ` [LocationRequest](https://developer.android.com/reference/kotlin/android/location/LocationRequest)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `listener:` ` [LocationListener](https://developer.android.com/reference/kotlin/android/location/LocationListener)`)` Register for location updates from the specified provider, using a [LocationRequest](https://developer.android.com/reference/kotlin/android/location/LocationRequest), and a callback on the specified [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestLocationUpdates](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.String,%20kotlin.Long,%20kotlin.Float,%20android.app.PendingIntent))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `minTimeMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `minDistanceM:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `pendingIntent:` ` [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)`)` Register for location updates using the named provider, and callbacks delivered via the provided [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestLocationUpdates](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.String,%20kotlin.Long,%20kotlin.Float,%20android.location.LocationListener))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `minTimeMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `minDistanceM:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `listener:` ` [LocationListener](https://developer.android.com/reference/kotlin/android/location/LocationListener)`)` Register for location updates from the given provider with the given arguments, and a callback on the [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#) of the calling thread. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestLocationUpdates](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.String,%20kotlin.Long,%20kotlin.Float,%20android.location.LocationListener,%20android.os.Looper))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `minTimeMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `minDistanceM:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `listener:` ` [LocationListener](https://developer.android.com/reference/kotlin/android/location/LocationListener)`, `looper:` ` [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#)?`)` Register for location updates from the given provider with the given arguments, and a callback on the specified [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestLocationUpdates](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.String,%20kotlin.Long,%20kotlin.Float,%20java.util.concurrent.Executor,%20android.location.LocationListener))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `minTimeMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `minDistanceM:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `listener:` ` [LocationListener](https://developer.android.com/reference/kotlin/android/location/LocationListener)`)` Register for location updates using the named provider, and a callback on the specified [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestLocationUpdates](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.Long,%20kotlin.Float,%20android.location.Criteria,%20android.app.PendingIntent))`(`minTimeMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `minDistanceM:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `criteria:` ` [Criteria](https://developer.android.com/reference/kotlin/android/location/Criteria)`, `pendingIntent:` ` [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)`)` Register for location updates using a provider selected through the given Criteria, and callbacks delivered via the provided [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestLocationUpdates](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.Long,%20kotlin.Float,%20android.location.Criteria,%20android.location.LocationListener,%20android.os.Looper))`(`minTimeMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `minDistanceM:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `criteria:` ` [Criteria](https://developer.android.com/reference/kotlin/android/location/Criteria)`, `listener:` ` [LocationListener](https://developer.android.com/reference/kotlin/android/location/LocationListener)`, `looper:` ` [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#)?`)` Register for location updates using a provider selected through the given Criteria, and a callback on the specified [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestLocationUpdates](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.Long,%20kotlin.Float,%20android.location.Criteria,%20java.util.concurrent.Executor,%20android.location.LocationListener))`(`minTimeMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `minDistanceM:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `criteria:` ` [Criteria](https://developer.android.com/reference/kotlin/android/location/Criteria)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `listener:` ` [LocationListener](https://developer.android.com/reference/kotlin/android/location/LocationListener)`)` Register for location updates using a provider selected through the given Criteria, and a callback on the specified [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestSingleUpdate](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestSingleUpdate(android.location.Criteria,%20android.app.PendingIntent))`(`criteria:` ` [Criteria](https://developer.android.com/reference/kotlin/android/location/Criteria)`, `pendingIntent:` ` [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)`)` Register for a single location update using a Criteria and pending intent. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestSingleUpdate](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestSingleUpdate(android.location.Criteria,%20android.location.LocationListener,%20android.os.Looper))`(`criteria:` ` [Criteria](https://developer.android.com/reference/kotlin/android/location/Criteria)`, `listener:` ` [LocationListener](https://developer.android.com/reference/kotlin/android/location/LocationListener)`, `looper:` ` [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#)?`)` Register for a single location update using a Criteria and a callback. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestSingleUpdate](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestSingleUpdate(kotlin.String,%20android.app.PendingIntent))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `pendingIntent:` ` [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)`)` Register for a single location update using a named provider and pending intent. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestSingleUpdate](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestSingleUpdate(kotlin.String,%20android.location.LocationListener,%20android.os.Looper))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `listener:` ` [LocationListener](https://developer.android.com/reference/kotlin/android/location/LocationListener)`, `looper:` ` [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#)?`)` Register for a single location update using the named provider and a callback. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [sendExtraCommand](https://developer.android.com/reference/kotlin/android/location/LocationManager#sendExtraCommand(kotlin.String,%20kotlin.String,%20android.os.Bundle))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `command:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` Sends additional commands to a location provider. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTestProviderEnabled](https://developer.android.com/reference/kotlin/android/location/LocationManager#setTestProviderEnabled(kotlin.String,%20kotlin.Boolean))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the given test provider to be enabled or disabled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTestProviderLocation](https://developer.android.com/reference/kotlin/android/location/LocationManager#setTestProviderLocation(kotlin.String,%20android.location.Location))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `location:` ` [Location](https://developer.android.com/reference/kotlin/android/location/Location)`)` Sets a new location for the given test provider. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTestProviderStatus](https://developer.android.com/reference/kotlin/android/location/LocationManager#setTestProviderStatus(kotlin.String,%20kotlin.Int,%20android.os.Bundle,%20kotlin.Long))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `updateTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` This method has no effect as provider status has been deprecated and is no longer supported. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterAntennaInfoListener](https://developer.android.com/reference/kotlin/android/location/LocationManager#unregisterAntennaInfoListener(android.location.GnssAntennaInfo.Listener))`(`listener:` ` [GnssAntennaInfo.Listener](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.Listener)`)` Unregisters a GNSS antenna info listener. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterGnssMeasurementsCallback](https://developer.android.com/reference/kotlin/android/location/LocationManager#unregisterGnssMeasurementsCallback(android.location.GnssMeasurementsEvent.Callback))`(`callback:` ` [GnssMeasurementsEvent.Callback](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent.Callback)`)` Unregisters a GPS Measurement callback. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterGnssNavigationMessageCallback](https://developer.android.com/reference/kotlin/android/location/LocationManager#unregisterGnssNavigationMessageCallback(android.location.GnssNavigationMessage.Callback))`(`callback:` ` [GnssNavigationMessage.Callback](https://developer.android.com/reference/kotlin/android/location/GnssNavigationMessage.Callback)`)` Unregisters a GNSS Navigation Message callback. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterGnssStatusCallback](https://developer.android.com/reference/kotlin/android/location/LocationManager#unregisterGnssStatusCallback(android.location.GnssStatus.Callback))`(`callback:` ` [GnssStatus.Callback](https://developer.android.com/reference/kotlin/android/location/GnssStatus.Callback)`)` Removes a GNSS status callback. |

## Constants

### ACTION_GNSS_CAPABILITIES_CHANGED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_GNSS_CAPABILITIES_CHANGED: String
```

Broadcast intent action when GNSS capabilities change. This is most common at boot time as GNSS capabilities are queried from the chipset. Includes an intent extra, [EXTRA_GNSS_CAPABILITIES](https://developer.android.com/reference/kotlin/android/location/LocationManager#EXTRA_GNSS_CAPABILITIES:kotlin.String), with the new [GnssCapabilities](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities). 

 Value: "android.location.action.GNSS_CAPABILITIES_CHANGED"

**See Also**

- [#EXTRA_GNSS_CAPABILITIES](https://developer.android.com/reference/kotlin/android/location/LocationManager#EXTRA_GNSS_CAPABILITIES:kotlin.String)
- <https://developer.android.com/reference/kotlin/android/location/LocationManager#getGnssCapabilities()> 

### EXTRA_GNSS_CAPABILITIES

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_GNSS_CAPABILITIES: String
```

Intent extra included with [ACTION_GNSS_CAPABILITIES_CHANGED](https://developer.android.com/reference/kotlin/android/location/LocationManager#ACTION_GNSS_CAPABILITIES_CHANGED:kotlin.String) broadcasts, containing the new [GnssCapabilities](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities). 

 Value: "android.location.extra.GNSS_CAPABILITIES"

**See Also**

- [#ACTION_GNSS_CAPABILITIES_CHANGED](https://developer.android.com/reference/kotlin/android/location/LocationManager#ACTION_GNSS_CAPABILITIES_CHANGED:kotlin.String) 

### EXTRA_LOCATION_ENABLED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_LOCATION_ENABLED: String
```

Intent extra included with [MODE_CHANGED_ACTION](https://developer.android.com/reference/kotlin/android/location/LocationManager#MODE_CHANGED_ACTION:kotlin.String) broadcasts, containing the boolean enabled state of location. 

 Value: "android.location.extra.LOCATION_ENABLED"

**See Also**

- [#MODE_CHANGED_ACTION](https://developer.android.com/reference/kotlin/android/location/LocationManager#MODE_CHANGED_ACTION:kotlin.String) 

### EXTRA_PROVIDER_ENABLED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PROVIDER_ENABLED: String
```

Intent extra included with [PROVIDERS_CHANGED_ACTION](https://developer.android.com/reference/kotlin/android/location/LocationManager#PROVIDERS_CHANGED_ACTION:kotlin.String) broadcasts, containing the boolean enabled state of the location provider that has changed. 

 Value: "android.location.extra.PROVIDER_ENABLED"

**See Also**

- [#PROVIDERS_CHANGED_ACTION](https://developer.android.com/reference/kotlin/android/location/LocationManager#PROVIDERS_CHANGED_ACTION:kotlin.String)
- [#EXTRA_PROVIDER_NAME](https://developer.android.com/reference/kotlin/android/location/LocationManager#EXTRA_PROVIDER_NAME:kotlin.String) 

### EXTRA_PROVIDER_NAME

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PROVIDER_NAME: String
```

Intent extra included with [PROVIDERS_CHANGED_ACTION](https://developer.android.com/reference/kotlin/android/location/LocationManager#PROVIDERS_CHANGED_ACTION:kotlin.String) broadcasts, containing the name of the location provider that has changed. 

 Value: "android.location.extra.PROVIDER_NAME"

**See Also**

- [#PROVIDERS_CHANGED_ACTION](https://developer.android.com/reference/kotlin/android/location/LocationManager#PROVIDERS_CHANGED_ACTION:kotlin.String)
- [#EXTRA_PROVIDER_ENABLED](https://developer.android.com/reference/kotlin/android/location/LocationManager#EXTRA_PROVIDER_ENABLED:kotlin.String) 

### FUSED_PROVIDER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FUSED_PROVIDER: String
```

Standard name of the fused location provider.

If present, this provider may combine inputs from several other location providers to provide the best possible location fix. It is implicitly used for all requestLocationUpdates APIs that involve a [Criteria](https://developer.android.com/reference/kotlin/android/location/Criteria). 

 Value: "fused"

### GPS_PROVIDER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GPS_PROVIDER: String
```

Standard name of the GNSS location provider.

If present, this provider determines location using GNSS satellites. The responsiveness and accuracy of location fixes may depend on GNSS signal conditions.

Locations returned from this provider are with respect to the primary GNSS antenna position within the device. [getGnssAntennaInfos()](https://developer.android.com/reference/kotlin/android/location/LocationManager#getGnssAntennaInfos())may be used to determine the GNSS antenna position with respect to the Android Coordinate System, and convert between them if necessary. This is generally only necessary for high accuracy applications.

The extras Bundle for locations derived by this location provider may contain the following key/value pairs:

- satellites - the number of satellites used to derive the fix

 Value: "gps"

### KEY_FLUSH_COMPLETE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_FLUSH_COMPLETE: String
```

Key used for an extra holding an integer request code when location flush completion is sent using a PendingIntent. 

 Value: "flushComplete"

**See Also**

- [#requestFlush(String, PendingIntent, int)](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestFlush(kotlin.String,%20android.app.PendingIntent,%20kotlin.Int)) 

### KEY_LOCATIONS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_LOCATIONS: String
```

Key used for an extra holding a array of [Location](https://developer.android.com/reference/kotlin/android/location/Location) s when a location change is sent using a PendingIntent. This key will only be present if the location change includes multiple (ie, batched) locations, otherwise only [KEY_LOCATION_CHANGED](https://developer.android.com/reference/kotlin/android/location/LocationManager#KEY_LOCATION_CHANGED:kotlin.String) will be present. Use [Intent.getParcelableArrayExtra(String)](https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableArrayExtra(kotlin.String))to retrieve the locations.

The array of locations will never be empty, and will ordered from earliest location to latest location, the same as with [LocationListener.onLocationChanged(List)](https://developer.android.com/reference/kotlin/android/location/LocationListener#onLocationChanged(kotlin.collections.MutableList)). 

 Value: "locations"

**See Also**

- [#requestLocationUpdates(String, LocationRequest, PendingIntent)](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.String,%20android.location.LocationRequest,%20android.app.PendingIntent)) 

### KEY_LOCATION_CHANGED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_LOCATION_CHANGED: String
```

Key used for an extra holding a [Location](https://developer.android.com/reference/kotlin/android/location/Location) value when a location change is sent using a PendingIntent. If the location change includes a list of batched locations via [KEY_LOCATIONS](https://developer.android.com/reference/kotlin/android/location/LocationManager#KEY_LOCATIONS:kotlin.String) then this key will still be present, and will hold the last location in the batch. Use [Intent.getParcelableExtra(String)](https://developer.android.com/reference/kotlin/android/content/Intent.html#getParcelableExtra(kotlin.String))to retrieve the location. 

 Value: "location"

**See Also**

- [#requestLocationUpdates(String, LocationRequest, PendingIntent)](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.String,%20android.location.LocationRequest,%20android.app.PendingIntent)) 

### KEY_PROVIDER_ENABLED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_PROVIDER_ENABLED: String
```

Key used for an extra holding a boolean enabled/disabled status value when a provider enabled/disabled event is broadcast using a PendingIntent. 

 Value: "providerEnabled"

**See Also**

- [#requestLocationUpdates(String, LocationRequest, PendingIntent)](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.String,%20android.location.LocationRequest,%20android.app.PendingIntent)) 

### KEY_PROXIMITY_ENTERING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_PROXIMITY_ENTERING: String
```

Key used for the Bundle extra holding a boolean indicating whether a proximity alert is entering (true) or exiting (false).. 

 Value: "entering"

### KEY_STATUS_CHANGED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_STATUS_CHANGED: String
```

**Deprecated:** *Status changes are deprecated and no longer broadcast from Android Q onwards.*

This key is no longer in use.

Key used for a Bundle extra holding an Integer status value when a status change is broadcast using a PendingIntent. 

 Value: "status"

### MODE_CHANGED_ACTION

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_CHANGED_ACTION: String
```

Broadcast intent action when the device location enabled state changes. From Android R and above, will include a boolean intent extra, [EXTRA_LOCATION_ENABLED](https://developer.android.com/reference/kotlin/android/location/LocationManager#EXTRA_LOCATION_ENABLED:kotlin.String), with the enabled state of location. 

 Value: "android.location.MODE_CHANGED"

**See Also**

- [#EXTRA_LOCATION_ENABLED](https://developer.android.com/reference/kotlin/android/location/LocationManager#EXTRA_LOCATION_ENABLED:kotlin.String)
- <https://developer.android.com/reference/kotlin/android/location/LocationManager#isLocationEnabled()> 

### NETWORK_PROVIDER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NETWORK_PROVIDER: String
```

Standard name of the network location provider.

If present, this provider determines location based on nearby of cell tower and WiFi access points. Operation of this provider may require a data connection. 

 Value: "network"

### PASSIVE_PROVIDER

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PASSIVE_PROVIDER: String
```

A special location provider for receiving locations without actively initiating a location fix. This location provider is always present.

This provider can be used to passively receive location updates when other applications or services request them without actually requesting the locations yourself. This provider will only return locations generated by other providers. 

 Value: "passive"

### PROVIDERS_CHANGED_ACTION

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROVIDERS_CHANGED_ACTION: String
```

Broadcast intent action when the set of enabled location providers changes. To check the status of a provider, use [isProviderEnabled(java.lang.String)](https://developer.android.com/reference/kotlin/android/location/LocationManager#isProviderEnabled(kotlin.String)). From Android Q and above, will include a string intent extra, [EXTRA_PROVIDER_NAME](https://developer.android.com/reference/kotlin/android/location/LocationManager#EXTRA_PROVIDER_NAME:kotlin.String), with the name of the provider whose state has changed. From Android R and above, will include a boolean intent extra, [EXTRA_PROVIDER_ENABLED](https://developer.android.com/reference/kotlin/android/location/LocationManager#EXTRA_PROVIDER_ENABLED:kotlin.String), with the enabled state of the provider. 

 Value: "android.location.PROVIDERS_CHANGED"

**See Also**

- [#EXTRA_PROVIDER_NAME](https://developer.android.com/reference/kotlin/android/location/LocationManager#EXTRA_PROVIDER_NAME:kotlin.String)
- [#EXTRA_PROVIDER_ENABLED](https://developer.android.com/reference/kotlin/android/location/LocationManager#EXTRA_PROVIDER_ENABLED:kotlin.String)
- [#isProviderEnabled(String)](https://developer.android.com/reference/kotlin/android/location/LocationManager#isProviderEnabled(kotlin.String))

## Public methods

### addGpsStatusListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addGpsStatusListener(listener: GpsStatus.Listener!): Boolean
```

**Deprecated:** *Use [registerGnssStatusCallback(android.location.GnssStatus.Callback,android.os.Handler)](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerGnssStatusCallback(android.location.GnssStatus.Callback,%20android.os.Handler))or [registerGnssStatusCallback(java.util.concurrent.Executor,android.location.GnssStatus.Callback)](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerGnssStatusCallback(java.util.concurrent.Executor,%20android.location.GnssStatus.Callback))instead.*

Adds a GPS status listener. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [GpsStatus.Listener](https://developer.android.com/reference/kotlin/android/location/GpsStatus.Listener)!:GPS status listener object to register |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the listener was successfully added |

| Exceptions ||
|-------------------------------|-------------------------------------------------------|
| `java.lang.SecurityException` | if the ACCESS_FINE_LOCATION permission is not present |

### addNmeaListener

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addNmeaListener(listener: GpsStatus.NmeaListener): Boolean
```

**Deprecated:** *Use [addNmeaListener(android.location.OnNmeaMessageListener,android.os.Handler)](https://developer.android.com/reference/kotlin/android/location/LocationManager#addNmeaListener(android.location.OnNmeaMessageListener,%20android.os.Handler))or [addNmeaListener(java.util.concurrent.Executor,android.location.OnNmeaMessageListener)](https://developer.android.com/reference/kotlin/android/location/LocationManager#addNmeaListener(java.util.concurrent.Executor,%20android.location.OnNmeaMessageListener))instead.*

No-op method to keep backward-compatibility. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [GpsStatus.NmeaListener](https://developer.android.com/reference/kotlin/android/location/GpsStatus.NmeaListener):This value cannot be`null`. |

### addNmeaListener

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addNmeaListener(listener: OnNmeaMessageListener): Boolean
```

**Deprecated:** *Use [addNmeaListener(android.location.OnNmeaMessageListener,android.os.Handler)](https://developer.android.com/reference/kotlin/android/location/LocationManager#addNmeaListener(android.location.OnNmeaMessageListener,%20android.os.Handler))or [addNmeaListener(java.util.concurrent.Executor,android.location.OnNmeaMessageListener)](https://developer.android.com/reference/kotlin/android/location/LocationManager#addNmeaListener(java.util.concurrent.Executor,%20android.location.OnNmeaMessageListener))instead.*

Adds an NMEA listener.

See [addNmeaListener(java.util.concurrent.Executor,android.location.OnNmeaMessageListener)](https://developer.android.com/reference/kotlin/android/location/LocationManager#addNmeaListener(java.util.concurrent.Executor,%20android.location.OnNmeaMessageListener))for more detail on how this method works. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [OnNmeaMessageListener](https://developer.android.com/reference/kotlin/android/location/OnNmeaMessageListener):the listener to register This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`always |

| Exceptions ||
|-------------------------------|-------------------------------------------------------|
| `java.lang.SecurityException` | if the ACCESS_FINE_LOCATION permission is not present |

### addNmeaListener

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addNmeaListener(
    listener: OnNmeaMessageListener, 
    handler: Handler?
): Boolean
```

Adds an NMEA listener.

See [addNmeaListener(java.util.concurrent.Executor,android.location.OnNmeaMessageListener)](https://developer.android.com/reference/kotlin/android/location/LocationManager#addNmeaListener(java.util.concurrent.Executor,%20android.location.OnNmeaMessageListener))for more detail on how this method works. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [OnNmeaMessageListener](https://developer.android.com/reference/kotlin/android/location/OnNmeaMessageListener):the listener to register This value cannot be`null`. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?:the handler that the listener runs on This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`always |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if listener is null |
| `java.lang.SecurityException` | if the ACCESS_FINE_LOCATION permission is not present |

### addNmeaListener

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addNmeaListener(
    executor: Executor, 
    listener: OnNmeaMessageListener
): Boolean
```

Adds an NMEA listener. GNSS NMEA information will only be received while the [GPS_PROVIDER](https://developer.android.com/reference/kotlin/android/location/LocationManager#GPS_PROVIDER:kotlin.String) is enabled, and while the client app is in the foreground. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [OnNmeaMessageListener](https://developer.android.com/reference/kotlin/android/location/OnNmeaMessageListener):the listener to register This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the executor that the listener runs on This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`always |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if listener is null |
| `java.lang.SecurityException` | if the ACCESS_FINE_LOCATION permission is not present |

### addProximityAlert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addProximityAlert(
    latitude: Double, 
    longitude: Double, 
    radius: Float, 
    expiration: Long, 
    pendingIntent: PendingIntent
): Unit
```

Sets a proximity alert for the location given by the position (latitude, longitude) and the given radius.

When the device detects that it has entered or exited the area surrounding the location, the given PendingIntent will be fired.

The fired intent will have a boolean extra added with key [KEY_PROXIMITY_ENTERING](https://developer.android.com/reference/kotlin/android/location/LocationManager#KEY_PROXIMITY_ENTERING:kotlin.String). If the value is true, the device is entering the proximity region; if false, it is exiting.

Due to the approximate nature of position estimation, if the device passes through the given area briefly, it is possible that no Intent will be fired. Similarly, an intent could be fired if the device passes very close to the given area but does not actually enter it.

Before API version 17, this method could be used with [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String) or [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String). From API version 17 and onwards, this method requires [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String) permission. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String) or [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `latitude` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the latitude of the central point of the alert region |
| `longitude` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the longitude of the central point of the alert region |
| `radius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the radius of the central point of the alert region in meters |
| `expiration` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):expiration realtime for this proximity alert in milliseconds, or -1 to indicate no expiration |
| `pendingIntent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#):a [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) that will sent when entry to or exit from the alert region is detected This value cannot be`null`. |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String) permission is not present |

### addTestProvider

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addTestProvider(
    provider: String, 
    properties: ProviderProperties
): Unit
```

Creates a test location provider and adds it to the set of active providers. This provider will replace any provider with the same name that exists prior to this call.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the provider name This value cannot be`null`. |
| `properties` | [ProviderProperties](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties):This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if properties is null |
| `java.lang.SecurityException` | if [mock location app op](https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#OPSTR_MOCK_LOCATION:kotlin.String) is not set to [allowed](https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#MODE_ALLOWED:kotlin.Int) for your app. |

### addTestProvider

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addTestProvider(
    provider: String, 
    properties: ProviderProperties, 
    extraAttributionTags: MutableSet<String!>
): Unit
```

Creates a test location provider and adds it to the set of active providers. This provider will replace any provider with the same name that exists prior to this call.

| Parameters ||
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the provider name This value cannot be`null`. |
| `properties` | [ProviderProperties](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties):the provider properties This value cannot be`null`. |
| `extraAttributionTags` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:additional attribution tags associated with this provider This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if properties is null |
| `java.lang.SecurityException` | if [mock location app op](https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#OPSTR_MOCK_LOCATION:kotlin.String) is not set to [allowed](https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#MODE_ALLOWED:kotlin.Int) for your app. |

### addTestProvider

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addTestProvider(
    provider: String, 
    requiresNetwork: Boolean, 
    requiresSatellite: Boolean, 
    requiresCell: Boolean, 
    hasMonetaryCost: Boolean, 
    supportsAltitude: Boolean, 
    supportsSpeed: Boolean, 
    supportsBearing: Boolean, 
    powerUsage: Int, 
    accuracy: Int
): Unit
```

Creates a test location provider and adds it to the set of active providers. This provider will replace any provider with the same name that exists prior to this call.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the provider name This value cannot be`null`. |
| `powerUsage` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.location.provider.ProviderProperties#POWER_USAGE_LOW](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#POWER_USAGE_LOW:kotlin.Int), [android.location.provider.ProviderProperties#POWER_USAGE_MEDIUM](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#POWER_USAGE_MEDIUM:kotlin.Int), or [android.location.provider.ProviderProperties#POWER_USAGE_HIGH](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#POWER_USAGE_HIGH:kotlin.Int) |
| `accuracy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.location.provider.ProviderProperties#ACCURACY_FINE](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#ACCURACY_FINE:kotlin.Int), or [android.location.provider.ProviderProperties#ACCURACY_COARSE](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties#ACCURACY_COARSE:kotlin.Int) |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if provider is null |
| `java.lang.SecurityException` | if [mock location app op](https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#OPSTR_MOCK_LOCATION:kotlin.String) is not set to [allowed](https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#MODE_ALLOWED:kotlin.Int) for your app. |

### clearTestProviderEnabled

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearTestProviderEnabled(provider: String): Unit
```

**Deprecated:** *Use [setTestProviderEnabled(java.lang.String,boolean)](https://developer.android.com/reference/kotlin/android/location/LocationManager#setTestProviderEnabled(kotlin.String,%20kotlin.Boolean))instead.*

Equivalent to calling [setTestProviderEnabled(java.lang.String,boolean)](https://developer.android.com/reference/kotlin/android/location/LocationManager#setTestProviderEnabled(kotlin.String,%20kotlin.Boolean))to disable a test provider.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

### clearTestProviderLocation

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearTestProviderLocation(provider: String): Unit
```

**Deprecated:** *This method has always been a no-op, and may be removed in the future.*

Does nothing.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

### clearTestProviderStatus

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearTestProviderStatus(provider: String): Unit
```

**Deprecated:** *This method has no effect.*

This method has no effect as provider status has been deprecated and is no longer supported.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

### getAllProviders

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAllProviders(): MutableList<String!>
```

Returns a list of the names of all available location providers. All providers are returned, including those that are currently disabled.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | list of provider names This value cannot be`null`. |

### getBestProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBestProvider(
    criteria: Criteria, 
    enabledOnly: Boolean
): String?
```

**Deprecated:** *Criteria based APIs are deprecated, prefer to select a provider explicitly.*

Returns the name of the provider that best meets the given criteria. Only providers that are permitted to be accessed by the caller will be returned. If several providers meet the criteria, the one with the best accuracy is returned. If no provider meets the criteria, the criteria are loosened in the following order:

- power requirement
- accuracy
- bearing
- speed
- altitude

<br />

Note that the requirement on monetary cost is not removed in this process.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `criteria` | [Criteria](https://developer.android.com/reference/kotlin/android/location/Criteria):the criteria that need to be matched This value cannot be`null`. |
| `enabledOnly` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true then only enabled providers are included |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | name of the provider that best matches the criteria, or null if none match |

| Exceptions ||
|--------------------------------------|---------------------|
| `java.lang.IllegalArgumentException` | if criteria is null |

### getCurrentLocation

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrentLocation(
    provider: String, 
    locationRequest: LocationRequest, 
    cancellationSignal: CancellationSignal?, 
    executor: Executor, 
    consumer: Consumer<Location!>
): Unit
```

Asynchronously returns a single current location fix from the given provider based on the given [LocationRequest](https://developer.android.com/reference/kotlin/android/location/LocationRequest). This may activate sensors in order to compute a new location, unlike [getLastKnownLocation(java.lang.String)](https://developer.android.com/reference/kotlin/android/location/LocationManager#getLastKnownLocation(kotlin.String)), which will only return a cached fix if available. The given callback will be invoked once and only once, either with a valid location or with a null location if the provider was unable to generate a valid location.

A client may supply an optional [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#). If this is used to cancel the operation, no callback should be expected after the cancellation.

This method may return locations from the very recent past (on the order of several seconds), but will never return older locations (for example, several minutes old or older). Clients may rely upon the guarantee that if this method returns a location, it will represent the best estimation of the location of the device in the present moment.

Clients calling this method from the background may notice that the method fails to determine a valid location fix more often than while in the foreground. Background applications may be throttled in their location accesses to some degree. The given location request may be used to provide hints on how a fresh location is computed if necessary. In particular [LocationRequest.getDurationMillis()](https://developer.android.com/reference/kotlin/android/location/LocationRequest#getDurationMillis())can be used to provide maximum duration allowed before failing. The system will always cap the maximum amount of time a request for current location may run to some reasonable value (less than a minute for example) before the request is failed. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String) or [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](https://developer.android.com/reference/kotlin/android/location/LocationManager#getAllProviders())This value cannot be`null`. |
| `locationRequest` | [LocationRequest](https://developer.android.com/reference/kotlin/android/location/LocationRequest):the location request containing location parameters This value cannot be`null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:an optional signal that allows for cancelling this call This value may be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the callback will take place on this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `consumer` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [Location](https://developer.android.com/reference/kotlin/android/location/Location)!\>:the callback invoked with either a [Location](https://developer.android.com/reference/kotlin/android/location/Location) or null |

| Exceptions ||
|--------------------------------------|--------------------------------------|
| `java.lang.IllegalArgumentException` | if consumer is null |
| `java.lang.SecurityException` | if no suitable permission is present |

### getCurrentLocation

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrentLocation(
    provider: String, 
    cancellationSignal: CancellationSignal?, 
    executor: Executor, 
    consumer: Consumer<Location!>
): Unit
```

Asynchronously returns a single current location fix from the given provider.

See [getCurrentLocation(java.lang.String,android.location.LocationRequest,android.os.CancellationSignal,java.util.concurrent.Executor,java.util.function.Consumer)](https://developer.android.com/reference/kotlin/android/location/LocationManager#getCurrentLocation(kotlin.String,%20android.location.LocationRequest,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer))for more information. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String) or [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](https://developer.android.com/reference/kotlin/android/location/LocationManager#getAllProviders())This value cannot be`null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:an optional signal that allows for cancelling this call This value may be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the callback will take place on this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `consumer` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\< [Location](https://developer.android.com/reference/kotlin/android/location/Location)!\>:the callback invoked with either a [Location](https://developer.android.com/reference/kotlin/android/location/Location) or null |

| Exceptions ||
|--------------------------------------|--------------------------------------|
| `java.lang.IllegalArgumentException` | if consumer is null |
| `java.lang.SecurityException` | if no suitable permission is present |

### getGnssAntennaInfos

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGnssAntennaInfos(): MutableList<GnssAntennaInfo!>?
```

Returns the current list of GNSS antenna infos, or null if unknown or unsupported. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/location/LocationManager#getGnssCapabilities()> 

### getGnssCapabilities

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGnssCapabilities(): GnssCapabilities
```

Returns the supported capabilities of the GNSS chipset.

| Return ||
|------------------------------------------------------------------------------------------------------|-----------------------------|
| [GnssCapabilities](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities) | This value cannot be`null`. |

### getGnssHardwareModelName

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGnssHardwareModelName(): String?
```

Returns the model name (including vendor and hardware/software version) of the GNSS hardware driver, or null if this information is not available.

No device-specific serial number or ID is returned from this API. 

### getGnssYearOfHardware

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGnssYearOfHardware(): Int
```

Returns the model year of the GNSS hardware and software build, or 0 if the model year is before 2016. 

### getGpsStatus

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGpsStatus(status: GpsStatus?): GpsStatus?
```

**Deprecated:** *GpsStatus APIs are deprecated, use [GnssStatus](https://developer.android.com/reference/kotlin/android/location/GnssStatus) APIs instead. No longer supported in apps targeting S and above.*

Retrieves information about the current status of the GPS engine. This should only be called from within the [GpsStatus.Listener.onGpsStatusChanged](https://developer.android.com/reference/kotlin/android/location/GpsStatus.Listener#onGpsStatusChanged(kotlin.Int))callback to ensure that the data is copied atomically. The caller may either pass in an existing [GpsStatus](https://developer.android.com/reference/kotlin/android/location/GpsStatus) object to be overwritten, or pass null to create a new [GpsStatus](https://developer.android.com/reference/kotlin/android/location/GpsStatus) object. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `status` | [GpsStatus](https://developer.android.com/reference/kotlin/android/location/GpsStatus)?:object containing GPS status details, or null. |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| [GpsStatus](https://developer.android.com/reference/kotlin/android/location/GpsStatus)? | status object containing updated GPS status. |

### getLastKnownLocation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLastKnownLocation(provider: String): Location?
```

Gets the last known location from the given provider, or null if there is no last known location. The returned location may be quite old in some circumstances, so the age of the location should always be checked.

This will never activate sensors to compute a new location, and will only ever return a cached location.

See also [getCurrentLocation(java.lang.String,android.os.CancellationSignal,java.util.concurrent.Executor,java.util.function.Consumer)](https://developer.android.com/reference/kotlin/android/location/LocationManager#getCurrentLocation(kotlin.String,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer))which will always attempt to return a current location, but will potentially use additional power in the course of the attempt as compared to this method. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String) or [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](https://developer.android.com/reference/kotlin/android/location/LocationManager#getAllProviders())This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Location](https://developer.android.com/reference/kotlin/android/location/Location)? | the last known location for the given provider, or null if not available |

| Exceptions ||
|--------------------------------------|--------------------------------------|
| `java.lang.SecurityException` | if no suitable permission is present |
| `java.lang.IllegalArgumentException` | if provider is null or doesn't exist |

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProvider(provider: String): LocationProvider?
```

**Deprecated:** *This method has no way to indicate that a provider's properties are unknown, and so may return incorrect results on rare occasions. Use [getProviderProperties(java.lang.String)](https://developer.android.com/reference/kotlin/android/location/LocationManager#getProviderProperties(kotlin.String))instead.*

Returns the information about the location provider with the given name, or null if no provider exists by that name.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](https://developer.android.com/reference/kotlin/android/location/LocationManager#getAllProviders())This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [LocationProvider](https://developer.android.com/reference/kotlin/android/location/LocationProvider)? | location provider information, or null if provider does not exist |

| Exceptions ||
|--------------------------------------|---------------------|
| `java.lang.IllegalArgumentException` | if provider is null |

### getProviderProperties

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProviderProperties(provider: String): ProviderProperties?
```

Returns the properties of the given provider, or null if the properties are currently unknown. Provider properties may change over time, although this is discouraged, and should be rare. The most common transition is when provider properties go from being unknown to known, which is most common near boot time.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](https://developer.android.com/reference/kotlin/android/location/LocationManager#getAllProviders())This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [ProviderProperties](https://developer.android.com/reference/kotlin/android/location/provider/ProviderProperties)? | location provider properties, or null if properties are currently unknown |

| Exceptions ||
|--------------------------------------|---------------------------------------|
| `java.lang.IllegalArgumentException` | if provider is null or does not exist |

### getProviders

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProviders(
    criteria: Criteria, 
    enabledOnly: Boolean
): MutableList<String!>
```

**Deprecated:** *Criteria based APIs are deprecated, prefer to select a provider explicitly.*

Returns a list of the names of available location providers that satisfy the given criteria.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `criteria` | [Criteria](https://developer.android.com/reference/kotlin/android/location/Criteria):the criteria that providers must match This value cannot be`null`. |
| `enabledOnly` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true then only enabled providers are included |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | list of provider names This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|---------------------|
| `java.lang.IllegalArgumentException` | if criteria is null |

### getProviders

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProviders(enabledOnly: Boolean): MutableList<String!>
```

Returns a list of the names of available location providers. If`enabledOnly`is false, this is functionally the same as [getAllProviders()](https://developer.android.com/reference/kotlin/android/location/LocationManager#getAllProviders()).

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `enabledOnly` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true then only enabled providers are included |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | list of provider names This value cannot be`null`. |

### hasProvider

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasProvider(provider: String): Boolean
```

Returns true if the given location provider exists on this device, irrespective of whether it is currently enabled or not.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a potential location provider This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the location provider exists, false otherwise |

| Exceptions ||
|--------------------------------------|---------------------|
| `java.lang.IllegalArgumentException` | if provider is null |

### isLocationEnabled

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isLocationEnabled(): Boolean
```

Returns the current enabled/disabled state of location. To listen for changes, see [MODE_CHANGED_ACTION](https://developer.android.com/reference/kotlin/android/location/LocationManager#MODE_CHANGED_ACTION:kotlin.String).

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if location is enabled and false if location is disabled. |

### isProviderEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isProviderEnabled(provider: String): Boolean
```

Returns the current enabled/disabled status of the given provider. To listen for changes, see [PROVIDERS_CHANGED_ACTION](https://developer.android.com/reference/kotlin/android/location/LocationManager#PROVIDERS_CHANGED_ACTION:kotlin.String). Before API version [android.os.Build.VERSION_CODES#LOLLIPOP](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int), this method would throw [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) if the location permissions were not sufficient to use the specified provider.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](https://developer.android.com/reference/kotlin/android/location/LocationManager#getAllProviders())This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the provider exists and is enabled |

| Exceptions ||
|--------------------------------------|---------------------|
| `java.lang.IllegalArgumentException` | if provider is null |

### registerAntennaInfoListener

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerAntennaInfoListener(
    executor: Executor, 
    listener: GnssAntennaInfo.Listener
): Boolean
```

Registers a GNSS antenna info listener that will receive all changes to antenna info. Use [getGnssAntennaInfos()](https://developer.android.com/reference/kotlin/android/location/LocationManager#getGnssAntennaInfos())to get current antenna info.

Not all GNSS chipsets support antenna info updates, see [getGnssCapabilities()](https://developer.android.com/reference/kotlin/android/location/LocationManager#getGnssCapabilities()). If unsupported, the listener will never be invoked.

Prior to Android S, this requires the [Manifest.permission.ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String) permission.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the executor that the listener runs on This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `listener` | [GnssAntennaInfo.Listener](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.Listener):the listener to register This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`always |

| Exceptions ||
|--------------------------------------|---------------------|
| `java.lang.IllegalArgumentException` | if listener is null |

### registerGnssMeasurementsCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerGnssMeasurementsCallback(
    request: GnssMeasurementRequest, 
    executor: Executor, 
    callback: GnssMeasurementsEvent.Callback
): Boolean
```

Registers a GNSS measurement callback. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [GnssMeasurementRequest](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementRequest):extra parameters to pass to GNSS measurement provider. For example, if [android.location.GnssMeasurementRequest#isFullTracking()](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementRequest#isFullTracking())is true, GNSS chipset switches off duty cycling. This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the executor that the callback runs on This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [GnssMeasurementsEvent.Callback](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent.Callback):a [GnssMeasurementsEvent.Callback](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent.Callback) object to register. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`always if the callback was added successfully,`false`otherwise. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if callback is null |
| `java.lang.SecurityException` | if the ACCESS_FINE_LOCATION permission is not present |

### registerGnssMeasurementsCallback

```
open fun registerGnssMeasurementsCallback(callback: GnssMeasurementsEvent.Callback): Boolean
```

**Deprecated:** *Deprecated in Java.*

Registers a GNSS measurements callback which will run on a binder thread.

See [for more detail on how this method works.](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerGnssMeasurementsCallback(java.util.concurrent.Executor,%20android.location.GnssMeasurementsEvent.Callback)) 

### registerGnssMeasurementsCallback

```
open fun registerGnssMeasurementsCallback(
    callback: GnssMeasurementsEvent.Callback, 
    handler: Handler?
): Boolean
```

Registers a GNSS measurements callback.

See [for more detail on how this method works.](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerGnssMeasurementsCallback(java.util.concurrent.Executor,%20android.location.GnssMeasurementsEvent.Callback)) 

### registerGnssMeasurementsCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerGnssMeasurementsCallback(
    executor: Executor, 
    callback: GnssMeasurementsEvent.Callback
): Boolean
```

Registers a GNSS measurements callback. GNSS measurements information will only be received while the [GPS_PROVIDER](https://developer.android.com/reference/kotlin/android/location/LocationManager#GPS_PROVIDER:kotlin.String) is enabled, and while the client app is in the foreground.

Not all GNSS chipsets support measurements updates, see [getGnssCapabilities()](https://developer.android.com/reference/kotlin/android/location/LocationManager#getGnssCapabilities()).

On Android R devices that have not yet upgraded to Android R QPR1, using this API will cause unavoidable crashes in the client application when GNSS measurements are received. If a client needs to receive GNSS measurements on Android R devices that have not been upgraded to QPR1, clients are instead encouraged to use [LocationManagerCompat.registerGnssMeasurementsCallback()](https://developer.android.com/reference/androidx/core/location/LocationManagerCompat#registerGnssMeasurementsCallback(android.location.LocationManager,java.util.concurrent.Executor,android.location.GnssMeasurementsEvent.Callback))from the compat libraries instead to avoid this crash. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the executor that the callback runs on This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [GnssMeasurementsEvent.Callback](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent.Callback):the callback to register This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`always |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if callback is null |
| `java.lang.SecurityException` | if the ACCESS_FINE_LOCATION permission is not present |

### registerGnssNavigationMessageCallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerGnssNavigationMessageCallback(callback: GnssNavigationMessage.Callback): Boolean
```

**Deprecated:** *Use [registerGnssNavigationMessageCallback(android.location.GnssNavigationMessage.Callback,android.os.Handler)](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerGnssNavigationMessageCallback(android.location.GnssNavigationMessage.Callback,%20android.os.Handler))or [registerGnssNavigationMessageCallback(java.util.concurrent.Executor,android.location.GnssNavigationMessage.Callback)](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerGnssNavigationMessageCallback(java.util.concurrent.Executor,%20android.location.GnssNavigationMessage.Callback))instead.*

Registers a GNSS navigation message callback which will run on a binder thread.

See [registerGnssNavigationMessageCallback(java.util.concurrent.Executor,android.location.GnssNavigationMessage.Callback)](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerGnssNavigationMessageCallback(java.util.concurrent.Executor,%20android.location.GnssNavigationMessage.Callback))for more detail on how this method works.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [GnssNavigationMessage.Callback](https://developer.android.com/reference/kotlin/android/location/GnssNavigationMessage.Callback):the callback to register This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`always |

### registerGnssNavigationMessageCallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerGnssNavigationMessageCallback(
    callback: GnssNavigationMessage.Callback, 
    handler: Handler?
): Boolean
```

Registers a GNSS navigation message callback.

See [registerGnssNavigationMessageCallback(java.util.concurrent.Executor,android.location.GnssNavigationMessage.Callback)](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerGnssNavigationMessageCallback(java.util.concurrent.Executor,%20android.location.GnssNavigationMessage.Callback))for more detail on how this method works. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [GnssNavigationMessage.Callback](https://developer.android.com/reference/kotlin/android/location/GnssNavigationMessage.Callback):the callback to register This value cannot be`null`. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?:the handler that the callback runs on This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`always |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if callback is null |
| `java.lang.SecurityException` | if the ACCESS_FINE_LOCATION permission is not present |

### registerGnssNavigationMessageCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerGnssNavigationMessageCallback(
    executor: Executor, 
    callback: GnssNavigationMessage.Callback
): Boolean
```

Registers a GNSS navigation message callback. GNSS navigation messages will only be received while the [GPS_PROVIDER](https://developer.android.com/reference/kotlin/android/location/LocationManager#GPS_PROVIDER:kotlin.String) is enabled, and while the client app is in the foreground.

Not all GNSS chipsets support navigation message updates, see [getGnssCapabilities()](https://developer.android.com/reference/kotlin/android/location/LocationManager#getGnssCapabilities()). 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the executor that the callback runs on This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [GnssNavigationMessage.Callback](https://developer.android.com/reference/kotlin/android/location/GnssNavigationMessage.Callback):the callback to register This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`always |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if callback is null |
| `java.lang.SecurityException` | if the ACCESS_FINE_LOCATION permission is not present |

### registerGnssStatusCallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerGnssStatusCallback(callback: GnssStatus.Callback): Boolean
```

**Deprecated:** *Use [registerGnssStatusCallback(android.location.GnssStatus.Callback,android.os.Handler)](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerGnssStatusCallback(android.location.GnssStatus.Callback,%20android.os.Handler))or [registerGnssStatusCallback(java.util.concurrent.Executor,android.location.GnssStatus.Callback)](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerGnssStatusCallback(java.util.concurrent.Executor,%20android.location.GnssStatus.Callback))instead.*

Registers a GNSS status callback. This method must be called from a [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#) thread, and callbacks will occur on that looper.

See [registerGnssStatusCallback(java.util.concurrent.Executor,android.location.GnssStatus.Callback)](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerGnssStatusCallback(java.util.concurrent.Executor,%20android.location.GnssStatus.Callback))for more detail on how this method works. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [GnssStatus.Callback](https://developer.android.com/reference/kotlin/android/location/GnssStatus.Callback):the callback to register This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`always |

| Exceptions ||
|-------------------------------|-------------------------------------------------------|
| `java.lang.SecurityException` | if the ACCESS_FINE_LOCATION permission is not present |

### registerGnssStatusCallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerGnssStatusCallback(
    callback: GnssStatus.Callback, 
    handler: Handler?
): Boolean
```

Registers a GNSS status callback.

See [registerGnssStatusCallback(java.util.concurrent.Executor,android.location.GnssStatus.Callback)](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerGnssStatusCallback(java.util.concurrent.Executor,%20android.location.GnssStatus.Callback))for more detail on how this method works. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [GnssStatus.Callback](https://developer.android.com/reference/kotlin/android/location/GnssStatus.Callback):the callback to register This value cannot be`null`. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?:the handler the callback runs on This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`always |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if callback is null |
| `java.lang.SecurityException` | if the ACCESS_FINE_LOCATION permission is not present |

### registerGnssStatusCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerGnssStatusCallback(
    executor: Executor, 
    callback: GnssStatus.Callback
): Boolean
```

Registers a GNSS status callback. GNSS status information will only be received while the [GPS_PROVIDER](https://developer.android.com/reference/kotlin/android/location/LocationManager#GPS_PROVIDER:kotlin.String) is enabled, and while the client app is in the foreground. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the executor that the callback runs on This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [GnssStatus.Callback](https://developer.android.com/reference/kotlin/android/location/GnssStatus.Callback):the callback to register This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`always |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if callback is null |
| `java.lang.SecurityException` | if the ACCESS_FINE_LOCATION permission is not present |

### removeGpsStatusListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeGpsStatusListener(listener: GpsStatus.Listener!): Unit
```

**Deprecated:** *use [unregisterGnssStatusCallback(android.location.GnssStatus.Callback)](https://developer.android.com/reference/kotlin/android/location/LocationManager#unregisterGnssStatusCallback(android.location.GnssStatus.Callback))instead. No longer supported in apps targeting S and above.*

Removes a GPS status listener.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [GpsStatus.Listener](https://developer.android.com/reference/kotlin/android/location/GpsStatus.Listener)!:GPS status listener object to remove |

### removeNmeaListener

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeNmeaListener(listener: GpsStatus.NmeaListener): Unit
```

**Deprecated:** *Use [removeNmeaListener(android.location.OnNmeaMessageListener)](https://developer.android.com/reference/kotlin/android/location/LocationManager#removeNmeaListener(android.location.OnNmeaMessageListener))instead.*

No-op method to keep backward-compatibility.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [GpsStatus.NmeaListener](https://developer.android.com/reference/kotlin/android/location/GpsStatus.NmeaListener):This value cannot be`null`. |

### removeNmeaListener

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeNmeaListener(listener: OnNmeaMessageListener): Unit
```

Removes an NMEA listener.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [OnNmeaMessageListener](https://developer.android.com/reference/kotlin/android/location/OnNmeaMessageListener):a [OnNmeaMessageListener](https://developer.android.com/reference/kotlin/android/location/OnNmeaMessageListener) object to remove This value cannot be`null`. |

### removeProximityAlert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeProximityAlert(intent: PendingIntent): Unit
```

Removes the proximity alert with the given PendingIntent.

Before API version 17, this method could be used with [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String) or [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String). From API version 17 and onwards, this method requires [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String) permission. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String) or [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String) 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String) or [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#):the PendingIntent that no longer needs to be notified of proximity alerts This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if intent is null |
| `java.lang.SecurityException` | if [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String) permission is not present |

### removeTestProvider

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeTestProvider(provider: String): Unit
```

Removes the test location provider with the given name or does nothing if no such test location provider exists.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the provider name This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if provider is null |
| `java.lang.SecurityException` | if [mock location app op](https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#OPSTR_MOCK_LOCATION:kotlin.String) is not set to [allowed](https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#MODE_ALLOWED:kotlin.Int) for your app. |

### removeUpdates

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeUpdates(pendingIntent: PendingIntent): Unit
```

Removes location updates for the specified [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#). Following this call, the PendingIntent will no longer receive location updates.

See [removeUpdates(android.location.LocationListener)](https://developer.android.com/reference/kotlin/android/location/LocationManager#removeUpdates(android.location.LocationListener))for more detail on how this method works.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pendingIntent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#):pending intent that no longer needs location updates This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------|
| `java.lang.IllegalArgumentException` | if pendingIntent is null |

### removeUpdates

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeUpdates(listener: LocationListener): Unit
```

Removes all location updates for the specified [LocationListener](https://developer.android.com/reference/kotlin/android/location/LocationListener). The given listener is guaranteed not to receive any invocations that**happens-after**this method is invoked.

If the given listener has any batched requests, this method will not flush any incomplete location batches before stopping location updates. If you wish to flush any pending locations before stopping, you must first call [requestFlush(java.lang.String,android.location.LocationListener,int)](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestFlush(kotlin.String,%20android.location.LocationListener,%20kotlin.Int))and then call this method once the flush is complete. If this method is invoked before the flush is complete, you may not receive the flushed locations. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String) or [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String) 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String) or [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [LocationListener](https://developer.android.com/reference/kotlin/android/location/LocationListener):listener that no longer needs location updates This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|---------------------|
| `java.lang.IllegalArgumentException` | if listener is null |

### requestFlush

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestFlush(
    provider: String, 
    pendingIntent: PendingIntent, 
    requestCode: Int
): Unit
```

Requests that the given provider flush any batched locations to listeners. The given PendingIntent (registered with the provider) will be sent with [KEY_FLUSH_COMPLETE](https://developer.android.com/reference/kotlin/android/location/LocationManager#KEY_FLUSH_COMPLETE:kotlin.String) present in the extra keys, and`requestCode`as the corresponding value.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](https://developer.android.com/reference/kotlin/android/location/LocationManager#getAllProviders())This value cannot be`null`. |
| `pendingIntent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#):a pendingIntent registered under the provider This value cannot be`null`. |
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an arbitrary integer that will be passed back as the extra value for [KEY_FLUSH_COMPLETE](https://developer.android.com/reference/kotlin/android/location/LocationManager#KEY_FLUSH_COMPLETE:kotlin.String) |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if pending intent is null or is not registered under the provider |

### requestFlush

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestFlush(
    provider: String, 
    listener: LocationListener, 
    requestCode: Int
): Unit
```

Requests that the given provider flush any batched locations to listeners. The given listener (registered with the provider) will have [LocationListener.onFlushComplete(int)](https://developer.android.com/reference/kotlin/android/location/LocationListener#onFlushComplete(kotlin.Int))invoked with the given result code after any locations that were flushed have been delivered. If [removeUpdates(android.location.LocationListener)](https://developer.android.com/reference/kotlin/android/location/LocationManager#removeUpdates(android.location.LocationListener))is invoked before the flush callback is executed, then the flush callback will never be executed.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](https://developer.android.com/reference/kotlin/android/location/LocationManager#getAllProviders())This value cannot be`null`. |
| `listener` | [LocationListener](https://developer.android.com/reference/kotlin/android/location/LocationListener):a listener registered under the provider This value cannot be`null`. |
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an arbitrary integer passed through to [LocationListener.onFlushComplete(int)](https://developer.android.com/reference/kotlin/android/location/LocationListener#onFlushComplete(kotlin.Int)) |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if listener is null or is not registered under the provider |

### requestLocationUpdates

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestLocationUpdates(
    provider: String, 
    locationRequest: LocationRequest, 
    pendingIntent: PendingIntent
): Unit
```

Register for location updates from the specified provider, using a [LocationRequest](https://developer.android.com/reference/kotlin/android/location/LocationRequest), and callbacks delivered via the provided [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#).

The delivered pending intents will contain extras with the callback information. The keys used for the extras are [KEY_LOCATION_CHANGED](https://developer.android.com/reference/kotlin/android/location/LocationManager#KEY_LOCATION_CHANGED:kotlin.String) and [KEY_PROVIDER_ENABLED](https://developer.android.com/reference/kotlin/android/location/LocationManager#KEY_PROVIDER_ENABLED:kotlin.String). See the documentation for each respective extra key for information on the values.

To unregister for location updates, use [removeUpdates(android.app.PendingIntent)](https://developer.android.com/reference/kotlin/android/location/LocationManager#removeUpdates(android.app.PendingIntent)). 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String) or [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](https://developer.android.com/reference/kotlin/android/location/LocationManager#getAllProviders())This value cannot be`null`. |
| `locationRequest` | [LocationRequest](https://developer.android.com/reference/kotlin/android/location/LocationRequest):the location request containing location parameters This value cannot be`null`. |
| `pendingIntent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#):the pending intent to send location updates This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------|
| `java.lang.IllegalArgumentException` | if pendingIntent is null |
| `java.lang.SecurityException` | if no suitable permission is present |

### requestLocationUpdates

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestLocationUpdates(
    provider: String, 
    locationRequest: LocationRequest, 
    executor: Executor, 
    listener: LocationListener
): Unit
```

Register for location updates from the specified provider, using a [LocationRequest](https://developer.android.com/reference/kotlin/android/location/LocationRequest), and a callback on the specified [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#).

Only one request can be registered for each unique listener/provider pair, so any subsequent requests with the same provider and listener will overwrite all associated arguments. The same listener may be used across multiple providers with different requests for each provider.

It may take some time to receive the first location update depending on the conditions the device finds itself in. In order to take advantage of cached locations, application may consider using [getLastKnownLocation(java.lang.String)](https://developer.android.com/reference/kotlin/android/location/LocationManager#getLastKnownLocation(kotlin.String))or [getCurrentLocation(java.lang.String,android.location.LocationRequest,android.os.CancellationSignal,java.util.concurrent.Executor,java.util.function.Consumer)](https://developer.android.com/reference/kotlin/android/location/LocationManager#getCurrentLocation(kotlin.String,%20android.location.LocationRequest,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer))instead.

See [LocationRequest](https://developer.android.com/reference/kotlin/android/location/LocationRequest) documentation for an explanation of various request parameters and how they can affect the received locations.

If your application wants to passively observe location updates from all providers, then use the [PASSIVE_PROVIDER](https://developer.android.com/reference/kotlin/android/location/LocationManager#PASSIVE_PROVIDER:kotlin.String). This provider does not turn on or modify active location providers, so you do not need to be as careful about minimum time and minimum distance parameters. However, if your application performs heavy work on a location update (such as network activity) then you should set an explicit fastest interval on your location request in case another application enables a location provider with extremely fast updates.

In case the provider you have selected is disabled, location updates will cease, and a provider availability update will be sent. As soon as the provider is enabled again, another provider availability update will be sent and location updates will resume.

Locations returned from [GPS_PROVIDER](https://developer.android.com/reference/kotlin/android/location/LocationManager#GPS_PROVIDER:kotlin.String) are with respect to the primary GNSS antenna position within the device. [getGnssAntennaInfos()](https://developer.android.com/reference/kotlin/android/location/LocationManager#getGnssAntennaInfos())may be used to determine the GNSS antenna position with respect to the Android Coordinate System, and convert between them if necessary. This is generally only necessary for high accuracy applications.

When location callbacks are invoked, the system will hold a wakelock on your application's behalf for some period of time, but not indefinitely. If your application requires a long running wakelock within the location callback, you should acquire it yourself.

Spamming location requests is a drain on system resources, and the system has preventative measures in place to ensure that this behavior will never result in more locations than could be achieved with a single location request with an equivalent interval that is left in place the whole time. As part of this amelioration, applications that target Android S and above may receive cached or historical locations through their listener. These locations will never be older than the interval of the location request.

To unregister for location updates, use [removeUpdates(android.location.LocationListener)](https://developer.android.com/reference/kotlin/android/location/LocationManager#removeUpdates(android.location.LocationListener)). 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String) or [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](https://developer.android.com/reference/kotlin/android/location/LocationManager#getAllProviders())This value cannot be`null`. |
| `locationRequest` | [LocationRequest](https://developer.android.com/reference/kotlin/android/location/LocationRequest):the location request containing location parameters This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the executor handling listener callbacks This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `listener` | [LocationListener](https://developer.android.com/reference/kotlin/android/location/LocationListener):the listener to receive location updates This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------|
| `java.lang.IllegalArgumentException` | if listener is null |
| `java.lang.SecurityException` | if no suitable permission is present |

### requestLocationUpdates

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestLocationUpdates(
    provider: String, 
    minTimeMs: Long, 
    minDistanceM: Float, 
    pendingIntent: PendingIntent
): Unit
```

Register for location updates using the named provider, and callbacks delivered via the provided [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#).

See [requestLocationUpdates(java.lang.String,android.location.LocationRequest,android.app.PendingIntent)](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.String,%20android.location.LocationRequest,%20android.app.PendingIntent))for more detail on how this method works. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String) or [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](https://developer.android.com/reference/kotlin/android/location/LocationManager#getAllProviders())This value cannot be`null`. |
| `minTimeMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):minimum time interval between location updates in milliseconds |
| `minDistanceM` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):minimum distance between location updates in meters |
| `pendingIntent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#):the pending intent to send location updates This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------|
| `java.lang.IllegalArgumentException` | if pendingIntent is null |
| `java.lang.SecurityException` | if no suitable permission is present |

### requestLocationUpdates

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestLocationUpdates(
    provider: String, 
    minTimeMs: Long, 
    minDistanceM: Float, 
    listener: LocationListener
): Unit
```

Register for location updates from the given provider with the given arguments, and a callback on the [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#) of the calling thread.

See [requestLocationUpdates(java.lang.String,android.location.LocationRequest,java.util.concurrent.Executor,android.location.LocationListener)](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.String,%20android.location.LocationRequest,%20java.util.concurrent.Executor,%20android.location.LocationListener))for more detail on how this method works.

Prior to Jellybean, the minTime parameter was only a hint, and some location provider implementations ignored it. For Jellybean and onwards however, it is mandatory for Android compatible devices to observe both the minTime and minDistance parameters. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String) or [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](https://developer.android.com/reference/kotlin/android/location/LocationManager#getAllProviders())This value cannot be`null`. |
| `minTimeMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):minimum time interval between location updates in milliseconds |
| `minDistanceM` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):minimum distance between location updates in meters |
| `listener` | [LocationListener](https://developer.android.com/reference/kotlin/android/location/LocationListener):the listener to receive location updates This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------|
| `java.lang.IllegalArgumentException` | if listener is null |
| `java.lang.RuntimeException` | if the calling thread has no Looper |
| `java.lang.SecurityException` | if no suitable permission is present |

### requestLocationUpdates

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestLocationUpdates(
    provider: String, 
    minTimeMs: Long, 
    minDistanceM: Float, 
    listener: LocationListener, 
    looper: Looper?
): Unit
```

Register for location updates from the given provider with the given arguments, and a callback on the specified [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#).

See [requestLocationUpdates(java.lang.String,android.location.LocationRequest,java.util.concurrent.Executor,android.location.LocationListener)](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.String,%20android.location.LocationRequest,%20java.util.concurrent.Executor,%20android.location.LocationListener))for more detail on how this method works.

Prior to Jellybean, the minTime parameter was only a hint, and some location provider implementations ignored it. For Jellybean and onwards however, it is mandatory for Android compatible devices to observe both the minTime and minDistance parameters. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String) or [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](https://developer.android.com/reference/kotlin/android/location/LocationManager#getAllProviders())This value cannot be`null`. |
| `minTimeMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):minimum time interval between location updates in milliseconds |
| `minDistanceM` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):minimum distance between location updates in meters |
| `listener` | [LocationListener](https://developer.android.com/reference/kotlin/android/location/LocationListener):the listener to receive location updates This value cannot be`null`. |
| `looper` | [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#)?:the looper handling listener callbacks, or null to use the looper of the calling thread |

| Exceptions ||
|--------------------------------------|--------------------------------------|
| `java.lang.IllegalArgumentException` | if listener is null |
| `java.lang.SecurityException` | if no suitable permission is present |

### requestLocationUpdates

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestLocationUpdates(
    provider: String, 
    minTimeMs: Long, 
    minDistanceM: Float, 
    executor: Executor, 
    listener: LocationListener
): Unit
```

Register for location updates using the named provider, and a callback on the specified [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#).

See [requestLocationUpdates(java.lang.String,android.location.LocationRequest,java.util.concurrent.Executor,android.location.LocationListener)](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.String,%20android.location.LocationRequest,%20java.util.concurrent.Executor,%20android.location.LocationListener))for more detail on how this method works.

Prior to Jellybean, the minTime parameter was only a hint, and some location provider implementations ignored it. For Jellybean and onwards however, it is mandatory for Android compatible devices to observe both the minTime and minDistance parameters. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String) or [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](https://developer.android.com/reference/kotlin/android/location/LocationManager#getAllProviders())This value cannot be`null`. |
| `minTimeMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):minimum time interval between location updates in milliseconds |
| `minDistanceM` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):minimum distance between location updates in meters |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the executor handling listener callbacks This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `listener` | [LocationListener](https://developer.android.com/reference/kotlin/android/location/LocationListener):the listener to receive location updates This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------|
| `java.lang.IllegalArgumentException` | if listener is null |
| `java.lang.SecurityException` | if no suitable permission is present |

### requestLocationUpdates

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestLocationUpdates(
    minTimeMs: Long, 
    minDistanceM: Float, 
    criteria: Criteria, 
    pendingIntent: PendingIntent
): Unit
```

**Deprecated:** *Use [requestLocationUpdates(java.lang.String,long,float,android.app.PendingIntent)](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.String,%20kotlin.Long,%20kotlin.Float,%20android.app.PendingIntent))instead to explicitly select a provider.*

Register for location updates using a provider selected through the given Criteria, and callbacks delivered via the provided [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#).

Note: Since Android KitKat, Criteria requests will always result in using the [FUSED_PROVIDER](https://developer.android.com/reference/kotlin/android/location/LocationManager#FUSED_PROVIDER:kotlin.String).

See [requestLocationUpdates(java.lang.String,long,float,android.app.PendingIntent)](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.String,%20kotlin.Long,%20kotlin.Float,%20android.app.PendingIntent))for more detail on how this method works. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String) or [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `minTimeMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):minimum time interval between location updates in milliseconds |
| `minDistanceM` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):minimum distance between location updates in meters |
| `criteria` | [Criteria](https://developer.android.com/reference/kotlin/android/location/Criteria):contains parameters to choose the appropriate provider for location updates This value cannot be`null`. |
| `pendingIntent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#):the pending intent to send location updates This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------|
| `java.lang.IllegalArgumentException` | if pendingIntent is null |
| `java.lang.SecurityException` | if no suitable permission is present |

### requestLocationUpdates

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestLocationUpdates(
    minTimeMs: Long, 
    minDistanceM: Float, 
    criteria: Criteria, 
    listener: LocationListener, 
    looper: Looper?
): Unit
```

**Deprecated:** *Use [requestLocationUpdates(java.lang.String,long,float,android.location.LocationListener,android.os.Looper)](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.String,%20kotlin.Long,%20kotlin.Float,%20android.location.LocationListener,%20android.os.Looper))instead to explicitly select a provider.*

Register for location updates using a provider selected through the given Criteria, and a callback on the specified [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#).

Note: Since Android KitKat, Criteria requests will always result in using the [FUSED_PROVIDER](https://developer.android.com/reference/kotlin/android/location/LocationManager#FUSED_PROVIDER:kotlin.String).

See [requestLocationUpdates(java.lang.String,android.location.LocationRequest,java.util.concurrent.Executor,android.location.LocationListener)](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.String,%20android.location.LocationRequest,%20java.util.concurrent.Executor,%20android.location.LocationListener))for more detail on how this method works. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String) or [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `minTimeMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):minimum time interval between location updates in milliseconds |
| `minDistanceM` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):minimum distance between location updates in meters |
| `criteria` | [Criteria](https://developer.android.com/reference/kotlin/android/location/Criteria):contains parameters to choose the appropriate provider for location updates This value cannot be`null`. |
| `listener` | [LocationListener](https://developer.android.com/reference/kotlin/android/location/LocationListener):the listener to receive location updates This value cannot be`null`. |
| `looper` | [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#)?:This value may be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------|
| `java.lang.IllegalArgumentException` | if listener is null |
| `java.lang.SecurityException` | if no suitable permission is present |

### requestLocationUpdates

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestLocationUpdates(
    minTimeMs: Long, 
    minDistanceM: Float, 
    criteria: Criteria, 
    executor: Executor, 
    listener: LocationListener
): Unit
```

**Deprecated:** *Use [requestLocationUpdates(java.lang.String,long,float,java.util.concurrent.Executor,android.location.LocationListener)](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.String,%20kotlin.Long,%20kotlin.Float,%20java.util.concurrent.Executor,%20android.location.LocationListener))instead to explicitly select a provider.*

Register for location updates using a provider selected through the given Criteria, and a callback on the specified [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#).

Note: Since Android KitKat, Criteria requests will always result in using the [FUSED_PROVIDER](https://developer.android.com/reference/kotlin/android/location/LocationManager#FUSED_PROVIDER:kotlin.String).

See [requestLocationUpdates(java.lang.String,android.location.LocationRequest,java.util.concurrent.Executor,android.location.LocationListener)](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.String,%20android.location.LocationRequest,%20java.util.concurrent.Executor,%20android.location.LocationListener))for more detail on how this method works. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String) or [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `minTimeMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):minimum time interval between location updates in milliseconds |
| `minDistanceM` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):minimum distance between location updates in meters |
| `criteria` | [Criteria](https://developer.android.com/reference/kotlin/android/location/Criteria):contains parameters to choose the appropriate provider for location updates This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the executor handling listener callbacks This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `listener` | [LocationListener](https://developer.android.com/reference/kotlin/android/location/LocationListener):the listener to receive location updates This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------|
| `java.lang.IllegalArgumentException` | if listener is null |
| `java.lang.SecurityException` | if no suitable permission is present |

### requestSingleUpdate

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestSingleUpdate(
    criteria: Criteria, 
    pendingIntent: PendingIntent
): Unit
```

**Deprecated:** *Use [getCurrentLocation(java.lang.String,android.os.CancellationSignal,java.util.concurrent.Executor,java.util.function.Consumer)](https://developer.android.com/reference/kotlin/android/location/LocationManager#getCurrentLocation(kotlin.String,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer))instead as it does not carry a risk of extreme battery drain.*

Register for a single location update using a Criteria and pending intent.

Note: Since Android KitKat, Criteria requests will always result in using the [FUSED_PROVIDER](https://developer.android.com/reference/kotlin/android/location/LocationManager#FUSED_PROVIDER:kotlin.String).

See [requestLocationUpdates(long,float,android.location.Criteria,android.app.PendingIntent)](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.Long,%20kotlin.Float,%20android.location.Criteria,%20android.app.PendingIntent))for more detail on how to use this method. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String) or [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `criteria` | [Criteria](https://developer.android.com/reference/kotlin/android/location/Criteria):contains parameters to choose the appropriate provider for location updates This value cannot be`null`. |
| `pendingIntent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#):the pending intent to send location updates This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------|
| `java.lang.IllegalArgumentException` | if intent is null |
| `java.lang.SecurityException` | if no suitable permission is present |

### requestSingleUpdate

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestSingleUpdate(
    criteria: Criteria, 
    listener: LocationListener, 
    looper: Looper?
): Unit
```

**Deprecated:** *Use [getCurrentLocation(java.lang.String,android.os.CancellationSignal,java.util.concurrent.Executor,java.util.function.Consumer)](https://developer.android.com/reference/kotlin/android/location/LocationManager#getCurrentLocation(kotlin.String,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer))instead as it does not carry a risk of extreme battery drain.*

Register for a single location update using a Criteria and a callback.

Note: Since Android KitKat, Criteria requests will always result in using the [FUSED_PROVIDER](https://developer.android.com/reference/kotlin/android/location/LocationManager#FUSED_PROVIDER:kotlin.String).

See [requestLocationUpdates(long,float,android.location.Criteria,android.app.PendingIntent)](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.Long,%20kotlin.Float,%20android.location.Criteria,%20android.app.PendingIntent))for more detail on how to use this method. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String) or [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `criteria` | [Criteria](https://developer.android.com/reference/kotlin/android/location/Criteria):contains parameters to choose the appropriate provider for location updates This value cannot be`null`. |
| `listener` | [LocationListener](https://developer.android.com/reference/kotlin/android/location/LocationListener):the listener to receive location updates This value cannot be`null`. |
| `looper` | [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#)?:the looper handling listener callbacks, or null to use the looper of the calling thread |

| Exceptions ||
|--------------------------------------|--------------------------------------|
| `java.lang.IllegalArgumentException` | if listener is null |
| `java.lang.SecurityException` | if no suitable permission is present |

### requestSingleUpdate

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestSingleUpdate(
    provider: String, 
    pendingIntent: PendingIntent
): Unit
```

**Deprecated:** *Use [getCurrentLocation(java.lang.String,android.os.CancellationSignal,java.util.concurrent.Executor,java.util.function.Consumer)](https://developer.android.com/reference/kotlin/android/location/LocationManager#getCurrentLocation(kotlin.String,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer))instead as it does not carry a risk of extreme battery drain.*

Register for a single location update using a named provider and pending intent.

See [requestLocationUpdates(long,float,android.location.Criteria,android.app.PendingIntent)](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.Long,%20kotlin.Float,%20android.location.Criteria,%20android.app.PendingIntent))for more detail on how to use this method. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String) or [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](https://developer.android.com/reference/kotlin/android/location/LocationManager#getAllProviders())This value cannot be`null`. |
| `pendingIntent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#):the pending intent to send location updates This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------|
| `java.lang.IllegalArgumentException` | if intent is null |
| `java.lang.SecurityException` | if no suitable permission is present |

### requestSingleUpdate

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestSingleUpdate(
    provider: String, 
    listener: LocationListener, 
    looper: Looper?
): Unit
```

**Deprecated:** *Use [getCurrentLocation(java.lang.String,android.os.CancellationSignal,java.util.concurrent.Executor,java.util.function.Consumer)](https://developer.android.com/reference/kotlin/android/location/LocationManager#getCurrentLocation(kotlin.String,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20java.util.function.Consumer))instead as it does not carry a risk of extreme battery drain.*

Register for a single location update using the named provider and a callback.

See [requestLocationUpdates(java.lang.String,long,float,android.location.LocationListener,android.os.Looper)](https://developer.android.com/reference/kotlin/android/location/LocationManager#requestLocationUpdates(kotlin.String,%20kotlin.Long,%20kotlin.Float,%20android.location.LocationListener,%20android.os.Looper))for more detail on how to use this method. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String) or [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String)

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](https://developer.android.com/reference/kotlin/android/location/LocationManager#getAllProviders())This value cannot be`null`. |
| `listener` | [LocationListener](https://developer.android.com/reference/kotlin/android/location/LocationListener):the listener to receive location updates This value cannot be`null`. |
| `looper` | [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#)?:the looper handling listener callbacks, or null to use the looper of the calling thread |

| Exceptions ||
|--------------------------------------|--------------------------------------|
| `java.lang.IllegalArgumentException` | if listener is null |
| `java.lang.SecurityException` | if no suitable permission is present |

### sendExtraCommand

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sendExtraCommand(
    provider: String, 
    command: String, 
    extras: Bundle?
): Boolean
```

Sends additional commands to a location provider. Can be used to support provider specific extensions to the Location Manager API.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](https://developer.android.com/reference/kotlin/android/location/LocationManager#getAllProviders())This value cannot be`null`. |
| `command` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name of the command to send to the provider This value cannot be`null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:optional arguments for the command, or null |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true always, the return value may be ignored |

### setTestProviderEnabled

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTestProviderEnabled(
    provider: String, 
    enabled: Boolean
): Unit
```

Sets the given test provider to be enabled or disabled.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the provider name This value cannot be`null`. |
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the mock enabled value |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if [mock location app op](https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#OPSTR_MOCK_LOCATION:kotlin.String) is not set to [allowed](https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#MODE_ALLOWED:kotlin.Int) for your app. |
| `java.lang.IllegalArgumentException` | if provider is null or not a test provider |

### setTestProviderLocation

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTestProviderLocation(
    provider: String, 
    location: Location
): Unit
```

Sets a new location for the given test provider. This location will be identiable as a mock location to all clients via [Location.isMock()](https://developer.android.com/reference/kotlin/android/location/Location#isMock()).

The location object must have a minimum number of fields set to be considered valid, as per documentation on [Location](https://developer.android.com/reference/kotlin/android/location/Location) class.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the provider name This value cannot be`null`. |
| `location` | [Location](https://developer.android.com/reference/kotlin/android/location/Location):the mock location This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if [mock location app op](https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#OPSTR_MOCK_LOCATION:kotlin.String) is not set to [allowed](https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#MODE_ALLOWED:kotlin.Int) for your app. |
| `java.lang.IllegalArgumentException` | if the location is null or incomplete |

### setTestProviderStatus

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTestProviderStatus(
    provider: String, 
    status: Int, 
    extras: Bundle?, 
    updateTime: Long
): Unit
```

**Deprecated:** *This method has no effect.*

This method has no effect as provider status has been deprecated and is no longer supported.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:This value may be`null`. |

### unregisterAntennaInfoListener

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterAntennaInfoListener(listener: GnssAntennaInfo.Listener): Unit
```

Unregisters a GNSS antenna info listener.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [GnssAntennaInfo.Listener](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.Listener):a [GnssAntennaInfo.Listener](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.Listener) object to remove This value cannot be`null`. |

### unregisterGnssMeasurementsCallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterGnssMeasurementsCallback(callback: GnssMeasurementsEvent.Callback): Unit
```

Unregisters a GPS Measurement callback.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [GnssMeasurementsEvent.Callback](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent.Callback):a [GnssMeasurementsEvent.Callback](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent.Callback) object to remove. This value cannot be`null`. |

### unregisterGnssNavigationMessageCallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterGnssNavigationMessageCallback(callback: GnssNavigationMessage.Callback): Unit
```

Unregisters a GNSS Navigation Message callback.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [GnssNavigationMessage.Callback](https://developer.android.com/reference/kotlin/android/location/GnssNavigationMessage.Callback):a [GnssNavigationMessage.Callback](https://developer.android.com/reference/kotlin/android/location/GnssNavigationMessage.Callback) object to remove. This value cannot be`null`. |

### unregisterGnssStatusCallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterGnssStatusCallback(callback: GnssStatus.Callback): Unit
```

Removes a GNSS status callback.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [GnssStatus.Callback](https://developer.android.com/reference/kotlin/android/location/GnssStatus.Callback):GNSS status callback object to remove This value cannot be`null`. |
