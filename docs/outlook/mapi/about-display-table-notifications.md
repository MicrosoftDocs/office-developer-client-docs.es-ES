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
ms.openlocfilehash: a696357c97a85442bbfd5532892c06d570f6367c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816353"
---
# <a name="about-display-table-notifications"></a><span data-ttu-id="f003b-103">Acerca de las notificaciones de tabla para mostrar</span><span class="sxs-lookup"><span data-stu-id="f003b-103">About display table notifications</span></span>

<span data-ttu-id="f003b-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f003b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f003b-105">En una tabla para mostrar se envían por el proveedor de servicio responsable de la creación de la tabla para mostrar de MAPI.</span><span class="sxs-lookup"><span data-stu-id="f003b-105">Notifications on a display table are sent by the service provider responsible for creating the display table to MAPI.</span></span> <span data-ttu-id="f003b-106">MAPI se registra para estas notificaciones al llamar al método [IMAPITable::Advise](imapitable-advise.md) de una tabla para mostrar y especificar el evento de modificación de tabla.</span><span class="sxs-lookup"><span data-stu-id="f003b-106">MAPI registers for these notifications by calling a display table's [IMAPITable::Advise](imapitable-advise.md) method and specifying the table modified event.</span></span> 
  
<span data-ttu-id="f003b-107">Al igual que con todas las notificaciones de tabla, mostrar notificaciones de tabla incluyen la estructura de [TABLE_NOTIFICATION](table_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="f003b-107">As with all table notifications, display table notifications include a [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> <span data-ttu-id="f003b-108">El **ulTableEvent** y los miembros de **propIndex** de esta estructura son significativos; se omiten los demás miembros.</span><span class="sxs-lookup"><span data-stu-id="f003b-108">Only the **ulTableEvent** and the **propIndex** members of this structure are significant; the other members are ignored.</span></span> <span data-ttu-id="f003b-109">El miembro **ulTableEvent** está establecido en TABLE_ROW_MODIFIED y el miembro **propIndex** se establece en el valor de la columna **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) en la fila correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f003b-109">The **ulTableEvent** member is set to TABLE_ROW_MODIFIED and the **propIndex** member is set to the value of the **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) column in the corresponding row.</span></span> <span data-ttu-id="f003b-110">MAPI se responde a la notificación llamando al método [IMAPIProp::GetProps](imapiprop-getprops.md) para la propiedad que se muestra en el control y mostrando el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="f003b-110">MAPI responds to the notification by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method for the property displayed in the control and by displaying the new value.</span></span> 
  
<span data-ttu-id="f003b-111">Mostrar notificaciones de tabla se pueden usar un proveedor de servicios para coordinar los cambios realizados en los controles relacionados en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f003b-111">Display table notifications can be used by a service provider to coordinate changes to related controls on the dialog box.</span></span> <span data-ttu-id="f003b-112">Por ejemplo, si la implementación de la interfaz de la propiedad tiene que actualizar uno o más campos en el cuadro de diálogo, quizás como respuesta a otro control que se ha establecido el indicador DT_SET_IMMEDIATE en su propiedad **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)): puede generar una notificación de la tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="f003b-112">For example, if the property interface implementation needs to refresh one or more fields on the dialog box — perhaps in response to another control that has set the DT_SET_IMMEDIATE flag in its **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property — it can generate a display table notification.</span></span> <span data-ttu-id="f003b-113">Una notificación de la tabla para mostrar puede alertar a la implementación de la interfaz de propiedad que necesita el valor de uno o varios controles a leer debido a realizar un cambio o que se produzca un evento externo.</span><span class="sxs-lookup"><span data-stu-id="f003b-113">A display table notification can alert the property interface implementation that the value of one or more controls needs to be reread due to a change being made or an external event occurring.</span></span> 
  
<span data-ttu-id="f003b-114">Un proveedor de servicios puede emitir notificaciones de tabla para mostrar por:</span><span class="sxs-lookup"><span data-stu-id="f003b-114">A service provider can issue display table notifications by:</span></span>
  
- <span data-ttu-id="f003b-115">Al llamar a [ITableData::HrNotify](itabledata-hrnotify.md), si se creó la tabla para mostrar con un objeto de datos de tabla.</span><span class="sxs-lookup"><span data-stu-id="f003b-115">Calling [ITableData::HrNotify](itabledata-hrnotify.md), if the display table was built with a table data object.</span></span>
    
    - <span data-ttu-id="f003b-116">O bien -</span><span class="sxs-lookup"><span data-stu-id="f003b-116">Or -</span></span>
    
- <span data-ttu-id="f003b-117">Uso de su propio código, si se creó la tabla para mostrar con la implementación del proveedor **IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="f003b-117">Using its own code, if the display table was built with the provider's **IMAPITable** implementation.</span></span> 
    
<span data-ttu-id="f003b-118">MAPI responde para mostrar las notificaciones de tabla cuando sea necesario volver a leer un valor del control de la implementación de la interfaz de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="f003b-118">MAPI responds to display table notifications when necessary by rereading a control's value from the property interface implementation.</span></span> <span data-ttu-id="f003b-119">En la siguiente tabla se describe los detalles que lo rodea cómo MAPI controla las notificaciones para tipos específicos de controles.</span><span class="sxs-lookup"><span data-stu-id="f003b-119">The following table describes the details surrounding how MAPI handles notifications for specific types of controls.</span></span>
  
|<span data-ttu-id="f003b-120">**Control**</span><span class="sxs-lookup"><span data-stu-id="f003b-120">**Control**</span></span>|<span data-ttu-id="f003b-121">**Acción de MAPI**</span><span class="sxs-lookup"><span data-stu-id="f003b-121">**MAPI action**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f003b-122">Botón</span><span class="sxs-lookup"><span data-stu-id="f003b-122">Button</span></span>  <br/> |<span data-ttu-id="f003b-123">Llama a [IMAPIProp::OpenProperty](imapiprop-openproperty.md)para recuperar el objeto de control mediante la propiedad representada por el miembro **ulPRControl** de la estructura [DTBLBUTTON](dtblbutton.md) si la llamada no había anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f003b-123">Calls [IMAPIProp::OpenProperty](imapiprop-openproperty.md)to retrieve the control object by way of the property represented by the **ulPRControl** member of the [DTBLBUTTON](dtblbutton.md) structure if the call had failed previously.</span></span> <span data-ttu-id="f003b-124">Las llamadas [IMAPIControl::GetState](imapicontrol-getstate.md) para determinar si el botón debe estar habilitado y habilita o deshabilita el botón según corresponda del objeto control.</span><span class="sxs-lookup"><span data-stu-id="f003b-124">Calls the control object's [IMAPIControl::GetState](imapicontrol-getstate.md) to determine whether the button should be enabled and enables or disables the button accordingly.</span></span>  <br/> |
|<span data-ttu-id="f003b-125">Casilla</span><span class="sxs-lookup"><span data-stu-id="f003b-125">Check box</span></span>  <br/> |<span data-ttu-id="f003b-126">Vuelve a leer el valor para el miembro **ulPRPropertyName** .</span><span class="sxs-lookup"><span data-stu-id="f003b-126">Rereads the value for the **ulPRPropertyName** member.</span></span>  <br/> |
|<span data-ttu-id="f003b-127">Cuadro combinado</span><span class="sxs-lookup"><span data-stu-id="f003b-127">Combo box</span></span>  <br/> |<span data-ttu-id="f003b-128">Vuelve a abrir la tabla asociada con el miembro **ulPRTableName** de la estructura [DTBLCOMBOBOX](dtblcombobox.md) .</span><span class="sxs-lookup"><span data-stu-id="f003b-128">Reopens the table associated with the **ulPRTableName** member of the [DTBLCOMBOBOX](dtblcombobox.md) structure.</span></span> <span data-ttu-id="f003b-129">Vuelve a leer todas las filas, incluidos el valor para el miembro **ulPRPropertyName**.</span><span class="sxs-lookup"><span data-stu-id="f003b-129">Rereads all of the rows including the value for the **ulPRPropertyName**member.</span></span>  <br/> |
|<span data-ttu-id="f003b-130">Cuadro de lista desplegable</span><span class="sxs-lookup"><span data-stu-id="f003b-130">Drop-down list box</span></span>  <br/> |<span data-ttu-id="f003b-131">Vuelve a abrir la tabla asociada con el miembro **ulPRTableName** de la estructura [DTBLDDLBX](dtblddlbx.md) y vuelve a leer todas las filas.</span><span class="sxs-lookup"><span data-stu-id="f003b-131">Reopens the table associated with the **ulPRTableName** member of the [DTBLDDLBX](dtblddlbx.md) structure and rereads all of the rows.</span></span> <span data-ttu-id="f003b-132">Llama a [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar los valores de las propiedades almacenadas en el **ulPRDisplayProperty** y los miembros de **ulPRSetProperty** .</span><span class="sxs-lookup"><span data-stu-id="f003b-132">Calls [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve the values for the properties stored in the **ulPRDisplayProperty** and the **ulPRSetProperty** members.</span></span>  <br/> |
|<span data-ttu-id="f003b-133">Edit</span><span class="sxs-lookup"><span data-stu-id="f003b-133">Edit</span></span>  <br/> |<span data-ttu-id="f003b-134">Vuelve a leer la propiedad y vuelve a mostrar.</span><span class="sxs-lookup"><span data-stu-id="f003b-134">Rereads the property and redisplays.</span></span>  <br/> |
|<span data-ttu-id="f003b-135">Cuadro de grupo</span><span class="sxs-lookup"><span data-stu-id="f003b-135">Group box</span></span>  <br/> |<span data-ttu-id="f003b-136">Pasa por alto la notificación.</span><span class="sxs-lookup"><span data-stu-id="f003b-136">Ignores the notification.</span></span>  <br/> |
|<span data-ttu-id="f003b-137">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="f003b-137">Label</span></span>  <br/> |<span data-ttu-id="f003b-138">Pasa por alto la notificación.</span><span class="sxs-lookup"><span data-stu-id="f003b-138">Ignores the notification.</span></span>  <br/> |
|<span data-ttu-id="f003b-139">Cuadro de lista de selección múltiple</span><span class="sxs-lookup"><span data-stu-id="f003b-139">Multiple selection list box</span></span>  <br/> |<span data-ttu-id="f003b-140">Si una de las columnas es un identificador de entrada, actualiza el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="f003b-140">If one of the columns is an entry identifier, refreshes the list box.</span></span> <span data-ttu-id="f003b-141">El objeto correspondiente no está cerrado o se vuelve a cargar.</span><span class="sxs-lookup"><span data-stu-id="f003b-141">The corresponding object is not closed or reloaded.</span></span>  <br/> |
|<span data-ttu-id="f003b-142">Cuadro de lista de selección única</span><span class="sxs-lookup"><span data-stu-id="f003b-142">Single selection list box</span></span>  <br/> |<span data-ttu-id="f003b-143">Lee la propiedad set, intenta identificarla.</span><span class="sxs-lookup"><span data-stu-id="f003b-143">Reads the set property, trying to identify it.</span></span>  <br/> |
|<span data-ttu-id="f003b-144">Cuadro de lista multivalor</span><span class="sxs-lookup"><span data-stu-id="f003b-144">Multivalued list box</span></span>  <br/> |<span data-ttu-id="f003b-145">Vuelve a leer la propiedad y rellena el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="f003b-145">Rereads the property and repopulates the list box.</span></span>  <br/> |
|<span data-ttu-id="f003b-146">Página con fichas</span><span class="sxs-lookup"><span data-stu-id="f003b-146">Tabbed page</span></span>  <br/> |<span data-ttu-id="f003b-147">No hay ninguna notificación de este control; todo el contenido es estático.</span><span class="sxs-lookup"><span data-stu-id="f003b-147">There are no notifications for this control; everything is static.</span></span>  <br/> |
|<span data-ttu-id="f003b-148">Botón de opción</span><span class="sxs-lookup"><span data-stu-id="f003b-148">Radio button</span></span>  <br/> |<span data-ttu-id="f003b-149">Vuelve a leer la propiedad que está asociada con el botón y se almacena en el miembro **ulPropTag** de la estructura [DTBLRADIOBUTTON](dtblradiobutton.md) y hace que la selección apropiada con los controles.</span><span class="sxs-lookup"><span data-stu-id="f003b-149">Rereads the property that is associated with the button and is stored in the **ulPropTag** member of the [DTBLRADIOBUTTON](dtblradiobutton.md) structure and makes the appropriate selection with the controls.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f003b-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="f003b-150">See also</span></span>

- [<span data-ttu-id="f003b-151">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="f003b-151">MAPI Tables</span></span>](mapi-tables.md)
