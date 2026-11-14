# AudioMetadata.Key

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Key

Kotlin| [Java](https://developer.android.com/reference/android/media/AudioMetadata.Key "View this page in Java") 
| --- | --- |

```
interface Key<T : Any!>
```

| [android.media.AudioMetadata.Key](https://developer.android.com/reference/kotlin/android/media/AudioMetadata.Key#) |

Key interface for the`AudioMetadata`map.

The presence of this`Key`interface on an object allows it to reference metadata in the Audio Framework.

Vendors are allowed to implement this`Key`interface for their debugging or private application use. To avoid name conflicts, vendor key names should be qualified by the vendor company name followed by a dot; for example, "vendorCompany.someVolume".

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getName](https://developer.android.com/reference/kotlin/android/media/AudioMetadata.Key#getName())`()` Returns the internal name of the key. |
| abstract [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\> | [getValueClass](https://developer.android.com/reference/kotlin/android/media/AudioMetadata.Key#getValueClass())`()` Returns the class type`T`of the associated value. |

## Public methods

### getName

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getName(): String
```

Returns the internal name of the key. The name should be unique in the`AudioMetadata`namespace. Vendors should prefix their keys with the company name followed by a dot.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getValueClass

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getValueClass(): Class<T>
```

Returns the class type`T`of the associated value. Valid class types for [android.os.Build.VERSION_CODES#R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) are`Integer.class`,`Long.class`,`Float.class`,`Double.class`,`String.class`.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T> | This value cannot be`null`. |
