Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PatternMatcher

Kotlin | [Java](PatternMatcher.md)
| --- | --- |

```
open class PatternMatcher : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.PatternMatcher](PatternMatcher.md) |

| Known Direct Subclasses [PathPermission](../android.content.pm/PathPermission.md) |---|---| | [PathPermission](../android.content.pm/PathPermission.md) | Description of permissions needed to access a particular path in a `https://developer.android.com/reference/kotlin/android/content/pm/ProviderInfo.html#`. | |
| --- | --- | --- | --- | --- | --- | --- |

A simple pattern matcher, which is safe to use on untrusted data: it does not provide full reg-exp support, only simple globbing that can not be used maliciously.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PatternMatcher#PATTERN_ADVANCED_GLOB:kotlin.Int` Pattern type: the given pattern is interpreted with a regular expression-like syntax for matching against the string it is tested against. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PatternMatcher#PATTERN_LITERAL:kotlin.Int` Pattern type: the given pattern must exactly match the string it is tested against. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PatternMatcher#PATTERN_PREFIX:kotlin.Int` Pattern type: the given pattern must match the beginning of the string it is tested against. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PatternMatcher#PATTERN_SIMPLE_GLOB:kotlin.Int` Pattern type: the given pattern is interpreted with a simple glob syntax for matching against the string it is tested against. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PatternMatcher#PATTERN_SUFFIX:kotlin.Int` Pattern type: the given pattern must match the end of the string it is tested against. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/PatternMatcher#PatternMatcher(android.os.Parcel)(src: https://developer.android.com/reference/kotlin/android/os/Parcel!)` <br /> |
| `https://developer.android.com/reference/kotlin/android/os/PatternMatcher#PatternMatcher(kotlin.String,%20kotlin.Int)(pattern: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PatternMatcher#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/os/PatternMatcher#getPath()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/PatternMatcher#getType()()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/PatternMatcher#match(kotlin.String)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/os/PatternMatcher#toString()()` Returns a string representation of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/PatternMatcher#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PatternMatcher](PatternMatcher.md)!\> | `https://developer.android.com/reference/kotlin/android/os/PatternMatcher#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### PATTERN_ADVANCED_GLOB

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PATTERN_ADVANCED_GLOB: Int
```

Pattern type: the given pattern is interpreted with a regular expression-like syntax for matching against the string it is tested against. Supported tokens include dot (`.`) and sets (`[...]`) with full support for character ranges and the not (`^`) modifier. Supported modifiers include star (`*`) for zero-or-more, plus (`+`) for one-or-more and full range (`{...}`) support. This is a simple evaluation implementation in which matching is done against the pattern in real time with no backtracking support.

 Value: 3

### PATTERN_LITERAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PATTERN_LITERAL: Int
```

Pattern type: the given pattern must exactly match the string it is tested against.

 Value: 0

### PATTERN_PREFIX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PATTERN_PREFIX: Int
```

Pattern type: the given pattern must match the beginning of the string it is tested against.

 Value: 1

### PATTERN_SIMPLE_GLOB

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PATTERN_SIMPLE_GLOB: Int
```

Pattern type: the given pattern is interpreted with a simple glob syntax for matching against the string it is tested against. In this syntax, you can use the '\*' character to match against zero or more occurrences of the character immediately before. If the character before it is '.' it will match any character. The character '\\' can be used as an escape. This essentially provides only the '\*' wildcard part of a normal regexp.

 Value: 2

### PATTERN_SUFFIX

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PATTERN_SUFFIX: Int
```

Pattern type: the given pattern must match the end of the string it is tested against.

 Value: 4

## Public constructors

### PatternMatcher

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PatternMatcher(src: Parcel!)
```

### PatternMatcher

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PatternMatcher(
    pattern: String!, 
    type: Int)
```

## Public methods

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPath(): String!
```

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getType(): Int
```

### match

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun match(str: String!): Boolean
```

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<PatternMatcher!>
```
