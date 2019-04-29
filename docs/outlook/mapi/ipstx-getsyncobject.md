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
ms.openlocfilehash: 31ef1f5c6af498f042ab766ae90fcfbce805700a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407112"
---
# <a name="ipstxgetsyncobject"></a>IPSTX::GetSyncObject

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Inicia una sesión de sincronización y obtiene la interfaz **[IOSTX](iostxiunknown.md)** asociada. 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a>Parameters

 _ppostx_
  
>  contempla Puntero a la interfaz **IOSTX** que se va a obtener. 
    
## <a name="remarks"></a>Comentarios

El autor de la llamada debe asegurarse de que la misma carpeta no esté sincronizada al mismo tiempo en más de un subproceso.
  
## <a name="see-also"></a>Ver también



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetLastError](ipstx-getlasterror.md)

