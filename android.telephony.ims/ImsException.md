# ImsException

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ImsException

Kotlin| [Java](ImsException.md) 
| --- | --- |

```
class ImsException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||
| | | ↳ | [android.telephony.ims.ImsException](ImsException.md) |
| --- | --- | --- | --- |

This class defines an IMS-related exception that has been thrown while interacting with a device or carrier provided ImsService implementation.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CODE_ERROR_INVALID_SUBSCRIPTION](ImsException.md) The subscription ID associated with this operation is invalid or not active. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CODE_ERROR_SERVICE_UNAVAILABLE](ImsException.md) The operation has failed because there is no remote process available to service it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CODE_ERROR_UNSPECIFIED](ImsException.md) The operation has failed due to an unknown or unspecified error. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CODE_ERROR_UNSUPPORTED_OPERATION](ImsException.md) This device or carrier configuration does not support this feature for this subscription. |

| Public methods ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCode](ImsException.md))`()` <br /> |

## Constants

### CODE_ERROR_INVALID_SUBSCRIPTION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CODE_ERROR_INVALID_SUBSCRIPTION: Int
```

The subscription ID associated with this operation is invalid or not active.

This is a configuration error and there should be no retry. The subscription used for this operation is either invalid or has become inactive. The active subscriptions can be queried with [SubscriptionManager.getActiveSubscriptionInfoList()](../android.telephony/SubscriptionManager.md)). 

 Value: 3

### CODE_ERROR_SERVICE_UNAVAILABLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CODE_ERROR_SERVICE_UNAVAILABLE: Int
```

The operation has failed because there is no remote process available to service it. This may be due to a process crash or other illegal state.

This is a temporary error and the operation may be retried until the connection to the remote process is restored. 

 Value: 1

### CODE_ERROR_UNSPECIFIED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CODE_ERROR_UNSPECIFIED: Int
```

The operation has failed due to an unknown or unspecified error. 

 Value: 0

### CODE_ERROR_UNSUPPORTED_OPERATION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CODE_ERROR_UNSUPPORTED_OPERATION: Int
```

This device or carrier configuration does not support this feature for this subscription.

This is a permanent configuration error and there should be no retry until the subscription changes if this operation is denied due to a carrier configuration. If this is due to a device configuration, the feature [PackageManager.FEATURE_TELEPHONY_IMS](../android.content.pm/PackageManager.md) is not available or the device has no ImsService implementation to service this request. 

 Value: 2

## Public methods

### getCode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the IMS Error code that is associated with this [ImsException](ImsException.md). Value is [android.telephony.ims.ImsException#CODE_ERROR_UNSPECIFIED](ImsException.md), [android.telephony.ims.ImsException#CODE_ERROR_SERVICE_UNAVAILABLE](ImsException.md), [android.telephony.ims.ImsException#CODE_ERROR_UNSUPPORTED_OPERATION](ImsException.md), or [android.telephony.ims.ImsException#CODE_ERROR_INVALID_SUBSCRIPTION](ImsException.md) |
