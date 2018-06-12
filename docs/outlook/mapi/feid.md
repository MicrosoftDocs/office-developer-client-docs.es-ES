---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Última modificación: 02 de julio de 2012'
ms.openlocfilehash: bb2d347d218a7c33a2184bf1fcf181a11fa7d8fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816808"
---
# <a name="feid"></a>FEID

 
  
**Se aplica a**: Outlook 
  
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
  
> identificador de entrada de 4 bytes de la carpeta. Para obtener más información acerca de los identificadores de entrada MAPI, vea la **[propiedad ENTRYID](entryid.md)**. 
    
 _muid_
  
> GUID que identifica el proveedor de almacenamiento. Vea mapidefs.h para la definición de tipo de **MAPIUID**. 
    
 _marcador de posición_
  
> Este miembro está reservado para el uso interno de Outlook y no se admite.
    
 _ltid_
  
> Identificador a largo plazo de la carpeta.
    
## <a name="see-also"></a>Ver también



[Acerca de la máquina de estado de replicación](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[LTID](ltid.md)
  
[UPFLD](upfld.md)
  
[SINCRONIZACIÓN](sync.md)

