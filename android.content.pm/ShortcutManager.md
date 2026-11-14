Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ShortcutManager

```
open class ShortcutManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.pm.ShortcutManager](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#) |

`ShortcutManager` executes operations on an app's set of *shortcuts* , which represent specific tasks and actions that users can perform within your app. This page lists components of the `ShortcutManager` class that you can use to create and manage sets of shortcuts.

To learn about methods that retrieve information about a single shortcut---including identifiers, type, and status---read the ` https://developer.android.com/reference/kotlin/reference/android/content/pm/ShortcutInfo.html` reference.

For guidance about using shortcuts, see [App shortcuts](https://developer.android.com/reference/kotlin/guide/topics/ui/shortcuts/index.html).

### Retrieving class instances

. 
Restricted for SDK Runtime environment in API level 34.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#FLAG_MATCH_CACHED:kotlin.Int` Include cached shortcuts in the result. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#FLAG_MATCH_DYNAMIC:kotlin.Int` Include dynamic shortcuts in the result. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#FLAG_MATCH_MANIFEST:kotlin.Int` Include manifest shortcuts in the result. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#FLAG_MATCH_PINNED:kotlin.Int` Include pinned shortcuts in the result. |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#addDynamicShortcuts(kotlin.collections.MutableList)(shortcutInfoList: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo!>)` Publish the list of dynamic shortcuts. |
| open [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)! | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#createShortcutResultIntent(android.content.pm.ShortcutInfo)(shortcut: https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo)` Returns an Intent which can be used by the default launcher to pin a shortcut containing the given `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#disableShortcuts(kotlin.collections.MutableList)(shortcutIds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)` Disable pinned shortcuts. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#disableShortcuts(kotlin.collections.MutableList,%20kotlin.CharSequence)(shortcutIds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>, disabledMessage: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Disable pinned shortcuts, showing the user a custom error message when they try to select the disabled shortcuts. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#enableShortcuts(kotlin.collections.MutableList)(shortcutIds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)` Re-enable pinned shortcuts that were previously disabled. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ShortcutInfo](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo)!\> | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#getDynamicShortcuts()()` Return all dynamic shortcuts from the caller app. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#getIconMaxHeight()()` Return the max height for icons, in pixels. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#getIconMaxWidth()()` Return the max width for icons, in pixels. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ShortcutInfo](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo)!\> | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#getManifestShortcuts()()` Return all static (manifest) shortcuts from the caller app. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#getMaxShortcutCountPerActivity()()` Return the maximum number of static and dynamic shortcuts that each launcher icon can have at a time. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ShortcutInfo](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo)!\> | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#getPinnedShortcuts()()` Return all pinned shortcuts from the caller app. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ShortcutInfo](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo)!\> | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#getShortcuts(kotlin.Int)(matchFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo`s that match `matchFlags`. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#isRateLimitingActive()()` Return `true` when rate-limiting is active for the caller app. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#isRequestPinShortcutSupported()()` Returns `true` if the app is running on a device whose default launcher supports `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#requestPinShortcut(android.content.pm.ShortcutInfo,%20android.content.IntentSender)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#pushDynamicShortcut(android.content.pm.ShortcutInfo)(shortcut: https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo)` Publish a single dynamic shortcut. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#removeAllDynamicShortcuts()()` Delete all dynamic shortcuts from the caller app. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#removeDynamicShortcuts(kotlin.collections.MutableList)(shortcutIds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)` Delete dynamic shortcuts by ID. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#removeLongLivedShortcuts(kotlin.collections.MutableList)(shortcutIds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)` Delete long lived shortcuts by ID. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#reportShortcutUsed(kotlin.String)(shortcutId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Apps that publish shortcuts should call this method whenever the user selects the shortcut containing the given ID or when the user completes an action in the app that is equivalent to selecting the shortcut. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#requestPinShortcut(android.content.pm.ShortcutInfo,%20android.content.IntentSender)(shortcut: https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo, resultIntent: https://developer.android.com/reference/kotlin/android/content/IntentSender.html#?)` Request to create a pinned shortcut. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#setDynamicShortcuts(kotlin.collections.MutableList)(shortcutInfoList: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo!>)` Publish the list of shortcuts. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#updateShortcuts(kotlin.collections.MutableList)(shortcutInfoList: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo!>)` Update all existing shortcuts with the same IDs. |

## Constants

### FLAG_MATCH_CACHED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_MATCH_CACHED: Int
```

Include cached shortcuts in the result.

 Value: 8

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#getShortcuts(kotlin.Int)`

### FLAG_MATCH_DYNAMIC

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_MATCH_DYNAMIC: Int
```

Include dynamic shortcuts in the result.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#getShortcuts(kotlin.Int)`

### FLAG_MATCH_MANIFEST

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_MATCH_MANIFEST: Int
```

Include manifest shortcuts in the result.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#getShortcuts(kotlin.Int)`

### FLAG_MATCH_PINNED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_MATCH_PINNED: Int
```

Include pinned shortcuts in the result.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#getShortcuts(kotlin.Int)`

## Public methods

### addDynamicShortcuts

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addDynamicShortcuts(shortcutInfoList: MutableList<ShortcutInfo!>): Boolean
```

Publish the list of dynamic shortcuts. If there are already dynamic or pinned shortcuts with the same IDs, each mutable shortcut is updated.

This API will be rate-limited. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `shortcutInfoList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ShortcutInfo](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo)!\>: This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the call has succeeded. `false` if the call is rate-limited. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#getMaxShortcutCountPerActivity()` is exceeded, or when trying to update immutable shortcuts. |
| `java.lang.IllegalStateException` | when the user is locked. |

### createShortcutResultIntent

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createShortcutResultIntent(shortcut: ShortcutInfo): Intent!
```

Returns an Intent which can be used by the default launcher to pin a shortcut containing the given `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo`. This method should be used by an Activity to set a result in response to `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CREATE_SHORTCUT:kotlin.String`. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `shortcut` | [ShortcutInfo](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo): New shortcut to pin. If an app wants to pin an existing (either dynamic or manifest) shortcut, then it only needs to have an ID, and other fields don't have to be set, in which case, the target shortcut must be enabled. If it's a new shortcut, all the mandatory fields, such as a short label, must be set. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Intent.html#!` | The intent that should be set as the result for the calling activity, or `null` if the current launcher doesn't support shortcuts. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if a shortcut with the same ID exists and is disabled. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_CREATE_SHORTCUT:kotlin.String`

### disableShortcuts

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun disableShortcuts(shortcutIds: MutableList<String!>): Unit
```

Disable pinned shortcuts. For more details, read [Disable shortcuts](https://developer.android.com/reference/kotlin/guide/topics/ui/shortcuts/managing-shortcuts.html#disable-shortcuts).

| Parameters ||
|---|---|
| `shortcutIds` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If trying to disable immutable shortcuts. |
| `java.lang.IllegalStateException` | when the user is locked. |

### disableShortcuts

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun disableShortcuts(
    shortcutIds: MutableList<String!>, 
    disabledMessage: CharSequence!
): Unit
```

Disable pinned shortcuts, showing the user a custom error message when they try to select the disabled shortcuts. For more details, read [Disable shortcuts](https://developer.android.com/reference/kotlin/guide/topics/ui/shortcuts/managing-shortcuts.html#disable-shortcuts).

| Parameters ||
|---|---|
| `shortcutIds` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If trying to disable immutable shortcuts. |
| `java.lang.IllegalStateException` | when the user is locked. |

### enableShortcuts

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun enableShortcuts(shortcutIds: MutableList<String!>): Unit
```

Re-enable pinned shortcuts that were previously disabled. If the target shortcuts are already enabled, this method does nothing.

| Parameters ||
|---|---|
| `shortcutIds` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If trying to enable immutable shortcuts. |
| `java.lang.IllegalStateException` | when the user is locked. |

### getDynamicShortcuts

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDynamicShortcuts(): MutableList<ShortcutInfo!>
```

Return all dynamic shortcuts from the caller app.

This API is intended to be used for examining what shortcuts are currently published. Re-publishing returned `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo`s via APIs such as `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#setDynamicShortcuts(kotlin.collections.MutableList)` may cause loss of information such as icons. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo!>` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | when the user is locked. |

### getIconMaxHeight

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIconMaxHeight(): Int
```

Return the max height for icons, in pixels.

### getIconMaxWidth

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIconMaxWidth(): Int
```

Return the max width for icons, in pixels.

Note that this method returns max width of icon's visible part. Hence, it does not take into account the inset introduced by `https://developer.android.com/reference/kotlin/android/graphics/drawable/AdaptiveIconDrawable.html#`. To calculate bitmap image to function as `https://developer.android.com/reference/kotlin/android/graphics/drawable/AdaptiveIconDrawable.html#`, multiply 1 + 2 \* `https://developer.android.com/reference/kotlin/android/graphics/drawable/AdaptiveIconDrawable.html#getExtraInsetFraction()` to the returned size.

### getManifestShortcuts

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getManifestShortcuts(): MutableList<ShortcutInfo!>
```

Return all static (manifest) shortcuts from the caller app.

This API is intended to be used for examining what shortcuts are currently published. Re-publishing returned `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo`s via APIs such as `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#setDynamicShortcuts(kotlin.collections.MutableList)` may cause loss of information such as icons. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo!>` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | when the user is locked. |

### getMaxShortcutCountPerActivity

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMaxShortcutCountPerActivity(): Int
```

Return the maximum number of static and dynamic shortcuts that each launcher icon can have at a time.

### getPinnedShortcuts

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPinnedShortcuts(): MutableList<ShortcutInfo!>
```

Return all pinned shortcuts from the caller app.

This API is intended to be used for examining what shortcuts are currently published. Re-publishing returned `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo`s via APIs such as `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#setDynamicShortcuts(kotlin.collections.MutableList)` may cause loss of information such as icons. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo!>` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | when the user is locked. |

### getShortcuts

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getShortcuts(matchFlags: Int): MutableList<ShortcutInfo!>
```

Returns `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo`s that match `matchFlags`. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `matchFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): result includes shortcuts matching this flags. Any combination of: - `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#FLAG_MATCH_MANIFEST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#FLAG_MATCH_DYNAMIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#FLAG_MATCH_PINNED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#FLAG_MATCH_CACHED:kotlin.Int` . Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#FLAG_MATCH_MANIFEST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#FLAG_MATCH_DYNAMIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#FLAG_MATCH_PINNED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#FLAG_MATCH_CACHED:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo!>` | list of `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo`s that match the flag. At least one of the `MATCH` flags should be set. Otherwise no shortcuts will be returned. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | when the user is locked. |

### isRateLimitingActive

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isRateLimitingActive(): Boolean
```

Return `true` when rate-limiting is active for the caller app.

For details, see [Rate limiting](https://developer.android.com/reference/kotlin/guide/topics/ui/shortcuts/managing-shortcuts#rate-limiting).

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | when the user is locked. |

### isRequestPinShortcutSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isRequestPinShortcutSupported(): Boolean
```

Returns `true` if the app is running on a device whose default launcher supports `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#requestPinShortcut(android.content.pm.ShortcutInfo,%20android.content.IntentSender)`.

Returns `false` if the default launcher does not support pinning, or if App Lock is currently enabled for the calling app. App Lock is a feature that allows users to require authentication before opening apps (see `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getEnableAppLockIntentForPackage(kotlin.String,%20kotlin.Boolean)`). Applications should re-query this method when returning to the foreground (e.g. in `https://developer.android.com/reference/kotlin/android/app/Activity.html#onResume()`) to update shortcut pinning UI.

The return value may change in subsequent calls if the user changes the default launcher app.

**Note:** See also the support library counterpart androidx.core.content.pm.ShortcutManagerCompat#isRequestPinShortcutSupported(android.content.Context), which supports Android versions lower than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` using the legacy private intent `com.android.launcher.action.INSTALL_SHORTCUT`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#requestPinShortcut(android.content.pm.ShortcutInfo,%20android.content.IntentSender)`

### pushDynamicShortcut

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun pushDynamicShortcut(shortcut: ShortcutInfo): Unit
```

Publish a single dynamic shortcut. If there are already dynamic or pinned shortcuts with the same ID, each mutable shortcut is updated.

This method is useful when posting notifications which are tagged with shortcut IDs; In order to make sure shortcuts exist and are up-to-date, without the need to explicitly handle the shortcut count limit.

| Parameters ||
|---|---|
| `shortcut` | [ShortcutInfo](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo): This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if trying to update an immutable shortcut. |
| `java.lang.IllegalStateException` | when the user is locked. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/NotificationManager.html#notify(kotlin.Int,%20android.app.Notification)`
- `https://developer.android.com/reference/kotlin/android/app/Notification.Builder.html#setShortcutId(kotlin.String)`

### removeAllDynamicShortcuts

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeAllDynamicShortcuts(): Unit
```

Delete all dynamic shortcuts from the caller app.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | when the user is locked. |

### removeDynamicShortcuts

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeDynamicShortcuts(shortcutIds: MutableList<String!>): Unit
```

Delete dynamic shortcuts by ID.

| Parameters ||
|---|---|
| `shortcutIds` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | when the user is locked. |

### removeLongLivedShortcuts

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeLongLivedShortcuts(shortcutIds: MutableList<String!>): Unit
```

Delete long lived shortcuts by ID.

| Parameters ||
|---|---|
| `shortcutIds` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | when the user is locked. |

### reportShortcutUsed

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reportShortcutUsed(shortcutId: String!): Unit
```

Apps that publish shortcuts should call this method whenever the user selects the shortcut containing the given ID or when the user completes an action in the app that is equivalent to selecting the shortcut. For more details, read about [tracking shortcut usage](https://developer.android.com/reference/kotlin/guide/topics/ui/shortcuts/managing-shortcuts.html#track-usage).

The information is accessible via android.app.usage.UsageStatsManager#queryEvents Typically, launcher apps use this information to build a prediction model so that they can promote the shortcuts that are likely to be used at the moment.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | when the user is locked. |

### requestPinShortcut

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestPinShortcut(
    shortcut: ShortcutInfo, 
    resultIntent: IntentSender?
): Boolean
```

Request to create a pinned shortcut. The default launcher will receive this request and ask the user for approval. If the user approves it, the shortcut will be created, and `resultIntent` will be sent. If a request is denied by the user, however, no response will be sent to the caller.

Only apps with a foreground activity or a foreground service can call this method. Otherwise, it'll throw `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`.

It's up to the launcher to decide how to handle previous pending requests when the same package calls this API multiple times in a row. One possible strategy is to ignore any previous requests.

**Note:** See also the support library counterpart androidx.core.content.pm.ShortcutManagerCompat#requestPinShortcut(android.content.Context,ShortcutInfoCompat,android.content.IntentSender), which supports Android versions lower than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int` using the legacy private intent `com.android.launcher.action.INSTALL_SHORTCUT`. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `shortcut` | [ShortcutInfo](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo): Shortcut to pin. If an app wants to pin an existing (either static or dynamic) shortcut, then it only needs to have an ID. Although other fields don't have to be set, the target shortcut must be enabled. If it's a new shortcut, all the mandatory fields, such as a short label, must be set. This value cannot be `null`. |
| `resultIntent` | [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender.html#)?: If not null, this intent will be sent when the shortcut is pinned. Use `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#getIntentSender()` to create an `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#`. To avoid background execution limits, use an unexported, manifest-declared receiver. For more details, see [Creating pinned shortcuts](https://developer.android.com/reference/kotlin/guide/topics/ui/shortcuts/creating-shortcuts.html#pinned). |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the launcher supports this feature. Note the API will return without waiting for the user to respond, so getting `true` from this API does \*not\* mean the shortcut was pinned successfully. `false` if the launcher doesn't support this feature or if calling app belongs to a user-profile with items restricted on home screen. If App Lock is enabled for the calling app, shortcut pinning requests will be rejected and this method will return `false`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if a shortcut with the same ID exists and is disabled. |
| `java.lang.IllegalStateException` | The caller doesn't have a foreground activity or a foreground service, or the device is locked. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#isRequestPinShortcutSupported()`
- `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#`
- `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#getIntentSender()`

### setDynamicShortcuts

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDynamicShortcuts(shortcutInfoList: MutableList<ShortcutInfo!>): Boolean
```

Publish the list of shortcuts. All existing dynamic shortcuts from the caller app will be replaced. If there are already pinned shortcuts with the same IDs, the mutable pinned shortcuts are updated.

This API will be rate-limited. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `shortcutInfoList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ShortcutInfo](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo)!\>: This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the call has succeeded. `false` if the call is rate-limited. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager#getMaxShortcutCountPerActivity()` is exceeded, or when trying to update immutable shortcuts. |
| `java.lang.IllegalStateException` | when the user is locked. |

### updateShortcuts

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateShortcuts(shortcutInfoList: MutableList<ShortcutInfo!>): Boolean
```

Update all existing shortcuts with the same IDs. Target shortcuts may be pinned and/or dynamic, but they must not be immutable.

This API will be rate-limited. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `shortcutInfoList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ShortcutInfo](https://developer.android.com/reference/kotlin/android/content/pm/ShortcutInfo)!\>: This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the call has succeeded. `false` if the call is rate-limited. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If trying to update immutable shortcuts. |
| `java.lang.IllegalStateException` | when the user is locked. |
