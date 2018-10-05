---
title: Interfaces de ventana (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e6900ad7-c147-4816-93a9-5773170b115a
description: Las interfaces de ventana y Windows son que objetos de OneNote 2013 API que permite a los usuarios trabajar con ventanas de OneNote. Estos objetos permiten a los usuarios enumerar a través del conjunto de ventanas de OneNote y modificar determinadas propiedades de la ventana.
ms.openlocfilehash: efc34312def588ecff54c63b3db84f8bf909352b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399952"
---
# <a name="window-interfaces-onenote"></a><span data-ttu-id="fb400-104">Interfaces de ventana (OneNote)</span><span class="sxs-lookup"><span data-stu-id="fb400-104">Window interfaces (OneNote)</span></span>

<span data-ttu-id="fb400-105">Las interfaces de **ventana** y **Windows** son que objetos de OneNote 2013 API que permite a los usuarios trabajar con ventanas de OneNote.</span><span class="sxs-lookup"><span data-stu-id="fb400-105">The **Window** and **Windows** interfaces are OneNote 2013 API objects that enables users to work with OneNote windows.</span></span> <span data-ttu-id="fb400-106">Estos objetos permiten a los usuarios enumerar a través del conjunto de ventanas de OneNote y modificar determinadas propiedades de la ventana.</span><span class="sxs-lookup"><span data-stu-id="fb400-106">These objects allow users to enumerate through the set of OneNote windows and modify certain window properties.</span></span> 
  
## <a name="onenote-window-views"></a><span data-ttu-id="fb400-107">Vistas de ventana de OneNote</span><span class="sxs-lookup"><span data-stu-id="fb400-107">OneNote window views</span></span>

<span data-ttu-id="fb400-108">En la siguiente lista se muestra los modos de cuatro vistas que pueden usar para ventanas de OneNote:</span><span class="sxs-lookup"><span data-stu-id="fb400-108">The following list shows the four view modes that you can use for OneNote windows:</span></span> 
  
- <span data-ttu-id="fb400-109">La vista normal: muestra la ventana de OneNote predeterminado en el que los paneles de navegación del Bloc de notas y página están visibles.</span><span class="sxs-lookup"><span data-stu-id="fb400-109">Normal view—Displays the default OneNote window in which the Notebook and Page navigation panes are visible.</span></span>
    
- <span data-ttu-id="fb400-110">Vista de página completa: muestra la vista de una mínimo de interfaz de usuario (UI) en que no se muestran los paneles de Bloc de notas y página.</span><span class="sxs-lookup"><span data-stu-id="fb400-110">Full Page view—Displays a minimal user-interface (UI) view in which the Notebook and Page panes are not displayed.</span></span>
    
- <span data-ttu-id="fb400-111">Nota rápida: muestra una pequeña ventana que permite a los usuarios tomar notas breves.</span><span class="sxs-lookup"><span data-stu-id="fb400-111">Quick note—Displays a small window that allows users to take short notes.</span></span> <span data-ttu-id="fb400-112">Normalmente, podría tener acceso a notas rápidas mediante el icono de OneNote en el área de notificación de Windows, pero también se pueden tener acceso a ellas a través de la ficha **Ver** en OneNote.</span><span class="sxs-lookup"><span data-stu-id="fb400-112">You would usually access quick notes through the OneNote icon in the Windows notification area, but you can also access them through the **View** tab in OneNote.</span></span> 
    
- <span data-ttu-id="fb400-113">Acople al escritorio: muestra una ventana de OneNote que se puede acoplar a cualquier lado del escritorio (similar a la barra de tareas).</span><span class="sxs-lookup"><span data-stu-id="fb400-113">Dock to Desktop—Displays a OneNote window that you can dock to any side of the desktop (similar to the taskbar).</span></span> <span data-ttu-id="fb400-114">Esta vista reduce el tamaño del escritorio para ajustarlo a la ventana.</span><span class="sxs-lookup"><span data-stu-id="fb400-114">This view reduces the size of the desktop to fit the window.</span></span> <span data-ttu-id="fb400-115">Sólo una ventana se puede acoplar en cualquier momento, y la ventana está siempre visible sin bloquear el escritorio.</span><span class="sxs-lookup"><span data-stu-id="fb400-115">You can dock only one window at any time, and the window is always visible without blocking the desktop.</span></span> 
    
<span data-ttu-id="fb400-116">La siguiente ilustración muestra qué la vista de página completa, vista del escritorio, el tránsito y notas rápidas de aspecto en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="fb400-116">The following figure shows what the Full Page view, Dock to Desktop view, and quick notes look like on your desktop.</span></span>
  
<span data-ttu-id="fb400-117">**Vistas de OneNote**</span><span class="sxs-lookup"><span data-stu-id="fb400-117">**OneNote views**</span></span>

<span data-ttu-id="fb400-118">![Vistas de la ventana de OneNote] (media/ON15Con_views.jpg "Vistas de la ventana de OneNote")</span><span class="sxs-lookup"><span data-stu-id="fb400-118">![OneNote window views](media/ON15Con_views.jpg "OneNote window views")</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="fb400-119">Interfaces</span><span class="sxs-lookup"><span data-stu-id="fb400-119">Interfaces</span></span>

<span data-ttu-id="fb400-120">En esta sección se enumera las interfaces y miembros que se pueden utilizar para modificar ventanas de OneNote mediante programación.</span><span class="sxs-lookup"><span data-stu-id="fb400-120">This section lists the interfaces and members that you can use to modify OneNote windows programmatically.</span></span>
  
### <a name="windows-interface"></a><span data-ttu-id="fb400-121">Interfaz de Windows</span><span class="sxs-lookup"><span data-stu-id="fb400-121">Windows interface</span></span>

<span data-ttu-id="fb400-122">La interfaz de **Windows** permite al usuario tener acceso al conjunto de ventanas abiertas de OneNote.</span><span class="sxs-lookup"><span data-stu-id="fb400-122">The **Windows** interface allows the user to access the set of opened OneNote windows.</span></span> <span data-ttu-id="fb400-123">Es una propiedad de la clase de **aplicación** de OneNote, tiene acceso a través de **Application.Windows**.</span><span class="sxs-lookup"><span data-stu-id="fb400-123">It is a property of the OneNote **Application** class, accessed through **Application.Windows**.</span></span> <span data-ttu-id="fb400-124">Esto devuelve el conjunto enumerado de ventanas de OneNote.</span><span class="sxs-lookup"><span data-stu-id="fb400-124">This returns the enumerated set of OneNote windows.</span></span> 
  
<span data-ttu-id="fb400-125">**Propiedades**</span><span class="sxs-lookup"><span data-stu-id="fb400-125">**Properties**</span></span>

|<span data-ttu-id="fb400-126">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="fb400-126">**Name**</span></span>|<span data-ttu-id="fb400-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fb400-127">**Type**</span></span>|<span data-ttu-id="fb400-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fb400-128">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fb400-129">**Count**</span><span class="sxs-lookup"><span data-stu-id="fb400-129">**Count**</span></span> <br/> |<span data-ttu-id="fb400-130">ulong</span><span class="sxs-lookup"><span data-stu-id="fb400-130">ulong</span></span>  <br/> |<span data-ttu-id="fb400-131">Obtiene el número de objetos de **ventana** en el conjunto de **Windows** .</span><span class="sxs-lookup"><span data-stu-id="fb400-131">Gets the number of **Window** objects in the **Windows** set.</span></span>  <br/> |
|<span data-ttu-id="fb400-132">**CurrentWindow**</span><span class="sxs-lookup"><span data-stu-id="fb400-132">**CurrentWindow**</span></span> <br/> |<span data-ttu-id="fb400-133">**Window**</span><span class="sxs-lookup"><span data-stu-id="fb400-133">**Window**</span></span> <br/> |<span data-ttu-id="fb400-134">Obtiene el objeto de **ventana** de la ventana activa de OneNote.</span><span class="sxs-lookup"><span data-stu-id="fb400-134">Gets the **Window** object of the active OneNote window.</span></span>  <br/> |
|<span data-ttu-id="fb400-135">**Items**</span><span class="sxs-lookup"><span data-stu-id="fb400-135">**Items**</span></span> <br/> |<span data-ttu-id="fb400-136">**Window**</span><span class="sxs-lookup"><span data-stu-id="fb400-136">**Window**</span></span> <br/> |<span data-ttu-id="fb400-137">Devuelve el objeto de **ventana** que corresponde al valor de índice que se pasa.</span><span class="sxs-lookup"><span data-stu-id="fb400-137">Returns the **Window** object that corresponds to the index value passed.</span></span> <span data-ttu-id="fb400-138">Esta propiedad no se puede tener acceso directamente.</span><span class="sxs-lookup"><span data-stu-id="fb400-138">This property cannot be accessed directly.</span></span> <span data-ttu-id="fb400-139">Para devolver un objeto **Window** , use **Windows [(uint) índice]**.</span><span class="sxs-lookup"><span data-stu-id="fb400-139">To return a **Window** object, use **Windows [(uint) index]**.</span></span>  <br/> |
   
### <a name="window-interface"></a><span data-ttu-id="fb400-140">Interfaz de ventana</span><span class="sxs-lookup"><span data-stu-id="fb400-140">Window interface</span></span>

<span data-ttu-id="fb400-141">La interfaz de **ventana** permite al usuario tener acceso a determinadas propiedades de cada ventana.</span><span class="sxs-lookup"><span data-stu-id="fb400-141">The **Window** interface allows the user to access certain properties of each window.</span></span> <span data-ttu-id="fb400-142">Para obtener acceso a cada ventana de OneNote enumerar a través de la propiedad de **Windows** de la clase de **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="fb400-142">Each OneNote window can be accessed by enumerating through the **Windows** property of the **Application** class.</span></span> 
  
<span data-ttu-id="fb400-143">**Propiedades**</span><span class="sxs-lookup"><span data-stu-id="fb400-143">**Properties**</span></span>

|<span data-ttu-id="fb400-144">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="fb400-144">**Name**</span></span>|<span data-ttu-id="fb400-145">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fb400-145">**Type**</span></span>|<span data-ttu-id="fb400-146">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fb400-146">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fb400-147">**Active**</span><span class="sxs-lookup"><span data-stu-id="fb400-147">**Active**</span></span> <br/> |<span data-ttu-id="fb400-148">bool</span><span class="sxs-lookup"><span data-stu-id="fb400-148">bool</span></span>  <br/> |<span data-ttu-id="fb400-149">Obtiene o establece un valor que indica si la ventana es la ventana activa de OneNote.</span><span class="sxs-lookup"><span data-stu-id="fb400-149">Gets or sets a value that indicates whether the window is the active OneNote window.</span></span>  <br/> |
|<span data-ttu-id="fb400-150">**Application**</span><span class="sxs-lookup"><span data-stu-id="fb400-150">**Application**</span></span> <br/> |<span data-ttu-id="fb400-151">**Application**</span><span class="sxs-lookup"><span data-stu-id="fb400-151">**Application**</span></span> <br/> |<span data-ttu-id="fb400-152">Obtiene el objeto de **aplicación** de OneNote que está asociado a la ventana.</span><span class="sxs-lookup"><span data-stu-id="fb400-152">Gets the OneNote **Application** object that is associated with the window.</span></span>  <br/> |
|<span data-ttu-id="fb400-153">**CurrentPageId**</span><span class="sxs-lookup"><span data-stu-id="fb400-153">**CurrentPageId**</span></span> <br/> |<span data-ttu-id="fb400-154">string</span><span class="sxs-lookup"><span data-stu-id="fb400-154">string</span></span>  <br/> |<span data-ttu-id="fb400-155">Obtiene el identificador del objeto de la página activa de OneNote de la ventana.</span><span class="sxs-lookup"><span data-stu-id="fb400-155">Gets the object ID of the active OneNote page of the window.</span></span>  <br/> |
|<span data-ttu-id="fb400-156">**CurrentSectionId**</span><span class="sxs-lookup"><span data-stu-id="fb400-156">**CurrentSectionId**</span></span> <br/> |<span data-ttu-id="fb400-157">string</span><span class="sxs-lookup"><span data-stu-id="fb400-157">string</span></span>  <br/> |<span data-ttu-id="fb400-158">Obtiene el identificador del objeto de la sección activa de OneNote de la ventana.</span><span class="sxs-lookup"><span data-stu-id="fb400-158">Gets the object ID of the active OneNote section of the window.</span></span>  <br/> |
|<span data-ttu-id="fb400-159">**CurrentSectionGroupId**</span><span class="sxs-lookup"><span data-stu-id="fb400-159">**CurrentSectionGroupId**</span></span> <br/> |<span data-ttu-id="fb400-160">string</span><span class="sxs-lookup"><span data-stu-id="fb400-160">string</span></span>  <br/> |<span data-ttu-id="fb400-161">Obtiene el identificador de objeto del grupo de sección de OneNote activo de la ventana.</span><span class="sxs-lookup"><span data-stu-id="fb400-161">Gets the object ID of the active OneNote section group of the window.</span></span>  <br/> |
|<span data-ttu-id="fb400-162">**CurrentNotebookId**</span><span class="sxs-lookup"><span data-stu-id="fb400-162">**CurrentNotebookId**</span></span> <br/> |<span data-ttu-id="fb400-163">string</span><span class="sxs-lookup"><span data-stu-id="fb400-163">string</span></span>  <br/> |<span data-ttu-id="fb400-164">Obtiene el identificador de objeto del Bloc de notas de OneNote activo de la ventana.</span><span class="sxs-lookup"><span data-stu-id="fb400-164">Gets the object ID of the active OneNote notebook of the window.</span></span>  <br/> |
|<span data-ttu-id="fb400-165">**DockedLocation**</span><span class="sxs-lookup"><span data-stu-id="fb400-165">**DockedLocation**</span></span> <br/> |<span data-ttu-id="fb400-166">**DockedLocation**</span><span class="sxs-lookup"><span data-stu-id="fb400-166">**DockedLocation**</span></span> <br/> |<span data-ttu-id="fb400-167">Obtiene o establece la ubicación acoplada de la ventana de OneNote.</span><span class="sxs-lookup"><span data-stu-id="fb400-167">Gets or sets the docked location of the OneNote window.</span></span>  <br/> |
|<span data-ttu-id="fb400-168">**FullPageView**</span><span class="sxs-lookup"><span data-stu-id="fb400-168">**FullPageView**</span></span> <br/> |<span data-ttu-id="fb400-169">bool</span><span class="sxs-lookup"><span data-stu-id="fb400-169">bool</span></span>  <br/> |<span data-ttu-id="fb400-170">Obtiene o establece un valor que indica si la ventana está en vista de página completa (vista mínima de la interfaz de usuario).</span><span class="sxs-lookup"><span data-stu-id="fb400-170">Gets or sets a value that indicates whether the window is in Full Page view (minimal UI view).</span></span>  <br/> |
|<span data-ttu-id="fb400-171">**Nota al margen**</span><span class="sxs-lookup"><span data-stu-id="fb400-171">**SideNote**</span></span> <br/> |<span data-ttu-id="fb400-172">bool</span><span class="sxs-lookup"><span data-stu-id="fb400-172">bool</span></span>  <br/> |<span data-ttu-id="fb400-173">Obtiene o establece un valor que indica si la ventana es una ventana de nota rápida.</span><span class="sxs-lookup"><span data-stu-id="fb400-173">Gets or sets a value that indicates whether the window is a quick note window.</span></span>  <br/> |
|<span data-ttu-id="fb400-174">**WindowHandle**</span><span class="sxs-lookup"><span data-stu-id="fb400-174">**WindowHandle**</span></span> <br/> |<span data-ttu-id="fb400-175">ulong</span><span class="sxs-lookup"><span data-stu-id="fb400-175">ulong</span></span>  <br/> |<span data-ttu-id="fb400-176">Obtiene el identificador del controlador de la ventana de OneNote.</span><span class="sxs-lookup"><span data-stu-id="fb400-176">Gets the handle ID of the OneNote window.</span></span>  <br/> |
   
<span data-ttu-id="fb400-177">**Métodos**</span><span class="sxs-lookup"><span data-stu-id="fb400-177">**Methods**</span></span>
  
<span data-ttu-id="fb400-178">Puede usar los siguientes métodos de la interfaz de **ventana** para navegar a los objetos especificados en la ventana de OneNote o a las direcciones URL especificadas.</span><span class="sxs-lookup"><span data-stu-id="fb400-178">You can use the following methods of the **Window** interface to navigate to specified objects in the OneNote window or to specified URLs.</span></span> 
  
<span data-ttu-id="fb400-179">**NavigateTo**</span><span class="sxs-lookup"><span data-stu-id="fb400-179">**NavigateTo**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fb400-180">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fb400-180">**Description**</span></span> <br/> |<span data-ttu-id="fb400-181">Se desplaza al objeto especificado en la ventana de OneNote.</span><span class="sxs-lookup"><span data-stu-id="fb400-181">Navigates to the specified object in the OneNote window.</span></span> <span data-ttu-id="fb400-182">Por ejemplo, puede navegar a secciones, páginas y elementos de esquema dentro de las páginas.</span><span class="sxs-lookup"><span data-stu-id="fb400-182">For example, you can navigate to sections, pages, and outline elements within pages.</span></span>  <br/> |
|<span data-ttu-id="fb400-183">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="fb400-183">**Syntax**</span></span> <br/> | <span data-ttu-id="fb400-184">`HRESULT NavigateTo(`           ` [in]BSTR bstrHierarchyObjectID, `           ` [in]BSTR bstrObjectID); `</span><span class="sxs-lookup"><span data-stu-id="fb400-184"></span></span> <br/> |
|<span data-ttu-id="fb400-185">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="fb400-185">**Parameters**</span></span> <br/> | <span data-ttu-id="fb400-186">_bstrHierarchyObjectID_: la jerarquía de OneNote identificador del objeto que va a explorar a.</span><span class="sxs-lookup"><span data-stu-id="fb400-186">_bstrHierarchyObjectID_—The hierarchy OneNote ID of the object you want to navigate to.</span></span> <span data-ttu-id="fb400-187">El identificador de objeto puede hacer referencia a un bloc de notas de OneNote, sección, grupo de sección o página.</span><span class="sxs-lookup"><span data-stu-id="fb400-187">The object ID can reference a OneNote notebook, section, section group, or page.</span></span>  <br/>  <span data-ttu-id="fb400-188">_bstrObjectID_: el identificador de OneNote del objeto específico al que navegar dentro de una página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="fb400-188">_bstrObjectID_—The OneNote ID of the specific object to navigate to within a OneNote page.</span></span> <span data-ttu-id="fb400-189">Si no desea que el usuario navegar a un objeto específico en una página, este parámetro se establece en null.</span><span class="sxs-lookup"><span data-stu-id="fb400-189">If the user does not want to navigate to a specific object on a page, this parameter is set to null.</span></span>  <br/> |
   
<span data-ttu-id="fb400-190">**NavigateToUrl**</span><span class="sxs-lookup"><span data-stu-id="fb400-190">**NavigateToUrl**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fb400-191">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fb400-191">**Description**</span></span> <br/> |<span data-ttu-id="fb400-192">Si pasa un vínculo de OneNote (onenote: / /), se abre la ventana de OneNote a la ubicación correspondiente en OneNote.</span><span class="sxs-lookup"><span data-stu-id="fb400-192">If passed a OneNote link (onenote://), opens the OneNote window to the corresponding location in OneNote.</span></span> <span data-ttu-id="fb400-193">Sin embargo, si el vínculo es un vínculo externo, por ejemplo, https:// o file://, aparecerá un cuadro de diálogo de seguridad.</span><span class="sxs-lookup"><span data-stu-id="fb400-193">However, if the link is an external link, such as https:// or file://, a security dialog box will appear.</span></span> <span data-ttu-id="fb400-194">Tras despido, OneNote intenta abrir el vínculo y se devuelve un error de HResult.hrObjectDoesNotExist.</span><span class="sxs-lookup"><span data-stu-id="fb400-194">Upon dismissal, OneNote attempts to open up the link and an HResult.hrObjectDoesNotExist error is returned.</span></span>  <br/> |
|<span data-ttu-id="fb400-195">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="fb400-195">**Syntax**</span></span> <br/> | <span data-ttu-id="fb400-196">`HRESULT NavigateToUrl (`           ` [in]BSTR bstrUrl); `</span><span class="sxs-lookup"><span data-stu-id="fb400-196"></span></span> <br/> |
|<span data-ttu-id="fb400-197">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="fb400-197">**Parameters**</span></span> <br/> | <span data-ttu-id="fb400-198">_bstrUrl_: la dirección URL de destino.</span><span class="sxs-lookup"><span data-stu-id="fb400-198">_bstrUrl_—The URL to navigate to.</span></span>  <br/> |
   
<span data-ttu-id="fb400-199">**SetDockedLocation**</span><span class="sxs-lookup"><span data-stu-id="fb400-199">**SetDockedLocation**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fb400-200">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fb400-200">**Description**</span></span> <br/> |<span data-ttu-id="fb400-201">La ventana se acopla a la ubicación especificada por el monitor en **ptMonitor**y **dockLocation** .</span><span class="sxs-lookup"><span data-stu-id="fb400-201">Docks the window to the location specified by **dockLocation** and the monitor at **ptMonitor**.</span></span>  <br/> |
|<span data-ttu-id="fb400-202">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="fb400-202">**Syntax**</span></span> <br/> | <span data-ttu-id="fb400-203">`HRESULT SetDockedLocation`(           `[in] DockLocation dockLocation,`           `[in] POINT ptMonitor);`</span><span class="sxs-lookup"><span data-stu-id="fb400-203"></span></span> <br/> |
|<span data-ttu-id="fb400-204">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="fb400-204">**Parameters**</span></span> <br/> | <span data-ttu-id="fb400-205">_dockLocation_ - indica la ubicación de una ventana de OneNote 2013 acoplada.</span><span class="sxs-lookup"><span data-stu-id="fb400-205">_dockLocation_ - Indicates the docked location of a OneNote 2013 window.</span></span>  <br/>  <span data-ttu-id="fb400-206">_ptMonitor_ - indica (opcional) en x, y de coordenadas que supervisar la ventana debe se puede acoplar a.</span><span class="sxs-lookup"><span data-stu-id="fb400-206">_ptMonitor_ - (Optional) Indicates in x,y co-ordinates which monitor the window should be docked to.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="fb400-207">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fb400-207">Example</span></span>

<span data-ttu-id="fb400-208">El siguiente código recorre en iteración las ventanas de OneNote para buscar una ventana acoplada.</span><span class="sxs-lookup"><span data-stu-id="fb400-208">The following code iterates through the OneNote windows to find a docked window.</span></span> <span data-ttu-id="fb400-209">Si no existe ninguna ventana acoplada, en el ejemplo se acopla a la ventana activa.</span><span class="sxs-lookup"><span data-stu-id="fb400-209">If no docked window exists, the example docks the active window.</span></span> <span data-ttu-id="fb400-210">Si no existe ninguna ventana activa, el código crea una nueva ventana acoplada.</span><span class="sxs-lookup"><span data-stu-id="fb400-210">If no active window exists, the code creates a new docked window.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="fb400-211">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb400-211">See also</span></span>

- [<span data-ttu-id="fb400-212">Referencia para desarrolladores de OneNote</span><span class="sxs-lookup"><span data-stu-id="fb400-212">OneNote developer reference</span></span>](onenote-developer-reference.md)

