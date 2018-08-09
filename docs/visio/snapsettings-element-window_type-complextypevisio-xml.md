---
title: Elemento SnapSettings (Window_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b87a244-b331-7e93-d304-239f8ca77061
description: Especifica los objetos que las formas ajustan ajustar cuando está en la ventana activa.
ms.openlocfilehash: 55558301b1f85f70f723d4282b438e4883d90c25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823280"
---
# <a name="snapsettings-element-windowtype-complextype-visio-xml"></a>Elemento SnapSettings (Window_Type complexType) ('XML de Visio')

Especifica los objetos que las formas ajustan ajustar cuando está en la ventana activa.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Windows.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |Representa una ventana abierta en una instancia de Microsoft Visio.
  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
## <a name="remarks"></a>Comentarios

El valor puede ser una suma de los valores en la tabla siguiente.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |No se ajusta a ningún objeto.  <br/> |
|1  <br/> |Se ajusta a subdivisiones de regla.  <br/> |
|2  <br/> |Se ajusta a la cuadrícula.  <br/> |
|4  <br/> |Se ajusta a las guías.  <br/> |
|8  <br/> |Se ajustan a asas de selección.  <br/> |
|16  <br/> |Se ajusta a los vértices.  <br/> |
|32  <br/> |Se ajusta a los puntos de conexión.  <br/> |
|256  <br/> |Se ajusta a los bordes visibles de formas.  <br/> |
|512  <br/> |Se ajusta al cuadro de alineación.  <br/> |
|1024  <br/> |Se ajusta a las opciones de extensión de las formas.  <br/> |
|32768  <br/> |Complemento deshabilitado.  <br/> |
|65536  <br/> |Se ajusta a las intersecciones.  <br/> |
   

