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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326302"
---
# <a name="pidlidofflinestatus-canonical-property"></a>Propiedad canónica PidLidOfflineStatus

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Determina el estado de un archivo de documento en un servidor que implementa [MS-LISTSWS].
  
|||
|:-----|:-----|
|Propiedades asociadas  <br/> |dispidOfflineStatus  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|IDENTIFICADOR largo (LID):  <br/> |0x000085B9  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Mensajes generales  <br/> |
   
## <a name="remarks"></a>Comentarios

En la siguiente tabla se muestran los valores posibles de esta propiedad.
  
|**Value**|**Descripción**|
|:-----|:-----|
|comprendi  <br/> |El documento no está desprotegido.  <br/> |
|1  <br/> |El documento está desprotegido para el usuario actual.  <br/> |
|segundo  <br/> |El documento no está desprotegido, pero el usuario actual tiene una copia del archivo guardada para editarla en el equipo actual.  <br/> |
   
Esta propiedad se calcula de forma local y no se envía a un servidor en cualquier momento a menos que un usuario arrastre el elemento a otra cuenta. En ese caso, se trata como una propiedad personalizada definida por el usuario.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]] 
  
> Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

