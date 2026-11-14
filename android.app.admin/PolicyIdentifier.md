Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PolicyIdentifier

```
open class PolicyIdentifier<T : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.admin.PolicyIdentifier](https://developer.android.com/reference/kotlin/android/app/admin/PolicyIdentifier#) |

Represents a type safe identifier for a policy. Use it as a key for `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setPolicy(android.app.admin.PolicyIdentifier,%20kotlin.Int,%20android.app.admin.DevicePolicyManager.setPolicy.T)` and related APIs.

Policies should be structured as:

```kotlin
<code>{ @}TypePolicyDefinition
  private static final PolicyIdentifier&lt;Type&gt; POLICY_NAME =
      new SimplePolicyIdentifier&lt;&gt;("POLICY_NAME");
  </code>
```

Currently policy definitions are restricted to the `android.app.admin.policy` namespace. This restriction might be lifted in the future.

## Summary

| Public methods ||
|---|---|
| open static [PolicyIdentifier](https://developer.android.com/reference/kotlin/android/app/admin/PolicyIdentifier#)\<U\> | `https://developer.android.com/reference/kotlin/android/app/admin/PolicyIdentifier#createForTesting(kotlin.String)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Create an instance of PolicyIdentifier for testing purposes. |

## Public methods

### createForTesting

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <U : Any!> createForTesting(id: String): PolicyIdentifier<U>
```

**Deprecated:** *Use android.app.admin.PolicyIdentifier.SimplePolicyIdentifier#createForTesting(java.lang.String) instead.*

Create an instance of PolicyIdentifier for testing purposes. This must NOT be used in any real production code.

| Parameters ||
|---|---|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/admin/PolicyIdentifier#<U>` | This value cannot be `null`. |
