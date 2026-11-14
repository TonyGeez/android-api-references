# JavascriptInterface

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JavascriptInterface

Kotlin| [Java](JavascriptInterface.md) 
| --- | --- |

```
@Target([AnnotationTarget.FUNCTION, AnnotationTarget.PROPERTY_GETTER, AnnotationTarget.PROPERTY_SETTER]) class JavascriptInterface
```

| [android.webkit.JavascriptInterface](JavascriptInterface.md) |

Annotation that allows exposing methods to JavaScript. Starting from API level [android.os.Build.VERSION_CODES#JELLY_BEAN_MR1](../android/os/Build.VERSION_CODES.md) and above, only methods explicitly marked with this annotation are available to the Javascript code. See [android.webkit.WebView#addJavascriptInterface](WebView.md))for more information about it.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [JavascriptInterface](JavascriptInterface.md))`()` Annotation that allows exposing methods to JavaScript. |

## Public constructors

### JavascriptInterface

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JavascriptInterface()
```

Annotation that allows exposing methods to JavaScript. Starting from API level [android.os.Build.VERSION_CODES#JELLY_BEAN_MR1](../android/os/Build.VERSION_CODES.md) and above, only methods explicitly marked with this annotation are available to the Javascript code. See [android.webkit.WebView#addJavascriptInterface](WebView.md))for more information about it.
