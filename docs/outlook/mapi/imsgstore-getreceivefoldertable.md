---
title: IMsgStoreGetReceiveFolderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolderTable
api_type:
- COM
ms.assetid: d115ab58-07d2-4b49-8e08-2881c2924102
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 303c2ef855d5cfc1d6614bda92b46c2da97717c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317356"
---
# <a name="imsgstoregetreceivefoldertable"></a>IMsgStore::GetReceiveFolderTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso a la tabla de la carpeta de recepción, una tabla que incluye información acerca de todas las carpetas de recepción del almacén de mensajes.
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Máscara de máscara de marcadores que controla el acceso a la tabla. Se pueden establecer los siguientes indicadores:
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **GetReceiveFolderTable** vuelva correctamente, posiblemente antes de que la tabla esté completamente disponible para el autor de la llamada. Si la tabla no está completamente disponible, puede producirse un error si se realiza una llamada posterior a la tabla. 
    
MAPI_UNICODE 
  
> Las cadenas devueltas están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.
    
 _lppTable_
  
> contempla Un puntero a un puntero a la tabla de la carpeta de recepción.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla de recepción de la carpeta se ha devuelto correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMsgStore:: GetReceiveFolderTable** proporciona acceso a una tabla que muestra la configuración de las propiedades de todas las carpetas de recepción del almacén de mensajes. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Para obtener una lista de las columnas necesarias en una tabla de carpetas de recepción, consulte [Receive Folder tables](receive-folder-tables.md). 
  
Implemente las tablas de la carpeta de recepción para admitir la configuración de restricciones de propiedad en la propiedad **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)). Esto permite un acceso sencillo a determinadas carpetas de recepción.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

La configuración de la marca MAPI_UNICODE en el parámetro _ulFlags_ afecta al formato de las columnas que se devuelven desde los métodos [IMAPITable:: QueryColumns](imapitable-querycolumns.md) y [IMAPITable:: QueryRows](imapitable-queryrows.md) . Esta marca también controla los tipos de propiedades en el criterio de ordenación devueltos por el método [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MsgStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnDisplayReceiveFolderTable  <br/> |MFCMAPI usa el método **IMsgStore:: GetReceiveFolderTable** para obtener la tabla de la carpeta de recepción que se va a mostrar.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

