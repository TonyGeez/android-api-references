# FabricatedOverlay

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FabricatedOverlay

Kotlin| [Java](FabricatedOverlay.md) 
| --- | --- |

```
open class FabricatedOverlay
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.om.FabricatedOverlay](FabricatedOverlay.md) |

FabricatedOverlay describes the content of Fabricated Runtime Resource Overlay (FRRO) that is used to overlay the app's resources. The app should register the [FabricatedOverlay](FabricatedOverlay.md) instance in an [OverlayManagerTransaction](OverlayManagerTransaction.md) by calling [android.content.om.OverlayManagerTransaction#registerFabricatedOverlay(android.content.om.FabricatedOverlay)](OverlayManagerTransaction.md)). The FRRO is created once the transaction is committed successfully.

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

The overlay must assign the target overlayable name just like the above example by calling [setTargetOverlayable(java.lang.String)](FabricatedOverlay.md)). Here is an example: 

```kotlin
<code>FabricatedOverlay fabricatedOverlay = new FabricatedOverlay("overlay_name",
                                                              context.getPackageName());
  fabricatedOverlay.setTargetOverlayable("SignatureOverlayable")
  fabricatedOverlay.setResourceValue("mycolor", TypedValue.TYPE_INT_COLOR_ARGB8, Color.White)
  fabricatedOverlay.setResourceValue("mystring", TypedValue.TYPE_STRING, "Hello")
  </code>
```

The app can create any [FabricatedOverlay](FabricatedOverlay.md) instance by calling the following APIs.

- [setTargetOverlayable(java.lang.String)](FabricatedOverlay.md))
- [setResourceValue(java.lang.String,int,int,java.lang.String)](FabricatedOverlay.md))
- [setResourceValue(java.lang.String,int,java.lang.String,java.lang.String)](FabricatedOverlay.md))
- [setResourceValue(java.lang.String,android.os.ParcelFileDescriptor,java.lang.String)](FabricatedOverlay.md))

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FabricatedOverlay](FabricatedOverlay.md))`(`overlayName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `targetPackage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Create a fabricated overlay to overlay on the specified package. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [OverlayIdentifier](OverlayIdentifier.md) | [getIdentifier](FabricatedOverlay.md))`()` Retrieves the identifier for this fabricated overlay. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNinePatchResourceValue](FabricatedOverlay.md))`(`resourceName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)`, `configuration:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Sets the resource value in the fabricated overlay from a nine patch. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResourceValue](FabricatedOverlay.md))`(`resourceName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [AssetFileDescriptor](../android.content.res/AssetFileDescriptor.md)`, `configuration:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Sets the resource value in the fabricated overlay for the file descriptor type with the configuration. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResourceValue](FabricatedOverlay.md))`(`resourceName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)`, `configuration:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Sets the resource value in the fabricated overlay for the file descriptor type with the configuration. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResourceValue](FabricatedOverlay.md))`(`resourceName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `dimensionValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `dimensionUnit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `configuration:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Sets the resource value in the fabricated overlay for the dimension type with the given configuration. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResourceValue](FabricatedOverlay.md))`(`resourceName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `configuration:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Sets the resource value in the fabricated overlay for the float type with the given configuration. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResourceValue](FabricatedOverlay.md))`(`resourceName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `dataType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `configuration:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Sets the resource value in the fabricated overlay for the integer-like types with the configuration. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResourceValue](FabricatedOverlay.md))`(`resourceName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `dataType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `configuration:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Sets the resource value in the fabricated overlay for the string-like type with the configuration. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTargetOverlayable](FabricatedOverlay.md))`(`targetOverlayable:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Set the target overlayable name of the overlay The target package defines may define several overlayables. |
| --- | --- |

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
| [OverlayIdentifier](OverlayIdentifier.md) | the overlay identifier This value cannot be`null`. |

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
| `value` | [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md):the file descriptor whose contents are the value of the frro This value cannot be`null`. |
| `configuration` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string representation of the config this overlay is enabled for This value may be`null`. |
| --- | --- |

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
| `value` | [AssetFileDescriptor](../android.content.res/AssetFileDescriptor.md):the file descriptor whose contents are the value of the frro This value cannot be`null`. |
| `configuration` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string representation of the config this overlay is enabled for This value may be`null`. |
| --- | --- |

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
| `value` | [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md):the file descriptor whose contents are the value of the frro This value cannot be`null`. |
| `configuration` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string representation of the config this overlay is enabled for This value may be`null`. |
| --- | --- |

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
For overlaying unitless dimension resources, use [setResourceValue(java.lang.String,float,java.lang.String)](FabricatedOverlay.md))instead.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resourceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name of the target resource to overlay (in the form \[package\]:type/entry) This value cannot be`null`. |
| `dimensionValue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the float representing the dimension value |
| `dimensionUnit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the integer representing the dimension unit Value is [android.util.TypedValue#COMPLEX_UNIT_PX](../android.util/TypedValue.md), [android.util.TypedValue#COMPLEX_UNIT_DIP](../android.util/TypedValue.md), [android.util.TypedValue#COMPLEX_UNIT_SP](../android.util/TypedValue.md), [android.util.TypedValue#COMPLEX_UNIT_PT](../android.util/TypedValue.md), [android.util.TypedValue#COMPLEX_UNIT_IN](../android.util/TypedValue.md), or [android.util.TypedValue#COMPLEX_UNIT_MM](../android.util/TypedValue.md) |
| --- | --- |
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
For overlaying dimension resources with units, use [setResourceValue(java.lang.String,float,int,java.lang.String)](FabricatedOverlay.md))instead.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resourceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):name of the target resource to overlay (in the form \[package\]:type/entry) This value cannot be`null`. |
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the float representing the new value |
| `configuration` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string representation of the config this overlay is enabled for This value may be`null`. |
| --- | --- |

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
| `dataType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the data type of the new value Value is between [android.util.TypedValue#TYPE_FIRST_INT](../android.util/TypedValue.md) and [android.util.TypedValue#TYPE_LAST_INT](../android.util/TypedValue.md) inclusive |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the integer representing the new value |
| --- | --- |
| `configuration` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string representation of the config this overlay is enabled for This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | This value cannot be`null`. |

**See Also**

- [android.util.TypedValue#TYPE_INT_COLOR_ARGB8](../android.util/TypedValue.md) 

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
| `dataType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the data type of the new value Value is [android.util.TypedValue#TYPE_STRING](../android.util/TypedValue.md) |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the string representing the new value This value cannot be`null`. |
| --- | --- |
| `configuration` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The string representation of the config this overlay is enabled for This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | This value cannot be`null`. |

**See Also**

- [android.util.TypedValue#TYPE_STRING](../android.util/TypedValue.md) 

### setTargetOverlayable

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTargetOverlayable(targetOverlayable: String?): Unit
```

Set the target overlayable name of the overlay The target package defines may define several overlayables. The [FabricatedOverlay](FabricatedOverlay.md) should specify which overlayable to be overlaid.

| Parameters ||
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `targetOverlayable` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:the overlayable name defined in target package. This value may be`null`. |
