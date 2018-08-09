---
title: Propiedad canónica PidTagResourcePath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourcePath
api_type:
- COM
ms.assetid: ac49538e-6ee8-4ab4-9d79-88a83c7d0149
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d7385ea403e7ea45c97f6fd98e422ad7eb762c4c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820112"
---
# <a name="pidtagresourcepath-canonical-property"></a>Propiedad canónica PidTagResourcePath

  
  
**Hace referencia a**: Outlook 
  
Contiene una ruta de acceso al servidor del proveedor de servicios.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W  <br/> |
|Identificador:  <br/> |0x3E07  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Estado MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

La ruta de acceso contenida en estas propiedades representa la ruta de acceso sugerida donde el usuario puede encontrar recursos. La definición de estas propiedades es específico del proveedor. Por ejemplo, una aplicación de programación usa estas propiedades para especificar la ubicación sugerida para sus archivos de aplicación de programación.
  
El perfil de usuario de mensajería proporciona estas propiedades como una comodidad para que una aplicación cliente no tiene que solicitar al usuario de mensajería de una ruta de acceso de red o la letra de la unidad de red.
  
MAPI sólo funciona con los nombres de archivo en el juego de caracteres estadounidense National Standards Institute (ANSI). Las aplicaciones que usan nombres de archivo en un juego de caracteres del fabricante de equipos originales (OEM) deben convertirlos a ANSI antes de llamar a MAPI.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

