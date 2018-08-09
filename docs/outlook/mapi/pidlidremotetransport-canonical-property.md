---
title: Propiedad canónica PidLidRemoteTransport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRemoteTransport
api_type:
- COM
ms.assetid: b3b30d6a-05cd-4dd1-a162-20768f12e680
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b0f86b2260299d2d0294598628f2895c50ed9452
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818901"
---
# <a name="pidlidremotetransport-canonical-property"></a>Propiedad canónica PidLidRemoteTransport

  
  
**Hace referencia a**: Outlook 
  
Identifica el elemento de encabezado de qué cuenta está asociado, principalmente para implementar la deje de POP en la funcionalidad del servidor. 
  
|||
|:-----|:-----|
|Propiedades asociadas  <br/> |dispidRemoteXP  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Remote  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008F03  <br/> |
|Tipo de datos:  <br/> |PT_STRING8  <br/> |
|Área:  <br/> |Mensaje remoto  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad sólo es relevante en los mensajes que tienen una clase de mensaje IPM. Remoto. Microsoft Outlook mantiene una asignación de varias cuentas que va a descargar en un almacén determinado en un mensaje de información de asociados de carpeta (FAI), pero también puede mantener esta información en el registro.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]] 
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

