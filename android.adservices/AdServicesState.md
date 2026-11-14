# AdServicesState

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# AdServicesState

Kotlin| [Java](../android/adservices/AdServicesState.md) 
| --- | --- |

```
open class AdServicesState
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.AdServicesState](../android/adservices/AdServicesState.md) |

This class specifies the state of the APIs exposed by AdServicesApi apk.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAdServicesStateEnabled](../android/adservices/AdServicesState.md))`()` Returns current state of the`AdServicesApi`. |

## Public methods

### isAdServicesStateEnabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
open static fun isAdServicesStateEnabled(): Boolean
```

Returns current state of the`AdServicesApi`. The state of AdServicesApi may change only upon reboot, so this value can be cached, but not persisted, i.e., the value should be rechecked after a reboot.
