# Application.ActivityLifecycleCallbacks

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ActivityLifecycleCallbacks

Kotlin| [Java](https://developer.android.com/reference/android/app/Application.ActivityLifecycleCallbacks "View this page in Java") 
| --- | --- |

```
interface ActivityLifecycleCallbacks
```

| [android.app.Application.ActivityLifecycleCallbacks](https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#) |

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityCreated](https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivityCreated(android.app.Activity,%20android.os.Bundle))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)`, `savedInstanceState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` Called when the Activity calls android. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityDestroyed](https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivityDestroyed(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)`)` Called when the Activity calls [super.onDestroy()](https://developer.android.com/reference/kotlin/android/app/Activity#onDestroy()). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPaused](https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivityPaused(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)`)` Called when the Activity calls [super.onPause()](https://developer.android.com/reference/kotlin/android/app/Activity#onPause()). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPostCreated](https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivityPostCreated(android.app.Activity,%20android.os.Bundle))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)`, `savedInstanceState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` Called as the last step of the Activity being created. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPostDestroyed](https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivityPostDestroyed(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)`)` Called as the last step of the Activity being destroyed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPostPaused](https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivityPostPaused(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)`)` Called as the last step of the Activity being paused. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPostResumed](https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivityPostResumed(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)`)` Called as the last step of the Activity being resumed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPostSaveInstanceState](https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivityPostSaveInstanceState(android.app.Activity,%20android.os.Bundle))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)`, `outState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)`)` Called as the last step of the Activity saving its instance state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPostStarted](https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivityPostStarted(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)`)` Called as the last step of the Activity being started. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPostStopped](https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivityPostStopped(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)`)` Called as the last step of the Activity being stopped. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPreCreated](https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivityPreCreated(android.app.Activity,%20android.os.Bundle))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)`, `savedInstanceState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` Called as the first step of the Activity being created. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPreDestroyed](https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivityPreDestroyed(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)`)` Called as the first step of the Activity being destroyed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPrePaused](https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivityPrePaused(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)`)` Called as the first step of the Activity being paused. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPreResumed](https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivityPreResumed(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)`)` Called as the first step of the Activity being resumed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPreSaveInstanceState](https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivityPreSaveInstanceState(android.app.Activity,%20android.os.Bundle))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)`, `outState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)`)` Called as the first step of the Activity saving its instance state. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPreStarted](https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivityPreStarted(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)`)` Called as the first step of the Activity being started. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityPreStopped](https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivityPreStopped(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)`)` Called as the first step of the Activity being stopped. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityResumed](https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivityResumed(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)`)` Called when the Activity calls [super.onResume()](https://developer.android.com/reference/kotlin/android/app/Activity#onResume()). |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivitySaveInstanceState](https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivitySaveInstanceState(android.app.Activity,%20android.os.Bundle))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)`, `outState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)`)` Called when the Activity calls android. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityStarted](https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivityStarted(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)`)` Called when the Activity calls [super.onStart()](https://developer.android.com/reference/kotlin/android/app/Activity#onStart()). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityStopped](https://developer.android.com/reference/kotlin/android/app/Application.ActivityLifecycleCallbacks#onActivityStopped(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)`)` Called when the Activity calls [super.onStop()](https://developer.android.com/reference/kotlin/android/app/Activity#onStop()). |
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
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity):This value cannot be`null`. |
| `savedInstanceState` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:This value may be`null`. |

### onActivityDestroyed

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActivityDestroyed(activity: Activity): Unit
```

Called when the Activity calls [super.onDestroy()](https://developer.android.com/reference/kotlin/android/app/Activity#onDestroy()).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity):This value cannot be`null`. |

### onActivityPaused

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActivityPaused(activity: Activity): Unit
```

Called when the Activity calls [super.onPause()](https://developer.android.com/reference/kotlin/android/app/Activity#onPause()).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity):This value cannot be`null`. |

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
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity):This value cannot be`null`. |
| `savedInstanceState` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:This value may be`null`. |

### onActivityPostDestroyed

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityPostDestroyed(activity: Activity): Unit
```

Called as the last step of the Activity being destroyed. This is always called after [Activity.onDestroy](https://developer.android.com/reference/kotlin/android/app/Activity#onDestroy()).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity):This value cannot be`null`. |

### onActivityPostPaused

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityPostPaused(activity: Activity): Unit
```

Called as the last step of the Activity being paused. This is always called after [Activity.onPause](https://developer.android.com/reference/kotlin/android/app/Activity#onPause()).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity):This value cannot be`null`. |

### onActivityPostResumed

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityPostResumed(activity: Activity): Unit
```

Called as the last step of the Activity being resumed. This is always called after [Activity.onResume](https://developer.android.com/reference/kotlin/android/app/Activity#onResume())and [Activity.onPostResume](https://developer.android.com/reference/kotlin/android/app/Activity#onPostResume()).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity):This value cannot be`null`. |

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
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity):This value cannot be`null`. |
| `outState` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#):This value cannot be`null`. |

### onActivityPostStarted

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityPostStarted(activity: Activity): Unit
```

Called as the last step of the Activity being started. This is always called after [Activity.onStart](https://developer.android.com/reference/kotlin/android/app/Activity#onStart()).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity):This value cannot be`null`. |

### onActivityPostStopped

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityPostStopped(activity: Activity): Unit
```

Called as the last step of the Activity being stopped. This is always called after [Activity.onStop](https://developer.android.com/reference/kotlin/android/app/Activity#onStop()).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity):This value cannot be`null`. |

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
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity):This value cannot be`null`. |
| `savedInstanceState` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:This value may be`null`. |

### onActivityPreDestroyed

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityPreDestroyed(activity: Activity): Unit
```

Called as the first step of the Activity being destroyed. This is always called before [Activity.onDestroy](https://developer.android.com/reference/kotlin/android/app/Activity#onDestroy()).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity):This value cannot be`null`. |

### onActivityPrePaused

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityPrePaused(activity: Activity): Unit
```

Called as the first step of the Activity being paused. This is always called before [Activity.onPause](https://developer.android.com/reference/kotlin/android/app/Activity#onPause()).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity):This value cannot be`null`. |

### onActivityPreResumed

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityPreResumed(activity: Activity): Unit
```

Called as the first step of the Activity being resumed. This is always called before [Activity.onResume](https://developer.android.com/reference/kotlin/android/app/Activity#onResume()).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity):This value cannot be`null`. |

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
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity):This value cannot be`null`. |
| `outState` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#):This value cannot be`null`. |

### onActivityPreStarted

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityPreStarted(activity: Activity): Unit
```

Called as the first step of the Activity being started. This is always called before [Activity.onStart](https://developer.android.com/reference/kotlin/android/app/Activity#onStart()).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity):This value cannot be`null`. |

### onActivityPreStopped

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityPreStopped(activity: Activity): Unit
```

Called as the first step of the Activity being stopped. This is always called before [Activity.onStop](https://developer.android.com/reference/kotlin/android/app/Activity#onStop()).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity):This value cannot be`null`. |

### onActivityResumed

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActivityResumed(activity: Activity): Unit
```

Called when the Activity calls [super.onResume()](https://developer.android.com/reference/kotlin/android/app/Activity#onResume()).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity):This value cannot be`null`. |

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
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity):This value cannot be`null`. |
| `outState` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#):This value cannot be`null`. |

### onActivityStarted

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActivityStarted(activity: Activity): Unit
```

Called when the Activity calls [super.onStart()](https://developer.android.com/reference/kotlin/android/app/Activity#onStart()).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity):This value cannot be`null`. |

### onActivityStopped

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActivityStopped(activity: Activity): Unit
```

Called when the Activity calls [super.onStop()](https://developer.android.com/reference/kotlin/android/app/Activity#onStop()).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity):This value cannot be`null`. |
