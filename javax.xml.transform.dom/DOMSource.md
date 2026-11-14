Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DOMSource

```
open class DOMSource : Source
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.transform.dom.DOMSource](DOMSource.md) |

Acts as a holder for a transformation Source tree in the form of a Document Object Model (DOM) tree.

Note that XSLT requires namespace support. Attempting to transform a DOM that was not contructed with a namespace-aware parser may result in errors. Parsers can be made namespace aware by calling `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilderFactory.html#setNamespaceAware(kotlin.Boolean)`.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMSource#FEATURE:kotlin.String` If `https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#getFeature(kotlin.String)` returns true when passed this value as an argument, the Transformer supports Source input of this type. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMSource#DOMSource()()` Zero-argument default constructor. |
| `https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMSource#DOMSource(org.w3c.dom.Node)(n: https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html!)` Create a new input source with a DOM node. |
| `https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMSource#DOMSource(org.w3c.dom.Node,%20kotlin.String)(node: https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html!, systemID: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Create a new input source with a DOM node, and with the system ID also passed in as the base URI. |

| Public methods ||
|---|---|
| open [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | `https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMSource#getNode()()` Get the node that represents a Source DOM tree. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMSource#getSystemId()()` Get the base ID (URL or system ID) from where URLs will be resolved. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMSource#setNode(org.w3c.dom.Node)(node: https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html!)` Set the node that will represents a Source DOM tree. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMSource#setSystemId(kotlin.String)(systemID: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Set the base ID (URL or system ID) from where URLs will be resolved. |

## Constants

### FEATURE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE: String
```

If `https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory.html#getFeature(kotlin.String)` returns true when passed this value as an argument, the Transformer supports Source input of this type.

 Value: "http://javax.xml.transform.dom.DOMSource/feature"

## Public constructors

### DOMSource

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DOMSource()
```

Zero-argument default constructor. If this constructor is used, and no DOM source is set using `https://developer.android.com/reference/kotlin/javax/xml/transform/dom/DOMSource#setNode(org.w3c.dom.Node)` , then the `Transformer` will create an empty source `https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-document/index.html` using `https://developer.android.com/reference/kotlin/javax/xml/parsers/DocumentBuilder.html#newDocument()`.
**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer.html#transform(javax.xml.transform.Source,%20javax.xml.transform.Result)`

### DOMSource

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DOMSource(n: Node!)
```

Create a new input source with a DOM node. The operation will be applied to the subtree rooted at this node. In XSLT, a "/" pattern still means the root of the tree (not the subtree), and the evaluation of global variables and parameters is done from the root node also.

| Parameters ||
|---|---|
| `n` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!: The DOM node that will contain the Source tree. |

### DOMSource

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DOMSource(
    node: Node!, 
    systemID: String!)
```

Create a new input source with a DOM node, and with the system ID also passed in as the base URI.

| Parameters ||
|---|---|
| `node` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!: The DOM node that will contain the Source tree. |
| `systemID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Specifies the base URI associated with node. |

## Public methods

### getNode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNode(): Node!
```

Get the node that represents a Source DOM tree.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html!` | The node that is to be transformed. |

### getSystemId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSystemId(): String!
```

Get the base ID (URL or system ID) from where URLs will be resolved.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | Base URL for this DOM tree. |

### setNode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNode(node: Node!): Unit
```

Set the node that will represents a Source DOM tree.

| Parameters ||
|---|---|
| `node` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!: The node that is to be transformed. |

### setSystemId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSystemId(systemID: String!): Unit
```

Set the base ID (URL or system ID) from where URLs will be resolved.

| Parameters ||
|---|---|
| `systemId` | The system identifier as a URL string. |
| `systemID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Base URL for this DOM tree. |
