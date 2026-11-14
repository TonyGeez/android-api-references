# android.window

# android.window

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [OnBackAnimationCallback](OnBackAnimationCallback.md) | Interface for applications to register back animation callbacks along their custom back handling. |
| --- | --- |
| [OnBackInvokedCallback](OnBackInvokedCallback.md) | Callback allowing applications to handle back events in place of the system. |
| [OnBackInvokedDispatcher](OnBackInvokedDispatcher.md) | Dispatcher to register [OnBackInvokedCallback](OnBackInvokedCallback.md) instances for handling back invocations. |
| [SplashScreen](SplashScreen.md) | The interface that apps use to talk to the splash screen. |
| --- | --- |

## Classes

| [BackEvent](BackEvent.md) | Object used to report back gesture progress. |
| --- | --- |
| [InputTransferToken](InputTransferToken.md) | A token that can be used to request focus on or to transfer touch gesture to a [SurfaceControlViewHost](../android.view/SurfaceControlViewHost.md) or [android.view.SurfaceControl](../android.view/SurfaceControl.md) that has an input channel. |
| [SplashScreenView](SplashScreenView.md) | The view which allows an activity to customize its splash screen exit animation. |
| [SurfaceSyncGroup](SurfaceSyncGroup.md) | A way for data to be gathered so multiple surfaces can be synced. |
| --- | --- |
| [SystemOnBackInvokedCallbacks](SystemOnBackInvokedCallbacks.md) | Utility class providing [OnBackInvokedCallback](OnBackInvokedCallback.md) s to override the default behavior when system back is invoked. |
| [TrustedPresentationThresholds](TrustedPresentationThresholds.md) | Threshold values that are sent with android. |
