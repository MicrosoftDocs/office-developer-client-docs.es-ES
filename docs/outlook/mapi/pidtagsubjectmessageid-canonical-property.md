---
title: Propiedad canónica PidTagSubjectMessageId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubjectMessageId
api_type:
- COM
ms.assetid: d4b1a087-0986-467a-aaa9-fc643f7c56fc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c89a0a86ac733cd2cce1efc071e47fcb011fec18
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573071"
---
# <a name="pidtagsubjectmessageid-canonical-property"></a>Propiedad canónica PidTagSubjectMessageId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un valor binario que se copió desde el mensaje para el que se genera un informe. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SUBJECT_IPM  <br/> |
|Identificador:  <br/> |0x0038  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Sobres MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad, al igual que la propiedad **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)), se puede usar para correlacionar un informe con el mensaje original. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

