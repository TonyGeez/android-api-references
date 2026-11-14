# android.graphics.drawable

# android.graphics.drawable

Kotlin| [Java](../android/graphics/drawable/_package.md)
| --- | --- |

## Interfaces

| [Animatable](../android/graphics/drawable/Animatable.md) | Interface that drawables supporting animations should implement. |
| --- | --- |
| [Animatable2](../android/graphics/drawable/Animatable2.md) | Abstract class that drawables supporting animations and callbacks should extend. |
| [Callback](../android/graphics/drawable/Drawable.Callback.md) | Implement this interface if you want to create an animated drawable that extends [Drawable](../android/graphics/drawable/Drawable.md). |
| [OnDrawableLoadedListener](../android/graphics/drawable/Icon.OnDrawableLoadedListener.md) | Implement this interface to receive a callback when [loadDrawableAsync](../android/graphics/drawable/Icon.md))is finished and your Drawable is ready. |
| --- | --- |

## Classes

| [AdaptiveIconDrawable](../android/graphics/drawable/AdaptiveIconDrawable.md) | This class can also be created via XML inflation using`<adaptive-icon>`tag in addition to dynamic creation. |
| --- | --- |
| [AnimatedImageDrawable](../android/graphics/drawable/AnimatedImageDrawable.md) | [Drawable](../android/graphics/drawable/Drawable.md) for drawing animated images (like GIF). |
| [AnimatedStateListDrawable](../android/graphics/drawable/AnimatedStateListDrawable.md) | Drawable containing a set of Drawable keyframes where the currently displayed keyframe is chosen based on the current state set. |
| [AnimatedVectorDrawable](../android/graphics/drawable/AnimatedVectorDrawable.md) | This class animates properties of a [android.graphics.drawable.VectorDrawable](../android/graphics/drawable/VectorDrawable.md) with animations defined using [android.animation.ObjectAnimator](../android/animation/ObjectAnimator.md) or [android.animation.AnimatorSet](../android/animation/AnimatorSet.md). |
| --- | --- |
| [AnimationDrawable](../android/graphics/drawable/AnimationDrawable.md) | An object used to create frame-by-frame animations, defined by a series of Drawable objects, which can be used as a View object's background. |
| [BitmapDrawable](../android/graphics/drawable/BitmapDrawable.md) | A Drawable that wraps a bitmap and can be tiled, stretched, or aligned. |
| [ClipDrawable](../android/graphics/drawable/ClipDrawable.md) | A Drawable that clips another Drawable based on this Drawable's current level value. |
| --- | --- |
| [ColorDrawable](../android/graphics/drawable/ColorDrawable.md) | A specialized Drawable that fills the Canvas with a specified color. |
| [ColorStateListDrawable](../android/graphics/drawable/ColorStateListDrawable.md) | A Drawable that manages a [ColorDrawable](../android/graphics/drawable/ColorDrawable.md) to make it stateful and backed by a [ColorStateList](../android/content/res/ColorStateList.md). |
| [Drawable](../android/graphics/drawable/Drawable.md) | A Drawable is a general abstraction for "something that can be drawn. |
| --- | --- |
| [DrawableContainer](../android/graphics/drawable/DrawableContainer.md) | A helper class that contains several [Drawable](../android/graphics/drawable/Drawable.md) s and selects which one to use. |
| [DrawableWrapper](../android/graphics/drawable/DrawableWrapper.md) | Drawable container with only one child element. |
| [GradientDrawable](../android/graphics/drawable/GradientDrawable.md) | A Drawable with a color gradient for buttons, backgrounds, etc. |
| --- | --- |
| [Icon](../android/graphics/drawable/Icon.md) | An umbrella container for several serializable graphics representations, including Bitmaps, compressed bitmap images (e.g. JPG or PNG), and drawable resources (including vectors). |
| [InsetDrawable](../android/graphics/drawable/InsetDrawable.md) | A Drawable that insets another Drawable by a specified distance or fraction of the content bounds. |
| [LayerDrawable](../android/graphics/drawable/LayerDrawable.md) | A Drawable that manages an array of other Drawables. |
| --- | --- |
| [LevelListDrawable](../android/graphics/drawable/LevelListDrawable.md) | A resource that manages a number of alternate Drawables, each assigned a maximum numerical value. |
| [NinePatchDrawable](../android/graphics/drawable/NinePatchDrawable.md) | A resizeable bitmap, with stretchable areas that you define. |
| [PaintDrawable](../android/graphics/drawable/PaintDrawable.md) | Drawable that draws its bounds in the given paint, with optional rounded corners. |
| --- | --- |
| [PictureDrawable](../android/graphics/drawable/PictureDrawable.md) | Drawable subclass that wraps a Picture, allowing the picture to be used wherever a Drawable is supported. |
| [RippleDrawable](../android/graphics/drawable/RippleDrawable.md) | Drawable that shows a ripple effect in response to state changes. |
| [RotateDrawable](../android/graphics/drawable/RotateDrawable.md) | A Drawable that can rotate another Drawable based on the current level value. |
| --- | --- |
| [ScaleDrawable](../android/graphics/drawable/ScaleDrawable.md) | A Drawable that changes the size of another Drawable based on its current level value. |
| [ShapeDrawable](../android/graphics/drawable/ShapeDrawable.md) | A Drawable object that draws primitive shapes. |
| [StateListDrawable](../android/graphics/drawable/StateListDrawable.md) | Lets you assign a number of graphic images to a single Drawable and swap out the visible item by a string ID value. |
| --- | --- |
| [TransitionDrawable](../android/graphics/drawable/TransitionDrawable.md) | An extension of LayerDrawables that is intended to cross-fade between the first and second layer. |
| [VectorDrawable](../android/graphics/drawable/VectorDrawable.md) | This lets you create a drawable based on an XML vector graphic. |
