# CustomPrinterIconCallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CustomPrinterIconCallback

Kotlin| [Java](../android/printservice/CustomPrinterIconCallback.md) 
| --- | --- |

```
class CustomPrinterIconCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.printservice.CustomPrinterIconCallback](../android/printservice/CustomPrinterIconCallback.md) |

Callback for [PrinterDiscoverySession.onRequestCustomPrinterIcon](../android/printservice/PrinterDiscoverySession.md)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onCustomPrinterIconLoaded](../android/printservice/CustomPrinterIconCallback.md))`(`icon:` ` [Icon](../android/graphics/drawable/Icon.md)?`)` Provide a new icon for a printer. |

## Public methods

### onCustomPrinterIconLoaded

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun onCustomPrinterIconLoaded(icon: Icon?): Boolean
```

Provide a new icon for a printer. Can be called more than once to update the icon.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `icon` | [Icon](../android/graphics/drawable/Icon.md)?:The new icon for the printer or null to unset the current icon |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true iff the icon could be updated |
