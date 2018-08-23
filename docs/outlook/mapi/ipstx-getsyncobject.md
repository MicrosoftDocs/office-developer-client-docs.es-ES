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
ms.openlocfilehash: e0e27d86098ec55849fa96cc150c60934ef2810b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585454"
---
# <a name="ipstxgetsyncobject"></a>IPSTX::GetSyncObject

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
  
## <a name="see-also"></a>Recursos adicionales



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetLastError](ipstx-getlasterror.md)

