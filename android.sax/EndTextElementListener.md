# EndTextElementListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EndTextElementListener

Kotlin| [Java](EndTextElementListener.md) 
| --- | --- |

```
interface EndTextElementListener
```

| [android.sax.EndTextElementListener](EndTextElementListener.md) |

| Known Direct Subclasses [TextElementListener](TextElementListener.md) |-------------------------------------------------------------------------------------------------------|--------------------------------------------------------| | [TextElementListener](TextElementListener.md) | Listens for the beginning and ending of text elements. | |
| --- | --- | --- | --- | --- | --- | --- |

Listens for the end of text elements.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](EndTextElementListener.md))`(`body:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Invoked at the end of a text element with the body of the element. |

## Public methods

### end

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun end(body: String!): Unit
```

Invoked at the end of a text element with the body of the element.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------|
| `body` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:of the element |
