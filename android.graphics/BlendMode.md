# BlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BlendMode

Kotlin| [Java](BlendMode.md) 
| --- | --- |

```
class BlendMode
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [android.graphics.BlendMode](BlendMode.md)\> ||
| | ↳ | [android.graphics.BlendMode](BlendMode.md) |

| Known Direct Subclasses [BlendMode.CLEAR](BlendMode.md), [BlendMode.COLOR](BlendMode.md), [BlendMode.COLOR_BURN](BlendMode.md), [BlendMode.COLOR_DODGE](BlendMode.md), [BlendMode.DARKEN](BlendMode.md), [BlendMode.DIFFERENCE](BlendMode.md), [BlendMode.DST](BlendMode.md), [BlendMode.DST_ATOP](BlendMode.md), [BlendMode.DST_IN](BlendMode.md), [BlendMode.DST_OUT](BlendMode.md), [BlendMode.DST_OVER](BlendMode.md), [BlendMode.EXCLUSION](BlendMode.md), and 17 others. |---------------------------------------------------------------------------------------------------------------------------|--------| | [BlendMode.CLEAR](BlendMode.md) | <br /> | | [BlendMode.COLOR](BlendMode.md) | <br /> | | [BlendMode.COLOR_BURN](BlendMode.md) | <br /> | | [BlendMode.COLOR_DODGE](BlendMode.md) | <br /> | | [BlendMode.DARKEN](BlendMode.md) | <br /> | | [BlendMode.DIFFERENCE](BlendMode.md) | <br /> | | [BlendMode.DST](BlendMode.md) | <br /> | | [BlendMode.DST_ATOP](BlendMode.md) | <br /> | | [BlendMode.DST_IN](BlendMode.md) | <br /> | | [BlendMode.DST_OUT](BlendMode.md) | <br /> | | [BlendMode.DST_OVER](BlendMode.md) | <br /> | | [BlendMode.EXCLUSION](BlendMode.md) | <br /> | | [BlendMode.HARD_LIGHT](BlendMode.md) | <br /> | | [BlendMode.HUE](BlendMode.md) | <br /> | | [BlendMode.LIGHTEN](BlendMode.md) | <br /> | | [BlendMode.LUMINOSITY](BlendMode.md) | <br /> | | [BlendMode.MODULATE](BlendMode.md) | <br /> | | [BlendMode.MULTIPLY](BlendMode.md) | <br /> | | [BlendMode.OVERLAY](BlendMode.md) | <br /> | | [BlendMode.PLUS](BlendMode.md) | <br /> | | [BlendMode.SATURATION](BlendMode.md) | <br /> | | [BlendMode.SCREEN](BlendMode.md) | <br /> | | [BlendMode.SOFT_LIGHT](BlendMode.md) | <br /> | | [BlendMode.SRC](BlendMode.md) | <br /> | | [BlendMode.SRC_ATOP](BlendMode.md) | <br /> | | [BlendMode.SRC_IN](BlendMode.md) | <br /> | | [BlendMode.SRC_OUT](BlendMode.md) | <br /> | | [BlendMode.SRC_OVER](BlendMode.md) | <br /> | | [BlendMode.XOR](BlendMode.md) | <br /> | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Summary

| Enum values ||
|------------------------------------------------------------------------------------------------------------------------|---|
| [CLEAR](BlendMode.md) <br /> |
| [COLOR](BlendMode.md) <br /> |
| [COLOR_BURN](BlendMode.md) <br /> |
| [COLOR_DODGE](BlendMode.md) <br /> |
| [DARKEN](BlendMode.md) <br /> |
| [DIFFERENCE](BlendMode.md) <br /> |
| [DST](BlendMode.md) <br /> |
| [DST_ATOP](BlendMode.md) <br /> |
| [DST_IN](BlendMode.md) <br /> |
| [DST_OUT](BlendMode.md) <br /> |
| [DST_OVER](BlendMode.md) <br /> |
| [EXCLUSION](BlendMode.md) <br /> |
| [HARD_LIGHT](BlendMode.md) <br /> |
| [HUE](BlendMode.md) <br /> |
| [LIGHTEN](BlendMode.md) <br /> |
| [LUMINOSITY](BlendMode.md) <br /> |
| [MODULATE](BlendMode.md) <br /> |
| [MULTIPLY](BlendMode.md) <br /> |
| [OVERLAY](BlendMode.md) <br /> |
| [PLUS](BlendMode.md) <br /> |
| [SATURATION](BlendMode.md) <br /> |
| [SCREEN](BlendMode.md) <br /> |
| [SOFT_LIGHT](BlendMode.md) <br /> |
| [SRC](BlendMode.md) <br /> |
| [SRC_ATOP](BlendMode.md) <br /> |
| [SRC_IN](BlendMode.md) <br /> |
| [SRC_OUT](BlendMode.md) <br /> |
| [SRC_OVER](BlendMode.md) <br /> |
| [XOR](BlendMode.md) <br /> |

## Enum values

### CLEAR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val CLEAR : BlendMode
```

<br />

Destination pixels covered by the source are cleared to 0.

<br />

\\(\\alpha_{out} = 0\\)

\\(C_{out} = 0\\) 

### COLOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val COLOR : BlendMode
```

<br />

Replaces hue and saturation of destination with hue and saturation of source, leaving luminosity unchanged.

<br />

### COLOR_BURN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val COLOR_BURN : BlendMode
```

<br />

Makes destination darker to reflect source.

<br />

\\(\\alpha_{out} = \\alpha_{src} + \\alpha_{dst} - \\alpha_{src} \* \\alpha_{dst}\\)

\\begin{equation} C_{out} = \\begin{cases} C_{dst} + C_{src}\*(1 - \\alpha_{dst}) \& C_{dst} = \\alpha_{dst} \\\\ \\alpha_{dst}\*(1 - \\alpha_{src}) \& C_{src} = 0 \\\\ \\alpha_{src}\*(\\alpha_{dst} - min(\\alpha_{dst}, (\\alpha_{dst} - C_{dst})\*\\alpha_{src}/C_{src})) + C_{src} \* (1 - \\alpha_{dst}) + \\alpha_{dst}\*(1-\\alpha_{src}) \& otherwise \\end{cases} \\end{equation} 

### COLOR_DODGE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val COLOR_DODGE : BlendMode
```

<br />

Makes destination brighter to reflect source.

<br />

\\(\\alpha_{out} = \\alpha_{src} + \\alpha_{dst} - \\alpha_{src} \* \\alpha_{dst}\\)

\\begin{equation} C_{out} = \\begin{cases} C_{src} \* (1 - \\alpha_{dst}) \& C_{dst} = 0 \\\\ C_{src} + \\alpha_{dst}\*(1 - \\alpha_{src}) \& C_{src} = \\alpha_{src} \\\\ \\alpha_{src} \* min(\\alpha_{dst}, C_{dst} \* \\alpha_{src}/(\\alpha_{src} - C_{src})) + C_{src} \*(1 - \\alpha_{dst} + \\alpha_{dst}\*(1 - \\alpha_{src}) \& otherwise \\end{cases} \\end{equation} 

### DARKEN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val DARKEN : BlendMode
```

<br />

Retains the smallest component of the source and destination pixels.

<br />

\\(\\alpha_{out} = \\alpha_{src} + \\alpha_{dst} - \\alpha_{src} \* \\alpha_{dst}\\)

\\(C_{out} = (1 - \\alpha_{dst}) \* C_{src} + (1 - \\alpha_{src}) \* C_{dst} + min(C_{src}, C_{dst})\\) 

### DIFFERENCE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val DIFFERENCE : BlendMode
```

<br />

Subtracts darker from lighter with higher contrast.

<br />

\\begin{equation} \\alpha_{out} = \\alpha_{src} + \\alpha_{dst} - \\alpha_{src} \* \\alpha_{dst} \\end{equation}

\\begin{equation} C_{out} = C_{src} + C_{dst} - 2 \* min(C_{src} \* \\alpha_{dst}, C_{dst} \* \\alpha_{src}) \\end{equation} 

### DST

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val DST : BlendMode
```

<br />

The source pixels are discarded, leaving the destination intact.

<br />

\\(\\alpha_{out} = \\alpha_{dst}\\)

\\(C_{out} = C_{dst}\\) 

### DST_ATOP

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val DST_ATOP : BlendMode
```

<br />

Discards the destination pixels that are not covered by source pixels. Draws remaining destination pixels over source pixels.

<br />

\\(\\alpha_{out} = \\alpha_{src}\\)

\\(C_{out} = \\alpha_{src} \* C_{dst} + (1 - \\alpha_{dst}) \* C_{src}\\) 

### DST_IN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val DST_IN : BlendMode
```

<br />

Keeps the destination pixels that cover source pixels, discards the remaining source and destination pixels.

<br />

\\(\\alpha_{out} = \\alpha_{src} \* \\alpha_{dst}\\)

\\(C_{out} = C_{dst} \* \\alpha_{src}\\) 

### DST_OUT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val DST_OUT : BlendMode
```

<br />

Keeps the destination pixels that are not covered by source pixels. Discards destination pixels that are covered by source pixels. Discards all source pixels.

<br />

\\(\\alpha_{out} = (1 - \\alpha_{src}) \* \\alpha_{dst}\\)

\\(C_{out} = (1 - \\alpha_{src}) \* C_{dst}\\) 

### DST_OVER

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val DST_OVER : BlendMode
```

<br />

The source pixels are drawn behind the destination pixels.

<br />

\\(\\alpha_{out} = \\alpha_{dst} + (1 - \\alpha_{dst}) \* \\alpha_{src}\\)

\\(C_{out} = C_{dst} + (1 - \\alpha_{dst}) \* C_{src}\\) 

### EXCLUSION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val EXCLUSION : BlendMode
```

<br />

Subtracts darker from lighter with lower contrast.

<br />

\\begin{equation} \\alpha_{out} = \\alpha_{src} + \\alpha_{dst} - \\alpha_{src} \* \\alpha_{dst} \\end{equation}

\\begin{equation} C_{out} = C_{src} + C_{dst} - 2 \* C_{src} \* C_{dst} \\end{equation} 

### HARD_LIGHT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val HARD_LIGHT : BlendMode
```

<br />

Makes destination lighter or darker, depending on source.

<br />

\\(\\alpha_{out} = \\alpha_{src} + \\alpha_{dst} - \\alpha_{src} \* \\alpha_{dst}\\)

\\begin{equation} C_{out} = \\begin{cases} 2\*C_{src}\*C_{dst} \& C_{src}\*(1-\\alpha_{dst}) + C_{dst}\*(1-\\alpha_{src}) + 2\*C_{src} \\leq \\alpha_{src} \\\\ \\alpha_{src}\*\\alpha_{dst}- 2\*(\\alpha_{dst} - C_{dst})\*(\\alpha_{src} - C_{src}) \& otherwise \\end{cases} \\end{equation} 

### HUE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val HUE : BlendMode
```

<br />

Replaces hue of destination with hue of source, leaving saturation and luminosity unchanged.

<br />

### LIGHTEN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val LIGHTEN : BlendMode
```

<br />

Retains the largest component of the source and destination pixel.

<br />

\\(\\alpha_{out} = \\alpha_{src} + \\alpha_{dst} - \\alpha_{src} \* \\alpha_{dst}\\)

\\(C_{out} = (1 - \\alpha_{dst}) \* C_{src} + (1 - \\alpha_{src}) \* C_{dst} + max(C_{src}, C_{dst})\\) 

### LUMINOSITY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val LUMINOSITY : BlendMode
```

<br />

Replaces luminosity of destination with luminosity of source, leaving hue and saturation unchanged.

<br />

### MODULATE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val MODULATE : BlendMode
```

<br />

Multiplies the source and destination pixels.

<br />

\\(\\alpha_{out} = \\alpha_{src} \* \\alpha_{dst}\\)

\\(C_{out} = C_{src} \* C_{dst}\\) 

### MULTIPLY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val MULTIPLY : BlendMode
```

<br />

Multiplies the source and destination pixels.

<br />

\\(\\alpha_{out} = \\alpha_{src} + \\alpha_{dst} - \\alpha_{src} \* \\alpha_{dst}\\)

\\(C_{out} = C_{src} \* (1 - \\alpha_{dst}) + C_{dst} \* (1 - \\alpha_{src}) + (C_{src} \* C_{dst})\\) 

### OVERLAY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val OVERLAY : BlendMode
```

<br />

Multiplies or screens the source and destination depending on the destination color.

<br />

\\(\\alpha_{out} = \\alpha_{src} + \\alpha_{dst} - \\alpha_{src} \* \\alpha_{dst}\\)

\\(\\begin{equation} C_{out} = \\begin{cases} 2 \* C_{src} \* C_{dst} \& 2 \* C_{dst} \\lt \\alpha_{dst} \\\\ \\alpha_{src} \* \\alpha_{dst} - 2 (\\alpha_{dst} - C_{src}) (\\alpha_{src} - C_{dst}) \& otherwise \\end{cases} \\end{equation}\\) 

### PLUS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val PLUS : BlendMode
```

<br />

Adds the source pixels to the destination pixels and saturates the result.

<br />

\\(\\alpha_{out} = max(0, min(\\alpha_{src} + \\alpha_{dst}, 1))\\)

\\(C_{out} = max(0, min(C_{src} + C_{dst}, 1))\\) 

### SATURATION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SATURATION : BlendMode
```

<br />

Replaces saturation of destination saturation hue of source, leaving hue and luminosity unchanged.

<br />

### SCREEN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SCREEN : BlendMode
```

<br />

Adds the source and destination pixels, then subtracts the source pixels multiplied by the destination.

<br />

\\(\\alpha_{out} = \\alpha_{src} + \\alpha_{dst} - \\alpha_{src} \* \\alpha_{dst}\\)

\\(C_{out} = C_{src} + C_{dst} - C_{src} \* C_{dst}\\) 

### SOFT_LIGHT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SOFT_LIGHT : BlendMode
```

<br />

Makes destination lighter or darker, depending on source.

<br />

Where \\begin{equation} m = \\begin{cases} C_{dst} / \\alpha_{dst} \& \\alpha_{dst} \\gt 0 \\\\ 0 \& otherwise \\end{cases} \\end{equation}

\\begin{equation} g = \\begin{cases} (16 \* m \* m + 4 \* m) \* (m - 1) + 7 \* m \& 4 \* C_{dst} \\leq \\alpha_{dst} \\\\ \\sqrt m - m \& otherwise \\end{cases} \\end{equation}

\\begin{equation} f = \\begin{cases} C_{dst} \* (\\alpha_{src} + (2 \* C_{src} - \\alpha_{src}) \* (1 - m)) \& 2 \* C_{src} \\leq \\alpha_{src} \\\\ C_{dst} \* \\alpha_{src} + \\alpha_{dst} \* (2 \* C_{src} - \\alpha_{src}) \* g \& otherwise \\end{cases} \\end{equation}

\\begin{equation} \\alpha_{out} = \\alpha_{src} + \\alpha_{dst} - \\alpha_{src} \* \\alpha_{dst} \\end{equation} \\begin{equation} C_{out} = C_{src} / \\alpha_{dst} + C_{dst} / \\alpha_{src} + f \\end{equation} 

### SRC

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SRC : BlendMode
```

<br />

The source pixels replace the destination pixels.

<br />

\\(\\alpha_{out} = \\alpha_{src}\\)

\\(C_{out} = C_{src}\\) 

### SRC_ATOP

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SRC_ATOP : BlendMode
```

<br />

Discards the source pixels that do not cover destination pixels. Draws remaining source pixels over destination pixels.

<br />

\\(\\alpha_{out} = \\alpha_{dst}\\)

\\(C_{out} = \\alpha_{dst} \* C_{src} + (1 - \\alpha_{src}) \* C_{dst}\\) 

### SRC_IN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SRC_IN : BlendMode
```

<br />

Keeps the source pixels that cover the destination pixels, discards the remaining source and destination pixels.

<br />

\\(\\alpha_{out} = \\alpha_{src} \* \\alpha_{dst}\\)

\\(C_{out} = C_{src} \* \\alpha_{dst}\\) 

### SRC_OUT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SRC_OUT : BlendMode
```

<br />

Keeps the source pixels that do not cover destination pixels. Discards source pixels that cover destination pixels. Discards all destination pixels.

<br />

\\(\\alpha_{out} = (1 - \\alpha_{dst}) \* \\alpha_{src}\\)

\\(C_{out} = (1 - \\alpha_{dst}) \* C_{src}\\) 

### SRC_OVER

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SRC_OVER : BlendMode
```

<br />

The source pixels are drawn over the destination pixels.

<br />

\\(\\alpha_{out} = \\alpha_{src} + (1 - \\alpha_{src}) \* \\alpha_{dst}\\)

\\(C_{out} = C_{src} + (1 - \\alpha_{src}) \* C_{dst}\\) 

### XOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val XOR : BlendMode
```

<br />

Discards the source and destination pixels where source pixels cover destination pixels. Draws remaining source pixels.

<br />

\\(\\alpha_{out} = (1 - \\alpha_{dst}) \* \\alpha_{src} + (1 - \\alpha_{src}) \* \\alpha_{dst}\\)

\\(C_{out} = (1 - \\alpha_{dst}) \* C_{src} + (1 - \\alpha_{src}) \* C_{dst}\\)
