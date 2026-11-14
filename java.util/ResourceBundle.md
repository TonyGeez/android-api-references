Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ResourceBundle

```
abstract class ResourceBundle
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.ResourceBundle](ResourceBundle.md) |

Known Direct Subclasses [ListResourceBundle](ListResourceBundle.md), [PropertyResourceBundle](PropertyResourceBundle.md) [ListResourceBundle](ListResourceBundle.md) `ListResourceBundle` is an abstract subclass of `ResourceBundle` that manages resources for a locale in a convenient and easy to use list.
[PropertyResourceBundle](PropertyResourceBundle.md) `PropertyResourceBundle` is a concrete subclass of `ResourceBundle` that manages resources for a locale using a set of static strings from a property file.

Resource bundles contain locale-specific objects. When your program needs a locale-specific resource, a for example, your program can load it from the resource bundle that is appropriate for the current user's locale. In this way, you can write program code that is largely independent of the user's locale isolating most, if not all, of the locale-specific information in resource bundles.

This allows you to write programs that can:

- be easily localized, or translated, into different languages
- handle multiple locales at once
- be easily modified later to support even more locales

Resource bundles belong to families whose members share a common base name, but whose names also have additional components that identify their locales. For example, the base name of a family of resource bundles might be "MyResources". The family should have a default resource bundle which simply has the same name as its family - "MyResources" - and will be used as the bundle of last resort if a specific locale is not supported. The family can then provide as many locale-specific members as needed, for example a German one named "MyResources_de".

Each resource bundle in a family contains the same items, but the items have been translated for the locale represented by that resource bundle. For example, both "MyResources" and "MyResources_de" may have a `String` that's used on a button for canceling operations. In "MyResources" the `String` may contain "Cancel" and in "MyResources_de" it may contain "Abbrechen".

If there are different resources for different countries, you can make specializations: for example, "MyResources_de_CH" contains objects for the German language (de) in Switzerland (CH). If you want to only modify some of the resources in the specialization, you can do so.

When your program needs a locale-specific object, it loads the `ResourceBundle` class using the `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#getBundle(kotlin.String,%20java.util.Locale)` method:

```kotlin
ResourceBundle myResources =
       ResourceBundle.getBundle("MyResources", currentLocale);
  
```

Resource bundles contain key/value pairs. The keys uniquely identify a locale-specific object in the bundle. Here's an example of a `ListResourceBundle` that contains two key/value pairs:

```kotlin
public class MyResources extends ListResourceBundle {
      protected Object[][] getContents() {
          return new Object[][] {
              // LOCALIZE THE SECOND STRING OF EACH ARRAY (e.g., "OK")
              {"OkKey", "OK"},
              {"CancelKey", "Cancel"},
              // END OF MATERIAL TO LOCALIZE
         };
      }
  }
  
```
Keys are always `String`s. In this example, the keys are "OkKey" and "CancelKey". In the above example, the values are also `String`s--"OK" and "Cancel"--but they don't have to be. The values can be any type of object.

You retrieve an object from resource bundle using the appropriate getter method. Because "OkKey" and "CancelKey" are both strings, you would use `getString` to retrieve them:

```kotlin
button1 = new Button(myResources.getString("OkKey"));
  button2 = new Button(myResources.getString("CancelKey"));
  
```
The getter methods all require the key as an argument and return the object if found. If the object is not found, the getter method throws a `MissingResourceException`.

Besides `getString`, `ResourceBundle` also provides a method for getting string arrays, `getStringArray`, as well as a generic `getObject` method for any other type of object. When using `getObject`, you'll have to cast the result to the appropriate type. For example:

```kotlin
int[] myIntegers = (int[]) myResources.getObject("intList");
  
```

The Java Platform provides two subclasses of `ResourceBundle`, `ListResourceBundle` and `PropertyResourceBundle`, that provide a fairly simple way to create resources. As you saw briefly in a previous example, `ListResourceBundle` manages its resource as a list of key/value pairs. `PropertyResourceBundle` uses a properties file to manage its resources.

If `ListResourceBundle` or `PropertyResourceBundle` do not suit your needs, you can write your own `ResourceBundle` subclass. Your subclasses must override two methods: `handleGetObject` and `getKeys()`.

The implementation of a `ResourceBundle` subclass must be thread-safe if it's simultaneously used by multiple threads. The default implementations of the non-abstract methods in this class, and the methods in the direct known concrete subclasses `ListResourceBundle` and `PropertyResourceBundle` are thread-safe.

### ResourceBundle.Control

The `https://developer.android.com/reference/kotlin/java/util/ResourceBundle.Control` class provides information necessary to perform the bundle loading process by the `getBundle` factory methods that take a `ResourceBundle.Control` instance. You can implement your own subclass in order to enable non-standard resource bundle formats, change the search strategy, or define caching parameters. Refer to the descriptions of the class and the `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#getBundle(kotlin.String,%20java.util.Locale,%20java.lang.ClassLoader,%20java.util.ResourceBundle.Control)` factory method for details.

### Cache Management

Resource bundle instances created by the `getBundle` factory methods are cached by default, and the factory methods return the same resource bundle instance multiple times if it has been cached. `getBundle` clients may clear the cache, manage the lifetime of cached resource bundle instances using time-to-live values, or specify not to cache resource bundle instances. Refer to the descriptions of the [`getBundle` factory method](ResourceBundle.md)), `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#clearCache(java.lang.ClassLoader)`, `https://developer.android.com/reference/kotlin/java/util/ResourceBundle.Control#getTimeToLive(kotlin.String,%20java.util.Locale)`, and `https://developer.android.com/reference/kotlin/java/util/ResourceBundle.Control#needsReload(kotlin.String,%20java.util.Locale,%20kotlin.String,%20java.lang.ClassLoader,%20java.util.ResourceBundle,%20kotlin.Long)` for details.

### Example

The following is a very simple example of a `ResourceBundle` subclass, `MyResources`, that manages two resources (for a larger number of resources you would probably use a `Map`). Notice that you don't need to supply a value if a "parent-level" `ResourceBundle` handles the same key with the same value (as for the okKey below).

```kotlin
// default (English language, United States)
  public class MyResources extends ResourceBundle {
      public Object handleGetObject(String key) {
          if (key.equals("okKey")) return "Ok";
          if (key.equals("cancelKey")) return "Cancel";
          return null;
      }
 
      public Enumeration<String> getKeys() {
          return Collections.enumeration(keySet());
      }
 
      // Overrides handleKeySet() so that the getKeys() implementation
      // can rely on the keySet() value.
      protected Set<String> handleKeySet() {
          return new HashSet<String>(Arrays.asList("okKey", "cancelKey"));
      }
  }
 
  // German language
  public class MyResources_de extends MyResources {
      public Object handleGetObject(String key) {
          // don't need okKey, since parent level handles it.
          if (key.equals("cancelKey")) return "Abbrechen";
          return null;
      }
 
      protected Set<String> handleKeySet() {
          return new HashSet<String>(Arrays.asList("cancelKey"));
      }
  }
  
```
You do not have to restrict yourself to using a single family of `ResourceBundle`s. For example, you could have a set of bundles for exception messages, `ExceptionResources` (`ExceptionResources_fr`, `ExceptionResources_de`, ...), and one for widgets, `WidgetResource` (`WidgetResources_fr`, `WidgetResources_de`, ...); breaking up the resources however you like.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/java/util/ResourceBundle.Control` `ResourceBundle.Control` defines a set of callback methods that are invoked by the `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#getBundle(kotlin.String,%20java.util.Locale,%20java.lang.ClassLoader,%20java.util.ResourceBundle.Control)` factory methods during the bundle loading process. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#ResourceBundle()()` Sole constructor. |

| Public methods ||
|---|---|
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#clearCache()()` Removes all resource bundles from the cache that have been loaded using the caller's class loader. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#clearCache(java.lang.ClassLoader)(loader: https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#!)` Removes all resource bundles from the cache that have been loaded by the given class loader. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#containsKey(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Determines whether the given `key` is contained in this `ResourceBundle` or its parent bundles. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#getBaseBundleName()()` Returns the base name of this bundle, if known, or `null` if unknown. |
| static [ResourceBundle](ResourceBundle.md)! | `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#getBundle(kotlin.String)(baseName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Gets a resource bundle using the specified base name, the default locale, and the caller's class loader. |
| static [ResourceBundle](ResourceBundle.md)! | `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#getBundle(kotlin.String,%20java.util.Locale)(baseName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, locale: https://developer.android.com/reference/kotlin/java/util/Locale!)` Gets a resource bundle using the specified base name and locale, and the caller's class loader. |
| --- | --- |
| open static [ResourceBundle](ResourceBundle.md)! | `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#getBundle(kotlin.String,%20java.util.Locale,%20java.lang.ClassLoader)(baseName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, locale: https://developer.android.com/reference/kotlin/java/util/Locale!, loader: https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#!)` Gets a resource bundle using the specified base name, locale, and class loader. |
| open static [ResourceBundle](ResourceBundle.md)! | `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#getBundle(kotlin.String,%20java.util.Locale,%20java.lang.ClassLoader,%20java.util.ResourceBundle.Control)(baseName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, targetLocale: https://developer.android.com/reference/kotlin/java/util/Locale!, loader: https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#!, control: https://developer.android.com/reference/kotlin/java/util/ResourceBundle.Control!)` Returns a resource bundle using the specified base name, target locale, class loader and control. |
| static [ResourceBundle](ResourceBundle.md)! | `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#getBundle(kotlin.String,%20java.util.Locale,%20java.util.ResourceBundle.Control)(baseName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, targetLocale: https://developer.android.com/reference/kotlin/java/util/Locale!, control: https://developer.android.com/reference/kotlin/java/util/ResourceBundle.Control!)` Returns a resource bundle using the specified base name, target locale and control, and the caller's class loader. |
| --- | --- |
| static [ResourceBundle](ResourceBundle.md)! | `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#getBundle(kotlin.String,%20java.util.ResourceBundle.Control)(baseName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, control: https://developer.android.com/reference/kotlin/java/util/ResourceBundle.Control!)` Returns a resource bundle using the specified base name, the default locale and the specified control. |
| abstract [Enumeration](Enumeration.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#getKeys()()` Returns an enumeration of the keys. |
| open [Locale](Locale.md)! | `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#getLocale()()` Returns the locale of this resource bundle. |
| --- | --- |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#getObject(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Gets an object for the given key from this resource bundle or one of its parents. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#getString(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Gets a string for the given key from this resource bundle or one of its parents. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#getStringArray(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Gets a string array for the given key from this resource bundle or one of its parents. |
| --- | --- |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#keySet()()` Returns a `Set` of all keys contained in this `ResourceBundle` and its parent bundles. |

| Protected methods ||
|---|---|
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#handleGetObject(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Gets an object for the given key from this resource bundle. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#handleKeySet()()` Returns a `Set` of the keys contained *only* in this `ResourceBundle`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#setParent(java.util.ResourceBundle)(parent: https://developer.android.com/reference/kotlin/java/util/ResourceBundle#!)` Sets the parent bundle of this bundle. |
| --- | --- |

| Properties ||
|---|---|
| [ResourceBundle](ResourceBundle.md)! | `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#parent:java.util.ResourceBundle` The parent bundle of this bundle. |

## Public constructors

### ResourceBundle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ResourceBundle()
```

Sole constructor. (For invocation by subclass constructors, typically implicit.)

## Public methods

### clearCache

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun clearCache(): Unit
```

Removes all resource bundles from the cache that have been loaded using the caller's class loader.
**See Also**

- `https://developer.android.com/reference/kotlin/java/util/ResourceBundle.Control#getTimeToLive(kotlin.String,%20java.util.Locale)`

### clearCache

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun clearCache(loader: ClassLoader!): Unit
```

Removes all resource bundles from the cache that have been loaded by the given class loader.

| Parameters ||
|---|---|
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)!: the class loader |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `loader` is null |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/ResourceBundle.Control#getTimeToLive(kotlin.String,%20java.util.Locale)`

### containsKey

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun containsKey(key: String!): Boolean
```

Determines whether the given `key` is contained in this `ResourceBundle` or its parent bundles.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the resource `key` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the given `key` is contained in this `ResourceBundle` or its parent bundles; `false` otherwise. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `key` is `null` |

### getBaseBundleName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBaseBundleName(): String!
```

Returns the base name of this bundle, if known, or `null` if unknown. If not null, then this is the value of the `baseName` parameter that was passed to the `ResourceBundle.getBundle(...)` method when the resource bundle was loaded.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The base name of the resource bundle, as provided to and expected by the `ResourceBundle.getBundle(...)` methods. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#getBundle(kotlin.String,%20java.util.Locale,%20java.lang.ClassLoader)`

### getBundle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getBundle(baseName: String!): ResourceBundle!
```

Gets a resource bundle using the specified base name, the default locale, and the caller's class loader. Calling this method is equivalent to calling `getBundle(baseName, Locale.getDefault(), this.getClass().getClassLoader())`,

| Parameters ||
|---|---|
| `baseName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the base name of the resource bundle, a fully qualified class name |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#!` | a resource bundle for the given base name and the default locale |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `baseName` is `null` |
| `java.util.MissingResourceException` | if no resource bundle for the specified base name can be found |

**See Also**

### getBundle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getBundle(
    baseName: String!, 
    locale: Locale!
): ResourceBundle!
```

Gets a resource bundle using the specified base name and locale, and the caller's class loader. Calling this method is equivalent to calling `getBundle(baseName, locale, this.getClass().getClassLoader())`,

| Parameters ||
|---|---|
| `baseName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the base name of the resource bundle, a fully qualified class name |
| `locale` | [Locale](Locale.md)!: the locale for which a resource bundle is desired |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#!` | a resource bundle for the given base name and locale |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `baseName` or `locale` is `null` |
| `java.util.MissingResourceException` | if no resource bundle for the specified base name can be found |

**See Also**

### getBundle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getBundle(
    baseName: String!, 
    locale: Locale!, 
    loader: ClassLoader!
): ResourceBundle!
```

Gets a resource bundle using the specified base name, locale, and class loader. This is equivalent to calling:

```kotlin
getBundle(baseName, targetLocale, loader, control)
  
```
passing a default instance of `https://developer.android.com/reference/kotlin/java/util/ResourceBundle.Control`. Refer to the description of [modifying the default behavior](ResourceBundle.md). The following describes the default behavior.

<br />

**Resource Bundle Search and Loading Strategy**

`getBundle` uses the base name, the specified locale, and the default locale (obtained from `https://developer.android.com/reference/kotlin/java/util/Locale#getDefault()`) to generate a sequence of *candidate bundle names*. If the specified locale's language, script, country, and variant are all empty strings, then the base name is the only candidate bundle name. Otherwise, a list of candidate locales is generated from the attribute values of the specified locale (language, script, country and variant) and appended to the base name. Typically, this will look like the following:

```kotlin
baseName + "_" + language + "_" + script + "_" + country + "_" + variant
      baseName + "_" + language + "_" + script + "_" + country
      baseName + "_" + language + "_" + script
      baseName + "_" + language + "_" + country + "_" + variant
      baseName + "_" + language + "_" + country
      baseName + "_" + language
  
```

Candidate bundle names where the final component is an empty string are omitted, along with the underscore. For example, if country is an empty string, the second and the fifth candidate bundle names above would be omitted. Also, if script is an empty string, the candidate names including script are omitted. For example, a locale with language "de" and variant "JAVA" will produce candidate names with base name "MyResource" below.

```kotlin
MyResource_de__JAVA
      MyResource_de
  
```
In the case that the variant contains one or more underscores ('_'), a sequence of bundle names generated by truncating the last underscore and the part following it is inserted after a candidate bundle name with the original variant. For example, for a locale with language "en", script "Latn, country "US" and variant "WINDOWS_VISTA", and bundle base name "MyResource", the list of candidate bundle names below is generated:

```kotlin
MyResource_en_Latn_US_WINDOWS_VISTA
  MyResource_en_Latn_US_WINDOWS
  MyResource_en_Latn_US
  MyResource_en_Latn
  MyResource_en_US_WINDOWS_VISTA
  MyResource_en_US_WINDOWS
  MyResource_en_US
  MyResource_en
  
```
**Note:** For some `Locale`s, the list of candidate bundle names contains extra names, or the order of bundle names is slightly modified. See the description of the default implementation of `https://developer.android.com/reference/kotlin/java/util/ResourceBundle.Control#getCandidateLocales(kotlin.String,%20java.util.Locale)` for details.

`getBundle` then iterates over the candidate bundle names to find the first one for which it can *instantiate* an actual resource bundle. It uses the default controls' `https://developer.android.com/reference/kotlin/java/util/ResourceBundle.Control#getFormats(kotlin.String)` method, which generates two bundle names for each generated name, the first a class name and the second a properties file name. For each candidate bundle name, it attempts to create a resource bundle:

- First, it attempts to load a class using the generated class name. If such a class can be found and loaded using the specified class loader, is assignment compatible with ResourceBundle, is accessible from ResourceBundle, and can be instantiated, `getBundle` creates a new instance of this class and uses it as the *result resource bundle*.
- Otherwise, `getBundle` attempts to locate a property resource file using the generated properties file name. It generates a path name from the candidate bundle name by replacing all "." characters with "/" and appending the string ".properties". It attempts to find a "resource" with this name using `https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#getResource(kotlin.String)`. (Note that a "resource" in the sense of `getResource` has nothing to do with the contents of a resource bundle, it is just a container of data, such as a file.) If it finds a "resource", it attempts to create a new `https://developer.android.com/reference/kotlin/java/util/PropertyResourceBundle` instance from its contents. If successful, this instance becomes the *result resource bundle*.

This continues until a result resource bundle is instantiated or the list of candidate bundle names is exhausted. If no matching resource bundle is found, the default control's `https://developer.android.com/reference/kotlin/java/util/ResourceBundle.Control#getFallbackLocale(kotlin.String,%20java.util.Locale)` method is called, which returns the current default locale. A new sequence of candidate locale names is generated using this locale and searched again, as above.

If still no result bundle is found, the base name alone is looked up. If this still fails, a `MissingResourceException` is thrown.

Once a result resource bundle has been found, its *parent chain* is instantiated. If the result bundle already has a parent (perhaps because it was returned from a cache) the chain is complete.

Otherwise, `getBundle` examines the remainder of the candidate locale list that was used during the pass that generated the result resource bundle. (As before, candidate bundle names where the final component is an empty string are omitted.) When it comes to the end of the candidate list, it tries the plain bundle name. With each of the candidate bundle names it attempts to instantiate a resource bundle (first looking for a class and then a properties file, as described above).

Whenever it succeeds, it calls the previously instantiated resource bundle's `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#setParent(java.util.ResourceBundle)` method with the new resource bundle. This continues until the list of names is exhausted or the current bundle already has a non-null parent.

Once the parent chain is complete, the bundle is returned.

**Note:** `getBundle` caches instantiated resource bundles and might return the same resource bundle instance multiple times.

**Note:** The `baseName` argument should be a fully qualified class name. However, for compatibility with earlier versions, Java SE Runtime Environments do not verify this, and so it is possible to access `PropertyResourceBundle`s by specifying a path name (using "/") instead of a fully qualified class name (using ".").

**Example:**

The following class and property files are provided:

- MyResources.class
- MyResources.properties
- MyResources_fr.properties
- MyResources_fr_CH.class
- MyResources_fr_CH.properties
- MyResources_en.properties
- MyResources_es_ES.class

The contents of all files are valid (that is, public non-abstract subclasses of `ResourceBundle` for the ".class" files, syntactically correct ".properties" files). The default locale is `Locale("en", "GB")`.

Calling `getBundle` with the locale arguments below will instantiate resource bundles as follows:

| Locale | Resource bundle |
| --- | --- |
| Locale("fr", "CH") | MyResources_fr_CH.class, parent MyResources_fr.properties, parent MyResources.class |
| Locale("fr", "FR") | MyResources_fr.properties, parent MyResources.class |
| Locale("de", "DE") | MyResources_en.properties, parent MyResources.class |
| --- | --- |
| Locale("en", "US") | MyResources_en.properties, parent MyResources.class |
| Locale("es", "ES") | MyResources_es_ES.class, parent MyResources.class |
|---|---|

The file MyResources_fr_CH.properties is never used because it is hidden by the MyResources_fr_CH.class. Likewise, MyResources.properties is also hidden by MyResources.class.

| Parameters ||
|---|---|
| `baseName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the base name of the resource bundle, a fully qualified class name |
| `locale` | [Locale](Locale.md)!: the locale for which a resource bundle is desired |
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)!: the class loader from which to load the resource bundle |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#!` | a resource bundle for the given base name and locale |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `baseName`, `locale`, or `loader` is `null` |
| `java.util.MissingResourceException` | if no resource bundle for the specified base name can be found |

### getBundle

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getBundle(
    baseName: String!, 
    targetLocale: Locale!, 
    loader: ClassLoader!, 
    control: ResourceBundle.Control!
): ResourceBundle!
```

Returns a resource bundle using the specified base name, target locale, class loader and control. Unlike the `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#getBundle(kotlin.String,%20java.util.Locale,%20java.lang.ClassLoader)` factory methods with no `control` argument, the given `control` specifies how to locate and instantiate resource bundles. Conceptually, the bundle loading process with the given `control` is performed in the following steps.

1. This factory method looks up the resource bundle in the cache for the specified `baseName`, `targetLocale` and `loader`. If the requested resource bundle instance is found in the cache and the time-to-live periods of the instance and all of its parent instances have not expired, the instance is returned to the caller. Otherwise, this factory method proceeds with the loading process below.
2. The `https://developer.android.com/reference/kotlin/java/util/ResourceBundle.Control#getFormats(kotlin.String)` method is called to get resource bundle formats to produce bundle or resource names. The strings `"java.class"` and `"java.properties"` designate class-based and [property](PropertyResourceBundle.md)-based resource bundles, respectively. Other strings starting with `"java."` are reserved for future extensions and must not be used for application-defined formats. Other strings designate application-defined formats.
3. The `https://developer.android.com/reference/kotlin/java/util/ResourceBundle.Control#getCandidateLocales(kotlin.String,%20java.util.Locale)` method is called with the target locale to get a list of *candidate `Locale`s* for which resource bundles are searched.
4. The `https://developer.android.com/reference/kotlin/java/util/ResourceBundle.Control#newBundle(kotlin.String,%20java.util.Locale,%20kotlin.String,%20java.lang.ClassLoader,%20kotlin.Boolean)` method is called to instantiate a `ResourceBundle` for the base bundle name, a candidate locale, and a format. (Refer to the note on the cache lookup below.) This step is iterated over all combinations of the candidate locales and formats until the `newBundle` method returns a `ResourceBundle` instance or the iteration has used up all the combinations. For example, if the candidate locales are `Locale("de", "DE")`, `Locale("de")` and `Locale("")` and the formats are `"java.class"` and `"java.properties"`, then the following is the sequence of locale-format combinations to be used to call `control.newBundle`.

 | Index | `Locale` | `format` |
| --- | --- | --- |
 | 1 | `Locale("de", "DE")` | `java.class` |
 | 2 | `Locale("de", "DE")` | `java.properties` |
 | 3 | `Locale("de")` | `java.class` |
| --- | --- | --- |
 | 4 | `Locale("de")` | `java.properties` |
 | 5 | `Locale("")` | `java.class` |
 | 6 | `Locale("")` | `java.properties` |
 |---|---|---|

5. If the previous step has found no resource bundle, proceed to Step 6. If a bundle has been found that is a base bundle (a bundle for `Locale("")`), and the candidate locale list only contained `Locale("")`, return the bundle to the caller. If a bundle has been found that is a base bundle, but the candidate locale list contained locales other than Locale(""), put the bundle on hold and proceed to Step 6. If a bundle has been found that is not a base bundle, proceed to Step 7.
6. The `https://developer.android.com/reference/kotlin/java/util/ResourceBundle.Control#getFallbackLocale(kotlin.String,%20java.util.Locale)` method is called to get a fallback locale (alternative to the current target locale) to try further finding a resource bundle. If the method returns a non-null locale, it becomes the next target locale and the loading process starts over from Step 3. Otherwise, if a base bundle was found and put on hold in a previous Step 5, it is returned to the caller now. Otherwise, a MissingResourceException is thrown.
7. At this point, we have found a resource bundle that's not the base bundle. If this bundle set its parent during its instantiation, it is returned to the caller. Otherwise, its [parent chain](ResourceBundle.md) is instantiated based on the list of candidate locales from which it was found. Finally, the bundle is returned to the caller.

<br />

During the resource bundle loading process above, this factory method looks up the cache before calling the `https://developer.android.com/reference/kotlin/java/util/ResourceBundle.Control#newBundle(kotlin.String,%20java.util.Locale,%20kotlin.String,%20java.lang.ClassLoader,%20kotlin.Boolean)` method. If the time-to-live period of the resource bundle found in the cache has expired, the factory method calls the `https://developer.android.com/reference/kotlin/java/util/ResourceBundle.Control#needsReload(kotlin.String,%20java.util.Locale,%20kotlin.String,%20java.lang.ClassLoader,%20java.util.ResourceBundle,%20kotlin.Long)` method to determine whether the resource bundle needs to be reloaded. If reloading is required, the factory method calls `control.newBundle` to reload the resource bundle. If `control.newBundle` returns `null`, the factory method puts a dummy resource bundle in the cache as a mark of nonexistent resource bundles in order to avoid lookup overhead for subsequent requests. Such dummy resource bundles are under the same expiration control as specified by `control`.

All resource bundles loaded are cached by default. Refer to `https://developer.android.com/reference/kotlin/java/util/ResourceBundle.Control#getTimeToLive(kotlin.String,%20java.util.Locale)` for details.

The following is an example of the bundle loading process with the default `ResourceBundle.Control` implementation.

Conditions:

- Base bundle name: `foo.bar.Messages`
- Requested `Locale`: `https://developer.android.com/reference/kotlin/java/util/Locale#ITALY:java.util.Locale`
- Default `Locale`: `https://developer.android.com/reference/kotlin/java/util/Locale#FRENCH:java.util.Locale`
- Available resource bundles: `foo/bar/Messages_fr.properties` and `foo/bar/Messages.properties`

First, `getBundle` tries loading a resource bundle in the following sequence.

- class `foo.bar.Messages_it_IT`
- file `foo/bar/Messages_it_IT.properties`
- class `foo.bar.Messages_it`
- file `foo/bar/Messages_it.properties`
- class `foo.bar.Messages`
- file `foo/bar/Messages.properties`

At this point, `getBundle` finds `foo/bar/Messages.properties`, which is put on hold because it's the base bundle. `getBundle` calls `https://developer.android.com/reference/kotlin/java/util/ResourceBundle.Control#getFallbackLocale(kotlin.String,%20java.util.Locale)` which returns `Locale.FRENCH`. Next, `getBundle` tries loading a bundle in the following sequence.

- class `foo.bar.Messages_fr`
- file `foo/bar/Messages_fr.properties`
- class `foo.bar.Messages`
- file `foo/bar/Messages.properties`

`getBundle` finds `foo/bar/Messages_fr.properties` and creates a `ResourceBundle` instance. Then, `getBundle` sets up its parent chain from the list of the candidate locales. Only `foo/bar/Messages.properties` is found in the list and `getBundle` creates a `ResourceBundle` instance that becomes the parent of the instance for `foo/bar/Messages_fr.properties`.

| Parameters ||
|---|---|
| `baseName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the base name of the resource bundle, a fully qualified class name |
| `targetLocale` | [Locale](Locale.md)!: the locale for which a resource bundle is desired |
| `loader` | [ClassLoader](../java.lang/ClassLoader.md)!: the class loader from which to load the resource bundle |
| --- | --- |
| `control` | [ResourceBundle.Control](../java/util/ResourceBundle.Control.md)!: the control which gives information for the resource bundle loading process |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#!` | a resource bundle for the given base name and locale |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the given `control` doesn't perform properly (e.g., `control.getCandidateLocales` returns null.) Note that validation of `control` is performed as needed. |
| `java.lang.NullPointerException` | if `baseName`, `targetLocale`, `loader`, or `control` is `null` |
| `java.util.MissingResourceException` | if no resource bundle for the specified base name can be found |
| --- | --- |

### getBundle

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getBundle(
    baseName: String!, 
    targetLocale: Locale!, 
    control: ResourceBundle.Control!
): ResourceBundle!
```

Returns a resource bundle using the specified base name, target locale and control, and the caller's class loader. Calling this method is equivalent to calling

```kotlin
getBundle(baseName, targetLocale, this.getClass().getClassLoader(),
            control),
  
```
except that `getClassLoader()` is run with the security privileges of `ResourceBundle`. See `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#getBundle(kotlin.String,%20java.util.Locale,%20java.lang.ClassLoader,%20java.util.ResourceBundle.Control)` for the complete description of the resource bundle loading process with a `ResourceBundle.Control`.

<br />

| Parameters ||
|---|---|
| `baseName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the base name of the resource bundle, a fully qualified class name |
| `targetLocale` | [Locale](Locale.md)!: the locale for which a resource bundle is desired |
| `control` | [ResourceBundle.Control](../java/util/ResourceBundle.Control.md)!: the control which gives information for the resource bundle loading process |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#!` | a resource bundle for the given base name and a `Locale` in `locales` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the given `control` doesn't perform properly (e.g., `control.getCandidateLocales` returns null.) Note that validation of `control` is performed as needed. |
| `java.lang.NullPointerException` | if `baseName`, `locales` or `control` is `null` |
| `java.util.MissingResourceException` | if no resource bundle for the specified base name in any of the `locales` can be found. |
| --- | --- |

### getBundle

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getBundle(
    baseName: String!, 
    control: ResourceBundle.Control!
): ResourceBundle!
```

Returns a resource bundle using the specified base name, the default locale and the specified control. Calling this method is equivalent to calling

```kotlin
getBundle(baseName, Locale.getDefault(),
            this.getClass().getClassLoader(), control),
  
```
except that `getClassLoader()` is run with the security privileges of `ResourceBundle`. See `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#getBundle(kotlin.String,%20java.util.Locale,%20java.lang.ClassLoader,%20java.util.ResourceBundle.Control)` for the complete description of the resource bundle loading process with a `ResourceBundle.Control`.

<br />

| Parameters ||
|---|---|
| `baseName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the base name of the resource bundle, a fully qualified class name |
| `control` | [ResourceBundle.Control](../java/util/ResourceBundle.Control.md)!: the control which gives information for the resource bundle loading process |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#!` | a resource bundle for the given base name and the default locale |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the given `control` doesn't perform properly (e.g., `control.getCandidateLocales` returns null.) Note that validation of `control` is performed as needed. |
| `java.lang.NullPointerException` | if `baseName` or `control` is `null` |
| `java.util.MissingResourceException` | if no resource bundle for the specified base name can be found |
| --- | --- |

### getKeys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getKeys(): Enumeration<String!>!
```

Returns an enumeration of the keys.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Enumeration<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | an `Enumeration` of the keys contained in this `ResourceBundle` and its parent bundles. |

### getLocale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLocale(): Locale!
```

Returns the locale of this resource bundle. This method can be used after a call to getBundle() to determine whether the resource bundle returned really corresponds to the requested locale or is a fallback.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Locale!` | the locale of this resource bundle |

### getObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getObject(key: String!): Any!
```

Gets an object for the given key from this resource bundle or one of its parents. This method first tries to obtain the object from this resource bundle using `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#handleGetObject(kotlin.String)`. If not successful, and the parent resource bundle is not null, it calls the parent's `getObject` method. If still not successful, it throws a MissingResourceException.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the key for the desired object |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | the object for the given key |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `key` is `null` |
| `java.util.MissingResourceException` | if no object for the given key can be found |

### getString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getString(key: String!): String!
```

Gets a string for the given key from this resource bundle or one of its parents. Calling this method is equivalent to calling ``(String) `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#getObject(kotlin.String)`(key)``.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the key for the desired string |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the string for the given key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the object found for the given key is not a string |
| `java.lang.NullPointerException` | if `key` is `null` |
| `java.util.MissingResourceException` | if no object for the given key can be found |
| --- | --- |

### getStringArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStringArray(key: String!): Array<String!>!
```

Gets a string array for the given key from this resource bundle or one of its parents. Calling this method is equivalent to calling ``(String[]) `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#getObject(kotlin.String)`(key)``.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the key for the desired string array |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | the string array for the given key |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the object found for the given key is not a string array |
| `java.lang.NullPointerException` | if `key` is `null` |
| `java.util.MissingResourceException` | if no object for the given key can be found |
| --- | --- |

### keySet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun keySet(): MutableSet<String!>!
```

Returns a `Set` of all keys contained in this `ResourceBundle` and its parent bundles.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | a `Set` of all keys contained in this `ResourceBundle` and its parent bundles. |

## Protected methods

### handleGetObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun handleGetObject(key: String!): Any!
```

Gets an object for the given key from this resource bundle. Returns null if this resource bundle does not contain an object for the given key.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the key for the desired object |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | the object for the given key, or null |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `key` is `null` |

### handleKeySet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun handleKeySet(): MutableSet<String!>!
```

Returns a `Set` of the keys contained *only* in this `ResourceBundle`.

The default implementation returns a `Set` of the keys returned by the `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#getKeys()` method except for the ones for which the `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#handleGetObject(kotlin.String)` method returns `null`. Once the `Set` has been created, the value is kept in this `ResourceBundle` in order to avoid producing the same `Set` in subsequent calls. Subclasses can override this method for faster handling.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | a `Set` of the keys contained only in this `ResourceBundle` |

### setParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun setParent(parent: ResourceBundle!): Unit
```

Sets the parent bundle of this bundle. The parent bundle is searched by `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#getObject(kotlin.String)` when this bundle does not contain a particular resource.

| Parameters ||
|---|---|
| `parent` | [ResourceBundle](ResourceBundle.md)!: this bundle's parent bundle. |

## Properties

### parent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var parent: ResourceBundle!
```

The parent bundle of this bundle. The parent bundle is searched by `https://developer.android.com/reference/kotlin/java/util/ResourceBundle#getObject(kotlin.String)` when this bundle does not contain a particular resource.
