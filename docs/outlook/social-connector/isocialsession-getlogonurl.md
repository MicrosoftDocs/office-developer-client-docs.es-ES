---
title: ISocialSessionGetLogonUrl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Obtiene un valor de tipo string que representa una dirección URL que se usa para presentar un formulario basado en explorador al usuario durante la autenticación web.
ms.openlocfilehash: 343919f194b238fc519bb8f6d808b44a8ab6e7b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821113"
---
# <a name="isocialsessiongetlogonurl"></a>ISocialSession::GetLogonUrl

Obtiene un valor de tipo string que representa una dirección URL que se usa para presentar un formulario basado en explorador al usuario durante la autenticación web.
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a>Sintaxis

_url_
  
> [out] Una cadena que contiene una dirección URL para el formulario usado en la autenticación web.
    
## <a name="remarks"></a>Notas

Después de que el formulario se presenta al usuario, se llama al método de [ISocialSession::LogonWeb](isocialsession-logonweb.md) con una cadena vacía para el parámetro de _configuración_ . 
  
## <a name="see-also"></a>Ver también

- [ISocialSession: IUnknown](isocialsessioniunknown.md)

