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
ms.openlocfilehash: 9a77d335f3c8980de29dab6e14079c83bd711b43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349276"
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

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Máscara de máscara de los marcadores que se relacionan con la creación de la tabla. Se puede establecer la siguiente marca: 
    
MAPI_UNICODE 
  
> Las columnas de cadena están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las columnas de la cadena tienen formato ANSI.
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **GetAttachmentTable** se devuelva correctamente, posiblemente antes de que la tabla esté completamente disponible para el cliente que realiza la llamada. Si la tabla no está disponible, realizar una llamada subsiguiente a ella puede provocar un error. 
    
 _lppTable_
  
> contempla Puntero a un puntero a la tabla de datos adjuntos.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla de datos adjuntos se recuperó correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMessage:: GetAttachmentTable** devuelve un puntero a la tabla de datos adjuntos del mensaje, que incluye información sobre todos los datos adjuntos del mensaje. Los clientes pueden obtener acceso a datos adjuntos solo a través de la tabla de datos adjuntos. Al recuperar el número de datos adjuntos, su propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)), un cliente puede usar varios de los métodos **IMessage** para trabajar con los datos adjuntos. 
  
Hay una fila por cada dato adjunto. Para obtener una lista completa de las columnas de una tabla de datos adjuntos, vea [tablas de datos](attachment-tables.md)adjuntos.
  
Los datos adjuntos no suelen aparecer en la tabla de datos adjuntos hasta que se guardan los datos adjuntos y el mensaje con una llamada a [IMAPIProp:: SaveChanges](imapiprop-savechanges.md). Las tablas de datos adJuntos son dinámicas. Si un cliente crea un nuevo dato adjunto, elimina un archivo de datos adjuntos existente o cambia una o más propiedades una vez que se han realizado las llamadas de **SaveChanges** en los datos adjuntos del mensaje, la tabla de datos adjuntos se actualizará para reflejar la nueva información. 
  
Algunas tablas de datos adjuntos admiten una amplia variedad de restricciones; otros no. La compatibilidad con las restricciones depende de la implementación del proveedor de almacenamiento de mensajes. 
  
Cuando se abren por primera vez, las tablas de datos adjuntos no están necesariamente ordenadas en un orden determinado. 
  
Si se establece la marca MAPI_UNICODE en el parámetro _ulFlags_ , se verán afectadas las siguientes llamadas a la tabla Attachment: 
  
- [IMAPITable:: QueryColumns](imapitable-querycolumns.md) para recuperar el conjunto de columnas. 
    
- [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar filas. 
    
- [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) para recuperar el criterio de ordenación. 
    
Al establecer el indicador Unicode, se solicita que la información de las columnas de cadena devueltas por estas llamadas esté en formato Unicode. Sin embargo, como no todos los proveedores de almacenamiento de mensajes admiten Unicode, establecer esta marca es solo una solicitud.
  
## <a name="see-also"></a>Vea también



[IMessage::CreateAttach](imessage-createattach.md)
  
[IMessage::DeleteAttach](imessage-deleteattach.md)
  
[IMessage::OpenAttach](imessage-openattach.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

