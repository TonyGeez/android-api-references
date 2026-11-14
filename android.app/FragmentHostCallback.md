Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FragmentHostCallback

Kotlin | [Java](https://developer.android.com/reference/android/app/FragmentHostCallback "View this page in Java")
| --- | --- |

```
abstract class FragmentHostCallback<E : Any!> : FragmentContainer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.app.FragmentContainer](https://developer.android.com/reference/kotlin/android/app/FragmentContainer) ||
| | ↳ | [android.app.FragmentHostCallback](https://developer.android.com/reference/kotlin/android/app/FragmentHostCallback#) |

| **This class was deprecated in API level 28.**
|
| Use the [Support Library](https://developer.android.com/tools/extras/support-library.html) androidx.fragment.app.FragmentHostCallback

Integration points with the Fragment host.

Fragments may be hosted by any object; such as an `https://developer.android.com/reference/kotlin/android/app/Activity`. In order to host fragments, implement `https://developer.android.com/reference/kotlin/android/app/FragmentHostCallback#`, overriding the methods applicable to the host.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/FragmentHostCallback#FragmentHostCallback(android.content.Context,%20android.os.Handler,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!, windowAnimations: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentHostCallback#onAttachFragment(android.app.Fragment)(fragment: https://developer.android.com/reference/kotlin/android/app/Fragment!)` Called when a `https://developer.android.com/reference/kotlin/android/app/Fragment` is being attached to this host, immediately after the call to its `https://developer.android.com/reference/kotlin/android/app/Fragment#onAttach(android.content.Context)` method and before `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreate(android.os.Bundle)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentHostCallback#onDump(kotlin.String,%20java.io.FileDescriptor,%20java.io.PrintWriter,%20kotlin.Array)(prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#!, writer: https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#!, args: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Print internal state into the given stream. |
| open T? | `https://developer.android.com/reference/kotlin/android/app/FragmentHostCallback#onFindViewById(kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the view with the given resource ID. |
| --- | --- |
| abstract E? | `https://developer.android.com/reference/kotlin/android/app/FragmentHostCallback#onGetHost()()` Return the object that's currently hosting the fragment. |
| open [LayoutInflater](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#)! | `https://developer.android.com/reference/kotlin/android/app/FragmentHostCallback#onGetLayoutInflater()()` Return a `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentHostCallback#onGetWindowAnimations()()` Return the window animations. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentHostCallback#onHasView()()` Return `true` if the container holds any view. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentHostCallback#onHasWindowAnimations()()` Return `true` if there are window animations. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentHostCallback#onInvalidateOptionsMenu()()` Invalidates the activity's options menu. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentHostCallback#onRequestPermissionsFromFragment(android.app.Fragment,%20kotlin.Array,%20kotlin.Int)(fragment: https://developer.android.com/reference/kotlin/android/app/Fragment, permissions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Requests permissions from the given fragment. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentHostCallback#onShouldSaveFragmentState(android.app.Fragment)(fragment: https://developer.android.com/reference/kotlin/android/app/Fragment!)` Return `true` if the fragment's state needs to be saved. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentHostCallback#onStartActivityFromFragment(android.app.Fragment,%20android.content.Intent,%20kotlin.Int,%20android.os.Bundle)(fragment: https://developer.android.com/reference/kotlin/android/app/Fragment!, intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Starts a new `https://developer.android.com/reference/kotlin/android/app/Activity` from the given fragment. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentHostCallback#onStartIntentSenderFromFragment(android.app.Fragment,%20android.content.IntentSender,%20kotlin.Int,%20android.content.Intent,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)(fragment: https://developer.android.com/reference/kotlin/android/app/Fragment!, intent: https://developer.android.com/reference/kotlin/android/content/IntentSender.html#!, requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, fillInIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#?, flagsMask: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flagsValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, extraFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Starts a new `https://developer.android.com/reference/kotlin/android/content/IntentSender.html#` from the given fragment. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/FragmentHostCallback#onUseFragmentManagerInflaterFactory()()` Return `true` if the FragmentManager's LayoutInflaterFactory should be used. |

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

Called when a `https://developer.android.com/reference/kotlin/android/app/Fragment` is being attached to this host, immediately after the call to its `https://developer.android.com/reference/kotlin/android/app/Fragment#onAttach(android.content.Context)` method and before `https://developer.android.com/reference/kotlin/android/app/Fragment#onCreate(android.os.Bundle)`.

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
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!: The raw file descriptor that the dump is being sent to. |
| `writer` | [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)!: The PrintWriter to which you should dump your state. This will be closed for you after you return. |
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

Return the object that's currently hosting the fragment. If a `https://developer.android.com/reference/kotlin/android/app/Fragment` is hosted by a `https://developer.android.com/reference/kotlin/android/app/Activity`, the object returned here should be the same object returned from `https://developer.android.com/reference/kotlin/android/app/Fragment#getActivity()`.

| Return ||
|---|---|
| `E?` | This value may be `null`. |

### onGetLayoutInflater

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onGetLayoutInflater(): LayoutInflater!
```

**Deprecated:** *Deprecated in Java.*

Return a `https://developer.android.com/reference/kotlin/android/view/LayoutInflater.html#`. See `https://developer.android.com/reference/kotlin/android/app/Activity#getLayoutInflater()`.

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

Invalidates the activity's options menu. See `https://developer.android.com/reference/kotlin/android/app/Activity#invalidateOptionsMenu()`

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

Requests permissions from the given fragment. See `https://developer.android.com/reference/kotlin/android/app/Activity#requestPermissions(kotlin.Array,%20kotlin.Int)`

| Parameters ||
|---|---|
| `fragment` | [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment): This value cannot be `null`. |
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

Starts a new `https://developer.android.com/reference/kotlin/android/app/Activity` from the given fragment. See `https://developer.android.com/reference/kotlin/android/app/Activity#startActivityForResult(android.content.Intent,%20kotlin.Int)`.

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
| `fillInIntent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)?: This value may be `null`. |

### onUseFragmentManagerInflaterFactory

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onUseFragmentManagerInflaterFactory(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Return `true` if the FragmentManager's LayoutInflaterFactory should be used.
