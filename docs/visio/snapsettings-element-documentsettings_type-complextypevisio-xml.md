---
title: Elemento SnapSettings (complexType DocumentSettings_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e86e943-bd29-0a7b-3d6a-d91281f98777
description: Especifica los objetos a los que se ajustan las formas cuando se activa ajustar en la ventana.
ms.openlocfilehash: 68c2bd198a20047ce4f56fe06630177a17319191
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334492"
---
# <a name="snapsettings-element-documentsettingstype-complextype-visio-xml"></a>Elemento SnapSettings (complexType DocumentSettings_Type) ("XML" de Visio)

Especifica los objetos a los que se ajustan las formas cuando se activa ajustar en la ventana.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Contiene los elementos que especifican la configuración del documento.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
## <a name="remarks"></a>Comentarios

El valor puede ser una suma de los valores de la tabla siguiente.
  
|**Value**|**Descripción**|
|:-----|:-----|
|comprendi  <br/> |No se ajusta a ningún objeto.  <br/> |
|1  <br/> |Se ajusta a las subdivisiones de regla.  <br/> |
|segundo  <br/> |Ajustar a la cuadrícula.  <br/> |
|4  <br/> |Se ajusta a las guías.  <br/> |
|8,5  <br/> |Se ajustan a asas de selección.  <br/> |
|16  <br/> |Se ajusta a los vértices.  <br/> |
|32  <br/> |Se ajusta a los puntos de conexión.  <br/> |
|256  <br/> |Se ajusta a los bordes visibles de las formas.  <br/> |
|512  <br/> |Se ajusta al cuadro de alineación.  <br/> |
|1024  <br/> |Se ajusta a las opciones de extensión de las formas.  <br/> |
|32768  <br/> |Ajuste deshabilitado.  <br/> |
|65536  <br/> |Se ajusta a las intersecciones.  <br/> |
   

