# TextElementListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextElementListener

Kotlin| [Java](https://developer.android.com/reference/android/sax/TextElementListener "View this page in Java") 

```
interface TextElementListener : EndTextElementListener, StartElementListener
```

| [android.sax.TextElementListener](https://developer.android.com/reference/kotlin/android/sax/TextElementListener#) |

Listens for the beginning and ending of text elements.

## Summary

| Inherited functions ||
|---|---|
| From class [EndTextElementListener](https://developer.android.com/reference/kotlin/android/sax/EndTextElementListener) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](https://developer.android.com/reference/kotlin/android/sax/EndTextElementListener#end(kotlin.String))`(`body:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Invoked at the end of a text element with the body of the element. <br /> | ||
| From class [StartElementListener](https://developer.android.com/reference/kotlin/android/sax/StartElementListener) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](https://developer.android.com/reference/kotlin/android/sax/StartElementListener#start(org.xml.sax.Attributes))`(`attributes:` ` [Attributes](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#)!`)` <br /> Invoked at the beginning of an element. <br /> | ||
