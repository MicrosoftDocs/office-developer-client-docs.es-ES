---
title: IMAPIViewAdviseSinkOnPrint
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnPrint
api_type:
- COM
ms.assetid: d16219a0-268c-428d-9f02-4f06eb5b6d7d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 202d461d4acefe18e69b47db9319cb328c61406e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592321"
---
# <a name="imapiviewadvisesinkonprint"></a>IMAPIViewAdviseSink::OnPrint

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Se notifica el Visor de formulario del estado de impresión de un formulario.
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a>Parámetros

 _dwPageNumber_
  
> [entrada] Imprime el número de la última página.
    
 _hrStatus_
  
> [entrada] Valor HRESULT que indica el estado del trabajo de impresión. Los valores posibles son:
    
S_FALSE 
  
> El trabajo de impresión se completó satisfactoriamente.
    
S_OK 
  
> El trabajo de impresión está en curso.
    
NO SE PUDO 
  
> El trabajo de impresión se ha terminado debido a un error.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La notificación se ha realizado correctamente.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el botón Cancelar en un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

Objetos de formulario llamar al método **IMAPIViewAdviseSink::OnPrint** durante la impresión para notificar al Visor de progreso de la impresión. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si el trabajo de impresión implica varias páginas, puede llamar a **OnPrint** después de cada página se imprime. Establezca _dwPageNumber_ a la página que actualmente se está imprimiendo y _hrStatus_ en S_OK. Una vez completado el trabajo de impresión, llame al que conjunto de **OnPrint** con _dwPageNumber_ a la última página impresa y _hrStatus_ se establecen en S_FALSE. 
  
Para obtener más información acerca de las notificaciones de formulario, vea [Enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

