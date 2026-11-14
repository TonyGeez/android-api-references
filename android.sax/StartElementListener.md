# StartElementListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StartElementListener

Kotlin| [Java](https://developer.android.com/reference/android/sax/StartElementListener "View this page in Java") 
| --- | --- |

```
interface StartElementListener
```

| [android.sax.StartElementListener](https://developer.android.com/reference/kotlin/android/sax/StartElementListener#) |

| Known Direct Subclasses [ElementListener](https://developer.android.com/reference/kotlin/android/sax/ElementListener), [TextElementListener](https://developer.android.com/reference/kotlin/android/sax/TextElementListener) |-------------------------------------------------------------------------------------------------------|--------------------------------------------------------| | [ElementListener](https://developer.android.com/reference/kotlin/android/sax/ElementListener) | Listens for the beginning and ending of elements. | | [TextElementListener](https://developer.android.com/reference/kotlin/android/sax/TextElementListener) | Listens for the beginning and ending of text elements. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Listens for the beginning of elements.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](https://developer.android.com/reference/kotlin/android/sax/StartElementListener#start(org.xml.sax.Attributes))`(`attributes:` ` [Attributes](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#)!`)` Invoked at the beginning of an element. |

## Public methods

### start

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun start(attributes: Attributes!): Unit
```

Invoked at the beginning of an element.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------|
| `attributes` | [Attributes](https://developer.android.com/reference/kotlin/org/xml/sax/Attributes.html#)!:from the element |
