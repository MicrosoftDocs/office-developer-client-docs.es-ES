---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2ea877c9328279322de0f15e5755096e74819425
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357417"
---
# <a name="ltid"></a>LTID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
IDENTIFICADOR de término largo genérico de un objeto en un almacén de Outlook.
  
## <a name="quick-info"></a>Información rápida

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a>Miembros

 _guid_
  
- contempla GUID del servidor que creó el objeto.
    
 _globcnt_
  
- contempla Un número único de 6 bytes que identifica el objeto en el almacén de Outlook.
    
 _wLevel_
  
- contempla El nivel de jerarquía del identificador de entrada de una carpeta pública favorita de Exchange.
    
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[FEID](feid.md)

