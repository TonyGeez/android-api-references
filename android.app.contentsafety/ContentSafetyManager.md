Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContentSafetyManager

```
class ContentSafetyManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.contentsafety.ContentSafetyManager](ContentSafetyManager.md) |

The ContentSafetyManager provides access to content safety features.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentSafetyManager#ACTION_SHOW_RESTRICTED_CONTENT_DETAILS:kotlin.String` Activity Action: Launch an activity showing information about restricted content. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentSafetyManager#EXTRA_CONTENT_LOCUS_ID:kotlin.String` Extra for `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentSafetyManager#ACTION_SHOW_RESTRICTED_CONTENT_DETAILS:kotlin.String` containing the locus ID of the restricted content. |

| Public methods ||
|---|---|
| [Intent](../android.content/Intent.md)? | createContentRestrictedIntent Creates an `https://developer.android.com/reference/kotlin/android/content/Intent.html#` that can be used with startActivity to display a dialog about the restricted content. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isContentSafetyEnabled Returns whether content safety is currently enabled for the user. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | requestContentClassification Requests classification of the specified content. |
| --- | --- |

## Constants

### ACTION_SHOW_RESTRICTED_CONTENT_DETAILS

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SHOW_RESTRICTED_CONTENT_DETAILS: String
```

Activity Action: Launch an activity showing information about restricted content.

Apps holding the `https://developer.android.com/reference/kotlin/android/app/role/RoleManager.html#ROLE_CONTENT_SAFETY:kotlin.String` must declare an activity that handles this action to show specific content restriction details.

 Value: "android.app.contentsafety.action.SHOW_RESTRICTED_CONTENT_DETAILS"

### EXTRA_CONTENT_LOCUS_ID

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CONTENT_LOCUS_ID: String
```

Extra for `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentSafetyManager#ACTION_SHOW_RESTRICTED_CONTENT_DETAILS:kotlin.String` containing the locus ID of the restricted content.

 Value: "android.app.contentsafety.extra.CONTENT_LOCUS_ID"

## Public methods

### createContentRestrictedIntent

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createContentRestrictedIntent(locusId: LocusId): Intent?
```

Creates an `https://developer.android.com/reference/kotlin/android/content/Intent.html#` that can be used with startActivity to display a dialog about the restricted content.

| Parameters ||
|---|---|
| `locusId` | [LocusId](../android.content/LocusId.md): the `https://developer.android.com/reference/kotlin/android/content/LocusId.html#` of the content to be restricted. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Intent.html#?` | the intent to display the restricted content dialog. This value may be `null`. |

### isContentSafetyEnabled

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isContentSafetyEnabled(): Boolean
```

Returns whether content safety is currently enabled for the user.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if content safety is enabled for the user, `false` otherwise |

### requestContentClassification

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun requestContentClassification(
    content: ClassifiableContent, 
    executor: Executor, 
    callback: ContentClassificationCallback
): Unit
```

Requests classification of the specified content.

When content safety is enabled, this method determines if the specified content is appropriate based on the user's settings.

If the content is classified, the result provided to the callback will have a classification type of `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentClassificationResult#TYPE_ALLOWED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentClassificationResult#TYPE_WARNING:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentClassificationResult#TYPE_BLOCKED:kotlin.Int`. If the content could not be classified or if content safety is disabled, the classification type will be `https://developer.android.com/reference/kotlin/android/app/contentsafety/ContentClassificationResult#TYPE_UNCLASSIFIED:kotlin.Int`.

| Parameters ||
|---|---|
| `content` | [ClassifiableContent](ClassifiableContent.md): the content to be classified. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): the executor on which to run the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [ContentClassificationCallback](ContentClassificationCallback.md): the callback to receive the classification result. This value cannot be `null`. |
| --- | --- |
