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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421175"
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

## <a name="parameters"></a>Parámetros

 _ulFlags_
  
> [entrada] Máscara de bits de marcas relacionadas con la creación de la tabla. Se puede establecer la siguiente marca: 
    
MAPI_UNICODE 
  
> Las columnas de cadena están en formato Unicode. Si no MAPI_UNICODE marca, las columnas de cadena están en formato ANSI.
    
MAPI_DEFERRED_ERRORS 
  
> Permite **que GetAttachmentTable** vuelva correctamente, posiblemente antes de que la tabla esté totalmente disponible para el cliente que realiza la llamada. Si la tabla no está disponible, realizar una llamada posterior a ella puede provocar un error. 
    
 _lppTable_
  
> [salida] Puntero a un puntero a la tabla de datos adjuntos.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla de datos adjuntos se recuperó correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMessage::GetAttachmentTable** devuelve un puntero a la tabla de datos adjuntos del mensaje, que incluye información sobre todos los datos adjuntos del mensaje. Los clientes pueden obtener acceso a datos adjuntos solo a través de la tabla de datos adjuntos. Al recuperar el número de datos adjuntos, su propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) un cliente puede usar varios de los métodos **IMessage** para trabajar con los datos adjuntos. 
  
Hay una fila para cada dato adjunto. Para obtener una lista completa de las columnas de una tabla de datos adjuntos, vea [Tablas de datos adjuntos.](attachment-tables.md)
  
Normalmente, los datos adjuntos no aparecen en la tabla de datos adjuntos hasta que se han guardado los datos adjuntos y el mensaje con una llamada a [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Las tablas de datos adjuntos son dinámicas. Si un cliente crea nuevos datos adjuntos, elimina datos adjuntos existentes o cambia una o más propiedades una vez que se han realizado las llamadas **a SaveChanges** en los datos adjuntos del mensaje, la tabla de datos adjuntos se actualizará para reflejar la nueva información. 
  
Algunas tablas de datos adjuntos admiten una amplia variedad de restricciones; otros no lo hacen. La compatibilidad con las restricciones depende de la implementación del proveedor del almacén de mensajes. 
  
Cuando se abren inicialmente, las tablas de datos adjuntos no se ordenan necesariamente en un orden determinado. 
  
Establecer el MAPI_UNICODE en el  _parámetro ulFlags_ afecta a las siguientes llamadas a la tabla de datos adjuntos: 
  
- [IMAPITable::QueryColumns](imapitable-querycolumns.md) para recuperar el conjunto de columnas. 
    
- [IMAPITable::QueryRows](imapitable-queryrows.md) para recuperar filas. 
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) para recuperar el criterio de ordenación. 
    
Al establecer la marca Unicode, se solicita que la información de las columnas de cadena devueltas por estas llamadas esté en formato Unicode. Sin embargo, dado que no todos los proveedores de al almacenamiento de mensajes admiten Unicode, establecer esta marca es solo una solicitud.
  
## <a name="see-also"></a>Consulte también



[IMessage::CreateAttach](imessage-createattach.md)
  
[IMessage::DeleteAttach](imessage-deleteattach.md)
  
[IMessage::OpenAttach](imessage-openattach.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

