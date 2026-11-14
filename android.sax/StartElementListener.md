# StartElementListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StartElementListener

Kotlin| [Java](../android/sax/StartElementListener.md) 
| --- | --- |

```
interface StartElementListener
```

| [android.sax.StartElementListener](../android/sax/StartElementListener.md) |

| Known Direct Subclasses [ElementListener](../android/sax/ElementListener.md), [TextElementListener](../android/sax/TextElementListener.md) |-------------------------------------------------------------------------------------------------------|--------------------------------------------------------| | [ElementListener](../android/sax/ElementListener.md) | Listens for the beginning and ending of elements. | | [TextElementListener](../android/sax/TextElementListener.md) | Listens for the beginning and ending of text elements. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Listens for the beginning of elements.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](../android/sax/StartElementListener.md))`(`attributes:` ` [Attributes](../org/xml/sax/Attributes.md)!`)` Invoked at the beginning of an element. |

## Public methods

### start

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun start(attributes: Attributes!): Unit
```

Invoked at the beginning of an element.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------|
| `attributes` | [Attributes](../org/xml/sax/Attributes.md)!:from the element |
