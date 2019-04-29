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
  
Expande una categoría de tabla contraída, agregando las filas de título de la hoja o del nivel inferior que pertenecen a la categoría a la vista de tabla.
  
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

## <a name="parameters"></a>Parameters

 _cbInstanceKey_
  
> a El número de bytes de la propiedad PR_INSTANCE_KEY a la que apunta el parámetro _pbInstanceKey_ . 
    
 _pbInstanceKey_
  
> a Un puntero a la propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) que identifica la fila de encabezado de la categoría. 
    
 _ulRowCount_
  
> a El número máximo de filas que se devolverán en el parámetro _lppRows_ . 
    
 _ulFlags_
  
> Reserve debe ser cero.
    
 _lppRows_
  
> contempla Un puntero a una estructura [SRowSet](srowset.md) que recibe la primera (hasta _ulRowCount_) filas que se han insertado en la vista de tabla como resultado de la expansión. Estas filas se insertan después de la fila de encabezado identificada por el parámetro _pbInstanceKey_ . El parámetro _lppRows_ puede ser null si el parámetro _ulRowCount_ es cero. 
    
 _lpulMoreRows_
  
> contempla Un puntero al número total de filas que se agregaron a la vista de tabla.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La categoría se ha expandido correctamente.
    
MAPI_E_NOT_FOUND 
  
> La fila identificada por el parámetro _pbInstanceKey_ no existe. 
    
## <a name="remarks"></a>Comentarios

El método **IMAPITable:: ExpandRow** expande una categoría de tabla contraída, agregando las filas de título de hoja o de encabezado de nivel inferior que pertenecen a la categoría a la vista de tabla. Se puede especificar un límite en el número de filas que se van a devolver en el parámetro _lppRows_ en el parámetro _ulRowCount_ . Cuando _ulRowCount_ se establece en un valor mayor que cero y se devuelven una o más filas en el conjunto de filas al que apunta _lppRows_, la posición del marcador BOOKMARK_CURRENT se mueve a la fila inmediatamente posterior a la última fila del conjunto de filas.
  
Cuando _ulRowCount_ se establece en cero, solicitando que las filas de título de hoja cero o de nivel inferior se agreguen a la categoría, o que se devuelvan cero filas porque no hay ninguna hoja ni filas de título de nivel inferior en la categoría, la posición de BOOKMARK_CURRENT se establece en la fila siguiendo la fila identificada por _pbInstanceKey_. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

No genere notificaciones en las filas que se agreguen a una vista de tabla debido a la expansión de categorías.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

El número de filas en el conjunto de filas al que apuntaba el parámetro _lppRows_ podría no ser igual al número de filas que realmente se agregaron a la tabla, el conjunto completo de filas de título de hoja o de nivel inferior de la categoría. Se pueden producir errores, como memoria insuficiente o el número de filas de la categoría que supera el número especificado en el parámetro _ulRowCount_ . En cualquier caso, BOOKMARK_CURRENT se colocará en la última fila devuelta. Para recuperar inmediatamente el resto de las filas de la categoría, llame al [IMAPITable:: QueryRows](imapitable-queryrows.md).
  
No espere recibir una notificación de tabla cuando una categoría cambie su estado. Puede mantener una memoria caché local de filas que se pueden actualizar con cada llamada a **ExpandRow** o **CollapseRow** . 
  
Para obtener más información acerca de las tablas clasificadas por categorías, vea [ordenar y categorización](sorting-and-categorization.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContentsTableListCtrl::D oExpandCollapse  <br/> |MFCMAPI usa el método **IMAPITable:: ExpandRow** para expandir una categoría de tabla contraída.  <br/> |
   
## <a name="see-also"></a>Ver también



[IMAPITable::CollapseRow](imapitable-collapserow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

