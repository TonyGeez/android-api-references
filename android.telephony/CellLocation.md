# CellLocation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CellLocation

Kotlin| [Java](https://developer.android.com/reference/android/telephony/CellLocation "View this page in Java") 
| --- | --- |

```
abstract class CellLocation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.CellLocation](https://developer.android.com/reference/kotlin/android/telephony/CellLocation#) |

| Known Direct Subclasses [CdmaCellLocation](https://developer.android.com/reference/kotlin/android/telephony/cdma/CdmaCellLocation), [GsmCellLocation](https://developer.android.com/reference/kotlin/android/telephony/gsm/GsmCellLocation) |------------------------------------------------------------------------------------------------------------|-----------------------------------------------| | [CdmaCellLocation](https://developer.android.com/reference/kotlin/android/telephony/cdma/CdmaCellLocation) | Represents the cell location on a CDMA phone. | | [GsmCellLocation](https://developer.android.com/reference/kotlin/android/telephony/gsm/GsmCellLocation) | Represents the cell location on a GSM phone. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| **This class was deprecated in API level 31.**
|
| use [CellIdentity](https://developer.android.com/reference/kotlin/android/telephony/CellIdentity).

Abstract class that represents the location of the device. {@more}

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------|---|
| [CellLocation](https://developer.android.com/reference/kotlin/android/telephony/CellLocation#CellLocation())`()` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [CellLocation](https://developer.android.com/reference/kotlin/android/telephony/CellLocation#)! | [getEmpty](https://developer.android.com/reference/kotlin/android/telephony/CellLocation#getEmpty())`()` Return a new CellLocation object representing an unknown location, or null for unknown/none phone radio types. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestLocationUpdate](https://developer.android.com/reference/kotlin/android/telephony/CellLocation#requestLocationUpdate())`()` Request an updated CellLocation for callers targeting SDK 30 or older. |

## Public constructors

### CellLocation

```
CellLocation()
```

## Public methods

### getEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getEmpty(): CellLocation!
```

**Deprecated:** *Deprecated in Java.*

Return a new CellLocation object representing an unknown location, or null for unknown/none phone radio types. 

### requestLocationUpdate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun requestLocationUpdate(): Unit
```

**Deprecated:** *use [TelephonyManager.requestCellInfoUpdate](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#requestCellInfoUpdate(java.util.concurrent.Executor,%20android.telephony.TelephonyManager.CellInfoCallback)).*

Request an updated CellLocation for callers targeting SDK 30 or older. Whenever Android is aware of location changes, a callback will automatically be sent to all registrants of [PhoneStateListener.LISTEN_CELL_LOCATION](https://developer.android.com/reference/kotlin/android/telephony/PhoneStateListener#LISTEN_CELL_LOCATION:kotlin.Int). This API requests an additional location update for cases where power saving might cause location updates to be missed.

This method is a no-op for callers targeting SDK level 31 or greater.

This method is a no-op for callers that target SDK level 29 or 30 and lack [android.Manifest.permission#ACCESS_FINE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String).

This method is a no-op for callers that target SDK level 28 or below and lack [android.Manifest.permission#ACCESS_COARSE_LOCATION](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String).
