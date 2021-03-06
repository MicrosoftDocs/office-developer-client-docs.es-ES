---
title: Propiedad canónica PidLidSideEffects
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSideEffects
api_type:
- COM
ms.assetid: 90d601d9-5eeb-40b6-885d-ccd8a95ae322
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2d57e6a195036ead9eb42666876e91a72f65eb8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331300"
---
# <a name="pidlidsideeffects-canonical-property"></a>Propiedad canónica PidLidSideEffects

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Controla el modo en que el cliente controla un objeto de mensaje al actuar en la entrada del usuario final.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidSideEffects  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Id. largo (LID):  <br/> |0x00008510  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Configuración en tiempo de ejecución  <br/> |
   
## <a name="remarks"></a>Comentarios

Debe establecerse en una bit a bit o en cero o más de las siguientes marcas.
  
|**Name**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|seOpenToDelete  <br/> |0x0001  <br/> |Se requiere procesamiento adicional en el objeto de mensaje al eliminar.  <br/> |
|seNoFrame  <br/> |0x0008  <br/> |No hay ninguna interfaz de usuario asociada con el objeto de mensaje.  <br/> |
|seCoerceToInbox  <br/> |0x0010  <br/> |Se requiere procesamiento adicional en el objeto de mensaje al mover o copiar a un objeto de carpeta con una propiedad **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) de "IPF. Nota".  <br/> |
|seOpenTocopy  <br/> |0x0020  <br/> |Se requiere procesamiento adicional en el objeto de mensaje al copiar en otra carpeta.  <br/> |
|seOpenToMove  <br/> |0x0040  <br/> |Se requiere procesamiento adicional en el objeto de mensaje al mover a otra carpeta.  <br/> |
|seOpenForCtxMenu  <br/> |0x0100  <br/> |Se requiere procesamiento adicional en el objeto de mensaje al mostrar verbos al usuario final.  <br/> |
|seCannotUndoDelete  <br/> |0x0400  <br/> |No se puede deshacer la operación de eliminación, no se debe establecer a menos que se establezca "seOpenToDelete".  <br/> |
|seCannotUndoCopy  <br/> |0x0800  <br/> |No se puede deshacer la operación de copia, no se debe establecer a menos que se establezca "seOpenTocopy".  <br/> |
|seCannotUndoMove  <br/> |0x1000  <br/> |No se puede deshacer la operación de movimiento, no se debe establecer a menos que se establezca "seOpenToMove".  <br/> |
|seHasScript  <br/> |0x2000  <br/> |El objeto message contiene un script de usuario final.  <br/> |
|seOpenToPermDelete  <br/> |0x4000  <br/> |Se requiere procesamiento adicional para eliminar permanentemente el objeto de mensaje.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona la definición del conjunto de propiedades y las referencias a las Exchange Server de protocolo relacionados.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla objetos de mensaje y datos adjuntos.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

