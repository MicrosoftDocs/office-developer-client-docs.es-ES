---
title: Elemento SnapExtensions (complexType Window_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a12ae10-6aa4-c845-5ede-1c14c6dac80f
description: Especifica si una configuración de extensión de ajuste específica está habilitada o deshabilitada para la ventana activa. El valor puede ser una suma de los valores de la tabla siguiente.
ms.openlocfilehash: 57fde520d3dc8e0582c0062a599d5f38a73169b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334422"
---
# <a name="snapextensions-element-windowtype-complextype-visio-xml"></a>Elemento SnapExtensions (complexType Window_Type) ("XML" de Visio)

Especifica si una configuración de extensión de ajuste específica está habilitada o deshabilitada para la ventana activa. El valor puede ser una suma de los valores de la tabla siguiente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Windows. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
## <a name="remarks"></a>Comentarios

El valor del elemento **SnapExtensions** puede ser una suma de los valores de la tabla siguiente. 
  
|**Value**|**Descripción**|
|:-----|:-----|
|comprendi  <br/> |No se ajusta a ningún objeto.  <br/> |
|1  <br/> |Se ajusta a la extensión del cuadro de alineación.  <br/> |
|segundo  <br/> |Se ajusta a la extensión del eje central.  <br/> |
|4  <br/> |Ajustar a la extensión tangente a curva.  <br/> |
|8,5  <br/> |Ajustar a la extensión de extremo.  <br/> |
|16  <br/> |Se ajusta a la extensión de punto medio.  <br/> |
|32  <br/> |Se ajusta a la extensión lineal.  <br/> |
|64  <br/> |Ajustar a la extensión de curva.  <br/> |
|128  <br/> |Ajustar a la extensión perpendicular del extremo.  <br/> |
|256  <br/> |Se ajusta a la extensión perpendicular de punto medio.  <br/> |
|512  <br/> |Ajustar a la extensión horizontal del extremo.  <br/> |
|1024  <br/> |Ajustar a la extensión vertical del extremo.  <br/> |
|2048  <br/> |Se ajusta a la extensión del centro de elipses.  <br/> |
|4096  <br/> |Ajustar a la extensión ángulos isométricos.  <br/> |
   

