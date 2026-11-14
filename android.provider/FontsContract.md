# FontsContract

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FontsContract

Kotlin| [Java](https://developer.android.com/reference/android/provider/FontsContract "View this page in Java") 
| --- | --- |

```
open class FontsContract
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.provider.FontsContract](https://developer.android.com/reference/kotlin/android/provider/FontsContract#) |

| **This class was deprecated in API level 31.**
|
| Use the [Jetpack Core Library](https://developer.android.com/jetpack) androidx.core.provider.FontsContractCompat for consistent behavior across all devices.

Utility class to deal with Font ContentProviders.

## Summary

| Nested classes ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Columns](https://developer.android.com/reference/kotlin/android/provider/FontsContract.Columns) Defines the constants used in a response from a Font Provider. |
| open | [FontFamilyResult](https://developer.android.com/reference/kotlin/android/provider/FontsContract.FontFamilyResult) Object returned from [fetchFonts](https://developer.android.com/reference/kotlin/android/provider/FontsContract#fetchFonts(android.content.Context,%20android.os.CancellationSignal,%20android.provider.FontRequest)). |
| open | [FontInfo](https://developer.android.com/reference/kotlin/android/provider/FontsContract.FontInfo) Object represent a font entry in the family returned from [fetchFonts](https://developer.android.com/reference/kotlin/android/provider/FontsContract#fetchFonts(android.content.Context,%20android.os.CancellationSignal,%20android.provider.FontRequest)). |
| --- | --- |
| open | [FontRequestCallback](https://developer.android.com/reference/kotlin/android/provider/FontsContract.FontRequestCallback) Interface used to receive asynchronously fetched typefaces. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Typeface](https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#)! | [buildTypeface](https://developer.android.com/reference/kotlin/android/provider/FontsContract#buildTypeface(android.content.Context,%20android.os.CancellationSignal,%20kotlin.Array))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`, `fonts:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [FontsContract.FontInfo](https://developer.android.com/reference/kotlin/android/provider/FontsContract.FontInfo)!>`)` Build a Typeface from an array of [FontInfo](https://developer.android.com/reference/kotlin/android/provider/FontsContract.FontInfo) Results that are marked as not ready will be skipped. |
| openstatic [FontsContract.FontFamilyResult](https://developer.android.com/reference/kotlin/android/provider/FontsContract.FontFamilyResult) | [fetchFonts](https://developer.android.com/reference/kotlin/android/provider/FontsContract#fetchFonts(android.content.Context,%20android.os.CancellationSignal,%20android.provider.FontRequest))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`, `request:` ` [FontRequest](https://developer.android.com/reference/kotlin/android/provider/FontRequest)`)` Fetch fonts given a font request. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestFonts](https://developer.android.com/reference/kotlin/android/provider/FontsContract#requestFonts(android.content.Context,%20android.provider.FontRequest,%20android.os.Handler,%20android.os.CancellationSignal,%20android.provider.FontsContract.FontRequestCallback))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `request:` ` [FontRequest](https://developer.android.com/reference/kotlin/android/provider/FontRequest)`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)`, `cancellationSignal:` ` [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?`, `callback:` ` [FontsContract.FontRequestCallback](https://developer.android.com/reference/kotlin/android/provider/FontsContract.FontRequestCallback)`)` Create a typeface object given a font request. |
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

Build a Typeface from an array of [FontInfo](https://developer.android.com/reference/kotlin/android/provider/FontsContract.FontInfo) Results that are marked as not ready will be skipped.

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):A [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) that will be used to fetch the font contents. This value cannot be`null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:A signal to cancel the operation in progress, or null if none. If the operation is canceled, then will be thrown. |
| `fonts` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [FontsContract.FontInfo](https://developer.android.com/reference/kotlin/android/provider/FontsContract.FontInfo)!\>:An array of [FontInfo](https://developer.android.com/reference/kotlin/android/provider/FontsContract.FontInfo) to be used to create a Typeface. This value cannot be`null`. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Typeface](https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#)! | A Typeface object. Returns null if typeface creation fails. |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):A [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) to be used for fetching fonts. This value cannot be`null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:A signal to cancel the operation in progress, or null if none. If the operation is canceled, then will be thrown when the query is executed. |
| `request` | [FontRequest](https://developer.android.com/reference/kotlin/android/provider/FontRequest):A [FontRequest](https://developer.android.com/reference/kotlin/android/provider/FontRequest) object that identifies the provider and query for the request. This value cannot be`null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [FontsContract.FontFamilyResult](https://developer.android.com/reference/kotlin/android/provider/FontsContract.FontFamilyResult) | [FontFamilyResult](https://developer.android.com/reference/kotlin/android/provider/FontsContract.FontFamilyResult) This value cannot be`null`. |

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

Create a typeface object given a font request. The font will be asynchronously fetched, therefore the result is delivered to the given callback. See [FontRequest](https://developer.android.com/reference/kotlin/android/provider/FontRequest). Only one of the methods in callback will be invoked, depending on whether the request succeeds or fails. These calls will happen on the caller thread. Note that the result Typeface may be cached internally and the same instance will be returned the next time you call this method with the same request. If you want to bypass this cache, use [fetchFonts](https://developer.android.com/reference/kotlin/android/provider/FontsContract#fetchFonts(android.content.Context,%20android.os.CancellationSignal,%20android.provider.FontRequest))and [buildTypeface](https://developer.android.com/reference/kotlin/android/provider/FontsContract#buildTypeface(android.content.Context,%20android.os.CancellationSignal,%20kotlin.Array))instead.

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):A context to be used for fetching from font provider. This value cannot be`null`. |
| `request` | [FontRequest](https://developer.android.com/reference/kotlin/android/provider/FontRequest):A [FontRequest](https://developer.android.com/reference/kotlin/android/provider/FontRequest) object that identifies the provider and query for the request. May not be null. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#):A handler to be processed the font fetching. This value cannot be`null`. |
| --- | --- |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?:A signal to cancel the operation in progress, or null if none. If the operation is canceled, then will be thrown. |
| `callback` | [FontsContract.FontRequestCallback](https://developer.android.com/reference/kotlin/android/provider/FontsContract.FontRequestCallback):A callback that will be triggered when results are obtained. May not be null. |
