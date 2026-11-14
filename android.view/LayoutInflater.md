# LayoutInflater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LayoutInflater

Kotlin | [Java](LayoutInflater.md) 
| --- | --- |

```
abstract class LayoutInflater
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.LayoutInflater](LayoutInflater.md) |

Instantiates a layout XML file into its corresponding [android.view.View](View.md) objects. It is never used directly. Instead, use [android.app.Activity#getLayoutInflater()](../android.app/Activity.md)) or android.content.Context#getSystemService to retrieve a standard LayoutInflater instance that is already hooked up to the current context and correctly configured for the device you are running on.

To create a new LayoutInflater with an additional [Factory](../android/view/LayoutInflater.Factory.md) for your own views, you can use [cloneInContext](LayoutInflater.md)) to clone an existing ViewFactory, and then call [setFactory](LayoutInflater.md)) on it to include your Factory.

For performance reasons, view inflation relies heavily on pre-processing of XML files that is done at build time. Therefore, it is not currently possible to use LayoutInflater with an XmlPullParser over a plain XML file at runtime; it only works with an XmlPullParser returned from a compiled resource (R.*something* file.)

**Note:** This class is **not** thread-safe and a given instance should only be accessed by a single thread.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Factory](../android/view/LayoutInflater.Factory.md) <br /> |
| abstract | [Factory2](../android/view/LayoutInflater.Factory2.md) <br /> |
| abstract | [Filter](../android/view/LayoutInflater.Filter.md) Hook to allow clients of the LayoutInflater to restrict the set of Views that are allowed to be inflated. |
| --- | --- |

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LayoutInflater](LayoutInflater.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Create a new LayoutInflater instance associated with a particular Context. |
| [LayoutInflater](LayoutInflater.md))`(`original:` ` [LayoutInflater](LayoutInflater.md)!`, `newContext:` ` [Context](../android.content/Context.md)!`)` Create a new LayoutInflater instance that is a copy of an existing LayoutInflater, optionally with its Context changed. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [LayoutInflater](LayoutInflater.md)! | [cloneInContext](LayoutInflater.md))`(`newContext:` ` [Context](../android.content/Context.md)!`)` Create a copy of the existing LayoutInflater object, with the copy pointing to a different Context than the original. |
| [View](View.md)? | [createView](LayoutInflater.md))`(`viewContext:` ` [Context](../android.content/Context.md)`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)?`)` Low-level function for instantiating a view by name. |
| [View](View.md)! | [createView](LayoutInflater.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)!`)` Low-level function for instantiating a view by name. |
| --- | --- |
| open static [LayoutInflater](LayoutInflater.md)! | [from](LayoutInflater.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Obtains the LayoutInflater from the given context. |
| open [Context](../android.content/Context.md)! | [getContext](LayoutInflater.md))`()` Return the context we are running in, for access to resources, class loader, etc. |
| [LayoutInflater.Factory](../android/view/LayoutInflater.Factory.md)! | [getFactory](LayoutInflater.md))`()` Return the current [Factory](../android/view/LayoutInflater.Factory.md) (or null). |
| --- | --- |
| [LayoutInflater.Factory2](../android/view/LayoutInflater.Factory2.md)! | [getFactory2](LayoutInflater.md))`()` Return the current [Factory2](../android/view/LayoutInflater.Factory2.md). |
| open [LayoutInflater.Filter](../android/view/LayoutInflater.Filter.md)! | [getFilter](LayoutInflater.md))`()` <br /> |
| open [View](View.md)! | [inflate](LayoutInflater.md))`(`resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `root:` ` [ViewGroup](ViewGroup.md)?`)` Inflate a new view hierarchy from the specified xml resource. |
| --- | --- |
| open [View](View.md)! | [inflate](LayoutInflater.md))`(`resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `root:` ` [ViewGroup](ViewGroup.md)?`, `attachToRoot:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Inflate a new view hierarchy from the specified xml resource. |
| open [View](View.md)! | [inflate](LayoutInflater.md))`(`parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)!`, `root:` ` [ViewGroup](ViewGroup.md)?`)` Inflate a new view hierarchy from the specified xml node. |
| open [View](View.md)! | [inflate](LayoutInflater.md))`(`parser:` ` [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)!`, `root:` ` [ViewGroup](ViewGroup.md)?`, `attachToRoot:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Inflate a new view hierarchy from the specified XML node. |
| --- | --- |
| open [View](View.md)? | [onCreateView](LayoutInflater.md))`(`viewContext:` ` [Context](../android.content/Context.md)`, `parent:` ` [View](View.md)?`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)?`)` Version of [onCreateView(android.view.View,java.lang.String,android.util.AttributeSet)](LayoutInflater.md)) that also takes the inflation context. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFactory](LayoutInflater.md))`(`factory:` ` [LayoutInflater.Factory](../android/view/LayoutInflater.Factory.md)!`)` Attach a custom Factory interface for creating views while using this LayoutInflater. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFactory2](LayoutInflater.md))`(`factory:` ` [LayoutInflater.Factory2](../android/view/LayoutInflater.Factory2.md)!`)` Like [setFactory](LayoutInflater.md)), but allows you to set a [Factory2](../android/view/LayoutInflater.Factory2.md) interface. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilter](LayoutInflater.md))`(`filter:` ` [LayoutInflater.Filter](../android/view/LayoutInflater.Filter.md)!`)` Sets the [Filter](../android/view/LayoutInflater.Filter.md) to by this LayoutInflater. |

| Protected methods ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [View](View.md)! | [onCreateView](LayoutInflater.md))`(`parent:` ` [View](View.md)!`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)!`)` Version of [onCreateView(java.lang.String,android.util.AttributeSet)](LayoutInflater.md)) that also takes the future parent of the view being constructed. |
| open [View](View.md)! | [onCreateView](LayoutInflater.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)!`)` This routine is responsible for creating the correct subclass of View given the xml element name. |

## Protected constructors

### LayoutInflater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected LayoutInflater(context: Context!)
```

Create a new LayoutInflater instance associated with a particular Context. Applications will almost always want to use android.content.Context#getSystemService to retrieve the standard [Context.INFLATER_SERVICE](../android.content/Context.md).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!: The Context in which this LayoutInflater will create its Views; most importantly, this supplies the theme from which the default values for their attributes are retrieved. |

### LayoutInflater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected LayoutInflater(
    original: LayoutInflater!, 
    newContext: Context!)
```

Create a new LayoutInflater instance that is a copy of an existing LayoutInflater, optionally with its Context changed. For use in implementing [cloneInContext](LayoutInflater.md)).

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `original` | [LayoutInflater](LayoutInflater.md)!: The original LayoutInflater to copy. |
| `newContext` | [Context](../android.content/Context.md)!: The new Context to use. |

## Public methods

### cloneInContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun cloneInContext(newContext: Context!): LayoutInflater!
```

Create a copy of the existing LayoutInflater object, with the copy pointing to a different Context than the original. This is used by [ContextThemeWrapper](ContextThemeWrapper.md) to create a new LayoutInflater to go along with the new Context theme.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newContext` | [Context](../android.content/Context.md)!: The new Context to associate with the new LayoutInflater. May be the same as the original Context if desired. |

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [LayoutInflater](LayoutInflater.md)! | Returns a brand spanking new LayoutInflater object associated with the given Context. |

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
| `viewContext` | [Context](../android.content/Context.md): The context used as the context parameter of the View constructor This value cannot be `null`. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The full name of the class to be instantiated. This value cannot be `null`. |
| `attrs` | [AttributeSet](../android.util/AttributeSet.md)?: The XML attributes supplied for this instance. This value may be `null`. |
| --- | --- |
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

| Return ||
|---------------------------------------------------------------------------|--------------------------------------------|
| [View](View.md)? | View The newly instantiated view, or null. |

### createView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createView(
    name: String!, 
    prefix: String!, 
    attrs: AttributeSet!
): View!
```

Low-level function for instantiating a view by name. This attempts to instantiate a view class of the given name found in this LayoutInflater's ClassLoader. To use an explicit Context in the View constructor, use [createView(android.content.Context,java.lang.String,java.lang.String,android.util.AttributeSet)](LayoutInflater.md)) instead.

There are two things that can happen in an error case: either the exception describing the error will be thrown, or a null will be returned. You must deal with both possibilities -- the former will happen the first time createView() is called for a class of a particular name, the latter every time there-after for that class name.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The full name of the class to be instantiated. |
| `attrs` | [AttributeSet](../android.util/AttributeSet.md)!: The XML attributes supplied for this instance. |

| Return ||
|---------------------------------------------------------------------------|--------------------------------------------|
| [View](View.md)! | View The newly instantiated view, or null. |

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

Return the current [Factory](../android/view/LayoutInflater.Factory.md) (or null). This is called on each element name. If the factory returns a View, add that to the hierarchy. If it returns null, proceed to call onCreateView(name). 

### getFactory2

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFactory2(): LayoutInflater.Factory2!
```

Return the current [Factory2](../android/view/LayoutInflater.Factory2.md). Returns null if no factory is set or the set factory does not implement the [Factory2](../android/view/LayoutInflater.Factory2.md) interface. This is called on each element name. If the factory returns a View, add that to the hierarchy. If it returns null, proceed to call onCreateView(name). 

### getFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFilter(): LayoutInflater.Filter!
```

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LayoutInflater.Filter](../android/view/LayoutInflater.Filter.md)! | The [Filter](../android/view/LayoutInflater.Filter.md) currently used by this LayoutInflater to restrict the set of Views that are allowed to be inflated. |

### inflate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun inflate(
    resource: Int, 
    root: ViewGroup?
): View!
```

Inflate a new view hierarchy from the specified xml resource. Throws [InflateException](InflateException.md) if there is an error.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): ID for an XML layout resource to load (e.g., `R.layout.main_page`) |
| `root` | [ViewGroup](ViewGroup.md)?: Optional view to be the parent of the generated hierarchy. This value may be `null`. |

| Return ||
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [View](View.md)! | The root View of the inflated hierarchy. If root was supplied, this is the root View; otherwise it is the root of the inflated XML file. |

### inflate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun inflate(
    resource: Int, 
    root: ViewGroup?, 
    attachToRoot: Boolean
): View!
```

Inflate a new view hierarchy from the specified xml resource. Throws [InflateException](InflateException.md) if there is an error.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): ID for an XML layout resource to load (e.g., `R.layout.main_page`) |
| `root` | [ViewGroup](ViewGroup.md)?: Optional view to be the parent of the generated hierarchy (if *attachToRoot* is true), or else simply an object that provides a set of LayoutParams values for root of the returned hierarchy (if *attachToRoot* is false.) This value may be `null`. |
| `attachToRoot` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether the inflated hierarchy should be attached to the root parameter? If false, root is only used to create the correct subclass of LayoutParams for the root view in the XML. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [View](View.md)! | The root View of the inflated hierarchy. If root was supplied and attachToRoot is true, this is root; otherwise it is the root of the inflated XML file. |

### inflate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun inflate(
    parser: XmlPullParser!, 
    root: ViewGroup?
): View!
```

Inflate a new view hierarchy from the specified xml node. Throws [InflateException](InflateException.md) if there is an error. \*

***Important*** For performance reasons, view inflation relies heavily on pre-processing of XML files that is done at build time. Therefore, it is not currently possible to use LayoutInflater with an XmlPullParser over a plain XML file at runtime.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parser` | [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)!: XML dom node containing the description of the view hierarchy. |
| `root` | [ViewGroup](ViewGroup.md)?: Optional view to be the parent of the generated hierarchy. This value may be `null`. |

| Return ||
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [View](View.md)! | The root View of the inflated hierarchy. If root was supplied, this is the root View; otherwise it is the root of the inflated XML file. |

### inflate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun inflate(
    parser: XmlPullParser!, 
    root: ViewGroup?, 
    attachToRoot: Boolean
): View!
```

Inflate a new view hierarchy from the specified XML node. Throws [InflateException](InflateException.md) if there is an error.

***Important*** For performance reasons, view inflation relies heavily on pre-processing of XML files that is done at build time. Therefore, it is not currently possible to use LayoutInflater with an XmlPullParser over a plain XML file at runtime.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parser` | [XmlPullParser](../org.xmlpull.v1/XmlPullParser.md)!: XML dom node containing the description of the view hierarchy. |
| `root` | [ViewGroup](ViewGroup.md)?: Optional view to be the parent of the generated hierarchy (if *attachToRoot* is true), or else simply an object that provides a set of LayoutParams values for root of the returned hierarchy (if *attachToRoot* is false.) This value may be `null`. |
| `attachToRoot` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether the inflated hierarchy should be attached to the root parameter? If false, root is only used to create the correct subclass of LayoutParams for the root view in the XML. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [View](View.md)! | The root View of the inflated hierarchy. If root was supplied and attachToRoot is true, this is root; otherwise it is the root of the inflated XML file. |

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

Version of [onCreateView(android.view.View,java.lang.String,android.util.AttributeSet)](LayoutInflater.md)) that also takes the inflation context. The default implementation simply calls [onCreateView(android.view.View,java.lang.String,android.util.AttributeSet)](LayoutInflater.md)).

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `viewContext` | [Context](../android.content/Context.md): The Context to be used as a constructor parameter for the View This value cannot be `null`. |
| `parent` | [View](View.md)?: The future parent of the returned view. *Note that this may be null.* |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The fully qualified class name of the View to be create. This value cannot be `null`. |
| --- | --- |
| `attrs` | [AttributeSet](../android.util/AttributeSet.md)?: An AttributeSet of attributes to apply to the View. This value may be `null`. |

| Return ||
|---------------------------------------------------------------------------|--------------------------------------------------|
| [View](View.md)? | View The View created. This value may be `null`. |

### setFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFactory(factory: LayoutInflater.Factory!): Unit
```

Attach a custom Factory interface for creating views while using this LayoutInflater. This must not be null, and can only be set once; after setting, you can not change the factory. This is called on each element name as the xml is parsed. If the factory returns a View, that is added to the hierarchy. If it returns null, the next factory default #onCreateView method is called.

If you have an existing LayoutInflater and want to add your own factory to it, use [cloneInContext](LayoutInflater.md)) to clone the existing instance and then you can use this function (once) on the returned new instance. This will merge your own factory with whatever factory the original instance is using. 

### setFactory2

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFactory2(factory: LayoutInflater.Factory2!): Unit
```

Like [setFactory](LayoutInflater.md)), but allows you to set a [Factory2](../android/view/LayoutInflater.Factory2.md) interface. 

### setFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFilter(filter: LayoutInflater.Filter!): Unit
```

Sets the [Filter](../android/view/LayoutInflater.Filter.md) to by this LayoutInflater. If a view is attempted to be inflated which is not allowed by the [Filter](../android/view/LayoutInflater.Filter.md), the [inflate(int,android.view.ViewGroup)](LayoutInflater.md)) call will throw an [InflateException](InflateException.md). This filter will replace any previous filter set on this LayoutInflater.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `filter` | [LayoutInflater.Filter](../android/view/LayoutInflater.Filter.md)!: The Filter which restricts the set of Views that are allowed to be inflated. This filter will replace any previous filter set on this LayoutInflater. |

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

Version of [onCreateView(java.lang.String,android.util.AttributeSet)](LayoutInflater.md)) that also takes the future parent of the view being constructed. The default implementation simply calls [onCreateView(java.lang.String,android.util.AttributeSet)](LayoutInflater.md)).

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [View](View.md)!: The future parent of the returned view. *Note that this may be null.* |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The fully qualified class name of the View to be create. |
| `attrs` | [AttributeSet](../android.util/AttributeSet.md)!: An AttributeSet of attributes to apply to the View. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------|------------------------|
| [View](View.md)! | View The View created. |

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
| `attrs` | [AttributeSet](../android.util/AttributeSet.md)!: An AttributeSet of attributes to apply to the View. |

| Return ||
|---------------------------------------------------------------------------|------------------------|
| [View](View.md)! | View The View created. |
