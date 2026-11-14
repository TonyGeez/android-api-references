# android.graphics.drawable

# android.graphics.drawable

Kotlin| [Java](https://developer.android.com/reference/android/graphics/drawable/package-summary "View this page in Java")

## Interfaces

| [Animatable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable) | Interface that drawables supporting animations should implement. |
| [Animatable2](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable2) | Abstract class that drawables supporting animations and callbacks should extend. |
| [Callback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback) | Implement this interface if you want to create an animated drawable that extends [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable). |
| [OnDrawableLoadedListener](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.OnDrawableLoadedListener) | Implement this interface to receive a callback when [loadDrawableAsync](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#loadDrawableAsync(android.content.Context,%20android.graphics.drawable.Icon.OnDrawableLoadedListener,%20android.os.Handler))is finished and your Drawable is ready. |

## Classes

| [AdaptiveIconDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AdaptiveIconDrawable) | This class can also be created via XML inflation using`<adaptive-icon>`tag in addition to dynamic creation. |
| [AnimatedImageDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable) | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) for drawing animated images (like GIF). |
| [AnimatedStateListDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedStateListDrawable) | Drawable containing a set of Drawable keyframes where the currently displayed keyframe is chosen based on the current state set. |
| [AnimatedVectorDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable) | This class animates properties of a [android.graphics.drawable.VectorDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/VectorDrawable) with animations defined using [android.animation.ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator.html#) or [android.animation.AnimatorSet](https://developer.android.com/reference/kotlin/android/animation/AnimatorSet.html#). |
| [AnimationDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimationDrawable) | An object used to create frame-by-frame animations, defined by a series of Drawable objects, which can be used as a View object's background. |
| [BitmapDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/BitmapDrawable) | A Drawable that wraps a bitmap and can be tiled, stretched, or aligned. |
| [ClipDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ClipDrawable) | A Drawable that clips another Drawable based on this Drawable's current level value. |
| [ColorDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorDrawable) | A specialized Drawable that fills the Canvas with a specified color. |
| [ColorStateListDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorStateListDrawable) | A Drawable that manages a [ColorDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorDrawable) to make it stateful and backed by a [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#). |
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | A Drawable is a general abstraction for "something that can be drawn. |
| [DrawableContainer](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableContainer) | A helper class that contains several [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) s and selects which one to use. |
| [DrawableWrapper](https://developer.android.com/reference/kotlin/android/graphics/drawable/DrawableWrapper) | Drawable container with only one child element. |
| [GradientDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable) | A Drawable with a color gradient for buttons, backgrounds, etc. |
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon) | An umbrella container for several serializable graphics representations, including Bitmaps, compressed bitmap images (e.g. JPG or PNG), and drawable resources (including vectors). |
| [InsetDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/InsetDrawable) | A Drawable that insets another Drawable by a specified distance or fraction of the content bounds. |
| [LayerDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/LayerDrawable) | A Drawable that manages an array of other Drawables. |
| [LevelListDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/LevelListDrawable) | A resource that manages a number of alternate Drawables, each assigned a maximum numerical value. |
| [NinePatchDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/NinePatchDrawable) | A resizeable bitmap, with stretchable areas that you define. |
| [PaintDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/PaintDrawable) | Drawable that draws its bounds in the given paint, with optional rounded corners. |
| [PictureDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/PictureDrawable) | Drawable subclass that wraps a Picture, allowing the picture to be used wherever a Drawable is supported. |
| [RippleDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/RippleDrawable) | Drawable that shows a ripple effect in response to state changes. |
| [RotateDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/RotateDrawable) | A Drawable that can rotate another Drawable based on the current level value. |
| [ScaleDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ScaleDrawable) | A Drawable that changes the size of another Drawable based on its current level value. |
| [ShapeDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/ShapeDrawable) | A Drawable object that draws primitive shapes. |
| [StateListDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/StateListDrawable) | Lets you assign a number of graphic images to a single Drawable and swap out the visible item by a string ID value. |
| [TransitionDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/TransitionDrawable) | An extension of LayerDrawables that is intended to cross-fade between the first and second layer. |
| [VectorDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/VectorDrawable) | This lets you create a drawable based on an XML vector graphic. |
