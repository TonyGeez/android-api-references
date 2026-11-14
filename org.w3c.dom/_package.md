# org.w3c.dom

# org.w3c.dom

## Interfaces

| [Attr](https://developer.android.com/reference/kotlin/org/w3c/dom/Attr) | The `Attr` interface represents an attribute in an `Element` object. |
| [CDATASection](https://developer.android.com/reference/kotlin/org/w3c/dom/CDATASection) | CDATA sections are used to escape blocks of text containing characters that would otherwise be regarded as markup. |
| [CharacterData](https://developer.android.com/reference/kotlin/org/w3c/dom/CharacterData) | The `CharacterData` interface extends Node with a set of attributes and methods for accessing character data in the DOM. |
| [Comment](https://developer.android.com/reference/kotlin/org/w3c/dom/Comment) | This interface inherits from `CharacterData` and represents the content of a comment, i. |
| [Document](https://developer.android.com/reference/kotlin/org/w3c/dom/Document) | The `Document` interface represents the entire HTML or XML document. |
| [DocumentFragment](https://developer.android.com/reference/kotlin/org/w3c/dom/DocumentFragment) | `DocumentFragment` is a "lightweight" or "minimal" `Document` object. |
| [DocumentType](https://developer.android.com/reference/kotlin/org/w3c/dom/DocumentType) | Each `Document` has a `doctype` attribute whose value is either `null` or a `DocumentType` object. |
| [DOMConfiguration](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMConfiguration) | The `DOMConfiguration` interface represents the configuration of a document and maintains a table of recognized parameters. |
| [DOMError](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMError) | `DOMError` is an interface that describes an error. |
| [DOMErrorHandler](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMErrorHandler) | `DOMErrorHandler` is a callback interface that the DOM implementation can call when reporting errors that happens while processing XML data, or when doing some other processing (e.g. validating a document). |
| [DOMImplementation](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMImplementation) | The `DOMImplementation` interface provides a number of methods for performing operations that are independent of any particular instance of the document object model. |
| [DOMImplementationList](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMImplementationList) | The `DOMImplementationList` interface provides the abstraction of an ordered collection of DOM implementations, without defining or constraining how this collection is implemented. |
| [DOMImplementationSource](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMImplementationSource) | This interface permits a DOM implementer to supply one or more implementations, based upon requested features and versions, as specified in . |
| [DOMLocator](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMLocator) | `DOMLocator` is an interface that describes a location (e.g. where an error occurred). |
| [DOMStringList](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMStringList) | The `DOMStringList` interface provides the abstraction of an ordered collection of `DOMString` values, without defining or constraining how this collection is implemented. |
| [Element](https://developer.android.com/reference/kotlin/org/w3c/dom/Element) | The `Element` interface represents an element in an HTML or XML document. |
| [Entity](https://developer.android.com/reference/kotlin/org/w3c/dom/Entity) | This interface represents a known entity, either parsed or unparsed, in an XML document. |
| [EntityReference](https://developer.android.com/reference/kotlin/org/w3c/dom/EntityReference) | `EntityReference` nodes may be used to represent an entity reference in the tree. |
| [NamedNodeMap](https://developer.android.com/reference/kotlin/org/w3c/dom/NamedNodeMap) | Objects implementing the `NamedNodeMap` interface are used to represent collections of nodes that can be accessed by name. |
| [NameList](https://developer.android.com/reference/kotlin/org/w3c/dom/NameList) | The `NameList` interface provides the abstraction of an ordered collection of parallel pairs of name and namespace values (which could be null values), without defining or constraining how this collection is implemented. |
| [Node](https://developer.android.com/reference/kotlin/org/w3c/dom/Node) | The `Node` interface is the primary datatype for the entire Document Object Model. |
| [NodeList](https://developer.android.com/reference/kotlin/org/w3c/dom/NodeList) | The `NodeList` interface provides the abstraction of an ordered collection of nodes, without defining or constraining how this collection is implemented. |
| [Notation](https://developer.android.com/reference/kotlin/org/w3c/dom/Notation) | This interface represents a notation declared in the DTD. |
| [ProcessingInstruction](https://developer.android.com/reference/kotlin/org/w3c/dom/ProcessingInstruction) | The `ProcessingInstruction` interface represents a "processing instruction", used in XML as a way to keep processor-specific information in the text of the document. |
| [Text](https://developer.android.com/reference/kotlin/org/w3c/dom/Text) | The `Text` interface inherits from `CharacterData` and represents the textual content (termed [character data](http://www.w3.org/TR/2004/REC-xml-20040204#syntax) in XML) of an `Element` or `Attr`. |
| [TypeInfo](https://developer.android.com/reference/kotlin/org/w3c/dom/TypeInfo) | The `TypeInfo` interface represents a type referenced from `Element` or `Attr` nodes, specified in the schemas associated with the document. |
| [UserDataHandler](https://developer.android.com/reference/kotlin/org/w3c/dom/UserDataHandler) | When associating an object to a key on a node using `Node.setUserData()` the application can provide a handler that gets called when the node the object is associated to is being cloned, imported, or renamed. |

## Exceptions

| [DOMException](https://developer.android.com/reference/kotlin/org/w3c/dom/DOMException) | DOM operations only raise exceptions in "exceptional" circumstances, i. |
