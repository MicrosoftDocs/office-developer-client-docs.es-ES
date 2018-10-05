---
title: ISocialProviderLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6356f7bf-e3a1-4294-ad6e-df77bdd0356c
description: Inicializa el proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: 73d14f66785417e80448f622256d0b9cb059b83c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385833"
---
# <a name="isocialproviderload"></a>ISocialProvider::Load

Inicializa el proveedor de Outlook Social Connector (OSC).
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a>Parámetros

_socialProviderInterfaceVersion_
  
> [entrada] La versión de las interfaces de proveedor OSC esperado por el OSC.
    
_languageTag_
  
> [entrada] La etiqueta de idioma de ingeniería de Internet (IETF), definida por [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) y [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt), que representa el idioma de interfaz de usuario de Outlook actual.
    
## <a name="remarks"></a>Comentarios

El formato de versión para el parámetro _socialProviderInterfaceVersion_ es _X_. _xxxx_, donde _X_ es la versión principal y _xxxx_ es la versión secundaria de la OSC. Para Office 2013, compruebe si la versión principal que se va a 15. 
  
## <a name="see-also"></a>Vea también

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

