# android.window

# android.window

Kotlin| [Java](https://developer.android.com/reference/android/window/package-summary "View this page in Java")
| --- | --- |

## Interfaces

| [OnBackAnimationCallback](https://developer.android.com/reference/kotlin/android/window/OnBackAnimationCallback) | Interface for applications to register back animation callbacks along their custom back handling. |
| --- | --- |
| [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback) | Callback allowing applications to handle back events in place of the system. |
| [OnBackInvokedDispatcher](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher) | Dispatcher to register [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback) instances for handling back invocations. |
| [SplashScreen](https://developer.android.com/reference/kotlin/android/window/SplashScreen) | The interface that apps use to talk to the splash screen. |
| --- | --- |

## Classes

| [BackEvent](https://developer.android.com/reference/kotlin/android/window/BackEvent) | Object used to report back gesture progress. |
| --- | --- |
| [InputTransferToken](https://developer.android.com/reference/kotlin/android/window/InputTransferToken) | A token that can be used to request focus on or to transfer touch gesture to a [SurfaceControlViewHost](https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.html#) or [android.view.SurfaceControl](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.html#) that has an input channel. |
| [SplashScreenView](https://developer.android.com/reference/kotlin/android/window/SplashScreenView) | The view which allows an activity to customize its splash screen exit animation. |
| [SurfaceSyncGroup](https://developer.android.com/reference/kotlin/android/window/SurfaceSyncGroup) | A way for data to be gathered so multiple surfaces can be synced. |
| --- | --- |
| [SystemOnBackInvokedCallbacks](https://developer.android.com/reference/kotlin/android/window/SystemOnBackInvokedCallbacks) | Utility class providing [OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback) s to override the default behavior when system back is invoked. |
| [TrustedPresentationThresholds](https://developer.android.com/reference/kotlin/android/window/TrustedPresentationThresholds) | Threshold values that are sent with android. |
