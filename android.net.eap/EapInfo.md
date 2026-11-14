# EapInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EapInfo

Kotlin| [Java](EapInfo.md) 
| --- | --- |

```
abstract class EapInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.eap.EapInfo](EapInfo.md) |

| Known Direct Subclasses [EapAkaInfo](EapAkaInfo.md) |-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------| | [EapAkaInfo](EapAkaInfo.md) | EapAkaInfo represents data provided by the server during EAP AKA authentication | |
| --- | --- | --- | --- | --- | --- | --- |

EapInfo represents data provided by the server during EAP authentication

## Summary

| Public methods ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEapMethodType](EapInfo.md))`()` Retrieves EAP method type |

## Public methods

### getEapMethodType

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEapMethodType(): Int
```

Retrieves EAP method type

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | EAP method type Value is [android.net.eap.EapSessionConfig.EapMethodConfig#EAP_TYPE_SIM](../android/net/eap/EapSessionConfig.EapMethodConfig.md), [android.net.eap.EapSessionConfig.EapMethodConfig#EAP_TYPE_TTLS](../android/net/eap/EapSessionConfig.EapMethodConfig.md), [android.net.eap.EapSessionConfig.EapMethodConfig#EAP_TYPE_AKA](../android/net/eap/EapSessionConfig.EapMethodConfig.md), [android.net.eap.EapSessionConfig.EapMethodConfig#EAP_TYPE_MSCHAP_V2](../android/net/eap/EapSessionConfig.EapMethodConfig.md), or [android.net.eap.EapSessionConfig.EapMethodConfig#EAP_TYPE_AKA_PRIME](../android/net/eap/EapSessionConfig.EapMethodConfig.md) |
