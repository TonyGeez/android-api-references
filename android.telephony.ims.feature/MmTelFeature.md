# MmTelFeature

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MmTelFeature

Kotlin| [Java](MmTelFeature.md) 
| --- | --- |

```
open class MmTelFeature
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.ims.feature.MmTelFeature](MmTelFeature.md) |

Base implementation for Voice and SMS (IR-92) and Video (IR-94) IMS support. Any class wishing to use MmTelFeature should extend this class and implement all methods that the service supports.

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [MmTelCapabilities](../android/telephony/ims/feature/MmTelFeature.MmTelCapabilities.md) Contains the capabilities defined and supported by a MmTelFeature in the form of a Bitmask. |
