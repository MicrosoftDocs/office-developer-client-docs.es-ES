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
ms.openlocfilehash: ec305fc872d1bf1718592dabdd230617d50d3f54
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434336"
---
# <a name="imapitablegetstatus"></a>IMAPITable::GetStatus

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve el estado y el tipo de la tabla.
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a>Parámetros

 _lpulTableStatus_
  
> [salida] Puntero a un valor que indica el estado de la tabla. Se puede devolver uno de los siguientes valores:
    
TBLSTAT_COMPLETE 
  
> No hay ninguna operación en curso.
    
TBLSTAT_QCHANGED 
  
> El contenido de la tabla ha cambiado de forma esperada. Este valor de estado no se devuelve para los cambios que resultan de operaciones de ordenación o restricción.
    
TBLSTAT_RESTRICT_ERROR 
  
> Se produjo un error durante [una operación IMAPITable::Restrict.](imapitable-restrict.md) 
    
TBLSTAT_RESTRICTING 
  
> Hay **una operación IMAPITable::Restrict** en curso. 
    
TBLSTAT_SETCOL_ERROR 
  
> Se produjo un error [durante una operación IMAPITable::SetColumns.](imapitable-setcolumns.md) 
    
TBLSTAT_SETTING_COLS 
  
> Hay **una operación IMAPITable::SetColumns** en curso. 
    
TBLSTAT_SORT_ERROR 
  
> Se produjo un error durante una [operación IMAPITable::SortTable.](imapitable-sorttable.md) 
    
TBLSTAT_SORTING 
  
> Hay **una operación IMAPITable::SortTable** en curso. 
    
 _lpulTableType_
  
> [salida] Puntero a un valor que indica el tipo de la tabla. Se puede devolver uno de los tres tipos de tabla siguientes:
    
TBLTYPE_DYNAMIC 
  
> El contenido de la tabla es dinámico; los valores de filas y columnas pueden cambiar a medida que cambian los datos subyacentes.
    
TBLTYPE_KEYSET 
  
> Las filas de la tabla son fijas, pero los valores de las columnas dentro de estas filas son dinámicos y pueden cambiar a medida que cambian los datos subyacentes.
    
TBLTYPE_SNAPSHOT 
  
> La tabla es estática y su contenido no cambia cuando cambian los datos subyacentes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El estado de la tabla se ha devuelto correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMAPTable::GetStatus** recupera información sobre el tipo y el estado actual de una tabla. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede usar **GetStatus junto** con otros tres métodos **IMAPITable** para supervisar el estado de esas operaciones y determinar el efecto en la tabla. Llame **a GetStatus** después de realizar una de las **siguientes llamadas IMAPITable:** 
  
- [IMAPITable::Restrict](imapitable-restrict.md) para establecer una restricción. 
    
- [IMAPITable::SortTable](imapitable-sorttable.md) para establecer un criterio de ordenación. 
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md) para definir un conjunto de columnas. 
    
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::GetStatus  <br/> |MFCMAPI usa el **método IMAPITable::GetStatus** para notificar el estado de una tabla.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

