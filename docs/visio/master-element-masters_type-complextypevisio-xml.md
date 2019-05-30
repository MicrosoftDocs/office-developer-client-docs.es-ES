---
title: Elemento Master (Masters_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c102fd71-c621-2bde-9fbb-8e9203fdf31e
description: Contiene elementos que definen un patrón para el documento.
ms.openlocfilehash: 83727b89eaf44aae5dddecacff1f05f369ee0bf0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538049"
---
# <a name="master-element-masterstype-complextype-visio-xml"></a>Elemento Master (Masters_Type complexType) (XML de Visio)

Contiene elementos que definen un patrón para el documento.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Masters. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Master" type="Master_Type" minOccurs="0" maxOccurs="unbounded" >
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
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Contiene un elemento **Connect** para cada conexión entre dos formas de un dibujo.  <br/> |
|[Icon](icon-element-master_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Especifica un icono binario codificado MIME (Extensiones multipropósito de correo Internet) (en formato. ico) para un elemento **Master** o **MasterShortcut** en un documento.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Contiene los elementos que definen la hoja de página de un elemento **Page** o **Master** .  <br/> |
|Formas  <br/> |Shapes_Type  <br/> |Contiene una colección de elementos **Shape** .  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd: unsignedShort  <br/> |opcional  <br/> |Especifica si el texto del patrón de la ventana de la galería de símbolos se alinea a la izquierda, a la derecha o en el centro.  <br/> |Valores del tipo xsd: unsignedShort.  <br/> |
|BaseID  <br/> |xsd: String  <br/> |opcional  <br/> |GUID (identificador único global) que identifica el patrón entre documentos.  <br/> |Valores del tipo xsd: String.  <br/> |
|Hidden  <br/> |xsd: Boolean  <br/> |opcional  <br/> |Especifica si el patrón está oculto en la interfaz de usuario.  <br/> |Valores del tipo xsd: Boolean.  <br/> |
|IconSize  <br/> |xsd: unsignedShort  <br/> |opcional  <br/> |El tamaño del icono del elemento.  <br/> |Valores del tipo xsd: unsignedShort.  <br/> |
|IconUpdate  <br/> |xsd: Boolean  <br/> |opcional  <br/> |Especifica si el icono se genera automáticamente a partir del propio patrón.  <br/> |Valores del tipo xsd: Boolean.  <br/> |
|ID  <br/> |xsd: unsignedInt  <br/> |necesario  <br/> |IDENTIFICADOR único del elemento dentro de su elemento primario.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|MatchByName  <br/> |xsd: Boolean  <br/> |opcional  <br/> |Determina la forma en que Microsoft Visio decide si un patrón de documento ya está presente cuando se coloca una instancia de un patrón en la página de dibujo.  <br/> |Valores del tipo xsd: Boolean.  <br/> |
|Nombre  <br/> |xsd: String  <br/> |opcional  <br/> |Nombre del elemento.  <br/> |Valores del tipo xsd: String.  <br/> |
|NameU  <br/> |xsd: String  <br/> |opcional  <br/> |Nombre universal del elemento.  <br/> |Valores del tipo xsd: String.  <br/> |
|PatternFlags  <br/> |xsd: unsignedShort  <br/> |opcional  <br/> |Determina si un patrón se comporta como una trama personalizada.  <br/> |Valores del tipo xsd: unsignedShort.  <br/> |
|Prompt  <br/> |xsd: String  <br/> |opcional  <br/> |La barra de estado y la sugerencia de herramienta para el elemento.  <br/> |Valores del tipo xsd: String.  <br/> |
|UniqueID  <br/> |xsd: String  <br/> |opcional  <br/> |GUID que identifica el patrón en el documento.  <br/> |Valores del tipo xsd: String.  <br/> |
   

