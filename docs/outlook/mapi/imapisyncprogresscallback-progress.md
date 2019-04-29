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
ms.openlocfilehash: 9b44337a4bc9615558ac6337e99ea206ba063b1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429113"
---
# <a name="imapisyncprogresscallbackprogress"></a>IMAPISyncProgressCallback::Progress

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Actualiza el estado en el cuadro de diálogo de envío y recepción. El proveedor de almacén llama periódicamente a esta función.
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a>Parameters

 **pwczsProgress**
  
> Un puntero a una cadena que muestra el paso de progreso actual. Puede ser NULL para actualizar el progreso.
    
 **ulIndex**
  
> Posición actual en curso.
    
 **ulIndexMax**
  
> Índice que indica el progreso total.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="see-also"></a>Ver también



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

