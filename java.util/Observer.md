# Observer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Observer

```
interface Observer
```

| [java.util.Observer](https://developer.android.com/reference/kotlin/java/util/Observer#) |

| **This interface was deprecated in API level 33.**
|
| This interface has been deprecated. See the [Observable](https://developer.android.com/reference/kotlin/java/util/Observable) class for further information.

A class can implement the`Observer`interface when it wants to be informed of changes in observable objects.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](https://developer.android.com/reference/kotlin/java/util/Observer#update(java.util.Observable,%20kotlin.Any))`(`o:` ` [Observable](https://developer.android.com/reference/kotlin/java/util/Observable)!`, `arg:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` This method is called whenever the observed object is changed. |

## Public methods

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun update(
    o: Observable!, 
    arg: Any!
): Unit
```

**Deprecated:** *Deprecated in Java.*

This method is called whenever the observed object is changed. An application calls an`Observable`object's`notifyObservers`method to have all the object's observers notified of the change.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------|
| `o` | [Observable](https://developer.android.com/reference/kotlin/java/util/Observable)!:the observable object. |
| `arg` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:an argument passed to the`notifyObservers`method. |
