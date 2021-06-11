---
title: Implementación de hoja de propiedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f3475206-0237-4b5b-8efd-abd5d5e0b6c3
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3f1c6497a182231645691f669d8900d33b495503
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430052"
---
# <a name="property-sheet-implementation"></a><span data-ttu-id="dd695-103">Implementación de hoja de propiedades</span><span class="sxs-lookup"><span data-stu-id="dd695-103">Property Sheet Implementation</span></span>

  
  
<span data-ttu-id="dd695-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd695-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd695-105">Una hoja de propiedades es un cuadro de diálogo para mostrar las propiedades de un objeto.</span><span class="sxs-lookup"><span data-stu-id="dd695-105">A property sheet is a dialog box for displaying the properties of an object.</span></span> <span data-ttu-id="dd695-106">Las propiedades pueden ser de solo lectura, lo que permite que el usuario solo las vea, o de lectura y escritura, lo que permite al usuario realizar cambios.</span><span class="sxs-lookup"><span data-stu-id="dd695-106">The properties can be read-only, enabling the user only to view them, or read/write, enabling the user to make changes.</span></span> <span data-ttu-id="dd695-107">Una hoja de propiedades contiene una o más ventanas secundarias superpuestas denominadas páginas.</span><span class="sxs-lookup"><span data-stu-id="dd695-107">A property sheet contains one or more overlapping child windows called pages.</span></span> <span data-ttu-id="dd695-108">Cada página contiene ventanas de control para establecer un grupo de propiedades relacionadas.</span><span class="sxs-lookup"><span data-stu-id="dd695-108">Each page contains control windows for setting a group of related properties.</span></span> <span data-ttu-id="dd695-109">Los usuarios navegan de una página a otra seleccionando una pestaña que lleva la página correspondiente al primer plano de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="dd695-109">Users navigate from page to page by selecting a tab that brings the corresponding page to the foreground of the property sheet.</span></span>
  
<span data-ttu-id="dd695-110">Los proveedores de servicios deben implementar una hoja de propiedades que muestre un conjunto mínimo de propiedades relacionadas con la configuración en el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="dd695-110">Service providers must implement a property sheet that displays a minimal set of properties related to configuration in the message service.</span></span> <span data-ttu-id="dd695-111">Si permite que se cambien estas propiedades del servicio de mensajes, puede permitir que los usuarios de aplicaciones cliente, como el Panel de control, realicen los cambios o implementen los cambios mediante programación.</span><span class="sxs-lookup"><span data-stu-id="dd695-111">If you allow these message service properties to be changed, you can either allow users of client applications, such as the Control Panel, to make the changes or implement the changes programmatically.</span></span> <span data-ttu-id="dd695-112">La implementación de hojas de propiedades para mostrar y editar otros tipos de propiedades es opcional.</span><span class="sxs-lookup"><span data-stu-id="dd695-112">Implementing property sheets to display and edit other types of properties is optional.</span></span> 
  
<span data-ttu-id="dd695-113">Normalmente, deberá mostrar una hoja de propiedades en las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="dd695-113">Typically, you will need to display a property sheet in the following situations:</span></span>
  
- <span data-ttu-id="dd695-114">Cuando un cliente llama al método [IMAPIStatus::SettingsDialog del](imapistatus-settingsdialog.md) objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="dd695-114">When a client calls your status object's [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method.</span></span> 
    
- <span data-ttu-id="dd695-115">Cuando MAPI llama al método de inicio de sesión del objeto de proveedor.</span><span class="sxs-lookup"><span data-stu-id="dd695-115">When MAPI calls your provider object's logon method.</span></span>
    
- <span data-ttu-id="dd695-116">Cuando MAPI llama a la función de punto de entrada del servicio de mensajes del proveedor.</span><span class="sxs-lookup"><span data-stu-id="dd695-116">When MAPI calls the entry point function for your provider's message service.</span></span>
    
<span data-ttu-id="dd695-117">Los proveedores de transporte también implementan hojas de propiedades para mostrar propiedades relacionadas con las opciones de mensaje y los proveedores de libreta de direcciones implementan hojas de propiedades para ver y editar información detallada sobre los usuarios de mensajería y las listas de distribución, los criterios de búsqueda avanzados y las plantillas para introducir nuevos usuarios.</span><span class="sxs-lookup"><span data-stu-id="dd695-117">Transport providers also implement property sheets to display properties related to message options, and address book providers implement property sheets to view and edit detailed information about messaging users and distribution lists, advanced search criteria, and templates for entering new users.</span></span>
  
<span data-ttu-id="dd695-118">Puede usar una de las tres técnicas siguientes para crear una hoja de propiedades:</span><span class="sxs-lookup"><span data-stu-id="dd695-118">You can use one of the following three techniques to create a property sheet:</span></span>
  
- <span data-ttu-id="dd695-119">Manualmente, como cualquier cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="dd695-119">Manually, as you would any dialog box.</span></span>
    
- <span data-ttu-id="dd695-120">Mediante el uso del control común de hoja de propiedades proporcionado en el SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="dd695-120">By using the property sheet common control provided in the Windows SDK.</span></span>
    
- <span data-ttu-id="dd695-121">Mediante una tabla para mostrar MAPI.</span><span class="sxs-lookup"><span data-stu-id="dd695-121">By using a MAPI display table.</span></span>
    
<span data-ttu-id="dd695-122">Los proveedores deben elegir la última opción (crear una hoja de propiedades mediante una tabla para mostrar).</span><span class="sxs-lookup"><span data-stu-id="dd695-122">Providers should choose the last option (create a property sheet by using a display table).</span></span> <span data-ttu-id="dd695-123">Esta es la opción más sencilla porque elimina la necesidad de trabajar con la interfaz Windows usuario.</span><span class="sxs-lookup"><span data-stu-id="dd695-123">This is the simplest option because it eliminates the need to work with the Windows user interface.</span></span> 
  
<span data-ttu-id="dd695-124">Para implementar una hoja de propiedades creada a partir de una tabla para mostrar para las propiedades del servicio de mensajes, use el siguiente procedimiento:</span><span class="sxs-lookup"><span data-stu-id="dd695-124">To implement a property sheet built from a display table for your message service properties, use the following procedure:</span></span>
  
1. <span data-ttu-id="dd695-125">Llame [a IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para abrir una sección en el perfil actual.</span><span class="sxs-lookup"><span data-stu-id="dd695-125">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) to open a section in the current profile.</span></span> <span data-ttu-id="dd695-126">Pase [mapiuid](mapiuid.md) o null para abrir la sección de perfil del proveedor.</span><span class="sxs-lookup"><span data-stu-id="dd695-126">Pass your [MAPIUID](mapiuid.md) or NULL to open your provider's profile section.</span></span> 
    
2. <span data-ttu-id="dd695-127">Llame [a CreateIProp para](createiprop.md) crear un objeto de datos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="dd695-127">Call [CreateIProp](createiprop.md) to create a property data object.</span></span> 
    
3. <span data-ttu-id="dd695-128">Llame al método [IMAPIProp::CopyTo](imapiprop-copyto.md) de la sección de perfil para copiar todas las propiedades de la sección en el objeto de datos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="dd695-128">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy all of the section's properties to the property data object.</span></span> 
    
4. <span data-ttu-id="dd695-129">Cree una tabla para mostrar creando una o varias estructuras [DTPAGE](dtpage.md) que describen los controles que aparecen en la hoja de propiedades y llamando a la [función BuildDisplayTable,](builddisplaytable.md) o implementando código personalizado.</span><span class="sxs-lookup"><span data-stu-id="dd695-129">Create a display table either by building one or more [DTPAGE](dtpage.md) structures that describe the controls to appear on the property sheet and calling the [BuildDisplayTable](builddisplaytable.md) function, or by implementing custom code.</span></span> 
    
5. <span data-ttu-id="dd695-130">Llame a [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) para mostrar una hoja de propiedades que tenga las propiedades copiadas.</span><span class="sxs-lookup"><span data-stu-id="dd695-130">Call [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) to display a property sheet that has the copied properties.</span></span> <span data-ttu-id="dd695-131">Pase un puntero al objeto de datos de propiedad como el parámetro _lpConfigData_ y un puntero a la tabla para mostrar como el _parámetro lpDisplayTable._</span><span class="sxs-lookup"><span data-stu-id="dd695-131">Pass a pointer to the property data object as the  _lpConfigData_ parameter and a pointer to the display table as the  _lpDisplayTable_ parameter.</span></span> <span data-ttu-id="dd695-132">Si desea invalidar el modo de acceso predeterminado para esta hoja de propiedades, no establezca la marca DT_EDITABLE para cada control de la tabla para mostrar que representa una propiedad de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dd695-132">If you want to override the default access mode for this property sheet, do not set the DT_EDITABLE flag for each control in the display table that represents a read-only property.</span></span> 
    
6. <span data-ttu-id="dd695-133">Cuando se hayan realizado todos los cambios en la hoja de propiedades, llame al método **IMAPIProp::CopyTo** del objeto de datos de propiedad para copiar las propiedades modificadas de nuevo en la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="dd695-133">When all of the changes have been made in the property sheet, call the property data object's **IMAPIProp::CopyTo** method to copy the changed properties back to the profile section.</span></span> 
    
<span data-ttu-id="dd695-134">Para obtener información general sobre las tablas para mostrar, vea [Tablas para mostrar.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="dd695-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> 
  
<span data-ttu-id="dd695-135">Para obtener información detallada acerca de las tablas para mostrar, vea [Display Table Implementation](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="dd695-135">For detailed information about display tables, see [Display Table Implementation](display-table-implementation.md).</span></span> 
  
<span data-ttu-id="dd695-136">Para obtener información sobre cómo implementar un control, vea [Control Object Implementation](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="dd695-136">For information about implementing a control, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
<span data-ttu-id="dd695-137">Para recuperar el índice de un control que un usuario selecciona en un cuadro de lista de tabla para mostrar, espere hasta que el usuario haga clic en **Aceptar** o **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="dd695-137">To retrieve the index of a control that a user selects in a display table list box, wait until the user clicks **OK** or **Apply**.</span></span> <span data-ttu-id="dd695-138">En este momento, el identificador de entrada del elemento seleccionado se escribe de nuevo en la interfaz [IMAPIProp : IUnknown](imapipropiunknown.md) como el valor de la propiedad especificada por el miembro **ulPRSetProperty** en la estructura [DTBLLBX.](dtbllbx.md)</span><span class="sxs-lookup"><span data-stu-id="dd695-138">At this point, the entry identifier of the selected item is written back to the [IMAPIProp : IUnknown](imapipropiunknown.md) interface as the value of the property specified by the **ulPRSetProperty** member in the [DTBLLBX](dtbllbx.md) structure.</span></span> 
  
<span data-ttu-id="dd695-139">Si necesita poder agregar o quitar elementos del cuadro de lista, el uso de una tabla para mostrar y el método [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) no funcionarán.</span><span class="sxs-lookup"><span data-stu-id="dd695-139">If you need to be able to add or remove items from your list box, using a display table and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method will not work.</span></span> <span data-ttu-id="dd695-140">En su lugar, considere la posibilidad de implementar una hoja de propiedades con la API de hoja de propiedades de Win32 incluida en el comdlg32.dll archivo.</span><span class="sxs-lookup"><span data-stu-id="dd695-140">Instead, consider implementing a property sheet with the Win32 property sheet API contained in the comdlg32.dll file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dd695-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd695-141">See also</span></span>



[<span data-ttu-id="dd695-142">Proveedores de servicios MAPI</span><span class="sxs-lookup"><span data-stu-id="dd695-142">MAPI Service Providers</span></span>](mapi-service-providers.md)

