---
title: Propiedad canónica PidTagSpoolerStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSpoolerStatus
api_type:
- COM
ms.assetid: a10d86fc-3a73-49dc-b974-ed852ec715e9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 426d26cae147faf3f843ac547de9d205d766ac44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348212"
---
# <a name="pidtagspoolerstatus-canonical-property"></a>Propiedad canónica PidTagSpoolerStatus

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el estado del mensaje en función de la información que está disponible para la cola MAPI.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SPOOLER_STATUS  <br/> |
|Identificador:  <br/> |0x0E10  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI no transmitible  <br/> |
   
## <a name="remarks"></a>Comentarios

MAPI calcula esta propiedad en los objetos de mensaje.
  
Esta propiedad aparece sólo en los mensajes entrantes y está reservada en los demás casos. Indica si un mensaje se ha entregado o no a su ubicación final o si un proveedor de mensajes de mensajería puede eliminar el mensaje mientras se reenruta.
  
Las aplicaciones cliente nunca deben establecer esta propiedad. Para un mensaje entrante, un proveedor de servicios o cliente puede llamar a [IMAPIProp:: GetProps](imapiprop-getprops.md) en esta propiedad para determinar el estado del mensaje. El valor S_OK indica que el mensaje se entregó correctamente al almacén de mensajes. El valor MAPI_E_OBJECT_DELETED indica que el mensaje se eliminó y que nunca se confirmó en el almacén. 
  
Los proveedores de almacenamiento de mensajes deben admitir esta propiedad en los mensajes, las tablas de destinatarios y la tabla de colas de salida. Los clientes y proveedores deben poder establecer columnas en la tabla de colas de salida y restringir en función de esta propiedad.
  
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

