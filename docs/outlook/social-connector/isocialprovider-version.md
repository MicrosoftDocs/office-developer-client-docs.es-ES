---
title: ISocialProviderVersion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dfc92878-ab8b-4721-aee8-997c56a8e45b
description: Devuelve una cadena que representa el número de versión del proveedor de esta red social.
ms.openlocfilehash: 0749b8fb83a11328233442b79e1f9de50076effe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285388"
---
# <a name="isocialproviderversion"></a>ISocialProvider::Version

Devuelve una cadena que representa el número de versión del proveedor de esta red social. 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a>Valor de propiedad

Una cadena que contiene el número de versión del proveedor.
  
## <a name="remarks"></a>Comentarios

La cadena de versión debe usar _MajorVersion_. _MinorVersion_ formato (por ejemplo, 1,4730). 
  
## <a name="see-also"></a>Vea también

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

