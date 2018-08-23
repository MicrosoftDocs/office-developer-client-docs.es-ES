---
title: IMAPIProgressGetMin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetMin
api_type:
- COM
ms.assetid: caceddf1-0f7c-47b5-97bf-17ffe3440a6c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cff866ce73eb6ada45a2b629a6c95c69ad189045
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587827"
---
# <a name="imapiprogressgetmin"></a>IMAPIProgress::GetMin

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve el valor mínimo en el método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) de progreso que se muestra la información. 
  
```cpp
HRESULT GetMin(
  ULONG FAR * lpulMin
);
```

## <a name="parameters"></a>Parámetros

 _lpulMin_
  
> [out] Un puntero al número mínimo de elementos de la operación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se ha recuperado el número mínimo de elementos de la operación.
    
## <a name="remarks"></a>Comentarios

El valor mínimo representa el inicio de la operación con formato numérico. El valor puede ser un valor máximo global, usado para representar el ámbito de la pantalla de progreso todo, o un valor local, que se usa para representar sólo una parte de la pantalla. 
  
El valor de la opción marca determina si el objeto de progreso comprende el valor mínimo para ser local o global. Cuando se establece la marca MAPI_TOP_LEVEL, el valor mínimo se considera que es global y se utiliza para calcular el progreso de toda la operación. Cuando MAPI_TOP_LEVEL no está establecido, el valor mínimo se considera local y proveedores de utilizan internamente para mostrar el progreso de subobjetos de nivel inferiores. Objetos de progreso guardar el valor mínimo local sólo para devolver a un proveedor a través de una llamada **GetMin** . 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Inicializar el valor mínimo en 1. Proveedores de servicios pueden restablecer este valor llamando al método **IMAPIProgress::SetLimits** . Para obtener más información acerca de cómo implementar otros métodos [IMAPIProgress](imapiprogressiunknown.md) y **GetMin** , vea [implementar un indicador de progreso](implementing-a-progress-indicator.md).
  
Para que obtener más información acerca de cómo y cuándo se deben realizar llamadas a un objeto de progreso, vea [Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMin  <br/> |MFCMAPI usa el método **IMAPIProgress::GetMin** para obtener el valor mínimo para el indicador de progreso. Devuelve el valor 1 a menos que se hayan establecido previamente límites llamando al método **IMAPIProgress::SetLimits** .  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)
  
[Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md)
  
[Implementar un indicador de progreso](implementing-a-progress-indicator.md)

