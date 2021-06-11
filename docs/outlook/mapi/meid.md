---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: a9aea0db700de9c82aa2a41a443ebf03da8ce9b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430311"
---
# <a name="meid"></a>MEID

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Identificador de un Outlook elemento. Contiene un identificador de entrada y otra información relevante.
  
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
  
> Identificador de entrada de 4 bytes para el Outlook elemento. Para obtener más información acerca de los identificadores de entrada MAPI, vea **[ENTRYID](entryid.md)**. 
    
 _muid_
  
> GUID que identifica el proveedor de almacenamiento. Vea mapidefs.h para obtener la definición de tipo **de MAPIUID**. 
    
 _marcador de posición_
  
> Este miembro está reservado para el uso interno de Outlook y no es compatible.
    
 _ltidFld_
  
> Identificador a largo plazo de la carpeta.
    
 _ltidMsg_
  
> Identificador a largo plazo del Outlook elemento.
    
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[LTID](ltid.md)
  
[Sincronizar](sync.md)
  
[UPMSG](upmsg.md)

