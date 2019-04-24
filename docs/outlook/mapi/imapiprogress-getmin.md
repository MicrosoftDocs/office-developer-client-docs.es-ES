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
ms.openlocfilehash: 6cd31f8ac713c21053db7ef461220a360ebeec74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331685"
---
# <a name="imapiprogressgetmin"></a>IMAPIProgress::GetMin

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Devuelve el valor mínimo del método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) para el que se muestra información de progreso. 
  
```cpp
HRESULT GetMin(
  ULONG FAR * lpulMin
);
```

## <a name="parameters"></a>Parámetros

 _lpulMin_
  
> [salida] Un puntero al número mínimo de elementos de la operación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El número mínimo de elementos de la operación que se ha recuperado.
    
## <a name="remarks"></a>Comentarios

El valor mínimo representa el inicio de la operación en formato numérico. El valor puede ser un valor máximo global, usado para representar el ámbito de la pantalla de progreso total, o un valor local, para representar únicamente una parte de la pantalla. 
  
El valor de la configuración de la etiqueta determina si el objeto de progreso comprende el valor mínimo local o global. Cuando se establece la etiqueta MAPI_TOP_LEVEL, el valor mínimo se considera global y se usa para calcular el progreso de toda la operación. Cuando no se establece MAPI_TOP_LEVEL, el valor mínimo se considera local y los proveedores lo usan internamente para mostrar el progreso de objetos secundarios de nivel inferior. Los objetos de progreso guardan el valor mínimo local solo para devolverlo a un proveedor a través de una llamada **GetMin**. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Inicialice el valor mínimo en 1. Los proveedores de servicios pueden restablecer este valor llamando al método **IMAPIProgress::SetLimits**. Para obtener más información sobre cómo implementar **GetMin** y otros métodos [IMAPIProgress](imapiprogressiunknown.md), vea [Implementar un indicador de progreso](implementing-a-progress-indicator.md).
  
Para obtener más información sobre cómo y cuándo debe realizar llamadas a un objeto de progreso, vea [Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMin  <br/> |MFCMAPI usa el método **IMAPIProgress::GetMin** para obtener el valor mínimo para el indicador de progreso. Devuelve el valor 1 a menos que se hayan establecido límites anteriormente llamando al método **IMAPIProgress::SetLimits**.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md)
  
[Implementar un indicador de progreso](implementing-a-progress-indicator.md)

