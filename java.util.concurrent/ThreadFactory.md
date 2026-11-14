# ThreadFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ThreadFactory

```
interface ThreadFactory
```

| [java.util.concurrent.ThreadFactory](ThreadFactory.md) |

An object that creates new threads on demand. Using thread factories removes hardwiring of calls to [new Thread](../java.lang/Thread.md)), enabling applications to use special thread subclasses, priorities, etc.

The simplest implementation of this interface is just: 

```kotlin
<code>class SimpleThreadFactory implements ThreadFactory {
    public Thread newThread(Runnable r) {
      return new Thread(r);
    }
  }</code>
```
The [Executors.defaultThreadFactory](Executors.md))method provides a more useful simple implementation, that sets the created thread context to known values before returning it.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Thread](../java.lang/Thread.md)! | [newThread](ThreadFactory.md))`(`r:` ` [Runnable](../java.lang/Runnable.md)!`)` Constructs a new unstarted`Thread`to run the given runnable. |

## Public methods

### newThread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newThread(r: Runnable!): Thread!
```

Constructs a new unstarted`Thread`to run the given runnable.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [Runnable](../java.lang/Runnable.md)!:a runnable to be executed by new thread instance |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Thread](../java.lang/Thread.md)! | constructed thread, or`null`if the request to create a thread is rejected |

**See Also**
