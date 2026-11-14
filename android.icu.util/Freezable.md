# Freezable

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Freezable

Kotlin| [Java](https://developer.android.com/reference/android/icu/util/Freezable "View this page in Java") 
| --- | --- |

```
interface Freezable<T : Any!> : Cloneable
```

| [android.icu.util.Freezable](https://developer.android.com/reference/kotlin/android/icu/util/Freezable#) |

| Known Direct Subclasses [Collator](https://developer.android.com/reference/kotlin/android/icu/text/Collator.html#), [DateIntervalInfo](https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo.html#), [DateTimePatternGenerator](https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator.html#), [MessagePattern](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern.html#), [TimeZone](https://developer.android.com/reference/kotlin/android/icu/util/TimeZone), [TimeZoneFormat](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.html#), [UnicodeSet](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.html#) |----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------| | [Collator](https://developer.android.com/reference/kotlin/android/icu/text/Collator.html#) | **\[icu enhancement\]** ICU's replacement for [java.text.Collator](https://developer.android.com/reference/kotlin/java/text/Collator.html#). | | [DateIntervalInfo](https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo.html#) | DateIntervalInfo is a public class for encapsulating localizable date time interval patterns. | | [DateTimePatternGenerator](https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator.html#) | This class provides flexible generation of date format patterns, like "yy-MM-dd". | | [MessagePattern](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern.html#) | Parses and represents ICU MessageFormat patterns. | | [TimeZone](https://developer.android.com/reference/kotlin/android/icu/util/TimeZone) | **\[icu enhancement\]** ICU's replacement for [java.util.TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone.html#). | | [TimeZoneFormat](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.html#) | `TimeZoneFormat`supports time zone display name formatting and parsing. | | [UnicodeSet](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.html#) | A mutable set of Unicode characters and multicharacter strings. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [RuleBasedCollator](https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator.html#) |--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------| | [RuleBasedCollator](https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator.html#) | RuleBasedCollator is a concrete subclass of Collator. | |
| --- | --- | --- | --- | --- | --- | --- |

Provides a flexible mechanism for controlling access, without requiring that a class be immutable. Once frozen, an object can never be unfrozen, so it is thread-safe from that point onward. Once the object has been frozen, it must guarantee that no changes can be made to it. Any attempt to alter it must raise an UnsupportedOperationException exception. This means that when the object returns internal objects, or if anyone has references to those internal objects, that those internal objects must either be immutable, or must also raise exceptions if any attempt to modify them is made. Of course, the object can return clones of internal objects, since those are safe.

## Background

<br />

There are often times when you need objects to be objects 'safe', so that they can't be modified. Examples are when objects need to be thread-safe, or in writing robust code, or in caches. If you are only creating your own objects, you can guarantee this, of course -- but only if you don't make a mistake. If you have objects handed into you, or are creating objects using others handed into you, it is a different story. It all comes down to whether you want to take the Blanche Dubois approach ("depend on the kindness of strangers") or the Andy Grove approach ("Only the Paranoid Survive").

For example, suppose we have a simple class: 

```kotlin
public class A {
       protected Collection b;
 
       protected Collection c;
 
       public Collection get_b() {
               return b;
       }
 
       public Collection get_c() {
               return c;
       }
 
       public A(Collection new_b, Collection new_c) {
               b = new_b;
               c = new_c;
       }
  }
  
```

Since the class doesn't have any setters, someone might think that it is immutable. You know where this is leading, of course; this class is unsafe in a number of ways. The following illustrates that. 

```kotlin
public test1(SupposedlyImmutableClass x, SafeStorage y) {
     // unsafe getter
     A a = x.getA();
     Collection col = a.get_b();
     col.add(something); // a has now been changed, and x too
 
     // unsafe constructor
     a = new A(col, col);
     y.store(a);
     col.add(something); // a has now been changed, and y too
   }
  
```

There are a few different techniques for having safe classes.

1. Const objects. In C++, you can declare parameters const.
2. Immutable wrappers. For example, you can put a collection in an immutable wrapper.
3. Always-Immutable objects. Java uses this approach, with a few variations. Examples:
 1. Simple. Once a Color is created (eg from R, G, and B integers) it is immutable.
 2. Builder Class. There is a separate 'builder' class. For example, modifiable Strings are created using StringBuffer (which doesn't have the full String API available). Once you want an immutable form, you create one with toString().
 3. Primitives. These are always safe, since they are copied on input/output from methods.
4. Cloning. Where you need an object to be safe, you clone it.

There are advantages and disadvantages of each of these.

1. Const provides a certain level of protection, but since const can be and is often cast away, it only protects against most inadvertent mistakes. It also offers no threading protection, since anyone who has a pointer to the (unconst) object in another thread can mess you up.
2. Immutable wrappers are safer than const in that the constness can't be cast away. But other than that they have all the same problems: not safe if someone else keeps hold of the original object, or if any of the objects returned by the class are mutable.
3. Always-Immutable Objects are safe, but usage can require excessive object creation.
4. Cloning is only safe if the object truly has a 'safe' clone; defined as one that*ensures that no change to the clone affects the original*. Unfortunately, many objects don't have a 'safe' clone, and always cloning can require excessive object creation.

## Freezable Model

The`Freezable`model supplements these choices by giving you the ability to build up an object by calling various methods, then when it is in a final state, you can*make* it immutable. Once immutable, an object cannot*ever* be modified, and is completely thread-safe: that is, multiple threads can have references to it without any synchronization. If someone needs a mutable version of an object, they can use`cloneAsThawed()`, and modify the copy. This provides a simple, effective mechanism for safe classes in circumstances where the alternatives are insufficient or clumsy. (If an object is shared before it is immutable, then it is the responsibility of each thread to mutex its usage (as with other objects).)

Here is what needs to be done to implement this interface, depending on the type of the object.

### **Immutable Objects**

These are the easiest. You just use the interface to reflect that, by adding the following: 

```kotlin
public class A implements Freezable<A> {
    ...
    public final boolean isFrozen() {return true;}
    public final A freeze() {return this;}
    public final A cloneAsThawed() { return this; }
    }
  
```

These can be final methods because subclasses of immutable objects must themselves be immutable. (Note:`freeze`is returning`this`for chaining.)

### **Mutable Objects**

Add a protected 'flagging' field: 

```kotlin
protected volatile boolean frozen; // WARNING: must be volatile
  
```

Add the following methods: 

```kotlin
public final boolean isFrozen() {
       return frozen;
  };
 
  public A freeze() {
       frozen = true;  // WARNING: must be final statement before return
       return this;
  }
  
```

Add a`cloneAsThawed()`method following the normal pattern for`clone()`, except that`frozen=false`in the new clone.

Then take the setters (that is, any method that can change the internal state of the object), and add the following as the first statement: 

```kotlin
if (isFrozen()) {
       throw new UnsupportedOperationException("Attempt to modify frozen object");
  }
  
```

#### **Subclassing**

Any subclass of a`Freezable`will just use its superclass's flagging field. It must override`freeze()`and`cloneAsThawed()`to call the superclass, but normally does not override`isFrozen()`. It must then just pay attention to its own getters, setters and fields.

#### **Internal Caches**

Internal caches are cases where the object is logically unmodified, but internal state of the object changes. For example, there are const C++ functions that cast away the const on the "this" pointer in order to modify an object cache. These cases are handled by mutexing the internal cache to ensure thread-safety. For example, suppose that UnicodeSet had an internal marker to the last code point accessed. In this case, the field is not externally visible, so the only thing you need to do is to synchronize the field for thread safety.

#### Unsafe Internal Access

Internal fields are called*safe* if they are either`frozen`or immutable (such as String or primitives). If you've never allowed internal access to these, then you are all done. For example, converting UnicodeSet to be`Freezable`is just accomplished with the above steps. But remember that you***have***allowed access to unsafe internals if you have any code like the following, in a getter, setter, or constructor: 

```kotlin
Collection getStuff() {
       return stuff;
  } // caller could keep reference & modify
 
  void setStuff(Collection x) {
       stuff = x;
  } // caller could keep reference & modify
 
  MyClass(Collection x) {
       stuff = x;
  } // caller could keep reference & modify
  
```

These also illustrated in the code sample in**Background**above.

To deal with unsafe internals, the simplest course of action is to do the work in the`freeze()`function. Just make all of your internal fields frozen, and set the frozen flag. Any subsequent getter/setter will work properly. Here is an example:

**Warning!**The 'frozen' boolean MUST be volatile, and must be set as the last statement in the method. 

```kotlin
public A freeze() {
       if (!frozen) {
               foo.freeze();
               frozen = true;
       }
       return this;
  }
  
```

If the field is a`Collection`or`Map`, then to make it frozen you have two choices. If you have never allowed access to the collection from outside your object, then just wrap it to prevent future modification. 

```kotlin
zone_to_country = Collections.unmodifiableMap(zone_to_country);
  
```

If you have*ever* allowed access, then do a`clone()`before wrapping it. 

```kotlin
zone_to_country = Collections.unmodifiableMap(zone_to_country.clone());
  
```

If a collection*(or any other container of objects)*itself can contain mutable objects, then for a safe clone you need to recurse through it to make the entire collection immutable. The recursing code should pick the most specific collection available, to avoid the necessity of later downcasing.

**Note:** An annoying flaw in Java is that the generic collections, like`Map`or`Set`, don't have a`clone()`operation. When you don't know the type of the collection, the simplest course is to just create a new collection: 

```kotlin
zone_to_country = Collections.unmodifiableMap(new HashMap(zone_to_country));
  
```

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstractT | [cloneAsThawed](https://developer.android.com/reference/kotlin/android/icu/util/Freezable#cloneAsThawed())`()` Provides for the clone operation. |
| abstractT | [freeze](https://developer.android.com/reference/kotlin/android/icu/util/Freezable#freeze())`()` Freezes the object. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFrozen](https://developer.android.com/reference/kotlin/android/icu/util/Freezable#isFrozen())`()` Determines whether the object has been frozen or not. |
| --- | --- |

## Public methods

### cloneAsThawed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun cloneAsThawed(): T
```

Provides for the clone operation. Any clone is initially unfrozen. 

### freeze

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun freeze(): T
```

Freezes the object.

| Return ||
|---|--------------------|
| T | the object itself. |

### isFrozen

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isFrozen(): Boolean
```

Determines whether the object has been frozen or not.
