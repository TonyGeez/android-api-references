# DisplayManager.DisplayListener

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DisplayListener

Kotlin| [Java](../android/hardware/display/DisplayManager.DisplayListener.md) 
| --- | --- |

```
interface DisplayListener
```

| [android.hardware.display.DisplayManager.DisplayListener](../android/hardware/display/DisplayManager.DisplayListener.md) |

Listens for changes in available display devices.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDisplayAdded](../android/hardware/display/DisplayManager.DisplayListener.md))`(`displayId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called whenever a logical display has been added to the system. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDisplayChanged](../android/hardware/display/DisplayManager.DisplayListener.md))`(`displayId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called whenever the properties of a logical [android.view.Display](../android.view/Display.md), such as size and density, have changed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDisplayRemoved](../android/hardware/display/DisplayManager.DisplayListener.md))`(`displayId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called whenever a logical display has been removed from the system. |
| --- | --- |

## Public methods

### onDisplayAdded

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDisplayAdded(displayId: Int): Unit
```

Called whenever a logical display has been added to the system. Use [DisplayManager.getDisplay](DisplayManager.md))to get more information about the display.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| `displayId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The id of the logical display that was added. |

### onDisplayChanged

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDisplayChanged(displayId: Int): Unit
```

Called whenever the properties of a logical [android.view.Display](../android.view/Display.md), such as size and density, have changed.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------|
| `displayId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The id of the logical display that changed. |

### onDisplayRemoved

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDisplayRemoved(displayId: Int): Unit
```

Called whenever a logical display has been removed from the system.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------|
| `displayId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The id of the logical display that was removed. |
