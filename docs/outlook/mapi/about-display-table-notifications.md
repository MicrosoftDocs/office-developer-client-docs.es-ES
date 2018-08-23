---
title: Acerca de las notificaciones de tabla para mostrar
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 085151e9-4809-4d2b-ae4d-e318355e1f5a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 487a5dbcdefe901b514083ee910972354574bd82
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564461"
---
# <a name="about-display-table-notifications"></a>Acerca de las notificaciones de tabla para mostrar

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En una tabla para mostrar se envían por el proveedor de servicio responsable de la creación de la tabla para mostrar de MAPI. MAPI se registra para estas notificaciones al llamar al método [IMAPITable::Advise](imapitable-advise.md) de una tabla para mostrar y especificar el evento de modificación de tabla. 
  
Al igual que con todas las notificaciones de tabla, mostrar notificaciones de tabla incluyen la estructura de [TABLE_NOTIFICATION](table_notification.md) . El **ulTableEvent** y los miembros de **propIndex** de esta estructura son significativos; se omiten los demás miembros. El miembro **ulTableEvent** está establecido en TABLE_ROW_MODIFIED y el miembro **propIndex** se establece en el valor de la columna **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) en la fila correspondiente. MAPI se responde a la notificación llamando al método [IMAPIProp::GetProps](imapiprop-getprops.md) para la propiedad que se muestra en el control y mostrando el nuevo valor. 
  
Mostrar notificaciones de tabla se pueden usar un proveedor de servicios para coordinar los cambios realizados en los controles relacionados en el cuadro de diálogo. Por ejemplo, si la implementación de la interfaz de la propiedad tiene que actualizar uno o más campos en el cuadro de diálogo, quizás como respuesta a otro control que se ha establecido el indicador DT_SET_IMMEDIATE en su propiedad **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)): puede generar una notificación de la tabla para mostrar. Una notificación de la tabla para mostrar puede alertar a la implementación de la interfaz de propiedad que necesita el valor de uno o varios controles a leer debido a realizar un cambio o que se produzca un evento externo. 
  
Un proveedor de servicios puede emitir notificaciones de tabla para mostrar por:
  
- Al llamar a [ITableData::HrNotify](itabledata-hrnotify.md), si se creó la tabla para mostrar con un objeto de datos de tabla.
    
    - O bien -
    
- Uso de su propio código, si se creó la tabla para mostrar con la implementación del proveedor **IMAPITable** . 
    
MAPI responde para mostrar las notificaciones de tabla cuando sea necesario volver a leer un valor del control de la implementación de la interfaz de la propiedad. En la siguiente tabla se describe los detalles que lo rodea cómo MAPI controla las notificaciones para tipos específicos de controles.
  
|**Control**|**Acción de MAPI**|
|:-----|:-----|
|Botón  <br/> |Llama a [IMAPIProp::OpenProperty](imapiprop-openproperty.md)para recuperar el objeto de control mediante la propiedad representada por el miembro **ulPRControl** de la estructura [DTBLBUTTON](dtblbutton.md) si la llamada no había anteriormente. Las llamadas [IMAPIControl::GetState](imapicontrol-getstate.md) para determinar si el botón debe estar habilitado y habilita o deshabilita el botón según corresponda del objeto control.  <br/> |
|Casilla  <br/> |Vuelve a leer el valor para el miembro **ulPRPropertyName** .  <br/> |
|Cuadro combinado  <br/> |Vuelve a abrir la tabla asociada con el miembro **ulPRTableName** de la estructura [DTBLCOMBOBOX](dtblcombobox.md) . Vuelve a leer todas las filas, incluidos el valor para el miembro **ulPRPropertyName**.  <br/> |
|Cuadro de lista desplegable  <br/> |Vuelve a abrir la tabla asociada con el miembro **ulPRTableName** de la estructura [DTBLDDLBX](dtblddlbx.md) y vuelve a leer todas las filas. Llama a [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar los valores de las propiedades almacenadas en el **ulPRDisplayProperty** y los miembros de **ulPRSetProperty** .  <br/> |
|Edit  <br/> |Vuelve a leer la propiedad y vuelve a mostrar.  <br/> |
|Cuadro de grupo  <br/> |Pasa por alto la notificación.  <br/> |
|Etiqueta  <br/> |Pasa por alto la notificación.  <br/> |
|Cuadro de lista de selección múltiple  <br/> |Si una de las columnas es un identificador de entrada, actualiza el cuadro de lista. El objeto correspondiente no está cerrado o se vuelve a cargar.  <br/> |
|Cuadro de lista de selección única  <br/> |Lee la propiedad set, intenta identificarla.  <br/> |
|Cuadro de lista multivalor  <br/> |Vuelve a leer la propiedad y rellena el cuadro de lista.  <br/> |
|Página con fichas  <br/> |No hay ninguna notificación de este control; todo el contenido es estático.  <br/> |
|Botón de opción  <br/> |Vuelve a leer la propiedad que está asociada con el botón y se almacena en el miembro **ulPropTag** de la estructura [DTBLRADIOBUTTON](dtblradiobutton.md) y hace que la selección apropiada con los controles.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales

- [Tablas MAPI](mapi-tables.md)

