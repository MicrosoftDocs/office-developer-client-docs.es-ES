---
title: IPSTXGetSyncObject
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.GetSyncObject
api_type:
- COM
ms.assetid: b93dae79-4305-9a3a-7b93-42319f7e26ba
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 44261e5ac296004fd113d4c9123b99c482bcb732
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817950"
---
# <a name="ipstxgetsyncobject"></a>IPSTX::GetSyncObject

  
  
**Hace referencia a**: Outlook 
  
Inicia una sesión de sincronización y obtiene la interfaz **[IOSTX](iostxiunknown.md)** asociada. 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a>Parámetros

 _ppostx_
  
>  [out] Puntero a la interfaz **IOSTX** para obtener. 
    
## <a name="remarks"></a>Comentarios

El llamador debe asegurarse de que la misma carpeta no se sincroniza al mismo tiempo en más de un subproceso.
  
## <a name="see-also"></a>Vea también



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetLastError](ipstx-getlasterror.md)

