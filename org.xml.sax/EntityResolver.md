# EntityResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EntityResolver

```
interface EntityResolver
```

| [org.xml.sax.EntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver#) |

| Known Direct Subclasses [DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler), [EntityResolver2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/EntityResolver2), [HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase), [XMLFilterImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl) |-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------| | [DefaultHandler](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/DefaultHandler) | Default base class for SAX2 event handlers. | | [EntityResolver2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/EntityResolver2) | Extended interface for mapping external entity references to input sources, or providing a missing external subset. | | [HandlerBase](https://developer.android.com/reference/kotlin/org/xml/sax/HandlerBase) | Default base class for handlers. | | [XMLFilterImpl](https://developer.android.com/reference/kotlin/org/xml/sax/helpers/XMLFilterImpl) | Base class for deriving an XML filter. | |

| Known Indirect Subclasses [DefaultHandler2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2) [DefaultHandler2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2) |---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DefaultHandler2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2) | This class extends the SAX2 base handler class to support the SAX2 [LexicalHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler), [DeclHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DeclHandler), and [EntityResolver2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/EntityResolver2) extensions. | | [DefaultHandler2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DefaultHandler2) | This class extends the SAX2 base handler class to support the SAX2 [LexicalHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler), [DeclHandler](https://developer.android.com/reference/kotlin/org/xml/sax/ext/DeclHandler), and [EntityResolver2](https://developer.android.com/reference/kotlin/org/xml/sax/ext/EntityResolver2) extensions. | |

Basic interface for resolving entities.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

If a SAX application needs to implement customized handling for external entities, it must implement this interface and register an instance with the SAX driver using the [setEntityResolver](https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader#setEntityResolver(org.xml.sax.EntityResolver))method.

The XML reader will then allow the application to intercept any external entities (including the external DTD subset and external parameter entities, if any) before including them.

Many SAX applications will not need to implement this interface, but it will be especially useful for applications that build XML documents from databases or other specialised input sources, or for applications that use URI types other than URLs.

The following resolver would provide the application with a special character stream for the entity with the system identifier "http://www.myhost.com/today": 

```kotlin
import org.xml.sax.EntityResolver;
  import org.xml.sax.InputSource;
 
  public class MyResolver implements EntityResolver {
    public InputSource resolveEntity (String publicId, String systemId)
    {
      if (systemId.equals("http://www.myhost.com/today")) {
               // return a special input source
        MyReader reader = new MyReader();
        return new InputSource(reader);
      } else {
               // use the default behaviour
        return null;
      }
    }
  }
  
```

The application can also use this interface to redirect system identifiers to local URIs or to look up replacements in a catalog (possibly by using the public identifier).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource)! | [resolveEntity](https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver#resolveEntity(kotlin.String,%20kotlin.String))`(`publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Allow the application to resolve external entities. |

## Public methods

### resolveEntity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun resolveEntity(
    publicId: String!, 
    systemId: String!
): InputSource!
```

Allow the application to resolve external entities.

The parser will call this method before opening any external entity except the top-level document entity. Such entities include the external DTD subset and external parameter entities referenced within the DTD (in either case, only if the parser reads external parameter entities), and external general entities referenced within the document element (if the parser reads external general entities). The application may request that the parser locate the entity itself, that it use an alternative URI, or that it use data provided by the application (as a character or byte input stream).

Application writers can use this method to redirect external system identifiers to secure and/or local URIs, to look up public identifiers in a catalogue, or to read an entity from a database or other input source (including, for example, a dialog box). Neither XML nor SAX specifies a preferred policy for using public or system IDs to resolve resources. However, SAX specifies how to interpret any InputSource returned by this method, and that if none is returned, then the system ID will be dereferenced as a URL.

If the system identifier is a URL, the SAX parser must resolve it fully before reporting it to the application.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The public identifier of the external entity being referenced, or null if none was supplied. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The system identifier of the external entity being referenced. |

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource)! | An InputSource object describing the new input source, or null to request that the parser open a regular URI connection to the system identifier. |

| Exceptions ||
|----------------------------|----------------------------------------------------------------------------------------------------------------|
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |
| `java.io.IOException` | A Java-specific IO exception, possibly the result of creating a new InputStream or Reader for the InputSource. |

**See Also**

- [org.xml.sax.InputSource](https://developer.android.com/reference/kotlin/org/xml/sax/InputSource)
