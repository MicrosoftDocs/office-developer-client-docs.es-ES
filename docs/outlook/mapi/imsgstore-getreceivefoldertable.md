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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421357"
---
# <a name="imsgstoregetreceivefoldertable"></a>IMsgStore::GetReceiveFolderTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso a la tabla de carpetas de recepción, una tabla que incluye información sobre todas las carpetas de recepción para el almacén de mensajes.
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a>Parámetros

 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla el acceso a las tablas. Se pueden establecer las siguientes marcas:
    
MAPI_DEFERRED_ERRORS 
  
> Permite **que GetReceiveFolderTable** vuelva correctamente, posiblemente antes de que la tabla esté totalmente disponible para el llamador. Si la tabla no está totalmente disponible, realizar una llamada de tabla posterior puede generar un error. 
    
MAPI_UNICODE 
  
> Las cadenas devueltas están en formato Unicode. Si no MAPI_UNICODE marca, las cadenas están en formato ANSI.
    
 _lppTable_
  
> [salida] Puntero a un puntero a la tabla de la carpeta de recepción.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla de carpetas de recepción se ha devuelto correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMsgStore::GetReceiveFolderTable** proporciona acceso a una tabla que muestra la configuración de propiedades de todas las carpetas de recepción del almacén de mensajes. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Para obtener una lista de las columnas necesarias en una tabla de carpetas de recepción, vea [Tablas de carpetas de recepción.](receive-folder-tables.md) 
  
Implemente las tablas de la carpeta de recepción para admitir la configuración de restricciones de propiedad en **PR_RECORD_KEY** propiedad ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)). Esto permite un fácil acceso a carpetas de recepción concretas.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Establecer el MAPI_UNICODE en el parámetro _ulFlags_ afecta al formato de las columnas devueltas de los métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable::QueryRows.](imapitable-queryrows.md) Esta marca también controla los tipos de propiedad en el criterio de ordenación devuelto por el método [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md) 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDisplayReceiveFolderTable  <br/> |MFCMAPI usa el **método IMsgStore::GetReceiveFolderTable** para obtener la tabla de carpetas de recepción que se mostrará.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

