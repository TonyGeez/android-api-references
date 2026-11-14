# TaskStackBuilder

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TaskStackBuilder

Kotlin| [Java](https://developer.android.com/reference/android/app/TaskStackBuilder "View this page in Java") 

```
open class TaskStackBuilder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.TaskStackBuilder](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#) |

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
| open [TaskStackBuilder](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#)! | [addNextIntent](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#addNextIntent(android.content.Intent))`(`nextIntent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` Add a new Intent to the task stack. |
| open [TaskStackBuilder](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#)! | [addNextIntentWithParentStack](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#addNextIntentWithParentStack(android.content.Intent))`(`nextIntent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` Add a new Intent with the resolved chain of parents for the target activity to the task stack. |
| open [TaskStackBuilder](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#)! | [addParentStack](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#addParentStack(android.app.Activity))`(`sourceActivity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)!`)` Add the activity parent chain as specified by the [getParentActivityIntent()](https://developer.android.com/reference/kotlin/android/app/Activity#getParentActivityIntent())method of the activity specified and the [parentActivityName](https://developer.android.com/reference/kotlin/android/R.attr.html#parentActivityName:kotlin.Int) attributes of each successive activity (or activity-alias) element in the application's manifest to the task stack builder. |
| open [TaskStackBuilder](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#)! | [addParentStack](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#addParentStack(android.content.ComponentName))`(`sourceActivityName:` ` [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)!`)` Add the activity parent chain as specified by the [parentActivityName](https://developer.android.com/reference/kotlin/android/R.attr.html#parentActivityName:kotlin.Int) attribute of the activity (or activity-alias) element in the application's manifest to the task stack builder. |
| open [TaskStackBuilder](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#)! | [addParentStack](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#addParentStack(java.lang.Class))`(`sourceActivityClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!`)` Add the activity parent chain as specified by the [parentActivityName](https://developer.android.com/reference/kotlin/android/R.attr.html#parentActivityName:kotlin.Int) attribute of the activity (or activity-alias) element in the application's manifest to the task stack builder. |
| openstatic [TaskStackBuilder](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#)! | [create](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#create(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Return a new TaskStackBuilder for launching a fresh task stack consisting of a series of activities. |
| open [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)! | [editIntentAt](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#editIntentAt(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the intent at the specified index for modification. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIntentCount](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#getIntentCount())`()` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!\> | [getIntents](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#getIntents())`()` Return an array containing the intents added to this builder. |
| open [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent)! | [getPendingIntent](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#getPendingIntent(kotlin.Int,%20kotlin.Int))`(`requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Obtain a [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent) for launching the task constructed by this builder so far. |
| open [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent)! | [getPendingIntent](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#getPendingIntent(kotlin.Int,%20kotlin.Int,%20android.os.Bundle))`(`requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `options:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Obtain a [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent) for launching the task constructed by this builder so far. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startActivities](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#startActivities())`()` Start the task stack constructed by this builder. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startActivities](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#startActivities(android.os.Bundle))`(`options:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Start the task stack constructed by this builder. |

## Public methods

### addNextIntent

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addNextIntent(nextIntent: Intent!): TaskStackBuilder!
```

Add a new Intent to the task stack. The most recently added Intent will invoke the Activity at the top of the final task stack.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `nextIntent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:Intent for the next Activity in the synthesized task stack |

| Return ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| [TaskStackBuilder](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#)! | This TaskStackBuilder for method chaining |

### addNextIntentWithParentStack

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addNextIntentWithParentStack(nextIntent: Intent!): TaskStackBuilder!
```

Add a new Intent with the resolved chain of parents for the target activity to the task stack.

This is equivalent to calling [addParentStack](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#addParentStack(android.content.ComponentName))with the resolved ComponentName of nextIntent (if it can be resolved), followed by [addNextIntent](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#addNextIntent(android.content.Intent))with nextIntent.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `nextIntent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:Intent for the topmost Activity in the synthesized task stack. Its chain of parents as specified in the manifest will be added. |

| Return ||
|---------------------------------------------------------------------------------------------------|--------------------------------------------|
| [TaskStackBuilder](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#)! | This TaskStackBuilder for method chaining. |

### addParentStack

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addParentStack(sourceActivity: Activity!): TaskStackBuilder!
```

Add the activity parent chain as specified by the [getParentActivityIntent()](https://developer.android.com/reference/kotlin/android/app/Activity#getParentActivityIntent())method of the activity specified and the [parentActivityName](https://developer.android.com/reference/kotlin/android/R.attr.html#parentActivityName:kotlin.Int) attributes of each successive activity (or activity-alias) element in the application's manifest to the task stack builder.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `sourceActivity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)!:All parents of this activity will be added |

| Return ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| [TaskStackBuilder](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#)! | This TaskStackBuilder for method chaining |

### addParentStack

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addParentStack(sourceActivityName: ComponentName!): TaskStackBuilder!
```

Add the activity parent chain as specified by the [parentActivityName](https://developer.android.com/reference/kotlin/android/R.attr.html#parentActivityName:kotlin.Int) attribute of the activity (or activity-alias) element in the application's manifest to the task stack builder.

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sourceActivityName` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)!:Must specify an Activity component. All parents of this activity will be added |

| Return ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| [TaskStackBuilder](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#)! | This TaskStackBuilder for method chaining |

### addParentStack

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addParentStack(sourceActivityClass: Class<*>!): TaskStackBuilder!
```

Add the activity parent chain as specified by the [parentActivityName](https://developer.android.com/reference/kotlin/android/R.attr.html#parentActivityName:kotlin.Int) attribute of the activity (or activity-alias) element in the application's manifest to the task stack builder.

| Parameters ||
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `sourceActivityClass` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<\*\>!:All parents of this activity will be added |

| Return ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| [TaskStackBuilder](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#)! | This TaskStackBuilder for method chaining |

### create

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun create(context: Context!): TaskStackBuilder!
```

Return a new TaskStackBuilder for launching a fresh task stack consisting of a series of activities.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The context that will launch the new task stack or generate a PendingIntent |

| Return ||
|---------------------------------------------------------------------------------------------------|------------------------|
| [TaskStackBuilder](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#)! | A new TaskStackBuilder |

### editIntentAt

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun editIntentAt(index: Int): Intent!
```

Return the intent at the specified index for modification. Useful if you need to modify the flags or extras of an intent that was previously added, for example with [addParentStack(android.app.Activity)](https://developer.android.com/reference/kotlin/android/app/TaskStackBuilder#addParentStack(android.app.Activity)).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index from 0-getIntentCount() |

| Return ||
|----------------------------------------------------------------------------------------|------------------------------|
| [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)! | the intent at position index |

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
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!> | An array containing the intents added to this builder. This value cannot be`null`. |

### getPendingIntent

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPendingIntent(
    requestCode: Int, 
    flags: Int
): PendingIntent!
```

Obtain a [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent) for launching the task constructed by this builder so far.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Private request code for the sender |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):May be [PendingIntent.FLAG_ONE_SHOT](https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ONE_SHOT:kotlin.Int), [PendingIntent.FLAG_NO_CREATE](https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int), [PendingIntent.FLAG_CANCEL_CURRENT](https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_CANCEL_CURRENT:kotlin.Int), [PendingIntent.FLAG_UPDATE_CURRENT](https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int), or any of the flags supported by [Intent.fillIn(Intent, int)](https://developer.android.com/reference/kotlin/android/content/Intent.html#fillIn(android.content.Intent,%20kotlin.Int))to control which unspecified parts of the intent that can be supplied when the actual send happens. Value is either`0`or a combination of [android.app.PendingIntent#FLAG_ONE_SHOT](https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ONE_SHOT:kotlin.Int), [android.app.PendingIntent#FLAG_NO_CREATE](https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int), [android.app.PendingIntent#FLAG_CANCEL_CURRENT](https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_CANCEL_CURRENT:kotlin.Int), [android.app.PendingIntent#FLAG_UPDATE_CURRENT](https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int), [android.app.PendingIntent#FLAG_IMMUTABLE](https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int), [android.app.PendingIntent#FLAG_MUTABLE](https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_MUTABLE:kotlin.Int), android.app.PendingIntent.FLAG_MUTABLE_UNAUDITED, [android.app.PendingIntent#FLAG_ALLOW_UNSAFE_IMPLICIT_INTENT](https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ALLOW_UNSAFE_IMPLICIT_INTENT:kotlin.Int), [android.content.Intent#FILL_IN_ACTION](https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_ACTION:kotlin.Int), [android.content.Intent#FILL_IN_DATA](https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_DATA:kotlin.Int), [android.content.Intent#FILL_IN_CATEGORIES](https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_CATEGORIES:kotlin.Int), [android.content.Intent#FILL_IN_COMPONENT](https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_COMPONENT:kotlin.Int), [android.content.Intent#FILL_IN_PACKAGE](https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_PACKAGE:kotlin.Int), [android.content.Intent#FILL_IN_SOURCE_BOUNDS](https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_SOURCE_BOUNDS:kotlin.Int), [android.content.Intent#FILL_IN_SELECTOR](https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_SELECTOR:kotlin.Int), and [android.content.Intent#FILL_IN_CLIP_DATA](https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_CLIP_DATA:kotlin.Int) |

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------|
| [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent)! | The obtained PendingIntent |

### getPendingIntent

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPendingIntent(
    requestCode: Int, 
    flags: Int, 
    options: Bundle!
): PendingIntent!
```

Obtain a [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent) for launching the task constructed by this builder so far.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Private request code for the sender |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):May be [PendingIntent.FLAG_ONE_SHOT](https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ONE_SHOT:kotlin.Int), [PendingIntent.FLAG_NO_CREATE](https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int), [PendingIntent.FLAG_CANCEL_CURRENT](https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_CANCEL_CURRENT:kotlin.Int), [PendingIntent.FLAG_UPDATE_CURRENT](https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int), or any of the flags supported by [Intent.fillIn(Intent, int)](https://developer.android.com/reference/kotlin/android/content/Intent.html#fillIn(android.content.Intent,%20kotlin.Int))to control which unspecified parts of the intent that can be supplied when the actual send happens. Value is either`0`or a combination of [android.app.PendingIntent#FLAG_ONE_SHOT](https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ONE_SHOT:kotlin.Int), [android.app.PendingIntent#FLAG_NO_CREATE](https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_NO_CREATE:kotlin.Int), [android.app.PendingIntent#FLAG_CANCEL_CURRENT](https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_CANCEL_CURRENT:kotlin.Int), [android.app.PendingIntent#FLAG_UPDATE_CURRENT](https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_UPDATE_CURRENT:kotlin.Int), [android.app.PendingIntent#FLAG_IMMUTABLE](https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_IMMUTABLE:kotlin.Int), [android.app.PendingIntent#FLAG_MUTABLE](https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_MUTABLE:kotlin.Int), android.app.PendingIntent.FLAG_MUTABLE_UNAUDITED, [android.app.PendingIntent#FLAG_ALLOW_UNSAFE_IMPLICIT_INTENT](https://developer.android.com/reference/kotlin/android/app/PendingIntent#FLAG_ALLOW_UNSAFE_IMPLICIT_INTENT:kotlin.Int), [android.content.Intent#FILL_IN_ACTION](https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_ACTION:kotlin.Int), [android.content.Intent#FILL_IN_DATA](https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_DATA:kotlin.Int), [android.content.Intent#FILL_IN_CATEGORIES](https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_CATEGORIES:kotlin.Int), [android.content.Intent#FILL_IN_COMPONENT](https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_COMPONENT:kotlin.Int), [android.content.Intent#FILL_IN_PACKAGE](https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_PACKAGE:kotlin.Int), [android.content.Intent#FILL_IN_SOURCE_BOUNDS](https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_SOURCE_BOUNDS:kotlin.Int), [android.content.Intent#FILL_IN_SELECTOR](https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_SELECTOR:kotlin.Int), and [android.content.Intent#FILL_IN_CLIP_DATA](https://developer.android.com/reference/kotlin/android/content/Intent.html#FILL_IN_CLIP_DATA:kotlin.Int) |
| `options` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:Additional options for how the Activity should be started. See [android.content.Context#startActivity(Intent, Bundle)](https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent,%20android.os.Bundle))Context.startActivity(Intent, Bundle)} for more details. |

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------|
| [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent)! | The obtained PendingIntent |

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
| `options` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:Additional options for how the Activity should be started. See [android.content.Context#startActivity(Intent, Bundle)](https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent,%20android.os.Bundle))Context.startActivity(Intent, Bundle)} for more details. |
