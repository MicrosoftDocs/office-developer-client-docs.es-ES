---
title: ISocialProviderSocialNetworkIcon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b51675f-77b7-4df0-8496-b1e8958c6544
description: Devuelve una matriz de bytes que representa el icono de la red social.
ms.openlocfilehash: c63d9996d4478c8ce7e46210aae34791bcfe9222
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438690"
---
# <a name="isocialprovidersocialnetworkicon"></a>ISocialProvider::SocialNetworkIcon

Devuelve una matriz de bytes que representa el icono de la red social. 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkIcon([out, retval] SAFEARRAY(unsigned char)* networkIcon);
```

## <a name="property-value"></a>Valor de propiedad

Puntero a una estructura que especifica una matriz de bytes que contiene el icono de la red social.
  
## <a name="remarks"></a>Comentarios

Los recursos de imagen admitidos son formatos .bmp, .jpeg y .png.
  
## <a name="see-also"></a>Vea también

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

