---
title: IMAPITable IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable
api_type:
- COM
ms.assetid: f25be2b1-0f94-4a0c-b29d-d2201dc70ab7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0ffaf5909c978059343067c93a2b30f5969327e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817606"
---
# <a name="imapitable--iunknown"></a>IMAPITable : IUnknown

  
  
**Hace referencia a**: Outlook 
  
Proporciona una vista de sólo lectura de una tabla. **IMAPITable** se usa en los clientes y proveedores de servicios para manipular la apariencia de una tabla. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuestos por:  <br/> |Objetos de la tabla  <br/> |
|Se implementa mediante:  <br/> |Proveedores de servicios y MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente, los proveedores de servicios  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPITable  <br/> |
|Tipo de puntero:  <br/> |LPMAPITABLE  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[GetLastError](imapitable-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior en la tabla.  <br/> |
|[Aviso](imapitable-advise.md) <br/> |Se registra para recibir notificaciones de los eventos que afectan a la tabla.  <br/> |
|[Desaconsejar](imapitable-unadvise.md) <br/> |Cancela el envío de notificaciones configuradas previamente con una llamada al método **IMAPITable::Advise** .  <br/> |
|[GetStatus](imapitable-getstatus.md) <br/> |Devuelve el estado y el tipo de la tabla.  <br/> |
|[SetColumns](imapitable-setcolumns.md) <br/> |Define las propiedades concretas y el orden de las propiedades que aparecen como columnas en la tabla.  <br/> |
|[QueryColumns](imapitable-querycolumns.md) <br/> |Devuelve una lista de columnas para la tabla.  <br/> |
|[GetRowCount](imapitable-getrowcount.md) <br/> |Devuelve el número total de filas en la tabla.  <br/> |
|[SeekRow](imapitable-seekrow.md) <br/> |Mueve el cursor a una posición específica en la tabla.  <br/> |
|[SeekRowApprox](imapitable-seekrowapprox.md) <br/> |Mueve el cursor a una posición aproximada fraccionaria en la tabla.  <br/> |
|[QueryPosition](imapitable-queryposition.md) <br/> |Recupera la posición de fila de tabla actual del cursor, basándose en un valor decimal.  <br/> |
|[FindRow](imapitable-findrow.md) <br/> |Busca la siguiente fila en una tabla que coincida con los criterios de búsqueda específicos.  <br/> |
|[Restringir](imapitable-restrict.md) <br/> |Se aplica un filtro a una tabla, reducción de la fila que se establece en sólo las filas que coincidan con los criterios especificados.  <br/> |
|[CreateBookmark](imapitable-createbookmark.md) <br/> |Marca la posición actual de la tabla.  <br/> |
|[FreeBookmark](imapitable-freebookmark.md) <br/> |Libera la memoria asociada con un marcador.  <br/> |
|[SortTable](imapitable-sorttable.md) <br/> |Ordena las filas de la tabla en función de los criterios de ordenación.  <br/> |
|[QuerySortOrder](imapitable-querysortorder.md) <br/> |Recupera el criterio de ordenación actual para una tabla.  <br/> |
|[QueryRows](imapitable-queryrows.md) <br/> |Devuelve una o varias filas de una tabla, que comienza en la posición actual del cursor.  <br/> |
|[Anular](imapitable-abort.md) <br/> |Detiene cualquier operación asincrónica actualmente en curso para la tabla.  <br/> |
|[ExpandRow](imapitable-expandrow.md) <br/> |Expande una categoría de tabla contraído, adición de las filas de la hoja que pertenecen a la categoría a la vista de tabla.  <br/> |
|[CollapseRow](imapitable-collapserow.md) <br/> |Contrae una categoría de tabla expandida, quitar las filas de la hoja que pertenecen a la categoría de la vista de tabla.  <br/> |
|[WaitForCompletion](imapitable-waitforcompletion.md) <br/> |Suspende el procesamiento hasta que han completado una o varias operaciones asincrónicas en curso en la tabla.  <br/> |
|[GetCollapseState](imapitable-getcollapsestate.md) <br/> |Devuelve los datos necesarios para volver a generar la actual contraído o expandido el estado de una tabla con categorías.  <br/> |
|[SetCollapseState](imapitable-setcollapsestate.md) <br/> |Vuelve a crear el estado actual de expandidos o contraído de una tabla con categorías utilizando los datos que se guardan por una llamada anterior al método **IMAPITable::GetCollapseState** .  <br/> |
   
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

