# LocationManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocationManager

Kotlin| [Java](../android/location/LocationManager.md) 
| --- | --- |

```
open class LocationManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.location.LocationManager](../android/location/LocationManager.md) |

This class provides access to the system location services. These services allow applications to obtain periodic updates of the device's geographical location, or to be notified when the device enters the proximity of a given geographical location.

Unless otherwise noted, all Location API methods require the [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md) or [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md) permissions. If your application only has the coarse permission then providers will still return location results, but the exact location will be obfuscated to a coarse level of accuracy. 
Requires the [PackageManager#FEATURE_LOCATION](../android/content/pm/PackageManager.md) feature which can be detected using [PackageManager.hasSystemFeature(String)](../android/content/pm/PackageManager.md)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_GNSS_CAPABILITIES_CHANGED](../android/location/LocationManager.md) Broadcast intent action when GNSS capabilities change. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_GNSS_CAPABILITIES](../android/location/LocationManager.md) Intent extra included with [ACTION_GNSS_CAPABILITIES_CHANGED](../android/location/LocationManager.md) broadcasts, containing the new [GnssCapabilities](../android/location/GnssCapabilities.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_LOCATION_ENABLED](../android/location/LocationManager.md) Intent extra included with [MODE_CHANGED_ACTION](../android/location/LocationManager.md) broadcasts, containing the boolean enabled state of location. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PROVIDER_ENABLED](../android/location/LocationManager.md) Intent extra included with [PROVIDERS_CHANGED_ACTION](../android/location/LocationManager.md) broadcasts, containing the boolean enabled state of the location provider that has changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PROVIDER_NAME](../android/location/LocationManager.md) Intent extra included with [PROVIDERS_CHANGED_ACTION](../android/location/LocationManager.md) broadcasts, containing the name of the location provider that has changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FUSED_PROVIDER](../android/location/LocationManager.md) Standard name of the fused location provider. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [GPS_PROVIDER](../android/location/LocationManager.md) Standard name of the GNSS location provider. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_FLUSH_COMPLETE](../android/location/LocationManager.md) Key used for an extra holding an integer request code when location flush completion is sent using a PendingIntent. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_LOCATIONS](../android/location/LocationManager.md) Key used for an extra holding a array of [Location](../android/location/Location.md) s when a location change is sent using a PendingIntent. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_LOCATION_CHANGED](../android/location/LocationManager.md) Key used for an extra holding a [Location](../android/location/Location.md) value when a location change is sent using a PendingIntent. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_PROVIDER_ENABLED](../android/location/LocationManager.md) Key used for an extra holding a boolean enabled/disabled status value when a provider enabled/disabled event is broadcast using a PendingIntent. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_PROXIMITY_ENTERING](../android/location/LocationManager.md) Key used for the Bundle extra holding a boolean indicating whether a proximity alert is entering (true) or exiting (false). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_STATUS_CHANGED](../android/location/LocationManager.md) This key is no longer in use. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MODE_CHANGED_ACTION](../android/location/LocationManager.md) Broadcast intent action when the device location enabled state changes. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NETWORK_PROVIDER](../android/location/LocationManager.md) Standard name of the network location provider. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PASSIVE_PROVIDER](../android/location/LocationManager.md) A special location provider for receiving locations without actively initiating a location fix. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PROVIDERS_CHANGED_ACTION](../android/location/LocationManager.md) Broadcast intent action when the set of enabled location providers changes. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addGpsStatusListener](../android/location/LocationManager.md))`(`listener:` ` [GpsStatus.Listener](../android/location/GpsStatus.Listener.md)!`)` Adds a GPS status listener. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addNmeaListener](../android/location/LocationManager.md))`(`listener:` ` [GpsStatus.NmeaListener](../android/location/GpsStatus.NmeaListener.md)`)` No-op method to keep backward-compatibility. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addNmeaListener](../android/location/LocationManager.md))`(`listener:` ` [OnNmeaMessageListener](../android/location/OnNmeaMessageListener.md)`)` Adds an NMEA listener. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addNmeaListener](../android/location/LocationManager.md))`(`listener:` ` [OnNmeaMessageListener](../android/location/OnNmeaMessageListener.md)`, `handler:` ` [Handler](../android/os/Handler.md)?`)` Adds an NMEA listener. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addNmeaListener](../android/location/LocationManager.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `listener:` ` [OnNmeaMessageListener](../android/location/OnNmeaMessageListener.md)`)` Adds an NMEA listener. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addProximityAlert](../android/location/LocationManager.md))`(`latitude:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `longitude:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `radius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `expiration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `pendingIntent:` ` [PendingIntent](../android/app/PendingIntent.md)`)` Sets a proximity alert for the location given by the position (latitude, longitude) and the given radius. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTestProvider](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `properties:` ` [ProviderProperties](../android/location/provider/ProviderProperties.md)`)` Creates a test location provider and adds it to the set of active providers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTestProvider](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `properties:` ` [ProviderProperties](../android/location/provider/ProviderProperties.md)`, `extraAttributionTags:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Creates a test location provider and adds it to the set of active providers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTestProvider](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `requiresNetwork:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `requiresSatellite:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `requiresCell:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `hasMonetaryCost:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `supportsAltitude:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `supportsSpeed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `supportsBearing:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `powerUsage:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `accuracy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a test location provider and adds it to the set of active providers. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearTestProviderEnabled](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Equivalent to calling [setTestProviderEnabled(java.lang.String,boolean)](../android/location/LocationManager.md))to disable a test provider. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearTestProviderLocation](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Does nothing. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearTestProviderStatus](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` This method has no effect as provider status has been deprecated and is no longer supported. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getAllProviders](../android/location/LocationManager.md))`()` Returns a list of the names of all available location providers. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getBestProvider](../android/location/LocationManager.md))`(`criteria:` ` [Criteria](../android/location/Criteria.md)`, `enabledOnly:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns the name of the provider that best meets the given criteria. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getCurrentLocation](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `locationRequest:` ` [LocationRequest](../android/location/LocationRequest.md)`, `cancellationSignal:` ` [CancellationSignal](../android/os/CancellationSignal.md)?`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `consumer:` ` [Consumer](../java/util/function/Consumer.md)< [Location](../android/location/Location.md)!>`)` Asynchronously returns a single current location fix from the given provider based on the given [LocationRequest](../android/location/LocationRequest.md). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getCurrentLocation](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `cancellationSignal:` ` [CancellationSignal](../android/os/CancellationSignal.md)?`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `consumer:` ` [Consumer](../java/util/function/Consumer.md)< [Location](../android/location/Location.md)!>`)` Asynchronously returns a single current location fix from the given provider. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [GnssAntennaInfo](../android/location/GnssAntennaInfo.md)!\>? | [getGnssAntennaInfos](../android/location/LocationManager.md))`()` Returns the current list of GNSS antenna infos, or null if unknown or unsupported. |
| open [GnssCapabilities](../android/location/GnssCapabilities.md) | [getGnssCapabilities](../android/location/LocationManager.md))`()` Returns the supported capabilities of the GNSS chipset. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getGnssHardwareModelName](../android/location/LocationManager.md))`()` Returns the model name (including vendor and hardware/software version) of the GNSS hardware driver, or null if this information is not available. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGnssYearOfHardware](../android/location/LocationManager.md))`()` Returns the model year of the GNSS hardware and software build, or 0 if the model year is before 2016. |
| open [GpsStatus](../android/location/GpsStatus.md)? | [getGpsStatus](../android/location/LocationManager.md))`(`status:` ` [GpsStatus](../android/location/GpsStatus.md)?`)` Retrieves information about the current status of the GPS engine. |
| --- | --- |
| open [Location](../android/location/Location.md)? | [getLastKnownLocation](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Gets the last known location from the given provider, or null if there is no last known location. |
| open [LocationProvider](../android/location/LocationProvider.md)? | [getProvider](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the information about the location provider with the given name, or null if no provider exists by that name. |
| open [ProviderProperties](../android/location/provider/ProviderProperties.md)? | [getProviderProperties](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the properties of the given provider, or null if the properties are currently unknown. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getProviders](../android/location/LocationManager.md))`(`criteria:` ` [Criteria](../android/location/Criteria.md)`, `enabledOnly:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns a list of the names of available location providers that satisfy the given criteria. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getProviders](../android/location/LocationManager.md))`(`enabledOnly:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns a list of the names of available location providers. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasProvider](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns true if the given location provider exists on this device, irrespective of whether it is currently enabled or not. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLocationEnabled](../android/location/LocationManager.md))`()` Returns the current enabled/disabled state of location. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isProviderEnabled](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns the current enabled/disabled status of the given provider. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerAntennaInfoListener](../android/location/LocationManager.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `listener:` ` [GnssAntennaInfo.Listener](../android/location/GnssAntennaInfo.Listener.md)`)` Registers a GNSS antenna info listener that will receive all changes to antenna info. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerGnssMeasurementsCallback](../android/location/LocationManager.md))`(`request:` ` [GnssMeasurementRequest](../android/location/GnssMeasurementRequest.md)`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [GnssMeasurementsEvent.Callback](../android/location/GnssMeasurementsEvent.Callback.md)`)` Registers a GNSS measurement callback. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerGnssMeasurementsCallback](../android/location/LocationManager.md))`(`callback:` ` [GnssMeasurementsEvent.Callback](../android/location/GnssMeasurementsEvent.Callback.md)`)` Registers a GNSS measurements callback which will run on a binder thread. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerGnssMeasurementsCallback](../android/location/LocationManager.md))`(`callback:` ` [GnssMeasurementsEvent.Callback](../android/location/GnssMeasurementsEvent.Callback.md)`, `handler:` ` [Handler](../android/os/Handler.md)?`)` Registers a GNSS measurements callback. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerGnssMeasurementsCallback](../android/location/LocationManager.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [GnssMeasurementsEvent.Callback](../android/location/GnssMeasurementsEvent.Callback.md)`)` Registers a GNSS measurements callback. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerGnssNavigationMessageCallback](../android/location/LocationManager.md))`(`callback:` ` [GnssNavigationMessage.Callback](../android/location/GnssNavigationMessage.Callback.md)`)` Registers a GNSS navigation message callback which will run on a binder thread. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerGnssNavigationMessageCallback](../android/location/LocationManager.md))`(`callback:` ` [GnssNavigationMessage.Callback](../android/location/GnssNavigationMessage.Callback.md)`, `handler:` ` [Handler](../android/os/Handler.md)?`)` Registers a GNSS navigation message callback. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerGnssNavigationMessageCallback](../android/location/LocationManager.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [GnssNavigationMessage.Callback](../android/location/GnssNavigationMessage.Callback.md)`)` Registers a GNSS navigation message callback. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerGnssStatusCallback](../android/location/LocationManager.md))`(`callback:` ` [GnssStatus.Callback](../android/location/GnssStatus.Callback.md)`)` Registers a GNSS status callback. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerGnssStatusCallback](../android/location/LocationManager.md))`(`callback:` ` [GnssStatus.Callback](../android/location/GnssStatus.Callback.md)`, `handler:` ` [Handler](../android/os/Handler.md)?`)` Registers a GNSS status callback. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerGnssStatusCallback](../android/location/LocationManager.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [GnssStatus.Callback](../android/location/GnssStatus.Callback.md)`)` Registers a GNSS status callback. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeGpsStatusListener](../android/location/LocationManager.md))`(`listener:` ` [GpsStatus.Listener](../android/location/GpsStatus.Listener.md)!`)` Removes a GPS status listener. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeNmeaListener](../android/location/LocationManager.md))`(`listener:` ` [GpsStatus.NmeaListener](../android/location/GpsStatus.NmeaListener.md)`)` No-op method to keep backward-compatibility. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeNmeaListener](../android/location/LocationManager.md))`(`listener:` ` [OnNmeaMessageListener](../android/location/OnNmeaMessageListener.md)`)` Removes an NMEA listener. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeProximityAlert](../android/location/LocationManager.md))`(`intent:` ` [PendingIntent](../android/app/PendingIntent.md)`)` Removes the proximity alert with the given PendingIntent. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeTestProvider](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Removes the test location provider with the given name or does nothing if no such test location provider exists. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeUpdates](../android/location/LocationManager.md))`(`pendingIntent:` ` [PendingIntent](../android/app/PendingIntent.md)`)` Removes location updates for the specified [PendingIntent](../android/app/PendingIntent.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeUpdates](../android/location/LocationManager.md))`(`listener:` ` [LocationListener](../android/location/LocationListener.md)`)` Removes all location updates for the specified [LocationListener](../android/location/LocationListener.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestFlush](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `pendingIntent:` ` [PendingIntent](../android/app/PendingIntent.md)`, `requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Requests that the given provider flush any batched locations to listeners. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestFlush](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `listener:` ` [LocationListener](../android/location/LocationListener.md)`, `requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Requests that the given provider flush any batched locations to listeners. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestLocationUpdates](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `locationRequest:` ` [LocationRequest](../android/location/LocationRequest.md)`, `pendingIntent:` ` [PendingIntent](../android/app/PendingIntent.md)`)` Register for location updates from the specified provider, using a [LocationRequest](../android/location/LocationRequest.md), and callbacks delivered via the provided [PendingIntent](../android/app/PendingIntent.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestLocationUpdates](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `locationRequest:` ` [LocationRequest](../android/location/LocationRequest.md)`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `listener:` ` [LocationListener](../android/location/LocationListener.md)`)` Register for location updates from the specified provider, using a [LocationRequest](../android/location/LocationRequest.md), and a callback on the specified [Executor](../java/util/concurrent/Executor.md). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestLocationUpdates](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `minTimeMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `minDistanceM:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `pendingIntent:` ` [PendingIntent](../android/app/PendingIntent.md)`)` Register for location updates using the named provider, and callbacks delivered via the provided [PendingIntent](../android/app/PendingIntent.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestLocationUpdates](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `minTimeMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `minDistanceM:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `listener:` ` [LocationListener](../android/location/LocationListener.md)`)` Register for location updates from the given provider with the given arguments, and a callback on the [Looper](../android/os/Looper.md) of the calling thread. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestLocationUpdates](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `minTimeMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `minDistanceM:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `listener:` ` [LocationListener](../android/location/LocationListener.md)`, `looper:` ` [Looper](../android/os/Looper.md)?`)` Register for location updates from the given provider with the given arguments, and a callback on the specified [Looper](../android/os/Looper.md). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestLocationUpdates](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `minTimeMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `minDistanceM:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `listener:` ` [LocationListener](../android/location/LocationListener.md)`)` Register for location updates using the named provider, and a callback on the specified [Executor](../java/util/concurrent/Executor.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestLocationUpdates](../android/location/LocationManager.md))`(`minTimeMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `minDistanceM:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `criteria:` ` [Criteria](../android/location/Criteria.md)`, `pendingIntent:` ` [PendingIntent](../android/app/PendingIntent.md)`)` Register for location updates using a provider selected through the given Criteria, and callbacks delivered via the provided [PendingIntent](../android/app/PendingIntent.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestLocationUpdates](../android/location/LocationManager.md))`(`minTimeMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `minDistanceM:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `criteria:` ` [Criteria](../android/location/Criteria.md)`, `listener:` ` [LocationListener](../android/location/LocationListener.md)`, `looper:` ` [Looper](../android/os/Looper.md)?`)` Register for location updates using a provider selected through the given Criteria, and a callback on the specified [Looper](../android/os/Looper.md). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestLocationUpdates](../android/location/LocationManager.md))`(`minTimeMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `minDistanceM:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `criteria:` ` [Criteria](../android/location/Criteria.md)`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `listener:` ` [LocationListener](../android/location/LocationListener.md)`)` Register for location updates using a provider selected through the given Criteria, and a callback on the specified [Executor](../java/util/concurrent/Executor.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestSingleUpdate](../android/location/LocationManager.md))`(`criteria:` ` [Criteria](../android/location/Criteria.md)`, `pendingIntent:` ` [PendingIntent](../android/app/PendingIntent.md)`)` Register for a single location update using a Criteria and pending intent. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestSingleUpdate](../android/location/LocationManager.md))`(`criteria:` ` [Criteria](../android/location/Criteria.md)`, `listener:` ` [LocationListener](../android/location/LocationListener.md)`, `looper:` ` [Looper](../android/os/Looper.md)?`)` Register for a single location update using a Criteria and a callback. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestSingleUpdate](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `pendingIntent:` ` [PendingIntent](../android/app/PendingIntent.md)`)` Register for a single location update using a named provider and pending intent. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestSingleUpdate](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `listener:` ` [LocationListener](../android/location/LocationListener.md)`, `looper:` ` [Looper](../android/os/Looper.md)?`)` Register for a single location update using the named provider and a callback. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [sendExtraCommand](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `command:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `extras:` ` [Bundle](../android/os/Bundle.md)?`)` Sends additional commands to a location provider. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTestProviderEnabled](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the given test provider to be enabled or disabled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTestProviderLocation](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `location:` ` [Location](../android/location/Location.md)`)` Sets a new location for the given test provider. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTestProviderStatus](../android/location/LocationManager.md))`(`provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `extras:` ` [Bundle](../android/os/Bundle.md)?`, `updateTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` This method has no effect as provider status has been deprecated and is no longer supported. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterAntennaInfoListener](../android/location/LocationManager.md))`(`listener:` ` [GnssAntennaInfo.Listener](../android/location/GnssAntennaInfo.Listener.md)`)` Unregisters a GNSS antenna info listener. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterGnssMeasurementsCallback](../android/location/LocationManager.md))`(`callback:` ` [GnssMeasurementsEvent.Callback](../android/location/GnssMeasurementsEvent.Callback.md)`)` Unregisters a GPS Measurement callback. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterGnssNavigationMessageCallback](../android/location/LocationManager.md))`(`callback:` ` [GnssNavigationMessage.Callback](../android/location/GnssNavigationMessage.Callback.md)`)` Unregisters a GNSS Navigation Message callback. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterGnssStatusCallback](../android/location/LocationManager.md))`(`callback:` ` [GnssStatus.Callback](../android/location/GnssStatus.Callback.md)`)` Removes a GNSS status callback. |

## Constants

### ACTION_GNSS_CAPABILITIES_CHANGED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_GNSS_CAPABILITIES_CHANGED: String
```

Broadcast intent action when GNSS capabilities change. This is most common at boot time as GNSS capabilities are queried from the chipset. Includes an intent extra, [EXTRA_GNSS_CAPABILITIES](../android/location/LocationManager.md), with the new [GnssCapabilities](../android/location/GnssCapabilities.md). 

 Value: "android.location.action.GNSS_CAPABILITIES_CHANGED"

**See Also**

- [#EXTRA_GNSS_CAPABILITIES](../android/location/LocationManager.md)
- <https://developer.android.com/reference/kotlin/android/location/LocationManager#getGnssCapabilities()> 

### EXTRA_GNSS_CAPABILITIES

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_GNSS_CAPABILITIES: String
```

Intent extra included with [ACTION_GNSS_CAPABILITIES_CHANGED](../android/location/LocationManager.md) broadcasts, containing the new [GnssCapabilities](../android/location/GnssCapabilities.md). 

 Value: "android.location.extra.GNSS_CAPABILITIES"

**See Also**

- [#ACTION_GNSS_CAPABILITIES_CHANGED](../android/location/LocationManager.md) 

### EXTRA_LOCATION_ENABLED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_LOCATION_ENABLED: String
```

Intent extra included with [MODE_CHANGED_ACTION](../android/location/LocationManager.md) broadcasts, containing the boolean enabled state of location. 

 Value: "android.location.extra.LOCATION_ENABLED"

**See Also**

- [#MODE_CHANGED_ACTION](../android/location/LocationManager.md) 

### EXTRA_PROVIDER_ENABLED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PROVIDER_ENABLED: String
```

Intent extra included with [PROVIDERS_CHANGED_ACTION](../android/location/LocationManager.md) broadcasts, containing the boolean enabled state of the location provider that has changed. 

 Value: "android.location.extra.PROVIDER_ENABLED"

**See Also**

- [#PROVIDERS_CHANGED_ACTION](../android/location/LocationManager.md)
- [#EXTRA_PROVIDER_NAME](../android/location/LocationManager.md) 

### EXTRA_PROVIDER_NAME

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PROVIDER_NAME: String
```

Intent extra included with [PROVIDERS_CHANGED_ACTION](../android/location/LocationManager.md) broadcasts, containing the name of the location provider that has changed. 

 Value: "android.location.extra.PROVIDER_NAME"

**See Also**

- [#PROVIDERS_CHANGED_ACTION](../android/location/LocationManager.md)
- [#EXTRA_PROVIDER_ENABLED](../android/location/LocationManager.md) 

### FUSED_PROVIDER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FUSED_PROVIDER: String
```

Standard name of the fused location provider.

If present, this provider may combine inputs from several other location providers to provide the best possible location fix. It is implicitly used for all requestLocationUpdates APIs that involve a [Criteria](../android/location/Criteria.md). 

 Value: "fused"

### GPS_PROVIDER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GPS_PROVIDER: String
```

Standard name of the GNSS location provider.

If present, this provider determines location using GNSS satellites. The responsiveness and accuracy of location fixes may depend on GNSS signal conditions.

Locations returned from this provider are with respect to the primary GNSS antenna position within the device. [getGnssAntennaInfos()](../android/location/LocationManager.md))may be used to determine the GNSS antenna position with respect to the Android Coordinate System, and convert between them if necessary. This is generally only necessary for high accuracy applications.

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

- [#requestFlush(String, PendingIntent, int)](../android/location/LocationManager.md)) 

### KEY_LOCATIONS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_LOCATIONS: String
```

Key used for an extra holding a array of [Location](../android/location/Location.md) s when a location change is sent using a PendingIntent. This key will only be present if the location change includes multiple (ie, batched) locations, otherwise only [KEY_LOCATION_CHANGED](../android/location/LocationManager.md) will be present. Use [Intent.getParcelableArrayExtra(String)](../android/content/Intent.md))to retrieve the locations.

The array of locations will never be empty, and will ordered from earliest location to latest location, the same as with [LocationListener.onLocationChanged(List)](../android/location/LocationListener.md)). 

 Value: "locations"

**See Also**

- [#requestLocationUpdates(String, LocationRequest, PendingIntent)](../android/location/LocationManager.md)) 

### KEY_LOCATION_CHANGED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_LOCATION_CHANGED: String
```

Key used for an extra holding a [Location](../android/location/Location.md) value when a location change is sent using a PendingIntent. If the location change includes a list of batched locations via [KEY_LOCATIONS](../android/location/LocationManager.md) then this key will still be present, and will hold the last location in the batch. Use [Intent.getParcelableExtra(String)](../android/content/Intent.md))to retrieve the location. 

 Value: "location"

**See Also**

- [#requestLocationUpdates(String, LocationRequest, PendingIntent)](../android/location/LocationManager.md)) 

### KEY_PROVIDER_ENABLED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_PROVIDER_ENABLED: String
```

Key used for an extra holding a boolean enabled/disabled status value when a provider enabled/disabled event is broadcast using a PendingIntent. 

 Value: "providerEnabled"

**See Also**

- [#requestLocationUpdates(String, LocationRequest, PendingIntent)](../android/location/LocationManager.md)) 

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

Broadcast intent action when the device location enabled state changes. From Android R and above, will include a boolean intent extra, [EXTRA_LOCATION_ENABLED](../android/location/LocationManager.md), with the enabled state of location. 

 Value: "android.location.MODE_CHANGED"

**See Also**

- [#EXTRA_LOCATION_ENABLED](../android/location/LocationManager.md)
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

Broadcast intent action when the set of enabled location providers changes. To check the status of a provider, use [isProviderEnabled(java.lang.String)](../android/location/LocationManager.md)). From Android Q and above, will include a string intent extra, [EXTRA_PROVIDER_NAME](../android/location/LocationManager.md), with the name of the provider whose state has changed. From Android R and above, will include a boolean intent extra, [EXTRA_PROVIDER_ENABLED](../android/location/LocationManager.md), with the enabled state of the provider. 

 Value: "android.location.PROVIDERS_CHANGED"

**See Also**

- [#EXTRA_PROVIDER_NAME](../android/location/LocationManager.md)
- [#EXTRA_PROVIDER_ENABLED](../android/location/LocationManager.md)
- [#isProviderEnabled(String)](../android/location/LocationManager.md))

## Public methods

### addGpsStatusListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addGpsStatusListener(listener: GpsStatus.Listener!): Boolean
```

**Deprecated:** *Use [registerGnssStatusCallback(android.location.GnssStatus.Callback,android.os.Handler)](../android/location/LocationManager.md))or [registerGnssStatusCallback(java.util.concurrent.Executor,android.location.GnssStatus.Callback)](../android/location/LocationManager.md))instead.*

Adds a GPS status listener. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [GpsStatus.Listener](../android/location/GpsStatus.Listener.md)!:GPS status listener object to register |

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

**Deprecated:** *Use [addNmeaListener(android.location.OnNmeaMessageListener,android.os.Handler)](../android/location/LocationManager.md))or [addNmeaListener(java.util.concurrent.Executor,android.location.OnNmeaMessageListener)](../android/location/LocationManager.md))instead.*

No-op method to keep backward-compatibility. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [GpsStatus.NmeaListener](../android/location/GpsStatus.NmeaListener.md):This value cannot be`null`. |

### addNmeaListener

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addNmeaListener(listener: OnNmeaMessageListener): Boolean
```

**Deprecated:** *Use [addNmeaListener(android.location.OnNmeaMessageListener,android.os.Handler)](../android/location/LocationManager.md))or [addNmeaListener(java.util.concurrent.Executor,android.location.OnNmeaMessageListener)](../android/location/LocationManager.md))instead.*

Adds an NMEA listener.

See [addNmeaListener(java.util.concurrent.Executor,android.location.OnNmeaMessageListener)](../android/location/LocationManager.md))for more detail on how this method works. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [OnNmeaMessageListener](../android/location/OnNmeaMessageListener.md):the listener to register This value cannot be`null`. |

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

See [addNmeaListener(java.util.concurrent.Executor,android.location.OnNmeaMessageListener)](../android/location/LocationManager.md))for more detail on how this method works. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [OnNmeaMessageListener](../android/location/OnNmeaMessageListener.md):the listener to register This value cannot be`null`. |
| `handler` | [Handler](../android/os/Handler.md)?:the handler that the listener runs on This value may be`null`. |

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

Adds an NMEA listener. GNSS NMEA information will only be received while the [GPS_PROVIDER](../android/location/LocationManager.md) is enabled, and while the client app is in the foreground. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [OnNmeaMessageListener](../android/location/OnNmeaMessageListener.md):the listener to register This value cannot be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):the executor that the listener runs on This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |

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

The fired intent will have a boolean extra added with key [KEY_PROXIMITY_ENTERING](../android/location/LocationManager.md). If the value is true, the device is entering the proximity region; if false, it is exiting.

Due to the approximate nature of position estimation, if the device passes through the given area briefly, it is possible that no Intent will be fired. Similarly, an intent could be fired if the device passes very close to the given area but does not actually enter it.

Before API version 17, this method could be used with [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md) or [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md). From API version 17 and onwards, this method requires [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md) permission. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md) or [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `latitude` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the latitude of the central point of the alert region |
| `longitude` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the longitude of the central point of the alert region |
| `radius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the radius of the central point of the alert region in meters |
| --- | --- |
| `expiration` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):expiration realtime for this proximity alert in milliseconds, or -1 to indicate no expiration |
| `pendingIntent` | [PendingIntent](../android/app/PendingIntent.md):a [PendingIntent](../android/app/PendingIntent.md) that will sent when entry to or exit from the alert region is detected This value cannot be`null`. |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md) permission is not present |

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
| `properties` | [ProviderProperties](../android/location/provider/ProviderProperties.md):This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if properties is null |
| `java.lang.SecurityException` | if [mock location app op](../android/app/AppOpsManager.md) is not set to [allowed](../android/app/AppOpsManager.md) for your app. |

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
| `properties` | [ProviderProperties](../android/location/provider/ProviderProperties.md):the provider properties This value cannot be`null`. |
| `extraAttributionTags` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:additional attribution tags associated with this provider This value cannot be`null`. |
| --- | --- |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if properties is null |
| `java.lang.SecurityException` | if [mock location app op](../android/app/AppOpsManager.md) is not set to [allowed](../android/app/AppOpsManager.md) for your app. |

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
| `powerUsage` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.location.provider.ProviderProperties#POWER_USAGE_LOW](../android/location/provider/ProviderProperties.md), [android.location.provider.ProviderProperties#POWER_USAGE_MEDIUM](../android/location/provider/ProviderProperties.md), or [android.location.provider.ProviderProperties#POWER_USAGE_HIGH](../android/location/provider/ProviderProperties.md) |
| `accuracy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.location.provider.ProviderProperties#ACCURACY_FINE](../android/location/provider/ProviderProperties.md), or [android.location.provider.ProviderProperties#ACCURACY_COARSE](../android/location/provider/ProviderProperties.md) |
| --- | --- |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if provider is null |
| `java.lang.SecurityException` | if [mock location app op](../android/app/AppOpsManager.md) is not set to [allowed](../android/app/AppOpsManager.md) for your app. |

### clearTestProviderEnabled

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearTestProviderEnabled(provider: String): Unit
```

**Deprecated:** *Use [setTestProviderEnabled(java.lang.String,boolean)](../android/location/LocationManager.md))instead.*

Equivalent to calling [setTestProviderEnabled(java.lang.String,boolean)](../android/location/LocationManager.md))to disable a test provider.

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
| `criteria` | [Criteria](../android/location/Criteria.md):the criteria that need to be matched This value cannot be`null`. |
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

Asynchronously returns a single current location fix from the given provider based on the given [LocationRequest](../android/location/LocationRequest.md). This may activate sensors in order to compute a new location, unlike [getLastKnownLocation(java.lang.String)](../android/location/LocationManager.md)), which will only return a cached fix if available. The given callback will be invoked once and only once, either with a valid location or with a null location if the provider was unable to generate a valid location.

A client may supply an optional [CancellationSignal](../android/os/CancellationSignal.md). If this is used to cancel the operation, no callback should be expected after the cancellation.

This method may return locations from the very recent past (on the order of several seconds), but will never return older locations (for example, several minutes old or older). Clients may rely upon the guarantee that if this method returns a location, it will represent the best estimation of the location of the device in the present moment.

Clients calling this method from the background may notice that the method fails to determine a valid location fix more often than while in the foreground. Background applications may be throttled in their location accesses to some degree. The given location request may be used to provide hints on how a fresh location is computed if necessary. In particular [LocationRequest.getDurationMillis()](../android/location/LocationRequest.md))can be used to provide maximum duration allowed before failing. The system will always cap the maximum amount of time a request for current location may run to some reasonable value (less than a minute for example) before the request is failed. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md) or [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](../android/location/LocationManager.md))This value cannot be`null`. |
| `locationRequest` | [LocationRequest](../android/location/LocationRequest.md):the location request containing location parameters This value cannot be`null`. |
| `cancellationSignal` | [CancellationSignal](../android/os/CancellationSignal.md)?:an optional signal that allows for cancelling this call This value may be`null`. |
| --- | --- |
| `executor` | [Executor](../java/util/concurrent/Executor.md):the callback will take place on this [Executor](../java/util/concurrent/Executor.md) This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `consumer` | [Consumer](../java/util/function/Consumer.md)\< [Location](../android/location/Location.md)!\>:the callback invoked with either a [Location](../android/location/Location.md) or null |

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

See [getCurrentLocation(java.lang.String,android.location.LocationRequest,android.os.CancellationSignal,java.util.concurrent.Executor,java.util.function.Consumer)](../android/location/LocationManager.md))for more information. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md) or [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](../android/location/LocationManager.md))This value cannot be`null`. |
| `cancellationSignal` | [CancellationSignal](../android/os/CancellationSignal.md)?:an optional signal that allows for cancelling this call This value may be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):the callback will take place on this [Executor](../java/util/concurrent/Executor.md) This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| --- | --- |
| `consumer` | [Consumer](../java/util/function/Consumer.md)\< [Location](../android/location/Location.md)!\>:the callback invoked with either a [Location](../android/location/Location.md) or null |

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
| [GnssCapabilities](../android/location/GnssCapabilities.md) | This value cannot be`null`. |

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

**Deprecated:** *GpsStatus APIs are deprecated, use [GnssStatus](../android/location/GnssStatus.md) APIs instead. No longer supported in apps targeting S and above.*

Retrieves information about the current status of the GPS engine. This should only be called from within the [GpsStatus.Listener.onGpsStatusChanged](../android/location/GpsStatus.Listener.md))callback to ensure that the data is copied atomically. The caller may either pass in an existing [GpsStatus](../android/location/GpsStatus.md) object to be overwritten, or pass null to create a new [GpsStatus](../android/location/GpsStatus.md) object. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `status` | [GpsStatus](../android/location/GpsStatus.md)?:object containing GPS status details, or null. |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| [GpsStatus](../android/location/GpsStatus.md)? | status object containing updated GPS status. |

### getLastKnownLocation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLastKnownLocation(provider: String): Location?
```

Gets the last known location from the given provider, or null if there is no last known location. The returned location may be quite old in some circumstances, so the age of the location should always be checked.

This will never activate sensors to compute a new location, and will only ever return a cached location.

See also [getCurrentLocation(java.lang.String,android.os.CancellationSignal,java.util.concurrent.Executor,java.util.function.Consumer)](../android/location/LocationManager.md))which will always attempt to return a current location, but will potentially use additional power in the course of the attempt as compared to this method. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md) or [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](../android/location/LocationManager.md))This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Location](../android/location/Location.md)? | the last known location for the given provider, or null if not available |

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

**Deprecated:** *This method has no way to indicate that a provider's properties are unknown, and so may return incorrect results on rare occasions. Use [getProviderProperties(java.lang.String)](../android/location/LocationManager.md))instead.*

Returns the information about the location provider with the given name, or null if no provider exists by that name.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](../android/location/LocationManager.md))This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [LocationProvider](../android/location/LocationProvider.md)? | location provider information, or null if provider does not exist |

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
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](../android/location/LocationManager.md))This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [ProviderProperties](../android/location/provider/ProviderProperties.md)? | location provider properties, or null if properties are currently unknown |

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
| `criteria` | [Criteria](../android/location/Criteria.md):the criteria that providers must match This value cannot be`null`. |
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

Returns a list of the names of available location providers. If`enabledOnly`is false, this is functionally the same as [getAllProviders()](../android/location/LocationManager.md)).

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

Returns the current enabled/disabled state of location. To listen for changes, see [MODE_CHANGED_ACTION](../android/location/LocationManager.md).

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if location is enabled and false if location is disabled. |

### isProviderEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isProviderEnabled(provider: String): Boolean
```

Returns the current enabled/disabled status of the given provider. To listen for changes, see [PROVIDERS_CHANGED_ACTION](../android/location/LocationManager.md). Before API version [android.os.Build.VERSION_CODES#LOLLIPOP](../android/os/Build.VERSION_CODES.md), this method would throw [SecurityException](../java/lang/SecurityException.md) if the location permissions were not sufficient to use the specified provider.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](../android/location/LocationManager.md))This value cannot be`null`. |

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

Registers a GNSS antenna info listener that will receive all changes to antenna info. Use [getGnssAntennaInfos()](../android/location/LocationManager.md))to get current antenna info.

Not all GNSS chipsets support antenna info updates, see [getGnssCapabilities()](../android/location/LocationManager.md)). If unsupported, the listener will never be invoked.

Prior to Android S, this requires the [Manifest.permission.ACCESS_FINE_LOCATION](../android/Manifest.permission.md) permission.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md):the executor that the listener runs on This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `listener` | [GnssAntennaInfo.Listener](../android/location/GnssAntennaInfo.Listener.md):the listener to register This value cannot be`null`. |

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
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [GnssMeasurementRequest](../android/location/GnssMeasurementRequest.md):extra parameters to pass to GNSS measurement provider. For example, if [android.location.GnssMeasurementRequest#isFullTracking()](../android/location/GnssMeasurementRequest.md))is true, GNSS chipset switches off duty cycling. This value cannot be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):the executor that the callback runs on This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [GnssMeasurementsEvent.Callback](../android/location/GnssMeasurementsEvent.Callback.md):a [GnssMeasurementsEvent.Callback](../android/location/GnssMeasurementsEvent.Callback.md) object to register. This value cannot be`null`. |
| --- | --- |

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

See [for more detail on how this method works.](../android/location/LocationManager.md)) 

### registerGnssMeasurementsCallback

```
open fun registerGnssMeasurementsCallback(
    callback: GnssMeasurementsEvent.Callback, 
    handler: Handler?
): Boolean
```

Registers a GNSS measurements callback.

See [for more detail on how this method works.](../android/location/LocationManager.md)) 

### registerGnssMeasurementsCallback

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun registerGnssMeasurementsCallback(
    executor: Executor, 
    callback: GnssMeasurementsEvent.Callback
): Boolean
```

Registers a GNSS measurements callback. GNSS measurements information will only be received while the [GPS_PROVIDER](../android/location/LocationManager.md) is enabled, and while the client app is in the foreground.

Not all GNSS chipsets support measurements updates, see [getGnssCapabilities()](../android/location/LocationManager.md)).

On Android R devices that have not yet upgraded to Android R QPR1, using this API will cause unavoidable crashes in the client application when GNSS measurements are received. If a client needs to receive GNSS measurements on Android R devices that have not been upgraded to QPR1, clients are instead encouraged to use [LocationManagerCompat.registerGnssMeasurementsCallback()](../androidx/core/location/LocationManagerCompat.md))from the compat libraries instead to avoid this crash. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md):the executor that the callback runs on This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [GnssMeasurementsEvent.Callback](../android/location/GnssMeasurementsEvent.Callback.md):the callback to register This value cannot be`null`. |

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

**Deprecated:** *Use [registerGnssNavigationMessageCallback(android.location.GnssNavigationMessage.Callback,android.os.Handler)](../android/location/LocationManager.md))or [registerGnssNavigationMessageCallback(java.util.concurrent.Executor,android.location.GnssNavigationMessage.Callback)](../android/location/LocationManager.md))instead.*

Registers a GNSS navigation message callback which will run on a binder thread.

See [registerGnssNavigationMessageCallback(java.util.concurrent.Executor,android.location.GnssNavigationMessage.Callback)](../android/location/LocationManager.md))for more detail on how this method works.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [GnssNavigationMessage.Callback](../android/location/GnssNavigationMessage.Callback.md):the callback to register This value cannot be`null`. |

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

See [registerGnssNavigationMessageCallback(java.util.concurrent.Executor,android.location.GnssNavigationMessage.Callback)](../android/location/LocationManager.md))for more detail on how this method works. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [GnssNavigationMessage.Callback](../android/location/GnssNavigationMessage.Callback.md):the callback to register This value cannot be`null`. |
| `handler` | [Handler](../android/os/Handler.md)?:the handler that the callback runs on This value may be`null`. |

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

Registers a GNSS navigation message callback. GNSS navigation messages will only be received while the [GPS_PROVIDER](../android/location/LocationManager.md) is enabled, and while the client app is in the foreground.

Not all GNSS chipsets support navigation message updates, see [getGnssCapabilities()](../android/location/LocationManager.md)). 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md):the executor that the callback runs on This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [GnssNavigationMessage.Callback](../android/location/GnssNavigationMessage.Callback.md):the callback to register This value cannot be`null`. |

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

**Deprecated:** *Use [registerGnssStatusCallback(android.location.GnssStatus.Callback,android.os.Handler)](../android/location/LocationManager.md))or [registerGnssStatusCallback(java.util.concurrent.Executor,android.location.GnssStatus.Callback)](../android/location/LocationManager.md))instead.*

Registers a GNSS status callback. This method must be called from a [Looper](../android/os/Looper.md) thread, and callbacks will occur on that looper.

See [registerGnssStatusCallback(java.util.concurrent.Executor,android.location.GnssStatus.Callback)](../android/location/LocationManager.md))for more detail on how this method works. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [GnssStatus.Callback](../android/location/GnssStatus.Callback.md):the callback to register This value cannot be`null`. |

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

See [registerGnssStatusCallback(java.util.concurrent.Executor,android.location.GnssStatus.Callback)](../android/location/LocationManager.md))for more detail on how this method works. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [GnssStatus.Callback](../android/location/GnssStatus.Callback.md):the callback to register This value cannot be`null`. |
| `handler` | [Handler](../android/os/Handler.md)?:the handler the callback runs on This value may be`null`. |

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

Registers a GNSS status callback. GNSS status information will only be received while the [GPS_PROVIDER](../android/location/LocationManager.md) is enabled, and while the client app is in the foreground. 
Requires [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md):the executor that the callback runs on This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [GnssStatus.Callback](../android/location/GnssStatus.Callback.md):the callback to register This value cannot be`null`. |

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

**Deprecated:** *use [unregisterGnssStatusCallback(android.location.GnssStatus.Callback)](../android/location/LocationManager.md))instead. No longer supported in apps targeting S and above.*

Removes a GPS status listener.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [GpsStatus.Listener](../android/location/GpsStatus.Listener.md)!:GPS status listener object to remove |

### removeNmeaListener

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeNmeaListener(listener: GpsStatus.NmeaListener): Unit
```

**Deprecated:** *Use [removeNmeaListener(android.location.OnNmeaMessageListener)](../android/location/LocationManager.md))instead.*

No-op method to keep backward-compatibility.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [GpsStatus.NmeaListener](../android/location/GpsStatus.NmeaListener.md):This value cannot be`null`. |

### removeNmeaListener

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeNmeaListener(listener: OnNmeaMessageListener): Unit
```

Removes an NMEA listener.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [OnNmeaMessageListener](../android/location/OnNmeaMessageListener.md):a [OnNmeaMessageListener](../android/location/OnNmeaMessageListener.md) object to remove This value cannot be`null`. |

### removeProximityAlert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeProximityAlert(intent: PendingIntent): Unit
```

Removes the proximity alert with the given PendingIntent.

Before API version 17, this method could be used with [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md) or [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md). From API version 17 and onwards, this method requires [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md) permission. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md) or [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md) 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md) or [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [PendingIntent](../android/app/PendingIntent.md):the PendingIntent that no longer needs to be notified of proximity alerts This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if intent is null |
| `java.lang.SecurityException` | if [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md) permission is not present |

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
| `java.lang.SecurityException` | if [mock location app op](../android/app/AppOpsManager.md) is not set to [allowed](../android/app/AppOpsManager.md) for your app. |

### removeUpdates

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeUpdates(pendingIntent: PendingIntent): Unit
```

Removes location updates for the specified [PendingIntent](../android/app/PendingIntent.md). Following this call, the PendingIntent will no longer receive location updates.

See [removeUpdates(android.location.LocationListener)](../android/location/LocationManager.md))for more detail on how this method works.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pendingIntent` | [PendingIntent](../android/app/PendingIntent.md):pending intent that no longer needs location updates This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------|
| `java.lang.IllegalArgumentException` | if pendingIntent is null |

### removeUpdates

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeUpdates(listener: LocationListener): Unit
```

Removes all location updates for the specified [LocationListener](../android/location/LocationListener.md). The given listener is guaranteed not to receive any invocations that**happens-after**this method is invoked.

If the given listener has any batched requests, this method will not flush any incomplete location batches before stopping location updates. If you wish to flush any pending locations before stopping, you must first call [requestFlush(java.lang.String,android.location.LocationListener,int)](../android/location/LocationManager.md))and then call this method once the flush is complete. If this method is invoked before the flush is complete, you may not receive the flushed locations. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md) or [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md) 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md) or [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [LocationListener](../android/location/LocationListener.md):listener that no longer needs location updates This value cannot be`null`. |

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

Requests that the given provider flush any batched locations to listeners. The given PendingIntent (registered with the provider) will be sent with [KEY_FLUSH_COMPLETE](../android/location/LocationManager.md) present in the extra keys, and`requestCode`as the corresponding value.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](../android/location/LocationManager.md))This value cannot be`null`. |
| `pendingIntent` | [PendingIntent](../android/app/PendingIntent.md):a pendingIntent registered under the provider This value cannot be`null`. |
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an arbitrary integer that will be passed back as the extra value for [KEY_FLUSH_COMPLETE](../android/location/LocationManager.md) |
| --- | --- |

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

Requests that the given provider flush any batched locations to listeners. The given listener (registered with the provider) will have [LocationListener.onFlushComplete(int)](../android/location/LocationListener.md))invoked with the given result code after any locations that were flushed have been delivered. If [removeUpdates(android.location.LocationListener)](../android/location/LocationManager.md))is invoked before the flush callback is executed, then the flush callback will never be executed.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](../android/location/LocationManager.md))This value cannot be`null`. |
| `listener` | [LocationListener](../android/location/LocationListener.md):a listener registered under the provider This value cannot be`null`. |
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an arbitrary integer passed through to [LocationListener.onFlushComplete(int)](../android/location/LocationListener.md)) |
| --- | --- |

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

Register for location updates from the specified provider, using a [LocationRequest](../android/location/LocationRequest.md), and callbacks delivered via the provided [PendingIntent](../android/app/PendingIntent.md).

The delivered pending intents will contain extras with the callback information. The keys used for the extras are [KEY_LOCATION_CHANGED](../android/location/LocationManager.md) and [KEY_PROVIDER_ENABLED](../android/location/LocationManager.md). See the documentation for each respective extra key for information on the values.

To unregister for location updates, use [removeUpdates(android.app.PendingIntent)](../android/location/LocationManager.md)). 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md) or [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](../android/location/LocationManager.md))This value cannot be`null`. |
| `locationRequest` | [LocationRequest](../android/location/LocationRequest.md):the location request containing location parameters This value cannot be`null`. |
| `pendingIntent` | [PendingIntent](../android/app/PendingIntent.md):the pending intent to send location updates This value cannot be`null`. |
| --- | --- |

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

Register for location updates from the specified provider, using a [LocationRequest](../android/location/LocationRequest.md), and a callback on the specified [Executor](../java/util/concurrent/Executor.md).

Only one request can be registered for each unique listener/provider pair, so any subsequent requests with the same provider and listener will overwrite all associated arguments. The same listener may be used across multiple providers with different requests for each provider.

It may take some time to receive the first location update depending on the conditions the device finds itself in. In order to take advantage of cached locations, application may consider using [getLastKnownLocation(java.lang.String)](../android/location/LocationManager.md))or [getCurrentLocation(java.lang.String,android.location.LocationRequest,android.os.CancellationSignal,java.util.concurrent.Executor,java.util.function.Consumer)](../android/location/LocationManager.md))instead.

See [LocationRequest](../android/location/LocationRequest.md) documentation for an explanation of various request parameters and how they can affect the received locations.

If your application wants to passively observe location updates from all providers, then use the [PASSIVE_PROVIDER](../android/location/LocationManager.md). This provider does not turn on or modify active location providers, so you do not need to be as careful about minimum time and minimum distance parameters. However, if your application performs heavy work on a location update (such as network activity) then you should set an explicit fastest interval on your location request in case another application enables a location provider with extremely fast updates.

In case the provider you have selected is disabled, location updates will cease, and a provider availability update will be sent. As soon as the provider is enabled again, another provider availability update will be sent and location updates will resume.

Locations returned from [GPS_PROVIDER](../android/location/LocationManager.md) are with respect to the primary GNSS antenna position within the device. [getGnssAntennaInfos()](../android/location/LocationManager.md))may be used to determine the GNSS antenna position with respect to the Android Coordinate System, and convert between them if necessary. This is generally only necessary for high accuracy applications.

When location callbacks are invoked, the system will hold a wakelock on your application's behalf for some period of time, but not indefinitely. If your application requires a long running wakelock within the location callback, you should acquire it yourself.

Spamming location requests is a drain on system resources, and the system has preventative measures in place to ensure that this behavior will never result in more locations than could be achieved with a single location request with an equivalent interval that is left in place the whole time. As part of this amelioration, applications that target Android S and above may receive cached or historical locations through their listener. These locations will never be older than the interval of the location request.

To unregister for location updates, use [removeUpdates(android.location.LocationListener)](../android/location/LocationManager.md)). 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md) or [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](../android/location/LocationManager.md))This value cannot be`null`. |
| `locationRequest` | [LocationRequest](../android/location/LocationRequest.md):the location request containing location parameters This value cannot be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):the executor handling listener callbacks This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| --- | --- |
| `listener` | [LocationListener](../android/location/LocationListener.md):the listener to receive location updates This value cannot be`null`. |

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

Register for location updates using the named provider, and callbacks delivered via the provided [PendingIntent](../android/app/PendingIntent.md).

See [requestLocationUpdates(java.lang.String,android.location.LocationRequest,android.app.PendingIntent)](../android/location/LocationManager.md))for more detail on how this method works. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md) or [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](../android/location/LocationManager.md))This value cannot be`null`. |
| `minTimeMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):minimum time interval between location updates in milliseconds |
| `minDistanceM` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):minimum distance between location updates in meters |
| --- | --- |
| `pendingIntent` | [PendingIntent](../android/app/PendingIntent.md):the pending intent to send location updates This value cannot be`null`. |

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

Register for location updates from the given provider with the given arguments, and a callback on the [Looper](../android/os/Looper.md) of the calling thread.

See [requestLocationUpdates(java.lang.String,android.location.LocationRequest,java.util.concurrent.Executor,android.location.LocationListener)](../android/location/LocationManager.md))for more detail on how this method works.

Prior to Jellybean, the minTime parameter was only a hint, and some location provider implementations ignored it. For Jellybean and onwards however, it is mandatory for Android compatible devices to observe both the minTime and minDistance parameters. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md) or [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](../android/location/LocationManager.md))This value cannot be`null`. |
| `minTimeMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):minimum time interval between location updates in milliseconds |
| `minDistanceM` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):minimum distance between location updates in meters |
| --- | --- |
| `listener` | [LocationListener](../android/location/LocationListener.md):the listener to receive location updates This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------|
| `java.lang.IllegalArgumentException` | if listener is null |
| `java.lang.RuntimeException` | if the calling thread has no Looper |
| `java.lang.SecurityException` | if no suitable permission is present |
| --- | --- |

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

Register for location updates from the given provider with the given arguments, and a callback on the specified [Looper](../android/os/Looper.md).

See [requestLocationUpdates(java.lang.String,android.location.LocationRequest,java.util.concurrent.Executor,android.location.LocationListener)](../android/location/LocationManager.md))for more detail on how this method works.

Prior to Jellybean, the minTime parameter was only a hint, and some location provider implementations ignored it. For Jellybean and onwards however, it is mandatory for Android compatible devices to observe both the minTime and minDistance parameters. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md) or [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](../android/location/LocationManager.md))This value cannot be`null`. |
| `minTimeMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):minimum time interval between location updates in milliseconds |
| `minDistanceM` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):minimum distance between location updates in meters |
| --- | --- |
| `listener` | [LocationListener](../android/location/LocationListener.md):the listener to receive location updates This value cannot be`null`. |
| `looper` | [Looper](../android/os/Looper.md)?:the looper handling listener callbacks, or null to use the looper of the calling thread |

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

Register for location updates using the named provider, and a callback on the specified [Executor](../java/util/concurrent/Executor.md).

See [requestLocationUpdates(java.lang.String,android.location.LocationRequest,java.util.concurrent.Executor,android.location.LocationListener)](../android/location/LocationManager.md))for more detail on how this method works.

Prior to Jellybean, the minTime parameter was only a hint, and some location provider implementations ignored it. For Jellybean and onwards however, it is mandatory for Android compatible devices to observe both the minTime and minDistance parameters. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md) or [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](../android/location/LocationManager.md))This value cannot be`null`. |
| `minTimeMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):minimum time interval between location updates in milliseconds |
| `minDistanceM` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):minimum distance between location updates in meters |
| --- | --- |
| `executor` | [Executor](../java/util/concurrent/Executor.md):the executor handling listener callbacks This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `listener` | [LocationListener](../android/location/LocationListener.md):the listener to receive location updates This value cannot be`null`. |

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

**Deprecated:** *Use [requestLocationUpdates(java.lang.String,long,float,android.app.PendingIntent)](../android/location/LocationManager.md))instead to explicitly select a provider.*

Register for location updates using a provider selected through the given Criteria, and callbacks delivered via the provided [PendingIntent](../android/app/PendingIntent.md).

Note: Since Android KitKat, Criteria requests will always result in using the [FUSED_PROVIDER](../android/location/LocationManager.md).

See [requestLocationUpdates(java.lang.String,long,float,android.app.PendingIntent)](../android/location/LocationManager.md))for more detail on how this method works. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md) or [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `minTimeMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):minimum time interval between location updates in milliseconds |
| `minDistanceM` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):minimum distance between location updates in meters |
| `criteria` | [Criteria](../android/location/Criteria.md):contains parameters to choose the appropriate provider for location updates This value cannot be`null`. |
| --- | --- |
| `pendingIntent` | [PendingIntent](../android/app/PendingIntent.md):the pending intent to send location updates This value cannot be`null`. |

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

**Deprecated:** *Use [requestLocationUpdates(java.lang.String,long,float,android.location.LocationListener,android.os.Looper)](../android/location/LocationManager.md))instead to explicitly select a provider.*

Register for location updates using a provider selected through the given Criteria, and a callback on the specified [Looper](../android/os/Looper.md).

Note: Since Android KitKat, Criteria requests will always result in using the [FUSED_PROVIDER](../android/location/LocationManager.md).

See [requestLocationUpdates(java.lang.String,android.location.LocationRequest,java.util.concurrent.Executor,android.location.LocationListener)](../android/location/LocationManager.md))for more detail on how this method works. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md) or [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `minTimeMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):minimum time interval between location updates in milliseconds |
| `minDistanceM` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):minimum distance between location updates in meters |
| `criteria` | [Criteria](../android/location/Criteria.md):contains parameters to choose the appropriate provider for location updates This value cannot be`null`. |
| --- | --- |
| `listener` | [LocationListener](../android/location/LocationListener.md):the listener to receive location updates This value cannot be`null`. |
| `looper` | [Looper](../android/os/Looper.md)?:This value may be`null`. |

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

**Deprecated:** *Use [requestLocationUpdates(java.lang.String,long,float,java.util.concurrent.Executor,android.location.LocationListener)](../android/location/LocationManager.md))instead to explicitly select a provider.*

Register for location updates using a provider selected through the given Criteria, and a callback on the specified [Executor](../java/util/concurrent/Executor.md).

Note: Since Android KitKat, Criteria requests will always result in using the [FUSED_PROVIDER](../android/location/LocationManager.md).

See [requestLocationUpdates(java.lang.String,android.location.LocationRequest,java.util.concurrent.Executor,android.location.LocationListener)](../android/location/LocationManager.md))for more detail on how this method works. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md) or [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `minTimeMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):minimum time interval between location updates in milliseconds |
| `minDistanceM` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):minimum distance between location updates in meters |
| `criteria` | [Criteria](../android/location/Criteria.md):contains parameters to choose the appropriate provider for location updates This value cannot be`null`. |
| --- | --- |
| `executor` | [Executor](../java/util/concurrent/Executor.md):the executor handling listener callbacks This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `listener` | [LocationListener](../android/location/LocationListener.md):the listener to receive location updates This value cannot be`null`. |

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

**Deprecated:** *Use [getCurrentLocation(java.lang.String,android.os.CancellationSignal,java.util.concurrent.Executor,java.util.function.Consumer)](../android/location/LocationManager.md))instead as it does not carry a risk of extreme battery drain.*

Register for a single location update using a Criteria and pending intent.

Note: Since Android KitKat, Criteria requests will always result in using the [FUSED_PROVIDER](../android/location/LocationManager.md).

See [requestLocationUpdates(long,float,android.location.Criteria,android.app.PendingIntent)](../android/location/LocationManager.md))for more detail on how to use this method. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md) or [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `criteria` | [Criteria](../android/location/Criteria.md):contains parameters to choose the appropriate provider for location updates This value cannot be`null`. |
| `pendingIntent` | [PendingIntent](../android/app/PendingIntent.md):the pending intent to send location updates This value cannot be`null`. |

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

**Deprecated:** *Use [getCurrentLocation(java.lang.String,android.os.CancellationSignal,java.util.concurrent.Executor,java.util.function.Consumer)](../android/location/LocationManager.md))instead as it does not carry a risk of extreme battery drain.*

Register for a single location update using a Criteria and a callback.

Note: Since Android KitKat, Criteria requests will always result in using the [FUSED_PROVIDER](../android/location/LocationManager.md).

See [requestLocationUpdates(long,float,android.location.Criteria,android.app.PendingIntent)](../android/location/LocationManager.md))for more detail on how to use this method. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md) or [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `criteria` | [Criteria](../android/location/Criteria.md):contains parameters to choose the appropriate provider for location updates This value cannot be`null`. |
| `listener` | [LocationListener](../android/location/LocationListener.md):the listener to receive location updates This value cannot be`null`. |
| `looper` | [Looper](../android/os/Looper.md)?:the looper handling listener callbacks, or null to use the looper of the calling thread |
| --- | --- |

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

**Deprecated:** *Use [getCurrentLocation(java.lang.String,android.os.CancellationSignal,java.util.concurrent.Executor,java.util.function.Consumer)](../android/location/LocationManager.md))instead as it does not carry a risk of extreme battery drain.*

Register for a single location update using a named provider and pending intent.

See [requestLocationUpdates(long,float,android.location.Criteria,android.app.PendingIntent)](../android/location/LocationManager.md))for more detail on how to use this method. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md) or [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](../android/location/LocationManager.md))This value cannot be`null`. |
| `pendingIntent` | [PendingIntent](../android/app/PendingIntent.md):the pending intent to send location updates This value cannot be`null`. |

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

**Deprecated:** *Use [getCurrentLocation(java.lang.String,android.os.CancellationSignal,java.util.concurrent.Executor,java.util.function.Consumer)](../android/location/LocationManager.md))instead as it does not carry a risk of extreme battery drain.*

Register for a single location update using the named provider and a callback.

See [requestLocationUpdates(java.lang.String,long,float,android.location.LocationListener,android.os.Looper)](../android/location/LocationManager.md))for more detail on how to use this method. 
Requires [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md) or [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md)

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](../android/location/LocationManager.md))This value cannot be`null`. |
| `listener` | [LocationListener](../android/location/LocationListener.md):the listener to receive location updates This value cannot be`null`. |
| `looper` | [Looper](../android/os/Looper.md)?:the looper handling listener callbacks, or null to use the looper of the calling thread |
| --- | --- |

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
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a provider listed by [getAllProviders()](../android/location/LocationManager.md))This value cannot be`null`. |
| `command` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name of the command to send to the provider This value cannot be`null`. |
| `extras` | [Bundle](../android/os/Bundle.md)?:optional arguments for the command, or null |
| --- | --- |

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
| `java.lang.SecurityException` | if [mock location app op](../android/app/AppOpsManager.md) is not set to [allowed](../android/app/AppOpsManager.md) for your app. |
| `java.lang.IllegalArgumentException` | if provider is null or not a test provider |

### setTestProviderLocation

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTestProviderLocation(
    provider: String, 
    location: Location
): Unit
```

Sets a new location for the given test provider. This location will be identiable as a mock location to all clients via [Location.isMock()](../android/location/Location.md)).

The location object must have a minimum number of fields set to be considered valid, as per documentation on [Location](../android/location/Location.md) class.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the provider name This value cannot be`null`. |
| `location` | [Location](../android/location/Location.md):the mock location This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if [mock location app op](../android/app/AppOpsManager.md) is not set to [allowed](../android/app/AppOpsManager.md) for your app. |
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
| `extras` | [Bundle](../android/os/Bundle.md)?:This value may be`null`. |

### unregisterAntennaInfoListener

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterAntennaInfoListener(listener: GnssAntennaInfo.Listener): Unit
```

Unregisters a GNSS antenna info listener.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [GnssAntennaInfo.Listener](../android/location/GnssAntennaInfo.Listener.md):a [GnssAntennaInfo.Listener](../android/location/GnssAntennaInfo.Listener.md) object to remove This value cannot be`null`. |

### unregisterGnssMeasurementsCallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterGnssMeasurementsCallback(callback: GnssMeasurementsEvent.Callback): Unit
```

Unregisters a GPS Measurement callback.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [GnssMeasurementsEvent.Callback](../android/location/GnssMeasurementsEvent.Callback.md):a [GnssMeasurementsEvent.Callback](../android/location/GnssMeasurementsEvent.Callback.md) object to remove. This value cannot be`null`. |

### unregisterGnssNavigationMessageCallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterGnssNavigationMessageCallback(callback: GnssNavigationMessage.Callback): Unit
```

Unregisters a GNSS Navigation Message callback.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [GnssNavigationMessage.Callback](../android/location/GnssNavigationMessage.Callback.md):a [GnssNavigationMessage.Callback](../android/location/GnssNavigationMessage.Callback.md) object to remove. This value cannot be`null`. |

### unregisterGnssStatusCallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unregisterGnssStatusCallback(callback: GnssStatus.Callback): Unit
```

Removes a GNSS status callback.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [GnssStatus.Callback](../android/location/GnssStatus.Callback.md):GNSS status callback object to remove This value cannot be`null`. |
