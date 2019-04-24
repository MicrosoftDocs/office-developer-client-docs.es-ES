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
ms.openlocfilehash: e66315042f8b5cd5aff0e4aa076588c9f312376a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328787"
---
# <a name="imapiviewadvisesinkonprint"></a>IMAPIViewAdviseSink::OnPrint

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Notifica al visor del formulario el estado de impresión de un formulario.
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a>Parameters

 _dwPageNumber_
  
> a Número de la última página impresa.
    
 _hrStatus_
  
> a Valor HRESULT que indica el estado del trabajo de impresión. Los valores posibles son:
    
S_FALSE 
  
> El trabajo de impresión ha finalizado correctamente.
    
S_OK 
  
> El trabajo de impresión está en curso.
    
ERRÓNEA 
  
> El trabajo de impresión se terminó debido a un error.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La notificación se realizó correctamente.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el botón Cancelar en un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

Los objetos de formulario llaman al método **IMAPIViewAdviseSink:: OnPrint** durante la impresión para informar al usuario sobre el progreso de la impresión. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si el trabajo de impresión implica varias páginas, puede llamar a **OnPrint** después de imprimir cada página. Establezca _dwPageNumber_ en la página que se está imprimiendo actualmente y _hrStatus_ en S_OK. Una vez finalizado el trabajo de impresión, llame a **OnPrint** con _dwPageNumber_ establecido en la última página impresa y _hrStatus_ establecido en S_FALSE. 
  
Para obtener más información acerca de las notificaciones de formulario, vea [enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Vea también



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

