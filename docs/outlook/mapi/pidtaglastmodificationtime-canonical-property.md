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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279712"
---
# <a name="pidtaglastmodificationtime-canonical-property"></a>Propiedad canónica PidTagLastModificationTime

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene la fecha y hora en que se modificó por última vez el objeto o subobjeto. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_LAST_MODIFICATION_TIME  <br/> |
|Identificador:  <br/> |0x3008  <br/> |
|Tipo de datos:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Hora del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se establece inicialmente en el mismo valor que la **propiedad PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)). Los subobjetos adjuntos pueden actualizarlo según sea necesario copiando la última hora de modificación mantenida por el sistema de archivos nativo. Una aplicación cliente puede establecer esta propiedad hasta la primera llamada al método [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) A partir de entonces, el proveedor debe actualizar **PR_LAST_MODIFICATION_TIME** durante cada **llamada IMAPIProp::SaveChanges.** 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla objetos de mensaje y datos adjuntos.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla la sincronización de datos de objetos de mensajería entre un servidor y un cliente.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones de listas de usuarios, contactos, grupos y recursos.
    
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

