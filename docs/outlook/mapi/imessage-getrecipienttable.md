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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 90ae9cee915296475d7fe64952b40ab7344e89e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817644"
---
# <a name="imessagegetrecipienttable"></a>IMessage::GetRecipientTable

  
  
**Se aplica a**: Outlook 
  
Devuelve la tabla de destinatarios del mensaje.
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Máscara de bits de indicadores que controla la devolución de la tabla. Se pueden establecer los siguientes indicadores:
    
MAPI_DEFERRED_ERRORS 
  
> Permite **GetRecipientTable** devolver de correctamente, posiblemente antes de la tabla es completamente disponible para el cliente de la llamada. Si no está disponible en la tabla, realizar una llamada posterior a él puede provocar un error. 
    
MAPI_UNICODE. 
  
> Columnas de la cadena deben estar en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las columnas de la cadena deben estar en formato ANSI.
    
 _lppTable_
  
> [out] Puntero a un puntero a la tabla de destinatarios.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla de destinatarios se devolvió correctamente.
    
## <a name="remarks"></a>Notas

El método **IMessage::GetRecipientTable** devuelve un puntero a la tabla de destinatarios del mensaje, que incluye información acerca de todos los destinatarios del mensaje. No hay una fila por cada destinatario. 
  
Tablas de destinatarios tienen una columna diferente establecer dependiendo de si se ha enviado el mensaje. Para obtener una lista completa de las columnas de una tabla de destinatarios, vea [Las tablas de destinatario](recipient-tables.md).
  
Algunas tablas de destinatarios de admiten una amplia variedad de restricciones; otros no lo hacen. Compatibilidad con restricciones depende de la implementación del proveedor de almacén de mensajes. 
  
Establecer el indicador MAPI_UNICODE en el parámetro _ulFlags_ afecta a las siguientes llamadas a la tabla de destinatarios: 
  
- [IMAPITable::QueryColumns](imapitable-querycolumns.md) para recuperar el conjunto de columnas. 
    
- [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar las filas. 
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) para recuperar el criterio de ordenación. 
    
Configuración de las solicitudes de marca de Unicode que la información de todas las columnas de cadena devueltos por estas llamadas estar en formato Unicode. Sin embargo, debido a que no todos los proveedores de almacén de mensajes compatible con Unicode, al establecer este indicador es sólo una solicitud.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede cambiar una tabla de destinatario mientras está abierto llamando al método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) . **ModifyRecipients** agrega a destinatarios, elimina a los destinatarios o modifica las propiedades de destinatarios. 
  
## <a name="see-also"></a>Ver también



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPITable:: QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

