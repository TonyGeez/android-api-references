# Document

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Document

```
interface Document : Node
```

| [org.w3c.dom.Document](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#) |

The `Document` interface represents the entire HTML or XML document. Conceptually, it is the root of the document tree, and provides the primary access to the document's data.

Since elements, text nodes, comments, processing instructions, etc. cannot exist outside the context of a `Document`, the `Document` interface also contains the factory methods needed to create these objects. The `Node` objects created have a `ownerDocument` attribute which associates them with the `Document` within whose context they were created.

See also the [Document Object Model (DOM) Level 3 Core Specification](http://www.w3.org/TR/2004/REC-DOM-Level-3-Core-20040407).

## Summary

| Inherited constants ||
|---|---|
| From class [Node](https://developer.android.com/reference/kotlin/org/w3c/dom/Node) |--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [ATTRIBUTE_NODE](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#ATTRIBUTE_NODE:kotlin.Short) The node is an `Attr`. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [CDATA_SECTION_NODE](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#CDATA_SECTION_NODE:kotlin.Short) The node is a `CDATASection`. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [COMMENT_NODE](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#COMMENT_NODE:kotlin.Short) The node is a `Comment`. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [DOCUMENT_FRAGMENT_NODE](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#DOCUMENT_FRAGMENT_NODE:kotlin.Short) The node is a `DocumentFragment`. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [DOCUMENT_NODE](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#DOCUMENT_NODE:kotlin.Short) The node is a `Document`. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [DOCUMENT_POSITION_CONTAINED_BY](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#DOCUMENT_POSITION_CONTAINED_BY:kotlin.Short) The node is contained by the reference node. A node which is contained is always following, too. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [DOCUMENT_POSITION_CONTAINS](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#DOCUMENT_POSITION_CONTAINS:kotlin.Short) The node contains the reference node. A node which contains is always preceding, too. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [DOCUMENT_POSITION_DISCONNECTED](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#DOCUMENT_POSITION_DISCONNECTED:kotlin.Short) The two nodes are disconnected. Order between disconnected nodes is always implementation-specific. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [DOCUMENT_POSITION_FOLLOWING](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#DOCUMENT_POSITION_FOLLOWING:kotlin.Short) The node follows the reference node. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [DOCUMENT_POSITION_IMPLEMENTATION_SPECIFIC](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#DOCUMENT_POSITION_IMPLEMENTATION_SPECIFIC:kotlin.Short) The determination of preceding versus following is implementation-specific. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [DOCUMENT_POSITION_PRECEDING](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#DOCUMENT_POSITION_PRECEDING:kotlin.Short) The second node precedes the reference node. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [DOCUMENT_TYPE_NODE](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#DOCUMENT_TYPE_NODE:kotlin.Short) The node is a `DocumentType`. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [ELEMENT_NODE](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#ELEMENT_NODE:kotlin.Short) The node is an `Element`. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [ENTITY_NODE](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#ENTITY_NODE:kotlin.Short) The node is an `Entity`. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [ENTITY_REFERENCE_NODE](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#ENTITY_REFERENCE_NODE:kotlin.Short) The node is an `EntityReference`. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [NOTATION_NODE](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#NOTATION_NODE:kotlin.Short) The node is a `Notation`. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [PROCESSING_INSTRUCTION_NODE](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#PROCESSING_INSTRUCTION_NODE:kotlin.Short) The node is a `ProcessingInstruction`. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [TEXT_NODE](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#TEXT_NODE:kotlin.Short) The node is a `Text` node. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [adoptNode](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#adoptNode(org.w3c.dom.Node))`(`source:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`)` Attempts to adopt a node from another document to this document. |
| abstract [Attr](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-attr/index.html)! | [createAttribute](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#createAttribute(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates an `Attr` of the given name. |
| abstract [Attr](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-attr/index.html)! | [createAttributeNS](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#createAttributeNS(kotlin.String,%20kotlin.String))`(`namespaceURI:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `qualifiedName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates an attribute of the given qualified name and namespace URI. |
| --- | --- |
| abstract [CDATASection](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-c-d-a-t-a-section/index.html)! | [createCDATASection](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#createCDATASection(kotlin.String))`(`data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a `CDATASection` node whose value is the specified string. |
| abstract [Comment](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-comment/index.html)! | [createComment](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#createComment(kotlin.String))`(`data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a `Comment` node given the specified string. |
| abstract [DocumentFragment](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document-fragment/index.html)! | [createDocumentFragment](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#createDocumentFragment())`()` Creates an empty `DocumentFragment` object. |
| --- | --- |
| abstract [Element](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-element/index.html)! | [createElement](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#createElement(kotlin.String))`(`tagName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates an element of the type specified. |
| abstract [Element](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-element/index.html)! | [createElementNS](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#createElementNS(kotlin.String,%20kotlin.String))`(`namespaceURI:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `qualifiedName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates an element of the given qualified name and namespace URI. |
| abstract [EntityReference](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-entity-reference/index.html)! | [createEntityReference](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#createEntityReference(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates an `EntityReference` object. |
| --- | --- |
| abstract [ProcessingInstruction](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-processing-instruction/index.html)! | [createProcessingInstruction](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#createProcessingInstruction(kotlin.String,%20kotlin.String))`(`target:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a `ProcessingInstruction` node given the specified name and data strings. |
| abstract [Text](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-text/index.html)! | [createTextNode](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#createTextNode(kotlin.String))`(`data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a `Text` node given the specified string. |
| abstract [DocumentType](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document-type/index.html)! | [getDoctype](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#getDoctype())`()` The Document Type Declaration (see `DocumentType`) associated with this document. |
| --- | --- |
| abstract [Element](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-element/index.html)! | [getDocumentElement](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#getDocumentElement())`()` This is a convenience attribute that allows direct access to the child node that is the document element of the document. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDocumentURI](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#getDocumentURI())`()` The location of the document or `null` if undefined or if the `Document` was created using `DOMImplementation.createDocument`. |
| abstract [DOMConfiguration](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-d-o-m-configuration/index.html)! | [getDomConfig](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#getDomConfig())`()` The configuration used when `Document.normalizeDocument()` is invoked. |
| --- | --- |
| abstract [Element](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-element/index.html)! | [getElementById](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#getElementById(kotlin.String))`(`elementId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the `Element` that has an ID attribute with the given value. |
| abstract [NodeList](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node-list/index.html)! | [getElementsByTagName](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#getElementsByTagName(kotlin.String))`(`tagname:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a `NodeList` of all the `Elements` in document order with a given tag name and are contained in the document. |
| abstract [NodeList](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node-list/index.html)! | [getElementsByTagNameNS](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#getElementsByTagNameNS(kotlin.String,%20kotlin.String))`(`namespaceURI:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a `NodeList` of all the `Elements` with a given local name and namespace URI in document order. |
| --- | --- |
| abstract [DOMImplementation](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-d-o-m-implementation/index.html)! | [getImplementation](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#getImplementation())`()` The `DOMImplementation` object that handles this document. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getInputEncoding](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#getInputEncoding())`()` An attribute specifying the encoding used for this document at the time of the parsing. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getStrictErrorChecking](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#getStrictErrorChecking())`()` An attribute specifying whether error checking is enforced or not. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getXmlEncoding](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#getXmlEncoding())`()` An attribute specifying, as part of the [XML declaration](http://www.w3.org/TR/2004/REC-xml-20040204#NT-XMLDecl), the encoding of this document. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getXmlStandalone](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#getXmlStandalone())`()` An attribute specifying, as part of the [XML declaration](http://www.w3.org/TR/2004/REC-xml-20040204#NT-XMLDecl), whether this document is standalone. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getXmlVersion](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#getXmlVersion())`()` An attribute specifying, as part of the [XML declaration](http://www.w3.org/TR/2004/REC-xml-20040204#NT-XMLDecl), the version number of this document. |
| --- | --- |
| abstract [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [importNode](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#importNode(org.w3c.dom.Node,%20kotlin.Boolean))`(`importedNode:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`, `deep:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Imports a node from another document to this document, without altering or removing the source node from the original document; this method creates a new copy of the source node. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [normalizeDocument](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#normalizeDocument())`()` This method acts as if the document was going through a save and load cycle, putting the document in a "normal" form. |
| abstract [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [renameNode](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#renameNode(org.w3c.dom.Node,%20kotlin.String,%20kotlin.String))`(`n:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`, `namespaceURI:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `qualifiedName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Rename an existing node of type `ELEMENT_NODE` or `ATTRIBUTE_NODE`. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDocumentURI](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#setDocumentURI(kotlin.String))`(`documentURI:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` The location of the document or `null` if undefined or if the `Document` was created using `DOMImplementation.createDocument`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStrictErrorChecking](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#setStrictErrorChecking(kotlin.Boolean))`(`strictErrorChecking:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` An attribute specifying whether error checking is enforced or not. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setXmlStandalone](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#setXmlStandalone(kotlin.Boolean))`(`xmlStandalone:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` An attribute specifying, as part of the [XML declaration](http://www.w3.org/TR/2004/REC-xml-20040204#NT-XMLDecl), whether this document is standalone. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setXmlVersion](https://developer.android.com/reference/kotlin/org/w3c/dom/Document#setXmlVersion(kotlin.String))`(`xmlVersion:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` An attribute specifying, as part of the [XML declaration](http://www.w3.org/TR/2004/REC-xml-20040204#NT-XMLDecl), the version number of this document. |

| Inherited functions ||
|---|---|
| From class [Node](https://developer.android.com/reference/kotlin/org/w3c/dom/Node) |------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [appendChild](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#appendChild(org.w3c.dom.Node))`(`newChild:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`)` Adds the node `newChild` to the end of the list of children of this node. If the `newChild` is already in the tree, it is first removed. <br /> | | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [cloneNode](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#cloneNode(kotlin.Boolean))`(`deep:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns a duplicate of this node, i.e., serves as a generic copy constructor for nodes. The duplicate node has no parent ( `parentNode` is `null`) and no user data. User data associated to the imported node is not carried over. However, if any `UserDataHandlers` has been specified along with the associated data these handlers will be called with the appropriate parameters before this method returns. Cloning an `Element` copies all attributes and their values, including those generated by the XML processor to represent defaulted attributes, but this method does not copy any children it contains unless it is a deep clone. This includes text contained in an the `Element` since the text is contained in a child `Text` node. Cloning an `Attr` directly, as opposed to be cloned as part of an `Element` cloning operation, returns a specified attribute (`specified` is `true`). Cloning an `Attr` always clones its children, since they represent its value, no matter whether this is a deep clone or not. Cloning an `EntityReference` automatically constructs its subtree if a corresponding `Entity` is available, no matter whether this is a deep clone or not. Cloning any other type of node simply returns a copy of this node. Note that cloning an immutable subtree results in a mutable copy, but the children of an `EntityReference` clone are readonly . In addition, clones of unspecified `Attr` nodes are specified. And, cloning `Document`, `DocumentType`, `Entity`, and `Notation` nodes is implementation dependent. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [compareDocumentPosition](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#compareDocumentPosition(org.w3c.dom.Node))`(`other:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`)` Compares the reference node, i.e. the node on which this method is being called, with a node, i.e. the one passed as a parameter, with regard to their position in the document and according to the document order. <br /> | | [NamedNodeMap](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-named-node-map/index.html)! | [getAttributes](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getAttributes())`()` A `NamedNodeMap` containing the attributes of this node (if it is an `Element`) or `null` otherwise. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getBaseURI](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getBaseURI())`()` The absolute base URI of this node or `null` if the implementation wasn't able to obtain an absolute URI. This value is computed as described in . However, when the `Document` supports the feature "HTML" \ [[DOM Level 2 HTML](http://www.w3.org/TR/2003/REC-DOM-Level-2-HTML-20030109)\] , the base URI is computed using first the value of the href attribute of the HTML BASE element if any, and the value of the `documentURI` attribute from the `Document` interface otherwise. <br /> | | [NodeList](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node-list/index.html)! | [getChildNodes](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getChildNodes())`()` A `NodeList` that contains all children of this node. If there are no children, this is a `NodeList` containing no nodes. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getFeature](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getFeature(kotlin.String,%20kotlin.String))`(`feature:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `version:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` This method returns a specialized object which implements the specialized APIs of the specified feature and version, as specified in . The specialized object may also be obtained by using binding-specific casting methods but is not necessarily expected to, as discussed in . This method also allow the implementation to provide specialized objects which do not support the `Node` interface. <br /> | | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [getFirstChild](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getFirstChild())`()` The first child of this node. If there is no such node, this returns `null`. <br /> | | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [getLastChild](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getLastChild())`()` The last child of this node. If there is no such node, this returns `null`. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLocalName](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getLocalName())`()` Returns the local part of the qualified name of this node. For nodes of any type other than `ELEMENT_NODE` and `ATTRIBUTE_NODE` and nodes created with a DOM Level 1 method, such as `Document.createElement()`, this is always `null`. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNamespaceURI](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getNamespaceURI())`()` The namespace URI of this node, or `null` if it is unspecified (see ). This is not a computed value that is the result of a namespace lookup based on an examination of the namespace declarations in scope. It is merely the namespace URI given at creation time. For nodes of any type other than `ELEMENT_NODE` and `ATTRIBUTE_NODE` and nodes created with a DOM Level 1 method, such as `Document.createElement()`, this is always `null`. **Note:** Per the *Namespaces in XML* Specification \ [[XML Namespaces](http://www.w3.org/TR/1999/REC-xml-names-19990114/)\] an attribute does not inherit its namespace from the element it is attached to. If an attribute is not explicitly given a namespace, it simply has no namespace. <br /> | | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [getNextSibling](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getNextSibling())`()` The node immediately following this node. If there is no such node, this returns `null`. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNodeName](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getNodeName())`()` The name of this node, depending on its type; see the table above. <br /> | | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getNodeType](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getNodeType())`()` A code representing the type of the underlying object, as defined above. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNodeValue](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getNodeValue())`()` The value of this node, depending on its type; see the table above. When it is defined to be `null`, setting it has no effect, including if the node is read-only. <br /> | | [Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html)! | [getOwnerDocument](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getOwnerDocument())`()` The `Document` object associated with this node. This is also the `Document` object used to create new nodes. When this node is a `Document` or a `DocumentType` which is not used with any `Document` yet, this is `null`. <br /> | | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [getParentNode](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getParentNode())`()` The parent of this node. All nodes, except `Attr`, `Document`, `DocumentFragment`, `Entity`, and `Notation` may have a parent. However, if a node has just been created and not yet added to the tree, or if it has been removed from the tree, this is `null`. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPrefix](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getPrefix())`()` The namespace prefix of this node, or `null` if it is unspecified. When it is defined to be `null`, setting it has no effect, including if the node is read-only. Note that setting this attribute, when permitted, changes the `nodeName` attribute, which holds the qualified name, as well as the `tagName` and `name` attributes of the `Element` and `Attr` interfaces, when applicable. Setting the prefix to `null` makes it unspecified, setting it to an empty string is implementation dependent. Note also that changing the prefix of an attribute that is known to have a default value, does not make a new attribute with the default value and the original prefix appear, since the `namespaceURI` and `localName` do not change. For nodes of any type other than `ELEMENT_NODE` and `ATTRIBUTE_NODE` and nodes created with a DOM Level 1 method, such as `createElement` from the `Document` interface, this is always `null`. <br /> | | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [getPreviousSibling](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getPreviousSibling())`()` The node immediately preceding this node. If there is no such node, this returns `null`. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTextContent](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getTextContent())`()` This attribute returns the text content of this node and its descendants. When it is defined to be `null`, setting it has no effect. On setting, any possible children this node may have are removed and, if it the new string is not empty or `null`, replaced by a single `Text` node containing the string this attribute is set to. On getting, no serialization is performed, the returned string does not contain any markup. No whitespace normalization is performed and the returned string does not contain the white spaces in element content (see the attribute `Text.isElementContentWhitespace`). Similarly, on setting, no parsing is performed either, the input string is taken as pure textual content. The string returned is made of the text content of this node depending on its type, as defined below: | Node type | Content | |------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | ELEMENT_NODE, ATTRIBUTE_NODE, ENTITY_NODE, ENTITY_REFERENCE_NODE, DOCUMENT_FRAGMENT_NODE | concatenation of the `textContent` attribute value of every child node, excluding COMMENT_NODE and PROCESSING_INSTRUCTION_NODE nodes. This is the empty string if the node has no children. | | TEXT_NODE, CDATA_SECTION_NODE, COMMENT_NODE, PROCESSING_INSTRUCTION_NODE | `nodeValue` | | DOCUMENT_NODE, DOCUMENT_TYPE_NODE, NOTATION_NODE | *null* | <br /> <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getUserData](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#getUserData(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the object associated to a key on a this node. The object must first have been set to this node by calling `setUserData` with the same key. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasAttributes](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#hasAttributes())`()` Returns whether this node (if it is an element) has any attributes. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasChildNodes](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#hasChildNodes())`()` Returns whether this node has any children. <br /> | | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [insertBefore](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#insertBefore(org.w3c.dom.Node,%20org.w3c.dom.Node))`(`newChild:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`, `refChild:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`)` Inserts the node `newChild` before the existing child node `refChild`. If `refChild` is `null`, insert `newChild` at the end of the list of children. If `newChild` is a `DocumentFragment` object, all of its children are inserted, in the same order, before `refChild`. If the `newChild` is already in the tree, it is first removed. **Note:** Inserting a node before itself is implementation dependent. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDefaultNamespace](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#isDefaultNamespace(kotlin.String))`(`namespaceURI:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` This method checks if the specified `namespaceURI` is the default namespace or not. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEqualNode](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#isEqualNode(org.w3c.dom.Node))`(`arg:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`)` Tests whether two nodes are equal. This method tests for equality of nodes, not sameness (i.e., whether the two nodes are references to the same object) which can be tested with `Node.isSameNode()`. All nodes that are the same will also be equal, though the reverse may not be true. Two nodes are equal if and only if the following conditions are satisfied: - The two nodes are of the same type. - The following string attributes are equal: `nodeName`, `localName`, `namespaceURI`, `prefix`, `nodeValue` . This is: they are both `null`, or they have the same length and are character for character identical. - The `attributes` `NamedNodeMaps` are equal. This is: they are both `null`, or they have the same length and for each node that exists in one map there is a node that exists in the other map and is equal, although not necessarily at the same index. - The `childNodes` `NodeLists` are equal. This is: they are both `null`, or they have the same length and contain equal nodes at the same index. Note that normalization can affect equality; to avoid this, nodes should be normalized before being compared. <br /> For two `DocumentType` nodes to be equal, the following conditions must also be satisfied: - The following string attributes are equal: `publicId`, `systemId`, `internalSubset`. - The `entities` `NamedNodeMaps` are equal. - The `notations` `NamedNodeMaps` are equal. <br /> On the other hand, the following do not affect equality: the `ownerDocument`, `baseURI`, and `parentNode` attributes, the `specified` attribute for `Attr` nodes, the `schemaTypeInfo` attribute for `Attr` and `Element` nodes, the `Text.isElementContentWhitespace` attribute for `Text` nodes, as well as any user data or event listeners registered on the nodes. <br /> **Note:** As a general rule, anything not mentioned in the description above is not significant in consideration of equality checking. Note that future versions of this specification may take into account more attributes and implementations conform to this specification are expected to be updated accordingly. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSameNode](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#isSameNode(org.w3c.dom.Node))`(`other:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`)` Returns whether this node is the same node as the given one. This method provides a way to determine whether two `Node` references returned by the implementation reference the same object. When two `Node` references are references to the same object, even if through a proxy, the references may be used completely interchangeably, such that all attributes have the same values and calling the same DOM method on either reference always has exactly the same effect. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#isSupported(kotlin.String,%20kotlin.String))`(`feature:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `version:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Tests whether the DOM implementation implements a specific feature and that feature is supported by this node, as specified in . <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [lookupNamespaceURI](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#lookupNamespaceURI(kotlin.String))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up the namespace URI associated to the given prefix, starting from this node. See for details on the algorithm used by this method. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [lookupPrefix](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#lookupPrefix(kotlin.String))`(`namespaceURI:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up the prefix associated to the given namespace URI, starting from this node. The default namespace declarations are ignored by this method. See for details on the algorithm used by this method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [normalize](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#normalize())`()` Puts all `Text` nodes in the full depth of the sub-tree underneath this `Node`, including attribute nodes, into a "normal" form where only structure (e.g., elements, comments, processing instructions, CDATA sections, and entity references) separates `Text` nodes, i.e., there are neither adjacent `Text` nodes nor empty `Text` nodes. This can be used to ensure that the DOM view of a document is the same as if it were saved and re-loaded, and is useful when operations (such as XPointer \ [[XPointer](http://www.w3.org/TR/2003/REC-xptr-framework-20030325/)\] lookups) that depend on a particular document tree structure are to be used. If the parameter "normalize-characters" of the `DOMConfiguration` object attached to the `Node.ownerDocument` is `true`, this method will also fully normalize the characters of the `Text` nodes. **Note:** In cases where the document contains `CDATASections`, the normalize operation alone may not be sufficient, since XPointers do not differentiate between `Text` nodes and `CDATASection` nodes. <br /> | | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [removeChild](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#removeChild(org.w3c.dom.Node))`(`oldChild:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`)` Removes the child node indicated by `oldChild` from the list of children, and returns it. <br /> | | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [replaceChild](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#replaceChild(org.w3c.dom.Node,%20org.w3c.dom.Node))`(`newChild:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`, `oldChild:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`)` Replaces the child node `oldChild` with `newChild` in the list of children, and returns the `oldChild` node. If `newChild` is a `DocumentFragment` object, `oldChild` is replaced by all of the `DocumentFragment` children, which are inserted in the same order. If the `newChild` is already in the tree, it is first removed. **Note:** Replacing a node with itself is implementation dependent. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNodeValue](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#setNodeValue(kotlin.String))`(`nodeValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` The value of this node, depending on its type; see the table above. When it is defined to be `null`, setting it has no effect, including if the node is read-only. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPrefix](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#setPrefix(kotlin.String))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` The namespace prefix of this node, or `null` if it is unspecified. When it is defined to be `null`, setting it has no effect, including if the node is read-only. Note that setting this attribute, when permitted, changes the `nodeName` attribute, which holds the qualified name, as well as the `tagName` and `name` attributes of the `Element` and `Attr` interfaces, when applicable. Setting the prefix to `null` makes it unspecified, setting it to an empty string is implementation dependent. Note also that changing the prefix of an attribute that is known to have a default value, does not make a new attribute with the default value and the original prefix appear, since the `namespaceURI` and `localName` do not change. For nodes of any type other than `ELEMENT_NODE` and `ATTRIBUTE_NODE` and nodes created with a DOM Level 1 method, such as `createElement` from the `Document` interface, this is always `null`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTextContent](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#setTextContent(kotlin.String))`(`textContent:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` This attribute returns the text content of this node and its descendants. When it is defined to be `null`, setting it has no effect. On setting, any possible children this node may have are removed and, if it the new string is not empty or `null`, replaced by a single `Text` node containing the string this attribute is set to. On getting, no serialization is performed, the returned string does not contain any markup. No whitespace normalization is performed and the returned string does not contain the white spaces in element content (see the attribute `Text.isElementContentWhitespace`). Similarly, on setting, no parsing is performed either, the input string is taken as pure textual content. The string returned is made of the text content of this node depending on its type, as defined below: | Node type | Content | |------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | ELEMENT_NODE, ATTRIBUTE_NODE, ENTITY_NODE, ENTITY_REFERENCE_NODE, DOCUMENT_FRAGMENT_NODE | concatenation of the `textContent` attribute value of every child node, excluding COMMENT_NODE and PROCESSING_INSTRUCTION_NODE nodes. This is the empty string if the node has no children. | | TEXT_NODE, CDATA_SECTION_NODE, COMMENT_NODE, PROCESSING_INSTRUCTION_NODE | `nodeValue` | | DOCUMENT_NODE, DOCUMENT_TYPE_NODE, NOTATION_NODE | *null* | <br /> <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [setUserData](https://developer.android.com/reference/kotlin/org/w3c/dom/Node#setUserData(kotlin.String,%20kotlin.Any,%20org.w3c.dom.UserDataHandler))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `data:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `handler:` ` [UserDataHandler](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-user-data-handler/index.html)!`)` Associate an object to a key on this node. The object can later be retrieved from this node by calling `getUserData` with the same key. <br /> | ||

## Public methods

### adoptNode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun adoptNode(source: Node!): Node!
```

Attempts to adopt a node from another document to this document. If supported, it changes the `ownerDocument` of the source node, its children, as well as the attached attribute nodes if there are any. If the source node has a parent it is first removed from the child list of its parent. This effectively allows moving a subtree from one document to another (unlike `importNode()` which create a copy of the source node instead of moving it). When it fails, applications should use `Document.importNode()` instead. Note that if the adopted node is already part of this document (i.e. the source and target document are the same), this method still has the effect of removing the source node from the child list of its parent, if any. The following list describes the specifics for each type of node.

ATTRIBUTE_NODE
: The `ownerElement` attribute is set to `null` and the `specified` flag is set to `true` on the adopted `Attr`. The descendants of the source `Attr` are recursively adopted.

DOCUMENT_FRAGMENT_NODE
: The descendants of the source node are recursively adopted.

DOCUMENT_NODE
: `Document` nodes cannot be adopted.

DOCUMENT_TYPE_NODE
: `DocumentType` nodes cannot be adopted.

ELEMENT_NODE
: *Specified* attribute nodes of the source element are adopted. Default attributes are discarded, though if the document being adopted into defines default attributes for this element name, those are assigned. The descendants of the source element are recursively adopted.

ENTITY_NODE
: `Entity` nodes cannot be adopted.

ENTITY_REFERENCE_NODE
: Only the `EntityReference` node itself is adopted, the descendants are discarded, since the source and destination documents might have defined the entity differently. If the document being imported into provides a definition for this entity name, its value is assigned.

NOTATION_NODE
: `Notation` nodes cannot be adopted.

PROCESSING_INSTRUCTION_NODE, TEXT_NODE, CDATA_SECTION_NODE, COMMENT_NODE
: These nodes can all be adopted. No specifics.

<br />

**Note:** Since it does not create new nodes unlike the `Document.importNode()` method, this method does not raise an `INVALID_CHARACTER_ERR` exception, and applications should use the `Document.normalizeDocument()` method to check if an imported name is not an XML name according to the XML version in use.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------|
| `source` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!: The node to move into this document. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | The adopted node, or `null` if this operation fails, such as when the source node comes from a different implementation. |

| Exceptions ||
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | NOT_SUPPORTED_ERR: Raised if the source node is of type `DOCUMENT`, `DOCUMENT_TYPE`. NO_MODIFICATION_ALLOWED_ERR: Raised when the source node is readonly. |

### createAttribute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createAttribute(name: String!): Attr!
```

Creates an `Attr` of the given name. Note that the `Attr` instance can then be set on an `Element` using the `setAttributeNode` method. 
To create an attribute with a qualified name and namespace URI, use the `createAttributeNS` method.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the attribute. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Attr](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-attr/index.html)! | A new `Attr` object with the `nodeName` attribute set to `name`, and `localName`, `prefix`, and `namespaceURI` set to `null`. The value of the attribute is the empty string. |

| Exceptions ||
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | INVALID_CHARACTER_ERR: Raised if the specified name is not an XML name according to the XML version in use specified in the `Document.xmlVersion` attribute. |

### createAttributeNS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createAttributeNS(
    namespaceURI: String!, 
    qualifiedName: String!
): Attr!
```

Creates an attribute of the given qualified name and namespace URI. 
Per \ [[XML Namespaces](http://www.w3.org/TR/1999/REC-xml-names-19990114/)\] , applications must use the value `null` as the `namespaceURI` parameter for methods if they wish to have no namespace.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `namespaceURI` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The namespace URI of the attribute to create. |
| `qualifiedName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The qualified name of the attribute to instantiate. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Attr](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-attr/index.html)! | A new `Attr` object with the following attributes: | Attribute | Value | |---------------------|-------------------------------------------------------------------------| | `Node.nodeName` | qualifiedName | | `Node.namespaceURI` | `namespaceURI` | | `Node.prefix` | prefix, extracted from `qualifiedName`, or `null` if there is no prefix | | `Node.localName` | local name, extracted from `qualifiedName` | | `Attr.name` | `qualifiedName` | | `Node.nodeValue` | the empty string | |

| Exceptions ||
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | INVALID_CHARACTER_ERR: Raised if the specified `qualifiedName` is not an XML name according to the XML version in use specified in the `Document.xmlVersion` attribute. NAMESPACE_ERR: Raised if the `qualifiedName` is a malformed qualified name, if the `qualifiedName` has a prefix and the `namespaceURI` is `null`, if the `qualifiedName` has a prefix that is "xml" and the `namespaceURI` is different from "<http://www.w3.org/XML/1998/namespace>", if the `qualifiedName` or its prefix is "xmlns" and the `namespaceURI` is different from "<http://www.w3.org/2000/xmlns/>", or if the `namespaceURI` is "<http://www.w3.org/2000/xmlns/>" and neither the `qualifiedName` nor its prefix is "xmlns". NOT_SUPPORTED_ERR: Always thrown if the current document does not support the `"XML"` feature, since namespaces were defined by XML. |

### createCDATASection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createCDATASection(data: String!): CDATASection!
```

Creates a `CDATASection` node whose value is the specified string.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------|
| `data` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The data for the `CDATASection` contents. |

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------|
| [CDATASection](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-c-d-a-t-a-section/index.html)! | The new `CDATASection` object. |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------|
| `org.w3c.dom.DOMException` | NOT_SUPPORTED_ERR: Raised if this document is an HTML document. |

### createComment

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createComment(data: String!): Comment!
```

Creates a `Comment` node given the specified string.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------|
| `data` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The data for the node. |

| Return ||
|------------------------------------------------------------------------------------------|---------------------------|
| [Comment](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-comment/index.html)! | The new `Comment` object. |

### createDocumentFragment

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createDocumentFragment(): DocumentFragment!
```

Creates an empty `DocumentFragment` object.

| Return ||
|-------------------------------------------------------------------------------------------------------------|---------------------------|
| [DocumentFragment](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document-fragment/index.html)! | A new `DocumentFragment`. |

### createElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createElement(tagName: String!): Element!
```

Creates an element of the type specified. Note that the instance returned implements the `Element` interface, so attributes can be specified directly on the returned object. 
In addition, if there are known attributes with default values, `Attr` nodes representing them are automatically created and attached to the element. 
To create an element with a qualified name and namespace URI, use the `createElementNS` method.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tagName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the element type to instantiate. For XML, this is case-sensitive, otherwise it depends on the case-sensitivity of the markup language in use. In that case, the name is mapped to the canonical form of that markup by the DOM implementation. |

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [Element](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-element/index.html)! | A new `Element` object with the `nodeName` attribute set to `tagName`, and `localName`, `prefix`, and `namespaceURI` set to `null`. |

| Exceptions ||
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | INVALID_CHARACTER_ERR: Raised if the specified name is not an XML name according to the XML version in use specified in the `Document.xmlVersion` attribute. |

### createElementNS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createElementNS(
    namespaceURI: String!, 
    qualifiedName: String!
): Element!
```

Creates an element of the given qualified name and namespace URI. 
Per \ [[XML Namespaces](http://www.w3.org/TR/1999/REC-xml-names-19990114/)\] , applications must use the value `null` as the namespaceURI parameter for methods if they wish to have no namespace.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `namespaceURI` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The namespace URI of the element to create. |
| `qualifiedName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The qualified name of the element type to instantiate. |

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Element](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-element/index.html)! | A new `Element` object with the following attributes: | Attribute | Value | |---------------------|-------------------------------------------------------------------------| | `Node.nodeName` | `qualifiedName` | | `Node.namespaceURI` | `namespaceURI` | | `Node.prefix` | prefix, extracted from `qualifiedName`, or `null` if there is no prefix | | `Node.localName` | local name, extracted from `qualifiedName` | | `Element.tagName` | `qualifiedName` | |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | INVALID_CHARACTER_ERR: Raised if the specified `qualifiedName` is not an XML name according to the XML version in use specified in the `Document.xmlVersion` attribute. NAMESPACE_ERR: Raised if the `qualifiedName` is a malformed qualified name, if the `qualifiedName` has a prefix and the `namespaceURI` is `null`, or if the `qualifiedName` has a prefix that is "xml" and the `namespaceURI` is different from "<http://www.w3.org/XML/1998/namespace>" \ [[XML Namespaces](http://www.w3.org/TR/1999/REC-xml-names-19990114/)\] , or if the `qualifiedName` or its prefix is "xmlns" and the `namespaceURI` is different from "<http://www.w3.org/2000/xmlns/>", or if the `namespaceURI` is "<http://www.w3.org/2000/xmlns/>" and neither the `qualifiedName` nor its prefix is "xmlns". NOT_SUPPORTED_ERR: Always thrown if the current document does not support the `"XML"` feature, since namespaces were defined by XML. |

### createEntityReference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createEntityReference(name: String!): EntityReference!
```

Creates an `EntityReference` object. In addition, if the referenced entity is known, the child list of the `EntityReference` node is made the same as that of the corresponding `Entity` node.

**Note:** If any descendant of the `Entity` node has an unbound namespace prefix, the corresponding descendant of the created `EntityReference` node is also unbound; (its `namespaceURI` is `null`). The DOM Level 2 and 3 do not support any mechanism to resolve namespace prefixes in this case.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the entity to reference.Unlike `Document.createElementNS` or `Document.createAttributeNS`, no namespace well-formed checking is done on the entity name. Applications should invoke `Document.normalizeDocument()` with the parameter " namespaces" set to `true` in order to ensure that the entity name is namespace well-formed. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-----------------------------------|
| [EntityReference](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-entity-reference/index.html)! | The new `EntityReference` object. |

| Exceptions ||
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | INVALID_CHARACTER_ERR: Raised if the specified name is not an XML name according to the XML version in use specified in the `Document.xmlVersion` attribute. NOT_SUPPORTED_ERR: Raised if this document is an HTML document. |

### createProcessingInstruction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createProcessingInstruction(
    target: String!, 
    data: String!
): ProcessingInstruction!
```

Creates a `ProcessingInstruction` node given the specified name and data strings.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The target part of the processing instruction.Unlike `Document.createElementNS` or `Document.createAttributeNS`, no namespace well-formed checking is done on the target name. Applications should invoke `Document.normalizeDocument()` with the parameter " namespaces" set to `true` in order to ensure that the target name is namespace well-formed. |
| `data` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The data for the node. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [ProcessingInstruction](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-processing-instruction/index.html)! | The new `ProcessingInstruction` object. |

| Exceptions ||
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | INVALID_CHARACTER_ERR: Raised if the specified target is not an XML name according to the XML version in use specified in the `Document.xmlVersion` attribute. NOT_SUPPORTED_ERR: Raised if this document is an HTML document. |

### createTextNode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createTextNode(data: String!): Text!
```

Creates a `Text` node given the specified string.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------|
| `data` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The data for the node. |

| Return ||
|------------------------------------------------------------------------------------|------------------------|
| [Text](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-text/index.html)! | The new `Text` object. |

### getDoctype

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDoctype(): DocumentType!
```

The Document Type Declaration (see `DocumentType`) associated with this document. For XML documents without a document type declaration this returns `null`. For HTML documents, a `DocumentType` object may be returned, independently of the presence or absence of document type declaration in the HTML document. 
This provides direct access to the `DocumentType` node, child node of this `Document`. This node can be set at document creation time and later changed through the use of child nodes manipulation methods, such as `Node.insertBefore`, or `Node.replaceChild`. Note, however, that while some implementations may instantiate different types of `Document` objects supporting additional features than the "Core", such as "HTML" \ [[DOM Level 2 HTML](http://www.w3.org/TR/2003/REC-DOM-Level-2-HTML-20030109)\] , based on the `DocumentType` specified at creation time, changing it afterwards is very unlikely to result in a change of the features supported. 

### getDocumentElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDocumentElement(): Element!
```

This is a convenience attribute that allows direct access to the child node that is the document element of the document. 

### getDocumentURI

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDocumentURI(): String!
```

The location of the document or `null` if undefined or if the `Document` was created using `DOMImplementation.createDocument`. No lexical checking is performed when setting this attribute; this could result in a `null` value returned when using `Node.baseURI` . 
Beware that when the `Document` supports the feature "HTML" \ [[DOM Level 2 HTML](http://www.w3.org/TR/2003/REC-DOM-Level-2-HTML-20030109)\] , the href attribute of the HTML BASE element takes precedence over this attribute when computing `Node.baseURI`. 

### getDomConfig

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDomConfig(): DOMConfiguration!
```

The configuration used when `Document.normalizeDocument()` is invoked. 

### getElementById

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getElementById(elementId: String!): Element!
```

Returns the `Element` that has an ID attribute with the given value. If no such element exists, this returns `null` . If more than one element has an ID attribute with that value, what is returned is undefined. 
The DOM implementation is expected to use the attribute `Attr.isId` to determine if an attribute is of type ID.

**Note:** Attributes with the name "ID" or "id" are not of type ID unless so defined.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| `elementId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The unique `id` value for an element. |

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------|
| [Element](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-element/index.html)! | The matching element or `null` if there is none. |

### getElementsByTagName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getElementsByTagName(tagname: String!): NodeList!
```

Returns a `NodeList` of all the `Elements` in document order with a given tag name and are contained in the document.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tagname` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the tag to match on. The special value "\*" matches all tags. For XML, the `tagname` parameter is case-sensitive, otherwise it depends on the case-sensitivity of the markup language in use. |

| Return ||
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [NodeList](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node-list/index.html)! | A new `NodeList` object containing all the matched `Elements`. |

### getElementsByTagNameNS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getElementsByTagNameNS(
    namespaceURI: String!, 
    localName: String!
): NodeList!
```

Returns a `NodeList` of all the `Elements` with a given local name and namespace URI in document order.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `namespaceURI` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The namespace URI of the elements to match on. The special value `"*"` matches all namespaces. |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The local name of the elements to match on. The special value "\*" matches all local names. |

| Return ||
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [NodeList](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node-list/index.html)! | A new `NodeList` object containing all the matched `Elements`. |

### getImplementation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getImplementation(): DOMImplementation!
```

The `DOMImplementation` object that handles this document. A DOM application may use objects from multiple implementations. 

### getInputEncoding

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getInputEncoding(): String!
```

An attribute specifying the encoding used for this document at the time of the parsing. This is `null` when it is not known, such as when the `Document` was created in memory. 

### getStrictErrorChecking

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getStrictErrorChecking(): Boolean
```

An attribute specifying whether error checking is enforced or not. When set to `false`, the implementation is free to not test every possible error case normally defined on DOM operations, and not raise any `DOMException` on DOM operations or report errors while using `Document.normalizeDocument()`. In case of error, the behavior is undefined. This attribute is `true` by default. 

### getXmlEncoding

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getXmlEncoding(): String!
```

An attribute specifying, as part of the [XML declaration](http://www.w3.org/TR/2004/REC-xml-20040204#NT-XMLDecl), the encoding of this document. This is `null` when unspecified or when it is not known, such as when the `Document` was created in memory. 

### getXmlStandalone

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getXmlStandalone(): Boolean
```

An attribute specifying, as part of the [XML declaration](http://www.w3.org/TR/2004/REC-xml-20040204#NT-XMLDecl), whether this document is standalone. This is `false` when unspecified.

**Note:** No verification is done on the value when setting this attribute. Applications should use `Document.normalizeDocument()` with the "validate" parameter to verify if the value matches the [validity constraint for standalone document declaration](http://www.w3.org/TR/2004/REC-xml-20040204#sec-rmd) as defined in \ [[XML 1.0](http://www.w3.org/TR/2004/REC-xml-20040204)\]. 

### getXmlVersion

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getXmlVersion(): String!
```

An attribute specifying, as part of the [XML declaration](http://www.w3.org/TR/2004/REC-xml-20040204#NT-XMLDecl), the version number of this document. If there is no declaration and if this document supports the "XML" feature, the value is `"1.0"`. If this document does not support the "XML" feature, the value is always `null`. Changing this attribute will affect methods that check for invalid characters in XML names. Application should invoke `Document.normalizeDocument()` in order to check for invalid characters in the `Node`s that are already part of this `Document`. 
DOM applications may use the `DOMImplementation.hasFeature(feature, version)` method with parameter values "XMLVersion" and "1.0" (respectively) to determine if an implementation supports \ [[XML 1.0](http://www.w3.org/TR/2004/REC-xml-20040204)\]. DOM applications may use the same method with parameter values "XMLVersion" and "1.1" (respectively) to determine if an implementation supports \ [[XML 1.1](http://www.w3.org/TR/2004/REC-xml11-20040204/)\]. In both cases, in order to support XML, an implementation must also support the "XML" feature defined in this specification. `Document` objects supporting a version of the "XMLVersion" feature must not raise a `NOT_SUPPORTED_ERR` exception for the same version number when using `Document.xmlVersion`. 

### importNode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun importNode(
    importedNode: Node!, 
    deep: Boolean
): Node!
```

Imports a node from another document to this document, without altering or removing the source node from the original document; this method creates a new copy of the source node. The returned node has no parent; (`parentNode` is `null`). 
For all nodes, importing a node creates a node object owned by the importing document, with attribute values identical to the source node's `nodeName` and `nodeType`, plus the attributes related to namespaces (`prefix`, `localName`, and `namespaceURI`). As in the `cloneNode` operation, the source node is not altered. User data associated to the imported node is not carried over. However, if any `UserDataHandlers` has been specified along with the associated data these handlers will be called with the appropriate parameters before this method returns. 
Additional information is copied as appropriate to the `nodeType`, attempting to mirror the behavior expected if a fragment of XML or HTML source was copied from one document to another, recognizing that the two documents may have different DTDs in the XML case. The following list describes the specifics for each type of node.

ATTRIBUTE_NODE
: The `ownerElement` attribute is set to `null` and the `specified` flag is set to `true` on the generated `Attr`. The descendants of the source `Attr` are recursively imported and the resulting nodes reassembled to form the corresponding subtree. Note that the `deep` parameter has no effect on `Attr` nodes; they always carry their children with them when imported.

DOCUMENT_FRAGMENT_NODE
: If the `deep` option was set to `true`, the descendants of the source `DocumentFragment` are recursively imported and the resulting nodes reassembled under the imported `DocumentFragment` to form the corresponding subtree. Otherwise, this simply generates an empty `DocumentFragment`.

DOCUMENT_NODE
: `Document` nodes cannot be imported.

DOCUMENT_TYPE_NODE
: `DocumentType` nodes cannot be imported.

ELEMENT_NODE
: *Specified* attribute nodes of the source element are imported, and the generated `Attr` nodes are attached to the generated `Element`. Default attributes are *not* copied, though if the document being imported into defines default attributes for this element name, those are assigned. If the `importNode` `deep` parameter was set to `true`, the descendants of the source element are recursively imported and the resulting nodes reassembled to form the corresponding subtree.

ENTITY_NODE
: `Entity` nodes can be imported, however in the current release of the DOM the `DocumentType` is readonly. Ability to add these imported nodes to a `DocumentType` will be considered for addition to a future release of the DOM.On import, the `publicId`, `systemId`, and `notationName` attributes are copied. If a `deep` import is requested, the descendants of the the source `Entity` are recursively imported and the resulting nodes reassembled to form the corresponding subtree.

ENTITY_REFERENCE_NODE
: Only the `EntityReference` itself is copied, even if a `deep` import is requested, since the source and destination documents might have defined the entity differently. If the document being imported into provides a definition for this entity name, its value is assigned.

NOTATION_NODE
: `Notation` nodes can be imported, however in the current release of the DOM the `DocumentType` is readonly. Ability to add these imported nodes to a `DocumentType` will be considered for addition to a future release of the DOM.On import, the `publicId` and `systemId` attributes are copied. Note that the `deep` parameter has no effect on this type of nodes since they cannot have any children.

PROCESSING_INSTRUCTION_NODE
: The imported node copies its `target` and `data` values from those of the source node.Note that the `deep` parameter has no effect on this type of nodes since they cannot have any children.

TEXT_NODE, CDATA_SECTION_NODE, COMMENT_NODE
: These three types of nodes inheriting from `CharacterData` copy their `data` and `length` attributes from those of the source node.Note that the `deep` parameter has no effect on these types of nodes since they cannot have any children.

<br />

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `importedNode` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!: The node to import. |
| `deep` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If `true`, recursively import the subtree under the specified node; if `false`, import only the node itself, as explained above. This has no effect on nodes that cannot have any children, and on `Attr`, and `EntityReference` nodes. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | The imported node that belongs to this `Document`. |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | NOT_SUPPORTED_ERR: Raised if the type of node being imported is not supported. INVALID_CHARACTER_ERR: Raised if one of the imported names is not an XML name according to the XML version in use specified in the `Document.xmlVersion` attribute. This may happen when importing an XML 1.1 \ [[XML 1.1](http://www.w3.org/TR/2004/REC-xml11-20040204/)\] element into an XML 1.0 document, for instance. |

### normalizeDocument

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun normalizeDocument(): Unit
```

This method acts as if the document was going through a save and load cycle, putting the document in a "normal" form. As a consequence, this method updates the replacement tree of `EntityReference` nodes and normalizes `Text` nodes, as defined in the method `Node.normalize()`. 
Otherwise, the actual result depends on the features being set on the `Document.domConfig` object and governing what operations actually take place. Noticeably this method could also make the document namespace well-formed according to the algorithm described in , check the character normalization, remove the `CDATASection` nodes, etc. See `DOMConfiguration` for details. 

```kotlin
// Keep in the document
  the information defined // in the XML Information Set (Java example)
  DOMConfiguration docConfig = myDocument.getDomConfig();
  docConfig.setParameter("infoset", Boolean.TRUE);
  myDocument.normalizeDocument();
```

Mutation events, when supported, are generated to reflect the changes occurring on the document. 
If errors occur during the invocation of this method, such as an attempt to update a read-only node or a `Node.nodeName` contains an invalid character according to the XML version in use, errors or warnings (`DOMError.SEVERITY_ERROR` or `DOMError.SEVERITY_WARNING`) will be reported using the `DOMErrorHandler` object associated with the "error-handler " parameter. Note this method might also report fatal errors ( `DOMError.SEVERITY_FATAL_ERROR`) if an implementation cannot recover from an error.

<br />

### renameNode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun renameNode(
    n: Node!, 
    namespaceURI: String!, 
    qualifiedName: String!
): Node!
```

Rename an existing node of type `ELEMENT_NODE` or `ATTRIBUTE_NODE`. 
When possible this simply changes the name of the given node, otherwise this creates a new node with the specified name and replaces the existing node with the new node as described below. 
If simply changing the name of the given node is not possible, the following operations are performed: a new node is created, any registered event listener is registered on the new node, any user data attached to the old node is removed from that node, the old node is removed from its parent if it has one, the children are moved to the new node, if the renamed node is an `Element` its attributes are moved to the new node, the new node is inserted at the position the old node used to have in its parent's child nodes list if it has one, the user data that was attached to the old node is attached to the new node. 
When the node being renamed is an `Element` only the specified attributes are moved, default attributes originated from the DTD are updated according to the new element name. In addition, the implementation may update default attributes from other schemas. Applications should use `Document.normalizeDocument()` to guarantee these attributes are up-to-date. 
When the node being renamed is an `Attr` that is attached to an `Element`, the node is first removed from the `Element` attributes map. Then, once renamed, either by modifying the existing node or creating a new one as described above, it is put back. 
In addition,

- a user data event `NODE_RENAMED` is fired,
- when the implementation supports the feature "MutationNameEvents", each mutation operation involved in this method fires the appropriate event, and in the end the event { `http://www.w3.org/2001/xml-events`, `DOMElementNameChanged`} or { `http://www.w3.org/2001/xml-events`, `DOMAttributeNameChanged`} is fired.

<br />

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------|
| `n` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!: The node to rename. |
| `namespaceURI` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The new namespace URI. |
| `qualifiedName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The new qualified name. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | The renamed node. This is either the specified node or the new node that was created to replace the specified node. |

| Exceptions ||
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | NOT_SUPPORTED_ERR: Raised when the type of the specified node is neither `ELEMENT_NODE` nor `ATTRIBUTE_NODE`, or if the implementation does not support the renaming of the document element. INVALID_CHARACTER_ERR: Raised if the new qualified name is not an XML name according to the XML version in use specified in the `Document.xmlVersion` attribute. WRONG_DOCUMENT_ERR: Raised when the specified node was created from a different document than this document. NAMESPACE_ERR: Raised if the `qualifiedName` is a malformed qualified name, if the `qualifiedName` has a prefix and the `namespaceURI` is `null`, or if the `qualifiedName` has a prefix that is "xml" and the `namespaceURI` is different from "<http://www.w3.org/XML/1998/namespace>" \ [[XML Namespaces](http://www.w3.org/TR/1999/REC-xml-names-19990114/)\] . Also raised, when the node being renamed is an attribute, if the `qualifiedName`, or its prefix, is "xmlns" and the `namespaceURI` is different from "<http://www.w3.org/2000/xmlns/>". |

### setDocumentURI

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setDocumentURI(documentURI: String!): Unit
```

The location of the document or `null` if undefined or if the `Document` was created using `DOMImplementation.createDocument`. No lexical checking is performed when setting this attribute; this could result in a `null` value returned when using `Node.baseURI` . 
Beware that when the `Document` supports the feature "HTML" \ [[DOM Level 2 HTML](http://www.w3.org/TR/2003/REC-DOM-Level-2-HTML-20030109)\] , the href attribute of the HTML BASE element takes precedence over this attribute when computing `Node.baseURI`. 

### setStrictErrorChecking

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setStrictErrorChecking(strictErrorChecking: Boolean): Unit
```

An attribute specifying whether error checking is enforced or not. When set to `false`, the implementation is free to not test every possible error case normally defined on DOM operations, and not raise any `DOMException` on DOM operations or report errors while using `Document.normalizeDocument()`. In case of error, the behavior is undefined. This attribute is `true` by default. 

### setXmlStandalone

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setXmlStandalone(xmlStandalone: Boolean): Unit
```

An attribute specifying, as part of the [XML declaration](http://www.w3.org/TR/2004/REC-xml-20040204#NT-XMLDecl), whether this document is standalone. This is `false` when unspecified.

**Note:** No verification is done on the value when setting this attribute. Applications should use `Document.normalizeDocument()` with the "validate" parameter to verify if the value matches the [validity constraint for standalone document declaration](http://www.w3.org/TR/2004/REC-xml-20040204#sec-rmd) as defined in \ [[XML 1.0](http://www.w3.org/TR/2004/REC-xml-20040204)\].

| Exceptions ||
|----------------------------|--------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | NOT_SUPPORTED_ERR: Raised if this document does not support the "XML" feature. |

### setXmlVersion

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setXmlVersion(xmlVersion: String!): Unit
```

An attribute specifying, as part of the [XML declaration](http://www.w3.org/TR/2004/REC-xml-20040204#NT-XMLDecl), the version number of this document. If there is no declaration and if this document supports the "XML" feature, the value is `"1.0"`. If this document does not support the "XML" feature, the value is always `null`. Changing this attribute will affect methods that check for invalid characters in XML names. Application should invoke `Document.normalizeDocument()` in order to check for invalid characters in the `Node`s that are already part of this `Document`. 
DOM applications may use the `DOMImplementation.hasFeature(feature, version)` method with parameter values "XMLVersion" and "1.0" (respectively) to determine if an implementation supports \ [[XML 1.0](http://www.w3.org/TR/2004/REC-xml-20040204)\]. DOM applications may use the same method with parameter values "XMLVersion" and "1.1" (respectively) to determine if an implementation supports \ [[XML 1.1](http://www.w3.org/TR/2004/REC-xml11-20040204/)\]. In both cases, in order to support XML, an implementation must also support the "XML" feature defined in this specification. `Document` objects supporting a version of the "XMLVersion" feature must not raise a `NOT_SUPPORTED_ERR` exception for the same version number when using `Document.xmlVersion`.

| Exceptions ||
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | NOT_SUPPORTED_ERR: Raised if the version is set to a value that is not supported by this `Document` or if this document does not support the "XML" feature. |
