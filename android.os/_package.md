# android.os

Kotlin | [Java](../android/os/_package.md)
| --- | --- |

## Interfaces

| [OnCancelListener](../android/os/CancellationSignal.OnCancelListener.md) | Listens for cancellation. |
| --- | --- |
| [ProgressListener](../android/os/FileUtils.ProgressListener.md) | Listener that is called periodically as progress is made. |
| [Callback](../android/os/Handler.Callback.md) | Callback interface you can use when instantiating a Handler to avoid having to implement your own subclass of Handler. |
| [IBinder](../android/os/IBinder.md) | Base interface for a remotable object, the core part of a lightweight remote procedure call mechanism designed for high performance when performing in-process and cross-process calls. |
| --- | --- |
| [IInterface](../android/os/IInterface.md) | Base class for Binder interfaces. |
| [IdleHandler](../android/os/MessageQueue.IdleHandler.md) | Callback interface for discovering when a thread is going to block waiting for more messages. |
| [OnFileDescriptorEventListener](../android/os/MessageQueue.OnFileDescriptorEventListener.md) | A listener which is invoked when file descriptor related events occur. |
| --- | --- |
| [OutcomeReceiver](../android/os/OutcomeReceiver.md) | Callback interface intended for use when an asynchronous operation may result in a failure. |
| [Parcelable](../android/os/Parcelable.md) | Interface for classes whose instances can be written to and restored from a `https://developer.android.com/reference/kotlin/android/os/Parcel`. |
| [OnCloseListener](../android/os/ParcelFileDescriptor.OnCloseListener.md) | Callback indicating that a ParcelFileDescriptor has been closed. |
| --- | --- |
| [OnThermalHeadroomChangedListener](../android/os/PowerManager.OnThermalHeadroomChangedListener.md) | Listener passed to android. |
| [OnThermalStatusChangedListener](../android/os/PowerManager.OnThermalStatusChangedListener.md) | Listener passed to android. |
| [WakeLockStateListener](../android/os/PowerManager.WakeLockStateListener.md) | A listener interface to get notified when the wakelock is enabled/disabled. |
| --- | --- |
| [ProgressListener](../android/os/RecoverySystem.ProgressListener.md) | Interface definition for a callback to be invoked regularly as verification proceeds. |
| [OnThreadViolationListener](../android/os/StrictMode.OnThreadViolationListener.md) | When #`https://developer.android.com/reference/kotlin/android/os/StrictMode.ThreadPolicy.Builder#penaltyListener(java.util.concurrent.Executor,%20android.os.StrictMode.OnThreadViolationListener)` is enabled, the listener is called on the provided executor when a Thread violation occurs. |
| [OnVmViolationListener](../android/os/StrictMode.OnVmViolationListener.md) | When #`https://developer.android.com/reference/kotlin/android/os/StrictMode.VmPolicy.Builder#penaltyListener(java.util.concurrent.Executor,%20android.os.StrictMode.OnVmViolationListener)` is enabled, the listener is called on the provided executor when a VM violation occurs. |
| --- | --- |

## Classes

| [AsyncTask](../android/os/AsyncTask.md) | AsyncTask was intended to enable proper and easy use of the UI thread. |
| --- | --- |
| [BaseBundle](../android/os/BaseBundle.md) | A mapping from String keys to values of various types. |
| [BatteryManager](../android/os/BatteryManager.md) | The BatteryManager class contains strings and constants used for values in the `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String` Intent, and provides a method for querying battery and charging properties. |
| [Binder](../android/os/Binder.md) | Base class for a remotable object, the core part of a lightweight remote procedure call mechanism defined by `https://developer.android.com/reference/kotlin/android/os/IBinder`. |
| --- | --- |
| [BugreportManager](../android/os/BugreportManager.md) | Class that provides a privileged API to capture and consume bugreports. |
| [Build](../android/os/Build.md) | Information about the current build, extracted from system properties. |
| [Bundle](../android/os/Bundle.md) | A mapping from String keys to various `https://developer.android.com/reference/kotlin/android/os/Parcelable` values. |
| --- | --- |
| [CancellationSignal](../android/os/CancellationSignal.md) | Provides the ability to cancel an operation in progress. |
| [CombinedVibration](../android/os/CombinedVibration.md) | A CombinedVibration describes a combination of haptic effects to be performed by one or more `https://developer.android.com/reference/kotlin/android/os/Vibrator`. |
| [ConditionVariable](../android/os/ConditionVariable.md) | Class that implements the condition variable locking paradigm. |
| --- | --- |
| [CountDownTimer](../android/os/CountDownTimer.md) | Schedule a countdown until a time in the future, with regular notifications on intervals along the way. |
| [CpuHeadroomParams](../android/os/CpuHeadroomParams.md) | Headroom request params used by `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#getCpuHeadroom(android.os.CpuHeadroomParams)`. |
| [CpuUsageInfo](../android/os/CpuUsageInfo.md) | CPU usage information per core. |
| --- | --- |
| [Debug](../android/os/Debug.md) | Provides various debugging methods for Android applications, including tracing and allocation counts. |
| [DropBoxManager](../android/os/DropBoxManager.md) | Enqueues chunks of data (from various sources -- application crashes, kernel log records, etc.). |
| [Environment](../android/os/Environment.md) | Provides access to environment variables. |
| --- | --- |
| [FileObserver](../android/os/FileObserver.md) | Monitors files (using [inotify](http://en.wikipedia.org/wiki/Inotify)) to fire an event after files are accessed or changed by any process on the device (including this one). |
| [FileUtils](../android/os/FileUtils.md) | Utility methods useful for working with files. |
| [GpuHeadroomParams](../android/os/GpuHeadroomParams.md) | Headroom request params used by `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#getGpuHeadroom(android.os.GpuHeadroomParams)`. |
| --- | --- |
| [Handler](../android/os/Handler.md) | A Handler allows you to send and process `https://developer.android.com/reference/kotlin/android/os/Message` and Runnable objects associated with a thread's `https://developer.android.com/reference/kotlin/android/os/MessageQueue`. |
| [HandlerThread](../android/os/HandlerThread.md) | A `https://developer.android.com/reference/kotlin/java/lang/Thread.html#` that has a `https://developer.android.com/reference/kotlin/android/os/Looper`. |
| [HardwarePropertiesManager](../android/os/HardwarePropertiesManager.md) | The HardwarePropertiesManager class provides a mechanism of accessing hardware state of a device: CPU, GPU and battery temperatures, CPU usage per core, fan speed, etc. |
| --- | --- |
| [LocaleList](../android/os/LocaleList.md) | LocaleList is an immutable list of Locales, typically used to keep an ordered list of user preferences for locales. |
| [Looper](../android/os/Looper.md) | Class used to run a message loop for a thread. |
| [MemoryFile](../android/os/MemoryFile.md) | MemoryFile is a wrapper for `https://developer.android.com/reference/kotlin/android/os/SharedMemory` which can optionally be set to purgeable. |
| --- | --- |
| [Message](../android/os/Message.md) | Defines a message containing a description and arbitrary data object that can be sent to a `https://developer.android.com/reference/kotlin/android/os/Handler`. |
| [MessageQueue](../android/os/MessageQueue.md) | Low-level class holding the list of messages to be dispatched by a `https://developer.android.com/reference/kotlin/android/os/Looper`. |
| [Messenger](../android/os/Messenger.md) | Reference to a Handler, which others can use to send messages to it. |
| --- | --- |
| [Parcel](../android/os/Parcel.md) | Container for a message (data and object references) that can be sent through an IBinder. |
| [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md) | The FileDescriptor returned by `https://developer.android.com/reference/kotlin/android/os/Parcel#readFileDescriptor()`, allowing you to close it when done with it. |
| [ParcelUuid](../android/os/ParcelUuid.md) | This class is a Parcelable wrapper around `https://developer.android.com/reference/kotlin/java/util/UUID.html#` which is an immutable representation of a 128-bit universally unique identifier. |
| --- | --- |
| [PatternMatcher](../android/os/PatternMatcher.md) | A simple pattern matcher, which is safe to use on untrusted data: it does not provide full reg-exp support, only simple globbing that can not be used maliciously. |
| [PerformanceHintManager](../android/os/PerformanceHintManager.md) | The PerformanceHintManager allows apps to send performance hint to system. |
| [PersistableBundle](../android/os/PersistableBundle.md) | A mapping from String keys to values of various types. |
| --- | --- |
| [PowerManager](../android/os/PowerManager.md) | This class lets you query and request control of aspects of the device's power state. |
| [PowerMonitor](../android/os/PowerMonitor.md) | A PowerMonitor represents either an ODPM rail (on-device power rail monitor) or a modeled energy consumer. |
| [PowerMonitorReadings](../android/os/PowerMonitorReadings.md) | A collection of energy measurements from Power Monitors. |
| --- | --- |
| [Process](../android/os/Process.md) | Tools for managing OS processes. |
| [ProfilingManager](../android/os/ProfilingManager.md) | This class allows the caller to: - Request profiling and listen for results. Profiling types supported are: system traces, java heap dumps, heap profiles, and stack traces. - Register triggers for the system to capture profiling on the apps behalf. <br /> |
| [ProfilingResult](../android/os/ProfilingResult.md) | Encapsulates results of a single profiling request operation. |
| --- | --- |
| [ProfilingTrigger](../android/os/ProfilingTrigger.md) | Encapsulates a single profiling trigger. |
| [ProxyFileDescriptorCallback](../android/os/ProxyFileDescriptorCallback.md) | Callback that handles file system requests from ProxyFileDescriptor. |
| [RecoverySystem](../android/os/RecoverySystem.md) | RecoverySystem contains methods for interacting with the Android recovery system (the separate partition that can be used to install system updates, wipe user data, etc.) |
| --- | --- |
| [RemoteCallbackList](../android/os/RemoteCallbackList.md) | Takes care of the grunt work of maintaining a list of remote interfaces, typically for the use of performing callbacks from a `https://developer.android.com/reference/kotlin/android/app/Service.html#` to its clients. |
| [ResultReceiver](../android/os/ResultReceiver.md) | Generic interface for receiving a callback result from someone. |
| [SecurityStateManager](../android/os/SecurityStateManager.md) | SecurityStateManager provides the functionality to query the security status of the system and platform components. |
| --- | --- |
| [SharedMemory](../android/os/SharedMemory.md) | SharedMemory enables the creation, mapping, and protection control over anonymous shared memory. |
| [StatFs](../android/os/StatFs.md) | Retrieve overall information about the space on a filesystem. |
| [StrictMode](../android/os/StrictMode.md) | StrictMode is a developer tool which detects things you might be doing by accident and brings them to your attention so you can fix them. |
| --- | --- |
| [SystemClock](../android/os/SystemClock.md) | Core timekeeping facilities. |
| [TestLooperManager](../android/os/TestLooperManager.md) | Blocks a looper from executing any messages, and allows the holder of this object to control when and which messages get executed until it is released. |
| [TokenWatcher](../android/os/TokenWatcher.md) | A TokenWatcher watches a collection of `https://developer.android.com/reference/kotlin/android/os/IBinder`s. |
| --- | --- |
| [Trace](../android/os/Trace.md) | Writes trace events to the system trace buffer. |
| [UserHandle](../android/os/UserHandle.md) | Representation of a user on the device. |
| [UserManager](../android/os/UserManager.md) | Manages users and user details on a multi-user system. |
| --- | --- |
| [VibrationAttributes](../android/os/VibrationAttributes.md) | Encapsulates a collection of attributes describing information about a vibration. |
| [VibrationEffect](../android/os/VibrationEffect.md) | A VibrationEffect describes a haptic effect to be performed by a `https://developer.android.com/reference/kotlin/android/os/Vibrator`. |
| [Vibrator](../android/os/Vibrator.md) | Class that operates the vibrator on the device. |
| --- | --- |
| [VibratorManager](../android/os/VibratorManager.md) | Provides access to all vibrators from the device, as well as the ability to run them in a synchronized fashion. |
| [WorkDuration](../android/os/WorkDuration.md) | WorkDuration contains the measured time in nano seconds of the workload in each component, see `https://developer.android.com/reference/kotlin/android/os/PerformanceHintManager.Session#reportActualWorkDuration(android.os.WorkDuration)`. |
| [WorkSource](../android/os/WorkSource.md) | Describes the source of some work that may be done by someone else. |
| --- | --- |

## Exceptions

| [BadParcelableException](../android/os/BadParcelableException.md) | Exception thrown when a `https://developer.android.com/reference/kotlin/android/os/Parcelable` is malformed or otherwise invalid. |
| --- | --- |
| [DeadObjectException](../android/os/DeadObjectException.md) | The object you are calling has died, because its hosting process no longer exists, or there has been a low-level binder error. |
| [DeadSystemException](../android/os/DeadSystemException.md) | The core Android system has died and is going through a runtime restart. |
| [FileUriExposedException](../android/os/FileUriExposedException.md) | The exception that may be thrown when an application exposes a `file://` `https://developer.android.com/reference/kotlin/android/net/Uri.html#` to another app. |
| --- | --- |
| [LimitExceededException](../android/os/LimitExceededException.md) | Indicates that the app has exceeded a limit set by the System. |
| [NetworkOnMainThreadException](../android/os/NetworkOnMainThreadException.md) | The exception that is thrown when an application attempts to perform a networking operation on its main thread. |
| [OperationCanceledException](../android/os/OperationCanceledException.md) | An exception type that is thrown when an operation in progress is canceled. |
| --- | --- |
| [ParcelFormatException](../android/os/ParcelFormatException.md) | The contents of a Parcel (usually during unmarshalling) does not contain the expected data. |
| [RemoteException](../android/os/RemoteException.md) | Parent exception for all Binder remote-invocation errors Note: not all exceptions from binder services will be subclasses of this. |
| [TransactionTooLargeException](../android/os/TransactionTooLargeException.md) | The Binder transaction failed because it was too large. |
| --- | --- |
