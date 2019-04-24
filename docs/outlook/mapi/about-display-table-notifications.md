---
title: Información sobre las notificaciones de tabla para mostrar
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 085151e9-4809-4d2b-ae4d-e318355e1f5a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 41e6a2c8b6856bf072972325e7e08aabe3e17446
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326414"
---
# <a name="about-display-table-notifications"></a>Información sobre las notificaciones de tabla para mostrar

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las notificaciones de una tabla de presentación las envía el proveedor de servicios responsable de crear la tabla de presentación en MAPI. MAPI registra las notificaciones llamando al método [IMAPITable:: Advise](imapitable-advise.md) de una tabla de presentación y especificando el evento Table Modified. 
  
Como con todas las notificaciones de tabla, las notificaciones de tabla de visualización incluyen una estructura [TABLE_NOTIFICATION](table_notification.md) . Solo los miembros **ulTableEvent** y **propIndex** de esta estructura son significativos; se omiten los demás miembros. El miembro **ulTableEvent** se establece en TABLE_ROW_MODIFIED y el miembro **propIndex** se establece en el valor de la columna **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) en la fila correspondiente. MAPI responde a la notificación llamando al método [IMAPIProp:: GetProps](imapiprop-getprops.md) para la propiedad mostrada en el control y mostrando el nuevo valor. 
  
Mostrar la tabla las notificaciones se pueden usar por un proveedor de servicios para coordinar los cambios en los controles relacionados en el cuadro de diálogo. Por ejemplo, si la implementación de la interfaz de propiedades necesita actualizar uno o más campos en el cuadro de diálogo, tal vez en respuesta a otro control que haya establecido la marca DT_SET_IMMEDIATE en su propiedad **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)): puede generar una notificación de tabla de visualización. Una notificación de la tabla de visualización puede avisar a la implementación de la interfaz de propiedad de que es necesario volver a leer el valor de uno o más controles debido a un cambio realizado o que se produce un evento externo. 
  
Un proveedor de servicios puede emitir notificaciones de tabla de visualización mediante:
  
- Si se llama a [ITableData:: HrNotify](itabledata-hrnotify.md), si la tabla de presentación se compiló con un objeto de datos de tabla.
    
    - O
    
- Con su propio código, si la tabla de presentación se ha creado con la implementación de **IMAPITable** del proveedor. 
    
MAPI responde para mostrar las notificaciones de tabla cuando es necesario volviendo a leer el valor de un control desde la implementación de la interfaz de propiedades. En la tabla siguiente se describen los detalles relacionados con la forma en que MAPI controla las notificaciones de tipos específicos de controles.
  
|**Control**|**Acción de MAPI**|
|:-----|:-----|
|Botón  <br/> |Llama a [IMAPIProp:: OpenProperty](imapiprop-openproperty.md)para recuperar el objeto de control por medio de la propiedad representada por el miembro **ulPRControl** de la estructura [DTBLBUTTON](dtblbutton.md) si la llamada ha fallado anteriormente. Llama al método [IMAPIControl:: GetState](imapicontrol-getstate.md) del objeto control para determinar si el botón debe estar habilitado y habilitar o deshabilitar el botón en consecuencia.  <br/> |
|Casilla  <br/> |Relee el valor del miembro **ulPRPropertyName** .  <br/> |
|Cuadro combinado  <br/> |Vuelve a abrir la tabla asociada con el miembro **ulPRTableName** de la estructura [DTBLCOMBOBOX](dtblcombobox.md) . Relee todas las filas, incluido el valor del miembro **ulPRPropertyName**.  <br/> |
|Cuadro de lista desPlegable  <br/> |Vuelve a abrir la tabla asociada con el miembro **ulPRTableName** de la estructura [DTBLDDLBX](dtblddlbx.md) y vuelve a leer todas las filas. Llama a [IMAPIProp:: GetProps](imapiprop-getprops.md) para recuperar los valores de las propiedades almacenadas en los miembros **ulPRDisplayProperty** y **ulPRSetProperty** .  <br/> |
|Editar  <br/> |Vuelve a leer la propiedad y vuelve a mostrarla.  <br/> |
|Cuadro de grupo  <br/> |Omite la notificación.  <br/> |
|Label  <br/> |Omite la notificación.  <br/> |
|Cuadro de lista de selección múltiple  <br/> |Si una de las columnas es un identificador de entrada, actualiza el cuadro de lista. El objeto correspondiente no está cerrado o se ha recargado.  <br/> |
|Cuadro de lista de selección única  <br/> |Lee la propiedad Set, intentando identificarla.  <br/> |
|Cuadro de lista multivalor  <br/> |Vuelve a leer la propiedad y vuelve a rellenar el cuadro de lista.  <br/> |
|Página con fichas  <br/> |No hay notificaciones para este control; todo es estático.  <br/> |
|Botón de opción  <br/> |Relee la propiedad asociada al botón y se almacena en el miembro **ulPropTag** de la estructura [DTBLRADIOBUTTON](dtblradiobutton.md) y realiza la selección adecuada con los controles.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Tablas MAPI](mapi-tables.md)

