---
title: IMAPITableCollapseRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CollapseRow
api_type:
- COM
ms.assetid: 1a23e555-be26-43fb-a715-cfc4ffa623cd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1fd711683ff476ef5d381bca2f9db6bc25b07c68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817587"
---
# <a name="imapitablecollapserow"></a>IMAPITable::CollapseRow

  
  
**Hace referencia a**: Outlook 
  
Contrae una categoría de tabla expandida, quitar los encabezados de nivel inferior y filas de la hoja que pertenecen a la categoría de la vista de tabla.
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a>Parámetros

 _cbInstanceKey_
  
> [entrada] El número de bytes de la propiedad PR_INSTANCE_KEY indicada por el parámetro _pbInstanceKey_ . 
    
 _pbInstanceKey_
  
> [entrada] Un puntero a la propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) que identifica la fila de encabezado de la categoría. 
    
 _ulFlags_
  
> Reservado; debe ser cero.
    
 _lpulRowCount_
  
> [out] Un puntero al número total de filas que se va a quitar de la vista de tabla.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se ha realizado correctamente la operación de contraer.
    
MAPI_E_NOT_FOUND 
  
> La fila identificada por el parámetro _pbInstanceKey_ no existe. 
    
MAPI_E_INVALID_ENTRYID 
  
> La fila identificada por el parámetro _pbInstanceKey_ no existe. Este error es una alternativa a MAPI_E_NOT_FOUND; proveedores de servicios pueden devolver cualquiera de ellas. 
    
## <a name="remarks"></a>Comentarios

El método **IMAPITable::CollapseRow** contrae una categoría de tabla y lo quita de la vista de tabla. Las filas están contraídas empezando por la fila identificada por la propiedad **PR_INSTANCE_KEY** indicada por el parámetro _pbInstanceKey_ . Se devuelve el número de filas que se han quitado de la vista en el contenido del parámetro _lpulRowCount_ . 
  
Nunca se generan notificaciones para las filas de tabla que se quitan de una vista como resultado de una operación de contracción. 
  
Cuando se contrae una fila que se define mediante un marcador fuera de la vista, el marcador se mueve para que apunte a la siguiente fila visible. 
  
Para obtener más información acerca de las tablas ordenadas por categorías, vea [Ordenar y la categorización](sorting-and-categorization.md).
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::DoExpandCollapse  <br/> |MFCMAPI usa el método **IMAPITable::CollapseRow** para contraer una categoría de tabla.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

