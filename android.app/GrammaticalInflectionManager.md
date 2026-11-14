# GrammaticalInflectionManager

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GrammaticalInflectionManager

Kotlin| [Java](../android/app/GrammaticalInflectionManager.md) 
| --- | --- |

```
open class GrammaticalInflectionManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.GrammaticalInflectionManager](../android/app/GrammaticalInflectionManager.md) |

This class allow applications to control granular grammatical inflection settings (such as per-app grammatical gender).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getApplicationGrammaticalGender](../android/app/GrammaticalInflectionManager.md))`()` Returns the current grammatical gender for the calling app. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSystemGrammaticalGender](../android/app/GrammaticalInflectionManager.md))`()` Allows privileged preloaded applications to get the system grammatical gender when set. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRequestedApplicationGrammaticalGender](../android/app/GrammaticalInflectionManager.md))`(`grammaticalGender:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the current grammatical gender for the calling app (keyed by package name and user ID retrieved from the calling pid). |
| --- | --- |

## Public methods

### getApplicationGrammaticalGender

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getApplicationGrammaticalGender(): Int
```

Returns the current grammatical gender for the calling app. A new value can be requested via [setRequestedApplicationGrammaticalGender(int)](../android/app/GrammaticalInflectionManager.md))and will be updated with a new configuration change. The method always returns the value received with the last received configuration change.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value of grammatical gender Value is [android.content.res.Configuration#GRAMMATICAL_GENDER_NOT_SPECIFIED](../android/content/res/Configuration.md), [android.content.res.Configuration#GRAMMATICAL_GENDER_NEUTRAL](../android/content/res/Configuration.md), [android.content.res.Configuration#GRAMMATICAL_GENDER_FEMININE](../android/content/res/Configuration.md), or [android.content.res.Configuration#GRAMMATICAL_GENDER_MASCULINE](../android/content/res/Configuration.md) |

**See Also**

- [android.content.res.Configuration#getGrammaticalGender](../android/content/res/Configuration.md)) 

### getSystemGrammaticalGender

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSystemGrammaticalGender(): Int
```

Allows privileged preloaded applications to get the system grammatical gender when set. 
Requires android.Manifest.permission.READ_SYSTEM_GRAMMATICAL_GENDER

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The value of system grammatical gender only if the calling app has the permission, otherwise throwing an exception. Value is [android.content.res.Configuration#GRAMMATICAL_GENDER_NOT_SPECIFIED](../android/content/res/Configuration.md), [android.content.res.Configuration#GRAMMATICAL_GENDER_NEUTRAL](../android/content/res/Configuration.md), [android.content.res.Configuration#GRAMMATICAL_GENDER_FEMININE](../android/content/res/Configuration.md), or [android.content.res.Configuration#GRAMMATICAL_GENDER_MASCULINE](../android/content/res/Configuration.md) |

| Exceptions ||
|-------------------------------|------------------------------------------------------|
| `java.lang.SecurityException` | If the caller does not have the required permission. |

**See Also**

- [android.content.res.Configuration#getGrammaticalGender](../android/content/res/Configuration.md)) 

### setRequestedApplicationGrammaticalGender

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRequestedApplicationGrammaticalGender(grammaticalGender: Int): Unit
```

Sets the current grammatical gender for the calling app (keyed by package name and user ID retrieved from the calling pid).

**Note:** Changes to app grammatical gender will result in a configuration change (and potentially an Activity re-creation) being applied to the specified application. For more information, see the [section on handling configuration changes](https://developer.android.com/guide/topics/resources/runtime-changes). The set grammatical gender are persisted across application restarts; they are backed up if the user has enabled Backup \& Restore.\`

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `grammaticalGender` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the terms of address the user preferred in an application. Value is [android.content.res.Configuration#GRAMMATICAL_GENDER_NOT_SPECIFIED](../android/content/res/Configuration.md), [android.content.res.Configuration#GRAMMATICAL_GENDER_NEUTRAL](../android/content/res/Configuration.md), [android.content.res.Configuration#GRAMMATICAL_GENDER_FEMININE](../android/content/res/Configuration.md), or [android.content.res.Configuration#GRAMMATICAL_GENDER_MASCULINE](../android/content/res/Configuration.md) |

**See Also**

- [android.content.res.Configuration#getGrammaticalGender](../android/content/res/Configuration.md))
