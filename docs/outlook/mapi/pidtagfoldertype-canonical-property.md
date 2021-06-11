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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316320"
---
# <a name="pidtagfoldertype-canonical-property"></a>Propiedad canónica PidTagFolderType

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
  
> Una carpeta genérica que contiene mensajes y otras carpetas.
    
FOLDER_ROOT 
  
> La carpeta raíz de la tabla de jerarquía de carpetas, es decir, una carpeta que no tiene ninguna carpeta primaria.
    
FOLDER_SEARCH 
  
> Carpeta que contiene los resultados de una búsqueda, en forma de vínculos a mensajes que cumplen los criterios de búsqueda.
    
La raíz de un almacén de mensajes no debe confundirse con la raíz del subárbol de mensajes interpersonales (IPM) de ese almacén. La carpeta raíz del almacén, que no tiene ningún elemento primario, se obtiene llamando al método [IMsgStore::OpenEntry](imsgstore-openentry.md) con un identificador de entrada nulo. La carpeta raíz del subárbol IPM, que tiene un elemento primario, se obtiene mediante el valor de la propiedad **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) para la **llamada OpenEntry.** 
  
MAPI solo permite una carpeta raíz por almacén de mensajes. Esta carpeta contiene mensajes y otras carpetas. La propiedad de **PR_PARENT_ENTRYID** raíz ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) contiene el identificador de entrada de la carpeta.
  
La información de una carpeta de resultados de búsqueda se almacena principalmente en su tabla de contenido, que contiene las mismas columnas que una tabla de contenido típica, así como dos columnas adicionales que identifican la carpeta en la que se encontró cada mensaje: **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (nombre para mostrar, obligatorio) y esta propiedad (identificador de entrada, opcional).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Controla las operaciones de carpeta.
    
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

