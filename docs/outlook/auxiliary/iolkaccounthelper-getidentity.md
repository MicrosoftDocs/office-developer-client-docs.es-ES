---
title: IOlkAccountHelperGetIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea8b8f02-959f-cd71-9cfe-5ebdf4bae2bc
description: Obtiene el nombre de perfil de una cuenta.
ms.openlocfilehash: d725f309a29b026395e2795a49d31b45a4a49562
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322109"
---
# <a name="iolkaccounthelpergetidentity"></a>IOlkAccountHelper::GetIdentity

Obtiene el nombre de perfil de una cuenta.
  
## <a name="quick-info"></a>Información rápida

Vea [IOlkAccountHelper](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::GetIdentity (  
    LPWSTR pwszIdentity, 
    DWORD *pcch 
);
```

## <a name="parameters"></a>Parameters

_pwszIdentity_
  
> [in] [salida] Nombre del perfil.
    
_pcch_
  
> [in] [salida] Al llamar a este método, contiene el tamaño (en número de caracteres) de  _pwszIdentity_ que se ha asignado. Al devolver, contiene la longitud real, incluido el carácter de 0 terminación, del nombre del perfil devuelto. 
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
|E_OUTOFMEMORY  <br/> |El nombre del perfil devuelto es mayor que el tamaño de  _pwszIdentity_.  <br/> |
|E_INVALIDARG  <br/> | _pcch_ es NULL.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si  _pwszIdentity_ es demasiado pequeño para contener el nombre del perfil, no se establecerá en la devolución y  _pcch_ señalará el tamaño necesario para  _pwszIdentity_.
  
## <a name="see-also"></a>Vea también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md)
- [PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)

