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
ms.openlocfilehash: fa29a55a5fc2ce89e125909d13a2c14a347ef831
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594029"
---
# <a name="pidlidsideeffects-canonical-property"></a>Propiedad canónica PidLidSideEffects

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Controla cómo se administra un objeto de mensaje por el cliente cuando actúa en la entrada del usuario final.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidSideEffects  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008510  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Configuración de tiempo de ejecución  <br/> |
   
## <a name="remarks"></a>Comentarios

Se debe establecer en un bit a bit o cero o más de las siguientes marcas.
  
|**Nombre**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|seOpenToDelete  <br/> |0 x 0001  <br/> |Al eliminar, se requiere procesamiento adicional en el objeto de mensaje.  <br/> |
|seNoFrame  <br/> |0x0008  <br/> |Interfaz de usuario no está asociado con el objeto de mensaje.  <br/> |
|seCoerceToInbox  <br/> |0x0010  <br/> |Se requiere procesamiento adicional en el objeto de mensaje al mover o copiar a un objeto de carpeta con una propiedad de **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) de "IPF. Tenga en cuenta".  <br/> |
|seOpenTocopy  <br/> |0 x 0020  <br/> |Se requiere procesamiento adicional en el objeto de mensaje cuando se copian a otra carpeta.  <br/> |
|seOpenToMove  <br/> |0x0040  <br/> |Se requiere procesamiento adicional en el objeto de mensaje cuando se mueve a otra carpeta.  <br/> |
|seOpenForCtxMenu  <br/> |0 x 0100  <br/> |Se requiere procesamiento adicional en el objeto de mensaje al mostrar los verbos para el usuario final.  <br/> |
|seCannotUndoDelete  <br/> |0 x 0400  <br/> |No se puede deshacer la operación de eliminación, no debe estar establecida a menos que se establezca "seOpenToDelete".  <br/> |
|seCannotUndoCopy  <br/> |0 x 0800  <br/> |No se puede deshacer la operación de copia, no debe estar establecida a menos que se establezca "seOpenTocopy".  <br/> |
|seCannotUndoMove  <br/> |0 x 1000  <br/> |No se puede deshacer la operación de movimiento, no debe estar establecida a menos que se establezca "seOpenToMove".  <br/> |
|seHasScript  <br/> |0 x 2000  <br/> |El objeto de mensaje contiene secuencias de comandos de usuario final.  <br/> |
|seOpenToPermDelete  <br/> |0 x 4000  <br/> |Se requiere procesamiento adicional para eliminar permanentemente el objeto de mensaje.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona la definición del conjunto de propiedad y referencias a las especificaciones de protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

