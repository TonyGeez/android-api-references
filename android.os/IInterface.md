# IInterface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IInterface

Kotlin| [Java](IInterface.md) 
| --- | --- |

```
interface IInterface
```

| [android.os.IInterface](IInterface.md) |

Base class for Binder interfaces. When defining a new interface, you must derive it from IInterface.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [IBinder](IBinder.md)! | [asBinder](IInterface.md))`()` Retrieve the Binder object associated with this interface. |

## Public methods

### asBinder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun asBinder(): IBinder!
```

Retrieve the Binder object associated with this interface. You must use this instead of a plain cast, so that proxy objects can return the correct result.
