---
title: Conectar (Connects_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: Representa una conexión entre dos formas de un dibujo, como una línea y un cuadro en un organigrama.
ms.openlocfilehash: 3450a07e042fc633b9cd4952d9b3ad6b8190ed1e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541999"
---
# <a name="connect-element-connects_type-complextype-visio-xml"></a>Conectar (Connects_Type complexType) (Visio XML)

Representa una conexión entre dos formas de un dibujo, como una línea y un cuadro en un organigrama.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Connect_Type](connect_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Contiene un **Conectar** para cada conexión entre dos formas de un dibujo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|FromCell  <br/> |xsd:string  <br/> |opcional  <br/> |Celda desde la que se origina una conexión.  <br/> |Valores del tipo xsd:string.  <br/> |
|FromPart  <br/> |xsd:int  <br/> |opcional  <br/> |La parte de una forma desde la que se origina una conexión.  <br/> |Valores del tipo xsd:int.  <br/> |
|FromSheet  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Identificador de la forma desde la que se origina una conexión o conexiones.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|ToCell  <br/> |xsd:string  <br/> |opcional  <br/> |Celda a la que se realiza una conexión.  <br/> |Valores del tipo xsd:string.  <br/> |
|ToPart  <br/> |xsd:int  <br/> |opcional  <br/> |La parte de una forma a la que se realiza una conexión.  <br/> |Valores del tipo xsd:Int.  <br/> |
|ToSheet  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |Identificador de la forma a la que se realizan una o más conexiones.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
   

