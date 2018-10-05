---
title: Propiedad canónica PidLidReminderOverride
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderOverride
api_type:
- COM
ms.assetid: ad7e37e1-bd12-409f-87e5-ebc0c298a072
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4956ce33d00135c34193dec3df832c6878b2c6db
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385966"
---
# <a name="pidlidreminderoverride-canonical-property"></a>Propiedad canónica PidLidReminderOverride

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Especifica si el cliente debe respetar los valores de las propiedades de **dispidReminderFileParam** ( [PidLidReminderFileParameter ](pidlidreminderfileparameter-canonical-property.md)) y **dispidReminderPlaySound** ([PidLidReminderPlaySound](pidlidreminderplaysound-canonical-property.md)).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidReminderOverride  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x0000851C  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Reminder  <br/> |
   
## <a name="remarks"></a>Comentarios

Un cliente puede utilizar los valores predeterminados en lugar de los valores de las propiedades **dispidReminderPlaySound** y **dispidReminderFileParam** . 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Especifica las propiedades y el modelo de interacción para correo electrónico y otros avisos de objeto.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

