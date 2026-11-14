# Element

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Element

Kotlin| [Java](https://developer.android.com/reference/android/sax/Element "View this page in Java") 
| --- | --- |

```
open class Element
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.sax.Element](https://developer.android.com/reference/kotlin/android/sax/Element#) |

| Known Direct Subclasses [RootElement](https://developer.android.com/reference/kotlin/android/sax/RootElement) |---------------------------------------------------------------------------------------|-----------------------| | [RootElement](https://developer.android.com/reference/kotlin/android/sax/RootElement) | The root XML element. | |
| --- | --- | --- | --- | --- | --- | --- |

An XML element. Provides access to child elements and hooks to listen for events related to this element.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Element](https://developer.android.com/reference/kotlin/android/sax/Element#)! | [getChild](https://developer.android.com/reference/kotlin/android/sax/Element#getChild(kotlin.String))`(`localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets the child element with the given name. |
| open [Element](https://developer.android.com/reference/kotlin/android/sax/Element#)! | [getChild](https://developer.android.com/reference/kotlin/android/sax/Element#getChild(kotlin.String,%20kotlin.String))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets the child element with the given name. |
| open [Element](https://developer.android.com/reference/kotlin/android/sax/Element#)! | [requireChild](https://developer.android.com/reference/kotlin/android/sax/Element#requireChild(kotlin.String))`(`localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets the child element with the given name. |
| --- | --- |
| open [Element](https://developer.android.com/reference/kotlin/android/sax/Element#)! | [requireChild](https://developer.android.com/reference/kotlin/android/sax/Element#requireChild(kotlin.String,%20kotlin.String))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets the child element with the given name. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setElementListener](https://developer.android.com/reference/kotlin/android/sax/Element#setElementListener(android.sax.ElementListener))`(`elementListener:` ` [ElementListener](https://developer.android.com/reference/kotlin/android/sax/ElementListener)!`)` Sets start and end element listeners at the same time. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEndElementListener](https://developer.android.com/reference/kotlin/android/sax/Element#setEndElementListener(android.sax.EndElementListener))`(`endElementListener:` ` [EndElementListener](https://developer.android.com/reference/kotlin/android/sax/EndElementListener)!`)` Sets a listener for the end of this element. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEndTextElementListener](https://developer.android.com/reference/kotlin/android/sax/Element#setEndTextElementListener(android.sax.EndTextElementListener))`(`endTextElementListener:` ` [EndTextElementListener](https://developer.android.com/reference/kotlin/android/sax/EndTextElementListener)!`)` Sets a listener for the end of this text element. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStartElementListener](https://developer.android.com/reference/kotlin/android/sax/Element#setStartElementListener(android.sax.StartElementListener))`(`startElementListener:` ` [StartElementListener](https://developer.android.com/reference/kotlin/android/sax/StartElementListener)!`)` Sets a listener for the start of this element. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTextElementListener](https://developer.android.com/reference/kotlin/android/sax/Element#setTextElementListener(android.sax.TextElementListener))`(`elementListener:` ` [TextElementListener](https://developer.android.com/reference/kotlin/android/sax/TextElementListener)!`)` Sets start and end text element listeners at the same time. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/sax/Element#toString())`()` <br /> |

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

Gets the child element with the given name. Uses an empty string as the namespace. We will throw a [org.xml.sax.SAXException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException.html#) at parsing time if the specified child is missing. This helps you ensure that your listeners are called. 

### requireChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requireChild(
    uri: String!, 
    localName: String!
): Element!
```

Gets the child element with the given name. We will throw a [org.xml.sax.SAXException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException.html#) at parsing time if the specified child is missing. This helps you ensure that your listeners are called. 

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
