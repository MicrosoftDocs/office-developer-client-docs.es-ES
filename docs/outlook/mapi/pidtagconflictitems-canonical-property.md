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
ms.openlocfilehash: 83940d9239bc172d5fab76232f6644f0e89033b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338020"
---
# <a name="pidtagconflictitems-canonical-property"></a>Propiedad canónica PidTagConflictItems

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene uno o más identificadores de entrada de elementos que han participado en una resolución automática de conflictos.
  
## 

|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONFLICT_ITEMS  <br/> |
|Identificador:  <br/> |0x1098  <br/> |
|Tipo de propiedad:  <br/> |PT_MV_BINARY  <br/> |
|Área:  <br/> |ICS  <br/> |
   
## <a name="remarks"></a>Comentarios

Los tipos de elementos estándar de Microsoft Outlook que admiten la resolución automática de conflictos incluyen los siguientes tipos de elementos estándar: elementos de cita, elementos de contacto, elementos de diario, elementos de correo, elementos de reunión, elementos de notas adhesivas y elementos de tareas. Un elemento que pertenece a una clase de mensaje que deriva de uno de estos tipos de elementos estándar también admite la resolución automática de conflictos. En Microsoft Outlook 2003 y Microsoft Office Outlook 2007, cuando Outlook sincroniza elementos y considera que existe la posibilidad de que la copia resultante no contenga todos los datos esenciales, Outlook  almacena las copias en conflicto en la carpeta **Conflictos,** en la carpeta Problemas de sincronización. 
  
> [!NOTE]
> **Los problemas de** sincronización y sus subcarpetas están ocultos hasta que haga clic en **Lista de carpetas** en el **menú** Ir. 
  
Un elemento expone la propiedad **PR_CONFLICT_ITEMS** si es uno de los tipos de elementos que admiten la resolución automática de conflictos, si ha ganado en una resolución de conflictos o si se ha colocado en la carpeta Conflictos debido a una resolución de **conflictos.** La carpeta en la que se coloca el elemento determina el contenido de **PR_CONFLICT_ITEMS**. Si el elemento se encuentra en alguna carpeta que no sea la carpeta **Conflictos** y el elemento expone la propiedad **PR_CONFLICT_ITEMS,** el elemento debe haber ganado la resolución de conflictos y **PR_CONFLICT_ITEMS** contendrá uno o más identificadores de entrada de los elementos que se perdieron en la resolución de conflictos. Si el elemento se encuentra en la carpeta **Conflictos** y el elemento expone la propiedad **PR_CONFLICT_ITEMS,** este elemento debe haber perdido la resolución de conflictos y **PR_CONFLICT_ITEMS** contendrá el identificador de entrada del elemento que obtuvo la resolución de conflictos. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla la sincronización de datos de objetos de mensajería entre un servidor y un cliente.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Acerca de las adiciones de MAPI](about-mapi-additions.md)
  
[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

