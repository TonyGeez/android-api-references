# FragmentTransaction

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FragmentTransaction

Kotlin| [Java](https://developer.android.com/reference/android/app/FragmentTransaction "View this page in Java") 
| --- | --- |

```
abstract class FragmentTransaction
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#) |

| **This class was deprecated in API level 28.**
|
| Use the [Support Library](https://developer.android.com/tools/extras/support-library.html) androidx.fragment.app.FragmentTransaction

API for performing a set of Fragment operations.
|
| ### Developer Guides
|
| For more information about using fragments, read the [Fragments](https://developer.android.com/guide/components/fragments.html) developer guide.

<br />

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSIT_ENTER_MASK](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#TRANSIT_ENTER_MASK:kotlin.Int) Bit mask that is set for all enter transitions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSIT_EXIT_MASK](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#TRANSIT_EXIT_MASK:kotlin.Int) Bit mask that is set for all exit transitions. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSIT_FRAGMENT_CLOSE](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#TRANSIT_FRAGMENT_CLOSE:kotlin.Int) Fragment is being removed from the stack |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSIT_FRAGMENT_FADE](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#TRANSIT_FRAGMENT_FADE:kotlin.Int) Fragment should simply fade in or out; that is, no strong navigation associated with it except that it is appearing or disappearing for some reason. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSIT_FRAGMENT_OPEN](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#TRANSIT_FRAGMENT_OPEN:kotlin.Int) Fragment is being added onto the stack |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSIT_NONE](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#TRANSIT_NONE:kotlin.Int) No animation for transition. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSIT_UNSET](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#TRANSIT_UNSET:kotlin.Int) Not set up for a transition. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------|---|
| [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#FragmentTransaction())`()` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | [add](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#add(android.app.Fragment,%20kotlin.String))`(`fragment:` ` [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!`, `tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Calls [add(int,android.app.Fragment,java.lang.String)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#add(kotlin.Int,%20android.app.Fragment,%20kotlin.String))with a 0 containerViewId. |
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | [add](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#add(kotlin.Int,%20android.app.Fragment))`(`containerViewId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fragment:` ` [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!`)` Calls [add(int,android.app.Fragment,java.lang.String)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#add(kotlin.Int,%20android.app.Fragment,%20kotlin.String))with a null tag. |
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | [add](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#add(kotlin.Int,%20android.app.Fragment,%20kotlin.String))`(`containerViewId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fragment:` ` [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!`, `tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Add a fragment to the activity state. |
| --- | --- |
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | [addSharedElement](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#addSharedElement(android.view.View,%20kotlin.String))`(`sharedElement:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Used with to map a View from a removed or hidden Fragment to a View from a shown or added Fragment. |
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | [addToBackStack](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#addToBackStack(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Add this transaction to the back stack. |
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | [attach](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#attach(android.app.Fragment))`(`fragment:` ` [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!`)` Re-attach a fragment after it had previously been detached from the UI with [detach(android.app.Fragment)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#detach(android.app.Fragment)). |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [commit](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#commit())`()` Schedules a commit of this transaction. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [commitAllowingStateLoss](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#commitAllowingStateLoss())`()` Like [commit](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#commit())but allows the commit to be executed after an activity's state is saved. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [commitNow](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#commitNow())`()` Commits this transaction synchronously. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [commitNowAllowingStateLoss](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#commitNowAllowingStateLoss())`()` Like [commitNow](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#commitNow())but allows the commit to be executed after an activity's state is saved. |
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | [detach](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#detach(android.app.Fragment))`(`fragment:` ` [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!`)` Detach the given fragment from the UI. |
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | [disallowAddToBackStack](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#disallowAddToBackStack())`()` Disallow calls to [addToBackStack(java.lang.String)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#addToBackStack(kotlin.String)). |
| --- | --- |
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | [hide](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#hide(android.app.Fragment))`(`fragment:` ` [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!`)` Hides an existing fragment. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAddToBackStackAllowed](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#isAddToBackStackAllowed())`()` Returns true if this FragmentTransaction is allowed to be added to the back stack. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#isEmpty())`()` <br /> |
| --- | --- |
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | [remove](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#remove(android.app.Fragment))`(`fragment:` ` [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!`)` Remove an existing fragment. |
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | [replace](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#replace(kotlin.Int,%20android.app.Fragment))`(`containerViewId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fragment:` ` [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!`)` Calls [replace(int,android.app.Fragment,java.lang.String)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#replace(kotlin.Int,%20android.app.Fragment,%20kotlin.String))with a null tag. |
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | [replace](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#replace(kotlin.Int,%20android.app.Fragment,%20kotlin.String))`(`containerViewId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fragment:` ` [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!`, `tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Replace an existing fragment that was added to a container. |
| --- | --- |
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | [runOnCommit](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#runOnCommit(java.lang.Runnable))`(`runnable:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` Add a Runnable to this transaction that will be run after this transaction has been committed. |
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | [setBreadCrumbShortTitle](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#setBreadCrumbShortTitle(kotlin.Int))`(`res:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the short title to show as a bread crumb when this transaction is on the back stack, as used by [FragmentBreadCrumbs](https://developer.android.com/reference/kotlin/android/app/FragmentBreadCrumbs). |
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | [setBreadCrumbShortTitle](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#setBreadCrumbShortTitle(kotlin.CharSequence))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Like [setBreadCrumbShortTitle(int)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#setBreadCrumbShortTitle(kotlin.Int))but taking a raw string; this method is*not*recommended, as the string can not be changed later if the locale changes. |
| --- | --- |
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | [setBreadCrumbTitle](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#setBreadCrumbTitle(kotlin.Int))`(`res:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the full title to show as a bread crumb when this transaction is on the back stack, as used by [FragmentBreadCrumbs](https://developer.android.com/reference/kotlin/android/app/FragmentBreadCrumbs). |
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | [setBreadCrumbTitle](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#setBreadCrumbTitle(kotlin.CharSequence))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Like [setBreadCrumbTitle(int)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#setBreadCrumbTitle(kotlin.Int))but taking a raw string; this method is*not*recommended, as the string can not be changed later if the locale changes. |
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | [setCustomAnimations](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#setCustomAnimations(kotlin.Int,%20kotlin.Int))`(`enter:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `exit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set specific animation resources to run for the fragments that are entering and exiting in this transaction. |
| --- | --- |
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | [setCustomAnimations](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#setCustomAnimations(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`enter:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `exit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `popEnter:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `popExit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set specific animation resources to run for the fragments that are entering and exiting in this transaction. |
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | [setPrimaryNavigationFragment](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#setPrimaryNavigationFragment(android.app.Fragment))`(`fragment:` ` [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!`)` Set a currently active fragment in this FragmentManager as the primary navigation fragment. |
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | [setReorderingAllowed](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#setReorderingAllowed(kotlin.Boolean))`(`reorderingAllowed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether or not to allow optimizing operations within and across transactions. |
| --- | --- |
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | [setTransition](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#setTransition(kotlin.Int))`(`transit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Select a standard transition animation for this transaction. |
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | [setTransitionStyle](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#setTransitionStyle(kotlin.Int))`(`styleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set a custom style resource that will be used for resolving transit animations. |
| abstract [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | [show](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#show(android.app.Fragment))`(`fragment:` ` [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!`)` Shows a previously hidden fragment. |
| --- | --- |

## Constants

### TRANSIT_ENTER_MASK

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSIT_ENTER_MASK: Int
```

**Deprecated:** *Deprecated in Java.*

Bit mask that is set for all enter transitions. 

 Value: 4096

### TRANSIT_EXIT_MASK

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSIT_EXIT_MASK: Int
```

**Deprecated:** *Deprecated in Java.*

Bit mask that is set for all exit transitions. 

 Value: 8192

### TRANSIT_FRAGMENT_CLOSE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSIT_FRAGMENT_CLOSE: Int
```

**Deprecated:** *Deprecated in Java.*

Fragment is being removed from the stack 

 Value: 8194

### TRANSIT_FRAGMENT_FADE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSIT_FRAGMENT_FADE: Int
```

**Deprecated:** *Deprecated in Java.*

Fragment should simply fade in or out; that is, no strong navigation associated with it except that it is appearing or disappearing for some reason. 

 Value: 4099

### TRANSIT_FRAGMENT_OPEN

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSIT_FRAGMENT_OPEN: Int
```

**Deprecated:** *Deprecated in Java.*

Fragment is being added onto the stack 

 Value: 4097

### TRANSIT_NONE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSIT_NONE: Int
```

**Deprecated:** *Deprecated in Java.*

No animation for transition. 

 Value: 0

### TRANSIT_UNSET

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSIT_UNSET: Int
```

**Deprecated:** *Deprecated in Java.*

Not set up for a transition. 

 Value: -1

## Public constructors

### FragmentTransaction

```
FragmentTransaction()
```

## Public methods

### add

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun add(
    fragment: Fragment!, 
    tag: String!
): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Calls [add(int,android.app.Fragment,java.lang.String)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#add(kotlin.Int,%20android.app.Fragment,%20kotlin.String))with a 0 containerViewId. 

### add

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun add(
    containerViewId: Int, 
    fragment: Fragment!
): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Calls [add(int,android.app.Fragment,java.lang.String)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#add(kotlin.Int,%20android.app.Fragment,%20kotlin.String))with a null tag. 

### add

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun add(
    containerViewId: Int, 
    fragment: Fragment!, 
    tag: String!
): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Add a fragment to the activity state. This fragment may optionally also have its view (if [Fragment.onCreateView](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreateView(android.view.LayoutInflater,%20android.view.ViewGroup,%20android.os.Bundle))returns non-null) inserted into a container view of the activity.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `containerViewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Optional identifier of the container this fragment is to be placed in. If 0, it will not be placed in a container. |
| `fragment` | [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!:The fragment to be added. This fragment must not already be added to the activity. |
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Optional tag name for the fragment, to later retrieve the fragment with [FragmentManager.findFragmentByTag(String)](https://developer.android.com/reference/kotlin/android/app/FragmentManager#findFragmentByTag(kotlin.String)). |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | Returns the same FragmentTransaction instance. |

### addSharedElement

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addSharedElement(
    sharedElement: View!, 
    name: String!
): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Used with to map a View from a removed or hidden Fragment to a View from a shown or added Fragment.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedElement` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:A View in a disappearing Fragment to match with a View in an appearing Fragment. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The transitionName for a View in an appearing Fragment to match to the shared element. |

### addToBackStack

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addToBackStack(name: String?): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Add this transaction to the back stack. This means that the transaction will be remembered after it is committed, and will reverse its operation when later popped off the stack.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:An optional name for this back stack state, or null. |

### attach

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun attach(fragment: Fragment!): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Re-attach a fragment after it had previously been detached from the UI with [detach(android.app.Fragment)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#detach(android.app.Fragment)). This causes its view hierarchy to be re-created, attached to the UI, and displayed.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------|
| `fragment` | [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!:The fragment to be attached. |

| Return ||
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | Returns the same FragmentTransaction instance. |

### commit

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun commit(): Int
```

**Deprecated:** *Deprecated in Java.*

Schedules a commit of this transaction. The commit does not happen immediately; it will be scheduled as work on the main thread to be done the next time that thread is ready.

A transaction can only be committed with this method prior to its containing activity saving its state. If the commit is attempted after that point, an exception will be thrown. This is because the state after the commit can be lost if the activity needs to be restored from its state. See [commitAllowingStateLoss()](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#commitAllowingStateLoss())for situations where it may be okay to lose the commit.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Returns the identifier of this transaction's back stack entry, if [addToBackStack(java.lang.String)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#addToBackStack(kotlin.String))had been called. Otherwise, returns a negative number. |

### commitAllowingStateLoss

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun commitAllowingStateLoss(): Int
```

**Deprecated:** *Deprecated in Java.*

Like [commit](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#commit())but allows the commit to be executed after an activity's state is saved. This is dangerous because the commit can be lost if the activity needs to later be restored from its state, so this should only be used for cases where it is okay for the UI state to change unexpectedly on the user. 

### commitNow

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun commitNow(): Unit
```

**Deprecated:** *Deprecated in Java.*

Commits this transaction synchronously. Any added fragments will be initialized and brought completely to the lifecycle state of their host and any removed fragments will be torn down accordingly before this call returns. Committing a transaction in this way allows fragments to be added as dedicated, encapsulated components that monitor the lifecycle state of their host while providing firmer ordering guarantees around when those fragments are fully initialized and ready. Fragments that manage views will have those views created and attached.

Calling`commitNow`is preferable to calling [commit()](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#commit())followed by [FragmentManager.executePendingTransactions()](https://developer.android.com/reference/kotlin/android/app/FragmentManager#executePendingTransactions())as the latter will have the side effect of attempting to commit*all*currently pending transactions whether that is the desired behavior or not.

Transactions committed in this way may not be added to the FragmentManager's back stack, as doing so would break other expected ordering guarantees for other asynchronously committed transactions. This method will throw [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) if the transaction previously requested to be added to the back stack with [addToBackStack(java.lang.String)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#addToBackStack(kotlin.String)).

A transaction can only be committed with this method prior to its containing activity saving its state. If the commit is attempted after that point, an exception will be thrown. This is because the state after the commit can be lost if the activity needs to be restored from its state. See [commitAllowingStateLoss()](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#commitAllowingStateLoss())for situations where it may be okay to lose the commit. 

### commitNowAllowingStateLoss

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun commitNowAllowingStateLoss(): Unit
```

**Deprecated:** *Deprecated in Java.*

Like [commitNow](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#commitNow())but allows the commit to be executed after an activity's state is saved. This is dangerous because the commit can be lost if the activity needs to later be restored from its state, so this should only be used for cases where it is okay for the UI state to change unexpectedly on the user. 

### detach

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun detach(fragment: Fragment!): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Detach the given fragment from the UI. This is the same state as when it is put on the back stack: the fragment is removed from the UI, however its state is still being actively managed by the fragment manager. When going into this state its view hierarchy is destroyed.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------|
| `fragment` | [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!:The fragment to be detached. |

| Return ||
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | Returns the same FragmentTransaction instance. |

### disallowAddToBackStack

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun disallowAddToBackStack(): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Disallow calls to [addToBackStack(java.lang.String)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#addToBackStack(kotlin.String)). Any future calls to addToBackStack will throw [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#). If addToBackStack has already been called, this method will throw IllegalStateException. 

### hide

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hide(fragment: Fragment!): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Hides an existing fragment. This is only relevant for fragments whose views have been added to a container, as this will cause the view to be hidden.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `fragment` | [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!:The fragment to be hidden. |

| Return ||
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | Returns the same FragmentTransaction instance. |

### isAddToBackStackAllowed

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isAddToBackStackAllowed(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if this FragmentTransaction is allowed to be added to the back stack. If this method would return false, [addToBackStack(java.lang.String)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#addToBackStack(kotlin.String))will throw [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#).

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if [addToBackStack(java.lang.String)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#addToBackStack(kotlin.String))is permitted on this transaction. |

### isEmpty

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isEmpty(): Boolean
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this transaction contains no operations,`false`otherwise. |

### remove

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun remove(fragment: Fragment!): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Remove an existing fragment. If it was added to a container, its view is also removed from that container.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------|
| `fragment` | [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!:The fragment to be removed. |

| Return ||
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | Returns the same FragmentTransaction instance. |

### replace

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun replace(
    containerViewId: Int, 
    fragment: Fragment!
): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Calls [replace(int,android.app.Fragment,java.lang.String)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#replace(kotlin.Int,%20android.app.Fragment,%20kotlin.String))with a null tag. 

### replace

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun replace(
    containerViewId: Int, 
    fragment: Fragment!, 
    tag: String!
): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Replace an existing fragment that was added to a container. This is essentially the same as calling [remove(android.app.Fragment)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#remove(android.app.Fragment))for all currently added fragments that were added with the same containerViewId and then [add(int,android.app.Fragment,java.lang.String)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#add(kotlin.Int,%20android.app.Fragment,%20kotlin.String))with the same arguments given here.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `containerViewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Identifier of the container whose fragment(s) are to be replaced. |
| `fragment` | [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!:The new fragment to place in the container. |
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Optional tag name for the fragment, to later retrieve the fragment with [FragmentManager.findFragmentByTag(String)](https://developer.android.com/reference/kotlin/android/app/FragmentManager#findFragmentByTag(kotlin.String)). |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | Returns the same FragmentTransaction instance. |

### runOnCommit

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun runOnCommit(runnable: Runnable!): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Add a Runnable to this transaction that will be run after this transaction has been committed. If fragment transactions are [optimized](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#setReorderingAllowed(kotlin.Boolean))this may be after other subsequent fragment operations have also taken place, or operations in this transaction may have been optimized out due to the presence of a subsequent fragment transaction in the batch.

If a transaction is committed using [commitAllowingStateLoss()](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#commitAllowingStateLoss())this runnable may be executed when the FragmentManager is in a state where new transactions may not be committed without allowing state loss.

`runOnCommit`may not be used with transactions [added to the back stack](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#addToBackStack(kotlin.String))as Runnables cannot be persisted with back stack state. [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) will be thrown if [addToBackStack(java.lang.String)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#addToBackStack(kotlin.String))has been previously called for this transaction or if it is called after a call to`runOnCommit`.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------|
| `runnable` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!:Runnable to add |

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------|
| [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | this FragmentTransaction |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if [addToBackStack(java.lang.String)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#addToBackStack(kotlin.String))has been called |

### setBreadCrumbShortTitle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBreadCrumbShortTitle(res: Int): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Set the short title to show as a bread crumb when this transaction is on the back stack, as used by [FragmentBreadCrumbs](https://developer.android.com/reference/kotlin/android/app/FragmentBreadCrumbs).

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------|
| `res` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A string resource containing the title. |

### setBreadCrumbShortTitle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBreadCrumbShortTitle(text: CharSequence!): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Like [setBreadCrumbShortTitle(int)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#setBreadCrumbShortTitle(kotlin.Int))but taking a raw string; this method is*not*recommended, as the string can not be changed later if the locale changes. 

### setBreadCrumbTitle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBreadCrumbTitle(res: Int): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Set the full title to show as a bread crumb when this transaction is on the back stack, as used by [FragmentBreadCrumbs](https://developer.android.com/reference/kotlin/android/app/FragmentBreadCrumbs).

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------|
| `res` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A string resource containing the title. |

### setBreadCrumbTitle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBreadCrumbTitle(text: CharSequence!): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Like [setBreadCrumbTitle(int)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#setBreadCrumbTitle(kotlin.Int))but taking a raw string; this method is*not*recommended, as the string can not be changed later if the locale changes. 

### setCustomAnimations

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCustomAnimations(
    enter: Int, 
    exit: Int
): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Set specific animation resources to run for the fragments that are entering and exiting in this transaction. These animations will not be played when popping the back stack. 

### setCustomAnimations

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCustomAnimations(
    enter: Int, 
    exit: Int, 
    popEnter: Int, 
    popExit: Int
): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Set specific animation resources to run for the fragments that are entering and exiting in this transaction. The`popEnter`and`popExit`animations will be played for enter/exit operations specifically when popping the back stack. 

### setPrimaryNavigationFragment

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setPrimaryNavigationFragment(fragment: Fragment!): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Set a currently active fragment in this FragmentManager as the primary navigation fragment.

The primary navigation fragment's [child FragmentManager](https://developer.android.com/reference/kotlin/android/app/Fragment#getChildFragmentManager())will be called first to process delegated navigation actions such as [FragmentManager.popBackStack()](https://developer.android.com/reference/kotlin/android/app/FragmentManager#popBackStack())if no ID or transaction name is provided to pop to. Navigation operations outside of the fragment system may choose to delegate those actions to the primary navigation fragment as returned by [FragmentManager.getPrimaryNavigationFragment()](https://developer.android.com/reference/kotlin/android/app/FragmentManager#getPrimaryNavigationFragment()).

The fragment provided must currently be added to the FragmentManager to be set as a primary navigation fragment, or previously added as part of this transaction.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `fragment` | [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!:the fragment to set as the primary navigation fragment |

| Return ||
|---------------------------------------------------------------------------------------------------------|---------------------------------------|
| [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | the same FragmentTransaction instance |

### setReorderingAllowed

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setReorderingAllowed(reorderingAllowed: Boolean): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Sets whether or not to allow optimizing operations within and across transactions. This will remove redundant operations, eliminating operations that cancel. For example, if two transactions are executed together, one that adds a fragment A and the next replaces it with fragment B, the operations will cancel and only fragment B will be added. That means that fragment A may not go through the creation/destruction lifecycle.

The side effect of removing redundant operations is that fragments may have state changes out of the expected order. For example, one transaction adds fragment A, a second adds fragment B, then a third removes fragment A. Without removing the redundant operations, fragment B could expect that while it is being created, fragment A will also exist because fragment A will be removed after fragment B was added. With removing redundant operations, fragment B cannot expect fragment A to exist when it has been created because fragment A's add/remove will be optimized out.

It can also reorder the state changes of Fragments to allow for better Transitions. Added Fragments may have [Fragment.onCreate(Bundle)](https://developer.android.com/reference/kotlin/android/app/Fragment#onCreate(android.os.Bundle))called before replaced Fragments have [Fragment.onDestroy()](https://developer.android.com/reference/kotlin/android/app/Fragment#onDestroy())called.

The default is`false`for applications targeting version versions prior to O and`true`for applications targeting O and later.

| Parameters ||
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reorderingAllowed` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`to enable optimizing out redundant operations or`false`to disable optimizing out redundant operations on this transaction. |

### setTransition

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTransition(transit: Int): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Select a standard transition animation for this transaction. May be one of [TRANSIT_NONE](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#TRANSIT_NONE:kotlin.Int), [TRANSIT_FRAGMENT_OPEN](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#TRANSIT_FRAGMENT_OPEN:kotlin.Int), [TRANSIT_FRAGMENT_CLOSE](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#TRANSIT_FRAGMENT_CLOSE:kotlin.Int), or [TRANSIT_FRAGMENT_FADE](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#TRANSIT_FRAGMENT_FADE:kotlin.Int).

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.app.FragmentTransaction#TRANSIT_NONE](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#TRANSIT_NONE:kotlin.Int), [android.app.FragmentTransaction#TRANSIT_FRAGMENT_OPEN](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#TRANSIT_FRAGMENT_OPEN:kotlin.Int), [android.app.FragmentTransaction#TRANSIT_FRAGMENT_CLOSE](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#TRANSIT_FRAGMENT_CLOSE:kotlin.Int), or [android.app.FragmentTransaction#TRANSIT_FRAGMENT_FADE](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#TRANSIT_FRAGMENT_FADE:kotlin.Int) |

### setTransitionStyle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTransitionStyle(styleRes: Int): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Set a custom style resource that will be used for resolving transit animations. 

### show

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun show(fragment: Fragment!): FragmentTransaction!
```

**Deprecated:** *Deprecated in Java.*

Shows a previously hidden fragment. This is only relevant for fragments whose views have been added to a container, as this will cause the view to be shown.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------|
| `fragment` | [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)!:The fragment to be shown. |

| Return ||
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| [FragmentTransaction](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#)! | Returns the same FragmentTransaction instance. |
