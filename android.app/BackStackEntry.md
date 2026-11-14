# FragmentManager.BackStackEntry

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BackStackEntry

Kotlin| [Java](https://developer.android.com/reference/android/app/FragmentManager.BackStackEntry "View this page in Java") 
| --- | --- |

```
interface BackStackEntry
```

| [android.app.FragmentManager.BackStackEntry](https://developer.android.com/reference/kotlin/android/app/FragmentManager.BackStackEntry#) |

| **This interface was deprecated in API level 28.**
|
| Use the [Support Library](https://developer.android.com/tools/extras/support-library.html) androidx.fragment.app.FragmentManager.BackStackEntry

Representation of an entry on the fragment back stack, as created with [FragmentTransaction.addToBackStack()](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#addToBackStack(kotlin.String)). Entries can later be retrieved with [FragmentManager.getBackStackEntryAt()](https://developer.android.com/reference/kotlin/android/app/FragmentManager#getBackStackEntryAt(kotlin.Int)).

Note that you should never hold on to a BackStackEntry object; the identifier as returned by [getId](https://developer.android.com/reference/kotlin/android/app/FragmentManager.BackStackEntry#getId())is the only thing that will be persisted across activity instances.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getBreadCrumbShortTitle](https://developer.android.com/reference/kotlin/android/app/FragmentManager.BackStackEntry#getBreadCrumbShortTitle())`()` Return the short bread crumb title for the entry, or null if it does not have one. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBreadCrumbShortTitleRes](https://developer.android.com/reference/kotlin/android/app/FragmentManager.BackStackEntry#getBreadCrumbShortTitleRes())`()` Return the short bread crumb title resource identifier for the entry, or 0 if it does not have one. |
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getBreadCrumbTitle](https://developer.android.com/reference/kotlin/android/app/FragmentManager.BackStackEntry#getBreadCrumbTitle())`()` Return the full bread crumb title for the entry, or null if it does not have one. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBreadCrumbTitleRes](https://developer.android.com/reference/kotlin/android/app/FragmentManager.BackStackEntry#getBreadCrumbTitleRes())`()` Return the full bread crumb title resource identifier for the entry, or 0 if it does not have one. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](https://developer.android.com/reference/kotlin/android/app/FragmentManager.BackStackEntry#getId())`()` Return the unique identifier for the entry. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/android/app/FragmentManager.BackStackEntry#getName())`()` Get the name that was supplied to [FragmentTransaction.addToBackStack(String)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#addToBackStack(kotlin.String))when creating this entry. |
| --- | --- |

## Public methods

### getBreadCrumbShortTitle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBreadCrumbShortTitle(): CharSequence!
```

**Deprecated:** *Deprecated in Java.*

Return the short bread crumb title for the entry, or null if it does not have one. 

### getBreadCrumbShortTitleRes

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBreadCrumbShortTitleRes(): Int
```

**Deprecated:** *Deprecated in Java.*

Return the short bread crumb title resource identifier for the entry, or 0 if it does not have one. 

### getBreadCrumbTitle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBreadCrumbTitle(): CharSequence!
```

**Deprecated:** *Deprecated in Java.*

Return the full bread crumb title for the entry, or null if it does not have one. 

### getBreadCrumbTitleRes

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBreadCrumbTitleRes(): Int
```

**Deprecated:** *Deprecated in Java.*

Return the full bread crumb title resource identifier for the entry, or 0 if it does not have one. 

### getId

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getId(): Int
```

**Deprecated:** *Deprecated in Java.*

Return the unique identifier for the entry. This is the only representation of the entry that will persist across activity instances. 

### getName

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getName(): String!
```

**Deprecated:** *Deprecated in Java.*

Get the name that was supplied to [FragmentTransaction.addToBackStack(String)](https://developer.android.com/reference/kotlin/android/app/FragmentTransaction#addToBackStack(kotlin.String))when creating this entry.
