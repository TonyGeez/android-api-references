# org.w3c.dom

# org.w3c.dom

## Interfaces

| [Attr](../org/w3c/dom/Attr.md) | The `Attr` interface represents an attribute in an `Element` object. |
| --- | --- |
| [CDATASection](../org/w3c/dom/CDATASection.md) | CDATA sections are used to escape blocks of text containing characters that would otherwise be regarded as markup. |
| [CharacterData](../org/w3c/dom/CharacterData.md) | The `CharacterData` interface extends Node with a set of attributes and methods for accessing character data in the DOM. |
| [Comment](../org/w3c/dom/Comment.md) | This interface inherits from `CharacterData` and represents the content of a comment, i. |
| --- | --- |
| [Document](../org/w3c/dom/Document.md) | The `Document` interface represents the entire HTML or XML document. |
| [DocumentFragment](../org/w3c/dom/DocumentFragment.md) | `DocumentFragment` is a "lightweight" or "minimal" `Document` object. |
| [DocumentType](../org/w3c/dom/DocumentType.md) | Each `Document` has a `doctype` attribute whose value is either `null` or a `DocumentType` object. |
| --- | --- |
| [DOMConfiguration](../org/w3c/dom/DOMConfiguration.md) | The `DOMConfiguration` interface represents the configuration of a document and maintains a table of recognized parameters. |
| [DOMError](../org/w3c/dom/DOMError.md) | `DOMError` is an interface that describes an error. |
| [DOMErrorHandler](../org/w3c/dom/DOMErrorHandler.md) | `DOMErrorHandler` is a callback interface that the DOM implementation can call when reporting errors that happens while processing XML data, or when doing some other processing (e.g. validating a document). |
| --- | --- |
| [DOMImplementation](../org/w3c/dom/DOMImplementation.md) | The `DOMImplementation` interface provides a number of methods for performing operations that are independent of any particular instance of the document object model. |
| [DOMImplementationList](../org/w3c/dom/DOMImplementationList.md) | The `DOMImplementationList` interface provides the abstraction of an ordered collection of DOM implementations, without defining or constraining how this collection is implemented. |
| [DOMImplementationSource](../org/w3c/dom/DOMImplementationSource.md) | This interface permits a DOM implementer to supply one or more implementations, based upon requested features and versions, as specified in . |
| --- | --- |
| [DOMLocator](../org/w3c/dom/DOMLocator.md) | `DOMLocator` is an interface that describes a location (e.g. where an error occurred). |
| [DOMStringList](../org/w3c/dom/DOMStringList.md) | The `DOMStringList` interface provides the abstraction of an ordered collection of `DOMString` values, without defining or constraining how this collection is implemented. |
| [Element](../org/w3c/dom/Element.md) | The `Element` interface represents an element in an HTML or XML document. |
| --- | --- |
| [Entity](../org/w3c/dom/Entity.md) | This interface represents a known entity, either parsed or unparsed, in an XML document. |
| [EntityReference](../org/w3c/dom/EntityReference.md) | `EntityReference` nodes may be used to represent an entity reference in the tree. |
| [NamedNodeMap](../org/w3c/dom/NamedNodeMap.md) | Objects implementing the `NamedNodeMap` interface are used to represent collections of nodes that can be accessed by name. |
| --- | --- |
| [NameList](../org/w3c/dom/NameList.md) | The `NameList` interface provides the abstraction of an ordered collection of parallel pairs of name and namespace values (which could be null values), without defining or constraining how this collection is implemented. |
| [Node](../org/w3c/dom/Node.md) | The `Node` interface is the primary datatype for the entire Document Object Model. |
| [NodeList](../org/w3c/dom/NodeList.md) | The `NodeList` interface provides the abstraction of an ordered collection of nodes, without defining or constraining how this collection is implemented. |
| --- | --- |
| [Notation](../org/w3c/dom/Notation.md) | This interface represents a notation declared in the DTD. |
| [ProcessingInstruction](../org/w3c/dom/ProcessingInstruction.md) | The `ProcessingInstruction` interface represents a "processing instruction", used in XML as a way to keep processor-specific information in the text of the document. |
| [Text](../org/w3c/dom/Text.md) | The `Text` interface inherits from `CharacterData` and represents the textual content (termed [character data](http://www.w3.org/TR/2004/REC-xml-20040204#syntax) in XML) of an `Element` or `Attr`. |
| --- | --- |
| [TypeInfo](../org/w3c/dom/TypeInfo.md) | The `TypeInfo` interface represents a type referenced from `Element` or `Attr` nodes, specified in the schemas associated with the document. |
| [UserDataHandler](../org/w3c/dom/UserDataHandler.md) | When associating an object to a key on a node using `Node.setUserData()` the application can provide a handler that gets called when the node the object is associated to is being cloned, imported, or renamed. |

## Exceptions

| [DOMException](../org/w3c/dom/DOMException.md) | DOM operations only raise exceptions in "exceptional" circumstances, i. |
| --- | --- |
