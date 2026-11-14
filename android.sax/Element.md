# Element

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Element

Kotlin| [Java](../android/sax/Element.md) 
| --- | --- |

```
open class Element
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.sax.Element](../android/sax/Element.md) |

| Known Direct Subclasses [RootElement](../android/sax/RootElement.md) |---------------------------------------------------------------------------------------|-----------------------| | [RootElement](../android/sax/RootElement.md) | The root XML element. | |
| --- | --- | --- | --- | --- | --- | --- |

An XML element. Provides access to child elements and hooks to listen for events related to this element.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Element](../android/sax/Element.md)! | [getChild](../android/sax/Element.md))`(`localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets the child element with the given name. |
| open [Element](../android/sax/Element.md)! | [getChild](../android/sax/Element.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets the child element with the given name. |
| open [Element](../android/sax/Element.md)! | [requireChild](../android/sax/Element.md))`(`localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets the child element with the given name. |
| --- | --- |
| open [Element](../android/sax/Element.md)! | [requireChild](../android/sax/Element.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets the child element with the given name. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setElementListener](../android/sax/Element.md))`(`elementListener:` ` [ElementListener](../android/sax/ElementListener.md)!`)` Sets start and end element listeners at the same time. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEndElementListener](../android/sax/Element.md))`(`endElementListener:` ` [EndElementListener](../android/sax/EndElementListener.md)!`)` Sets a listener for the end of this element. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEndTextElementListener](../android/sax/Element.md))`(`endTextElementListener:` ` [EndTextElementListener](../android/sax/EndTextElementListener.md)!`)` Sets a listener for the end of this text element. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStartElementListener](../android/sax/Element.md))`(`startElementListener:` ` [StartElementListener](../android/sax/StartElementListener.md)!`)` Sets a listener for the start of this element. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTextElementListener](../android/sax/Element.md))`(`elementListener:` ` [TextElementListener](../android/sax/TextElementListener.md)!`)` Sets start and end text element listeners at the same time. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/sax/Element.md))`()` <br /> |

## Public methods

### getChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChild(localName: String!): Element!
```

Gets the child element with the given name. Uses an empty string as the namespace. 

### getChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getChild(
    uri: String!, 
    localName: String!
): Element!
```

Gets the child element with the given name. 

### requireChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requireChild(localName: String!): Element!
```

Gets the child element with the given name. Uses an empty string as the namespace. We will throw a [org.xml.sax.SAXException](../org/xml/sax/SAXException.md) at parsing time if the specified child is missing. This helps you ensure that your listeners are called. 

### requireChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requireChild(
    uri: String!, 
    localName: String!
): Element!
```

Gets the child element with the given name. We will throw a [org.xml.sax.SAXException](../org/xml/sax/SAXException.md) at parsing time if the specified child is missing. This helps you ensure that your listeners are called. 

### setElementListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setElementListener(elementListener: ElementListener!): Unit
```

Sets start and end element listeners at the same time. 

### setEndElementListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEndElementListener(endElementListener: EndElementListener!): Unit
```

Sets a listener for the end of this element. 

### setEndTextElementListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEndTextElementListener(endTextElementListener: EndTextElementListener!): Unit
```

Sets a listener for the end of this text element. 

### setStartElementListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStartElementListener(startElementListener: StartElementListener!): Unit
```

Sets a listener for the start of this element. 

### setTextElementListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTextElementListener(elementListener: TextElementListener!): Unit
```

Sets start and end text element listeners at the same time. 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
