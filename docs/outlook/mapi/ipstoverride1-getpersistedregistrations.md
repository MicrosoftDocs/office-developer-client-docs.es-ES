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
ms.openlocfilehash: 548ec33e39e181aba8a72b5325f3f426b9d51762
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575871"
---
# <a name="ipstoverride1getpersistedregistrations"></a>IPSTOVERRIDE1::GetPersistedRegistrations

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="see-also"></a>Recursos adicionales



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

