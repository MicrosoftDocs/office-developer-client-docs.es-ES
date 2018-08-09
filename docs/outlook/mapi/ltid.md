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
ms.openlocfilehash: 4a60e2fe3a58e1d696ae9645e03ce8dde5340d9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818040"
---
# <a name="ltid"></a>LTID

  
  
**Hace referencia a**: Outlook 
  
Largo términos identificador genérico de un objeto en un almacén de Outlook.
  
## <a name="quick-info"></a>Información rápida

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a>Members

 _guid_
  
- [out] El GUID del servidor que creó el objeto.
    
 _globcnt_
  
- [out] Número único de 6 bytes que identifica el objeto en el almacén de Outlook.
    
 _wLevel_
  
- [out] El nivel de la jerarquía del identificador de entrada para una carpeta pública Favoritos de Exchange.
    
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[FEID](feid.md)

