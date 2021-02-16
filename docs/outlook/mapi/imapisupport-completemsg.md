---
title: IMAPISupportCompleteMsg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompleteMsg
api_type:
- COM
ms.assetid: e7932433-abe0-4341-95e0-91b37c848145
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e8c52d71ee47966be09c6c0806eceafae0c5ff5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411193"
---
# <a name="imapisupportcompletemsg"></a>IMAPISupport::CompleteMsg

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Realiza el posprocesamiento en un mensaje. 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parámetros

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _cbEntryID_
  
> [entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [entrada] Puntero al identificador de entrada del mensaje que se debe procesar.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El posprocesamiento se ha realizado correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::CompleteMsg** se implementa para los objetos de soporte del proveedor de al almacenamiento de mensajes y solo lo llaman los proveedores de almacenamiento de mensajes estrechamente asociados con los proveedores de transporte. Los proveedores de almacenamiento estrechamente acoplados llaman a **IMAPISupport::CompleteMsg** para indicar a la cola MAPI que postprocese un mensaje. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llame **a CompleteMsg** solo cuando esté estrechamente emparejado con un proveedor de transporte, puede controlar todos los destinatarios del mensaje y existe una de las siguientes condiciones: 
  
- El mensaje se preprocesó.
    
- El mensaje requiere el posprocesamiento mediante la cola MAPI.
    
## <a name="see-also"></a>Consulte también



[IMAPISupport: IUnknown](imapisupportiunknown.md)

