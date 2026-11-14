Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LauncherActivityInfo

```
open class LauncherActivityInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.content.pm.LauncherActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/LauncherActivityInfo#) |

A representation of an activity that can belong to this user or a managed profile associated with this user. It can be used to query the label, icon and badged icon for the activity.

## Summary

| Public methods ||
|---|---|
| open [ActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo) | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherActivityInfo#getActivityInfo()()` Returns the ActivityInfo of the activity. |
| open [ApplicationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo)! | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherActivityInfo#getApplicationInfo()()` Returns the application info for the application this activity belongs to. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)! | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherActivityInfo#getBadgedIcon(kotlin.Int)(density: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the activity icon with badging appropriate for the profile. |
| open [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)! | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherActivityInfo#getComponentName()()` Returns the component name of this activity. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherActivityInfo#getFirstInstallTime()()` Returns the time at which the package was first installed. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)! | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherActivityInfo#getIcon(kotlin.Int)(density: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the icon for this activity, without any badging for the profile. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherActivityInfo#getLabel()()` Retrieves the label for the activity. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherActivityInfo#getLoadingProgress()()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherActivityInfo#getName()()` Returns the name for the activity from android:name in the manifest. |
| open [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)! | `https://developer.android.com/reference/kotlin/android/content/pm/LauncherActivityInfo#getUser()()` Returns the user handle of the user profile that this activity belongs to. |

## Public methods

### getActivityInfo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActivityInfo(): ActivityInfo
```

Returns the ActivityInfo of the activity.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo` | Activity Info. This value cannot be `null`. |

### getApplicationInfo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getApplicationInfo(): ApplicationInfo!
```

Returns the application info for the application this activity belongs to.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo!` | |

### getBadgedIcon

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBadgedIcon(density: Int): Drawable!
```

Returns the activity icon with badging appropriate for the profile.

| Parameters ||
|---|---|
| `density` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Optional density for the icon, or 0 to use the default density. Use `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#` for DPI values. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` | A badged icon for the activity. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#`

### getComponentName

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getComponentName(): ComponentName!
```

Returns the component name of this activity.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!` | ComponentName of the activity |

### getFirstInstallTime

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFirstInstallTime(): Long
```

Returns the time at which the package was first installed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The time of installation of the package, in milliseconds. |

### getIcon

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIcon(density: Int): Drawable!
```

Returns the icon for this activity, without any badging for the profile.

The returned drawable is subject to the same size capping limits as described in `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getApplicationIcon(android.content.pm.ApplicationInfo)`.

| Parameters ||
|---|---|
| `density` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The preferred density of the icon, zero for default density. Use density DPI values from `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` | The drawable associated with the activity. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/LauncherActivityInfo#getBadgedIcon(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#`

### getLabel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLabel(): CharSequence!
```

Retrieves the label for the activity. If the activity's label is invisible for the user, use the application's label instead. If the application's label is still invisible for the user, use the package name instead.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | The label for the activity. If the activity's label is invisible for the user, return the application's label instead. If the application's label is still invisible for the user, return the package name instead. |

### getLoadingProgress

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLoadingProgress(): Float
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Package loading progress, range between \[0, 1\]. Value is between 0.0f and 1.0f inclusive |

### getName

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getName(): String!
```

Returns the name for the activity from android:name in the manifest.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the name from android:name for the activity. |

### getUser

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUser(): UserHandle!
```

Returns the user handle of the user profile that this activity belongs to. In order to persist the identity of the profile, do not store the UserHandle. Instead retrieve its serial number from UserManager. You can convert the serial number back to a UserHandle for later use.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!` | The UserHandle of the profile. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/UserManager.html#getSerialNumberForUser(android.os.UserHandle)`
- `https://developer.android.com/reference/kotlin/android/os/UserManager.html#getUserForSerialNumber(kotlin.Long)`
