# DOMImplementation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DOMImplementation

```
interface DOMImplementation
```

| [org.w3c.dom.DOMImplementation](../org/w3c/dom/DOMImplementation.md) |

The`DOMImplementation`interface provides a number of methods for performing operations that are independent of any particular instance of the document object model.

See also the [Document Object Model (DOM) Level 3 Core Specification](http://www.w3.org/TR/2004/REC-DOM-Level-3-Core-20040407).

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | [createDocument](../org/w3c/dom/DOMImplementation.md))`(`namespaceURI:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `qualifiedName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `doctype:` ` [DocumentType](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document-type/index.html)!`)` Creates a DOM Document object of the specified type with its document element. |
| abstract [DocumentType](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document-type/index.html)! | [createDocumentType](../org/w3c/dom/DOMImplementation.md))`(`qualifiedName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates an empty`DocumentType`node. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getFeature](../org/w3c/dom/DOMImplementation.md))`(`feature:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `version:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` This method returns a specialized object which implements the specialized APIs of the specified feature and version, as specified in . |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasFeature](../org/w3c/dom/DOMImplementation.md))`(`feature:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `version:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Test if the DOM implementation implements a specific feature and version, as specified in . |

## Public methods

### createDocument

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createDocument(
    namespaceURI: String!, 
    qualifiedName: String!, 
    doctype: DocumentType!
): Document!
```

Creates a DOM Document object of the specified type with its document element. 
Note that based on the`DocumentType`given to create the document, the implementation may instantiate specialized`Document`objects that support additional features than the "Core", such as "HTML" \ [[DOM Level 2 HTML](http://www.w3.org/TR/2003/REC-DOM-Level-2-HTML-20030109)\] . On the other hand, setting the`DocumentType`after the document was created makes this very unlikely to happen. Alternatively, specialized`Document`creation methods, such as`createHTMLDocument`\ [[DOM Level 2 HTML](http://www.w3.org/TR/2003/REC-DOM-Level-2-HTML-20030109)\] , can be used to obtain specific types of`Document`objects.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `namespaceURI` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The namespace URI of the document element to create or`null`. |
| `qualifiedName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The qualified name of the document element to be created or`null`. |
| `doctype` | [DocumentType](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document-type/index.html)!:The type of document to be created or`null`. When`doctype`is not`null`, its`Node.ownerDocument`attribute is set to the document being created. |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | A new`Document`object with its document element. If the`NamespaceURI`,`qualifiedName`, and`doctype`are`null`, the returned`Document`is empty with no document element. |

| Exceptions ||
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | INVALID_CHARACTER_ERR: Raised if the specified qualified name is not an XML name according to \ [[XML 1.0](http://www.w3.org/TR/2004/REC-xml-20040204)\]. NAMESPACE_ERR: Raised if the`qualifiedName`is malformed, if the`qualifiedName`has a prefix and the`namespaceURI`is`null`, or if the`qualifiedName`is`null`and the`namespaceURI`is different from`null`, or if the`qualifiedName`has a prefix that is "xml" and the`namespaceURI`is different from "<http://www.w3.org/XML/1998/namespace>" \ [[XML Namespaces](http://www.w3.org/TR/1999/REC-xml-names-19990114/)\] , or if the DOM implementation does not support the`"XML"`feature but a non-null namespace URI was provided, since namespaces were defined by XML. WRONG_DOCUMENT_ERR: Raised if`doctype`has already been used with a different document or was created from a different implementation. NOT_SUPPORTED_ERR: May be raised if the implementation does not support the feature "XML" and the language exposed through the Document does not support XML Namespaces (such as \ [[HTML 4.01](http://www.w3.org/TR/1999/REC-html401-19991224/)\]). |

### createDocumentType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createDocumentType(
    qualifiedName: String!, 
    publicId: String!, 
    systemId: String!
): DocumentType!
```

Creates an empty`DocumentType`node. Entity declarations and notations are not made available. Entity reference expansions and default attribute additions do not occur..

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `qualifiedName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The qualified name of the document type to be created. |
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The external subset public identifier. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The external subset system identifier. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [DocumentType](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document-type/index.html)! | A new`DocumentType`node with`Node.ownerDocument`set to`null`. |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | INVALID_CHARACTER_ERR: Raised if the specified qualified name is not an XML name according to \ [[XML 1.0](http://www.w3.org/TR/2004/REC-xml-20040204)\]. NAMESPACE_ERR: Raised if the`qualifiedName`is malformed. NOT_SUPPORTED_ERR: May be raised if the implementation does not support the feature "XML" and the language exposed through the Document does not support XML Namespaces (such as \ [[HTML 4.01](http://www.w3.org/TR/1999/REC-html401-19991224/)\]). |

### getFeature

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFeature(
    feature: String!, 
    version: String!
): Any!
```

This method returns a specialized object which implements the specialized APIs of the specified feature and version, as specified in . The specialized object may also be obtained by using binding-specific casting methods but is not necessarily expected to, as discussed in . This method also allow the implementation to provide specialized objects which do not support the`DOMImplementation`interface.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `feature` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the feature requested. Note that any plus sign "+" prepended to the name of the feature will be ignored since it is not significant in the context of this method. |
| `version` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:This is the version number of the feature to test. |

| Return ||
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | Returns an object which implements the specialized APIs of the specified feature and version, if any, or`null`if there is no object which implements interfaces associated with that feature. If the`DOMObject`returned by this method implements the`DOMImplementation`interface, it must delegate to the primary core`DOMImplementation`and not return results inconsistent with the primary core`DOMImplementation`such as`hasFeature`,`getFeature`, etc. |

### hasFeature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasFeature(
    feature: String!, 
    version: String!
): Boolean
```

Test if the DOM implementation implements a specific feature and version, as specified in .

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `feature` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the feature to test. |
| `version` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:This is the version number of the feature to test. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the feature is implemented in the specified version,`false`otherwise. |
