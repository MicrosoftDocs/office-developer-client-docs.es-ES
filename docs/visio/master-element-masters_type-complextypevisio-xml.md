---
title: Elemento maestro (Masters_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c102fd71-c621-2bde-9fbb-8e9203fdf31e
description: Contiene elementos que definen a un patrón para el documento.
ms.openlocfilehash: 51c5f0ad8bee5000e981fcfd4d15e2e49f2bda3b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822583"
---
# <a name="master-element-masterstype-complextype-visio-xml"></a>Elemento maestro (Masters_Type complexType) ('XML de Visio')

Contiene elementos que definen a un patrón para el documento.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Masters.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Master" type="Master_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Patrones](masters-elementvisio-xml.md) <br/> |[Masters_Type](masters_type-complextypevisio-xml.md) <br/> |Contiene los elementos de **patrón** para el documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Se conecta](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Contiene un elemento **Connect** para cada conexión entre dos formas de un dibujo.  <br/> |
|[Icon](icon-element-master_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Especifica que un MIME (Extensiones multipropósito de correo Internet) codificado binario icono (en formato .ico) de un elemento **Master** o **MasterShortcut** en un documento.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Contiene elementos que definen la hoja de página de un elemento de **página** o del **patrón** .  <br/> |
|Formas  <br/> |Shapes_Type  <br/> |Contiene una colección de elementos de la **forma** .  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |Especifica si el texto del patrón en la ventana de galería de símbolos está alineado a la izquierda, derecha, o centro.  <br/> |Valores del tipo xsd:unsignedShort.  <br/> |
|BaseID  <br/> |xsd: String  <br/> |opcional  <br/> |Un GUID (identificador único global) que identifica al patrón de a través de documentos.  <br/> |Valores del tipo XSD: String.  <br/> |
|Oculta.  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Especifica si el patrón está oculta en la interfaz de usuario.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|IconSize  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |El tamaño del icono del elemento.  <br/> |Valores del tipo xsd:unsignedShort.  <br/> |
|IconUpdate  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Especifica si el icono se genera automáticamente a partir del patrón directamente.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|id.  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Identificador único del elemento dentro de su elemento primario.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|MatchByName  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Determina cómo Microsoft Visio decide que si un patrón de documento ya está presente cuando una instancia de un patrón se coloca en la página de dibujo.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|Nombre  <br/> |xsd: String  <br/> |opcional  <br/> |El nombre del elemento.  <br/> |Valores del tipo XSD: String.  <br/> |
|NameU  <br/> |xsd: String  <br/> |opcional  <br/> |El nombre universal del elemento.  <br/> |Valores del tipo XSD: String.  <br/> |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |Determina si un patrón se comporta como una trama personalizada.  <br/> |Valores del tipo xsd:unsignedShort.  <br/> |
|Prompt  <br/> |xsd: String  <br/> |opcional  <br/> |Sugerencia de la barra de estado y la herramienta de símbolo del sistema para el elemento.  <br/> |Valores del tipo XSD: String.  <br/> |
|UniqueID  <br/> |xsd: String  <br/> |opcional  <br/> |Un GUID que identifica al patrón dentro del documento.  <br/> |Valores del tipo XSD: String.  <br/> |
   

