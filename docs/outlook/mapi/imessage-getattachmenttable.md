---
title: IMessageGetAttachmentTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetAttachmentTable
api_type:
- COM
ms.assetid: e568917e-6085-4094-8728-89ba90a78c40
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bf100ed916080a91366062f45b9e3349516bdb98
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588520"
---
# <a name="imessagegetattachmenttable"></a>IMessage::GetAttachmentTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve la tabla de datos adjuntos del mensaje.
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Máscara de bits de marcadores que se relacionan con la creación de la tabla. Se puede establecer la marca siguiente: 
    
MAPI_UNICODE. 
  
> Las columnas de cadena se encuentran en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las columnas de cadena están en formato ANSI.
    
MAPI_DEFERRED_ERRORS 
  
> Permite **GetAttachmentTable** devolver de correctamente, posiblemente antes de la tabla es completamente disponible para el cliente de la llamada. Si no está disponible en la tabla, realizar una llamada posterior a él puede provocar un error. 
    
 _lppTable_
  
> [out] Puntero a un puntero a la tabla de datos adjuntos.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> En la tabla de datos adjuntos se recuperó correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMessage::GetAttachmentTable** devuelve un puntero a la tabla de datos adjuntos del mensaje, que incluye información acerca de todos los datos adjuntos en el mensaje. Los clientes pueden obtener acceso a los datos adjuntos sólo a través de la tabla de datos adjuntos. Al recuperar el número de adjuntos su propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) un cliente puede usar varios de los métodos **IMessage** para trabajar con los datos adjuntos. 
  
Hay una fila por cada dato adjunto. Para obtener una lista completa de las columnas de una tabla de datos adjuntos, vea [Las tablas de datos adjuntos](attachment-tables.md).
  
Normalmente, datos adjuntos no aparecen en la tabla de datos adjuntos hasta que se han guardado los datos adjuntos y el mensaje con una llamada a [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Tablas de datos adjuntos son dinámicas. Si un cliente crea un anexo nuevo, elimina un archivo adjunto existente o cambia una o más propiedades una vez que se han realizado las llamadas **SaveChanges** en los datos adjuntos en el mensaje, en la tabla de datos adjuntos se actualizarán para reflejar la nueva información. 
  
Algunas tablas de datos adjuntos admiten una amplia variedad de restricciones; otros no lo hacen. Compatibilidad con restricciones depende de la implementación del proveedor de almacén de mensajes. 
  
Cuando se abre inicialmente, tablas de datos adjuntos no se ordenan necesariamente en un orden determinado. 
  
Establecer el indicador MAPI_UNICODE en el parámetro _ulFlags_ afecta a las siguientes llamadas a la tabla de datos adjuntos: 
  
- [IMAPITable::QueryColumns](imapitable-querycolumns.md) para recuperar el conjunto de columnas. 
    
- [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar las filas. 
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) para recuperar el criterio de ordenación. 
    
Configuración de las solicitudes de marca de Unicode que la información de todas las columnas de cadena devueltos por estas llamadas estar en formato Unicode. Sin embargo, debido a que no todos los proveedores de almacén de mensajes compatible con Unicode, al establecer este indicador es sólo una solicitud.
  
## <a name="see-also"></a>Recursos adicionales



[IMessage::CreateAttach](imessage-createattach.md)
  
[IMessage::DeleteAttach](imessage-deleteattach.md)
  
[IMessage::OpenAttach](imessage-openattach.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

