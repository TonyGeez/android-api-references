# org.w3c.dom

# org.w3c.dom

## Interfaces

| [Attr](Attr.md) | The `Attr` interface represents an attribute in an `Element` object. |
| --- | --- |
| [CDATASection](CDATASection.md) | CDATA sections are used to escape blocks of text containing characters that would otherwise be regarded as markup. |
| [CharacterData](CharacterData.md) | The `CharacterData` interface extends Node with a set of attributes and methods for accessing character data in the DOM. |
| [Comment](Comment.md) | This interface inherits from `CharacterData` and represents the content of a comment, i. |
| --- | --- |
| [Document](Document.md) | The `Document` interface represents the entire HTML or XML document. |
| [DocumentFragment](DocumentFragment.md) | `DocumentFragment` is a "lightweight" or "minimal" `Document` object. |
| [DocumentType](DocumentType.md) | Each `Document` has a `doctype` attribute whose value is either `null` or a `DocumentType` object. |
| --- | --- |
| [DOMConfiguration](DOMConfiguration.md) | The `DOMConfiguration` interface represents the configuration of a document and maintains a table of recognized parameters. |
| [DOMError](DOMError.md) | `DOMError` is an interface that describes an error. |
| [DOMErrorHandler](DOMErrorHandler.md) | `DOMErrorHandler` is a callback interface that the DOM implementation can call when reporting errors that happens while processing XML data, or when doing some other processing (e.g. validating a document). |
| --- | --- |
| [DOMImplementation](DOMImplementation.md) | The `DOMImplementation` interface provides a number of methods for performing operations that are independent of any particular instance of the document object model. |
| [DOMImplementationList](DOMImplementationList.md) | The `DOMImplementationList` interface provides the abstraction of an ordered collection of DOM implementations, without defining or constraining how this collection is implemented. |
| [DOMImplementationSource](DOMImplementationSource.md) | This interface permits a DOM implementer to supply one or more implementations, based upon requested features and versions, as specified in . |
| --- | --- |
| [DOMLocator](DOMLocator.md) | `DOMLocator` is an interface that describes a location (e.g. where an error occurred). |
| [DOMStringList](DOMStringList.md) | The `DOMStringList` interface provides the abstraction of an ordered collection of `DOMString` values, without defining or constraining how this collection is implemented. |
| [Element](Element.md) | The `Element` interface represents an element in an HTML or XML document. |
| --- | --- |
| [Entity](Entity.md) | This interface represents a known entity, either parsed or unparsed, in an XML document. |
| [EntityReference](EntityReference.md) | `EntityReference` nodes may be used to represent an entity reference in the tree. |
| [NamedNodeMap](NamedNodeMap.md) | Objects implementing the `NamedNodeMap` interface are used to represent collections of nodes that can be accessed by name. |
| --- | --- |
| [NameList](NameList.md) | The `NameList` interface provides the abstraction of an ordered collection of parallel pairs of name and namespace values (which could be null values), without defining or constraining how this collection is implemented. |
| [Node](Node.md) | The `Node` interface is the primary datatype for the entire Document Object Model. |
| [NodeList](NodeList.md) | The `NodeList` interface provides the abstraction of an ordered collection of nodes, without defining or constraining how this collection is implemented. |
| --- | --- |
| [Notation](Notation.md) | This interface represents a notation declared in the DTD. |
| [ProcessingInstruction](ProcessingInstruction.md) | The `ProcessingInstruction` interface represents a "processing instruction", used in XML as a way to keep processor-specific information in the text of the document. |
| [Text](Text.md) | The `Text` interface inherits from `CharacterData` and represents the textual content (termed [character data](http://www.w3.org/TR/2004/REC-xml-20040204#syntax) in XML) of an `Element` or `Attr`. |
| --- | --- |
| [TypeInfo](TypeInfo.md) | The `TypeInfo` interface represents a type referenced from `Element` or `Attr` nodes, specified in the schemas associated with the document. |
| [UserDataHandler](UserDataHandler.md) | When associating an object to a key on a node using `Node.setUserData()` the application can provide a handler that gets called when the node the object is associated to is being cloned, imported, or renamed. |

## Exceptions

| [DOMException](DOMException.md) | DOM operations only raise exceptions in "exceptional" circumstances, i. |
| --- | --- |
