---
title: Propiedad canónica PidTagMessageToken
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageToken
api_type:
- HeaderDef
ms.assetid: fcb93346-db92-44b5-a447-59fd95f98f45
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2d832b3a53f8056c034b5e87f1f309fa3058173d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408190"
---
# <a name="pidtagmessagetoken-canonical-property"></a>Propiedad canónica PidTagMessageToken

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un token de seguridad ASN.1 para un mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MESSAGE_TOKEN  <br/> |
|Identificador:  <br/> |0x0C03  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Propiedades de mensajería segura  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad transmite información protegida relacionada con la seguridad desde su originador a su destinatario. Junto con la **propiedad PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)), garantiza la asociación de la etiqueta con el contenido del mensaje. Junto con la **propiedad PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)), comprueba que el contenido del mensaje no ha cambiado.
  
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

