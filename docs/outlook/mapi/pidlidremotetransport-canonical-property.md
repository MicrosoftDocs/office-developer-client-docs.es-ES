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
ms.openlocfilehash: ddedc2ca0785be2fe4850ec3cfdf979d1e5f2798
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439446"
---
# <a name="pidlidremotetransport-canonical-property"></a>Propiedad canónica PidLidRemoteTransport

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Identifica la cuenta con la que está asociado el elemento de encabezado, principalmente para implementar la funcionalidad pop Leave on Server. 
  
|||
|:-----|:-----|
|Propiedades asociadas  <br/> |dispidRemoteXP  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Remote  <br/> |
|Long ID (LID):  <br/> |0x00008F03  <br/> |
|Tipo de datos:  <br/> |PT_STRING8  <br/> |
|Área:  <br/> |Mensaje remoto  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad solo es relevante en los mensajes que tienen una clase de mensaje de IPM. Remoto. Microsoft Outlook mantiene una asignación de varias cuentas que se descargan en un almacén determinado en un mensaje de información asociada a carpetas (FAI), pero también podría mantener esta información en el Registro.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]] 
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

