# Node

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Node

```
interface Node
```

| [org.w3c.dom.Node](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#) |

| Known Direct Subclasses [Attr](https://developer.android.com/reference/kotlin/org/w3c/dom/Attr), [CharacterData](https://developer.android.com/reference/kotlin/org/w3c/dom/CharacterData), [Document](https://developer.android.com/reference/kotlin/org/w3c/dom/Document), [DocumentFragment](https://developer.android.com/reference/kotlin/org/w3c/dom/DocumentFragment), [DocumentType](https://developer.android.com/reference/kotlin/org/w3c/dom/DocumentType), [Element](https://developer.android.com/reference/kotlin/org/w3c/dom/Element), [Entity](https://developer.android.com/reference/kotlin/org/w3c/dom/Entity), [EntityReference](https://developer.android.com/reference/kotlin/org/w3c/dom/EntityReference), [Notation](https://developer.android.com/reference/kotlin/org/w3c/dom/Notation), [ProcessingInstruction](https://developer.android.com/reference/kotlin/org/w3c/dom/ProcessingInstruction) |-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Attr](https://developer.android.com/reference/kotlin/org/w3c/dom/Attr) | The`Attr`interface represents an attribute in an`Element`object. | | [CharacterData](https://developer.android.com/reference/kotlin/org/w3c/dom/CharacterData) | The`CharacterData`interface extends Node with a set of attributes and methods for accessing character data in the DOM. | | [Document](https://developer.android.com/reference/kotlin/org/w3c/dom/Document) | The`Document`interface represents the entire HTML or XML document. | | [DocumentFragment](https://developer.android.com/reference/kotlin/org/w3c/dom/DocumentFragment) | `DocumentFragment`is a "lightweight" or "minimal"`Document`object. | | [DocumentType](https://developer.android.com/reference/kotlin/org/w3c/dom/DocumentType) | Each`Document`has a`doctype`attribute whose value is either`null`or a`DocumentType`object. | | [Element](https://developer.android.com/reference/kotlin/org/w3c/dom/Element) | The`Element`interface represents an element in an HTML or XML document. | | [Entity](https://developer.android.com/reference/kotlin/org/w3c/dom/Entity) | This interface represents a known entity, either parsed or unparsed, in an XML document. | | [EntityReference](https://developer.android.com/reference/kotlin/org/w3c/dom/EntityReference) | `EntityReference`nodes may be used to represent an entity reference in the tree. | | [Notation](https://developer.android.com/reference/kotlin/org/w3c/dom/Notation) | This interface represents a notation declared in the DTD. | | [ProcessingInstruction](https://developer.android.com/reference/kotlin/org/w3c/dom/ProcessingInstruction) | The`ProcessingInstruction`interface represents a "processing instruction", used in XML as a way to keep processor-specific information in the text of the document. | |

| Known Indirect Subclasses [CDATASection](https://developer.android.com/reference/kotlin/org/w3c/dom/CDATASection), [Comment](https://developer.android.com/reference/kotlin/org/w3c/dom/Comment), [Text](https://developer.android.com/reference/kotlin/org/w3c/dom/Text) |-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CDATASection](https://developer.android.com/reference/kotlin/org/w3c/dom/CDATASection) | CDATA sections are used to escape blocks of text containing characters that would otherwise be regarded as markup. | | [Comment](https://developer.android.com/reference/kotlin/org/w3c/dom/Comment) | This interface inherits from`CharacterData`and represents the content of a comment, i. | | [Text](https://developer.android.com/reference/kotlin/org/w3c/dom/Text) | The`Text`interface inherits from`CharacterData`and represents the textual content (termed [character data](http://www.w3.org/TR/2004/REC-xml-20040204#syntax) in XML) of an`Element`or`Attr`. | |

The`Node`interface is the primary datatype for the entire Document Object Model. It represents a single node in the document tree. While all objects implementing the`Node`interface expose methods for dealing with children, not all objects implementing the`Node`interface may have children. For example,`Text`nodes may not have children, and adding children to such nodes results in a`DOMException`being raised.

The attributes`nodeName`,`nodeValue`and`attributes`are included as a mechanism to get at node information without casting down to the specific derived interface. In cases where there is no obvious mapping of these attributes for a specific`nodeType`(e.g.,`nodeValue`for an`Element`or`attributes`for a`Comment`), this returns`null`. Note that the specialized interfaces may contain additional and more convenient mechanisms to get and set the relevant information.

The values of`nodeName`,`nodeValue`, and`attributes`vary according to the node type as follows:

| Interface | nodeName | nodeValue | attributes |
|-------------------------|---------------------------------------|---------------------------------------------------------------|----------------|
| `Attr` | same as`Attr.name` | same as`Attr.value` | `null` |
| `CDATASection` | `"#cdata-section"` | same as`CharacterData.data`, the content of the CDATA Section | `null` |
| `Comment` | `"#comment"` | same as`CharacterData.data`, the content of the comment | `null` |
| `Document` | `"#document"` | `null` | `null` |
| `DocumentFragment` | `"#document-fragment"` | `null` | `null` |
| `DocumentType` | same as`DocumentType.name` | `null` | `null` |
| `Element` | same as`Element.tagName` | `null` | `NamedNodeMap` |
| `Entity` | entity name | `null` | `null` |
| `EntityReference` | name of entity referenced | `null` | `null` |
| `Notation` | notation name | `null` | `null` |
| `ProcessingInstruction` | same as`ProcessingInstruction.target` | same as`ProcessingInstruction.data` | `null` |
| `Text` | `"#text"` | same as`CharacterData.data`, the content of the text node | `null` |

See also the [Document Object Model (DOM) Level 3 Core Specification](http://www.w3.org/TR/2004/REC-DOM-Level-3-Core-20040407).

## Summary

| Constants ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [ATTRIBUTE_NODE](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#ATTRIBUTE_NODE:kotlin.Short) The node is an`Attr`. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [CDATA_SECTION_NODE](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#CDATA_SECTION_NODE:kotlin.Short) The node is a`CDATASection`. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [COMMENT_NODE](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#COMMENT_NODE:kotlin.Short) The node is a`Comment`. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [DOCUMENT_FRAGMENT_NODE](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#DOCUMENT_FRAGMENT_NODE:kotlin.Short) The node is a`DocumentFragment`. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [DOCUMENT_NODE](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#DOCUMENT_NODE:kotlin.Short) The node is a`Document`. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [DOCUMENT_POSITION_CONTAINED_BY](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#DOCUMENT_POSITION_CONTAINED_BY:kotlin.Short) The node is contained by the reference node. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [DOCUMENT_POSITION_CONTAINS](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#DOCUMENT_POSITION_CONTAINS:kotlin.Short) The node contains the reference node. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [DOCUMENT_POSITION_DISCONNECTED](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#DOCUMENT_POSITION_DISCONNECTED:kotlin.Short) The two nodes are disconnected. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [DOCUMENT_POSITION_FOLLOWING](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#DOCUMENT_POSITION_FOLLOWING:kotlin.Short) The node follows the reference node. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [DOCUMENT_POSITION_IMPLEMENTATION_SPECIFIC](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#DOCUMENT_POSITION_IMPLEMENTATION_SPECIFIC:kotlin.Short) The determination of preceding versus following is implementation-specific. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [DOCUMENT_POSITION_PRECEDING](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#DOCUMENT_POSITION_PRECEDING:kotlin.Short) The second node precedes the reference node. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [DOCUMENT_TYPE_NODE](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#DOCUMENT_TYPE_NODE:kotlin.Short) The node is a`DocumentType`. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [ELEMENT_NODE](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#ELEMENT_NODE:kotlin.Short) The node is an`Element`. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [ENTITY_NODE](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#ENTITY_NODE:kotlin.Short) The node is an`Entity`. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [ENTITY_REFERENCE_NODE](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#ENTITY_REFERENCE_NODE:kotlin.Short) The node is an`EntityReference`. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [NOTATION_NODE](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#NOTATION_NODE:kotlin.Short) The node is a`Notation`. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [PROCESSING_INSTRUCTION_NODE](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#PROCESSING_INSTRUCTION_NODE:kotlin.Short) The node is a`ProcessingInstruction`. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [TEXT_NODE](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#TEXT_NODE:kotlin.Short) The node is a`Text`node. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [appendChild](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#appendChild(org.w3c.dom.Node))`(`newChild:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`)` Adds the node`newChild`to the end of the list of children of this node. |
| abstract [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [cloneNode](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#cloneNode(kotlin.Boolean))`(`deep:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns a duplicate of this node, i. |
| abstract [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [compareDocumentPosition](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#compareDocumentPosition(org.w3c.dom.Node))`(`other:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`)` Compares the reference node, i. |
| abstract [NamedNodeMap](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-named-node-map/index.html)! | [getAttributes](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getAttributes())`()` A`NamedNodeMap`containing the attributes of this node (if it is an`Element`) or`null`otherwise. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getBaseURI](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getBaseURI())`()` The absolute base URI of this node or`null`if the implementation wasn't able to obtain an absolute URI. |
| abstract [NodeList](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node-list/index.html)! | [getChildNodes](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getChildNodes())`()` A`NodeList`that contains all children of this node. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getFeature](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getFeature(kotlin.String,%20kotlin.String))`(`feature:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `version:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` This method returns a specialized object which implements the specialized APIs of the specified feature and version, as specified in . |
| abstract [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [getFirstChild](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getFirstChild())`()` The first child of this node. |
| abstract [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [getLastChild](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getLastChild())`()` The last child of this node. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLocalName](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getLocalName())`()` Returns the local part of the qualified name of this node. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNamespaceURI](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getNamespaceURI())`()` The namespace URI of this node, or`null`if it is unspecified (see ). |
| abstract [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [getNextSibling](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getNextSibling())`()` The node immediately following this node. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNodeName](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getNodeName())`()` The name of this node, depending on its type; see the table above. |
| abstract [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getNodeType](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getNodeType())`()` A code representing the type of the underlying object, as defined above. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNodeValue](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getNodeValue())`()` The value of this node, depending on its type; see the table above. |
| abstract [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | [getOwnerDocument](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getOwnerDocument())`()` The`Document`object associated with this node. |
| abstract [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [getParentNode](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getParentNode())`()` The parent of this node. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPrefix](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getPrefix())`()` The namespace prefix of this node, or`null`if it is unspecified. |
| abstract [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [getPreviousSibling](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getPreviousSibling())`()` The node immediately preceding this node. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTextContent](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getTextContent())`()` This attribute returns the text content of this node and its descendants. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getUserData](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getUserData(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the object associated to a key on a this node. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasAttributes](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#hasAttributes())`()` Returns whether this node (if it is an element) has any attributes. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasChildNodes](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#hasChildNodes())`()` Returns whether this node has any children. |
| abstract [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [insertBefore](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#insertBefore(org.w3c.dom.Node,%20org.w3c.dom.Node))`(`newChild:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`, `refChild:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`)` Inserts the node`newChild`before the existing child node`refChild`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDefaultNamespace](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#isDefaultNamespace(kotlin.String))`(`namespaceURI:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` This method checks if the specified`namespaceURI`is the default namespace or not. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEqualNode](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#isEqualNode(org.w3c.dom.Node))`(`arg:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`)` Tests whether two nodes are equal. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSameNode](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#isSameNode(org.w3c.dom.Node))`(`other:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`)` Returns whether this node is the same node as the given one. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#isSupported(kotlin.String,%20kotlin.String))`(`feature:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `version:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Tests whether the DOM implementation implements a specific feature and that feature is supported by this node, as specified in . |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [lookupNamespaceURI](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#lookupNamespaceURI(kotlin.String))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up the namespace URI associated to the given prefix, starting from this node. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [lookupPrefix](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#lookupPrefix(kotlin.String))`(`namespaceURI:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up the prefix associated to the given namespace URI, starting from this node. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [normalize](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#normalize())`()` Puts all`Text`nodes in the full depth of the sub-tree underneath this`Node`, including attribute nodes, into a "normal" form where only structure (e.g., elements, comments, processing instructions, CDATA sections, and entity references) separates |
| abstract [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [removeChild](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#removeChild(org.w3c.dom.Node))`(`oldChild:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`)` Removes the child node indicated by`oldChild`from the list of children, and returns it. |
| abstract [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [replaceChild](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#replaceChild(org.w3c.dom.Node,%20org.w3c.dom.Node))`(`newChild:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`, `oldChild:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`)` Replaces the child node`oldChild`with`newChild`in the list of children, and returns the`oldChild`node. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNodeValue](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#setNodeValue(kotlin.String))`(`nodeValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` The value of this node, depending on its type; see the table above. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPrefix](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#setPrefix(kotlin.String))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` The namespace prefix of this node, or`null`if it is unspecified. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTextContent](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#setTextContent(kotlin.String))`(`textContent:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` This attribute returns the text content of this node and its descendants. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [setUserData](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#setUserData(kotlin.String,%20kotlin.Any,%20org.w3c.dom.UserDataHandler))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `data:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `handler:` ` [UserDataHandler](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-user-data-handler/index.html)!`)` Associate an object to a key on this node. |

## Constants

### ATTRIBUTE_NODE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ATTRIBUTE_NODE: Short
```

The node is an`Attr`. 

 Value: 2

### CDATA_SECTION_NODE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CDATA_SECTION_NODE: Short
```

The node is a`CDATASection`. 

 Value: 4

### COMMENT_NODE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMMENT_NODE: Short
```

The node is a`Comment`. 

 Value: 8

### DOCUMENT_FRAGMENT_NODE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOCUMENT_FRAGMENT_NODE: Short
```

The node is a`DocumentFragment`. 

 Value: 11

### DOCUMENT_NODE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOCUMENT_NODE: Short
```

The node is a`Document`. 

 Value: 9

### DOCUMENT_POSITION_CONTAINED_BY

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOCUMENT_POSITION_CONTAINED_BY: Short
```

The node is contained by the reference node. A node which is contained is always following, too. 

 Value: 16

### DOCUMENT_POSITION_CONTAINS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOCUMENT_POSITION_CONTAINS: Short
```

The node contains the reference node. A node which contains is always preceding, too. 

 Value: 8

### DOCUMENT_POSITION_DISCONNECTED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOCUMENT_POSITION_DISCONNECTED: Short
```

The two nodes are disconnected. Order between disconnected nodes is always implementation-specific. 

 Value: 1

### DOCUMENT_POSITION_FOLLOWING

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOCUMENT_POSITION_FOLLOWING: Short
```

The node follows the reference node. 

 Value: 4

### DOCUMENT_POSITION_IMPLEMENTATION_SPECIFIC

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOCUMENT_POSITION_IMPLEMENTATION_SPECIFIC: Short
```

The determination of preceding versus following is implementation-specific. 

 Value: 32

### DOCUMENT_POSITION_PRECEDING

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOCUMENT_POSITION_PRECEDING: Short
```

The second node precedes the reference node. 

 Value: 2

### DOCUMENT_TYPE_NODE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOCUMENT_TYPE_NODE: Short
```

The node is a`DocumentType`. 

 Value: 10

### ELEMENT_NODE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ELEMENT_NODE: Short
```

The node is an`Element`. 

 Value: 1

### ENTITY_NODE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENTITY_NODE: Short
```

The node is an`Entity`. 

 Value: 6

### ENTITY_REFERENCE_NODE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENTITY_REFERENCE_NODE: Short
```

The node is an`EntityReference`. 

 Value: 5

### NOTATION_NODE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NOTATION_NODE: Short
```

The node is a`Notation`. 

 Value: 12

### PROCESSING_INSTRUCTION_NODE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROCESSING_INSTRUCTION_NODE: Short
```

The node is a`ProcessingInstruction`. 

 Value: 7

### TEXT_NODE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TEXT_NODE: Short
```

The node is a`Text`node. 

 Value: 3

## Public methods

### appendChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun appendChild(newChild: Node!): Node!
```

Adds the node`newChild`to the end of the list of children of this node. If the`newChild`is already in the tree, it is first removed.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newChild` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!:The node to add.If it is a`DocumentFragment`object, the entire contents of the document fragment are moved into the child list of this node |

| Return ||
|------------------------------------------------------------------------------------|-----------------|
| [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | The node added. |

| Exceptions ||
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | HIERARCHY_REQUEST_ERR: Raised if this node is of a type that does not allow children of the type of the`newChild`node, or if the node to append is one of this node's ancestors or this node itself, or if this node is of type`Document`and the DOM application attempts to append a second`DocumentType`or`Element`node. WRONG_DOCUMENT_ERR: Raised if`newChild`was created from a different document than the one that created this node. NO_MODIFICATION_ALLOWED_ERR: Raised if this node is readonly or if the previous parent of the node being inserted is readonly. NOT_SUPPORTED_ERR: if the`newChild`node is a child of the`Document`node, this exception might be raised if the DOM implementation doesn't support the removal of the`DocumentType`child or`Element`child. |

### cloneNode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun cloneNode(deep: Boolean): Node!
```

Returns a duplicate of this node, i.e., serves as a generic copy constructor for nodes. The duplicate node has no parent (`parentNode`is`null`) and no user data. User data associated to the imported node is not carried over. However, if any`UserDataHandlers`has been specified along with the associated data these handlers will be called with the appropriate parameters before this method returns. 
Cloning an`Element`copies all attributes and their values, including those generated by the XML processor to represent defaulted attributes, but this method does not copy any children it contains unless it is a deep clone. This includes text contained in an the`Element`since the text is contained in a child`Text`node. Cloning an`Attr`directly, as opposed to be cloned as part of an`Element`cloning operation, returns a specified attribute (`specified`is`true`). Cloning an`Attr`always clones its children, since they represent its value, no matter whether this is a deep clone or not. Cloning an`EntityReference`automatically constructs its subtree if a corresponding`Entity`is available, no matter whether this is a deep clone or not. Cloning any other type of node simply returns a copy of this node. 
Note that cloning an immutable subtree results in a mutable copy, but the children of an`EntityReference`clone are readonly . In addition, clones of unspecified`Attr`nodes are specified. And, cloning`Document`,`DocumentType`,`Entity`, and`Notation`nodes is implementation dependent.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deep` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If`true`, recursively clone the subtree under the specified node; if`false`, clone only the node itself (and its attributes, if it is an`Element`). |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | The duplicate node. |

### compareDocumentPosition

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun compareDocumentPosition(other: Node!): Short
```

Compares the reference node, i.e. the node on which this method is being called, with a node, i.e. the one passed as a parameter, with regard to their position in the document and according to the document order.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!:The node to compare against the reference node. |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | Returns how the node is positioned relatively to the reference node. |

| Exceptions ||
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | NOT_SUPPORTED_ERR: when the compared nodes are from different DOM implementations that do not coordinate to return consistent implementation-specific results. |

### getAttributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAttributes(): NamedNodeMap!
```

A`NamedNodeMap`containing the attributes of this node (if it is an`Element`) or`null`otherwise. 

### getBaseURI

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBaseURI(): String!
```

The absolute base URI of this node or`null`if the implementation wasn't able to obtain an absolute URI. This value is computed as described in . However, when the`Document`supports the feature "HTML" \ [[DOM Level 2 HTML](http://www.w3.org/TR/2003/REC-DOM-Level-2-HTML-20030109)\] , the base URI is computed using first the value of the href attribute of the HTML BASE element if any, and the value of the`documentURI`attribute from the`Document`interface otherwise. 

### getChildNodes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getChildNodes(): NodeList!
```

A`NodeList`that contains all children of this node. If there are no children, this is a`NodeList`containing no nodes. 

### getFeature

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFeature(
    feature: String!, 
    version: String!
): Any!
```

This method returns a specialized object which implements the specialized APIs of the specified feature and version, as specified in . The specialized object may also be obtained by using binding-specific casting methods but is not necessarily expected to, as discussed in . This method also allow the implementation to provide specialized objects which do not support the`Node`interface.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `feature` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the feature requested. Note that any plus sign "+" prepended to the name of the feature will be ignored since it is not significant in the context of this method. |
| `version` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:This is the version number of the feature to test. |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | Returns an object which implements the specialized APIs of the specified feature and version, if any, or`null`if there is no object which implements interfaces associated with that feature. If the`DOMObject`returned by this method implements the`Node`interface, it must delegate to the primary core`Node`and not return results inconsistent with the primary core`Node`such as attributes, childNodes, etc. |

### getFirstChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFirstChild(): Node!
```

The first child of this node. If there is no such node, this returns`null`. 

### getLastChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLastChild(): Node!
```

The last child of this node. If there is no such node, this returns`null`. 

### getLocalName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLocalName(): String!
```

Returns the local part of the qualified name of this node. 
For nodes of any type other than`ELEMENT_NODE`and`ATTRIBUTE_NODE`and nodes created with a DOM Level 1 method, such as`Document.createElement()`, this is always`null`. 

### getNamespaceURI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNamespaceURI(): String!
```

The namespace URI of this node, or`null`if it is unspecified (see ). 
This is not a computed value that is the result of a namespace lookup based on an examination of the namespace declarations in scope. It is merely the namespace URI given at creation time. 
For nodes of any type other than`ELEMENT_NODE`and`ATTRIBUTE_NODE`and nodes created with a DOM Level 1 method, such as`Document.createElement()`, this is always`null`.

**Note:** Per the*Namespaces in XML* Specification \ [[XML Namespaces](http://www.w3.org/TR/1999/REC-xml-names-19990114/)\] an attribute does not inherit its namespace from the element it is attached to. If an attribute is not explicitly given a namespace, it simply has no namespace. 

### getNextSibling

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNextSibling(): Node!
```

The node immediately following this node. If there is no such node, this returns`null`. 

### getNodeName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNodeName(): String!
```

The name of this node, depending on its type; see the table above. 

### getNodeType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNodeType(): Short
```

A code representing the type of the underlying object, as defined above. 

### getNodeValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNodeValue(): String!
```

The value of this node, depending on its type; see the table above. When it is defined to be`null`, setting it has no effect, including if the node is read-only.

| Exceptions ||
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | DOMSTRING_SIZE_ERR: Raised when it would return more characters than fit in a`DOMString`variable on the implementation platform. |

### getOwnerDocument

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getOwnerDocument(): Document!
```

The`Document`object associated with this node. This is also the`Document`object used to create new nodes. When this node is a`Document`or a`DocumentType`which is not used with any`Document`yet, this is`null`. 

### getParentNode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParentNode(): Node!
```

The parent of this node. All nodes, except`Attr`,`Document`,`DocumentFragment`,`Entity`, and`Notation`may have a parent. However, if a node has just been created and not yet added to the tree, or if it has been removed from the tree, this is`null`. 

### getPrefix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrefix(): String!
```

The namespace prefix of this node, or`null`if it is unspecified. When it is defined to be`null`, setting it has no effect, including if the node is read-only. 
Note that setting this attribute, when permitted, changes the`nodeName`attribute, which holds the qualified name, as well as the`tagName`and`name`attributes of the`Element`and`Attr`interfaces, when applicable. 
Setting the prefix to`null`makes it unspecified, setting it to an empty string is implementation dependent. 
Note also that changing the prefix of an attribute that is known to have a default value, does not make a new attribute with the default value and the original prefix appear, since the`namespaceURI`and`localName`do not change. 
For nodes of any type other than`ELEMENT_NODE`and`ATTRIBUTE_NODE`and nodes created with a DOM Level 1 method, such as`createElement`from the`Document`interface, this is always`null`. 

### getPreviousSibling

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPreviousSibling(): Node!
```

The node immediately preceding this node. If there is no such node, this returns`null`. 

### getTextContent

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTextContent(): String!
```

This attribute returns the text content of this node and its descendants. When it is defined to be`null`, setting it has no effect. On setting, any possible children this node may have are removed and, if it the new string is not empty or`null`, replaced by a single`Text`node containing the string this attribute is set to. 
On getting, no serialization is performed, the returned string does not contain any markup. No whitespace normalization is performed and the returned string does not contain the white spaces in element content (see the attribute`Text.isElementContentWhitespace`). Similarly, on setting, no parsing is performed either, the input string is taken as pure textual content. 
The string returned is made of the text content of this node depending on its type, as defined below:

| Node type | Content |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ELEMENT_NODE, ATTRIBUTE_NODE, ENTITY_NODE, ENTITY_REFERENCE_NODE, DOCUMENT_FRAGMENT_NODE | concatenation of the`textContent`attribute value of every child node, excluding COMMENT_NODE and PROCESSING_INSTRUCTION_NODE nodes. This is the empty string if the node has no children. |
| TEXT_NODE, CDATA_SECTION_NODE, COMMENT_NODE, PROCESSING_INSTRUCTION_NODE | `nodeValue` |
| DOCUMENT_NODE, DOCUMENT_TYPE_NODE, NOTATION_NODE | *null* |

<br />

| Exceptions ||
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | DOMSTRING_SIZE_ERR: Raised when it would return more characters than fit in a`DOMString`variable on the implementation platform. |

### getUserData

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getUserData(key: String!): Any!
```

Retrieves the object associated to a key on a this node. The object must first have been set to this node by calling`setUserData`with the same key.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The key the object is associated to. |

| Return ||
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | Returns the`DOMUserData`associated to the given key on this node, or`null`if there was none. |

### hasAttributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasAttributes(): Boolean
```

Returns whether this node (if it is an element) has any attributes.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns`true`if this node has any attributes,`false`otherwise. |

### hasChildNodes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasChildNodes(): Boolean
```

Returns whether this node has any children.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns`true`if this node has any children,`false`otherwise. |

### insertBefore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun insertBefore(
    newChild: Node!, 
    refChild: Node!
): Node!
```

Inserts the node`newChild`before the existing child node`refChild`. If`refChild`is`null`, insert`newChild`at the end of the list of children. 
If`newChild`is a`DocumentFragment`object, all of its children are inserted, in the same order, before`refChild`. If the`newChild`is already in the tree, it is first removed.

**Note:**Inserting a node before itself is implementation dependent.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newChild` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!:The node to insert. |
| `refChild` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!:The reference node, i.e., the node before which the new node must be inserted. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------|
| [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | The node being inserted. |

| Exceptions ||
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | HIERARCHY_REQUEST_ERR: Raised if this node is of a type that does not allow children of the type of the`newChild`node, or if the node to insert is one of this node's ancestors or this node itself, or if this node is of type`Document`and the DOM application attempts to insert a second`DocumentType`or`Element`node. WRONG_DOCUMENT_ERR: Raised if`newChild`was created from a different document than the one that created this node. NO_MODIFICATION_ALLOWED_ERR: Raised if this node is readonly or if the parent of the node being inserted is readonly. NOT_FOUND_ERR: Raised if`refChild`is not a child of this node. NOT_SUPPORTED_ERR: if this node is of type`Document`, this exception might be raised if the DOM implementation doesn't support the insertion of a`DocumentType`or`Element`node. |

### isDefaultNamespace

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isDefaultNamespace(namespaceURI: String!): Boolean
```

This method checks if the specified`namespaceURI`is the default namespace or not.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------|
| `namespaceURI` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The namespace URI to look for. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns`true`if the specified`namespaceURI`is the default namespace,`false`otherwise. |

### isEqualNode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isEqualNode(arg: Node!): Boolean
```

Tests whether two nodes are equal. 
This method tests for equality of nodes, not sameness (i.e., whether the two nodes are references to the same object) which can be tested with`Node.isSameNode()`. All nodes that are the same will also be equal, though the reverse may not be true. 
Two nodes are equal if and only if the following conditions are satisfied:

- The two nodes are of the same type.
- The following string attributes are equal:`nodeName`,`localName`,`namespaceURI`,`prefix`,`nodeValue`. This is: they are both`null`, or they have the same length and are character for character identical.
- The`attributes``NamedNodeMaps`are equal. This is: they are both`null`, or they have the same length and for each node that exists in one map there is a node that exists in the other map and is equal, although not necessarily at the same index.
- The`childNodes``NodeLists`are equal. This is: they are both`null`, or they have the same length and contain equal nodes at the same index. Note that normalization can affect equality; to avoid this, nodes should be normalized before being compared.

<br />

For two`DocumentType`nodes to be equal, the following conditions must also be satisfied:

- The following string attributes are equal:`publicId`,`systemId`,`internalSubset`.
- The`entities``NamedNodeMaps`are equal.
- The`notations``NamedNodeMaps`are equal.

<br />

On the other hand, the following do not affect equality: the`ownerDocument`,`baseURI`, and`parentNode`attributes, the`specified`attribute for`Attr`nodes, the`schemaTypeInfo`attribute for`Attr`and`Element`nodes, the`Text.isElementContentWhitespace`attribute for`Text`nodes, as well as any user data or event listeners registered on the nodes.

<br />

**Note:**As a general rule, anything not mentioned in the description above is not significant in consideration of equality checking. Note that future versions of this specification may take into account more attributes and implementations conform to this specification are expected to be updated accordingly.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------|
| `arg` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!:The node to compare equality with. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns`true`if the nodes are equal,`false`otherwise. |

### isSameNode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isSameNode(other: Node!): Boolean
```

Returns whether this node is the same node as the given one. 
This method provides a way to determine whether two`Node`references returned by the implementation reference the same object. When two`Node`references are references to the same object, even if through a proxy, the references may be used completely interchangeably, such that all attributes have the same values and calling the same DOM method on either reference always has exactly the same effect.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `other` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!:The node to test against. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns`true`if the nodes are the same,`false`otherwise. |

### isSupported

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isSupported(
    feature: String!, 
    version: String!
): Boolean
```

Tests whether the DOM implementation implements a specific feature and that feature is supported by this node, as specified in .

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `feature` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the feature to test. |
| `version` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:This is the version number of the feature to test. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns`true`if the specified feature is supported on this node,`false`otherwise. |

### lookupNamespaceURI

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun lookupNamespaceURI(prefix: String!): String!
```

Look up the namespace URI associated to the given prefix, starting from this node. 
See for details on the algorithm used by this method.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The prefix to look for. If this parameter is`null`, the method will return the default namespace URI if any. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | Returns the associated namespace URI or`null`if none is found. |

### lookupPrefix

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun lookupPrefix(namespaceURI: String!): String!
```

Look up the prefix associated to the given namespace URI, starting from this node. The default namespace declarations are ignored by this method. 
See for details on the algorithm used by this method.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------|
| `namespaceURI` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The namespace URI to look for. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | Returns an associated namespace prefix if found or`null`if none is found. If more than one prefix are associated to the namespace prefix, the returned namespace prefix is implementation dependent. |

### normalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun normalize(): Unit
```

Puts all`Text`nodes in the full depth of the sub-tree underneath this`Node`, including attribute nodes, into a "normal" form where only structure (e.g., elements, comments, processing instructions, CDATA sections, and entity references) separates`Text`nodes, i.e., there are neither adjacent`Text`nodes nor empty`Text`nodes. This can be used to ensure that the DOM view of a document is the same as if it were saved and re-loaded, and is useful when operations (such as XPointer \ [[XPointer](http://www.w3.org/TR/2003/REC-xptr-framework-20030325/)\] lookups) that depend on a particular document tree structure are to be used. If the parameter "normalize-characters" of the`DOMConfiguration`object attached to the`Node.ownerDocument`is`true`, this method will also fully normalize the characters of the`Text`nodes.

**Note:** In cases where the document contains`CDATASections`, the normalize operation alone may not be sufficient, since XPointers do not differentiate between`Text`nodes and`CDATASection`nodes. 

### removeChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeChild(oldChild: Node!): Node!
```

Removes the child node indicated by`oldChild`from the list of children, and returns it.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------|
| `oldChild` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!:The node being removed. |

| Return ||
|------------------------------------------------------------------------------------|-------------------|
| [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | The node removed. |

| Exceptions ||
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | NO_MODIFICATION_ALLOWED_ERR: Raised if this node is readonly. NOT_FOUND_ERR: Raised if`oldChild`is not a child of this node. NOT_SUPPORTED_ERR: if this node is of type`Document`, this exception might be raised if the DOM implementation doesn't support the removal of the`DocumentType`child or the`Element`child. |

### replaceChild

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun replaceChild(
    newChild: Node!, 
    oldChild: Node!
): Node!
```

Replaces the child node`oldChild`with`newChild`in the list of children, and returns the`oldChild`node. 
If`newChild`is a`DocumentFragment`object,`oldChild`is replaced by all of the`DocumentFragment`children, which are inserted in the same order. If the`newChild`is already in the tree, it is first removed.

**Note:**Replacing a node with itself is implementation dependent.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------|
| `newChild` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!:The new node to put in the child list. |
| `oldChild` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!:The node being replaced in the list. |

| Return ||
|------------------------------------------------------------------------------------|--------------------|
| [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | The node replaced. |

| Exceptions ||
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | HIERARCHY_REQUEST_ERR: Raised if this node is of a type that does not allow children of the type of the`newChild`node, or if the node to put in is one of this node's ancestors or this node itself, or if this node is of type`Document`and the result of the replacement operation would add a second`DocumentType`or`Element`on the`Document`node. WRONG_DOCUMENT_ERR: Raised if`newChild`was created from a different document than the one that created this node. NO_MODIFICATION_ALLOWED_ERR: Raised if this node or the parent of the new node is readonly. NOT_FOUND_ERR: Raised if`oldChild`is not a child of this node. NOT_SUPPORTED_ERR: if this node is of type`Document`, this exception might be raised if the DOM implementation doesn't support the replacement of the`DocumentType`child or`Element`child. |

### setNodeValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNodeValue(nodeValue: String!): Unit
```

The value of this node, depending on its type; see the table above. When it is defined to be`null`, setting it has no effect, including if the node is read-only.

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | NO_MODIFICATION_ALLOWED_ERR: Raised when the node is readonly and if it is not defined to be`null`. |

### setPrefix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setPrefix(prefix: String!): Unit
```

The namespace prefix of this node, or`null`if it is unspecified. When it is defined to be`null`, setting it has no effect, including if the node is read-only. 
Note that setting this attribute, when permitted, changes the`nodeName`attribute, which holds the qualified name, as well as the`tagName`and`name`attributes of the`Element`and`Attr`interfaces, when applicable. 
Setting the prefix to`null`makes it unspecified, setting it to an empty string is implementation dependent. 
Note also that changing the prefix of an attribute that is known to have a default value, does not make a new attribute with the default value and the original prefix appear, since the`namespaceURI`and`localName`do not change. 
For nodes of any type other than`ELEMENT_NODE`and`ATTRIBUTE_NODE`and nodes created with a DOM Level 1 method, such as`createElement`from the`Document`interface, this is always`null`.

| Exceptions ||
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | INVALID_CHARACTER_ERR: Raised if the specified prefix contains an illegal character according to the XML version in use specified in the`Document.xmlVersion`attribute. NO_MODIFICATION_ALLOWED_ERR: Raised if this node is readonly. NAMESPACE_ERR: Raised if the specified`prefix`is malformed per the Namespaces in XML specification, if the`namespaceURI`of this node is`null`, if the specified prefix is "xml" and the`namespaceURI`of this node is different from "<http://www.w3.org/XML/1998/namespace>", if this node is an attribute and the specified prefix is "xmlns" and the`namespaceURI`of this node is different from "<http://www.w3.org/2000/xmlns/>", or if this node is an attribute and the`qualifiedName`of this node is "xmlns" \ [[XML Namespaces](http://www.w3.org/TR/1999/REC-xml-names-19990114/)\] . |

### setTextContent

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTextContent(textContent: String!): Unit
```

This attribute returns the text content of this node and its descendants. When it is defined to be`null`, setting it has no effect. On setting, any possible children this node may have are removed and, if it the new string is not empty or`null`, replaced by a single`Text`node containing the string this attribute is set to. 
On getting, no serialization is performed, the returned string does not contain any markup. No whitespace normalization is performed and the returned string does not contain the white spaces in element content (see the attribute`Text.isElementContentWhitespace`). Similarly, on setting, no parsing is performed either, the input string is taken as pure textual content. 
The string returned is made of the text content of this node depending on its type, as defined below:

| Node type | Content |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ELEMENT_NODE, ATTRIBUTE_NODE, ENTITY_NODE, ENTITY_REFERENCE_NODE, DOCUMENT_FRAGMENT_NODE | concatenation of the`textContent`attribute value of every child node, excluding COMMENT_NODE and PROCESSING_INSTRUCTION_NODE nodes. This is the empty string if the node has no children. |
| TEXT_NODE, CDATA_SECTION_NODE, COMMENT_NODE, PROCESSING_INSTRUCTION_NODE | `nodeValue` |
| DOCUMENT_NODE, DOCUMENT_TYPE_NODE, NOTATION_NODE | *null* |

<br />

| Exceptions ||
|----------------------------|----------------------------------------------------------------|
| `org.w3c.dom.DOMException` | NO_MODIFICATION_ALLOWED_ERR: Raised when the node is readonly. |

### setUserData

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setUserData(
    key: String!, 
    data: Any!, 
    handler: UserDataHandler!
): Any!
```

Associate an object to a key on this node. The object can later be retrieved from this node by calling`getUserData`with the same key.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The key to associate the object to. |
| `data` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The object to associate to the given key, or`null`to remove any existing association to that key. |
| `handler` | [UserDataHandler](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-user-data-handler/index.html)!:The handler to associate to that key, or`null`. |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | Returns the`DOMUserData`previously associated to the given key on this node, or`null`if there was none. |
