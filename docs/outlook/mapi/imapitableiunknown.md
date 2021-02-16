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
ms.openlocfilehash: d6a13799da4ef9315f9c23317fa18853d71c72f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420118"
---
# <a name="imapitable--iunknown"></a>IMAPITable : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona una vista de solo lectura de una tabla. Los clientes y proveedores de servicios usan **IMAPITable** para manipular la forma en que aparece una tabla. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuesto por:  <br/> |Objetos Table  <br/> |
|Implementado por:  <br/> |Proveedores de servicios y MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente, proveedores de servicios  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPITable  <br/> |
|Tipo de puntero:  <br/> |LPMAPITABLE  <br/> |
   
## <a name="vtable-order"></a>Orden de tabla virtual

|||
|:-----|:-----|
|[GetLastError](imapitable-getlasterror.md) <br/> |Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior de la tabla.  <br/> |
|[Aconsejar](imapitable-advise.md) <br/> |Se registra para recibir una notificación de eventos especificados que afectan a la tabla.  <br/> |
|[Unadvise](imapitable-unadvise.md) <br/> |Cancela el envío de notificaciones previamente configuradas con una llamada al método **IMAPITable::Advise.**  <br/> |
|[GetStatus](imapitable-getstatus.md) <br/> |Devuelve el estado y el tipo de la tabla.  <br/> |
|[SetColumns](imapitable-setcolumns.md) <br/> |Define las propiedades concretas y el orden de las propiedades que aparecen como columnas en la tabla.  <br/> |
|[QueryColumns](imapitable-querycolumns.md) <br/> |Devuelve una lista de columnas para la tabla.  <br/> |
|[GetRowCount](imapitable-getrowcount.md) <br/> |Devuelve el número total de filas de la tabla.  <br/> |
|[SeekRow](imapitable-seekrow.md) <br/> |Mueve el cursor a una posición específica de la tabla.  <br/> |
|[SeekRowApprox](imapitable-seekrowapprox.md) <br/> |Mueve el cursor a una posición fraccional aproximada en la tabla.  <br/> |
|[QueryPosition](imapitable-queryposition.md) <br/> |Recupera la posición actual de fila de tabla del cursor, basándose en un valor fraccionrio.  <br/> |
|[FindRow](imapitable-findrow.md) <br/> |Busca la siguiente fila de una tabla que coincide con criterios de búsqueda específicos.  <br/> |
|[Restrict](imapitable-restrict.md) <br/> |Aplica un filtro a una tabla, lo que reduce el conjunto de filas a solo aquellas filas que coincidan con los criterios especificados.  <br/> |
|[CreateBookmark](imapitable-createbookmark.md) <br/> |Marca la posición actual de la tabla.  <br/> |
|[FreeBookmark](imapitable-freebookmark.md) <br/> |Libera la memoria asociada a un marcador.  <br/> |
|[SortTable](imapitable-sorttable.md) <br/> |Ordena las filas de la tabla según criterios de ordenación.  <br/> |
|[QuerySortOrder](imapitable-querysortorder.md) <br/> |Recupera el criterio de ordenación actual de una tabla.  <br/> |
|[QueryRows](imapitable-queryrows.md) <br/> |Devuelve una o más filas de una tabla, comenzando en la posición actual del cursor.  <br/> |
|[Anular](imapitable-abort.md) <br/> |Detiene las operaciones asincrónicas actualmente en curso para la tabla.  <br/> |
|[ExpandRow](imapitable-expandrow.md) <br/> |Expande una categoría de tabla contrayendo y agrega las filas hoja pertenecientes a la categoría a la vista de tabla.  <br/> |
|[CollapseRow](imapitable-collapserow.md) <br/> |Contrae una categoría de tabla expandida, quitando las filas hoja pertenecientes a la categoría de la vista de tabla.  <br/> |
|[WaitForCompletion](imapitable-waitforcompletion.md) <br/> |Suspende el procesamiento hasta que se hayan completado una o varias operaciones asincrónicas en curso en la tabla.  <br/> |
|[GetCollapseState](imapitable-getcollapsestate.md) <br/> |Devuelve los datos necesarios para volver a generar el estado contraído o expandido actual de una tabla categorizada.  <br/> |
|[SetCollapseState](imapitable-setcollapsestate.md) <br/> |Vuelve a generar el estado expandido o contraído actual de una tabla categorizada con datos guardados por una llamada anterior al método **IMAPITable::GetCollapseState.**  <br/> |
   
## <a name="see-also"></a>Consulte también



[Interfaces MAPI](mapi-interfaces.md)

