---
title: Propiedad canónica PidTagServiceDeleteFiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDeleteFiles
api_type:
- COM
ms.assetid: 9ec80a93-9e8f-46be-a1d4-7648aae47fec
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 236349a6b53eeb2f5c18c841c05cfb80a3fce824
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580225"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a>Propiedad canónica PidTagServiceDeleteFiles

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una lista de nombres de archivo que se va a eliminar cuando se desinstala el servicio de mensajes.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W  <br/> |
|Identificador:  <br/> |0x3D10  <br/> |
|Tipo de datos:  <br/> |PT_MV_STRING8, PT_MV_UNICODE  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Los nombres de archivo en la lista de contenidos en estas propiedades se eliminan del equipo cuando se usa el panel de control para desinstalar el servicio de mensajes. No incluir en la lista de cualquier archivo DLL que es compatible con varios servicios de mensaje o servicios adicionales de mensaje podrían quitarse sin darse cuenta.
  
MAPI sólo funciona con los nombres de archivo y otras cadenas pasan a ella, en el juego de caracteres ANSI. Las aplicaciones que usan nombres de archivo en un juego de caracteres OEM deben convertirlos a ANSI antes de llamar a MAPI.
  
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

