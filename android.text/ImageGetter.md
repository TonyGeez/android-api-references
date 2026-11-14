# Html.ImageGetter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ImageGetter

Kotlin| [Java](../android/text/Html.ImageGetter.md) 
| --- | --- |

```
interface ImageGetter
```

| [android.text.Html.ImageGetter](../android/text/Html.ImageGetter.md) |

Retrieves images for HTML \<img\> tags.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Drawable](../android/graphics/drawable/Drawable.md)! | [getDrawable](../android/text/Html.ImageGetter.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` This method is called when the HTML parser encounters an \<img\> tag. |

## Public methods

### getDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDrawable(source: String!): Drawable!
```

This method is called when the HTML parser encounters an \<img\> tag. The`source`argument is the string from the "src" attribute; the return value should be a Drawable representation of the image or`null`for a generic replacement image. Make sure you call setBounds() on your Drawable if it doesn't already have its bounds set.
