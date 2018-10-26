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
ms.openlocfilehash: 753067c8c0af15a44e0f3b71f6122d8683db4a98
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572112"
---
# <a name="itabledatahrdeleterows"></a>ITableData::HrDeleteRows

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Elimina varias filas de tabla.
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla la eliminación. Se puede establecer la marca siguiente:
    
TAD_ALL_ROWS 
  
> Elimina todas las filas de la tabla y todas las vistas correspondientes, enviar una notificación de TABLE_RELOAD único.
    
 _lprowsetToDelete_
  
> [entrada] Un puntero a un conjunto de filas que se describe las filas que se va a eliminar. El parámetro _lprowsetToDelete_ puede ser NULL si la marca TAD_ALL_ROWS se establece en el parámetro _ulFlags indicado_ . 
    
 _cRowsDeleted_
  
> [out] El recuento de las filas eliminadas.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las filas de tabla se eliminaron correctamente.
    
## <a name="remarks"></a>Comentarios

El método **ITableData::HrDeleteRows** busca y quita las filas de tabla que contienen las columnas que coinciden con la propiedad apuntada establece el miembro **lpProps** de cada entrada de **aRow** en la fila. Una columna de índice se usa para identificar cada fila; Esta columna debe tener la misma etiqueta de propiedad, como la etiqueta de propiedad que se pasa en el parámetro _ulPropTagIndexColumn_ en la llamada a la función [CreateTable](createtable.md) . 
  
Se devuelve el número de filas que realmente se eliminaron en _cRowsDeleted_. Se devuelve ningún error si no se podrían encontrar una o varias filas. 
  
Después de que se eliminan las filas, las notificaciones se envían a todos los clientes o proveedores de servicios que tienen una vista de la tabla y que ha llamado [IMAPITable::Advise](imapitable-advise.md) (método) de la tabla para registrar para las notificaciones. 
  
Eliminación de filas no reduce las columnas disponibles para las vistas de tabla existentes o vuelven a abrir vistas de tabla, incluso si las filas eliminadas son la última que tienen los valores de una columna específica.
  
## <a name="see-also"></a>Vea también



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRow](itabledata-hrdeleterow.md)
  
[ITableData::HrModifyRows](itabledata-hrmodifyrows.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

