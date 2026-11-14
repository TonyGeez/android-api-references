# MmTelFeature

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MmTelFeature

Kotlin| [Java](https://developer.android.com/reference/android/telephony/ims/feature/MmTelFeature "View this page in Java") 

```
open class MmTelFeature
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telephony.ims.feature.MmTelFeature](https://developer.android.com/reference/kotlin/android/telephony/ims/feature/MmTelFeature#) |

Base implementation for Voice and SMS (IR-92) and Video (IR-94) IMS support. Any class wishing to use MmTelFeature should extend this class and implement all methods that the service supports.

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [MmTelCapabilities](https://developer.android.com/reference/kotlin/android/telephony/ims/feature/MmTelFeature.MmTelCapabilities) Contains the capabilities defined and supported by a MmTelFeature in the form of a Bitmask. |
