---
title: Propiedad canónica PidTagConflictItems
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConflictItems
api_type:
- HeaderDef
ms.assetid: 0d147827-f0e2-dcc1-4427-c4a2f48ca801
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3ff428d96de40e70e63659c5a3e5fa1c7cf0d564
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569116"
---
# <a name="pidtagconflictitems-canonical-property"></a>Propiedad canónica PidTagConflictItems

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene la entrada de uno o varios identificadores de elementos que han participado en una resolución automática de conflictos.
  
## 

|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONFLICT_ITEMS  <br/> |
|Identificador:  <br/> |0x1098  <br/> |
|Tipo de propiedad:  <br/> |PT_MV_BINARY  <br/> |
|Área:  <br/> |ICS  <br/> |
   
## <a name="remarks"></a>Comentarios

Los tipos de elementos estándar de Microsoft Outlook que admiten la resolución de conflictos automática incluyen los siguientes tipos de elemento estándar: elementos de cita, elementos de contactos, los elementos del diario, elementos de correo, convocatorias de reunión, elementos de notas rápidas y elementos de tarea. Un elemento que pertenecen a una clase de mensaje que se deriva de uno de estos tipos de elementos estándar también es compatible con la resolución de conflictos automática. En Microsoft Outlook 2003 y Microsoft Office Outlook 2007, cuando Outlook sincroniza los elementos y se considera que existe la posibilidad de que la copia resultante no puede contener todos los datos esenciales, Outlook almacena las copias en conflicto en los **conflictos** carpeta, bajo la carpeta **Problemas de sincronización** . 
  
> [!NOTE]
> **Problemas de sincronización** y sus subcarpetas están ocultos hasta que haga clic en **Lista de carpetas** en el menú **Ir** . 
  
Un elemento expone la propiedad **PR_CONFLICT_ITEMS** si es uno de los tipos de elemento que admiten la resolución de conflictos automática, se obtuvo en una resolución de conflictos o se ha puesto en la carpeta **conflictos** debido a una resolución de conflictos. La carpeta en la que se coloca el elemento determina el contenido de **PR_CONFLICT_ITEMS**. Si el elemento se encuentra en alguna carpeta que no sea la carpeta **conflictos** y el elemento expone la propiedad **PR_CONFLICT_ITEMS** , el elemento debe ha obtenido la resolución de conflictos y **PR_CONFLICT_ITEMS** va a contener uno o varios identificadores de entrada de los elementos que se perdió en la resolución de conflictos. Si el elemento se encuentra en la carpeta **conflictos** y el elemento expone la propiedad **PR_CONFLICT_ITEMS** , este elemento debe ha perdido la resolución de conflictos y **PR_CONFLICT_ITEMS** va a contener el identificador de entrada del elemento que obtuvo en el conflicto resolución. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla la sincronización de datos de objeto mensajería entre un servidor y un cliente.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Información sobre las adiciones de MAPI](about-mapi-additions.md)
  
[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

