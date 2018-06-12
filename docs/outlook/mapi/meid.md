---
title: MEID.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Última modificación: 03 de julio de 2012'
ms.openlocfilehash: 1b725dc5151f1f088f2547a1ef82d322c8458b6e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818412"
---
# <a name="meid"></a>MEID.

 
  
**Se aplica a**: Outlook 
  
Identificador de un elemento de Outlook. Contiene un identificador de entrada y otra información relevante.
  
## <a name="quick-info"></a>Información rápida

```cpp
struct MEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltidFld; 
    LTID ltidMsg; 
};
```

## <a name="members"></a>Miembros

 _abFlags_
  
> identificador de entrada de 4 bytes para el elemento de Outlook. Para obtener más información acerca de los identificadores de entrada MAPI, vea la **[propiedad ENTRYID](entryid.md)**. 
    
 _muid_
  
> GUID que identifica el proveedor de almacenamiento. Vea mapidefs.h para la definición de tipo de **MAPIUID**. 
    
 _marcador de posición_
  
> Este miembro está reservado para el uso interno de Outlook y no se admite.
    
 _ltidFld_
  
> Identificador a largo plazo de la carpeta.
    
 _ltidMsg_
  
> Identificador a largo plazo del elemento de Outlook.
    
## <a name="see-also"></a>Ver también



[Acerca de la API de replicación](about-the-replication-api.md)
  
[Acerca de la máquina de estado de replicación](about-the-replication-state-machine.md)
  
[LTID](ltid.md)
  
[SINCRONIZACIÓN](sync.md)
  
[UPMSG](upmsg.md)

