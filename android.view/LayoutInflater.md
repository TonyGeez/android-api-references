# LayoutInflater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LayoutInflater

Kotlin | [Java](https://developer.android.com/reference/android/view/LayoutInflater "View this page in Java") 

```
abstract class LayoutInflater
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.LayoutInflater](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#) |

Instantiates a layout XML file into its corresponding [android.view.View](https://developer.android.com/reference/kotlin/android/view/View) objects. It is never used directly. Instead, use [android.app.Activity#getLayoutInflater()](https://developer.android.com/reference/kotlin/android/app/Activity.html#getLayoutInflater()) or android.content.Context#getSystemService to retrieve a standard LayoutInflater instance that is already hooked up to the current context and correctly configured for the device you are running on.

To create a new LayoutInflater with an additional [Factory](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Factory) for your own views, you can use [cloneInContext](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#cloneInContext(android.content.Context)) to clone an existing ViewFactory, and then call [setFactory](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#setFactory(android.view.LayoutInflater.Factory)) on it to include your Factory.

For performance reasons, view inflation relies heavily on pre-processing of XML files that is done at build time. Therefore, it is not currently possible to use LayoutInflater with an XmlPullParser over a plain XML file at runtime; it only works with an XmlPullParser returned from a compiled resource (R.*something* file.)

**Note:** This class is **not** thread-safe and a given instance should only be accessed by a single thread.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Factory](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Factory) <br /> |
| abstract | [Factory2](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Factory2) <br /> |
| abstract | [Filter](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Filter) Hook to allow clients of the LayoutInflater to restrict the set of Views that are allowed to be inflated. |

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LayoutInflater](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#LayoutInflater(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Create a new LayoutInflater instance associated with a particular Context. |
| [LayoutInflater](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#LayoutInflater(android.view.LayoutInflater,%20android.content.Context))`(`original:` ` [LayoutInflater](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#)!`, `newContext:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Create a new LayoutInflater instance that is a copy of an existing LayoutInflater, optionally with its Context changed. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [LayoutInflater](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#)! | [cloneInContext](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#cloneInContext(android.content.Context))`(`newContext:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Create a copy of the existing LayoutInflater object, with the copy pointing to a different Context than the original. |
| [View](https://developer.android.com/reference/kotlin/android/view/View)? | [createView](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#createView(android.content.Context,%20kotlin.String,%20kotlin.String,%20android.util.AttributeSet))`(`viewContext:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)?`)` Low-level function for instantiating a view by name. |
| [View](https://developer.android.com/reference/kotlin/android/view/View)! | [createView](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#createView(kotlin.String,%20kotlin.String,%20android.util.AttributeSet))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`)` Low-level function for instantiating a view by name. |
| open static [LayoutInflater](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#)! | [from](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#from(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Obtains the LayoutInflater from the given context. |
| open [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)! | [getContext](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#getContext())`()` Return the context we are running in, for access to resources, class loader, etc. |
| [LayoutInflater.Factory](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Factory)! | [getFactory](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#getFactory())`()` Return the current [Factory](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Factory) (or null). |
| [LayoutInflater.Factory2](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Factory2)! | [getFactory2](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#getFactory2())`()` Return the current [Factory2](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Factory2). |
| open [LayoutInflater.Filter](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Filter)! | [getFilter](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#getFilter())`()` <br /> |
| open [View](https://developer.android.com/reference/kotlin/android/view/View)! | [inflate](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#inflate(kotlin.Int,%20android.view.ViewGroup))`(`resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `root:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup)?`)` Inflate a new view hierarchy from the specified xml resource. |
| open [View](https://developer.android.com/reference/kotlin/android/view/View)! | [inflate](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#inflate(kotlin.Int,%20android.view.ViewGroup,%20kotlin.Boolean))`(`resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `root:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup)?`, `attachToRoot:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Inflate a new view hierarchy from the specified xml resource. |
| open [View](https://developer.android.com/reference/kotlin/android/view/View)! | [inflate](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#inflate(org.xmlpull.v1.XmlPullParser,%20android.view.ViewGroup))`(`parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)!`, `root:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup)?`)` Inflate a new view hierarchy from the specified xml node. |
| open [View](https://developer.android.com/reference/kotlin/android/view/View)! | [inflate](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#inflate(org.xmlpull.v1.XmlPullParser,%20android.view.ViewGroup,%20kotlin.Boolean))`(`parser:` ` [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)!`, `root:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup)?`, `attachToRoot:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Inflate a new view hierarchy from the specified XML node. |
| open [View](https://developer.android.com/reference/kotlin/android/view/View)? | [onCreateView](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#onCreateView(android.content.Context,%20android.view.View,%20kotlin.String,%20android.util.AttributeSet))`(`viewContext:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `parent:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)?`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)?`)` Version of [onCreateView(android.view.View,java.lang.String,android.util.AttributeSet)](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#onCreateView(android.view.View,%20kotlin.String,%20android.util.AttributeSet)) that also takes the inflation context. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFactory](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#setFactory(android.view.LayoutInflater.Factory))`(`factory:` ` [LayoutInflater.Factory](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Factory)!`)` Attach a custom Factory interface for creating views while using this LayoutInflater. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFactory2](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#setFactory2(android.view.LayoutInflater.Factory2))`(`factory:` ` [LayoutInflater.Factory2](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Factory2)!`)` Like [setFactory](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#setFactory(android.view.LayoutInflater.Factory)), but allows you to set a [Factory2](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Factory2) interface. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilter](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#setFilter(android.view.LayoutInflater.Filter))`(`filter:` ` [LayoutInflater.Filter](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Filter)!`)` Sets the [Filter](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Filter) to by this LayoutInflater. |

| Protected methods ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [View](https://developer.android.com/reference/kotlin/android/view/View)! | [onCreateView](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#onCreateView(android.view.View,%20kotlin.String,%20android.util.AttributeSet))`(`parent:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`)` Version of [onCreateView(java.lang.String,android.util.AttributeSet)](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#onCreateView(kotlin.String,%20android.util.AttributeSet)) that also takes the future parent of the view being constructed. |
| open [View](https://developer.android.com/reference/kotlin/android/view/View)! | [onCreateView](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#onCreateView(kotlin.String,%20android.util.AttributeSet))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`)` This routine is responsible for creating the correct subclass of View given the xml element name. |

## Protected constructors

### LayoutInflater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected LayoutInflater(context: Context!)
```

Create a new LayoutInflater instance associated with a particular Context. Applications will almost always want to use android.content.Context#getSystemService to retrieve the standard [Context.INFLATER_SERVICE](https://developer.android.com/reference/kotlin/android/content/Context.html#LAYOUT_INFLATER_SERVICE:kotlin.String).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The Context in which this LayoutInflater will create its Views; most importantly, this supplies the theme from which the default values for their attributes are retrieved. |

### LayoutInflater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected LayoutInflater(
    original: LayoutInflater!, 
    newContext: Context!)
```

Create a new LayoutInflater instance that is a copy of an existing LayoutInflater, optionally with its Context changed. For use in implementing [cloneInContext](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#cloneInContext(android.content.Context)).

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `original` | [LayoutInflater](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#)!: The original LayoutInflater to copy. |
| `newContext` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The new Context to use. |

## Public methods

### cloneInContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun cloneInContext(newContext: Context!): LayoutInflater!
```

Create a copy of the existing LayoutInflater object, with the copy pointing to a different Context than the original. This is used by [ContextThemeWrapper](https://developer.android.com/reference/kotlin/android/view/ContextThemeWrapper) to create a new LayoutInflater to go along with the new Context theme.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newContext` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The new Context to associate with the new LayoutInflater. May be the same as the original Context if desired. |

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [LayoutInflater](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#)! | Returns a brand spanking new LayoutInflater object associated with the given Context. |

### createView

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createView(
    viewContext: Context, 
    name: String, 
    prefix: String?, 
    attrs: AttributeSet?
): View?
```

Low-level function for instantiating a view by name. This attempts to instantiate a view class of the given name found in this LayoutInflater's ClassLoader.

There are two things that can happen in an error case: either the exception describing the error will be thrown, or a null will be returned. You must deal with both possibilities -- the former will happen the first time createView() is called for a class of a particular name, the latter every time there-after for that class name.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `viewContext` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): The context used as the context parameter of the View constructor This value cannot be `null`. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The full name of the class to be instantiated. This value cannot be `null`. |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)?: The XML attributes supplied for this instance. This value may be `null`. |
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

| Return ||
|---------------------------------------------------------------------------|--------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View)? | View The newly instantiated view, or null. |

### createView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createView(
    name: String!, 
    prefix: String!, 
    attrs: AttributeSet!
): View!
```

Low-level function for instantiating a view by name. This attempts to instantiate a view class of the given name found in this LayoutInflater's ClassLoader. To use an explicit Context in the View constructor, use [createView(android.content.Context,java.lang.String,java.lang.String,android.util.AttributeSet)](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#createView(android.content.Context,%20kotlin.String,%20kotlin.String,%20android.util.AttributeSet)) instead.

There are two things that can happen in an error case: either the exception describing the error will be thrown, or a null will be returned. You must deal with both possibilities -- the former will happen the first time createView() is called for a class of a particular name, the latter every time there-after for that class name.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The full name of the class to be instantiated. |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!: The XML attributes supplied for this instance. |

| Return ||
|---------------------------------------------------------------------------|--------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View)! | View The newly instantiated view, or null. |

### from

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun from(context: Context!): LayoutInflater!
```

Obtains the LayoutInflater from the given context. 

### getContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContext(): Context!
```

Return the context we are running in, for access to resources, class loader, etc. 

### getFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFactory(): LayoutInflater.Factory!
```

Return the current [Factory](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Factory) (or null). This is called on each element name. If the factory returns a View, add that to the hierarchy. If it returns null, proceed to call onCreateView(name). 

### getFactory2

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFactory2(): LayoutInflater.Factory2!
```

Return the current [Factory2](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Factory2). Returns null if no factory is set or the set factory does not implement the [Factory2](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Factory2) interface. This is called on each element name. If the factory returns a View, add that to the hierarchy. If it returns null, proceed to call onCreateView(name). 

### getFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFilter(): LayoutInflater.Filter!
```

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LayoutInflater.Filter](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Filter)! | The [Filter](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Filter) currently used by this LayoutInflater to restrict the set of Views that are allowed to be inflated. |

### inflate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun inflate(
    resource: Int, 
    root: ViewGroup?
): View!
```

Inflate a new view hierarchy from the specified xml resource. Throws [InflateException](https://developer.android.com/reference/kotlin/android/view/InflateException) if there is an error.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): ID for an XML layout resource to load (e.g., `R.layout.main_page`) |
| `root` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup)?: Optional view to be the parent of the generated hierarchy. This value may be `null`. |

| Return ||
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View)! | The root View of the inflated hierarchy. If root was supplied, this is the root View; otherwise it is the root of the inflated XML file. |

### inflate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun inflate(
    resource: Int, 
    root: ViewGroup?, 
    attachToRoot: Boolean
): View!
```

Inflate a new view hierarchy from the specified xml resource. Throws [InflateException](https://developer.android.com/reference/kotlin/android/view/InflateException) if there is an error.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): ID for an XML layout resource to load (e.g., `R.layout.main_page`) |
| `root` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup)?: Optional view to be the parent of the generated hierarchy (if *attachToRoot* is true), or else simply an object that provides a set of LayoutParams values for root of the returned hierarchy (if *attachToRoot* is false.) This value may be `null`. |
| `attachToRoot` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether the inflated hierarchy should be attached to the root parameter? If false, root is only used to create the correct subclass of LayoutParams for the root view in the XML. |

| Return ||
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View)! | The root View of the inflated hierarchy. If root was supplied and attachToRoot is true, this is root; otherwise it is the root of the inflated XML file. |

### inflate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun inflate(
    parser: XmlPullParser!, 
    root: ViewGroup?
): View!
```

Inflate a new view hierarchy from the specified xml node. Throws [InflateException](https://developer.android.com/reference/kotlin/android/view/InflateException) if there is an error. \*

***Important*** For performance reasons, view inflation relies heavily on pre-processing of XML files that is done at build time. Therefore, it is not currently possible to use LayoutInflater with an XmlPullParser over a plain XML file at runtime.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parser` | [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)!: XML dom node containing the description of the view hierarchy. |
| `root` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup)?: Optional view to be the parent of the generated hierarchy. This value may be `null`. |

| Return ||
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View)! | The root View of the inflated hierarchy. If root was supplied, this is the root View; otherwise it is the root of the inflated XML file. |

### inflate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun inflate(
    parser: XmlPullParser!, 
    root: ViewGroup?, 
    attachToRoot: Boolean
): View!
```

Inflate a new view hierarchy from the specified XML node. Throws [InflateException](https://developer.android.com/reference/kotlin/android/view/InflateException) if there is an error.

***Important*** For performance reasons, view inflation relies heavily on pre-processing of XML files that is done at build time. Therefore, it is not currently possible to use LayoutInflater with an XmlPullParser over a plain XML file at runtime.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parser` | [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser.html#)!: XML dom node containing the description of the view hierarchy. |
| `root` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup)?: Optional view to be the parent of the generated hierarchy (if *attachToRoot* is true), or else simply an object that provides a set of LayoutParams values for root of the returned hierarchy (if *attachToRoot* is false.) This value may be `null`. |
| `attachToRoot` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether the inflated hierarchy should be attached to the root parameter? If false, root is only used to create the correct subclass of LayoutParams for the root view in the XML. |

| Return ||
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View)! | The root View of the inflated hierarchy. If root was supplied and attachToRoot is true, this is root; otherwise it is the root of the inflated XML file. |

### onCreateView

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCreateView(
    viewContext: Context, 
    parent: View?, 
    name: String, 
    attrs: AttributeSet?
): View?
```

Version of [onCreateView(android.view.View,java.lang.String,android.util.AttributeSet)](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#onCreateView(android.view.View,%20kotlin.String,%20android.util.AttributeSet)) that also takes the inflation context. The default implementation simply calls [onCreateView(android.view.View,java.lang.String,android.util.AttributeSet)](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#onCreateView(android.view.View,%20kotlin.String,%20android.util.AttributeSet)).

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `viewContext` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): The Context to be used as a constructor parameter for the View This value cannot be `null`. |
| `parent` | [View](https://developer.android.com/reference/kotlin/android/view/View)?: The future parent of the returned view. *Note that this may be null.* |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The fully qualified class name of the View to be create. This value cannot be `null`. |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)?: An AttributeSet of attributes to apply to the View. This value may be `null`. |

| Return ||
|---------------------------------------------------------------------------|--------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View)? | View The View created. This value may be `null`. |

### setFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFactory(factory: LayoutInflater.Factory!): Unit
```

Attach a custom Factory interface for creating views while using this LayoutInflater. This must not be null, and can only be set once; after setting, you can not change the factory. This is called on each element name as the xml is parsed. If the factory returns a View, that is added to the hierarchy. If it returns null, the next factory default #onCreateView method is called.

If you have an existing LayoutInflater and want to add your own factory to it, use [cloneInContext](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#cloneInContext(android.content.Context)) to clone the existing instance and then you can use this function (once) on the returned new instance. This will merge your own factory with whatever factory the original instance is using. 

### setFactory2

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFactory2(factory: LayoutInflater.Factory2!): Unit
```

Like [setFactory](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#setFactory(android.view.LayoutInflater.Factory)), but allows you to set a [Factory2](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Factory2) interface. 

### setFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFilter(filter: LayoutInflater.Filter!): Unit
```

Sets the [Filter](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Filter) to by this LayoutInflater. If a view is attempted to be inflated which is not allowed by the [Filter](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Filter), the [inflate(int,android.view.ViewGroup)](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#inflate(kotlin.Int,%20android.view.ViewGroup)) call will throw an [InflateException](https://developer.android.com/reference/kotlin/android/view/InflateException). This filter will replace any previous filter set on this LayoutInflater.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `filter` | [LayoutInflater.Filter](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Filter)!: The Filter which restricts the set of Views that are allowed to be inflated. This filter will replace any previous filter set on this LayoutInflater. |

## Protected methods

### onCreateView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onCreateView(
    parent: View!, 
    name: String!, 
    attrs: AttributeSet!
): View!
```

Version of [onCreateView(java.lang.String,android.util.AttributeSet)](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#onCreateView(kotlin.String,%20android.util.AttributeSet)) that also takes the future parent of the view being constructed. The default implementation simply calls [onCreateView(java.lang.String,android.util.AttributeSet)](https://developer.android.com/reference/kotlin/android/view/LayoutInflater#onCreateView(kotlin.String,%20android.util.AttributeSet)).

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: The future parent of the returned view. *Note that this may be null.* |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The fully qualified class name of the View to be create. |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!: An AttributeSet of attributes to apply to the View. |

| Return ||
|---------------------------------------------------------------------------|------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View)! | View The View created. |

### onCreateView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onCreateView(
    name: String!, 
    attrs: AttributeSet!
): View!
```

This routine is responsible for creating the correct subclass of View given the xml element name. Override it to handle custom view objects. If you override this in your subclass be sure to call through to super.onCreateView(name) for names you do not recognize.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The fully qualified class name of the View to be create. |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!: An AttributeSet of attributes to apply to the View. |

| Return ||
|---------------------------------------------------------------------------|------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View)! | View The View created. |
