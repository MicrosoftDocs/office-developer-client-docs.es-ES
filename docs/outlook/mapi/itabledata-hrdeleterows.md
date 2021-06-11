---
title: ITableDataHrDeleteRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRows
api_type:
- COM
ms.assetid: 7b351eec-9624-4b38-9978-5d0b67b64687
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fdd6f40b4d7aa7f65bf1a46d3d9a4f18472b19f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416457"
---
# <a name="itabledatahrdeleterows"></a>ITableData::HrDeleteRows

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Elimina varias filas de tabla.
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Máscara de bits de marcas que controla la eliminación. Se puede establecer la siguiente marca:
    
TAD_ALL_ROWS 
  
> Elimina todas las filas de la tabla y todas las vistas correspondientes, enviando una sola TABLE_RELOAD notificación.
    
 _lprowsetToDelete_
  
> [in] Puntero a un conjunto de filas que describe las filas que se eliminarán. El _parámetro lprowsetToDelete_ puede ser NULL si la marca TAD_ALL_ROWS se establece en el _parámetro ulFlags._ 
    
 _cRowsDeleted_
  
> [salida] Recuento de filas eliminadas.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las filas de tabla se eliminaron correctamente.
    
## <a name="remarks"></a>Comentarios

El **método ITableData::HrDeleteRows** busca y quita las filas de tabla que contienen las columnas que coinciden con la propiedad señalada por el miembro **lpProps** de cada entrada **de aRow** del conjunto de filas. Se usa una columna de índice para identificar cada fila; esta columna debe tener la misma etiqueta de propiedad que la etiqueta de propiedad pasada en el _parámetro ulPropTagIndexColumn_ en la llamada a la [función CreateTable.](createtable.md) 
  
El número de filas que se eliminaron realmente se devuelve en  _cRowsDeleted_. No se devuelve ningún error si no se pudo encontrar una o más filas. 
  
Una vez eliminadas las filas, se envían notificaciones a todos los clientes o proveedores de servicios que tienen una vista de la tabla y que han llamado al método [IMAPITable::Advise](imapitable-advise.md) de la tabla para registrar las notificaciones. 
  
La eliminación de filas no reduce las columnas disponibles para las vistas de tabla existentes o las vistas de tabla abiertas posteriormente, incluso si las filas eliminadas son las últimas que tienen valores para una columna específica.
  
## <a name="see-also"></a>Vea también



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRow](itabledata-hrdeleterow.md)
  
[ITableData::HrModifyRows](itabledata-hrmodifyrows.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

