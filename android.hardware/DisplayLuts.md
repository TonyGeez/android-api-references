Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DisplayLuts

```
class DisplayLuts
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.DisplayLuts](DisplayLuts.md) |

DisplayLuts provides the developers to apply Lookup Tables (Luts) to a `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.html#`. Luts provides ways to control tonemapping for specific content. The general flow for how DisplayLuts fits into a display pipeline is as follows:

DisplayLuts flow

<br />

Or in list form:

1. A `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.html#`'s content is converted to RGB colors, if the source is YUV.
2. The RGB colors are de-gammed into linear values, normalized to the range of \[0, 1\].
3. The linear values are passed through a 1D LUT (if set). The 1D LUT looks up and applies gain multipliers.
4. The linear values are passed through a 3D LUT (if set). The 3D LUT maps input colors to a final linear color.
5. The output values are transformed to the panel color gamut, and then gammed to arrive at the final color.

Importantly: the LUT is applied on colors in linear space, in the source content's color gamut.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/hardware/DisplayLuts.Entry` <br /> |

| Public constructors ||
|---|---|
| DisplayLuts Create a DisplayLuts instance. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | set Set a Lut to be applied. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | set Set Luts in order to be applied. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| --- | --- |

## Public constructors

### DisplayLuts

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DisplayLuts()
```

Create a DisplayLuts instance.

## Public methods

### set

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun set(entry: DisplayLuts.Entry): Unit
```

Set a Lut to be applied.

Use either this or set. The function will replace any previously set lut(s).

| Parameters ||
|---|---|
| `entry` | [DisplayLuts.Entry](../android/hardware/DisplayLuts.Entry.md): Either an 1D Lut or a 3D Lut. This value cannot be `null`. |

### set

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun set(
    first: DisplayLuts.Entry, 
    second: DisplayLuts.Entry
): Unit
```

Set Luts in order to be applied.

An 1D Lut and 3D Lut will be applied in order. Use either this or set. The function will replace any previously set lut(s)

| Parameters ||
|---|---|
| `first` | [DisplayLuts.Entry](../android/hardware/DisplayLuts.Entry.md): An 1D Lut. This value cannot be `null`. |
| `second` | [DisplayLuts.Entry](../android/hardware/DisplayLuts.Entry.md): A 3D Lut. This value cannot be `null`. |

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
