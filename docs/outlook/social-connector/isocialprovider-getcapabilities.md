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
ms.openlocfilehash: 54e28f22f2dc8fdbe19821d8188087b78c327518
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821106"
---
# <a name="isocialprovidergetcapabilities"></a>ISocialProvider::GetCapabilities

Obtiene una cadena que describe las capacidades del proveedor.
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a>Sintaxis

_resultado_
  
> [out] Una cadena XML que representa las funciones de un proveedor de Outlook Social Connector (OSC).
    
## <a name="remarks"></a>Notas

La cadena XML devuelto _resultados_ debe cumplir con la definición del esquema para el elemento **capabilities** , tal como se define en el esquema XML de extensibilidad de proveedores OSC. 
  
El proveedor debe devolver una cadena de _resultado_ para habilitar las llamadas subsiguientes desde el OSC para el proveedor funcionar correctamente. 
  
## <a name="see-also"></a>Ver también

- [ISocialProvider: IUnknown](isocialprovideriunknown.md)

