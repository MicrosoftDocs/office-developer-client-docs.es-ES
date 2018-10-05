---
title: Propiedad canónica PidTagDeferredSendUnits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendUnits
api_type:
- HeaderDef
ms.assetid: 2386be9f-18c9-4949-a2aa-efc8e212801c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: becc076efe0f4f805eb2a8db071b70ad731ee256
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385690"
---
# <a name="pidtagdeferredsendunits-canonical-property"></a>Propiedad canónica PidTagDeferredSendUnits

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Especifica la unidad de tiempo por el que se multiplicará el valor de la propiedad **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DEFERRED_SEND_UNITS  <br/> |
|Identificador:  <br/> |0x3FEC  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Estado MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Si se establece, esta propiedad debe tener uno de los siguientes valores:
  
|||
|:-----|:-----|
|**PidTagDeferredSendUnits** <br/> |Descripción  <br/> |
|0  <br/> |Minutos, por ejemplo 60 segundos  <br/> |
|1  <br/> |Horas, por ejemplo 60 x 60 segundos  <br/> |
|2  <br/> |Día, por ejemplo 24 x 60 x 60 segundos  <br/> |
|3  <br/> |Semana, por ejemplo 7x24x60x60 segundos  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

