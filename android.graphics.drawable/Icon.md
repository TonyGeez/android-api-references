# Icon

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Icon

Kotlin| [Java](Icon.md) 
| --- | --- |

```
class Icon : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.drawable.Icon](Icon.md) |

An umbrella container for several serializable graphics representations, including Bitmaps, compressed bitmap images (e.g. JPG or PNG), and drawable resources (including vectors). [Much ink](https://developer.android.com/training/displaying-bitmaps/index.html) has been spilled on the best way to load images, and many clients may have different needs when it comes to threading and fetching. This class is therefore focused on encapsulation rather than behavior.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnDrawableLoadedListener](../android/graphics/drawable/Icon.OnDrawableLoadedListener.md) Implement this interface to receive a callback when [loadDrawableAsync](Icon.md))is finished and your Drawable is ready. |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ADAPTIVE_BITMAP](Icon.md) An icon that was created using [Icon.createWithAdaptiveBitmap](Icon.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BITMAP](Icon.md) An icon that was created using [Icon.createWithBitmap(Bitmap)](Icon.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_DATA](Icon.md) An icon that was created using[Icon.createWithData(byte[], int, int)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#createWithData(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RESOURCE](Icon.md) An icon that was created using android. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_URI](Icon.md) An icon that was created using android. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_URI_ADAPTIVE_BITMAP](Icon.md) An icon that was created using android. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Icon](Icon.md) | [createWithAdaptiveBitmap](Icon.md))`(`bits:` ` [Bitmap](../android.graphics/Bitmap.md)!`)` Create an Icon pointing to a bitmap in memory that follows the icon design guideline defined by [AdaptiveIconDrawable](AdaptiveIconDrawable.md). |
| static [Icon](Icon.md) | [createWithAdaptiveBitmapContentUri](Icon.md))`(`uri:` ` [Uri](../android.net/Uri.md)`)` Create an Icon pointing to an image file specified by URI. |
| static [Icon](Icon.md) | [createWithAdaptiveBitmapContentUri](Icon.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Create an Icon pointing to an image file specified by URI. |
| --- | --- |
| static [Icon](Icon.md) | [createWithBitmap](Icon.md))`(`bits:` ` [Bitmap](../android.graphics/Bitmap.md)!`)` Create an Icon pointing to a bitmap in memory. |
| static [Icon](Icon.md) | [createWithContentUri](Icon.md))`(`uri:` ` [Uri](../android.net/Uri.md)!`)` Create an Icon pointing to an image file specified by URI. |
| static [Icon](Icon.md) | [createWithContentUri](Icon.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create an Icon pointing to an image file specified by URI. |
| --- | --- |
| static [Icon](Icon.md) | [createWithData](Icon.md))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create an Icon pointing to a compressed bitmap stored in a byte array. |
| static [Icon](Icon.md) | [createWithFilePath](Icon.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create an Icon pointing to an image file specified by path. |
| static [Icon](Icon.md) | [createWithResource](Icon.md))`(`context:` ` [Context](../android.content/Context.md)!`, `resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create an Icon pointing to a drawable resource. |
| --- | --- |
| static [Icon](Icon.md) | [createWithResource](Icon.md))`(`resPackage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create an Icon pointing to a drawable resource. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](Icon.md))`()` Parcelable interface |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResId](Icon.md))`()` Gets the resource used to create this icon. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getResPackage](Icon.md))`()` Gets the package used to create this icon. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](Icon.md))`()` Gets the type of the icon provided. |
| [Uri](../android.net/Uri.md) | [getUri](Icon.md))`()` Gets the uri used to create this icon. |
| --- | --- |
| [Drawable](Drawable.md)? | [loadDrawable](Icon.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Returns a Drawable that can be used to draw the image inside this Icon, constructing it if necessary. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadDrawableAsync](Icon.md))`(`context:` ` [Context](../android.content/Context.md)`, `listener:` ` [Icon.OnDrawableLoadedListener](../android/graphics/drawable/Icon.OnDrawableLoadedListener.md)!`, `handler:` ` [Handler](../android.os/Handler.md)!`)` Invokes [loadDrawable(android.content.Context)](Icon.md))on a background thread and notifies the` ` [listener](../android/graphics/drawable/Icon.OnDrawableLoadedListener.md))` `on the`handler`when finished. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadDrawableAsync](Icon.md))`(`context:` ` [Context](../android.content/Context.md)`, `andThen:` ` [Message](../android.os/Message.md)`)` Invokes [loadDrawable(android.content.Context)](Icon.md))on the given [Handler](../android.os/Handler.md) and then sends`andThen`to the same Handler when finished. |
| --- | --- |
| [Icon](Icon.md) | [setTint](Icon.md))`(`tint:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Store a color to use whenever this Icon is drawn. |
| [Icon](Icon.md) | [setTintBlendMode](Icon.md))`(`mode:` ` [BlendMode](../android.graphics/BlendMode.md)`)` Store a blending mode to use whenever this Icon is drawn. |
| [Icon](Icon.md) | [setTintList](Icon.md))`(`tintList:` ` [ColorStateList](../android.content.res/ColorStateList.md)!`)` Store a color to use whenever this Icon is drawn. |
| --- | --- |
| [Icon](Icon.md) | [setTintMode](Icon.md))`(`mode:` ` [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)`)` Store a blending mode to use whenever this Icon is drawn. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Icon.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](Icon.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Icon](Icon.md)!\> | [CREATOR](Icon.md) <br /> |

## Constants

### TYPE_ADAPTIVE_BITMAP

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ADAPTIVE_BITMAP: Int
```

An icon that was created using [Icon.createWithAdaptiveBitmap](Icon.md)). 

 Value: 5

**See Also**

- [#getType](Icon.md)) 

### TYPE_BITMAP

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_BITMAP: Int
```

An icon that was created using [Icon.createWithBitmap(Bitmap)](Icon.md)). 

 Value: 1

**See Also**

- [#getType](Icon.md)) 

### TYPE_DATA

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_DATA: Int
```

An icon that was created using[Icon.createWithData(byte[], int, int)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#createWithData(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)). 

 Value: 3

**See Also**

- [#getType](Icon.md)) 

### TYPE_RESOURCE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_RESOURCE: Int
```

An icon that was created using android.graphics.drawable.Icon#createWithResource. 

 Value: 2

**See Also**

- [#getType](Icon.md)) 

### TYPE_URI

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_URI: Int
```

An icon that was created using android.graphics.drawable.Icon#createWithContentUri or [Icon.createWithFilePath(String)](Icon.md)). 

 Value: 4

**See Also**

- [#getType](Icon.md)) 

### TYPE_URI_ADAPTIVE_BITMAP

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_URI_ADAPTIVE_BITMAP: Int
```

An icon that was created using android.graphics.drawable.Icon#createWithAdaptiveBitmapContentUri. 

 Value: 6

**See Also**

- [#getType](Icon.md))

## Public methods

### createWithAdaptiveBitmap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createWithAdaptiveBitmap(bits: Bitmap!): Icon
```

Create an Icon pointing to a bitmap in memory that follows the icon design guideline defined by [AdaptiveIconDrawable](AdaptiveIconDrawable.md).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bits` | [Bitmap](../android.graphics/Bitmap.md)!:A valid [android.graphics.Bitmap](../android.graphics/Bitmap.md) object |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Icon](Icon.md) | This value cannot be`null`. |

### createWithAdaptiveBitmapContentUri

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createWithAdaptiveBitmapContentUri(uri: Uri): Icon
```

Create an Icon pointing to an image file specified by URI. Image file should follow the icon design guideline defined by [AdaptiveIconDrawable](AdaptiveIconDrawable.md).

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android.net/Uri.md):A uri referring to local content:// or file:// image data. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Icon](Icon.md) | This value cannot be`null`. |

### createWithAdaptiveBitmapContentUri

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createWithAdaptiveBitmapContentUri(uri: String): Icon
```

Create an Icon pointing to an image file specified by URI. Image file should follow the icon design guideline defined by [AdaptiveIconDrawable](AdaptiveIconDrawable.md).

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):A uri referring to local content:// or file:// image data. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Icon](Icon.md) | This value cannot be`null`. |

### createWithBitmap

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createWithBitmap(bits: Bitmap!): Icon
```

Create an Icon pointing to a bitmap in memory.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bits` | [Bitmap](../android.graphics/Bitmap.md)!:A valid [android.graphics.Bitmap](../android.graphics/Bitmap.md) object |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Icon](Icon.md) | This value cannot be`null`. |

### createWithContentUri

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createWithContentUri(uri: Uri!): Icon
```

Create an Icon pointing to an image file specified by URI.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android.net/Uri.md)!:A uri referring to local content:// or file:// image data. |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Icon](Icon.md) | This value cannot be`null`. |

### createWithContentUri

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createWithContentUri(uri: String!): Icon
```

Create an Icon pointing to an image file specified by URI.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A uri referring to local content:// or file:// image data. |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Icon](Icon.md) | This value cannot be`null`. |

### createWithData

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createWithData(
    data: ByteArray!, 
    offset: Int, 
    length: Int
): Icon
```

Create an Icon pointing to a compressed bitmap stored in a byte array.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:Byte array storing compressed bitmap data of a type that [android.graphics.BitmapFactory](../android.graphics/BitmapFactory.md) can decode (see [android.graphics.Bitmap.CompressFormat](../android/graphics/Bitmap.CompressFormat.md)). |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset into`data`at which the bitmap data starts |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Length of the bitmap data |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Icon](Icon.md) | This value cannot be`null`. |

### createWithFilePath

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createWithFilePath(path: String!): Icon
```

Create an Icon pointing to an image file specified by path.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A path to a file that contains compressed bitmap data of a type that [android.graphics.BitmapFactory](../android.graphics/BitmapFactory.md) can decode. |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Icon](Icon.md) | This value cannot be`null`. |

### createWithResource

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createWithResource(
    context: Context!, 
    resId: Int
): Icon
```

Create an Icon pointing to a drawable resource.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:The context for the application whose resources should be used to resolve the given resource ID. |
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):ID of the drawable resource |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Icon](Icon.md) | This value cannot be`null`. |

### createWithResource

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createWithResource(
    resPackage: String!, 
    resId: Int
): Icon
```

Create an Icon pointing to a drawable resource.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `resPackage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Name of the package containing the resource in question |
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):ID of the drawable resource |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Icon](Icon.md) | This value cannot be`null`. |

### describeContents

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Parcelable interface

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getResId

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getResId(): Int
```

Gets the resource used to create this icon.

Only valid for icons of type [TYPE_RESOURCE](Icon.md). Note: This resource may not be available if the application changes at all, and it is up to the caller to ensure safety if this resource is re-used and/or persisted. 

### getResPackage

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getResPackage(): String
```

Gets the package used to create this icon.

Only valid for icons of type [TYPE_RESOURCE](Icon.md). Note: This package may not be available if referenced in the future, and it is up to the caller to ensure safety if this package is re-used and/or persisted.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getType

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Int
```

Gets the type of the icon provided.

Note that new types may be added later, so callers should guard against other types being returned.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.graphics.drawable.Icon#TYPE_BITMAP](Icon.md), [android.graphics.drawable.Icon#TYPE_RESOURCE](Icon.md), [android.graphics.drawable.Icon#TYPE_DATA](Icon.md), [android.graphics.drawable.Icon#TYPE_URI](Icon.md), [android.graphics.drawable.Icon#TYPE_ADAPTIVE_BITMAP](Icon.md), or [android.graphics.drawable.Icon#TYPE_URI_ADAPTIVE_BITMAP](Icon.md) |

### getUri

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUri(): Uri
```

Gets the uri used to create this icon.

Only valid for icons of type [TYPE_URI](Icon.md) and [TYPE_URI_ADAPTIVE_BITMAP](Icon.md). Note: This uri may not be available in the future, and it is up to the caller to ensure safety if this uri is re-used and/or persisted.

| Return ||
|-----------------------------------------------------------------------------|-----------------------------|
| [Uri](../android.net/Uri.md) | This value cannot be`null`. |

### loadDrawable

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadDrawable(context: Context!): Drawable?
```

Returns a Drawable that can be used to draw the image inside this Icon, constructing it if necessary. Depending on the type of image, this may not be something you want to do on the UI thread, so consider using [loadDrawableAsync](Icon.md))instead.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!: [Context](../android.content/Context.md) in which to load the drawable; used to access [Resources](../android.content.res/Resources.md), for example. |

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Drawable](Drawable.md)? | A fresh instance of a drawable for this image, yours to keep. This value may be`null`. |

### loadDrawableAsync

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadDrawableAsync(
    context: Context, 
    listener: Icon.OnDrawableLoadedListener!, 
    handler: Handler!
): Unit
```

Invokes [loadDrawable(android.content.Context)](Icon.md))on a background thread and notifies the` ` [listener](../android/graphics/drawable/Icon.OnDrawableLoadedListener.md))` `on the`handler`when finished.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md): [Context](../android.content/Context.md) in which to load the drawable; see [loadDrawable(android.content.Context)](Icon.md))This value cannot be`null`. |
| `listener` | [Icon.OnDrawableLoadedListener](../android/graphics/drawable/Icon.OnDrawableLoadedListener.md)!:to be [notified](../android/graphics/drawable/Icon.OnDrawableLoadedListener.md))when [loadDrawable(android.content.Context)](Icon.md))finished |
| `handler` | [Handler](../android.os/Handler.md)!: [Handler](../android.os/Handler.md) on which to notify the`listener` |
| --- | --- |

### loadDrawableAsync

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadDrawableAsync(
    context: Context, 
    andThen: Message
): Unit
```

Invokes [loadDrawable(android.content.Context)](Icon.md))on the given [Handler](../android.os/Handler.md) and then sends`andThen`to the same Handler when finished.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md): [Context](../android.content/Context.md) in which to load the drawable; see [loadDrawable(android.content.Context)](Icon.md))This value cannot be`null`. |
| `andThen` | [Message](../android.os/Message.md): [android.os.Message](../android.os/Message.md) to send to its target once the drawable is available. The [obj](../android.os/Message.md) property is populated with the Drawable. This value cannot be`null`. |

### setTint

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTint(tint: Int): Icon
```

Store a color to use whenever this Icon is drawn.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a color, as in [Drawable.setTint(int)](Drawable.md)) |

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Icon](Icon.md) | this same object, for use in chained construction This value cannot be`null`. |

### setTintBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTintBlendMode(mode: BlendMode): Icon
```

Store a blending mode to use whenever this Icon is drawn.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [BlendMode](../android.graphics/BlendMode.md):a blending mode, as in [Drawable.setTintMode(PorterDuff.Mode)](Drawable.md)), may be null |

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Icon](Icon.md) | this same object, for use in chained construction This value cannot be`null`. |

### setTintList

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTintList(tintList: ColorStateList!): Icon
```

Store a color to use whenever this Icon is drawn.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tintList` | [ColorStateList](../android.content.res/ColorStateList.md)!:as in [Drawable.setTintList(ColorStateList)](Drawable.md)), null to remove tint |

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Icon](Icon.md) | this same object, for use in chained construction This value cannot be`null`. |

### setTintMode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTintMode(mode: PorterDuff.Mode): Icon
```

Store a blending mode to use whenever this Icon is drawn.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md):a blending mode, as in [Drawable.setTintMode(PorterDuff.Mode)](Drawable.md)), may be null |

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Icon](Icon.md) | this same object, for use in chained construction This value cannot be`null`. |

### toString

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Icon!>
```
