---
title: Propiedad canónica PidLidOfflineStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOfflineStatus
api_type:
- COM
ms.assetid: ee69f0c4-b552-4cfd-8a39-a822d414549e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 537b45420390903d67722c074a1edcc04a0aede8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418837"
---
# <a name="pidlidofflinestatus-canonical-property"></a>Propiedad canónica PidLidOfflineStatus

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Determina el estado de un archivo de documento en un servidor que implementa [MS-LISTSWS].
  
|||
|:-----|:-----|
|Propiedades asociadas  <br/> |dispidOfflineStatus  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Id. largo (LID):  <br/> |0x000085B9  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Mensajería general  <br/> |
   
## <a name="remarks"></a>Comentarios

En la tabla siguiente se muestran los valores posibles de esta propiedad.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |El documento no está desprotebado.  <br/> |
|1  <br/> |El documento se desproteme para el usuario actual.  <br/> |
|2  <br/> |El documento no está desprotegiendo, pero el usuario actual tiene una copia del archivo guardado para su edición en el equipo actual.  <br/> |
   
Esta propiedad se calcula localmente y no se envía a un servidor en ningún momento a menos que un usuario arrastre el elemento a otra cuenta. En ese caso, se trata como una propiedad personalizada definida por el usuario.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]] 
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

