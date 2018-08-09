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
ms.openlocfilehash: 1b3d8c74d85696e733b378a4cac2b8e2a3b6a072
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817577"
---
# <a name="imapitableexpandrow"></a>IMAPITable::ExpandRow

  
  
**Hace referencia a**: Outlook 
  
Expande una categoría de tabla contraído, adición de la hoja o las filas de encabezado de nivel inferior que pertenecen a la categoría a la vista de tabla.
  
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
  
> [entrada] El número de bytes de la propiedad PR_INSTANCE_KEY indicada por el parámetro _pbInstanceKey_ . 
    
 _pbInstanceKey_
  
> [entrada] Un puntero a la propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) que identifica la fila de encabezado de la categoría. 
    
 _ulRowCount_
  
> [entrada] El número máximo de filas que se devuelven en el parámetro _lppRows_ . 
    
 _ulFlags_
  
> Reservado; debe ser cero.
    
 _lppRows_
  
> [out] Un puntero a una estructura [SRowSet](srowset.md) recibir las filas primeros (hasta _ulRowCount_) que se han insertado en la vista de tabla como resultado de la expansión. Estas filas se insertan después de la fila de encabezado identificada mediante el parámetro _pbInstanceKey_ . El parámetro _lppRows_ puede ser NULL si el parámetro _ulRowCount_ es cero. 
    
 _lpulMoreRows_
  
> [out] Un puntero al número total de filas que se han agregado a la vista de tabla.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La categoría se expandió correctamente.
    
MAPI_E_NOT_FOUND 
  
> La fila identificada por el parámetro _pbInstanceKey_ no existe. 
    
## <a name="remarks"></a>Comentarios

El método **IMAPITable::ExpandRow** expande una categoría de tabla contraído, adición de la hoja o las filas de encabezado de nivel inferior que pertenecen a la categoría a la vista de tabla. En el parámetro _ulRowCount_ se puede especificar un límite para el número de filas que se devuelven en el parámetro _lppRows_ . Cuando _ulRowCount_ se establece en un valor mayor que cero y se devuelven una o varias filas en el conjunto de filas que señala _lppRows_, se establece la posición del marcador que bookmark_current se mueve a la fila inmediatamente después de la última fila de la fila.
  
Cuando _ulRowCount_ se establece en cero, que solicita que cero hoja o filas de título de nivel inferior se agrega a la categoría o, se devuelven cero filas porque no hay ninguna hoja o las filas de encabezado de nivel inferior de la categoría, se establece la posición de BOOKMARK_CURRENT en la fila Después de la fila identificada por _pbInstanceKey_. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

No generan notificaciones en las filas que se agregan a una vista de tabla debido a la expansión de la categoría.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

El número de filas en el conjunto de filas que apunta el parámetro _lppRows_ no podría ser igual al número de filas que realmente se han agregado a la tabla, todo el conjunto de hoja o heading filas para la categoría de nivel inferior. Pueden producirse errores, como memoria insuficiente o el número de filas en la categoría si se excede el número especificado en el parámetro _ulRowCount_ . En cualquier caso, BOOKMARK_CURRENT se colocará en la última fila devuelta. Para recuperar inmediatamente el resto de las filas de la categoría, llame [IMAPITable:: QueryRows](imapitable-queryrows.md).
  
No se debe esperar recibir una notificación de tabla cuando una categoría cambia su estado. Puede mantener una memoria caché local de filas que se pueden actualizar con cada llamada **ExpandRow** o **CollapseRow** . 
  
Para obtener más información acerca de las tablas ordenadas por categorías, vea [Ordenar y la categorización](sorting-and-categorization.md).
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::DoExpandCollapse  <br/> |MFCMAPI usa el método **IMAPITable::ExpandRow** para expandir una categoría de tabla contraídos.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPITable::CollapseRow](imapitable-collapserow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

