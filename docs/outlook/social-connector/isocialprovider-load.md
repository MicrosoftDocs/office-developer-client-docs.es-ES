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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285766"
---
# <a name="isocialproviderload"></a>ISocialProvider::Load

Inicializa el proveedor de Outlook Social Connector (OSC).
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a>Parameters

_socialProviderInterfaceVersion_
  
> a La versión de las interfaces del proveedor OSC que esperaba el OSC.
    
_languageTag_
  
> a La etiqueta de idioma del Departamento de tareas de ingeniería de Internet (IETF), definida por [[rfc4646]](https://www.ietf.org/rfc/rfc4646.txt) y [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt), que representa el idioma actual de la interfaz de usuario de Outlook.
    
## <a name="remarks"></a>Comentarios

El formato de la versión para el parámetro _socialProviderInterfaceVersion_ es _X_. _xxxx_, donde _X_ es la versión principal y _xxxx_ es la versión secundaria del OSC. Para Office 2013, compruebe si la versión principal es 15. 
  
## <a name="see-also"></a>Vea también

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

