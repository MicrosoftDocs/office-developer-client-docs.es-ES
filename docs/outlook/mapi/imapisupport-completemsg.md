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
ms.openlocfilehash: a948c8c25eec9b31735bb34b91e2dec4bca5fcfc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583452"
---
# <a name="imapisupportcompletemsg"></a>IMAPISupport::CompleteMsg

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Realiza procesamiento posterior en un mensaje. 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _cbEntryID_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada del mensaje para procesar.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El procesamiento posterior realizada correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::CompleteMsg** se implementa para objetos de soporte técnico de proveedor de almacén de mensajes y se denomina sólo por los proveedores de almacén de mensajes que estén asociados estrechamente con los proveedores de transporte. Los proveedores de almacén acoplado llame a **IMAPISupport::CompleteMsg** para indicar a la cola MAPI para postprocess un mensaje. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llamar a **CompleteMsg** sólo cuando estrechamente con un proveedor de transporte, puede administrar todos los destinatarios del mensaje y da alguna de las siguientes condiciones: 
  
- El mensaje se preprocesa.
    
- El mensaje requiere procesamiento posterior por la cola de MAPI.
    
## <a name="see-also"></a>Recursos adicionales



[IMAPISupport: IUnknown](imapisupportiunknown.md)

