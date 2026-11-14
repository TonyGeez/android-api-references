# FontsContract

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FontsContract

Kotlin| [Java](FontsContract.md) 
| --- | --- |

```
open class FontsContract
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.provider.FontsContract](FontsContract.md) |

| **This class was deprecated in API level 31.**
|
| Use the [Jetpack Core Library](https://developer.android.com/jetpack) androidx.core.provider.FontsContractCompat for consistent behavior across all devices.

Utility class to deal with Font ContentProviders.

## Summary

| Nested classes ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Columns](../android/provider/FontsContract.Columns.md) Defines the constants used in a response from a Font Provider. |
| open | [FontFamilyResult](../android/provider/FontsContract.FontFamilyResult.md) Object returned from [fetchFonts](FontsContract.md)). |
| open | [FontInfo](../android/provider/FontsContract.FontInfo.md) Object represent a font entry in the family returned from [fetchFonts](FontsContract.md)). |
| --- | --- |
| open | [FontRequestCallback](../android/provider/FontsContract.FontRequestCallback.md) Interface used to receive asynchronously fetched typefaces. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Typeface](../android.graphics/Typeface.md)! | [buildTypeface](FontsContract.md))`(`context:` ` [Context](../android.content/Context.md)`, `cancellationSignal:` ` [CancellationSignal](../android.os/CancellationSignal.md)?`, `fonts:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [FontsContract.FontInfo](../android/provider/FontsContract.FontInfo.md)!>`)` Build a Typeface from an array of [FontInfo](../android/provider/FontsContract.FontInfo.md) Results that are marked as not ready will be skipped. |
| openstatic [FontsContract.FontFamilyResult](../android/provider/FontsContract.FontFamilyResult.md) | [fetchFonts](FontsContract.md))`(`context:` ` [Context](../android.content/Context.md)`, `cancellationSignal:` ` [CancellationSignal](../android.os/CancellationSignal.md)?`, `request:` ` [FontRequest](FontRequest.md)`)` Fetch fonts given a font request. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestFonts](FontsContract.md))`(`context:` ` [Context](../android.content/Context.md)`, `request:` ` [FontRequest](FontRequest.md)`, `handler:` ` [Handler](../android.os/Handler.md)`, `cancellationSignal:` ` [CancellationSignal](../android.os/CancellationSignal.md)?`, `callback:` ` [FontsContract.FontRequestCallback](../android/provider/FontsContract.FontRequestCallback.md)`)` Create a typeface object given a font request. |
| --- | --- |

## Public methods

### buildTypeface

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun buildTypeface(
    context: Context, 
    cancellationSignal: CancellationSignal?, 
    fonts: Array<FontsContract.FontInfo!>
): Typeface!
```

**Deprecated:** *Deprecated in Java.*

Build a Typeface from an array of [FontInfo](../android/provider/FontsContract.FontInfo.md) Results that are marked as not ready will be skipped.

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md):A [Context](../android.content/Context.md) that will be used to fetch the font contents. This value cannot be`null`. |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)?:A signal to cancel the operation in progress, or null if none. If the operation is canceled, then will be thrown. |
| `fonts` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [FontsContract.FontInfo](../android/provider/FontsContract.FontInfo.md)!\>:An array of [FontInfo](../android/provider/FontsContract.FontInfo.md) to be used to create a Typeface. This value cannot be`null`. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Typeface](../android.graphics/Typeface.md)! | A Typeface object. Returns null if typeface creation fails. |

### fetchFonts

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun fetchFonts(
    context: Context, 
    cancellationSignal: CancellationSignal?, 
    request: FontRequest
): FontsContract.FontFamilyResult
```

**Deprecated:** *Deprecated in Java.*

Fetch fonts given a font request.

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md):A [Context](../android.content/Context.md) to be used for fetching fonts. This value cannot be`null`. |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)?:A signal to cancel the operation in progress, or null if none. If the operation is canceled, then will be thrown when the query is executed. |
| `request` | [FontRequest](FontRequest.md):A [FontRequest](FontRequest.md) object that identifies the provider and query for the request. This value cannot be`null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [FontsContract.FontFamilyResult](../android/provider/FontsContract.FontFamilyResult.md) | [FontFamilyResult](../android/provider/FontsContract.FontFamilyResult.md) This value cannot be`null`. |

| Exceptions ||
|-----------------------------------------------------------|------------------------------------------------------------|
| `android.content.pm.PackageManager.NameNotFoundException` | If requested package or authority was not found in system. |

### requestFonts

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun requestFonts(
    context: Context, 
    request: FontRequest, 
    handler: Handler, 
    cancellationSignal: CancellationSignal?, 
    callback: FontsContract.FontRequestCallback
): Unit
```

**Deprecated:** *Deprecated in Java.*

Create a typeface object given a font request. The font will be asynchronously fetched, therefore the result is delivered to the given callback. See [FontRequest](FontRequest.md). Only one of the methods in callback will be invoked, depending on whether the request succeeds or fails. These calls will happen on the caller thread. Note that the result Typeface may be cached internally and the same instance will be returned the next time you call this method with the same request. If you want to bypass this cache, use [fetchFonts](FontsContract.md))and [buildTypeface](FontsContract.md))instead.

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md):A context to be used for fetching from font provider. This value cannot be`null`. |
| `request` | [FontRequest](FontRequest.md):A [FontRequest](FontRequest.md) object that identifies the provider and query for the request. May not be null. |
| `handler` | [Handler](../android.os/Handler.md):A handler to be processed the font fetching. This value cannot be`null`. |
| --- | --- |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)?:A signal to cancel the operation in progress, or null if none. If the operation is canceled, then will be thrown. |
| `callback` | [FontsContract.FontRequestCallback](../android/provider/FontsContract.FontRequestCallback.md):A callback that will be triggered when results are obtained. May not be null. |
