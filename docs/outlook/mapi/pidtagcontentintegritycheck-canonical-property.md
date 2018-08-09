---
title: Propiedad canónica PidTagContentIntegrityCheck
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentIntegrityCheck
api_type:
- HeaderDef
ms.assetid: c7f10b8a-6b20-44cf-bde6-8d2b711c1c14
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2082db4ccd107fcd02e37882707e4e3ee697695d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819366"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a>Propiedad canónica PidTagContentIntegrityCheck

  
  
**Hace referencia a**: Outlook 
  
Contiene un valor de comprobación de integridad del contenido de ASN.1 que permite a un remitente del mensaje proteger el contenido del mensaje de divulgación a destinatarios no autorizados.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTENT_INTEGRITY_CHECK  <br/> |
|Identificador:  <br/> |0x0c00  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se proporciona para el no rechazo del contenido del mensaje. Junto con **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), se asegura de que el contenido de un mensaje llega a su destino sin cambios.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

