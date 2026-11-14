# ElementListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ElementListener

Kotlin| [Java](../android/sax/ElementListener.md) 
| --- | --- |

```
interface ElementListener : EndElementListener, StartElementListener
```

| [android.sax.ElementListener](../android/sax/ElementListener.md) |

Listens for the beginning and ending of elements.

## Summary

| Inherited functions ||
|---|---|
| From class [EndElementListener](../android/sax/EndElementListener.md) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](../android/sax/EndElementListener.md))`()` <br /> Invoked at the end of an element. <br /> | ||
| From class [StartElementListener](../android/sax/StartElementListener.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](../android/sax/StartElementListener.md))`(`attributes:` ` [Attributes](../org/xml/sax/Attributes.md)!`)` <br /> Invoked at the beginning of an element. <br /> | ||
