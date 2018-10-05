---
title: Propiedad canónica PidTagLastModificationTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLastModificationTime
api_type:
- HeaderDef
ms.assetid: a64e5300-6865-4588-8e1b-158cfd9c60c2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dea709b457e28efef62718fc388621e01c4eb5bf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387331"
---
# <a name="pidtaglastmodificationtime-canonical-property"></a>Propiedad canónica PidTagLastModificationTime

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene la fecha y hora de última modificación de el objeto o subobjetos. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_LAST_MODIFICATION_TIME  <br/> |
|Identificador:  <br/> |0x3008  <br/> |
|Tipo de datos:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Hora del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se establece inicialmente en el mismo valor que la propiedad **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)). Datos adjuntos subobjetos actualizarlo, según sea necesario mediante la copia de la hora de última modificación mantenida por el sistema de archivos nativo. Una aplicación cliente puede establecer esta propiedad hasta la primera llamada al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . En el proveedor debe actualizar **PR_LAST_MODIFICATION_TIME** durante cada llamada **IMAPIProp::SaveChanges** . 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla la sincronización de datos de objeto mensajería entre un servidor y un cliente.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.
    
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

