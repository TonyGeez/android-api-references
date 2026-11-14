# Layout.TextInclusionStrategy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextInclusionStrategy

Kotlin| [Java](../android/text/Layout.TextInclusionStrategy.md) 
| --- | --- |

```
@FunctionalInterface interface TextInclusionStrategy
```

| [android.text.Layout.TextInclusionStrategy](../android/text/Layout.TextInclusionStrategy.md) |

Strategy for determining whether a text segment is inside a rectangle area.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSegmentInside](../android/text/Layout.TextInclusionStrategy.md))`(`segmentBounds:` ` [RectF](../android.graphics/RectF.md)`, `area:` ` [RectF](../android.graphics/RectF.md)`)` Returns true if this [TextInclusionStrategy](../android/text/Layout.TextInclusionStrategy.md) considers the segment with bounds`segmentBounds`to be inside`area`. |

## Public methods

### isSegmentInside

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isSegmentInside(
    segmentBounds: RectF, 
    area: RectF
): Boolean
```

Returns true if this [TextInclusionStrategy](../android/text/Layout.TextInclusionStrategy.md) considers the segment with bounds`segmentBounds`to be inside`area`.

The segment is a range of text which does not cross line boundaries or directional run boundaries. The horizontal bounds of the segment are the start bound of the first character to the end bound of the last character. The vertical bounds match the line bounds (`getLineTop(line)`and`getLineBottom(line, false)`).

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------|
| `segmentBounds` | [RectF](../android.graphics/RectF.md):This value cannot be`null`. |
| `area` | [RectF](../android.graphics/RectF.md):This value cannot be`null`. |
