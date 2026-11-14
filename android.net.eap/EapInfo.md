# EapInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EapInfo

Kotlin| [Java](https://developer.android.com/reference/android/net/eap/EapInfo "View this page in Java") 

```
abstract class EapInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.eap.EapInfo](https://developer.android.com/reference/kotlin/android/net/eap/EapInfo#) |

| Known Direct Subclasses [EapAkaInfo](https://developer.android.com/reference/kotlin/android/net/eap/EapAkaInfo) |-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------| | [EapAkaInfo](https://developer.android.com/reference/kotlin/android/net/eap/EapAkaInfo) | EapAkaInfo represents data provided by the server during EAP AKA authentication | |

EapInfo represents data provided by the server during EAP authentication

## Summary

| Public methods ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEapMethodType](https://developer.android.com/reference/kotlin/android/net/eap/EapInfo#getEapMethodType())`()` Retrieves EAP method type |

## Public methods

### getEapMethodType

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEapMethodType(): Int
```

Retrieves EAP method type

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | EAP method type Value is [android.net.eap.EapSessionConfig.EapMethodConfig#EAP_TYPE_SIM](https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig.EapMethodConfig#EAP_TYPE_SIM:kotlin.Int), [android.net.eap.EapSessionConfig.EapMethodConfig#EAP_TYPE_TTLS](https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig.EapMethodConfig#EAP_TYPE_TTLS:kotlin.Int), [android.net.eap.EapSessionConfig.EapMethodConfig#EAP_TYPE_AKA](https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig.EapMethodConfig#EAP_TYPE_AKA:kotlin.Int), [android.net.eap.EapSessionConfig.EapMethodConfig#EAP_TYPE_MSCHAP_V2](https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig.EapMethodConfig#EAP_TYPE_MSCHAP_V2:kotlin.Int), or [android.net.eap.EapSessionConfig.EapMethodConfig#EAP_TYPE_AKA_PRIME](https://developer.android.com/reference/kotlin/android/net/eap/EapSessionConfig.EapMethodConfig#EAP_TYPE_AKA_PRIME:kotlin.Int) |
