# EapAkaInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EapAkaInfo

Kotlin | [Java](https://developer.android.com/reference/android/net/eap/EapAkaInfo "View this page in Java") 
| --- | --- |

```
class EapAkaInfo : EapInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.net.eap.EapInfo](https://developer.android.com/reference/kotlin/android/net/eap/EapInfo) ||
| | ↳ | [android.net.eap.EapAkaInfo](https://developer.android.com/reference/kotlin/android/net/eap/EapAkaInfo#) |

EapAkaInfo represents data provided by the server during EAP AKA authentication

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/net/eap/EapAkaInfo.Builder) This class can be used to incrementally construct an [EapAkaInfo](https://developer.android.com/reference/kotlin/android/net/eap/EapAkaInfo#). |

| Public methods ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getReauthId](https://developer.android.com/reference/kotlin/android/net/eap/EapAkaInfo#getReauthId())`()` Retrieves re-authentication ID from server for next use. |

| Inherited functions ||
|---|---|
| From class [EapInfo](https://developer.android.com/reference/kotlin/android/net/eap/EapInfo) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEapMethodType](https://developer.android.com/reference/kotlin/android/net/eap/EapInfo#getEapMethodType())`()` Retrieves EAP method type <br /> | ||

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
