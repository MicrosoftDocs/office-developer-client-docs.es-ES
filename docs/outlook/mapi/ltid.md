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
ms.openlocfilehash: 29dd2e3b47d0f43df7824274d2fdcc4f7f16eeb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569858"
---
# <a name="ltid"></a>LTID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="see-also"></a>Recursos adicionales



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[FEID](feid.md)

