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
ms.openlocfilehash: 32174e213334d784220b960364443e60db6d1d19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582780"
---
# <a name="imapisupportdoprogressdialog"></a>IMAPISupport::DoProgressDialog

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recupera un objeto de progreso que muestra un indicador de progreso.
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a>Parámetros

 _ulUIParam_
  
> [entrada] Identificador de la ventana principal del indicador de progreso.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo el objeto de progreso debe calcular el progreso. Se puede establecer la marca siguiente:
    
MAPI_TOP_LEVEL 
  
> Progreso se calcula para un elemento de nivel superior, como una carpeta principal. El objeto de progreso debe utilizar los valores de parámetros de _ulCount_ y _ulTotal_ del método [IMAPIProgress::Progress](imapiprogress-progress.md) , que indican el elemento actual y los elementos totales en la operación, respectivamente, para incrementar el progreso indicador para la operación. 
    
 _lppProgress_
  
> [out] Un puntero a un puntero al objeto de progreso.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El objeto de progreso se recuperó correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::DoProgressDialog** se implementa para dirección libreta de direcciones y el mensaje de proveedor compatibilidad con objetos de almacén. Estos proveedores de llamar a **DoProgressDialog** para obtener acceso a la implementación de la interfaz [IMAPIProgress](imapiprogressiunknown.md) , que calcula la información de progreso y muestra un cuadro de diálogo estándar de MAPI. 
  
Para obtener información acerca de cómo usar un objeto de progreso y la interfaz de **IMAPIProgress** , consulte [para mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md)

