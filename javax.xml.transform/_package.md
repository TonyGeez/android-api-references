# javax.xml.transform

# javax.xml.transform

## Interfaces

| [ErrorListener](ErrorListener.md) | To provide customized error handling, implement this interface and use the`setErrorListener`method to register an instance of the implementation with the [javax.xml.transform.Transformer](Transformer.md). |
| --- | --- |
| [Result](Result.md) | An object that implements this interface contains the information needed to build a transformation result tree. |
| [Source](Source.md) | An object that implements this interface contains the information needed to act as source input (XML source or transformation instructions). |
| [SourceLocator](SourceLocator.md) | This interface is primarily for the purposes of reporting where an error occurred in the XML source or transformation instructions. |
| --- | --- |
| [Templates](Templates.md) | An object that implements this interface is the runtime representation of processed transformation instructions. |
| [URIResolver](URIResolver.md) | An object that implements this interface that can be called by the processor to turn a URI used in document(), xsl:import, or xsl:include into a Source object. |

## Classes

| [OutputKeys](OutputKeys.md) | Provides string constants that can be used to set output properties for a Transformer, or to retrieve output properties from a Transformer or Templates object. |
| --- | --- |
| [Transformer](Transformer.md) | An instance of this abstract class can transform a source tree into a result tree. |
| [TransformerFactory](TransformerFactory.md) | A TransformerFactory instance can be used to create [javax.xml.transform.Transformer](Transformer.md) and [javax.xml.transform.Templates](Templates.md) objects. |

## Exceptions

| [TransformerConfigurationException](TransformerConfigurationException.md) | Indicates a serious configuration error. |
| --- | --- |
| [TransformerException](TransformerException.md) | This class specifies an exceptional condition that occurred during the transformation process. |
| [TransformerFactoryConfigurationError](TransformerFactoryConfigurationError.md) | Thrown when a problem with configuration with the Transformer Factories exists. |
