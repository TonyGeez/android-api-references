# TextElementListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextElementListener

Kotlin| [Java](../android/sax/TextElementListener.md) 
| --- | --- |

```
interface TextElementListener : EndTextElementListener, StartElementListener
```

| [android.sax.TextElementListener](../android/sax/TextElementListener.md) |

Listens for the beginning and ending of text elements.

## Summary

| Inherited functions ||
|---|---|
| From class [EndTextElementListener](../android/sax/EndTextElementListener.md) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](../android/sax/EndTextElementListener.md))`(`body:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Invoked at the end of a text element with the body of the element. <br /> | ||
| From class [StartElementListener](../android/sax/StartElementListener.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](../android/sax/StartElementListener.md))`(`attributes:` ` [Attributes](../org/xml/sax/Attributes.md)!`)` <br /> Invoked at the beginning of an element. <br /> | ||
