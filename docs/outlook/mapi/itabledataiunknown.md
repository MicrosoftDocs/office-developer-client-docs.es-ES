---
title: IUnknown ITableData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData
api_type:
- COM
ms.assetid: ac7ae09f-ce19-45cf-8963-fad5bba75452
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3992bea899239ee5975505dec366490d6bbe1698
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348772"
---
# <a name="itabledata--iunknown"></a>ITableData : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona métodos de utilidades para trabajar con tablas. MAPI proporciona objetos de datos de tabla u objetos que implementan **ITableData** para ayudar a los proveedores de servicios a realizar el mantenimiento de tablas. Para obtener un objeto de datos de tabla, los proveedores de servicios llaman a la función [createTable](createtable.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Expuesto por:  <br/> |Objetos de datos de tabla  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPITableData  <br/> |
|Tipo de puntero:  <br/> |LPTABLEDATA  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[HrGetView](itabledata-hrgetview.md) <br/> |Crea una vista de tabla y devuelve un puntero a una implementación de [IMAPITable](imapitableiunknown.md) .  <br/> |
|[HrModifyRow](itabledata-hrmodifyrow.md) <br/> |Inserta una nueva fila de tabla, posiblemente reemplazando una fila existente.  <br/> |
|[HrDeleteRow](itabledata-hrdeleterow.md) <br/> |Elimina una fila de tabla.  <br/> |
|[HrQueryRow](itabledata-hrqueryrow.md) <br/> |Recupera una fila de tabla.  <br/> |
|[HrEnumRow](itabledata-hrenumrow.md) <br/> |Recupera una fila basada en su posición en la tabla.  <br/> |
|[HrNotify](itabledata-hrnotify.md) <br/> |Envía una notificación para una fila de tabla.  <br/> |
|[HrInsertRow](itabledata-hrinsertrow.md) <br/> |Inserta una fila de tabla.  <br/> |
|[HrModifyRows](itabledata-hrmodifyrows.md) <br/> |Inserta varias filas de tabla, posiblemente reemplazando las filas existentes.  <br/> |
|[HrDeleteRows](itabledata-hrdeleterows.md) <br/> |Elimina varias filas de tabla.  <br/> |
   
## <a name="remarks"></a>Comentarios

La implementación de MAPI de **ITableData** trabaja con tablas mediante la retención de todos los datos y las restricciones asociadas en la memoria, lo que hace que no sea adecuado para su uso con tablas de gran tamaño. No se admiten restricciones y operaciones complejas de gran tamaño, como la categorización. 
  
Los objetos de datos de tabla identifican las filas mediante una columna de índice, una propiedad que se garantiza que tendrá un valor único para cada fila. La mayoría de los proveedores de servicios usan la propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) como columna de índice. Las propiedades que tienen varios valores no se pueden usar como columna de índice.
  
Los objetos de datos de tabla generan una sola notificación independientemente del número de filas afectadas por un cambio o la eliminación. Si no existe una fila de destino en una operación, se agrega una fila.
  
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

