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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432586"
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

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Identificador de la ventana principal del indicador de progreso.
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo debe calcularse el progreso el objeto de progreso. Se puede establecer la siguiente marca:
    
MAPI_TOP_LEVEL 
  
> El progreso se calcula para un elemento de nivel superior, como una carpeta primaria. El objeto progress debe usar los valores de los parámetros _ulCount_ y _ulTotal_ del método [IMAPIProgress::P rogress,](imapiprogress-progress.md) que indican el elemento actual y el total de elementos de la operación, respectivamente, para incrementar el indicador de progreso de la operación. 
    
 _lppProgress_
  
> [salida] Puntero a un puntero al objeto de progreso.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El objeto progress se recuperó correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::D oProgressDialog** se implementa para objetos de soporte del proveedor de libreta de direcciones y almacén de mensajes. Estos proveedores llaman a **DoProgressDialog** para obtener acceso a la implementación MAPI de la interfaz [IMAPIProgress,](imapiprogressiunknown.md) que calcula la información de progreso y muestra un cuadro de diálogo estándar. 
  
Para obtener información sobre cómo usar un objeto de progreso y la interfaz **IMAPIProgress,** vea [Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).
  
## <a name="see-also"></a>Vea también



[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md)

