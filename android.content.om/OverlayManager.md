Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OverlayManager

Kotlin | [Java](OverlayManager.md)
| --- | --- |

```
open class OverlayManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.om.OverlayManager](OverlayManager.md) |

OverlayManager gives apps the ability to create an OverlayManagerTransaction to maintain the overlays and list the registered fabricated runtime resources overlays(FRROs).

OverlayManager returns the list of overlays to the app calling getOverlayInfosForTarget. The app starts an OverlayManagerTransaction to manage the overlays. The app can achieve the following by using OverlayManagerTransaction.

- register overlays
- unregister overlays
- execute multiple operations in one commitment by calling commit

## Summary

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | commit Commit the overlay manager transaction. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [OverlayInfo](OverlayInfo.md)!\> | getOverlayInfosForTarget Get the related information of self-targeting overlays for `targetPackageName`. |

## Public methods

### commit

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun commit(transaction: OverlayManagerTransaction): Unit
```

Commit the overlay manager transaction.

Applications can register overlays and unregister the registered overlays in an atomic operation via OverlayManagerTransaction.

| Parameters ||
|---|---|
| `transaction` | [OverlayManagerTransaction](OverlayManagerTransaction.md): the series of overlay related requests to perform. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.Exception` | if not all the requests could be successfully |

**See Also**

- OverlayManagerTransaction

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
