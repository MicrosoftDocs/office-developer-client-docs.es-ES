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
ms.openlocfilehash: e6a180ceb325a705ebf226bb728c52cce7396490
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416177"
---
# <a name="imapitablecollapserow"></a>IMAPITable::CollapseRow

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contrae una categoría de tabla expandida, quitando los títulos de nivel inferior y las filas de hoja que pertenecen a la categoría de la vista de tabla.
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a>Parameters

 _cbInstanceKey_
  
> a El número de bytes de la propiedad PR_INSTANCE_KEY a la que apunta el parámetro _pbInstanceKey_ . 
    
 _pbInstanceKey_
  
> a Un puntero a la propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) que identifica la fila de encabezado de la categoría. 
    
 _ulFlags_
  
> Reserve debe ser cero.
    
 _lpulRowCount_
  
> contempla Un puntero al número total de filas que se van a quitar de la vista de tabla.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de contracción se realizó correctamente.
    
MAPI_E_NOT_FOUND 
  
> La fila identificada por el parámetro _pbInstanceKey_ no existe. 
    
MAPI_E_INVALID_ENTRYID 
  
> La fila identificada por el parámetro _pbInstanceKey_ no existe. Este error es una alternativa a MAPI_E_NOT_FOUND; los proveedores de servicios pueden devolver cualquiera de los dos. 
    
## <a name="remarks"></a>Comentarios

El método **IMAPITable:: CollapseRow** contrae una categoría de tabla y la quita de la vista de tabla. Las filas se contraen comenzando en la fila identificada por la propiedad **PR_INSTANCE_KEY** a la que señala el parámetro _pbInstanceKey_ . El número de filas que se quitan de la vista se devuelve en el contenido del parámetro _lpulRowCount_ . 
  
Las notificaciones nunca se generan para las filas de tabla que se quitan de una vista como resultado de una operación de contracción. 
  
Cuando una fila definida por un marcador está contraída de la vista, el marcador se mueve para que apunte a la siguiente fila visible. 
  
Para obtener más información acerca de las tablas clasificadas por categorías, vea [ordenar y categorización](sorting-and-categorization.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContentsTableListCtrl::D oExpandCollapse  <br/> |MFCMAPI usa el método **IMAPITable:: CollapseRow** para contraer una categoría de tabla.  <br/> |
   
## <a name="see-also"></a>Ver también



[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

