# ComponentName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ComponentName

Kotlin| [Java](../android/content/ComponentName.md) 
| --- | --- |

```
class ComponentName : Cloneable, Comparable<ComponentName!>, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.ComponentName](../android/content/ComponentName.md) |

Identifier for a specific application component ([android.app.Activity](../android/app/Activity.md), [android.app.Service](../android/app/Service.md), [android.content.BroadcastReceiver](../android/content/BroadcastReceiver.md), or [android.content.ContentProvider](../android/content/ContentProvider.md)) that is available. Two pieces of information, encapsulated here, are required to identify a component: the package (a String) it exists in, and the class (a String) name inside of that package.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ComponentName](../android/content/ComponentName.md))`(`pkg:` ` [Context](../android/content/Context.md)`, `cls:` ` [Class](../java/lang/Class.md)<*>`)` Create a new component identifier from a Context and Class object. |
| [ComponentName](../android/content/ComponentName.md))`(`pkg:` ` [Context](../android/content/Context.md)`, `cls:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Create a new component identifier from a Context and class name. |
| [ComponentName](../android/content/ComponentName.md))`(`in:` ` [Parcel](../android/os/Parcel.md)!`)` Instantiate a new ComponentName from the data in a Parcel that was previously written with [writeToParcel(android.os.Parcel,int)](../android/content/ComponentName.md)). |
| [ComponentName](../android/content/ComponentName.md))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `cls:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Create a new component identifier. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ComponentName](../android/content/ComponentName.md) | [clone](../android/content/ComponentName.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](../android/content/ComponentName.md))`(`other:` ` [ComponentName](../android/content/ComponentName.md)!`)` <br /> |
| static [ComponentName](../android/content/ComponentName.md) | [createRelative](../android/content/ComponentName.md))`(`pkg:` ` [Context](../android/content/Context.md)`, `cls:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Create a new component identifier where the class name may be specified as either absolute or relative to the containing package. |
| --- | --- |
| static [ComponentName](../android/content/ComponentName.md) | [createRelative](../android/content/ComponentName.md))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `cls:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Create a new component identifier where the class name may be specified as either absolute or relative to the containing package. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/content/ComponentName.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/content/ComponentName.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [flattenToShortString](../android/content/ComponentName.md))`()` The same as [flattenToString()](../android/content/ComponentName.md)), but abbreviates the class name if it is a suffix of the package. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [flattenToString](../android/content/ComponentName.md))`()` Return a String that unambiguously describes both the package and class names contained in the ComponentName. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getClassName](../android/content/ComponentName.md))`()` Return the class name of this component. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getPackageName](../android/content/ComponentName.md))`()` Return the package name of this component. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getShortClassName](../android/content/ComponentName.md))`()` Return the class name, either fully qualified or in a shortened form (with a leading '.') if it is a suffix of the package. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/content/ComponentName.md))`()` <br /> |
| --- | --- |
| static [ComponentName](../android/content/ComponentName.md)! | [readFromParcel](../android/content/ComponentName.md))`(`in:` ` [Parcel](../android/os/Parcel.md)!`)` Read a ComponentName from a Parcel that was previously written with [writeToParcel(android.content.ComponentName,android.os.Parcel)](../android/content/ComponentName.md)), returning either a null or new object as appropriate. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toShortString](../android/content/ComponentName.md))`()` Return string representation of this class without the class's name as a prefix. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/content/ComponentName.md))`()` <br /> |
| --- | --- |
| static [ComponentName](../android/content/ComponentName.md)? | [unflattenFromString](../android/content/ComponentName.md))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Recover a ComponentName from a String that was previously created with [flattenToString()](../android/content/ComponentName.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/content/ComponentName.md))`(`out:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/content/ComponentName.md))`(`c:` ` [ComponentName](../android/content/ComponentName.md)!`, `out:` ` [Parcel](../android/os/Parcel.md)!`)` Write a ComponentName to a Parcel, handling null pointers. |
| --- | --- |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ComponentName](../android/content/ComponentName.md)!\> | [CREATOR](../android/content/ComponentName.md) <br /> |

## Public constructors

### ComponentName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ComponentName(
    pkg: Context, 
    cls: Class<*>)
```

Create a new component identifier from a Context and Class object.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pkg` | [Context](../android/content/Context.md):A Context for the package implementing the component, from which the actual package name will be retrieved. This value cannot be`null`. |
| `cls` | [Class](../java/lang/Class.md)\<\*\>:The Class object of the desired component, from which the actual class name will be retrieved. This value cannot be`null`. |

### ComponentName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ComponentName(
    pkg: Context, 
    cls: String)
```

Create a new component identifier from a Context and class name.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pkg` | [Context](../android/content/Context.md):A Context for the package implementing the component, from which the actual package name will be retrieved. This value cannot be`null`. |
| `cls` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the class inside of pkg that implements the component. This value cannot be`null`. |

### ComponentName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ComponentName(in: Parcel!)
```

Instantiate a new ComponentName from the data in a Parcel that was previously written with [writeToParcel(android.os.Parcel,int)](../android/content/ComponentName.md)). Note that you must not use this with data written by [writeToParcel(android.content.ComponentName,android.os.Parcel)](../android/content/ComponentName.md))since it is not possible to handle a null ComponentObject here.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `in` | [Parcel](../android/os/Parcel.md)!:The Parcel containing the previously written ComponentName, positioned at the location in the buffer where it was written. |

### ComponentName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ComponentName(
    pkg: String, 
    cls: String)
```

Create a new component identifier.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pkg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the package that the component exists in. Can not be null. |
| `cls` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the class inside of pkg that implements the component. Can not be null. |

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clone(): ComponentName
```

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------|
| [ComponentName](../android/content/ComponentName.md) | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### compareTo

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareTo(other: ComponentName!): Int
```

| Parameters ||
|-----|----------------------------|
| `o` | the object to be compared. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a negative integer, zero, or a positive integer as this object is less than, equal to, or greater than the specified object. |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified object is null |
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |

### createRelative

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createRelative(
    pkg: Context, 
    cls: String
): ComponentName
```

Create a new component identifier where the class name may be specified as either absolute or relative to the containing package.

Relative package names begin with a`'.'`character. For a package`"com.example"`and class name`".app.MyActivity"`this method will return a ComponentName with the package`"com.example"`and class name`"com.example.app.MyActivity"`. Fully qualified class names are also permitted.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pkg` | [Context](../android/content/Context.md):a Context for the package implementing the component This value cannot be`null`. |
| `cls` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the class inside of pkg that implements the component This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [ComponentName](../android/content/ComponentName.md) | the new ComponentName This value cannot be`null`. |

### createRelative

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createRelative(
    pkg: String, 
    cls: String
): ComponentName
```

Create a new component identifier where the class name may be specified as either absolute or relative to the containing package.

Relative package names begin with a`'.'`character. For a package`"com.example"`and class name`".app.MyActivity"`this method will return a ComponentName with the package`"com.example"`and class name`"com.example.app.MyActivity"`. Fully qualified class names are also permitted.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pkg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the package the component exists in This value cannot be`null`. |
| `cls` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the name of the class inside of pkg that implements the component This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [ComponentName](../android/content/ComponentName.md) | the new ComponentName This value cannot be`null`. |

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

Two components are considered to be equal if the packages in which they reside have the same name, and if the classes that implement each component also have the same name.

| Parameters ||
|-------|--------------------------|
| `obj` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### flattenToShortString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun flattenToShortString(): String
```

The same as [flattenToString()](../android/content/ComponentName.md)), but abbreviates the class name if it is a suffix of the package. The result can still be used with [unflattenFromString(java.lang.String)](../android/content/ComponentName.md)).

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | Returns a new String holding the package and class names. This is represented as the package name, concatenated with a '/' and then the class name. This value cannot be`null`. |

**See Also**

- [#unflattenFromString(String)](../android/content/ComponentName.md)) 

### flattenToString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun flattenToString(): String
```

Return a String that unambiguously describes both the package and class names contained in the ComponentName. You can later recover the ComponentName from this string through [unflattenFromString(java.lang.String)](../android/content/ComponentName.md)).

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | Returns a new String holding the package and class names. This is represented as the package name, concatenated with a '/' and then the class name. This value cannot be`null`. |

**See Also**

- [#unflattenFromString(String)](../android/content/ComponentName.md)) 

### getClassName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClassName(): String
```

Return the class name of this component.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getPackageName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPackageName(): String
```

Return the package name of this component.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getShortClassName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getShortClassName(): String!
```

Return the class name, either fully qualified or in a shortened form (with a leading '.') if it is a suffix of the package. 

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### readFromParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun readFromParcel(in: Parcel!): ComponentName!
```

Read a ComponentName from a Parcel that was previously written with [writeToParcel(android.content.ComponentName,android.os.Parcel)](../android/content/ComponentName.md)), returning either a null or new object as appropriate.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------|
| `in` | [Parcel](../android/os/Parcel.md)!:The Parcel from which to read the ComponentName |

| Return ||
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [ComponentName](../android/content/ComponentName.md)! | Returns a new ComponentName matching the previously written object, or null if a null had been written. |

**See Also**

- [#writeToParcel(ComponentName, Parcel)](../android/content/ComponentName.md)) 

### toShortString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toShortString(): String!
```

Return string representation of this class without the class's name as a prefix. 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### unflattenFromString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun unflattenFromString(str: String): ComponentName?
```

Recover a ComponentName from a String that was previously created with [flattenToString()](../android/content/ComponentName.md)). It splits the string at the first '/', taking the part before as the package name and the part after as the class name. As a special convenience (to use, for example, when parsing component names on the command line), if the '/' is immediately followed by a '.' then the final class name will be the concatenation of the package name with the string following the '/'. Thus "com.foo/.Blah" becomes package="com.foo" class="com.foo.Blah".

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The String that was returned by flattenToString(). This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [ComponentName](../android/content/ComponentName.md)? | Returns a new ComponentName containing the package and class names that were encoded in str This value may be`null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/content/ComponentName#flattenToString()> 

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun writeToParcel(
    c: ComponentName!, 
    out: Parcel!
): Unit
```

Write a ComponentName to a Parcel, handling null pointers. Must be read with [readFromParcel(android.os.Parcel)](../android/content/ComponentName.md)).

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [ComponentName](../android/content/ComponentName.md)!:The ComponentName to be written. |
| `out` | [Parcel](../android/os/Parcel.md)!:The Parcel in which the ComponentName will be placed. |

**See Also**

- [#readFromParcel(Parcel)](../android/content/ComponentName.md))

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ComponentName!>
```
