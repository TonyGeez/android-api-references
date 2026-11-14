# DisplayManager.DisplayListener

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DisplayListener

Kotlin| [Java](https://developer.android.com/reference/android/hardware/display/DisplayManager.DisplayListener "View this page in Java") 

```
interface DisplayListener
```

| [android.hardware.display.DisplayManager.DisplayListener](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.DisplayListener#) |

Listens for changes in available display devices.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDisplayAdded](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.DisplayListener#onDisplayAdded(kotlin.Int))`(`displayId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called whenever a logical display has been added to the system. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDisplayChanged](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.DisplayListener#onDisplayChanged(kotlin.Int))`(`displayId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called whenever the properties of a logical [android.view.Display](https://developer.android.com/reference/kotlin/android/view/Display.html#), such as size and density, have changed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDisplayRemoved](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.DisplayListener#onDisplayRemoved(kotlin.Int))`(`displayId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called whenever a logical display has been removed from the system. |

## Public methods

### onDisplayAdded

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDisplayAdded(displayId: Int): Unit
```

Called whenever a logical display has been added to the system. Use [DisplayManager.getDisplay](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager#getDisplay(kotlin.Int))to get more information about the display.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| `displayId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The id of the logical display that was added. |

### onDisplayChanged

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDisplayChanged(displayId: Int): Unit
```

Called whenever the properties of a logical [android.view.Display](https://developer.android.com/reference/kotlin/android/view/Display.html#), such as size and density, have changed.

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
