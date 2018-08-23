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
ms.openlocfilehash: d950ee21c0c4c41e84c0fe1f8104219e63f84cec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592678"
---
# <a name="pidtagservicename-canonical-property"></a>Propiedad canónica PidTagServiceName

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el nombre de un servicio de mensajes como conjunto por el usuario en el archivo MapiSvc.inf.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W  <br/> |
|Identificador:  <br/> |0x3D09  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

El nombre de estas propiedades es específico para el servicio de mensajes. Se trata de la sección [Services] en MapiSvc.inf.
  
Estas propiedades aparecen como una columna en la tabla de servicios de mensaje y se pueden usar para filtrar los servicios. Debido a que se usa para identificar y filtrar los servicios, el valor no debe estar adaptado.
  
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

