---
title: IMAPITableExpandRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.ExpandRow
api_type:
- COM
ms.assetid: b96dd8f6-e648-4014-8a1d-ae1da771c439
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5e2ce756baaefef7bd0028e746b1dbe10756365e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415169"
---
# <a name="imapitableexpandrow"></a>IMAPITable::ExpandRow

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Expande una categoría de tabla contrayendo, agregando las filas de título hoja o de nivel inferior que pertenecen a la categoría a la vista de tabla.
  
```cpp
HRESULT ExpandRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows,
ULONG FAR * lpulMoreRows
);
```

## <a name="parameters"></a>Parámetros

 _cbInstanceKey_
  
> [entrada] El recuento de bytes de la PR_INSTANCE_KEY que apunta el _parámetro pbInstanceKey._ 
    
 _pbInstanceKey_
  
> [entrada] Puntero a la propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) que identifica la fila de título de la categoría. 
    
 _ulRowCount_
  
> [entrada] Número máximo de filas que se devolverán en el _parámetro lppRows._ 
    
 _ulFlags_
  
> Reservado; debe ser cero.
    
 _lppRows_
  
> [salida] Puntero a una estructura [SRowSet](srowset.md) que recibe las primeras filas (hasta  _ulRowCount_) que se han insertado en la vista de tabla como resultado de la expansión. Estas filas se insertan después de la fila de título identificada por el _parámetro pbInstanceKey._ El  _parámetro lppRows_ puede ser NULL si  _el parámetro ulRowCount_ es cero. 
    
 _lpulMoreRows_
  
> [salida] Puntero al número total de filas que se agregaron a la vista de tabla.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La categoría se expandió correctamente.
    
MAPI_E_NOT_FOUND 
  
> La fila identificada por el  _parámetro pbInstanceKey_ no existe. 
    
## <a name="remarks"></a>Comentarios

El **método IMAPITable::ExpandRow** expande una categoría de tabla contrae, agregando las filas de título hoja o de nivel inferior que pertenecen a la categoría a la vista de tabla. Se puede especificar un límite en el número de filas que se devolverán en el parámetro _lppRows_ en el _parámetro ulRowCount._ Cuando  _ulRowCount_ se establece en un valor mayor que cero y se devuelve una o más filas en el conjunto de filas señalado por  _lppRows_, la posición del marcador BOOKMARK_CURRENT se mueve a la fila inmediatamente posterior a la última fila del conjunto de filas.
  
Cuando  _ulRowCount_ se establece en cero, solicitando que las filas de título de hoja cero o de nivel inferior se agregan a la categoría, o se devuelven cero filas porque no hay filas de encabezado de hoja o de nivel inferior en la categoría, la posición de BOOKMARK_CURRENT se establece en la fila que sigue a la fila identificada por  _pbInstanceKey_. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

No genere notificaciones en filas que se agregan a una vista de tabla debido a la expansión de categorías.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Es posible que el número de filas del conjunto de filas al que apunta el parámetro  _lppRows_ no sea igual al número de filas que se agregaron realmente a la tabla, todo el conjunto de filas de título hoja o de nivel inferior de la categoría. Pueden producirse errores, como memoria insuficiente o el número de filas de la categoría que supera el número especificado en el _parámetro ulRowCount._ En cualquier caso, BOOKMARK_CURRENT se colocará en la última fila devuelta. Para recuperar inmediatamente el resto de las filas de la categoría, llame a [IMAPITable::QueryRows](imapitable-queryrows.md).
  
No espere recibir una notificación de tabla cuando una categoría cambie su estado. Puede mantener una caché local de filas que se pueden actualizar con cada **llamada ExpandRow** o **CollapseRow.** 
  
Para obtener más información acerca de las tablas categorizadas, vea [Ordenar y categorizar.](sorting-and-categorization.md)
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oExpandCollapse  <br/> |MFCMAPI usa el **método IMAPITable::ExpandRow** para expandir una categoría de tabla contrae.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IMAPITable::CollapseRow](imapitable-collapserow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

