Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UriCustomizationAction

```
class UriCustomizationAction : CustomizationAction
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.hardware.input.CustomizationAction](../android/hardware/input/CustomizationAction.md) ||
| | ↳ | [android.hardware.input.UriCustomizationAction](../android/hardware/input/UriCustomizationAction.md) |

Represents an action that requires an accompanying URI to execute.

Examples include opening a specific file, navigating to a URL, or opening a directory in a file browser.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/UriCustomizationAction#TYPE_OPEN_FILE:kotlin.Int` Action type: Open File. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/UriCustomizationAction#TYPE_OPEN_FOLDER:kotlin.Int` Action type: Open Folder. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/UriCustomizationAction#TYPE_OPEN_URL:kotlin.Int` Action type: Open URL. |
| --- | --- |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/input/UriCustomizationAction#UriCustomizationAction(kotlin.Int,%20android.net.Uri)(actionType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Creates a new `https://developer.android.com/reference/kotlin/android/hardware/input/UriCustomizationAction#`. |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/UriCustomizationAction#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/UriCustomizationAction#getType()()` Gets the action type associated with this customization. |
| [Uri](../android/net/Uri.md) | `https://developer.android.com/reference/kotlin/android/hardware/input/UriCustomizationAction#getUri()()` Gets the URI for this action. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/UriCustomizationAction#hashCode()()` Returns a hash code value for the object. |

## Constants

### TYPE_OPEN_FILE

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_OPEN_FILE: Int
```

Action type: Open File.

Specifies the action to open a file when the peripheral input is triggered.

 Value: 1

### TYPE_OPEN_FOLDER

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_OPEN_FOLDER: Int
```

Action type: Open Folder.

Specifies the action to launch the system file browser for a specific directory when the peripheral input is triggered.

 Value: 2

### TYPE_OPEN_URL

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_OPEN_URL: Int
```

Action type: Open URL.

Specifies the action to open a web URL when the peripheral input is triggered.

 Value: 3

## Public constructors

### UriCustomizationAction

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
UriCustomizationAction(
    actionType: Int, 
    uri: Uri)
```

Creates a new `https://developer.android.com/reference/kotlin/android/hardware/input/UriCustomizationAction#`.

| Parameters ||
|---|---|
| `actionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The type of action to create. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/input/UriCustomizationAction#TYPE_OPEN_FILE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/UriCustomizationAction#TYPE_OPEN_FOLDER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/UriCustomizationAction#TYPE_OPEN_URL:kotlin.Int` |
| `uri` | [Uri](../android/net/Uri.md): The URI to be opened. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the action type is invalid. |
| `java.lang.NullPointerException` | if the `uri` is null. |

## Public methods

### equals

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getType

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getType(): Int
```

Gets the action type associated with this customization.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/input/UriCustomizationAction#TYPE_OPEN_FILE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/UriCustomizationAction#TYPE_OPEN_FOLDER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/UriCustomizationAction#TYPE_OPEN_URL:kotlin.Int` |

### getUri

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUri(): Uri
```

Gets the URI for this action.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#` | The target `https://developer.android.com/reference/kotlin/android/net/Uri.html#`. This value cannot be `null`. |

### hashCode

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
