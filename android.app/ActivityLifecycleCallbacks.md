# Application.ActivityLifecycleCallbacks

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ActivityLifecycleCallbacks

Kotlin| [Java](../android/app/Application.ActivityLifecycleCallbacks.md) 
| --- | --- |

```
interface ActivityLifecycleCallbacks
```

| [android.app.Application.ActivityLifecycleCallbacks](../android/app/Application.ActivityLifecycleCallbacks.md) |

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityCreated](../android/app/Application.ActivityLifecycleCallbacks.md))`(`activity:` ` [Activity](../android/app/Activity.md)`, `savedInstanceState:` ` [Bundle](../android/os/Bundle.md)?`)` Called when the Activity calls android. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityDestroyed](../android/app/Application.ActivityLifecycleCallbacks.md))`(`activity:` ` [Activity](../android/app/Activity.md)`)` Called when the Activity calls [super.onDestroy()](../android/app/Activity.md)). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPaused](../android/app/Application.ActivityLifecycleCallbacks.md))`(`activity:` ` [Activity](../android/app/Activity.md)`)` Called when the Activity calls [super.onPause()](../android/app/Activity.md)). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPostCreated](../android/app/Application.ActivityLifecycleCallbacks.md))`(`activity:` ` [Activity](../android/app/Activity.md)`, `savedInstanceState:` ` [Bundle](../android/os/Bundle.md)?`)` Called as the last step of the Activity being created. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPostDestroyed](../android/app/Application.ActivityLifecycleCallbacks.md))`(`activity:` ` [Activity](../android/app/Activity.md)`)` Called as the last step of the Activity being destroyed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPostPaused](../android/app/Application.ActivityLifecycleCallbacks.md))`(`activity:` ` [Activity](../android/app/Activity.md)`)` Called as the last step of the Activity being paused. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPostResumed](../android/app/Application.ActivityLifecycleCallbacks.md))`(`activity:` ` [Activity](../android/app/Activity.md)`)` Called as the last step of the Activity being resumed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPostSaveInstanceState](../android/app/Application.ActivityLifecycleCallbacks.md))`(`activity:` ` [Activity](../android/app/Activity.md)`, `outState:` ` [Bundle](../android/os/Bundle.md)`)` Called as the last step of the Activity saving its instance state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPostStarted](../android/app/Application.ActivityLifecycleCallbacks.md))`(`activity:` ` [Activity](../android/app/Activity.md)`)` Called as the last step of the Activity being started. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPostStopped](../android/app/Application.ActivityLifecycleCallbacks.md))`(`activity:` ` [Activity](../android/app/Activity.md)`)` Called as the last step of the Activity being stopped. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPreCreated](../android/app/Application.ActivityLifecycleCallbacks.md))`(`activity:` ` [Activity](../android/app/Activity.md)`, `savedInstanceState:` ` [Bundle](../android/os/Bundle.md)?`)` Called as the first step of the Activity being created. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPreDestroyed](../android/app/Application.ActivityLifecycleCallbacks.md))`(`activity:` ` [Activity](../android/app/Activity.md)`)` Called as the first step of the Activity being destroyed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPrePaused](../android/app/Application.ActivityLifecycleCallbacks.md))`(`activity:` ` [Activity](../android/app/Activity.md)`)` Called as the first step of the Activity being paused. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPreResumed](../android/app/Application.ActivityLifecycleCallbacks.md))`(`activity:` ` [Activity](../android/app/Activity.md)`)` Called as the first step of the Activity being resumed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPreSaveInstanceState](../android/app/Application.ActivityLifecycleCallbacks.md))`(`activity:` ` [Activity](../android/app/Activity.md)`, `outState:` ` [Bundle](../android/os/Bundle.md)`)` Called as the first step of the Activity saving its instance state. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPreStarted](../android/app/Application.ActivityLifecycleCallbacks.md))`(`activity:` ` [Activity](../android/app/Activity.md)`)` Called as the first step of the Activity being started. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPreStopped](../android/app/Application.ActivityLifecycleCallbacks.md))`(`activity:` ` [Activity](../android/app/Activity.md)`)` Called as the first step of the Activity being stopped. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityResumed](../android/app/Application.ActivityLifecycleCallbacks.md))`(`activity:` ` [Activity](../android/app/Activity.md)`)` Called when the Activity calls [super.onResume()](../android/app/Activity.md)). |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivitySaveInstanceState](../android/app/Application.ActivityLifecycleCallbacks.md))`(`activity:` ` [Activity](../android/app/Activity.md)`, `outState:` ` [Bundle](../android/os/Bundle.md)`)` Called when the Activity calls android. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityStarted](../android/app/Application.ActivityLifecycleCallbacks.md))`(`activity:` ` [Activity](../android/app/Activity.md)`)` Called when the Activity calls [super.onStart()](../android/app/Activity.md)). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityStopped](../android/app/Application.ActivityLifecycleCallbacks.md))`(`activity:` ` [Activity](../android/app/Activity.md)`)` Called when the Activity calls [super.onStop()](../android/app/Activity.md)). |
| --- | --- |

## Public methods

### onActivityCreated

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActivityCreated(
    activity: Activity, 
    savedInstanceState: Bundle?
): Unit
```

Called when the Activity calls android.app.Activity#onCreate.

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android/app/Activity.md):This value cannot be`null`. |
| `savedInstanceState` | [Bundle](../android/os/Bundle.md)?:This value may be`null`. |

### onActivityDestroyed

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActivityDestroyed(activity: Activity): Unit
```

Called when the Activity calls [super.onDestroy()](../android/app/Activity.md)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android/app/Activity.md):This value cannot be`null`. |

### onActivityPaused

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActivityPaused(activity: Activity): Unit
```

Called when the Activity calls [super.onPause()](../android/app/Activity.md)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android/app/Activity.md):This value cannot be`null`. |

### onActivityPostCreated

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityPostCreated(
    activity: Activity, 
    savedInstanceState: Bundle?
): Unit
```

Called as the last step of the Activity being created. This is always called after android.app.Activity#onCreate.

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android/app/Activity.md):This value cannot be`null`. |
| `savedInstanceState` | [Bundle](../android/os/Bundle.md)?:This value may be`null`. |

### onActivityPostDestroyed

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityPostDestroyed(activity: Activity): Unit
```

Called as the last step of the Activity being destroyed. This is always called after [Activity.onDestroy](../android/app/Activity.md)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android/app/Activity.md):This value cannot be`null`. |

### onActivityPostPaused

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityPostPaused(activity: Activity): Unit
```

Called as the last step of the Activity being paused. This is always called after [Activity.onPause](../android/app/Activity.md)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android/app/Activity.md):This value cannot be`null`. |

### onActivityPostResumed

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityPostResumed(activity: Activity): Unit
```

Called as the last step of the Activity being resumed. This is always called after [Activity.onResume](../android/app/Activity.md))and [Activity.onPostResume](../android/app/Activity.md)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android/app/Activity.md):This value cannot be`null`. |

### onActivityPostSaveInstanceState

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityPostSaveInstanceState(
    activity: Activity, 
    outState: Bundle
): Unit
```

Called as the last step of the Activity saving its instance state. This is always called afterandroid.app.Activity#onSaveInstanceState.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android/app/Activity.md):This value cannot be`null`. |
| `outState` | [Bundle](../android/os/Bundle.md):This value cannot be`null`. |

### onActivityPostStarted

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityPostStarted(activity: Activity): Unit
```

Called as the last step of the Activity being started. This is always called after [Activity.onStart](../android/app/Activity.md)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android/app/Activity.md):This value cannot be`null`. |

### onActivityPostStopped

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityPostStopped(activity: Activity): Unit
```

Called as the last step of the Activity being stopped. This is always called after [Activity.onStop](../android/app/Activity.md)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android/app/Activity.md):This value cannot be`null`. |

### onActivityPreCreated

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityPreCreated(
    activity: Activity, 
    savedInstanceState: Bundle?
): Unit
```

Called as the first step of the Activity being created. This is always called before android.app.Activity#onCreate.

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android/app/Activity.md):This value cannot be`null`. |
| `savedInstanceState` | [Bundle](../android/os/Bundle.md)?:This value may be`null`. |

### onActivityPreDestroyed

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityPreDestroyed(activity: Activity): Unit
```

Called as the first step of the Activity being destroyed. This is always called before [Activity.onDestroy](../android/app/Activity.md)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android/app/Activity.md):This value cannot be`null`. |

### onActivityPrePaused

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityPrePaused(activity: Activity): Unit
```

Called as the first step of the Activity being paused. This is always called before [Activity.onPause](../android/app/Activity.md)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android/app/Activity.md):This value cannot be`null`. |

### onActivityPreResumed

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityPreResumed(activity: Activity): Unit
```

Called as the first step of the Activity being resumed. This is always called before [Activity.onResume](../android/app/Activity.md)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android/app/Activity.md):This value cannot be`null`. |

### onActivityPreSaveInstanceState

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityPreSaveInstanceState(
    activity: Activity, 
    outState: Bundle
): Unit
```

Called as the first step of the Activity saving its instance state. This is always called before android.app.Activity#onSaveInstanceState.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android/app/Activity.md):This value cannot be`null`. |
| `outState` | [Bundle](../android/os/Bundle.md):This value cannot be`null`. |

### onActivityPreStarted

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityPreStarted(activity: Activity): Unit
```

Called as the first step of the Activity being started. This is always called before [Activity.onStart](../android/app/Activity.md)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android/app/Activity.md):This value cannot be`null`. |

### onActivityPreStopped

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityPreStopped(activity: Activity): Unit
```

Called as the first step of the Activity being stopped. This is always called before [Activity.onStop](../android/app/Activity.md)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android/app/Activity.md):This value cannot be`null`. |

### onActivityResumed

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActivityResumed(activity: Activity): Unit
```

Called when the Activity calls [super.onResume()](../android/app/Activity.md)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android/app/Activity.md):This value cannot be`null`. |

### onActivitySaveInstanceState

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActivitySaveInstanceState(
    activity: Activity, 
    outState: Bundle
): Unit
```

Called when the Activity calls android.app.Activity#onSaveInstanceState.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android/app/Activity.md):This value cannot be`null`. |
| `outState` | [Bundle](../android/os/Bundle.md):This value cannot be`null`. |

### onActivityStarted

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActivityStarted(activity: Activity): Unit
```

Called when the Activity calls [super.onStart()](../android/app/Activity.md)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android/app/Activity.md):This value cannot be`null`. |

### onActivityStopped

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActivityStopped(activity: Activity): Unit
```

Called when the Activity calls [super.onStop()](../android/app/Activity.md)).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android/app/Activity.md):This value cannot be`null`. |
