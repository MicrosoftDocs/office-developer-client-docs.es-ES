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
ms.openlocfilehash: da01385f83d9af9ad02eeb2fed08e3bc22d4df84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336403"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a>Propiedad canónica PidTagServiceDeleteFiles

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una lista de nombres de archivo que se eliminarán cuando se desinstale el servicio de mensajes.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W  <br/> |
|Identificador:  <br/> |0x3D10  <br/> |
|Tipo de datos:  <br/> |PT_MV_STRING8, PT_MV_UNICODE  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Los nombres de archivo de la lista que se encuentran en estas propiedades se eliminan del equipo cuando se usa el panel de control para desinstalar el servicio de mensajes. No incluya en la lista ninguna DLL que admita varios servicios de mensajes o que se puedan quitar accidentalmente servicios de mensajes adicionales.
  
MAPI solo funciona con nombres de archivo y otras cadenas que se le pasan, en el juego de caracteres ANSI. Las aplicaciones que usan nombres de archivo en un conjunto de caracteres OEM deben convertirlos a ANSI antes de llamar a MAPI.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

