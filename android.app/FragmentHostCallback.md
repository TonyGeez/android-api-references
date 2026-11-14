Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FragmentHostCallback

Kotlin | [Java](FragmentHostCallback.md)
| --- | --- |

```
abstract class FragmentHostCallback<E : Any!> : FragmentContainer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.app.FragmentContainer](FragmentContainer.md) ||
| | ↳ | [android.app.FragmentHostCallback](FragmentHostCallback.md) |

| **This class was deprecated in API level 28.**
|
| Use the [Support Library](https://developer.android.com/tools/extras/support-library.html) androidx.fragment.app.FragmentHostCallback

Integration points with the Fragment host.

Fragments may be hosted by any object; such as an Activity. In order to host fragments, implement FragmentHostCallback, overriding the methods applicable to the host.

## Summary

| Public constructors ||
|---|---|
| FragmentHostCallback <br /> |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onAttachFragment Called when a Fragment is being attached to this host, immediately after the call to its onAttach method and before onCreate. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onDump Print internal state into the given stream. |
| open T? | onFindViewById Return the view with the given resource ID. |
| --- | --- |
| abstract E? | onGetHost Return the object that's currently hosting the fragment. |
| open [LayoutInflater](../android.view/LayoutInflater.md)! | onGetLayoutInflater Return a `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | onGetWindowAnimations Return the window animations. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onHasView Return `true` if the container holds any view. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onHasWindowAnimations Return `true` if there are window animations. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onInvalidateOptionsMenu Invalidates the activity's options menu. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onRequestPermissionsFromFragment Requests permissions from the given fragment. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onShouldSaveFragmentState Return `true` if the fragment's state needs to be saved. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onStartActivityFromFragment Starts a new Activity from the given fragment. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onStartIntentSenderFromFragment Starts a new `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` from the given fragment. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onUseFragmentManagerInflaterFactory Return `true` if the FragmentManager's LayoutInflaterFactory should be used. |

## Public constructors

### FragmentHostCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
FragmentHostCallback(
    context: Context!, 
    handler: Handler!, 
    windowAnimations: Int)
```

## Public methods

### onAttachFragment

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onAttachFragment(fragment: Fragment!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when a Fragment is being attached to this host, immediately after the call to its onAttach method and before onCreate.

### onDump

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onDump(
    prefix: String!, 
    fd: FileDescriptor!, 
    writer: PrintWriter!, 
    args: Array<String!>!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Print internal state into the given stream.

| Parameters ||
|---|---|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Desired prefix to prepend at each line of output. |
| `fd` | [FileDescriptor](../java.io/FileDescriptor.md)!: The raw file descriptor that the dump is being sent to. |
| `writer` | [PrintWriter](../java.io/PrintWriter.md)!: The PrintWriter to which you should dump your state. This will be closed for you after you return. |
| --- | --- |
| `args` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: additional arguments to the dump request. |

### onFindViewById

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <T : View!> onFindViewById(id: Int): T?
```

**Deprecated:** *Deprecated in Java.*

Return the view with the given resource ID. May return `null` if the view is not a child of this container.

| Return ||
|---|---|
| `T?` | This value may be `null`. |

### onGetHost

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onGetHost(): E?
```

**Deprecated:** *Deprecated in Java.*

Return the object that's currently hosting the fragment. If a Fragment is hosted by a Activity, the object returned here should be the same object returned from getActivity.

| Return ||
|---|---|
| `E?` | This value may be `null`. |

### onGetLayoutInflater

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onGetLayoutInflater(): LayoutInflater!
```

**Deprecated:** *Deprecated in Java.*

Return a `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#`. See getLayoutInflater.

### onGetWindowAnimations

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onGetWindowAnimations(): Int
```

**Deprecated:** *Deprecated in Java.*

Return the window animations.

### onHasView

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onHasView(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Return `true` if the container holds any view.

### onHasWindowAnimations

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onHasWindowAnimations(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Return `true` if there are window animations.

### onInvalidateOptionsMenu

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onInvalidateOptionsMenu(): Unit
```

**Deprecated:** *Deprecated in Java.*

Invalidates the activity's options menu. See invalidateOptionsMenu

### onRequestPermissionsFromFragment

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onRequestPermissionsFromFragment(
    fragment: Fragment, 
    permissions: Array<String!>, 
    requestCode: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Requests permissions from the given fragment. See requestPermissions

| Parameters ||
|---|---|
| `fragment` | [Fragment](Fragment.md): This value cannot be `null`. |
| `permissions` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: This value cannot be `null`. |

### onShouldSaveFragmentState

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onShouldSaveFragmentState(fragment: Fragment!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Return `true` if the fragment's state needs to be saved.

### onStartActivityFromFragment

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onStartActivityFromFragment(
    fragment: Fragment!, 
    intent: Intent!, 
    requestCode: Int, 
    options: Bundle!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Starts a new Activity from the given fragment. See startActivityForResult.

### onStartIntentSenderFromFragment

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onStartIntentSenderFromFragment(
    fragment: Fragment!, 
    intent: IntentSender!, 
    requestCode: Int, 
    fillInIntent: Intent?, 
    flagsMask: Int, 
    flagsValues: Int, 
    extraFlags: Int, 
    options: Bundle!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Starts a new `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` from the given fragment. See android.app.Activity#startIntentSender(android.content.IntentSender,android.content.Intent,int,int,int,android.os.Bundle).

| Parameters ||
|---|---|
| `fillInIntent` | [Intent](../android.content/Intent.md)?: This value may be `null`. |

### onUseFragmentManagerInflaterFactory

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onUseFragmentManagerInflaterFactory(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Return `true` if the FragmentManager's LayoutInflaterFactory should be used.
