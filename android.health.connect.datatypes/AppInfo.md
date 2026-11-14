# AppInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppInfo

Kotlin| [Java](../android/health/connect/datatypes/AppInfo.md) 
| --- | --- |

```
class AppInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.datatypes.AppInfo](../android/health/connect/datatypes/AppInfo.md) |

Application Info class containing details about a given application

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bitmap](../android/graphics/Bitmap.md)? | [getIcon](../android/health/connect/datatypes/AppInfo.md))`()` Returns the application icon as bitmap |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getName](../android/health/connect/datatypes/AppInfo.md))`()` Returns the application name/label |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getPackageName](../android/health/connect/datatypes/AppInfo.md))`()` Returns the application package name |
| --- | --- |

## Public methods

### getIcon

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIcon(): Bitmap?
```

Returns the application icon as bitmap

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------|
| [Bitmap](../android/graphics/Bitmap.md)? | This value may be`null`. |

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
