Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppInteractionManager

```
class AppInteractionManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.AppInteractionManager](https://developer.android.com/reference/kotlin/android/app/AppInteractionManager#) |

Provides access to App Interaction access control APIs.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppInteractionManager#ACTION_MANAGE_APP_INTERACTION_ACCESS:kotlin.String` Activity action: Launches a UI that shows list of all interactors and provides management of App Interaction access of those interactors. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppInteractionManager#ACTION_MANAGE_INTERACTOR_ACCESS:kotlin.String` Activity action: Launches a UI that shows a list of all targets that the specified interactor package can access, and provides management of App Interaction access of those targets. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppInteractionManager#ACTION_MANAGE_INTERACTOR_TARGET_ACCESS:kotlin.String` Activity action: Launches a UI that provides management of App Interaction access of a specific interactor to a specific target. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppInteractionManager#ACTION_MANAGE_TARGET_ACCESS:kotlin.String` Activity action: Launches a UI that shows list of all interactors for a specific target and provides management of App Interaction access by those interactors. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppInteractionManager#EXTRA_INTERACTOR_PACKAGE_NAME:kotlin.String` Intent extra: A `https://developer.android.com/reference/kotlin/java/lang/String.html#` specifying the package name of the interactor when requesting or managing App Interaction access. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppInteractionManager#EXTRA_TARGET_PACKAGE_NAME:kotlin.String` Intent extra: A `String` specifying the target package name when managing App Interaction access. |
| --- | --- |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppInteractionManager#createSession(android.app.AppInteractionSession.CreateParams,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(params: https://developer.android.com/reference/kotlin/android/app/AppInteractionSession.CreateParams, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/app/AppInteractionSession!, https://developer.android.com/reference/kotlin/android/app/AppInteractionException!>)` Creates an app interaction session for the given params. |

## Constants

### ACTION_MANAGE_APP_INTERACTION_ACCESS

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MANAGE_APP_INTERACTION_ACCESS: String
```

Activity action: Launches a UI that shows list of all interactors and provides management of App Interaction access of those interactors.

Input: Nothing.

Output: Nothing.

 Value: "android.app.action.MANAGE_APP_INTERACTION_ACCESS"

### ACTION_MANAGE_INTERACTOR_ACCESS

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MANAGE_INTERACTOR_ACCESS: String
```

Activity action: Launches a UI that shows a list of all targets that the specified interactor package can access, and provides management of App Interaction access of those targets.

Input: `https://developer.android.com/reference/kotlin/android/app/AppInteractionManager#EXTRA_INTERACTOR_PACKAGE_NAME:kotlin.String` specifies the package whose access will be managed by the launched UI.

Output: Nothing.

 Value: "android.app.action.MANAGE_INTERACTOR_ACCESS"

### ACTION_MANAGE_INTERACTOR_TARGET_ACCESS

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MANAGE_INTERACTOR_TARGET_ACCESS: String
```

Activity action: Launches a UI that provides management of App Interaction access of a specific interactor to a specific target.

Input: `https://developer.android.com/reference/kotlin/android/app/AppInteractionManager#EXTRA_INTERACTOR_PACKAGE_NAME:kotlin.String` specifies the interactor package name.

Input: `https://developer.android.com/reference/kotlin/android/app/AppInteractionManager#EXTRA_TARGET_PACKAGE_NAME:kotlin.String` specifies the target package name.

Output: Nothing.

 Value: "android.app.action.MANAGE_INTERACTOR_TARGET_ACCESS"

### ACTION_MANAGE_TARGET_ACCESS

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_MANAGE_TARGET_ACCESS: String
```

Activity action: Launches a UI that shows list of all interactors for a specific target and provides management of App Interaction access by those interactors.

Input: `https://developer.android.com/reference/kotlin/android/app/AppInteractionManager#EXTRA_TARGET_PACKAGE_NAME:kotlin.String` specifies the package whose access will be managed by the launched UI.

Output: Nothing.

 Value: "android.app.action.MANAGE_TARGET_ACCESS"

### EXTRA_INTERACTOR_PACKAGE_NAME

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_INTERACTOR_PACKAGE_NAME: String
```

Intent extra: A `https://developer.android.com/reference/kotlin/java/lang/String.html#` specifying the package name of the interactor when requesting or managing App Interaction access.

 Value: "android.app.extra.INTERACTOR_PACKAGE_NAME"

### EXTRA_TARGET_PACKAGE_NAME

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_TARGET_PACKAGE_NAME: String
```

Intent extra: A `String` specifying the target package name when managing App Interaction access.

 Value: "android.app.extra.TARGET_PACKAGE_NAME"

## Public methods

### createSession

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createSession(
    params: AppInteractionSession.CreateParams, 
    executor: Executor, 
    callback: OutcomeReceiver<AppInteractionSession!, AppInteractionException!>
): Unit
```

Creates an app interaction session for the given params.

Example usage:

```kotlin
<code>AppInteractionSession.CreateParams createSessionParams =
      new AppInteractionSession.CreateParams.Builder()
          .setOnStartIntentSenderCallback(
              executor,
              intentSender -&gt; {
                  // The callback will be invoked if the session creation requires user consent
                  try {
                      context.startIntentSender(intentSender, null, 0, 0, 0);
                  } catch (IntentSender.SendIntentException e) {
                      // Handle exception
                  }
              }
          )
          .setTargetPackages(Arrays.asList("com.example.target1"))
          .build();
 
  appInteractionManager.createSession(createSessionParams, executor, callback);
  </code>
```

| Parameters ||
|---|---|
| `params` | [AppInteractionSession.CreateParams](https://developer.android.com/reference/kotlin/android/app/AppInteractionSession.CreateParams): The params to create the session. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor to run the callback on. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [AppInteractionSession](https://developer.android.com/reference/kotlin/android/app/AppInteractionSession)!, [AppInteractionException](https://developer.android.com/reference/kotlin/android/app/AppInteractionException)!\>: The callback to be called when the session is created or an error occurs. This value cannot be `null`. |
| --- | --- |
