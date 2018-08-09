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
ms.openlocfilehash: 8146b5c2b9c9fb5429a9c1d46bca687c32bcf3dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817772"
---
# <a name="imsgstoregetreceivefoldertable"></a>IMsgStore::GetReceiveFolderTable

  
  
**Hace referencia a**: Outlook 
  
Proporciona acceso a la tabla de la carpeta de recepción, una tabla que incluye información acerca de todas las carpetas de recepción para el almacén de mensajes.
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores de que los controles de la tabla de access. Se pueden establecer los siguientes indicadores:
    
MAPI_DEFERRED_ERRORS 
  
> Permite **GetReceiveFolderTable** devolver de correctamente, posiblemente antes de la tabla es completamente disponible para el autor de la llamada. Si la tabla no está completamente disponible, realizar una llamada de tabla subsiguiente puede producir un error. 
    
MAPI_UNICODE. 
  
> Las cadenas devueltas están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.
    
 _lppTable_
  
> [out] Un puntero a un puntero a la tabla de la carpeta de recepción.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> En la tabla de la carpeta de recepción se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMsgStore::GetReceiveFolderTable** proporciona acceso a una tabla que muestra que los valores de propiedad para todos los del almacén de mensajes reciben las carpetas. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Para obtener una lista de columnas obligatorias en una tabla de la carpeta de recepción, vea [Recibir carpeta tablas](receive-folder-tables.md). 
  
Implementar su recibir tablas de carpeta para admitir las restricciones de propiedad de configuración de la propiedad **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)). Este permite el acceso fácil a determinado reciben las carpetas.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Establecer el indicador MAPI_UNICODE en el parámetro _ulFlags_ afecta al formato de las columnas devueltas desde los métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md) . Esta marca también controla los tipos de propiedad en el criterio de ordenación devuelto por el método [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDisplayReceiveFolderTable  <br/> |MFCMAPI usa el método **IMsgStore::GetReceiveFolderTable** para obtener la tabla de la carpeta de recepción para mostrar.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

