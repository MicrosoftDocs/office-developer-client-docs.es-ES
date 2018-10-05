---
title: Propiedad canónica PidLidReminderTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderTime
api_type:
- COM
ms.assetid: f4068ff0-2aa2-4332-be7d-ecebda30dfff
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8371418aabc557f48c74039320305df59624d7ac
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382473"
---
# <a name="pidlidremindertime-canonical-property"></a>Propiedad canónica PidLidReminderTime

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Especifica la hora de señal inicial de un aviso.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidReminderTime  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008502  <br/> |
|Tipo de datos:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Reminder  <br/> |
   
## <a name="remarks"></a>Comentarios

Para los objetos de calendario, esta propiedad representa la hora cuando el usuario sería las últimas que es la hora de inicio de la cita. Los clientes deben establecer el valor en hora Universal coordinada (UTC).
  
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

