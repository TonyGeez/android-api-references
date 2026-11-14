# CellLocation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CellLocation

Kotlin| [Java](../android/telephony/CellLocation.md) 
| --- | --- |

```
abstract class CellLocation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.CellLocation](../android/telephony/CellLocation.md) |

| Known Direct Subclasses [CdmaCellLocation](../android/telephony/cdma/CdmaCellLocation.md), [GsmCellLocation](../android/telephony/gsm/GsmCellLocation.md) |------------------------------------------------------------------------------------------------------------|-----------------------------------------------| | [CdmaCellLocation](../android/telephony/cdma/CdmaCellLocation.md) | Represents the cell location on a CDMA phone. | | [GsmCellLocation](../android/telephony/gsm/GsmCellLocation.md) | Represents the cell location on a GSM phone. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| **This class was deprecated in API level 31.**
|
| use [CellIdentity](../android/telephony/CellIdentity.md).

Abstract class that represents the location of the device. {@more}

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------|---|
| [CellLocation](../android/telephony/CellLocation.md))`()` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [CellLocation](../android/telephony/CellLocation.md)! | [getEmpty](../android/telephony/CellLocation.md))`()` Return a new CellLocation object representing an unknown location, or null for unknown/none phone radio types. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestLocationUpdate](../android/telephony/CellLocation.md))`()` Request an updated CellLocation for callers targeting SDK 30 or older. |

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

**Deprecated:** *use [TelephonyManager.requestCellInfoUpdate](../android/telephony/TelephonyManager.md)).*

Request an updated CellLocation for callers targeting SDK 30 or older. Whenever Android is aware of location changes, a callback will automatically be sent to all registrants of [PhoneStateListener.LISTEN_CELL_LOCATION](../android/telephony/PhoneStateListener.md). This API requests an additional location update for cases where power saving might cause location updates to be missed.

This method is a no-op for callers targeting SDK level 31 or greater.

This method is a no-op for callers that target SDK level 29 or 30 and lack [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md).

This method is a no-op for callers that target SDK level 28 or below and lack [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md).
