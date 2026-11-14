Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Instrumentation

Kotlin | [Java](Instrumentation.md)
| --- | --- |

```
open class Instrumentation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.Instrumentation](Instrumentation.md) |

| Known Direct Subclasses [InstrumentationTestRunner](../android.test/InstrumentationTestRunner.md), [LaunchPerformanceBase](../android.test/LaunchPerformanceBase.md) |---|---| | [InstrumentationTestRunner](../android.test/InstrumentationTestRunner.md) | An Instrumentation that runs various types of junit. | | [LaunchPerformanceBase](../android.test/LaunchPerformanceBase.md) | Base class for all launch performance Instrumentation classes. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Base class for implementing application instrumentation code. When running with instrumentation turned on, this class will be instantiated for you before any of the application code, allowing you to monitor all of the interaction the system has with the application. An Instrumentation implementation is described to the system through an AndroidManifest.xml's \<instrumentation\> tag.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor` Information about a particular kind of Intent that is being monitored. |
| | `https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityResult` Description of a Activity execution result to return to the original activity. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Instrumentation#REPORT_KEY_IDENTIFIER:kotlin.String` If included in the status or final bundle sent to an IInstrumentationWatcher, this key identifies the class that is writing the report. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/Instrumentation#REPORT_KEY_STREAMRESULT:kotlin.String` If included in the status or final bundle sent to an IInstrumentationWatcher, this key identifies a string which can simply be printed to the output stream. |

| Public constructors ||
|---|---|
| Instrumentation <br /> |

| Public methods ||
|---|---|
| open [TestLooperManager](../android.os/TestLooperManager.md)! | acquireLooperManager Takes control of the execution of messages on the specified looper until release is called. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addMonitor Add a new `https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor` that will be checked whenever an activity is started. |
| open [Instrumentation.ActivityMonitor](../android/app/Instrumentation.ActivityMonitor.md)! | addMonitor A convenience wrapper for addMonitor that creates an intent filter matching `https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor` for you and returns it. |
| --- | --- |
| open [Instrumentation.ActivityMonitor](../android/app/Instrumentation.ActivityMonitor.md)! | addMonitor A convenience wrapper for addMonitor that creates a class matching `https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor` for you and returns it. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addResults Report some results in the middle of instrumentation execution. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | callActivityOnCreate Perform calling of an activity's android. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | callActivityOnCreate Perform calling of an activity's android. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | callActivityOnDestroy <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | callActivityOnNewIntent Perform calling of an activity's android. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | callActivityOnNewIntent Same as callActivityOnNewIntent, but with an extra parameter for the ComponentCaller instance associated with the app that sent the intent. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | callActivityOnPause Perform calling of an activity's onPause method. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | callActivityOnPictureInPictureRequested Perform calling of an activity's onPictureInPictureRequested method. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | callActivityOnPostCreate Perform calling of an activity's android. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | callActivityOnPostCreate Perform calling of an activity's android. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | callActivityOnRestart Perform calling of an activity's onRestart method. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | callActivityOnRestoreInstanceState Perform calling of an activity's android. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | callActivityOnRestoreInstanceState Perform calling of an activity's android. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | callActivityOnResume Perform calling of an activity's onResume method. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | callActivityOnSaveInstanceState Perform calling of an activity's android. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | callActivityOnSaveInstanceState Perform calling of an activity's android. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | callActivityOnStart Perform calling of an activity's onStart method. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | callActivityOnStop Perform calling of an activity's onStop method. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | callActivityOnUserLeaving Perform calling of an activity's onUserLeaveHint method. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | callApplicationOnCreate Perform calling of the application's onCreate method. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | checkMonitorHit Test whether an existing `https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor` has been hit. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | endPerformanceSnapshot <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | finish Terminate instrumentation of the application. |
| --- | --- |
| open [Bundle](../android.os/Bundle.md)! | getAllocCounts Returns a bundle with the current results from the allocation counting. |
| open [Bundle](../android.os/Bundle.md)! | getBinderCounts Returns a bundle with the counts for various binder counts for this process. |
| open [ComponentName](../android.content/ComponentName.md)! | getComponentName Returns complete component name of this instrumentation. |
| --- | --- |
| open [Context](../android.content/Context.md)! | getContext Return the Context of this instrumentation's package. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getProcessName Return the name of the process this instrumentation is running in. |
| open [Context](../android.content/Context.md)! | getTargetContext Return a Context for the target application being instrumented. |
| --- | --- |
| open [UiAutomation](UiAutomation.md)! | getUiAutomation Gets the UiAutomation instance with no flags set. |
| open [UiAutomation](UiAutomation.md)! | getUiAutomation Gets the UiAutomation instance with flags set. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | invokeContextMenuAction Show the context menu for the currently focused view and executes a particular context menu item. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | invokeMenuActionSync Execute a particular menu item. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isProfiling Check whether this instrumentation was started with profiling enabled. |
| open [Activity](Activity.md)! | newActivity Perform instantiation of an Activity object. |
| --- | --- |
| open [Activity](Activity.md)! | newActivity Perform instantiation of the process's Activity object. |
| open [Application](Application.md)! | newApplication Perform instantiation of the process's Application object. |
| open static [Application](Application.md)! | newApplication Perform instantiation of the process's Application object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onCreate Called when the instrumentation is starting, before any application code has been loaded. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onDestroy Called when the instrumented application is stopping, after all of the normal application cleanup has occurred. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onException This is called whenever the system captures an unhandled exception that was thrown by the application. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onStart Method where the instrumentation thread enters execution. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | removeMonitor Remove an `https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor` that was previously added with #addMonitor. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | resetInTouchMode Resets the setInTouchMode to the device default. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | runOnMainSync Execute a call on the application's main thread, blocking until it is complete. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendCharacterSync Sends up and down key events with the given key code to the currently focused window, and waits for it to be processed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendKeyDownUpSync Sends up and down key events with the given key code to the currently focused window, and waits for it to be processed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendKeySync Sends a key event to the currently focused window, and waits for it to be processed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendPointerSync Dispatches a pointer event into a window owned by the instrumented application, and waits for it to be processed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendStatus Provide a status report about the application. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendStringSync Sends the key events that result in the given text being typed into the currently focused window, and waits for it to be processed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendTrackballEventSync Dispatches a trackball event into the currently focused window, and waits for it to be processed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAutomaticPerformanceSnapshots <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setInTouchMode Force the global system in or out of touch mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | start Create and start a new thread in which to run instrumentation. |
| open [Activity](Activity.md)! | startActivitySync Start a new activity and wait for it to begin running before returning. |
| --- | --- |
| open [Activity](Activity.md) | startActivitySync Start a new activity and wait for it to begin running before returning. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | startAllocCounting <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | startPerformanceSnapshot <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | startProfiling This method will start profiling if isProfiling() returns true. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | stopAllocCounting <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | stopProfiling Stops profiling if isProfiling() returns true. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | waitForIdle Schedule a callback for when the application's main thread goes idle (has no more events to process). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | waitForIdleSync Synchronously wait for the application to be idle. |
| open [Activity](Activity.md)! | waitForMonitor Wait for an existing `https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor` to be hit. |
| --- | --- |
| open [Activity](Activity.md)! | waitForMonitorWithTimeout Wait for an existing `https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor` to be hit till the timeout expires. |

## Constants

### REPORT_KEY_IDENTIFIER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REPORT_KEY_IDENTIFIER: String
```

If included in the status or final bundle sent to an IInstrumentationWatcher, this key identifies the class that is writing the report. This can be used to provide more structured logging or reporting capabilities in the IInstrumentationWatcher.

 Value: "id"

### REPORT_KEY_STREAMRESULT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REPORT_KEY_STREAMRESULT: String
```

If included in the status or final bundle sent to an IInstrumentationWatcher, this key identifies a string which can simply be printed to the output stream. Using these streams provides a "pretty printer" version of the status \& final packets. Any bundles including this key should also include the complete set of raw key/value pairs, so that the instrumentation can also be launched, and results collected, by an automated system.

 Value: "stream"

## Public constructors

### Instrumentation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Instrumentation()
```

## Public methods

### acquireLooperManager

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun acquireLooperManager(looper: Looper!): TestLooperManager!
```

Takes control of the execution of messages on the specified looper until release is called.

### addMonitor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addMonitor(monitor: Instrumentation.ActivityMonitor!): Unit
```

Add a new `https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor` that will be checked whenever an activity is started. The monitor is added after any existing ones; the monitor will be hit only if none of the existing monitors can themselves handle the Intent.

| Parameters ||
|---|---|
| `monitor` | [Instrumentation.ActivityMonitor](../android/app/Instrumentation.ActivityMonitor.md)!: The new ActivityMonitor to see. |

**See Also**

- addMonitor
- checkMonitorHit

### addMonitor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addMonitor(
    filter: IntentFilter!, 
    result: Instrumentation.ActivityResult!, 
    block: Boolean
): Instrumentation.ActivityMonitor!
```

A convenience wrapper for addMonitor that creates an intent filter matching `https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor` for you and returns it.

| Parameters ||
|---|---|
| `filter` | [IntentFilter](../android.content/IntentFilter.md)!: The set of intents this monitor is responsible for. |
| `result` | [Instrumentation.ActivityResult](../android/app/Instrumentation.ActivityResult.md)!: A canned result to return if the monitor is hit; can be null. |
| `block` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Controls whether the monitor should block the activity start (returning its canned result) or let the call proceed. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor!` | The newly created and added activity monitor. |

**See Also**

- addMonitor
- checkMonitorHit

### addMonitor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addMonitor(
    cls: String!, 
    result: Instrumentation.ActivityResult!, 
    block: Boolean
): Instrumentation.ActivityMonitor!
```

A convenience wrapper for addMonitor that creates a class matching `https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor` for you and returns it.

| Parameters ||
|---|---|
| `cls` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The activity class this monitor is responsible for. |
| `result` | [Instrumentation.ActivityResult](../android/app/Instrumentation.ActivityResult.md)!: A canned result to return if the monitor is hit; can be null. |
| `block` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Controls whether the monitor should block the activity start (returning its canned result) or let the call proceed. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor!` | The newly created and added activity monitor. |

**See Also**

- addMonitor
- checkMonitorHit

### addResults

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addResults(results: Bundle!): Unit
```

Report some results in the middle of instrumentation execution. Later results (including those provided by finish) will be combined with android.os.Bundle#putAll.

### callActivityOnCreate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun callActivityOnCreate(
    activity: Activity!, 
    icicle: Bundle!
): Unit
```

Perform calling of an activity's android.app.Activity#onCreate method. The default implementation simply calls through to that method.

| Parameters ||
|---|---|
| `activity` | [Activity](Activity.md)!: The activity being created. |
| `icicle` | [Bundle](../android.os/Bundle.md)!: The previously frozen state (or null) to pass through to onCreate(). |

### callActivityOnCreate

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun callActivityOnCreate(
    activity: Activity!, 
    icicle: Bundle!, 
    persistentState: PersistableBundle!
): Unit
```

Perform calling of an activity's android.app.Activity#onCreate method. The default implementation simply calls through to that method.

| Parameters ||
|---|---|
| `activity` | [Activity](Activity.md)!: The activity being created. |
| `icicle` | [Bundle](../android.os/Bundle.md)!: The previously frozen state (or null) to pass through to |
| `persistentState` | [PersistableBundle](../android.os/PersistableBundle.md)!: The previously persisted state (or null) |
| --- | --- |

### callActivityOnDestroy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun callActivityOnDestroy(activity: Activity!): Unit
```

### callActivityOnNewIntent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun callActivityOnNewIntent(
    activity: Activity!, 
    intent: Intent!
): Unit
```

Perform calling of an activity's android.app.Activity#onNewIntent method. The default implementation simply calls through to that method.

| Parameters ||
|---|---|
| `activity` | [Activity](Activity.md)!: The activity receiving a new Intent. |
| `intent` | [Intent](../android.content/Intent.md)!: The new intent being received. |

### callActivityOnNewIntent

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun callActivityOnNewIntent(
    activity: Activity, 
    intent: Intent, 
    caller: ComponentCaller
): Unit
```

Same as callActivityOnNewIntent, but with an extra parameter for the ComponentCaller instance associated with the app that sent the intent.

| Parameters ||
|---|---|
| `activity` | [Activity](Activity.md): The activity receiving a new Intent. This value cannot be `null`. |
| `intent` | [Intent](../android.content/Intent.md): The new intent being received. This value cannot be `null`. |
| `caller` | [ComponentCaller](ComponentCaller.md): The ComponentCaller instance that launched the activity with the new intent. This value cannot be `null`. |
| --- | --- |

### callActivityOnPause

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun callActivityOnPause(activity: Activity!): Unit
```

Perform calling of an activity's onPause method. The default implementation simply calls through to that method.

| Parameters ||
|---|---|
| `activity` | [Activity](Activity.md)!: The activity being paused. |

### callActivityOnPictureInPictureRequested

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun callActivityOnPictureInPictureRequested(activity: Activity): Unit
```

Perform calling of an activity's onPictureInPictureRequested method. The default implementation simply calls through to that method.

| Parameters ||
|---|---|
| `activity` | [Activity](Activity.md): The activity being notified that picture-in-picture is being requested. This value cannot be `null`. |

### callActivityOnPostCreate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun callActivityOnPostCreate(
    activity: Activity, 
    savedInstanceState: Bundle?
): Unit
```

Perform calling of an activity's android.app.Activity#onPostCreate method. The default implementation simply calls through to that method.

| Parameters ||
|---|---|
| `activity` | [Activity](Activity.md): The activity being created. This value cannot be `null`. |
| `savedInstanceState` | [Bundle](../android.os/Bundle.md)?: The previously saved state (or null) to pass through to onPostCreate(). |

### callActivityOnPostCreate

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun callActivityOnPostCreate(
    activity: Activity, 
    savedInstanceState: Bundle?, 
    persistentState: PersistableBundle?
): Unit
```

Perform calling of an activity's android.app.Activity#onPostCreate method. The default implementation simply calls through to that method.

| Parameters ||
|---|---|
| `activity` | [Activity](Activity.md): The activity being created. This value cannot be `null`. |
| `savedInstanceState` | [Bundle](../android.os/Bundle.md)?: The previously frozen state (or null) to pass through to onPostCreate(). |
| `persistentState` | [PersistableBundle](../android.os/PersistableBundle.md)?: The previously persisted state (or null) |
| --- | --- |

### callActivityOnRestart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun callActivityOnRestart(activity: Activity!): Unit
```

Perform calling of an activity's onRestart method. The default implementation simply calls through to that method.

| Parameters ||
|---|---|
| `activity` | [Activity](Activity.md)!: The activity being restarted. |

### callActivityOnRestoreInstanceState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun callActivityOnRestoreInstanceState(
    activity: Activity, 
    savedInstanceState: Bundle
): Unit
```

Perform calling of an activity's android.app.Activity#onRestoreInstanceState method. The default implementation simply calls through to that method.

| Parameters ||
|---|---|
| `activity` | [Activity](Activity.md): The activity being restored. This value cannot be `null`. |
| `savedInstanceState` | [Bundle](../android.os/Bundle.md): The previously saved state being restored. This value cannot be `null`. |

### callActivityOnRestoreInstanceState

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun callActivityOnRestoreInstanceState(
    activity: Activity, 
    savedInstanceState: Bundle?, 
    persistentState: PersistableBundle?
): Unit
```

Perform calling of an activity's android.app.Activity#onRestoreInstanceState method. The default implementation simply calls through to that method.

| Parameters ||
|---|---|
| `activity` | [Activity](Activity.md): The activity being restored. This value cannot be `null`. |
| `savedInstanceState` | [Bundle](../android.os/Bundle.md)?: The previously saved state being restored (or null). |
| `persistentState` | [PersistableBundle](../android.os/PersistableBundle.md)?: The previously persisted state (or null) |
| --- | --- |

### callActivityOnResume

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun callActivityOnResume(activity: Activity!): Unit
```

Perform calling of an activity's onResume method. The default implementation simply calls through to that method.

| Parameters ||
|---|---|
| `activity` | [Activity](Activity.md)!: The activity being resumed. |

### callActivityOnSaveInstanceState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun callActivityOnSaveInstanceState(
    activity: Activity, 
    outState: Bundle
): Unit
```

Perform calling of an activity's android.app.Activity#onSaveInstanceState method. The default implementation simply calls through to that method.

| Parameters ||
|---|---|
| `activity` | [Activity](Activity.md): The activity being saved. This value cannot be `null`. |
| `outState` | [Bundle](../android.os/Bundle.md): The bundle to pass to the call. This value cannot be `null`. |

### callActivityOnSaveInstanceState

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun callActivityOnSaveInstanceState(
    activity: Activity, 
    outState: Bundle, 
    outPersistentState: PersistableBundle
): Unit
```

Perform calling of an activity's android.app.Activity#onSaveInstanceState method. The default implementation simply calls through to that method.

| Parameters ||
|---|---|
| `activity` | [Activity](Activity.md): The activity being saved. This value cannot be `null`. |
| `outState` | [Bundle](../android.os/Bundle.md): The bundle to pass to the call. This value cannot be `null`. |
| `outPersistentState` | [PersistableBundle](../android.os/PersistableBundle.md): The persistent bundle to pass to the call. This value cannot be `null`. |
| --- | --- |

### callActivityOnStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun callActivityOnStart(activity: Activity!): Unit
```

Perform calling of an activity's onStart method. The default implementation simply calls through to that method.

| Parameters ||
|---|---|
| `activity` | [Activity](Activity.md)!: The activity being started. |

### callActivityOnStop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun callActivityOnStop(activity: Activity!): Unit
```

Perform calling of an activity's onStop method. The default implementation simply calls through to that method.

| Parameters ||
|---|---|
| `activity` | [Activity](Activity.md)!: The activity being stopped. |

### callActivityOnUserLeaving

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun callActivityOnUserLeaving(activity: Activity!): Unit
```

Perform calling of an activity's onUserLeaveHint method. The default implementation simply calls through to that method.

| Parameters ||
|---|---|
| `activity` | [Activity](Activity.md)!: The activity being notified that the user has navigated away |

### callApplicationOnCreate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun callApplicationOnCreate(app: Application!): Unit
```

Perform calling of the application's onCreate method. The default implementation simply calls through to that method.

Note: This method will be called immediately after onCreate. Often instrumentation tests start their test thread in onCreate(); you need to be careful of races between these. (Well between it and everything else, but let's start here.)

| Parameters ||
|---|---|
| `app` | [Application](Application.md)!: The application being created. |

### checkMonitorHit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun checkMonitorHit(
    monitor: Instrumentation.ActivityMonitor!, 
    minHits: Int
): Boolean
```

Test whether an existing `https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor` has been hit. If the monitor has been hit at least minHits times, then it will be removed from the activity monitor list and true returned. Otherwise it is left as-is and false is returned.

| Parameters ||
|---|---|
| `monitor` | [Instrumentation.ActivityMonitor](../android/app/Instrumentation.ActivityMonitor.md)!: The ActivityMonitor to check. |
| `minHits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The minimum number of hits required. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the hit count has been reached, else false. |

**See Also**

### endPerformanceSnapshot

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun endPerformanceSnapshot(): Unit
```

### finish

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun finish(
    resultCode: Int, 
    results: Bundle!
): Unit
```

Terminate instrumentation of the application. This will cause the application process to exit, removing this instrumentation from the next time the application is started. If multiple processes are currently running for this instrumentation, all of those processes will be killed.

| Parameters ||
|---|---|
| `resultCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Overall success/failure of instrumentation. |
| `results` | [Bundle](../android.os/Bundle.md)!: Any results to send back to the code that started the instrumentation. |

### getAllocCounts

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAllocCounts(): Bundle!
```

Returns a bundle with the current results from the allocation counting.

### getBinderCounts

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBinderCounts(): Bundle!
```

Returns a bundle with the counts for various binder counts for this process. Currently the only two that are reported are the number of send and the number of received transactions.

### getComponentName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getComponentName(): ComponentName!
```

Returns complete component name of this instrumentation.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!` | Returns the complete component name for this instrumentation. |

### getContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getContext(): Context!
```

Return the Context of this instrumentation's package. Note that this is often different than the Context of the application being instrumentated, since the instrumentation code often lives is a different package than that of the application it is running against. See getTargetContext to retrieve a Context for the target application.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Context.html#!` | The instrumentation's package context. |

**See Also**

- getTargetContext

### getProcessName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getProcessName(): String!
```

Return the name of the process this instrumentation is running in. Note this should only be used for testing and debugging. If you are thinking about using this to, for example, conditionalize what is initialized in an Application class, it is strongly recommended to instead use lazy initialization (such as a getter for the state that only creates it when requested). This can greatly reduce the work your process does when created for secondary things, such as to receive a broadcast.

### getTargetContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTargetContext(): Context!
```

Return a Context for the target application being instrumented. Note that this is often different than the Context of the instrumentation code, since the instrumentation code often lives is a different package than that of the application it is running against. See getContext to retrieve a Context for the instrumentation code.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Context.html#!` | A Context in the target application. |

**See Also**

- getContext

### getUiAutomation

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUiAutomation(): UiAutomation!
```

Gets the UiAutomation instance with no flags set.

**Note:** The APIs exposed via the returned UiAutomation work across application boundaries while the APIs exposed by the instrumentation do not. For example, sendPointerSync will not allow you to inject the event in an app different from the instrumentation target, while injectInputEvent will work regardless of the current application.

A typical test case should be using either the UiAutomation or Instrumentation APIs. Using both APIs at the same time is not a mistake by itself but a client has to be aware of the APIs limitations.

Equivalent to `getUiAutomation(0)`. If a UiAutomation exists with different flags, the flags on that instance will be changed, and then it will be returned.

Compatibility mode: This method is infallible for apps targeted for `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` and earlier versions; for apps targeted for later versions, it will return null if UiAutomation fails to connect. The caller can check the return value and retry on error.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/UiAutomation!` | The UI automation instance. |

**See Also**

- UiAutomation

### getUiAutomation

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUiAutomation(flags: Int): UiAutomation!
```

Gets the UiAutomation instance with flags set.

**Note:** The APIs exposed via the returned UiAutomation work across application boundaries while the APIs exposed by the instrumentation do not. For example, sendPointerSync will not allow you to inject the event in an app different from the instrumentation target, while injectInputEvent will work regardless of the current application.

A typical test case should be using either the UiAutomation or Instrumentation APIs. Using both APIs at the same time is not a mistake by itself but a client has to be aware of the APIs limitations.

If a UiAutomation exists with different flags, the flags on that instance will be changed, and then it will be returned.

Compatibility mode: This method is infallible for apps targeted for `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` and earlier versions; for apps targeted for later versions, it will return null if UiAutomation fails to connect. The caller can check the return value and retry on error.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The flags to be passed to the UiAutomation, for example `https://developer.android.com/reference/kotlin/android/app/UiAutomation#FLAG_DONT_SUPPRESS_ACCESSIBILITY_SERVICES:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/UiAutomation#FLAG_DONT_USE_ACCESSIBILITY:kotlin.Int`. Value is one of the following: - 0 - `https://developer.android.com/reference/kotlin/android/app/UiAutomation#FLAG_DONT_SUPPRESS_ACCESSIBILITY_SERVICES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/UiAutomation#FLAG_DONT_USE_ACCESSIBILITY:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/UiAutomation!` | The UI automation instance. |

**See Also**

- UiAutomation

### invokeContextMenuAction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun invokeContextMenuAction(
    targetActivity: Activity!, 
    id: Int, 
    flag: Int
): Boolean
```

Show the context menu for the currently focused view and executes a particular context menu item.

| Parameters ||
|---|---|
| `targetActivity` | [Activity](Activity.md)!: The activity in question. |
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The identifier associated with the context menu item. |
| `flag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags, if any. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the invocation was successful (for example, it could be false if item is disabled). |

### invokeMenuActionSync

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun invokeMenuActionSync(
    targetActivity: Activity!, 
    id: Int, 
    flag: Int
): Boolean
```

Execute a particular menu item.

| Parameters ||
|---|---|
| `targetActivity` | [Activity](Activity.md)!: The activity in question. |
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The identifier associated with the menu item. |
| `flag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags, if any. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the invocation was successful (for example, it could be false if item is disabled). |

### isProfiling

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isProfiling(): Boolean
```

Check whether this instrumentation was started with profiling enabled.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if profiling was enabled when starting, else false. |

### newActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun newActivity(
    clazz: Class<*>!, 
    context: Context!, 
    token: IBinder!, 
    application: Application!, 
    intent: Intent!, 
    info: ActivityInfo!, 
    title: CharSequence!, 
    parent: Activity!, 
    id: String!, 
    lastNonConfigurationInstance: Any!
): Activity!
```

Perform instantiation of an Activity object. This method is intended for use with unit tests, such as android.test.ActivityUnitTestCase. The activity will be useable locally but will be missing some of the linkages necessary for use within the system.

| Parameters ||
|---|---|
| `clazz` | [Class](../java.lang/Class.md)\<\*\>!: The Class of the desired Activity |
| `context` | [Context](../android.content/Context.md)!: The base context for the activity to use |
| `token` | [IBinder](../android.os/IBinder.md)!: The token for this activity to communicate with |
| --- | --- |
| `application` | [Application](Application.md)!: The application object (if any) |
| `intent` | [Intent](../android.content/Intent.md)!: The intent that started this Activity |
| `info` | [ActivityInfo](../android.content.pm/ActivityInfo.md)!: ActivityInfo from the manifest |
| --- | --- |
| `title` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The title, typically retrieved from the ActivityInfo record |
| `parent` | [Activity](Activity.md)!: The parent Activity (if any) |
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The embedded Id (if any) |
| --- | --- |
| `lastNonConfigurationInstance` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: Arbitrary object that will be available via getLastNonConfigurationInstance. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/Activity!` | Returns the instantiated activity |

| Exceptions ||
|---|---|
| `java.lang.IllegalAccessException` | |
| `java.lang.InstantiationException` | |

### newActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun newActivity(
    cl: ClassLoader!, 
    className: String!, 
    intent: Intent!
): Activity!
```

Perform instantiation of the process's Activity object. The default implementation provides the normal system behavior.

| Parameters ||
|---|---|
| `cl` | [ClassLoader](../java.lang/ClassLoader.md)!: The ClassLoader with which to instantiate the object. |
| `className` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the class implementing the Activity object. |
| `intent` | [Intent](../android.content/Intent.md)!: The Intent object that specified the activity class being instantiated. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/Activity!` | The newly instantiated Activity object. |

### newApplication

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun newApplication(
    cl: ClassLoader!, 
    className: String!, 
    context: Context!
): Application!
```

Perform instantiation of the process's Application object. The default implementation provides the normal system behavior.

| Parameters ||
|---|---|
| `cl` | [ClassLoader](../java.lang/ClassLoader.md)!: The ClassLoader with which to instantiate the object. |
| `className` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the class implementing the Application object. |
| `context` | [Context](../android.content/Context.md)!: The context to initialize the application with |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/Application!` | The newly instantiated Application object. |

### newApplication

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun newApplication(
    clazz: Class<*>!, 
    context: Context!
): Application!
```

Perform instantiation of the process's Application object. The default implementation provides the normal system behavior.

| Parameters ||
|---|---|
| `clazz` | [Class](../java.lang/Class.md)\<\*\>!: The class used to create an Application object from. |
| `context` | [Context](../android.content/Context.md)!: The context to initialize the application with |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/Application!` | The newly instantiated Application object. |

### onCreate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreate(arguments: Bundle!): Unit
```

Called when the instrumentation is starting, before any application code has been loaded. Usually this will be implemented to simply call start to begin the instrumentation thread, which will then continue execution in onStart.

If you do not need your own thread -- that is you are writing your instrumentation to be completely asynchronous (returning to the event loop so that the application can run), you can simply begin your instrumentation here, for example call android.content.Context#startActivity to begin the appropriate first activity of the application.

| Parameters ||
|---|---|
| `arguments` | [Bundle](../android.os/Bundle.md)!: Any additional arguments that were supplied when the instrumentation was started. |

### onDestroy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDestroy(): Unit
```

Called when the instrumented application is stopping, after all of the normal application cleanup has occurred.

### onException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onException(
    obj: Any!, 
    e: Throwable!
): Boolean
```

This is called whenever the system captures an unhandled exception that was thrown by the application. The default implementation simply returns false, allowing normal system handling of the exception to take place.

| Parameters ||
|---|---|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The client object that generated the exception. May be an Application, Activity, BroadcastReceiver, Service, or null. |
| `e` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: The exception that was thrown. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | To allow normal system exception process to occur, return false. If true is returned, the system will proceed as if the exception didn't happen. |

### onStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onStart(): Unit
```

Method where the instrumentation thread enters execution. This allows you to run your instrumentation code in a separate thread than the application, so that it can perform blocking operation such as sendKeySync or #startActivitySync.

You will typically want to call finish() when this function is done, to end your instrumentation.

### removeMonitor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeMonitor(monitor: Instrumentation.ActivityMonitor!): Unit
```

Remove an `https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor` that was previously added with #addMonitor.

| Parameters ||
|---|---|
| `monitor` | [Instrumentation.ActivityMonitor](../android/app/Instrumentation.ActivityMonitor.md)!: The monitor to remove. |

**See Also**

### resetInTouchMode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun resetInTouchMode(): Unit
```

Resets the setInTouchMode to the device default.

### runOnMainSync

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun runOnMainSync(runner: Runnable!): Unit
```

Execute a call on the application's main thread, blocking until it is complete. Useful for doing things that are not thread-safe, such as looking at or modifying the view hierarchy.

| Parameters ||
|---|---|
| `runner` | [Runnable](../java.lang/Runnable.md)!: The code to run on the main thread. |

### sendCharacterSync

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendCharacterSync(keyCode: Int): Unit
```

Sends up and down key events with the given key code to the currently focused window, and waits for it to be processed.

Equivalent to sendKeyDownUpSync.

| Parameters ||
|---|---|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The key code of the character to send. |

**See Also**

- sendKeySync

### sendKeyDownUpSync

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendKeyDownUpSync(keyCode: Int): Unit
```

Sends up and down key events with the given key code to the currently focused window, and waits for it to be processed.

| Parameters ||
|---|---|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The key code for the events to send. |

**See Also**

- sendKeySync

### sendKeySync

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendKeySync(event: KeyEvent!): Unit
```

Sends a key event to the currently focused window, and waits for it to be processed.

This method blocks until the recipient has finished handling the event. Note that the recipient may *not* have completely finished reacting from the event when this method returns. For example, it may still be in the process of updating its display or UI contents upon reacting to the injected event.

| Parameters ||
|---|---|
| `event` | [KeyEvent](../android.view/KeyEvent.md)!: The event to send to the current focus. |

### sendPointerSync

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendPointerSync(event: MotionEvent!): Unit
```

Dispatches a pointer event into a window owned by the instrumented application, and waits for it to be processed.

If the motion event being injected is targeted at a window that is not owned by the instrumented application, the input injection will fail. See getUiAutomation for injecting events into all windows.

This method blocks until the recipient has finished handling the event. Note that the recipient may *not* have completely finished reacting from the event when this method returns. For example, it may still be in the process of updating its display or UI contents upon reacting to the injected event.

| Parameters ||
|---|---|
| `event` | [MotionEvent](../android.view/MotionEvent.md)!: A motion event describing the pointer action. (As noted in obtain, be sure to use uptimeMillis as the timebase. |

### sendStatus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendStatus(
    resultCode: Int, 
    results: Bundle!
): Unit
```

Provide a status report about the application.

| Parameters ||
|---|---|
| `resultCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Current success/failure of instrumentation. |
| `results` | [Bundle](../android.os/Bundle.md)!: Any results to send back to the code that started the instrumentation. |

### sendStringSync

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendStringSync(text: String!): Unit
```

Sends the key events that result in the given text being typed into the currently focused window, and waits for it to be processed.

| Parameters ||
|---|---|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The text to be sent. |

**See Also**

- sendKeySync

### sendTrackballEventSync

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendTrackballEventSync(event: MotionEvent!): Unit
```

Dispatches a trackball event into the currently focused window, and waits for it to be processed.

This method blocks until the recipient has finished handling the event. Note that the recipient may *not* have completely finished reacting from the event when this method returns. For example, it may still be in the process of updating its display or UI contents upon reacting to the injected event.

| Parameters ||
|---|---|
| `event` | [MotionEvent](../android.view/MotionEvent.md)!: A motion event describing the trackball action. (As noted in obtain, be sure to use uptimeMillis as the timebase. |

### setAutomaticPerformanceSnapshots

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAutomaticPerformanceSnapshots(): Unit
```

### setInTouchMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setInTouchMode(inTouch: Boolean): Unit
```

Force the global system in or out of touch mode. This can be used if your instrumentation relies on the UI being in one more or the other when it starts.

**Note:** Starting from Android `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, this method will only take effect if the instrumentation was sourced from a process with `MODIFY_TOUCH_MODE_STATE` internal permission granted (shell already have it).

| Parameters ||
|---|---|
| `inTouch` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Set to true to be in touch mode, false to be in focus mode. |

### start

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun start(): Unit
```

Create and start a new thread in which to run instrumentation. This new thread will call to onStart where you can implement the instrumentation.

### startActivitySync

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startActivitySync(intent: Intent!): Activity!
```

Start a new activity and wait for it to begin running before returning. In addition to being synchronous, this method as some semantic differences from the standard android.content.Context#startActivity call: the activity component is resolved before talking with the activity manager (its class name is specified in the Intent that this method ultimately starts), and it does not allow you to start activities that run in a different process. In addition, if the given Intent resolves to multiple activities, instead of displaying a dialog for the user to select an activity, an exception will be thrown.

The function returns as soon as the activity goes idle following the call to its android.app.Activity#onCreate. Generally this means it has gone through the full initialization including onResume and drawn and displayed its initial window.

| Parameters ||
|---|---|
| `intent` | [Intent](../android.content/Intent.md)!: Description of the activity to start. |

**See Also**

- startActivitySync

### startActivitySync

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startActivitySync(
    intent: Intent, 
    options: Bundle?
): Activity
```

Start a new activity and wait for it to begin running before returning. In addition to being synchronous, this method as some semantic differences from the standard android.content.Context#startActivity call: the activity component is resolved before talking with the activity manager (its class name is specified in the Intent that this method ultimately starts), and it does not allow you to start activities that run in a different process. In addition, if the given Intent resolves to multiple activities, instead of displaying a dialog for the user to select an activity, an exception will be thrown.

The function returns as soon as the activity goes idle following the call to its android.app.Activity#onCreate. Generally this means it has gone through the full initialization including onResume and drawn and displayed its initial window.

| Parameters ||
|---|---|
| `intent` | [Intent](../android.content/Intent.md): Description of the activity to start. This value cannot be `null`. |
| `options` | [Bundle](../android.os/Bundle.md)?: Additional options for how the Activity should be started. May be null if there are no options. See ActivityOptions for how to build the Bundle supplied here; there are no supported definitions for building it manually. |

| Return ||
|---|---|
| Activity | This value cannot be `null`. |

**See Also**

- startActivity

### startAllocCounting

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startAllocCounting(): Unit
```

**Deprecated:** *Deprecated in Java.*

### startPerformanceSnapshot

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startPerformanceSnapshot(): Unit
```

### startProfiling

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startProfiling(): Unit
```

This method will start profiling if isProfiling() returns true. You should only call this method if you set the handleProfiling attribute in the manifest file for this Instrumentation to true.

### stopAllocCounting

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun stopAllocCounting(): Unit
```

**Deprecated:** *Deprecated in Java.*

### stopProfiling

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun stopProfiling(): Unit
```

Stops profiling if isProfiling() returns true.

### waitForIdle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun waitForIdle(recipient: Runnable!): Unit
```

Schedule a callback for when the application's main thread goes idle (has no more events to process).

| Parameters ||
|---|---|
| `recipient` | [Runnable](../java.lang/Runnable.md)!: Called the next time the thread's message queue is idle. |

### waitForIdleSync

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun waitForIdleSync(): Unit
```

Synchronously wait for the application to be idle. Can not be called from the main application thread -- use start to execute instrumentation in its own thread.

### waitForMonitor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun waitForMonitor(monitor: Instrumentation.ActivityMonitor!): Activity!
```

Wait for an existing `https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor` to be hit. Once the monitor has been hit, it is removed from the activity monitor list and the first created Activity object that matched it is returned.

| Parameters ||
|---|---|
| `monitor` | [Instrumentation.ActivityMonitor](../android/app/Instrumentation.ActivityMonitor.md)!: The ActivityMonitor to wait for. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/Activity!` | The Activity object that matched the monitor. |

### waitForMonitorWithTimeout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun waitForMonitorWithTimeout(
    monitor: Instrumentation.ActivityMonitor!, 
    timeOut: Long
): Activity!
```

Wait for an existing `https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor` to be hit till the timeout expires. Once the monitor has been hit, it is removed from the activity monitor list and the first created Activity object that matched it is returned. If the timeout expires, a null object is returned.

| Parameters ||
|---|---|
| `monitor` | [Instrumentation.ActivityMonitor](../android/app/Instrumentation.ActivityMonitor.md)!: The ActivityMonitor to wait for. |
| `timeOut` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The timeout value in milliseconds. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/Activity!` | The Activity object that matched the monitor. |
