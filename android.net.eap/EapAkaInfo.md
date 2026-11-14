# EapAkaInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EapAkaInfo

Kotlin | [Java](EapAkaInfo.md) 
| --- | --- |

```
class EapAkaInfo : EapInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.net.eap.EapInfo](EapInfo.md) ||
| | ↳ | [android.net.eap.EapAkaInfo](EapAkaInfo.md) |

EapAkaInfo represents data provided by the server during EAP AKA authentication

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/net/eap/EapAkaInfo.Builder.md) This class can be used to incrementally construct an [EapAkaInfo](EapAkaInfo.md). |

| Public methods ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getReauthId](EapAkaInfo.md))`()` Retrieves re-authentication ID from server for next use. |

| Inherited functions ||
|---|---|
| From class [EapInfo](EapInfo.md) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEapMethodType](EapInfo.md))`()` Retrieves EAP method type <br /> | ||

## Public methods

### getReauthId

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getReauthId(): ByteArray?
```

Retrieves re-authentication ID from server for next use.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | re-authentication ID This value may be `null`. |

**See Also**
