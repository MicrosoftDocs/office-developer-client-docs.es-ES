---
title: ISocialProviderDefaultSiteUrls
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: Devuelve una matriz de cadenas que especifican direcciones URL de sitio para el Outlook social Connector (OSC).
ms.openlocfilehash: 34d779d5eb42b81a14c5236685104e9ef4fe36f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413776"
---
# <a name="isocialproviderdefaultsiteurls"></a>ISocialProvider::DefaultSiteUrls

Devuelve una matriz de cadenas que especifican direcciones URL de sitio para el Outlook social Connector (OSC).
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a>Valor de propiedad

Puntero a una estructura que especifica una matriz de cadenas que representan direcciones URL de sitio para el proveedor de OSC.
  
## <a name="remarks"></a>Comentarios

Un proveedor puede admitir varias direcciones URL de sitio. El OSC establece la [propiedad ISocialSession::SiteUrl](isocialsession-siteurl.md) para informar al proveedor de la dirección URL del sitio seleccionado. 
  
El OSC usa el primer elemento de la matriz como la dirección URL del sitio predeterminada. Un proveedor puede devolver elementos adicionales en la matriz de direcciones URL del sitio, pero el OSC no los usa. 
  
## <a name="see-also"></a>Vea también

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

