---
title: ITableData IUnknown
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
ms.openlocfilehash: bec68568b30bdc3112493a656de591f222801e46
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586245"
---
# <a name="itabledata--iunknown"></a>ITableData : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona métodos de utilidad para trabajar con tablas. MAPI proporciona objetos de datos de tabla u objetos que implementan **ITableData** para ayudar a los proveedores de servicios de realizar el mantenimiento de la tabla. Para obtener un objeto de datos de tabla, proveedores de servicios de llamar a la función [CreateTable](createtable.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Expuestos por:  <br/> |Objetos de datos de tabla  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPITableData  <br/> |
|Tipo de puntero:  <br/> |LPTABLEDATA  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[HrGetView](itabledata-hrgetview.md) <br/> |Crea una vista de tabla, la devolución de un puntero a una implementación [IMAPITable](imapitableiunknown.md) .  <br/> |
|[HrModifyRow](itabledata-hrmodifyrow.md) <br/> |Inserta una nueva fila de tabla, posiblemente reemplazando una fila existente.  <br/> |
|[HrDeleteRow](itabledata-hrdeleterow.md) <br/> |Elimina una fila de tabla.  <br/> |
|[HrQueryRow](itabledata-hrqueryrow.md) <br/> |Recupera una fila de tabla.  <br/> |
|[HrEnumRow](itabledata-hrenumrow.md) <br/> |Recupera una fila en función de su posición en la tabla.  <br/> |
|[HrNotify](itabledata-hrnotify.md) <br/> |Envía una notificación para una fila de tabla.  <br/> |
|[HrInsertRow](itabledata-hrinsertrow.md) <br/> |Inserta una fila de tabla.  <br/> |
|[HrModifyRows](itabledata-hrmodifyrows.md) <br/> |Inserta varias filas de tabla, posiblemente reemplazando las filas existentes.  <br/> |
|[HrDeleteRows](itabledata-hrdeleterows.md) <br/> |Elimina varias filas de tabla.  <br/> |
   
## <a name="remarks"></a>Comentarios

La implementación de MAPI de **ITableData** funciona con tablas manteniendo todos los datos y las restricciones asociadas en la memoria, lo que apropiadas para su uso con tablas muy grandes. No se admiten las restricciones de gran tamaño y operaciones complejas, como la categorización. 
  
Objetos de datos de tabla identifican filas mediante el uso de una columna de índice, una propiedad que se garantiza que tiene un valor único para cada fila. La mayoría de los proveedores de servicios use la propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) como la columna de índice. Las propiedades que tienen varios valores no se puede usar como una columna de índice.
  
Objetos de datos de tabla generan una única notificación independientemente del número de filas afectadas por un cambio o la eliminación. Si no existe una fila de destino de una operación, se agrega una fila.
  
## <a name="see-also"></a>Recursos adicionales



[Interfaces MAPI](mapi-interfaces.md)

