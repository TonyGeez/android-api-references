# PolicyUpdateResult

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PolicyUpdateResult

Kotlin | [Java](../android/app/admin/PolicyUpdateResult.md) 
| --- | --- |

```
class PolicyUpdateResult
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.admin.PolicyUpdateResult](../android/app/admin/PolicyUpdateResult.md) |

Class containing the reason for the policy (set from [DevicePolicyManager](../android/app/admin/DevicePolicyManager.md)) update (e.g. success, failure reasons, etc.). This is passed in to [PolicyUpdateReceiver.onPolicySetResult](../android/app/admin/PolicyUpdateReceiver.md))) and [PolicyUpdateReceiver.onPolicyChanged](../android/app/admin/PolicyUpdateReceiver.md))).

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_FAILURE_CONFLICTING_ADMIN_POLICY](../android/app/admin/PolicyUpdateResult.md) Result code to indicate that the policy has not been enforced or has changed because another admin has set a conflicting policy on the device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_FAILURE_HARDWARE_LIMITATION](../android/app/admin/PolicyUpdateResult.md) Result code to indicate that the policy set by the admin has not been enforced because of a permanent hardware limitation/issue. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_FAILURE_STORAGE_LIMIT_REACHED](../android/app/admin/PolicyUpdateResult.md) Result code to indicate that the policy set by the admin has not been enforced because the local storage has reached its max limit. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_FAILURE_UNKNOWN](../android/app/admin/PolicyUpdateResult.md) Result code to indicate that the policy has not been enforced or has changed for an unknown reason. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_POLICY_CLEARED](../android/app/admin/PolicyUpdateResult.md) Result code to indicate that the policy set by the admin has been successfully cleared, admins will no longer receive policy updates for this policy after this point. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_POLICY_SET](../android/app/admin/PolicyUpdateResult.md) Result code to indicate that the policy has been changed to the desired value set by the admin. |
| --- | --- |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PolicyUpdateResult](../android/app/admin/PolicyUpdateResult.md))`(`resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor for `PolicyUpdateResult` that takes in a result code describing why the policy has changed. |

| Public methods ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResultCode](../android/app/admin/PolicyUpdateResult.md))`()` Returns result code describing why the policy has changed. |

## Constants

### RESULT_FAILURE_CONFLICTING_ADMIN_POLICY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULT_FAILURE_CONFLICTING_ADMIN_POLICY: Int
```

Result code to indicate that the policy has not been enforced or has changed because another admin has set a conflicting policy on the device.

The system will automatically try to enforce the policy when it can without additional calls from the admin. 

 Value: 1

### RESULT_FAILURE_HARDWARE_LIMITATION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULT_FAILURE_HARDWARE_LIMITATION: Int
```

Result code to indicate that the policy set by the admin has not been enforced because of a permanent hardware limitation/issue.

The system will NOT try to automatically store and enforce this policy again. 

 Value: 4

### RESULT_FAILURE_STORAGE_LIMIT_REACHED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULT_FAILURE_STORAGE_LIMIT_REACHED: Int
```

Result code to indicate that the policy set by the admin has not been enforced because the local storage has reached its max limit.

The system will NOT try to automatically store and enforce this policy again. 

 Value: 3

### RESULT_FAILURE_UNKNOWN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULT_FAILURE_UNKNOWN: Int
```

Result code to indicate that the policy has not been enforced or has changed for an unknown reason. 

 Value: -1

### RESULT_POLICY_CLEARED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULT_POLICY_CLEARED: Int
```

Result code to indicate that the policy set by the admin has been successfully cleared, admins will no longer receive policy updates for this policy after this point.

Note that the policy can still be enforced by some other admin. 

 Value: 2

### RESULT_POLICY_SET

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULT_POLICY_SET: Int
```

Result code to indicate that the policy has been changed to the desired value set by the admin. 

 Value: 0

## Public constructors

### PolicyUpdateResult

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PolicyUpdateResult(resultCode: Int)
```

Constructor for `PolicyUpdateResult` that takes in a result code describing why the policy has changed.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resultCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Describes why the policy has changed. Value is [android.app.admin.PolicyUpdateResult#RESULT_FAILURE_UNKNOWN](../android/app/admin/PolicyUpdateResult.md), [android.app.admin.PolicyUpdateResult#RESULT_POLICY_SET](../android/app/admin/PolicyUpdateResult.md), [android.app.admin.PolicyUpdateResult#RESULT_FAILURE_CONFLICTING_ADMIN_POLICY](../android/app/admin/PolicyUpdateResult.md), [android.app.admin.PolicyUpdateResult#RESULT_POLICY_CLEARED](../android/app/admin/PolicyUpdateResult.md), [android.app.admin.PolicyUpdateResult#RESULT_FAILURE_STORAGE_LIMIT_REACHED](../android/app/admin/PolicyUpdateResult.md), or [android.app.admin.PolicyUpdateResult#RESULT_FAILURE_HARDWARE_LIMITATION](../android/app/admin/PolicyUpdateResult.md) |

## Public methods

### getResultCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getResultCode(): Int
```

Returns result code describing why the policy has changed.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.app.admin.PolicyUpdateResult#RESULT_FAILURE_UNKNOWN](../android/app/admin/PolicyUpdateResult.md), [android.app.admin.PolicyUpdateResult#RESULT_POLICY_SET](../android/app/admin/PolicyUpdateResult.md), [android.app.admin.PolicyUpdateResult#RESULT_FAILURE_CONFLICTING_ADMIN_POLICY](../android/app/admin/PolicyUpdateResult.md), [android.app.admin.PolicyUpdateResult#RESULT_POLICY_CLEARED](../android/app/admin/PolicyUpdateResult.md), [android.app.admin.PolicyUpdateResult#RESULT_FAILURE_STORAGE_LIMIT_REACHED](../android/app/admin/PolicyUpdateResult.md), or [android.app.admin.PolicyUpdateResult#RESULT_FAILURE_HARDWARE_LIMITATION](../android/app/admin/PolicyUpdateResult.md) |
