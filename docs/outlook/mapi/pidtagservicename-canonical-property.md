---
title: Propiedad canónica PidTagServiceName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceName
api_type:
- COM
ms.assetid: 9a63d647-7504-42fc-b317-6b02b89070eb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e5659113b1c6579913042ae0c8dfcd03e9802621
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438963"
---
# <a name="pidtagservicename-canonical-property"></a>Propiedad canónica PidTagServiceName

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el nombre de un servicio de mensajes establecido por el usuario en el archivo MapiSvc.inf.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W  <br/> |
|Identificador:  <br/> |0x3D09  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

El nombre contenido en estas propiedades es específico del servicio de mensajes. Proviene de la sección [Servicios] de MapiSvc.inf.
  
Estas propiedades aparecen como una columna en la tabla de servicio de mensajes y se pueden usar para filtrar servicios. Dado que se usa para identificar y filtrar servicios, el valor no debe localizarse.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

