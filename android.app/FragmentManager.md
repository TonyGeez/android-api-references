Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FragmentManager

Kotlin | [Java](https://developer.android.com/reference/android/app/FragmentManager "View this page in Java")

```
abstract class FragmentManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.FragmentManager](https://developer.android.com/reference/kotlin/android/app/FragmentManager#) |

> [!CAUTION]
> **This class was deprecated in API level 28.**
>
> Use the [Support Library](https://developer.android.com/tools/extras/support-library.html) androidx.fragment.app.FragmentManager for consistent behavior across all devices and access to [Lifecycle](https://developer.android.com/topic/libraries/architecture/lifecycle.html).

Interface for interacting with `https://developer.android.com/reference/kotlin/android/app/Fragment` objects inside of an `https://developer.android.com/reference/kotlin/android/app/Activity`

> [!NOTE]
>
> ### Developer Guides
>
> For more information about using fragments, read the [Fragments](https://developer.android.com/guide/components/fragments.html) developer guide.

While the FragmentManager API was introduced in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int`, a version of the API at is also available for use on older platforms through androidx.fragment.app.FragmentActivity. See the blog post [Fragments For All](http://android-developers.blogspot.com/2011/03/fragments-for-all.html) for more details.

<br />

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/app/FragmentManager.BackStackEntry` Representation of an entry on the fragment back stack, as created with `https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#addToBackStack(kotlin.String)`. |
| abstract | `https://developer.android.com/reference/kotlin/android/app/FragmentManager.FragmentLifecycleCallbacks` Callback interface for listening to fragment state changes that happen within a given FragmentManager. |
| abstract | `https://developer.android.com/reference/kotlin/android/app/FragmentManager.OnBackStackChangedListener` Interface to watch for changes to the back stack. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#POP_BACK_STACK_INCLUSIVE:kotlin.Int` Flag for `https://developer.android.com/reference/kotlin/android/app/FragmentManager#popBackStack(kotlin.String,%20kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/app/FragmentManager#popBackStack(kotlin.Int,%20kotlin.Int)`: If set, and the name or ID of a back stack entry has been supplied, then all matching entries will be consumed until one that doesn't match is found or the bottom of the stack is reached. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/FragmentManager#FragmentManager()()` <br /> |

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#addOnBackStackChangedListener(android.app.FragmentManager.OnBackStackChangedListener)(listener: https://developer.android.com/reference/kotlin/android/app/FragmentManager.OnBackStackChangedListener!)` Add a new listener for changes to the fragment back stack. |
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction)! | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#beginTransaction()()` Start a series of edit operations on the Fragments associated with this FragmentManager. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#dump(kotlin.String,%20java.io.FileDescriptor,%20java.io.PrintWriter,%20kotlin.Array)(prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, writer: https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#!, args: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Print the FragmentManager's state into the given stream. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#enableDebugLogging(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Control whether the framework's internal fragment manager debugging logs are turned on. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#executePendingTransactions()()` After a `https://developer.android.com/reference/kotlin/android/app/FragmentTransaction` is committed with `https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#commit()`, it is scheduled to be executed asynchronously on the process's main thread. |
| abstract [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)! | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#findFragmentById(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Finds a fragment that was identified by the given id either when inflated from XML or as the container ID when added in a transaction. |
| abstract [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)! | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#findFragmentByTag(kotlin.String)(tag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Finds a fragment that was identified by the given tag either when inflated from XML or as supplied when added in a transaction. |
| abstract [FragmentManager.BackStackEntry](https://developer.android.com/reference/kotlin/android/app/FragmentManager.BackStackEntry)! | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#getBackStackEntryAt(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the BackStackEntry at index index in the back stack; where the item on the bottom of the stack has index 0. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#getBackStackEntryCount()()` Return the number of entries currently in the back stack. |
| abstract [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)! | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#getFragment(android.os.Bundle,%20kotlin.String)(bundle: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!, key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Retrieve the current Fragment instance for a reference previously placed with `https://developer.android.com/reference/kotlin/android/app/FragmentManager#putFragment(android.os.Bundle,%20kotlin.String,%20android.app.Fragment)`. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!\>! | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#getFragments()()` Get a list of all fragments that are currently added to the FragmentManager. |
| abstract [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)! | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#getPrimaryNavigationFragment()()` Return the currently active primary navigation fragment for this FragmentManager. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#invalidateOptionsMenu()()` Invalidate the attached activity's options menu as necessary. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#isDestroyed()()` Returns true if the final `https://developer.android.com/reference/kotlin/android/app/Activity#onDestroy()` call has been made on the FragmentManager's Activity, so this instance is now dead. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#isStateSaved()()` Returns `true` if the FragmentManager's state has already been saved by its host. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#popBackStack()()` Pop the top state off the back stack. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#popBackStack(kotlin.Int,%20kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Pop all back stack states up to the one with the given identifier. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#popBackStack(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Pop the last fragment transition from the manager's fragment back stack. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#popBackStackImmediate()()` Like `https://developer.android.com/reference/kotlin/android/app/FragmentManager#popBackStack()`, but performs the operation immediately inside of the call. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#popBackStackImmediate(kotlin.Int,%20kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Like `https://developer.android.com/reference/kotlin/android/app/FragmentManager#popBackStack(kotlin.Int,%20kotlin.Int)`, but performs the operation immediately inside of the call. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#popBackStackImmediate(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Like `https://developer.android.com/reference/kotlin/android/app/FragmentManager#popBackStack(kotlin.String,%20kotlin.Int)`, but performs the operation immediately inside of the call. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#putFragment(android.os.Bundle,%20kotlin.String,%20android.app.Fragment)(bundle: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!, key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, fragment: https://developer.android.com/reference/kotlin/android/app/Fragment!)` Put a reference to a fragment in a Bundle. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#registerFragmentLifecycleCallbacks(android.app.FragmentManager.FragmentLifecycleCallbacks,%20kotlin.Boolean)(cb: https://developer.android.com/reference/kotlin/android/app/FragmentManager.FragmentLifecycleCallbacks!, recursive: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Registers a `https://developer.android.com/reference/kotlin/android/app/FragmentManager.FragmentLifecycleCallbacks` to listen to fragment lifecycle events happening in this FragmentManager. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#removeOnBackStackChangedListener(android.app.FragmentManager.OnBackStackChangedListener)(listener: https://developer.android.com/reference/kotlin/android/app/FragmentManager.OnBackStackChangedListener!)` Remove a listener that was previously added with `https://developer.android.com/reference/kotlin/android/app/FragmentManager#addOnBackStackChangedListener(android.app.FragmentManager.OnBackStackChangedListener)`. |
| abstract [Fragment.SavedState](https://developer.android.com/reference/kotlin/android/app/Fragment.SavedState)! | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#saveFragmentInstanceState(android.app.Fragment)(f: https://developer.android.com/reference/kotlin/android/app/Fragment!)` Save the current instance state of the given Fragment. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentManager#unregisterFragmentLifecycleCallbacks(android.app.FragmentManager.FragmentLifecycleCallbacks)(cb: https://developer.android.com/reference/kotlin/android/app/FragmentManager.FragmentLifecycleCallbacks!)` Unregisters a previously registered `https://developer.android.com/reference/kotlin/android/app/FragmentManager.FragmentLifecycleCallbacks`. |

## Constants

### POP_BACK_STACK_INCLUSIVE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val POP_BACK_STACK_INCLUSIVE: Int
```

**Deprecated:** *Deprecated in Java.*

Flag for `https://developer.android.com/reference/kotlin/android/app/FragmentManager#popBackStack(kotlin.String,%20kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/app/FragmentManager#popBackStack(kotlin.Int,%20kotlin.Int)`: If set, and the name or ID of a back stack entry has been supplied, then all matching entries will be consumed until one that doesn't match is found or the bottom of the stack is reached. Otherwise, all entries up to but not including that entry will be removed.

 Value: 1

## Public constructors

### FragmentManager

```
FragmentManager()
```

## Public methods

### addOnBackStackChangedListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun addOnBackStackChangedListener(listener: FragmentManager.OnBackStackChangedListener!): Unit
```

**Deprecated:** *Deprecated in Java.*

Add a new listener for changes to the fragment back stack.

### beginTransaction

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun beginTransaction(): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Start a series of edit operations on the Fragments associated with this FragmentManager.

Note: A fragment transaction can only be created/committed prior to an activity saving its state. If you try to commit a transaction after android.app.Activity#onSaveInstanceState (and prior to a following `https://developer.android.com/reference/kotlin/android/app/Activity#onStart()` or `https://developer.android.com/reference/kotlin/android/app/Activity#onResume()`, you will get an error. This is because the framework takes care of saving your current fragments in the state, and if changes are made after the state is saved then they will be lost.

### dump

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun dump(
    prefix: String!, 
    fd: FileDescriptor!, 
    writer: PrintWriter!, 
    args: Array<String!>!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Print the FragmentManager's state into the given stream.

| Parameters ||
|---|---|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Text to print at the front of each line. |
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!: The raw file descriptor that the dump is being sent to. |
| `writer` | [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)!: A PrintWriter to which the dump is to be set. |
| `args` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: Additional arguments to the dump request. |

### enableDebugLogging

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun enableDebugLogging(enabled: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Control whether the framework's internal fragment manager debugging logs are turned on. If enabled, you will see output in logcat as the framework performs fragment operations.

### executePendingTransactions

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun executePendingTransactions(): Boolean
```

**Deprecated:** *Deprecated in Java.*

After a `https://developer.android.com/reference/kotlin/android/app/FragmentTransaction` is committed with `https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#commit()`, it is scheduled to be executed asynchronously on the process's main thread. If you want to immediately executing any such pending operations, you can call this function (only from the main thread) to do so. Note that all callbacks and other related behavior will be done from within this call, so be careful about where this is called from.

This also forces the start of any postponed Transactions where `https://developer.android.com/reference/kotlin/android/app/Fragment#postponeEnterTransition()` has been called.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if there were any pending transactions to be executed. |

### findFragmentById

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun findFragmentById(id: Int): Fragment!
```

**Deprecated:** *Deprecated in Java.*

Finds a fragment that was identified by the given id either when inflated from XML or as the container ID when added in a transaction. This first searches through fragments that are currently added to the manager's activity; if no such fragment is found, then all fragments currently on the back stack associated with this ID are searched.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/Fragment!` | The fragment if found or null otherwise. |

### findFragmentByTag

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun findFragmentByTag(tag: String!): Fragment!
```

**Deprecated:** *Deprecated in Java.*

Finds a fragment that was identified by the given tag either when inflated from XML or as supplied when added in a transaction. This first searches through fragments that are currently added to the manager's activity; if no such fragment is found, then all fragments currently on the back stack are searched.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/Fragment!` | The fragment if found or null otherwise. |

### getBackStackEntryAt

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getBackStackEntryAt(index: Int): FragmentManager.BackStackEntry!
```

**Deprecated:** *Deprecated in Java.*

Return the BackStackEntry at index index in the back stack; where the item on the bottom of the stack has index 0.

### getBackStackEntryCount

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getBackStackEntryCount(): Int
```

**Deprecated:** *Deprecated in Java.*

Return the number of entries currently in the back stack.

### getFragment

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getFragment(
    bundle: Bundle!, 
    key: String!
): Fragment!
```

**Deprecated:** *Deprecated in Java.*

Retrieve the current Fragment instance for a reference previously placed with `https://developer.android.com/reference/kotlin/android/app/FragmentManager#putFragment(android.os.Bundle,%20kotlin.String,%20android.app.Fragment)`.

| Parameters ||
|---|---|
| `bundle` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: The bundle from which to retrieve the fragment reference. |
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the entry in the bundle. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/Fragment!` | Returns the current Fragment instance that is associated with the given reference. |

### getFragments

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getFragments(): MutableList<Fragment!>!
```

**Deprecated:** *Deprecated in Java.*

Get a list of all fragments that are currently added to the FragmentManager. This may include those that are hidden as well as those that are shown. This will not include any fragments only in the back stack, or fragments that are detached or removed.

The order of the fragments in the list is the order in which they were added or attached.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/Fragment!>!` | A list of all fragments that are added to the FragmentManager. |

### getPrimaryNavigationFragment

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getPrimaryNavigationFragment(): Fragment!
```

**Deprecated:** *Deprecated in Java.*

Return the currently active primary navigation fragment for this FragmentManager.

The primary navigation fragment's `https://developer.android.com/reference/kotlin/android/app/Fragment#getChildFragmentManager()` will be called first to process delegated navigation actions such as `https://developer.android.com/reference/kotlin/android/app/FragmentManager#popBackStack()` if no ID or transaction name is provided to pop to.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/Fragment!` | the fragment designated as the primary navigation fragment |

### invalidateOptionsMenu

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun invalidateOptionsMenu(): Unit
```

**Deprecated:** *Deprecated in Java.*

Invalidate the attached activity's options menu as necessary. This may end up being deferred until we move to the resumed state.

### isDestroyed

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun isDestroyed(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if the final `https://developer.android.com/reference/kotlin/android/app/Activity#onDestroy()` call has been made on the FragmentManager's Activity, so this instance is now dead.

### isStateSaved

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun isStateSaved(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns `true` if the FragmentManager's state has already been saved by its host. Any operations that would change saved state should not be performed if this method returns true. For example, any popBackStack() method, such as `https://developer.android.com/reference/kotlin/android/app/FragmentManager#popBackStackImmediate()` or any FragmentTransaction using `https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#commit()` instead of `https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#commitAllowingStateLoss()` will change the state and will result in an error.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this FragmentManager's state has already been saved by its host |

### popBackStack

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun popBackStack(): Unit
```

**Deprecated:** *Deprecated in Java.*

Pop the top state off the back stack. This function is asynchronous -- it enqueues the request to pop, but the action will not be performed until the application returns to its event loop.

### popBackStack

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun popBackStack(
    id: Int, 
    flags: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Pop all back stack states up to the one with the given identifier. This function is asynchronous -- it enqueues the request to pop, but the action will not be performed until the application returns to its event loop.

| Parameters ||
|---|---|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Identifier of the stated to be popped. If no identifier exists, false is returned. The identifier is the number returned by `https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#commit()`. The `https://developer.android.com/reference/kotlin/android/app/FragmentManager#POP_BACK_STACK_INCLUSIVE:kotlin.Int` flag can be used to control whether the named state itself is popped. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Either 0 or `https://developer.android.com/reference/kotlin/android/app/FragmentManager#POP_BACK_STACK_INCLUSIVE:kotlin.Int`. |

### popBackStack

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun popBackStack(
    name: String!, 
    flags: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Pop the last fragment transition from the manager's fragment back stack. If there is nothing to pop, false is returned. This function is asynchronous -- it enqueues the request to pop, but the action will not be performed until the application returns to its event loop.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: If non-null, this is the name of a previous back state to look for; if found, all states up to that state will be popped. The `https://developer.android.com/reference/kotlin/android/app/FragmentManager#POP_BACK_STACK_INCLUSIVE:kotlin.Int` flag can be used to control whether the named state itself is popped. If null, only the top state is popped. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Either 0 or `https://developer.android.com/reference/kotlin/android/app/FragmentManager#POP_BACK_STACK_INCLUSIVE:kotlin.Int`. |

### popBackStackImmediate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun popBackStackImmediate(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Like `https://developer.android.com/reference/kotlin/android/app/FragmentManager#popBackStack()`, but performs the operation immediately inside of the call. This is like calling `https://developer.android.com/reference/kotlin/android/app/FragmentManager#executePendingTransactions()` afterwards without forcing the start of postponed Transactions.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if there was something popped, else false. |

### popBackStackImmediate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun popBackStackImmediate(
    id: Int, 
    flags: Int
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Like `https://developer.android.com/reference/kotlin/android/app/FragmentManager#popBackStack(kotlin.Int,%20kotlin.Int)`, but performs the operation immediately inside of the call. This is like calling `https://developer.android.com/reference/kotlin/android/app/FragmentManager#executePendingTransactions()` afterwards without forcing the start of postponed Transactions.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if there was something popped, else false. |

### popBackStackImmediate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun popBackStackImmediate(
    name: String!, 
    flags: Int
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Like `https://developer.android.com/reference/kotlin/android/app/FragmentManager#popBackStack(kotlin.String,%20kotlin.Int)`, but performs the operation immediately inside of the call. This is like calling `https://developer.android.com/reference/kotlin/android/app/FragmentManager#executePendingTransactions()` afterwards without forcing the start of postponed Transactions.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if there was something popped, else false. |

### putFragment

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun putFragment(
    bundle: Bundle!, 
    key: String!, 
    fragment: Fragment!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Put a reference to a fragment in a Bundle. This Bundle can be persisted as saved state, and when later restoring `https://developer.android.com/reference/kotlin/android/app/FragmentManager#getFragment(android.os.Bundle,%20kotlin.String)` will return the current instance of the same fragment.

| Parameters ||
|---|---|
| `bundle` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: The bundle in which to put the fragment reference. |
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the entry in the bundle. |
| `fragment` | [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!: The Fragment whose reference is to be stored. |

### registerFragmentLifecycleCallbacks

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun registerFragmentLifecycleCallbacks(
    cb: FragmentManager.FragmentLifecycleCallbacks!, 
    recursive: Boolean
): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers a `https://developer.android.com/reference/kotlin/android/app/FragmentManager.FragmentLifecycleCallbacks` to listen to fragment lifecycle events happening in this FragmentManager. All registered callbacks will be automatically unregistered when this FragmentManager is destroyed.

| Parameters ||
|---|---|
| `cb` | [FragmentManager.FragmentLifecycleCallbacks](https://developer.android.com/reference/kotlin/android/app/FragmentManager.FragmentLifecycleCallbacks)!: Callbacks to register |
| `recursive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to automatically register this callback for all child FragmentManagers |

### removeOnBackStackChangedListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun removeOnBackStackChangedListener(listener: FragmentManager.OnBackStackChangedListener!): Unit
```

**Deprecated:** *Deprecated in Java.*

Remove a listener that was previously added with `https://developer.android.com/reference/kotlin/android/app/FragmentManager#addOnBackStackChangedListener(android.app.FragmentManager.OnBackStackChangedListener)`.

### saveFragmentInstanceState

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun saveFragmentInstanceState(f: Fragment!): Fragment.SavedState!
```

**Deprecated:** *Deprecated in Java.*

Save the current instance state of the given Fragment. This can be used later when creating a new instance of the Fragment and adding it to the fragment manager, to have it create itself to match the current state returned here. Note that there are limits on how this can be used:

- The Fragment must currently be attached to the FragmentManager.
- A new Fragment created using this saved state must be the same class type as the Fragment it was created from.
- The saved state can not contain dependencies on other fragments -- that is it can't use `https://developer.android.com/reference/kotlin/android/app/FragmentManager#putFragment(android.os.Bundle,%20kotlin.String,%20android.app.Fragment)` to store a fragment reference because that reference may not be valid when this saved state is later used. Likewise the Fragment's target and result code are not included in this state.

<br />

| Parameters ||
|---|---|
| `f` | [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!: The Fragment whose state is to be saved. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/Fragment.SavedState!` | The generated state. This will be null if there was no interesting state created by the fragment. |

### unregisterFragmentLifecycleCallbacks

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun unregisterFragmentLifecycleCallbacks(cb: FragmentManager.FragmentLifecycleCallbacks!): Unit
```

**Deprecated:** *Deprecated in Java.*

Unregisters a previously registered `https://developer.android.com/reference/kotlin/android/app/FragmentManager.FragmentLifecycleCallbacks`. If the callback was not previously registered this call has no effect. All registered callbacks will be automatically unregistered when this FragmentManager is destroyed.

| Parameters ||
|---|---|
| `cb` | [FragmentManager.FragmentLifecycleCallbacks](https://developer.android.com/reference/kotlin/android/app/FragmentManager.FragmentLifecycleCallbacks)!: Callbacks to unregister |
