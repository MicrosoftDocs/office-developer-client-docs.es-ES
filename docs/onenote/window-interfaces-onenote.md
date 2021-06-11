---
title: Interfaces de ventana (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e6900ad7-c147-4816-93a9-5773170b115a
description: Las interfaces Window y Windows son OneNote api de 2013 que permite a los usuarios trabajar con OneNote windows. Estos objetos permiten a los usuarios enumerar a través del conjunto de ventanas de OneNote y modificar determinadas propiedades de la ventana.
ms.openlocfilehash: efc34312def588ecff54c63b3db84f8bf909352b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317041"
---
# <a name="window-interfaces-onenote"></a><span data-ttu-id="1ad75-104">Interfaces de ventana (OneNote)</span><span class="sxs-lookup"><span data-stu-id="1ad75-104">Window interfaces (OneNote)</span></span>

<span data-ttu-id="1ad75-105">Las **interfaces Window** **y Windows** son OneNote api de 2013 que permite a los usuarios trabajar con OneNote windows.</span><span class="sxs-lookup"><span data-stu-id="1ad75-105">The **Window** and **Windows** interfaces are OneNote 2013 API objects that enables users to work with OneNote windows.</span></span> <span data-ttu-id="1ad75-106">Estos objetos permiten a los usuarios enumerar a través del conjunto de ventanas de OneNote y modificar determinadas propiedades de la ventana.</span><span class="sxs-lookup"><span data-stu-id="1ad75-106">These objects allow users to enumerate through the set of OneNote windows and modify certain window properties.</span></span> 
  
## <a name="onenote-window-views"></a><span data-ttu-id="1ad75-107">Vistas de ventana de OneNote</span><span class="sxs-lookup"><span data-stu-id="1ad75-107">OneNote window views</span></span>

<span data-ttu-id="1ad75-108">En la lista siguiente se muestran los cuatro modos de vista que se pueden usar para OneNote ventanas:</span><span class="sxs-lookup"><span data-stu-id="1ad75-108">The following list shows the four view modes that you can use for OneNote windows:</span></span> 
  
- <span data-ttu-id="1ad75-109">Vista normal: muestra la ventana OneNote predeterminada en la que están visibles los paneles de navegación Bloc de notas y Página.</span><span class="sxs-lookup"><span data-stu-id="1ad75-109">Normal view—Displays the default OneNote window in which the Notebook and Page navigation panes are visible.</span></span>
    
- <span data-ttu-id="1ad75-110">Vista Página completa: muestra una vista de interfaz de usuario (UI) mínima en la que no se muestran los paneles Bloc de notas y Página.</span><span class="sxs-lookup"><span data-stu-id="1ad75-110">Full Page view—Displays a minimal user-interface (UI) view in which the Notebook and Page panes are not displayed.</span></span>
    
- <span data-ttu-id="1ad75-111">Nota rápida: muestra una pequeña ventana que permite a los usuarios tomar notas breves.</span><span class="sxs-lookup"><span data-stu-id="1ad75-111">Quick note—Displays a small window that allows users to take short notes.</span></span> <span data-ttu-id="1ad75-112">Normalmente, accedería a notas rápidas a través del icono OneNote en el área de  notificación de Windows, pero también puede acceder a ellas a través de la pestaña Ver en OneNote.</span><span class="sxs-lookup"><span data-stu-id="1ad75-112">You would usually access quick notes through the OneNote icon in the Windows notification area, but you can also access them through the **View** tab in OneNote.</span></span> 
    
- <span data-ttu-id="1ad75-113">Acoplar a escritorio: muestra una OneNote que puede acoplar a cualquier lado del escritorio (similar a la barra de tareas).</span><span class="sxs-lookup"><span data-stu-id="1ad75-113">Dock to Desktop—Displays a OneNote window that you can dock to any side of the desktop (similar to the taskbar).</span></span> <span data-ttu-id="1ad75-114">Esta vista reduce el tamaño del escritorio para que se ajuste a la ventana.</span><span class="sxs-lookup"><span data-stu-id="1ad75-114">This view reduces the size of the desktop to fit the window.</span></span> <span data-ttu-id="1ad75-115">Solo puede acoplar una ventana en cualquier momento y la ventana siempre está visible sin bloquear el escritorio.</span><span class="sxs-lookup"><span data-stu-id="1ad75-115">You can dock only one window at any time, and the window is always visible without blocking the desktop.</span></span> 
    
<span data-ttu-id="1ad75-116">En la siguiente figura se muestra el aspecto de la vista Página completa, la vista Acoplar a escritorio y las notas rápidas en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="1ad75-116">The following figure shows what the Full Page view, Dock to Desktop view, and quick notes look like on your desktop.</span></span>
  
<span data-ttu-id="1ad75-117">**Vistas de OneNote**</span><span class="sxs-lookup"><span data-stu-id="1ad75-117">**OneNote views**</span></span>

<span data-ttu-id="1ad75-118">![OneNote vistas de ventana OneNote]vistas de(media/ON15Con_views.jpg "ventana")</span><span class="sxs-lookup"><span data-stu-id="1ad75-118">![OneNote window views](media/ON15Con_views.jpg "OneNote window views")</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="1ad75-119">Interfaces</span><span class="sxs-lookup"><span data-stu-id="1ad75-119">Interfaces</span></span>

<span data-ttu-id="1ad75-120">En esta sección se enumeran las interfaces y los miembros que puede usar para modificar las OneNote mediante programación.</span><span class="sxs-lookup"><span data-stu-id="1ad75-120">This section lists the interfaces and members that you can use to modify OneNote windows programmatically.</span></span>
  
### <a name="windows-interface"></a><span data-ttu-id="1ad75-121">Windows interfaz</span><span class="sxs-lookup"><span data-stu-id="1ad75-121">Windows interface</span></span>

<span data-ttu-id="1ad75-122">La **Windows** permite al usuario tener acceso al conjunto de ventanas OneNote abiertas.</span><span class="sxs-lookup"><span data-stu-id="1ad75-122">The **Windows** interface allows the user to access the set of opened OneNote windows.</span></span> <span data-ttu-id="1ad75-123">Es una propiedad de la clase OneNote **Application,** a la que se accede a través **de Application.Windows**.</span><span class="sxs-lookup"><span data-stu-id="1ad75-123">It is a property of the OneNote **Application** class, accessed through **Application.Windows**.</span></span> <span data-ttu-id="1ad75-124">Esto devuelve el conjunto enumerado de OneNote ventanas.</span><span class="sxs-lookup"><span data-stu-id="1ad75-124">This returns the enumerated set of OneNote windows.</span></span> 
  
<span data-ttu-id="1ad75-125">**Properties**</span><span class="sxs-lookup"><span data-stu-id="1ad75-125">**Properties**</span></span>

|<span data-ttu-id="1ad75-126">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="1ad75-126">**Name**</span></span>|<span data-ttu-id="1ad75-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1ad75-127">**Type**</span></span>|<span data-ttu-id="1ad75-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1ad75-128">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1ad75-129">**Count**</span><span class="sxs-lookup"><span data-stu-id="1ad75-129">**Count**</span></span> <br/> |<span data-ttu-id="1ad75-130">ulong</span><span class="sxs-lookup"><span data-stu-id="1ad75-130">ulong</span></span>  <br/> |<span data-ttu-id="1ad75-131">Obtiene el número de **objetos Window** del **Windows** conjunto.</span><span class="sxs-lookup"><span data-stu-id="1ad75-131">Gets the number of **Window** objects in the **Windows** set.</span></span>  <br/> |
|<span data-ttu-id="1ad75-132">**CurrentWindow**</span><span class="sxs-lookup"><span data-stu-id="1ad75-132">**CurrentWindow**</span></span> <br/> |<span data-ttu-id="1ad75-133">**Window**</span><span class="sxs-lookup"><span data-stu-id="1ad75-133">**Window**</span></span> <br/> |<span data-ttu-id="1ad75-134">Obtiene el **objeto Window** de la ventana OneNote activa.</span><span class="sxs-lookup"><span data-stu-id="1ad75-134">Gets the **Window** object of the active OneNote window.</span></span>  <br/> |
|<span data-ttu-id="1ad75-135">**Items**</span><span class="sxs-lookup"><span data-stu-id="1ad75-135">**Items**</span></span> <br/> |<span data-ttu-id="1ad75-136">**Window**</span><span class="sxs-lookup"><span data-stu-id="1ad75-136">**Window**</span></span> <br/> |<span data-ttu-id="1ad75-137">Devuelve el **objeto Window** que corresponde al valor de índice pasado.</span><span class="sxs-lookup"><span data-stu-id="1ad75-137">Returns the **Window** object that corresponds to the index value passed.</span></span> <span data-ttu-id="1ad75-138">No se puede tener acceso a esta propiedad directamente.</span><span class="sxs-lookup"><span data-stu-id="1ad75-138">This property cannot be accessed directly.</span></span> <span data-ttu-id="1ad75-139">Para devolver un **objeto Window,** use **Windows [(uint) index]**.</span><span class="sxs-lookup"><span data-stu-id="1ad75-139">To return a **Window** object, use **Windows [(uint) index]**.</span></span>  <br/> |
   
### <a name="window-interface"></a><span data-ttu-id="1ad75-140">Interfaz de ventana</span><span class="sxs-lookup"><span data-stu-id="1ad75-140">Window interface</span></span>

<span data-ttu-id="1ad75-141">La **interfaz Window** permite al usuario tener acceso a determinadas propiedades de cada ventana.</span><span class="sxs-lookup"><span data-stu-id="1ad75-141">The **Window** interface allows the user to access certain properties of each window.</span></span> <span data-ttu-id="1ad75-142">Cada OneNote puede tener acceso enumerando a través de la **Windows** propiedad de la **clase Application.**</span><span class="sxs-lookup"><span data-stu-id="1ad75-142">Each OneNote window can be accessed by enumerating through the **Windows** property of the **Application** class.</span></span> 
  
<span data-ttu-id="1ad75-143">**Properties**</span><span class="sxs-lookup"><span data-stu-id="1ad75-143">**Properties**</span></span>

|<span data-ttu-id="1ad75-144">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="1ad75-144">**Name**</span></span>|<span data-ttu-id="1ad75-145">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1ad75-145">**Type**</span></span>|<span data-ttu-id="1ad75-146">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1ad75-146">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1ad75-147">**Active**</span><span class="sxs-lookup"><span data-stu-id="1ad75-147">**Active**</span></span> <br/> |<span data-ttu-id="1ad75-148">bool</span><span class="sxs-lookup"><span data-stu-id="1ad75-148">bool</span></span>  <br/> |<span data-ttu-id="1ad75-149">Obtiene o establece un valor que indica si la ventana es la ventana OneNote activa.</span><span class="sxs-lookup"><span data-stu-id="1ad75-149">Gets or sets a value that indicates whether the window is the active OneNote window.</span></span>  <br/> |
|<span data-ttu-id="1ad75-150">**Application**</span><span class="sxs-lookup"><span data-stu-id="1ad75-150">**Application**</span></span> <br/> |<span data-ttu-id="1ad75-151">**Application**</span><span class="sxs-lookup"><span data-stu-id="1ad75-151">**Application**</span></span> <br/> |<span data-ttu-id="1ad75-152">Obtiene el OneNote **application** asociado a la ventana.</span><span class="sxs-lookup"><span data-stu-id="1ad75-152">Gets the OneNote **Application** object that is associated with the window.</span></span>  <br/> |
|<span data-ttu-id="1ad75-153">**CurrentPageId**</span><span class="sxs-lookup"><span data-stu-id="1ad75-153">**CurrentPageId**</span></span> <br/> |<span data-ttu-id="1ad75-154">string</span><span class="sxs-lookup"><span data-stu-id="1ad75-154">string</span></span>  <br/> |<span data-ttu-id="1ad75-155">Obtiene el identificador de objeto de la página OneNote activa de la ventana.</span><span class="sxs-lookup"><span data-stu-id="1ad75-155">Gets the object ID of the active OneNote page of the window.</span></span>  <br/> |
|<span data-ttu-id="1ad75-156">**CurrentSectionId**</span><span class="sxs-lookup"><span data-stu-id="1ad75-156">**CurrentSectionId**</span></span> <br/> |<span data-ttu-id="1ad75-157">string</span><span class="sxs-lookup"><span data-stu-id="1ad75-157">string</span></span>  <br/> |<span data-ttu-id="1ad75-158">Obtiene el identificador de objeto de la OneNote de la ventana.</span><span class="sxs-lookup"><span data-stu-id="1ad75-158">Gets the object ID of the active OneNote section of the window.</span></span>  <br/> |
|<span data-ttu-id="1ad75-159">**CurrentSectionGroupId**</span><span class="sxs-lookup"><span data-stu-id="1ad75-159">**CurrentSectionGroupId**</span></span> <br/> |<span data-ttu-id="1ad75-160">string</span><span class="sxs-lookup"><span data-stu-id="1ad75-160">string</span></span>  <br/> |<span data-ttu-id="1ad75-161">Obtiene el identificador de objeto del grupo de OneNote de sección activo de la ventana.</span><span class="sxs-lookup"><span data-stu-id="1ad75-161">Gets the object ID of the active OneNote section group of the window.</span></span>  <br/> |
|<span data-ttu-id="1ad75-162">**CurrentNotebookId**</span><span class="sxs-lookup"><span data-stu-id="1ad75-162">**CurrentNotebookId**</span></span> <br/> |<span data-ttu-id="1ad75-163">string</span><span class="sxs-lookup"><span data-stu-id="1ad75-163">string</span></span>  <br/> |<span data-ttu-id="1ad75-164">Obtiene el identificador de objeto del bloc de notas OneNote activo de la ventana.</span><span class="sxs-lookup"><span data-stu-id="1ad75-164">Gets the object ID of the active OneNote notebook of the window.</span></span>  <br/> |
|<span data-ttu-id="1ad75-165">**DockedLocation**</span><span class="sxs-lookup"><span data-stu-id="1ad75-165">**DockedLocation**</span></span> <br/> |<span data-ttu-id="1ad75-166">**DockedLocation**</span><span class="sxs-lookup"><span data-stu-id="1ad75-166">**DockedLocation**</span></span> <br/> |<span data-ttu-id="1ad75-167">Obtiene o establece la ubicación acoplada de la OneNote ventana.</span><span class="sxs-lookup"><span data-stu-id="1ad75-167">Gets or sets the docked location of the OneNote window.</span></span>  <br/> |
|<span data-ttu-id="1ad75-168">**FullPageView**</span><span class="sxs-lookup"><span data-stu-id="1ad75-168">**FullPageView**</span></span> <br/> |<span data-ttu-id="1ad75-169">bool</span><span class="sxs-lookup"><span data-stu-id="1ad75-169">bool</span></span>  <br/> |<span data-ttu-id="1ad75-170">Obtiene o establece un valor que indica si la ventana está en la vista Página completa (vista de interfaz de usuario mínima).</span><span class="sxs-lookup"><span data-stu-id="1ad75-170">Gets or sets a value that indicates whether the window is in Full Page view (minimal UI view).</span></span>  <br/> |
|<span data-ttu-id="1ad75-171">**SideNote**</span><span class="sxs-lookup"><span data-stu-id="1ad75-171">**SideNote**</span></span> <br/> |<span data-ttu-id="1ad75-172">bool</span><span class="sxs-lookup"><span data-stu-id="1ad75-172">bool</span></span>  <br/> |<span data-ttu-id="1ad75-173">Obtiene o establece un valor que indica si la ventana es una ventana de nota rápida.</span><span class="sxs-lookup"><span data-stu-id="1ad75-173">Gets or sets a value that indicates whether the window is a quick note window.</span></span>  <br/> |
|<span data-ttu-id="1ad75-174">**WindowHandle**</span><span class="sxs-lookup"><span data-stu-id="1ad75-174">**WindowHandle**</span></span> <br/> |<span data-ttu-id="1ad75-175">ulong</span><span class="sxs-lookup"><span data-stu-id="1ad75-175">ulong</span></span>  <br/> |<span data-ttu-id="1ad75-176">Obtiene el identificador de identificador de la OneNote ventana.</span><span class="sxs-lookup"><span data-stu-id="1ad75-176">Gets the handle ID of the OneNote window.</span></span>  <br/> |
   
<span data-ttu-id="1ad75-177">**Métodos**</span><span class="sxs-lookup"><span data-stu-id="1ad75-177">**Methods**</span></span>
  
<span data-ttu-id="1ad75-178">Puede usar los siguientes métodos de la interfaz **Window** para navegar a objetos especificados en la ventana OneNote o a direcciones URL especificadas.</span><span class="sxs-lookup"><span data-stu-id="1ad75-178">You can use the following methods of the **Window** interface to navigate to specified objects in the OneNote window or to specified URLs.</span></span> 
  
<span data-ttu-id="1ad75-179">**NavigateTo**</span><span class="sxs-lookup"><span data-stu-id="1ad75-179">**NavigateTo**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ad75-180">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1ad75-180">**Description**</span></span> <br/> |<span data-ttu-id="1ad75-181">Navega hasta el objeto especificado en la OneNote ventana.</span><span class="sxs-lookup"><span data-stu-id="1ad75-181">Navigates to the specified object in the OneNote window.</span></span> <span data-ttu-id="1ad75-182">Por ejemplo, puede navegar a secciones, páginas y elementos de esquema dentro de las páginas.</span><span class="sxs-lookup"><span data-stu-id="1ad75-182">For example, you can navigate to sections, pages, and outline elements within pages.</span></span>  <br/> |
|<span data-ttu-id="1ad75-183">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="1ad75-183">**Syntax**</span></span> <br/> | <span data-ttu-id="1ad75-184">`HRESULT NavigateTo(`           ` [in]BSTR bstrHierarchyObjectID, `           ` [in]BSTR bstrObjectID); `</span><span class="sxs-lookup"><span data-stu-id="1ad75-184">`HRESULT NavigateTo(`           ` [in]BSTR bstrHierarchyObjectID, `           ` [in]BSTR bstrObjectID); `</span></span> <br/> |
|<span data-ttu-id="1ad75-185">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="1ad75-185">**Parameters**</span></span> <br/> | <span data-ttu-id="1ad75-186">_bstrHierarchyObjectID:_ la jerarquía OneNote identificador del objeto al que desea navegar.</span><span class="sxs-lookup"><span data-stu-id="1ad75-186">_bstrHierarchyObjectID_—The hierarchy OneNote ID of the object you want to navigate to.</span></span> <span data-ttu-id="1ad75-187">El identificador de objeto puede hacer referencia a OneNote bloc de notas, sección, grupo de secciones o página.</span><span class="sxs-lookup"><span data-stu-id="1ad75-187">The object ID can reference a OneNote notebook, section, section group, or page.</span></span>  <br/>  <span data-ttu-id="1ad75-188">_bstrObjectID:_ el OneNote identificador del objeto específico al que se va a navegar dentro de una OneNote página.</span><span class="sxs-lookup"><span data-stu-id="1ad75-188">_bstrObjectID_—The OneNote ID of the specific object to navigate to within a OneNote page.</span></span> <span data-ttu-id="1ad75-189">Si el usuario no desea navegar a un objeto específico de una página, este parámetro se establece en null.</span><span class="sxs-lookup"><span data-stu-id="1ad75-189">If the user does not want to navigate to a specific object on a page, this parameter is set to null.</span></span>  <br/> |
   
<span data-ttu-id="1ad75-190">**NavigateToUrl**</span><span class="sxs-lookup"><span data-stu-id="1ad75-190">**NavigateToUrl**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ad75-191">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1ad75-191">**Description**</span></span> <br/> |<span data-ttu-id="1ad75-192">Si se pasó un vínculo de OneNote (onenote://), se abrirá la ventana de OneNote en la ubicación correspondiente en OneNote.</span><span class="sxs-lookup"><span data-stu-id="1ad75-192">If passed a OneNote link (onenote://), opens the OneNote window to the corresponding location in OneNote.</span></span> <span data-ttu-id="1ad75-193">Sin embargo, si el vínculo es un vínculo externo, como https:// o file://, aparecerá un cuadro de diálogo de seguridad.</span><span class="sxs-lookup"><span data-stu-id="1ad75-193">However, if the link is an external link, such as https:// or file://, a security dialog box will appear.</span></span> <span data-ttu-id="1ad75-194">Tras el despido, OneNote intenta abrir el vínculo y se devuelve un error HResult.hrObjectDoesNotExist.</span><span class="sxs-lookup"><span data-stu-id="1ad75-194">Upon dismissal, OneNote attempts to open up the link and an HResult.hrObjectDoesNotExist error is returned.</span></span>  <br/> |
|<span data-ttu-id="1ad75-195">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="1ad75-195">**Syntax**</span></span> <br/> | <span data-ttu-id="1ad75-196">`HRESULT NavigateToUrl (`           ` [in]BSTR bstrUrl); `</span><span class="sxs-lookup"><span data-stu-id="1ad75-196">`HRESULT NavigateToUrl (`           ` [in]BSTR bstrUrl); `</span></span> <br/> |
|<span data-ttu-id="1ad75-197">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="1ad75-197">**Parameters**</span></span> <br/> | <span data-ttu-id="1ad75-198">_bstrUrl:_ la dirección URL a la que se va a navegar.</span><span class="sxs-lookup"><span data-stu-id="1ad75-198">_bstrUrl_—The URL to navigate to.</span></span>  <br/> |
   
<span data-ttu-id="1ad75-199">**SetDockedLocation**</span><span class="sxs-lookup"><span data-stu-id="1ad75-199">**SetDockedLocation**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ad75-200">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1ad75-200">**Description**</span></span> <br/> |<span data-ttu-id="1ad75-201">Acopla la ventana a la ubicación especificada por **dockLocation** y el monitor en **ptMonitor**.</span><span class="sxs-lookup"><span data-stu-id="1ad75-201">Docks the window to the location specified by **dockLocation** and the monitor at **ptMonitor**.</span></span>  <br/> |
|<span data-ttu-id="1ad75-202">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="1ad75-202">**Syntax**</span></span> <br/> | <span data-ttu-id="1ad75-203">`HRESULT SetDockedLocation`(           `[in] DockLocation dockLocation,`           `[in] POINT ptMonitor);`</span><span class="sxs-lookup"><span data-stu-id="1ad75-203">`HRESULT SetDockedLocation`(           `[in] DockLocation dockLocation,`           `[in] POINT ptMonitor);`</span></span> <br/> |
|<span data-ttu-id="1ad75-204">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="1ad75-204">**Parameters**</span></span> <br/> | <span data-ttu-id="1ad75-205">_dockLocation:_ indica la ubicación acoplada de una OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="1ad75-205">_dockLocation_ - Indicates the docked location of a OneNote 2013 window.</span></span>  <br/>  <span data-ttu-id="1ad75-206">_ptMonitor:_ (opcional) Indica en las coordenadas x,y a las que se debe acoplar la ventana.</span><span class="sxs-lookup"><span data-stu-id="1ad75-206">_ptMonitor_ - (Optional) Indicates in x,y co-ordinates which monitor the window should be docked to.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="1ad75-207">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1ad75-207">Example</span></span>

<span data-ttu-id="1ad75-208">El siguiente código recorre en iteración las ventanas OneNote para buscar una ventana acoplada.</span><span class="sxs-lookup"><span data-stu-id="1ad75-208">The following code iterates through the OneNote windows to find a docked window.</span></span> <span data-ttu-id="1ad75-209">Si no existe ninguna ventana acoplada, el ejemplo acopla la ventana activa.</span><span class="sxs-lookup"><span data-stu-id="1ad75-209">If no docked window exists, the example docks the active window.</span></span> <span data-ttu-id="1ad75-210">Si no existe ninguna ventana activa, el código crea una nueva ventana acoplada.</span><span class="sxs-lookup"><span data-stu-id="1ad75-210">If no active window exists, the code creates a new docked window.</span></span>
  
```cs
using System;
using System.Diagnostics;
using Microsoft.Office.Interop.OneNote;
namespace SampleWND
{
    class DockOneNoteWindow
    {
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = new Microsoft.Office.Interop.OneNote.Application();
            // Search through all OneNote windows for a docked window and activate it.
            bool foundDockedWND = false;
            for (int i = 0; i < app.Windows.Count; i++)
            {
                if (app.Windows[(uint) i].DockedLocation != DockLocation.dlNone)
                {
                    foundDockedWND = true;
                    app.Windows[(uint) i].Active = true;
                }
            }
            
            // If no docked window exists, dock the active window.
            if (!foundDockedWND && (app.Windows.Count > 0))
                app.Windows.CurrentWindow.DockedLocation = DockLocation.dlDefault;
            // If no active window exists, create a new docked window.
            if (app.Windows.Count < 1)
            {
                Process oneProc = new Process();
                oneProc.StartInfo.FileName = "onenote.exe";
                oneProc.StartInfo.Arguments = "/docked";
                oneProc.Start();
            }
        }
    }
}

```

## <a name="see-also"></a><span data-ttu-id="1ad75-211">Ver también</span><span class="sxs-lookup"><span data-stu-id="1ad75-211">See also</span></span>

- [<span data-ttu-id="1ad75-212">Referencia para desarrolladores de OneNote</span><span class="sxs-lookup"><span data-stu-id="1ad75-212">OneNote developer reference</span></span>](onenote-developer-reference.md)

