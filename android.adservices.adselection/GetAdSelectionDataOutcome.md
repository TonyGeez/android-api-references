# GetAdSelectionDataOutcome

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions)

# GetAdSelectionDataOutcome

Kotlin| [Java](https://developer.android.com/reference/android/adservices/adselection/GetAdSelectionDataOutcome "View this page in Java") 
| --- | --- |

```
class GetAdSelectionDataOutcome
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adselection.GetAdSelectionDataOutcome](https://developer.android.com/reference/kotlin/android/adservices/adselection/GetAdSelectionDataOutcome#) |

Represents ad selection data collected from device for ad selection.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getAdSelectionData](https://developer.android.com/reference/kotlin/android/adservices/adselection/GetAdSelectionDataOutcome#getAdSelectionData())`()` Returns the adSelectionData that is collected from device. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAdSelectionDataId](https://developer.android.com/reference/kotlin/android/adservices/adselection/GetAdSelectionDataOutcome#getAdSelectionDataId())`()` Returns the id that uniquely identifies this GetAdSelectionData payload. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAdSelectionId](https://developer.android.com/reference/kotlin/android/adservices/adselection/GetAdSelectionDataOutcome#getAdSelectionId())`()` Returns the adSelectionId that identifies the AdSelection. |
| --- | --- |

## Public methods

### getAdSelectionData

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
fun getAdSelectionData(): ByteArray?
```

Returns the adSelectionData that is collected from device.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | This value may be`null`. |

### getAdSelectionDataId

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 12](https://developer.android.com/sdkExtensions) 

```
fun getAdSelectionDataId(): Long
```

Returns the id that uniquely identifies this GetAdSelectionData payload. 

### getAdSelectionId

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAdSelectionId(): Long
```

**Deprecated:** *Use the [getAdSelectionDataId()](https://developer.android.com/reference/kotlin/android/adservices/adselection/GetAdSelectionDataOutcome#getAdSelectionDataId())instead.*

Returns the adSelectionId that identifies the AdSelection.
