# UserDataHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UserDataHandler

```
interface UserDataHandler
```

| [org.w3c.dom.UserDataHandler](https://developer.android.com/reference/kotlin/org/w3c/dom/UserDataHandler#) |

When associating an object to a key on a node using`Node.setUserData()`the application can provide a handler that gets called when the node the object is associated to is being cloned, imported, or renamed. This can be used by the application to implement various behaviors regarding the data it associates to the DOM nodes. This interface defines that handler.

See also the [Document Object Model (DOM) Level 3 Core Specification](http://www.w3.org/TR/2004/REC-DOM-Level-3-Core-20040407).

## Summary

| Constants ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [NODE_ADOPTED](https://developer.android.com/reference/kotlin/org/w3c/dom/UserDataHandler#NODE_ADOPTED:kotlin.Short) The node is adopted, using`Document.adoptNode()`. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [NODE_CLONED](https://developer.android.com/reference/kotlin/org/w3c/dom/UserDataHandler#NODE_CLONED:kotlin.Short) The node is cloned, using`Node.cloneNode()`. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [NODE_DELETED](https://developer.android.com/reference/kotlin/org/w3c/dom/UserDataHandler#NODE_DELETED:kotlin.Short) The node is deleted. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [NODE_IMPORTED](https://developer.android.com/reference/kotlin/org/w3c/dom/UserDataHandler#NODE_IMPORTED:kotlin.Short) The node is imported, using`Document.importNode()`. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [NODE_RENAMED](https://developer.android.com/reference/kotlin/org/w3c/dom/UserDataHandler#NODE_RENAMED:kotlin.Short) The node is renamed, using`Document.renameNode()`. |

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [handle](https://developer.android.com/reference/kotlin/org/w3c/dom/UserDataHandler#handle(kotlin.Short,%20kotlin.String,%20kotlin.Any,%20org.w3c.dom.Node,%20org.w3c.dom.Node))`(`operation:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`, `key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `data:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `src:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`, `dst:` ` [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!`)` This method is called whenever the node for which this handler is registered is imported or cloned. |

## Constants

### NODE_ADOPTED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NODE_ADOPTED: Short
```

The node is adopted, using`Document.adoptNode()`. 

 Value: 5

### NODE_CLONED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NODE_CLONED: Short
```

The node is cloned, using`Node.cloneNode()`. 

 Value: 1

### NODE_DELETED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NODE_DELETED: Short
```

The node is deleted.

**Note:**This may not be supported or may not be reliable in certain environments, such as Java, where the implementation has no real control over when objects are actually deleted. 

 Value: 3

### NODE_IMPORTED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NODE_IMPORTED: Short
```

The node is imported, using`Document.importNode()`. 

 Value: 2

### NODE_RENAMED

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NODE_RENAMED: Short
```

The node is renamed, using`Document.renameNode()`. 

 Value: 4

## Public methods

### handle

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun handle(
    operation: Short, 
    key: String!, 
    data: Any!, 
    src: Node!, 
    dst: Node!
): Unit
```

This method is called whenever the node for which this handler is registered is imported or cloned. 
DOM applications must not raise exceptions in a`UserDataHandler`. The effect of throwing exceptions from the handler is DOM implementation dependent.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `operation` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):Specifies the type of operation that is being performed on the node. |
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Specifies the key for which this handler is being called. |
| `data` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:Specifies the data for which this handler is being called. |
| `src` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!:Specifies the node being cloned, adopted, imported, or renamed. This is`null`when the node is being deleted. |
| `dst` | [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)!:Specifies the node newly created if any, or`null`. |
