# ImsRegistrationImplBase

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ImsRegistrationImplBase

Kotlin| [Java](../android/telephony/ims/stub/ImsRegistrationImplBase.md) 
| --- | --- |

```
open class ImsRegistrationImplBase
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.ims.stub.ImsRegistrationImplBase](../android/telephony/ims/stub/ImsRegistrationImplBase.md) |

Controls IMS registration for this ImsService and notifies the framework when the IMS registration for this ImsService has changed status.

Note: There is no guarantee on the thread that the calls from the framework will be called on. It is the implementors responsibility to handle moving the calls to a working thread if required.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REGISTRATION_TECH_3G](../android/telephony/ims/stub/ImsRegistrationImplBase.md) This ImsService is registered to IMS via 3G. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REGISTRATION_TECH_CROSS_SIM](../android/telephony/ims/stub/ImsRegistrationImplBase.md) This ImsService is registered to IMS via internet over second subscription. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REGISTRATION_TECH_IWLAN](../android/telephony/ims/stub/ImsRegistrationImplBase.md) This ImsService is registered to IMS via IWLAN. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REGISTRATION_TECH_LTE](../android/telephony/ims/stub/ImsRegistrationImplBase.md) This ImsService is registered to IMS via LTE. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REGISTRATION_TECH_NONE](../android/telephony/ims/stub/ImsRegistrationImplBase.md) No registration technology specified, used when we are not registered. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REGISTRATION_TECH_NR](../android/telephony/ims/stub/ImsRegistrationImplBase.md) This ImsService is registered to IMS via NR. |
| --- | --- |

## Constants

### REGISTRATION_TECH_3G

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REGISTRATION_TECH_3G: Int
```

This ImsService is registered to IMS via 3G. 

 Value: 4

### REGISTRATION_TECH_CROSS_SIM

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REGISTRATION_TECH_CROSS_SIM: Int
```

This ImsService is registered to IMS via internet over second subscription. 

 Value: 2

### REGISTRATION_TECH_IWLAN

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REGISTRATION_TECH_IWLAN: Int
```

This ImsService is registered to IMS via IWLAN. 

 Value: 1

### REGISTRATION_TECH_LTE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REGISTRATION_TECH_LTE: Int
```

This ImsService is registered to IMS via LTE. 

 Value: 0

### REGISTRATION_TECH_NONE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REGISTRATION_TECH_NONE: Int
```

No registration technology specified, used when we are not registered. 

 Value: -1

### REGISTRATION_TECH_NR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REGISTRATION_TECH_NR: Int
```

This ImsService is registered to IMS via NR. 

 Value: 3
