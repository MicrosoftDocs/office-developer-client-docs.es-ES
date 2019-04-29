---
title: ISocialProviderGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: Obtiene una cadena que describe las funciones del proveedor.
ms.openlocfilehash: cf3d1418ac0ecbfc3f67bb550a24ec71781f2637
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408106"
---
# <a name="isocialprovidergetcapabilities"></a>ISocialProvider::GetCapabilities

Obtiene una cadena que describe las funciones del proveedor.
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a>Parameters

_result_
  
> contempla Cadena XML que representa las funciones de un proveedor de Outlook Social Connector (OSC).
    
## <a name="remarks"></a>Comentarios

La cadena XML de _resultado_ devuelta debe cumplir con la definición de esquema del elemento **Capabilities** , tal como se define en el esquema XML de la extensibilidad del proveedor OSC. 
  
El proveedor debe devolver una cadena de _resultado_ para permitir llamadas posteriores desde el OSC al proveedor para que funcionen correctamente. 
  
## <a name="see-also"></a>Vea también

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

