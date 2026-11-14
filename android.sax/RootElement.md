# RootElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RootElement

Kotlin| [Java](RootElement.md) 
| --- | --- |

```
open class RootElement : Element
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.sax.Element](Element.md) ||
| | ↳ | [android.sax.RootElement](RootElement.md) |

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
| [RootElement](RootElement.md))`(`localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new root element with the given name. |
| [RootElement](RootElement.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new root element with the given name. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ContentHandler](../org.xml.sax/ContentHandler.md)! | [getContentHandler](RootElement.md))`()` Gets the SAX`ContentHandler`. |

| Inherited functions ||
|---|---|
| From class [Element](Element.md) |----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Element](Element.md)! | [getChild](Element.md))`(`localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Gets the child element with the given name. Uses an empty string as the namespace. <br /> | | [Element](Element.md)! | [getChild](Element.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Gets the child element with the given name. <br /> | | [Element](Element.md)! | [requireChild](Element.md))`(`localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Gets the child element with the given name. Uses an empty string as the namespace. We will throw a [org.xml.sax.SAXException](../org.xml.sax/SAXException.md) at parsing time if the specified child is missing. This helps you ensure that your listeners are called. <br /> | | [Element](Element.md)! | [requireChild](Element.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Gets the child element with the given name. We will throw a [org.xml.sax.SAXException](../org.xml.sax/SAXException.md) at parsing time if the specified child is missing. This helps you ensure that your listeners are called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setElementListener](Element.md))`(`elementListener:` ` [ElementListener](ElementListener.md)!`)` <br /> Sets start and end element listeners at the same time. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEndElementListener](Element.md))`(`endElementListener:` ` [EndElementListener](EndElementListener.md)!`)` <br /> Sets a listener for the end of this element. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEndTextElementListener](Element.md))`(`endTextElementListener:` ` [EndTextElementListener](EndTextElementListener.md)!`)` <br /> Sets a listener for the end of this text element. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStartElementListener](Element.md))`(`startElementListener:` ` [StartElementListener](StartElementListener.md)!`)` <br /> Sets a listener for the start of this element. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTextElementListener](Element.md))`(`elementListener:` ` [TextElementListener](TextElementListener.md)!`)` <br /> Sets start and end text element listeners at the same time. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Element.md))`()` <br /> | ||

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
