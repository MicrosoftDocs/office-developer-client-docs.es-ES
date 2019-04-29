---
title: ISocialSessionGetLogonUrl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Obtiene una cadena que representa una dirección URL que se usa para presentar un formulario basado en el explorador al usuario durante la autenticación Web.
ms.openlocfilehash: 83867282922ea136b9673609cc2ba2f1a206f6ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427916"
---
# <a name="isocialsessiongetlogonurl"></a>ISocialSession::GetLogonUrl

Obtiene una cadena que representa una dirección URL que se usa para presentar un formulario basado en el explorador al usuario durante la autenticación Web.
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a>Parameters

_url_
  
> contempla Una cadena que contiene una dirección URL para el formulario usado en la autenticación Web.
    
## <a name="remarks"></a>Comentarios

Una vez que el formulario se presenta al usuario, se llama al método [ISocialSession:: LogonWeb](isocialsession-logonweb.md) con una cadena vacía para __ el parámetro connecten. 
  
## <a name="see-also"></a>Ver también

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

