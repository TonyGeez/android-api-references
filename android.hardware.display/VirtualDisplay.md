# VirtualDisplay

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VirtualDisplay

Kotlin| [Java](../android/hardware/display/VirtualDisplay.md) 
| --- | --- |

```
class VirtualDisplay
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.display.VirtualDisplay](../android/hardware/display/VirtualDisplay.md) |

Represents a virtual display. The content of a virtual display is rendered to a [android.view.Surface](../android/view/Surface.md) that you must provide to android.hardware.display.DisplayManager#createVirtualDisplay.

Because a virtual display renders to a surface provided by the application, it will be released automatically when the process terminates and all remaining windows on it will be forcibly removed. However, you should also explicitly call [release](../android/hardware/display/VirtualDisplay.md))when you're done with it.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Callback](../android/hardware/display/VirtualDisplay.Callback.md) Interface for receiving information about a [VirtualDisplay](../android/hardware/display/VirtualDisplay.md)'s state changes. |

| Public methods ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Display](../android/view/Display.md)! | [getDisplay](../android/hardware/display/VirtualDisplay.md))`()` Gets the virtual display. |
| [Surface](../android/view/Surface.md)! | [getSurface](../android/hardware/display/VirtualDisplay.md))`()` Gets the surface that backs the virtual display. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](../android/hardware/display/VirtualDisplay.md))`()` Releases the virtual display and destroys its underlying surface. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resize](../android/hardware/display/VirtualDisplay.md))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `densityDpi:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Asks the virtual display to resize. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRotation](../android/hardware/display/VirtualDisplay.md))`(`rotation:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the rotation of the virtual display. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSurface](../android/hardware/display/VirtualDisplay.md))`(`surface:` ` [Surface](../android/view/Surface.md)!`)` Sets the surface that backs the virtual display. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/hardware/display/VirtualDisplay.md))`()` <br /> |

## Public methods

### getDisplay

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplay(): Display!
```

Gets the virtual display. 

### getSurface

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSurface(): Surface!
```

Gets the surface that backs the virtual display. 

### release

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun release(): Unit
```

Releases the virtual display and destroys its underlying surface.

All remaining windows on the virtual display will be forcibly removed as part of releasing the virtual display. 

### resize

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun resize(
    width: Int, 
    height: Int, 
    densityDpi: Int
): Unit
```

Asks the virtual display to resize.

This is really just a convenience to allow applications using virtual displays to adapt to changing conditions without having to tear down and recreate the display. 

### setRotation

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setRotation(rotation: Int): Unit
```

Sets the rotation of the virtual display.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rotation` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new rotation of the display. May be one of [Surface.ROTATION_0](../android/view/Surface.md), [Surface.ROTATION_90](../android/view/Surface.md), [Surface.ROTATION_180](../android/view/Surface.md), [Surface.ROTATION_270](../android/view/Surface.md). Upon creation, the rotation of the virtual display is always [Surface.ROTATION_0](../android/view/Surface.md). Value is [android.view.Surface#ROTATION_0](../android/view/Surface.md), [android.view.Surface#ROTATION_90](../android/view/Surface.md), [android.view.Surface#ROTATION_180](../android/view/Surface.md), or [android.view.Surface#ROTATION_270](../android/view/Surface.md) |

### setSurface

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setSurface(surface: Surface!): Unit
```

Sets the surface that backs the virtual display.

Detaching the surface that backs a virtual display has a similar effect to turning off the screen.

It is still the caller's responsibility to destroy the surface after it has been detached.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `surface` | [Surface](../android/view/Surface.md)!:The surface to set, or null to detach the surface from the virtual display. |

### toString

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
