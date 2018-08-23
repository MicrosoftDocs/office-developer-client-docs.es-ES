---
title: Propiedad canónica PidTagRemoteProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteProgress
api_type:
- COM
ms.assetid: 01cae79e-5b56-4cd4-83a6-f0956ff539fb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e1f57fd95ff38ef102cd74b0035dbb6b553259c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569354"
---
# <a name="pidtagremoteprogress-canonical-property"></a>Propiedad canónica PidTagRemoteProgress

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Esta propiedad contiene un número que indica el estado de una transferencia remota.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_REMOTE_PROGRESS  <br/> |
|Identificador:  <br/> |0x3E0B  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Estado MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Si no hay transferencia está en curso, esta propiedad debe establecerse en 1. Si hay una transferencia en curso, debe establecerse en un valor de 0 a 100 que indica el porcentaje de la transferencia de finalización.
  
El texto asociado con el código de estado numérico aparece en la propiedad **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)).
  
Para esta propiedad se pueden establecer los siguientes indicadores:
  
MSGSTATUS_REMOTE_DELETE
  
> Se elimina la transferencia del mensaje.
    
MSGSTATUS_REMOTE_DOWNLOAD
  
> La transferencia del mensaje está en curso.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

