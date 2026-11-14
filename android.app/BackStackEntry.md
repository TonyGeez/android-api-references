# FragmentManager.BackStackEntry

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BackStackEntry

Kotlin| [Java](../android/app/FragmentManager.BackStackEntry.md) 
| --- | --- |

```
interface BackStackEntry
```

| [android.app.FragmentManager.BackStackEntry](../android/app/FragmentManager.BackStackEntry.md) |

| **This interface was deprecated in API level 28.**
|
| Use the [Support Library](https://developer.android.com/tools/extras/support-library.html) androidx.fragment.app.FragmentManager.BackStackEntry

Representation of an entry on the fragment back stack, as created with [FragmentTransaction.addToBackStack()](FragmentTransaction.md)). Entries can later be retrieved with [FragmentManager.getBackStackEntryAt()](FragmentManager.md)).

Note that you should never hold on to a BackStackEntry object; the identifier as returned by [getId](../android/app/FragmentManager.BackStackEntry.md))is the only thing that will be persisted across activity instances.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getBreadCrumbShortTitle](../android/app/FragmentManager.BackStackEntry.md))`()` Return the short bread crumb title for the entry, or null if it does not have one. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBreadCrumbShortTitleRes](../android/app/FragmentManager.BackStackEntry.md))`()` Return the short bread crumb title resource identifier for the entry, or 0 if it does not have one. |
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getBreadCrumbTitle](../android/app/FragmentManager.BackStackEntry.md))`()` Return the full bread crumb title for the entry, or null if it does not have one. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBreadCrumbTitleRes](../android/app/FragmentManager.BackStackEntry.md))`()` Return the full bread crumb title resource identifier for the entry, or 0 if it does not have one. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](../android/app/FragmentManager.BackStackEntry.md))`()` Return the unique identifier for the entry. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../android/app/FragmentManager.BackStackEntry.md))`()` Get the name that was supplied to [FragmentTransaction.addToBackStack(String)](FragmentTransaction.md))when creating this entry. |
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

Get the name that was supplied to [FragmentTransaction.addToBackStack(String)](FragmentTransaction.md))when creating this entry.
