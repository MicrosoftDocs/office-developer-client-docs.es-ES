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
ms.openlocfilehash: bbd52116a108be12df7697f45df41b03adeba68e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817387"
---
# <a name="imapiprogressgetmax"></a>IMAPIProgress::GetMax

  
  
**Hace referencia a**: Outlook 
  
Devuelve el número máximo de elementos en la operación de progreso que se muestra la información.
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a>Parámetros

 _lpulMax_
  
> [out] Un puntero al número máximo de elementos de la operación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se ha recuperado el número máximo de elementos de la operación.
    
## <a name="remarks"></a>Comentarios

El valor máximo representa el final de la operación con formato numérico. El valor puede ser un valor máximo global, usado para representar el ámbito de la pantalla de progreso todo, o un valor local, que se usa para representar sólo una parte de la pantalla. 
  
El valor de la opción marca determina si el objeto de progreso comprende el valor máximo para ser local o global. Cuando se establece la marca MAPI_TOP_LEVEL, el valor máximo se considera que es global y se utiliza para calcular el progreso de toda la operación. Cuando MAPI_TOP_LEVEL no está establecida, se considera que el valor máximo es local, y proveedores de usarlo internamente para mostrar progreso para subobjetos de nivel inferiores. Objetos de progreso guardar el valor máximo local sólo para devolver a un proveedor a través de una llamada **GetMax** . 
  
Para que obtener más información acerca de cómo y cuándo se deben realizar llamadas a un objeto de progreso, vea [Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Inicializar el valor máximo en 1000. Proveedores de servicios pueden restablecer este valor llamando al método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) . Para obtener más información acerca de cómo implementar otros métodos [IMAPIProgress](imapiprogressiunknown.md) y **GetMax** , vea [implementar un indicador de progreso](implementing-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMax  <br/> |MFCMAPI usa el método **IMAPIProgress::GetMax** para obtener el valor máximo para el objeto de progreso. Devuelve 1000 a menos que los límites se han establecido previamente con el método **IMAPIProgress::SetLimits** .  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)
  
[Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md)
  
[Implementar un indicador de progreso](implementing-a-progress-indicator.md)

