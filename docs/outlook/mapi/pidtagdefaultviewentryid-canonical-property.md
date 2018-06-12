---
title: Propiedad canónico PidTagDefaultViewEntryId
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 0db245efdd8aad73b0c094c35079f50925ca4478
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819423"
---
# <a name="pidtagdefaultviewentryid-canonical-property"></a>Propiedad canónico PidTagDefaultViewEntryId

  
  
**Se aplica a**: Outlook 
  
Contiene el identificador de entrada de la vista predeterminada de una carpeta.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DEFAULT_VIEW_ENTRYID  <br/> |
|Identificador:  <br/> |0x3616  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Contenedor MAPI  <br/> |
   
## <a name="remarks"></a>Notas

Esta propiedad es el identificador de entrada de la vista de carpeta que se debe establecer como la vista inicial. No se necesita establecer la propiedad si la vista de "Normal" es que se utilizará como la vista inicial.
  
Una aplicación cliente puede obtener esta propiedad en el momento en que se abre la carpeta y mejorar el rendimiento significativo. Esta propiedad puede usarse como un acceso directo para obtener la vista predeterminada, en lugar de abrir la tabla de contenido asociado y envío de una restricción.
  
Implementación de un proveedor de servicio del método [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) puede copiar esta propiedad cuando copian las carpetas. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Controla las operaciones de la carpeta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Ver también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedad canónico a nombres de MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI para nombres canónicos (propiedad)](mapping-mapi-names-to-canonical-property-names.md)

