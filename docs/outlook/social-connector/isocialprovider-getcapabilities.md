---
title: ISocialProviderGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: Obtiene una cadena que describe las capacidades del proveedor.
ms.openlocfilehash: cf3d1418ac0ecbfc3f67bb550a24ec71781f2637
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408106"
---
# <a name="isocialprovidergetcapabilities"></a>ISocialProvider::GetCapabilities

Obtiene una cadena que describe las capacidades del proveedor.
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a>Parameters

_result_
  
> [salida] Una cadena XML que representa las capacidades de un Outlook de Social Connector (OSC).
    
## <a name="remarks"></a>Comentarios

La  _cadena_ XML de resultado devuelta debe cumplir con la definición de esquema del elemento **capabilities,** tal como se define en el esquema XML para la extensibilidad del proveedor de OSC. 
  
El proveedor debe devolver una  _cadena de_ resultados para permitir que las llamadas posteriores desde el OSC al proveedor funcionen correctamente. 
  
## <a name="see-also"></a>Vea también

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

