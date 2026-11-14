# javax.xml.transform

# javax.xml.transform

## Interfaces

| [ErrorListener](https://developer.android.com/reference/kotlin/javax/xml/transform/ErrorListener) | To provide customized error handling, implement this interface and use the`setErrorListener`method to register an instance of the implementation with the [javax.xml.transform.Transformer](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer). |
| [Result](https://developer.android.com/reference/kotlin/javax/xml/transform/Result) | An object that implements this interface contains the information needed to build a transformation result tree. |
| [Source](https://developer.android.com/reference/kotlin/javax/xml/transform/Source) | An object that implements this interface contains the information needed to act as source input (XML source or transformation instructions). |
| [SourceLocator](https://developer.android.com/reference/kotlin/javax/xml/transform/SourceLocator) | This interface is primarily for the purposes of reporting where an error occurred in the XML source or transformation instructions. |
| [Templates](https://developer.android.com/reference/kotlin/javax/xml/transform/Templates) | An object that implements this interface is the runtime representation of processed transformation instructions. |
| [URIResolver](https://developer.android.com/reference/kotlin/javax/xml/transform/URIResolver) | An object that implements this interface that can be called by the processor to turn a URI used in document(), xsl:import, or xsl:include into a Source object. |

## Classes

| [OutputKeys](https://developer.android.com/reference/kotlin/javax/xml/transform/OutputKeys) | Provides string constants that can be used to set output properties for a Transformer, or to retrieve output properties from a Transformer or Templates object. |
| [Transformer](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer) | An instance of this abstract class can transform a source tree into a result tree. |
| [TransformerFactory](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactory) | A TransformerFactory instance can be used to create [javax.xml.transform.Transformer](https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer) and [javax.xml.transform.Templates](https://developer.android.com/reference/kotlin/javax/xml/transform/Templates) objects. |

## Exceptions

| [TransformerConfigurationException](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerConfigurationException) | Indicates a serious configuration error. |
| [TransformerException](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException) | This class specifies an exceptional condition that occurred during the transformation process. |
| [TransformerFactoryConfigurationError](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerFactoryConfigurationError) | Thrown when a problem with configuration with the Transformer Factories exists. |
