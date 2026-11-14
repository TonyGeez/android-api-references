Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EntityResolver2

```
interface EntityResolver2 : EntityResolver
```

| [org.xml.sax.ext.EntityResolver2](EntityResolver2.md) |

| Known Direct Subclasses [DefaultHandler2](DefaultHandler2.md) |---|---| | [DefaultHandler2](DefaultHandler2.md) | This class extends the SAX2 base handler class to support the SAX2 `https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler`, `https://developer.android.com/reference/kotlin/org/xml/sax/ext/DeclHandler`, and `https://developer.android.com/reference/kotlin/org/xml/sax/ext/EntityResolver2#` extensions. | |
| --- | --- | --- | --- | --- | --- | --- |

Extended interface for mapping external entity references to input sources, or providing a missing external subset. The `https://developer.android.com/reference/kotlin/org/xml/sax/XMLReader.html#setEntityResolver(org.xml.sax.EntityResolver)` method is used to provide implementations of this interface to parsers. When a parser uses the methods in this interface, the #resolveEntity method (in this interface) is used *instead of* the older (SAX 1.0) `https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver.html#resolveEntity(kotlin.String,%20kotlin.String)` method. *This module, both source code and documentation, is in the Public Domain, and comes with **NO WARRANTY**.*

If a SAX application requires the customized handling which this interface defines for external entities, it must ensure that it uses an XMLReader with the *http://xml.org/sax/features/use-entity-resolver2* feature flag set to *true* (which is its default value when the feature is recognized). If that flag is unrecognized, or its value is false, or the resolver does not implement this interface, then only the `https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver.html#` method will be used.

That supports three categories of application that modify entity resolution. *Old Style* applications won't know about this interface; they will provide an EntityResolver. *Transitional Mode* provide an EntityResolver2 and automatically get the benefit of its methods in any systems (parsers or other tools) supporting it, due to polymorphism. Both *Old Style* and *Transitional Mode* applications will work with any SAX2 parser. *New style* applications will fail to run except on SAX2 parsers that support this particular feature. They will insist that feature flag have a value of "true", and the EntityResolver2 implementation they provide might throw an exception if the original SAX 1.0 style entity resolution method is invoked.

## Summary

| Public methods ||
|---|---|
| abstract [InputSource](../org.xml.sax/InputSource.md)! | `https://developer.android.com/reference/kotlin/org/xml/sax/ext/EntityResolver2#getExternalSubset(kotlin.String,%20kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, baseURI: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Allows applications to provide an external subset for documents that don't explicitly define one. |
| abstract [InputSource](../org.xml.sax/InputSource.md)! | `https://developer.android.com/reference/kotlin/org/xml/sax/ext/EntityResolver2#resolveEntity(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, publicId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, baseURI: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, systemId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Allows applications to map references to external entities into input sources, or tell the parser it should use conventional URI resolution. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver.html#` |---|---| | `https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#!` | `https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver.html#resolveEntity(kotlin.String,%20kotlin.String)(publicId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, systemId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Allow the application to resolve external entities. The parser will call this method before opening any external entity except the top-level document entity. Such entities include the external DTD subset and external parameter entities referenced within the DTD (in either case, only if the parser reads external parameter entities), and external general entities referenced within the document element (if the parser reads external general entities). The application may request that the parser locate the entity itself, that it use an alternative URI, or that it use data provided by the application (as a character or byte input stream). Application writers can use this method to redirect external system identifiers to secure and/or local URIs, to look up public identifiers in a catalogue, or to read an entity from a database or other input source (including, for example, a dialog box). Neither XML nor SAX specifies a preferred policy for using public or system IDs to resolve resources. However, SAX specifies how to interpret any InputSource returned by this method, and that if none is returned, then the system ID will be dereferenced as a URL. If the system identifier is a URL, the SAX parser must resolve it fully before reporting it to the application. <br /> | ||

## Public methods

### getExternalSubset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getExternalSubset(
    name: String!, 
    baseURI: String!
): InputSource!
```

Allows applications to provide an external subset for documents that don't explicitly define one. Documents with DOCTYPE declarations that omit an external subset can thus augment the declarations available for validation, entity processing, and attribute processing (normalization, defaulting, and reporting types including ID). This augmentation is reported through the `https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler#startDTD(kotlin.String,%20kotlin.String,%20kotlin.String)` method as if the document text had originally included the external subset; this callback is made before any internal subset data or errors are reported.

<br />

This method can also be used with documents that have no DOCTYPE declaration. When the root element is encountered, but no DOCTYPE declaration has been seen, this method is invoked. If it returns a value for the external subset, that root element is declared to be the root element, giving the effect of splicing a DOCTYPE declaration at the end the prolog of a document that could not otherwise be valid. The sequence of parser callbacks in that case logically resembles this:

```kotlin
... comments and PIs from the prolog (as usual)
  startDTD ("rootName", source.getPublicId (), source.getSystemId ());
  startEntity ("[dtd]");
  ... declarations, comments, and PIs from the external subset
  endEntity ("[dtd]");
  endDTD ();
  ... then the rest of the document (as usual)
  startElement (..., "rootName", ...);
  
```

Note that the InputSource gets no further resolution. Implementations of this method may wish to invoke #resolveEntity to gain benefits such as use of local caches of DTD entities. Also, this method will never be used by a (non-validating) processor that is not including external parameter entities.

Uses for this method include facilitating data validation when interoperating with XML processors that would always require undesirable network accesses for external entities, or which for other reasons adopt a "no DTDs" policy. Non-validation motives include forcing documents to include DTDs so that attributes are handled consistently. For example, an XPath processor needs to know which attibutes have type "ID" before it can process a widely used type of reference.

**Warning:** Returning an external subset modifies the input document. By providing definitions for general entities, it can make a malformed document appear to be well formed.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Identifies the document root element. This name comes from a DOCTYPE declaration (where available) or from the actual root element. |
| `baseURI` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The document's base URI, serving as an additional hint for selecting the external subset. This is always an absolute URI, unless it is null because the XMLReader was given an InputSource without one. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#!` | An InputSource object describing the new external subset to be used by the parser, or null to indicate that no external subset is provided. |

| Exceptions ||
|---|---|
| `java.io.IOException` | Probably indicating a failure to create a new InputStream or Reader, or an illegal URL. |
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |

### resolveEntity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun resolveEntity(
    name: String!, 
    publicId: String!, 
    baseURI: String!, 
    systemId: String!
): InputSource!
```

Allows applications to map references to external entities into input sources, or tell the parser it should use conventional URI resolution. This method is only called for external entities which have been properly declared. This method provides more flexibility than the `https://developer.android.com/reference/kotlin/org/xml/sax/EntityResolver.html#` interface, supporting implementations of more complex catalogue schemes such as the one defined by the [OASIS XML Catalogs](http://www.oasis-open.org/committees/entity/spec-2001-08-06.html) specification.

<br />

Parsers configured to use this resolver method will call it to determine the input source to use for any external entity being included because of a reference in the XML text. That excludes the document entity, and any external entity returned by `https://developer.android.com/reference/kotlin/org/xml/sax/ext/EntityResolver2#getExternalSubset(kotlin.String,%20kotlin.String)`. When a (non-validating) processor is configured not to include a class of entities (parameter or general) through use of feature flags, this method is not invoked for such entities.

Note that the entity naming scheme used here is the same one used in the `https://developer.android.com/reference/kotlin/org/xml/sax/ext/LexicalHandler`, or in the `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#skippedEntity(kotlin.String)` method.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Identifies the external entity being resolved. Either "\[dtd\]" for the external subset, or a name starting with "%" to indicate a parameter entity, or else the name of a general entity. This is never null when invoked by a SAX2 parser. |
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The public identifier of the external entity being referenced (normalized as required by the XML specification), or null if none was supplied. |
| `baseURI` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The URI with respect to which relative systemIDs are interpreted. This is always an absolute URI, unless it is null (likely because the XMLReader was given an InputSource without one). This URI is defined by the XML specification to be the one associated with the "\<" starting the relevant declaration. |
| --- | --- |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The system identifier of the external entity being referenced; either a relative or absolute URI. This is never null when invoked by a SAX2 parser; only declared entities, and any external subset, are resolved by such parsers. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/org/xml/sax/InputSource.html#!` | An InputSource object describing the new input source to be used by the parser. Returning null directs the parser to resolve the system ID against the base URI and open a connection to resulting URI. |

| Exceptions ||
|---|---|
| `java.io.IOException` | Probably indicating a failure to create a new InputStream or Reader, or an illegal URL. |
| `org.xml.sax.SAXException` | Any SAX exception, possibly wrapping another exception. |
