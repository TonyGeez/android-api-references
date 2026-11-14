# AdServicesState

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# AdServicesState

Kotlin| [Java](https://developer.android.com/reference/android/adservices/AdServicesState "View this page in Java") 
| --- | --- |

```
open class AdServicesState
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.AdServicesState](https://developer.android.com/reference/kotlin/android/adservices/AdServicesState#) |

This class specifies the state of the APIs exposed by AdServicesApi apk.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAdServicesStateEnabled](https://developer.android.com/reference/kotlin/android/adservices/AdServicesState#isAdServicesStateEnabled())`()` Returns current state of the`AdServicesApi`. |

## Public methods

### isAdServicesStateEnabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
open static fun isAdServicesStateEnabled(): Boolean
```

Returns current state of the`AdServicesApi`. The state of AdServicesApi may change only upon reboot, so this value can be cached, but not persisted, i.e., the value should be rechecked after a reboot.
