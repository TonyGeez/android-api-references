# TaskStackBuilder

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TaskStackBuilder

Kotlin| [Java](TaskStackBuilder.md) 
| --- | --- |

```
open class TaskStackBuilder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.TaskStackBuilder](TaskStackBuilder.md) |

Utility class for constructing synthetic back stacks for cross-task navigation on Android 3.0 and newer.

In API level 11 (Android 3.0/Honeycomb) the recommended conventions for app navigation using the back key changed. The back key's behavior is local to the current task and does not capture navigation across different tasks. Navigating across tasks and easily reaching the previous task is accomplished through the "recents" UI, accessible through the software-provided Recents key on the navigation or system bar. On devices with the older hardware button configuration the recents UI can be accessed with a long press on the Home key.

When crossing from one task stack to another post-Android 3.0, the application should synthesize a back stack/history for the new task so that the user may navigate out of the new task and back to the Launcher by repeated presses of the back key. Back key presses should not navigate across task stacks.

TaskStackBuilder provides a way to obey the correct conventions around cross-task navigation.
|
| ### About Navigation
|
| For more detailed information about tasks, the back stack, and navigation design guidelines, please read [Tasks and Back Stack](https://developer.android.com/guide/topics/fundamentals/tasks-and-back-stack.html) from the developer guide and [Navigation](https://developer.android.com/design/patterns/navigation.html) from the design guide.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [TaskStackBuilder](TaskStackBuilder.md)! | [addNextIntent](TaskStackBuilder.md))`(`nextIntent:` ` [Intent](../android.content/Intent.md)!`)` Add a new Intent to the task stack. |
| open [TaskStackBuilder](TaskStackBuilder.md)! | [addNextIntentWithParentStack](TaskStackBuilder.md))`(`nextIntent:` ` [Intent](../android.content/Intent.md)!`)` Add a new Intent with the resolved chain of parents for the target activity to the task stack. |
| open [TaskStackBuilder](TaskStackBuilder.md)! | [addParentStack](TaskStackBuilder.md))`(`sourceActivity:` ` [Activity](Activity.md)!`)` Add the activity parent chain as specified by the [getParentActivityIntent()](Activity.md))method of the activity specified and the [parentActivityName](../android/R.attr.md) attributes of each successive activity (or activity-alias) element in the application's manifest to the task stack builder. |
| --- | --- |
| open [TaskStackBuilder](TaskStackBuilder.md)! | [addParentStack](TaskStackBuilder.md))`(`sourceActivityName:` ` [ComponentName](../android.content/ComponentName.md)!`)` Add the activity parent chain as specified by the [parentActivityName](../android/R.attr.md) attribute of the activity (or activity-alias) element in the application's manifest to the task stack builder. |
| open [TaskStackBuilder](TaskStackBuilder.md)! | [addParentStack](TaskStackBuilder.md))`(`sourceActivityClass:` ` [Class](../java.lang/Class.md)<*>!`)` Add the activity parent chain as specified by the [parentActivityName](../android/R.attr.md) attribute of the activity (or activity-alias) element in the application's manifest to the task stack builder. |
| openstatic [TaskStackBuilder](TaskStackBuilder.md)! | [create](TaskStackBuilder.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Return a new TaskStackBuilder for launching a fresh task stack consisting of a series of activities. |
| --- | --- |
| open [Intent](../android.content/Intent.md)! | [editIntentAt](TaskStackBuilder.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the intent at the specified index for modification. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntentCount](TaskStackBuilder.md))`()` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Intent](../android.content/Intent.md)!\> | [getIntents](TaskStackBuilder.md))`()` Return an array containing the intents added to this builder. |
| --- | --- |
| open [PendingIntent](PendingIntent.md)! | [getPendingIntent](TaskStackBuilder.md))`(`requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Obtain a [PendingIntent](PendingIntent.md) for launching the task constructed by this builder so far. |
| open [PendingIntent](PendingIntent.md)! | [getPendingIntent](TaskStackBuilder.md))`(`requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `options:` ` [Bundle](../android.os/Bundle.md)!`)` Obtain a [PendingIntent](PendingIntent.md) for launching the task constructed by this builder so far. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startActivities](TaskStackBuilder.md))`()` Start the task stack constructed by this builder. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startActivities](TaskStackBuilder.md))`(`options:` ` [Bundle](../android.os/Bundle.md)!`)` Start the task stack constructed by this builder. |

## Public methods

### addNextIntent

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addNextIntent(nextIntent: Intent!): TaskStackBuilder!
```

Add a new Intent to the task stack. The most recently added Intent will invoke the Activity at the top of the final task stack.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `nextIntent` | [Intent](../android.content/Intent.md)!:Intent for the next Activity in the synthesized task stack |

| Return ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| [TaskStackBuilder](TaskStackBuilder.md)! | This TaskStackBuilder for method chaining |

### addNextIntentWithParentStack

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addNextIntentWithParentStack(nextIntent: Intent!): TaskStackBuilder!
```

Add a new Intent with the resolved chain of parents for the target activity to the task stack.

This is equivalent to calling [addParentStack](TaskStackBuilder.md))with the resolved ComponentName of nextIntent (if it can be resolved), followed by [addNextIntent](TaskStackBuilder.md))with nextIntent.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `nextIntent` | [Intent](../android.content/Intent.md)!:Intent for the topmost Activity in the synthesized task stack. Its chain of parents as specified in the manifest will be added. |

| Return ||
|---------------------------------------------------------------------------------------------------|--------------------------------------------|
| [TaskStackBuilder](TaskStackBuilder.md)! | This TaskStackBuilder for method chaining. |

### addParentStack

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addParentStack(sourceActivity: Activity!): TaskStackBuilder!
```

Add the activity parent chain as specified by the [getParentActivityIntent()](Activity.md))method of the activity specified and the [parentActivityName](../android/R.attr.md) attributes of each successive activity (or activity-alias) element in the application's manifest to the task stack builder.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `sourceActivity` | [Activity](Activity.md)!:All parents of this activity will be added |

| Return ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| [TaskStackBuilder](TaskStackBuilder.md)! | This TaskStackBuilder for method chaining |

### addParentStack

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addParentStack(sourceActivityName: ComponentName!): TaskStackBuilder!
```

Add the activity parent chain as specified by the [parentActivityName](../android/R.attr.md) attribute of the activity (or activity-alias) element in the application's manifest to the task stack builder.

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sourceActivityName` | [ComponentName](../android.content/ComponentName.md)!:Must specify an Activity component. All parents of this activity will be added |

| Return ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| [TaskStackBuilder](TaskStackBuilder.md)! | This TaskStackBuilder for method chaining |

### addParentStack

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addParentStack(sourceActivityClass: Class<*>!): TaskStackBuilder!
```

Add the activity parent chain as specified by the [parentActivityName](../android/R.attr.md) attribute of the activity (or activity-alias) element in the application's manifest to the task stack builder.

| Parameters ||
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `sourceActivityClass` | [Class](../java.lang/Class.md)\<\*\>!:All parents of this activity will be added |

| Return ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| [TaskStackBuilder](TaskStackBuilder.md)! | This TaskStackBuilder for method chaining |

### create

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun create(context: Context!): TaskStackBuilder!
```

Return a new TaskStackBuilder for launching a fresh task stack consisting of a series of activities.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:The context that will launch the new task stack or generate a PendingIntent |

| Return ||
|---------------------------------------------------------------------------------------------------|------------------------|
| [TaskStackBuilder](TaskStackBuilder.md)! | A new TaskStackBuilder |

### editIntentAt

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun editIntentAt(index: Int): Intent!
```

Return the intent at the specified index for modification. Useful if you need to modify the flags or extras of an intent that was previously added, for example with [addParentStack(android.app.Activity)](TaskStackBuilder.md)).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index from 0-getIntentCount() |

| Return ||
|----------------------------------------------------------------------------------------|------------------------------|
| [Intent](../android.content/Intent.md)! | the intent at position index |

### getIntentCount

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIntentCount(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of intents added so far. |

### getIntents

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIntents(): Array<Intent!>
```

Return an array containing the intents added to this builder. The intent at the root of the task stack will appear as the first item in the array and the intent at the top of the stack will appear as the last item.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Intent](../android.content/Intent.md)!> | An array containing the intents added to this builder. This value cannot be`null`. |

### getPendingIntent

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPendingIntent(
    requestCode: Int, 
    flags: Int
): PendingIntent!
```

Obtain a [PendingIntent](PendingIntent.md) for launching the task constructed by this builder so far.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Private request code for the sender |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):May be [PendingIntent.FLAG_ONE_SHOT](PendingIntent.md), [PendingIntent.FLAG_NO_CREATE](PendingIntent.md), [PendingIntent.FLAG_CANCEL_CURRENT](PendingIntent.md), [PendingIntent.FLAG_UPDATE_CURRENT](PendingIntent.md), or any of the flags supported by [Intent.fillIn(Intent, int)](../android.content/Intent.md))to control which unspecified parts of the intent that can be supplied when the actual send happens. Value is either`0`or a combination of [android.app.PendingIntent#FLAG_ONE_SHOT](PendingIntent.md), [android.app.PendingIntent#FLAG_NO_CREATE](PendingIntent.md), [android.app.PendingIntent#FLAG_CANCEL_CURRENT](PendingIntent.md), [android.app.PendingIntent#FLAG_UPDATE_CURRENT](PendingIntent.md), [android.app.PendingIntent#FLAG_IMMUTABLE](PendingIntent.md), [android.app.PendingIntent#FLAG_MUTABLE](PendingIntent.md), android.app.PendingIntent.FLAG_MUTABLE_UNAUDITED, [android.app.PendingIntent#FLAG_ALLOW_UNSAFE_IMPLICIT_INTENT](PendingIntent.md), [android.content.Intent#FILL_IN_ACTION](../android.content/Intent.md), [android.content.Intent#FILL_IN_DATA](../android.content/Intent.md), [android.content.Intent#FILL_IN_CATEGORIES](../android.content/Intent.md), [android.content.Intent#FILL_IN_COMPONENT](../android.content/Intent.md), [android.content.Intent#FILL_IN_PACKAGE](../android.content/Intent.md), [android.content.Intent#FILL_IN_SOURCE_BOUNDS](../android.content/Intent.md), [android.content.Intent#FILL_IN_SELECTOR](../android.content/Intent.md), and [android.content.Intent#FILL_IN_CLIP_DATA](../android.content/Intent.md) |

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------|
| [PendingIntent](PendingIntent.md)! | The obtained PendingIntent |

### getPendingIntent

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPendingIntent(
    requestCode: Int, 
    flags: Int, 
    options: Bundle!
): PendingIntent!
```

Obtain a [PendingIntent](PendingIntent.md) for launching the task constructed by this builder so far.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Private request code for the sender |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):May be [PendingIntent.FLAG_ONE_SHOT](PendingIntent.md), [PendingIntent.FLAG_NO_CREATE](PendingIntent.md), [PendingIntent.FLAG_CANCEL_CURRENT](PendingIntent.md), [PendingIntent.FLAG_UPDATE_CURRENT](PendingIntent.md), or any of the flags supported by [Intent.fillIn(Intent, int)](../android.content/Intent.md))to control which unspecified parts of the intent that can be supplied when the actual send happens. Value is either`0`or a combination of [android.app.PendingIntent#FLAG_ONE_SHOT](PendingIntent.md), [android.app.PendingIntent#FLAG_NO_CREATE](PendingIntent.md), [android.app.PendingIntent#FLAG_CANCEL_CURRENT](PendingIntent.md), [android.app.PendingIntent#FLAG_UPDATE_CURRENT](PendingIntent.md), [android.app.PendingIntent#FLAG_IMMUTABLE](PendingIntent.md), [android.app.PendingIntent#FLAG_MUTABLE](PendingIntent.md), android.app.PendingIntent.FLAG_MUTABLE_UNAUDITED, [android.app.PendingIntent#FLAG_ALLOW_UNSAFE_IMPLICIT_INTENT](PendingIntent.md), [android.content.Intent#FILL_IN_ACTION](../android.content/Intent.md), [android.content.Intent#FILL_IN_DATA](../android.content/Intent.md), [android.content.Intent#FILL_IN_CATEGORIES](../android.content/Intent.md), [android.content.Intent#FILL_IN_COMPONENT](../android.content/Intent.md), [android.content.Intent#FILL_IN_PACKAGE](../android.content/Intent.md), [android.content.Intent#FILL_IN_SOURCE_BOUNDS](../android.content/Intent.md), [android.content.Intent#FILL_IN_SELECTOR](../android.content/Intent.md), and [android.content.Intent#FILL_IN_CLIP_DATA](../android.content/Intent.md) |
| `options` | [Bundle](../android.os/Bundle.md)!:Additional options for how the Activity should be started. See [android.content.Context#startActivity(Intent, Bundle)](../android.content/Context.md))Context.startActivity(Intent, Bundle)} for more details. |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------|
| [PendingIntent](PendingIntent.md)! | The obtained PendingIntent |

### startActivities

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startActivities(): Unit
```

Start the task stack constructed by this builder. 

### startActivities

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startActivities(options: Bundle!): Unit
```

Start the task stack constructed by this builder.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `options` | [Bundle](../android.os/Bundle.md)!:Additional options for how the Activity should be started. See [android.content.Context#startActivity(Intent, Bundle)](../android.content/Context.md))Context.startActivity(Intent, Bundle)} for more details. |
