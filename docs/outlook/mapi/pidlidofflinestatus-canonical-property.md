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
ms.openlocfilehash: 7d9f8cf4fbdeab70e40447411ed8efd35ef7899e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588779"
---
# <a name="pidlidofflinestatus-canonical-property"></a>Propiedad canónica PidLidOfflineStatus

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Determina el estado de un archivo de documento en un servidor que implementa [MS-LISTSWS].
  
|||
|:-----|:-----|
|Propiedades asociadas  <br/> |dispidOfflineStatus  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x000085B9  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |General de mensajería  <br/> |
   
## <a name="remarks"></a>Comentarios

En la siguiente tabla se muestra los valores posibles de esta propiedad.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |Documento no está desprotegido.  <br/> |
|1  <br/> |Documento está desprotegido para el usuario actual.  <br/> |
|2  <br/> |Documento no está desprotegido, pero el usuario actual tiene una copia del archivo guardado para su edición en el equipo actual.  <br/> |
   
Esta propiedad se calcula localmente y no se envía a un servidor en cualquier momento a menos que un usuario arrastra el elemento a otra cuenta. En ese caso, se trata como una propiedad personalizada definida por el usuario.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]] 
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

