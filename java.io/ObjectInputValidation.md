# ObjectInputValidation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ObjectInputValidation

```
interface ObjectInputValidation
```

| [java.io.ObjectInputValidation](ObjectInputValidation.md) |

Callback interface to allow validation of objects within a graph. Allows an object to be called when a complete graph of objects has been deserialized.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [validateObject](ObjectInputValidation.md))`()` Validates the object. |

## Public methods

### validateObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun validateObject(): Unit
```

Validates the object.

| Exceptions ||
|----------------------------------|---------------------------------------|
| `java.io.InvalidObjectException` | If the object cannot validate itself. |
