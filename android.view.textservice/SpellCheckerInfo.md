Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SpellCheckerInfo

```
class SpellCheckerInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.textservice.SpellCheckerInfo](SpellCheckerInfo.md) |

This class is used to specify meta information of a spell checker. The XML file specifying metadata for a spell checker service must adhere to the following constraints:

- All literal strings and resolved string resources must not exceed 1,000 characters in length each.
- The total size of the XML file must not exceed 204,800 bytes (200 KiB).
- The total length of all literal strings, resolved string resources, integers, and resource IDs must not exceed 204,800 bytes (200 KiB).

<br />

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerInfo#describeContents()()` Used to make this class parcelable. |
| [ComponentName](../android.content/ComponentName.md)! | `https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerInfo#getComponent()()` Return the component of the service that implements. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerInfo#getId()()` Return a unique ID for this spell checker. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerInfo#getPackageName()()` Return the . |
| [ServiceInfo](../android.content.pm/ServiceInfo.md)! | `https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerInfo#getServiceInfo()()` Return the raw information about the Service implementing this spell checker. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerInfo#getSettingsActivity()()` Return the class name of an activity that provides a settings UI. |
| --- | --- |
| [SpellCheckerSubtype](SpellCheckerSubtype.md)! | `https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerInfo#getSubtypeAt(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the subtype at the specified index. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerInfo#getSubtypeCount()()` Return the count of the subtypes. |
| [Drawable](../android.graphics.drawable/Drawable.md)! | `https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerInfo#loadIcon(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#!)` Load the user-displayed icon for this spell checker. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerInfo#loadLabel(android.content.pm.PackageManager)(pm: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#!)` Load the user-displayed label for this spell checker. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Used to package this object into a `https://developer.android.com/reference/kotlin/android/os/Parcel.html#`. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SpellCheckerInfo](SpellCheckerInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerInfo#CREATOR:android.os.Parcelable.Creator` Used to make this class parcelable. |

## Public methods

### describeContents

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Used to make this class parcelable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getComponent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getComponent(): ComponentName!
```

Return the component of the service that implements.

### getId

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getId(): String!
```

Return a unique ID for this spell checker. The ID is generated from the package and class name implementing the method.

### getPackageName

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPackageName(): String!
```

Return the .apk package that implements this.

### getServiceInfo

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getServiceInfo(): ServiceInfo!
```

Return the raw information about the Service implementing this spell checker. Do not modify the returned object.

### getSettingsActivity

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSettingsActivity(): String!
```

Return the class name of an activity that provides a settings UI. You can launch this activity be starting it with an `https://developer.android.com/reference/kotlin/android/content/Intent.html#` whose action is MAIN and with an explicit `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` composed of `https://developer.android.com/reference/kotlin/android/view/textservice/SpellCheckerInfo#getPackageName()` and the class name returned here.

A null will be returned if there is no settings activity.

### getSubtypeAt

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSubtypeAt(index: Int): SpellCheckerSubtype!
```

Return the subtype at the specified index.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the subtype to return. |

### getSubtypeCount

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSubtypeCount(): Int
```

Return the count of the subtypes.

### loadIcon

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun loadIcon(pm: PackageManager!): Drawable!
```

Load the user-displayed icon for this spell checker.

| Parameters ||
|---|---|
| `pm` | [PackageManager](../android.content.pm/PackageManager.md)!: Supply a PackageManager used to load the spell checker's resources. |

### loadLabel

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun loadLabel(pm: PackageManager!): CharSequence!
```

Load the user-displayed label for this spell checker.

| Parameters ||
|---|---|
| `pm` | [PackageManager](../android.content.pm/PackageManager.md)!: Supply a PackageManager used to load the spell checker's resources. |

### writeToParcel

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Used to package this object into a `https://developer.android.com/reference/kotlin/android/os/Parcel.html#`.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): The `https://developer.android.com/reference/kotlin/android/os/Parcel.html#` to be written. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The flags used for parceling. |

## Properties

### CREATOR

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<SpellCheckerInfo!>
```

Used to make this class parcelable.
