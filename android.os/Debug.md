# Debug

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Debug

Kotlin| [Java](Debug.md) 
| --- | --- |

```
class Debug
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.Debug](Debug.md) |

Provides various debugging methods for Android applications, including tracing and allocation counts.

**Logging Trace Files**

Debug can create log files that give details about an application, such as a call stack and start/stop times for any running methods. See [Inspect Trace Logs with Traceview](https://developer.android.com/studio/profile/traceview.html) for information about reading trace files. To start logging trace files, call one of the startMethodTracing() methods. To stop tracing, call [stopMethodTracing()](Debug.md)).

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [InstructionCount](../android/os/Debug.InstructionCount.md) API for gathering and querying instruction counts. |
| | [MemoryInfo](../android/os/Debug.MemoryInfo.md) This class is used to retrieved various statistics about the memory mappings for this process. |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_CLASSLOADER](Debug.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_FULL_DETAIL](Debug.md) Flags for printLoadedClasses(). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_INITIALIZED](Debug.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRACE_COUNT_ALLOCS](Debug.md) Flags for startMethodTracing(). |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [attachJvmtiAgent](Debug.md))`(`library:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `options:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `classLoader:` ` [ClassLoader](../java.lang/ClassLoader.md)?`)` Attach a library as a jvmti agent to the current runtime, with the given classloader determining the library search path. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [changeDebugPort](Debug.md))`(`port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Change the JDWP port. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dumpHprofData](Debug.md))`(`fileName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Dump "hprof" data to the specified file. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dumpService](Debug.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `fd:` ` [FileDescriptor](../java.io/FileDescriptor.md)!`, `args:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Get a debugging dump of a system service by name. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [enableEmulatorTraceOutput](Debug.md))`()` Enable "emulator traces", in which information about the current method is made available to the "emulator -trace" feature. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBinderDeathObjectCount](Debug.md))`()` Returns the number of death notification links to Binder objects that exist in the current process. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBinderLocalObjectCount](Debug.md))`()` Returns the number of active local Binder objects that exist in the current process. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBinderProxyObjectCount](Debug.md))`()` Returns the number of references to remote proxy Binder objects that exist in the current process. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBinderReceivedTransactions](Debug.md))`()` Returns the number of received transactions from the binder driver. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBinderSentTransactions](Debug.md))`()` Returns the number of sent transactions from this process. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGlobalAllocCount](Debug.md))`()` Returns the global count of objects allocated by the runtime between a [start](Debug.md))and [stop](Debug.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGlobalAllocSize](Debug.md))`()` Returns the global size, in bytes, of objects allocated by the runtime between a [start](Debug.md))and [stop](Debug.md)). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGlobalClassInitCount](Debug.md))`()` Returns the number of classes successfully initialized (ie those that executed without throwing an exception) between a [start](Debug.md))and [stop](Debug.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGlobalClassInitTime](Debug.md))`()` Returns the time spent successfully initializing classes between a [start](Debug.md))and [stop](Debug.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGlobalExternalAllocCount](Debug.md))`()` This method exists for compatibility and always returns 0. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGlobalExternalAllocSize](Debug.md))`()` This method exists for compatibility and always returns 0. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGlobalExternalFreedCount](Debug.md))`()` This method exists for compatibility and always returns 0. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGlobalExternalFreedSize](Debug.md))`()` This method exists for compatibility and has no effect. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGlobalFreedCount](Debug.md))`()` Returns the global count of objects freed by the runtime between a [start](Debug.md))and [stop](Debug.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGlobalFreedSize](Debug.md))`()` Returns the global size, in bytes, of objects freed by the runtime between a [start](Debug.md))and [stop](Debug.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGlobalGcInvocationCount](Debug.md))`()` Returns the number of non-concurrent GC invocations between a [start](Debug.md))and [stop](Debug.md)). |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getInstanceCount](Debug.md))`(`cls:` ` [Class](../java.lang/Class.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>`)` Counts the number of instances of the specified class. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getInstanceCount](Debug.md))`(`cls:` ` [Class](../java.lang/Class.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>`, `includeAssignable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Counts the number of instances of the specified class. |
| static [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html) | [getInstanceCounts](Debug.md))`(`classes:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Class](../java.lang/Class.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!>`)` Counts the number of instances of the specified classes. |
| --- | --- |
| static [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html) | [getInstanceCounts](Debug.md))`(`classes:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Class](../java.lang/Class.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!>`, `includeAssignable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Counts the number of instances of the specified classes. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLoadedClassCount](Debug.md))`()` Get the number of loaded classes. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getMemoryInfo](Debug.md))`(`memoryInfo:` ` [Debug.MemoryInfo](../android/os/Debug.MemoryInfo.md)!`)` Retrieves information about this processes memory usages. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getNativeHeapAllocatedSize](Debug.md))`()` Returns the amount of allocated memory in the native heap. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getNativeHeapFreeSize](Debug.md))`()` Returns the amount of free memory in the native heap. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getNativeHeapSize](Debug.md))`()` Returns the size of the native heap. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getPss](Debug.md))`()` Retrieves the PSS memory used by the process as given by the smaps. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getRss](Debug.md))`()` Retrieves the RSS memory used by the process as given by the status file. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getRuntimeStat](Debug.md))`(`statName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the value of a particular runtime statistic or`null`if no such runtime statistic exists. |
| --- | --- |
| static [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getRuntimeStats](Debug.md))`()` Returns a map of the names/values of the runtime statistics that [getRuntimeStat(java.lang.String)](Debug.md))supports. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getThreadAllocCount](Debug.md))`()` Returns the thread-local count of objects allocated by the runtime between a [start](Debug.md))and [stop](Debug.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getThreadAllocSize](Debug.md))`()` Returns the thread-local size of objects allocated by the runtime between a [start](Debug.md))and [stop](Debug.md)). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getThreadExternalAllocCount](Debug.md))`()` This method exists for compatibility and has no effect. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getThreadExternalAllocSize](Debug.md))`()` This method exists for compatibility and has no effect. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getThreadGcInvocationCount](Debug.md))`()` Returns the number of thread-local non-concurrent GC invocations between a [start](Debug.md))and [stop](Debug.md)). |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDebuggerConnected](Debug.md))`()` Determine if a debugger is currently attached. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [printLoadedClasses](Debug.md))`(`flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Dump a list of all currently loaded class to the log file. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetAllCounts](Debug.md))`()` Clears all the global and thread-local memory allocation counters. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetGlobalAllocCount](Debug.md))`()` Clears the global count of objects allocated. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetGlobalAllocSize](Debug.md))`()` Clears the global size of objects allocated. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetGlobalClassInitCount](Debug.md))`()` Clears the count of classes initialized. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetGlobalClassInitTime](Debug.md))`()` Clears the count of time spent initializing classes. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetGlobalExternalAllocCount](Debug.md))`()` This method exists for compatibility and has no effect. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetGlobalExternalAllocSize](Debug.md))`()` This method exists for compatibility and has no effect. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetGlobalExternalFreedCount](Debug.md))`()` This method exists for compatibility and has no effect. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetGlobalExternalFreedSize](Debug.md))`()` This method exists for compatibility and has no effect. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetGlobalFreedCount](Debug.md))`()` Clears the global count of objects freed. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetGlobalFreedSize](Debug.md))`()` Clears the global size of objects freed. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetGlobalGcInvocationCount](Debug.md))`()` Clears the count of non-concurrent GC invocations. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetThreadAllocCount](Debug.md))`()` Clears the thread-local count of objects allocated. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetThreadAllocSize](Debug.md))`()` Clears the thread-local count of objects allocated. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetThreadExternalAllocCount](Debug.md))`()` This method exists for compatibility and has no effect. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetThreadExternalAllocSize](Debug.md))`()` This method exists for compatibility and has no effect. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetThreadGcInvocationCount](Debug.md))`()` Clears the thread-local count of non-concurrent GC invocations. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setAllocationLimit](Debug.md))`(`limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Establish an object allocation limit in the current thread. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setGlobalAllocationLimit](Debug.md))`(`limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Establish a global object allocation limit. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startAllocCounting](Debug.md))`()` Start counting the number and aggregate size of memory allocations. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startMethodTracing](Debug.md))`()` Start method tracing with default log name and buffer size. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startMethodTracing](Debug.md))`(`tracePath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Start method tracing, specifying the trace log file path. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startMethodTracing](Debug.md))`(`tracePath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `bufferSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Start method tracing, specifying the trace log file name and the buffer size. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startMethodTracing](Debug.md))`(`tracePath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `bufferSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Start method tracing, specifying the trace log file name, the buffer size, and flags. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startMethodTracingSampling](Debug.md))`(`tracePath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `bufferSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `intervalUs:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Start sampling-based method tracing, specifying the trace log file name, the buffer size, and the sampling interval. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startNativeTracing](Debug.md))`()` Enable qemu tracing. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopAllocCounting](Debug.md))`()` Stop counting the number and aggregate size of memory allocations. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopMethodTracing](Debug.md))`()` Stop method tracing. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopNativeTracing](Debug.md))`()` Stop qemu tracing. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [threadCpuTimeNanos](Debug.md))`()` Get an indication of thread CPU usage. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [waitForDebugger](Debug.md))`()` Wait until a debugger attaches. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [waitingForDebugger](Debug.md))`()` Returns "true" if one or more threads is waiting for a debugger to attach. |

## Constants

### SHOW_CLASSLOADER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHOW_CLASSLOADER: Int
```  

 Value: 2

### SHOW_FULL_DETAIL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHOW_FULL_DETAIL: Int
```

Flags for printLoadedClasses(). Default behavior is to only show the class name. 

 Value: 1

### SHOW_INITIALIZED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHOW_INITIALIZED: Int
```  

 Value: 4

### TRACE_COUNT_ALLOCS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRACE_COUNT_ALLOCS: Int
```

**Deprecated:** *Accurate counting is a burden on the runtime and may be removed.*

Flags for startMethodTracing(). These can be ORed together. TRACE_COUNT_ALLOCS adds the results from startAllocCounting to the trace key file. 

 Value: 1

## Public methods

### attachJvmtiAgent

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun attachJvmtiAgent(
    library: String, 
    options: String?, 
    classLoader: ClassLoader?
): Unit
```

Attach a library as a jvmti agent to the current runtime, with the given classloader determining the library search path.

Note: agents may only be attached to debuggable apps. Otherwise, this function will throw a SecurityException.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `library` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the library containing the agent. This value cannot be`null`. |
| `options` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:the options passed to the agent. This value may be`null`. |
| `classLoader` | [ClassLoader](../java.lang/ClassLoader.md)?:the classloader determining the library search path. This value may be`null`. |
| --- | --- |

| Exceptions ||
|-------------------------------|-------------------------------------|
| `java.io.IOException` | if the agent could not be attached. |
| `java.lang.SecurityException` | if the app is not debuggable. |

### changeDebugPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun changeDebugPort(port: Int): Unit
```

**Deprecated:** *no longer needed or useful*

Change the JDWP port. 

### dumpHprofData

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun dumpHprofData(fileName: String!): Unit
```

Dump "hprof" data to the specified file. This may cause a GC.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Full pathname of output file (e.g. "/sdcard/dump.hprof"). |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the VM was built without HPROF support. |
| `java.io.IOException` | if an error occurs while opening or writing files. |

### dumpService

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun dumpService(
    name: String!, 
    fd: FileDescriptor!, 
    args: Array<String!>!
): Boolean
```

Get a debugging dump of a system service by name.

Most services require the caller to hold android.permission.DUMP.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:of the service to dump |
| `fd` | [FileDescriptor](../java.io/FileDescriptor.md)!:to write dump output to (usually an output log file) |
| `args` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:to pass to the service's dump method, may be null |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the service was dumped successfully, false if the service could not be found or had an error while dumping |

### enableEmulatorTraceOutput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun enableEmulatorTraceOutput(): Unit
```

**Deprecated:** *Please use other tracing method in this class.*

Enable "emulator traces", in which information about the current method is made available to the "emulator -trace" feature. There is no corresponding "disable" call -- this is intended for use by the framework when tracing should be turned on and left that way, so that traces captured with F9/F10 will include the necessary data. This puts the VM into "profile" mode, which has performance consequences. To temporarily enable tracing, use [startNativeTracing()](Debug.md)). 

### getBinderDeathObjectCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getBinderDeathObjectCount(): Int
```

Returns the number of death notification links to Binder objects that exist in the current process. 

### getBinderLocalObjectCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getBinderLocalObjectCount(): Int
```

Returns the number of active local Binder objects that exist in the current process. 

### getBinderProxyObjectCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getBinderProxyObjectCount(): Int
```

Returns the number of references to remote proxy Binder objects that exist in the current process. 

### getBinderReceivedTransactions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getBinderReceivedTransactions(): Int
```

Returns the number of received transactions from the binder driver.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of received transactions or -1 if it could not read the stats. |

### getBinderSentTransactions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getBinderSentTransactions(): Int
```

Returns the number of sent transactions from this process.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of sent transactions or -1 if it could not read t. |

### getGlobalAllocCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getGlobalAllocCount(): Int
```

**Deprecated:** *Accurate counting is a burden on the runtime and may be removed.*

Returns the global count of objects allocated by the runtime between a [start](Debug.md))and [stop](Debug.md)). 

### getGlobalAllocSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getGlobalAllocSize(): Int
```

**Deprecated:** *Accurate counting is a burden on the runtime and may be removed.*

Returns the global size, in bytes, of objects allocated by the runtime between a [start](Debug.md))and [stop](Debug.md)). 

### getGlobalClassInitCount

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getGlobalClassInitCount(): Int
```

**Deprecated:** *Accurate counting is a burden on the runtime and may be removed.*

Returns the number of classes successfully initialized (ie those that executed without throwing an exception) between a [start](Debug.md))and [stop](Debug.md)). 

### getGlobalClassInitTime

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getGlobalClassInitTime(): Int
```

**Deprecated:** *Accurate counting is a burden on the runtime and may be removed.*

Returns the time spent successfully initializing classes between a [start](Debug.md))and [stop](Debug.md)). 

### getGlobalExternalAllocCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getGlobalExternalAllocCount(): Int
```

**Deprecated:** *This method is now obsolete.*

This method exists for compatibility and always returns 0. 

### getGlobalExternalAllocSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getGlobalExternalAllocSize(): Int
```

**Deprecated:** *This method is now obsolete.*

This method exists for compatibility and always returns 0. 

### getGlobalExternalFreedCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getGlobalExternalFreedCount(): Int
```

**Deprecated:** *This method is now obsolete.*

This method exists for compatibility and always returns 0. 

### getGlobalExternalFreedSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getGlobalExternalFreedSize(): Int
```

**Deprecated:** *This method is now obsolete.*

This method exists for compatibility and has no effect. 

### getGlobalFreedCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getGlobalFreedCount(): Int
```

**Deprecated:** *Accurate counting is a burden on the runtime and may be removed.*

Returns the global count of objects freed by the runtime between a [start](Debug.md))and [stop](Debug.md)). 

### getGlobalFreedSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getGlobalFreedSize(): Int
```

**Deprecated:** *Accurate counting is a burden on the runtime and may be removed.*

Returns the global size, in bytes, of objects freed by the runtime between a [start](Debug.md))and [stop](Debug.md)). 

### getGlobalGcInvocationCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getGlobalGcInvocationCount(): Int
```

**Deprecated:** *Accurate counting is a burden on the runtime and may be removed.*

Returns the number of non-concurrent GC invocations between a [start](Debug.md))and [stop](Debug.md)). 

### getInstanceCount

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstanceCount(cls: Class<Any!>): Long
```

Counts the number of instances of the specified class.

**Warning:**This operation can be expensive, as it may involve traversing portions of the Java heap. It is primarily intended for debugging purposes and should not be used in performance-critical code.

It's intended to help developers identify object leaks or to validate the number of instances of a specific class during development.

It is the caller's responsibility to do GC if they don't want unreachable objects to get counted.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cls` | [Class](../java.lang/Class.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>: [Class](../java.lang/Class.md) the class to count instances of. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the number of matching instances. |

### getInstanceCount

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstanceCount(
    cls: Class<Any!>, 
    includeAssignable: Boolean
): Long
```

Counts the number of instances of the specified class.

**Warning:**This operation can be expensive, as it may involve traversing portions of the Java heap. It is primarily intended for debugging purposes and should not be used in performance-critical code.

It's intended to help developers identify object leaks or to validate the number of instances of a specific class during development.

It is the caller's responsibility to do GC if they don't want unreachable objects to get counted.

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cls` | [Class](../java.lang/Class.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>: [Class](../java.lang/Class.md) the class to count instances of. This value cannot be`null`. |
| `includeAssignable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true, any instance whose class is assignable to`cls`, as defined by [Class.isAssignableFrom](../java.lang/Class.md)), is counted. If false, only instances whose class is equal to`cls`are counted. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the number of matching instances. |

### getInstanceCounts

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstanceCounts(classes: MutableList<Class<Any!>!>): LongArray
```

Counts the number of instances of the specified classes.

**Warning:**This operation can be expensive, as it may involve traversing portions of the Java heap. It is primarily intended for debugging purposes and should not be used in performance-critical code.

It's intended to help developers identify object leaks or to validate the number of instances of a specific class during development.

It is the caller's responsibility to do GC if they don't want unreachable objects to get counted.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `classes` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Class](../java.lang/Class.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!\>:An array of [Class](../java.lang/Class.md) objects representing the classes to count instances of. Must not be null. |

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html) | An array of`long`values, where each element corresponds to the number of instances of the class at the same index in the`classes`list. The returned array will have the same length as the input`classes`array. If the system is under memory pressure and unable to allocate the return array a empty array will be returned. This value cannot be`null`. |

### getInstanceCounts

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstanceCounts(
    classes: MutableList<Class<Any!>!>, 
    includeAssignable: Boolean
): LongArray
```

Counts the number of instances of the specified classes.

**Warning:**This operation can be expensive, as it may involve traversing portions of the Java heap. It is primarily intended for debugging purposes and should not be used in performance-critical code.

It's intended to help developers identify object leaks or to validate the number of instances of a specific class during development.

It is the caller's responsibility to do GC if they don't want unreachable objects to get counted.

| Parameters ||
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `classes` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Class](../java.lang/Class.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!\>:An array of [Class](../java.lang/Class.md) objects representing the classes to count instances of. Must not be null. |
| `includeAssignable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true, any instance whose class is assignable to`cls`, as defined by [Class.isAssignableFrom](../java.lang/Class.md)), is counted. If false, only instances whose class is equal to`cls`are counted. |

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html) | An array of`long`values, where each element corresponds to the number of instances of the class at the same index in the`classes`list. The returned array will have the same length as the input`classes`array. If the system is under memory pressure and unable to allocate the return array a empty array will be returned. This value cannot be`null`. |

### getLoadedClassCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getLoadedClassCount(): Int
```

Get the number of loaded classes.

| Return ||
|----------------------------------------------------------------------------|-------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of loaded classes. |

### getMemoryInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getMemoryInfo(memoryInfo: Debug.MemoryInfo!): Unit
```

Retrieves information about this processes memory usages. This information is broken down by how much is in use by dalvik, the native heap, and everything else.

**Note:** this method directly retrieves memory information for the given process from low-level data available to it. It may not be able to retrieve information about some protected allocations, such as graphics. If you want to be sure you can see all information about allocations by the process, use[android.app.ActivityManager#getProcessMemoryInfo(int[])](https://developer.android.com/reference/kotlin/android/app/ActivityManager.html#getProcessMemoryInfo(kotlin.IntArray))instead. 

### getNativeHeapAllocatedSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getNativeHeapAllocatedSize(): Long
```

Returns the amount of allocated memory in the native heap.

| Return ||
|------------------------------------------------------------------------------|------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The allocated size in bytes. |

### getNativeHeapFreeSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getNativeHeapFreeSize(): Long
```

Returns the amount of free memory in the native heap.

| Return ||
|------------------------------------------------------------------------------|--------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The freed size in bytes. |

### getNativeHeapSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getNativeHeapSize(): Long
```

Returns the size of the native heap.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The size of the native heap in bytes. |

### getPss

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getPss(): Long
```

Retrieves the PSS memory used by the process as given by the smaps. 

### getRss

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getRss(): Long
```

Retrieves the RSS memory used by the process as given by the status file. 

### getRuntimeStat

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getRuntimeStat(statName: String!): String!
```

Returns the value of a particular runtime statistic or`null`if no such runtime statistic exists.

The following table lists the runtime statistics that the runtime supports. All statistics are approximate. Individual allocations may not be immediately reflected in the results. Note runtime statistics may be added or removed in a future API level.

| Runtime statistic name | Meaning | Example | Supported (API Levels) |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|------------------------|
| art.gc.gc-count | The number of garbage collection runs. | `164` | 23 |
| art.gc.gc-time | The total duration of garbage collection runs in ms. | `62364` | 23 |
| art.gc.bytes-allocated | The total number of bytes that the application allocated. | `1463948408` | 23 |
| --- | --- | --- | --- |
| art.gc.bytes-freed | The total number of bytes that garbage collection reclaimed. | `1313493084` | 23 |
| art.gc.blocking-gc-count | The number of blocking garbage collection runs. | `2` | 23 |
| art.gc.blocking-gc-time | The total duration of blocking garbage collection runs in ms. | `804` | 23 |
| --- | --- | --- | --- |
| art.gc.gc-count-rate-histogram | Every 10 seconds, the gc-count-rate is computed as the number of garbage collection runs that have occurred over the last 10 seconds. art.gc.gc-count-rate-histogram is a histogram of the gc-count-rate samples taken since the process began. The histogram can be used to identify instances of high rates of garbage collection runs. For example, a histogram of "0:34503,1:45350,2:11281,3:8088,4:43,5:8" shows that most of the time there are between 0 and 2 garbage collection runs every 10 seconds, but there were 8 distinct 10-second intervals in which 5 garbage collection runs occurred. | `0:34503,1:45350,2:11281,3:8088,4:43,5:8` | 23 |
| art.gc.blocking-gc-count-rate-histogram | Every 10 seconds, the blocking-gc-count-rate is computed as the number of blocking garbage collection runs that have occurred over the last 10 seconds. art.gc.blocking-gc-count-rate-histogram is a histogram of the blocking-gc-count-rate samples taken since the process began. The histogram can be used to identify instances of high rates of blocking garbage collection runs. For example, a histogram of "0:99269,1:1,2:1" shows that most of the time there are zero blocking garbage collection runs every 10 seconds, but there was one 10-second interval in which one blocking garbage collection run occurred, and there was one interval in which two blocking garbage collection runs occurred. | `0:99269,1:1,2:1` | 23 |

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------|
| `statName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the runtime statistic to look up. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the value of the specified runtime statistic or`null`if the runtime statistic doesn't exist. |

### getRuntimeStats

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getRuntimeStats(): MutableMap<String!, String!>!
```

Returns a map of the names/values of the runtime statistics that [getRuntimeStat(java.lang.String)](Debug.md))supports.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | a map of the names/values of the supported runtime statistics. |

### getThreadAllocCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getThreadAllocCount(): Int
```

**Deprecated:** *Accurate counting is a burden on the runtime and may be removed.*

Returns the thread-local count of objects allocated by the runtime between a [start](Debug.md))and [stop](Debug.md)). 

### getThreadAllocSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getThreadAllocSize(): Int
```

**Deprecated:** *Accurate counting is a burden on the runtime and may be removed.*

Returns the thread-local size of objects allocated by the runtime between a [start](Debug.md))and [stop](Debug.md)).

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The allocated size in bytes. |

### getThreadExternalAllocCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getThreadExternalAllocCount(): Int
```

**Deprecated:** *This method is now obsolete.*

This method exists for compatibility and has no effect. 

### getThreadExternalAllocSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getThreadExternalAllocSize(): Int
```

**Deprecated:** *This method is now obsolete.*

This method exists for compatibility and has no effect. 

### getThreadGcInvocationCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getThreadGcInvocationCount(): Int
```

**Deprecated:** *Accurate counting is a burden on the runtime and may be removed.*

Returns the number of thread-local non-concurrent GC invocations between a [start](Debug.md))and [stop](Debug.md)). 

### isDebuggerConnected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isDebuggerConnected(): Boolean
```

Determine if a debugger is currently attached. 

### printLoadedClasses

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun printLoadedClasses(flags: Int): Unit
```

Dump a list of all currently loaded class to the log file.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):See constants above. |

### resetAllCounts

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun resetAllCounts(): Unit
```

**Deprecated:** *Accurate counting is a burden on the runtime and may be removed.*

Clears all the global and thread-local memory allocation counters. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/os/Debug#startAllocCounting()> 

### resetGlobalAllocCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun resetGlobalAllocCount(): Unit
```

**Deprecated:** *Accurate counting is a burden on the runtime and may be removed.*

Clears the global count of objects allocated. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/os/Debug#getGlobalAllocCount()> 

### resetGlobalAllocSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun resetGlobalAllocSize(): Unit
```

**Deprecated:** *Accurate counting is a burden on the runtime and may be removed.*

Clears the global size of objects allocated. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/os/Debug#getGlobalAllocSize()> 

### resetGlobalClassInitCount

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun resetGlobalClassInitCount(): Unit
```

**Deprecated:** *Accurate counting is a burden on the runtime and may be removed.*

Clears the count of classes initialized. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/os/Debug#getGlobalClassInitCount()> 

### resetGlobalClassInitTime

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun resetGlobalClassInitTime(): Unit
```

**Deprecated:** *Accurate counting is a burden on the runtime and may be removed.*

Clears the count of time spent initializing classes. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/os/Debug#getGlobalClassInitTime()> 

### resetGlobalExternalAllocCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun resetGlobalExternalAllocCount(): Unit
```

**Deprecated:** *This method is now obsolete.*

This method exists for compatibility and has no effect. 

### resetGlobalExternalAllocSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun resetGlobalExternalAllocSize(): Unit
```

**Deprecated:** *This method is now obsolete.*

This method exists for compatibility and has no effect. 

### resetGlobalExternalFreedCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun resetGlobalExternalFreedCount(): Unit
```

**Deprecated:** *This method is now obsolete.*

This method exists for compatibility and has no effect. 

### resetGlobalExternalFreedSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun resetGlobalExternalFreedSize(): Unit
```

**Deprecated:** *This method is now obsolete.*

This method exists for compatibility and has no effect. 

### resetGlobalFreedCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun resetGlobalFreedCount(): Unit
```

**Deprecated:** *Accurate counting is a burden on the runtime and may be removed.*

Clears the global count of objects freed. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/os/Debug#getGlobalFreedCount()> 

### resetGlobalFreedSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun resetGlobalFreedSize(): Unit
```

**Deprecated:** *Accurate counting is a burden on the runtime and may be removed.*

Clears the global size of objects freed. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/os/Debug#getGlobalFreedSize()> 

### resetGlobalGcInvocationCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun resetGlobalGcInvocationCount(): Unit
```

**Deprecated:** *Accurate counting is a burden on the runtime and may be removed.*

Clears the count of non-concurrent GC invocations. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/os/Debug#getGlobalGcInvocationCount()> 

### resetThreadAllocCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun resetThreadAllocCount(): Unit
```

**Deprecated:** *Accurate counting is a burden on the runtime and may be removed.*

Clears the thread-local count of objects allocated. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/os/Debug#getThreadAllocCount()> 

### resetThreadAllocSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun resetThreadAllocSize(): Unit
```

**Deprecated:** *Accurate counting is a burden on the runtime and may be removed.*

Clears the thread-local count of objects allocated. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/os/Debug#getThreadAllocSize()> 

### resetThreadExternalAllocCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun resetThreadExternalAllocCount(): Unit
```

**Deprecated:** *This method is now obsolete.*

This method exists for compatibility and has no effect. 

### resetThreadExternalAllocSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun resetThreadExternalAllocSize(): Unit
```

**Deprecated:** *This method is now obsolete.*

This method exists for compatibility and has no effect. 

### resetThreadGcInvocationCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun resetThreadGcInvocationCount(): Unit
```

**Deprecated:** *Accurate counting is a burden on the runtime and may be removed.*

Clears the thread-local count of non-concurrent GC invocations. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/os/Debug#getThreadGcInvocationCount()> 

### setAllocationLimit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setAllocationLimit(limit: Int): Int
```

**Deprecated:** *This method is now obsolete.*

Establish an object allocation limit in the current thread. This feature was never enabled in release builds. The allocation limits feature was removed in Honeycomb. This method exists for compatibility and always returns -1 and has no effect. 

### setGlobalAllocationLimit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setGlobalAllocationLimit(limit: Int): Int
```

**Deprecated:** *This method is now obsolete.*

Establish a global object allocation limit. This feature was never enabled in release builds. The allocation limits feature was removed in Honeycomb. This method exists for compatibility and always returns -1 and has no effect. 

### startAllocCounting

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun startAllocCounting(): Unit
```

**Deprecated:** *Accurate counting is a burden on the runtime and may be removed.*

Start counting the number and aggregate size of memory allocations.

The [start](Debug.md))method resets the counts and enables counting. The [stop](Debug.md))method disables the counting so that the analysis code doesn't cause additional allocations. The various`get`methods return the specified value. And the various`reset`methods reset the specified count.

Counts are kept for the system as a whole (global) and for each thread. The per-thread counts for threads other than the current thread are not cleared by the "reset" or "start" calls. 

### startMethodTracing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun startMethodTracing(): Unit
```

Start method tracing with default log name and buffer size.

By default, the trace file is called "dmtrace.trace" and it's placed under your package-specific directory on primary shared/external storage, as returned by [Context.getExternalFilesDir(String)](../android.content/Context.md)).

See [Inspect Trace Logs with Traceview](https://developer.android.com/studio/profile/traceview.html) for information about reading trace files.

When method tracing is enabled, the VM will run more slowly than usual, so the timings from the trace files should only be considered in relative terms (e.g. was run #1 faster than run #2). The times for native methods will not change, so don't try to use this to compare the performance of interpreted and native implementations of the same method. As an alternative, consider using sampling-based method tracing via [startMethodTracingSampling(java.lang.String,int,int)](Debug.md))or "native" tracing in the emulator via [startNativeTracing()](Debug.md)). 

### startMethodTracing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun startMethodTracing(tracePath: String!): Unit
```

Start method tracing, specifying the trace log file path.

When a relative file path is given, the trace file will be placed under your package-specific directory on primary shared/external storage, as returned by [Context.getExternalFilesDir(String)](../android.content/Context.md)).

See [Inspect Trace Logs with Traceview](https://developer.android.com/studio/profile/traceview.html) for information about reading trace files.

When method tracing is enabled, the VM will run more slowly than usual, so the timings from the trace files should only be considered in relative terms (e.g. was run #1 faster than run #2). The times for native methods will not change, so don't try to use this to compare the performance of interpreted and native implementations of the same method. As an alternative, consider using sampling-based method tracing via [startMethodTracingSampling(java.lang.String,int,int)](Debug.md))or "native" tracing in the emulator via [startNativeTracing()](Debug.md)).

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tracePath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Path to the trace log file to create. If`null`, this will default to "dmtrace.trace". If the file already exists, it will be truncated. If the path given does not end in ".trace", it will be appended for you. |

### startMethodTracing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun startMethodTracing(
    tracePath: String!, 
    bufferSize: Int
): Unit
```

Start method tracing, specifying the trace log file name and the buffer size.

When a relative file path is given, the trace file will be placed under your package-specific directory on primary shared/external storage, as returned by [Context.getExternalFilesDir(String)](../android.content/Context.md)).

See [Inspect Trace Logs with Traceview](https://developer.android.com/studio/profile/traceview.html) for information about reading trace files.

When method tracing is enabled, the VM will run more slowly than usual, so the timings from the trace files should only be considered in relative terms (e.g. was run #1 faster than run #2). The times for native methods will not change, so don't try to use this to compare the performance of interpreted and native implementations of the same method. As an alternative, consider using sampling-based method tracing via [startMethodTracingSampling(java.lang.String,int,int)](Debug.md))or "native" tracing in the emulator via [startNativeTracing()](Debug.md)).

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tracePath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Path to the trace log file to create. If`null`, this will default to "dmtrace.trace". If the file already exists, it will be truncated. If the path given does not end in ".trace", it will be appended for you. |
| `bufferSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum amount of trace data we gather. If not given, it defaults to 8MB. |

### startMethodTracing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun startMethodTracing(
    tracePath: String!, 
    bufferSize: Int, 
    flags: Int
): Unit
```

Start method tracing, specifying the trace log file name, the buffer size, and flags.

When a relative file path is given, the trace file will be placed under your package-specific directory on primary shared/external storage, as returned by [Context.getExternalFilesDir(String)](../android.content/Context.md)).

See [Inspect Trace Logs with Traceview](https://developer.android.com/studio/profile/traceview.html) for information about reading trace files.

When method tracing is enabled, the VM will run more slowly than usual, so the timings from the trace files should only be considered in relative terms (e.g. was run #1 faster than run #2). The times for native methods will not change, so don't try to use this to compare the performance of interpreted and native implementations of the same method. As an alternative, consider using sampling-based method tracing via [startMethodTracingSampling(java.lang.String,int,int)](Debug.md))or "native" tracing in the emulator via [startNativeTracing()](Debug.md)).

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tracePath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Path to the trace log file to create. If`null`, this will default to "dmtrace.trace". If the file already exists, it will be truncated. If the path given does not end in ".trace", it will be appended for you. |
| `bufferSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum amount of trace data we gather. If not given, it defaults to 8MB. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Flags to control method tracing. The following flags are supported: 0x0001 [TRACE_COUNT_ALLOCS](Debug.md) Flags to control time source: These are available with API #34 and higher. 0x0010 Report the elapsed time since the start of the trace. 0x0100 Report the time the thread has spent on the CPU since the start of the trace. Please note that the thread cpu incurs a significant (typically 2-3x) performance penalty. Use this flag only when necessary. If neither of these flags are set, both the elapsed time and the thread cpu time are reported. |
| --- | --- |

### startMethodTracingSampling

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun startMethodTracingSampling(
    tracePath: String!, 
    bufferSize: Int, 
    intervalUs: Int
): Unit
```

Start sampling-based method tracing, specifying the trace log file name, the buffer size, and the sampling interval.

When a relative file path is given, the trace file will be placed under your package-specific directory on primary shared/external storage, as returned by [Context.getExternalFilesDir(String)](../android.content/Context.md)).

See [Inspect Trace Logs with Traceview](https://developer.android.com/studio/profile/traceview.html) for information about reading trace files.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tracePath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Path to the trace log file to create. If`null`, this will default to "dmtrace.trace". If the file already exists, it will be truncated. If the path given does not end in ".trace", it will be appended for you. |
| `bufferSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum amount of trace data we gather. If not given, it defaults to 8MB. |
| `intervalUs` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The amount of time between each sample in microseconds. |
| --- | --- |

### startNativeTracing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun startNativeTracing(): Unit
```

Enable qemu tracing. For this to work requires running everything inside the qemu emulator; otherwise, this method will have no effect. The trace file is specified on the command line when the emulator is started. For example, the following command line 
`emulator -trace foo` 
will start running the emulator and create a trace file named "foo". This method simply enables writing the trace records to the trace file.

The main differences between this and [startMethodTracing()](Debug.md))are that tracing in the qemu emulator traces every cpu instruction of every process, including kernel code, so we have more complete information, including all context switches. We can also get more detailed information such as cache misses. The sequence of calls is determined by post-processing the instruction trace. The qemu tracing is also done without modifying the application or perturbing the timing of calls because no instrumentation is added to the application being traced.

One limitation of using this method compared to using [startMethodTracing()](Debug.md))on the real device is that the emulator does not model all of the real hardware effects such as memory and bus contention. The emulator also has a simple cache model and cannot capture all the complexities of a real cache. 

### stopAllocCounting

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun stopAllocCounting(): Unit
```

**Deprecated:** *Accurate counting is a burden on the runtime and may be removed.*

Stop counting the number and aggregate size of memory allocations. 

### stopMethodTracing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun stopMethodTracing(): Unit
```

Stop method tracing. 

### stopNativeTracing

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun stopNativeTracing(): Unit
```

Stop qemu tracing. See [startNativeTracing()](Debug.md))to start tracing.

Tracing can be started and stopped as many times as desired. When the qemu emulator itself is stopped then the buffered trace records are flushed and written to the trace file. In fact, it is not necessary to call this method at all; simply killing qemu is sufficient. But starting and stopping a trace is useful for examining a specific region of code. 

### threadCpuTimeNanos

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun threadCpuTimeNanos(): Long
```

Get an indication of thread CPU usage. The value returned indicates the amount of time that the current thread has spent executing code or waiting for certain types of I/O. The time is expressed in nanoseconds, and is only meaningful when compared to the result from an earlier call. Note that nanosecond resolution does not imply nanosecond accuracy. On system which don't support this operation, the call returns -1. 

### waitForDebugger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun waitForDebugger(): Unit
```

Wait until a debugger attaches. As soon as the debugger attaches, this returns, so you will need to place a breakpoint after the waitForDebugger() call if you want to start tracing immediately. 

### waitingForDebugger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun waitingForDebugger(): Boolean
```

Returns "true" if one or more threads is waiting for a debugger to attach.
