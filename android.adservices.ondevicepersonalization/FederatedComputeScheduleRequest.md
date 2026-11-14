Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FederatedComputeScheduleRequest

```
class FederatedComputeScheduleRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.ondevicepersonalization.FederatedComputeScheduleRequest](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduleRequest#) |

> [!CAUTION]
> **This class was deprecated in API level 37.**
>
> The ODP APIs are deprecated and will not be supported in future Android releases. There is no direct replacement API available. Developers currently integrated with these APIs must cease further integration efforts. For comprehensive details regarding this deprecation and the future roadmap of Privacy Sandbox on Android, please consult the official Privacy Sandbox developer documentation and announcements: <https://privacysandbox.google.com>

The input for `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduler#schedule(android.adservices.ondevicepersonalization.FederatedComputeScheduleRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduleRequest#FederatedComputeScheduleRequest(android.adservices.ondevicepersonalization.FederatedComputeScheduler.Params,%20kotlin.String)(params: https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduler.Params, populationName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` <br /> |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduleRequest#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [FederatedComputeScheduler.Params](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduler.Params) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduleRequest#getParams()()` Parameters related to job scheduling. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduleRequest#getPopulationName()()` Population refers to a collection of devices that specific task groups can run on. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduleRequest#hashCode()()` Returns a hash code value for the object. |

## Public constructors

### FederatedComputeScheduleRequest

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
FederatedComputeScheduleRequest(
    params: FederatedComputeScheduler.Params, 
    populationName: String)
```

| Parameters ||
|---|---|
| `params` | [FederatedComputeScheduler.Params](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduler.Params): This value cannot be `null`. |
| `populationName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

## Public methods

### equals

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

**Deprecated:** *Deprecated in Java.*

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `o` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getParams

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getParams(): FederatedComputeScheduler.Params
```

**Deprecated:** *Deprecated in Java.*

Parameters related to job scheduling.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/FederatedComputeScheduler.Params` | This value cannot be `null`. |

### getPopulationName

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPopulationName(): String
```

**Deprecated:** *Deprecated in Java.*

Population refers to a collection of devices that specific task groups can run on. It should match task plan configured at remote federated compute server.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### hashCode

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |
