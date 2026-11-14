# LSParserFilter

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LSParserFilter

```
interface LSParserFilter
```

| [org.w3c.dom.ls.LSParserFilter](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSParserFilter#) |

`LSParserFilter`s provide applications the ability to examine nodes as they are being constructed while parsing. As each node is examined, it may be modified or removed, or the entire parse may be terminated early.

At the time any of the filter methods are called by the parser, the owner Document and DOMImplementation objects exist and are accessible. The document element is never passed to the`LSParserFilter`methods, i.e. it is not possible to filter out the document element.`Document`,`DocumentType`,`Notation`,`Entity`, and`Attr`nodes are never passed to the`acceptNode`method on the filter. The child nodes of an`EntityReference`node are passed to the filter if the parameter " [entities](http://www.w3.org/TR/DOM-Level-3-Core/core.html#parameter-entities)" is set to`false`. Note that, as described by the parameter " [entities](http://www.w3.org/TR/DOM-Level-3-Core/core.html#parameter-entities)", unexpanded entity reference nodes are never discarded and are always passed to the filter.

All validity checking while parsing a document occurs on the source document as it appears on the input stream, not on the DOM document as it is built in memory. With filters, the document in memory may be a subset of the document on the stream, and its validity may have been affected by the filtering.

All default attributes must be present on elements when the elements are passed to the filter methods. All other default content must be passed to the filter methods.

DOM applications must not raise exceptions in a filter. The effect of throwing exceptions from a filter is DOM implementation dependent.

See also the [Document Object Model (DOM) Level 3 Load and Save Specification](http://www.w3.org/TR/2004/REC-DOM-Level-3-LS-20040407).

## Summary

| Constants ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [FILTER_ACCEPT](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSParserFilter#FILTER_ACCEPT:kotlin.Short) Accept the node. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [FILTER_INTERRUPT](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSParserFilter#FILTER_INTERRUPT:kotlin.Short) Interrupt the normal processing of the document. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [FILTER_REJECT](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSParserFilter#FILTER_REJECT:kotlin.Short) Reject the node and its children. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [FILTER_SKIP](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSParserFilter#FILTER_SKIP:kotlin.Short) Skip this single node. |

| Public methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [acceptNode](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSParserFilter#acceptNode(org.w3c.dom.Node))`(`nodeArg:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`)` This method will be called by the parser at the completion of the parsing of each node. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWhatToShow](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSParserFilter#getWhatToShow())`()` Tells the`LSParser`what types of nodes to show to the method`LSParserFilter.acceptNode`. |
| abstract [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [startElement](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSParserFilter#startElement(org.w3c.dom.Element))`(`elementArg:` ` [Element](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-element/index.html)!`)` The parser will call this method after each`Element`start tag has been scanned, but before the remainder of the`Element`is processed. |

## Constants

### FILTER_ACCEPT

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FILTER_ACCEPT: Short
```

Accept the node. 

 Value: 1

### FILTER_INTERRUPT

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FILTER_INTERRUPT: Short
```

Interrupt the normal processing of the document. 

 Value: 4

### FILTER_REJECT

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FILTER_REJECT: Short
```

Reject the node and its children. 

 Value: 2

### FILTER_SKIP

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FILTER_SKIP: Short
```

Skip this single node. The children of this node will still be considered. 

 Value: 3

## Public methods

### acceptNode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun acceptNode(nodeArg: Node!): Short
```

This method will be called by the parser at the completion of the parsing of each node. The node and all of its descendants will exist and be complete. The parent node will also exist, although it may be incomplete, i.e. it may have additional children that have not yet been parsed. Attribute nodes are never passed to this function. 
From within this method, the new node may be freely modified - children may be added or removed, text nodes modified, etc. The state of the rest of the document outside this node is not defined, and the affect of any attempt to navigate to, or to modify any other part of the document is undefined. 
For validating parsers, the checks are made on the original document, before any modification by the filter. No validity checks are made on any document modifications made by the filter. 
If this new node is rejected, the parser might reuse the new node and any of its descendants.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `nodeArg` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!:The newly constructed element. At the time this method is called, the element is complete - it has all of its children (and their children, recursively) and attributes, and is attached as a child to its parent. |

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | - `FILTER_ACCEPT`if this`Node`should be included in the DOM document being built. - `FILTER_REJECT`if the`Node`and all of its children should be rejected. - `FILTER_SKIP`if the`Node`should be skipped and the`Node`should be replaced by all the children of the`Node`. - `FILTER_INTERRUPT`if the filter wants to stop the processing of the document. Interrupting the processing of the document does no longer guarantee that the resulting DOM tree is XML well-formed. The`Node`is accepted and will be the last completely parsed node. |

### getWhatToShow

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getWhatToShow(): Int
```

Tells the`LSParser`what types of nodes to show to the method`LSParserFilter.acceptNode`. If a node is not shown to the filter using this attribute, it is automatically included in the DOM document being built. See`NodeFilter`for definition of the constants. The constants`SHOW_ATTRIBUTE`,`SHOW_DOCUMENT`,`SHOW_DOCUMENT_TYPE`,`SHOW_NOTATION`,`SHOW_ENTITY`, and`SHOW_DOCUMENT_FRAGMENT`are meaningless here. Those nodes will never be passed to`LSParserFilter.acceptNode`. 
The constants used here are defined in \ [[DOM Level 2 Traversal and Range](http://www.w3.org/TR/2000/REC-DOM-Level-2-Traversal-Range-20001113)\] . 

### startElement

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun startElement(elementArg: Element!): Short
```

The parser will call this method after each`Element`start tag has been scanned, but before the remainder of the`Element`is processed. The intent is to allow the element, including any children, to be efficiently skipped. Note that only element nodes are passed to the`startElement`function. 
The element node passed to`startElement`for filtering will include all of the Element's attributes, but none of the children nodes. The Element may not yet be in place in the document being constructed (it may not have a parent node.) 
A`startElement`filter function may access or change the attributes for the Element. Changing Namespace declarations will have no effect on namespace resolution by the parser. 
For efficiency, the Element node passed to the filter may not be the same one as is actually placed in the tree if the node is accepted. And the actual node (node object identity) may be reused during the process of reading in and filtering a document.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `elementArg` | [Element](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-element/index.html)!:The newly encountered element. At the time this method is called, the element is incomplete - it will have its attributes, but no children. |

| Return ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | - `FILTER_ACCEPT`if the`Element`should be included in the DOM document being built. - `FILTER_REJECT`if the`Element`and all of its children should be rejected. - `FILTER_SKIP`if the`Element`should be skipped. All of its children are inserted in place of the skipped`Element`node. - `FILTER_INTERRUPT`if the filter wants to stop the processing of the document. Interrupting the processing of the document does no longer guarantee that the resulting DOM tree is XML well-formed. The`Element`is rejected. Returning any other values will result in unspecified behavior. |
