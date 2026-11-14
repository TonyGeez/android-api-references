Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TrainingInterval

Kotlin | [Java](TrainingInterval.md)
| --- | --- |

```
class TrainingInterval
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.ondevicepersonalization.TrainingInterval](TrainingInterval.md) |

Training interval settings required for federated computation jobs.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/TrainingInterval.Builder` A builder for `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/TrainingInterval#` |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/TrainingInterval#SCHEDULING_MODE_ONE_TIME:kotlin.Int` The scheduling mode for a one-off task. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/TrainingInterval#SCHEDULING_MODE_RECURRENT:kotlin.Int` The scheduling mode for a task that will be rescheduled after each run. |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/TrainingInterval#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Duration](../java.time/Duration.md) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/TrainingInterval#getMinimumInterval()()` Sets the minimum time interval between two training runs. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/TrainingInterval#getSchedulingMode()()` The scheduling mode for this task, either `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/TrainingInterval#SCHEDULING_MODE_ONE_TIME:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/TrainingInterval#SCHEDULING_MODE_RECURRENT:kotlin.Int`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/TrainingInterval#hashCode()()` Returns a hash code value for the object. |

## Constants

### SCHEDULING_MODE_ONE_TIME

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCHEDULING_MODE_ONE_TIME: Int
```

**Deprecated:** *Deprecated in Java.*

The scheduling mode for a one-off task.

 Value: 1

### SCHEDULING_MODE_RECURRENT

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCHEDULING_MODE_RECURRENT: Int
```

**Deprecated:** *Deprecated in Java.*

The scheduling mode for a task that will be rescheduled after each run.

 Value: 2

## Public methods

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### getMinimumInterval

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMinimumInterval(): Duration
```

**Deprecated:** *Deprecated in Java.*

Sets the minimum time interval between two training runs.

This field will only be used when the scheduling mode is `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/TrainingInterval#SCHEDULING_MODE_RECURRENT:kotlin.Int`. Only positive values are accepted, zero or negative values will result in IllegalArgumentException.

Please also note this value is advisory, which does not guarantee the job will be run immediately after the interval expired. Federated compute will still enforce a minimum required interval and training constraints to ensure system health. The current training constraints are device on unmetered network, idle and battery not low.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Duration.html#` | This value cannot be `null`. |

### getSchedulingMode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSchedulingMode(): Int
```

**Deprecated:** *Deprecated in Java.*

The scheduling mode for this task, either `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/TrainingInterval#SCHEDULING_MODE_ONE_TIME:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/TrainingInterval#SCHEDULING_MODE_RECURRENT:kotlin.Int`. The default scheduling mode is `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/TrainingInterval#SCHEDULING_MODE_ONE_TIME:kotlin.Int` if unspecified.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/TrainingInterval#SCHEDULING_MODE_ONE_TIME:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/TrainingInterval#SCHEDULING_MODE_RECURRENT:kotlin.Int` |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
