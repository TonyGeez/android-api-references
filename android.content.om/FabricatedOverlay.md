# FabricatedOverlay

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FabricatedOverlay

Kotlin| [Java](https://developer.android.com/reference/android/content/om/FabricatedOverlay "View this page in Java") 

```
open class FabricatedOverlay
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.content.om.FabricatedOverlay](https://developer.android.com/reference/kotlin/android/content/om/FabricatedOverlay#) |

FabricatedOverlay describes the content of Fabricated Runtime Resource Overlay (FRRO) that is used to overlay the app's resources. The app should register the [FabricatedOverlay](https://developer.android.com/reference/kotlin/android/content/om/FabricatedOverlay#) instance in an [OverlayManagerTransaction](https://developer.android.com/reference/kotlin/android/content/om/OverlayManagerTransaction) by calling [android.content.om.OverlayManagerTransaction#registerFabricatedOverlay(android.content.om.FabricatedOverlay)](https://developer.android.com/reference/kotlin/android/content/om/OverlayManagerTransaction#registerFabricatedOverlay(android.content.om.FabricatedOverlay)). The FRRO is created once the transaction is committed successfully.

The app creates a FabricatedOverlay to describe the how to overlay string, integer, and file type resources. Before creating any frro, please define a target overlayable in`res/values/overlayable.xml`that describes what kind of resources can be overlaid, what kind of roles or applications can overlay the resources. Here is an example. 

```kotlin
<code>&lt;overlayable name="SignatureOverlayable" actor="overlay://theme"&gt;
      &lt;!-- The app with the same signature can overlay the below resources --&gt;
      &lt;policy type="signature"&gt;
          &lt;item type="color" name="mycolor" /&gt;
          &lt;item type="string" name="mystring" /&gt;
      &lt;/policy&gt;
  &lt;/overlayable&gt;
  </code>
```

The overlay must assign the target overlayable name just like the above example by calling [setTargetOverlayable(java.lang.String)](https://developer.android.com/reference/kotlin/android/content/om/FabricatedOverlay#setTargetOverlayable(kotlin.String)). Here is an example: 

```kotlin
<code>FabricatedOverlay fabricatedOverlay = new FabricatedOverlay("overlay_name",
                                                              context.getPackageName());
  fabricatedOverlay.setTargetOverlayable("SignatureOverlayable")
  fabricatedOverlay.setResourceValue("mycolor", TypedValue.TYPE_INT_COLOR_ARGB8, Color.White)
  fabricatedOverlay.setResourceValue("mystring", TypedValue.TYPE_STRING, "Hello")
  </code>
```

The app can create any [FabricatedOverlay](https://developer.android.com/reference/kotlin/android/content/om/FabricatedOverlay#) instance by calling the following APIs.

- [setTargetOverlayable(java.lang.String)](https://developer.android.com/reference/kotlin/android/content/om/FabricatedOverlay#setTargetOverlayable(kotlin.String))
- [setResourceValue(java.lang.String,int,int,java.lang.String)](https://developer.android.com/reference/kotlin/android/content/om/FabricatedOverlay#setResourceValue(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.String))
- [setResourceValue(java.lang.String,int,java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/content/om/FabricatedOverlay#setResourceValue(kotlin.String,%20kotlin.Int,%20kotlin.String,%20kotlin.String))
- [setResourceValue(java.lang.String,android.os.ParcelFileDescriptor,java.lang.String)](https://developer.android.com/reference/kotlin/android/content/om/FabricatedOverlay#setResourceValue(kotlin.String,%20android.os.ParcelFileDescriptor,%20kotlin.String))

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FabricatedOverlay](https://developer.android.com/reference/kotlin/android/content/om/FabricatedOverlay#FabricatedOverlay(kotlin.String,%20kotlin.String))`(`overlayName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `targetPackage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Create a fabricated overlay to overlay on the specified package. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [OverlayIdentifier](https://developer.android.com/reference/kotlin/android/content/om/OverlayIdentifier) | [getIdentifier](https://developer.android.com/reference/kotlin/android/content/om/FabricatedOverlay#getIdentifier())`()` Retrieves the identifier for this fabricated overlay. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNinePatchResourceValue](https://developer.android.com/reference/kotlin/android/content/om/FabricatedOverlay#setNinePatchResourceValue(kotlin.String,%20android.os.ParcelFileDescriptor,%20kotlin.String))`(`resourceName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)`, `configuration:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Sets the resource value in the fabricated overlay from a nine patch. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResourceValue](https://developer.android.com/reference/kotlin/android/content/om/FabricatedOverlay#setResourceValue(kotlin.String,%20android.content.res.AssetFileDescriptor,%20kotlin.String))`(`resourceName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#)`, `configuration:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Sets the resource value in the fabricated overlay for the file descriptor type with the configuration. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResourceValue](https://developer.android.com/reference/kotlin/android/content/om/FabricatedOverlay#setResourceValue(kotlin.String,%20android.os.ParcelFileDescriptor,%20kotlin.String))`(`resourceName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)`, `configuration:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Sets the resource value in the fabricated overlay for the file descriptor type with the configuration. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResourceValue](https://developer.android.com/reference/kotlin/android/content/om/FabricatedOverlay#setResourceValue(kotlin.String,%20kotlin.Float,%20kotlin.Int,%20kotlin.String))`(`resourceName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `dimensionValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `dimensionUnit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `configuration:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Sets the resource value in the fabricated overlay for the dimension type with the given configuration. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResourceValue](https://developer.android.com/reference/kotlin/android/content/om/FabricatedOverlay#setResourceValue(kotlin.String,%20kotlin.Float,%20kotlin.String))`(`resourceName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `configuration:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Sets the resource value in the fabricated overlay for the float type with the given configuration. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResourceValue](https://developer.android.com/reference/kotlin/android/content/om/FabricatedOverlay#setResourceValue(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.String))`(`resourceName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `dataType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `configuration:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Sets the resource value in the fabricated overlay for the integer-like types with the configuration. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResourceValue](https://developer.android.com/reference/kotlin/android/content/om/FabricatedOverlay#setResourceValue(kotlin.String,%20kotlin.Int,%20kotlin.String,%20kotlin.String))`(`resourceName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `dataType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `configuration:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Sets the resource value in the fabricated overlay for the string-like type with the configuration. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTargetOverlayable](https://developer.android.com/reference/kotlin/android/content/om/FabricatedOverlay#setTargetOverlayable(kotlin.String))`(`targetOverlayable:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Set the target overlayable name of the overlay The target package defines may define several overlayables. |

## Public constructors

### FabricatedOverlay

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FabricatedOverlay(
    overlayName: String, 
    targetPackage: String)
```

Create a fabricated overlay to overlay on the specified package.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `overlayName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):a name used to uniquely identify the fabricated overlay owned by the caller itself. This value cannot be`null`. |
| `targetPackage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the package to be overlaid This value cannot be`null`. |

## Public methods

### getIdentifier

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIdentifier(): OverlayIdentifier
```

Retrieves the identifier for this fabricated overlay.

| Return ||
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [OverlayIdentifier](https://developer.android.com/reference/kotlin/android/content/om/OverlayIdentifier) | the overlay identifier This value cannot be`null`. |

### setNinePatchResourceValue

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNinePatchResourceValue(
    resourceName: String, 
    value: ParcelFileDescriptor, 
    configuration: String?
): Unit
```

Sets the resource value in the fabricated overlay from a nine patch.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resourceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name of the target resource to overlay (in the form \[package\]:type/entry) This value cannot be`null`. |
| `value` | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#):the file descriptor whose contents are the value of the frro This value cannot be`null`. |
| `configuration` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string representation of the config this overlay is enabled for This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | This value cannot be`null`. |

### setResourceValue

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setResourceValue(
    resourceName: String, 
    value: AssetFileDescriptor, 
    configuration: String?
): Unit
```

Sets the resource value in the fabricated overlay for the file descriptor type with the configuration.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resourceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name of the target resource to overlay (in the form \[package\]:type/entry) This value cannot be`null`. |
| `value` | [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#):the file descriptor whose contents are the value of the frro This value cannot be`null`. |
| `configuration` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string representation of the config this overlay is enabled for This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | This value cannot be`null`. |

### setResourceValue

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setResourceValue(
    resourceName: String, 
    value: ParcelFileDescriptor, 
    configuration: String?
): Unit
```

Sets the resource value in the fabricated overlay for the file descriptor type with the configuration.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resourceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name of the target resource to overlay (in the form \[package\]:type/entry) This value cannot be`null`. |
| `value` | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#):the file descriptor whose contents are the value of the frro This value cannot be`null`. |
| `configuration` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string representation of the config this overlay is enabled for This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | This value cannot be`null`. |

### setResourceValue

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setResourceValue(
    resourceName: String, 
    dimensionValue: Float, 
    dimensionUnit: Int, 
    configuration: String?
): Unit
```

Sets the resource value in the fabricated overlay for the dimension type with the given configuration.

This can be used to overlay dimension resources of the following formats. 

```kotlin
<dimen name="foo">10dp</dimen>
  <dimen name="foo">10sp</dimen>
  <dimen name="foo">10px</dimen>
  <dimen name="foo">10mm</dimen>
  <dimen name="foo">10in</dimen>
  <dimen name="foo">10pt</dimen>
  
```
For overlaying unitless dimension resources, use [setResourceValue(java.lang.String,float,java.lang.String)](https://developer.android.com/reference/kotlin/android/content/om/FabricatedOverlay#setResourceValue(kotlin.String,%20kotlin.Float,%20kotlin.String))instead.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resourceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name of the target resource to overlay (in the form \[package\]:type/entry) This value cannot be`null`. |
| `dimensionValue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the float representing the dimension value |
| `dimensionUnit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the integer representing the dimension unit Value is [android.util.TypedValue#COMPLEX_UNIT_PX](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PX:kotlin.Int), [android.util.TypedValue#COMPLEX_UNIT_DIP](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_DIP:kotlin.Int), [android.util.TypedValue#COMPLEX_UNIT_SP](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_SP:kotlin.Int), [android.util.TypedValue#COMPLEX_UNIT_PT](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_PT:kotlin.Int), [android.util.TypedValue#COMPLEX_UNIT_IN](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_IN:kotlin.Int), or [android.util.TypedValue#COMPLEX_UNIT_MM](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#COMPLEX_UNIT_MM:kotlin.Int) |
| `configuration` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string representation of the config this overlay is enabled for This value may be`null`. |

### setResourceValue

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setResourceValue(
    resourceName: String, 
    value: Float, 
    configuration: String?
): Unit
```

Sets the resource value in the fabricated overlay for the float type with the given configuration.

This can be used to overlay unitless float resources of the following format. 

```kotlin
<item name="foo" format="float" type="dimen">0.015</item>
  
```
For overlaying dimension resources with units, use [setResourceValue(java.lang.String,float,int,java.lang.String)](https://developer.android.com/reference/kotlin/android/content/om/FabricatedOverlay#setResourceValue(kotlin.String,%20kotlin.Float,%20kotlin.Int,%20kotlin.String))instead.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resourceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name of the target resource to overlay (in the form \[package\]:type/entry) This value cannot be`null`. |
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the float representing the new value |
| `configuration` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string representation of the config this overlay is enabled for This value may be`null`. |

| Exceptions ||
|--------------------------------------|---------------------------------|
| `java.lang.IllegalArgumentException` | If the resource name is invalid |

### setResourceValue

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setResourceValue(
    resourceName: String, 
    dataType: Int, 
    value: Int, 
    configuration: String?
): Unit
```

Sets the resource value in the fabricated overlay for the integer-like types with the configuration.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resourceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name of the target resource to overlay (in the form \[package\]:type/entry) This value cannot be`null`. |
| `dataType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the data type of the new value Value is between [android.util.TypedValue#TYPE_FIRST_INT](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#TYPE_FIRST_INT:kotlin.Int) and [android.util.TypedValue#TYPE_LAST_INT](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#TYPE_LAST_INT:kotlin.Int) inclusive |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the integer representing the new value |
| `configuration` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string representation of the config this overlay is enabled for This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | This value cannot be`null`. |

**See Also**

- [android.util.TypedValue#TYPE_INT_COLOR_ARGB8](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#TYPE_INT_COLOR_ARGB8:kotlin.Int) 

### setResourceValue

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setResourceValue(
    resourceName: String, 
    dataType: Int, 
    value: String, 
    configuration: String?
): Unit
```

Sets the resource value in the fabricated overlay for the string-like type with the configuration.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resourceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name of the target resource to overlay (in the form \[package\]:type/entry) This value cannot be`null`. |
| `dataType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the data type of the new value Value is [android.util.TypedValue#TYPE_STRING](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#TYPE_STRING:kotlin.Int) |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the string representing the new value This value cannot be`null`. |
| `configuration` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string representation of the config this overlay is enabled for This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | This value cannot be`null`. |

**See Also**

- [android.util.TypedValue#TYPE_STRING](https://developer.android.com/reference/kotlin/android/util/TypedValue.html#TYPE_STRING:kotlin.Int) 

### setTargetOverlayable

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTargetOverlayable(targetOverlayable: String?): Unit
```

Set the target overlayable name of the overlay The target package defines may define several overlayables. The [FabricatedOverlay](https://developer.android.com/reference/kotlin/android/content/om/FabricatedOverlay#) should specify which overlayable to be overlaid.

| Parameters ||
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `targetOverlayable` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:the overlayable name defined in target package. This value may be`null`. |
