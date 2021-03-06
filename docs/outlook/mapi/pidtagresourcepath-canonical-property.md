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
ms.openlocfilehash: 32d150e508f5c208e15d5ee5f0b8c800a1e597f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429862"
---
# <a name="pidtagresourcepath-canonical-property"></a>Propiedad canónica PidTagResourcePath

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una ruta de acceso al servidor del proveedor de servicios.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W  <br/> |
|Identificador:  <br/> |0x3E07  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Estado MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

La ruta de acceso contenida en estas propiedades representa la ruta de acceso sugerida donde el usuario puede encontrar recursos. La definición de estas propiedades es específica del proveedor. Por ejemplo, una aplicación de programación usa estas propiedades para especificar la ubicación sugerida para sus archivos de aplicación de programación.
  
El perfil de usuario de mensajería proporciona estas propiedades para que una aplicación cliente no tenga que solicitar al usuario de mensajería una ruta de acceso de red o una letra de unidad de red.
  
MAPI solo funciona con nombres de archivo en el conjunto de caracteres del American National Standards Institute (ANSI). Las aplicaciones que usan nombres de archivo en un juego de caracteres del fabricante de equipos originales (OEM) deben convertirlos en ANSI antes de llamar a MAPI.
  
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

