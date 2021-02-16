---
title: IMessageGetRecipientTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetRecipientTable
api_type:
- COM
ms.assetid: a335dfca-44da-452e-b16f-25d314b1758f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ca42e91528cdb7e61ae3620989c4a89966db1061
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424612"
---
# <a name="imessagegetrecipienttable"></a>IMessage::GetRecipientTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve la tabla de destinatarios del mensaje.
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parámetros

 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla la devolución de la tabla. Se pueden establecer las siguientes marcas:
    
MAPI_DEFERRED_ERRORS 
  
> Permite **que GetRecipientTable** vuelva correctamente, posiblemente antes de que la tabla esté totalmente disponible para el cliente que realiza la llamada. Si la tabla no está disponible, realizar una llamada posterior a ella puede provocar un error. 
    
MAPI_UNICODE 
  
> Las columnas de cadena deben estar en formato Unicode. Si no MAPI_UNICODE marca, las columnas de cadena deben estar en formato ANSI.
    
 _lppTable_
  
> [salida] Puntero a un puntero a la tabla de destinatarios.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla de destinatarios se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMessage::GetRecipientTable** devuelve un puntero a la tabla de destinatarios del mensaje, que incluye información sobre todos los destinatarios del mensaje. Hay una fila para cada destinatario. 
  
Las tablas de destinatarios tienen un conjunto de columnas diferente en función de si se ha enviado el mensaje. Para obtener una lista completa de las columnas de una tabla de destinatarios, vea [Tablas de destinatarios](recipient-tables.md).
  
Algunas tablas de destinatarios admiten una amplia variedad de restricciones; otros no lo hacen. La compatibilidad con restricciones depende de la implementación del proveedor de almacenamiento de mensajes. 
  
Establecer el MAPI_UNICODE en el  _parámetro ulFlags_ afecta a las siguientes llamadas a la tabla de destinatarios: 
  
- [IMAPITable::QueryColumns](imapitable-querycolumns.md) para recuperar el conjunto de columnas. 
    
- [IMAPITable::QueryRows](imapitable-queryrows.md) para recuperar filas. 
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) para recuperar el criterio de ordenación. 
    
Al establecer la marca Unicode, se solicita que la información de las columnas de cadena devueltas por estas llamadas esté en formato Unicode. Sin embargo, dado que no todos los proveedores de al almacenamiento de mensajes admiten Unicode, establecer esta marca es solo una solicitud.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede cambiar una tabla de destinatarios mientras está abierta llamando al método [IMessage::ModifyRecipients.](imessage-modifyrecipients.md) **ModifyRecipients** agrega destinatarios, elimina destinatarios o modifica las propiedades del destinatario. 
  
## <a name="see-also"></a>Consulte también



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

