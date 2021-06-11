---
title: Elemento EventItem (EventList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Encapsula un código de evento.
ms.openlocfilehash: 0db88a175d3e0330cb648f870559d9d2bd4dc1d8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541844"
---
# <a name="eventitem-element-eventlist_type-complextype-visio-xml"></a>Elemento EventItem (EventList_Type complexType) (Visio XML)

Encapsula un código de evento.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[EventItem_Type](eventitem_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[EventList](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[EventList_Type](eventlist_type-complextypevisio-xml.md) <br/> |Contiene un **elemento EventItem** para cada evento al que debe responder un objeto.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Acción  <br/> |xsd:unsignedShort  <br/> |necesario  <br/> |Especifica el código de acción del elemento **primario EventItem.**  <br/> |Valores del tipo xsd:unsignedShort.  <br/> |
|Habilitado  <br/> |xsd:boolean  <br/> |opcional  <br/> |Representa una marca que indica si el evento está habilitado o deshabilitado.  <br/> |Valores del tipo xsd:boolean.  <br/> |
|EventCode  <br/> |xsd:unsignedShort  <br/> |necesario  <br/> |Código que indica el evento que desencadena el complemento.  <br/> |Valores del tipo xsd:unsignedShort.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |El identificador del evento.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Target  <br/> |xsd:string  <br/> |necesario  <br/> |Especifica el destino de un evento.  <br/> |Valores del tipo xsd:string.  <br/> |
|TargetArgs  <br/> |xsd:string  <br/> |necesario  <br/> |Especifica una cadena que contiene argumentos que se enviarán al destino de un evento.  <br/> |Valores del tipo xsd:string.  <br/> |
   

