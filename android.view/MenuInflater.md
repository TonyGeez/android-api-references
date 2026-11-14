# MenuInflater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MenuInflater

Kotlin| [Java](MenuInflater.md) 
| --- | --- |

```
open class MenuInflater
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.MenuInflater](MenuInflater.md) |

This class is used to instantiate menu XML files into Menu objects.

For performance reasons, menu inflation relies heavily on pre-processing of XML files that is done at build time. Therefore, it is not currently possible to use MenuInflater with an XmlPullParser over a plain XML file at runtime; it only works with an XmlPullParser returned from a compiled resource (R.*something*file.)

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MenuInflater](MenuInflater.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Constructs a menu inflater. |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](MenuInflater.md))`(`menuRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `menu:` ` [Menu](Menu.md)!`)` Inflate a menu hierarchy from the specified XML resource. |

## Public constructors

### MenuInflater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MenuInflater(context: Context!)
```

Constructs a menu inflater. 
**See Also**

- [android.app.Activity#getMenuInflater()](../android.app/Activity.md))

## Public methods

### inflate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun inflate(
    menuRes: Int, 
    menu: Menu!
): Unit
```

Inflate a menu hierarchy from the specified XML resource. Throws [InflateException](InflateException.md) if there is an error.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `menuRes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Resource ID for an XML layout resource to load (e.g.,`R.menu.main_activity`) |
| `menu` | [Menu](Menu.md)!:The Menu to inflate into. The items and submenus will be added to this Menu. |
