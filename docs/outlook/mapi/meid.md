---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Última modificación: 03 de julio de 2012'
ms.openlocfilehash: 24cc4b00f02c61395565fb7ddeb6a5b5a62afdc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591943"
---
# <a name="meid"></a>MEID

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>Members

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
    
## <a name="see-also"></a>Recursos adicionales



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[LTID](ltid.md)
  
[SYNC](sync.md)
  
[UPMSG](upmsg.md)

