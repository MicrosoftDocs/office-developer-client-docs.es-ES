---
title: Propiedad canónica PidTagStoreProvider
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreProvider
api_type:
- COM
ms.assetid: 6f6cc66f-a08e-4f8e-b33a-d3674319248e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 02d2c30fede7e554910a1bedb01b79c488447bb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595359"
---
# <a name="pidtagstoreprovider-canonical-property"></a>Propiedad canónica PidTagStoreProvider

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una estructura [MAPIUID](mapiuid.md) definida por el proveedor que indica el tipo del almacén de mensajes. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MDB_PROVIDER  <br/> |
|Identificador:  <br/> |0x3414  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Propiedades de Id.  <br/> |
   
## <a name="remarks"></a>Comentarios

La estructura [MAPIUID](mapiuid.md) identifica el tipo de almacén de mensajes. El valor se calcula mediante los proveedores de almacén de mensajes en los objetos de almacén de mensajes y es único para cada proveedor. Normalmente se usa para la exploración a través de la tabla de almacenamiento de mensajes para buscar un almacén del tipo que desee, como las carpetas públicas. 
  
Esta propiedad es análoga a la propiedad **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) de libretas de direcciones. 
  
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

