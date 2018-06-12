---
title: Elemento MasterShortcut (Masters_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 62f0e093-5385-e552-f91a-02a65eb0e6e1
description: Especifica un acceso directo de patrón definido en el documento.
ms.openlocfilehash: be3e7d207e58d8c249598a7e156356d4f9e61849
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822589"
---
# <a name="mastershortcut-element-masterstype-complextype-visio-xml"></a>Elemento MasterShortcut (Masters_Type complexType) ('XML de Visio')

Especifica un acceso directo de patrón definido en el documento.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[MasterShortcut_Type](mastershortcut_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |maestro # .xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="MasterShortcut" type="MasterShortcut_Type" minOccurs="0" maxOccurs="unbounded" >
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
|[Icon](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Especifica que un MIME (Extensiones multipropósito de correo Internet) codificado binario icono (en formato .ico) de un elemento **Master** o **MasterShortcut** en un documento.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |Especifica si el texto del elemento en la ventana de galería de símbolos está alineado a la izquierda, derecha, o centro.  <br/> |Valores del tipo xsd:unsignedShort.  <br/> |
|IconSize  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |El tamaño del icono del elemento.  <br/> |Valores del tipo xsd:unsignedShort.  <br/> |
|id.  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Identificador único del elemento dentro de su elemento primario.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Nombre  <br/> |xsd: String  <br/> |opcional  <br/> |El nombre del elemento.  <br/> |Valores del tipo XSD: String.  <br/> |
|NameU  <br/> |xsd: String  <br/> |opcional  <br/> |El nombre universal del elemento.  <br/> |Valores del tipo XSD: String.  <br/> |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |opcional  <br/> |Determina si un patrón se comporta como una trama personalizada.  <br/> |Valores del tipo xsd:unsignedShort.  <br/> |
|Prompt  <br/> |xsd: String  <br/> |opcional  <br/> |Sugerencia de la barra de estado y la herramienta de símbolo del sistema para el elemento.  <br/> |Valores del tipo XSD: String.  <br/> |
|ShortcutHelp  <br/> |xsd: String  <br/> |opcional  <br/> |Una cadena de ayuda para el elemento.  <br/> |Valores del tipo XSD: String.  <br/> |
|ShortcutURL  <br/> |xsd: String  <br/> |opcional  <br/> |Una dirección URL a un elemento **MasterShortcut** .  <br/> |Valores del tipo XSD: String.  <br/> |
   

