---
title: ISocialProviderDefaultSiteUrls
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: Devuelve una matriz de cadenas que especifican las direcciones URL del sitio para el proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: 34d779d5eb42b81a14c5236685104e9ef4fe36f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285859"
---
# <a name="isocialproviderdefaultsiteurls"></a>ISocialProvider::DefaultSiteUrls

Devuelve una matriz de cadenas que especifican las direcciones URL del sitio para el proveedor de Outlook Social Connector (OSC).
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a>Valor de propiedad

Un puntero a una estructura que especifica una matriz de cadenas que representan las direcciones URL del sitio para el proveedor de OSC.
  
## <a name="remarks"></a>Comentarios

Un proveedor puede admitir varias direcciones URL de sitio. El OSC establece la propiedad [ISocialSession:: siteUrl](isocialsession-siteurl.md) para informar al proveedor de la dirección URL del sitio seleccionado. 
  
El OSC utiliza el primer elemento de la matriz como dirección URL predeterminada del sitio. Un proveedor puede devolver elementos adicionales en la matriz de dirección URL del sitio, pero el OSC no las usa. 
  
## <a name="see-also"></a>Vea también

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

