---
title: IMAPISessionGetStatusTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetStatusTable
api_type:
- COM
ms.assetid: 53428f8d-4838-46d1-a0ab-cafb194f4cc3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 48a69fa49735014dcbfffad0673f1d4da62452e7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594834"
---
# <a name="imapisessiongetstatustable"></a>IMAPISession::GetStatusTable

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso a la tabla de estado, una tabla que contiene información acerca de todos los recursos MAPI en la sesión.
  
```cpp
HRESULT GetStatusTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que determina el formato para las columnas que son cadenas de caracteres. Se puede establecer la marca siguiente:
    
MAPI_UNICODE 
  
> Las columnas de cadena se encuentran en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las columnas de cadena están en formato ANSI.
    
 _lppTable_
  
> [out] Un puntero a un puntero a la tabla de estado.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> En la tabla se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISession::GetStatusTable** proporciona acceso a la tabla de estado que contiene información acerca de todos los recursos MAPI en la sesión. No hay una fila en la tabla para obtener información sobre el subsistema MAPI, una fila de la cola MAPI, una fila de la libreta de direcciones integrada y una fila por cada proveedor de servicios en el perfil. 
  
Para obtener una lista completa de las columnas obligatorias y opcionales en la tabla de estado, vea [Las tablas de estado](status-tables.md). 
  
Establecer el indicador MAPI_UNICODE en el parámetro _ulFlags_ afecta al formato de las columnas devueltas desde los métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md) . Esta marca también controla los tipos de propiedad en el criterio de ordenación devuelto por el método [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnStatusTable  <br/> |MFCMAPI utiliza el método **IMAPISession::GetStatusTable** para obtener la tabla de estado que se va a representar.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Tablas de estado](status-tables.md)

