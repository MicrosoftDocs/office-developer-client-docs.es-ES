---
title: Implementación de la hoja de propiedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f3475206-0237-4b5b-8efd-abd5d5e0b6c3
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9a0fad8fa20b2d94077f9fbdf8a3c595c0ab219e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580869"
---
# <a name="property-sheet-implementation"></a><span data-ttu-id="841c4-103">Implementación de la hoja de propiedades</span><span class="sxs-lookup"><span data-stu-id="841c4-103">Property Sheet Implementation</span></span>

  
  
<span data-ttu-id="841c4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="841c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="841c4-105">Una hoja de propiedades es un cuadro de diálogo para mostrar las propiedades de un objeto.</span><span class="sxs-lookup"><span data-stu-id="841c4-105">A property sheet is a dialog box for displaying the properties of an object.</span></span> <span data-ttu-id="841c4-106">Las propiedades pueden ser de sólo lectura, permitiendo al usuario sólo ver, o lectura y escritura, permitiendo al usuario realizar cambios.</span><span class="sxs-lookup"><span data-stu-id="841c4-106">The properties can be read-only, enabling the user only to view them, or read/write, enabling the user to make changes.</span></span> <span data-ttu-id="841c4-107">Una hoja de propiedades contiene una o varias ventanas secundarias superpuestas denominadas páginas.</span><span class="sxs-lookup"><span data-stu-id="841c4-107">A property sheet contains one or more overlapping child windows called pages.</span></span> <span data-ttu-id="841c4-108">Cada página contiene el control de windows para la configuración de un grupo de propiedades relacionadas.</span><span class="sxs-lookup"><span data-stu-id="841c4-108">Each page contains control windows for setting a group of related properties.</span></span> <span data-ttu-id="841c4-109">Los usuarios desplazarse de una página a otra mediante la selección de una ficha que aporta la funcionalidad de la página correspondiente en el primer plano de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="841c4-109">Users navigate from page to page by selecting a tab that brings the corresponding page to the foreground of the property sheet.</span></span>
  
<span data-ttu-id="841c4-110">Proveedores de servicios deben implementar una hoja de propiedades que muestra un conjunto mínimo de propiedades relacionados con la configuración en el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="841c4-110">Service providers must implement a property sheet that displays a minimal set of properties related to configuration in the message service.</span></span> <span data-ttu-id="841c4-111">Si permite que se puede cambiar estas propiedades de servicio de mensaje, se pueden permitir que a los usuarios del cliente de aplicaciones, como el Panel de Control, debe realizar los cambios o implementar los cambios mediante programación.</span><span class="sxs-lookup"><span data-stu-id="841c4-111">If you allow these message service properties to be changed, you can either allow users of client applications, such as the Control Panel, to make the changes or implement the changes programmatically.</span></span> <span data-ttu-id="841c4-112">Implementación de las hojas de propiedades para mostrar y editar otros tipos de propiedades es opcional.</span><span class="sxs-lookup"><span data-stu-id="841c4-112">Implementing property sheets to display and edit other types of properties is optional.</span></span> 
  
<span data-ttu-id="841c4-113">Normalmente, se debe mostrar una hoja de propiedades en las situaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="841c4-113">Typically, you will need to display a property sheet in the following situations:</span></span>
  
- <span data-ttu-id="841c4-114">Cuando un cliente llama (método) [SettingsDialog](imapistatus-settingsdialog.md) del objeto de su estado.</span><span class="sxs-lookup"><span data-stu-id="841c4-114">When a client calls your status object's [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method.</span></span> 
    
- <span data-ttu-id="841c4-115">Cuando llama a método de inicio de sesión del objeto de su proveedor MAPI.</span><span class="sxs-lookup"><span data-stu-id="841c4-115">When MAPI calls your provider object's logon method.</span></span>
    
- <span data-ttu-id="841c4-116">Cuando MAPI llama a la función de punto de entrada para el servicio de mensajes de su proveedor.</span><span class="sxs-lookup"><span data-stu-id="841c4-116">When MAPI calls the entry point function for your provider's message service.</span></span>
    
<span data-ttu-id="841c4-117">Los proveedores de transporte también implementan las hojas de propiedades para mostrar las propiedades relacionadas con las opciones de mensajes, y los proveedores de la libreta de direcciones implementan las hojas de propiedades para ver y editar la información detallada acerca de la mensajería a los usuarios y las listas de distribución, búsqueda avanzada criterios y plantillas para escribir nuevos usuarios.</span><span class="sxs-lookup"><span data-stu-id="841c4-117">Transport providers also implement property sheets to display properties related to message options, and address book providers implement property sheets to view and edit detailed information about messaging users and distribution lists, advanced search criteria, and templates for entering new users.</span></span>
  
<span data-ttu-id="841c4-118">Puede usar una de las siguientes tres técnicas para crear una hoja de propiedades:</span><span class="sxs-lookup"><span data-stu-id="841c4-118">You can use one of the following three techniques to create a property sheet:</span></span>
  
- <span data-ttu-id="841c4-119">Manualmente, tal y como lo haría con cualquier cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="841c4-119">Manually, as you would any dialog box.</span></span>
    
- <span data-ttu-id="841c4-120">Con el control común de hoja de propiedad proporcionado en el SDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="841c4-120">By using the property sheet common control provided in the Windows SDK.</span></span>
    
- <span data-ttu-id="841c4-121">Si usa una MAPI Mostrar tabla.</span><span class="sxs-lookup"><span data-stu-id="841c4-121">By using a MAPI display table.</span></span>
    
<span data-ttu-id="841c4-122">Proveedores de deben elegir la opción última (crear una hoja de propiedades mediante el uso de una tabla para mostrar).</span><span class="sxs-lookup"><span data-stu-id="841c4-122">Providers should choose the last option (create a property sheet by using a display table).</span></span> <span data-ttu-id="841c4-123">Esta es la opción más sencilla, ya que elimina la necesidad de trabajar con la interfaz de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="841c4-123">This is the simplest option because it eliminates the need to work with the Windows user interface.</span></span> 
  
<span data-ttu-id="841c4-124">Para implementar una hoja de propiedades creada a partir de una tabla para mostrar para las propiedades del servicio de mensajes, use el procedimiento siguiente:</span><span class="sxs-lookup"><span data-stu-id="841c4-124">To implement a property sheet built from a display table for your message service properties, use the following procedure:</span></span>
  
1. <span data-ttu-id="841c4-125">Llame a [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para abrir una sección en el perfil actual.</span><span class="sxs-lookup"><span data-stu-id="841c4-125">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) to open a section in the current profile.</span></span> <span data-ttu-id="841c4-126">Pase el [MAPIUID](mapiuid.md) o NULL para abrir la sección de perfil de su proveedor.</span><span class="sxs-lookup"><span data-stu-id="841c4-126">Pass your [MAPIUID](mapiuid.md) or NULL to open your provider's profile section.</span></span> 
    
2. <span data-ttu-id="841c4-127">Llame a [CreateIProp](createiprop.md) para crear un objeto de datos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="841c4-127">Call [CreateIProp](createiprop.md) to create a property data object.</span></span> 
    
3. <span data-ttu-id="841c4-128">Llamar al método [IMAPIProp::CopyTo](imapiprop-copyto.md) de la sección de perfil para copiar todas las propiedades de la sección en el objeto de datos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="841c4-128">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy all of the section's properties to the property data object.</span></span> 
    
4. <span data-ttu-id="841c4-129">Crear una tabla para mostrar mediante la creación de una o más estructuras [DTPAGE](dtpage.md) que describen los controles para que aparezca en la hoja de propiedades y llamar a la función [BuildDisplayTable](builddisplaytable.md) o mediante la implementación de código personalizado.</span><span class="sxs-lookup"><span data-stu-id="841c4-129">Create a display table either by building one or more [DTPAGE](dtpage.md) structures that describe the controls to appear on the property sheet and calling the [BuildDisplayTable](builddisplaytable.md) function, or by implementing custom code.</span></span> 
    
5. <span data-ttu-id="841c4-130">Llame a [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) para mostrar una hoja de propiedades que tiene las propiedades copiadas.</span><span class="sxs-lookup"><span data-stu-id="841c4-130">Call [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) to display a property sheet that has the copied properties.</span></span> <span data-ttu-id="841c4-131">Pase un puntero al objeto de datos (propiedad) como el parámetro _lpConfigData_ y un puntero a la tabla para mostrar como el parámetro _lpDisplayTable_ .</span><span class="sxs-lookup"><span data-stu-id="841c4-131">Pass a pointer to the property data object as the  _lpConfigData_ parameter and a pointer to the display table as the  _lpDisplayTable_ parameter.</span></span> <span data-ttu-id="841c4-132">Si desea reemplazar el modo de acceso predeterminado para esta hoja de propiedades, no establezca la marca DT_EDITABLE para cada control en la tabla para mostrar que representa una propiedad de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="841c4-132">If you want to override the default access mode for this property sheet, do not set the DT_EDITABLE flag for each control in the display table that represents a read-only property.</span></span> 
    
6. <span data-ttu-id="841c4-133">Cuando todos los cambios se han realizado en la hoja de propiedades, llamar al método **IMAPIProp::CopyTo** del objeto de datos de propiedad para las propiedades modificadas volver a copiar la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="841c4-133">When all of the changes have been made in the property sheet, call the property data object's **IMAPIProp::CopyTo** method to copy the changed properties back to the profile section.</span></span> 
    
<span data-ttu-id="841c4-134">Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="841c4-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> 
  
<span data-ttu-id="841c4-135">Para obtener información detallada acerca de las tablas para mostrar, vea [Mostrar tabla de implementación](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="841c4-135">For detailed information about display tables, see [Display Table Implementation](display-table-implementation.md).</span></span> 
  
<span data-ttu-id="841c4-136">Para obtener información acerca de cómo implementar un control, vea [Implementación de objeto de Control](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="841c4-136">For information about implementing a control, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
<span data-ttu-id="841c4-137">Para recuperar el índice de un control que selecciona un usuario en un cuadro de lista de tabla para mostrar, espere hasta que el usuario hace clic en **Aceptar** o **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="841c4-137">To retrieve the index of a control that a user selects in a display table list box, wait until the user clicks **OK** or **Apply**.</span></span> <span data-ttu-id="841c4-138">En este momento, el identificador de entrada del elemento seleccionado se vuelve a escribir el [IMAPIProp: IUnknown](imapipropiunknown.md) interfaz como el valor de la propiedad especificada por el miembro **ulPRSetProperty** en la estructura [DTBLLBX](dtbllbx.md) .</span><span class="sxs-lookup"><span data-stu-id="841c4-138">At this point, the entry identifier of the selected item is written back to the [IMAPIProp : IUnknown](imapipropiunknown.md) interface as the value of the property specified by the **ulPRSetProperty** member in the [DTBLLBX](dtbllbx.md) structure.</span></span> 
  
<span data-ttu-id="841c4-139">Si necesita poder agregar o quitar elementos en el cuadro de lista, con una tabla para mostrar y con el método [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) no funcionará.</span><span class="sxs-lookup"><span data-stu-id="841c4-139">If you need to be able to add or remove items from your list box, using a display table and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method will not work.</span></span> <span data-ttu-id="841c4-140">En su lugar, considere la implementación de una hoja de propiedades con la API de Win32 (propiedad) hoja incluida en el archivo comdlg32.dll.</span><span class="sxs-lookup"><span data-stu-id="841c4-140">Instead, consider implementing a property sheet with the Win32 property sheet API contained in the comdlg32.dll file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="841c4-141">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="841c4-141">See also</span></span>



[<span data-ttu-id="841c4-142">Proveedores de servicios de MAPI</span><span class="sxs-lookup"><span data-stu-id="841c4-142">MAPI Service Providers</span></span>](mapi-service-providers.md)

