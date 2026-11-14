# Html.TagHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TagHandler

Kotlin| [Java](https://developer.android.com/reference/android/text/Html.TagHandler "View this page in Java") 
| --- | --- |

```
interface TagHandler
```

| [android.text.Html.TagHandler](https://developer.android.com/reference/kotlin/android/text/Html.TagHandler#) |

Is notified when HTML tags are encountered that the parser does not know how to interpret.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [handleTag](https://developer.android.com/reference/kotlin/android/text/Html.TagHandler#handleTag(kotlin.Boolean,%20kotlin.String,%20android.text.Editable,%20org.xml.sax.XMLReader))`(`opening:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `output:` ` [Editable](https://developer.android.com/reference/kotlin/android/text/Editable)!`, `xmlReader:` ` [XMLReader](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#)!`)` This method will be called whenn the HTML parser encounters a tag that it does not know how to interpret. |

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
