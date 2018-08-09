---
title: ISocialProviderDefaultSiteUrls
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: Devuelve una matriz de cadenas que especifican las direcciones URL de sitio para el proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: a2b2e0397c7c67476ac8067a53e2acbd4eddf270
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821096"
---
# <a name="isocialproviderdefaultsiteurls"></a>ISocialProvider::DefaultSiteUrls

Devuelve una matriz de cadenas que especifican las direcciones URL de sitio para el proveedor de Outlook Social Connector (OSC).
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a>Valor de propiedad

Un puntero a una estructura que especifica una matriz de cadenas que representan direcciones URL de sitio para el proveedor de OSC.
  
## <a name="remarks"></a>Comentarios

Un proveedor puede admitir varias direcciones URL de sitio. El OSC establece la propiedad [ISocialSession::SiteUrl](isocialsession-siteurl.md) para informar al proveedor de la dirección URL de sitio seleccionado. 
  
El OSC utiliza el primer elemento de la matriz como la dirección URL del sitio de forma predeterminada. Un proveedor puede devolver elementos adicionales en la matriz de dirección URL del sitio, pero el OSC no las usa. 
  
## <a name="see-also"></a>Vea también

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

