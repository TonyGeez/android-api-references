# CustomPrinterIconCallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CustomPrinterIconCallback

Kotlin| [Java](https://developer.android.com/reference/android/printservice/CustomPrinterIconCallback "View this page in Java") 

```
class CustomPrinterIconCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.printservice.CustomPrinterIconCallback](https://developer.android.com/reference/kotlin/android/printservice/CustomPrinterIconCallback#) |

Callback for [PrinterDiscoverySession.onRequestCustomPrinterIcon](https://developer.android.com/reference/kotlin/android/printservice/PrinterDiscoverySession#onRequestCustomPrinterIcon(android.print.PrinterId,%20android.os.CancellationSignal,%20android.printservice.CustomPrinterIconCallback)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onCustomPrinterIconLoaded](https://developer.android.com/reference/kotlin/android/printservice/CustomPrinterIconCallback#onCustomPrinterIconLoaded(android.graphics.drawable.Icon))`(`icon:` ` [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#)?`)` Provide a new icon for a printer. |

## Public methods

### onCustomPrinterIconLoaded

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun onCustomPrinterIconLoaded(icon: Icon?): Boolean
```

Provide a new icon for a printer. Can be called more than once to update the icon.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `icon` | [Icon](https://developer.android.com/reference/kotlin/android/graphics/drawable/Icon.html#)?:The new icon for the printer or null to unset the current icon |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true iff the icon could be updated |
