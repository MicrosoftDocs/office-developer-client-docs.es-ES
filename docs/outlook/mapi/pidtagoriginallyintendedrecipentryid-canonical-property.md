---
title: Propiedad canónica PidTagOriginallyIntendedRecipEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipEntryId
api_type:
- COM
ms.assetid: fc288a7a-1927-484e-b860-9cc118672ed2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cf9a070e8f892cb7bd4668b3f92397070e5b2284
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430143"
---
# <a name="pidtagoriginallyintendedrecipentryid-canonical-property"></a>Propiedad canónica PidTagOriginallyIntendedRecipEntryId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el identificador de entrada del destinatario original de un mensaje reenviado automáticamente.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ORIGINALLY_INTENDED_RECIP_ENTRYID  <br/> |
|Identificador:  <br/> |0x1012  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Servidor  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad es una de las propiedades de dirección para el destinatario del mensaje originalmente previsto. Debe ser establecido por el agente automático que reenvía el mensaje.
  
Esta propiedad corresponde al atributo X.400 report per-recipient.
  
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

