# ProcessedData

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProcessedData

Kotlin| [Java](../android/drm/ProcessedData.md) 
| --- | --- |

```
open class ProcessedData
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.drm.ProcessedData](../android/drm/ProcessedData.md) |

| **This class was deprecated in API level 30.**
|
| Please use [android.media.MediaDrm](../android/media/MediaDrm.md)

An entity class that wraps the result of a [processDrmInfo()](../android/drm/DrmManagerClient.md))transaction between a device and a DRM server. In a license acquisition scenario this class holds the rights information in binary form.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAccountId](../android/drm/ProcessedData.md))`()` Retrieves the account ID associated with this object. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getData](../android/drm/ProcessedData.md))`()` Retrieves the processed data. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSubscriptionId](../android/drm/ProcessedData.md))`()` Returns the subscription ID associated with this object. |
| --- | --- |

## Public methods

### getAccountId

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAccountId(): String!
```

**Deprecated:** *Deprecated in Java.*

Retrieves the account ID associated with this object.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The account ID of the user. |

### getData

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getData(): ByteArray!
```

**Deprecated:** *Deprecated in Java.*

Retrieves the processed data.

| Return ||
|------------------------------------------------------------------------------------------|------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | The rights data. |

### getSubscriptionId

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSubscriptionId(): String!
```

**Deprecated:** *Deprecated in Java.*

Returns the subscription ID associated with this object.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The subscription ID of the user. |
