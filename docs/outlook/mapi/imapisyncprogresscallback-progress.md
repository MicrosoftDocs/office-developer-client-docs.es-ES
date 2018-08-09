---
title: IMAPISyncProgressCallbackProgress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Progress
api_type:
- COM
ms.assetid: 6797cd1c-8a0b-4f42-ba56-6162d8e7b058
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 12624ef6212f9113041bf5cf3a82e2b7df6eca9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817559"
---
# <a name="imapisyncprogresscallbackprogress"></a>IMAPISyncProgressCallback::Progress

  
  
**Hace referencia a**: Outlook 
  
Actualiza el estado en el cuadro de diálogo de envío o recepción. El proveedor de almacenamiento periódicamente llama a esta función.
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a>Parámetros

 **pwczsProgress**
  
> Un puntero a una cadena que muestra el paso de progreso actual. Puede ser NULL para actualizar el progreso.
    
 **ulIndex**
  
> La posición actual en curso.
    
 **ulIndexMax**
  
> El índice que indica el progreso completado.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="see-also"></a>Vea también



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

