---
title: Elemento SnapSettings (Window_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b87a244-b331-7e93-d304-239f8ca77061
description: Especifica los objetos a los que se acoplan las formas cuando el ajuste está activo en la ventana.
ms.openlocfilehash: 0fbe54f56f79d84e6c6bd8ddc11aa28b7e5ba1dc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540318"
---
# <a name="snapsettings-element-window_type-complextype-visio-xml"></a>Elemento SnapSettings (Window_Type complexType) (XML de Visio)

Especifica los objetos a los que se acoplan las formas cuando el ajuste está activo en la ventana.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |windows.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |Representa una ventana abierta en una instancia de Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
## <a name="remarks"></a>Comentarios

El valor puede ser una suma de los valores de la tabla siguiente.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |No se ajusta a ningún objeto.  <br/> |
|1   <br/> |Se ajusta a subdivisiones de regla.  <br/> |
|2   <br/> |Se ajusta a la cuadrícula.  <br/> |
|4   <br/> |Se ajusta a las guías.  <br/> |
|8   <br/> |Se ajustan a asas de selección.  <br/> |
|16   <br/> |Se ajusta a los vértices.  <br/> |
|32  <br/> |Se ajusta a los puntos de conexión.  <br/> |
|256  <br/> |Se ajusta a los bordes visibles de las formas.  <br/> |
|512  <br/> |Se ajusta al cuadro de alineación.  <br/> |
|1024  <br/> |Se ajusta a las opciones de extensión de las formas.  <br/> |
|32768  <br/> |Ajuste deshabilitado.  <br/> |
|65536  <br/> |Se ajusta a las intersecciones.  <br/> |
   

