Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NamespaceSupport

```
open class NamespaceSupport
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [org.xml.sax.helpers.NamespaceSupport](NamespaceSupport.md) |

Encapsulate Namespace logic for use by applications using SAX, or internally by SAX drivers. *This module, both source code and documentation, is in the Public Domain, and comes with **NO WARRANTY**.* See <http://www.saxproject.org> for further information.

This class encapsulates the logic of Namespace processing: it tracks the declarations currently in force for each context and automatically processes qualified XML names into their Namespace parts; it can also be used in reverse for generating XML qnames from Namespaces.

Namespace support objects are reusable, but the reset method must be invoked between each session.

Here is a simple session:

```kotlin
String parts[] = new String[3];
  NamespaceSupport support = new NamespaceSupport();
 
  support.pushContext();
  support.declarePrefix("", "http://www.w3.org/1999/xhtml");
  support.declarePrefix("dc", "http://www.purl.org/dc#");
 
  parts = support.processName("p", parts, false);
  System.out.println("Namespace URI: " + parts[0]);
  System.out.println("Local name: " + parts[1]);
  System.out.println("Raw name: " + parts[2]);
 
  parts = support.processName("dc:title", parts, false);
  System.out.println("Namespace URI: " + parts[0]);
  System.out.println("Local name: " + parts[1]);
  System.out.println("Raw name: " + parts[2]);
 
  support.popContext();
  
```

Note that this class is optimized for the use case where most elements do not contain Namespace declarations: if the same prefix/URI mapping is repeated for each context (for example), this class will be somewhat less efficient.

Although SAX drivers (parsers) may choose to use this class to implement namespace handling, they are not required to do so. Applications must track namespace information themselves if they want to use namespace information.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/org/xml/sax/helpers/NamespaceSupport#NSDECL:kotlin.String` The namespace declaration URI as a constant. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/org/xml/sax/helpers/NamespaceSupport#XMLNS:kotlin.String` The XML Namespace URI as a constant. |

| Public constructors ||
|---|---|
| NamespaceSupport Create a new Namespace support object. |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | declarePrefix Declare a Namespace prefix. |
| open [Enumeration](../java.util/Enumeration.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | getDeclaredPrefixes Return an enumeration of all prefixes declared in this context. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getPrefix Return one of the prefixes mapped to a Namespace URI. |
| --- | --- |
| open [Enumeration](../java.util/Enumeration.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | getPrefixes Return an enumeration of all prefixes whose declarations are active in the current context. |
| open [Enumeration](../java.util/Enumeration.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | getPrefixes Return an enumeration of all prefixes for a given URI whose declarations are active in the current context. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getURI Look up a prefix and get the currently-mapped Namespace URI. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isNamespaceDeclUris Returns true if namespace declaration attributes are placed into a namespace. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | popContext Revert to the previous Namespace context. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | processName Process a raw XML qualified name, after all declarations in the current context have been handled by declarePrefix. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | pushContext Start a new Namespace context. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | reset Reset this Namespace support object for reuse. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setNamespaceDeclUris Controls whether namespace declaration attributes are placed into the `https://developer.android.com/reference/kotlin/org/xml/sax/helpers/NamespaceSupport#NSDECL:kotlin.String` namespace by processName. |
| --- | --- |

## Constants

### NSDECL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NSDECL: String
```

The namespace declaration URI as a constant. The value is `http://www.w3.org/xmlns/2000/`, as defined in a backwards-incompatible erratum to the "Namespaces in XML" recommendation. Because that erratum postdated SAX2, SAX2 defaults to the original recommendation, and does not normally use this URI.

This is the Namespace URI that is optionally applied to *xmlns* and *xmlns:\** attributes, which are used to declare namespaces.

 Value: "http://www.w3.org/xmlns/2000/"

**See Also**

- setNamespaceDeclUris
- isNamespaceDeclUris

### XMLNS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val XMLNS: String
```

The XML Namespace URI as a constant. The value is `http://www.w3.org/XML/1998/namespace` as defined in the "Namespaces in XML" \* recommendation.

This is the Namespace URI that is automatically mapped to the "xml" prefix.

 Value: "http://www.w3.org/XML/1998/namespace"

## Public constructors

### NamespaceSupport

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
NamespaceSupport()
```

Create a new Namespace support object.

## Public methods

### declarePrefix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun declarePrefix(
    prefix: String!, 
    uri: String!
): Boolean
```

Declare a Namespace prefix. All prefixes must be declared before they are referenced. For example, a SAX driver (parser) would scan an element's attributes in two passes: first for namespace declarations, then a second pass using processName to interpret prefixes against (potentially redefined) prefixes.

This method declares a prefix in the current Namespace context; the prefix will remain in force until this context is popped, unless it is shadowed in a descendant context.

To declare the default element Namespace, use the empty string as the prefix.

Note that you must *not* declare a prefix after you've pushed and popped another Namespace context, or treated the declarations phase as complete by processing a prefixed name.

Note that there is an asymmetry in this library: getPrefix will not return the "" prefix, even if you have declared a default element namespace. To check for a default namespace, you have to look it up explicitly using getURI. This asymmetry exists to make it easier to look up prefixes for attribute names, where the default prefix is not allowed.

| Parameters ||
|---|---|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The prefix to declare, or the empty string to indicate the default element namespace. This may never have the value "xml" or "xmlns". |
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The Namespace URI to associate with the prefix. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the prefix was legal, false otherwise |

**See Also**

- processName
- getURI
- getPrefix

### getDeclaredPrefixes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDeclaredPrefixes(): Enumeration<Any!>!
```

Return an enumeration of all prefixes declared in this context.

The empty (default) prefix will be included in this enumeration; note that this behaviour differs from that of getPrefix and #getPrefixes.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Enumeration.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>!` | An enumeration of all prefixes declared in this context. |

**See Also**

- getURI

### getPrefix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPrefix(uri: String!): String!
```

Return one of the prefixes mapped to a Namespace URI.

If more than one prefix is currently mapped to the same URI, this method will make an arbitrary selection; if you want all of the prefixes, use the #getPrefixes method instead.

**Note:** this will never return the empty (default) prefix; to check for a default prefix, use the getURI method with an argument of "".

| Parameters ||
|---|---|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the namespace URI |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | one of the prefixes currently mapped to the URI supplied, or null if none is mapped or if the URI is assigned to the default namespace |

**See Also**

- getPrefixes
- getURI

### getPrefixes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPrefixes(): Enumeration<Any!>!
```

Return an enumeration of all prefixes whose declarations are active in the current context. This includes declarations from parent contexts that have not been overridden.

**Note:** if there is a default prefix, it will not be returned in this enumeration; check for the default prefix using the getURI with an argument of "".

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Enumeration.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>!` | An enumeration of prefixes (never empty). |

**See Also**

- getDeclaredPrefixes
- getURI

### getPrefixes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPrefixes(uri: String!): Enumeration<Any!>!
```

Return an enumeration of all prefixes for a given URI whose declarations are active in the current context. This includes declarations from parent contexts that have not been overridden.

This method returns prefixes mapped to a specific Namespace URI. The xml: prefix will be included. If you want only one prefix that's mapped to the Namespace URI, and you don't care which one you get, use the getPrefix method instead.

**Note:** the empty (default) prefix is *never* included in this enumeration; to check for the presence of a default Namespace, use the getURI method with an argument of "".

| Parameters ||
|---|---|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The Namespace URI. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Enumeration.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>!` | An enumeration of prefixes (never empty). |

**See Also**

- getPrefix
- getDeclaredPrefixes
- getURI

### getURI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getURI(prefix: String!): String!
```

Look up a prefix and get the currently-mapped Namespace URI.

This method looks up the prefix in the current context. Use the empty string ("") for the default Namespace.

| Parameters ||
|---|---|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The prefix to look up. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The associated Namespace URI, or null if the prefix is undeclared in this context. |

**See Also**

- getPrefix

### isNamespaceDeclUris

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isNamespaceDeclUris(): Boolean
```

Returns true if namespace declaration attributes are placed into a namespace. This behavior is not the default.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if namespace declaration attributes are enabled, false otherwise. |

### popContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun popContext(): Unit
```

Revert to the previous Namespace context.

Normally, you should pop the context at the end of each XML element. After popping the context, all Namespace prefix mappings that were previously in force are restored.

You must not attempt to declare additional Namespace prefixes after popping a context, unless you push another context first.
**See Also**

- pushContext

### processName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun processName(
    qName: String!, 
    parts: Array<String!>!, 
    isAttribute: Boolean
): Array<String!>!
```

Process a raw XML qualified name, after all declarations in the current context have been handled by declarePrefix.

This method processes a raw XML qualified name in the current context by removing the prefix and looking it up among the prefixes currently declared. The return value will be the array supplied by the caller, filled in as follows:

parts\[0\]
:
 The Namespace URI, or an empty string if none is in use.

parts\[1\]
:
 The local name (without prefix).

parts\[2\]
:
 The original raw name.

All of the strings in the array will be internalized. If the raw name has a prefix that has not been declared, then the return value will be null.

Note that attribute names are processed differently than element names: an unprefixed element name will receive the default Namespace (if any), while an unprefixed attribute name will not.

| Parameters ||
|---|---|
| `qName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The XML qualified name to be processed. |
| `parts` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: An array supplied by the caller, capable of holding at least three members. |
| `isAttribute` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): A flag indicating whether this is an attribute name (true) or an element name (false). |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | The supplied array holding three internalized strings representing the Namespace URI (or empty string), the local name, and the XML qualified name; or null if there is an undeclared prefix. |

**See Also**

- declarePrefix
- intern

### pushContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun pushContext(): Unit
```

Start a new Namespace context. The new context will automatically inherit the declarations of its parent context, but it will also keep track of which declarations were made within this context.

Event callback code should start a new context once per element. This means being ready to call this in either of two places. For elements that don't include namespace declarations, the *ContentHandler.startElement()* callback is the right place. For elements with such a declaration, it'd done in the first *ContentHandler.startPrefixMapping()* callback. A boolean flag can be used to track whether a context has been started yet. When either of those methods is called, it checks the flag to see if a new context needs to be started. If so, it starts the context and sets the flag. After *ContentHandler.startElement()* does that, it always clears the flag.

Normally, SAX drivers would push a new context at the beginning of each XML element. Then they perform a first pass over the attributes to process all namespace declarations, making *ContentHandler.startPrefixMapping()* callbacks. Then a second pass is made, to determine the namespace-qualified names for all attributes and for the element name. Finally all the information for the *ContentHandler.startElement()* callback is available, so it can then be made.

The Namespace support object always starts with a base context already in force: in this context, only the "xml" prefix is declared.
**See Also**

- `https://developer.android.com/reference/kotlin/org/xml/sax/ContentHandler.html#`
- popContext

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reset(): Unit
```

Reset this Namespace support object for reuse.

It is necessary to invoke this method before reusing the Namespace support object for a new session. If namespace declaration URIs are to be supported, that flag must also be set to a non-default value.
**See Also**

- setNamespaceDeclUris

### setNamespaceDeclUris

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNamespaceDeclUris(value: Boolean): Unit
```

Controls whether namespace declaration attributes are placed into the `https://developer.android.com/reference/kotlin/org/xml/sax/helpers/NamespaceSupport#NSDECL:kotlin.String` namespace by processName. This may only be changed before any contexts have been pushed.

| Parameters ||
|---|---|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): the namespace declaration attribute state. A value of true enables this feature, a value of false disables it. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | when attempting to set this after any context has been pushed. |
