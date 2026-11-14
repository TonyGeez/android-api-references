# Icon

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Icon

Kotlin| [Java](https://developer.android.com/reference/android/graphics/drawable/Icon "View this page in Java") 

```
class Icon : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.graphics.drawable.Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) |

An umbrella container for several serializable graphics representations, including Bitmaps, compressed bitmap images (e.g. JPG or PNG), and drawable resources (including vectors). [Much ink](https://developer.android.com/training/displaying-bitmaps/index.html) has been spilled on the best way to load images, and many clients may have different needs when it comes to threading and fetching. This class is therefore focused on encapsulation rather than behavior.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnDrawableLoadedListener](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.OnDrawableLoadedListener) Implement this interface to receive a callback when [loadDrawableAsync](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#loadDrawableAsync(android.content.Context,%20android.graphics.drawable.Icon.OnDrawableLoadedListener,%20android.os.Handler))is finished and your Drawable is ready. |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ADAPTIVE_BITMAP](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#TYPE_ADAPTIVE_BITMAP:kotlin.Int) An icon that was created using [Icon.createWithAdaptiveBitmap](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#createWithAdaptiveBitmap(android.graphics.Bitmap)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BITMAP](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#TYPE_BITMAP:kotlin.Int) An icon that was created using [Icon.createWithBitmap(Bitmap)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#createWithBitmap(android.graphics.Bitmap)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_DATA](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#TYPE_DATA:kotlin.Int) An icon that was created using[Icon.createWithData(byte[], int, int)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#createWithData(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RESOURCE](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#TYPE_RESOURCE:kotlin.Int) An icon that was created using android. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_URI](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#TYPE_URI:kotlin.Int) An icon that was created using android. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_URI_ADAPTIVE_BITMAP](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#TYPE_URI_ADAPTIVE_BITMAP:kotlin.Int) An icon that was created using android. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | [createWithAdaptiveBitmap](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#createWithAdaptiveBitmap(android.graphics.Bitmap))`(`bits:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!`)` Create an Icon pointing to a bitmap in memory that follows the icon design guideline defined by [AdaptiveIconDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AdaptiveIconDrawable). |
| static [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | [createWithAdaptiveBitmapContentUri](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#createWithAdaptiveBitmapContentUri(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` Create an Icon pointing to an image file specified by URI. |
| static [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | [createWithAdaptiveBitmapContentUri](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#createWithAdaptiveBitmapContentUri(kotlin.String))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Create an Icon pointing to an image file specified by URI. |
| static [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | [createWithBitmap](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#createWithBitmap(android.graphics.Bitmap))`(`bits:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!`)` Create an Icon pointing to a bitmap in memory. |
| static [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | [createWithContentUri](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#createWithContentUri(android.net.Uri))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`)` Create an Icon pointing to an image file specified by URI. |
| static [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | [createWithContentUri](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#createWithContentUri(kotlin.String))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create an Icon pointing to an image file specified by URI. |
| static [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | [createWithData](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#createWithData(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create an Icon pointing to a compressed bitmap stored in a byte array. |
| static [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | [createWithFilePath](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#createWithFilePath(kotlin.String))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create an Icon pointing to an image file specified by path. |
| static [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | [createWithResource](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#createWithResource(android.content.Context,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create an Icon pointing to a drawable resource. |
| static [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | [createWithResource](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#createWithResource(kotlin.String,%20kotlin.Int))`(`resPackage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create an Icon pointing to a drawable resource. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#describeContents())`()` Parcelable interface |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResId](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#getResId())`()` Gets the resource used to create this icon. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getResPackage](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#getResPackage())`()` Gets the package used to create this icon. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#getType())`()` Gets the type of the icon provided. |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | [getUri](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#getUri())`()` Gets the uri used to create this icon. |
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)? | [loadDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#loadDrawable(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Returns a Drawable that can be used to draw the image inside this Icon, constructing it if necessary. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadDrawableAsync](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#loadDrawableAsync(android.content.Context,%20android.graphics.drawable.Icon.OnDrawableLoadedListener,%20android.os.Handler))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `listener:` ` [Icon.OnDrawableLoadedListener](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.OnDrawableLoadedListener)!`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!`)` Invokes [loadDrawable(android.content.Context)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#loadDrawable(android.content.Context))on a background thread and notifies the` ` [listener](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.OnDrawableLoadedListener#onDrawableLoaded(android.graphics.drawable.Drawable))` `on the`handler`when finished. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadDrawableAsync](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#loadDrawableAsync(android.content.Context,%20android.os.Message))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `andThen:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)`)` Invokes [loadDrawable(android.content.Context)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#loadDrawable(android.content.Context))on the given [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#) and then sends`andThen`to the same Handler when finished. |
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | [setTint](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#setTint(kotlin.Int))`(`tint:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Store a color to use whenever this Icon is drawn. |
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | [setTintBlendMode](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#setTintBlendMode(android.graphics.BlendMode))`(`mode:` ` [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#)`)` Store a blending mode to use whenever this Icon is drawn. |
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | [setTintList](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#setTintList(android.content.res.ColorStateList))`(`tintList:` ` [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)!`)` Store a color to use whenever this Icon is drawn. |
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | [setTintMode](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#setTintMode(android.graphics.PorterDuff.Mode))`(`mode:` ` [PorterDuff.Mode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#)`)` Store a blending mode to use whenever this Icon is drawn. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### TYPE_ADAPTIVE_BITMAP

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ADAPTIVE_BITMAP: Int
```

An icon that was created using [Icon.createWithAdaptiveBitmap](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#createWithAdaptiveBitmap(android.graphics.Bitmap)). 

 Value: 5

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#getType()) 

### TYPE_BITMAP

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_BITMAP: Int
```

An icon that was created using [Icon.createWithBitmap(Bitmap)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#createWithBitmap(android.graphics.Bitmap)). 

 Value: 1

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#getType()) 

### TYPE_DATA

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_DATA: Int
```

An icon that was created using[Icon.createWithData(byte[], int, int)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#createWithData(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)). 

 Value: 3

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#getType()) 

### TYPE_RESOURCE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_RESOURCE: Int
```

An icon that was created using android.graphics.drawable.Icon#createWithResource. 

 Value: 2

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#getType()) 

### TYPE_URI

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_URI: Int
```

An icon that was created using android.graphics.drawable.Icon#createWithContentUri or [Icon.createWithFilePath(String)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#createWithFilePath(kotlin.String)). 

 Value: 4

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#getType()) 

### TYPE_URI_ADAPTIVE_BITMAP

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_URI_ADAPTIVE_BITMAP: Int
```

An icon that was created using android.graphics.drawable.Icon#createWithAdaptiveBitmapContentUri. 

 Value: 6

**See Also**

- [#getType](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#getType())

## Public methods

### createWithAdaptiveBitmap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createWithAdaptiveBitmap(bits: Bitmap!): Icon
```

Create an Icon pointing to a bitmap in memory that follows the icon design guideline defined by [AdaptiveIconDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AdaptiveIconDrawable).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bits` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!:A valid [android.graphics.Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#) object |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | This value cannot be`null`. |

### createWithAdaptiveBitmapContentUri

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createWithAdaptiveBitmapContentUri(uri: Uri): Icon
```

Create an Icon pointing to an image file specified by URI. Image file should follow the icon design guideline defined by [AdaptiveIconDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AdaptiveIconDrawable).

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):A uri referring to local content:// or file:// image data. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | This value cannot be`null`. |

### createWithAdaptiveBitmapContentUri

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createWithAdaptiveBitmapContentUri(uri: String): Icon
```

Create an Icon pointing to an image file specified by URI. Image file should follow the icon design guideline defined by [AdaptiveIconDrawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/AdaptiveIconDrawable).

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):A uri referring to local content:// or file:// image data. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | This value cannot be`null`. |

### createWithBitmap

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createWithBitmap(bits: Bitmap!): Icon
```

Create an Icon pointing to a bitmap in memory.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bits` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!:A valid [android.graphics.Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#) object |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | This value cannot be`null`. |

### createWithContentUri

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createWithContentUri(uri: Uri!): Icon
```

Create an Icon pointing to an image file specified by URI.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:A uri referring to local content:// or file:// image data. |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | This value cannot be`null`. |

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
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | This value cannot be`null`. |

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
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:Byte array storing compressed bitmap data of a type that [android.graphics.BitmapFactory](https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.html#) can decode (see [android.graphics.Bitmap.CompressFormat](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.CompressFormat.html#)). |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset into`data`at which the bitmap data starts |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Length of the bitmap data |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | This value cannot be`null`. |

### createWithFilePath

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createWithFilePath(path: String!): Icon
```

Create an Icon pointing to an image file specified by path.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A path to a file that contains compressed bitmap data of a type that [android.graphics.BitmapFactory](https://developer.android.com/reference/kotlin/android/graphics/BitmapFactory.html#) can decode. |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | This value cannot be`null`. |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The context for the application whose resources should be used to resolve the given resource ID. |
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):ID of the drawable resource |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | This value cannot be`null`. |

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
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | This value cannot be`null`. |

### describeContents

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Parcelable interface

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getResId

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getResId(): Int
```

Gets the resource used to create this icon.

Only valid for icons of type [TYPE_RESOURCE](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#TYPE_RESOURCE:kotlin.Int). Note: This resource may not be available if the application changes at all, and it is up to the caller to ensure safety if this resource is re-used and/or persisted. 

### getResPackage

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getResPackage(): String
```

Gets the package used to create this icon.

Only valid for icons of type [TYPE_RESOURCE](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#TYPE_RESOURCE:kotlin.Int). Note: This package may not be available if referenced in the future, and it is up to the caller to ensure safety if this package is re-used and/or persisted.

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.graphics.drawable.Icon#TYPE_BITMAP](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#TYPE_BITMAP:kotlin.Int), [android.graphics.drawable.Icon#TYPE_RESOURCE](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#TYPE_RESOURCE:kotlin.Int), [android.graphics.drawable.Icon#TYPE_DATA](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#TYPE_DATA:kotlin.Int), [android.graphics.drawable.Icon#TYPE_URI](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#TYPE_URI:kotlin.Int), [android.graphics.drawable.Icon#TYPE_ADAPTIVE_BITMAP](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#TYPE_ADAPTIVE_BITMAP:kotlin.Int), or [android.graphics.drawable.Icon#TYPE_URI_ADAPTIVE_BITMAP](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#TYPE_URI_ADAPTIVE_BITMAP:kotlin.Int) |

### getUri

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUri(): Uri
```

Gets the uri used to create this icon.

Only valid for icons of type [TYPE_URI](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#TYPE_URI:kotlin.Int) and [TYPE_URI_ADAPTIVE_BITMAP](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#TYPE_URI_ADAPTIVE_BITMAP:kotlin.Int). Note: This uri may not be available in the future, and it is up to the caller to ensure safety if this uri is re-used and/or persisted.

| Return ||
|-----------------------------------------------------------------------------|-----------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | This value cannot be`null`. |

### loadDrawable

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadDrawable(context: Context!): Drawable?
```

Returns a Drawable that can be used to draw the image inside this Icon, constructing it if necessary. Depending on the type of image, this may not be something you want to do on the UI thread, so consider using [loadDrawableAsync](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#loadDrawableAsync(android.content.Context,%20android.os.Message))instead.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) in which to load the drawable; used to access [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#), for example. |

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable)? | A fresh instance of a drawable for this image, yours to keep. This value may be`null`. |

### loadDrawableAsync

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadDrawableAsync(
    context: Context, 
    listener: Icon.OnDrawableLoadedListener!, 
    handler: Handler!
): Unit
```

Invokes [loadDrawable(android.content.Context)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#loadDrawable(android.content.Context))on a background thread and notifies the` ` [listener](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.OnDrawableLoadedListener#onDrawableLoaded(android.graphics.drawable.Drawable))` `on the`handler`when finished.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) in which to load the drawable; see [loadDrawable(android.content.Context)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#loadDrawable(android.content.Context))This value cannot be`null`. |
| `listener` | [Icon.OnDrawableLoadedListener](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.OnDrawableLoadedListener)!:to be [notified](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.OnDrawableLoadedListener#onDrawableLoaded(android.graphics.drawable.Drawable))when [loadDrawable(android.content.Context)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#loadDrawable(android.content.Context))finished |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!: [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#) on which to notify the`listener` |

### loadDrawableAsync

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadDrawableAsync(
    context: Context, 
    andThen: Message
): Unit
```

Invokes [loadDrawable(android.content.Context)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#loadDrawable(android.content.Context))on the given [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#) and then sends`andThen`to the same Handler when finished.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) in which to load the drawable; see [loadDrawable(android.content.Context)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#loadDrawable(android.content.Context))This value cannot be`null`. |
| `andThen` | [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#): [android.os.Message](https://developer.android.com/reference/kotlin/android/os/Message.html#) to send to its target once the drawable is available. The [obj](https://developer.android.com/reference/kotlin/android/os/Message.html#obj:kotlin.Any) property is populated with the Drawable. This value cannot be`null`. |

### setTint

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTint(tint: Int): Icon
```

Store a color to use whenever this Icon is drawn.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a color, as in [Drawable.setTint(int)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTint(kotlin.Int)) |

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | this same object, for use in chained construction This value cannot be`null`. |

### setTintBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTintBlendMode(mode: BlendMode): Icon
```

Store a blending mode to use whenever this Icon is drawn.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#):a blending mode, as in [Drawable.setTintMode(PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintMode(android.graphics.PorterDuff.Mode)), may be null |

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | this same object, for use in chained construction This value cannot be`null`. |

### setTintList

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTintList(tintList: ColorStateList!): Icon
```

Store a color to use whenever this Icon is drawn.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tintList` | [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)!:as in [Drawable.setTintList(ColorStateList)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintList(android.content.res.ColorStateList)), null to remove tint |

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | this same object, for use in chained construction This value cannot be`null`. |

### setTintMode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTintMode(mode: PorterDuff.Mode): Icon
```

Store a blending mode to use whenever this Icon is drawn.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [PorterDuff.Mode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#):a blending mode, as in [Drawable.setTintMode(PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable#setTintMode(android.graphics.PorterDuff.Mode)), may be null |

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon#) | this same object, for use in chained construction This value cannot be`null`. |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Icon!>
```
