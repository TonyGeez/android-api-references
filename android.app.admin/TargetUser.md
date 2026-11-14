# TargetUser

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TargetUser

Kotlin| [Java](../android/app/admin/TargetUser.md) 
| --- | --- |

```
class TargetUser
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.admin.TargetUser](../android/app/admin/TargetUser.md) |

Class representing the target user of a policy set by an admin (set from [DevicePolicyManager](../android/app/admin/DevicePolicyManager.md)), this is passed in to [PolicyUpdateReceiver.onPolicySetResult](../android/app/admin/PolicyUpdateReceiver.md))and [PolicyUpdateReceiver.onPolicyChanged](../android/app/admin/PolicyUpdateReceiver.md)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/app/admin/TargetUser.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/app/admin/TargetUser.md))`()` <br /> |

| Properties ||
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [TargetUser](../android/app/admin/TargetUser.md) | [GLOBAL](../android/app/admin/TargetUser.md) This indicates the policy is a global policy. |
| static [TargetUser](../android/app/admin/TargetUser.md) | [LOCAL_USER](../android/app/admin/TargetUser.md) Indicates that the policy relates to the user the admin is installed on. |
| static [TargetUser](../android/app/admin/TargetUser.md) | [PARENT_USER](../android/app/admin/TargetUser.md) For admins of profiles, this indicates that the policy relates to the parent profile. |
| --- | --- |
| static [TargetUser](../android/app/admin/TargetUser.md) | [UNKNOWN_USER](../android/app/admin/TargetUser.md) Indicates that the policy relates to some unknown user on the device. |

## Public methods

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

## Properties

### GLOBAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GLOBAL: TargetUser
```

This indicates the policy is a global policy. 

### LOCAL_USER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCAL_USER: TargetUser
```

Indicates that the policy relates to the user the admin is installed on. 

### PARENT_USER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PARENT_USER: TargetUser
```

For admins of profiles, this indicates that the policy relates to the parent profile. 

### UNKNOWN_USER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNKNOWN_USER: TargetUser
```

Indicates that the policy relates to some unknown user on the device. For example, if Admin1 has set a global policy on a device and Admin2 has set a conflicting local policy on some other secondary user, Admin1 will get a policy update callback with`UNKNOWN_USER`as the target user.
