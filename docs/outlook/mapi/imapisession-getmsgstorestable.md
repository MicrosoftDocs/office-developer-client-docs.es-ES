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
ms.openlocfilehash: 5fced633023ebf00efaf5b667dc7994eeb5de316
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428140"
---
# <a name="imapisessiongetmsgstorestable"></a>IMAPISession::GetMsgStoresTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso a la tabla del almacén de mensajes que contiene información sobre todos los almacenes de mensajes en el perfil de sesión.
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parámetros

 _ulFlags_
  
> [entrada] Máscara de bits de marcas que determina el formato de las columnas que son cadenas de caracteres. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las columnas de cadena están en formato Unicode. Si no MAPI_UNICODE marca, las columnas de cadena están en formato ANSI.
    
 _lppTable_
  
> [salida] Puntero a un puntero a la tabla del almacén de mensajes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla se devolvió correctamente.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se MAPI_UNICODE marca y la sesión no admite Unicode.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISession::GetMsgStoresTable** recupera un puntero a la tabla del almacén de mensajes, una tabla mantenida por MAPI que contiene información sobre cada almacén de mensajes abierto en el perfil. 
  
Para obtener una lista completa de las columnas obligatorias y opcionales de la tabla del almacén de mensajes, vea [Tablas del almacén de mensajes.](message-store-tables.md) 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Dado que MAPI actualiza la tabla del almacén de mensajes durante la sesión siempre que se produzcan cambios, llame al método **Advise** de la tabla del almacén de mensajes para registrarse para recibir una notificación de estos cambios. Los cambios posibles incluyen la adición de nuevos almacenes de mensajes, la eliminación de almacenes existentes y los cambios en el almacén predeterminado. 
  
Establecer el MAPI_UNICODE en el parámetro _ulFlags_ afecta al formato de las columnas devueltas de los métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable::QueryRows.](imapitable-queryrows.md) Esta marca también controla los tipos de propiedad en el criterio de ordenación devuelto por el [método IMAPITable::QuerySortOrder.](imapitable-querysortorder.md) 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenMessageStoreTable  <br/> |MFCMAPI usa el método **IMAPISession::GetMsgStoresTable** para obtener la tabla del almacén de mensajes de modo que se pueda representar en el cuadro de diálogo principal de MFCMAPI.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Tablas del almacén de mensajes](message-store-tables.md)

