---
title: IPSTOVERRIDE1GetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.GetPersistedRegistrations
api_type:
- COM
ms.assetid: 027092f0-f2d6-49e8-a8d0-8926824953a2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 822b4164737aa6010ccce108b544410104ac023d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415134"
---
# <a name="ipstoverride1getpersistedregistrations"></a>IPSTOVERRIDE1::GetPersistedRegistrations

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recupera la lista de registros del archivo Carpetas personales (.pst).
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a>Parameters

 _ppmval_
  
> [in] Puntero a un puntero a una [estructura SPropValue.](spropvalue.md) El miembro ulPropTag de esta estructura es del tipo PT_MV_UNICODE y el miembro de valor MVszW será una matriz de cadenas Unicode terminadas en null. Estas cadenas son rutas de acceso a dll para las que se ha persistente el registro. 
    
> [!NOTE]
> No se implementa la compatibilidad con .pst para ANSI. 
  
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada a la función se ha realizado correctamente.
    
## <a name="see-also"></a>Vea también



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

