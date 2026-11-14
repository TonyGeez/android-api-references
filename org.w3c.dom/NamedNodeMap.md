# NamedNodeMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NamedNodeMap

```
interface NamedNodeMap
```

| [org.w3c.dom.NamedNodeMap](NamedNodeMap.md) |

Objects implementing the `NamedNodeMap` interface are used to represent collections of nodes that can be accessed by name. Note that `NamedNodeMap` does not inherit from `NodeList`; `NamedNodeMaps` are not maintained in any particular order. Objects contained in an object implementing `NamedNodeMap` may also be accessed by an ordinal index, but this is simply to allow convenient enumeration of the contents of a `NamedNodeMap`, and does not imply that the DOM specifies an order to these Nodes.

`NamedNodeMap` objects in the DOM are live.

See also the [Document Object Model (DOM) Level 3 Core Specification](http://www.w3.org/TR/2004/REC-DOM-Level-3-Core-20040407).

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLength](NamedNodeMap.md))`()` The number of nodes in this map. |
| abstract [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [getNamedItem](NamedNodeMap.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves a node specified by name. |
| abstract [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [getNamedItemNS](NamedNodeMap.md))`(`namespaceURI:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves a node specified by local name and namespace URI. |
| --- | --- |
| abstract [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [item](NamedNodeMap.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the `index`th item in the map. |
| abstract [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [removeNamedItem](NamedNodeMap.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Removes a node specified by name. |
| abstract [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [removeNamedItemNS](NamedNodeMap.md))`(`namespaceURI:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `localName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Removes a node specified by local name and namespace URI. |
| --- | --- |
| abstract [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [setNamedItem](NamedNodeMap.md))`(`arg:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`)` Adds a node using its `nodeName` attribute. |
| abstract [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [setNamedItemNS](NamedNodeMap.md))`(`arg:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`)` Adds a node using its `namespaceURI` and `localName`. |

## Public methods

### getLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLength(): Int
```

The number of nodes in this map. The range of valid child node indices is `0` to `length-1` inclusive. 

### getNamedItem

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNamedItem(name: String!): Node!
```

Retrieves a node specified by name.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The `nodeName` of a node to retrieve. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | A `Node` (of any type) with the specified `nodeName`, or `null` if it does not identify any node in this map. |

### getNamedItemNS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNamedItemNS(
    namespaceURI: String!, 
    localName: String!
): Node!
```

Retrieves a node specified by local name and namespace URI. 
Per \ [[XML Namespaces](http://www.w3.org/TR/1999/REC-xml-names-19990114/)\] , applications must use the value null as the namespaceURI parameter for methods if they wish to have no namespace.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------|
| `namespaceURI` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The namespace URI of the node to retrieve. |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The local name of the node to retrieve. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | A `Node` (of any type) with the specified local name and namespace URI, or `null` if they do not identify any node in this map. |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | NOT_SUPPORTED_ERR: May be raised if the implementation does not support the feature "XML" and the language exposed through the Document does not support XML Namespaces (such as \ [[HTML 4.01](http://www.w3.org/TR/1999/REC-html401-19991224/)\]). |

### item

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun item(index: Int): Node!
```

Returns the `index`th item in the map. If `index` is greater than or equal to the number of nodes in this map, this returns `null`.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Index into this map. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | The node at the `index`th position in the map, or `null` if that is not a valid index. |

### removeNamedItem

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeNamedItem(name: String!): Node!
```

Removes a node specified by name. When this map contains the attributes attached to an element, if the removed attribute is known to have a default value, an attribute immediately appears containing the default value as well as the corresponding namespace URI, local name, and prefix when applicable.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The `nodeName` of the node to remove. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | The node removed from this map if a node with such a name exists. |

| Exceptions ||
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | NOT_FOUND_ERR: Raised if there is no node named `name` in this map. NO_MODIFICATION_ALLOWED_ERR: Raised if this map is readonly. |

### removeNamedItemNS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeNamedItemNS(
    namespaceURI: String!, 
    localName: String!
): Node!
```

Removes a node specified by local name and namespace URI. A removed attribute may be known to have a default value when this map contains the attributes attached to an element, as returned by the attributes attribute of the `Node` interface. If so, an attribute immediately appears containing the default value as well as the corresponding namespace URI, local name, and prefix when applicable. 
Per \ [[XML Namespaces](http://www.w3.org/TR/1999/REC-xml-names-19990114/)\] , applications must use the value null as the namespaceURI parameter for methods if they wish to have no namespace.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| `namespaceURI` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The namespace URI of the node to remove. |
| `localName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The local name of the node to remove. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | The node removed from this map if a node with such a local name and namespace URI exists. |

| Exceptions ||
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | NOT_FOUND_ERR: Raised if there is no node with the specified `namespaceURI` and `localName` in this map. NO_MODIFICATION_ALLOWED_ERR: Raised if this map is readonly. NOT_SUPPORTED_ERR: May be raised if the implementation does not support the feature "XML" and the language exposed through the Document does not support XML Namespaces (such as \ [[HTML 4.01](http://www.w3.org/TR/1999/REC-html401-19991224/)\]). |

### setNamedItem

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNamedItem(arg: Node!): Node!
```

Adds a node using its `nodeName` attribute. If a node with that name is already present in this map, it is replaced by the new one. Replacing a node by itself has no effect. 
As the `nodeName` attribute is used to derive the name which the node must be stored under, multiple nodes of certain types (those that have a "special" string value) cannot be stored as the names would clash. This is seen as preferable to allowing nodes to be aliased.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `arg` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!: A node to store in this map. The node will later be accessible using the value of its `nodeName` attribute. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | If the new `Node` replaces an existing node the replaced `Node` is returned, otherwise `null` is returned. |

| Exceptions ||
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | WRONG_DOCUMENT_ERR: Raised if `arg` was created from a different document than the one that created this map. NO_MODIFICATION_ALLOWED_ERR: Raised if this map is readonly. INUSE_ATTRIBUTE_ERR: Raised if `arg` is an `Attr` that is already an attribute of another `Element` object. The DOM user must explicitly clone `Attr` nodes to re-use them in other elements. HIERARCHY_REQUEST_ERR: Raised if an attempt is made to add a node doesn't belong in this NamedNodeMap. Examples would include trying to insert something other than an Attr node into an Element's map of attributes, or a non-Entity node into the DocumentType's map of Entities. |

### setNamedItemNS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNamedItemNS(arg: Node!): Node!
```

Adds a node using its `namespaceURI` and `localName`. If a node with that namespace URI and that local name is already present in this map, it is replaced by the new one. Replacing a node by itself has no effect. 
Per \ [[XML Namespaces](http://www.w3.org/TR/1999/REC-xml-names-19990114/)\] , applications must use the value null as the namespaceURI parameter for methods if they wish to have no namespace.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `arg` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!: A node to store in this map. The node will later be accessible using the value of its `namespaceURI` and `localName` attributes. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | If the new `Node` replaces an existing node the replaced `Node` is returned, otherwise `null` is returned. |

| Exceptions ||
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `org.w3c.dom.DOMException` | WRONG_DOCUMENT_ERR: Raised if `arg` was created from a different document than the one that created this map. NO_MODIFICATION_ALLOWED_ERR: Raised if this map is readonly. INUSE_ATTRIBUTE_ERR: Raised if `arg` is an `Attr` that is already an attribute of another `Element` object. The DOM user must explicitly clone `Attr` nodes to re-use them in other elements. HIERARCHY_REQUEST_ERR: Raised if an attempt is made to add a node doesn't belong in this NamedNodeMap. Examples would include trying to insert something other than an Attr node into an Element's map of attributes, or a non-Entity node into the DocumentType's map of Entities. NOT_SUPPORTED_ERR: May be raised if the implementation does not support the feature "XML" and the language exposed through the Document does not support XML Namespaces (such as \ [[HTML 4.01](http://www.w3.org/TR/1999/REC-html401-19991224/)\]). |
