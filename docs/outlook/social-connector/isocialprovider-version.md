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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438277"
---
# <a name="isocialproviderversion"></a>ISocialProvider::Version

Devuelve una cadena que representa el número de versión del proveedor de esta red social. 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a>Valor de propiedad

Cadena que contiene el número de versión del proveedor.
  
## <a name="remarks"></a>Comentarios

La cadena de versión debe usar  _majorversion_. _Formato MinorVersion_ (por ejemplo, 1.4730). 
  
## <a name="see-also"></a>Vea también

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

