# TextElementListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextElementListener

Kotlin| [Java](TextElementListener.md) 
| --- | --- |

```
interface TextElementListener : EndTextElementListener, StartElementListener
```

| [android.sax.TextElementListener](TextElementListener.md) |

Listens for the beginning and ending of text elements.

## Summary

| Inherited functions ||
|---|---|
| From class [EndTextElementListener](EndTextElementListener.md) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](EndTextElementListener.md))`(`body:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Invoked at the end of a text element with the body of the element. <br /> | ||
| From class [StartElementListener](StartElementListener.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](StartElementListener.md))`(`attributes:` ` [Attributes](../org.xml.sax/Attributes.md)!`)` <br /> Invoked at the beginning of an element. <br /> | ||
