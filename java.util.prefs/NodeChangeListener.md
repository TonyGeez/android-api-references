# NodeChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NodeChangeListener

```
interface NodeChangeListener : EventListener
```

| [java.util.prefs.NodeChangeListener](../java/util/prefs/NodeChangeListener.md) |

A listener for receiving preference node change events.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [childAdded](../java/util/prefs/NodeChangeListener.md))`(`evt:` ` [NodeChangeEvent](../java/util/prefs/NodeChangeEvent.md)!`)` This method gets called when a child node is added. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [childRemoved](../java/util/prefs/NodeChangeListener.md))`(`evt:` ` [NodeChangeEvent](../java/util/prefs/NodeChangeEvent.md)!`)` This method gets called when a child node is removed. |

## Public methods

### childAdded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun childAdded(evt: NodeChangeEvent!): Unit
```

This method gets called when a child node is added.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `evt` | [NodeChangeEvent](../java/util/prefs/NodeChangeEvent.md)!:A node change event object describing the parent and child node. |

### childRemoved

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun childRemoved(evt: NodeChangeEvent!): Unit
```

This method gets called when a child node is removed.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `evt` | [NodeChangeEvent](../java/util/prefs/NodeChangeEvent.md)!:A node change event object describing the parent and child node. |
