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
ms.openlocfilehash: a5a9d0796bc92514ae6d990b7328364b85bc55cd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439845"
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

Si no hay ninguna transferencia en curso, esta propiedad debe establecerse en 1. Si una transferencia está en curso, debe establecerse en un valor de 0 a 100 que indica el porcentaje de finalización de la transferencia.
  
El texto asociado con el código de estado numérico aparece **en la propiedad PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)).
  
Se pueden establecer las siguientes marcas para esta propiedad:
  
MSGSTATUS_REMOTE_DELETE
  
> Se elimina la transferencia de mensajes.
    
MSGSTATUS_REMOTE_DOWNLOAD
  
> La transferencia de mensajes está en curso.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

