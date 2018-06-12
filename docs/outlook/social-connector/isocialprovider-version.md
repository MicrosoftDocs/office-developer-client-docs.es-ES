---
title: ISocialProviderVersion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dfc92878-ab8b-4721-aee8-997c56a8e45b
description: Devuelve un valor de tipo string que representa el número de versión del proveedor para esta red social.
ms.openlocfilehash: 5c82df2dc4c052b1a06bcecb16defbb4dee38b18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821111"
---
# <a name="isocialproviderversion"></a>ISocialProvider::Version

Devuelve un valor de tipo string que representa el número de versión del proveedor para esta red social. 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a>Valor de propiedad

Una cadena que contiene el número de versión del proveedor.
  
## <a name="remarks"></a>Notas

La cadena de versión debe usar el _MajorVersion_. _MinorVersion_ formato (por ejemplo, 1.4730). 
  
## <a name="see-also"></a>Ver también

- [ISocialProvider: IUnknown](isocialprovideriunknown.md)

