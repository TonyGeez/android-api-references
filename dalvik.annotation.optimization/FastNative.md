# FastNative

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FastNative

```
@Target([AnnotationTarget.FUNCTION, AnnotationTarget.PROPERTY_GETTER, AnnotationTarget.PROPERTY_SETTER]) class FastNative
```

| [dalvik.annotation.optimization.FastNative](https://developer.android.com/reference/kotlin/dalvik/annotation/optimization/FastNative#) |

An ART runtime built-in optimization for`native`methods to speed up JNI transitions: Compared to normal`native`methods,`native`methods that are annotated with @`FastNative`use faster JNI transitions from managed code to the native code and back. Calls from a @`FastNative`method implementation to JNI functions that access the managed heap or call managed code also have faster internal transitions.

While executing a @`FastNative`method, the garbage collection cannot suspend the thread for essential work and may become blocked. Use with caution. Do not use this annotation for long-running methods, including usually-fast, but generally unbounded, methods. In particular, the code should not perform significant I/O operations or acquire native locks that can be held for a long time. Never acquire a native lock that can also be held while a thread invokes Java code. That virtually guarantees deadlocks. (Otherwise some logging or native allocations, which internally acquire native locks for a short time, are generally OK. However, as the cost of several such operations adds up, the @`FastNative`performance gain can become insignificant and overshadowed by potential GC delays.) Acquiring managed locks is OK as it internally allows thread suspension.

For performance critical methods that need this annotation, it is strongly recommended to explicitly register the method(s) with JNI`RegisterNatives`instead of relying on the built-in dynamic JNI linking.

The @`FastNative`optimization was implemented for system use since Android 8 and became CTS-tested public API in Android 14. Developers aiming for maximum compatibility should avoid calling @`FastNative`methods on Android 13-. The optimization is likely to work also on Android 8-13 devices (after all, it was used in the system, albeit without the strong CTS guarantees), especially those that use unmodified versions of ART, such as Android 12+ devices with the official ART Module. The built-in dynamic JNI linking is working only in Android 12+, the explicit registration with JNI`RegisterNatives`is strictly required for running on Android versions 8-11. The annotation is ignored on Android 7-.

**Deadlock Warning:** As a rule of thumb, any native locks acquired in a @ [FastNative](https://developer.android.com/reference/kotlin/dalvik/annotation/optimization/FastNative#) call (despite the above warning that this is an unbounded operation that can block GC for a long time) must be released before returning to managed code.

Say some code does:` fast_jni_call_to_grab_a_lock(); does_some_java_work(); fast_jni_call_to_release_a_lock(); `

This code can lead to deadlocks. Say thread 1 just finishes`fast_jni_call_to_grab_a_lock()`and is in`does_some_java_work()`. GC kicks in and suspends thread 1. Thread 2 now is in`fast_jni_call_to_grab_a_lock()`but is blocked on grabbing the native lock since it's held by thread 1. Now thread suspension can't finish since thread 2 can't be suspended since it's doing FastNative JNI.

Normal JNI doesn't have the issue since once it's in native code, it is considered suspended from java's point of view. FastNative JNI however doesn't do the state transition done by JNI.

Note that even in FastNative methods you**are**allowed to allocate objects and make upcalls into Java code. A call from Java to a FastNative function and back to Java is equivalent to a call from one Java method to another. What's forbidden in a FastNative method is blocking the calling thread in some non-Java code and thereby preventing the thread from responding to requests from the garbage collector to enter the suspended state.

Has no effect when used with non-native methods.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FastNative](https://developer.android.com/reference/kotlin/dalvik/annotation/optimization/FastNative#FastNative())`()` An ART runtime built-in optimization for`native`methods to speed up JNI transitions: Compared to normal`native`methods,`native`methods that are annotated with @`FastNative`use faster JNI transitions from managed code to the native code and back. |

## Public constructors

### FastNative

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FastNative()
```

An ART runtime built-in optimization for`native`methods to speed up JNI transitions: Compared to normal`native`methods,`native`methods that are annotated with @`FastNative`use faster JNI transitions from managed code to the native code and back. Calls from a @`FastNative`method implementation to JNI functions that access the managed heap or call managed code also have faster internal transitions.

While executing a @`FastNative`method, the garbage collection cannot suspend the thread for essential work and may become blocked. Use with caution. Do not use this annotation for long-running methods, including usually-fast, but generally unbounded, methods. In particular, the code should not perform significant I/O operations or acquire native locks that can be held for a long time. Never acquire a native lock that can also be held while a thread invokes Java code. That virtually guarantees deadlocks. (Otherwise some logging or native allocations, which internally acquire native locks for a short time, are generally OK. However, as the cost of several such operations adds up, the @`FastNative`performance gain can become insignificant and overshadowed by potential GC delays.) Acquiring managed locks is OK as it internally allows thread suspension.

For performance critical methods that need this annotation, it is strongly recommended to explicitly register the method(s) with JNI`RegisterNatives`instead of relying on the built-in dynamic JNI linking.

The @`FastNative`optimization was implemented for system use since Android 8 and became CTS-tested public API in Android 14. Developers aiming for maximum compatibility should avoid calling @`FastNative`methods on Android 13-. The optimization is likely to work also on Android 8-13 devices (after all, it was used in the system, albeit without the strong CTS guarantees), especially those that use unmodified versions of ART, such as Android 12+ devices with the official ART Module. The built-in dynamic JNI linking is working only in Android 12+, the explicit registration with JNI`RegisterNatives`is strictly required for running on Android versions 8-11. The annotation is ignored on Android 7-.

**Deadlock Warning:** As a rule of thumb, any native locks acquired in a @ [FastNative](https://developer.android.com/reference/kotlin/dalvik/annotation/optimization/FastNative#) call (despite the above warning that this is an unbounded operation that can block GC for a long time) must be released before returning to managed code.

Say some code does:` fast_jni_call_to_grab_a_lock(); does_some_java_work(); fast_jni_call_to_release_a_lock(); `

This code can lead to deadlocks. Say thread 1 just finishes`fast_jni_call_to_grab_a_lock()`and is in`does_some_java_work()`. GC kicks in and suspends thread 1. Thread 2 now is in`fast_jni_call_to_grab_a_lock()`but is blocked on grabbing the native lock since it's held by thread 1. Now thread suspension can't finish since thread 2 can't be suspended since it's doing FastNative JNI.

Normal JNI doesn't have the issue since once it's in native code, it is considered suspended from java's point of view. FastNative JNI however doesn't do the state transition done by JNI.

Note that even in FastNative methods you**are**allowed to allocate objects and make upcalls into Java code. A call from Java to a FastNative function and back to Java is equivalent to a call from one Java method to another. What's forbidden in a FastNative method is blocking the calling thread in some non-Java code and thereby preventing the thread from responding to requests from the garbage collector to enter the suspended state.

Has no effect when used with non-native methods.
