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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430017"
---
# <a name="about-display-table-notifications"></a>Información sobre las notificaciones de tabla para mostrar

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las notificaciones de una tabla para mostrar las envía el proveedor de servicios responsable de crear la tabla para mostrar a MAPI. MAPI se registra para estas notificaciones llamando al método [IMAPITable::Advise](imapitable-advise.md) de una tabla para mostrar y especificando el evento modificado de tabla. 
  
Al igual que con todas las notificaciones de tabla, las notificaciones de tabla para mostrar incluyen [TABLE_NOTIFICATION](table_notification.md) estructura. Solo los **miembros ulTableEvent** y **propIndex** de esta estructura son significativos; se omiten los demás miembros. El **miembro ulTableEvent** se establece en TABLE_ROW_MODIFIED y el miembro **propIndex** se establece en el valor de la columna **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) de la fila correspondiente. MAPI responde a la notificación llamando al método [IMAPIProp::GetProps](imapiprop-getprops.md) para la propiedad mostrada en el control y mostrando el nuevo valor. 
  
Un proveedor de servicios puede usar las notificaciones de tabla para coordinar los cambios en los controles relacionados en el cuadro de diálogo. Por ejemplo, si la implementación de la interfaz de propiedades necesita actualizar uno o más campos en el cuadro de diálogo , quizás en respuesta a otro control que ha establecido la marca DT_SET_IMMEDIATE en su propiedad **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)), puede generar una notificación de tabla de visualización. Una notificación de tabla de visualización puede alertar a la implementación de la interfaz de propiedades de que el valor de uno o varios controles debe volver a leerse debido a un cambio que se está haciendo o a un evento externo. 
  
Un proveedor de servicios puede emitir notificaciones de tabla de visualización mediante:
  
- Llamar [a ITableData::HrNotify](itabledata-hrnotify.md), si la tabla para mostrar se creó con un objeto de datos de tabla.
    
    - O bien:
    
- Con su propio código, si la tabla para mostrar se creó con la **implementación imapitable del** proveedor. 
    
MAPI responde a las notificaciones de la tabla cuando es necesario mediante la relección del valor de un control desde la implementación de la interfaz de propiedades. En la tabla siguiente se describen los detalles que rodean cómo MAPI controla las notificaciones para tipos específicos de controles.
  
|**Control**|**Acción MAPI**|
|:-----|:-----|
|Botón  <br/> |Llama [a IMAPIProp::OpenProperty](imapiprop-openproperty.md)para recuperar el objeto de control por medio de la propiedad representada por el **miembro ulPRControl** de la estructura [DTBLBUTTON](dtblbutton.md) si la llamada había fallado anteriormente. Llama al [IMAPIControl::GetState](imapicontrol-getstate.md) del objeto de control para determinar si el botón debe habilitarse y habilitar o deshabilitar el botón en consecuencia.  <br/> |
|Casilla  <br/> |Vuelve a leer el valor del **miembro ulPRPropertyName.**  <br/> |
|Cuadro combinado  <br/> |Vuelve a abrir la tabla asociada con **el miembro ulPRTableName** de la [estructura DTBLCOMBOBOX.](dtblcombobox.md) Vuelve a leer todas las filas, incluido el valor del **miembro ulPRPropertyName.**  <br/> |
|Cuadro de lista desplegable  <br/> |Vuelve a abrir la tabla asociada con el **miembro ulPRTableName** de la estructura [DTBLDDLBX](dtblddlbx.md) y vuelve a leer todas las filas. Llama [a IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar los valores de las propiedades almacenadas en los miembros **ulPRDisplayProperty** y **ulPRSetProperty.**  <br/> |
|Editar  <br/> |Vuelve a leer la propiedad y vuelve a mostrarla.  <br/> |
|Cuadro de grupo  <br/> |Omite la notificación.  <br/> |
|Etiqueta  <br/> |Omite la notificación.  <br/> |
|Cuadro de lista de selección múltiple  <br/> |Si una de las columnas es un identificador de entrada, actualiza el cuadro de lista. El objeto correspondiente no se cierra ni se vuelve a cargar.  <br/> |
|Cuadro de lista de selección única  <br/> |Lee la propiedad set e intenta identificarla.  <br/> |
|Cuadro de lista multivalor  <br/> |Vuelve a leer la propiedad y vuelve a llenar el cuadro de lista.  <br/> |
|Página con pestañas  <br/> |No hay notificaciones para este control; todo es estático.  <br/> |
|Botón de radio  <br/> |Vuelve a leer la propiedad asociada con el botón y se almacena en el **miembro ulPropTag** de la estructura [DTBLRADIOBUTTON](dtblradiobutton.md) y realiza la selección adecuada con los controles.  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Tablas MAPI](mapi-tables.md)

