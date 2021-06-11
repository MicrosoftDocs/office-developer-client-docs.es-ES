---
title: IMAPIProgressGetMax
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetMax
api_type:
- COM
ms.assetid: 88a910ed-b55a-4e5b-a43d-eb3ea795a70e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 64b6235151c7700a24992bc1d4394553a53c0464
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436205"
---
# <a name="imapiprogressgetmax"></a>IMAPIProgress::GetMax

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve el número máximo de elementos de la operación para los que se muestra información de progreso.
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a>Parameters

 _lpulMax_
  
> [salida] Puntero al número máximo de elementos de la operación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se ha recuperado el número máximo de elementos de la operación.
    
## <a name="remarks"></a>Comentarios

El valor máximo representa el final de la operación en forma numérica. El valor puede ser un valor máximo global, usado para representar el ámbito de la pantalla de progreso total, o un valor local, para representar únicamente una parte de la pantalla. 
  
El valor de la configuración de marca afecta a si el objeto de progreso entiende que el valor máximo sea local o global. Cuando se MAPI_TOP_LEVEL marca, el valor máximo se considera global y se usa para calcular el progreso de toda la operación. Cuando MAPI_TOP_LEVEL no se establece, el valor máximo se considera local y los proveedores lo usan internamente para mostrar el progreso de los subobjetos de nivel inferior. Los objetos Progress guardan el valor máximo local solo para devolverlo a un proveedor a través de una **llamada GetMax.** 
  
Para obtener más información sobre cómo y cuándo debe realizar llamadas a un objeto de progreso, vea [Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Inicialice el valor máximo en 1000. Los proveedores de servicios pueden restablecer este valor llamando al método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md). Para obtener más información acerca de cómo implementar **GetMax** y los demás [métodos IMAPIProgress,](imapiprogressiunknown.md) vea [Implementing a Progress Indicator](implementing-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMax  <br/> |MFCMAPI usa el **método IMAPIProgress::GetMax** para obtener el valor máximo del objeto de progreso. Devuelve 1000 a menos que se hayan establecido anteriormente límites con el método **IMAPIProgress::SetLimits.**  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md)
  
[Implementar un indicador de progreso](implementing-a-progress-indicator.md)

