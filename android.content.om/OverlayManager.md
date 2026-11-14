Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OverlayManager

Kotlin | [Java](../android/content/om/OverlayManager.md)
| --- | --- |

```
open class OverlayManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.om.OverlayManager](../android/content/om/OverlayManager.md) |

OverlayManager gives apps the ability to create an `https://developer.android.com/reference/kotlin/android/content/om/OverlayManagerTransaction` to maintain the overlays and list the registered fabricated runtime resources overlays(FRROs).

OverlayManager returns the list of overlays to the app calling `https://developer.android.com/reference/kotlin/android/content/om/OverlayManager#getOverlayInfosForTarget(kotlin.String)`. The app starts an `https://developer.android.com/reference/kotlin/android/content/om/OverlayManagerTransaction` to manage the overlays. The app can achieve the following by using `https://developer.android.com/reference/kotlin/android/content/om/OverlayManagerTransaction`.

- register overlays
- unregister overlays
- execute multiple operations in one commitment by calling `https://developer.android.com/reference/kotlin/android/content/om/OverlayManager#commit(android.content.om.OverlayManagerTransaction)`

## Summary

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/om/OverlayManager#commit(android.content.om.OverlayManagerTransaction)(transaction: https://developer.android.com/reference/kotlin/android/content/om/OverlayManagerTransaction)` Commit the overlay manager transaction. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [OverlayInfo](../android/content/om/OverlayInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/content/om/OverlayManager#getOverlayInfosForTarget(kotlin.String)(targetPackageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Get the related information of self-targeting overlays for `targetPackageName`. |

## Public methods

### commit

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun commit(transaction: OverlayManagerTransaction): Unit
```

Commit the overlay manager transaction.

Applications can register overlays and unregister the registered overlays in an atomic operation via `https://developer.android.com/reference/kotlin/android/content/om/OverlayManagerTransaction`.

| Parameters ||
|---|---|
| `transaction` | [OverlayManagerTransaction](../android/content/om/OverlayManagerTransaction.md): the series of overlay related requests to perform. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.Exception` | if not all the requests could be successfully |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/om/OverlayManagerTransaction`

### getOverlayInfosForTarget

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOverlayInfosForTarget(targetPackageName: String): MutableList<OverlayInfo!>
```

Get the related information of self-targeting overlays for `targetPackageName`.

| Parameters ||
|---|---|
| `targetPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the target package name. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/om/OverlayInfo!>` | a list of overlay information. This value cannot be `null`. |
