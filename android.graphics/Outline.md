Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Outline

```
class Outline
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.Outline](Outline.md) |

Defines a simple shape, used for bounding graphical regions.

Can be computed for a View, or computed by a Drawable, to drive the shape of shadows cast by a View, or to clip the contents of the View.

## Summary

| Public constructors ||
|---|---|
| Outline Constructs an empty Outline. |
| Outline Constructs an Outline with a copy of the data in src. |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | canClip Returns whether the outline can be used to clip a View. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getAlpha Returns the alpha represented by the Outline. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getRadius Returns the rounded rect radius, if set, or a value less than 0 if a path has been set via setPath. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | getRect Populates `outBounds` with the outline bounds, if set, and returns `true`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isEmpty Returns whether the Outline is empty. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isOuterShadowOnly Returns whether the shadow cast by this Outline is only drawn outside the outline. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | offset Offsets the Outline by (dx,dy). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | set Replace the contents of this Outline with the contents of src. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAlpha Sets the alpha represented by the Outline - the degree to which the producer is guaranteed to be opaque over the Outline's shape. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setConvexPath Sets the Outline to a isConvex. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setEmpty Sets the outline to be empty. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOuterShadowOnly Sets whether the shadow cast by this Outline should only be drawn outside the outline. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOval Convenience for setOval |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOval Sets the outline to the oval defined by input rect. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPath Sets the Outline to a Path. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRect Convenience for setRect |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRect Sets the Outline to the rect defined by the input coordinates. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRoundRect Convenience for setRoundRect |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRoundRect Sets the Outline to the rounded rect defined by the input coordinates and corner radius. |

## Public constructors

### Outline

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Outline()
```

Constructs an empty Outline. Call one of the setter methods to make the outline valid for use with a View.

### Outline

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Outline(src: Outline)
```

Constructs an Outline with a copy of the data in src.

| Parameters ||
|---|---|
| `src` | [Outline](Outline.md): This value cannot be `null`. |

## Public methods

### canClip

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun canClip(): Boolean
```

Returns whether the outline can be used to clip a View.

As of API 33, all Outline shapes support clipping. Prior to API 33, only Outlines that could be represented as a rectangle, circle, or round rect supported clipping.
**See Also**

- setClipToOutline

### getAlpha

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAlpha(): Float
```

Returns the alpha represented by the Outline.

### getRadius

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRadius(): Float
```

Returns the rounded rect radius, if set, or a value less than 0 if a path has been set via setPath. A return value of `0` indicates a non-rounded rect.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the rounded rect radius, or value \< 0 |

### getRect

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRect(outRect: Rect): Boolean
```

Populates `outBounds` with the outline bounds, if set, and returns `true`. If no outline bounds are set, or if a path has been set via setPath, returns `false`.

| Parameters ||
|---|---|
| `outRect` | [Rect](Rect.md): the rect to populate with the outline bounds, if set. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if `outBounds` was populated with outline bounds, or `false` if no outline bounds are set |

### isEmpty

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isEmpty(): Boolean
```

Returns whether the Outline is empty.

Outlines are empty when constructed, or if setEmpty is called, until a setter method is called
**See Also**

- setEmpty

### isOuterShadowOnly

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isOuterShadowOnly(): Boolean
```

Returns whether the shadow cast by this Outline is only drawn outside the outline.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the shadow is only drawn outside the outline boundary, false otherwise |

### offset

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun offset(
    dx: Int, 
    dy: Int
): Unit
```

Offsets the Outline by (dx,dy). Offsetting is cumulative, so additional calls to offset() will add to previous offset values. Offset only applies to the current geometry (setRect(), setPath(), etc.); setting new geometry resets any existing offset.

### set

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun set(src: Outline): Unit
```

Replace the contents of this Outline with the contents of src.

| Parameters ||
|---|---|
| `src` | [Outline](Outline.md): Source outline to copy from. This value cannot be `null`. |

### setAlpha

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setAlpha(alpha: Float): Unit
```

Sets the alpha represented by the Outline - the degree to which the producer is guaranteed to be opaque over the Outline's shape.

An alpha value of `0.0f` either represents completely transparent content, or content that isn't guaranteed to fill the shape it publishes.

Content producing a fully opaque (alpha = `1.0f`) outline is assumed by the drawing system to fully cover content beneath it, meaning content beneath may be optimized away.

| Parameters ||
|---|---|
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Value is between 0.0f and 1.0f inclusive |

### setConvexPath

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setConvexPath(convexPath: Path): Unit
```

**Deprecated:** *As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int`, the restriction that the path must be convex is removed. However, the API is misnamed until `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`, when setPath is introduced. Use setPath instead.*

Sets the Outline to a isConvex.

| Parameters ||
|---|---|
| `convexPath` | [Path](Path.md): used to construct the Outline. As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int`, it is no longer required to be convex. This value cannot be `null`. |

### setEmpty

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setEmpty(): Unit
```

Sets the outline to be empty.
**See Also**

- isEmpty

### setOuterShadowOnly

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setOuterShadowOnly(outerShadowOnly: Boolean): Unit
```

Sets whether the shadow cast by this Outline should only be drawn outside the outline.

If enabled, the shadow under the outline area will be clipped out, the default value is `false`.

| Parameters ||
|---|---|
| `outerShadowOnly` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether to draw the shadow only outside the outline boundary |

### setOval

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setOval(rect: Rect): Unit
```

Convenience for setOval

| Parameters ||
|---|---|
| `rect` | [Rect](Rect.md): This value cannot be `null`. |

### setOval

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setOval(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Unit
```

Sets the outline to the oval defined by input rect.

### setPath

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPath(path: Path): Unit
```

Sets the Outline to a Path.

| Parameters ||
|---|---|
| `path` | [Path](Path.md): used to construct the Outline. This value cannot be `null`. |

### setRect

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setRect(rect: Rect): Unit
```

Convenience for setRect

| Parameters ||
|---|---|
| `rect` | [Rect](Rect.md): This value cannot be `null`. |

### setRect

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setRect(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Unit
```

Sets the Outline to the rect defined by the input coordinates.

### setRoundRect

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setRoundRect(
    rect: Rect, 
    radius: Float
): Unit
```

Convenience for setRoundRect

| Parameters ||
|---|---|
| `rect` | [Rect](Rect.md): This value cannot be `null`. |

### setRoundRect

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setRoundRect(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int, 
    radius: Float
): Unit
```

Sets the Outline to the rounded rect defined by the input coordinates and corner radius.

Passing a zero radius is equivalent to calling setRect
