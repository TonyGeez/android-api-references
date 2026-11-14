# RootElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RootElement

Kotlin| [Java](https://developer.android.com/reference/android/sax/RootElement "View this page in Java") 

```
open class RootElement : Element
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.sax.Element](https://developer.android.com/reference/kotlin/android/sax/Element) ||
| | ↳ | [android.sax.RootElement](https://developer.android.com/reference/kotlin/android/sax/RootElement#) |

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
| [RootElement](https://developer.android.com/reference/kotlin/android/sax/RootElement#RootElement(kotlin.String))`(`localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new root element with the given name. |
| [RootElement](https://developer.android.com/reference/kotlin/android/sax/RootElement#RootElement(kotlin.String,%20kotlin.String))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new root element with the given name. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ContentHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#)! | [getContentHandler](https://developer.android.com/reference/kotlin/android/sax/RootElement#getContentHandler())`()` Gets the SAX`ContentHandler`. |

| Inherited functions ||
|---|---|
| From class [Element](https://developer.android.com/reference/kotlin/android/sax/Element) |----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Element](https://developer.android.com/reference/kotlin/android/sax/Element)! | [getChild](https://developer.android.com/reference/kotlin/android/sax/Element#getChild(kotlin.String))`(`localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Gets the child element with the given name. Uses an empty string as the namespace. <br /> | | [Element](https://developer.android.com/reference/kotlin/android/sax/Element)! | [getChild](https://developer.android.com/reference/kotlin/android/sax/Element#getChild(kotlin.String,%20kotlin.String))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Gets the child element with the given name. <br /> | | [Element](https://developer.android.com/reference/kotlin/android/sax/Element)! | [requireChild](https://developer.android.com/reference/kotlin/android/sax/Element#requireChild(kotlin.String))`(`localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Gets the child element with the given name. Uses an empty string as the namespace. We will throw a [org.xml.sax.SAXException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException.html#) at parsing time if the specified child is missing. This helps you ensure that your listeners are called. <br /> | | [Element](https://developer.android.com/reference/kotlin/android/sax/Element)! | [requireChild](https://developer.android.com/reference/kotlin/android/sax/Element#requireChild(kotlin.String,%20kotlin.String))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Gets the child element with the given name. We will throw a [org.xml.sax.SAXException](https://developer.android.com/reference/kotlin/org/xml/sax/SAXException.html#) at parsing time if the specified child is missing. This helps you ensure that your listeners are called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setElementListener](https://developer.android.com/reference/kotlin/android/sax/Element#setElementListener(android.sax.ElementListener))`(`elementListener:` ` [ElementListener](https://developer.android.com/reference/kotlin/android/sax/ElementListener)!`)` <br /> Sets start and end element listeners at the same time. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEndElementListener](https://developer.android.com/reference/kotlin/android/sax/Element#setEndElementListener(android.sax.EndElementListener))`(`endElementListener:` ` [EndElementListener](https://developer.android.com/reference/kotlin/android/sax/EndElementListener)!`)` <br /> Sets a listener for the end of this element. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEndTextElementListener](https://developer.android.com/reference/kotlin/android/sax/Element#setEndTextElementListener(android.sax.EndTextElementListener))`(`endTextElementListener:` ` [EndTextElementListener](https://developer.android.com/reference/kotlin/android/sax/EndTextElementListener)!`)` <br /> Sets a listener for the end of this text element. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStartElementListener](https://developer.android.com/reference/kotlin/android/sax/Element#setStartElementListener(android.sax.StartElementListener))`(`startElementListener:` ` [StartElementListener](https://developer.android.com/reference/kotlin/android/sax/StartElementListener)!`)` <br /> Sets a listener for the start of this element. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTextElementListener](https://developer.android.com/reference/kotlin/android/sax/Element#setTextElementListener(android.sax.TextElementListener))`(`elementListener:` ` [TextElementListener](https://developer.android.com/reference/kotlin/android/sax/TextElementListener)!`)` <br /> Sets start and end text element listeners at the same time. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/sax/Element#toString())`()` <br /> | ||

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
