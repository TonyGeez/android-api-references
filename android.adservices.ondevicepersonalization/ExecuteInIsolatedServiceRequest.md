Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExecuteInIsolatedServiceRequest

Kotlin | [Java](ExecuteInIsolatedServiceRequest.md)
| --- | --- |

```
open class ExecuteInIsolatedServiceRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.ondevicepersonalization.ExecuteInIsolatedServiceRequest](ExecuteInIsolatedServiceRequest.md) |

The request of `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationManager#executeInIsolatedService(android.adservices.ondevicepersonalization.ExecuteInIsolatedServiceRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest.Builder` A builder for `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest#` |
| open | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest.OutputSpec` The set of spec to indicate output of `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService`. |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| open [PersistableBundle](../android.os/PersistableBundle.md) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest#getAppParams()()` A `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#` that is passed from the calling app to the `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService`. |
| open [ExecuteInIsolatedServiceRequest.OutputSpec](../android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest.OutputSpec.md) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest#getOutputSpec()()` The set of spec to indicate output of `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService`. |
| --- | --- |
| open [ComponentName](../android.content/ComponentName.md) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest#getService()()` The `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` of the `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest#hashCode()()` Returns a hash code value for the object. |

## Public methods

### equals

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
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

### getAppParams

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAppParams(): PersistableBundle
```

**Deprecated:** *Deprecated in Java.*

A `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#` that is passed from the calling app to the `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService`. The expected contents of this parameter are defined by the `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService`. The platform does not interpret this parameter.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#` | This value cannot be `null`. |

### getOutputSpec

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOutputSpec(): ExecuteInIsolatedServiceRequest.OutputSpec
```

**Deprecated:** *Deprecated in Java.*

The set of spec to indicate output of `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService`. It's mainly used by platform. For example, platform calls `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest.OutputSpec#getOutputType()` and validates the result received from `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest.OutputSpec` | This value cannot be `null`. |

### getService

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getService(): ComponentName
```

**Deprecated:** *Deprecated in Java.*

The `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` of the `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` | This value cannot be `null`. |

### hashCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
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
