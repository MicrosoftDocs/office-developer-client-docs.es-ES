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
ms.openlocfilehash: 30ed8053c9c3d77f4831da37ddd2456ad0564a5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415729"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a>Propiedad canónica PidTagContentIntegrityCheck

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un valor de comprobación de integridad de contenido ASN.1 que permite al remitente del mensaje proteger el contenido del mensaje de la divulgación a destinatarios no autorizados.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTENT_INTEGRITY_CHECK  <br/> |
|Identificador:  <br/> |0x0C00  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad proporciona no rechazo del contenido del mensaje. Junto con **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)), garantiza que el contenido de un mensaje llegue a su destino sin cambios.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

