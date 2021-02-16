---
title: Propiedad canónica PidTagDefaultViewEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultViewEntryId
api_type:
- HeaderDef
ms.assetid: 1b4e82ed-c207-4828-8a5b-0ef312962355
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6d284782de86b603e6bbe190931a85cd9196c88b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270017"
---
# <a name="pidtagdefaultviewentryid-canonical-property"></a>Propiedad canónica PidTagDefaultViewEntryId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el identificador de entrada de la vista predeterminada de una carpeta.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DEFAULT_VIEW_ENTRYID  <br/> |
|Identificador:  <br/> |0x3616  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Contenedor MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad es el identificador de entrada de la vista de carpeta que debe establecerse como vista inicial. No es necesario establecer la propiedad si se va a usar la vista "Normal" como vista inicial.
  
Una aplicación cliente puede obtener esta propiedad en el momento en que abre la carpeta y obtener mejoras significativas en el rendimiento. Esta propiedad se puede usar como acceso directo para obtener la vista predeterminada, en lugar de abrir la tabla de contenido asociada y enviar una restricción.
  
Una implementación del proveedor de servicios del [método IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) puede copiar esta propiedad cuando copia carpetas. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Controla las operaciones de carpeta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

