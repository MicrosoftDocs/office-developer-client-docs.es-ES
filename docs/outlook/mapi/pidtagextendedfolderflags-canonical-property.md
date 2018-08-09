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
ms.openlocfilehash: 4a4d3c940539c23be8ec212cb85e3dd4f3a04aab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819499"
---
# <a name="pidtagextendedfolderflags-canonical-property"></a>Propiedad canónica PidTagExtendedFolderFlags
 
**Hace referencia a**: Outlook 
  
Contiene indicadores extendidas acerca de una carpeta.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_EXTENDED_FOLDER_FLAGS  <br/> |
|Identificador:  <br/> |0x36DA  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Contenedor MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad es una secuencia binaria que contiene propiedades de subcaracterística codificadas para la carpeta. Si tiene un formato como una serie de elementos de sub de longitud variable. Los primeros 8 bits del elemento sub es un campo de identificador, lo que indica el tipo de marca que representa el elemento sub. La segundos 8 bits es el número de bytes de datos que le siguen.
  
Los valores de identificador posibles son:
  
- Invalid
    
   No utilice este valor
    
- ExtendedFlags
    
   Los datos están un valor de cuatro bytes con formato como:
    
   |**Bits**|**Descripción**|
   |:-----|:-----|
   |0-1  <br/> |Reservado.  <br/> |
   |2  <br/> |Se establece en 0 si la aplicación debe mostrar una descripción de la directiva.  <br/> |
   |3-5  <br/> |Reservado.  <br/> |
   |6-7  <br/> |Controla la visualización del número de mensajes en la carpeta.  <br/> 0 - utilizar la configuración predeterminada  <br/> 1: usar el número de mensajes no leídos  <br/> 3 - usar el número total de mensajes  <br/> |
   |8-31  <br/> |Reservado.  <br/> |
   
Artículos reservados pueden omitirse, pero deben conservarse los valores existentes.
    
- SearchFolderID
    
   El campo de datos es un campo de 16 bytes. Cuando la aplicación crea una carpeta de búsqueda persistente, debe establecer este campo en la carpeta en el mismo valor que la **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) una propiedad binaria en el mensaje de la carpeta de búsqueda.
    
- ToDoFolderVersion
    
   El campo de datos es un campo de 4 bytes. Cuando la aplicación crea la carpeta de búsqueda de tareas pendientes, debe establecer el valor de este campo en la carpeta para el valor entero de "little-endian" de "0x000c0000":
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Especifica la ubicación y las propiedades de datos de configuración de cliente y servidor, como las listas de categoría compartida y horas de trabajo.
    
[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para manipular la configuración de la lista de carpetas de búsqueda.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también

- [Propiedades MAPI](mapi-properties.md)
- [Propiedades MAPI canónicas](mapi-canonical-properties.md)
- [Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
- [Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

