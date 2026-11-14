# CriticalNative

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CriticalNative

```
@Target([AnnotationTarget.FUNCTION, AnnotationTarget.PROPERTY_GETTER, AnnotationTarget.PROPERTY_SETTER]) class CriticalNative
```

| [dalvik.annotation.optimization.CriticalNative](CriticalNative.md) |

An ART runtime built-in optimization for `native` methods to speed up JNI transitions: Methods that are annotated with @`CriticalNative` use the fastest available JNI transitions from managed code to the native code and back. This annotation can be applied only to native methods that do not use managed objects (in parameters or return values, or as an implicit `this`).

The @`CriticalNative` annotation changes the JNI transition ABI. The native implementation must exclude the `JNIEnv` and `jclass` parameters from its function signature.

While executing a @`CriticalNative` method, the garbage collection cannot suspend the thread for essential work and may become blocked. Use with caution. Do not use this annotation for long-running methods, including usually-fast, but generally unbounded, methods. In particular, the code should not perform significant I/O operations or acquire native locks that can be held for a long time. Never acquire a native lock that can also be held while a thread invokes Java code. That virtually guarantees deadlocks. (Otherwise some logging or native allocations, which internally acquire native locks for a short time, are generally OK. However, as the cost of several such operations adds up, the @`CriticalNative` performance gain can become insignificant and overshadowed by potential GC delays.)

For performance critical methods that need this annotation, it is strongly recommended to explicitly register the method(s) with JNI `RegisterNatives` instead of relying on the built-in dynamic JNI linking.

The @`CriticalNative` optimization was implemented for system use since Android 8 and became CTS-tested public API in Android 14. Developers aiming for maximum compatibility should avoid calling @`CriticalNative` methods on Android 13-. The optimization is likely to work also on Android 8-13 devices (after all, it was used in the system, albeit without the strong CTS guarantees), especially those that use unmodified versions of ART, such as Android 12+ devices with the official ART Module. The built-in dynamic JNI linking is working only in Android 12+, the explicit registration with JNI `RegisterNatives` is strictly required for running on Android versions 8-11. The annotation is ignored on Android 7-, so the ABI mismatch would lead to wrong argument marshalling and likely crashes.

A similar annotation, @ [FastNative](FastNative.md), exists for methods that need fast transitions but absolutely need to use managed objects, whether as the implicit `this` for non-static methods, or method arguments, return values or to otherwise call back to managed code (say, static methods), or access managed heap objects (say, static fields).

Performance of JNI transitions:

- Regular JNI cost in nanoseconds: 115
- Fast `(!)` JNI cost in nanoseconds: 60
- @ [FastNative](FastNative.md) cost in nanoseconds: 35
- @`CriticalNative` cost in nanoseconds: 25

(Measured on angler-userdebug in 07/2016).

<br />

**Deadlock Warning:** As a rule of thumb, any native locks acquired in a @ [CriticalNative](CriticalNative.md) call (despite the above warning that this is an unbounded operation that can block GC for a long time) must be released before returning to managed code.

Say some code does: ` critical_native_call_to_grab_a_lock(); does_some_java_work(); critical_native_call_to_release_a_lock(); `

This code can lead to deadlocks. Say thread 1 just finishes `critical_native_call_to_grab_a_lock()` and is in `does_some_java_work()`. GC kicks in and suspends thread 1. Thread 2 now is in `critical_native_call_to_grab_a_lock()` but is blocked on grabbing the native lock since it's held by thread 1. Now thread suspension can't finish since thread 2 can't be suspended since it's doing CriticalNative JNI.

Normal natives don't have the issue since once it's executing in native code, it is considered suspended from the runtime's point of view. CriticalNative natives however don't do the state transition done by the normal natives.

This annotation has no effect when used with non-native methods.

The runtime shall throw a [java.lang.VerifyError](../java.lang/VerifyError.md) during verification if this annotation is present on a native method that is non-static, or contains object parameters, or returns an object.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CriticalNative](CriticalNative.md))`()` An ART runtime built-in optimization for `native` methods to speed up JNI transitions: Methods that are annotated with @`CriticalNative` use the fastest available JNI transitions from managed code to the native code and back. |

## Public constructors

### CriticalNative

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CriticalNative()
```

An ART runtime built-in optimization for `native` methods to speed up JNI transitions: Methods that are annotated with @`CriticalNative` use the fastest available JNI transitions from managed code to the native code and back. This annotation can be applied only to native methods that do not use managed objects (in parameters or return values, or as an implicit `this`).

The @`CriticalNative` annotation changes the JNI transition ABI. The native implementation must exclude the `JNIEnv` and `jclass` parameters from its function signature.

While executing a @`CriticalNative` method, the garbage collection cannot suspend the thread for essential work and may become blocked. Use with caution. Do not use this annotation for long-running methods, including usually-fast, but generally unbounded, methods. In particular, the code should not perform significant I/O operations or acquire native locks that can be held for a long time. Never acquire a native lock that can also be held while a thread invokes Java code. That virtually guarantees deadlocks. (Otherwise some logging or native allocations, which internally acquire native locks for a short time, are generally OK. However, as the cost of several such operations adds up, the @`CriticalNative` performance gain can become insignificant and overshadowed by potential GC delays.)

For performance critical methods that need this annotation, it is strongly recommended to explicitly register the method(s) with JNI `RegisterNatives` instead of relying on the built-in dynamic JNI linking.

The @`CriticalNative` optimization was implemented for system use since Android 8 and became CTS-tested public API in Android 14. Developers aiming for maximum compatibility should avoid calling @`CriticalNative` methods on Android 13-. The optimization is likely to work also on Android 8-13 devices (after all, it was used in the system, albeit without the strong CTS guarantees), especially those that use unmodified versions of ART, such as Android 12+ devices with the official ART Module. The built-in dynamic JNI linking is working only in Android 12+, the explicit registration with JNI `RegisterNatives` is strictly required for running on Android versions 8-11. The annotation is ignored on Android 7-, so the ABI mismatch would lead to wrong argument marshalling and likely crashes.

A similar annotation, @ [FastNative](FastNative.md), exists for methods that need fast transitions but absolutely need to use managed objects, whether as the implicit `this` for non-static methods, or method arguments, return values or to otherwise call back to managed code (say, static methods), or access managed heap objects (say, static fields).

Performance of JNI transitions:

- Regular JNI cost in nanoseconds: 115
- Fast `(!)` JNI cost in nanoseconds: 60
- @ [FastNative](FastNative.md) cost in nanoseconds: 35
- @`CriticalNative` cost in nanoseconds: 25

(Measured on angler-userdebug in 07/2016).

<br />

**Deadlock Warning:** As a rule of thumb, any native locks acquired in a @ [CriticalNative](CriticalNative.md) call (despite the above warning that this is an unbounded operation that can block GC for a long time) must be released before returning to managed code.

Say some code does: ` critical_native_call_to_grab_a_lock(); does_some_java_work(); critical_native_call_to_release_a_lock(); `

This code can lead to deadlocks. Say thread 1 just finishes `critical_native_call_to_grab_a_lock()` and is in `does_some_java_work()`. GC kicks in and suspends thread 1. Thread 2 now is in `critical_native_call_to_grab_a_lock()` but is blocked on grabbing the native lock since it's held by thread 1. Now thread suspension can't finish since thread 2 can't be suspended since it's doing CriticalNative JNI.

Normal natives don't have the issue since once it's executing in native code, it is considered suspended from the runtime's point of view. CriticalNative natives however don't do the state transition done by the normal natives.

This annotation has no effect when used with non-native methods.

The runtime shall throw a [java.lang.VerifyError](../java.lang/VerifyError.md) during verification if this annotation is present on a native method that is non-static, or contains object parameters, or returns an object.
