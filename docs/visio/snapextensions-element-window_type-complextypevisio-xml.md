---
title: Elemento SnapExtensions (Window_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a12ae10-6aa4-c845-5ede-1c14c6dac80f
description: Especifica si una configuración de extensión de ajuste específica está habilitada o deshabilitada para la ventana activa. El valor puede ser una suma de los valores de la tabla siguiente.
ms.openlocfilehash: bf3a6ae8cbeaadca8d4d899d96c916ee13ce9dfc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540325"
---
# <a name="snapextensions-element-window_type-complextype-visio-xml"></a>Elemento SnapExtensions (Window_Type complexType) (XML de Visio)

Especifica si una configuración de extensión de ajuste específica está habilitada o deshabilitada para la ventana activa. El valor puede ser una suma de los valores de la tabla siguiente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |windows.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
## <a name="remarks"></a>Comentarios

El valor del **elemento SnapExtensions** puede ser una suma de los valores de la tabla siguiente. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |No se ajusta a ningún objeto.  <br/> |
|1   <br/> |Se ajusta a la extensión del cuadro de alineación.  <br/> |
|2   <br/> |Se ajusta a la extensión del eje central.  <br/> |
|4   <br/> |Se ajusta a la extensión tangente de curva.  <br/> |
|8   <br/> |Se ajusta a la extensión de extremo.  <br/> |
|16   <br/> |Se ajusta a la extensión de punto medio.  <br/> |
|32  <br/> |Se ajusta a la extensión lineal.  <br/> |
|64  <br/> |Ajustar a la extensión de curva.  <br/> |
|128  <br/> |Se ajusta a la extensión perpendicular del extremo.  <br/> |
|256  <br/> |Se ajusta a la extensión perpendicular del punto medio.  <br/> |
|512  <br/> |Se ajusta a la extensión horizontal del extremo.  <br/> |
|1024  <br/> |Se ajusta a la extensión vertical del extremo.  <br/> |
|2048  <br/> |Se ajusta a la extensión central de elipse.  <br/> |
|4096  <br/> |Se ajusta a la extensión de ángulos isométricos.  <br/> |
   

