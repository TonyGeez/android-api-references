Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CalledFromWrongThreadListener

```
interface CalledFromWrongThreadListener
```

| [android.view.View.CalledFromWrongThreadListener](https://developer.android.com/reference/kotlin/android/view/View.CalledFromWrongThreadListener#) |

A listener that is notified when certain View APIs are called from the wrong thread.

Example use case:

```kotlin
<code>
  View.registerCalledFromWrongThreadListener(() -&gt; {
      // Handle the issue, e.g. crash if this is a dev build, or log an event
      // Unregister the listener to avoid being notified again of possibly the same problem
      View.unregisterCalledFromWrongThreadListener(this);
  });
  </code>
```

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/View.CalledFromWrongThreadListener#onCalledFromWrongThread()()` Called when a View API is called from the wrong thread. |

## Public methods

### onCalledFromWrongThread

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onCalledFromWrongThread(): Unit
```

Called when a View API is called from the wrong thread.
