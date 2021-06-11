---
title: Propiedad canónica PidTagExtendedFolderFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedFolderFlags
api_type:
- HeaderDef
ms.assetid: e0c04f98-3d66-4ab5-ba05-69f9df539fcf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fe14f6ca101e6a546f99989ecc87b0c516ee5df4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316355"
---
# <a name="pidtagextendedfolderflags-canonical-property"></a>Propiedad canónica PidTagExtendedFolderFlags
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene marcas extendidas acerca de una carpeta.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_EXTENDED_FOLDER_FLAGS  <br/> |
|Identificador:  <br/> |0x36DA  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Contenedor MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad es una secuencia binaria que contiene sub-propiedades codificadas para la carpeta. Tiene el formato de una serie de sub elementos de longitud variable. Los primeros 8 bits del sub elemento son un campo id., que indica qué tipo de marca representa el sub elemento. Los segundos 8 bits son el número de bytes de datos siguientes.
  
Entre los posibles valores de id. se incluyen:
  
- Invalid
    
   No usar este valor
    
- ExtendedFlags
    
   Los datos son un valor de cuatro bytes con el formato siguiente:
    
   |**Bits**|**Descripción**|
   |:-----|:-----|
   |0-1  <br/> |Reservado.  <br/> |
   |2  <br/> |Se establece en 0 si la aplicación debe mostrar una descripción de directiva.  <br/> |
   |3-5  <br/> |Reservado.  <br/> |
   |6-7  <br/> |Controla la visualización del número de mensajes de la carpeta.  <br/> 0: usar la configuración predeterminada  <br/> 1: usar el número de mensajes no leídos  <br/> 3: usar el número total de mensajes  <br/> |
   |8-31  <br/> |Reservado.  <br/> |
   
Los elementos reservados se pueden omitir, pero los valores existentes deben conservarse.
    
- SearchFolderID
    
   El campo de datos es un campo de 16 bytes. Cuando la aplicación crea una carpeta de búsqueda persistente, debe establecer este campo en la carpeta en el mismo valor que la propiedad binaria **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) en el mensaje de carpeta de búsqueda.
    
- ToDoFolderVersion
    
   El campo de datos es un campo de 4 bytes. Cuando la aplicación crea la carpeta de búsqueda para hacer, debe establecer el valor de este campo en la carpeta en el valor entero little-endian de" 0x000c0000":
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Especifica la ubicación y las propiedades de los datos de configuración de cliente y servidor, como listas de categorías compartidas y horas laborables.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones para manipular una configuración de lista de carpetas de búsqueda.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también

- [Propiedades MAPI](mapi-properties.md)
- [Propiedades canónicas MAPI](mapi-canonical-properties.md)
- [Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
- [Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

