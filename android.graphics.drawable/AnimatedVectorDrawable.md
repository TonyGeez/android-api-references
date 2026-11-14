Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnimatedVectorDrawable

```
open class AnimatedVectorDrawable : Drawable, Animatable2
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.drawable.Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) ||
| | ↳ | [android.graphics.drawable.AnimatedVectorDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#) |

This class animates properties of a `https://developer.android.com/reference/kotlin/android/graphics/drawable/VectorDrawable` with animations defined using `https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator.html#` or `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet.html#`.

Starting from API 25, AnimatedVectorDrawable runs on RenderThread (as opposed to on UI thread for earlier APIs). This means animations in AnimatedVectorDrawable can remain smooth even when there is heavy workload on the UI thread. Note: If the UI thread is unresponsive, RenderThread may continue animating until the UI thread is capable of pushing another frame. Therefore, it is not possible to precisely coordinate a RenderThread-enabled AnimatedVectorDrawable with UI thread animations. Additionally, `https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable2.AnimationCallback#onAnimationEnd(android.graphics.drawable.Drawable)` will be called the frame after the AnimatedVectorDrawable finishes on the RenderThread.

AnimatedVectorDrawable can be defined in either [three separate XML files](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#ThreeXML), or [one XML](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#OneXML).

### Define an AnimatedVectorDrawable in three separate XML files

-

 #### XML for the VectorDrawable containing properties to be animated

 Animations can be performed on the animatable attributes in `https://developer.android.com/reference/kotlin/android/graphics/drawable/VectorDrawable`. These attributes will be animated by `https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator.html#`. The ObjectAnimator's target can be the root element, a group element or a path element. The targeted elements need to be named uniquely within the same VectorDrawable. Elements without animation do not need to be named.

 Here are all the animatable attributes in `https://developer.android.com/reference/kotlin/android/graphics/drawable/VectorDrawable`:

 | Element Name | Animatable attribute name |
 |---|---|
 | \<vector\> | alpha |
 | \<group\> | rotation |
 | \<group\> | pivotX |
| --- | --- |
 | \<group\> | pivotY |
 | \<group\> | scaleX |
 | \<group\> | scaleY |
| --- | --- |
 | \<group\> | translateX |
 | \<group\> | translateY |
 | \<path\> | pathData |
| --- | --- |
 | \<path\> | fillColor |
 | \<path\> | strokeColor |
 | \<path\> | strokeWidth |
| --- | --- |
 | \<path\> | strokeAlpha |
 | \<path\> | fillAlpha |
 | \<path\> | trimPathStart |
| --- | --- |
 | \<path\> | trimPathEnd |
 | \<path\> | trimPathOffset |
 | \<clip-path\> | pathData |
| --- | --- |

 <br />

 Below is an example of a VectorDrawable defined in vectordrawable.xml. This VectorDrawable is referred to by its file name (not including file suffix) in the [AnimatedVectorDrawable XML example](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#AVDExample).

  ```kotlin
  <vector xmlns:android="http://schemas.android.com/apk/res/android"
        android:height="64dp"
        android:width="64dp"
        android:viewportHeight="600"
        android:viewportWidth="600" >
        <group
            android:name="rotationGroup"
            android:pivotX="300.0"
            android:pivotY="300.0"
            android:rotation="45.0" >
            <path
                android:name="v"
                android:fillColor="#000000"
                android:pathData="M300,70 l 0,-70 70,70 0,0 -70,70z" />
        </group>
    </vector>
    
  ```
-

 #### XML for AnimatedVectorDrawable

 An AnimatedVectorDrawable element has a VectorDrawable attribute, and one or more target element(s). The target element can specify its target by android:name attribute, and link the target with the proper ObjectAnimator or AnimatorSet by android:animation attribute.
 The following code sample defines an AnimatedVectorDrawable. Note that the names refer to the groups and paths in the [VectorDrawable XML above](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#VDExample).

  ```kotlin
  <animated-vector xmlns:android="http://schemas.android.com/apk/res/android"
        android:drawable="@drawable/vectordrawable" >
        <target
            android:name="rotationGroup"
            android:animation="@animator/rotation" />
        <target
            android:name="v"
            android:animation="@animator/path_morph" />
    </animated-vector>
    
  ```
-

 #### XML for Animations defined using ObjectAnimator or AnimatorSet

 From the previous [example of AnimatedVectorDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#AVDExample), two animations were used: rotation.xml and path_morph.xml.
 rotation.xml rotates the target group from 0 degree to 360 degrees over 6000ms:

  ```kotlin
  <objectAnimator
        android:duration="6000"
        android:propertyName="rotation"
        android:valueFrom="0"
        android:valueTo="360" />
    
  ```
 path_morph.xml morphs the path from one shape into the other. Note that the paths must be compatible for morphing. Specifically, the paths must have the same commands, in the same order, and must have the same number of parameters for each command. It is recommended to store path strings as string resources for reuse.

  ```kotlin
  <set xmlns:android="http://schemas.android.com/apk/res/android">
        <objectAnimator
            android:duration="3000"
            android:propertyName="pathData"
            android:valueFrom="M300,70 l 0,-70 70,70 0,0 -70,70z"
            android:valueTo="M300,70 l 0,-70 70,0  0,140 -70,0 z"
            android:valueType="pathType"/>
    </set>
    
  ```

### Define an AnimatedVectorDrawable all in one XML file

Since the AAPT tool supports a new format that bundles several related XML files together, we can merge the XML files from the previous examples into one XML file:

```kotlin
<animated-vector xmlns:android="http://schemas.android.com/apk/res/android"
                   xmlns:aapt=&quothttp://schemas.android.com/aapt" >
      <aapt:attr name="android:drawable">
          <vector
              android:height="64dp"
              android:width="64dp"
              android:viewportHeight="600"
              android:viewportWidth="600" >
              <group
                  android:name="rotationGroup"
                  android:pivotX="300.0"
                  android:pivotY="300.0"
                  android:rotation="45.0" >
                  <path
                      android:name="v"
                      android:fillColor="#000000"
                      android:pathData="M300,70 l 0,-70 70,70 0,0 -70,70z" />
              </group>
          </vector>
      </aapt:attr>
 
      <target android:name="rotationGroup"> *
          <aapt:attr name="android:animation">
              <objectAnimator
              android:duration="6000"
              android:propertyName="rotation"
              android:valueFrom="0"
              android:valueTo="360" />
          </aapt:attr>
      </target>
 
      <target android:name="v" >
          <aapt:attr name="android:animation">
              <set>
                  <objectAnimator
                      android:duration="3000"
                      android:propertyName="pathData"
                      android:valueFrom="M300,70 l 0,-70 70,70 0,0 -70,70z"
                      android:valueTo="M300,70 l 0,-70 70,0  0,140 -70,0 z"
                      android:valueType="pathType"/>
              </set>
          </aapt:attr>
       </target>
  </animated-vector>
  
```

## Summary

| XML attributes ||
|---|---|
| [`android:animation`](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#attr_AnimatedVectorDrawable) | The animation for the target path, group or vector drawable. |
| [`android:drawable`](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#attr_AnimatedVectorDrawable) | The static vector drawable. |
| [`android:name`](https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#attr_AnimatedVectorDrawable) | The name of the target path, group or vector drawable. |
| --- | --- |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#AnimatedVectorDrawable()()` <br /> |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#applyTheme(android.content.res.Resources.Theme)(t: https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)` Applies the specified theme to this Drawable and its children. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#canApplyTheme()()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#clearAnimationCallbacks()()` Removes all existing animation callbacks. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#draw(android.graphics.Canvas)(canvas: https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)` Draws the AnimatedVectorDrawable into the given canvas. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#getAlpha()()` For API 25 and later, AnimatedVectorDrawable runs on RenderThread. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#getChangingConfigurations()()` Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. |
| --- | --- |
| open [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#)? | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#getColorFilter()()` Returns the current color filter, or `null` if none set. |
| open [Drawable.ConstantState](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState)? | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#getConstantState()()` Return a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState` instance that holds the shared state of this Drawable. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#getIntrinsicHeight()()` Returns the drawable's intrinsic height. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#getIntrinsicWidth()()` Returns the drawable's intrinsic width. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#getOpacity()()` Return the opacity/transparency of this Drawable. |
| open [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets.html#) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#getOpticalInsets()()` Return in insets the layout insets suggested by this Drawable for use with alignment operations during layout. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#getOutline(android.graphics.Outline)(outline: https://developer.android.com/reference/kotlin/android/graphics/Outline.html#)` Called to get the drawable to populate the Outline that defines its drawing area. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#inflate(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet,%20android.content.res.Resources.Theme)(res: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#, theme: https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#?)` Inflate this Drawable from an XML resource optionally styled by a theme. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#isRunning()()` Indicates whether the animation is running. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#isStateful()()` Indicates whether this drawable will change its appearance based on state. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#mutate()()` Make this drawable mutable. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#onLayoutDirectionChanged(kotlin.Int)(layoutDirection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Called when the drawable's resolved layout direction changes. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#registerAnimationCallback(android.graphics.drawable.Animatable2.AnimationCallback)(callback: https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable2.AnimationCallback)` Adds a callback to listen to the animation events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#reset()()` Resets the AnimatedVectorDrawable to the start state as specified in the animators. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#setAlpha(kotlin.Int)(alpha: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specify an alpha value for the drawable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#setColorFilter(android.graphics.ColorFilter)(colorFilter: https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#?)` Specify an optional color filter for the drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#setHotspot(kotlin.Float,%20kotlin.Float)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Specifies the hotspot's location within the drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#setHotspotBounds(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the bounds to which the hotspot is constrained, if they should be different from the drawable bounds. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#setTintBlendMode(android.graphics.BlendMode)(blendMode: https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#!)` Specifies a tint blending mode for this drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#setTintList(android.content.res.ColorStateList)(tint: https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#?)` Specifies tint color for this drawable as a color state list. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#setVisible(kotlin.Boolean,%20kotlin.Boolean)(visible: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, restart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set whether this Drawable is visible. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#start()()` Starts the drawable's animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#stop()()` Stops the drawable's animation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#unregisterAnimationCallback(android.graphics.drawable.Animatable2.AnimationCallback)(callback: https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable2.AnimationCallback)` Removes the specified animation callback. |
| --- | --- |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#onBoundsChange(android.graphics.Rect)(bounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)` Override this in your subclass to change appearance if you vary based on the bounds. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#onLevelChange(kotlin.Int)(level: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Override this in your subclass to change appearance if you vary based on level. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedVectorDrawable#onStateChange(kotlin.IntArray)(state: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)` Override this in your subclass to change appearance if you recognize the specified state. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#clearColorFilter()()` Removes the color filter for this drawable. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#copyBounds()()` Return a copy of the drawable's bounds in a new Rect. This returns the same values as getBounds(), but the returned object is guaranteed to not be changed later by the drawable (i.e. it retains no reference to this rect). If the caller already has a Rect allocated, call copyBounds(rect). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#copyBounds(android.graphics.Rect)(bounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)` Return a copy of the drawable's bounds in the specified Rect (allocated by the caller). The bounds specify where this will draw when its draw() method is called. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable?` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromPath(kotlin.String)(pathName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Create a drawable from file path name. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable?` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromResourceStream(android.content.res.Resources,%20android.util.TypedValue,%20java.io.InputStream,%20kotlin.String)(res: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#?, value: https://developer.android.com/reference/kotlin/android/util/TypedValue.html#?, is: https://developer.android.com/reference/kotlin/java/io/InputStream.html#?, srcName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable?` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromResourceStream(android.content.res.Resources,%20android.util.TypedValue,%20java.io.InputStream,%20kotlin.String,%20android.graphics.BitmapFactory.Options)(res: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#?, value: https://developer.android.com/reference/kotlin/android/util/TypedValue.html#?, is: https://developer.android.com/reference/kotlin/java/io/InputStream.html#?, srcName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?, opts: https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.Options.html#?)` Create a drawable from an inputstream, using the given resources and value to determine density information. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable?` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromStream(java.io.InputStream,%20kotlin.String)(is: https://developer.android.com/reference/kotlin/java/io/InputStream.html#?, srcName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Create a drawable from an inputstream <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXml(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)` Create a drawable from an XML document. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXml(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.content.res.Resources.Theme)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#, theme: https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#?)` Create a drawable from an XML document using an optional `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#`. For more information on how to create resources in XML, see [Drawable Resources](https://developer.android.com/guide/topics/resources/drawable-resource.html). <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXmlInner(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)` Create from inside an XML document. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns null if the tag is not a valid drawable. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#createFromXmlInner(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet,%20android.content.res.Resources.Theme)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#, theme: https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#?)` Create a drawable from inside an XML document using an optional `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#`. Called on a parser positioned at a tag in an XML document, tries to create a Drawable from that tag. Returns `null` if the tag is not a valid drawable. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getBounds()()` Return the drawable's bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed), so if a persistent copy of the bounds is needed, call copyBounds(rect) instead. You should also not change the object returned by this method as it may be the same object stored in the drawable. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback?` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getCallback()()` Return the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation attached to this Drawable. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getCurrent()()` <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getDirtyBounds()()` Return the drawable's dirty bounds Rect. Note: for efficiency, the returned object may be the same object stored in the drawable (though this is not guaranteed). By default, this returns the full drawable bounds. Custom drawables may override this method to perform more precise invalidation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getHotspotBounds(android.graphics.Rect)(outRect: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)` Populates `outRect` with the hotspot bounds. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getLayoutDirection()()` Returns the resolved layout direction for this Drawable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getLevel()()` Retrieve the current level. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getMinimumHeight()()` Returns the minimum height suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its height. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getMinimumWidth()()` Returns the minimum width suggested by this Drawable. If a View uses this Drawable as a background, it is suggested that the View use at least this value for its width. (There will be some scenarios where this will not be possible.) This value should INCLUDE any padding. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getPadding(android.graphics.Rect)(padding: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)` Return in padding the insets suggested by this Drawable for placing content inside the drawable's bounds. Positive values move toward the center of the Drawable (set Rect.inset). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getState()()` Describes the current state, as a union of primitive states, such as `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/R.attr.html#state_selected:kotlin.Int`, etc. Some drawables may modify their imagery based on the selected state. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/Region.html#?` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getTransparentRegion()()` Returns a Region representing the part of the Drawable that is completely transparent. This can be used to perform drawing operations, identifying which parts of the target will not change when rendering the Drawable. The default implementation returns null, indicating no transparent region; subclasses can optionally override this to return an actual Region if they want to supply this optimization information, but it is not required that they do so. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#hasFocusStateSpecified()()` Indicates whether this drawable has at least one state spec explicitly specifying `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int`. Note: A View uses a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` instance as its background and it changes its appearance based on a state. On keyboard devices, it should specify its `https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int` to make sure the user knows which view is holding the focus. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#inflate(android.content.res.Resources,%20org.xmlpull.v1.XmlPullParser,%20android.util.AttributeSet)(r: https://developer.android.com/reference/kotlin/android/content/res/Resources.html#, parser: https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)` Inflate this Drawable from an XML resource. Does not apply a theme. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf()()` Use the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation to have this Drawable redrawn. Does nothing if there is no Callback attached to the Drawable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isAutoMirrored()()` Tells if this Drawable will be automatically mirrored when its layout direction is RTL right-to-left. See `https://developer.android.com/reference/kotlin/android/util/LayoutDirection.html#`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isFilterBitmap()()` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isProjected()()` Whether this drawable requests projection. Indicates that the `https://developer.android.com/reference/kotlin/android/graphics/RenderNode.html#` this Drawable will draw into should be drawn immediately after the closest ancestor RenderNode containing a projection receiver. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#isVisible()()` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#jumpToCurrentState()()` If this Drawable does transition animations between states, ask that it immediately jump to the current state and skip any active animations. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#resolveOpacity(kotlin.Int,%20kotlin.Int)(op1: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, op2: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the appropriate opacity value for two source opacities. If either is UNKNOWN, that is returned; else, if either is TRANSLUCENT, that is returned; else, if either is TRANSPARENT, that is returned; else, OPAQUE is returned. This is to help in implementing `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#getOpacity()`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#scheduleSelf(java.lang.Runnable,%20kotlin.Long)(what: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#, when: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Use the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation to have this Drawable scheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setAutoMirrored(kotlin.Boolean)(mirrored: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set whether this Drawable is automatically mirrored when its layout direction is RTL (right-to left). See `https://developer.android.com/reference/kotlin/android/util/LayoutDirection.html#`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setBounds(android.graphics.Rect)(bounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)` Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setBounds(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specify a bounding rectangle for the Drawable. This is where the drawable will draw when its draw() method is called. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setCallback(android.graphics.drawable.Drawable.Callback)(cb: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback?)` Bind a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` object to this Drawable. Required for clients that want to support animated drawables. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setChangingConfigurations(kotlin.Int)(configs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)(color: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, mode: https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#)` Specify a color and Porter-Duff mode to be the color filter for this drawable. Convenience for `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)` which constructs a `https://developer.android.com/reference/kotlin/android/graphics/PorterDuffColorFilter.html#`. **Note:** Setting a color filter disables `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setDither(kotlin.Boolean)(dither: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set to true to have the drawable dither its colors when drawn to a device with fewer than 8-bits per color component. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setFilterBitmap(kotlin.Boolean)(filter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set to true to have the drawable filter its bitmaps with bilinear sampling when they are scaled or rotated. This can improve appearance when bitmaps are rotated. If the drawable does not use bitmaps, this call is ignored. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setLayoutDirection(kotlin.Int)(layoutDirection: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the layout direction for this drawable. Should be a resolved layout direction, as the Drawable has no capacity to do the resolution on its own. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setLevel(kotlin.Int)(level: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specify the level for the drawable. This allows a drawable to vary its imagery based on a continuous controller, for example to show progress or volume level. If the new level you are supplying causes the appearance of the Drawable to change, then it is responsible for calling `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf()` in order to have itself redrawn, *and* true will be returned from this function. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setState(kotlin.IntArray)(stateSet: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)` Specify a set of states for the drawable. These are use-case specific, so see the relevant documentation. As an example, the background for widgets like Button understand the following states: \[`https://developer.android.com/reference/kotlin/android/R.attr.html#state_focused:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/R.attr.html#state_pressed:kotlin.Int`\]. If the new state you are supplying causes the appearance of the Drawable to change, then it is responsible for calling `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#invalidateSelf()` in order to have itself redrawn, *and* true will be returned from this function. Note: The Drawable holds a reference on to stateSet until a new state array is given to it, so you must not modify this array during that time. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTint(kotlin.Int)(tintColor: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specifies tint color for this drawable. A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)`. To clear the tint, pass `null` to `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)`. **Note:** Setting a color filter via `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)` or `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)` overrides tint. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintMode(android.graphics.PorterDuff.Mode)(tintMode: https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#?)` Specifies a tint blending mode for this drawable. Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is `https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#`. **Note:** Setting a color filter via `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)` or `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)` overrides tint. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#unscheduleSelf(java.lang.Runnable)(what: https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)` Use the current `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.Callback` implementation to have this Drawable unscheduled. Does nothing if there is no Callback attached to the Drawable. <br /> | ||

## XML attributes

### android:animation

```
android:animation
```
The animation for the target path, group or vector drawable.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

### android:drawable

```
android:drawable
```
The static vector drawable.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

### android:name

```
android:name
```
The name of the target path, group or vector drawable.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character;

## Public constructors

### AnimatedVectorDrawable

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AnimatedVectorDrawable()
```

## Public methods

### applyTheme

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun applyTheme(t: Resources.Theme): Unit
```

Applies the specified theme to this Drawable and its children.

| Parameters ||
|---|---|
| `t` | [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#): the theme to apply. This value cannot be `null`. |

### canApplyTheme

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canApplyTheme(): Boolean
```

### clearAnimationCallbacks

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearAnimationCallbacks(): Unit
```

Removes all existing animation callbacks.

### draw

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun draw(canvas: Canvas): Unit
```

Draws the AnimatedVectorDrawable into the given canvas.

**Note:** Calling this method with a software canvas when the AnimatedVectorDrawable is being animated on RenderThread (for API 25 and later) may yield outdated result, as the UI thread is not guaranteed to be in sync with RenderThread on VectorDrawable's property changes during RenderThread animations.

| Parameters ||
|---|---|
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#): The canvas to draw into |

### getAlpha

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAlpha(): Int
```

For API 25 and later, AnimatedVectorDrawable runs on RenderThread. Therefore, when the root alpha is being animated, this getter does not guarantee to return an up-to-date alpha value.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the containing vector drawable's root alpha value. |

### getChangingConfigurations

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChangingConfigurations(): Int
```

Return a mask of the configuration parameters for which this drawable may change, requiring that it be re-created. The default implementation returns whatever was provided through `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setChangingConfigurations(kotlin.Int)` or 0 by default. Subclasses may extend this to or in the changing configurations of any other drawables they hold.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MCC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MNC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LOCALE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_TOUCHSCREEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD_HIDDEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_NAVIGATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ORIENTATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_LAYOUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_UI_MODE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_SIZE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SMALLEST_SCREEN_SIZE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_DENSITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LAYOUT_DIRECTION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_COLOR_MODE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_SCALE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_GRAMMATICAL_GENDER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_WEIGHT_ADJUSTMENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ASSETS_PATHS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_RESOURCES_UNUSED:kotlin.Int` |

### getColorFilter

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getColorFilter(): ColorFilter?
```

Returns the current color filter, or `null` if none set.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#?` | the current color filter, or `null` if none set |

### getConstantState

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getConstantState(): Drawable.ConstantState?
```

Return a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState` instance that holds the shared state of this Drawable.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.ConstantState?` | The ConstantState associated to that Drawable. This value may be `null`. |

### getIntrinsicHeight

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIntrinsicHeight(): Int
```

Returns the drawable's intrinsic height.

Intrinsic height is the height at which the drawable would like to be laid out, including any inherent padding. If the drawable has no intrinsic height, such as a solid color, this method returns -1.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the intrinsic height, or -1 if no intrinsic height |

### getIntrinsicWidth

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIntrinsicWidth(): Int
```

Returns the drawable's intrinsic width.

Intrinsic width is the width at which the drawable would like to be laid out, including any inherent padding. If the drawable has no intrinsic width, such as a solid color, this method returns -1.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the intrinsic width, or -1 if no intrinsic width |

### getOpacity

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOpacity(): Int
```

Return the opacity/transparency of this Drawable. The returned value is one of the abstract format constants in `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#`: `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#UNKNOWN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSLUCENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSPARENT:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#OPAQUE:kotlin.Int`.

An OPAQUE drawable is one that draws all all content within its bounds, completely covering anything behind the drawable. A TRANSPARENT drawable is one that draws nothing within its bounds, allowing everything behind it to show through. A TRANSLUCENT drawable is a drawable in any other state, where the drawable will draw some, but not all, of the content within its bounds and at least some content behind the drawable will be visible. If the visibility of the drawable's contents cannot be determined, the safest/best return value is TRANSLUCENT.

Generally a Drawable should be as conservative as possible with the value it returns. For example, if it contains multiple child drawables and only shows one of them at a time, if only one of the children is TRANSLUCENT and the others are OPAQUE then TRANSLUCENT should be returned. You can use the method `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#resolveOpacity(kotlin.Int,%20kotlin.Int)` to perform a standard reduction of two opacities to the appropriate single output.

Note that the returned value does not necessarily take into account a custom alpha or color filter that has been applied by the client through the `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setAlpha(kotlin.Int)` or #setColorFilter methods. Some subclasses, such as `https://developer.android.com/reference/kotlin/android/graphics/drawable/BitmapDrawable`, `https://developer.android.com/reference/kotlin/android/graphics/drawable/ColorDrawable`, and `https://developer.android.com/reference/kotlin/android/graphics/drawable/GradientDrawable`, do account for the value of `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setAlpha(kotlin.Int)`, but the general behavior is dependent upon the implementation of the subclass.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | int The opacity class of the Drawable. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSLUCENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#TRANSPARENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#OPAQUE:kotlin.Int` |

### getOpticalInsets

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOpticalInsets(): Insets
```

Return in insets the layout insets suggested by this Drawable for use with alignment operations during layout.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Insets.html#` | This value cannot be `null`. |

### getOutline

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOutline(outline: Outline): Unit
```

Called to get the drawable to populate the Outline that defines its drawing area.

This method is called by the default `https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider.html#` to define the outline of the View.

The default behavior defines the outline to be the bounding rectangle of 0 alpha. Subclasses that wish to convey a different shape or alpha value must override this method.

| Parameters ||
|---|---|
| `outline` | [Outline](https://developer.android.com/reference/kotlin/android/graphics/Outline.html#): This value cannot be `null`. |

### inflate

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun inflate(
    res: Resources, 
    parser: XmlPullParser, 
    attrs: AttributeSet, 
    theme: Resources.Theme?
): Unit
```

Inflate this Drawable from an XML resource optionally styled by a theme. This can't be called more than once for each Drawable. Note that framework may have called this once to create the Drawable instance from XML resource.

| Parameters ||
|---|---|
| `r` | Resources used to resolve attribute values. This value cannot be `null`. |
| `parser` | [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#): XML parser from which to inflate this Drawable. This value cannot be `null`. |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#): Base set of attribute values. This value cannot be `null`. |
| --- | --- |
| `theme` | [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?: Theme to apply, may be null |

| Exceptions ||
|---|---|
| `java.io.IOException` | |
| `org.xmlpull.v1.XmlPullParserException` | |

### isRunning

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isRunning(): Boolean
```

Indicates whether the animation is running.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the animation is running, false otherwise. |

### isStateful

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isStateful(): Boolean
```

Indicates whether this drawable will change its appearance based on state. Clients can use this to determine whether it is necessary to calculate their state and call setState.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this drawable changes its appearance based on state, false otherwise. |

### mutate

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun mutate(): Drawable
```

Make this drawable mutable. This operation cannot be reversed. A mutable drawable is guaranteed to not share its state with any other drawable. This is especially useful when you need to modify properties of drawables loaded from resources. By default, all drawables instances loaded from the same resource share a common state; if you modify the state of one instance, all the other instances will receive the same modification. Calling this method on a mutable Drawable will have no effect.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable` | This drawable. This value cannot be `null`. |

### onLayoutDirectionChanged

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onLayoutDirectionChanged(layoutDirection: Int): Boolean
```

Called when the drawable's resolved layout direction changes.

| Parameters ||
|---|---|
| `layoutDirection` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_LTR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/View.html#LAYOUT_DIRECTION_RTL:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the layout direction change has caused the appearance of the drawable to change such that it needs to be re-drawn, `false` otherwise |

### registerAnimationCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerAnimationCallback(callback: Animatable2.AnimationCallback): Unit
```

Adds a callback to listen to the animation events.

| Parameters ||
|---|---|
| `callback` | [Animatable2.AnimationCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable2.AnimationCallback): This value cannot be `null`. |

### reset

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reset(): Unit
```

Resets the AnimatedVectorDrawable to the start state as specified in the animators.

### setAlpha

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAlpha(alpha: Int): Unit
```

Specify an alpha value for the drawable. 0 means fully transparent, and 255 means fully opaque.

| Parameters ||
|---|---|
| `alpha` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is between 0 and 255 inclusive |

### setColorFilter

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setColorFilter(colorFilter: ColorFilter?): Unit
```

Specify an optional color filter for the drawable.

If a Drawable has a ColorFilter, each output pixel of the Drawable's drawing contents will be modified by the color filter before it is blended onto the render target of a Canvas.

Pass `null` to remove any existing color filter.

**Note:** Setting a non-`null` color filter disables `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)`.

| Parameters ||
|---|---|
| `colorFilter` | [ColorFilter](https://developer.android.com/reference/kotlin/android/graphics/ColorFilter.html#)?: The color filter to apply, or `null` to remove the existing color filter |

### setHotspot

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHotspot(
    x: Float, 
    y: Float
): Unit
```

Specifies the hotspot's location within the drawable.

| Parameters ||
|---|---|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The X coordinate of the center of the hotspot |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The Y coordinate of the center of the hotspot |

### setHotspotBounds

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHotspotBounds(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Unit
```

Sets the bounds to which the hotspot is constrained, if they should be different from the drawable bounds.

| Parameters ||
|---|---|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): position in pixels of the left bound |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): position in pixels of the top bound |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): position in pixels of the right bound |
| --- | --- |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): position in pixels of the bottom bound |

### setTintBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTintBlendMode(blendMode: BlendMode!): Unit
```

Specifies a tint blending mode for this drawable.

Defines how this drawable's tint color should be blended into the drawable before it is drawn to screen. Default tint mode is `https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#`.

**Note:** Setting a color filter via `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)`

| Parameters ||
|---|---|
| `blendMode` | [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#)!: This value cannot be `null`. |

### setTintList

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTintList(tint: ColorStateList?): Unit
```

Specifies tint color for this drawable as a color state list.

A Drawable's drawing content will be blended together with its tint before it is drawn to the screen. This functions similarly to `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)`.

**Note:** Setting a color filter via `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(android.graphics.ColorFilter)` or `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setColorFilter(kotlin.Int,%20android.graphics.PorterDuff.Mode)` overrides tint.

| Parameters ||
|---|---|
| `tint` | [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)?: Color state list to use for tinting this drawable, or `null` to clear the tint |

### setVisible

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setVisible(
    visible: Boolean, 
    restart: Boolean
): Boolean
```

Set whether this Drawable is visible. This generally does not impact the Drawable's behavior, but is a hint that can be used by some Drawables, for example, to decide whether run animations.

| Parameters ||
|---|---|
| `visible` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Set to true if visible, false if not. |
| `restart` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): You can supply true here to force the drawable to behave as if it has just become visible, even if it had last been set visible. Used for example to force animations to restart. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | boolean Returns true if the new visibility is different than its previous state. |

### start

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun start(): Unit
```

Starts the drawable's animation.

### stop

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun stop(): Unit
```

Stops the drawable's animation.

### unregisterAnimationCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterAnimationCallback(callback: Animatable2.AnimationCallback): Boolean
```

Removes the specified animation callback.

| Parameters ||
|---|---|
| `callback` | [Animatable2.AnimationCallback](https://developer.android.com/reference/kotlin/android/graphics/drawable/Animatable2.AnimationCallback): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `false` if callback didn't exist in the call back list, or `true` if callback has been removed successfully. |

## Protected methods

### onBoundsChange

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onBoundsChange(bounds: Rect): Unit
```

Override this in your subclass to change appearance if you vary based on the bounds.

| Parameters ||
|---|---|
| `bounds` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#): This value cannot be `null`. |

### onLevelChange

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onLevelChange(level: Int): Boolean
```

Override this in your subclass to change appearance if you vary based on level.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the level change has caused the appearance of the Drawable to change (that is, it needs to be drawn), else false if it looks the same and there is no need to redraw it since its last level. |

### onStateChange

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onStateChange(state: IntArray): Boolean
```

Override this in your subclass to change appearance if you recognize the specified state.

| Parameters ||
|---|---|
| `state` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the state change has caused the appearance of the Drawable to change (that is, it needs to be drawn), else false if it looks the same and there is no need to redraw it since its last state. |
