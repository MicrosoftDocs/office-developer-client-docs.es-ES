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
ms.openlocfilehash: 56aaf5caf93f90f54d152ab3684ca592cd45cd1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817917"
---
# <a name="ipstoverride1getpersistedregistrations"></a>IPSTOVERRIDE1::GetPersistedRegistrations

  
  
**Hace referencia a**: Outlook 
  
Recupera la lista de registros para el archivo de carpetas personales (.pst).
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a>Parámetros

 _ppmval_
  
> [entrada] Un puntero a un puntero a una estructura [SPropValue](spropvalue.md) . El miembro ulPropTag de esta estructura es del tipo PT_MV_UNICODE, y el miembro de valor MVszW será una matriz de cadenas de Unicode terminada en null. Estas cadenas son las rutas de acceso a los archivos DLL para el que se ha conservado el registro. 
    
> [!NOTE]
> no se implementa la compatibilidad con .pst ANSI. 
  
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada a la función fue correcta.
    
## <a name="see-also"></a>Vea también



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

