# AppInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppInfo

Kotlin| [Java](https://developer.android.com/reference/android/health/connect/datatypes/AppInfo "View this page in Java") 

```
class AppInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.health.connect.datatypes.AppInfo](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AppInfo#) |

Application Info class containing details about a given application

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | [getIcon](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AppInfo#getIcon())`()` Returns the application icon as bitmap |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getName](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AppInfo#getName())`()` Returns the application name/label |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getPackageName](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AppInfo#getPackageName())`()` Returns the application package name |

## Public methods

### getIcon

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIcon(): Bitmap?
```

Returns the application icon as bitmap

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | This value may be`null`. |

### getName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): String?
```

Returns the application name/label

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getPackageName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPackageName(): String
```

Returns the application package name

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |
