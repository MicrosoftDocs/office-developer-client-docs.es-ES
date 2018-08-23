---
title: Propiedad canónica PidTagItemTemporaryflags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagItemTemporaryflags
api_type:
- HeaderDef
ms.assetid: 8066de8e-2b77-4bac-8df3-e64b03ee42b9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e8bed42ee44e48540df52e806c7113e02b60cd07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593637"
---
# <a name="pidtagitemtemporaryflags-canonical-property"></a>Propiedad canónica PidTagItemTemporaryflags

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una marca que indica que un mensaje se ha de lectura, pero no está marcado como leído.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ITEM_TMPFLAGS  <br/> |
|Identificador:  <br/> |0x1097  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |General de mensajería  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se usa en la carpeta de búsqueda de mensajes no leídos de Outlook para realizar un seguimiento de los mensajes que se han leído sin realmente los marcar como leído, que debería quitarlos de la carpeta. Cuando los cambios de la vista se ha quitado esta propiedad y el elemento se marca como de lectura. Esta propiedad no se sincronizará con el servidor de Exchange.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Controla las operaciones de la carpeta.
    
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

