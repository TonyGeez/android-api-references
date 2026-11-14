# NodeChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NodeChangeListener

```
interface NodeChangeListener : EventListener
```

| [java.util.prefs.NodeChangeListener](https://developer.android.com/reference/kotlin/java/util/prefs/NodeChangeListener#) |

A listener for receiving preference node change events.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [childAdded](https://developer.android.com/reference/kotlin/java/util/prefs/NodeChangeListener#childAdded(java.util.prefs.NodeChangeEvent))`(`evt:` ` [NodeChangeEvent](https://developer.android.com/reference/kotlin/java/util/prefs/NodeChangeEvent)!`)` This method gets called when a child node is added. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [childRemoved](https://developer.android.com/reference/kotlin/java/util/prefs/NodeChangeListener#childRemoved(java.util.prefs.NodeChangeEvent))`(`evt:` ` [NodeChangeEvent](https://developer.android.com/reference/kotlin/java/util/prefs/NodeChangeEvent)!`)` This method gets called when a child node is removed. |

## Public methods

### childAdded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun childAdded(evt: NodeChangeEvent!): Unit
```

This method gets called when a child node is added.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `evt` | [NodeChangeEvent](https://developer.android.com/reference/kotlin/java/util/prefs/NodeChangeEvent)!:A node change event object describing the parent and child node. |

### childRemoved

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun childRemoved(evt: NodeChangeEvent!): Unit
```

This method gets called when a child node is removed.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `evt` | [NodeChangeEvent](https://developer.android.com/reference/kotlin/java/util/prefs/NodeChangeEvent)!:A node change event object describing the parent and child node. |
