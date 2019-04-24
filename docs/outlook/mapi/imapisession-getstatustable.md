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
ms.openlocfilehash: 17e936093536f548d16021523d9434f09777c6d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338767"
---
# <a name="imapisessiongetstatustable"></a>IMAPISession::GetStatusTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso a la tabla de estado, una tabla que contiene información sobre todos los recursos MAPI de la sesión.
  
```cpp
HRESULT GetStatusTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Máscara de caracteres de marcas que determina el formato de las columnas que son cadenas de caracteres. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las columnas de cadena están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las columnas de la cadena tienen formato ANSI.
    
 _lppTable_
  
> contempla Un puntero a un puntero a la tabla de estado.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISession:: GetStatusTable** proporciona acceso a la tabla de estado que contiene información sobre todos los recursos MAPI de la sesión. Hay una fila en la tabla para obtener información acerca del subsistema MAPI, una fila para la cola MAPI, una fila para la libreta de direcciones integrada y una fila para cada proveedor de servicios en el perfil. 
  
Para obtener una lista completa de las columnas necesarias y opcionales de la tabla de estado, consulte [TABLE status](status-tables.md). 
  
La configuración de la marca MAPI_UNICODE en el parámetro _ulFlags_ afecta al formato de las columnas que se devuelven desde los métodos [IMAPITable:: QueryColumns](imapitable-querycolumns.md) y [IMAPITable:: QueryRows](imapitable-queryrows.md) . Esta marca también controla los tipos de propiedades en el criterio de ordenación devueltos por el método [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MainDlg. cpp  <br/> |CMainDlg:: OnStatusTable  <br/> |MFCMAPI usa el método **IMAPISession:: GetStatusTable** para obtener la tabla de estado que se va a representar.  <br/> |
   
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

