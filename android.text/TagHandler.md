# Html.TagHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TagHandler

Kotlin| [Java](../android/text/Html.TagHandler.md) 
| --- | --- |

```
interface TagHandler
```

| [android.text.Html.TagHandler](../android/text/Html.TagHandler.md) |

Is notified when HTML tags are encountered that the parser does not know how to interpret.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [handleTag](../android/text/Html.TagHandler.md))`(`opening:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `output:` ` [Editable](../android/text/Editable.md)!`, `xmlReader:` ` [XMLReader](../org/xml/sax/XMLReader.md)!`)` This method will be called whenn the HTML parser encounters a tag that it does not know how to interpret. |

## Public methods

### handleTag

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun handleTag(
    opening: Boolean, 
    tag: String!, 
    output: Editable!, 
    xmlReader: XMLReader!
): Unit
```

This method will be called whenn the HTML parser encounters a tag that it does not know how to interpret.
