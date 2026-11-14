# PointerIcon

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PointerIcon

Kotlin| [Java](PointerIcon.md) 
| --- | --- |

```
class PointerIcon : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.PointerIcon](PointerIcon.md) |

Represents an icon that can be used as a mouse pointer.

Pointer icons can be provided either by the system using system types, or by applications using bitmaps or application resources.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ALIAS](PointerIcon.md) Type constant: alias (indicating an alias of/shortcut to something is to be created. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ALL_SCROLL](PointerIcon.md) Type constant: all-scroll. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ARROW](PointerIcon.md) Type constant: Arrow icon. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_CELL](PointerIcon.md) Type constant: cell. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_CONTEXT_MENU](PointerIcon.md) Type constant: context-menu. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_COPY](PointerIcon.md) Type constant: copy. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_CROSSHAIR](PointerIcon.md) Type constant: crosshair. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_DEFAULT](PointerIcon.md) The default pointer icon. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_GRAB](PointerIcon.md) Type constant: grab. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_GRABBING](PointerIcon.md) Type constant: grabbing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_HAND](PointerIcon.md) Type constant: hand. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_HANDWRITING](PointerIcon.md) Type constant: handwriting. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_HELP](PointerIcon.md) Type constant: help. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_HORIZONTAL_DOUBLE_ARROW](PointerIcon.md) Type constant: horizontal double arrow mainly for resizing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NO_DROP](PointerIcon.md) Type constant: no-drop. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NULL](PointerIcon.md) Type constant: Null icon. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT](PointerIcon.md) Type constant: text. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOP_LEFT_DIAGONAL_DOUBLE_ARROW](PointerIcon.md) Type constant: diagonal double arrow -- top-left to bottom-right. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOP_RIGHT_DIAGONAL_DOUBLE_ARROW](PointerIcon.md) Type constant: diagonal double arrow -- top-right to bottom-left. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VERTICAL_DOUBLE_ARROW](PointerIcon.md) Type constant: vertical double arrow mainly for resizing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VERTICAL_TEXT](PointerIcon.md) Type constant: vertical-text. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_WAIT](PointerIcon.md) Type constant: wait. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ZOOM_IN](PointerIcon.md) Type constant: zoom-in. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ZOOM_OUT](PointerIcon.md) Type constant: zoom-out. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [PointerIcon](PointerIcon.md) | [create](PointerIcon.md))`(`bitmap:` ` [Bitmap](../android.graphics/Bitmap.md)`, `hotSpotX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `hotSpotY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Creates a custom pointer icon from the given bitmap and hotspot information. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](PointerIcon.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](PointerIcon.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| --- | --- |
| static [PointerIcon](PointerIcon.md) | [getSystemIcon](PointerIcon.md))`(`context:` ` [Context](../android.content/Context.md)`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets a system pointer icon for the given type. |
| static [PointerIcon](PointerIcon.md) | [load](PointerIcon.md))`(`resources:` ` [Resources](../android.content.res/Resources.md)`, `resourceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Loads a custom pointer icon from an XML resource. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](PointerIcon.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](PointerIcon.md))`(`out:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PointerIcon](PointerIcon.md)!\> | [CREATOR](PointerIcon.md) <br /> |

## Constants

### TYPE_ALIAS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ALIAS: Int
```

Type constant: alias (indicating an alias of/shortcut to something is to be created. 

 Value: 1010

### TYPE_ALL_SCROLL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ALL_SCROLL: Int
```

Type constant: all-scroll. 

 Value: 1013

### TYPE_ARROW

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ARROW: Int
```

Type constant: Arrow icon. (Default mouse pointer) 

 Value: 1000

### TYPE_CELL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_CELL: Int
```

Type constant: cell. 

 Value: 1006

### TYPE_CONTEXT_MENU

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_CONTEXT_MENU: Int
```

Type constant: context-menu. 

 Value: 1001

### TYPE_COPY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_COPY: Int
```

Type constant: copy. 

 Value: 1011

### TYPE_CROSSHAIR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_CROSSHAIR: Int
```

Type constant: crosshair. 

 Value: 1007

### TYPE_DEFAULT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_DEFAULT: Int
```

**Deprecated:** *This is the same as using [TYPE_ARROW](PointerIcon.md). Use [TYPE_ARROW](PointerIcon.md) to explicitly show an arrow, or use a`null` [PointerIcon](PointerIcon.md) with [View.setPointerIcon(PointerIcon)](View.md))or [View.onResolvePointerIcon(MotionEvent, int)](View.md))instead to show the default pointer icon.*

The default pointer icon. 

 Value: 1000

### TYPE_GRAB

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_GRAB: Int
```

Type constant: grab. 

 Value: 1020

### TYPE_GRABBING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_GRABBING: Int
```

Type constant: grabbing. 

 Value: 1021

### TYPE_HAND

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_HAND: Int
```

Type constant: hand. 

 Value: 1002

### TYPE_HANDWRITING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_HANDWRITING: Int
```

Type constant: handwriting. 

 Value: 1022

### TYPE_HELP

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_HELP: Int
```

Type constant: help. 

 Value: 1003

### TYPE_HORIZONTAL_DOUBLE_ARROW

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_HORIZONTAL_DOUBLE_ARROW: Int
```

Type constant: horizontal double arrow mainly for resizing. 

 Value: 1014

### TYPE_NO_DROP

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_NO_DROP: Int
```

Type constant: no-drop. 

 Value: 1012

### TYPE_NULL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_NULL: Int
```

Type constant: Null icon. It has no bitmap. 

 Value: 0

### TYPE_TEXT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT: Int
```

Type constant: text. 

 Value: 1008

### TYPE_TOP_LEFT_DIAGONAL_DOUBLE_ARROW

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TOP_LEFT_DIAGONAL_DOUBLE_ARROW: Int
```

Type constant: diagonal double arrow -- top-left to bottom-right. 

 Value: 1017

### TYPE_TOP_RIGHT_DIAGONAL_DOUBLE_ARROW

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TOP_RIGHT_DIAGONAL_DOUBLE_ARROW: Int
```

Type constant: diagonal double arrow -- top-right to bottom-left. 

 Value: 1016

### TYPE_VERTICAL_DOUBLE_ARROW

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VERTICAL_DOUBLE_ARROW: Int
```

Type constant: vertical double arrow mainly for resizing. 

 Value: 1015

### TYPE_VERTICAL_TEXT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VERTICAL_TEXT: Int
```

Type constant: vertical-text. 

 Value: 1009

### TYPE_WAIT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_WAIT: Int
```

Type constant: wait. 

 Value: 1004

### TYPE_ZOOM_IN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ZOOM_IN: Int
```

Type constant: zoom-in. 

 Value: 1018

### TYPE_ZOOM_OUT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ZOOM_OUT: Int
```

Type constant: zoom-out. 

 Value: 1019

## Public methods

### create

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun create(
    bitmap: Bitmap, 
    hotSpotX: Float, 
    hotSpotY: Float
): PointerIcon
```

Creates a custom pointer icon from the given bitmap and hotspot information.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bitmap` | [Bitmap](../android.graphics/Bitmap.md):The bitmap for the icon. This value cannot be`null`. |
| `hotSpotX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The X offset of the pointer icon hotspot in the bitmap. Must be within the \[0, bitmap.getWidth()) range. |
| `hotSpotY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The Y offset of the pointer icon hotspot in the bitmap. Must be within the \[0, bitmap.getHeight()) range. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [PointerIcon](PointerIcon.md) | A pointer icon for this bitmap. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if bitmap is null, or if the x/y hotspot parameters are invalid. |

### describeContents

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `other` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getSystemIcon

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getSystemIcon(
    context: Context, 
    type: Int
): PointerIcon
```

Gets a system pointer icon for the given type.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md):The context. This value cannot be`null`. |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The pointer icon type. |

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------|
| [PointerIcon](PointerIcon.md) | The pointer icon. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|---------------------|
| `java.lang.IllegalArgumentException` | if context is null. |

### load

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun load(
    resources: Resources, 
    resourceId: Int
): PointerIcon
```

Loads a custom pointer icon from an XML resource.

The XML resource should have the following form:` <?xml version="1.0" encoding="utf-8"?> <pointer-icon xmlns:android="http://schemas.android.com/apk/res/android" android:bitmap="@drawable/my_pointer_bitmap" android:hotSpotX="24" android:hotSpotY="24" /> `

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `resources` | [Resources](../android.content.res/Resources.md):The resources object. This value cannot be`null`. |
| `resourceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource id. |

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------|
| [PointerIcon](PointerIcon.md) | The pointer icon. This value cannot be`null`. |

| Exceptions ||
|---------------------------------------------------|-------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if resources is null. |
| `android.content.res.Resources.NotFoundException` | if the resource was not found or the drawable linked in the resource was not found. |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<PointerIcon!>
```
