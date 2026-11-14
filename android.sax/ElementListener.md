# ElementListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ElementListener

Kotlin| [Java](ElementListener.md) 
| --- | --- |

```
interface ElementListener : EndElementListener, StartElementListener
```

| [android.sax.ElementListener](ElementListener.md) |

Listens for the beginning and ending of elements.

## Summary

| Inherited functions ||
|---|---|
| From class [EndElementListener](EndElementListener.md) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](EndElementListener.md))`()` <br /> Invoked at the end of an element. <br /> | ||
| From class [StartElementListener](StartElementListener.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](StartElementListener.md))`(`attributes:` ` [Attributes](../org.xml.sax/Attributes.md)!`)` <br /> Invoked at the beginning of an element. <br /> | ||
