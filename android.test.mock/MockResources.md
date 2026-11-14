# MockResources

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MockResources

Kotlin| [Java](https://developer.android.com/reference/android/test/mock/MockResources "View this page in Java") 
| --- | --- |

```
open class MockResources : Resources
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.content.res.Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#) ||
| | ↳ | [android.test.mock.MockResources](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#) |

| **This class was deprecated in API level 24.**
|
| Use a mocking framework like [Mockito](https://github.com/mockito/mockito). New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

A mock [android.content.res.Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#) class. All methods are non-functional and throw [java.lang.UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#). Override it to provide the operations that you need.

## Summary

| Inherited constants ||
|---|---|
| From class [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ID_NULL](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#ID_NULL:kotlin.Int) <br /> The`null`resource ID. This denotes an invalid resource ID that is returned by the system when a resource is not found or the value is set to`@null`in XML. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------|---|
| [MockResources](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#MockResources())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [XmlResourceParser](https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser.html#) | [getAnimation](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getAnimation(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColor](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getColor(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#) | [getColorStateList](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getColorStateList(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)! | [getConfiguration](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getConfiguration())`()` <br /> |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDimension](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getDimension(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDimensionPixelOffset](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getDimensionPixelOffset(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDimensionPixelSize](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getDimensionPixelSize(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#)! | [getDisplayMetrics](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getDisplayMetrics())`()` <br /> |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)! | [getDrawable](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getDrawable(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIdentifier](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getIdentifier(kotlin.String,%20kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `defType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `defPackage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getIntArray](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getIntArray(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInteger](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getInteger(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [XmlResourceParser](https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser.html#) | [getLayout](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getLayout(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Movie](https://developer.android.com/reference/kotlin/android/graphics/Movie.html#)! | [getMovie](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getMovie(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getQuantityString](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getQuantityString(kotlin.Int,%20kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `quantity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getQuantityString](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getQuantityString(kotlin.Int,%20kotlin.Int,%20kotlin.Any))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `quantity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `vararg` `formatArgs:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getQuantityText](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getQuantityText(kotlin.Int,%20kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `quantity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getResourceEntryName](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getResourceEntryName(kotlin.Int))`(`resid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getResourceName](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getResourceName(kotlin.Int))`(`resid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getResourcePackageName](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getResourcePackageName(kotlin.Int))`(`resid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getResourceTypeName](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getResourceTypeName(kotlin.Int))`(`resid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getString](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getString(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getString](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getString(kotlin.Int,%20kotlin.Any))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `vararg` `formatArgs:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getStringArray](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getStringArray(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getText](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getText(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getText](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getText(kotlin.Int,%20kotlin.CharSequence))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `def:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\> | [getTextArray](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getTextArray(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getValue](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getValue(kotlin.Int,%20android.util.TypedValue,%20kotlin.Boolean))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `outValue:` ` [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#)!`, `resolveRefs:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getValue](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getValue(kotlin.String,%20android.util.TypedValue,%20kotlin.Boolean))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `outValue:` ` [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#)!`, `resolveRefs:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [XmlResourceParser](https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser.html#) | [getXml](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#getXml(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [TypedArray](https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#)! | [obtainAttributes](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#obtainAttributes(android.util.AttributeSet,%20kotlin.IntArray))`(`set:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`, `attrs:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` <br /> |
| open [TypedArray](https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#) | [obtainTypedArray](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#obtainTypedArray(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#) | [openRawResource](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#openRawResource(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#)! | [openRawResourceFd](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#openRawResourceFd(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateConfiguration](https://developer.android.com/reference/kotlin/android/test/mock/MockResources#updateConfiguration(android.content.res.Configuration,%20android.util.DisplayMetrics))`(`config:` ` [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)!`, `metrics:` ` [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#) |--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addLoaders](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#addLoaders(android.content.res.loader.ResourcesLoader))`(`vararg` `loaders:` ` [ResourcesLoader](https://developer.android.com/reference/kotlin/android/content/res/loader/ResourcesLoader.html#)!`)` <br /> Adds a loader to the list of loaders. If the loader is already present in the list, the list will not be modified. This should only be called from the UI thread to avoid lock contention when propagating loader changes. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finishPreloading](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#finishPreloading())`()` <br /> Called by zygote when it is done preloading resources, to change back to normal Resources operation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flushLayoutCache](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#flushLayoutCache())`()` <br /> Call this to remove all cached loaded layout resources from the Resources object. Only intended for use with performance testing tools. <br /> | | [AssetManager](https://developer.android.com/reference/kotlin/android/content/res/AssetManager.html#)! | [getAssets](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#getAssets())`()` <br /> Retrieve underlying AssetManager storage for these resources. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAttributeSetSourceResId](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#getAttributeSetSourceResId(android.util.AttributeSet))`(`set:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)?`)` <br /> Returns the resource ID of the resource that was used to create this AttributeSet. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBoolean](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#getBoolean(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return a boolean associated with a particular resource ID. This can be used with any integral resource value, and will return true if it is non-zero. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColor](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#getColor(kotlin.Int,%20android.content.res.Resources.Theme))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` <br /> Returns a themed color integer associated with a particular resource ID. If the resource holds a complex [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#), then the default color from the set is returned. <br /> | | [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#) | [getColorStateList](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#getColorStateList(kotlin.Int,%20android.content.res.Resources.Theme))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` <br /> Returns a themed color state list associated with a particular resource ID. The resource may contain either a single raw color value or a complex [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#) holding multiple possible colors. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)! | [getDrawable](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#getDrawable(kotlin.Int,%20android.content.res.Resources.Theme))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` <br /> Return a drawable object associated with a particular resource ID and styled for the specified theme. Various types of objects will be returned depending on the underlying resource -- for example, a solid color, PNG image, scalable image, etc. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | [getDrawableForDensity](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#getDrawableForDensity(kotlin.Int,%20kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `density:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return a drawable object associated with a particular resource ID for the given screen density in DPI. This will set the drawable's density to be the device's density multiplied by the ratio of actual drawable density to requested density. This allows the drawable to be scaled up to the correct size if needed. Various types of objects will be returned depending on the underlying resource -- for example, a solid color, PNG image, scalable image, etc. The Drawable API hides these implementation details. **Note:** To obtain a themed drawable, use [Context.getDrawable(int)](https://developer.android.com/reference/kotlin/android/content/Context.html#getDrawable(kotlin.Int))or [getDrawableForDensity(int,int,android.content.res.Resources.Theme)](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#getDrawableForDensity(kotlin.Int,%20kotlin.Int,%20android.content.res.Resources.Theme))passing the desired theme. <br /> | | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | [getDrawableForDensity](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#getDrawableForDensity(kotlin.Int,%20kotlin.Int,%20android.content.res.Resources.Theme))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `density:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `theme:` ` [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)?`)` <br /> Return a drawable object associated with a particular resource ID for the given screen density in DPI and styled for the specified theme. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#getFloat(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieve a floating-point value for a particular resource ID. <br /> | | [Typeface](https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#) | [getFont](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#getFont(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return the Typeface value associated with a particular resource ID. {@more} <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFraction](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#getFraction(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `base:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pbase:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieve a fractional unit for a particular resource ID. <br /> | | [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#)! | [getSystem](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#getSystem())`()` <br /> Return a global shared Resources object that provides access to only system resources (no application resources), is not configured for the current screen (can not use dimension units, does not change based on orientation, etc), and is not affected by Runtime Resource Overlay. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getValueForDensity](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#getValueForDensity(kotlin.Int,%20kotlin.Int,%20android.util.TypedValue,%20kotlin.Boolean))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `density:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `outValue:` ` [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#)!`, `resolveRefs:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Get the raw value associated with a resource with associated density. <br /> | | [Resources.Theme](https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme.html#)! | [newTheme](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#newTheme())`()` <br /> Generate a new Theme object for this set of Resources. It initially starts out empty. <br /> | | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#) | [openRawResource](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#openRawResource(kotlin.Int,%20android.util.TypedValue))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#)!`)` <br /> Open a data stream for reading a raw resource. This can only be used with resources whose value is the name of an asset file -- that is, it can be used to open drawable, sound, and raw resources; it will fail on string and color resources. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parseBundleExtra](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#parseBundleExtra(kotlin.String,%20android.util.AttributeSet,%20android.os.Bundle))`(`tagName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`, `outBundle:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` <br /> Parse a name/value pair out of an XML tag holding that data. The AttributeSet must be holding the data defined by [android.R.styleable#Extra](https://developer.android.com/reference/kotlin/android/R.styleable.html#Extra:kotlin.IntArray). The following value types are supported: - [TypedValue.TYPE_STRING](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#TYPE_STRING:kotlin.Int): [Bundle.putCharSequence()](https://developer.android.com/reference/kotlin/android/os/Bundle.html#putCharSequence(kotlin.String,%20kotlin.CharSequence)) - [TypedValue.TYPE_INT_BOOLEAN](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#TYPE_INT_BOOLEAN:kotlin.Int): [Bundle.putBoolean()](https://developer.android.com/reference/kotlin/android/os/Bundle.html#putCharSequence(kotlin.String,%20kotlin.CharSequence)) - [TypedValue.TYPE_FIRST_INT](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#TYPE_FIRST_INT:kotlin.Int)- [TypedValue.TYPE_LAST_INT](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#TYPE_LAST_INT:kotlin.Int): [Bundle.putBoolean()](https://developer.android.com/reference/kotlin/android/os/Bundle.html#putCharSequence(kotlin.String,%20kotlin.CharSequence)) - [TypedValue.TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#TYPE_FLOAT:kotlin.Int): [Bundle.putFloat()](https://developer.android.com/reference/kotlin/android/os/Bundle.html#putCharSequence(kotlin.String,%20kotlin.CharSequence)) <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parseBundleExtras](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#parseBundleExtras(android.content.res.XmlResourceParser,%20android.os.Bundle))`(`parser:` ` [XmlResourceParser](https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser.html#)!`, `outBundle:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` <br /> Parse a series of [<extra>](https://developer.android.com/reference/kotlin/android/R.styleable.html#Extra:kotlin.IntArray) tags from an XML file. You call this when you are at the parent tag of the extra tags, and it will return once all of the child tags have been parsed. This will call [parseBundleExtra](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#parseBundleExtra(kotlin.String,%20android.util.AttributeSet,%20android.os.Bundle))for each extra tag encountered. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerResourcePaths](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#registerResourcePaths(kotlin.String,%20android.content.pm.ApplicationInfo))`(`uniqueId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `appInfo:` ` [ApplicationInfo](https://developer.android.com/reference/kotlin/android/content/pm/ApplicationInfo.html#)`)` <br /> Register the resources paths of a package (e.g. a shared library). This will collect the package resources' paths from its ApplicationInfo and add them to all existing and future contexts while the application is running. A second call with the same uniqueId is a no-op. The paths are not persisted during application restarts. The application is responsible for calling the API again if this happens. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeLoaders](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#removeLoaders(android.content.res.loader.ResourcesLoader))`(`vararg` `loaders:` ` [ResourcesLoader](https://developer.android.com/reference/kotlin/android/content/res/loader/ResourcesLoader.html#)!`)` <br /> Removes loaders from the list of loaders. If the loader is not present in the list, the list will not be modified. This should only be called from the UI thread to avoid lock contention when propagating loader changes. <br /> | ||

## Public constructors

### MockResources

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MockResources()
```

## Public methods

### getAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAnimation(id: Int): XmlResourceParser
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [XmlResourceParser](https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser.html#) | A new parser object through which you can read the XML data. This value cannot be`null`. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColor(id: Int): Int
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A single color value in the form 0xAARRGGBB. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getColorStateList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColorStateList(id: Int): ColorStateList
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired resource identifier of a [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#), as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#) | A ColorStateList object containing either a single solid color or multiple colors that can be selected based on a state. This value cannot be`null`. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getConfiguration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getConfiguration(): Configuration!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------------------------------------|---------------------------------------|
| [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)! | The resource's current configuration. |

### getDimension

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDimension(id: Int): Float
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | Resource dimension value multiplied by the appropriate metric to convert to pixels. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getDimensionPixelOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDimensionPixelOffset(id: Int): Int
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Resource dimension value multiplied by the appropriate metric and truncated to integer pixels. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getDimensionPixelSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDimensionPixelSize(id: Int): Int
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Resource dimension value multiplied by the appropriate metric and truncated to integer pixels. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getDisplayMetrics

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDisplayMetrics(): DisplayMetrics!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#)! | The resource's current display metrics. |

### getDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDrawable(id: Int): Drawable!
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)! | Drawable An object that can be used to draw this resource. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getIdentifier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIdentifier(
    name: String!, 
    defType: String!, 
    defPackage: String!
): Int
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the desired resource. |
| `defType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Optional default resource type to find, if "type/" is not included in the name. Can be null to require an explicit type. |
| `defPackage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Optional default package to find, if "package:" is not included in the name. Can be null to require an explicit package. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | int The associated resource identifier. Returns 0 if no such resource was found. (0 is not a valid resource ID.) |

### getIntArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIntArray(id: Int): IntArray
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | The int array associated with the resource. This value cannot be`null`. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getInteger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInteger(id: Int): Int
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Returns the integer value contained in the resource. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLayout(id: Int): XmlResourceParser
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [XmlResourceParser](https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser.html#) | A new parser object through which you can read the XML data. This value cannot be`null`. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getMovie

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMovie(id: Int): Movie!
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getQuantityString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getQuantityString(
    id: Int, 
    quantity: Int
): String
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |
| `quantity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number used to get the correct string for the current language's plural rules. |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | String The string data associated with the resource, stripped of styled text information. This value cannot be`null`. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getQuantityString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getQuantityString(
    id: Int, 
    quantity: Int, 
    vararg formatArgs: Any!
): String
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |
| `quantity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number used to get the correct string for the current language's plural rules. |
| `formatArgs` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The format arguments that will be used for substitution. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | String The string data associated with the resource, stripped of styled text information. This value cannot be`null`. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getQuantityText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getQuantityText(
    id: Int, 
    quantity: Int
): CharSequence
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |
| `quantity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number used to get the correct string for the current language's plural rules. |

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | CharSequence The string data associated with the resource, plus possibly styled text information. This value cannot be`null`. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getResourceEntryName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getResourceEntryName(resid: Int): String!
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `resid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource identifier whose entry name is to be retrieved. |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | A string holding the entry name of the resource. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getResourceName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getResourceName(resid: Int): String!
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| `resid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource identifier whose name is to be retrieved. |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | A string holding the name of the resource. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getResourcePackageName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getResourcePackageName(resid: Int): String!
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `resid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource identifier whose package name is to be retrieved. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | A string holding the package name of the resource. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getResourceTypeName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getResourceTypeName(resid: Int): String!
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------|
| `resid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource identifier whose type name is to be retrieved. |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | A string holding the type name of the resource. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getString(id: Int): String
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | String The string data associated with the resource, stripped of styled text information. This value cannot be`null`. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getString(
    id: Int, 
    vararg formatArgs: Any!
): String
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |
| `formatArgs` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The format arguments that will be used for substitution. |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | String The string data associated with the resource, stripped of styled text information. This value cannot be`null`. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getStringArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStringArray(id: Int): Array<String!>
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | The string array associated with the resource. This value cannot be`null`. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getText(id: Int): CharSequence
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | CharSequence The string data associated with the resource, plus possibly styled text information. This value cannot be`null`. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getText(
    id: Int, 
    def: CharSequence!
): CharSequence!
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |
| `def` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The default CharSequence to return. |

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | CharSequence The string data associated with the resource, plus possibly styled text information, or def if id is 0 or not found. |

### getTextArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTextArray(id: Int): Array<CharSequence!>
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!> | The styled text array associated with the resource. This value cannot be`null`. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValue(
    id: Int, 
    outValue: TypedValue!, 
    resolveRefs: Boolean
): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |
| `outValue` | [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#)!:Object in which to place the resource data. |
| `resolveRefs` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true, a resource that is a reference to another resource will be followed so that you receive the actual final resource data. If false, the TypedValue will be filled in with the reference itself. |
| --- | --- |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValue(
    name: String!, 
    outValue: TypedValue!, 
    resolveRefs: Boolean
): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the desired resource. This is passed to getIdentifier() with a default type of "string". |
| `outValue` | [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#)!:Object in which to place the resource data. |
| `resolveRefs` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true, a resource that is a reference to another resource will be followed so that you receive the actual final resource data. If false, the TypedValue will be filled in with the reference itself. |
| --- | --- |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getXml

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getXml(id: Int): XmlResourceParser
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [XmlResourceParser](https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser.html#) | A new parser object through which you can read the XML data. This value cannot be`null`. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### obtainAttributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun obtainAttributes(
    set: AttributeSet!, 
    attrs: IntArray!
): TypedArray!
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `set` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!:The current attribute values to retrieve. |
| `attrs` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The specific attributes to be retrieved. These attribute IDs must be sorted in ascending order. |

| Return ||
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [TypedArray](https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#)! | Returns a TypedArray holding an array of the attribute values. Be sure to call [TypedArray.recycle()](https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#recycle())when done with it. |

### obtainTypedArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun obtainTypedArray(id: Int): TypedArray
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [TypedArray](https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#) | Returns a TypedArray holding an array of the array values. Be sure to call [TypedArray.recycle()](https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#recycle())when done with it. This value cannot be`null`. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### openRawResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openRawResource(id: Int): InputStream
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource identifier to open, as generated by the aapt tool. |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#) | InputStream Access to the resource data. This value cannot be`null`. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### openRawResourceFd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openRawResourceFd(id: Int): AssetFileDescriptor!
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource identifier to open, as generated by the aapt tool. |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#)! | AssetFileDescriptor A new file descriptor you can use to read the resource. This includes the file descriptor itself, as well as the offset and length of data where the resource appears in the file. A null is returned if the file exists but is compressed. |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------------------|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### updateConfiguration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun updateConfiguration(
    config: Configuration!, 
    metrics: DisplayMetrics!
): Unit
```

**Deprecated:** *Deprecated in Java.*
