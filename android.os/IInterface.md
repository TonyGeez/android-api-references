# IInterface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IInterface

Kotlin| [Java](https://developer.android.com/reference/android/os/IInterface "View this page in Java") 
| --- | --- |

```
interface IInterface
```

| [android.os.IInterface](https://developer.android.com/reference/kotlin/android/os/IInterface#) |

Base class for Binder interfaces. When defining a new interface, you must derive it from IInterface.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder)! | [asBinder](https://developer.android.com/reference/kotlin/android/os/IInterface#asBinder())`()` Retrieve the Binder object associated with this interface. |

## Public methods

### asBinder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun asBinder(): IBinder!
```

Retrieve the Binder object associated with this interface. You must use this instead of a plain cast, so that proxy objects can return the correct result.
