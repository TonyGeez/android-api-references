# android.os

Kotlin | [Java](https://developer.android.com/reference/android/os/package-summary "View this page in Java")

## Interfaces

| [OnCancelListener](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.OnCancelListener) | Listens for cancellation. |
| [ProgressListener](https://developer.android.com/reference/kotlin/android/os/FileUtils.ProgressListener) | Listener that is called periodically as progress is made. |
| [Callback](https://developer.android.com/reference/kotlin/android/os/Handler.Callback) | Callback interface you can use when instantiating a Handler to avoid having to implement your own subclass of Handler. |
| [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder) | Base interface for a remotable object, the core part of a lightweight remote procedure call mechanism designed for high performance when performing in-process and cross-process calls. |
| [IInterface](https://developer.android.com/reference/kotlin/android/os/IInterface) | Base class for Binder interfaces. |
| [IdleHandler](https://developer.android.com/reference/kotlin/android/os/MessageQueue.IdleHandler) | Callback interface for discovering when a thread is going to block waiting for more messages. |
| [OnFileDescriptorEventListener](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener) | A listener which is invoked when file descriptor related events occur. |
| [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver) | Callback interface intended for use when an asynchronous operation may result in a failure. |
| [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable) | Interface for classes whose instances can be written to and restored from a `https://developer.android.com/reference/kotlin/android/os/Parcel`. |
| [OnCloseListener](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.OnCloseListener) | Callback indicating that a ParcelFileDescriptor has been closed. |
| [OnThermalHeadroomChangedListener](https://developer.android.com/reference/kotlin/android/os/PowerManager.OnThermalHeadroomChangedListener) | Listener passed to android. |
| [OnThermalStatusChangedListener](https://developer.android.com/reference/kotlin/android/os/PowerManager.OnThermalStatusChangedListener) | Listener passed to android. |
| [WakeLockStateListener](https://developer.android.com/reference/kotlin/android/os/PowerManager.WakeLockStateListener) | A listener interface to get notified when the wakelock is enabled/disabled. |
| [ProgressListener](https://developer.android.com/reference/kotlin/android/os/RecoverySystem.ProgressListener) | Interface definition for a callback to be invoked regularly as verification proceeds. |
| [OnThreadViolationListener](https://developer.android.com/reference/kotlin/android/os/StrictMode.OnThreadViolationListener) | When #`https://developer.android.com/reference/kotlin/android/os/StrictMode.ThreadPolicy.Builder#penaltyListener(java.util.concurrent.Executor,%20android.os.StrictMode.OnThreadViolationListener)` is enabled, the listener is called on the provided executor when a Thread violation occurs. |
| [OnVmViolationListener](https://developer.android.com/reference/kotlin/android/os/StrictMode.OnVmViolationListener) | When #`https://developer.android.com/reference/kotlin/android/os/StrictMode.VmPolicy.Builder#penaltyListener(java.util.concurrent.Executor,%20android.os.StrictMode.OnVmViolationListener)` is enabled, the listener is called on the provided executor when a VM violation occurs. |

## Classes

| [AsyncTask](https://developer.android.com/reference/kotlin/android/os/AsyncTask) | AsyncTask was intended to enable proper and easy use of the UI thread. |
| [BaseBundle](https://developer.android.com/reference/kotlin/android/os/BaseBundle) | A mapping from String keys to values of various types. |
| [BatteryManager](https://developer.android.com/reference/kotlin/android/os/BatteryManager) | The BatteryManager class contains strings and constants used for values in the `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_BATTERY_CHANGED:kotlin.String` Intent, and provides a method for querying battery and charging properties. |
| [Binder](https://developer.android.com/reference/kotlin/android/os/Binder) | Base class for a remotable object, the core part of a lightweight remote procedure call mechanism defined by `https://developer.android.com/reference/kotlin/android/os/IBinder`. |
| [BugreportManager](https://developer.android.com/reference/kotlin/android/os/BugreportManager) | Class that provides a privileged API to capture and consume bugreports. |
| [Build](https://developer.android.com/reference/kotlin/android/os/Build) | Information about the current build, extracted from system properties. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle) | A mapping from String keys to various `https://developer.android.com/reference/kotlin/android/os/Parcelable` values. |
| [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal) | Provides the ability to cancel an operation in progress. |
| [CombinedVibration](https://developer.android.com/reference/kotlin/android/os/CombinedVibration) | A CombinedVibration describes a combination of haptic effects to be performed by one or more `https://developer.android.com/reference/kotlin/android/os/Vibrator`. |
| [ConditionVariable](https://developer.android.com/reference/kotlin/android/os/ConditionVariable) | Class that implements the condition variable locking paradigm. |
| [CountDownTimer](https://developer.android.com/reference/kotlin/android/os/CountDownTimer) | Schedule a countdown until a time in the future, with regular notifications on intervals along the way. |
| [CpuHeadroomParams](https://developer.android.com/reference/kotlin/android/os/CpuHeadroomParams) | Headroom request params used by `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#getCpuHeadroom(android.os.CpuHeadroomParams)`. |
| [CpuUsageInfo](https://developer.android.com/reference/kotlin/android/os/CpuUsageInfo) | CPU usage information per core. |
| [Debug](https://developer.android.com/reference/kotlin/android/os/Debug) | Provides various debugging methods for Android applications, including tracing and allocation counts. |
| [DropBoxManager](https://developer.android.com/reference/kotlin/android/os/DropBoxManager) | Enqueues chunks of data (from various sources -- application crashes, kernel log records, etc.). |
| [Environment](https://developer.android.com/reference/kotlin/android/os/Environment) | Provides access to environment variables. |
| [FileObserver](https://developer.android.com/reference/kotlin/android/os/FileObserver) | Monitors files (using [inotify](http://en.wikipedia.org/wiki/Inotify)) to fire an event after files are accessed or changed by any process on the device (including this one). |
| [FileUtils](https://developer.android.com/reference/kotlin/android/os/FileUtils) | Utility methods useful for working with files. |
| [GpuHeadroomParams](https://developer.android.com/reference/kotlin/android/os/GpuHeadroomParams) | Headroom request params used by `https://developer.android.com/reference/kotlin/android/os/health/SystemHealthManager#getGpuHeadroom(android.os.GpuHeadroomParams)`. |
| [Handler](https://developer.android.com/reference/kotlin/android/os/Handler) | A Handler allows you to send and process `https://developer.android.com/reference/kotlin/android/os/Message` and Runnable objects associated with a thread's `https://developer.android.com/reference/kotlin/android/os/MessageQueue`. |
| [HandlerThread](https://developer.android.com/reference/kotlin/android/os/HandlerThread) | A `https://developer.android.com/reference/kotlin/java/lang/Thread.html#` that has a `https://developer.android.com/reference/kotlin/android/os/Looper`. |
| [HardwarePropertiesManager](https://developer.android.com/reference/kotlin/android/os/HardwarePropertiesManager) | The HardwarePropertiesManager class provides a mechanism of accessing hardware state of a device: CPU, GPU and battery temperatures, CPU usage per core, fan speed, etc. |
| [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList) | LocaleList is an immutable list of Locales, typically used to keep an ordered list of user preferences for locales. |
| [Looper](https://developer.android.com/reference/kotlin/android/os/Looper) | Class used to run a message loop for a thread. |
| [MemoryFile](https://developer.android.com/reference/kotlin/android/os/MemoryFile) | MemoryFile is a wrapper for `https://developer.android.com/reference/kotlin/android/os/SharedMemory` which can optionally be set to purgeable. |
| [Message](https://developer.android.com/reference/kotlin/android/os/Message) | Defines a message containing a description and arbitrary data object that can be sent to a `https://developer.android.com/reference/kotlin/android/os/Handler`. |
| [MessageQueue](https://developer.android.com/reference/kotlin/android/os/MessageQueue) | Low-level class holding the list of messages to be dispatched by a `https://developer.android.com/reference/kotlin/android/os/Looper`. |
| [Messenger](https://developer.android.com/reference/kotlin/android/os/Messenger) | Reference to a Handler, which others can use to send messages to it. |
| [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel) | Container for a message (data and object references) that can be sent through an IBinder. |
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor) | The FileDescriptor returned by `https://developer.android.com/reference/kotlin/android/os/Parcel#readFileDescriptor()`, allowing you to close it when done with it. |
| [ParcelUuid](https://developer.android.com/reference/kotlin/android/os/ParcelUuid) | This class is a Parcelable wrapper around `https://developer.android.com/reference/kotlin/java/util/UUID.html#` which is an immutable representation of a 128-bit universally unique identifier. |
| [PatternMatcher](https://developer.android.com/reference/kotlin/android/os/PatternMatcher) | A simple pattern matcher, which is safe to use on untrusted data: it does not provide full reg-exp support, only simple globbing that can not be used maliciously. |
| [PerformanceHintManager](https://developer.android.com/reference/kotlin/android/os/PerformanceHintManager) | The PerformanceHintManager allows apps to send performance hint to system. |
| [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle) | A mapping from String keys to values of various types. |
| [PowerManager](https://developer.android.com/reference/kotlin/android/os/PowerManager) | This class lets you query and request control of aspects of the device's power state. |
| [PowerMonitor](https://developer.android.com/reference/kotlin/android/os/PowerMonitor) | A PowerMonitor represents either an ODPM rail (on-device power rail monitor) or a modeled energy consumer. |
| [PowerMonitorReadings](https://developer.android.com/reference/kotlin/android/os/PowerMonitorReadings) | A collection of energy measurements from Power Monitors. |
| [Process](https://developer.android.com/reference/kotlin/android/os/Process) | Tools for managing OS processes. |
| [ProfilingManager](https://developer.android.com/reference/kotlin/android/os/ProfilingManager) | This class allows the caller to: - Request profiling and listen for results. Profiling types supported are: system traces, java heap dumps, heap profiles, and stack traces. - Register triggers for the system to capture profiling on the apps behalf. <br /> |
| [ProfilingResult](https://developer.android.com/reference/kotlin/android/os/ProfilingResult) | Encapsulates results of a single profiling request operation. |
| [ProfilingTrigger](https://developer.android.com/reference/kotlin/android/os/ProfilingTrigger) | Encapsulates a single profiling trigger. |
| [ProxyFileDescriptorCallback](https://developer.android.com/reference/kotlin/android/os/ProxyFileDescriptorCallback) | Callback that handles file system requests from ProxyFileDescriptor. |
| [RecoverySystem](https://developer.android.com/reference/kotlin/android/os/RecoverySystem) | RecoverySystem contains methods for interacting with the Android recovery system (the separate partition that can be used to install system updates, wipe user data, etc.) |
| [RemoteCallbackList](https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList) | Takes care of the grunt work of maintaining a list of remote interfaces, typically for the use of performing callbacks from a `https://developer.android.com/reference/kotlin/android/app/Service.html#` to its clients. |
| [ResultReceiver](https://developer.android.com/reference/kotlin/android/os/ResultReceiver) | Generic interface for receiving a callback result from someone. |
| [SecurityStateManager](https://developer.android.com/reference/kotlin/android/os/SecurityStateManager) | SecurityStateManager provides the functionality to query the security status of the system and platform components. |
| [SharedMemory](https://developer.android.com/reference/kotlin/android/os/SharedMemory) | SharedMemory enables the creation, mapping, and protection control over anonymous shared memory. |
| [StatFs](https://developer.android.com/reference/kotlin/android/os/StatFs) | Retrieve overall information about the space on a filesystem. |
| [StrictMode](https://developer.android.com/reference/kotlin/android/os/StrictMode) | StrictMode is a developer tool which detects things you might be doing by accident and brings them to your attention so you can fix them. |
| [SystemClock](https://developer.android.com/reference/kotlin/android/os/SystemClock) | Core timekeeping facilities. |
| [TestLooperManager](https://developer.android.com/reference/kotlin/android/os/TestLooperManager) | Blocks a looper from executing any messages, and allows the holder of this object to control when and which messages get executed until it is released. |
| [TokenWatcher](https://developer.android.com/reference/kotlin/android/os/TokenWatcher) | A TokenWatcher watches a collection of `https://developer.android.com/reference/kotlin/android/os/IBinder`s. |
| [Trace](https://developer.android.com/reference/kotlin/android/os/Trace) | Writes trace events to the system trace buffer. |
| [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle) | Representation of a user on the device. |
| [UserManager](https://developer.android.com/reference/kotlin/android/os/UserManager) | Manages users and user details on a multi-user system. |
| [VibrationAttributes](https://developer.android.com/reference/kotlin/android/os/VibrationAttributes) | Encapsulates a collection of attributes describing information about a vibration. |
| [VibrationEffect](https://developer.android.com/reference/kotlin/android/os/VibrationEffect) | A VibrationEffect describes a haptic effect to be performed by a `https://developer.android.com/reference/kotlin/android/os/Vibrator`. |
| [Vibrator](https://developer.android.com/reference/kotlin/android/os/Vibrator) | Class that operates the vibrator on the device. |
| [VibratorManager](https://developer.android.com/reference/kotlin/android/os/VibratorManager) | Provides access to all vibrators from the device, as well as the ability to run them in a synchronized fashion. |
| [WorkDuration](https://developer.android.com/reference/kotlin/android/os/WorkDuration) | WorkDuration contains the measured time in nano seconds of the workload in each component, see `https://developer.android.com/reference/kotlin/android/os/PerformanceHintManager.Session#reportActualWorkDuration(android.os.WorkDuration)`. |
| [WorkSource](https://developer.android.com/reference/kotlin/android/os/WorkSource) | Describes the source of some work that may be done by someone else. |

## Exceptions

| [BadParcelableException](https://developer.android.com/reference/kotlin/android/os/BadParcelableException) | Exception thrown when a `https://developer.android.com/reference/kotlin/android/os/Parcelable` is malformed or otherwise invalid. |
| [DeadObjectException](https://developer.android.com/reference/kotlin/android/os/DeadObjectException) | The object you are calling has died, because its hosting process no longer exists, or there has been a low-level binder error. |
| [DeadSystemException](https://developer.android.com/reference/kotlin/android/os/DeadSystemException) | The core Android system has died and is going through a runtime restart. |
| [FileUriExposedException](https://developer.android.com/reference/kotlin/android/os/FileUriExposedException) | The exception that may be thrown when an application exposes a `file://` `https://developer.android.com/reference/kotlin/android/net/Uri.html#` to another app. |
| [LimitExceededException](https://developer.android.com/reference/kotlin/android/os/LimitExceededException) | Indicates that the app has exceeded a limit set by the System. |
| [NetworkOnMainThreadException](https://developer.android.com/reference/kotlin/android/os/NetworkOnMainThreadException) | The exception that is thrown when an application attempts to perform a networking operation on its main thread. |
| [OperationCanceledException](https://developer.android.com/reference/kotlin/android/os/OperationCanceledException) | An exception type that is thrown when an operation in progress is canceled. |
| [ParcelFormatException](https://developer.android.com/reference/kotlin/android/os/ParcelFormatException) | The contents of a Parcel (usually during unmarshalling) does not contain the expected data. |
| [RemoteException](https://developer.android.com/reference/kotlin/android/os/RemoteException) | Parent exception for all Binder remote-invocation errors Note: not all exceptions from binder services will be subclasses of this. |
| [TransactionTooLargeException](https://developer.android.com/reference/kotlin/android/os/TransactionTooLargeException) | The Binder transaction failed because it was too large. |
