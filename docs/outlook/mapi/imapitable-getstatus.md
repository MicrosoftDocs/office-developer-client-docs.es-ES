---
title: IMAPITableGetStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetStatus
api_type:
- COM
ms.assetid: f114f1fa-bc05-4587-875b-71548c5912ea
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cda3de1719ec1b7cfca1a9ecdad7bc3b59a8b17d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571153"
---
# <a name="imapitablegetstatus"></a>IMAPITable::GetStatus

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Devuelve el estado y el tipo de la tabla.
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a>Parámetros

 _lpulTableStatus_
  
> [out] Puntero a un valor que indica el estado de la tabla. Puede devolver uno de los siguientes valores:
    
TBLSTAT_COMPLETE 
  
> No hay ninguna operación está en curso.
    
TBLSTAT_QCHANGED 
  
> El contenido de la tabla expectantly ha cambiado. No se devuelve este valor de estado para que los cambios que resultan de las operaciones de ordenación o restricción.
    
TBLSTAT_RESTRICT_ERROR 
  
> Se ha producido un error durante una operación [IMAPITable:: Restrict](imapitable-restrict.md) . 
    
TBLSTAT_RESTRICTING 
  
> Una operación **IMAPITable:: Restrict** está en curso. 
    
TBLSTAT_SETCOL_ERROR 
  
> Se ha producido un error durante una operación de [IMAPITable::SetColumns](imapitable-setcolumns.md) . 
    
TBLSTAT_SETTING_COLS 
  
> Una operación **IMAPITable::SetColumns** está en curso. 
    
TBLSTAT_SORT_ERROR 
  
> Se ha producido un error durante una operación de [SortTable](imapitable-sorttable.md) . 
    
TBLSTAT_SORTING 
  
> Una operación de **SortTable** está en curso. 
    
 _lpulTableType_
  
> [out] Puntero a un valor que indica el tipo de tabla. Puede devolver uno de los siguientes tipos de tres tabla:
    
TBLTYPE_DYNAMIC 
  
> Contenido de la tabla es dinámico; pueden cambiar las filas y los valores de columna como los cambios de datos subyacente.
    
TBLTYPE_KEYSET 
  
> Se corrigen las filas dentro de la tabla, pero los valores de las columnas dentro de estas filas son dinámicos y pueden cambiar como los cambios de datos subyacente.
    
TBLTYPE_SNAPSHOT 
  
> En la tabla es estática, y su contenido no cambian cuando cambian los datos subyacentes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Estado de la tabla se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPTable::GetStatus** recupera información sobre el tipo y el estado actual de una tabla. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar **GetStatus** junto con los otros tres métodos de **IMAPITable** para supervisar el estado de las operaciones y determinar el efecto en la tabla. Llamada **GetStatus** después de realizar una de las llamadas de **IMAPITable** siguientes: 
  
- [IMAPITable:: Restrict](imapitable-restrict.md) para establecer una restricción. 
    
- [SortTable](imapitable-sorttable.md) para establecer un criterio de ordenación. 
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md) para definir un conjunto de columnas. 
    
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::GetStatus  <br/> |MFCMAPI usa el método **IMAPITable::GetStatus** para informar del estado de una tabla.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

