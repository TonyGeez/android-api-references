# MockResources

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MockResources

Kotlin| [Java](MockResources.md) 
| --- | --- |

```
open class MockResources : Resources
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.content.res.Resources](../android.content.res/Resources.md) ||
| | ↳ | [android.test.mock.MockResources](MockResources.md) |

| **This class was deprecated in API level 24.**
|
| Use a mocking framework like [Mockito](https://github.com/mockito/mockito). New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

A mock [android.content.res.Resources](../android.content.res/Resources.md) class. All methods are non-functional and throw [java.lang.UnsupportedOperationException](../java.lang/UnsupportedOperationException.md). Override it to provide the operations that you need.

## Summary

| Inherited constants ||
|---|---|
| From class [Resources](../android.content.res/Resources.md) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ID_NULL](../android.content.res/Resources.md) <br /> The`null`resource ID. This denotes an invalid resource ID that is returned by the system when a resource is not found or the value is set to`@null`in XML. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------|---|
| [MockResources](MockResources.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [XmlResourceParser](../android.content.res/XmlResourceParser.md) | [getAnimation](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColor](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [ColorStateList](../android.content.res/ColorStateList.md) | [getColorStateList](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Configuration](../android.content.res/Configuration.md)! | [getConfiguration](MockResources.md))`()` <br /> |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDimension](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDimensionPixelOffset](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDimensionPixelSize](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [DisplayMetrics](../android.util/DisplayMetrics.md)! | [getDisplayMetrics](MockResources.md))`()` <br /> |
| open [Drawable](../android.graphics.drawable/Drawable.md)! | [getDrawable](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIdentifier](MockResources.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `defType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `defPackage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getIntArray](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInteger](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [XmlResourceParser](../android.content.res/XmlResourceParser.md) | [getLayout](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Movie](../android.graphics/Movie.md)! | [getMovie](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getQuantityString](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `quantity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getQuantityString](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `quantity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `vararg` `formatArgs:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getQuantityText](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `quantity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getResourceEntryName](MockResources.md))`(`resid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getResourceName](MockResources.md))`(`resid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getResourcePackageName](MockResources.md))`(`resid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getResourceTypeName](MockResources.md))`(`resid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getString](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getString](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `vararg` `formatArgs:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getStringArray](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getText](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getText](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `def:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\> | [getTextArray](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getValue](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `outValue:` ` [TypedValue](../android.util/TypedValue.md)!`, `resolveRefs:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getValue](MockResources.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `outValue:` ` [TypedValue](../android.util/TypedValue.md)!`, `resolveRefs:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [XmlResourceParser](../android.content.res/XmlResourceParser.md) | [getXml](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [TypedArray](../android.content.res/TypedArray.md)! | [obtainAttributes](MockResources.md))`(`set:` ` [AttributeSet](../android.util/AttributeSet.md)!`, `attrs:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` <br /> |
| open [TypedArray](../android.content.res/TypedArray.md) | [obtainTypedArray](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [InputStream](../java.io/InputStream.md) | [openRawResource](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [AssetFileDescriptor](../android.content.res/AssetFileDescriptor.md)! | [openRawResourceFd](MockResources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateConfiguration](MockResources.md))`(`config:` ` [Configuration](../android.content.res/Configuration.md)!`, `metrics:` ` [DisplayMetrics](../android.util/DisplayMetrics.md)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Resources](../android.content.res/Resources.md) |--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addLoaders](../android.content.res/Resources.md))`(`vararg` `loaders:` ` [ResourcesLoader](../android.content.res.loader/ResourcesLoader.md)!`)` <br /> Adds a loader to the list of loaders. If the loader is already present in the list, the list will not be modified. This should only be called from the UI thread to avoid lock contention when propagating loader changes. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finishPreloading](../android.content.res/Resources.md))`()` <br /> Called by zygote when it is done preloading resources, to change back to normal Resources operation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flushLayoutCache](../android.content.res/Resources.md))`()` <br /> Call this to remove all cached loaded layout resources from the Resources object. Only intended for use with performance testing tools. <br /> | | [AssetManager](../android.content.res/AssetManager.md)! | [getAssets](../android.content.res/Resources.md))`()` <br /> Retrieve underlying AssetManager storage for these resources. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAttributeSetSourceResId](../android.content.res/Resources.md))`(`set:` ` [AttributeSet](../android.util/AttributeSet.md)?`)` <br /> Returns the resource ID of the resource that was used to create this AttributeSet. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBoolean](../android.content.res/Resources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return a boolean associated with a particular resource ID. This can be used with any integral resource value, and will return true if it is non-zero. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColor](../android.content.res/Resources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` <br /> Returns a themed color integer associated with a particular resource ID. If the resource holds a complex [ColorStateList](../android.content.res/ColorStateList.md), then the default color from the set is returned. <br /> | | [ColorStateList](../android.content.res/ColorStateList.md) | [getColorStateList](../android.content.res/Resources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` <br /> Returns a themed color state list associated with a particular resource ID. The resource may contain either a single raw color value or a complex [ColorStateList](../android.content.res/ColorStateList.md) holding multiple possible colors. <br /> | | [Drawable](../android.graphics.drawable/Drawable.md)! | [getDrawable](../android.content.res/Resources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` <br /> Return a drawable object associated with a particular resource ID and styled for the specified theme. Various types of objects will be returned depending on the underlying resource -- for example, a solid color, PNG image, scalable image, etc. <br /> | | [Drawable](../android.graphics.drawable/Drawable.md)? | [getDrawableForDensity](../android.content.res/Resources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `density:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return a drawable object associated with a particular resource ID for the given screen density in DPI. This will set the drawable's density to be the device's density multiplied by the ratio of actual drawable density to requested density. This allows the drawable to be scaled up to the correct size if needed. Various types of objects will be returned depending on the underlying resource -- for example, a solid color, PNG image, scalable image, etc. The Drawable API hides these implementation details. **Note:** To obtain a themed drawable, use [Context.getDrawable(int)](../android.content/Context.md))or [getDrawableForDensity(int,int,android.content.res.Resources.Theme)](../android.content.res/Resources.md))passing the desired theme. <br /> | | [Drawable](../android.graphics.drawable/Drawable.md)? | [getDrawableForDensity](../android.content.res/Resources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `density:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `theme:` ` [Resources.Theme](../android/content/res/Resources.Theme.md)?`)` <br /> Return a drawable object associated with a particular resource ID for the given screen density in DPI and styled for the specified theme. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](../android.content.res/Resources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieve a floating-point value for a particular resource ID. <br /> | | [Typeface](../android.graphics/Typeface.md) | [getFont](../android.content.res/Resources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return the Typeface value associated with a particular resource ID. {@more} <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFraction](../android.content.res/Resources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `base:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pbase:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieve a fractional unit for a particular resource ID. <br /> | | [Resources](../android.content.res/Resources.md)! | [getSystem](../android.content.res/Resources.md))`()` <br /> Return a global shared Resources object that provides access to only system resources (no application resources), is not configured for the current screen (can not use dimension units, does not change based on orientation, etc), and is not affected by Runtime Resource Overlay. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getValueForDensity](../android.content.res/Resources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `density:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `outValue:` ` [TypedValue](../android.util/TypedValue.md)!`, `resolveRefs:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Get the raw value associated with a resource with associated density. <br /> | | [Resources.Theme](../android/content/res/Resources.Theme.md)! | [newTheme](../android.content.res/Resources.md))`()` <br /> Generate a new Theme object for this set of Resources. It initially starts out empty. <br /> | | [InputStream](../java.io/InputStream.md) | [openRawResource](../android.content.res/Resources.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [TypedValue](../android.util/TypedValue.md)!`)` <br /> Open a data stream for reading a raw resource. This can only be used with resources whose value is the name of an asset file -- that is, it can be used to open drawable, sound, and raw resources; it will fail on string and color resources. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parseBundleExtra](../android.content.res/Resources.md))`(`tagName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)!`, `outBundle:` ` [Bundle](../android.os/Bundle.md)!`)` <br /> Parse a name/value pair out of an XML tag holding that data. The AttributeSet must be holding the data defined by [android.R.styleable#Extra](../android/R.styleable.md). The following value types are supported: - [TypedValue.TYPE_STRING](../android.util/TypedValue.md): [Bundle.putCharSequence()](../android.os/Bundle.md)) - [TypedValue.TYPE_INT_BOOLEAN](../android.util/TypedValue.md): [Bundle.putBoolean()](../android.os/Bundle.md)) - [TypedValue.TYPE_FIRST_INT](../android.util/TypedValue.md)- [TypedValue.TYPE_LAST_INT](../android.util/TypedValue.md): [Bundle.putBoolean()](../android.os/Bundle.md)) - [TypedValue.TYPE_FLOAT](../android.util/TypedValue.md): [Bundle.putFloat()](../android.os/Bundle.md)) <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parseBundleExtras](../android.content.res/Resources.md))`(`parser:` ` [XmlResourceParser](../android.content.res/XmlResourceParser.md)!`, `outBundle:` ` [Bundle](../android.os/Bundle.md)!`)` <br /> Parse a series of [<extra>](../android/R.styleable.md) tags from an XML file. You call this when you are at the parent tag of the extra tags, and it will return once all of the child tags have been parsed. This will call [parseBundleExtra](../android.content.res/Resources.md))for each extra tag encountered. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerResourcePaths](../android.content.res/Resources.md))`(`uniqueId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `appInfo:` ` [ApplicationInfo](../android.content.pm/ApplicationInfo.md)`)` <br /> Register the resources paths of a package (e.g. a shared library). This will collect the package resources' paths from its ApplicationInfo and add them to all existing and future contexts while the application is running. A second call with the same uniqueId is a no-op. The paths are not persisted during application restarts. The application is responsible for calling the API again if this happens. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeLoaders](../android.content.res/Resources.md))`(`vararg` `loaders:` ` [ResourcesLoader](../android.content.res.loader/ResourcesLoader.md)!`)` <br /> Removes loaders from the list of loaders. If the loader is not present in the list, the list will not be modified. This should only be called from the UI thread to avoid lock contention when propagating loader changes. <br /> | ||

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
| [XmlResourceParser](../android.content.res/XmlResourceParser.md) | A new parser object through which you can read the XML data. This value cannot be`null`. |

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
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired resource identifier of a [ColorStateList](../android.content.res/ColorStateList.md), as generated by the aapt tool. This integer encodes the package, type, and resource entry. The value 0 is an invalid identifier. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ColorStateList](../android.content.res/ColorStateList.md) | A ColorStateList object containing either a single solid color or multiple colors that can be selected based on a state. This value cannot be`null`. |

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
| [Configuration](../android.content.res/Configuration.md)! | The resource's current configuration. |

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
| [DisplayMetrics](../android.util/DisplayMetrics.md)! | The resource's current display metrics. |

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
| [Drawable](../android.graphics.drawable/Drawable.md)! | Drawable An object that can be used to draw this resource. |

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
| [XmlResourceParser](../android.content.res/XmlResourceParser.md) | A new parser object through which you can read the XML data. This value cannot be`null`. |

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
| `outValue` | [TypedValue](../android.util/TypedValue.md)!:Object in which to place the resource data. |
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
| `outValue` | [TypedValue](../android.util/TypedValue.md)!:Object in which to place the resource data. |
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
| [XmlResourceParser](../android.content.res/XmlResourceParser.md) | A new parser object through which you can read the XML data. This value cannot be`null`. |

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
| `set` | [AttributeSet](../android.util/AttributeSet.md)!:The current attribute values to retrieve. |
| `attrs` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The specific attributes to be retrieved. These attribute IDs must be sorted in ascending order. |

| Return ||
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [TypedArray](../android.content.res/TypedArray.md)! | Returns a TypedArray holding an array of the attribute values. Be sure to call [TypedArray.recycle()](../android.content.res/TypedArray.md))when done with it. |

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
| [TypedArray](../android.content.res/TypedArray.md) | Returns a TypedArray holding an array of the array values. Be sure to call [TypedArray.recycle()](../android.content.res/TypedArray.md))when done with it. This value cannot be`null`. |

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
| [InputStream](../java.io/InputStream.md) | InputStream Access to the resource data. This value cannot be`null`. |

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
| [AssetFileDescriptor](../android.content.res/AssetFileDescriptor.md)! | AssetFileDescriptor A new file descriptor you can use to read the resource. This includes the file descriptor itself, as well as the offset and length of data where the resource appears in the file. A null is returned if the file exists but is compressed. |

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
