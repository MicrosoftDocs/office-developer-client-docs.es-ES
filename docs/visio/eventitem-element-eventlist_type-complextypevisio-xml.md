---
title: Elemento de EventItem (EventList_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Encapsula un código de evento.
ms.openlocfilehash: dcdd3aa264e8ddfb1aa6f2e908f1c43a0d470872
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822080"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a>Elemento de EventItem (EventList_Type complexType) ('XML de Visio')

Encapsula un código de evento.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[EventItem_Type](eventitem_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Document.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[EventList](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[EventList_Type](eventlist_type-complextypevisio-xml.md) <br/> |Contiene un elemento **EventItem** para cada evento al que debe responder un objeto.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obligatorio**|**Descripción**|**Valores posibles**|
|:-----|:-----|:-----|:-----|:-----|
|Acción  <br/> |xsd:unsignedShort  <br/> |necesario  <br/> |Especifica el código de acción del elemento primario **EventItem** .  <br/> |Valores del tipo xsd:unsignedShort.  <br/> |
|Habilitado  <br/> |Boolean con tipo  <br/> |opcional  <br/> |Representa una marca que indica si el evento está habilitado o deshabilitado.  <br/> |Valores del tipo Boolean con tipo.  <br/> |
|EventCode  <br/> |xsd:unsignedShort  <br/> |necesario  <br/> |Un código que indica el evento que desencadena el complemento.  <br/> |Valores del tipo xsd:unsignedShort.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |necesario  <br/> |El identificador del evento.  <br/> |Valores del tipo xsd:unsignedInt.  <br/> |
|Destino  <br/> |xsd: String  <br/> |necesario  <br/> |Especifica el destino de un evento.  <br/> |Valores del tipo XSD: String.  <br/> |
|TargetArgs  <br/> |xsd: String  <br/> |necesario  <br/> |Especifica una cadena que contiene los argumentos que se envíen al destino de un evento.  <br/> |Valores del tipo XSD: String.  <br/> |
   

