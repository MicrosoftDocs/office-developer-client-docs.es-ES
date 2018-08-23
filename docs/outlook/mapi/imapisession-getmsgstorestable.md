---
title: IMAPISessionGetMsgStoresTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetMsgStoresTable
api_type:
- COM
ms.assetid: 77db2dff-4534-440f-a05c-635711cbc2c3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cc0039cf2210446704d25b2156bd4ff50041a524
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586280"
---
# <a name="imapisessiongetmsgstorestable"></a>IMAPISession::GetMsgStoresTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso a la tabla de almacenamiento de mensaje que contiene información acerca de todos los almacenes de mensaje en el perfil de sesión.
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que determina el formato para las columnas que son cadenas de caracteres. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> Las columnas de cadena se encuentran en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las columnas de cadena están en formato ANSI.
    
 _lppTable_
  
> [out] Un puntero a un puntero a la tabla de almacén de mensajes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> En la tabla se devolvió correctamente.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido el indicador MAPI_UNICODE y la sesión no es compatible con Unicode.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISession::GetMsgStoresTable** recupera un puntero a la tabla de almacenamiento de mensajes, una tabla que mantienen MAPI que contiene información acerca de cada almacén de abrir el mensaje en el perfil. 
  
Para obtener una lista completa de columnas obligatorias y opcionales en el mensaje almacén tabla, consulte [Tablas de almacén de mensajes](message-store-tables.md). 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Debido a que MAPI actualiza la tabla de almacenamiento de mensaje durante la sesión cuando se producen cambios, llame al método **Advise** de la tabla de almacenamiento de mensajes para registrarse para recibir notificaciones de estos cambios. Posibles cambios incluyen la adición de nuevos almacenes de mensaje, almacena la eliminación de los existentes y los cambios en el almacén predeterminado. 
  
Establecer el indicador MAPI_UNICODE en el parámetro _ulFlags_ afecta al formato de las columnas devueltas desde los métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md) . Esta marca también controla los tipos de propiedad en el criterio de ordenación devuelto por el método [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenMessageStoreTable  <br/> |MFCMAPI utiliza el método **IMAPISession::GetMsgStoresTable** para obtener la tabla de almacenamiento de mensajes para que se puede representar en el cuadro de diálogo principal de MFCMAPI.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)
  
[Tablas de almacén de mensajes](message-store-tables.md)

