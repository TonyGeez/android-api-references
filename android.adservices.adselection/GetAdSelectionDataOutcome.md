# GetAdSelectionDataOutcome

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions)

# GetAdSelectionDataOutcome

Kotlin| [Java](../android/adservices/adselection/GetAdSelectionDataOutcome.md) 
| --- | --- |

```
class GetAdSelectionDataOutcome
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adselection.GetAdSelectionDataOutcome](../android/adservices/adselection/GetAdSelectionDataOutcome.md) |

Represents ad selection data collected from device for ad selection.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getAdSelectionData](../android/adservices/adselection/GetAdSelectionDataOutcome.md))`()` Returns the adSelectionData that is collected from device. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAdSelectionDataId](../android/adservices/adselection/GetAdSelectionDataOutcome.md))`()` Returns the id that uniquely identifies this GetAdSelectionData payload. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAdSelectionId](../android/adservices/adselection/GetAdSelectionDataOutcome.md))`()` Returns the adSelectionId that identifies the AdSelection. |
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

**Deprecated:** *Use the [getAdSelectionDataId()](../android/adservices/adselection/GetAdSelectionDataOutcome.md))instead.*

Returns the adSelectionId that identifies the AdSelection.
