---
title: elemento CP (complexType Text_Type) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4edd0a3f-e433-bf54-34cd-3b05fd10a5a5
description: Marca el principio de una ejecución de propiedades de carácter que tiene un formato conforme al elemento char correspondiente. La ejecución se define hasta el final del texto o hasta la siguiente etiqueta.
ms.openlocfilehash: 70f7d3f8333ff0f2c109862455fbd8cc3b340bf4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540563"
---
# <a name="cp-element-texttype-complextype-visio-xml"></a>elemento CP (complexType Text_Type) (XML de Visio)

Marca el principio de una ejecución de propiedades de carácter que tiene un formato conforme al elemento char correspondiente. La ejecución se define hasta el final del texto o hasta la siguiente etiqueta.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[cp_Type](cp_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Página #. XML, Master #. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="cp" type="cp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |Contiene el texto de una forma.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|IX  <br/> |xsd: unsignedInt  <br/> |necesario  <br/> |El índice del elemento char que esta propiedad ejecuta representa.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
   

