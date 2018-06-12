---
title: IMAPITableQueryColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryColumns
api_type:
- COM
ms.assetid: d6341acc-c6ca-4605-93af-77230040339d
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 96fd317c28d95335a3acc5d0603298f2fe8345e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817598"
---
# <a name="imapitablequerycolumns"></a>IMAPITable::QueryColumns

  
  
**Se aplica a**: Outlook 
  
Devuelve una lista de columnas para la tabla.
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Máscara de bits de marcadores que indica qué columna establece que se debe devolver. Se puede establecer la marca siguiente:
    
TBL_ALL_COLUMNS 
  
> La tabla debe devolver todas las columnas disponibles.
    
 _lpPropTagArray_
  
> [out] Establece el puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene las etiquetas de propiedad para la columna. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El conjunto de columnas se devolvió correctamente.
    
MAPI_E_BUSY 
  
> Otra operación se establece en curso que impide que la columna de operación de recuperación de inicio. Debe ser permite la operación en curso para llevar a cabo o se debe detener.
    
## <a name="remarks"></a>Notas

El método **IMAPITable::QueryColumns** se puede llamar para recuperar: 
  
- La columna predeterminado establecido para una tabla.
    
- La columna actual establecido para una tabla, según lo establecido por una llamada al método [IMAPITable::SetColumns](imapitable-setcolumns.md) . 
    
- La columna completa establecido para una tabla, las columnas que están disponibles, pero no necesariamente parte del conjunto actual.
    
## <a name="notes-to-callers"></a>Notas para los llamadores

Si no se establece la marca TBL_ALL_COLUMNS, **IMAPITable::QueryColumns** devuelve una tabla predeterminada o conjunto de columna actual, dependiendo de si la tabla se ha visto afectada por una llamada a **IMAPITable::SetColumns**. **SetColumns** cambia el orden y la selección de columnas en el conjunto de columnas de una tabla. 
  
Si se establece la marca TBL_ALL_COLUMNS, **QueryColumns** devuelve todas las columnas que son capaces de actuar en el conjunto de columnas de la tabla. 
  
Libere la memoria para la matriz de etiqueta de propiedad que apunta el parámetro _lpPropTagArray_ mediante una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::DoSetColumns  <br/> |MFCMAPI usa el método **IMAPITable::QueryColumns** para recuperar la columna actual establecido para una tabla para que el usuario pueda modificarlo.  <br/> |
   
## <a name="see-also"></a>Ver también



[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Elemento SPropTagArray](sproptagarray.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

