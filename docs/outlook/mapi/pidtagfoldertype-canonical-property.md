---
title: Propiedad canónica PidTagFolderType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderType
api_type:
- HeaderDef
ms.assetid: 2ab4681e-0013-4ba0-ba26-50517bbf3f5b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7cca884eae2111a94d87cc24a6d30542148ab845
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394877"
---
# <a name="pidtagfoldertype-canonical-property"></a>Propiedad canónica PidTagFolderType

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene una constante que indica el tipo de carpeta. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_FOLDER_TYPE  <br/> |
|Identificador:  <br/> |0x3601  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Contenedor MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad puede tener exactamente uno de los siguientes valores:
  
FOLDER_GENERIC 
  
> Una carpeta genérica que contiene otras carpetas y mensajes.
    
FOLDER_ROOT 
  
> La carpeta raíz de la tabla de jerarquía de carpeta, es decir, una carpeta que no tiene ninguna carpeta principal.
    
FOLDER_SEARCH 
  
> Una carpeta que contiene los resultados de una búsqueda, en el formulario de vínculos a los mensajes que cumplen los criterios de búsqueda.
    
La raíz de un almacén de mensajes no debe confundirse con la raíz del subárbol de mensajes interpersonales (IPM) de ese almacén. La carpeta del almacén raíz, que no tiene ningún elemento primario, se obtiene llamando al método [IMsgStore::OpenEntry](imsgstore-openentry.md) con un identificador de entrada es nulo. Carpeta raíz del subárbol IPM, que tiene un elemento primario, se obtiene mediante el valor de la propiedad **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) para la llamada **OpenEntry** . 
  
MAPI permite sólo una carpeta raíz por almacén de mensajes. Esta carpeta contiene los mensajes y otras carpetas. Propiedad de **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) de la carpeta raíz contiene el identificador de entrada de la carpeta.
  
La información en una carpeta de resultados de búsqueda se almacena principalmente en su tabla de contenido, que contiene las columnas de una tabla de contenido típico, así como dos columnas adicionales que identifica la carpeta en la que cada mensaje se encontró: **PR_PARENT_DISPLAY** ([ PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (Mostrar nombre, obligatorio) y esta propiedad (identificador de entrada, opcional).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Controla las operaciones de la carpeta.
    
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

