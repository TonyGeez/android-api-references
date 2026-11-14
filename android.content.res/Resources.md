Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Resources

Kotlin | [Java](Resources.md)
| --- | --- |

```
open class Resources
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.res.Resources](Resources.md) |

| Known Direct Subclasses [MockResources](../android.test.mock/MockResources.md) |---|---| | [MockResources](../android.test.mock/MockResources.md) | A mock Resources class. | |
| --- | --- | --- | --- | --- | --- | --- |

Class for accessing an application's resources. This sits on top of the asset manager of the application (accessible through getAssets) and provides a high-level API for getting typed data from the assets.

The Android resource system keeps track of all non-code assets associated with an application. You can use this class to access your application's resources. You can generally acquire the Resources instance associated with your application with getResources.

The Android SDK tools compile your application's resources into the application binary at build time. To use a resource, you must install it correctly in the source tree (inside your project's `res/` directory) and build your application. As part of the build process, the SDK tools generate symbols for each resource, which you can use in your application code to access the resources.

Using application resources makes it easy to update various characteristics of your application without modifying code, and---by providing sets of alternative resources---enables you to optimize your application for a variety of device configurations (such as for different languages and screen sizes). This is an important aspect of developing Android applications that are compatible on different types of devices.

After `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int`, Resources must be obtained by `https://developer.android.com/reference/kotlin/android/app/Activity.html#` or `https://developer.android.com/reference/kotlin/android/content/Context.html#` created with createWindowContext. getResources may report wrong values in multi-window or on secondary displays.

For more information about using resources, see the documentation about [Application Resources](https://developer.android.com/guide/topics/resources/index.html).

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/content/res/Resources.NotFoundException` This exception is thrown by the resource APIs when a requested resource can not be found. |
| | `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme` This class holds the current attribute values for a particular theme. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/res/Resources#ID_NULL:kotlin.Int` The `null` resource ID. |

| Public constructors ||
|---|---|
| Resources Create a new Resources object on top of an existing set of assets in an AssetManager. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addLoaders Adds a loader to the list of loaders. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | finishPreloading Called by zygote when it is done preloading resources, to change back to normal Resources operation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | flushLayoutCache Call this to remove all cached loaded layout resources from the Resources object. |
| --- | --- |
| open [XmlResourceParser](XmlResourceParser.md) | getAnimation Return an XmlResourceParser through which you can read an animation description for the given resource ID. |
| [AssetManager](AssetManager.md)! | getAssets Retrieve underlying AssetManager storage for these resources. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getAttributeSetSourceResId Returns the resource ID of the resource that was used to create this AttributeSet. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | getBoolean Return a boolean associated with a particular resource ID. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getColor Returns a color integer associated with a particular resource ID. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getColor Returns a themed color integer associated with a particular resource ID. |
| --- | --- |
| open [ColorStateList](ColorStateList.md) | getColorStateList Returns a color state list associated with a particular resource ID. |
| open [ColorStateList](ColorStateList.md) | getColorStateList Returns a themed color state list associated with a particular resource ID. |
| open [Configuration](Configuration.md)! | getConfiguration Return the current configuration that is in effect for this resource object. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getDimension Retrieve a dimensional for a particular resource ID. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getDimensionPixelOffset Retrieve a dimensional for a particular resource ID for use as an offset in raw pixels. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getDimensionPixelSize Retrieve a dimensional for a particular resource ID for use as a size in raw pixels. |
| --- | --- |
| open [DisplayMetrics](../android.util/DisplayMetrics.md)! | getDisplayMetrics Returns the current display metrics that are in effect for this resource object. |
| open [Drawable](../android.graphics.drawable/Drawable.md)! | getDrawable Return a drawable object associated with a particular resource ID. |
| open [Drawable](../android.graphics.drawable/Drawable.md)! | getDrawable Return a drawable object associated with a particular resource ID and styled for the specified theme. |
| --- | --- |
| open [Drawable](../android.graphics.drawable/Drawable.md)? | getDrawableForDensity Return a drawable object associated with a particular resource ID for the given screen density in DPI. |
| open [Drawable](../android.graphics.drawable/Drawable.md)? | getDrawableForDensity Return a drawable object associated with a particular resource ID for the given screen density in DPI and styled for the specified theme. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getFloat Retrieve a floating-point value for a particular resource ID. |
| --- | --- |
| open [Typeface](../android.graphics/Typeface.md) | getFont Return the Typeface value associated with a particular resource ID. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getFraction Retrieve a fractional unit for a particular resource ID. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getIdentifier Return a resource identifier for the given resource name. |
| --- | --- |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | getIntArray Return the int array associated with a particular resource ID. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getInteger Return an integer associated with a particular resource ID. |
| open [XmlResourceParser](XmlResourceParser.md) | getLayout Return an XmlResourceParser through which you can read a view layout description for the given resource ID. |
| --- | --- |
| open [Movie](../android.graphics/Movie.md)! | getMovie Return a movie object associated with the particular resource ID. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getQuantityString Returns the string necessary for grammatically correct pluralization of the given resource ID for the given quantity. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getQuantityString Formats the string necessary for grammatically correct pluralization of the given resource ID for the given quantity, using the given arguments. |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | getQuantityText Returns the character sequence necessary for grammatically correct pluralization of the given resource ID for the given quantity. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getResourceEntryName Return the entry name for a given resource identifier. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getResourceName Return the full name for a given resource identifier. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getResourcePackageName Return the package name for a given resource identifier. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getResourceTypeName Return the type name for a given resource identifier. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getString Return the string value associated with a particular resource ID. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getString Return the string value associated with a particular resource ID, substituting the format arguments as defined in `https://developer.android.com/reference/kotlin/java/util/Formatter.html#` and java. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | getStringArray Return the string array associated with a particular resource ID. |
| open static [Resources](Resources.md)! | getSystem Return a global shared Resources object that provides access to only system resources (no application resources), is not configured for the current screen (can not use dimension units, does not change based on orientation, etc), and is not affected by Runtime Resource Overlay. |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | getText Return the string value associated with a particular resource ID. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | getText Return the string value associated with a particular resource ID. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\> | getTextArray Return the styled text array associated with a particular resource ID. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getValue Return the raw data associated with a particular resource ID. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getValue Return the raw data associated with a particular resource ID. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getValueForDensity Get the raw value associated with a resource with associated density. |
| --- | --- |
| open [XmlResourceParser](XmlResourceParser.md) | getXml Return an XmlResourceParser through which you can read a generic XML resource for the given resource ID. |
| [Resources.Theme](../android/content/res/Resources.Theme.md)! | newTheme Generate a new Theme object for this set of Resources. |
| open [TypedArray](TypedArray.md)! | obtainAttributes Retrieve a set of basic attribute values from an AttributeSet, not performing styling of them using a theme and/or style resources. |
| --- | --- |
| open [TypedArray](TypedArray.md) | obtainTypedArray Return an array of heterogeneous values. |
| open [InputStream](../java.io/InputStream.md) | openRawResource Open a data stream for reading a raw resource. |
| open [InputStream](../java.io/InputStream.md) | openRawResource Open a data stream for reading a raw resource. |
| --- | --- |
| open [AssetFileDescriptor](AssetFileDescriptor.md)! | openRawResourceFd Open a file descriptor for reading a raw resource. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parseBundleExtra Parse a name/value pair out of an XML tag holding that data. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parseBundleExtras Parse a series of `https://developer.android.com/reference/kotlin/android/R.styleable.html#Extra:kotlin.IntArray` tags from an XML file. |
| --- | --- |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerResourcePaths Register the resources paths of a package (e.g. a shared library). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeLoaders Removes loaders from the list of loaders. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | updateConfiguration Store the newly updated configuration. |
| --- | --- |

## Constants

### ID_NULL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ID_NULL: Int
```

The `null` resource ID. This denotes an invalid resource ID that is returned by the system when a resource is not found or the value is set to `@null` in XML.

 Value: 0

## Public constructors

### Resources

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Resources(
    assets: AssetManager!, 
    metrics: DisplayMetrics!, 
    config: Configuration!)
```

**Deprecated:** *Resources should not be constructed by apps. See createConfigurationContext.*

Create a new Resources object on top of an existing set of assets in an AssetManager.

| Parameters ||
|---|---|
| `assets` | [AssetManager](AssetManager.md)!: Previously created AssetManager. |
| `metrics` | [DisplayMetrics](../android.util/DisplayMetrics.md)!: Current display metrics to consider when selecting/computing resource values. |
| `config` | [Configuration](Configuration.md)!: Desired device configuration to consider when selecting/computing resource values (optional). |
| --- | --- |

## Public methods

### addLoaders

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addLoaders(vararg loaders: ResourcesLoader!): Unit
```

Adds a loader to the list of loaders. If the loader is already present in the list, the list will not be modified.

This should only be called from the UI thread to avoid lock contention when propagating loader changes.

| Parameters ||
|---|---|
| `loaders` | [ResourcesLoader](../android.content.res.loader/ResourcesLoader.md)!: the loaders to add. This value cannot be `null`. |

### finishPreloading

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun finishPreloading(): Unit
```

Called by zygote when it is done preloading resources, to change back to normal Resources operation.

### flushLayoutCache

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun flushLayoutCache(): Unit
```

Call this to remove all cached loaded layout resources from the Resources object. Only intended for use with performance testing tools.

### getAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAnimation(id: Int): XmlResourceParser
```

Return an XmlResourceParser through which you can read an animation description for the given resource ID. This parser has limited functionality -- in particular, you can't change its input, and only the high-level events are available.

This function is really a simple wrapper for calling getXml with an animation resource.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|---|---|
| XmlResourceParser | A new parser object through which you can read the XML data. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

**See Also**

- getXml

### getAssets

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAssets(): AssetManager!
```

Retrieve underlying AssetManager storage for these resources.

### getAttributeSetSourceResId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getAttributeSetSourceResId(set: AttributeSet?): Int
```

Returns the resource ID of the resource that was used to create this AttributeSet.

| Parameters ||
|---|---|
| `set` | [AttributeSet](../android.util/AttributeSet.md)?: AttributeSet for which we want to find the source. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The resource ID for the source that is backing the given AttributeSet or `https://developer.android.com/reference/kotlin/android/content/res/Resources#ID_NULL:kotlin.Int` if the AttributeSet is `null`. |

### getBoolean

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBoolean(id: Int): Boolean
```

Return a boolean associated with a particular resource ID. This can be used with any integral resource value, and will return true if it is non-zero.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns the boolean value contained in the resource. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getColor(id: Int): Int
```

**Deprecated:** *Use getColor instead.*

Returns a color integer associated with a particular resource ID. If the resource holds a complex ColorStateList, then the default color from the set is returned.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A single color value in the form 0xAARRGGBB. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getColor

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getColor(
    id: Int, 
    theme: Resources.Theme?
): Int
```

Returns a themed color integer associated with a particular resource ID. If the resource holds a complex ColorStateList, then the default color from the set is returned.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |
| `theme` | [Resources.Theme](../android/content/res/Resources.Theme.md)?: The theme used to style the color attributes, may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A single color value in the form 0xAARRGGBB. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getColorStateList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getColorStateList(id: Int): ColorStateList
```

**Deprecated:** *Use getColorStateList instead.*

Returns a color state list associated with a particular resource ID. The resource may contain either a single raw color value or a complex ColorStateList holding multiple possible colors.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier of a ColorStateList, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|---|---|
| ColorStateList | A ColorStateList object containing either a single solid color or multiple colors that can be selected based on a state. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getColorStateList

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getColorStateList(
    id: Int, 
    theme: Resources.Theme?
): ColorStateList
```

Returns a themed color state list associated with a particular resource ID. The resource may contain either a single raw color value or a complex ColorStateList holding multiple possible colors.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier of a ColorStateList, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |
| `theme` | [Resources.Theme](../android/content/res/Resources.Theme.md)?: The theme used to style the color attributes, may be `null`. |

| Return ||
|---|---|
| ColorStateList | A themed ColorStateList object containing either a single solid color or multiple colors that can be selected based on a state. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getConfiguration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getConfiguration(): Configuration!
```

Return the current configuration that is in effect for this resource object. The returned object should be treated as read-only.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/Configuration!` | The resource's current configuration. |

### getDimension

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDimension(id: Int): Float
```

Retrieve a dimensional for a particular resource ID. Unit conversions are based on the current `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#` associated with the resources.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Resource dimension value multiplied by the appropriate metric to convert to pixels. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

**See Also**

- getDimensionPixelOffset
- getDimensionPixelSize

### getDimensionPixelOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDimensionPixelOffset(id: Int): Int
```

Retrieve a dimensional for a particular resource ID for use as an offset in raw pixels. This is the same as getDimension, except the returned value is converted to integer pixels for you. An offset conversion involves simply truncating the base value to an integer.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Resource dimension value multiplied by the appropriate metric and truncated to integer pixels. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

**See Also**

- getDimension
- getDimensionPixelSize

### getDimensionPixelSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDimensionPixelSize(id: Int): Int
```

Retrieve a dimensional for a particular resource ID for use as a size in raw pixels. This is the same as getDimension, except the returned value is converted to integer pixels for use as a size. A size conversion involves rounding the base value, and ensuring that a non-zero base value is at least one pixel in size.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Resource dimension value multiplied by the appropriate metric and truncated to integer pixels. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

**See Also**

- getDimension
- getDimensionPixelOffset

### getDisplayMetrics

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDisplayMetrics(): DisplayMetrics!
```

Returns the current display metrics that are in effect for this resource object. The returned object should be treated as read-only.

Note that the reported value may be different than the window this application is interested in.

The best practices is to obtain metrics from getCurrentWindowMetrics for window bounds. The value obtained from this API may be wrong if getResources is not from a `UiContext`. For example, use the `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#` obtained from getResources to build `https://developer.android.com/reference/kotlin/android/app/Activity.html#` UI elements especially when the `https://developer.android.com/reference/kotlin/android/app/Activity.html#` is in the multi-window mode or on the secondary `https://developer.android.com/reference/kotlin/android/view/Display.html#`.

<br />

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#!` | The resource's current display metrics. |

### getDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDrawable(id: Int): Drawable!
```

**Deprecated:** *Use getDrawable instead.*

Return a drawable object associated with a particular resource ID. Various types of objects will be returned depending on the underlying resource -- for example, a solid color, PNG image, scalable image, etc. The Drawable API hides these implementation details.

**Note:** Prior to `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN:kotlin.Int`, this function would not correctly retrieve the final configuration density when the resource ID passed here is an alias to another Drawable resource. This means that if the density configuration of the alias resource is different than the actual resource, the density of the returned Drawable would be incorrect, resulting in bad scaling. To work around this, you can instead manually resolve the aliased reference by using getValue and passing `true` for `resolveRefs`. The resulting `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#resourceId:kotlin.Int` value may be passed to this method.

**Note:** To obtain a themed drawable, use getDrawable or getDrawable passing the desired theme.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` | Drawable An object that can be used to draw this resource. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

**See Also**

- getDrawable

### getDrawable

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDrawable(
    id: Int, 
    theme: Resources.Theme?
): Drawable!
```

Return a drawable object associated with a particular resource ID and styled for the specified theme. Various types of objects will be returned depending on the underlying resource -- for example, a solid color, PNG image, scalable image, etc.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |
| `theme` | [Resources.Theme](../android/content/res/Resources.Theme.md)?: The theme used to style the drawable attributes, may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` | Drawable An object that can be used to draw this resource. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getDrawableForDensity

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDrawableForDensity(
    id: Int, 
    density: Int
): Drawable?
```

**Deprecated:** *Use getDrawableForDensity instead.*

Return a drawable object associated with a particular resource ID for the given screen density in DPI. This will set the drawable's density to be the device's density multiplied by the ratio of actual drawable density to requested density. This allows the drawable to be scaled up to the correct size if needed. Various types of objects will be returned depending on the underlying resource -- for example, a solid color, PNG image, scalable image, etc. The Drawable API hides these implementation details.

**Note:** To obtain a themed drawable, use getDrawable or getDrawableForDensity passing the desired theme.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |
| `density` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the desired screen density indicated by the resource as found in `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#`. A value of 0 means to use the density returned from getConfiguration. This is equivalent to calling getDrawable. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | Drawable An object that can be used to draw this resource. This value may be `null`. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

**See Also**

- getDrawableForDensity

### getDrawableForDensity

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDrawableForDensity(
    id: Int, 
    density: Int, 
    theme: Resources.Theme?
): Drawable?
```

Return a drawable object associated with a particular resource ID for the given screen density in DPI and styled for the specified theme.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |
| `density` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired screen density indicated by the resource as found in `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#`. A value of 0 means to use the density returned from getConfiguration. This is equivalent to calling getDrawable. |
| `theme` | [Resources.Theme](../android/content/res/Resources.Theme.md)?: The theme used to style the drawable attributes, may be `null` if the drawable cannot be decoded. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | Drawable An object that can be used to draw this resource. This value may be `null`. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getFloat

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFloat(id: Int): Float
```

Retrieve a floating-point value for a particular resource ID.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Returns the floating-point value contained in the resource. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist or is not a floating-point value. |

### getFont

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFont(id: Int): Typeface
```

Return the Typeface value associated with a particular resource ID. {@more}

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#` | Typeface The Typeface data associated with the resource. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getFraction

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFraction(
    id: Int, 
    base: Int, 
    pbase: Int
): Float
```

Retrieve a fractional unit for a particular resource ID.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |
| `base` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The base value of this fraction. In other words, a standard fraction is multiplied by this value. |
| `pbase` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The parent base value of this fraction. In other words, a parent fraction (nn%p) is multiplied by this value. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Attribute fractional value multiplied by the appropriate base value. |

| Exceptions ||
|---|---|
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

Return a resource identifier for the given resource name. A fully qualified resource name is of the form "package:type/entry". The first two components (package and type) are optional if defType and defPackage, respectively, are specified here.

Note: use of this function is discouraged. It is much more efficient to retrieve resources by identifier than by name.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the desired resource. |
| `defType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Optional default resource type to find, if "type/" is not included in the name. Can be null to require an explicit type. |
| `defPackage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Optional default package to find, if "package:" is not included in the name. Can be null to require an explicit package. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | int The associated resource identifier. Returns 0 if no such resource was found. (0 is not a valid resource ID.) |

### getIntArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIntArray(id: Int): IntArray
```

Return the int array associated with a particular resource ID.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | The int array associated with the resource. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getInteger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInteger(id: Int): Int
```

Return an integer associated with a particular resource ID.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns the integer value contained in the resource. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLayout(id: Int): XmlResourceParser
```

Return an XmlResourceParser through which you can read a view layout description for the given resource ID. This parser has limited functionality -- in particular, you can't change its input, and only the high-level events are available.

This function is really a simple wrapper for calling getXml with a layout resource.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|---|---|
| XmlResourceParser | A new parser object through which you can read the XML data. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

**See Also**

- getXml

### getMovie

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMovie(id: Int): Movie!
```

**Deprecated:** *Prefer `https://developer.android.com/reference/kotlin/android/graphics/drawable/AnimatedImageDrawable.html#`.*

Return a movie object associated with the particular resource ID.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getQuantityString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getQuantityString(
    id: Int, 
    quantity: Int
): String
```

Returns the string necessary for grammatically correct pluralization of the given resource ID for the given quantity. Note that the string is selected based solely on grammatical necessity, and that such rules differ between languages. Do not assume you know which string will be returned for a given quantity. See [String Resources](https://developer.android.com/guide/topics/resources/string-resource.html#Plurals) for more detail.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |
| `quantity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number used to get the correct string for the current language's plural rules. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | String The string data associated with the resource, stripped of styled text information. This value cannot be `null`. |

| Exceptions ||
|---|---|
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

Formats the string necessary for grammatically correct pluralization of the given resource ID for the given quantity, using the given arguments. Note that the string is selected based solely on grammatical necessity, and that such rules differ between languages. Do not assume you know which string will be returned for a given quantity. See [String Resources](https://developer.android.com/guide/topics/resources/string-resource.html#Plurals) for more detail.

Substitution of format arguments works as if using `https://developer.android.com/reference/kotlin/java/util/Formatter.html#` and java.lang.String#format. The resulting string will be stripped of any styled text information.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |
| `quantity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number used to get the correct string for the current language's plural rules. |
| `formatArgs` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The format arguments that will be used for substitution. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | String The string data associated with the resource, stripped of styled text information. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getQuantityText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getQuantityText(
    id: Int, 
    quantity: Int
): CharSequence
```

Returns the character sequence necessary for grammatically correct pluralization of the given resource ID for the given quantity. Note that the character sequence is selected based solely on grammatical necessity, and that such rules differ between languages. Do not assume you know which string will be returned for a given quantity. See [String Resources](https://developer.android.com/guide/topics/resources/string-resource.html#Plurals) for more detail.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |
| `quantity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number used to get the correct string for the current language's plural rules. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` | CharSequence The string data associated with the resource, plus possibly styled text information. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getResourceEntryName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getResourceEntryName(resid: Int): String!
```

Return the entry name for a given resource identifier.

| Parameters ||
|---|---|
| `resid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource identifier whose entry name is to be retrieved. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | A string holding the entry name of the resource. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

**See Also**

- getResourceName

### getResourceName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getResourceName(resid: Int): String!
```

Return the full name for a given resource identifier. This name is a single string of the form "package:type/entry".

| Parameters ||
|---|---|
| `resid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource identifier whose name is to be retrieved. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | A string holding the name of the resource. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

**See Also**

- getResourcePackageName
- getResourceTypeName
- getResourceEntryName

### getResourcePackageName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getResourcePackageName(resid: Int): String!
```

Return the package name for a given resource identifier.

| Parameters ||
|---|---|
| `resid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource identifier whose package name is to be retrieved. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | A string holding the package name of the resource. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

**See Also**

- getResourceName

### getResourceTypeName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getResourceTypeName(resid: Int): String!
```

Return the type name for a given resource identifier.

| Parameters ||
|---|---|
| `resid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource identifier whose type name is to be retrieved. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | A string holding the type name of the resource. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

**See Also**

- getResourceName

### getString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getString(id: Int): String
```

Return the string value associated with a particular resource ID. It will be stripped of any styled text information. {@more}

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | String The string data associated with the resource, stripped of styled text information. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getString(
    id: Int, 
    vararg formatArgs: Any!
): String
```

Return the string value associated with a particular resource ID, substituting the format arguments as defined in `https://developer.android.com/reference/kotlin/java/util/Formatter.html#` and java.lang.String#format. It will be stripped of any styled text information. {@more}

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |
| `formatArgs` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The format arguments that will be used for substitution. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | String The string data associated with the resource, stripped of styled text information. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getStringArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStringArray(id: Int): Array<String!>
```

Return the string array associated with a particular resource ID.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | The string array associated with the resource. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getSystem

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getSystem(): Resources!
```

Return a global shared Resources object that provides access to only system resources (no application resources), is not configured for the current screen (can not use dimension units, does not change based on orientation, etc), and is not affected by Runtime Resource Overlay.

### getText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getText(id: Int): CharSequence
```

Return the string value associated with a particular resource ID. The returned object will be a String if this is a plain string; it will be some other type of CharSequence if it is styled. {@more}

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` | CharSequence The string data associated with the resource, plus possibly styled text information. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getText(
    id: Int, 
    def: CharSequence!
): CharSequence!
```

Return the string value associated with a particular resource ID. The returned object will be a String if this is a plain string; it will be some other type of CharSequence if it is styled.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |
| `def` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The default CharSequence to return. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | CharSequence The string data associated with the resource, plus possibly styled text information, or def if id is 0 or not found. |

### getTextArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextArray(id: Int): Array<CharSequence!>
```

Return the styled text array associated with a particular resource ID.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!>` | The styled text array associated with the resource. This value cannot be `null`. |

| Exceptions ||
|---|---|
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

Return the raw data associated with a particular resource ID.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |
| `outValue` | [TypedValue](../android.util/TypedValue.md)!: Object in which to place the resource data. |
| `resolveRefs` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, a resource that is a reference to another resource will be followed so that you receive the actual final resource data. If false, the TypedValue will be filled in with the reference itself. |
| --- | --- |

| Exceptions ||
|---|---|
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

Return the raw data associated with a particular resource ID. See getIdentifier() for information on how names are mapped to resource IDs, and getString(int) for information on how string resources are retrieved.

Note: use of this function is discouraged. It is much more efficient to retrieve resources by identifier than by name.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the desired resource. This is passed to getIdentifier() with a default type of "string". |
| `outValue` | [TypedValue](../android.util/TypedValue.md)!: Object in which to place the resource data. |
| `resolveRefs` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, a resource that is a reference to another resource will be followed so that you receive the actual final resource data. If false, the TypedValue will be filled in with the reference itself. |
| --- | --- |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### getValueForDensity

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getValueForDensity(
    id: Int, 
    density: Int, 
    outValue: TypedValue!, 
    resolveRefs: Boolean
): Unit
```

Get the raw value associated with a resource with associated density.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): resource identifier |
| `density` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): density in DPI |
| `resolveRefs` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, a resource that is a reference to another resource will be followed so that you receive the actual final resource data. If false, the TypedValue will be filled in with the reference itself. |
| --- | --- |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

**See Also**

- getValue

### getXml

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getXml(id: Int): XmlResourceParser
```

Return an XmlResourceParser through which you can read a generic XML resource for the given resource ID.

The XmlPullParser implementation returned here has some limited functionality. In particular, you can't change its input, and only high-level parsing events are available (since the document was pre-parsed for you at build time, which involved merging text and stripping comments).

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|---|---|
| XmlResourceParser | A new parser object through which you can read the XML data. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#`

### newTheme

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun newTheme(): Resources.Theme!
```

Generate a new Theme object for this set of Resources. It initially starts out empty.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/Resources.Theme!` | Theme The newly created Theme container. |

### obtainAttributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun obtainAttributes(
    set: AttributeSet!, 
    attrs: IntArray!
): TypedArray!
```

Retrieve a set of basic attribute values from an AttributeSet, not performing styling of them using a theme and/or style resources.

| Parameters ||
|---|---|
| `set` | [AttributeSet](../android.util/AttributeSet.md)!: The current attribute values to retrieve. |
| `attrs` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: The specific attributes to be retrieved. These attribute IDs must be sorted in ascending order. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/TypedArray!` | Returns a TypedArray holding an array of the attribute values. Be sure to call recycle when done with it. |

**See Also**

- obtainStyledAttributes

### obtainTypedArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun obtainTypedArray(id: Int): TypedArray
```

Return an array of heterogeneous values.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The desired resource identifier, as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|---|---|
| TypedArray | Returns a TypedArray holding an array of the array values. Be sure to call recycle when done with it. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### openRawResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun openRawResource(id: Int): InputStream
```

Open a data stream for reading a raw resource. This can only be used with resources whose value is the name of an asset files -- that is, it can be used to open drawable, sound, and raw resources; it will fail on string and color resources.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource identifier to open, as generated by the aapt tool. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/InputStream.html#` | InputStream Access to the resource data. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### openRawResource

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun openRawResource(
    id: Int, 
    value: TypedValue!
): InputStream
```

Open a data stream for reading a raw resource. This can only be used with resources whose value is the name of an asset file -- that is, it can be used to open drawable, sound, and raw resources; it will fail on string and color resources.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource identifier to open, as generated by the aapt tool. |
| `value` | [TypedValue](../android.util/TypedValue.md)!: The TypedValue object to hold the resource information. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/InputStream.html#` | InputStream Access to the resource data. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### openRawResourceFd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun openRawResourceFd(id: Int): AssetFileDescriptor!
```

Open a file descriptor for reading a raw resource. This can only be used with resources whose value is the name of an asset files -- that is, it can be used to open drawable, sound, and raw resources; it will fail on string and color resources.

This function only works for resources that are stored in the package as uncompressed data, which typically includes things like mp3 files and png images.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource identifier to open, as generated by the aapt tool. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor!` | AssetFileDescriptor A new file descriptor you can use to read the resource. This includes the file descriptor itself, as well as the offset and length of data where the resource appears in the file. A null is returned if the file exists but is compressed. |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | Throws NotFoundException if the given ID does not exist. |

### parseBundleExtra

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun parseBundleExtra(
    tagName: String!, 
    attrs: AttributeSet!, 
    outBundle: Bundle!
): Unit
```

Parse a name/value pair out of an XML tag holding that data. The AttributeSet must be holding the data defined by `https://developer.android.com/reference/kotlin/android/R.styleable.html#Extra:kotlin.IntArray`. The following value types are supported:

- `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#TYPE_STRING:kotlin.Int`: putCharSequence
- `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#TYPE_INT_BOOLEAN:kotlin.Int`: putCharSequence
- `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#TYPE_FIRST_INT:kotlin.Int`-`https://developer.android.com/reference/kotlin/android/util/TypedValue.html#TYPE_LAST_INT:kotlin.Int`: putCharSequence
- `https://developer.android.com/reference/kotlin/android/util/TypedValue.html#TYPE_FLOAT:kotlin.Int`: putCharSequence

<br />

| Parameters ||
|---|---|
| `tagName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the tag these attributes come from; this is only used for reporting error messages. |
| `attrs` | [AttributeSet](../android.util/AttributeSet.md)!: The attributes from which to retrieve the name/value pair. |
| `outBundle` | [Bundle](../android.os/Bundle.md)!: The Bundle in which to place the parsed value. |
| --- | --- |

| Exceptions ||
|---|---|
| `org.xmlpull.v1.XmlPullParserException` | If the attributes are not valid. |

### parseBundleExtras

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun parseBundleExtras(
    parser: XmlResourceParser!, 
    outBundle: Bundle!
): Unit
```

Parse a series of `https://developer.android.com/reference/kotlin/android/R.styleable.html#Extra:kotlin.IntArray` tags from an XML file. You call this when you are at the parent tag of the extra tags, and it will return once all of the child tags have been parsed. This will call parseBundleExtra for each extra tag encountered.

| Parameters ||
|---|---|
| `parser` | [XmlResourceParser](XmlResourceParser.md)!: The parser from which to retrieve the extras. |
| `outBundle` | [Bundle](../android.os/Bundle.md)!: A Bundle in which to place all parsed extras. |

| Exceptions ||
|---|---|
| `java.io.IOException` | |
| `org.xmlpull.v1.XmlPullParserException` | |

### registerResourcePaths

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun registerResourcePaths(
    uniqueId: String, 
    appInfo: ApplicationInfo
): Unit
```

Register the resources paths of a package (e.g. a shared library). This will collect the package resources' paths from its ApplicationInfo and add them to all existing and future contexts while the application is running. A second call with the same uniqueId is a no-op. The paths are not persisted during application restarts. The application is responsible for calling the API again if this happens.

| Parameters ||
|---|---|
| `uniqueId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The unique id for the ApplicationInfo object, to detect and ignore repeated API calls. This value cannot be `null`. |
| `appInfo` | [ApplicationInfo](../android.content.pm/ApplicationInfo.md): The ApplicationInfo that contains resources paths of the package. This value cannot be `null`. |

### removeLoaders

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeLoaders(vararg loaders: ResourcesLoader!): Unit
```

Removes loaders from the list of loaders. If the loader is not present in the list, the list will not be modified.

This should only be called from the UI thread to avoid lock contention when propagating loader changes.

| Parameters ||
|---|---|
| `loaders` | [ResourcesLoader](../android.content.res.loader/ResourcesLoader.md)!: the loaders to remove. This value cannot be `null`. |

### updateConfiguration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateConfiguration(
    config: Configuration!, 
    metrics: DisplayMetrics!
): Unit
```

**Deprecated:** *See createConfigurationContext.*

Store the newly updated configuration.
