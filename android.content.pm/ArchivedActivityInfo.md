# ArchivedActivityInfo

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ArchivedActivityInfo

Kotlin| [Java](https://developer.android.com/reference/android/content/pm/ArchivedActivityInfo "View this page in Java") 
| --- | --- |

```
class ArchivedActivityInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.pm.ArchivedActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedActivityInfo#) |

Contains fields required to show archived package in Launcher.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ArchivedActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedActivityInfo#ArchivedActivityInfo(kotlin.CharSequence,%20android.content.ComponentName))`(`label:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `componentName:` ` [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)`)` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#) | [getComponentName](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedActivityInfo#getComponentName())`()` The component name of this activity. |
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | [getIcon](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedActivityInfo#getIcon())`()` Icon of the activity in the app's locale. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getLabel](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedActivityInfo#getLabel())`()` The label for the activity. |
| --- | --- |
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | [getMonochromeIcon](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedActivityInfo#getMonochromeIcon())`()` Monochrome icon, if defined, of the activity. |
| [ArchivedActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedActivityInfo#) | [setComponentName](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedActivityInfo#setComponentName(android.content.ComponentName))`(`value:` ` [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)`)` The component name of this activity. |
| [ArchivedActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedActivityInfo#) | [setIcon](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedActivityInfo#setIcon(android.graphics.drawable.Drawable))`(`value:` ` [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)`)` Icon of the activity in the app's locale. |
| --- | --- |
| [ArchivedActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedActivityInfo#) | [setLabel](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedActivityInfo#setLabel(kotlin.CharSequence))`(`value:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`)` The label for the activity. |
| [ArchivedActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedActivityInfo#) | [setMonochromeIcon](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedActivityInfo#setMonochromeIcon(android.graphics.drawable.Drawable))`(`value:` ` [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)`)` Monochrome icon, if defined, of the activity. |

## Public constructors

### ArchivedActivityInfo

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArchivedActivityInfo(
    label: CharSequence, 
    componentName: ComponentName)
```

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------|
| `label` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):This value cannot be`null`. |
| `componentName` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#):This value cannot be`null`. |

## Public methods

### getComponentName

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getComponentName(): ComponentName
```

The component name of this activity.

| Return ||
|-----------------------------------------------------------------------------------------------------|-----------------------------|
| [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#) | This value cannot be`null`. |

### getIcon

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIcon(): Drawable?
```

Icon of the activity in the app's locale. if null then the default icon would be shown in the launcher. 

### getLabel

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLabel(): CharSequence
```

The label for the activity.

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | This value cannot be`null`. |

### getMonochromeIcon

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMonochromeIcon(): Drawable?
```

Monochrome icon, if defined, of the activity.

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------|
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | This value may be`null`. |

### setComponentName

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setComponentName(value: ComponentName): ArchivedActivityInfo
```

The component name of this activity.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------|
| `value` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#):This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ArchivedActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedActivityInfo#) | This value cannot be`null`. |

### setIcon

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setIcon(value: Drawable): ArchivedActivityInfo
```

Icon of the activity in the app's locale. if null then the default icon would be shown in the launcher.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#):This value cannot be`null`. |

### setLabel

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLabel(value: CharSequence): ArchivedActivityInfo
```

The label for the activity.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `value` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ArchivedActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedActivityInfo#) | This value cannot be`null`. |

### setMonochromeIcon

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setMonochromeIcon(value: Drawable): ArchivedActivityInfo
```

Monochrome icon, if defined, of the activity.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#):This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ArchivedActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ArchivedActivityInfo#) | This value cannot be`null`. |
