Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Condition

Kotlin | [Java](../android/service/notification/Condition.md)
| --- | --- |

```
class Condition : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.notification.Condition](../android/service/notification/Condition.md) |

The current condition of an `https://developer.android.com/reference/kotlin/android/app/AutomaticZenRule.html#`, provided by the app that owns the rule. Used to tell the system to enter Do Not Disturb mode and request that the system exit Do Not Disturb mode.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#FLAG_RELEVANT_ALWAYS:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#FLAG_RELEVANT_NOW:kotlin.Int` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#SCHEME:kotlin.String` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#SOURCE_CONTEXT:kotlin.Int` The state is changing due to a change in context (such as detected driving or sleeping). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#SOURCE_SCHEDULE:kotlin.Int` The state is changing due to an automatic schedule (alarm, set time, etc). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#SOURCE_UNKNOWN:kotlin.Int` The state is changing due to an unknown reason. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#SOURCE_USER_ACTION:kotlin.Int` The state is changing due to an explicit user action. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#STATE_ERROR:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#STATE_FALSE:kotlin.Int` Indicates that Do Not Disturb should be turned off. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#STATE_TRUE:kotlin.Int` Indicates that Do Not Disturb should be turned on. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#STATE_UNKNOWN:kotlin.Int` <br /> |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/service/notification/Condition#Condition(android.net.Uri,%20kotlin.String,%20kotlin.Int)(id: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, summary: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, state: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` An object representing the current state of a `https://developer.android.com/reference/kotlin/android/app/AutomaticZenRule.html#`. |
| `https://developer.android.com/reference/kotlin/android/service/notification/Condition#Condition(android.net.Uri,%20kotlin.String,%20kotlin.Int,%20kotlin.Int)(id: https://developer.android.com/reference/kotlin/android/net/Uri.html#?, summary: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, state: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` An object representing the current state of a `https://developer.android.com/reference/kotlin/android/app/AutomaticZenRule.html#`. |
| `https://developer.android.com/reference/kotlin/android/service/notification/Condition#Condition(android.net.Uri,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(id: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, summary: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, line1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, line2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, icon: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, state: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| `https://developer.android.com/reference/kotlin/android/service/notification/Condition#Condition(android.net.Uri,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(id: https://developer.android.com/reference/kotlin/android/net/Uri.html#?, summary: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, line1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, line2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, icon: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, state: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` An object representing the current state of a `https://developer.android.com/reference/kotlin/android/app/AutomaticZenRule.html#`. |
| `https://developer.android.com/reference/kotlin/android/service/notification/Condition#Condition(android.os.Parcel)(source: https://developer.android.com/reference/kotlin/android/os/Parcel.html#!)` <br /> |

| Public methods ||
|---|---|
| [Condition](../android/service/notification/Condition.md)! | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#copy()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#hashCode()()` Returns a hash code value for the object. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#isValidId(android.net.Uri,%20kotlin.String)(id: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, pkg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` <br /> |
| static [Uri.Builder](../android/net/Uri.Builder.md)! | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#newId(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#relevanceToString(kotlin.Int)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#stateToString(kotlin.Int)(state: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#toString()()` Returns a string representation of the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Condition](../android/service/notification/Condition.md)!\> | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#CREATOR:android.os.Parcelable.Creator` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#flags:kotlin.Int` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#icon:kotlin.Int` <br /> |
| --- | --- |
| [Uri](../android/net/Uri.md)! | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#id:android.net.Uri` The URI representing the rule being updated. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#line1:kotlin.String` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#line2:kotlin.String` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#source:kotlin.Int` The source of, or reason for, the state change represented by this Condition. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#state:kotlin.Int` The state of this condition. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/service/notification/Condition#summary:kotlin.String` A summary of what the rule encoded in `https://developer.android.com/reference/kotlin/android/service/notification/Condition#id:android.net.Uri` means when it is enabled. |
| --- | --- |

## Constants

### FLAG_RELEVANT_ALWAYS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_RELEVANT_ALWAYS: Int
```

 Value: 2

### FLAG_RELEVANT_NOW

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_RELEVANT_NOW: Int
```

 Value: 1

### SCHEME

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCHEME: String
```

 Value: "condition"

### SOURCE_CONTEXT

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SOURCE_CONTEXT: Int
```

The state is changing due to a change in context (such as detected driving or sleeping).

 Value: 3

### SOURCE_SCHEDULE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SOURCE_SCHEDULE: Int
```

The state is changing due to an automatic schedule (alarm, set time, etc).

 Value: 2

### SOURCE_UNKNOWN

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SOURCE_UNKNOWN: Int
```

The state is changing due to an unknown reason.

 Value: 0

### SOURCE_USER_ACTION

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SOURCE_USER_ACTION: Int
```

The state is changing due to an explicit user action.

 Value: 1

### STATE_ERROR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_ERROR: Int
```

 Value: 3

### STATE_FALSE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_FALSE: Int
```

Indicates that Do Not Disturb should be turned off. Note that all Conditions from all `https://developer.android.com/reference/kotlin/android/app/AutomaticZenRule.html#` providers must be off for Do Not Disturb to be turned off on the device.

 Value: 0

### STATE_TRUE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_TRUE: Int
```

Indicates that Do Not Disturb should be turned on.

 Value: 1

### STATE_UNKNOWN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_UNKNOWN: Int
```

 Value: 2

## Public constructors

### Condition

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Condition(
    id: Uri!, 
    summary: String!, 
    state: Int)
```

An object representing the current state of a `https://developer.android.com/reference/kotlin/android/app/AutomaticZenRule.html#`.

| Parameters ||
|---|---|
| `id` | [Uri](../android/net/Uri.md)!: the `https://developer.android.com/reference/kotlin/android/app/AutomaticZenRule.html#getConditionId()` of the zen rule |
| `summary` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a user visible description of the rule state |
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): whether the mode should be activated or deactivated |
| --- | --- |

### Condition

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Condition(
    id: Uri?, 
    summary: String?, 
    state: Int, 
    source: Int)
```

An object representing the current state of a `https://developer.android.com/reference/kotlin/android/app/AutomaticZenRule.html#`.

| Parameters ||
|---|---|
| `id` | [Uri](../android/net/Uri.md)?: the `https://developer.android.com/reference/kotlin/android/app/AutomaticZenRule.html#getConditionId()` of the zen rule. This value may be `null`. |
| `summary` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a user visible description of the rule state. This value may be `null`. |
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): whether the mode should be activated or deactivated. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/service/notification/Condition#STATE_FALSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/notification/Condition#STATE_TRUE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/notification/Condition#STATE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/notification/Condition#STATE_ERROR:kotlin.Int` |
| --- | --- |
| `source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the source of, or reason for, the state change represented by this Condition. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/service/notification/Condition#SOURCE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/notification/Condition#SOURCE_USER_ACTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/notification/Condition#SOURCE_SCHEDULE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/notification/Condition#SOURCE_CONTEXT:kotlin.Int` |

### Condition

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Condition(
    id: Uri!, 
    summary: String!, 
    line1: String!, 
    line2: String!, 
    icon: Int, 
    state: Int, 
    flags: Int)
```

### Condition

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Condition(
    id: Uri?, 
    summary: String?, 
    line1: String?, 
    line2: String?, 
    icon: Int, 
    state: Int, 
    source: Int, 
    flags: Int)
```

An object representing the current state of a `https://developer.android.com/reference/kotlin/android/app/AutomaticZenRule.html#`.

| Parameters ||
|---|---|
| `id` | [Uri](../android/net/Uri.md)?: the `https://developer.android.com/reference/kotlin/android/app/AutomaticZenRule.html#getConditionId()` of the zen rule. This value may be `null`. |
| `summary` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a user visible description of the rule state. This value may be `null`. |
| `line1` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a user-visible description of when the rule will end. This value may be `null`. |
| --- | --- |
| `line2` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: a continuation of the user-visible description of when the rule will end. This value may be `null`. |
| `icon` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an icon representing this condition |
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): whether the mode should be activated or deactivated. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/service/notification/Condition#STATE_FALSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/notification/Condition#STATE_TRUE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/notification/Condition#STATE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/notification/Condition#STATE_ERROR:kotlin.Int` |
| --- | --- |
| `source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the source of, or reason for, the state change represented by this Condition. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/service/notification/Condition#SOURCE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/notification/Condition#SOURCE_USER_ACTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/notification/Condition#SOURCE_SCHEDULE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/notification/Condition#SOURCE_CONTEXT:kotlin.Int` |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): flags on this condition |

### Condition

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Condition(source: Parcel!)
```

## Public methods

### copy

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun copy(): Condition!
```

### describeContents

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

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

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isValidId

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isValidId(
    id: Uri!, 
    pkg: String!
): Boolean
```

### newId

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun newId(context: Context!): Uri.Builder!
```

### relevanceToString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun relevanceToString(flags: Int): String!
```

### stateToString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun stateToString(state: Int): String!
```

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android/os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<Condition!>
```

### flags

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
val flags: Int
```

### icon

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
val icon: Int
```

### id

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
val id: Uri!
```

The URI representing the rule being updated. See `https://developer.android.com/reference/kotlin/android/app/AutomaticZenRule.html#getConditionId()`.

### line1

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
val line1: String!
```

### line2

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
val line2: String!
```

### source

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
val source: Int
```

The source of, or reason for, the state change represented by this Condition. \*. 
Value is one of the following:

- `https://developer.android.com/reference/kotlin/android/service/notification/Condition#SOURCE_UNKNOWN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/service/notification/Condition#SOURCE_USER_ACTION:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/service/notification/Condition#SOURCE_SCHEDULE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/service/notification/Condition#SOURCE_CONTEXT:kotlin.Int`

<br />

### state

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
val state: Int
```

The state of this condition. `https://developer.android.com/reference/kotlin/android/service/notification/Condition#STATE_TRUE:kotlin.Int` will enable Do Not Disturb mode. `https://developer.android.com/reference/kotlin/android/service/notification/Condition#STATE_FALSE:kotlin.Int` will turn Do Not Disturb off for this rule. Note that Do Not Disturb might still be enabled globally if other conditions are in a `https://developer.android.com/reference/kotlin/android/service/notification/Condition#STATE_TRUE:kotlin.Int` state. 
Value is one of the following:

- `https://developer.android.com/reference/kotlin/android/service/notification/Condition#STATE_FALSE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/service/notification/Condition#STATE_TRUE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/service/notification/Condition#STATE_UNKNOWN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/service/notification/Condition#STATE_ERROR:kotlin.Int`

<br />

### summary

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
val summary: String!
```

A summary of what the rule encoded in `https://developer.android.com/reference/kotlin/android/service/notification/Condition#id:android.net.Uri` means when it is enabled. User visible if the state of the condition is `https://developer.android.com/reference/kotlin/android/service/notification/Condition#STATE_TRUE:kotlin.Int`.
