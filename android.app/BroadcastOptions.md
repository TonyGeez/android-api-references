# BroadcastOptions

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BroadcastOptions

Kotlin| [Java](https://developer.android.com/reference/android/app/BroadcastOptions "View this page in Java") 

```
open class BroadcastOptions
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.BroadcastOptions](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#) |

Helper class for building an options Bundle that can be used with [Context.sendBroadcast(Intent)](https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent))and related methods.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEFERRAL_POLICY_DEFAULT](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#DEFERRAL_POLICY_DEFAULT:kotlin.Int) Deferral policy that indicates no desire has been expressed, and that the system should use a reasonable default behavior. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEFERRAL_POLICY_NONE](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#DEFERRAL_POLICY_NONE:kotlin.Int) Deferral policy that indicates a strong desire that no receiver of this broadcast should be deferred. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEFERRAL_POLICY_UNTIL_ACTIVE](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#DEFERRAL_POLICY_UNTIL_ACTIVE:kotlin.Int) Deferral policy that indicates a strong desire that each receiver of this broadcast should be deferred until that receiver's process is in an active (non-cached) state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DELIVERY_GROUP_POLICY_ALL](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#DELIVERY_GROUP_POLICY_ALL:kotlin.Int) Delivery group policy that indicates that all the broadcasts in the delivery group need to be delivered as is. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DELIVERY_GROUP_POLICY_MOST_RECENT](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#DELIVERY_GROUP_POLICY_MOST_RECENT:kotlin.Int) Delivery group policy that indicates that only the most recent broadcast in the delivery group need to be delivered and the rest can be dropped. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearDeferralPolicy](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#clearDeferralPolicy())`()` Clears any deferral policy for this broadcast that specifies how this broadcast can be deferred for delivery at some future point. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearDeliveryGroupMatchingKey](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#clearDeliveryGroupMatchingKey())`()` Clears the namespace and key that was previously set using [setDeliveryGroupMatchingKey(java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#setDeliveryGroupMatchingKey(kotlin.String,%20kotlin.String)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearDeliveryGroupPolicy](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#clearDeliveryGroupPolicy())`()` Clears any previously set delivery group policies using [setDeliveryGroupMatchingKey(java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#setDeliveryGroupMatchingKey(kotlin.String,%20kotlin.String))and resets the delivery group policy to the default value ([DELIVERY_GROUP_POLICY_ALL](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#DELIVERY_GROUP_POLICY_ALL:kotlin.Int)). |
| openstatic [BroadcastOptions](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#) | [fromBundle](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#fromBundle(android.os.Bundle))`(`options:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)`)` Returns a [BroadcastOptions](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#) parsed from the given [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#), typically generated from [toBundle()](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#toBundle()). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDeferralPolicy](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#getDeferralPolicy())`()` Gets deferral policy for this broadcast that specifies how this broadcast can be deferred for delivery at some future point. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getDeliveryGroupMatchingKey](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#getDeliveryGroupMatchingKey())`()` Return the namespace and key that is used to identify the delivery group that this broadcast belongs to. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDeliveryGroupPolicy](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#getDeliveryGroupPolicy())`()` Get the delivery group policy for this broadcast that specifies how multiple broadcasts belonging to the same delivery group has to be handled. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isShareIdentityEnabled](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#isShareIdentityEnabled())`()` Returns whether the broadcasting app has opted-in to sharing its identity with the receiver. |
| openstatic [BroadcastOptions](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#) | [makeBasic](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#makeBasic())`()` Creates a basic [BroadcastOptions](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#) with no options initially set. |
| open [BroadcastOptions](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#) | [setDeferralPolicy](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#setDeferralPolicy(kotlin.Int))`(`deferralPolicy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets deferral policy for this broadcast that specifies how this broadcast can be deferred for delivery at some future point. |
| open [BroadcastOptions](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#) | [setDeliveryGroupMatchingKey](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#setDeliveryGroupMatchingKey(kotlin.String,%20kotlin.String))`(`namespace:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Set namespace and key to identify the delivery group that this broadcast belongs to. |
| open [BroadcastOptions](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#) | [setDeliveryGroupPolicy](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#setDeliveryGroupPolicy(kotlin.Int))`(`policy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set delivery group policy for this broadcast to specify how multiple broadcasts belonging to the same delivery group has to be handled. |
| open [BroadcastOptions](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#) | [setShareIdentityEnabled](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#setShareIdentityEnabled(kotlin.Boolean))`(`shareIdentityEnabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the identity of the broadcasting app should be shared with all receivers that will receive this broadcast. |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [toBundle](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#toBundle())`()` Returns the created options as a Bundle, which can be passed to [Context.sendBroadcast(Intent)](https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent))and related methods. |

## Constants

### DEFERRAL_POLICY_DEFAULT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFERRAL_POLICY_DEFAULT: Int
```

Deferral policy that indicates no desire has been expressed, and that the system should use a reasonable default behavior. 

 Value: 0

### DEFERRAL_POLICY_NONE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFERRAL_POLICY_NONE: Int
```

Deferral policy that indicates a strong desire that no receiver of this broadcast should be deferred. 

 Value: 1

### DEFERRAL_POLICY_UNTIL_ACTIVE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFERRAL_POLICY_UNTIL_ACTIVE: Int
```

Deferral policy that indicates a strong desire that each receiver of this broadcast should be deferred until that receiver's process is in an active (non-cached) state. Whether an app's process state is considered active is independent of its standby bucket.

This policy only applies to runtime registered receivers of a broadcast, and does not apply to ordered broadcasts, alarm broadcasts, interactive broadcasts, or manifest broadcasts.

This policy means that a runtime registered receiver will not typically execute until that receiver's process is brought to an active state by some other action, such as a job, alarm, or service binding. As a result, the receiver may be delayed indefinitely.

When this policy is set on an unordered broadcast with a completion callback, the completion callback will run once all eligible processes have finished receiving the broadcast. Processes in inactive process state are not considered eligible and may not receive the broadcast prior to the completion callback. 

 Value: 2

### DELIVERY_GROUP_POLICY_ALL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DELIVERY_GROUP_POLICY_ALL: Int
```

Delivery group policy that indicates that all the broadcasts in the delivery group need to be delivered as is. 

 Value: 0

### DELIVERY_GROUP_POLICY_MOST_RECENT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DELIVERY_GROUP_POLICY_MOST_RECENT: Int
```

Delivery group policy that indicates that only the most recent broadcast in the delivery group need to be delivered and the rest can be dropped. 

 Value: 1

## Public methods

### clearDeferralPolicy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearDeferralPolicy(): Unit
```

Clears any deferral policy for this broadcast that specifies how this broadcast can be deferred for delivery at some future point. 

### clearDeliveryGroupMatchingKey

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearDeliveryGroupMatchingKey(): Unit
```

Clears the namespace and key that was previously set using [setDeliveryGroupMatchingKey(java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#setDeliveryGroupMatchingKey(kotlin.String,%20kotlin.String)). 

### clearDeliveryGroupPolicy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearDeliveryGroupPolicy(): Unit
```

Clears any previously set delivery group policies using [setDeliveryGroupMatchingKey(java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#setDeliveryGroupMatchingKey(kotlin.String,%20kotlin.String))and resets the delivery group policy to the default value ([DELIVERY_GROUP_POLICY_ALL](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#DELIVERY_GROUP_POLICY_ALL:kotlin.Int)). 

### fromBundle

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun fromBundle(options: Bundle): BroadcastOptions
```

Returns a [BroadcastOptions](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#) parsed from the given [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#), typically generated from [toBundle()](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#toBundle()).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------|
| `options` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#):This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------|
| [BroadcastOptions](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#) | This value cannot be`null`. |

### getDeferralPolicy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDeferralPolicy(): Int
```

Gets deferral policy for this broadcast that specifies how this broadcast can be deferred for delivery at some future point.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.app.BroadcastOptions#DEFERRAL_POLICY_DEFAULT](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#DEFERRAL_POLICY_DEFAULT:kotlin.Int), [android.app.BroadcastOptions#DEFERRAL_POLICY_NONE](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#DEFERRAL_POLICY_NONE:kotlin.Int), or [android.app.BroadcastOptions#DEFERRAL_POLICY_UNTIL_ACTIVE](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#DEFERRAL_POLICY_UNTIL_ACTIVE:kotlin.Int) |

### getDeliveryGroupMatchingKey

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDeliveryGroupMatchingKey(): String?
```

Return the namespace and key that is used to identify the delivery group that this broadcast belongs to.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the delivery group namespace and key that was previously set using [setDeliveryGroupMatchingKey(java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#setDeliveryGroupMatchingKey(kotlin.String,%20kotlin.String)), concatenated with a`:`. This value may be`null`. |

### getDeliveryGroupPolicy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDeliveryGroupPolicy(): Int
```

Get the delivery group policy for this broadcast that specifies how multiple broadcasts belonging to the same delivery group has to be handled.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.app.BroadcastOptions#DELIVERY_GROUP_POLICY_ALL](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#DELIVERY_GROUP_POLICY_ALL:kotlin.Int), [android.app.BroadcastOptions#DELIVERY_GROUP_POLICY_MOST_RECENT](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#DELIVERY_GROUP_POLICY_MOST_RECENT:kotlin.Int), or android.app.BroadcastOptions.DELIVERY_GROUP_POLICY_MERGED |

### isShareIdentityEnabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isShareIdentityEnabled(): Boolean
```

Returns whether the broadcasting app has opted-in to sharing its identity with the receiver.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the broadcasting app has opted in to sharing its identity |

**See Also**

- [#setShareIdentityEnabled(boolean)](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#setShareIdentityEnabled(kotlin.Boolean))
- [android.content.BroadcastReceiver#getSentFromUid()](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#getSentFromUid())
- [android.content.BroadcastReceiver#getSentFromPackage()](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#getSentFromPackage()) 

### makeBasic

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun makeBasic(): BroadcastOptions
```

Creates a basic [BroadcastOptions](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#) with no options initially set.

| Return ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [BroadcastOptions](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#) | an instance of`BroadcastOptions`against which options can be set This value cannot be`null`. |

### setDeferralPolicy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDeferralPolicy(deferralPolicy: Int): BroadcastOptions
```

Sets deferral policy for this broadcast that specifies how this broadcast can be deferred for delivery at some future point.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deferralPolicy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.app.BroadcastOptions#DEFERRAL_POLICY_DEFAULT](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#DEFERRAL_POLICY_DEFAULT:kotlin.Int), [android.app.BroadcastOptions#DEFERRAL_POLICY_NONE](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#DEFERRAL_POLICY_NONE:kotlin.Int), or [android.app.BroadcastOptions#DEFERRAL_POLICY_UNTIL_ACTIVE](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#DEFERRAL_POLICY_UNTIL_ACTIVE:kotlin.Int) |

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------|
| [BroadcastOptions](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#) | This value cannot be`null`. |

### setDeliveryGroupMatchingKey

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDeliveryGroupMatchingKey(
    namespace: String, 
    key: String
): BroadcastOptions
```

Set namespace and key to identify the delivery group that this broadcast belongs to.

If`namespace`and`key`are specified, then another broadcast will be considered to be in the same delivery group as this iff it has the same`namespace`and`key`.

If not matching key using this API then by default [Intent.filterEquals(Intent)](https://developer.android.com/reference/kotlin/android/content/Intent.html#filterEquals(android.content.Intent))will be used to identify the delivery group.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------|
| `namespace` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------|
| [BroadcastOptions](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#) | This value cannot be`null`. |

### setDeliveryGroupPolicy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDeliveryGroupPolicy(policy: Int): BroadcastOptions
```

Set delivery group policy for this broadcast to specify how multiple broadcasts belonging to the same delivery group has to be handled.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `policy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.app.BroadcastOptions#DELIVERY_GROUP_POLICY_ALL](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#DELIVERY_GROUP_POLICY_ALL:kotlin.Int), [android.app.BroadcastOptions#DELIVERY_GROUP_POLICY_MOST_RECENT](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#DELIVERY_GROUP_POLICY_MOST_RECENT:kotlin.Int), or android.app.BroadcastOptions.DELIVERY_GROUP_POLICY_MERGED |

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------|
| [BroadcastOptions](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#) | This value cannot be`null`. |

### setShareIdentityEnabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setShareIdentityEnabled(shareIdentityEnabled: Boolean): BroadcastOptions
```

Sets whether the identity of the broadcasting app should be shared with all receivers that will receive this broadcast.

Use this option when broadcasting to a receiver that needs to know the identity of the broadcaster; with this set to`true`, the receiver will have access to the broadcasting app's package name and uid.

Defaults to`false`if not set.

| Parameters ||
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `shareIdentityEnabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the broadcasting app's identity should be shared with the receiver |

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [BroadcastOptions](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#) | `this` [BroadcastOptions](https://developer.android.com/reference/kotlin/android/app/BroadcastOptions#) instance This value cannot be`null`. |

**See Also**

- [android.content.BroadcastReceiver#getSentFromUid()](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#getSentFromUid())
- [android.content.BroadcastReceiver#getSentFromPackage()](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#getSentFromPackage()) 

### toBundle

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toBundle(): Bundle
```

Returns the created options as a Bundle, which can be passed to [Context.sendBroadcast(Intent)](https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent))and related methods. Note that the returned Bundle is still owned by the BroadcastOptions object; you must not modify it, but can supply it to the sendBroadcast methods that take an options Bundle.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the broadcast option values are inconsistent. For example, if the delivery group policy is specified as "MERGED" but no extras merger is supplied. |
