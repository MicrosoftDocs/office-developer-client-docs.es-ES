---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Última modificación: 2012 de julio de 2002'
ms.openlocfilehash: 88716719857cfd623d30a3684fc997ea8019455e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334842"
---
# <a name="feid"></a>FEID

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Identificador de una carpeta. Contiene un identificador de entrada y otra información relevante.
  
## <a name="quick-info"></a>Información rápida

```cpp
struct FEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltid; 
};
```

## <a name="members"></a>Miembros

 _abFlags_
  
> identificador de entrada de 4 bytes para la carpeta. Para obtener más información acerca de los identificadores de entrada MAPI, vea **[EntryID](entryid.md)**. 
    
 _Muid_
  
> GUID que identifica el proveedor de almacenamiento. Consulte mapidefs. h para obtener la definición de tipo de **MAPIUID**. 
    
 _marcador de posición_
  
> Este miembro está reservado para uso interno de Outlook y no es compatible.
    
 _ltid_
  
> IDENTIFICADOR a largo plazo de la carpeta.
    
## <a name="see-also"></a>Vea también



[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[LTID](ltid.md)
  
[UPFLD](upfld.md)
  
[SINCRONIZÁNDOSE](sync.md)

