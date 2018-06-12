---
title: ISocialProviderSocialNetworkName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96f32db2-d654-4e72-88d1-ef955e3ff42b
description: Devuelve un valor de tipo string que representa el nombre de redes sociales.
ms.openlocfilehash: 78424db0940b2c23914355b2b20ba5bc531ad3ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821110"
---
# <a name="isocialprovidersocialnetworkname"></a>ISocialProvider::SocialNetworkName

Devuelve un valor de tipo string que representa el nombre de redes sociales. 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkName([out, retval] BSTR* networkName);
```

## <a name="property-value"></a>Valor de propiedad

Una cadena que contiene el nombre de redes sociales.
  
## <a name="remarks"></a>Notas

Proveedores de Outlook Social Connector (OSC) deben localizar el nombre de redes sociales.
  
## <a name="see-also"></a>Ver también

- [ISocialProvider: IUnknown](isocialprovideriunknown.md)

