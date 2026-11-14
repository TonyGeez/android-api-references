# DOMResult

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DOMResult

```
open class DOMResult : Result
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [javax.xml.transform.dom.DOMResult](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#) |

Acts as a holder for a transformation result tree in the form of a Document Object Model (DOM) tree.

If no output DOM source is set, the transformation will create a Document node as the holder for the result of the transformation, which may be retrieved with [getNode()](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#getNode()).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#FEATURE:kotlin.String) If [javax.xml.transform.TransformerFactory#getFeature](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#getFeature(kotlin.String))returns`true`when passed this value as an argument, the`Transformer`supports`Result`output of this type. |

| Inherited constants ||
|---|---|
| From class [Result](https://developer.android.com/reference/kotlin/javax/xml/transform/Result.html#) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PI_DISABLE_OUTPUT_ESCAPING](https://developer.android.com/reference/kotlin/javax/xml/transform/Result.html#PI_DISABLE_OUTPUT_ESCAPING:kotlin.String) <br /> The name of the processing instruction that is sent if the result tree disables output escaping. Normally, result tree serialization escapes \& and \< (and possibly other characters) when outputting text nodes. This ensures that the output is well-formed XML. However, it is sometimes convenient to be able to produce output that is almost, but not quite well-formed XML; for example, the output may include ill-formed sections that will be transformed into well-formed XML by a subsequent non-XML aware process. If a processing instruction is sent with this name, serialization should be output without any escaping. Result DOM trees may also have PI_DISABLE_OUTPUT_ESCAPING and PI_ENABLE_OUTPUT_ESCAPING inserted into the tree. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PI_ENABLE_OUTPUT_ESCAPING](https://developer.android.com/reference/kotlin/javax/xml/transform/Result.html#PI_ENABLE_OUTPUT_ESCAPING:kotlin.String) <br /> The name of the processing instruction that is sent if the result tree enables output escaping at some point after having received a PI_DISABLE_OUTPUT_ESCAPING processing instruction. <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DOMResult](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#DOMResult())`()` Zero-argument default constructor. |
| [DOMResult](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#DOMResult(org.w3c.dom.Node))`(`node:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`)` Use a DOM node to create a new output target. |
| [DOMResult](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#DOMResult(org.w3c.dom.Node,%20kotlin.String))`(`node:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Use a DOM node to create a new output target with the specified System ID. |
| [DOMResult](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#DOMResult(org.w3c.dom.Node,%20org.w3c.dom.Node))`(`node:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`, `nextSibling:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`)` Use a DOM node to create a new output target specifying the child node where the result nodes should be inserted before. |
| [DOMResult](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#DOMResult(org.w3c.dom.Node,%20org.w3c.dom.Node,%20kotlin.String))`(`node:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`, `nextSibling:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`, `systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Use a DOM node to create a new output target specifying the child node where the result nodes should be inserted before and the specified System ID. |

| Public methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [getNextSibling](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#getNextSibling())`()` Get the child node before which the result nodes will be inserted. |
| open [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [getNode](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#getNode())`()` Get the node that will contain the result DOM tree. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSystemId](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#getSystemId())`()` Get the System Identifier. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNextSibling](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#setNextSibling(org.w3c.dom.Node))`(`nextSibling:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`)` Set the child node before which the result nodes will be inserted. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNode](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#setNode(org.w3c.dom.Node))`(`node:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`)` Set the node that will contain the result DOM tree. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSystemId](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#setSystemId(kotlin.String))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the systemId that may be used in association with the node. |

## Constants

### FEATURE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE: String
```

If [javax.xml.transform.TransformerFactory#getFeature](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#getFeature(kotlin.String))returns`true`when passed this value as an argument, the`Transformer`supports`Result`output of this type. 

 Value: "http://javax.xml.transform.dom.DOMResult/feature"

## Public constructors

### DOMResult

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DOMResult()
```

Zero-argument default constructor.

`node`,`siblingNode`and`systemId`will be set to`null`. 

### DOMResult

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DOMResult(node: Node!)
```

Use a DOM node to create a new output target.

In practice, the node should be a [org.w3c.dom.Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) node, a [org.w3c.dom.DocumentFragment](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document-fragment/index.html) node, or a [org.w3c.dom.Element](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-element/index.html) node. In other words, a node that accepts children.

`siblingNode`and`systemId`will be set to`null`.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------|
| `node` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!:The DOM node that will contain the result tree. |

### DOMResult

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DOMResult(
    node: Node!, 
    systemId: String!)
```

Use a DOM node to create a new output target with the specified System ID.

<br />

In practice, the node should be a [org.w3c.dom.Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) node, a [org.w3c.dom.DocumentFragment](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document-fragment/index.html) node, or a [org.w3c.dom.Element](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-element/index.html) node. In other words, a node that accepts children.

`siblingNode`will be set to`null`.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `node` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!:The DOM node that will contain the result tree. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The system identifier which may be used in association with this node. |

### DOMResult

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DOMResult(
    node: Node!, 
    nextSibling: Node!)
```

Use a DOM node to create a new output target specifying the child node where the result nodes should be inserted before.

In practice,`node`and`nextSibling`should be a [org.w3c.dom.Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) node, a [org.w3c.dom.DocumentFragment](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document-fragment/index.html) node, or a [org.w3c.dom.Element](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-element/index.html) node. In other words, a node that accepts children.

Use`nextSibling`to specify the child node where the result nodes should be inserted before. If`nextSibling`is not a sibling of`node`, then an`IllegalArgumentException`is thrown. If`node`is`null`and`nextSibling`is not`null`, then an`IllegalArgumentException`is thrown. If`nextSibling`is`null`, then the behavior is the same as calling [DOMResult(org.w3c.dom.Node)](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#DOMResult(org.w3c.dom.Node)), i.e. append the result nodes as the last child of the specified`node`.

`systemId`will be set to`null`.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `node` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!:The DOM node that will contain the result tree. |
| `nextSibling` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!:The child node where the result nodes should be inserted before. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------|
| `java.lang.IllegalArgumentException` | If`node`is`null`and`nextSibling`is not`null`. |

### DOMResult

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DOMResult(
    node: Node!, 
    nextSibling: Node!, 
    systemId: String!)
```

Use a DOM node to create a new output target specifying the child node where the result nodes should be inserted before and the specified System ID.

In practice,`node`and`nextSibling`should be a [org.w3c.dom.Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) node, a [org.w3c.dom.DocumentFragment](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document-fragment/index.html) node, or a [org.w3c.dom.Element](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-element/index.html) node. In other words, a node that accepts children.

Use`nextSibling`to specify the child node where the result nodes should be inserted before. If`nextSibling`is not a sibling of`node`, then an`IllegalArgumentException`is thrown. If`node`is`null`and`nextSibling`is not`null`, then an`IllegalArgumentException`is thrown. If`nextSibling`is`null`, then the behavior is the same as calling [DOMResult(org.w3c.dom.Node,java.lang.String)](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#DOMResult(org.w3c.dom.Node,%20kotlin.String)), i.e. append the result nodes as the last child of the specified node and use the specified System ID.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `node` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!:The DOM node that will contain the result tree. |
| `nextSibling` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!:The child node where the result nodes should be inserted before. |
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The system identifier which may be used in association with this node. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------|
| `java.lang.IllegalArgumentException` | If`node`is`null`and`nextSibling`is not`null`. |

## Public methods

### getNextSibling

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNextSibling(): Node!
```

Get the child node before which the result nodes will be inserted.

If no node was set via [DOMResult(org.w3c.dom.Node,org.w3c.dom.Node)](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#DOMResult(org.w3c.dom.Node,%20org.w3c.dom.Node)), [DOMResult(org.w3c.dom.Node,org.w3c.dom.Node,java.lang.String)](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#DOMResult(org.w3c.dom.Node,%20org.w3c.dom.Node,%20kotlin.String))or [setNextSibling(org.w3c.dom.Node)](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#setNextSibling(org.w3c.dom.Node)), then`null`will be returned.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | The child node before which the result nodes will be inserted. |

### getNode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNode(): Node!
```

Get the node that will contain the result DOM tree.

If no node was set via [DOMResult(org.w3c.dom.Node)](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#DOMResult(org.w3c.dom.Node)), [DOMResult(org.w3c.dom.Node,java.lang.String)](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#DOMResult(org.w3c.dom.Node,%20kotlin.String)), [DOMResult(org.w3c.dom.Node,org.w3c.dom.Node)](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#DOMResult(org.w3c.dom.Node,%20org.w3c.dom.Node)), [DOMResult(org.w3c.dom.Node,org.w3c.dom.Node,java.lang.String)](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#DOMResult(org.w3c.dom.Node,%20org.w3c.dom.Node,%20kotlin.String))or [setNode(org.w3c.dom.Node)](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#setNode(org.w3c.dom.Node)), then the node will be set by the transformation, and may be obtained from this method once the transformation is complete. Calling this method before the transformation will return`null`.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | The node to which the transformation will be appended. |

### getSystemId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSystemId(): String!
```

Get the System Identifier.

If no System ID was set via [DOMResult(org.w3c.dom.Node,java.lang.String)](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#DOMResult(org.w3c.dom.Node,%20kotlin.String)), [DOMResult(org.w3c.dom.Node,org.w3c.dom.Node,java.lang.String)](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#DOMResult(org.w3c.dom.Node,%20org.w3c.dom.Node,%20kotlin.String))or [setSystemId(java.lang.String)](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#setSystemId(kotlin.String)), then`null`will be returned.

| Return ||
|-----------------------------------------------------------------------------------|------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The system identifier. |

### setNextSibling

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNextSibling(nextSibling: Node!): Unit
```

Set the child node before which the result nodes will be inserted.

Use`nextSibling`to specify the child node before which the result nodes should be inserted. If`nextSibling`is not a descendant of`node`, then an`IllegalArgumentException`is thrown. If`node`is`null`and`nextSibling`is not`null`, then an`IllegalStateException`is thrown. If`nextSibling`is`null`, then the behavior is the same as calling [DOMResult(org.w3c.dom.Node)](https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMResult#DOMResult(org.w3c.dom.Node)), i.e. append the result nodes as the last child of the specified`node`.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `nextSibling` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!:The child node before which the result nodes will be inserted. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------|
| `java.lang.IllegalArgumentException` | If`nextSibling`is not a descendant of`node`. |
| `java.lang.IllegalStateException` | If`node`is`null`and`nextSibling`is not`null`. |

### setNode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNode(node: Node!): Unit
```

Set the node that will contain the result DOM tree.

<br />

In practice, the node should be a [org.w3c.dom.Document](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html) node, a [org.w3c.dom.DocumentFragment](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document-fragment/index.html) node, or a [org.w3c.dom.Element](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-element/index.html) node. In other words, a node that accepts children.

An`IllegalStateException`is thrown if`nextSibling`is not`null`and`node`is not a parent of`nextSibling`. An`IllegalStateException`is thrown if`node`is`null`and`nextSibling`is not`null`.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `node` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!:The node to which the transformation will be appended. |

| Exceptions ||
|-----------------------------------|-----------------------------------------------|
| `java.lang.IllegalStateException` | If`node`is`null`and`nextSibling`is not`null`. |

### setSystemId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSystemId(systemId: String!): Unit
```

Set the systemId that may be used in association with the node.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------|
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The system identifier as a URI string. |
