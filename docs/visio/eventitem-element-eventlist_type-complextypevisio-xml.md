---
title: Elemento EventItem (complexType EventList_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Encapsula un código de evento.
ms.openlocfilehash: 6ed539bd6cb4524b2498b636295442bed917c72a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337201"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a>Elemento EventItem (complexType EventList_Type) ("XML" de Visio)

Encapsula un código de evento.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[EventItem_Type](eventitem_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Archivo de esquema** <br/> |VisioSchema15. xsd  <br/> |
|**Elementos de documento** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Definición

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[EventList](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[EventList_Type](eventlist_type-complextypevisio-xml.md) <br/> |Contiene un elemento **EventItem** por cada evento al que debe responder un objeto.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obligatorio**|**Descripción**|**Posibles valores**|
|:-----|:-----|:-----|:-----|:-----|
|Acción  <br/> |xsd: unsignedShort  <br/> |necesario  <br/> |Especifica el código de acción del elemento **EventItem** primario.  <br/> |Valores del tipo xsd: unsignedShort.  <br/> |
|Habilitado  <br/> |xsd: Boolean  <br/> |opcional  <br/> |Representa una marca que indica si el evento está habilitado o deshabilitado.  <br/> |Valores del tipo xsd: Boolean.  <br/> |
|EventCode  <br/> |xsd: unsignedShort  <br/> |necesario  <br/> |Un código que indica el evento que desencadena el complemento.  <br/> |Valores del tipo xsd: unsignedShort.  <br/> |
|ID  <br/> |xsd: unsignedInt  <br/> |necesario  <br/> |IDENTIFICADOR del evento.  <br/> |Valores del tipo xsd: unsignedInt.  <br/> |
|Target  <br/> |xsd: String  <br/> |necesario  <br/> |Especifica el destino de un evento.  <br/> |Valores del tipo xsd: String.  <br/> |
|TargetArgs  <br/> |xsd: String  <br/> |necesario  <br/> |Especifica una cadena que contiene los argumentos que se enviarán al destino de un evento.  <br/> |Valores del tipo xsd: String.  <br/> |
   

