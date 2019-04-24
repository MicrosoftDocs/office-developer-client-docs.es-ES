---
title: IMAPISupportDoProgressDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoProgressDialog
api_type:
- COM
ms.assetid: 74c52b96-e903-444b-8bda-73a08f278c22
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3de29e9af5caa82d2e57c8fcbbdab7d5ddb19dd9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285209"
---
# <a name="imapisupportdoprogressdialog"></a>IMAPISupport::DoProgressDialog

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recupera un objeto Progress que muestra un indicador de progreso.
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> a Identificador de la ventana primaria del indicador de progreso.
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla cómo el objeto de progreso debe calcular el progreso. Se puede establecer la siguiente marca:
    
MAPI_TOP_LEVEL 
  
> El progreso se calcula para un elemento de nivel superior, como una carpeta principal. El objeto Progress debe usar los valores de los parámetros _ulCount_ y _UlTotal_ del método [método imapiprogress::P rogress](imapiprogress-progress.md) , que indican el elemento actual y el total de los elementos de la operación, respectivamente, para incrementar el progreso. indicador de la operación. 
    
 _lppProgress_
  
> contempla Un puntero a un puntero al objeto Progress.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El objeto de progreso se recuperó correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::D oprogressdialog** se implementa para los objetos de compatibilidad de la libreta de direcciones y del proveedor de almacenamiento de mensajes. Estos proveedores llaman a **DoProgressDialog** para obtener acceso a la implementación MAPI de la interfaz [método imapiprogress](imapiprogressiunknown.md) , que calcula la información de progreso y muestra un cuadro de diálogo estándar. 
  
Para obtener información sobre cómo usar un objeto de progreso y la interfaz **método imapiprogress** , vea [Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).
  
## <a name="see-also"></a>Vea también



[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md)

