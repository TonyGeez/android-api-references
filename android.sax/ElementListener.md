# ElementListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ElementListener

Kotlin| [Java](https://developer.android.com/reference/android/sax/ElementListener "View this page in Java") 

```
interface ElementListener : EndElementListener, StartElementListener
```

| [android.sax.ElementListener](https://developer.android.com/reference/kotlin/android/sax/ElementListener#) |

Listens for the beginning and ending of elements.

## Summary

| Inherited functions ||
|---|---|
| From class [EndElementListener](https://developer.android.com/reference/kotlin/android/sax/EndElementListener) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](https://developer.android.com/reference/kotlin/android/sax/EndElementListener#end())`()` <br /> Invoked at the end of an element. <br /> | ||
| From class [StartElementListener](https://developer.android.com/reference/kotlin/android/sax/StartElementListener) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](https://developer.android.com/reference/kotlin/android/sax/StartElementListener#start(org.xml.sax.Attributes))`(`attributes:` ` [Attributes](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#)!`)` <br /> Invoked at the beginning of an element. <br /> | ||
