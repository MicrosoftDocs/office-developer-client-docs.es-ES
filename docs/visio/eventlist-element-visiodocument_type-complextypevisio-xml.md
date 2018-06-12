---
title: Elemento de EventList (VisioDocument_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 40bb8c7c-89ef-22e1-5edf-e2423fc89660
description: Contiene un elemento EventItem para cada evento al que debe responder un objeto.
ms.openlocfilehash: e1033ae93ca272b8ea1d9855d08ad13a444612db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822076"
---
# <a name="eventlist-element-visiodocumenttype-complextype-visio-xml"></a>Elemento de EventList (VisioDocument_Type complexType) ('XML de Visio')

Contiene un elemento **EventItem** para cada evento al que debe responder un objeto. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[EventList_Type](eventlist_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Elementos de documento** <br/> |Document.Xml  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="EventList" type="EventList_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |El elemento raíz de un documento de Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[EventItem](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[EventItem_Type](eventitem_type-complextypevisio-xml.md) <br/> |Encapsula un código de evento.  <br/> |
   
### <a name="attributes"></a>Atributos

Ninguno.
  

