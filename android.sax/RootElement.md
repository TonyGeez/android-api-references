# RootElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RootElement

Kotlin| [Java](../android/sax/RootElement.md) 
| --- | --- |

```
open class RootElement : Element
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.sax.Element](../android/sax/Element.md) ||
| | ↳ | [android.sax.RootElement](../android/sax/RootElement.md) |

The root XML element. The entry point for this API. Not safe for concurrent use.

For example, passing this XML: 

```kotlin
<feed xmlns='http://www.w3.org/2005/Atom'>
    <entry>
      <id>bob</id>
    </entry>
  </feed>
  
```
to this code: 

```kotlin
static final String ATOM_NAMESPACE = "http://www.w3.org/2005/Atom";
 
  ...
 
  RootElement root = new RootElement(ATOM_NAMESPACE, "feed");
  Element entry = root.getChild(ATOM_NAMESPACE, "entry");
  entry.getChild(ATOM_NAMESPACE, "id").setEndTextElementListener(
    new EndTextElementListener() {
      public void end(String body) {
        System.out.println("Entry ID: " + body);
      }
    });
 
  XMLReader reader = ...;
  reader.setContentHandler(root.getContentHandler());
  reader.parse(...);
  
```
would output: 

```kotlin
Entry ID: bob
  
```

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RootElement](../android/sax/RootElement.md))`(`localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new root element with the given name. |
| [RootElement](../android/sax/RootElement.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new root element with the given name. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ContentHandler](../org/xml/sax/ContentHandler.md)! | [getContentHandler](../android/sax/RootElement.md))`()` Gets the SAX`ContentHandler`. |

| Inherited functions ||
|---|---|
| From class [Element](../android/sax/Element.md) |----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Element](../android/sax/Element.md)! | [getChild](../android/sax/Element.md))`(`localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Gets the child element with the given name. Uses an empty string as the namespace. <br /> | | [Element](../android/sax/Element.md)! | [getChild](../android/sax/Element.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Gets the child element with the given name. <br /> | | [Element](../android/sax/Element.md)! | [requireChild](../android/sax/Element.md))`(`localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Gets the child element with the given name. Uses an empty string as the namespace. We will throw a [org.xml.sax.SAXException](../org/xml/sax/SAXException.md) at parsing time if the specified child is missing. This helps you ensure that your listeners are called. <br /> | | [Element](../android/sax/Element.md)! | [requireChild](../android/sax/Element.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Gets the child element with the given name. We will throw a [org.xml.sax.SAXException](../org/xml/sax/SAXException.md) at parsing time if the specified child is missing. This helps you ensure that your listeners are called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setElementListener](../android/sax/Element.md))`(`elementListener:` ` [ElementListener](../android/sax/ElementListener.md)!`)` <br /> Sets start and end element listeners at the same time. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEndElementListener](../android/sax/Element.md))`(`endElementListener:` ` [EndElementListener](../android/sax/EndElementListener.md)!`)` <br /> Sets a listener for the end of this element. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEndTextElementListener](../android/sax/Element.md))`(`endTextElementListener:` ` [EndTextElementListener](../android/sax/EndTextElementListener.md)!`)` <br /> Sets a listener for the end of this text element. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStartElementListener](../android/sax/Element.md))`(`startElementListener:` ` [StartElementListener](../android/sax/StartElementListener.md)!`)` <br /> Sets a listener for the start of this element. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTextElementListener](../android/sax/Element.md))`(`elementListener:` ` [TextElementListener](../android/sax/TextElementListener.md)!`)` <br /> Sets start and end text element listeners at the same time. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/sax/Element.md))`()` <br /> | ||

## Public constructors

### RootElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RootElement(localName: String!)
```

Constructs a new root element with the given name. Uses an empty string as the namespace.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------|
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the local name |

### RootElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RootElement(
    uri: String!, 
    localName: String!)
```

Constructs a new root element with the given name.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the namespace |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the local name |

## Public methods

### getContentHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContentHandler(): ContentHandler!
```

Gets the SAX`ContentHandler`. Pass this to your SAX parser.
