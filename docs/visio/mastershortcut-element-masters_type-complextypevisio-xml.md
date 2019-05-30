---
title: Elemento MasterShortcut (complexType Masters_Type) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 62f0e093-5385-e552-f91a-02a65eb0e6e1
description: Especifica un acceso directo de patrón definido en el documento.
ms.openlocfilehash: 94ac64ff0080bf7d50df67674022ce53f32339a4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538210"
---
# <a name="mastershortcut-element-masterstype-complextype-visio-xml"></a>Elemento MasterShortcut (complexType Masters_Type) (XML de Visio)

Especifica un acceso directo de patrón definido en el documento.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[MasterShortcut_Type](mastershortcut_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Master #. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="MasterShortcut" type="MasterShortcut_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Masters](masters-elementvisio-xml.md) <br/> |[Masters_Type](masters_type-complextypevisio-xml.md) <br/> |Contiene los elementos **Master** del documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Icon](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Especifica un icono binario codificado MIME (Extensiones multipropósito de correo Internet) (en formato. ico) para un elemento **Master** o **MasterShortcut** en un documento.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd: unsignedShort  <br/> |opcional  <br/> |Especifica si el texto del elemento en la ventana de la galería de símbolos se alinea a la izquierda, a la derecha o en el centro.  <br/> |Valores del tipo xsd: unsignedShort.  <br/> |
|IconSize  <br/> |xsd: unsignedShort  <br/> |opcional  <br/> |El tamaño del icono del elemento.  <br/> |Valores del tipo xsd: unsignedShort.  <br/> |
|ID  <br/> |xsd: unsignedInt  <br/> |necesario  <br/> |IDENTIFICADOR único del elemento dentro de su elemento primario.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|Nombre  <br/> |xsd: String  <br/> |opcional  <br/> |Nombre del elemento.  <br/> |Valores del tipo xsd: String.  <br/> |
|NameU  <br/> |xsd: String  <br/> |opcional  <br/> |Nombre universal del elemento.  <br/> |Valores del tipo xsd: String.  <br/> |
|PatternFlags  <br/> |xsd: unsignedShort  <br/> |opcional  <br/> |Determina si un patrón se comporta como una trama personalizada.  <br/> |Valores del tipo xsd: unsignedShort.  <br/> |
|Prompt  <br/> |xsd: String  <br/> |opcional  <br/> |La barra de estado y la sugerencia de herramienta para el elemento.  <br/> |Valores del tipo xsd: String.  <br/> |
|ShortcutHelp  <br/> |xsd: String  <br/> |opcional  <br/> |Una cadena de ayuda para el elemento.  <br/> |Valores del tipo xsd: String.  <br/> |
|ShortcutURL  <br/> |xsd: String  <br/> |opcional  <br/> |Una dirección URL a un elemento **MasterShortcut** .  <br/> |Valores del tipo xsd: String.  <br/> |
   

