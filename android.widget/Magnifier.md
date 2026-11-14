# Magnifier

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Magnifier

Kotlin| [Java](https://developer.android.com/reference/android/widget/Magnifier "View this page in Java") 
| --- | --- |

```
class Magnifier
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.widget.Magnifier](https://developer.android.com/reference/kotlin/android/widget/Magnifier#) |

Android magnifier widget. Can be used by any view which is attached to a window.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/widget/Magnifier.Builder) Builder class for [Magnifier](https://developer.android.com/reference/kotlin/android/widget/Magnifier#) objects. |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_BOUND_MAX_IN_SURFACE](https://developer.android.com/reference/kotlin/android/widget/Magnifier#SOURCE_BOUND_MAX_IN_SURFACE:kotlin.Int) A source bound that will extend as much as possible, while remaining within the surface the content is copied from. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_BOUND_MAX_VISIBLE](https://developer.android.com/reference/kotlin/android/widget/Magnifier#SOURCE_BOUND_MAX_VISIBLE:kotlin.Int) A source bound that will extend as much as possible, while remaining within the visible region of the magnified view, as determined by [View.getGlobalVisibleRect(Rect)](https://developer.android.com/reference/kotlin/android/view/View.html#getGlobalVisibleRect(android.graphics.Rect)). |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Magnifier](https://developer.android.com/reference/kotlin/android/widget/Magnifier#Magnifier(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`)` Initializes a magnifier. |

| Public methods ||
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dismiss](https://developer.android.com/reference/kotlin/android/widget/Magnifier#dismiss())`()` Dismisses the magnifier from the screen. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getCornerRadius](https://developer.android.com/reference/kotlin/android/widget/Magnifier#getCornerRadius())`()` <br /> The units of this value are pixels. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDefaultHorizontalSourceToMagnifierOffset](https://developer.android.com/reference/kotlin/android/widget/Magnifier#getDefaultHorizontalSourceToMagnifierOffset())`()` Returns the horizontal offset, in pixels, to be applied to the source center position to obtain the magnifier center position when [show(float,float)](https://developer.android.com/reference/kotlin/android/widget/Magnifier#show(kotlin.Float,%20kotlin.Float))is called. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDefaultVerticalSourceToMagnifierOffset](https://developer.android.com/reference/kotlin/android/widget/Magnifier#getDefaultVerticalSourceToMagnifierOffset())`()` Returns the vertical offset, in pixels, to be applied to the source center position to obtain the magnifier center position when [show(float,float)](https://developer.android.com/reference/kotlin/android/widget/Magnifier#show(kotlin.Float,%20kotlin.Float))is called. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getElevation](https://developer.android.com/reference/kotlin/android/widget/Magnifier#getElevation())`()` <br /> The units of this value are pixels. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](https://developer.android.com/reference/kotlin/android/widget/Magnifier#getHeight())`()` <br /> The units of this value are pixels. |
| --- | --- |
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | [getOverlay](https://developer.android.com/reference/kotlin/android/widget/Magnifier#getOverlay())`()` Returns the overlay to be drawn on the top of the magnifier, or`null`if no overlay should be drawn. |
| [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#)? | [getPosition](https://developer.android.com/reference/kotlin/android/widget/Magnifier#getPosition())`()` Returns the top left coordinates of the magnifier, relative to the main application window. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSourceHeight](https://developer.android.com/reference/kotlin/android/widget/Magnifier#getSourceHeight())`()` <br /> The units of this value are pixels. |
| --- | --- |
| [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#)? | [getSourcePosition](https://developer.android.com/reference/kotlin/android/widget/Magnifier#getSourcePosition())`()` Returns the top left coordinates of the magnifier source (i.e. the view region going to be magnified and copied to the magnifier), relative to the window or surface the content is copied from. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSourceWidth](https://developer.android.com/reference/kotlin/android/widget/Magnifier#getSourceWidth())`()` <br /> The units of this value are pixels. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](https://developer.android.com/reference/kotlin/android/widget/Magnifier#getWidth())`()` <br /> The units of this value are pixels. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getZoom](https://developer.android.com/reference/kotlin/android/widget/Magnifier#getZoom())`()` Returns the zoom to be applied to the magnified view region copied to the magnifier. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClippingEnabled](https://developer.android.com/reference/kotlin/android/widget/Magnifier#isClippingEnabled())`()` Returns whether the magnifier position will be adjusted such that the magnifier will be fully within the bounds of the main application window, by also avoiding any overlap with system insets (such as the one corresponding to the status bar) i. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setZoom](https://developer.android.com/reference/kotlin/android/widget/Magnifier#setZoom(kotlin.Float))`(`zoom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the zoom to be applied to the chosen content before being copied to the magnifier popup. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [show](https://developer.android.com/reference/kotlin/android/widget/Magnifier#show(kotlin.Float,%20kotlin.Float))`(`sourceCenterX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `sourceCenterY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Shows the magnifier on the screen. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [show](https://developer.android.com/reference/kotlin/android/widget/Magnifier#show(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`sourceCenterX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `sourceCenterY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `magnifierCenterX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `magnifierCenterY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Shows the magnifier on the screen at a position that is independent from its content position. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](https://developer.android.com/reference/kotlin/android/widget/Magnifier#update())`()` Asks the magnifier to update its content. |
| --- | --- |

## Constants

### SOURCE_BOUND_MAX_IN_SURFACE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_BOUND_MAX_IN_SURFACE: Int
```

A source bound that will extend as much as possible, while remaining within the surface the content is copied from. 

 Value: 0

### SOURCE_BOUND_MAX_VISIBLE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_BOUND_MAX_VISIBLE: Int
```

A source bound that will extend as much as possible, while remaining within the visible region of the magnified view, as determined by [View.getGlobalVisibleRect(Rect)](https://developer.android.com/reference/kotlin/android/view/View.html#getGlobalVisibleRect(android.graphics.Rect)). 

 Value: 1

## Public constructors

### Magnifier

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Magnifier(view: View)
```

**Deprecated:** *Please use [Builder](https://developer.android.com/reference/kotlin/android/widget/Magnifier.Builder) instead*

Initializes a magnifier.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#):the view for which this magnifier is attached This value cannot be`null`. |

## Public methods

### dismiss

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun dismiss(): Unit
```

Dismisses the magnifier from the screen. Calling this on a dismissed magnifier is a no-op. 

### getCornerRadius

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCornerRadius(): Float
```

<br />

The units of this value are pixels.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the corner radius of the magnifier window, in pixels The units of this value are pixels. |

**See Also**

- [android.widget.Magnifier.Builder#setCornerRadius(float)](https://developer.android.com/reference/kotlin/android/widget/Magnifier.Builder#setCornerRadius(kotlin.Float)) 

### getDefaultHorizontalSourceToMagnifierOffset

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDefaultHorizontalSourceToMagnifierOffset(): Int
```

Returns the horizontal offset, in pixels, to be applied to the source center position to obtain the magnifier center position when [show(float,float)](https://developer.android.com/reference/kotlin/android/widget/Magnifier#show(kotlin.Float,%20kotlin.Float))is called. The value is ignored when [show(float,float,float,float)](https://developer.android.com/reference/kotlin/android/widget/Magnifier#show(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))is used instead. 
The units of this value are pixels.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the default horizontal offset between the source center and the magnifier The units of this value are pixels. |

**See Also**

- [android.widget.Magnifier.Builder#setDefaultSourceToMagnifierOffset(int, int)](https://developer.android.com/reference/kotlin/android/widget/Magnifier.Builder#setDefaultSourceToMagnifierOffset(kotlin.Int,%20kotlin.Int))
- [android.widget.Magnifier#show(float, float)](https://developer.android.com/reference/kotlin/android/widget/Magnifier#show(kotlin.Float,%20kotlin.Float)) 

### getDefaultVerticalSourceToMagnifierOffset

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDefaultVerticalSourceToMagnifierOffset(): Int
```

Returns the vertical offset, in pixels, to be applied to the source center position to obtain the magnifier center position when [show(float,float)](https://developer.android.com/reference/kotlin/android/widget/Magnifier#show(kotlin.Float,%20kotlin.Float))is called. The value is ignored when [show(float,float,float,float)](https://developer.android.com/reference/kotlin/android/widget/Magnifier#show(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))is used instead. 
The units of this value are pixels.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the default vertical offset between the source center and the magnifier The units of this value are pixels. |

**See Also**

- [android.widget.Magnifier.Builder#setDefaultSourceToMagnifierOffset(int, int)](https://developer.android.com/reference/kotlin/android/widget/Magnifier.Builder#setDefaultSourceToMagnifierOffset(kotlin.Int,%20kotlin.Int))
- [android.widget.Magnifier#show(float, float)](https://developer.android.com/reference/kotlin/android/widget/Magnifier#show(kotlin.Float,%20kotlin.Float)) 

### getElevation

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getElevation(): Float
```

<br />

The units of this value are pixels.

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the elevation set for the magnifier window, in pixels The units of this value are pixels. |

**See Also**

- [android.widget.Magnifier.Builder#setElevation(float)](https://developer.android.com/reference/kotlin/android/widget/Magnifier.Builder#setElevation(kotlin.Float)) 

### getHeight

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHeight(): Int
```

<br />

The units of this value are pixels.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the height of the magnifier window, in pixels The units of this value are pixels. |

**See Also**

- [android.widget.Magnifier.Builder#setSize(int, int)](https://developer.android.com/reference/kotlin/android/widget/Magnifier.Builder#setSize(kotlin.Int,%20kotlin.Int)) 

### getOverlay

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOverlay(): Drawable?
```

Returns the overlay to be drawn on the top of the magnifier, or`null`if no overlay should be drawn.

| Return ||
|------------------------------------------------------------------------------------------------------|-------------|
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | the overlay |

**See Also**

- [android.widget.Magnifier.Builder#setOverlay(Drawable)](https://developer.android.com/reference/kotlin/android/widget/Magnifier.Builder#setOverlay(android.graphics.drawable.Drawable)) 

### getPosition

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPosition(): Point?
```

Returns the top left coordinates of the magnifier, relative to the main application window. They will be determined by the coordinates of the last [show(float,float)](https://developer.android.com/reference/kotlin/android/widget/Magnifier#show(kotlin.Float,%20kotlin.Float))or [show(float,float,float,float)](https://developer.android.com/reference/kotlin/android/widget/Magnifier#show(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))call, adjusted to take into account any potential clamping behavior. The method can be used immediately after a #show call to find out where the magnifier will be positioned. However, the position of the magnifier will not be updated visually in the same frame, due to the async nature of the content copying and of the magnifier rendering. The method will return`null`if #show has not yet been called, or if the last operation performed was a #dismiss.

| Return ||
|---------------------------------------------------------------------------------------|-------------------------------------------|
| [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#)? | the top left coordinates of the magnifier |

### getSourceHeight

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSourceHeight(): Int
```

<br />

The units of this value are pixels.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the initial height of the content magnified and copied to the magnifier, in pixels The units of this value are pixels. |

**See Also**

- [android.widget.Magnifier.Builder#setSize(int, int)](https://developer.android.com/reference/kotlin/android/widget/Magnifier.Builder#setSize(kotlin.Int,%20kotlin.Int))
- [android.widget.Magnifier.Builder#setInitialZoom(float)](https://developer.android.com/reference/kotlin/android/widget/Magnifier.Builder#setInitialZoom(kotlin.Float)) 

### getSourcePosition

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSourcePosition(): Point?
```

Returns the top left coordinates of the magnifier source (i.e. the view region going to be magnified and copied to the magnifier), relative to the window or surface the content is copied from. The content will be copied: - if the magnified view is a [SurfaceView](https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#), from the surface backing it - otherwise, from the surface backing the main application window, and the coordinates returned will be relative to the main application window The method will return`null`if #show has not yet been called, or if the last operation performed was a #dismiss.

| Return ||
|---------------------------------------------------------------------------------------|--------------------------------------------------|
| [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#)? | the top left coordinates of the magnifier source |

### getSourceWidth

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSourceWidth(): Int
```

<br />

The units of this value are pixels.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the initial width of the content magnified and copied to the magnifier, in pixels The units of this value are pixels. |

**See Also**

- [android.widget.Magnifier.Builder#setSize(int, int)](https://developer.android.com/reference/kotlin/android/widget/Magnifier.Builder#setSize(kotlin.Int,%20kotlin.Int))
- [android.widget.Magnifier.Builder#setInitialZoom(float)](https://developer.android.com/reference/kotlin/android/widget/Magnifier.Builder#setInitialZoom(kotlin.Float)) 

### getWidth

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWidth(): Int
```

<br />

The units of this value are pixels.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the width of the magnifier window, in pixels The units of this value are pixels. |

**See Also**

- [android.widget.Magnifier.Builder#setSize(int, int)](https://developer.android.com/reference/kotlin/android/widget/Magnifier.Builder#setSize(kotlin.Int,%20kotlin.Int)) 

### getZoom

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getZoom(): Float
```

Returns the zoom to be applied to the magnified view region copied to the magnifier. If the zoom is x and the magnifier window size is (width, height), the original size of the content being magnified will be (width / x, height / x).

| Return ||
|--------------------------------------------------------------------------------|---------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the zoom applied to the content |

**See Also**

- [android.widget.Magnifier.Builder#setInitialZoom(float)](https://developer.android.com/reference/kotlin/android/widget/Magnifier.Builder#setInitialZoom(kotlin.Float)) 

### isClippingEnabled

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isClippingEnabled(): Boolean
```

Returns whether the magnifier position will be adjusted such that the magnifier will be fully within the bounds of the main application window, by also avoiding any overlap with system insets (such as the one corresponding to the status bar) i.e. whether the area where the magnifier can be positioned will be clipped to the main application window and the system insets.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the magnifier position will be adjusted |

**See Also**

- [android.widget.Magnifier.Builder#setClippingEnabled(boolean)](https://developer.android.com/reference/kotlin/android/widget/Magnifier.Builder#setClippingEnabled(kotlin.Boolean)) 

### setZoom

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setZoom(zoom: Float): Unit
```

Sets the zoom to be applied to the chosen content before being copied to the magnifier popup. The change will become effective at the next #show or #update call.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------|
| `zoom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the zoom to be set Value is 0.0f or greater |

### show

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun show(
    sourceCenterX: Float, 
    sourceCenterY: Float
): Unit
```

Shows the magnifier on the screen. The method takes the coordinates of the center of the content source going to be magnified and copied to the magnifier. The coordinates are relative to the top left corner of the magnified view. The magnifier will be positioned such that its center will be at the default offset from the center of the source. The default offset can be specified using the method [Builder.setDefaultSourceToMagnifierOffset(int, int)](https://developer.android.com/reference/kotlin/android/widget/Magnifier.Builder#setDefaultSourceToMagnifierOffset(kotlin.Int,%20kotlin.Int)). If the offset should be different across calls to this method, you should consider to use method [show(float,float,float,float)](https://developer.android.com/reference/kotlin/android/widget/Magnifier#show(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))instead.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sourceCenterX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):horizontal coordinate of the source center, relative to the view Value is 0.0f or greater |
| `sourceCenterY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):vertical coordinate of the source center, relative to the view Value is 0.0f or greater |

**See Also**

- [android.widget.Magnifier.Builder#setDefaultSourceToMagnifierOffset(int, int)](https://developer.android.com/reference/kotlin/android/widget/Magnifier.Builder#setDefaultSourceToMagnifierOffset(kotlin.Int,%20kotlin.Int))
- [android.widget.Magnifier.Builder#getDefaultHorizontalSourceToMagnifierOffset()](https://developer.android.com/reference/kotlin/android/widget/Magnifier#getDefaultHorizontalSourceToMagnifierOffset())
- [android.widget.Magnifier.Builder#getDefaultVerticalSourceToMagnifierOffset()](https://developer.android.com/reference/kotlin/android/widget/Magnifier#getDefaultVerticalSourceToMagnifierOffset())
- [#show(float, float, float, float)](https://developer.android.com/reference/kotlin/android/widget/Magnifier#show(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float)) 

### show

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun show(
    sourceCenterX: Float, 
    sourceCenterY: Float, 
    magnifierCenterX: Float, 
    magnifierCenterY: Float
): Unit
```

Shows the magnifier on the screen at a position that is independent from its content position. The first two arguments represent the coordinates of the center of the content source going to be magnified and copied to the magnifier. The last two arguments represent the coordinates of the center of the magnifier itself. All four coordinates are relative to the top left corner of the magnified view. If you consider using this method such that the offset between the source center and the magnifier center coordinates remains constant, you should consider using method [show(float,float)](https://developer.android.com/reference/kotlin/android/widget/Magnifier#show(kotlin.Float,%20kotlin.Float))instead.

| Parameters ||
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sourceCenterX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):horizontal coordinate of the source center relative to the view Value is 0.0f or greater |
| `sourceCenterY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):vertical coordinate of the source center, relative to the view Value is 0.0f or greater |
| `magnifierCenterX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):horizontal coordinate of the magnifier center, relative to the view |
| --- | --- |
| `magnifierCenterY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):vertical coordinate of the magnifier center, relative to the view |

### update

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun update(): Unit
```

Asks the magnifier to update its content. It uses the previous coordinates passed to [show(float,float)](https://developer.android.com/reference/kotlin/android/widget/Magnifier#show(kotlin.Float,%20kotlin.Float))or [show(float,float,float,float)](https://developer.android.com/reference/kotlin/android/widget/Magnifier#show(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float)). The method only has effect if the magnifier is currently showing.
