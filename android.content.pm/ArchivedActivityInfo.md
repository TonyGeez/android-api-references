# ArchivedActivityInfo

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ArchivedActivityInfo

Kotlin| [Java](ArchivedActivityInfo.md) 
| --- | --- |

```
class ArchivedActivityInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.pm.ArchivedActivityInfo](ArchivedActivityInfo.md) |

Contains fields required to show archived package in Launcher.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ArchivedActivityInfo](ArchivedActivityInfo.md))`(`label:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `componentName:` ` [ComponentName](../android.content/ComponentName.md)`)` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ComponentName](../android.content/ComponentName.md) | [getComponentName](ArchivedActivityInfo.md))`()` The component name of this activity. |
| [Drawable](../android.graphics.drawable/Drawable.md)? | [getIcon](ArchivedActivityInfo.md))`()` Icon of the activity in the app's locale. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getLabel](ArchivedActivityInfo.md))`()` The label for the activity. |
| --- | --- |
| [Drawable](../android.graphics.drawable/Drawable.md)? | [getMonochromeIcon](ArchivedActivityInfo.md))`()` Monochrome icon, if defined, of the activity. |
| [ArchivedActivityInfo](ArchivedActivityInfo.md) | [setComponentName](ArchivedActivityInfo.md))`(`value:` ` [ComponentName](../android.content/ComponentName.md)`)` The component name of this activity. |
| [ArchivedActivityInfo](ArchivedActivityInfo.md) | [setIcon](ArchivedActivityInfo.md))`(`value:` ` [Drawable](../android.graphics.drawable/Drawable.md)`)` Icon of the activity in the app's locale. |
| --- | --- |
| [ArchivedActivityInfo](ArchivedActivityInfo.md) | [setLabel](ArchivedActivityInfo.md))`(`value:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`)` The label for the activity. |
| [ArchivedActivityInfo](ArchivedActivityInfo.md) | [setMonochromeIcon](ArchivedActivityInfo.md))`(`value:` ` [Drawable](../android.graphics.drawable/Drawable.md)`)` Monochrome icon, if defined, of the activity. |

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
| `componentName` | [ComponentName](../android.content/ComponentName.md):This value cannot be`null`. |

## Public methods

### getComponentName

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getComponentName(): ComponentName
```

The component name of this activity.

| Return ||
|-----------------------------------------------------------------------------------------------------|-----------------------------|
| [ComponentName](../android.content/ComponentName.md) | This value cannot be`null`. |

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
| [Drawable](../android.graphics.drawable/Drawable.md)? | This value may be`null`. |

### setComponentName

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setComponentName(value: ComponentName): ArchivedActivityInfo
```

The component name of this activity.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------|
| `value` | [ComponentName](../android.content/ComponentName.md):This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ArchivedActivityInfo](ArchivedActivityInfo.md) | This value cannot be`null`. |

### setIcon

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setIcon(value: Drawable): ArchivedActivityInfo
```

Icon of the activity in the app's locale. if null then the default icon would be shown in the launcher.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Drawable](../android.graphics.drawable/Drawable.md):This value cannot be`null`. |

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
| [ArchivedActivityInfo](ArchivedActivityInfo.md) | This value cannot be`null`. |

### setMonochromeIcon

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setMonochromeIcon(value: Drawable): ArchivedActivityInfo
```

Monochrome icon, if defined, of the activity.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Drawable](../android.graphics.drawable/Drawable.md):This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ArchivedActivityInfo](ArchivedActivityInfo.md) | This value cannot be`null`. |
